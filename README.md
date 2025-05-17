# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.
- <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Navigation Bar -->
    <header class="navbar">
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="content">
        <section class="hero">
            <h1>Welcome to Our Website</h1>
            <p>This is a responsive webpage using Flexbox and CSS Grid.</p>
        </section>

        <section class="grid-container">
            <div class="grid-item">Item 1</div>
            <div class="grid-item">Item 2</div>
            <div class="grid-item">Item 3</div>
            <div class="grid-item">Item 4</div>
        </section>

        <section class="flex-container">
            <div class="flex-item">Flex Item 1</div>
            <div class="flex-item">Flex Item 2</div>
            <div class="flex-item">Flex Item 3</div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Your Website</p>
    </footer>

</body>
</html>
/* General Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

/* Navigation Bar */
.navbar {
    background-color: #333;
}

.navbar nav ul {
    display: flex;
    justify-content: center;
    padding: 1rem;
    list-style: none;
}

.navbar nav ul li {
    margin: 0 15px;
}

.navbar nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

.navbar nav ul li a:hover {
    text-decoration: underline;
}

/* Main Content */
.content {
    padding: 2rem;
}

.hero {
    text-align: center;
    margin-bottom: 2rem;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.2rem;
}

/* Grid Layout */
.grid-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
    margin-bottom: 2rem;
}

.grid-item {
    background-color: #f4f4f4;
    padding: 1rem;
    text-align: center;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Flexbox Layout */
.flex-container {
    display: flex;
    justify-content: space-between;
    margin-bottom: 2rem;
}

.flex-item {
    background-color: #f4f4f4;
    padding: 1rem;
    text-align: center;
    flex: 1;
    margin: 0 10px;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Footer */
footer {
    text-align: center;
    padding: 1rem;
    background-color: #333;
    color: white;
}

/* Media Queries */

/* Tablet: 768px and up */
@media (max-width: 768px) {
    .grid-container {
        grid-template-columns: repeat(2, 1fr);
    }

    .flex-container {
        flex-direction: column;
        align-items: center;
    }

    .flex-item {
        margin: 10px 0;
    }
}

/* Mobile: 480px and up */
@media (max-width: 480px) {
    .grid-container {
        grid-template-columns: 1fr;
    }

    .navbar nav ul {
        flex-direction: column;
    }

    .navbar nav ul li {
        margin: 10px 0;
    }

    .hero h1 {
        font-size: 2rem;
    }

    .hero p {
        font-size: 1rem;
    }
}


Happy Coding! 💻✨
