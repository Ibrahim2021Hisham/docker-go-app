# Go Docker App

Simple Go web application that runs in Docker.

## What it does

- Serves HTTP on port 8080
- Returns "Hello from Dockerized Go app!"

## How to run

### With Docker (recommended)

```bash
# Build and run
docker build -t my-go-app .
docker run -p 8080:8080 my-go-app
```

### Without Docker

```bash
# Run directly
go run main.go
```

Visit: <http://localhost:8080>

## Docker Hub

**Image:** [aliashraf510/my-go-app](https://hub.docker.com/r/aliashraf510/my-go-app)

```bash
# Pull and run from Docker Hub
docker pull aliashraf510/my-go-app:latest
docker run -p 8080:8080 aliashraf510/my-go-app:latest
```

## Files

- `main.go` - Go application
- `Dockerfile` - Docker configuration  
- `go.mod` - Go module file

## Author

Ali Ashraf