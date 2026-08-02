# Problem Solving with Programming (PSP)

**Course hub for IIIT Allahabad students** — notes, video lectures, live C compilers, and assignments, topic by topic.

**Instructor:** Dr. Mohammed Javed  ·  **Course code:** PSP
**Live website:** https://pramaniksubrata.github.io/PSP/

---

## How this project is organized

| File / Folder      | What it is |
|--------------------|-----------|
| `index.html`       | Home page — lists all 15 topics. Each topic links to its own page. |
| `topic.html`       | The viewer — opens a topic hub OR a chapter, and shows its content. |
| `topics/` (folder) | **All content lives here.** Two kinds of files (below). |

**Two kinds of files inside `topics/`:**

1. **Hub files** — `1.md`, `2.md` … `15.md` (one per topic).
   These list the **chapters** of a topic. Example (`1.md`):
   ```
   ## Chapters
   - Part 1 : Hardware & Memory | 1-1
   - Part 2 : Software Basics   | 1-2
   ```
   Left of `|` = the title shown. Right of `|` = the chapter file name (without `.md`).

2. **Chapter (content) files** — `1-1.md`, `1-2.md`, `2-1.md` …
   Each holds the real content: **Description** (left) + **Notes / Videos / Assignment** (right).

---

## How to edit (for Sir / TA)

**To change what a chapter contains** → open its file, e.g. `topics/1-1.md`:

```
## Description
### 1. Your heading
Write anything — text, lists, tables, or code.

## Notes
- Chapter Notes | "https://drive.google.com/xxxx"

## Videos
- Intro Lecture | "https://youtu.be/xxxx"

## Assignment
- Assignment 1 : 20 Aug 2026 | "https://forms.gle/xxxx"
```
Just paste your real link **inside the quotes** `""`. Add or remove lines freely.

**To add / rename / remove a chapter** → edit the topic's hub file (`topics/1.md`) `## Chapters` list, and create/delete the matching `1-N.md` file.

**Notes**
- If a link is not ready yet, leave it as `#`.
- The 5 compilers (OnlineGDB, CodeChef, HackerRank, VS Code, LeetCode) appear on every chapter automatically — you do **not** add them.
- You almost never touch `index.html` or `topic.html`.

---

## The 15 topics

1. Basic knowledge of computer
2. Introduction
3. Data Types and Expressions
4. Conditionals and Branching
5. Loops and Iteration
6. Arrays
7. Function
8. Recursion
9. Two Dimensional Array
10. Structures
11. Pointers
12. Dynamic Memory Allocation
13. Linked List
14. File Handling and Command Line Argument
15. Sorting and Searching

---

_Maintained by SUBRATA (IIITA)._
