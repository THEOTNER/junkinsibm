# Jenkins CI/CD Pipeline Setup

## Overview
This project demonstrates the setup of a Continuous Integration/Continuous Deployment (CI/CD) pipeline using Jenkins. The pipeline is configured to pull code from a GitHub repository, build the application, run tests, and deploy the application.

## Steps Completed

### 1. **Environment Setup**
- Installed **Git Bash** from the official Git website.
- Configured Git with a username and email using the following commands:
  ```bash
  git config --global user.name "Aditya M"
  git config --global user.email "you@example.com"
  ```

### 2. **Git Repository Initialization**
- Initialized a Git repository in the project directory.
  ```bash
  cd /path/to/your/project
  git init
  ```
- Added all files to the staging area and committed them.
  ```bash
  git add .
  git commit -m "Initial commit"
  ```

### 3. **GitHub Repository Creation**
- Created a new GitHub repository (`internshiptesting`) and pushed the local project to this repository.
  ```bash
  git remote add origin https://github.com/THEOTNER/junkinsibm.git
  git push -u origin main
  ```

### 4. **Jenkins Installation and Configuration**
- Installed necessary Jenkins plugins:
  - **Pipeline**
  - **Git**
  
### 5. **Jenkins Pipeline Job Creation**
- Created a new Pipeline job in Jenkins named `IBMTest`.
- Wrote the following Jenkins pipeline script:

```groovy
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/THEOTNER/junkinsibm.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add your build commands here
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deploy commands here
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
```

### 6. **Pipeline Execution**
- Triggered the pipeline, which completed successfully:
  - **Checkout Stage**: Cloned the repository from GitHub.
  - **Build Stage**: Displayed "Building the application...".
  - **Test Stage**: Displayed "Running tests...".
  - **Deploy Stage**: Displayed "Deploying the application...".
  - **Final Status**: Pipeline succeeded!

## Conclusion
The Jenkins CI/CD pipeline has been successfully set up to automate the processes of building, testing, and deploying applications. This setup can be further enhanced by adding specific build and test commands as per project requirements.

## Future Enhancements
- Integrate actual build tools and testing frameworks.
- Set up notifications for pipeline success or failure.
- Implement more sophisticated deployment strategies.
