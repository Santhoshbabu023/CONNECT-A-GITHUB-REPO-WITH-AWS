# CONNECT-A-GITHUB-REPO-WITH-AWS

# 🚀 Connect a GitHub Repo with AWS

## 📌 Project Overview
This project demonstrates how to set up **Git** and **GitHub** for a web app, initialize a Git repository, connect it to GitHub, and push files. It covers making changes, tracking updates, and using version control for smooth collaboration.

## 🛠 Key Tools & Concepts
- **Git** – A version control system to track code changes and enable collaboration.
- **GitHub** – A cloud-based platform for hosting and managing Git repositories.
- **EC2 (AWS)** – Used for saving and sharing code.
- **Branches & Commits** – For managing changes safely and efficiently.
- **Authentication** – Using SSH keys or Personal Access Tokens (PAT) for secure access.

## 🔧 Git & GitHub Setup
### 1️⃣ Install Git (on EC2)

sudo dnf update -y
sudo dnf install git -y


### 2️⃣ Initialize a Local Repository

git init

### 3️⃣ Configure Git Identity

git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

## 🔄 Tracking & Pushing Changes to GitHub
### 1️⃣ Add files to staging area

git add .

### 2️⃣ Commit changes with a message

git commit -m "Initial commit"

### 3️⃣ Connect to GitHub Repository

git remote add origin https://github.com/user/repo.git

### 4️⃣ Push changes

git push -u origin master

## 🔑 Authentication (HTTPS vs SSH)
### Using Personal Access Token (PAT)
GitHub no longer supports password authentication. Instead:
1. Go to **GitHub > Settings > Developer Settings > Personal Access Tokens**
2. Generate a **new token** with repo permissions.
3. Use the token instead of your password when pushing code.

### Using SSH Keys (Alternative)
1. Generate an SSH key:
 
   ssh-keygen -t rsa -b 4096 -C "your.email@example.com"
  
2. Add the key to GitHub:
   - Copy the public key: `cat ~/.ssh/id_rsa.pub`
   - Go to **GitHub > Settings > SSH and GPG Keys > New SSH Key**
3. Test the connection:

   ssh -T git@github.com
  

## 🔄 Updating Code on GitHub
After making changes to files:

git add .
git commit -m "Updated index.jsp"
git push

Changes will now be visible in the GitHub repository!

## 📌 Project Reflection
- **Challenges:** Setting up GitHub authentication without using a password.
- **Successes:** Successfully pushing code, tracking changes, and understanding Git workflows.
- **Future Work:** This is part of a **DevOps CI/CD series**, where I'll automate deployments and integrate DevOps tools for efficient software delivery.

---
💡 *This project helped me gain hands-on experience with Git & GitHub for version control and collaboration!* 🚀
