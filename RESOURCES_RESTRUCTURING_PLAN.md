# Comprehensive Resources Restructuring Plan

## 1. **Reorganize Courses by Level Number (100, 200, 300, 400)**

### Current Structure:
- Grouped by: Freshman, Sophomore, Junior, Senior
- Not aligned with actual course numbers

### New Structure:
```yaml
100-level:  # Introductory Courses
  - PHYS 101, 102, 133

200-level:  # Intermediate Courses  
  - PHYS 201, 203, 204, 205, 210, 211, 212, 213, 215

300-level:  # Advanced Undergraduate
  - PHYS 300, 305, 306, 308, 309, 310, 336, 373, 399

400-level:  # Senior & Specialized
  - PHYS 403, 410, 422, 423, 430, 432, 441, 497, 499
```

## 2. **Minimalistic Course Pages**

### Remove:
- Vibrant colors (blue links, colored badges)
- Complex layouts and cards
- Extensive inline content

### Keep:
- Simple course information extracted from KFUPM Bulletin
- Clean list of available resources
- Links to files in respective folders

### New Course Page Structure:
```markdown
---
layout: course
code: PHYS 101
title: General Physics I
credits: 3-3-4
level: 100
---

Particle kinematics and dynamics; conservation of energy...
[Simple description from KFUPM Bulletin]

**Prerequisites:** None
**Corequisites:** MATH 101

## Resources
[Auto-generated list of files from /assets/resources/phys101/]
```

## 3. **Minimalistic Design Changes**

### Colors:
- Remove all `text-primary` (blue) classes
- Use only grays and whites
- Maintain dark mode consistency

### Layout:
- Simple hierarchical list (like Categories)
- No cards or badges
- Plain text descriptions
- Monospace font for course codes

### CSS Updates:
```css
.level-title { 
  color: white; 
  font-weight: normal;
}
.course-link { 
  color: inherit; /* No blue */
  text-decoration: none;
}
.course-link:hover {
  text-decoration: underline; /* Simple hover */
}
```

## 4. **Enable Dark/Light Mode Toggle**

### Config Change (_config.yml):
```yaml
# Current:
theme_mode: dark

# Change to:
theme_mode: # Empty = allows toggle
```

This enables the theme toggle button in the sidebar (already built into Chirpy theme).

## 5. **File Organization**

### Current Issues:
- Duplicate files across multiple folders
- Inconsistent organization
- Files scattered in wrong level folders

### Solution:
- Single folder per course: `/assets/resources/phys[number]/`
- Remove duplicates
- Organize all files by actual course number

## 6. **Data Structure Update**

### _data/courses.yml:
```yaml
100-level:
  title: "100-Level Courses"
  courses:
    - code: "PHYS 101"
      name: "General Physics I"
      slug: "phys101"
      credits: "3-3-4"
      description: "Particle kinematics and dynamics..."
      prerequisites: "None"
      
200-level:
  title: "200-Level Courses"
  courses:
    - code: "PHYS 204"
      name: "General Physics III"
      slug: "phys204"
      credits: "3-3-4"
      description: "Inductance, AC circuits..."
      prerequisites: "MATH 102, PHYS 102"
```

## 7. **Implementation Steps**

1. **Update _config.yml**
   - Remove `theme_mode: dark` or set to empty

2. **Restructure _data/courses.yml**
   - Group by 100, 200, 300, 400 levels
   - Add course info from KFUPM Bulletin

3. **Simplify _layouts/resources.html**
   - Remove custom colors
   - Use native theme classes only

4. **Update _layouts/course.html**
   - Minimalistic design
   - Auto-list files from folders
   - No vibrant colors

5. **Reorganize files**
   - Move to proper course folders
   - Remove duplicates

6. **Update course markdown files**
   - Extract info from KFUPM Bulletin
   - Minimal formatting

## 8. **Benefits**

- **Clean & Professional**: No distracting colors
- **Easy Navigation**: Courses grouped by level
- **Consistent**: Matches Categories tab style
- **Accessible**: Dark/light mode toggle
- **Maintainable**: Simple structure
- **Scalable**: Easy to add new courses

## 9. **Course Information from KFUPM Bulletin**

### PHYS 101 - General Physics I
**Credits:** 3-3-4  
**Description:** Particle kinematics and dynamics; conservation of energy and momentum; rotational motion; periodic motion; introduction to special relativity.

### PHYS 102 - General Physics II  
**Credits:** 3-3-4  
**Prerequisites:** PHYS 101  
**Description:** Electric field and potential; capacitance and inductance; current, resistance, and simple DC and AC circuits; magnetic fields; Faraday's law; electromagnetic waves; geometrical and physical optics.

### PHYS 204 - General Physics III
**Credits:** 3-3-4  
**Prerequisites:** MATH 102, PHYS 102  
**Description:** Inductance; magnetic properties of matter, electromagnetic oscillations and waves; geometrical and physical optics. Modern physics topics including relativity, quantum physics, atomic physics, nuclear physics.

### PHYS 300 - Classical Mechanics
**Credits:** 3-0-3  
**Prerequisites:** PHYS 102, MATH 201  
**Description:** Newton's laws and their application; oscillatory motion; central force motion; rigid body motion; Lagrangian and Hamiltonian formulations.

## 10. **File Structure After Implementation**
```
assets/resources/
├── phys101/
│   ├── textbooks/
│   ├── solutions/
│   ├── exams/
│   └── notes/
├── phys102/
├── phys204/
└── ... (organized by course number)
```