#  Base Go Fiber Application 

This repository contains a Go application structured using the Go Fiber web framework. The structure follows best practices for a clean and maintainable codebase.

## Folder Structure

```
├── .gitignore
├── README.md
├── cmd
│   └── main.go
├── internal
│   ├── api
│   │   ├── handlers
│   │   │   ├── handlers.go
│   │   │   └── user_handler.go
│   │   ├── middleware
│   │   │   └── middleware.go
│   │   ├── models
│   │   │   └── user.go
│   │   ├── routes
│   │   │   ├── routes.go
│   │   ├── api.go
│   ├── config
│   │   └── config.go
│   ├── customerrors
│   │   └── errors.go
│   ├── db
│   │   ├── migrations
│   │   │   ├── m.sql
│   │   ├── repositories
│   │   │   └── repository.go
│   │   └── db.go
│   ├── logger
│   │   └── logger.go
│   └── utils
│       └── json.go
├── scripts
│   └── Makefile
└── tests
    └── main_test.go
```

### Description of Directories and Files

- **cmd**: Contains the entry point for the application.
  - `main.go`: The main file that starts the application.

- **internal**: Contains application-specific code and packages.
  - **api**: Contains the API-related logic.
    - **handlers**: Contains the request handlers.
      - `handlers.go`: General handlers for the API.
      - `user_handler.go`: Handlers specific to user-related endpoints.
    - **middleware**: Middleware for the API.
      - `middleware.go`: General middleware functions.
    - **models**: Contains the data models.
      - `user.go`: User data model.
    - **routes**: Contains the routing logic.
      - `routes.go`: General routes for the API.
    - `api.go`: API-specific routes.

  - **config**: Configuration files for the application.
    - `config.go`: Configuration setup and management.

  - **customerrors**: Custom error definitions.
    - `errors.go`: Error handling and custom error definitions.

  - **db**: Database-related files and repositories.
   - **migrations**: contains all the migrations.
        - `m.sql`: SQL files for database schema and seed data.
    - **repositories**: Database interaction and repository pattern implementations.
      - `repository.go`: General repository functions.
      - `user_repository.go`: User-specific repository functions.
    - `db.go`: Database connection and setup.

  - **logger**: Logging utilities.
    - `logger.go`: Setup and configuration for logging.

  - **utils**: Utility functions.
    - `json.go`: JSON helper functions.

- **scripts**: Scripts for build, setup, and other tasks.
  - `Makefile`: Makefile containing various commands for building and managing the application.

- **tests**: Contains test files.
  - `main_test.go`: Main test file for the application.

## Getting Started

### Prerequisites

- Go (version 1.16+ recommended)
- A running instance of a compatible database

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/SahilDhingraa/go-folder-structure.git
   cd go-folder-structure
   ```

2. Install dependencies:
   ```sh
   go mod tidy
   ```

### Running the Application

To run the application, use the following command:
```sh
go run cmd/main.go
```

### Running Tests

To run the tests for the application, use:
```sh
go test ./...
```

## Contributing

Feel free to open issues or submit pull requests if you find any bugs or have feature requests.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

This README provides an overview of the project, explains the folder structure, and gives instructions for getting started with the application.