# Vim Installation and Usage Guide (Linux / WSL)

## 📌 Overview

**Vim** (Vi IMproved) is a powerful command-line text editor widely used for programming, scripting, and system administration. It is especially useful in Linux-based environments and is commonly used in academic labs and exams.

---

## ⚙️ System Requirements

* Linux Distribution (Ubuntu, Fedora, Arch, etc.)
  **OR**
* Windows with **Windows Subsystem for Linux (WSL)** installed

---

## 🐧 Installation Guide

### 🔹 Ubuntu / Debian (Recommended for beginners)

```bash
sudo apt update
sudo apt install vim -y
```

---

### 🔹 Fedora

```bash
sudo dnf install vim -y
```

---

### 🔹 Arch Linux

```bash
sudo pacman -S vim
```

---

### 🔹 Verify Installation

```bash
vim --version
```

---

## 🚀 Getting Started with Vim

### 📂 Create or Open a File

```bash
vim filename.c
```

---

## ⌨️ Basic Vim Modes

Vim operates in different modes:

### 1. Normal Mode (Default)

* Used for navigation and commands

### 2. Insert Mode

* Press `i` to start typing/editing

### 3. Command Mode

* Press `Esc`, then type commands like `:w`, `:q`

---

## 💡 Essential Commands

| Command | Description           |
| ------- | --------------------- |
| `i`     | Enter insert mode     |
| `Esc`   | Return to normal mode |
| `:w`    | Save file             |
| `:q`    | Quit                  |
| `:wq`   | Save and quit         |
| `:q!`   | Quit without saving   |

---

## 🧑‍💻 Writing a Sample Program (C)

### Step 1: Open file

```bash
vim program.c
```

### Step 2: Enter insert mode

Press:

```
i
```

### Step 3: Write code

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

### Step 4: Save and exit

Press `Esc`, then type:

```
:wq
```

---

## ▶️ Compile and Run Programs

### 🔹 C Program

```bash
gcc program.c -o program
./program
```

---

### 🔹 Bash Script

```bash
chmod +x script.sh
./script.sh
```

---

### 🔹 Python Program

```bash
python3 program.py
```

---

## 🛠️ Useful Tips

* Always press `Esc` before typing commands
* Use `:wq` frequently to save your work
* Practice basic navigation for faster coding
* Vim is lightweight and works well in low-resource environments

---

## 🎯 Conclusion

Vim is an essential tool for developers and students, especially in Linux-based environments. Mastering Vim improves productivity and is highly beneficial for lab exams and real-world programming tasks.

---

## 📚 References

* Vim Official Documentation
* Linux Manual Pages (`man vim`)
