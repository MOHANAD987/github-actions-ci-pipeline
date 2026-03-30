# 🚀 CI Pipeline using GitHub Actions

<p align="center">

  <img src="https://img.shields.io/badge/GitHub%20Actions-CI-blue?logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Java-17-orange?logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Maven-Build-red?logo=apachemaven&logoColor=white" />
  <img src="https://img.shields.io/badge/CI-Pipeline-success-green" />
  <img src="https://img.shields.io/badge/Status-Active-brightgreen" />

</p>

---

## 📌 Project Description
This project demonstrates how to build a **CI pipeline** using **GitHub Actions** for a Java application with Maven. It automates the build and testing process to ensure code quality before merging.

---

## 🎯 Project Goals
- Apply Continuous Integration (CI) concepts  
- Automate build and test processes  
- Improve code quality before merge  
- Gain hands-on experience with GitHub Actions  

---

## ⚙️ How the Pipeline Works

When a Pull Request is created to the `main` branch, the workflow is triggered automatically:

### 🔄 Steps:
1. Checkout the code  
2. Set up Java environment  
3. Build the project using Maven  
4. Run Unit Tests  
5. Show execution result (success or failure)  

---

## 🛠️ Technologies Used
- GitHub Actions  
- Java  
- Maven  

---

## 📂 Project Structure

```text
project/
│
├── .github/workflows/ci.yml
├── src/
├── pom.xml
├── README.md
├── .gitignore
│
├── screenshots/   
│
├── diagrams/
│   └── ci-architecture.png
```
---

## ⚡ Workflow File

📍 Path:
.github/workflows/ci.yml

```yaml

name: ci workflow

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  ci-workflow:
    name: CI Workflow
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Build the app
        run: mvn clean package
        shell: bash

      - name: Test the app
        run: mvn test
        shell: bash
```

---

## 🔄 Workflow Lifecycle

1. Developer creates a new branch
2. Developer pushes changes to the repository
3. A Pull Request is created to the main branch
4. GitHub Actions automatically triggers the CI pipeline
5. The pipeline executes:
   - Build
   - Test
6. If successful, the code can be merged

---


## 📸 Screenshots
🔗 [Open Screenshots Folder](./screenshots/)
 
---

## 📊 Architecture Diagram
🔗 [Open Diagrams Folder](./diagrams/)

---

## 📚 What I Learned
- Creating GitHub Actions workflows
- Understanding CI/CD pipelines
- Running Maven in a CI environment
- Working with runners
- Automating build and test processes

---

## 👨‍💻 Author

Mohanad Faisal

---

## 📄 License

This project is licensed under the MIT License.

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub!


