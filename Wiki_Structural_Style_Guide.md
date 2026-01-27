# Wiki Structural Style Guide

This document outlines the standardized structure for all articles in the One Mine Two Stars Wiki to ensure structural congruence and consistency across all pages.

## Page Structure Template

All wiki articles should follow this basic HTML structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Article Title - One Mine Two Stars Wiki</title>
  <link rel="icon" type="image/png" href="assets/images/favicon.png">
  <link rel="stylesheet" href="WikiStyle.css">
</head>
<body>
  <div class="top-banner">
    <a href="index.html" class="home-button">🏠 Home</a>
  </div>

  <h1 class="gradient-title">Article Title</h1>
  <div class="subtitle">Subtitle if applicable</div>

  <!-- Infobox (for character bios) -->
  <div class="infobox">
    <table class="infobox">
      <tr>
        <td colspan="2" class="text-center pb-2">
          <img src="assets/images/image-filename.jpg" alt="Portrait description" class="portrait">
          <div class="image-caption">Image caption</div>
        </td>
      </tr>
      <tr>
        <th>Field Name</th>
        <td>Field Value</td>
      </tr>
      <!-- Add more rows as needed -->
    </table>
  </div>

  <div class="article-content">
    <div class="card-bg">
      <h2 class="section-header">Overview</h2>
      <p>Article overview content goes here...</p>
    </div>

    <!-- Additional content sections as needed -->
  </div>

  <div id="footer">
    <p>Back to <a href="Cast.html">Characters</a> | <a href="index.html">Home</a></p>
    <p>&copy; One Mine Two Stars Wiki</p>
  </div>

  <!-- Back to Top Button -->
  <button id="toTopBtn" aria-label="Return to top">⬆️ Top</button>
  <script>
    const toTopBtn = document.getElementById("toTopBtn");
    window.addEventListener("scroll", () => {
      if (document.documentElement.scrollTop > 200) {
        toTopBtn.style.display = "block";
      } else {
        toTopBtn.style.display = "none";
      }
    });
    toTopBtn.addEventListener("click", () => {
      window.scrollTo({ top: 0, behavior: "smooth" });
    });
  </script>
</body>
</html>
```

## Structural Requirements

### 1. Head Section
- Always include the meta viewport tag for responsive design
- Title format: `"Page Title - One Mine Two Stars Wiki"`
- Include favicon and stylesheet links

### 2. Header Section
- Top banner with home link
- Main title using `gradient-title` class
- Optional subtitle using `subtitle` class

### 3. Content Structure
- **Infobox**: Required for character bios, optional for other articles
- **Article Content**: Container for main content using `article-content` class
- **Card Sections**: Each major section should be wrapped in a `card-bg` div
- **Headers**: Use `section-header` class for h2 elements

### 4. Footer Section
- Standard footer with navigation links
- Copyright notice

### 5. JavaScript Elements
- Consistent "Back to Top" button implementation

## Content Organization

### Character Biographies
Character biographies should include these standard sections when applicable:
- Overview
- Early Life and Background
- Role in Storyline/Key Events
- Personality and Traits
- Key Relationships
- Quotes (if applicable)

### Technical Articles and Other Content
Structure should follow logical topic organization with:
- Overview/Introduction
- Main content sections
- Conclusion or Summary (when appropriate)

## Style Consistency Points

1. **Navigation Links**: Always include link back to index.html and appropriate category page
2. **Image Handling**: Use consistent image paths and include alt text
3. **Internal Links**: Link to other wiki pages using relative paths
4. **Class Usage**: Use consistent CSS classes for styling elements
5. **Heading Hierarchy**: Maintain proper heading structure (h1 for title, h2 for sections, h3 for subsections)

## Implementation Notes

For existing articles that don't follow this structure, gradually update them to match these standards. The goal is to achieve structural congruence across all wiki content while preserving the existing information.