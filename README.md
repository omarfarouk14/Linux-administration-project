# Linux-administration-project
Linux Administration Course Project
# Linux Admin Course Project

This project demonstrates practical Linux administration skills using Bash scripting, C programming, and build systems like Makefiles and CMake. It also includes remote development and system monitoring on Raspberry Pi.

---

## 📁 Project Structure

```plaintext
Linux_Admin_Course_Project/
├── Part1/         
│   ├── userdef.sh            # User Management Script
│   ├── dir_files_manager.sh  # Directory and File Management Script
│
├── Part2/
│   ├── CMakeLists.txt        # CMake build file
│   ├── Makefile              # Makefile build system
│   ├── main.c                # Main encryption/decryption application
│   ├── caesar/               # Caesar Cipher Static Library
│   └── xor/                  # XOR Cipher Dynamic Library
│
├── Part3/
│   ├── monitor.c             # C program using fork() and execv()
│
└── README.md                # Project documentation


## 🧩 Part 1: Bash Scripting for User and File Management

### 1️⃣ `userdef.sh` – User Management Script

- Creates a user with:
  - A specified username, password, and group
  - Assigned UID and GID
- Validates:
  - Script is run with **root** privileges
  - Correct number of arguments
- Includes option to **remove the user and group**

### 2️⃣ `dir_files_manager.sh` – File Management Script

- Creates a directory and generates files inside it
- Compresses the files into a `.tar` archive
- Checks for and removes existing directory/archive if needed
- If a specific user exists:
  - Copies the archive to their home directory
  - Extracts the archive automatically

---

## 🔐 Part 2: Application Development with Makefiles & CMake

This part demonstrates modular C development with both static and dynamic libraries.

### 🧱 Components

- **Main Application** – Handles user input and encryption/decryption
- **Caesar Cipher** – Built as a **Static Library**
- **XOR Cipher** – Built as a **Dynamic Library**

### 🔧 Build System

---

## 🧵 Part 3: Process Management and Remote Execution

A C-based implementation for Linux process management.

- Uses `fork()` and `execv()` to execute:
  - `ps` (Process status)
  - `mpstat` (CPU usage stats)
- Transferred to **Raspberry Pi 5** via `scp`
- Compiled and executed remotely using `ssh`

---

## ✅ Skills Demonstrated

- ✅ Linux Bash scripting (user, group, and file management)
- ✅ Root privilege validation
- ✅ Static and dynamic C libraries
- ✅ Makefile and CMake usage
- ✅ Process creation (`fork`, `execv`)
- ✅ File compression (`tar`)
- ✅ Remote development with Raspberry Pi

---

## 🚀 How to Run

### Part 1 – Bash Scripts

```bash
cd Part1
sudo ./userdef.sh [username] [password] [groupname] [UID] [GID]
sudo ./dir_files_manager.sh [directory_name] [file_count] [target_user]
cd Part2
make          # or use: cmake . && make
./out/main
cd Part3
gcc monitor.c -o monitor
./monitor

Supports building with both `Makefile` and `CMake`.

