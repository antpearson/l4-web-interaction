# Portfolio Task - Music Festival Website

## Task Overview
Create a complete music festival website that demonstrates your skills in CSS background images and Flexbox layouts. This is your opportunity to show everything you've learned this week!

## What You're Building
A multi-section website for "SoundWave Festival 2025" featuring:
1. **Hero Section** - Full-width banner with background image
2. **Artist Lineup** - Flexible grid of artist cards
3. **Information Section** - Two-column layout (sidebar + main content)
4. **Optional Footer** - Contact and social media info

## Requirements Checklist

### ✅ File Setup
- [ ] Create `music-festival.html` in your skills-portfolio folder
- [ ] Create `music-festival.css` in your skills-portfolio folder
- [ ] Link the CSS file to your HTML
- [ ] Create an `images` folder for festival photos

### ✅ Hero Section
- [ ] Add a background image (provided in images folder)
- [ ] Use `background-size: cover;`
- [ ] Set minimum height to 400px
- [ ] Add semi-transparent overlay for text readability
- [ ] Include festival name and dates as overlaid text
- [ ] Center the text vertically and horizontally
- [ ] Ensure text color contrasts well with background

### ✅ Artist Lineup Section
- [ ] Create container with `display: flex;`
- [ ] Add `flex-wrap: wrap;` for responsive behavior
- [ ] Include at least 6 artist cards
- [ ] Each card should contain:
  - Artist/band name
  - Performance time
  - Stage name
  - Optional: genre or image
- [ ] Use `gap` for spacing between cards
- [ ] Cards should be equal width using flex properties
- [ ] Add hover effects to cards

### ✅ Two-Column Information Section
- [ ] Create flex container for two-column layout
- [ ] Sidebar (fixed width ~250-300px):
  - Festival location
  - Dates and times
  - Ticket prices
  - Key facilities
- [ ] Main content (flexible width):
  - Festival description
  - What to bring
  - How to get there
  - Sustainability info
- [ ] Use appropriate flex properties

### ✅ Responsive Design
- [ ] Cards wrap to new rows on smaller screens
- [ ] Use `flex: 1 1 300px;` or similar for cards
- [ ] Test at different screen widths
- [ ] Ensure nothing breaks on mobile view

### ✅ Styling & Polish
- [ ] Consistent color scheme throughout
- [ ] Proper use of padding and margins
- [ ] Use `box-sizing: border-box;`
- [ ] Text is readable on all backgrounds
- [ ] Smooth hover effects
- [ ] Professional appearance

## Getting Started

### Step 1: HTML Structure
Create the basic structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SoundWave Festival 2025</title>
    <link rel="stylesheet" href="music-festival.css">
</head>
<body>
    <!-- Hero Section -->
    <header class="hero">
        <!-- Hero content here -->
    </header>

    <!-- Artist Lineup -->
    <section class="lineup">
        <h2>Artist Lineup</h2>
        <div class="lineup-container">
            <!-- Artist cards here -->
        </div>
    </section>

    <!-- Information Section -->
    <section class="info-section">
        <aside class="sidebar">
            <!-- Sidebar info -->
        </aside>
        <div class="main-content">
            <!-- Main content -->
        </div>
    </section>
</body>
</html>
```

### Step 2: CSS Reset
Start your CSS with:
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
}
```

### Step 3: Hero Section
```css
.hero {
    background: url('images/festival-hero.jpg') no-repeat center / cover;
    min-height: 400px;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}

/* Overlay for text readability */
.hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
}
```

### Step 4: Artist Cards
```css
.lineup-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

.artist-card {
    flex: 1 1 300px;
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
```

### Step 5: Two-Column Layout
```css
.info-section {
    display: flex;
    gap: 30px;
    max-width: 1200px;
    margin: 40px auto;
    padding: 20px;
}

.sidebar {
    flex: 0 0 250px; /* Fixed width */
    background: #f8f9fa;
    padding: 20px;
}

.main-content {
    flex: 1; /* Takes remaining space */
}
```

## Content Provided
All content is in `festival-content.txt`:
- Festival name and dates
- 10 artist names with times and stages
- Sidebar information
- Main content paragraphs
- Footer information

## Images Needed

### You Need to Provide:
1. **Hero background image** - Wide landscape photo (1920x1080 minimum)
   - Suggested: concert crowd, festival atmosphere, stage setup
   - Free sources: Unsplash, Pexels, Pixabay
   - Save as: `festival-hero.jpg`

2. **Optional: Artist card images** - Square photos for each artist
   - Can use icons, patterns, or colored blocks instead
   - Keep file sizes reasonable (under 500KB each)

## Testing Your Work

### Visual Checks:
- [ ] Hero image loads and covers the section
- [ ] Hero text is clearly readable
- [ ] Cards arrange in rows (2-3 per row on desktop)
- [ ] Cards wrap to new rows when resized
- [ ] Sidebar and main content sit side-by-side
- [ ] All spacing looks professional
- [ ] Hover effects work smoothly

### Resize Testing:
1. Start with full-screen browser
2. Gradually make window narrower
3. Check cards wrap appropriately
4. Verify nothing overlaps or breaks
5. Test on mobile size (375px width)

## Common Mistakes to Avoid

❌ **DON'T:**
- Forget `display: flex` on containers
- Use fixed widths on cards (use flex instead)
- Forget `flex-wrap: wrap` for responsive cards
- Use low-quality or wrong-sized images
- Forget fallback background colors
- Skip testing at different screen sizes
- Forget to add `box-sizing: border-box`

✅ **DO:**
- Use semantic HTML (`<header>`, `<section>`, `<aside>`)
- Test your layout by resizing the browser
- Use appropriate image sizes (not too large!)
- Add hover effects for interactivity
- Use consistent spacing and colors
- Comment your CSS for clarity
- Validate your HTML

## Bonus Challenges (Optional)

### Level 1 - Easy
- [ ] Add a navigation bar at the top using Flexbox
- [ ] Add a footer with social media links
- [ ] Use Google Fonts for better typography
- [ ] Add icons to the sidebar items

### Level 2 - Medium
- [ ] Add background patterns or textures to sections
- [ ] Create "featured" artist cards that are larger
- [ ] Add multiple background images with layers
- [ ] Include a map or embedded Google Maps

### Level 3 - Advanced
- [ ] Add media queries to change layout on mobile
- [ ] Create a ticket purchase button with modal
- [ ] Add smooth scroll to anchor links
- [ ] Implement a sticky navigation bar
- [ ] Add CSS animations to cards on scroll

## Grading Criteria

Your work will be assessed on:
1. **Functionality** (40%)
   - All required sections present
   - Flexbox used correctly
   - Background images implemented
   - Responsive behavior works

2. **Code Quality** (30%)
   - Clean, organized HTML/CSS
   - Proper use of semantic elements
   - Good naming conventions
   - Comments where helpful

3. **Design** (20%)
   - Professional appearance
   - Good use of color and spacing
   - Typography is readable
   - Images are appropriate

4. **Responsiveness** (10%)
   - Works on different screen sizes
   - Cards wrap appropriately
   - Nothing breaks at mobile sizes

## Resources

### Finding Images
- [Unsplash](https://unsplash.com/) - Free high-quality photos
- [Pexels](https://pexels.com/) - Free stock photos
- [Pixabay](https://pixabay.com/) - Free images and videos

### Color Schemes
- [Coolors](https://coolors.co/) - Color palette generator
- [Adobe Color](https://color.adobe.com/) - Color wheel tool

### Flexbox Help
- Week 6 tutorial (this week's content)
- [CSS-Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox Froggy](https://flexboxfroggy.com/) - Practice game

## Submission

Save your completed files:
```
skills-portfolio/
├── music-festival.html
├── music-festival.css
└── images/
    ├── festival-hero.jpg
    └── [any other images]
```

Your tutor will review your work in next week's session. Be prepared to:
- Demonstrate your website working
- Explain your Flexbox layout choices
- Show how it responds to different screen sizes
- Discuss any challenges you faced

## Need Help?

If you're stuck:
1. Review the Week 6 tutorial
2. Check the exercise examples
3. Ask in the discussion forum
4. Attend office hours
5. Review CSS-Tricks Flexbox Guide

**Good luck and have fun creating your festival website!** 🎵🎉
