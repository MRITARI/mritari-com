# mritari.com

This repository holds the frontend code and infrastructure setup for my personal website.

---

* **Frontend:** HTML5, Tailwind CSS, Vanilla JavaScript, Service Workers
* **Backend:** Nginx, PHP, Bludit
* **Infrastructure:** Docker Compose, Linux, Cloudflare Tunnels
* **Deployment:** GitHub Actions, Git

---

* **No open ports:** The server doesn't have any inbound ports exposed to the public internet. All web traffic and deployment SSH connections are routed through an encrypted Cloudflare Tunnel.
* **Automated deployments:** Pushing code to the main branch triggers a GitHub Action. It securely tunnels into the server, backs up the current directory, and pulls the new code automatically.

---

* **WAF & Nginx rules:** A Cloudflare Web Application Firewall drops unauthorized access attempts against administrative endpoints and mitigates automated bot traffic, and Nginx is explicitly configured to block all HTTP requests to the backend database folders.