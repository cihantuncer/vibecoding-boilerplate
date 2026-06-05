# Database Directives Index

Use for SQL, schema, migrations, indexes, data access, and persistence.

- Identify affected tables/models, read/write paths, and data ownership.
- Prefer reversible, narrow changes; preserve existing data and constraints.
- Use parameterized queries and existing migration/data-access patterns.
- Validate with the smallest relevant query, test, or migration check.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| routine query/data-access edit | none | this index is enough |
| migration, constraint, index, backfill, import/export, prod data | `./database-migrations.md` | data shape or integrity may change |
| transactions, query safety, unclear persistence risk | `./database.md` | risk is not covered by this index |

Open at most one database directive unless the task clearly needs more.
