# Notification Service Documentation

## Responsibilities

- Send push and in-app notifications
- Remind about pending goals, completed goals, rewards, and promotions
- Receive internal events from Goals, Rewards, and Store
- Not called directly by the client

## Suggested Stack

- **Node.js + NestJS**
- **Extras:** Firebase Cloud Messaging (FCM) for mobile, Web push for future web, asynchronous messaging (RabbitMQ/Kafka/NATS) for events

## Received Events

- `goal_completed` - Notifies XP/coins/badges earned
- `purchase_completed` - Notifies purchase completed
- `meta_due` - Reminder of pending goal
- `promotion` - Notifies promotions of items in the store