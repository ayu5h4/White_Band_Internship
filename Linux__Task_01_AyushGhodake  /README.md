# Linux Task 01: Linux Environment Setup & Essential Commands

## Objective

The purpose of this task is to become familiar with the Linux operating system, terminal interface usage, directory navigation, and core file management utilities. Linux serves as a fundamental environment for Cyber Security professionals, System Administrators, and Ethical Hackers.

---

## 🖥️ Part A: Linux Installation & Verification

For this environment setup, **Kali Linux** was successfully deployed inside a virtual machine (VM) container.

### System Verification Screenshots

* [x] Desktop Environment initialized

![Desktop Environment](./Screenshots/Desktop.png)

* [x] Active Terminal window functional

![Active Terminal window](./Screenshots/Terminal.png)

* [x] Base system parameters verified
 
![Base system parameters verified](./Screenshots/SystemInfo.png)
---

## 🧭 Part B: Basic Navigation Commands

The execution metrics for foundational shell traversal commands inside the bash environment are detailed below:

* **`pwd` (Print Working Directory):**

  * **Purpose:** Displays the absolute directory path of the current shell focus.
  * **Output Example:** `/home/kali`

 ![Commands](./Screenshots/pwd.png)

* **`ls` (List Storage Contents):**

  * **Purpose:** Lists non-hidden files and subdirectories located within the current working folder.

* **`ls -la` (List All Long Format):**

  * **Purpose:** Lists all system file elements in long-form details, including hidden configuration files (those prefixed with a dot `.`), along with permissions, file sizes, ownership information, and modification timestamps.

![Commands](./Screenshots/ls.png)

* **`cd` (Change Directory):**

  * **Purpose:** Changes the current shell context to a specified directory. Running it without parameters returns the user to the home directory (`~`).

* **`clear` (Reset Screen):**

  * **Purpose:** Clears previous terminal output from the visible screen, providing a clean workspace.

* **`history` (Command Log Review):**

  * **Purpose:** Displays a chronological list of previously executed commands in the current shell session.

![Commands](./Screenshots/history.png)

* **`whoami` (Identity Verification):**

  * **Purpose:** Displays the username of the currently logged-in user.
  * **Output:** `kali`

* **`hostname` (Device Domain ID):**

  * **Purpose:** Displays the logical name assigned to the local device or virtual machine.
  * **Output:** `kali`

---
## 📁 Part C: Directory Management

The directory hierarchy was created using the `mkdir` utility with the `-p` option, which automatically generates parent directories when they do not already exist.

### 1. Directory Creation Commands

```bash
mkdir -p "Cyber Security_Lab/Networking"
mkdir -p "Cyber Security_Lab/Linux/Cyber Security/Ethical Hacking"
mkdir -p "Cyber Security_Lab/Linux/Reports"
```

### 2. Directory Structure Verification

The `tree` command was used to display and verify the complete directory hierarchy:

```bash
tree "Cyber Security_Lab"
```

### 3. Resulting Directory Structure

```text
Cyber Security_Lab/
├── Networking/
└── Linux/
    ├── Cyber Security/
    │   └── Ethical Hacking/
    └── Reports/
```
![Directory Structure](./Screenshots/DirectoryTree.png)

### 4. Operations Summary

* Created the root directory `Cyber Security_Lab`.
* Generated the `Networking` subdirectory.
* Built a nested directory path for `Linux/Cyber Security/Ethical Hacking`.
* Created the `Reports` directory under the Linux section.
* Verified the final directory hierarchy using the `tree` utility.

## 📄 Part D: File Management

File management operations were performed within the `Cyber Security_Lab` workspace using standard Linux utilities. These commands were used to create, copy, move, rename, and delete files while maintaining an organized directory structure.

### 1. File Management Commands Used

#### Creating Files

The `touch` command was used to create empty files for storing notes, commands, and reports.

```bash
touch "Cyber Security_Lab/Linux/notes.txt"
touch "Cyber Security_Lab/Linux/commands.txt"
touch "Cyber Security_Lab/Linux/report.txt"
```

#### Copying Files

The `cp` command was used to create a duplicate copy of `notes.txt` in the Networking directory.

```bash
cp "Cyber Security_Lab/Linux/notes.txt" "Cyber Security_Lab/Networking/"
```

#### Moving Files

The `mv` command was used to move the report file into the dedicated Reports directory.

```bash
mv "Cyber Security_Lab/Linux/report.txt" "Cyber Security_Lab/Linux/Reports/"
```

#### Renaming Files

The `mv` command was also used to rename `commands.txt` to `linux_commands.txt`.

```bash
mv "Cyber Security_Lab/Linux/commands.txt" "Cyber Security_Lab/Linux/linux_commands.txt"
```

#### Deleting Files

The `rm` command was used to remove the temporary `notes.txt` file after completing the required operations.

```bash
rm "Cyber Security_Lab/Linux/notes.txt"
```

### 2. Operations Summary

* Created `notes.txt`, `commands.txt`, and `report.txt` using the `touch` command.
* Copied `notes.txt` to the `Networking` directory using `cp`.
* Moved `report.txt` to the `Linux/Reports` directory using `mv`.
* Renamed `commands.txt` to `linux_commands.txt`.
* Removed the temporary `notes.txt` file using `rm`.

### File Management Verification Screenshot

![ File Management](./Screenshots/DirectoryMGT.png)

## 📊 Part E: System Information Collection

The system diagnostic evaluations and configuration parameters pulled directly from the virtual machine environment terminal window reveal the following exact environment telemetry variables:  

* **Kernel Version:** `Linux kali 6.x-amd64`
* **Username:** `kali`
* **Current Directory Context:** `/home/kali`
* **Current Date and Time:** *Tue Jun  9 08:24:34 AM EDT 2026*
* **System Uptime Status:** Running continuously since current hypervisor initialization runtime logs 08:24:53 up  1:12,  1 user,  load average: 0.03, 0.02, 0.00
---

### System Diagnostic Verification Screenshot
The terminal execution window capture below explicitly validates the extraction of the telemetry variables listed above via standard system information utility commands (`uname -a`, `hostname`, `whoami`, `date`, `uptime`, and `pwd`):

![System Information Verification](./Screenshots/commands.png)

# Part F: Linux Research Activity

## 1. What is Linux?

Linux is an open-source, Unix-like operating system kernel created by Linus Torvalds in 1991. The kernel serves as the core component that manages communication between software applications and computer hardware. Due to its flexibility and modular design, Linux is used as the foundation for many operating system distributions designed for different purposes.

## 2. Why is Linux Important in Cyber Security?

Linux plays a critical role in cyber security because it provides extensive control over system resources, network configurations, and security settings. Security professionals use Linux to analyze network traffic, manage permissions, perform vulnerability assessments, and develop security tools. Additionally, most servers, cloud platforms, and network devices run Linux, making Linux knowledge essential for protecting modern IT infrastructure.

## 3. Difference Between Linux and Windows

| Feature        | Linux                                                                 | Windows                                                       |
| -------------- | --------------------------------------------------------------------- | ------------------------------------------------------------- |
| Source Code    | Open-source and freely available                                      | Proprietary and closed-source                                 |
| User Interface | Primarily command-line based, with optional GUIs                      | Primarily graphical user interface (GUI)                      |
| Customization  | Highly customizable                                                   | Limited customization                                         |
| Security Model | Strong permission-based access control using root and sudo privileges | Uses User Account Control (UAC) and administrative privileges |
| Cost           | Usually free                                                          | Requires a commercial license                                 |

## 4. What is a Linux Distribution?

A Linux distribution (or distro) is a complete operating system built around the Linux kernel. It includes system utilities, software packages, desktop environments, and package management tools. Different distributions are designed for specific purposes. Examples include Ubuntu for general use, Debian for stability, and Kali Linux for cyber security and penetration testing.

## 5. Why Do Ethical Hackers Prefer Linux-Based Operating Systems?

Ethical hackers prefer Linux-based operating systems because they offer powerful command-line tools, advanced networking capabilities, and extensive customization options. Security-focused distributions such as Kali Linux come pre-installed with penetration testing, vulnerability assessment, and digital forensics tools. Linux also supports scripting and automation, enabling security professionals to perform complex tasks efficiently and effectively.

## Conclusion

Linux is a powerful, secure, and highly customizable operating system that serves as the backbone of modern computing infrastructure. Its widespread use in servers, cloud environments, and cyber security makes it an essential skill for IT professionals and ethical hackers. Understanding Linux fundamentals helps build a strong foundation for system administration, network security, and penetration testing.


