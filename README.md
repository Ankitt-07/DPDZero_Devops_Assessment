# DPDZero_Devops_Assessment

# 🔁 Nginx Reverse Proxy with Docker Compose

This project shows how to use **Nginx** as a reverse proxy to route requests to two backend services running in **Docker containers**.

---

## 📦 Project Structure

.
├── docker-compose.yml
├── nginx/
│ ├── nginx.conf
│ └── Dockerfile
├── service_1/
│ ├── main.go
│ ├── go.mod
│ └── Dockerfile
├── service_2/
│ ├── app.py
│ └── Dockerfile
└── README.md




---

## ⚙️ How It Works

- **Nginx** runs in its own container and listens on port **8080**.
- It forwards incoming requests based on the URL path:
  - `/service1` → **Go backend** (Service 1)
  - `/service2` → **Flask backend** (Service 2)
- Both services run on their own ports (8001 and 8002) inside the Docker network.
- Nginx logs every request with a **timestamp** and **path**.

---

## 🚀 How to Run the Project

1. Make sure you have **Docker** and **Docker Compose** installed.
2. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/nginx-reverse-proxy-example.git
   cd nginx-reverse-proxy-example


## To Run this project
docker-compose up --build



🌐 Test the Services
Once running, open your browser or use curl:

Service 1:

http://localhost:8080/service1/hello

http://localhost:8080/service1/ping

Service 2:

http://localhost:8080/service2/hello

http://localhost:8080/service2/ping




🧪 Health Checks
Each service has a health check:

Nginx waits until /ping endpoints of both services respond before routing traffic.


