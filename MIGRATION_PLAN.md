# Course Resources Migration Plan - REVISED
## Level 300 & 400 Courses from tmp/ to assets/resources/

---

## Overview
This plan details the migration of course resources from the `tmp/` folder to the organized `assets/resources/` structure, with standardized naming conventions and proper categorization.

## Important Notes
- **Textbooks under 100MB will be INCLUDED** (not skipped)
- **MUST CHECK existing course resources** to determine if homework files are questions or solutions
- **Will READ files during execution** to properly identify and name solution files

## Files to Skip (>100MB ONLY)
- `/tmp/Level#3 - Junior/Physics#300/Numerical Homework/Dr.Saeed Workshop for Mathematica.mp4` (230MB - video file)
- `/tmp/Physics#xxx/PHYS#373/PHYS 373.zip` (124MB - compressed file)

---

## Implementation Process

### Critical Step: File Content Verification
**During execution (not now), I will:**
1. **READ each homework/quiz/exam file** to determine if it contains solutions
2. **COMPARE with existing files** in assets/resources to avoid duplicates
3. **NAME files appropriately:**
   - If it's a solution: `HW1_Solution.pdf`
   - If it's just questions: `HW1.pdf`
   - If both exist: Keep both with clear naming

---

## Level 300 (Junior) Courses

### PHYS 300 - Classical Mechanics ✅
**Must check existing files:** Currently has 4 files in `/assets/resources/core/phys300/`
- **Action:** READ existing .nb files to compare with new homework files

**Resources to Add:**
- **Textbooks (INCLUDE - under 100MB):**
  - `Classical Dynamics of Particles & Systems - Marion & Thornton.pdf`
  - `Classical Mechanics John Taylor - PDF Room.pdf` (54MB - INCLUDE)

- **Homework:** 
  - **MUST READ** each file to determine if solution or questions
  - Files to check:
    - `PHYS-300-Numerical-HW-1.pdf`
    - `PHYS300-Numerical-HW2.pdf`
    - `PHYS300NumericalHW3.pdf`
    - `HW-4-Swinging Atwood Machine.pdf`

- **Exams:** Files labeled "Solution" are clearly solutions
- **Quizzes:** Files labeled "Solution" are clearly solutions

### PHYS 305 - Electricity & Magnetism I 🆕 (New course)
**Textbook:** `David J. Griffiths-Introduction to Electrodynamics` (INCLUDE if <100MB)
**MUST READ** homework files - no "solution" labels, need to verify content

### PHYS 306 - Electricity & Magnetism II 🆕 (New course)
**Textbook:** `David J. Griffiths-Introduction to Electrodynamics` (INCLUDE if <100MB)
**MUST READ** homework files - no "solution" labels, need to verify content

### PHYS 308 - Electronics 🆕 (New course)
**Homework:** Already labeled "(solution)" - clear identification
**Notes:** Extensive subfolder structure to preserve

### PHYS 309 - Experimental Physics ✅
Basic resources - no homework files to verify

### PHYS 310 - Quantum Mechanics I ✅
**Must check existing files:** Currently has 6 files
- **Action:** Compare new homework with existing computational materials

**Resources to Add:**
- **Textbooks (INCLUDE ALL):**
  - `E-BOOK Zettili.pdf` (INCLUDE)
  - `Griffiths - Introduction to quantum mechanics.pdf` (INCLUDE)

- **Homework:**
  - **MUST READ** to verify if solutions are included
  - No "solution" in filename - need to check content

---

## Level 400 (Senior) Courses

### PHYS 403 - Senior Lab ✅
Lab manuals - no homework to verify

### PHYS 410 - Quantum Mechanics II ✅
**Homework:** "NHW" files - need to READ to determine content
**Quizzes/Exams:** Clearly labeled as solutions

### PHYS 422 - Nuclear Physics ✅
**All homework files explicitly labeled "Solutions"** - no checking needed

**Include ALL textbooks (even if large but <100MB):**
- `1.Introductory Nuclear Physics-Kenneth S. Krane.pdf` (INCLUDE)
- `2. Modern Physics 3rd Edition (Serway, Moses, Moyer).pdf` (INCLUDE)
- `3. Nuclei and Particles-An Introduction (Segre).pdf` (INCLUDE)
- `4. Subatomic Physics (Henley, Garcia).pdf` (INCLUDE)
- `5. The Atomic Nucleus (Evans).djvu` (INCLUDE)

### PHYS 423 - Physics of Nuclear Reactors 🆕 (New course)
**Textbook:** `Lewis - Fundamentals of Nuclear Reactor Physics` (INCLUDE if <100MB)
**MUST READ** homework files to identify which are solutions

### PHYS 430 - Thermal & Statistical Physics ✅
Basic textbooks and course info - no homework verification needed

### PHYS 432 - Introduction to Solid State Physics 🆕 (New course)
**Textbook:** `kittel.pdf` (INCLUDE)

### PHYS 336 - Semiconductors ✅
**Include ALL textbooks:**
- `Physics of Semiconductor Devices.pdf`
- `Semiconductor Physics and Devices Neaman.pdf`
- `Sol_semiconductor-physics-and-devices-4th-edition-neaman.pdf` (clearly solutions)

### PHYS 373 - Computational Physics ✅
**Must check existing files:** Currently has 15 files including labs and quizzes
- **Action:** Compare new materials with existing Lab01-12.ipynb files

**Skip only:**
- `PHYS 373.zip` (124MB)
- `PHYS373_T222.zip` (66MB)

**Include ALL textbooks:**
- `Computational Physics Problem Solving with Python.pdf` (INCLUDE)
- `Python for Everyone2ndEdition.pdf` (INCLUDE)
- `numerical_analysis_9th.pdf` (INCLUDE)

### PHYS 399 - Summer Training ✅
Basic forms - no homework verification needed

### PHYS 441 - Particle Physics ✅
**Include textbooks under 100MB:**
- `9781420083002.pdf` (INCLUDE)
- `Introduction to Elementary Particles, 2nd Edition by David Jeffery Griffiths (1).pdf` (64MB - INCLUDE)
- `Griffiths_Particle_Physics_Solutions_Manual.pdf` (INCLUDE)

### PHYS 497 & 499 ✅
No additional resources found

---

## New Courses to Create

1. **PHYS 305** - Electricity & Magnetism I (Core - Level 300)
2. **PHYS 306** - Electricity & Magnetism II (Core - Level 300)
3. **PHYS 308** - Electronics (Elective - Level 300)
4. **PHYS 423** - Physics of Nuclear Reactors (Elective - Level 400)
5. **PHYS 432** - Introduction to Solid State Physics (Elective - Level 400)

---

## Execution Steps

1. **For each course:**
   - READ existing files in assets/resources to understand current content
   - READ new files from tmp/ to identify if they contain solutions
   - Compare to avoid duplicates
   - Name appropriately based on actual content

2. **Naming Convention:**
   - Questions only: `HW1.pdf`, `Quiz1.pdf`
   - Solutions only: `HW1_Solution.pdf`, `Quiz1_Solution.pdf`
   - Both in one file: `HW1_with_Solutions.pdf`
   - Unclear content: READ file first, then decide

3. **File Size Check:**
   - Skip ONLY files >100MB
   - Include ALL textbooks <100MB
   - Include ALL PDFs <100MB

---

## Summary of Changes from Previous Plan

1. ✅ **Include textbooks under 100MB** (previously skipped at 50MB+)
2. ✅ **Must READ files** to determine if they contain solutions
3. ✅ **Check existing files** before adding to avoid duplicates
4. ✅ **Explicit naming** based on actual content, not just filename

This approach ensures accurate categorization and prevents mislabeling of homework solutions vs. questions.

---

*Generated: August 2025*