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

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout with Flexbox and Grid</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Navigation Bar -->
  <header>
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
  <main>
    <section class="left-column">
      <h2>Welcome to Our Website!</h2>
      <p>This is some introductory text to explain the website's content and purpose.</p>
    </section>

    <section class="right-column">
      <div class="grid-container">
        <div class="grid-item">Item 1</div>
        <div class="grid-item">Item 2</div>
        <div class="grid-item">Item 3</div>
        <div class="grid-item">Item 4</div>
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Your Website. All rights reserved.</p>
  </footer>
</body>
</html>

/* Reset basic styling */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Basic Styling */
body {
  font-family: Arial, sans-serif;
}

/* Navigation Bar */
header {
  background-color: #333;
  color: white;
  padding: 10px 0;
}

nav ul {
  display: flex;
  justify-content: center;
  list-style: none;
}

nav ul li {
  margin: 0 20px;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

/* Main Layout - Flexbox */
main {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 20px;
}

.left-column {
  flex: 1;
  padding: 20px;
  background-color: #f4f4f4;
  margin-right: 20px;
}

.right-column {
  flex: 2;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.grid-item {
  background-color: #ddd;
  padding: 20px;
  text-align: center;
  border-radius: 5px;
}

/* Footer */
footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
}

/* Media Queries for Responsive Design */

/* Tablet and larger screens */
@media screen and (max-width: 768px) {
  main {
    flex-direction: column;
  }

  .grid-container {
    grid-template-columns: 1fr; /* Stack grid items on smaller screens */
  }

  nav ul {
    flex-direction: column;
    padding: 0;
  }

  nav ul li {
    margin: 10px 0;
  }
}

/* Mobile screens */
@media screen and (max-width: 480px) {
  nav ul {
    flex-direction: column;
    align-items: center;
  }

  nav ul li {
    margin: 5px 0;
  }

  .left-column {
    padding: 15px;
  }

  .grid-container {
    grid-template-columns: 1fr; /* Stack grid items vertically */
  }
}
