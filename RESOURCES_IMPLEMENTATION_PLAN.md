# Resources Implementation Plan

## Architecture Overview
Create a **two-tier system** where the main Resources tab shows a clean overview with 1-2 featured resources per course, then links to dedicated course pages with full content.

## 1. **Jekyll Collection for Courses**
Add to `_config.yml`:
```yaml
collections:
  courses:
    output: true
    permalink: /resources/:collection/:name/
```

## 2. **Directory Structure**
```
_courses/
├── phys101.md
├── phys102.md
├── phys204.md
└── ... (one .md file per course)

assets/resources/
└── [keep existing organized file structure]
```

## 3. **Main Resources Tab** (`_tabs/resources.md`)
- Keep existing card layout but simplified
- Each card shows:
  - Course code & name
  - Brief description (1-2 lines)
  - **Featured resources** (1-2 most important files)
  - "View All Resources →" button linking to course page

## 4. **Individual Course Pages** (`_courses/phys101.md`)
Example structure:
```markdown
---
layout: course
code: PHYS 101
title: Fundamental Physics I
level: freshman
category: core
credits: 4
description: Introduction to mechanics, thermodynamics...
prerequisites: None
instructor: Dr. Name
---

## Course Overview
[Your custom markdown content here]

## Learning Objectives
- Understand Newton's laws
- Apply conservation principles
- ...

## Course Topics
1. Kinematics
2. Dynamics
3. Energy & Momentum
...

## Important Notes
[Any special instructions, tips, etc.]
```

## 5. **Course Layout** (`_layouts/course.html`)
- Header with course info (code, title, credits)
- Markdown content area (fully editable by you)
- Resources section (auto-populated from YAML)
- Download buttons for all resources
- Navigation back to main resources page

## 6. **Data Structure** (`_data/resources.yml`)
Simplified to:
```yaml
phys101:
  featured:  # Shows on main page
    - name: "Textbook (10th Ed.)"
      path: "/assets/resources/..."
    - name: "Formula Sheet"
      path: "/assets/resources/..."
  
  all:  # Shows on course page
    textbooks:
      - name: "Fundamentals of Physics"
        path: "..."
    exams:
      - name: "Past Finals"
        path: "..."
    # ... etc
```

## 7. **Key Benefits**
- **Clean overview page** - not overwhelming
- **SEO-friendly** - each course has its own URL
- **Easy to edit** - just markdown files for course details
- **Scalable** - add new courses by creating new .md files
- **Flexible content** - mix auto-generated resources with custom content
- **Better navigation** - students can bookmark specific courses

## 8. **Implementation Steps**

### Step 1: Add courses collection to _config.yml
- [x] Research existing Jekyll collections structure
- [ ] Add courses collection configuration
- [ ] Set up proper permalink structure

### Step 2: Create _courses directory structure  
- [ ] Create `_courses/` directory
- [ ] Plan file naming convention (e.g., phys101.md, phys102.md)
- [ ] Set up directory permissions

### Step 3: Create course layout template (_layouts/course.html)
- [ ] Design course page header with metadata
- [ ] Create markdown content area
- [ ] Build resources section with auto-population
- [ ] Add navigation breadcrumbs
- [ ] Style consistently with site theme

### Step 4: Create sample course markdown files
- [ ] Create phys101.md template
- [ ] Create phys102.md template  
- [ ] Add front matter with all required fields
- [ ] Write sample course content for testing

### Step 5: Simplify main resources page to show overview with featured resources
- [ ] Modify existing _layouts/resources.html
- [ ] Update card layout to show only featured resources
- [ ] Add "View All Resources" buttons
- [ ] Maintain search and filter functionality
- [ ] Update styling for cleaner look

### Step 6: Update data structure for featured vs all resources
- [ ] Restructure _data/resources.yml
- [ ] Separate featured resources from complete lists
- [ ] Update resource paths to match new structure
- [ ] Add metadata for course pages

### Step 7: Test the new implementation
- [ ] Run Jekyll server
- [ ] Test main resources page navigation
- [ ] Test individual course pages
- [ ] Verify all download links work
- [ ] Test search functionality
- [ ] Check mobile responsiveness

## 9. **Enhanced Features**
- **Search** works across all course pages
- **Tags** for course difficulty, semester offered
- **Related courses** suggestions
- **Quick links** in sidebar for navigation
- **Breadcrumbs** for easy navigation

## 10. **File Structure After Implementation**
```
ibralyousef.github.io/
├── _config.yml (updated with courses collection)
├── _tabs/
│   └── resources.md (simplified overview)
├── _layouts/
│   ├── resources.html (updated)
│   └── course.html (new)
├── _courses/
│   ├── phys101.md
│   ├── phys102.md
│   ├── phys204.md
│   ├── ...
├── _data/
│   └── resources.yml (restructured)
└── assets/
    └── resources/
        └── [existing file structure]
```

## 11. **Content Management**
- **Easy editing**: Just edit markdown files in `_courses/`
- **Add new courses**: Create new `.md` file in `_courses/`
- **Update resources**: Modify `_data/resources.yml`
- **Custom content**: Full markdown support in course pages
- **Consistent styling**: Automatic theme application

## 12. **SEO & Navigation Benefits**
- Each course gets its own URL: `/resources/courses/phys101/`
- Better search engine indexing
- Bookmarkable course pages
- Clean URL structure
- Improved site navigation