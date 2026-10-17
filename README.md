# Student Management System

## Experiment: Gitflow and Merge Conflict Resolution

### Overview
This repository demonstrates a complete Gitflow branching workflow, feature development, intentional merge conflict generation, and manual resolution.

---

### Project Structure & Files
- **`student.txt`**: Core application specification containing student management feature definitions and data fields.
- **`README.md`**: Project documentation and experiment walkthrough.

#### Content of `student.txt`:
```text
Student Management System
Feature: Manage and display student information
Fields: Name, Roll Number, Marks
```

---

### Branching Strategy (Gitflow)
- **`main`**: Production-ready, stable releases.
- **`develop`**: Integration branch for accumulating completed features and resolutions.
- **`feature/student-details`**: Feature branch for developing student record management features.

---

### Merge Conflict & Resolution Summary
1. **Divergence:**
   - On `develop`: Line 2 updated to `Feature: Manage student records`
   - On `feature/student-details`: Line 2 updated to `Feature: Display student information`
2. **Conflict Trigger:**
   - Running `git merge feature/student-details` into `develop` produced a content merge conflict on Line 2.
3. **Resolution:**
   - Both changes were reconciled into:  
     `Feature: Manage and display student information`
   - Resolved file staged and committed as merge commit.

---

### Verification
Run the following command in terminal to view the complete commit tree:
```bash
git log --oneline --graph --all
```