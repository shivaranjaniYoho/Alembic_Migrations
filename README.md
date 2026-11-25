# Alembic Migrations

## Project Description
This task demonstrates how to manage database schema changes using Alembic with SQLAlchemy and PostgreSQL.

## Requirements
- Python
- PostgreSQL
- SQLAlchemy
- Alembic
- psycopg2-binary
- python-dotenv
- VS Code

## Tasks Completed

### 1. Alembic Initialization
- Initialized Alembic using `alembic init`.
- Configured `env.py` to read DATABASE_URL from the `.env` file.
- Connected Alembic to PostgreSQL.

### 2. First Migration
- Created a Customer model with id, name, and email columns.
- Generated the first migration using autogenerate.
- Applied the migration using `alembic upgrade head`.
- Created the customers table in PostgreSQL.

### 3. Second Migration
- Added a phone column to the Customer model.
- Generated a second migration.
- Applied the migration using `alembic upgrade head`.
- Verified the phone column in pgAdmin.

### 4. Rollback Migration
- Used `alembic downgrade -1` to roll back one migration.
- Verified that the phone column was removed from the customers table.

### 5. Migration History
- Used `alembic history` to display migration history.
- Used `alembic current` to check the current database migration version.

## Commands Used

Initialize Alembic:
```bash
python -m alembic init alembic
```

Generate first migration:
```bash
python -m alembic revision --autogenerate -m "create customers"
```

Apply migration:
```bash
python -m alembic upgrade head
```

Generate second migration:
```bash
python -m alembic revision --autogenerate -m "add phone column"
```

Roll back one migration:
```bash
python -m alembic downgrade -1
```

Check migration history:
```bash
python -m alembic history
```

Check current migration:
```bash
python -m alembic current
```

## Conclusion
Learned how to use Alembic to create, apply, and roll back database migrations. Also learned how to manage database schema changes and track migration history using PostgreSQL.
