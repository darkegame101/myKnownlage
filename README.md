# IT Knowledge Base & Capability Tracker

Welcome to the IT Knowledge Base & Capability Tracker. This repository maintains a structured, evidence-based representation of technical knowledge, practical capabilities, source traceability, gap analyses, and dependency-based learning roadmaps.

> [!IMPORTANT]
> **Core Principle**: Completion of a course video does **NOT** equal mastery. Practical capabilities are strictly verified based on concrete evidence.

---

## 🏛️ Repository Architecture

```
myKnownlage/
├── AGENTS.md                          # Master Agent instructions & repository rules
├── README.md                          # Repository overview & entry point index
├── 00-sources/                        # Master source registry & course records
│   ├── learning-sources.md           # Master Learning Sources Registry (SRC-001 - SRC-008)
│   ├── courses.md                    # Course Catalog & Index
│   ├── rules.md                      # Source Processing & Knowledge Base Expansion rules
│   ├── C001-java-core.md             # Course record for Java Core
│   ├── C002-dsa-java.md              # Course record for CTDL-GT Java
│   ├── C003-sql-server.md            # Course record for SQL Server
│   ├── C004-java-jdbc.md             # Course record for Java JDBC
│   ├── C005-os-concepts.md           # Course record for OS Principles
│   ├── C006-java-network.md          # Course record for Java Network Programming
│   ├── C007-git-github.md            # Course record for Git & GitHub
│   └── C008-linux-lpi.md             # Course record for Linux (LPI 1-2)
├── 00-dashboard/                      # Master dynamic dashboards & analytical reports
│   ├── knowledge-map.md              # Overall visual & domain knowledge map
│   ├── skill-matrix.md               # Capability evaluations across 5 dimensions (0-5 scale)
│   ├── gap-analysis.md               # Detailed report on missing knowledge & prerequisite gaps
│   └── learning-roadmap.md           # Dependency-based dual-branch roadmap
├── 01-programming/                    # Java Core & Object-Oriented Programming
│   ├── summary.md                    # Programming domain summary
│   ├── java-core.md                  # Java Core syntax, Collections, File I/O, Swing
│   └── oop-java.md                   # OOP Pillars, UML modeling, interfaces
├── 02-dsa/                            # Data Structures & Algorithms
│   ├── summary.md                    # DSA domain summary
│   └── data-structures-algorithms-java.md # Big O, Arrays, Singly Linked List
├── 03-databases/                      # Relational Databases & Data Access
│   ├── summary.md                    # Databases domain summary
│   ├── sql-server.md                 # SQL Server 2022, T-SQL, CTE, Window Functions
│   └── java-jdbc.md                  # JDBC connectivity, PreparedStatement, DAO pattern
├── 04-operating-systems/              # OS Concepts & Linux Administration
│   ├── summary.md                    # Operating Systems & Linux domain summary
│   ├── os-concepts.md                # System calls, processes, CPU scheduling, deadlock
│   └── linux-sysadmin-bash.md        # Linux CLI, FHS hierarchy, permissions, Bash scripts
├── 05-networking/                     # Computer Networking & Network Programming
│   ├── summary.md                    # Networking domain summary
│   └── java-network-programming.md   # Java TCP/UDP Sockets, Chat app, Remote Desktop
└── 06-devops-tools/                   # Version Control & Development Tools
    ├── summary.md                    # DevOps tools domain summary
    └── git-github.md                 # Git CLI, branching, rebasing, GitHub PR workflow
```

---

## 🧭 Master Navigation & Dashboards

- 📖 **[Master Learning Sources Registry](00-sources/learning-sources.md)**: Catalog of all learning inputs (`SRC-001` – `SRC-008`) with bidirectional mapping.
- 📚 **[Course Catalog & Index](00-sources/courses.md)**: List of all course records with direct lesson indexes.
- 🗺️ **[Knowledge Map](00-dashboard/knowledge-map.md)**: Visual diagram and domain level mapping.
- 📊 **[Skill Matrix](00-dashboard/skill-matrix.md)**: Capability evaluations on a 0–5 scale across Theory, Practical, Troubleshooting, Design, and Confidence.
- 🔍 **[Gap Analysis](00-dashboard/gap-analysis.md)**: Detailed report on missing knowledge, practical gaps, and prerequisite blockers.
- 🚀 **[Learning Roadmap](00-dashboard/learning-roadmap.md)**: Dependency-based dual-branch roadmap for Backend Development and Systems/DevOps.

---

## 🎯 Skill Scale Reference (0–5)
- **0 = Not Learned**: Never studied or no exposure.
- **1 = Terminology Known**: Recognizes terms, knows topic exists, cannot explain mechanism.
- **2 = Concept Understood**: Explains basic concepts and purpose, cannot explain deep mechanisms.
- **3 = Mechanism Understood**: Explains HOW and WHY, understands main flow and internal components.
- **4 = Able to Use / Implement**: Independently writes code, configures labs, solves routine issues.
- **5 = Troubleshoot / Design**: Debugs production issues, analyzes trade-offs, designs solution architectures.
