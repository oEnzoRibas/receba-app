# Auth Service Documentation

## Responsibilities

- Login via OAuth (Google, Apple, GitHub).
- Issuing and validating JWT tokens.
- Session management.

## Suggested Stack

- **Node.js + NestJS** (modular and scalable)
- **Database:** PostgreSQL (users and tokens)
- **Extras:** passport.js or @nestjs/passport for OAuth; optional Redis for session caching

## Endpoints

- `@POST /auth/login/oauth` - Login via OAuth, returns JWT
- `@POST /auth/refresh-token` - Refresh expired token using refresh token
- `@POST /auth/logout` - Ends user session
- `@GET /auth/validate` - Validates JWT and returns user data
