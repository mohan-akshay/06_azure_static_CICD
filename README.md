# 🌐 Azure Static Website with CI/CD

## 📁 Project: Static Web App Deployment with GitHub Integration

### 🎯 Goal

Host a modern static website using **Azure Static Web Apps** with **CI/CD from GitHub**, enabling global content delivery, HTTPS, and auto-deployment on every commit.

---

## 🧠 Topics Covered

- Azure Static Web Apps (Free Tier)
- GitHub Actions (CI/CD)
- Global Hosting via Azure CDN
- Static Website Deployment

---

## 🧰 Tools & Services Used

- **Azure Static Web Apps**
- **GitHub Repository**
- **GitHub Actions (CI/CD Pipeline)**
- **Azure Portal**

---

## 📘 Summary

This project demonstrates how to deploy a static site (HTML/CSS/JS or SPA like React/Vue) directly from GitHub to **Azure Static Web Apps**, leveraging built-in GitHub Actions for continuous deployment.

Your site is:
- Live on a globally distributed CDN
- Auto-updated with each Git push
- Protected with free HTTPS

---

## 📌 Scenario

You're building a portfolio or marketing page and want:
- ⚡ Instant global load times
- 🔁 CI/CD from GitHub
- 🔒 HTTPS encryption
- 💰 Zero infrastructure cost

---

## 🛠️ Implementation Steps

### 1. Prepare GitHub Repository

- Push your static site (e.g., `index.html`, `style.css`, etc.) to GitHub  
- Root structure:
`
/index.html
/about.html
/assets/

`


### 2. Create Azure Static Web App

- Go to [Azure Portal](https://portal.azure.com)
- Search: **Static Web Apps** → **+ Create**
- Fill the form:
- **Resource Group**: `az900-staticweb-rg`
- **Name**: `my-portfolio-site`
- **Plan Type**: Free
- **Region**: closest to your users
- **Source**: GitHub
- **Repo**: select your GitHub repo
- **Branch**: `main`
- **App location**: `/`
- **Output location**: `/`
- Click **Review + Create** → **Create**

### 3. GitHub CI/CD Auto-Generated

- Azure will auto-create a GitHub Action in `.github/workflows/azure-static-web-apps.yml`
- On any push to `main`, your site will auto-build and deploy!

### 4. Access Your Website

- Find the URL in your Static Web App resource  
Example:  `https://<random-name>.azurestaticapps.net`

- Test updates by pushing changes to GitHub

---

## 🌐 (Optional) Custom Domain + HTTPS

1. Go to your Static Web App in Azure  
2. Select **Custom Domains** → **Add**  
3. Follow the DNS instructions (CNAME)  
4. Azure provides **free SSL certs** automatically

---

## 🧪 Example Output

![screenshot](screenshots/website-homepage.png)

---

## 🚀 Outcome

- ✅ Hosted static site globally
- ✅ CI/CD pipeline from GitHub
- ✅ HTTPS and fast CDN delivery
- ✅ Ready for custom domain

---

## 🧹 Cleanup (If needed)

To remove and avoid future charges:

- Go to: **Azure Portal** → **Resource Groups**
- Select: `az900-staticweb-rg`
- Click: **Delete Resource Group**

---

## 🏁 Final Thoughts

This project shows the power of **serverless web hosting**. No need to manage infrastructure — just push code and go live! It’s perfect for:

- Portfolios
- Blogs
- Landing pages
- Marketing websites

---

