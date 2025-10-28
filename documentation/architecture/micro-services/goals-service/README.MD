# Goals Service Documentation

## Responsibilities

- CRUD for individual and collaborative goals
- Offline-first support: pending actions queue
- Triggers goal completed events for Rewards Service
- Integration with Notification Service for alerts

## Suggested Stack

- **Node.js + NestJS**
- **Database:** PostgreSQL
- **Extras:** Sync queue (RabbitMQ, Kafka, or NATS)

## Endpoints

- `@POST /goals` - Creates a new goal (with XP/coins defined by the user)
- `@GET /goals/:id` - Returns details of a goal
- `@PUT /goals/:id` - Updates a goal (status, XP, coins, description, deadline)
- `@DELETE /goals/:id` - Removes a goal
- `@GET /goals/user/:userId` - Lists all goals for a user
- `@GET /goals/group/:groupId` - Lists collaborative goals for a group
- `@POST /goals/sync` - Syncs the queue of pending offline actions
