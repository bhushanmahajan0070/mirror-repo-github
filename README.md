# 🪞 GitLab ↔ GitHub Repository Mirroring

This project demonstrates how to **create a mirrored repository between GitLab and GitHub** — allowing automatic synchronization between the two platforms.  

---

## 📘 Project Overview

- **Source Repo (GitLab):** `Mirror-repo-gitlab`
- **Destination Repo (GitHub):** `mirror-repo-github`
- **Direction:** Push Mirror (GitLab → GitHub)
- **Author:** [Bhushan Mahajan](https://gitlab.com/Bhushanmahajan)

---

## ⚙️ Step-by-Step Setup Guide

### 🧩 Step 1 — Create a New Blank Project on GitLab
1. Navigate to **Projects → New Project → Create Blank Project**
2. Enter project name → `Mirror-repo-gitlab`
3. Set visibility → **Public**
4. Click **Create Project**

📸 **Screenshot:**  
![GitLab Create Project](images/Gitlab-repo.png)

---

### 🧩 Step 2 — Create a New Repository on GitHub
1. Go to your GitHub profile → **New Repository**
2. Set repository name → `mirror-repo-github`
3. Set visibility → **Public**
4. Optionally add a README
5. Click **Create Repository**

📸 **Screenshot:**  
![GitHub Create Repo](images/mirror-repo-github.png)

---

### 🧩 Step 3 — Configure GitLab Repository Mirroring
1. Open **Settings → Repository → Mirroring Repositories**
2. Click **Add New**
3. Paste your **GitHub repo URL** (e.g., `https://github.com/bhushanmahajan0070/mirror-repo-github.git`)
4. Select **Push direction**
5. Choose **Authentication method → Password / Token**
6. Enter your **GitHub Personal Access Token**
7. Click **Mirror Repository**

📸 **Screenshot:**  
![GitLab Mirror Settings](images/configure.png)

---

### 🧩 Step 4 — Copy GitHub HTTPS URL
From your GitHub repository:
- Click the **Code** button → Copy the HTTPS URL

📸 **Screenshot:**  
![GitHub HTTPS URL](images/github-repo.png)

---

### 🧩 Step 5 — Add and Push Files from Local Machine
Initialize files locally and push to GitLab:

```bash
git status -s
git add .
git commit -m "hi"
git push -u origin main


# 🪞 GitLab → GitHub Repository Mirroring Verification

This documentation verifies that the **GitLab → GitHub mirror setup** works successfully.  
All screenshots below confirm that files pushed from GitLab are reflected automatically on GitHub.

---

## 🧩 Step 6 — Verify on GitHub

After pushing your commits to GitLab, check your **GitHub repository** to confirm that the files and commits have synced automatically.

📸 **Screenshot:**  
![GitHub Mirror Result](images/push.png)

**Details:**
- Repository: `mirror-repo-github`
- Branch: `main`
- Files synced:  
  - `README.md`  
  - `index.html`
- Commit message: `hi`

✅ The files from GitLab appeared successfully in the GitHub repository.

---

## 🧩 Step 7 — Verify on GitLab

Check your GitLab repository to ensure the same files and commits are present.

📸 **Screenshot:**  
![GitLab Result](images/Screenshot-2025-11-09-104431.png)

**Details:**
- Repository: `Mirror-repo-gitlab`
- Branch: `main`
- Files:  
  - `README.md`  
  - `index.html`
- Commit message: `hi`

✅ The GitLab project shows identical structure and commit details.

---

## 🧩 Step 8 — Git CLI Confirmation

Below is the Git command output showing how the commit and push were done successfully from the local environment.

📸 **Screenshot:**  
![Git CLI Push](images/Screenshot-2025-11-09-104408.png)

**Commands used:**
```bash
git status -s
git add .
git commit -m "hi"
git push -u origin main
