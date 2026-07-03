# React CI/CD Pipeline Tutorial & Sandbox 🚀

Welcome to the React + GitHub Actions CI/CD Sandbox! This project is designed as an educational tool to learn, inspect, and simulate how Continuous Integration (CI) and Continuous Delivery (CD) pipelines work in modern web development.

The application includes an **Interactive CI/CD Pipeline Simulator** that teaches the pipeline stages in real time right in the browser!

---

## 🛠️ Tech Stack & Architecture

- **Frontend Framework**: React 19 + Vite (fast developer tooling & light bundle size)
- **Deployment Platform**: GitHub Pages (fully integrated with GitHub Actions)
- **CI/CD Pipeline**: GitHub Actions

---

## 🚀 Step-by-Step: How to Make this Site Live

To trigger the real GitHub Actions CI/CD pipeline and publish this website, follow these steps:

### 1. Enable GitHub Actions for GitHub Pages (One-time setup)
Before pushing, you must tell GitHub to build and deploy Pages using GitHub Actions:
1. Open your repository page on GitHub: `https://github.com/ponaalagar/ci-cd`
2. Go to **Settings** (top tab navigation).
3. Click **Pages** in the left sidebar menu.
4. Under **Build and deployment** -> **Source**, select **GitHub Actions** from the dropdown menu (instead of "Deploy from a branch").

### 2. Stage and Commit Your Code
Run these commands in your local project terminal:
```bash
git add .
git commit -m "feat: setup interactive CI/CD sandbox and GitHub Actions workflow"
```

### 3. Push to GitHub
Publish the commits to trigger the pipeline:
```bash
git push origin main
```

### 4. Monitor the Build & Go Live!
1. Go to the **Actions** tab in your GitHub repository.
2. You will see a workflow named `Deploy React App to GitHub Pages` start running automatically.
3. Once the workflow turns green (Success), your site is live! You can visit it at:
   `https://ponaalagar.github.io/ci-cd/`

---

## 💻 Local Development Commands

If you want to run the project locally on your machine:

| Command | Description |
| :--- | :--- |
| `npm install` | Installs all required project dependencies |
| `npm run dev` | Runs the app in development mode at `http://localhost:5173` |
| `npm run lint` | Runs the static code quality checks (ESLint) |
| `npm run build` | Compiles the React production bundle into static assets inside `dist/` |
| `npm run preview` | Previews the compiled production build locally |

---

## 🎓 Classroom Demonstration Ideas

- **Demonstrate a Successful Build**: Show the pipeline running automatically on push and deploying.
- **Demonstrate a Blocked Build (Lint Failure)**: 
  - Go to `src/App.jsx` and add an unused variable (e.g. `const unusedVariable = "break-me";`).
  - Try to commit and push this.
  - Show your classmates how the lint job (`npm run lint`) fails on GitHub Actions, halting the pipeline and preventing the bad code from deploying to production!
