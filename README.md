[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vi5FCpOf)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=21970176&assignment_repo_type=AssignmentRepo)
# Normalization and Normal Forms

This repository is used to submit your work for the “Normalization and Normal Forms” practical assignment in Database Systems.

In this assignment you will:
- Analyze a single large table for functional and transitive dependencies.
- Normalize a schema to 3NF (or justify staying in 2NF if appropriate).
- Translate the final normalized design into a Crow’s Foot ERD.

---

## 1. Source Table (STUDENT)

We start from the **STUDENT** table shown in Table P6.4.

> In the repository you will find the file 'student_table_p64.png':
> ![Dependency Diagram](student_table_p64.png)
>
> containing the table with attributes and sample rows.

Main attributes (column names):

- `STU_NUM`  
- `STU_LNAME`  
- `STU_MAJOR`  
- `DEPT_CODE`  
- `DEPT_NAME`  
- `DEPT_PHONE`  
- `COLLEGE_NAME`  
- `ADVISOR_LNAME`  
- `ADVISOR_OFFICE`  
- `ADVISOR_BLDG`  
- `ADVISOR_PHONE`  
- `STU_GPA`  
- `STU_HOURS`  
- `STU_CLASS`

---

## 2. Tasks

Create a file named **`answers.md`** (or `answers.pdf` / `answers.docx` if allowed) and provide **clear, numbered solutions** to tasks (a)–(c) below. You may also include hand-drawn diagrams as images if that is more convenient (for example, `dependency_diagram.png`, `erd.png`).

### (a) Unnormalized schema and dependency analysis

1. **Write the relational schema** for the original STUDENT table, using standard notation, e.g.:

   ```text
   STUDENT(STU_NUM, STU_LNAME, ..., STU_CLASS)

2. **Draw the dependency diagram** for this schema.

   * Identify **all functional dependencies**.
   * Clearly mark **primary key(s)** and **all transitive dependencies**.
   * You may create this diagram using any tool (draw.io, Lucidchart, hand-drawn + photo, etc.) and save it as an image in the repo.

Describe your assumptions explicitly (for example, whether department phone depends on department code, etc.).

---

### (b) Normalization to 3NF (or justified 2NF)

3. **Normalize the schema** to meet **Third Normal Form (3NF)** requirements to the greatest practical extent possible.

   * Decompose the original STUDENT table into several relations.
   * For each relation, write its **relational schema**, underline the **primary key**, and list any **foreign keys**.

4. **Draw the dependency diagram(s)** for your 3NF design.

   * Show all determinants and dependencies within each relation.
   * If you believe that practical considerations justify leaving some relation in **2NF**, clearly:

     * Identify that relation.
     * Explain **why** keeping it in 2NF is reasonable (e.g., performance, simplicity, low redundancy in this context, etc.).

5. If needed, **add or rename attributes** to:

   * Create appropriate determinants.
   * Ensure that the design follows good **naming conventions** (e.g., consistent prefixes, no spaces, meaningful names).

---

### (c) Crow’s Foot ERD

5. Using your **final normalized design** from part (b), draw the **Crow’s Foot ERD**.

   * Show all entities, primary keys, and important attributes.
   * Include all relationships, with correct **connectivity and optionality**.
   * Indicate foreign keys using standard Crow’s Foot notation (or by listing them in the entity boxes).

> **Important note:** Although completed student hours (`STU_HOURS`) are related to student classification (`STU_CLASS`), this dependency is not a simple 1:1 mapping. For example, a student is considered a junior if they have completed between 61 and 90 credit hours. Take this into account when reasoning about functional dependencies and normalization.

Save your ERD as an image (for example, `student_erd.png`) and reference it from `answers.md`.

---

## 3. Deliverables

To complete the assignment, you must:

1. **Clone** the GitHub Classroom repository to your local machine.

2. Add the following files:

   * `answers.md` (or `answers.pdf` / `answers.docx`) with your written answers and explanations.
   * One or more image files with your dependency diagram(s) and ERD (for example,
     `dependency_diagram.png`, `normalized_dependency_diagram.png`, `student_erd.png`).

3. **Reference** your diagrams from `answers.md` using Markdown, e.g.:

   ```markdown
   ![Dependency Diagram](dependency_diagram.png)
   ```

4. **Commit and push** all changes to the repository before the deadline.

Suggested structure:

```text
.
├── student_table_p64.png          # Provided source table (Table P6.4)
├── README.md                      # This file
├── answers.md                     # Your written answers
├── dependency_diagram.png         # Part (a)
├── normalized_dependency_diagram.png  # Part (b)
└── student_erd.png                # Part (c)
```

## 4. Academic Integrity

All work must be **your own**.
You may use the textbook, lecture notes, and trusted online resources for reference, but **do not copy solutions** directly from any source or from other students.

Happy normalizing!
