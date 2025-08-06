# Demo Jenkins CI/CD Project 🚀

This project demonstrates a simple CI/CD pipeline using **Jenkins**, **GitHub**, **Maven**, and **Tomcat** to automate the build and deployment of a Java `.war` file.

---

## 📦 Project Overview

- **Application Type**: Java Web Application (WAR file)
- **Build Tool**: Maven
- **CI/CD Tool**: Jenkins
- **Deployment Server**: Apache Tomcat
- **Version Control**: Git & GitHub

---

## 🔧 Setup Details

### 💻 Environment

- **Jenkins VM**: `192.168.1.9`
- **Tomcat VM**: `192.168.1.8`
- **GitHub Repo**: [Demo-Jenkins-Project](https://github.com/Hyghen/Demo-Jenkins-Project)

---

## ✅ Step-by-Step explanation of what i have done

1. **Created GitHub Repo**  
   - [https://github.com/Hyghen/Demo-Jenkins-Project](https://github.com/Hyghen/Demo-Jenkins-Project)

2. **Set Up Jenkins on a Fresh VM**  
   - Installed Jenkins manually (not using EC2).
   - Installed necessary Jenkins plugins: Git, Maven Integration, Deploy to container, etc.

3. **Configured Jenkins**  
   - Created a new pipeline job.
   - Connected to the GitHub repository.
   - Used **Poll SCM** to check for code changes every 15 minutes.

4. **Set Up Apache Tomcat on Another VM**  
   - Downloaded and configured Tomcat server on `192.168.1.8`.
   - Configured Tomcat users and allowed deployment via Jenkins.

5. **Created Jenkins Pipeline (Jenkinsfile)**  
   - Pipeline stages: `Build`, `Test`, and `Deploy to Prod`.
   - Built WAR using `mvn package`.
   - Deployed WAR file to the Tomcat server using `Deploy to Container` plugin.

6. **Tested the CI/CD Workflow**  
   - Made a code change and pushed to GitHub.
   - Jenkins job triggered automatically via SCM polling.
   - WAR file built and deployed successfully to Tomcat server.
   - Verified output on browser: [http://192.168.1.8:8080/app](http://192.168.1.8:8080/app)

---

## 🧪 How to Test

1. Clone the repo:

-- git clone https://github.com/Hyghen/Demo-Jenkins-Project.git
  Modify the code.

Commit and push changes:

-- git add .
-- git commit -m "Test change"
-- git push origin main
 
 Jenkins will poll the repo and trigger the build.


Check the deployed app:

-- http://192.168.1.8:8080/app

🔗 Useful Links

-- Jenkins Dashboard: http://192.168.1.9:8080
-- Deployed App: http://192.168.1.8:8080/app
-- GitHub Repo: https://github.com/Hyghen/Demo-Jenkins-Project/

📌 Technologies Used

-- Git & GitHub
-- Jenkins
-- Maven
-- Apache Tomcat
-- Shell Scripting (basic)
-- WAR Deployment

🙌 Author
Chitransh Jangid
DevOps Enthusiast | Always learning through real-time troubleshooting
