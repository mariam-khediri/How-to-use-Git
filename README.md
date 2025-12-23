
# 🚀 How to Use Git

This is a simple guide to help you use Git for managing and pushing your projects to GitHub.

---

## ✅ Initial Setup

1. **Navigate to your project folder using Git Bash:**
   ```bash
   cd path/to/your-folder
   ```

2. **Initialize a Git repository** (do this only once in your local project):
   ```bash
   git init
   ```

3. **Add files to staging:**
   - To add a specific file:
     ```bash
     git add file_name
     ```
   - To add all files in the folder:
     ```bash
     git add .
     ```

4. **Commit your changes with a message:**
   ```bash
   git commit -m "Message describing what you uploaded"
   ```

5. **Set the branch name to `main` (do this only once):**
   ```bash
   git branch -M main
   ```

6. **Link your local repo to your GitHub repository:**
   ```bash
   git remote add origin https://github.com/your-username/your-repo.git
   ```

7. **Pull existing content from GitHub (e.g., README) before the first push:**
   ```bash
   git pull origin main --rebase
   ```

8. **Push your changes to GitHub:**
   ```bash
   git push -u origin main
   ```

---

## 📁 Creating Empty Subfolders in GitHub

Git does not track empty folders by default. To include them, add a hidden `.gitkeep` file to each empty folder:

```bash
touch folder1/subfolder11/.gitkeep
touch folder1/subfolder12/.gitkeep
touch folder2/subfolder21/.gitkeep
```

These `.gitkeep` files act as placeholders so the folders appear in your GitHub repo.

---

## ✏️ Adding Files Later

When you add new files to any folder, use the following steps:

```bash
git add folder1/subfolder11/file-name.py
git commit -m "Progress added"
git push origin main
```

---

### 🧹 Step-by-Step: Remove `.gitkeep` After Adding a Real File

1. **Navigate to the folder**:
   ```bash
   cd folder1/subfolder11
   ```

2. **Delete the `.gitkeep` file**:
   ```bash
   rm .gitkeep
   ```

3. **Stage the deletion** for Git:
   ```bash
   git rm folder1/subfolder11/.gitkeep
   ```

4. **Commit the change**:
   ```bash
   git commit -m "Removed .gitkeep after adding real files"
   ```

5. **Push to GitHub**:
   ```bash
   git push origin main
   ```

---

After this, the folder will still be tracked by Git (and visible on GitHub) **as long as it contains other files**. You’ve just cleaned it up by removing the placeholder.

---

## ✏️ how to modify your repo on github directly from vs code when you don't have the folder locally

### 🟢 SOLUTION 1 _ Clone directy from Github

**🔹 Step 1 — Clone the repo properly **
   ```bash
   cd path to place the new folder
   git clone https://github.com/.... (repo to clone).git
   ```

**🔹 Step 2 — Open in VS Code **
   ```bash
   cd folder name
   code .
   ```
### 🟡 SOLUTION 2 _ Download the repo as zip file
   ```bash
   cd folder name
   git init
   git remote add origin (git repo path.git)
   git add .
   git commit -m "message"
   git pull origin main --allow-unrelated-histories
   ```



