# Proffy Api

## Techs

- ReactJs
- TypeScript
- Express
- Node
- SQLite
- Knex

## Run

To install all dependencies execute:

```
yarn install
```

then, start the project:

```
yarn start
```

## Migrations

Run migrations:

```
yarn knex:migrate
```

Rollback migrations:

```
yarn knex:rollback
```

## Endpoints

### Connections

- Route to list all connections
  ```
  GET: http://localhost:3333/connections/
  ```
- Route to create a new connection
  ```
  POST: http://localhost:3333/connections/
  {
    "user_id": Number
  }
  ```

### Classes

- Route to create a new class
  ```
  POST: http://localhost:3333/classes/
  {
    "name": String,
    "avatar": String,
    "whatsapp": String,
    "bio": String,
    "subject": String,
    "cost": Number,
    "schedule": [
      {
        "week_day": Number,
        "from": String, //Example 08:00
        "to": String //Example 21:00
      }
    ]
  }
  ```
- Route to list all classes
  ```
  GET: http://localhost:3333/classes/
  ```
  - Filter by subject, day of week and available hour
  ```
  ?week_day=1&subject=Math&time=11%3A00
  ```
