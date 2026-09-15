# Golf-MD-Project
# GOLF Infrastructure Project

> Full-stack application with automated DEV and PROD deployment infrastructure.

### authorship + version

`@sclary2001` | `2026-09-14` | `GOLF`

### deployments, codebase, & repo features

| resource                   | link                                                                                      |
| -------------------------- | ----------------------------------------------------------------------------------------- |
| PROD codebase              | [`main`](https://github.com/sclary2001/GOLF/tree/main)                                    |
| PROD server                | `GCP_PROD_URL_HERE`                                                                       |
| DEV codebase               | [`dev`](https://github.com/sclary2001/GOLF/tree/dev)                                      |
| DEV server                 | `RENDER_DEV_URL_HERE`                                                                     |
| docs                       | [`docs/`](https://github.com/sclary2001/GOLF/tree/main/docs)                              |
| published docs             | `GITHUB_PAGES_URL_HERE`                                                                   |
| CI/CD workflow             | [`deploy.yml`](https://github.com/sclary2001/GOLF/blob/main/.github/workflows/deploy.yml) |
| successful PROD deployment | `SUCCESSFUL_GITHUB_ACTION_URL_HERE`                                                       |
| resolved GOLF issue        | `GOLF_ISSUE_URL_HERE`                                                                     |

### user story

* **As a** burgeoning full-stack developer,
* **I want** a CI/CD infrastructure
* **so that** I can develop locally, manage my code in GitHub, and
  automatically deploy changes to DEV and PROD environments.

### narrative

This project demonstrates a full-stack development and deployment workflow using GitHub, Render, and Google Cloud Platform. The application is developed locally and pushed to the `dev` branch for automatic deployment to the Render DEV environment, while changes merged into `main` trigger GitHub Actions to deploy the production application to a GCP virtual machine. Nginx, PM2, HTTPS, and Node.js/Express are used to provide a reliable production environment.

### architecture

```text
LOCAL
  │
  ▼
GitHub
  │
  ├── dev  ──► Render ─────────────► DEV
  │
  └── main ──► GitHub Actions ─────► GCP ──► Nginx ──► PM2 ──► PROD
```

### stack

`HTML/CSS/JS` | `Node.js` | `Express` | `Git/GitHub` | `Render` |
`GCP` | `Linux` | `Nginx` | `PM2` | `Certbot` | `GitHub Actions`

### project structure

```text
GOLF/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── docs/
│   └── README.md
├── public/
│   ├── index.html
│   ├── css/
│   │   └── styles.css
│   ├── js/
│   │   └── app.js
│   └── assets/
├── server/
│   ├── server.js
│   └── package.json
├── .gitignore
├── package.json
└── README.md
```

### GCP

external IP: `GCP_EXTERNAL_IP_HERE`
Linux user: `GCP_LINUX_USERNAME_HERE`
instructor SSH public key installed: `yes`

### grading checkpoints

* [x] Repository uses `public/` and `server/`
* [x] `node_modules/` is excluded from Git
* [ ] Push to `dev` automatically deploys to Render DEV
* [ ] Push to `main` triggers GitHub Actions
* [ ] GitHub Actions deploys to GCP PROD
* [ ] PROD uses assigned subdomain + HTTPS
* [ ] Nginx reverse proxy is running
* [ ] PM2 is running the Node.js application
* [ ] Successful PROD GitHub Action is linked above
* [ ] A real GOLF problem is documented in a closed GitHub Issue
* [ ] GCP VM remains running from submission until graded

### security

No passwords, private SSH keys, GitHub tokens, repository secrets, `.env` values, or other sensitive credentials are stored in this repository.

### GOLF issue

A real deployment or infrastructure problem encountered during development will be documented in a GitHub Issue and resolved before submission.

**Resolved Issue:** `GOLF_ISSUE_URL_HERE`

### production verification

Production will be verified after a successful GitHub Actions deployment. The deployed change must be visible on the production server and the application must be accessible through the assigned HTTPS subdomain.
