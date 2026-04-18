# IoT Lab

## 1. Initial Build & Launch

This command builds your images and starts the services. The --build flag ensures that any changes to your Dockerfile are applied.

```bash
docker-compose up --build
```

## 2. The "Emergency Reset" (Clean Start)

If you run into the nodemon: not found error or if your node_modules get corrupted, run this sequence. It wipes the cache and the volumes to give you a 100% fresh start.

### Stop containers and delete anonymous volumes

```bash
docker-compose down -v
```

### Rebuild from scratch without using cached layers

```bash
docker-compose build --no-cache
```

### Start it up

```bash
docker-compose up
```

## 3. Running in the Background

If you don't want to see the logs and want to keep using your terminal:

```bash
docker-compose up -d
```