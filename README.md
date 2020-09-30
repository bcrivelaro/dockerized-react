### Dev

Using docker only:

```bash
  $ docker build -f Dockerfile.dev .
  $ docker run -p 3000:3000 -it 4b00a3e45304
  $ docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app -it 4b00a3e45304
```

Using docker-compose:

```bash
  $ docker-compose up
```

### Test

Already exists a service for tests on docker-compose.yml.

Or, you can run `docker-compose up` and exec tests inside web service container:

```bash
  $ docker exec -it ed23bbad5dcc npm run test
```

If you want to launch a container just for test:

```bash
  $ docker run -it ed23bbad5dcc npm run test
```

### Production

```bash
  $ docker build -f Dockerfile.prod .
  $ docker run -p 8080:80 f725bd5904a7
```
