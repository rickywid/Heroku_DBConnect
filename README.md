# Setting up Heroku Postgres DB
There is a lot of information in the Heroku [Postgres documentation](https://devcenter.heroku.com/articles/heroku-postgresql) page. I want to create a cheat sheet type documentation containing only the relevent information that I'll be using.

##### Find your Heroku Postgres DB
`heroku pg:info`

```
=== DATABASE_URL
Plan:                  Hobby-dev
Status:                Available
Connections:           0/20
PG Version:            10.6
Created:               2019-02-24 21:26 UTC
Data Size:             7.9 MB
Tables:                1
Rows:                  2/10000 (In compliance)
Fork/Follow:           Unsupported
Rollback:              Unsupported
Continuous Protection: Off
Add-on:                postgresql-metric-41174 <==========================
```

##### Establish a psql session with your remote database
`heroku pg:psql`

##### Push Local Postgres database to remote Heroku Postgres database
`heroku pg:push mylocaldb HEROKU_POSTGRESQL_MAGENTA --app sushi`

##### Pull remote Heroku Postgres databaseto local Postgres database
`heroku pg:pull HEROKU_POSTGRESQL_MAGENTA mylocaldb --app sushi`

##### Drop and recreate your database
`heroku pg:reset`
