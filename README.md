/* style.css */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Roboto', sans-serif;
  background-color: #f0f0f0;
  color: #333;
}

/* Navbar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  background-color: #333;
  color: white;
}

.navbar .logo {
  font-size: 1.5rem;
  font-weight: 500;
}

.navbar nav ul {
  list-style-type: none;
  display: flex;
}

.navbar nav ul li {
  margin: 0 15px;
}

.navbar nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: 500;
}

.navbar nav ul li a:hover {
  color: #f39c12;
}

/* Hero Section */
.hero {
  background: url('https://via.placeholder.com/1600x800') no-repeat center center/cover;
  color: white;
  padding: 80px 0;
  text-align: center;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 20px;
}

.hero p {
  font-size: 1.2rem;
}

.cta-button {
  background-color: #f39c12;
  padding: 15px 30px;
  text-decoration: none;
  font-size: 1.1rem;
  color: white;
  border-radius: 5px;
  font-weight: 500;
}

.cta-button:hover {
  background-color: #e67e22;
}

/* About Section */
.about {
  padding: 60px 30px;
  text-align: center;
}

.about h2 {
  font-size: 2.5rem;
  margin-bottom: 15px;
}

.about p {
  font-size: 1.1rem;
  color: #555;
}

/* Programs Section */
.programs {
  background-color: #fff;
  padding: 60px 30px;
  text-align: center;
}

.programs h2 {
  font-size: 2.5rem;
  margin-bottom: 30px;
}

.programs-list {
  display: flex;
  justify-content: center;
  gap: 30px;
}

.program {
  background-color: #f9f9f9;
  padding: 30px;
  width: 250px;
  border-radius: 5px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.program h3 {
  font-size: 1.6rem;
  margin-bottom: 10px;
}

.program p {
  font-size: 1.1rem;
  color: #777;
}

/* Footer */
footer {
  background-color: #333;
  color: white;
  padding: 20px;
  text-align: center;
}

footer .footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

footer .social-media a {
  color: white;
  text-decoration: none;
  margin: 0 10px;
}

footer .social-media a:hover {
  color: #f39c12;
}
// script.js

// Smooth Scroll for "Learn More" button
const ctaButton = document.querySelector('.cta-button');
ctaButton.addEventListener('click', (e) => {
  e.preventDefault();
  document.querySelector('#about').scrollIntoView({
    behavior: 'smooth'
  });
});
