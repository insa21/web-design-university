# Online Courses Web Application

## Overview

This project is a web application designed for online courses, utilizing semantic HTML and modern CSS for a clean and accessible user interface. The application includes various sections such as Home, About, Blog, Course, and Contact, each accessible through a navigation menu.

## Features

- **Responsive Navigation Menu**: The application features a responsive navigation menu with a close button for better user experience on mobile devices.
- **Semantic HTML**: Uses semantic HTML5 elements for better accessibility and SEO.
- **Modern CSS**: Incorporates modern CSS techniques for a clean and responsive design.

## File Structure

```
/online-courses
│
├── index.html        # Home page
├── about.html        # About page
├── blog.html         # Blog page
├── course.html       # Course page
├── contact.html      # Contact page
├── css
│   ├── style.css     # Main stylesheet
│
├── js
│   ├── script.js     # JavaScript for interactive elements
│
└── images            # Folder for images
```

## HTML Structure

Below is the basic structure of the navigation menu with semantic HTML:

```html
<nav>
  <ul id="menu">
    <i id="menu-close" class="fas fa-times"></i
    ><!-- Tombol Close -->
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="blog.html">Blog</a></li>
    <li><a href="course.html">Course</a></li>
    <li><a class="active" href="contact.html">Contact</a></li>
  </ul>
</nav>
```

## CSS (style.css)

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

nav {
  background-color: #333;
  overflow: hidden;
}

nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  align-items: center;
}

nav ul li {
  flex: 1;
}

nav ul li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 20px;
  text-decoration: none;
}

nav ul li a:hover,
nav ul li a.active {
  background-color: #111;
}

#menu-close {
  display: none; /* This will be handled with JavaScript */
  cursor: pointer;
  padding: 14px 20px;
}

@media (max-width: 600px) {
  nav ul {
    flex-direction: column;
    display: none;
  }

  nav ul.show {
    display: flex;
  }

  #menu-close {
    display: block;
  }
}
```

## JavaScript (script.js)

```javascript
document.getElementById("menu-close").addEventListener("click", function () {
  document.getElementById("menu").classList.toggle("show");
});
```

## How to Run

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/online-courses.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd online-courses
   ```

3. **Open `index.html` in your browser:**

   ```bash
   open index.html
   ```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to contribute to this project by opening issues or submitting pull requests. Happy coding!
