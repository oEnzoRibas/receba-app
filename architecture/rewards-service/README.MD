# Rewards Service Documentation

## Responsibilities

- Calculates XP, coins, badges, and achievements
- Processes completed goal events (`goal_completed`)
- Updates user history in the User Service
- Integrates with Notification Service for reward alerts

## Suggested Stack

- **Node.js + NestJS**
- **Database:** PostgreSQL
- **Extras:** Redis for caching balances and rewards

## Endpoints

- `@GET /rewards/user/:userId` - Returns user's XP, coins, and badges
- `@POST /rewards/calculate` - Processes `goal_completed` event and updates rewards
