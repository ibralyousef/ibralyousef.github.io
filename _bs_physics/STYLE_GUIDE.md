# Course Page Style Guide for BS Physics

This guide ensures consistency across all course pages in the `_bs_physics` directory.

## Standard Collapsible Section Structure

**ALL course pages MUST include these 6 sections in this exact order:**

1. **Textbooks & References** - `<i class="fas fa-book"></i>`
2. **Homework & Assignments** - `<i class="fas fa-file-alt"></i>`
3. **Exams & Solutions** - `<i class="fas fa-chart-bar"></i>`
4. **Quizzes & Solutions** - `<i class="fas fa-check-circle"></i>`
5. **Lecture Notes** - `<i class="fas fa-book-open"></i>`
6. **Computational Materials** - `<i class="fas fa-laptop-code"></i>`

### Additional Specialized Sections (Optional)

Add these AFTER the 6 standard sections when applicable:

- **Lab Materials** - `<i class="fas fa-flask"></i>` (for laboratory courses)
- **Projects** - `<i class="fas fa-clipboard-list"></i>` (for project-based courses)
- **Seminar Materials** - `<i class="fas fa-chart-bar"></i>` (for seminar courses like PHYS 499)
- **Research Materials** - `<i class="fas fa-clipboard-list"></i>` (for research courses like PHYS 497)

## Section Template

### Basic Structure
```markdown
<details>
<summary><strong><i class="fas fa-[ICON]"></i> [Section Title]</strong></summary>
<ul>
<li><a href="/assets/resources/[path]/[file].pdf">[Description]</a></li>
</ul>
</details>
```

### First Section (Always Open)
The first section (Textbooks & References) should always be open by default:
```markdown
<details open>
<summary><strong><i class="fas fa-book"></i> Textbooks & References</strong></summary>
```

### Empty Sections
If a section has no content yet, use this placeholder:
```markdown
<details>
<summary><strong><i class="fas fa-[ICON]"></i> [Section Title]</strong></summary>
<ul>
<li>No materials available yet</li>
</ul>
</details>
```

## Complete Course Page Template

```markdown
---
layout: course
code: PHYS XXX
title: [Course Title]
slug: physXXX
credits: X-X-X
level: XXX
description: [Course description]
prerequisites: [Prerequisites]
semester_offered: F/S/F,S
course_type: Core/Elective
---

[Course description paragraph]

**Prerequisites:** [Prerequisites]

## <i class="fas fa-book"></i> Course Resources

<details open>
<summary><strong><i class="fas fa-book"></i> Textbooks & References</strong></summary>
<ul>
<li><a href="/assets/resources/core/physXXX/textbooks/[file].pdf">[Book Title - Author]</a></li>
</ul>
</details>

<details>
<summary><strong><i class="fas fa-file-alt"></i> Homework & Assignments</strong></summary>
<ul>
<li><a href="/assets/resources/core/physXXX/homework/[file].pdf">Homework 1</a></li>
</ul>
</details>

<details>
<summary><strong><i class="fas fa-chart-bar"></i> Exams & Solutions</strong></summary>
<ul>
<li><a href="/assets/resources/core/physXXX/exams/[file].pdf">Major Exam I - Solution</a></li>
</ul>
</details>

<details>
<summary><strong><i class="fas fa-check-circle"></i> Quizzes & Solutions</strong></summary>
<ul>
<li><a href="/assets/resources/core/physXXX/quizzes/[file].pdf">Quiz 1 - Solution</a></li>
</ul>
</details>

<details>
<summary><strong><i class="fas fa-book-open"></i> Lecture Notes</strong></summary>
<ul>
<li><a href="/assets/resources/core/physXXX/notes/[file].pdf">Chapter 1 - Notes</a></li>
</ul>
</details>

<details>
<summary><strong><i class="fas fa-laptop-code"></i> Computational Materials</strong></summary>
<ul>
<li><a href="/assets/resources/core/physXXX/computational/[file].nb">[Description] (Mathematica)</a></li>
</ul>
</details>
```

## File Naming Conventions

### Link Text Format
- **Homework:** "Homework [Number]" or descriptive title
- **Exams:** "Major Exam [Number] - Solution" or "Final Exam - Solution"
- **Quizzes:** "Quiz [Number] - Solution"
- **Lecture Notes:** "Chapter [Number] - [Topic]" or descriptive title
- **Computational:** "[Description] (Software Name)"

### Path Structure
All resources should follow this path pattern:
```
/assets/resources/[core|elective]/physXXX/[category]/[filename]
```

Where `[category]` is one of:
- `textbooks`
- `homework`
- `exams`
- `quizzes`
- `notes`
- `computational`
- `lab` (for lab materials)
- `projects`

## Important Rules

### DO NOT:
- Mix icons with different section titles
- Use `fas fa-clipboard-list` for "Homework Assignments" (use `fas fa-file-alt` for "Homework & Assignments")
- Use variations like "Homework & Solutions" or "Homework Assignments"
- Combine "Quizzes & Exams" in one section (keep them separate)
- Use `fas fa-book-open` for multiple different purposes
- Change the order of the standard 6 sections
- Omit any of the standard 6 sections (use placeholder if empty)

### ALWAYS:
- Include all 6 standard sections, even if empty
- Use exact icon-title pairings as specified
- Keep the first section (Textbooks & References) open by default
- Place specialized sections AFTER the standard 6
- Use "No materials available yet" for empty sections
- Maintain consistent link text formatting

## Examples of Common Mistakes to Avoid

❌ **Wrong:**
```markdown
<summary><strong><i class="fas fa-clipboard-list"></i> Homework Assignments</strong></summary>
```

✅ **Correct:**
```markdown
<summary><strong><i class="fas fa-file-alt"></i> Homework & Assignments</strong></summary>
```

❌ **Wrong:**
```markdown
<summary><strong><i class="fas fa-chart-bar"></i> Quizzes & Exams</strong></summary>
```

✅ **Correct:** (Two separate sections)
```markdown
<summary><strong><i class="fas fa-chart-bar"></i> Exams & Solutions</strong></summary>
...
<summary><strong><i class="fas fa-check-circle"></i> Quizzes & Solutions</strong></summary>
```

## Validation Checklist

Before committing any course page, verify:
- [ ] All 6 standard sections are present in the correct order
- [ ] Icons match the section titles exactly as specified
- [ ] First section has `<details open>` attribute
- [ ] Empty sections have "No materials available yet" placeholder
- [ ] No duplicate or redundant sections
- [ ] Specialized sections appear after the standard 6
- [ ] File paths follow the `/assets/resources/[type]/physXXX/[category]/` pattern

## Adding New Content

When adding new materials to existing sections:
1. Maintain alphabetical or numerical order within sections
2. Use consistent naming patterns (e.g., all homework as "Homework 1", "Homework 2", etc.)
3. Include file format in parentheses for computational materials (e.g., "(Mathematica)", "(Python)", "(PDF)")
4. For solutions, always append " - Solution" to the title

---

*Last Updated: January 2025*
*This guide ensures consistency across all physics course pages. Any deviations require explicit justification and should be documented.*