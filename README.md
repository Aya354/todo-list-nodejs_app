# 📝 Todo List App - DevOps Focused Project

This is a simple Todo List web application designed to demonstrate a full DevOps workflow from development to deployment.

## ⚙️ Tech Stack
- **Backend:** Node.js + Express.js  
- **Database:** MongoDB  
- **Templating Engine:** EJS  
- **Containerization:** Docker & Docker Compose  
- **CI/CD:** GitHub Actions  
- **Automation & Provisioning:** Ansible  
- **Image Registry:** DockerHub  
- **Auto Deployment:** Watchtower

## 🚀 DevOps Workflow

- The app is containerized using Docker and managed with Docker Compose.
- CI pipeline is implemented using GitHub Actions:
  - Automatically builds and pushes the Docker image to a private DockerHub registry on every push.
- A virtual machine (VM) is provisioned and configured using Ansible to install Docker and run the app.
- **Watchtower** is used inside the VM to automatically detect new image versions and redeploy the container without manual intervention.

## 📁 Notes
- Secrets and credentials are never committed to the repository.
- I chose Watchtower because it’s easy to use and runs as a container without complex configurations,It operates in the background, monitoring the registry for image updates. If a new version is available, it automatically pulls and restarts the container,This ensures the application always stays up-to-date without manual intervention.
- Also I chose to run MongoDB as a containerized service instead of using an online service like MongoDB Atlas, in order to have full control over the database environment and avoid potential connectivity issues or unexpected costs. Running MongoDB locally within Docker also provides better isolation and integration during development and testing.
- To prevent data loss when the container is restarted or removed, I implemented persistent storage using Docker volumes. This ensures that the data is safely stored outside the container lifecycle.
- Additionally, I installed Ansible on my local Windows machine using WSL (Windows Subsystem for Linux), which allowed me to manage and configure the virtual machine automatically—simulating a real production environment.



---

## Screenshots
<img width="1920" height="1032" alt="2" src="https://github.com/user-attachments/assets/441235d4-7737-4ada-ab8d-289b4faf92f3" />
<img width="1916" height="1037" alt="1" src="https://github.com/user-attachments/assets/8feeb0af-8c0d-40d4-a862-2b83ec2343ff" />
<img width="1918" height="1045" alt="3" src="https://github.com/user-attachments/assets/e60d19ea-6a33-4b91-836d-5d943ad12255" />
<img width="1712" height="955" alt="5" src="https://github.com/user-attachments/assets/b5c2e0f5-6cbc-48e9-90a9-c0a0a58ccd11" />
<img width="1920" height="1080" alt="4" src="https://github.com/user-attachments/assets/22f6ee35-776e-41b1-90c8-5db546054f97" />
<img width="1517" height="376" alt="8PNG" src="https://github.com/user-attachments/assets/a711dbf4-bdd6-40e6-9b95-f8c161b650ea" />


