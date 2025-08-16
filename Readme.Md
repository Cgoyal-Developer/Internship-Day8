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
hello-java-maven/
│── src/
│ └── main/
│ └── java/
│ └── HelloWorld.java
│── pom.xml

---

## Start Jenkins
Run Jenkins using Docker:
1. Access Jenkins: http://localhost:8080
2. Unlock Jenkins (password from logs).
3. Install Suggested Plugins.
👉 Concept: Jenkins runs on port 8080 and manages automation jobs

---

## Configure Maven in Jenkins

1. Go to Manage Jenkins → Global Tool Configuration.
2. Add Maven installation (e.g., Maven 3.8.6).
3. Ensure JDK installation (JDK 8 or 11) is also added.
👉 Concept: Jenkins needs to know where Maven & JDK are installed to build projects.

----

## Create a Jenkins Freestyle Job
1. Click New Item → Freestyle Project.
2. Name: hello-java-maven.
3. In Source Code Management:
   -If using GitHub repo → Add repo URL.
   -If using local project → Skip Git.
4. In Build Section:
   -Select Invoke top-level Maven targets.
   -Enter Goal: clean package
5. In Post-build Actions Section:
   -Select Archive the artifacts
   -Enter Files to archive: target/*.jar
6. Save the job.
👉 Concept: A Freestyle Job lets you define simple build steps.

---

## Run the Build
 1. Click Build Now.
 2. Check Console Output.
 3. You should see: ✅ BUILD SUCCESS


## 📸 Screenshots  

- **Jenkins Build Success**  
  ![Build Success](https://github.com/Cgoyal-Developer/Internship-Day8/blob/main/build-success.png?raw=true)  

- **Jenkins Workspace – `ls` Command Output**  
  ![Workspace ls](https://github.com/Cgoyal-Developer/Internship-Day8/blob/main/workspace-ls.png?raw=true)  

- **Target Folder Showing JAR File**  
  ![Target JAR](https://github.com/Cgoyal-Developer/Internship-Day8/blob/main/target-jar.png?raw=true)  

