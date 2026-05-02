 🚀 Task Manager API (DevOps Project)
A cloud-native Task Manager application built using **Spring Boot** and deployed using modern **DevOps practices** including Docker, CI/CD, and Kubernetes.
---

📌 Features
* Create, update, delete, and fetch tasks
* RESTful APIs using Spring Boot
* In-memory database (H2)
* Containerized using Docker
* CI/CD pipeline using GitHub Actions
* Kubernetes deployment with multiple replicas
* Exposed using NodePort service
---

🛠️ Tech Stack
* **Backend**: Spring Boot (Java 21)
* **Database**: H2
* **Build Tool**: Maven
* **Containerization**: Docker
* **CI/CD**: GitHub Actions
* **Orchestration**: Kubernetes (Minikube)
---

📁 Project Structure
```bash
taskmanager/
├── src/
├── Dockerfile
├── pom.xml
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
└── .github/
    └── workflows/
        └── docker.yml
```
---

⚙️ How to Run Locally

### 1. Clone Repository

```bash
git clone https://github.com/<your-username>/taskmanager.git
cd taskmanager
```

### 2. Build the Application

```bash
mvn clean package
```

### 3. Run the Application

```bash
mvn spring-boot:run
```
---

🐳 Run with Docker

### Build Image

```bash
docker build -t taskmanager-app .
```

### Run Container

```bash
docker run -p 8080:8080 taskmanager-app
```
---

☁️ Kubernetes Deployment

### Apply manifests

```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

### Access application

```bash
minikube service taskmanager-service
```
---

⚠️ Configuration Note

Before deploying to Kubernetes, update the Docker image name in the deployment file:

```yaml
image: <docker-username>/taskmanager-app:latest
```

👉 Replace `<docker-username>` with your Docker Hub username.
---

🔄 CI/CD Pipeline
* Triggered on push to `main` branch
* Builds the application using Maven
* Builds Docker image
* Pushes image to Docker Hub
---

🌐 API Endpoints

| Method | Endpoint    | Description   |
| ------ | ----------- | ------------- |
| GET    | /tasks      | Get all tasks |
| POST   | /tasks      | Create a task |
| PUT    | /tasks/{id} | Update a task |
| DELETE | /tasks/{id} | Delete a task |

---

🧠 DevOps Highlights

* Implemented containerization using Docker
* Automated CI/CD pipeline with GitHub Actions
* Deployed scalable application on Kubernetes
* Used Infrastructure as Code (Kubernetes YAML)

---

📌 Future Improvements
* Add persistent database (MySQL/PostgreSQL)
* Implement Helm charts
* Add monitoring (Prometheus & Grafana)
* Add authentication (JWT)
---

👨‍💻 Author
Harshit
---

