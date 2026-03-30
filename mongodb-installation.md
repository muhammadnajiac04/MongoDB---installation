# MongoDB Installation on Linux (Ubuntu/Debian)

## 📌 Overview

MongoDB is a NoSQL database that stores data in JSON-like documents (BSON format).
This guide explains how to install, start, and test MongoDB on a Linux system.

---

## ⚙️ Prerequisites

* Ubuntu/Debian-based Linux system
* Internet connection
* Sudo privileges

---

## 🟢 Step 1: Import MongoDB GPG Key

```bash
wget -qO - https://www.mongodb.org/static/pgp/server-6.0.asc | sudo apt-key add -
```

### 🔍 Description:

This command adds the official MongoDB GPG key to your system.
It ensures that the packages you install are authentic and secure.

---

## 🟢 Step 2: Add MongoDB Repository

```bash
echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu \
$(lsb_release -cs)/mongodb-org-6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list
```

### 🔍 Description:

This command adds the MongoDB repository to your system so that you can install MongoDB using `apt`.

---

## 🟢 Step 3: Update Package List

```bash
sudo apt update
```

### 🔍 Description:

Updates the package list to include the MongoDB repository.

---

## 🟢 Step 4: Install MongoDB

```bash
sudo apt install -y mongodb-org
```

### 🔍 Description:

Installs MongoDB server, client tools, and related packages.

---

## 🟢 Step 5: Start MongoDB Service

```bash
sudo systemctl start mongod
```

### 🔍 Description:

Starts the MongoDB database service.

---

## 🟢 Step 6: Enable Auto Start

```bash
sudo systemctl enable mongod
```

### 🔍 Description:

Ensures MongoDB starts automatically when the system boots.

---

## 🟢 Step 7: Check MongoDB Status

```bash
sudo systemctl status mongod
```

### 🔍 Description:

Displays the current status of MongoDB.
You should see **active (running)**.

---

## 🧪 Step 8: Open MongoDB Shell

```bash
mongosh
```

### 🔍 Description:

Launches the MongoDB shell to interact with the database.

---

## 🧪 Basic Test Commands

```js
show dbs
use collegeDB

db.students.insertOne({
  name: "Arun",
  age: 22,
  dept: "MCA"
})

db.students.find()
```

### 🔍 Description:

* `show dbs` → Lists databases
* `use collegeDB` → Creates/uses a database
* `insertOne()` → Inserts a document
* `find()` → Retrieves data

---

## ⚠️ Common Errors and Fixes

### ❌ MongoDB not starting

```bash
sudo systemctl restart mongod
```

### ❌ Port already in use (27017)

```bash
sudo lsof -i :27017
```

### ❌ Permission issues

```bash
sudo chown -R mongodb:mongodb /var/lib/mongodb
```

---

## 🎯 Viva Questions

* Default MongoDB port → **27017**
* Data format → **BSON**
* Service name → **mongod**
* Shell command → **mongosh**

---

## ✅ Conclusion

MongoDB is successfully installed and tested.
You can now perform CRUD operations and use it for DBMS lab experiments.
