# 🧰 DevOps Install Recipes

A living collection of **copy-paste installation guides** (and scripts) for common DevOps tools on **Ubuntu, CentOS, and Red Hat**. I update this repo frequently—each guide is short, repeatable, and works on a clean VM.

---

## 📦 What’s inside (quick links)

- [Connect_Remote_Machine](./Connect_Remote_Machine) — SSH setup, firewall ports, key auth
- [Docker_Ubuntu](./Docker_Ubuntu) — Docker Engine + Compose on Ubuntu
- [Docker_Redhat](./Docker_Redhat) — Docker (or Podman notes) on RHEL
- [Jenkins_Ubuntu_CentOS](./Jenkins_Ubuntu_CentOS) — Jenkins LTS, service setup, plugins
- [Minikube_Ubuntu](./Minikube_Ubuntu) — Minikube + kubectl + drivers on Ubuntu
- [Minikube_CentOS](./Minikube_CentOS) — Minikube + kubectl on CentOS

> 📁 Each item is a **single file** with steps and/or an executable script. Open it to view commands; if it’s a script, you can run it directly (see below).

---

## ✅ Support matrix

| Guide                    | Ubuntu | CentOS | Red Hat |
|--------------------------|:-----:|:-----:|:------:|
| Connect_Remote_Machine   |  ✅   |  ✅   |   ✅   |
| Docker_Ubuntu            |  ✅   |  ❌   |   ❌   |
| Docker_Redhat            |  ❌   |  ❌   |   ✅   |
| Jenkins_Ubuntu_CentOS    |  ✅   |  ✅   |   ❌   |
| Minikube_Ubuntu          |  ✅   |  ❌   |   ❌   |
| Minikube_CentOS          |  ❌   |  ✅   |   ❌   |

---

## 🚀 How to use any guide

1. **Pick a file** for your OS/tool (e.g., `Docker_Ubuntu`).  
2. **Open it** and follow the commands **line-by-line** — **or** run the script if executable:

```bash
chmod +x Docker_Ubuntu
sudo ./Docker_Ubuntu
```

3. **Reboot** if the guide says so (e.g., after kernel/driver installs).

### Prereqs

- Fresh VM or snapshot
- `sudo` privileges
- Internet access + open firewall ports (SSH: 22, Jenkins: 8080, Docker registries, etc.)

---

## 🧪 Quick sanity checks (per tool)

**Docker**
```bash
docker --version && docker run --rm hello-world
```

**Jenkins**
```bash
# Visit http://<host>:8080
# Unlock with the initial admin password:
cat /var/lib/jenkins/secrets/initialAdminPassword
```

**Minikube**
```bash
minikube start && kubectl get nodes
```

---

## 🔄 Updates & contributions

- I update these guides regularly as package sources and best practices change.  
- See something to improve? **Issues/PRs are welcome.**
  - Keep steps idempotent and tested on a clean VM.
  - Note OS version(s) verified (e.g., Ubuntu 22.04, CentOS 7/8, RHEL 9).

---

## ⚠️ Disclaimer

These scripts/steps are provided **as-is**. Run them on disposable VMs or after taking a snapshot. Always review commands before execution in production environments.
