# User Service Documentation

## Responsibilities

- Manage user profile (name, photo, preferences)
- Progress history: completed goals, XP, coins
- Friend and group management (for collaborative goals)
- Manual progress updates (offline synchronization)

## Suggested Stack

- **Node.js + NestJS**
- **Database:** PostgreSQL
- **Extras:** ORM like Prisma or TypeORM

## Endpoints

- `@GET /users/:id/profile` - Returns user profile
- `@PUT /users/:id/profile` - Updates user profile
- `@GET /users/:id/progress` - Returns overall progress: goals, XP, coins
- `@POST /users/:id/progress` - Updates progress manually
- `@GET /users/:id/friends` - Lists friends or group users
