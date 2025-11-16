# API Design: Patterns & Best Practices

This guide helps you design APIs for your product, whether REST, GraphQL, or other approaches.

---

## API Paradigms

### Option 1: REST (REpresentational State Transfer)

**Best for:** Standard CRUD apps, simple APIs, traditional backends

**Description:**
REST uses HTTP methods and follows resource-based URLs. Most common API style.

**HTTP Methods:**
- `GET` — Retrieve data
- `POST` — Create new resource
- `PUT` — Update entire resource
- `PATCH` — Update partial resource
- `DELETE` — Remove resource

**Pros:**
- Widely understood
- Cacheable (HTTP caching)
- Stateless
- Good for CRUD operations
- Works with any HTTP client

**Cons:**
- Over-fetching (gets more data than needed)
- Under-fetching (multiple requests needed)
- No type safety by default
- Versioning can be complex

---

### Example: REST API for Task Manager

**Base URL:** `https://api.taskly.com/v1`

#### Endpoints:

**Get all tasks:**
```http
GET /tasks
GET /tasks?status=completed
GET /tasks?sort=dueDate&order=asc
```

**Response:**
```json
{
  "data": [
    {
      "id": "task_123",
      "title": "Write API docs",
      "status": "in_progress",
      "dueDate": "2024-01-20",
      "userId": "user_456"
    }
  ],
  "meta": {
    "total": 42,
    "page": 1,
    "perPage": 20
  }
}
```

**Get single task:**
```http
GET /tasks/task_123
```

**Create task:**
```http
POST /tasks
Content-Type: application/json

{
  "title": "New task",
  "description": "Task description",
  "dueDate": "2024-01-25",
  "status": "todo"
}
```

**Update task:**
```http
PATCH /tasks/task_123

{
  "status": "completed"
}
```

**Delete task:**
```http
DELETE /tasks/task_123
```

**Nested resources:**
```http
GET /users/user_456/tasks
GET /projects/proj_789/tasks
```

---

### REST Best Practices

**1. Use Nouns, Not Verbs**
```
✅ GET /tasks
✅ POST /tasks
❌ GET /getTasks
❌ POST /createTask
```

**2. Use Plural Nouns**
```
✅ /tasks
❌ /task
```

**3. HTTP Status Codes**
```
200 OK — Successful GET, PATCH, PUT
201 Created — Successful POST
204 No Content — Successful DELETE
400 Bad Request — Invalid input
401 Unauthorized — Not authenticated
403 Forbidden — Not authorized
404 Not Found — Resource doesn't exist
500 Internal Server Error — Server error
```

**4. Versioning**
```
Option 1: URL versioning
GET /v1/tasks

Option 2: Header versioning
GET /tasks
Accept: application/vnd.taskly.v1+json
```

**5. Pagination**
```http
GET /tasks?page=2&perPage=20

Response:
{
  "data": [...],
  "meta": {
    "page": 2,
    "perPage": 20,
    "total": 142,
    "totalPages": 8
  }
}
```

**6. Filtering & Sorting**
```http
GET /tasks?status=completed&sort=dueDate&order=desc
GET /tasks?userId=user_456&priority=high
```

**7. Error Format**
```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid input",
    "details": [
      {
        "field": "title",
        "message": "Title is required"
      }
    ]
  }
}
```

---

## Option 2: GraphQL

**Best for:** Complex data relationships, mobile apps, flexible querying

**Description:**
GraphQL lets clients specify exactly what data they need. Single endpoint.

**Pros:**
- No over-fetching (request only needed fields)
- No under-fetching (get related data in one request)
- Strong typing (schema)
- Great developer experience
- Real-time with subscriptions

**Cons:**
- More complex setup
- Caching is harder
- Learning curve
- Can expose too much data if not secured

---

### Example: GraphQL API for Task Manager

**Endpoint:** `https://api.taskly.com/graphql`

#### Schema:

```graphql
type Task {
  id: ID!
  title: String!
  description: String
  status: TaskStatus!
  dueDate: String
  priority: Priority!
  user: User!
  project: Project
  createdAt: String!
  updatedAt: String!
}

type User {
  id: ID!
  name: String!
  email: String!
  tasks: [Task!]!
}

type Project {
  id: ID!
  name: String!
  tasks: [Task!]!
}

enum TaskStatus {
  TODO
  IN_PROGRESS
  COMPLETED
}

enum Priority {
  LOW
  MEDIUM
  HIGH
}

type Query {
  tasks(status: TaskStatus, limit: Int): [Task!]!
  task(id: ID!): Task
  user(id: ID!): User
}

type Mutation {
  createTask(input: CreateTaskInput!): Task!
  updateTask(id: ID!, input: UpdateTaskInput!): Task!
  deleteTask(id: ID!): Boolean!
}

input CreateTaskInput {
  title: String!
  description: String
  dueDate: String
  priority: Priority
  projectId: ID
}

input UpdateTaskInput {
  title: String
  status: TaskStatus
  priority: Priority
}
```

#### Example Queries:

**Get tasks with user info:**
```graphql
query GetTasks {
  tasks(status: IN_PROGRESS) {
    id
    title
    dueDate
    user {
      name
      email
    }
  }
}
```

**Get single task with nested data:**
```graphql
query GetTask {
  task(id: "task_123") {
    id
    title
    status
    user {
      name
    }
    project {
      name
      tasks {
        id
        title
      }
    }
  }
}
```

**Create task:**
```graphql
mutation CreateTask {
  createTask(input: {
    title: "New task"
    description: "Task description"
    priority: HIGH
  }) {
    id
    title
    createdAt
  }
}
```

**Update task:**
```graphql
mutation UpdateTask {
  updateTask(id: "task_123", input: {
    status: COMPLETED
  }) {
    id
    status
    updatedAt
  }
}
```

---

## Option 3: tRPC (TypeScript RPC)

**Best for:** Full-stack TypeScript apps, type safety

**Description:**
End-to-end type safety without code generation. Only works with TypeScript.

**Pros:**
- Full type safety
- No code generation
- Great developer experience
- Autocomplete everywhere
- Shared types between client/server

**Cons:**
- TypeScript only
- Less known
- Smaller ecosystem

**Example:**
```typescript
// Server
import { initTRPC } from '@trpc/server';

const t = initTRPC.create();

export const appRouter = t.router({
  getTasks: t.procedure.query(async () => {
    return db.task.findMany();
  }),
  createTask: t.procedure
    .input(z.object({ title: z.string() }))
    .mutation(async ({ input }) => {
      return db.task.create({ data: input });
    }),
});

// Client (full type safety!)
const tasks = await trpc.getTasks.query();
```

---

## Option 4: WebSockets / Real-time

**Best for:** Chat apps, live updates, collaborative editing

**Description:**
Bidirectional, persistent connection between client and server.

**Use Cases:**
- Chat messages
- Live notifications
- Real-time collaboration
- Live dashboards

**Example (Socket.io):**
```javascript
// Server
io.on('connection', (socket) => {
  socket.on('message', (data) => {
    io.emit('message', data); // Broadcast to all
  });
});

// Client
socket.emit('message', { text: 'Hello!' });
socket.on('message', (data) => {
  console.log(data);
});
```

---

## API Authentication

### Option 1: API Keys

**Simple, server-to-server.**

```http
GET /tasks
Authorization: Bearer sk_live_abc123xyz
```

**Pros:** Simple
**Cons:** Less secure, no user context

---

### Option 2: JWT (JSON Web Tokens)

**Most common for user authentication.**

**Flow:**
1. User logs in
2. Server returns JWT token
3. Client stores token
4. Client sends token with each request

```http
GET /tasks
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

**Token Structure:**
```json
{
  "sub": "user_123",
  "email": "user@example.com",
  "exp": 1705843200
}
```

**Pros:** Stateless, scalable
**Cons:** Can't revoke easily, token size

---

### Option 3: OAuth 2.0

**For third-party access (e.g., "Login with Google").**

**Pros:** Industry standard, secure
**Cons:** Complex setup

---

## Rate Limiting

**Prevent API abuse.**

**Headers:**
```http
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 73
X-RateLimit-Reset: 1705843200
```

**Response (429 Too Many Requests):**
```json
{
  "error": {
    "code": "RATE_LIMIT_EXCEEDED",
    "message": "Too many requests. Try again in 60 seconds.",
    "retryAfter": 60
  }
}
```

**Common Limits:**
- Free tier: 100 requests/hour
- Pro tier: 1000 requests/hour
- Enterprise: Unlimited

---

## API Documentation

### Option 1: OpenAPI (Swagger)

**Standard for REST APIs.**

```yaml
openapi: 3.0.0
info:
  title: Taskly API
  version: 1.0.0
paths:
  /tasks:
    get:
      summary: Get all tasks
      responses:
        '200':
          description: Success
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Task'
```

**Tools:**
- Swagger UI: https://swagger.io/tools/swagger-ui/
- Redoc: https://redocly.com

---

### Option 2: GraphQL Playground

**Built-in for GraphQL.**

Includes:
- Interactive query editor
- Schema explorer
- Autocomplete

**Tools:**
- Apollo Studio
- GraphQL Playground

---

## API Versioning Strategies

### 1. URL Versioning (Most Common)
```
/v1/tasks
/v2/tasks
```

**Pros:** Clear, easy to route
**Cons:** Duplicate code

---

### 2. Header Versioning
```http
GET /tasks
Accept: application/vnd.taskly.v1+json
```

**Pros:** Clean URLs
**Cons:** Less visible

---

### 3. Query Parameter
```
/tasks?version=1
```

**Pros:** Flexible
**Cons:** Can be messy

---

## Error Handling Best Practices

**1. Use Proper Status Codes**

**2. Consistent Error Format**
```json
{
  "error": {
    "code": "ERROR_CODE",
    "message": "Human-readable message",
    "details": []
  }
}
```

**3. Provide Helpful Messages**
```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Title must be at least 3 characters"
  }
}
```

---

## Testing APIs

**Tools:**
- **Postman** — API testing
- **Insomnia** — REST/GraphQL client
- **Hoppscotch** — Open-source API client
- **curl** — Command-line testing

**Example (curl):**
```bash
curl -X POST https://api.taskly.com/v1/tasks \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer token" \
  -d '{"title": "New task"}'
```

---

## Decision Guide

| **Your Need** | **Recommended API Type** |
|---|---|
| Simple CRUD app | REST |
| Complex data relationships | GraphQL |
| Full-stack TypeScript | tRPC |
| Real-time updates | WebSockets |
| Public API | REST with OpenAPI docs |
| Mobile app (reduce bandwidth) | GraphQL |
| Microservices | REST or gRPC |

---

## Resources

- **REST Best Practices:** https://restfulapi.net
- **GraphQL Docs:** https://graphql.org
- **tRPC:** https://trpc.io
- **OpenAPI Spec:** https://swagger.io/specification/
- **API Security:** https://owasp.org/www-project-api-security/
