# Problem Solving with Programming (PSP)

**Course hub for IIIT Allahabad students** — notes, video lectures, tutorials, live C compilers, and assignments, organised topic by topic.

**Instructor:** Dr. Mohammed Javed  ·  **Course code:** PSP
**Live website:** https://pramaniksubrata.github.io/PSP/

---

## How the site is organised (3 levels)

The home page is one file. The course has **15 topics**, and every topic has **15 chapters**.

```
Home (index.html)            ← content comes from home.md
  └── Topic  1 … 15          ← 1.md … 15.md          (HUB pages: just list chapters)
        └── Chapter 1 … 15   ← 1-1.md … 15-15.md     (CONTENT pages: the real study material)
```

| File | What it is |
|---|---|
| `index.html` | Home page **viewer**. Reads `home.md` and draws every section. Never edit. |
| `home.md` | **Home page content.** Objectives, outcomes, course info, topic list, applications, TA team, grading, policies, books, PYQ. |
| `topic.html` | Topic/chapter **viewer**. Opens any `.md` page. Never edit. |
| `1.md` … `15.md` | **Topic HUB pages.** Each lists its 15 chapters (clickable links). |
| `1-1.md` … `15-15.md` | **Chapter CONTENT pages.** Description, Notes, Lecture, Tutorial, Run Your Code, Assignment. |
| `LICENSE` | MIT license. |
| `README.md` | This guide. |

> **Total:** 1 home file + 15 hub files + (15 × 15 =) 225 content files.
> **All `.md` files live in the repo ROOT** — not inside any folder. `topic.html?t=1` opens `1.md`, and `topic.html?t=1-1` opens `1-1.md`.

You never touch `index.html` or `topic.html`.
**To change what students see, you only edit the `.md` files.**

---

## How the navigation flows

1. Student opens the **Home page** → sees everything written in `home.md`, including the 15 topics.
2. Clicks a topic (say *Basic knowledge of computer*) → opens `topic.html?t=1` → **1.md** shows the list of 15 chapters.
3. Clicks a chapter (say *Part 1*) → opens `topic.html?t=1-1` → **1-1.md** shows the full content:
   **Description · Notes · Lecture · Tutorial · Run Your Code · Assignment.**

The same rule applies to every topic — `2.md` → `2-1 … 2-15`, `11.md` → `11-1 … 11-15`, and so on.

---

## A) Editing the HOME page — `home.md`

Everything on the home page lives in this one file. Only three rules:

| You write | It means |
|---|---|
| `## Topics` | a section. **Do not rename these** — `index.html` looks for the exact name. |
| `- Pointers \| Unit 4` | one item. Parts are separated by `\|` |
| `-- Computer hardware, CPU` | a sub-line belonging to the item above it |

Anything inside `<!-- -->` is ignored, so the notes already written in the file are safe to leave there.

### The sections, in page order

| Section | Line format |
|---|---|
| `## Hero` | `- Badge \| ...`, `- Title \| ...`, `- Highlight \| ...`, `- Lead \| ...` |
| `## Course Info` | `- Label \| Value` (Instructor takes a third part: the email) |
| `## Description` | plain sentences, no dashes |
| `## Objectives` | `- one objective per line` |
| `## Outcomes` | `- one outcome per line` |
| `## Prerequisites` | `- one per line` |
| `## Units` | `- Unit 1 \| Title` then `-- one syllabus point per line` |
| `## Topics` | `- Topic name \| Unit` |
| `## Applications` | `- App name \| Concept used \| link` |
| `## TA Team` | `- Name \| email` (email may be left empty) |
| `## Grading` | `- Assessment \| Weight \| Due date` |
| `## Grading Scale` | `- Grade \| Range` |
| `## Policies` | `- Policy title` then `-- one rule per line` |
| `## Primary Textbooks` | `- Book title \| Author, edition, publisher \| link` |
| `## Reference Books` | same as above |
| `## Software` | plain sentences |
| `## PYQ` | `- Year \| Exam type \| link` |

### Links on the home page

Leave `#` where a link is not ready — the button shows **"Coming soon"** and stays unclickable. Paste a real link in its place and the button turns active on its own. Nothing else to change.

```
## PYQ
- 2025 | End Sem | https://drive.google.com/xxxx     ← live button
- 2025 | Mid Sem | #                                 ← "Coming soon"
```

### Two things to be careful about

- **Topic numbers come from the order** in `## Topics`. The 1st line opens `1.md`, the 2nd opens `2.md`. If you reorder the list, rename the `.md` files to match.
- **Do not rename the `##` headings.** Change the lines under them as much as you like.
- If a section is left empty, it simply disappears from the page — nothing breaks.

---

## B) Editing a CHAPTER's content (the file you edit most)

Open the chapter file you want, e.g. **`11-3.md`** for *Pointers, Chapter 3*, click the pencil (**Edit**) icon, and fill in the sections.

### Description
Write points as `### 1.`, `### 2.` … You can use text, lists, tables, and code blocks.

```
## Description

### 1. Adding two numbers in C
To add two numbers in C, declare variables, read input with `scanf()`,
and use the `+` operator.

​```c
#include <stdio.h>
int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    printf("Sum = %d\n", a + b);
    return 0;
}
​```
```

### Notes / Lecture / Tutorial / Assignment
One link per line, format: `- <label> | "<link>"` (paste the real link inside the quotes).

```
## Notes
- Chapter Notes (PDF)   | "https://drive.google.com/xxxx"
- Quick Revision Sheet  | "https://drive.google.com/yyyy"

## Lecture
- Intro to Pointers     | "https://youtu.be/xxxx"

## Tutorial
- Practice Walkthrough  | "https://youtu.be/zzzz"

## Assignment
- 20 Aug 2026 : deadline | "https://forms.gle/xxxx"
```

- **Run Your Code** (5 compilers — OnlineGDB, CodeChef, HackerRank, VS Code Web, LeetCode) appears on every chapter **automatically**. You do **not** add it.
- If a link is not ready yet, leave it as `#`. It will show **"Coming soon…"**.

---

## C) Editing a TOPIC hub (rename / add / remove chapters)

Open the topic file, e.g. **`5.md`** for *Loops and Iteration*, and edit the `## Chapters` list.

Each line format: `- <title shown> | <chapter-file-name-without-.md>`

```
# Loops and Iteration
Unit 3

## Chapters
- 1. Loops and Iteration — Part 1 | 5-1
- 2. Loops and Iteration — Part 2 | 5-2
- 3. Loops and Iteration — Part 3 | 5-3
...
- 15. Loops and Iteration — Part 15 | 5-15
```

- The part after `|` (e.g. `5-3`) is the file it opens (`5-3.md`).
- Add or remove chapter lines freely. If you add a new line, remember to also create that `.md` file (e.g. `5-16.md`).
- You may add a `## Description` block above the chapters list if you want an intro on the hub page.

---

## Which file do I edit?

| I want to change… | Edit |
|---|---|
| Course objectives, outcomes, timings, instructor | `home.md` |
| The list of topics shown on the home page | `home.md` → `## Topics` |
| Applications, grading table, policies, books, PYQ | `home.md` |
| TA names and emails | `home.md` → `## TA Team` |
| The chapter list inside one topic | that topic's `1.md` … `15.md` |
| Notes / lecture / tutorial / assignment links | that chapter's `1-1.md` … `15-15.md` |

---

## How to publish

1. On GitHub, click the file you want, then the pencil (**Edit**) icon.
2. Make your change.
3. Click **Commit changes**.
4. The website updates within about a minute — students see it live.

**Tip:** After editing, open the live page and do a hard refresh (**Ctrl + Shift + R**) to skip the browser cache.

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

## License

Code is released under the MIT License (see `LICENSE`). Course notes and study material are shared for educational use — please credit the source if you reuse them.

_Maintained by Teaching Assistant Team (IIITA)._
