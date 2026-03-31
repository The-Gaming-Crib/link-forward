Here is a complete, professional README.md you can copy and paste directly into your GitHub repository. It covers the logic, the code setup, and the specific steps for both GitHub and Cloudflare.
# 🌐 Multi-Subdomain Redirect Router

A lightweight, client-side redirection engine designed to run on **GitHub Pages**. This tool allows you to host a single website that acts as a traffic controller: detecting which subdomain a user is visiting (e.g., `1.example.com`) and instantly routing them to a specific destination (e.g., `blablabla.example.com`).

---

## 🛠️ How It Works
Since GitHub Pages is a static hosting service, it cannot perform server-side (301) redirects. This project uses a **JavaScript-based Client-Side Redirect**. 

1. The browser hits your GitHub Pages site via a custom subdomain.
2. The script captures the `window.location.hostname`.
3. It looks up that hostname in a "mapping" dictionary.
4. If a match is found, it updates `window.location.href` to the new destination.

---

## 🚀 Quick Setup

### 1. Edit the Router
Open `index.html` and locate the `redirectMap`. Add your source subdomains and their target destinations here:

```javascript
const redirectMap = {
    "1.example.com": "https://blablabla.example.com",
    "2.example.com": "https://blabla2.example.com"
};
```
