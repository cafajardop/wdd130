# WDD 130 - Web Design & Development Fundamentals

## Project Structure & Learning Progression

This is an educational repository for **WDD 130** course with weekly assignments building HTML/CSS skills progressively:

- `week01/` - Basic HTML structure, images, file paths
- `week02/` - CSS box model, layouts, temple card exercises  
- `week03/` - Classes, IDs, float layouts
- `week04/` - Flexbox layouts and responsive design
- `week05/` - Forms, tables, and interactive elements
- `wwr/` - White Water Rafting capstone project

## Architecture & Conventions

### File Organization
- **Weekly exercises**: `weekXX/` contains practice files + `styles/` + `images/` subdirectories
- **Main project**: Root `index.html` is personal homepage, `wwr/` is the rafting business site
- **Shared assets**: Root `images/` and `styles/` for main site; weekly folders have isolated assets

### CSS Architecture
- **CSS Custom Properties**: Use `:root` variables for colors and fonts (see `wwr/styles/rafting.css`)
- **Box model reset**: Standard `* { margin: 0; padding: 0; box-sizing: border-box; }` pattern
- **Layout progression**: Float → Flexbox → Grid (follows weekly curriculum)
- **Container pattern**: `max-width: 840px; margin: 0 auto;` for centered layouts

### HTML Patterns
- **Semantic structure**: Use `header`, `main`, `aside`, `footer`, `section`, `article`
- **Accessibility**: Always include `alt` attributes, proper heading hierarchy
- **Meta tags**: Include `charset`, `viewport`, `author`, `description` in all pages
- **Navigation**: Consistent `nav` structure with `ul/li` or direct `a` elements

## Key Components

### Grid Layout System (`index.html` + `styles/styles.css`)
```css
.grid {
  display: grid;
  align-items: center;
}
main { grid-column: 2 / 3; }
aside { grid-column: 1 / 2; }
```

### Box Component Pattern
- `.box` class for consistent styling: border, padding, background
- Used across weekly exercises for visual consistency

### WWR Project (`wwr/`)
- **Color system**: CSS custom properties in `:root` with primary/secondary/accent colors
- **Component structure**: Logo + nav header, hero sections, figure galleries
- **Social media footer**: SVG icons with consistent styling

## Development Workflow

### Adding New Weekly Content
1. Create `weekXX/` directory with `styles/` and `images/` subdirectories
2. Follow naming convention: descriptive filenames (e.g., `flexbox-layout.html`)
3. Include solution files with `-solution` suffix when applicable
4. Link CSS: `<link rel="stylesheet" href="styles/filename.css">`

### Image Handling
- **Profile/personal images**: Root `images/` directory
- **Weekly exercise images**: `weekXX/images/` for isolation
- **WWR project images**: `wwr/images/` with descriptive names
- Always include meaningful `alt` attributes for accessibility

### CSS Development
- Start with CSS reset in each stylesheet
- Use semantic class names (`.hero`, `.adventures`, `.socialmedia`)
- Follow mobile-first approach for responsive design
- Leverage CSS custom properties for maintainable theming

## Common Patterns

- **Template structure**: `<!DOCTYPE html>` → `<html lang="en">` → proper `<head>` meta tags
- **Link targets**: External links use `target="_blank" rel="noopener"`
- **Image optimization**: Specify `width` and `height` attributes when possible
- **Form elements**: Use proper `label`/`input` associations with `for`/`id` attributes