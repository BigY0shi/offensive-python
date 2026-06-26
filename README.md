# Introduction to Python 3 Programming with Applied Cybersecurity Projects

> **Course Level:** Beginner — Grades 10–12 / Adult Learners (no prior programming experience required)
> **Duration:** 9 Weeks · 2 Live Sessions/Week · ~60 min/session
> **Total Contact Hours:** ~18 hours live instruction + async homework, tutoring, and project work
> **Delivery:** Fully Online — Synchronous via Moodle LMS (hosted on ProxMox)

---

## Table of Contents

1. [Course Description](#course-description)
2. [Prerequisites](#prerequisites)
3. [Learning Objectives](#learning-objectives)
4. [Required Materials](#required-materials)
5. [Course Structure & Schedule](#course-structure--schedule)
   - [Unit 1 — Python Foundations (Weeks 1–2)](#unit-1--python-foundations-weeks-12)
   - [Unit 2 — Functions, OOP, Files & Testing (Week 3)](#unit-2--functions-oop-files--testing-week-3)
   - [Unit 3 — Project 1: Game or Automation Tool (Week 4)](#unit-3--project-1-game-or-automation-tool-week-4)
   - [Unit 4 — Security-Flavored Python I: Keylogging & Ethics (Week 5)](#unit-4--security-flavored-python-i-keylogging--ethics-week-5)
   - [Unit 5 — Security-Flavored Python II: Networks & Scanning (Week 6)](#unit-5--security-flavored-python-ii-networks--scanning-week-6)
   - [Unit 6 — Capstone Project Build (Weeks 7–9)](#unit-6--capstone-project-build-weeks-79)
6. [Assessments & Grading](#assessments--grading)
7. [Tools & Technology Setup](#tools--technology-setup)
8. [Repository Structure](#repository-structure)
9. [Academic Integrity & Ethical Use Policy](#academic-integrity--ethical-use-policy)
10. [Standards Alignment](#standards-alignment)
11. [Instructor Notes](#instructor-notes)

---

## Course Description

This is a fast-paced, project-driven 9-week introduction to Python 3 designed for tech-savvy beginners with **no prior programming experience**. You will start from absolute zero — installing Python, writing your first `print()` statement — and finish by building real cybersecurity tools: keyloggers, port scanners, and packet sniffers, all in supervised, ethical, and legal environments.

The course uses **Python Crash Course, 3rd Edition** (Eric Matthes) as the instructional spine for core language fundamentals. For the security-focused project track, instructor-authored teaching modules adapted from **Caleb M. Kingsley's *Python Hacking Projects for Beginners*** provide the primary project and skill-check framework. These Kingsley modules (K1–K6) are delivered as interactive Moodle Books inside the LMS, with matching starter-code and written guides in this repository.

All content aligns with the **CSTA K–12 Computer Science Standards (Grades 9–12, 2017 Revised)**.

---

## Prerequisites

| Requirement | Details |
|---|---|
| Computer literacy | Comfortable navigating files, installing software, and using a web browser |
| Hardware | A computer (Windows, macOS, or Linux) with internet access |
| Moodle access | Enrolled students receive credentials from the instructor |
| Prior coding | **None required** — we start from scratch |

---

## Learning Objectives

By the end of this course, students will be able to:

- **Set up** a complete Python 3 development environment (VS Code + Python + pip)
- **Read and write** Python programs using variables, data types, control flow, functions, and classes
- **Organize** code into reusable modules with proper error handling and basic unit tests
- **Read from and write to** files and the command-line
- **Explain** fundamental cybersecurity concepts: threat modeling, ethical disclosure, and legal boundaries
- **Build** a supervised keylogger that captures and logs keyboard events to a file
- **Build** a port scanner using Python sockets and interpret the results
- **Capture and analyze** network packets using Scapy
- **Design, develop, test, document, and demo** an original capstone project

---

## Required Materials

### Textbooks / Reading

| # | Title | Author | Format | Notes |
|---|---|---|---|---|
| 1 | *Python Crash Course, 3rd Edition* | Eric Matthes | Print or Digital (No Starch Press) | Primary textbook — Chapters 1–11 assigned |
| 2 | *Python Hacking Projects for Beginners* | Caleb M. Kingsley | Digital (instructor-adapted modules in Moodle) | Basis for K1–K6 Moodle Books and security projects |

### Software (Free)

| Tool | Purpose | Install |
|---|---|---|
| Python 3.11+ | Runtime | [python.org/downloads](https://www.python.org/downloads/) |
| VS Code | Code editor | [code.visualstudio.com](https://code.visualstudio.com/) |
| VS Code Python Extension | IntelliSense, debugging | Marketplace ID: `ms-python.python` |
| Git | Version control | [git-scm.com](https://git-scm.com/) |
| pip | Package manager | Included with Python |
| pynput | Keyboard capture (Unit 4) | `pip install pynput` |
| scapy | Packet sniffing (Unit 5) | `pip install scapy` |

> **Note:** All tools marked with a security function (pynput, scapy) are to be installed **only** in your designated lab environment and used **only** within the scope of this course's supervised assignments. See the [Ethical Use Policy](#academic-integrity--ethical-use-policy).

---

## Course Structure & Schedule

### Unit 1 — Python Foundations (Weeks 1–2)

**Kingsley Module:** K1 · K2
**Textbook Chapters:** *PCC* Chapters 1–6

#### Week 1 — Getting Started & Core Syntax

| Session | Topics | Activities |
|---|---|---|
| 1.1 | Course intro, environment setup, `Hello, World!` | Install Python + VS Code; run first script |
| 1.2 | Variables, data types (int, float, str, bool), string methods | Guided coding: mad-libs style exercises |

**Concepts Covered:**
- Python interpreter vs. compiled languages
- Variables and assignment
- Primitive data types: `int`, `float`, `str`, `bool`
- String concatenation, f-strings, and common string methods (`.upper()`, `.lower()`, `.strip()`, `.replace()`)
- Basic I/O: `print()` and `input()`
- Comments and code style (PEP 8 basics)

#### Week 2 — Control Flow & Collections

| Session | Topics | Activities |
|---|---|---|
| 2.1 | `if`/`elif`/`else`, comparison & logical operators | Number guessing game (skeleton provided) |
| 2.2 | `for` loops, `while` loops, lists, dictionaries | Skill Check 1 review; Moodle quiz practice |

**Concepts Covered:**
- Boolean logic and truthiness
- `if`, `elif`, `else` branching
- `for` and `while` loops, `break`, `continue`, `range()`
- Lists: indexing, slicing, `.append()`, `.remove()`, `.sort()`
- Dictionaries: key/value pairs, `.get()`, iteration
- Nested data structures (intro)

> ✅ **Skill Check 1** — End of Week 2 (Moodle Quiz + short coding exercise)

---

### Unit 2 — Functions, OOP, Files & Testing (Week 3)

**Kingsley Module:** K3
**Textbook Chapters:** *PCC* Chapters 7–11

| Session | Topics | Activities |
|---|---|---|
| 3.1 | Defining functions, parameters, return values, scope; intro to classes | Refactor Week 1–2 exercises into functions |
| 3.2 | File I/O (`open`, `read`, `write`, `with`); `try`/`except`; intro to `pytest` | Mini file-parsing exercise |

**Concepts Covered:**
- `def`, parameters vs. arguments, default values, `*args`, `**kwargs`
- Return values and `None`
- Variable scope: local vs. global
- Classes and objects: `__init__`, instance variables, methods
- Inheritance basics
- Opening, reading, writing, and appending files
- `with` statement and context managers
- Exception handling: `try`, `except`, `finally`, custom exceptions
- Writing and running basic `pytest` tests

> ✅ **Skill Check 2** — End of Week 3 (Moodle Quiz)
> 📝 **Midterm Test** — End of Week 3 (Moodle: timed written + coding exam covering Units 1–2)

---

### Unit 3 — Project 1: Game or Automation Tool (Week 4)

**Kingsley Module:** K1 (applied)
**Description:** Students apply everything from Units 1–2 to build either a text-based game (e.g., adventure game, quiz app) or a simple automation tool (e.g., file organizer, password strength checker). This is the first fully student-authored project.

| Session | Topics | Activities |
|---|---|---|
| 4.1 | Project planning, pseudocode, Git commit workflow | Design doc + first commit push to repo |
| 4.2 | Code review, debugging workshop, documentation practice | Peer review session; `README` writing |

**Project 1 Requirements:**
- Minimum 50 lines of original Python (excluding comments/blank lines)
- At least one function, one class, and one file operation
- A project-level `README.md` with description, usage, and known issues
- Submitted via Moodle assignment upload **and** committed to the student's `starter-code/project1/` folder

> 📦 **Project 1 Due** — End of Week 4

---

### Unit 4 — Security-Flavored Python I: Keylogging & Ethics (Week 5)

**Kingsley Module:** K4
**⚠️ Important:** All work in this unit is performed in your **personal, isolated lab machine only**. You may NOT test keylogging software on any machine you do not personally own and have explicit authorization to test on.

| Session | Topics | Activities |
|---|---|---|
| 5.1 | What is a keylogger? Legal/ethical framing; `pynput` library intro | Discuss: legal gray areas; install pynput in lab VM |
| 5.2 | Building the keylogger: event listeners, file logging, graceful exit | Complete guided build; write ethics reflection |

**Concepts Covered:**
- Keyboard event capture with `pynput.keyboard.Listener`
- Logging key presses to a `.txt` file with timestamps
- Special key handling (`Key.space`, `Key.enter`, `Key.backspace`)
- Graceful process termination and file flushing
- Ethical hacking principles: consent, scope, disclosure
- Overview of the Computer Fraud and Abuse Act (CFAA) and relevant state laws

**Mini-Project A Requirements:**
- Functional keylogger that logs to file with timestamps
- Graceful stop mechanism (e.g., hotkey or timer)
- Written ethics reflection (1–2 paragraphs): What could go wrong if this tool were misused? What safeguards exist?
- Submitted to `starter-code/mini-project-a/`

> ✅ **Skill Check 3** — End of Week 5 (Moodle Quiz: security concepts + code reading)
> 📦 **Security Mini-Project A Due** — End of Week 5

---

### Unit 5 — Security-Flavored Python II: Networks & Scanning (Week 6)

**Kingsley Module:** K5
**⚠️ Important:** Port scanning and packet sniffing must be performed **only** on the provided lab network (your own machines on your own isolated network). Scanning external networks without authorization is illegal.

| Session | Topics | Activities |
|---|---|---|
| 6.1 | TCP/IP basics, the `socket` module, building a simple port scanner | Scan localhost; discuss open/closed/filtered ports |
| 6.2 | Packet sniffing with Scapy; CLI argument parsing with `argparse` | Capture and display packets on lab interface |

**Concepts Covered:**
- Networking fundamentals: IP addresses, ports, TCP handshake
- Python `socket` module: `socket.socket()`, `.connect()`, `.settimeout()`
- Writing a multi-threaded port scanner
- Introduction to Scapy: `sniff()`, packet layers (`IP`, `TCP`, `Raw`)
- Parsing command-line arguments with `argparse`
- Reading scan output and identifying common services

**Mini-Project B Requirements:**
- Port scanner that accepts a target IP and port range via CLI arguments
- Scapy packet sniffer that prints source/destination IP and protocol
- Brief written analysis (1 paragraph): Describe one real-world use case for port scanning in a defensive security context
- Submitted to `starter-code/mini-project-b/`

> 📦 **Security Mini-Project B Due** — End of Week 6

---

### Unit 6 — Capstone Project Build (Weeks 7–9)

**Kingsley Module:** K6
**Description:** The capstone is a student-designed or instructor-approved original Python project that demonstrates mastery of the full course. It must go through the complete software development lifecycle: planning, coding, testing, documentation, and a live demo.

#### Approved Capstone Project Categories

| Category | Example Ideas |
|---|---|
| Security Tool | Enhanced keylogger with email alerts, network monitor dashboard |
| Automation Tool | Web scraper, file backup utility, system health monitor |
| Game | Text RPG with save/load, quiz app with leaderboard |
| Data Tool | CSV analyzer, simple database app using SQLite |
| Open Proposal | Student-pitched idea approved by instructor by end of Week 7 |

#### Week-by-Week Milestones

| Week | Milestone | Deliverable |
|---|---|---|
| 7 | Project proposal approved; repo structure committed | `docs/capstone-proposal.md` submitted |
| 8 | Core feature complete; unit tests written | Mid-build check-in via Moodle submission |
| 9 | Final polish, documentation, and live demo | Capstone submitted + demo video or live session |

**Capstone Requirements:**
- Minimum 100 lines of original Python (excluding comments/blank lines)
- At least 3 functions and 2 classes
- File I/O or network feature included
- Minimum 5 passing unit tests (`pytest`)
- Full `README.md` (description, setup, usage, examples, known issues)
- Code committed to `starter-code/capstone/`

> 📦 **Capstone Project Due** — End of Week 9
> 🎤 **Live Demo** — Week 9 live session
> ✅ **Final Check Quiz** — End of Week 9

---

## Assessments & Grading

| Assessment | Weight | When |
|---|---|---|
| Skill Check 1 (Quiz + Coding) | 5% | End of Week 2 |
| Skill Check 2 (Quiz) | 5% | End of Week 3 |
| Midterm Test | 15% | End of Week 3 |
| Project 1 | 15% | End of Week 4 |
| Skill Check 3 (Quiz) | 5% | End of Week 5 |
| Security Mini-Project A | 10% | End of Week 5 |
| Security Mini-Project B | 10% | End of Week 6 |
| Capstone Project | 25% | End of Week 9 |
| Final Check Quiz | 5% | End of Week 9 |
| Participation & Attendance | 5% | Ongoing |
| **Total** | **100%** | |

### Grading Scale

| Grade | Range |
|---|---|
| A | 90–100% |
| B | 80–89% |
| C | 70–79% |
| D | 60–69% |
| F | Below 60% |

### Late Policy

- Assignments submitted within 24 hours of the deadline: **10% deduction**
- Assignments submitted 24–72 hours late: **25% deduction**
- Assignments submitted more than 72 hours late: **50% deduction**, instructor approval required
- **No late submissions accepted after the final day of the course**

---

## Tools & Technology Setup

### Step-by-Step Environment Setup

#### 1. Install Python 3

1. Go to [python.org/downloads](https://www.python.org/downloads/)
2. Download the latest Python 3.11+ installer for your OS
3. **Windows users:** Check ✅ "Add Python to PATH" during installation
4. Verify: open a terminal and run:
   ```
   python --version
   ```
   You should see `Python 3.11.x` (or higher)

#### 2. Install VS Code

1. Go to [code.visualstudio.com](https://code.visualstudio.com/) and download
2. Install the **Python** extension (Marketplace ID: `ms-python.python`)
3. Optional but recommended: **Pylint** or **Ruff** for real-time error checking

#### 3. Clone This Repository

```bash
git clone https://github.com/BigY0shi/offensive-python.git
cd offensive-python
```

#### 4. Install Required Packages

```bash
pip install pynput scapy pytest
```

> **macOS / Linux note:** Scapy may require elevated privileges for packet capture. Use `sudo` when running packet-sniffing scripts, or configure `setcap` on the Python binary.

#### 5. Access Moodle

- Your instructor will provide the Moodle LMS URL and your login credentials
- All quizzes, assignments, Moodle Books (K1–K6), and grades are managed there
- Live sessions are conducted via the video conferencing tool embedded in Moodle

---

## Repository Structure

```
offensive-python/
├─ README.md                  ← You are here
├─ LICENSE
├─ .gitignore
│
├─ course-info/               ← Administrative documents
│  ├─ syllabus/               ← Full syllabus PDF / Markdown
│  ├─ grading/                ← Rubrics for each assignment
│  └─ policies/               ← Attendance, late work, and AUP policies
│
├─ moodle/                    ← Moodle LMS import files
│  ├─ books/                  ← Exported Moodle Book HTML (K1–K6)
│  │  ├─ K1.html              ← Python Foundations: Getting Started
│  │  ├─ K2.html              ← Python Foundations: Control Flow & Collections
│  │  ├─ K3.html              ← Functions, OOP, Files & Testing
│  │  ├─ K4.html              ← Security I: Keylogging & Ethics
│  │  ├─ K5.html              ← Security II: Networks & Scanning
│  │  └─ K6.html              ← Capstone Project
│  ├─ quizzes/                ← Moodle XML quiz import files
│  ├─ assignments/            ← Moodle assignment definition files
│  └─ imports/                ← Full course backup (.mbz) and restore files
│
├─ modules/                   ← Instructor teaching modules (Kingsley-adapted)
│  ├─ k1/                     ← Module K1: Getting Started
│  ├─ k2/                     ← Module K2: Control Flow & Collections
│  ├─ k3/                     ← Module K3: Functions, OOP, Files & Testing
│  ├─ k4/                     ← Module K4: Keylogging & Ethics
│  ├─ k5/                     ← Module K5: Networks & Scanning
│  └─ k6/                     ← Module K6: Capstone
│
├─ starter-code/              ← Student project templates
│  ├─ project1/               ← Project 1 starter files
│  ├─ mini-project-a/         ← Security Mini-Project A (keylogger)
│  ├─ mini-project-b/         ← Security Mini-Project B (port scanner / sniffer)
│  └─ capstone/               ← Capstone project workspace
│
├─ examples/                  ← Instructor demo scripts used in live sessions
├─ docs/                      ← Additional documentation and student guides
├─ tests/                     ← Course-level test utilities and CI scripts
└─ output/                    ← Generated output files (gitignored in production)
```

---

## Academic Integrity & Ethical Use Policy

### The Golden Rule of Offensive Security

> **You may only use the techniques taught in this course on systems and networks that you own or have explicit, written permission to test.**

This is not just an academic policy — it is the law. Unauthorized access to computer systems is a federal crime under the **Computer Fraud and Abuse Act (CFAA), 18 U.S.C. § 1030**, and is similarly prohibited under state computer crime statutes.

### What This Means for You

| Allowed ✅ | NOT Allowed ❌ |
|---|---|
| Scanning your own machine (`127.0.0.1`, `localhost`) | Scanning your school, employer, or ISP's network |
| Running keylogger on your own lab VM | Installing keylogger on any shared or others' device |
| Sniffing packets on the course-provided lab network | Sniffing a public Wi-Fi or any unauthorized network |
| Discussing vulnerabilities in class | Publicly disclosing live vulnerabilities without authorization |
| Using Moodle sandbox environments | Attempting to access other students' Moodle accounts |

### Consequences

Violations of this policy will result in:
1. Immediate removal from the course with a grade of **F**
2. Referral to school administration or law enforcement, as appropriate
3. Permanent record notation

### Responsible Disclosure

If you discover a real security vulnerability during your coursework (unlikely, but possible), do not exploit it. Notify the instructor immediately. You will receive full credit and the instructor will handle proper disclosure.

---

## Standards Alignment

This course aligns with the **CSTA K–12 Computer Science Standards (2017 Revised), Grades 9–12**.

| CSTA Standard | Standard Description | Course Coverage |
|---|---|---|
| 3A-AP-13 | Create prototypes that use algorithms to solve computational problems | Units 1–3, Capstone |
| 3A-AP-14 | Use lists to simplify solutions, generalizing computational problems | Unit 1 (Week 2) |
| 3A-AP-15 | Justify the selection of specific control structures | Units 1–2 |
| 3A-AP-16 | Design and iteratively develop computational artifacts | Units 3, 6 |
| 3A-AP-17 | Decompose problems into smaller components through systematic analysis | Units 2–3, Capstone |
| 3A-AP-18 | Create artifacts by using procedures within a program | Unit 2 (functions/classes) |
| 3A-AP-23 | Document design decisions using text, graphics, presentations | All projects |
| 3A-IC-24 | Evaluate the ways computing impacts personal, ethical, social, economic & cultural practices | Unit 4 (ethics module) |
| 3A-IC-25 | Test and refine computational artifacts to reduce bias and increase accessibility | Capstone testing |
| 3A-NI-05 | Give examples to illustrate how sensitive data can be vulnerable when in transit | Unit 5 |
| 3A-NI-06 | Recommend security measures to address various scenarios | Units 4–5 |
| 3A-NI-07 | Compare various security measures with a focus on trade-offs between usability and security | Units 4–5 |
| 3B-AP-10 | Use and adapt classic algorithms to solve computational problems | Units 1–3 |
| 3B-AP-21 | Develop and use a series of test cases to verify that a program performs according to its design | Unit 2, Capstone |
| 3B-AP-22 | Modify an existing program to add additional functionality and discuss intended and unintended implications | Units 3–5 |
| 3B-NI-03 | Describe the issues that impact network functionality (e.g., bandwidth, load, delay, topology) | Unit 5 |
| 3B-NI-04 | Compare ways software developers protect devices and information from unauthorized access | Units 4–5 |

---

## Instructor Notes

### About the Kingsley Modules

The K1–K6 modules in this repository are instructor-authored adaptations of content from *Python Hacking Projects for Beginners* by Caleb M. Kingsley, reformatted and scaffolded for a Moodle Book delivery format. These are teaching materials intended for use within this course under Fair Use / educational exemption guidelines. They are **not** redistributable outside of enrolled students of this course.

### About the Course Sandbox Environment

This course runs on a **ProxMox**-hosted virtual environment. Each student has access to:
- A Kali Linux VM (for security labs in Units 4–5)
- An isolated internal network for scanning/sniffing labs
- Moodle LMS for content delivery, quizzes, and grading

Students should **not** perform any security-related exercises outside of their assigned VM environment.

### Contact & Support

| Resource | Details |
|---|---|
| Instructor | Contact via Moodle messaging system |
| Office Hours | Posted in Moodle course homepage |
| Technical Support | Use the Moodle "Help Desk" forum |
| Emergency (ethical issue) | Message instructor directly; urgent matters will be addressed within 24 hours |

---

*Course repository maintained by the instructor. Student submissions are managed through Moodle and are not stored in this repository.*
