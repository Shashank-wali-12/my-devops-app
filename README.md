# Real DevOps CI/CD Project

## Technologies Used

- GitHub
- Jenkins
- Docker
- DockerHub
- Kubernetes
- Google Kubernetes Engine (GKE)
- AWS EC2

---

## CI/CD Flow

Developer pushes code to GitHub.

Jenkins pipeline automatically:
- pulls latest code,
- builds Docker image,
- pushes image to DockerHub,
- deploys application to Kubernetes.

Kubernetes performs rolling updates and exposes application using LoadBalancer service.

---

## Project Architecture

GitHub → Jenkins → Docker → DockerHub → Kubernetes (GKE)

---

## Final Output

Application successfully deployed on Kubernetes cluster.
