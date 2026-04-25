# 🚀 Knightnum Professional Docker Template

A high-performance, production-ready Docker template designed by **Knightnum Limited**. This template provides a pre-configured environment for PHP-API or Static HTML projects.

## 🛠 Prerequisites
- **Docker** (v20.10+)
- **Docker Compose** (v2.0+)
- Basic knowledge of Terminal/Command Line

## 🚀 Getting Started

### 1. Initialize Project
Click the **"Use this template"** button on GitHub to create your own repository. Then clone it to your local machine:
```bash
git clone [https://github.com/your-username/your-project-name.git](https://github.com/your-username/your-project-name.git)
cd your-project-name
2. Configuration (Crucial Step)
Before running the containers, you must setup your environment variables. Copy the example file:

Bash
cp .env.example .env
3. Customizing Your Project
Open the .env file and modify the following values to avoid conflicts with other projects:

PROJECT_NAME: This will affect the Prefix of your network and volumes.

CONTAINER_NAME_PREFIX: (Optional) Used to identify your containers in docker ps.

HOST_PORT: Change this to any available port (e.g., 8081, 8082, 9000) to access your web app.

Example .env configuration:

ข้อมูลโค้ด
PROJECT_NAME=knightnum-crm
HOST_PORT=8085
4. Deployment
Run the following command to start the services in detached mode:

Bash
docker compose up -d --build
🌐 Accessing the App
Once started, your application will be available at:

Local: http://localhost:YOUR_HOST_PORT

Network: http://your-server-ip:YOUR_HOST_PORT

📁 Project Structure
/src - Place your PHP/HTML source code here (Hot-reload enabled).

/docker - Contains server configurations (Nginx/PHP-FPM).

docker-compose.yml - Main orchestration file.

.env - Environment-specific variables (Not tracked by Git).

🐳 Useful Docker Commands
Stop services: docker compose down

View logs: docker compose logs -f

Restart services: docker compose restart

Check container status: docker ps

Developed and Maintained by Knightnum Limited
