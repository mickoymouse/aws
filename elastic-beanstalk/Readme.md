### Install Deps

```sh
    npm install
```

### Start Server

```sh
    DATABASE_URL="postgresql://postgres:password@localhost:5432/study-sync" PORT=4567 npm start
```

# Run Postgres Server

```sh
    docker compose up
```

## Install Postgres Client

```sh
    sudo apt install postgres
```

## Create initial database

```sh
    createdb study-sync -h localhost -U postgres
```

## Connect to Postgres Client

```sh
    psql postgresql://postgres:password@localhost:5432/study-sync
```

## Create a postgres table

## Create Schema

psql study-sync < sql/schema.sql -h localhost -U postgres

## Import Data

psql study-sync < sql/seed.sql -h localhost -U postgres

## Verify Data

```sh
    psql postgresql://postgres:password@localhost:5432/study-sync
```

```sh
    select * from questions;
```

## Install EB CLI

> EB at the the time of creating this repo only works in 3.11 and not 3.12. I suggest using conda to handle python environment.

```sh
    pip install virtualenv
    python ./aws-elastic-beanstalk-cli-setup/scripts/ebcli_installer.py
```

> Follow additional steps mentioned in terminal (if any).

## Initialize EB

```sh
    eb init
```
