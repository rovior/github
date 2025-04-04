# 📌 What is Git?
Git is a version control system used to manage and track changes in files, especially in software projects. It allows developers to record modification history, compare versions, and revert changes when necessary.

## 🔍 Why is Git Important?
- **Change Tracking:** Git maintains a complete history of all changes made to a project, allowing you to review or restore previous versions.
- **Team Collaboration:** Multiple developers can work on the same project simultaneously without overwriting each other’s work.
- **Security and Reliability:** Git stores complete copies of the repository on each machine, preventing data loss.
- **Safe Experimentation:** You can create branches to test new ideas without affecting the main codebase.

## 🔄 How Does Git Work?
Git operates in three main areas:
- **Working Directory:** Where you edit project files.
- **Staging Area:** Where changes are temporarily stored before committing.
- **Repository:** Where finalized versions (commits) are stored and preserved.

## 📊 Git Workflow
1. **Edit:** Make changes to project files.
2. **Stage:** Select changes to be recorded (`git add .`).
3. **Commit:** Save changes permanently to the project history (`git commit -m "message"`).

---

## 🛠 Installing Git
To install Git on Ubuntu, use the following commands in the terminal:
```bash
sudo apt update
sudo apt install git
```
✅ To verify the installation:
```bash
git --version
```

---

## ⚙️ Basic Configuration
### Initializing a Repository
To start version control in a directory, initialize a Git repository inside it:
```bash
cd ~/Documents/gitTest
git init
```
This creates a `.git` directory containing Git configuration files that recognize `gitTest` as a versioned environment.

### Removing a Git Repository
To delete the `.git` repository from a folder:
```bash
rm -rf .git
```

### Setting the Default Branch Name
By default, Git names the main branch `master`. To change it to `main`:
```bash
git config --global init.defaultBranch main
```
For existing repositories, rename the branch:
```bash
git branch -M main
```

---

## 🔧 Configuring User, Email, and Editor
Set up your Git user details:
```bash
git config --global user.name "robert"
git config --global user.email "gitrobt@gmail.com"
```
Set the preferred text editor for commit messages:
```bash
git config --global core.editor "code -w"
git config --global core.editor "code --wait"
```
For IntelliJ users:
```bash
git config --global core.editor "intellij"
```
To check your current Git configuration:
```bash
git config --list
```

---

## 🔄 Changing the Git Username
To update your Git username, follow these steps:
```bash
git config --global user.name "NewUserName"
```
To check if the change was applied:
```bash
git config --list | grep user.name
```

This guide provides the fundamental Git setup and configuration steps to get started efficiently! 🚀

