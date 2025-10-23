# 🚀 CI/CD Deployment for cPanel

Implementing **CI/CD in cPanel** enables automated build, test, and deployment processes directly from a **GitHub repository**.  
With an efficient pipeline integration, every code change can be quickly and consistently deployed to production — improving **reliability, speed,** and **overall application development quality.**

---

## 📦 Project Structure

ci.cd-cpanel/
├── .github/
│ └── workflows/
│ └── deploy.yml # GitHub Actions workflow for CI/CD
├── index.html # Main HTML page
├── style.css # Stylesheet
└── .gitignore # Ignored files list

---

## ⚙️ CI/CD Workflow Overview

This repository uses **GitHub Actions** to automate deployment to a **cPanel** server.  
The workflow file (`.github/workflows/deploy.yml`) triggers automatically when code is pushed to the `main` branch.

### 🔁 Process Overview

1. Detect changes pushed to the `main` branch.
2. Run the CI/CD pipeline on GitHub Actions.
3. Connect securely to your cPanel server using SSH credentials.
4. If the project doesn’t exist on the server → perform `git clone`.
5. If it already exists → perform `git pull` to update code.
6. Deployment completes automatically and efficiently.

---

## 🔐 Required GitHub Secrets

Before deployment, make sure the following **GitHub Secrets** are configured:

| Secret Name       | Description                                                       |
| ----------------- | ----------------------------------------------------------------- |
| `SSH_HOST`        | Hostname or IP of your cPanel server                              |
| `SSH_USERNAME`    | SSH username                                                      |
| `SSH_PRIVATE_KEY` | Private SSH key for authentication                                |
| `SSH_PASSPHRASE`  | (Optional) Passphrase for private key                             |
| `SSH_PARENT_DIR`  | Parent directory on the server where the project will be deployed |

---

## 🧰 Technologies Used

- **GitHub Actions** — Continuous Integration & Deployment
- **cPanel** — Hosting environment
- **SSH** — Secure connection between GitHub and server
- **HTML / CSS** — Frontend assets for deployment

---

## 🚀 Benefits

- **Automated Deployment** — Push changes and let GitHub Actions handle the rest.
- **Consistency** — Every deployment follows the same automated process.
- **Speed** — Faster releases without manual uploads.
- **Security** — SSH-based connection ensures a secure deployment channel.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**98hub**  
Automating web deployment for faster and more reliable workflows.  
🌐 [GitHub Profile](https://github.com/98hub)
