# Source Processing Rules & Protocol

Standard Operating Procedure (SOP) for processing any new learning source (Course, Documentation, GitHub repository, YouTube playlist, Book, Lab, or Project) before updating the Knowledge Base.

---

## 📌 9-Step Processing Pipeline

```mermaid
graph TD
    A[User Provides New Source URL/Name] --> B[Step 1: Read & Parse Source Content]
    B --> C[Step 2: Check Existing Registry in learning-sources.md]
    C --> D[Step 3: Register / Update Source ID SRC-XXX]
    D --> E[Step 4: Analyze Coverage: NEW / EXISTING / DEEPER / PRACTICAL / DUPLICATE / MISSING]
    E --> F[Step 5: Source -> Knowledge Mapping]
    F --> G[Step 6: Knowledge -> Source Mapping]
    G --> H[Step 7: Update Dashboard & Gap Reports]
    H --> I[Step 8: Enforce Level Rules: Course Completion != Mastery]
    I --> J[Step 9: Generate Source Processing Report]
```

---

## 📋 Detailed Rules & Guidelines

### Step 1 — Read Source
- Fetch content from URL or parse curriculum items.
- Extract: Name, Provider, Domain, Topic, Subtopics, Concepts, Mechanisms, Practical Skills, Tools, Technologies, Structure, Chapters/Lectures.
- If content cannot be fetched or verified, mark: `Source content: Not verified`. Never fabricate missing content.

### Step 2 — Check Existing Source
- Inspect `00-sources/learning-sources.md` by URL, Source Name, and Provider.
- If source URL exists: Update existing entry (Do NOT create duplicate Source ID).
- If source is new: Assign next sequential ID (`SRC-009`, `SRC-010`, etc.).

### Step 3 — Register Source
Register complete details in `00-sources/learning-sources.md`:
- Source ID
- Domain
- Topic
- Source / Course Name
- Provider
- URL
- Status (`Completed`, `In Progress`, `Planned`, `Reference`)
- Detailed Coverage
- Structure & Lesson links
- Knowledge Mapping links
- Date added

### Step 4 — Coverage Analysis
Classify content into:
- `NEW`: Completely new concepts.
- `EXISTING`: Already present in Knowledge Base.
- `DEEPER`: Previously learned topic, new source dives deeper.
- `PRACTICAL`: Adds hands-on implementation skills.
- `DUPLICATE`: Overlapping content, do not duplicate topic files.
- `MISSING`: Source exposes a related gap in current Knowledge Base.

### Step 5 — Source $\rightarrow$ Knowledge Mapping
Link Source ID to specific Topic files in `01-programming/`, `02-dsa/`, `03-databases/`, `04-operating-systems/`, `05-networking/`, `06-devops-tools/`. Update existing topic files or create new ones if strictly necessary.

### Step 6 — Knowledge $\rightarrow$ Source Mapping
In every affected Topic file, add the Source ID (`SRC-XXX`) under `## Sources & Knowledge Traceability` to maintain bidirectional mapping:
```text
SOURCE  <--->  TOPIC  <--->  KNOWLEDGE
```

### Step 7 — Dashboard & Gap Update
Update:
- `00-dashboard/knowledge-map.md`
- `00-dashboard/skill-matrix.md`
- `00-dashboard/gap-analysis.md`
- `00-dashboard/learning-roadmap.md`

### Step 8 — Enforce Skill Level Rules (No Automatic Level Elevation)
- `Course Coverage != Mastery`. Completing a course does NOT automatically grant Level 4 or 5.
- If practical evidence is lacking:
  - `Theory: Verified`
  - `Practical: Not verified`
  - `Troubleshooting: Not verified`
  - `Design: Not verified`

### Step 9 — Standard Processing Report Format
After processing any new source, generate a structured report:

```text
Source Added: SRC-XXX
Source: <Name>
URL: <URL>
New Knowledge: ...
Existing Knowledge: ...
Deepened Knowledge: ...
Practical Knowledge: ...
Duplicate: ...
Knowledge Gaps: ...
Prerequisite Gaps: ...
Files Updated: ...
Recommended Next: ...
```
