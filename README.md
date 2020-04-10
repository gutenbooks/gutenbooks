# gutenberg-org

This project is a "monorepo" wrapper for the entire `gutenberg-org` stack. It's intent is to enable easy fullstack development on the entire project.

## Setup/Usage

```
git clone git@gitlab.com:gutenberg-org/gutenberg-org.git
cd gutenberg-org
./bin/init
```

Run Migrations

```
docker-compose run api python ./manage.py migrate
```

Seed the DB

```
docker-compose run api python ./manage.py updatecatalog
```

```
docker-compose run api python ./manage.py collectstatic
```

Then finally

```
docker-compose up
```

Once the project has spun up, the following services will be available:

| Service | URL |
|---------|-----|
| App | http://localhost:3000 |
| API | http://localhost:8000 |


## Updating

You can also run `./bin/init` to pull down all recent changes from the included repos.
