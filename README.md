# DevOps Frontend Project with Automated Testing

This project demonstrates a **frontend web application** whose builds and tests are fully automated using **Azure DevOps** pipelines and **Selenium Java automation scripts**. The workflow ensures that any code changes trigger an automated build, deployment, and testing process, making the pipeline fully CI/CD-ready.

---

## Project Overview

- The frontend project consists of **HTML/CSS** code.  
- Whenever code is updated in the repository, **Azure DevOps build pipeline** automatically creates a WAR file.  
- The WAR file is then used as an **artifact** to deploy to the QA environment and run automated tests.  
- Automated testing is handled using **Selenium Java test scripts**, integrated directly into the pipeline.

---

## Features

- **Automated WAR build:** Triggered automatically on code changes.  
- **Artifact management:** WAR file from the build pipeline is used for QA deployment.  
- **Automated testing:** Selenium Java test scripts run as part of the pipeline after deployment.  
- **CI/CD integration:** Fully automated process from code commit → build → deploy → test.  

---

## Workflow

1. **Code Commit:** Any changes pushed to the repository trigger the build pipeline.  
2. **Build Pipeline:**  
   - Compiles the frontend project.  
   - Creates a WAR file artifact.  
3. **Release Pipeline:**  
   - Deploys the WAR file to the QA environment.  
   - Executes Selenium Java test scripts automatically using the artifact.  
4. **Test Execution:**  
   - Scripts include **timeout polling** to handle delays in environment updates.  
   - Verifies application functionality automatically after deployment.

---

## Key Points & Lessons Learned

1. **WAR artifact triggers tests:**  
   Every code change results in a new WAR build, which ensures the QA environment always runs the latest version.  

2. **Timeout polling is critical:**  
   When a new WAR is deployed, the frontend may take some time to update. Without polling and retries in the test scripts, tests can fail.  

3. **Selenium dependency:**  
   Selenium 3 was used, which required proper browser setup to ensure tests ran reliably within the pipeline.  

4. **Full automation in pipeline:**  
   From build to deployment to testing, everything is executed automatically with no manual intervention.

---

## Screenshots of Azure Devops:

1. **Build Pipeline**
   <img width="1444" height="630" alt="image" src="https://github.com/user-attachments/assets/37f90bbe-ff1b-4f7c-8cd1-3a661a0a857f" />
   <img width="1444" height="630" alt="image" src="https://github.com/user-attachments/assets/d1253a6b-24c3-4151-8319-3a97d9b0850d" />

2. **Release Pipeline**
    <img width="1444" height="630" alt="image" src="https://github.com/user-attachments/assets/e4c11769-ab73-4e3c-9012-d0a48b54d554" />
    <img width="1444" height="630" alt="image" src="https://github.com/user-attachments/assets/612c300e-9bad-4d10-a762-72738d9bf01b" />

3. **Azure Repository added too**
   <img width="1444" height="1158" alt="image" src="https://github.com/user-attachments/assets/35c78710-aab0-4325-83a1-dd15194c77a5" />

