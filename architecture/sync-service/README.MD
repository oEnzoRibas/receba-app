# Sync Service Documentation

## Responsibilities

- Receive offline action queue from client
- Process actions by calling corresponding services (Goals, Store, Rewards, User)
- Resolve synchronization conflicts
- Return updated state to client

## Suggested Stack

- **Node.js + NestJS**
- **Database:** PostgreSQL (optional) or just temporary queue
- **Extras:** Asynchronous messaging to decouple processing

## Endpoints

- `@POST /sync/actions` - Send offline action queue for processing
- `@GET /sync/status/:userId` - Check status of pending/processed actions
- `@GET /sync/last-update/:userId` - Timestamp of last successful synchronization
