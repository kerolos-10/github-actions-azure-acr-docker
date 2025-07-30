
# GitHub Actions + Azure Container Registry (ACR) - CI/CD Pipeline

This project demonstrates how to build and push a Docker image to **Azure Container Registry (ACR)** using **GitHub Actions**, and how to run basic automation jobs in a separate workflow.

-----

## Project Structure

```
.
├── .github/
│   └── workflows/
│       ├── basic-automation.yml    # Workflow 1: Echo, cowsay, show README
│       └── docker-acr-pipeline.yml # Workflow 2: Build & Push Docker image to ACR
├── Dockerfile                  # Simple Dockerfile serving index.html
├── index.html                  # Basic HTML page
├── script.sh                   # Custom bash script used in Workflow 1
└── README.md                   # This file
```

-----

##  Workflows Overview

### Workflow 1: Basic Automation

Located in `.github/workflows/basic-automation.yml`, this workflow performs the following tasks:

  * Prints a welcome message.
  * Installs `cowsay`.
  * Displays the content of `README.md` and executes `script.sh`.

### Workflow 2: Docker Build & Push to Azure Container Registry

Located in `.github/workflows/docker-acr-pipeline.yml`, this workflow automates the following steps:

  * Builds the Docker image from your `Dockerfile`.
  * Tags the image as `githubactionsiti2025.azurecr.io/omar-adawy:latest`.
  * Pushes the tagged image to Azure Container Registry using credentials stored in GitHub Secrets.

-----

## Required Secrets

To ensure the workflows run successfully, you need to add the following secrets to your GitHub repository settings. Navigate to **Settings** → **Secrets and variables** → **Actions** and add:

  * `ACR_USERNAME`: Set this to `githubactionsiti2025`.
  * `ACR_PASSWORD`: Set this to `********************************`.

-----

## Some Screenshots

## 📦 Docker Output

This project builds a Docker image that serves a static HTML page. Once the container is pulled and run, you can view the deployed content by opening your browser to the specified address.

-----

## ✅ To Run Locally

To build and run the Docker image on your local machine, follow these steps:

```bash
docker build -t test-image .
docker run -p 8080:80 test-image
```

Then, visit `http://localhost:8080` in your browser.

-----

##  Author

**⭐ If this project helped you, please give it a star ⭐**

##  Support & Contact

Feel free to reach out if you have questions, feedback, or want to collaborate on DevOps, Cloud, or Infrastructure projects:

- 👨‍💻 **Name:** Kerolos Mamdouh  
- 📍 **Location:** Cairo, Egypt  
- 📧 **Email:** [kerolosmamdouh20@gmail.com](mailto:kerolosmamdouh20@gmail.com)  
- 💼 **LinkedIn:** [linkedin.com/in/kerolos-mamdouh-90a11b26b](https://www.linkedin.com/in/kerolos-mamdouh-90a11b26b)  
- 💻 **GitHub:** [github.com/kerolos-10](https://github.com/kerolos-10)  
