# 🚀 Ansible Role – HTTPD Installation & Deployment

This project demonstrates how to **install, start, enable, and deploy Apache HTTPD** using a **custom Ansible role**.
It follows **Ansible best practices** by separating orchestration (playbook) and implementation (role).

🔗 **GitHub Repository:**
👉 [https://github.com/aniket-jagadale/ansible-role-installation-HTTPD.git](https://github.com/aniket-jagadale/ansible-role-installation-HTTPD.git)

---

## 📌 Project Overview

This Ansible project:

* Installs **Apache HTTPD**
* Starts and enables the **httpd service**
* Deploys a custom **index.html** file
* Uses a **role-based structure** for reusability and scalability

The playbook runs on **localhost** and is ideal for:

* Learning Ansible roles
* DevOps practice
* Automation demos
* Interview preparation

---

## 🛠️ Technologies Used

* **Ansible**
* **Apache HTTPD**
* **YAML**
* **Linux (RHEL / Amazon Linux compatible)**

---

## 📂 Project Structure

```text
httpd/
├── README.md
├── defaults/
│   └── main.yml
├── files/
│   └── index.html
├── handlers/
│   └── main.yml
├── meta/
│   └── main.yml
├── tasks/
│   └── main.yml
├── templates/
├── tests/
│   ├── inventory
│   └── test.yml
└── vars/
    └── main.yml
```

---

## 📜 Playbook Used

```yaml
---
- name: Install httpd using a role
  hosts: localhost
  become: yes
  vars:
    pkg: httpd
    svc: httpd
    file_path: /var/www/html

  roles:
    - httpd
```

---

## 📋 Role Tasks (`roles/httpd/tasks/main.yml`)

* Install Apache HTTPD
* Start and enable the service
* Deploy `index.html` to `/var/www/html`

---

## ▶️ How to Run the Project

### 1️⃣ Clone the repository

```bash
git clone https://github.com/aniket-jagadale/ansible-role-installation-HTTPD.git
cd ansible-role-installation-HTTPD
```

### 2️⃣ Run syntax check

```bash
ansible-playbook ap_with_role.yml --syntax-check
```

### 3️⃣ Execute the playbook

```bash
ansible-playbook ap_with_role.yml
```

---

## ✅ Execution Proof

Below is the successful execution output showing:

* Syntax check passed
* HTTPD installed
* Service started and enabled
* index.html deployed
* No failures

![Ansible HTTPD Role Execution](1687f1ab-ab31-4e09-bc7f-5394d4d85691.png)

---

## 🌐 Verification

After execution, open in browser:

```
http://localhost
```

You should see the deployed **index.html** page.

---

## ⭐ Best Practices Followed

✔ Role-based architecture
✔ Idempotent tasks
✔ Variables for flexibility
✔ Clean directory structure
✔ Compatible with production standards

---

## 👨‍💻 Author

**Aniket Jagadale**
🔗 GitHub: [https://github.com/aniket-jagadale](https://github.com/aniket-jagadale)

---

## 📌 Future Enhancements

* Add handlers for service restart
* Support multiple OS families
* Add CI pipeline for linting
* Convert to Galaxy-ready role

---

If you want, I can also:

* ⭐ Optimize this README for **DevOps resume ATS**
* 📦 Prepare **Ansible Galaxy–ready metadata**
* 🧪 Add **Molecule testing**
* 📝 Write **interview explanation**

Just tell me 👍
