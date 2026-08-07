# Lecture 1: Restaurant Header & Navigation

A clean, responsive header and navigation section for the **Bella Vista** restaurant website, built using vanilla HTML5 and CSS.

---

## 📄 HTML Line-by-Line Breakdown

```html
<!DOCTYPE html>

```

> **Analogy:** *Think of this as introducing yourself to the browser.*
> It tells the browser, "Hey! I am writing modern HTML5 code, so parse this page using the latest web standards."

```html
<html lang="en">

```

> **Analogy:** *The main folder or house where everything lives.*
> Sets the root element of the document and specifies that the primary language of the content is English.

```html
<head>

```

> **Analogy:** *The behind-the-scenes control room.*
> Contains metadata, settings, and external links for the webpage that the browser needs, but visitors won't directly see on the screen.

```html
<meta charset="UTF-8">

```

> **Analogy:** *The universal translator.*
> Ensures the webpage can display all standard text characters, numbers, symbols, and emojis without turning them into broken gibberish.

```html
<meta name="viewport" content="width=device-width , initial-scale=1.0">

```

> **Analogy:** *Auto-adjusting camera lenses.*
> Tells mobile devices to match the webpage width to the screen's actual size at 100% zoom, preventing pages from looking tiny like desktop sites on smartphones.

```html
<meta name="description" content="Bella Vista - Authentic Italian Restaurant serving fresh pasta, wood-fried pizzas, and traditional Italian cuisine in the heart of the city.">

```

> **Analogy:** *Your website's business card for search engines.*
> Provides a short summary of your site that Google displays beneath your page title in search results.

```html
<title>Bella Vista Restuarant - Authentic Italian Cuisine</title>

```

> **Analogy:** *The signpost on your browser tab.*
> Sets the main title visible on the browser tab and when someone bookmarks your page.

```html
<link rel="stylesheet" href="style.css">

```

> **Analogy:** *Hanging clothes in the wardrobe.*
> Connects this HTML file (the raw skeleton) to your `style.css` file (the styling and design instructions).

```html
<body>

```

> **Analogy:** *The stage performance.*
> Everything wrapped inside `<body>` is visible content rendered directly to the user.

```html
<header class="header">

```

> **Analogy:** *The roof/top banner of the store.*
> A semantic HTML tag used to define the topmost section of a page or component, typically holding branding and main navigation.

```html
<div class="container">

```

> **Analogy:** *Invisible safety guardrails.*
> A helper container used to keep content centered and bounded within a clean max-width so text doesn't stretch awkwardly across large monitors.

```html
<nav class="navbar">

```

> **Analogy:** *The directional signpost.*
> A semantic container indicating that the links inside are for major page navigation.

```html
<div class="logo">
    <h1>Bella Vista</h1>
    <span class="tagline">Authentic Italian Cuisine</span>
</div>

```

> **Analogy:** *The store storefront badge.*
> * `<h1>`: The primary heading of the page—used here for the main restaurant name.
> * `<span>`: A inline wrapper used to attach sub-text (the tagline) right underneath the name.
> 
> 

```html
<ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#menu">Menu</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
</ul>

```

> **Analogy:** *The organized index menu.*
> An unordered list (`<ul>`) holding list items (`<li>`), each containing a hyperlink (`<a>`) pointing to different sections on the page using section IDs (`#home`, `#menu`, etc.).

---

## 🎨 CSS Line-by-Line Breakdown

### Global Resets & Typography

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

```

> **Analogy:** *Wiping the canvas clean before painting.*
> * `*`: Targets **every** element on the page.
> * `margin: 0; padding: 0;`: Strips away default gaps browsers automatically add around elements.
> * `box-sizing: border-box;`: Includes padding and borders in the element's total calculated width and height so sizing math stays predictable.
> 
> 

```css
body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.6;
    color: #333;
}

```

> **Analogy:** *Setting the default voice and tone of the book.*
> * `font-family`: Sets clean fallback fonts if primary ones fail.
> * `line-height: 1.6`: Adds breathing room between lines of text for better readability.
> * `color: #333`: Sets body text to a soft dark charcoal instead of harsh pure black.
> 
> 

---

### Layout Containers

```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

```

> **Analogy:** *A picture frame that stays centered on any wall.*
> * `max-width: 1200px`: Prevents content from expanding wider than 1200 pixels.
> * `margin: 0 auto`: Automatically splits remaining space on the left and right, keeping content perfectly centered.
> * `padding: 0 20px`: Adds small side cushions on mobile screens so content doesn't touch the screen edges.
> 
> 

---

### Header & Navigation Styling

```css
.header {
    background-color: #2c3e50;
    color: white;
    padding: 1rem 0;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
}

```

> **Analogy:** *Gluing the top bar to the top of the viewing screen.*
> * `background-color`: Sets a dark navy blue background shade.
> * `position: fixed; top: 0; left: 0; width: 100%;`: Locks the header stickied to the top edge of the browser, spanning full width even when scrolling.
> * `z-index: 1000`: Forces the header to stay stacked on top of all other elements on the page.
> 
> 

```css
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

```

> **Analogy:** *Pushing two items to opposite ends of a shelf.*
> * `display: flex`: Activates Flexbox layout mode.
> * `justify-content: space-between`: Pushes the logo to the far left and navigation links to the far right.
> * `align-items: center`: Aligns the logo and navigation links vertically along the middle.
> 
> 

```css
.logo h1 {
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 0.2rem;
}

.logo tagline {
    font-size: 0.9rem;
    opacity: 0.8;
}

```

> **Analogy:** *Adjusting main title text vs subtitle caption.*
> Styles the main title with large, bold font, and subtle space underneath. Reduces size and opacity (makes slightly translucent) for the tagline.

```css
.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem;
}

```

> **Analogy:** *Arranging a bullet list into a horizontal row.*
> * `display: flex`: Places list items side-by-side in a horizontal row instead of stacked vertically.
> * `list-style: none`: Removes default list bullet points.
> * `gap: 2rem`: Places consistent spacing between each navigation item.
> 
> 

```css
.nav-links a {
    color: white;
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    transition: background-color 0.3s ease-in;
}

```

> **Analogy:** *Making text look like clickable rounded buttons.*
> * `text-decoration: none`: Removes the default blue underline from links.
> * `border-radius: 4px`: Rounds the corners of the clickable target area.
> * `transition`: Creates a smooth 0.3-second fade animation when background color changes on hover.
> 
> 

```css
.nav-links a:hover {
    background-color: rgba(255,255,255,0.1);
}

```

> **Analogy:** *Turning on a light switch when hovering over a button.*
> Applies a subtle transparent white highlight behind any link when the mouse cursor rests over it.

# Lecture 2: Hero Section & Call-to-Action (CTA)

Building the main spotlight section of the **Bella Vista** restaurant website. This section introduces full-screen hero layouts, background dimming overlay techniques, centered flexbox alignment, and interactive button styles.

---

## 📄 HTML Line-by-Line Breakdown

```html
<section class="hero" id="home">

```

> **Analogy:** *The main storefront billboard.*
> Using the semantic `<section>` tag with an `id="home"` allows top navigation links (like `<a href="#home">`) to jump straight to this top area when clicked.

```html
<div class="hero-content">

```

> **Analogy:** *The spotlight box in the middle of the stage.*
> A wrapper element used to group the title, paragraph, and buttons together so we can center all of them at once.

```html
<h1>Taste the Authenticity of Italy</h1>

```

> **Analogy:** *The big neon sign over the entrance.*
> The main headline of the hero section designed to immediately catch the visitor's attention.

```html
<p>Handcrafted pasta, wood-fired pizzas, and timeless family recipes made fresh daily.</p>

```

> **Analogy:** *The short elevator pitch.*
> A supporting description giving visitors an instant summary of what makes the restaurant special.

```html
<div class="hero-buttons">

```

> **Analogy:** *The action tray holding two main doors.*
> A container grouping our primary call-to-action buttons together in a neat horizontal row.

```html
<a href="#menu" class="btn btn-primary">View Our Menu</a>
<a href="#contact" class="btn btn-secondary">Book a Table</a>

```

> **Analogy:** *The red carpet entrance vs. the side reservation desk.*
> * `btn`: Shared base styling (padding, rounded corners, hover transitions).
> * `btn-primary`: High-contrast, filled button for the main action (View Menu).
> * `btn-secondary`: Transparent/outlined button for a secondary action (Book a Table).
> 
> 

---

## 🎨 CSS Line-by-Line Breakdown

### Hero Container & Layout

```css
.hero {
    min-height: 100vh;
    background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('hero-bg.jpg') no-repeat center center/cover;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: white;
    padding: 0 20px;
}

```

> **Analogy:** *Setting up a massive movie screen with sunglasses over the picture.*
> * `min-height: 100vh`: Forces the hero section to fill **100% of the viewport height** (the full visible screen).
> * `linear-gradient(rgba(0,0,0,0.6)...)`: Applies a **dark semi-transparent overlay** over the background image so white text stays readable.
> * `url(...) no-repeat center center/cover`: Centers the background image and scales it to cover the whole screen without stretching or repeating.
> * `display: flex; justify-content: center; align-items: center;`: **Bullseye centering**—places the content perfectly in the center horizontally and vertically.
> 
> 

---

### Hero Typography & Text Styling

```css
.hero-content {
    max-width: 800px;
}

```

> **Analogy:** *Setting text margins in a book.*
> Limits paragraph width so long sentences don't stretch awkwardly across wide monitor screens.

```css
.hero h1 {
    font-size: 3.5rem;
    margin-bottom: 1rem;
    font-weight: 700;
}

```

> **Analogy:** *Turning up the volume knob on your title.*
> Makes the headline extra large (`3.5rem`), bold, and pushes content below it down using a 1rem bottom margin.

```css
.hero p {
    font-size: 1.25rem;
    margin-bottom: 2rem;
    opacity: 0.9;
}

```

> **Analogy:** *Subtle lighting for reading comfort.*
> Enlarges paragraph text slightly and uses `opacity: 0.9` to soften pure white text for easier reading over background images.

---

### Call-to-Action (CTA) Buttons

```css
.hero-buttons {
    display: flex;
    gap: 1rem;
    justify-content: center;
}

```

> **Analogy:** *Placing two chairs side-by-side with a gap between them.*
> Uses Flexbox to line up buttons horizontally with a consistent `1rem` gap between them.

```css
.btn {
    display: inline-block;
    padding: 0.8rem 1.8rem;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
    transition: all 0.3s ease;
}

```

> **Analogy:** *Manufacturing blank physical buttons before painting them.*
> Gives both buttons equal padding, removes link underlines, rounds corners, and adds a `0.3s` smooth animation transition for hover effects.

```css
.btn-primary {
    background-color: #e74c3c;
    color: white;
}

.btn-primary:hover {
    background-color: #c0392b;
    transform: translateY(-2px);
}

```

> **Analogy:** *A vibrant red button that lifts slightly when your hand hovers over it.*
> Uses warm crimson red for the main action button and darkens the red while shifting it up `2px` (`translateY`) when hovered.

```css
.btn-secondary {
    background-color: transparent;
    color: white;
    border: 2px solid white;
}

.btn-secondary:hover {
    background-color: white;
    color: #2c3e50;
}

```

> **Analogy:** *A clear glass button that fills with solid white light when touched.*
> Creates a sleek ghost button (transparent inside, white border) that flips to a solid white background on mouse hover.

# Lecture 3: Menu Section & Component Cards

Building the interactive **Our Menu** section of the Bella Vista website using semantic HTML5, CSS Grid layout, and elevation card components with hover micro-interactions.

---

## 📄 HTML Line-by-Line Breakdown

```html
<main>

```

> **Analogy:** *The main stage where the primary performance takes place.*
> A semantic wrapper tag that informs search engines and screen readers where the core content of the page lives (excluding header and footer).

```html
<section id="menu" class="menu">

```

> **Analogy:** *Dedicated dining section in a restaurant layout.*
> Defines a distinct logical area for the food menu, using `id="menu"` so header links (`href="#menu"`) scroll smoothly directly to this spot.

```html
<div class="container">

```

> **Analogy:** *Invisible safety guardrails.*
> Reuses our container class to keep the menu centered and bounded within 1200px across large monitors.

```html
<h2 class="section-title">Our Menu</h2>
<p class="section-subtitle">Discover our carefully crafted dishes.</p>

```

> **Analogy:** *The overhead signpost and tagline at a department entrance.*
> Creates a clean visual hierarchy using a prominent section title (`<h2>`) paired with a muted tagline (`<p>`) directly below it.

```html
<div class="menu-categories">
    <div class="menu-category">
        <h3>Appetizers</h3>

```

> **Analogy:** *Chapter titles in a food catalog.*
> Groups food items into logical categories (like Appetizers, Main Courses, Desserts) so customers can quickly scan the menu.

```html
<div class="menu-items">

```

> **Analogy:** *A structured tray grid holding individual dish cards.*
> Serves as the CSS Grid parent container that organizes all individual food item cards into a neat, uniform layout.

```html
<div class="menu-item">
    <div class="menu-item-info">
        <h4>Bruschetta Italiana</h4>
        <p>Fresh tomatoes, basil, and mozzarella on toasted bread.</p>
    </div>
    <span class="price">$12</span>
</div>

```

> **Analogy:** *A physical recipe card on display.*
> Encapsulates a single menu item component, separating the dish info (`<h4>` title and `<p>` description) from the price tag (`<span>`).

---

## 🎨 CSS Line-by-Line Breakdown

### Section Background & Header Styling

```css
.menu {
    padding: 5rem 0;
    background-color: #f8f9fa;
}

```

> **Analogy:** *Painting a wall a soft off-white to contrast with white cards.*
> Gives the entire section generous top and bottom spacing (`5rem`), and applies a subtle light gray background (`#f8f9fa`) to make white menu cards pop visually.

```css
.section-title {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: #2c3e50;
}

.section-subtitle {
    text-align: center;
    font-size: 1.1rem;
    color: #666;
    margin-bottom: 3rem;
}

```

> **Analogy:** *Formatting book headings for maximum readability.*
> Centers the titles, uses high-contrast dark navy `#2c3e50` for the main title, and muted gray `#666` for the subtitle with extra bottom space (`3rem`) before content starts.

---

### Category Titles & Accent Lines

```css
.menu-category {
    margin-bottom: 3rem;
}

.menu-category h3 {
    font-size: 2rem;
    margin-bottom: 1.5rem;
    color: #2c3e50;
    border-bottom: 2px solid #e74c3c;
    padding-bottom: 0.5rem;
}

```

> **Analogy:** *Underlining important notes with a vibrant red highlighter.*
> Adds a solid red underline (`border-bottom: 2px solid #e74c3c`) under category headers to create an elegant visual divider across the section.

---

### Grid Layout & Menu Card Components

```css
.menu-items {
    display: grid;
    gap: 1.5rem;
}

```

> **Analogy:** *An automated grid tray holding cards in place.*
> Turns on **CSS Grid** layout mode to stack menu items automatically with a consistent `1.5rem` gap between each card.

```css
.menu-item {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding: 1.5rem;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
}

```

> **Analogy:** *Crafting a clean paper card resting softly on a table.*
> * `display: flex; justify-content: space-between`: Pushes dish info to the left and price to the far right.
> * `align-items: flex-start`: Aligns price to top edge alongside the title.
> * `background-color: white; border-radius: 8px`: Soft white card background with rounded corners.
> * `box-shadow: 0 2px 10px rgba(0,0,0,0.1)`: Gives the card subtle depth so it appears floating above the page.
> 
> 

```css
.menu-item:hover {
    transform: translateY(-3px);
}

```

> **Analogy:** *Lifting a card up with your fingertips when hovering over it.*
> Moves the menu card up by 3 pixels on mouse hover, creating an interactive, tangible feel.

```css
.menu-item-info h4 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
    color: #2c3e50;
}

.menu-item-info p {
    color: #666;
    line-height: 1.4;
}

```

> **Analogy:** *Setting bold title text vs soft ingredient descriptions on a label.*
> Styles dish titles in bold dark blue and descriptions in readable gray with comfortable line height (`1.4`).

```css
.price {
    font-size: 1.1rem;
    font-weight: bold;
    color: #e74c3c;
    margin-left: 1rem;
}

```

> **Analogy:** *A bright red price tag sticker.*
> Highlights the price in bold red text (`#e74c3c`) so customers can instantly spot cost details.
