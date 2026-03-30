# 🐬 MySQL Installation on Linux

This guide provides a **simple 4-step method** to install **MySQL** on Linux distributions like **Ubuntu/Debian**, **CentOS/RHEL/Rocky Linux**, and **Arch Linux**. Follow these steps to install, start, and secure MySQL quickly.

---

## 🛠 4-Step Installation

```bash
# 1️⃣ Update your system
# Ubuntu/Debian
sudo apt update && sudo apt upgrade -y
# CentOS/RHEL/Rocky
# sudo dnf update -y
# Arch Linux
# sudo pacman -Syu

# 2️⃣ Install MySQL server
# Ubuntu/Debian
sudo apt install mysql-server -y
# CentOS/RHEL/Rocky
# sudo dnf install mysql-server -y
# Arch Linux
# sudo pacman -S mysql

# 3️⃣ Start and enable MySQL service
# Ubuntu/Debian
sudo systemctl start mysql
sudo systemctl enable mysql
# CentOS/RHEL/Arch (replace 'mysql' with 'mysqld' if needed)
# sudo systemctl start mysqld
# sudo systemctl enable mysqld

# 4️⃣ Secure MySQL installation 🔐
sudo mysql_secure_installation

# ✅ Access MySQL
sudo mysql -u root -p

# 🔍 Verify installation
mysql --version

# 🖥 Check Linux distribution
cat /etc/os-release
