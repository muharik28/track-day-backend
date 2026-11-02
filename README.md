# Project-Structure

    track-day-backend/
    │
    ├── openspec/
    │   ├── specs/
    │   │   ├── authentication/
    │   │   │   └── spec.md
    │   │   │
    │   │   ├── user-management/
    │   │   │   └── spec.md
    │   │   │
    │   │   ├── role-permission/
    │   │   │   └── spec.md
    │   │   │
    │   │   └── transaction/
    │   │       └── spec.md
    │   │
    │   ├── changes/
    │   │   ├── add-user-authentication/
    │   │   │   ├── proposal.md
    │   │   │   ├── specs/
    │   │   │   │   └── authentication/
    │   │   │   │       └── spec.md
    │   │   │   ├── design.md
    │   │   │   └── tasks.md
    │   │   │
    │   │   ├── add-role-permission/
    │   │   │   ├── proposal.md
    │   │   │   ├── specs/
    │   │   │   │   └── role-permission/
    │   │   │   │       └── spec.md
    │   │   │   ├── design.md
    │   │   │   └── tasks.md
    │   │   │
    │   │   └── archive/
    │   │
    │   └── config.yaml
    │
    ├── cmd/
    │   └── api/
    │       └── main.go
    │
    ├── build/                      # Build-related files
    │   └── package/                # Package-related files
    │       └── Dockerfile          # Dockerfile for building the application
    │
    ├── cmd/                        # Contains main applications
    │   ├── rest/                   # REST application
    │   |   ├── rest.go             # Entry point Cobra Command for REST app
    │   |   └── scheduler/          # Scheduler for tasks
    |   |       └── scheduler.go    # Entry point Cobra Command for scheduler
    |   |
    |   └── root.go                 # Entry point for the root Cobra Command
    |
    ├── internal/
    │   ├── domain/
    │   │   ├── user/
    │   │   │   ├── entity.go
    │   │   │   ├── repository.go
    │   │   │   └── errors.go
    │   │   │
    │   │   ├── auth/
    │   │   │   ├── entity.go
    │   │   │   └── repository.go
    │   │   │
    │   │   └── transaction/
    │   │       ├── entity.go
    │   │       └── repository.go
    │   │
    │   ├── application/
    │   │   ├── user/
    │   │   │   ├── create_user.go
    │   │   │   ├── get_user.go
    │   │   │   └── create_user_test.go
    │   │   │
    │   │   ├── auth/
    │   │   │   ├── login.go
    │   │   │   ├── register.go
    │   │   │   └── refresh_token.go
    │   │   │
    │   │   └── transaction/
    │   │       └── create_transaction.go
    │   │
    │   ├── infrastructure/
    │   │   ├── database/
    │   │   │   └── postgres.go
    │   │   │
    │   │   ├── cache/
    │   │   │   └── redis.go
    │   │   │
    │   │   ├── logger/
    │   │   │   └── logger.go
    │   │   │
    │   │   └── config/
    │   │       └── config.go
    │   │
    │   ├── adapters/
    │   │   ├── http/
    │   │   │   ├── handlers/
    │   │   │   │   ├── user_handler.go
    │   │   │   │   └── auth_handler.go
    │   │   │   │
    │   │   │   ├── middleware/
    │   │   │   │   └── auth_middleware.go
    │   │   │   │
    │   │   │   ├── requests/
    │   │   │   │   └── user_request.go
    │   │   │   │
    │   │   │   ├── responses/
    │   │   │   │   └── user_response.go
    │   │   │   │
    │   │   │   └── router.go
    │   │   │
    │   │   └── persistence/
    │   │       ├── user_repository.go
    │   │       └── transaction_repository.go
    │   │
    │   └── bootstrap/
    │       └── app.go
    │
    ├── migrations/
    │   ├── 001_create_users_table.up.sql
    │   └── 001_create_users_table.down.sql
    │
    ├── api/
    │   └── openapi.yaml
    │
    ├── tests/
    │   └── integration/
    │       └── user_test.go
    │
    ├── deployments/
    │   └── docker/
    │       └── Dockerfile
    │
    ├── docs/
    │   ├── architecture.md
    │   └── deployment.md
    │
    ├── .env.example
    ├── .gitignore
    ├── docker-compose.yml
    ├── Makefile
    ├── go.mod
    ├── go.sum
    └── README.md