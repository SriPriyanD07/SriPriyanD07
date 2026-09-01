# 🚀 How to Publish Your GitHub Profile README

To display this README on your main GitHub profile (`https://github.com/SriPriyanD07`), follow these simple steps:

### Step 1: Create the Special Repository on GitHub
1. Open your browser and go to [https://github.com/new](https://github.com/new).
2. Set the **Repository name** to: `SriPriyanD07` *(must match your GitHub username exactly)*.
3. Make sure **Public** is selected.
4. (Optional) Leave "Add a README file" unchecked (since we already have our custom `README.md` ready).
5. Click **Create repository**.

---

### Step 2: Push Your Local Files to GitHub

Open PowerShell or Terminal in this folder (`c:\Users\Sri Priyan D\OneDrive\Documents\SriPriyanD07`) and run:

```bash
git init
git add .
git commit -m "feat: initial GitHub profile README & workflows"
git branch -M main
git remote add origin https://github.com/SriPriyanD07/SriPriyanD07.git
git push -u origin main
```

*(Alternatively, if you prefer using GitHub Web UI, you can simply create the repository on GitHub with a README and copy-paste the contents of [`README.md`](./README.md) into it).*

---

### 🎉 That's it!
Visit [https://github.com/SriPriyanD07](https://github.com/SriPriyanD07) to see your new interactive profile!
