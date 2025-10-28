# Store Service Documentation

## Responsibilities

- CRUD for items created by users (e.g., "Eat ice cream", "Take a day off")
- Purchase/redeem items using user coins
- Purchase and redemption history
- Integration with Rewards Service and User Service for balance and XP
- Integration with Notification Service for purchase alerts or promotions

## Suggested Stack

- **Node.js + NestJS**
- **Database:** PostgreSQL
- **Extras:** Optional Redis for caching popular items

## Endpoints

- `@POST /store/items` - Create item by user
- `@GET /store/items/:itemId` - Get item details
- `@PUT /store/items/:itemId` - Update user-created item
- `@DELETE /store/items/:itemId` - Delete user-created item
- `@GET /store/user/:userId/items` - List all items of the user
- `@POST /store/purchase` - Purchase/redeem item using coins
- `@GET /store/user/:userId/purchases` - Get user's purchase/redemption history
