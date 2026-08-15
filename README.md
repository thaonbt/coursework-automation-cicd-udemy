# 🎓 Coursework: Robot Framework with Python
> **Subtitle:** Selenium UI & API Automation Testing (Step-by-Step Tutorial)

This repository contains all the hands-on exercises, automation scripts, and core concepts I developed while mastering automated testing using Robot Framework via Udemy.

---

### 📂 Repository Structure Note

To maintain clean project isolation and manage dependencies effectively, this learning track is divided into three specialized repositories:

*   **Framework Repo([coursework-robot-python-framework-udemy](https://github.com/thaonbt/coursework-robot-python-framework-udemy)):** Focuses on basic to advanced Robot Framework syntax, Selenium UI interactions, and API validation. Contains the scalable, production-ready custom automation framework built during the course.
*   **Automation CI/CD Repo(this repo):** Dedicated to DevOps configurations, pipeline setups, and continuous integration environments.

---

### 🛠️ Tech Stack & DevOps Tools
*   **Language:** Python 3.x
*   **Frameworks:** Robot Framework (SeleniumLibrary & RequestsLibrary)
*   **CI/CD Orchestration:** Jenkins (Local Server Server Setup)
*   **Webhook & Tunneling:** ngrok (For local-to-cloud GitHub integration)
*   **Build Automation Integration:** Maven (`mvn test -PRgression` reference)

---

### 🚀 Continuous Integration (Jenkins Setup Guide)

Follow these step-by-step instructions to deploy a local Jenkins controller and connect it with GitHub Webhooks for automated push-event testing:

#### 1. Launching Jenkins
*   Download the generic Java web archive package (`jenkins.war`) directly from the official [Jenkins Downloads Page](https://jenkins.io).
*   Open your terminal, navigate to the folder containing the downloaded file, and execute the following command to start the server on a custom port:
    ```bash
    java -jar jenkins.war --httpPort=9090
    ```

#### 2. Initial Configuration Wizard
*   Open your web browser and navigate to: `http://localhost:9090`
*   Copy the automatically generated **initial administrator password** from your terminal console and paste it into the Jenkins UI activation field.
*   Select **"Install suggested plugins"** to automatically load standard pipeline and SCM dependencies.
*   Complete the configuration by creating your primary Admin User account.

#### 3. Configuring the Automation Job & Webhooks
*   Click **New Item** on the dashboard to build a new automation job.
*   Under the job configuration panel, set up the execution build and test steps (e.g., executing test execution goals like `mvn test -PRgression`).
*   *(Optional but Recommended)* Launch **ngrok** to securely expose your local instance to the public internet:
    ```bash
    ngrok http 9090
    ```
*   Copy the public secure URL provided by ngrok and paste it into your GitHub Repository's **Webhooks** settings page.
*   Configure the Jenkins job trigger to listen strictly for GitHub **Push Events**. 

Now, whenever you perform a `git push` to this repository, GitHub will instantly ping your Jenkins server and trigger your test suites automatically!

---

### 📜 Verified Certificate
*   You can view my official course completion certificate here: [Udemy Verified Certificate](https://www.udemy.com/certificate/UC-1abc7252-f2e7-4f7c-a148-8b5c34692de1/)

---
_Disclaimer: This repository is maintained strictly for personal learning, code practice, and future reference._
