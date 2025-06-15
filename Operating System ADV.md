# Essential Duties of a System Administrator

## 1. Controlling Access
- Create and remove user accounts.
- Handle account-related issues (e.g., forgotten passwords, lost keys).
- Use configuration management or directory services for automation.

	## 2. Adding Hardware
- Install and configure new hardware (e.g., NICs, storage arrays).
- Ensure OS-level recognition and integration.

## 3. Automating Tasks
- Use scripting languages and automation tools to:
  - Increase efficiency
  - Reduce human error
  - Rapidly adapt to new requirements

## 4. Overseeing Backups
- Regularly back up systems and data.
- Test restore procedures.
- Use built-in OS tools and third-party solutions.

## 5. Installing and Upgrading Software
- Select, install, and configure software across systems.
- Manage patches and updates securely.
- Support continuous delivery pipelines.

## 6. Monitoring
- Track system performance and service availability.
- Analyze logs and resource usage.
- Automate alerting and recovery procedures.

## 7. Troubleshooting
- Diagnose and resolve unexpected system failures.
- Collaborate with subject-matter experts when needed.

## 8. Maintaining Local Documentation
- Document configurations, scripts, and vendor decisions.
- Use diagrams (e.g., network diagrams) where helpful.

## 9. Vigilantly Monitoring Security
- Enforce security policies and access controls.
- Set up monitoring, auditing, and intrusion detection.
- Champion security awareness and practices.

## 10. Tuning Performance
- Adjust system parameters for optimal performance.
- Respond to user needs and infrastructure constraints.

## 11. Developing Site Policies
- Assist in policy creation for:
  - Acceptable use
  - Data retention
  - Privacy and compliance

## 12. Working with Vendors
- Select vendors and negotiate contracts.
- Implement vendor-supported solutions.

## 13. Fire Fighting
- Handle day-to-day support requests and user issues.
- Maintain a helpful and professional demeanor.

| Distribution        | Website               | Comments                                              |
|---------------------|------------------------|--------------------------------------------------------|
| Arch                | [archlinux.org](https://archlinux.org)       | For those who fear not the command line               |
| CentOS              | [centos.org](https://centos.org)             | Free analog of Red Hat Enterprise                     |
| CoreOS              | [coreos.com](https://coreos.com)             | Containers, containers everywhere                     |
| Debian              | [debian.org](https://debian.org)             | Free as in freedom, most GNUish distro                |
| Fedora              | [fedoraproject.org](https://fedoraproject.org)| Test bed for Red Hat Linux                            |
| Kali                | [kali.org](https://kali.org)                 | For penetration testers                               |
| Linux Mint          | [linuxmint.com](https://linuxmint.com)       | Ubuntu-based, desktop-friendly                        |
| openSUSE            | [opensuse.org](https://opensuse.org)         | Free analog of SUSE Linux Enterprise                  |
| OpenWRT             | [openwrt.org](https://openwrt.org)           | Linux for routers and embedded devices                |
| Oracle Linux        | [oracle.com](https://oracle.com)             | Oracle-supported version of RHEL                      |
| RancherOS           | [rancher.com](https://rancher.com)           | 20MiB, everything in containers                       |
| Red Hat Enterprise  | [redhat.com](https://redhat.com)             | Reliable, slow-changing, commercial                   |
| Slackware           | [slackware.com](https://slackware.com)       | Grizzled, long-surviving distro                       |
| SUSE Linux Enterprise| [suse.com](https://suse.com)               | Strong in Europe, multilingual                        |
| Ubuntu              | [ubuntu.com](https://ubuntu.com)             | Cleaned-up version of Debian                          |
Here are the notes for **Chapter 1.5 – Notation and Typographical Conventions** formatted in Markdown, suitable for use in **Obsidian**:
# Notation and Typographical Conventions

## Command and Argument Formatting
- **Boldface** is used for:
  - Filenames
  - Commands
  - Literal arguments

- *Italics* are used for:
  - Placeholders that should be replaced with actual values

> Example: `cp *file* *directory*`  
> Replace *file* and *directory* with actual file/directory names.

## Code Font
- Used for:
  - Configuration file excerpts
  - Terminal session output
  - Annotated with `#` for bash comments

```bash
$ grep Bob /pub/phonelist  # Look up Bob's phone number
Bob Knowles 555-2834
Bob Smith   555-2311
````

## Shell Prompt Conventions

- `$` indicates normal user
    
- `#` indicates root user
    
- Distro-specific prompts (e.g., `debian#`) indicate distribution context
    

```bash
$ sudo su -         # Become root
# passwd            # Change root's password
debian# dpkg -l     # List installed packages on Debian/Ubuntu
```

## Command Syntax Notation (UNIX Manual Style)

- `[...]` — Optional elements
    
- `{item1 | item2}` — Choose one of the options
    
	- `...` — Indicates repetition
	    

> Example:
> 
> ```
> bork [ -x ] { on | off } filename ...
> ```

Valid forms:

```bash
bork on /etc/passwd
bork -x off /etc/passwd /etc/smartd.conf
bork off /usr/lib/tmac
```

## Shell-style Globbing

- `*` — Matches zero or more characters
    
- `?` — Matches exactly one character
    
- `~` — Home directory of current user
    
- `~user` — Home directory of the specified user
    

> Example:  
> `/etc/rc*.d` matches `/etc/rc0.d`, `/etc/rc1.d`, etc.

## Punctuation and Quotation

- Quotation marks around technical terms indicate specific meanings.
    
- Punctuation is placed **outside** quotes to avoid ambiguity.
    

---

Let's break down **shell-style globbing**—a powerful feature in UNIX/Linux shells (like `bash`) that helps you match filenames and directories using patterns. Here's how each pattern works with clear examples.

---

## 🔹 What is Shell-style Globbing?

"Globbing" means using special wildcard characters to match files and paths without needing exact names. It's especially useful when you work with many files at once.

---

## `*` – Match Zero or More Characters

- **Usage**: Matches any number (including zero) of characters **except `/`**.
    

### 📂 Example:

Suppose your directory contains:

```
report.txt
report_2024.pdf
notes.txt
summary.doc
```

### 🔍 Pattern:

```bash
ls report*
```

### ✅ Matches:

```
report.txt
report_2024.pdf
```

**Explanation**: `*` matches anything after `report`.

---

## `?` – Match Exactly One Character

- **Usage**: Matches exactly one character **except `/`**.
    

### 📂 Example:
	
Files in directory:

```
a.txt
ab.txt
abc.txt
```

### 🔍 Pattern:

```bash
ls a?.txt
```

### ✅ Matches:

```
ab.txt
```

**Explanation**: `?` matches one character (`b`) after `a`.

---

## `~` – Home Directory of Current User

- **Usage**: `~` is shorthand for your home directory.
    
- If your username is `alice`, `~` = `/home/alice` or `/Users/alice` (on macOS).
    

### 📂 Example:

```bash
cd ~
```

**Goes to**:

```
/home/yourusername
```

---

## `~user` – Home Directory of a Specific User

- **Usage**: Access another user's home directory if permissions allow.
    

### 📂 Example:

```bash
cd ~bob
```

**Goes to**:

```
/home/bob
```

(if `bob` is a valid user)

---

## 🧠 Summary Table

| Pattern | Meaning                        | Example     | Matches                        |
| ------- | ------------------------------ | ----------- | ------------------------------ |
| `*`     | Zero or more characters        | `file*`     | `file1`, `file_report`, `file` |
| `?`     | Exactly one character          | `file?.txt` | `file1.txt`, `fileA.txt`       |
| `~`     | Current user's home directory  | `cd ~`      | `/home/you`                    |
| `~user` | Specific user's home directory | `cd ~bob`   | `/home/bob`                    |

---
# 📏 Units – Metric vs Binary Prefixes in Computing

## 🔹 Metric vs Binary Prefixes

### 🔸 Metric Prefixes (Base 10)
- Common in general science and networking.
- Based on powers of 10:
  - **kilo-** (k) = 10³ = 1,000
  - **mega-** (M) = 10⁶ = 1,000,000
  - **giga-** (G) = 10⁹ = 1,000,000,000

### 🔸 Binary Prefixes (Base 2)
- Used in memory, filesystems, and hardware design.
- Based on powers of 2:
  - **kibi-** (Ki) = 2¹⁰ = 1,024
  - **mebi-** (Mi) = 2²⁰ = 1,048,576
  - **gibi-** (Gi) = 2³⁰ = 1,073,741,824

> ⚠️ Note: Traditional computing often used metric prefixes (e.g., MB) for binary values, leading to confusion.

---

## 🔹 Use Context Matters

| Domain           | Unit System     |
|------------------|------------------|
| **RAM**          | Binary (KiB, MiB, etc.) |
| **Network Speed**| Metric (Kb/s, Mb/s, etc.) |
| **Disk Storage** | Metric (though some block/page sizes use binary) |
| **Rough Values** | Metric or ambiguous (context-dependent) |

---

## 🔹 Abbreviations Used

| Unit     | Meaning         |
|----------|------------------|
| `b`      | Bit              |
| `B`      | Byte             |
| `KiB`    | 1,024 bytes      |
| `MiB`    | 1,048,576 bytes  |
| `GiB`    | 1,073,741,824 bytes |

---

## 🔹 About “K” in Computer Terminology

- **"K"** originally meant **1,024** in computing (e.g., `8KB of RAM`).
- But **"k"** in metric stands for **1,000**.
- The upper-case `K` doesn’t scale cleanly with larger units (M, G, etc.).
- Now it's used inconsistently; **context is key**.

---

## 🔹 Examples from Table 1.2

| Example               | Meaning / Comment                                           |
|------------------------|-------------------------------------------------------------|
| `1kB file`            | 1,000 bytes                                                 |
| `4KiB SSD pages`      | 4,096 bytes                                                 |
| `8KB of memory`       | Ambiguous / Not used in this book                          |
| `100MB file limit`    | Nominally 100,000,000 bytes; ambiguous context              |
| `100MB disk partition`| Likely ~99,999,744 bytes (aligned to 512-byte blocks)       |
| `1GiB of RAM`         | 1,073,741,824 bytes                                         |
| `1Gb/s Ethernet`      | 1,000,000,000 bits/sec (metric)                            |
| `6TB hard disk`       | ~6,000,000,000,000 bytes (metric)                          |

---

## 🔹 Notes
- **IEC units** (KiB, MiB, etc.) are **unambiguous** and preferred for powers of 2.
- Many Linux tools and distros (like Ubuntu) are starting to adopt these standards.
- See: [Ubuntu Units Policy](https://wiki.ubuntu.com/UnitsPolicy)

---
# 📚 Man Pages and Online Documentation

## 🔸 What Are Man Pages?
- "Man pages" (short for **manual pages**) are the traditional **command-line documentation** in UNIX/Linux.
- Accessed using the `man` command.
- Still widely used due to:
  - Local availability (no internet needed)
  - Authoritative detail
  - Examples and related commands

> 💡 Man pages cover individual programs, system calls, file formats—not general "how-to" topics.

---

## 🔸 Structure of Man Pages

Man pages are organized into **sections**, with each section focusing on different types of content:

| Section | Contents                                |
|---------|-----------------------------------------|
| 1       | User-level commands and applications    |
| 2       | System calls and kernel error codes     |
| 3       | Library calls                           |
| 4       | Device drivers and network protocols    |
| 5       | Standard file formats                   |
| 6       | Games and demonstrations                |
| 7       | Miscellaneous files and documents       |
| 8       | System administration commands          |
| 9       | Obscure kernel specs and interfaces     |

> 🔁 Some titles exist in multiple sections (e.g., `passwd` in section 1 **and** 5).

---

## 🔸 Using the `man` Command

### Basic Usage:
```bash
man <title>
````

- Searches sections in numeric order, with priority to sections 1 and 8.
    

### Specify a Section:

```bash
man <section> <title>
```

- Example:
    
    - `man sync` → Command description (Section 1)
        
    - `man 2 sync` → System call version (Section 2)
        

### Search by Keyword:

```bash
man -k <keyword>
# OR
apropos <keyword>
```

> Example:

```bash
man -k translate
```

Results might include:

- `objcopy (1)` - copy and translate object files
    
- `tr (1)` - translate or delete characters
    
- `dcgettext (3)` - translate message
    

---

## 🔸 Updating Man Page Index

- The keyword database used by `man -k` or `apropos` can become outdated.
    
- To refresh it:
    
    - On **Red Hat / FreeBSD**: `makewhatis`
        
    - On **Ubuntu**: `mandb`
        

---

## 🔸 Where Are Man Pages Stored?

- Source format: **nroff** input
    
- Location: `/usr/share/man`
    
- Files are **gzip-compressed** to save space
    

> The `man` command auto-decompresses these files.

### Cache:

- Formatted pages may be cached in:
    
    - `/var/cache/man`
        
    - `/usr/share/man`
        

> ⚠️ Caching preformatted man pages can be a **security risk**.

---

## 🔸 Customizing Man Search Path

- Use `manpath` to view the current search path:
    

```bash
manpath
```

> Typical output:

```
/usr/local/man:/usr/local/share/man:/usr/share/man
```

- To override:
    

```bash
export MANPATH=/home/share/localman:/usr/share/man
```

> You can also set **system-wide paths** for custom distributions (e.g., OpenPKG).

---

## 🔸 Packaging Custom Man Pages

- Best practice: use your system’s **standard package manager**.
    
- Place custom man pages in the **standard man directories**.