# Problem Solving with Programming (PSP)

**Course hub for IIIT Allahabad students** — notes, video lectures, tutorials, live C compilers, and assignments, organised topic by topic.

**Instructor:** Dr. Mohammed Javed  ·  **Course code:** PSP
**Live website:** https://pramaniksubrata.github.io/PSP/

---

## How the site is organised (2 levels)

The course has **15 topics**, and every topic has **15 chapters**.

```
Home (index.html)
  └── Topic  1 … 15          ← 1.md … 15.md          (HUB pages: just list chapters)
        └── Chapter 1 … 15   ← 1-1.md … 15-15.md     (CONTENT pages: the real study material)
```

| File                       | What it is                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| `index.html`               | Home page — lists all 15 topics. Each topic opens its own page.             |
| `topic.html`               | The viewer — opens any page and renders it (works for both hubs and chapters). |
| `1.md` … `15.md`           | **Topic HUB pages.** Each one only lists its 15 chapters (clickable links). |
| `1-1.md` … `15-15.md`      | **Chapter CONTENT pages.** Description, Notes, Lecture, Tutorial, Run Your Code, Assignment. |
| `README.md`                | This guide.                                                                 |

> **Total:** 15 hub files + (15 × 15 =) 225 content files.
> **All `.md` files live in the repo ROOT** — not inside any folder. `topic.html` reads them from the root, e.g. `topic.html?t=1` opens `1.md`, and `topic.html?t=1-1` opens `1-1.md`.

You almost never touch `index.html` or `topic.html`.
**To change what students see, you only edit the `.md` files.**

---

## How the navigation flows

1. Student opens the **Home page** → sees the 15 topics.
2. Clicks a topic (say *Basic knowledge of computer*) → opens `topic.html?t=1` → **1.md** shows the list of 15 chapters.
3. Clicks a chapter (say *Part 1*) → opens `topic.html?t=1-1` → **1-1.md** shows the full content:
   **Description · Notes · Lecture · Tutorial · Run Your Code · Assignment.**

The same rule applies to every topic — `2.md` → `2-1 … 2-15`, `11.md` → `11-1 … 11-15`, and so on.

---

## A) Editing a CHAPTER's content (the file you edit most)

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

## B) Editing a TOPIC hub (rename / add / remove chapters)

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

## How to publish (for Sir / TA)

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

_Maintained by Teaching Assistant Team (IIITA)._
