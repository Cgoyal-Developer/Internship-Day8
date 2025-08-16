# 🚀 TASK 8: Run a Simple Java Maven Build Job in Jenkins  

## 📌 Objective  
This task helps you understand how to **build a Java application using Jenkins and Maven**.  
It is your **first step into CI/CD (Continuous Integration / Continuous Delivery)**, where:  
- Developers push code → Jenkins automatically builds it.  
- Errors are detected early (faster feedback loop).  
- Builds are consistent and repeatable.  

---

## 🧠 Concepts You Should Know  

### 🔹 Jenkins  
- Jenkins is an **open-source automation server**.  
- It is widely used for **CI/CD pipelines**.  
- Supports **plugins** for integration with tools like Maven, Git, Docker, Kubernetes, etc.  

### 🔹 Maven  
- Maven is a **build automation tool** for Java projects.  
- Uses `pom.xml` to define dependencies, plugins, and project build instructions.  
- Provides standard build phases: **compile → test → package → install → deploy**.  

### 🔹 CI/CD Workflow (in this task)  
1. Developer writes Java code (`HelloWorld.java`).  
2. Defines build instructions in `pom.xml`.  
3. Jenkins fetches the project from GitHub (or local workspace).  
4. Jenkins runs **Maven Goals (`clean package`)**:  
   - `clean` → removes previous build files.  
   - `package` → compiles the code and packages it into a `.jar`.  
5. Jenkins shows **BUILD SUCCESS** when the process finishes.  

---

## 🛠️ Tools Required (All Free)  
- **Jenkins** (Installed locally or via Docker)  
- **Java JDK 8 or 11** (for compiling Java code)  
- **Maven** (for build & dependency management)  
- **Git** (optional, only if pulling code from repo; else local folder works)  

---

## 📂 Deliverables  
1. A **basic Java HelloWorld app** (with `pom.xml`)  
2. Jenkins **Freestyle Job** configured to build the Java app  
3. **Screenshot of successful Jenkins build console output**  

---

## 📦 Repository Structure  
