🚀 Quick Start
Option A: Run from Docker Hub (Fastest)
bash
docker run -p 8080:8080 --name go-web-app aliashraf510/my-go-app:latest
Access: http://localhost:8080

Option B: Build & Run Locally
bash
# Clone and build
git clone <your-repo>
cd go-docker-app

# Build Docker image
docker build -t go-web-app:local .

# Run container
docker run -p 8080:8080 --name go-web-app go-web-app:local
📌 Application Overview
Port: 8080
Endpoint: / (root)
Response: Hello from Dockerized Go app!
Health Check: http://localhost:8080/health (returns 200 OK)

This microservice demonstrates:

Minimal Go web server implementation

Optimized Docker containerization

Multi-stage Docker builds

Public image distribution via Docker Hub

🔧 Development & Customization
Run in Development Mode
bash
# Hot-reload with Air (watch for changes)
go install github.com/cosmtrek/air@latest
air

# Or with standard Go
go run main.go
Modify the Application
Edit main.go to change response messages

Update Dockerfile for additional dependencies

Adjust go.mod for new packages

Build Custom Image
bash
# Multi-architecture build
docker buildx build --platform linux/amd64,linux/arm64 -t yourusername/go-app:v1 .

# Push to registry
docker push your

Ibrahim Hisham
