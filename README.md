# NetFlix-Clone
## Date:09-07-2025
## Sachin B
## 212222060207

## Objective:
To create a modern, responsive navigation bar using CSS Flexbox, mimicking real-world websites like Netflix. This helps reinforce alignment, spacing, and layout structuring using Flexbox properties.

## Tasks:

#### 1. Structure the HTML Layout:
Use a ```<nav>``` tag as the main container.

Add a brand logo/title on the left using a ```<div> or <h1>```.

Add navigation links like Home, Menu, About, Contact, and Login using a ```<ul> with <li> and <a>```.

#### 2. Apply Flexbox for Layout:
Use display: flex on the ```<nav>``` container.

Use justify-content: space-between to align the logo and menu.

Use align-items: center to vertically center both sections.

Style list items with horizontal spacing using gap or margin.

#### 3. Style Like a Real-World Navbar:
Add background color (e.g., dark or gradient like Netflix/Zomato).

Style text with bold fonts, hover effects, and link styling.

Remove default ul and li styles (list-style: none, text-decoration: none).

#### 4. Bonus Enhancements:
Add a hover underline or button effect on links.

Make it responsive using flex-wrap or media queries.

Fix the nav bar to top with position: sticky.
## HTML Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Netflix Landing Page Clone</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <nav class="navbar">
    <div class="logo">NETFLIX</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">TV Shows</a></li>
      <li><a href="#">Movies</a></li>
      <li><a href="#">New & Popular</a></li>
      <li><a href="#">My List</a></li>
    </ul>
    <button class="btn-signin">Sign In</button>
  </nav>

  <header class="banner">
    <div class="banner-content">
      <h1>Unlimited movies, TV shows, and more.</h1>
      <p>Watch anywhere. Cancel anytime.</p>
      <button class="btn-getstarted">Get Started</button>
    </div>
  </header>

  <section class="content-row">
    <h2>Trending Now</h2>
    <div class="cards">
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Show+1" alt="Show 1" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Show+2" alt="Show 2" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Show+3" alt="Show 3" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Show+4" alt="Show 4" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Show+5" alt="Show 5" /></div>
    </div>
  </section>

  <section class="content-row">
    <h2>Top Picks for You</h2>
    <div class="cards">
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Movie+1" alt="Movie 1" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Movie+2" alt="Movie 2" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Movie+3" alt="Movie 3" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Movie+4" alt="Movie 4" /></div>
      <div class="card"><img src="https://via.placeholder.com/150x220?text=Movie+5" alt="Movie 5" /></div>
    </div>
  </section>

  <footer class="footer">
    <p>© 2025 Netflix, Inc.</p>
  </footer>
</body>
</html>
```
## CSS Code:
```
{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: #141414;
  color: white;
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #141414;
  padding: 16px 40px;
  position: sticky;
  top: 0;
  z-index: 1000;
}

.logo {
  font-size: 1.8rem;
  font-weight: 900;
  color: #e50914;
  letter-spacing: 2px;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 24px;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #e50914;
}

.btn-signin {
  background-color: #e50914;
  border: none;
  color: white;
  padding: 8px 18px;
  font-weight: 700;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-signin:hover {
  background-color: #b0060f;
}

.banner {
  background-size: cover;
  background-position: center;
  height: 60vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 0 20px;
}

.banner-content h1 {
  font-size: 3rem;
  margin-bottom: 16px;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
}

.banner-content p {
  font-size: 1.4rem;
  margin-bottom: 24px;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.7);
}

.btn-getstarted {
  background-color: #e50914;
  border: none;
  color: white;
  padding: 12px 28px;
  font-size: 1.2rem;
  font-weight: 700;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-getstarted:hover {
  background-color: #b0060f;
}

.content-row {
  padding: 24px 40px;
}

.content-row h2 {
  font-size: 1.6rem;
  margin-bottom: 16px;
}

.cards {
  display: flex;
  gap: 12px;
  overflow-x: auto;
  padding-bottom: 8px;
}

.cards::-webkit-scrollbar {
  height: 8px;
}

.cards::-webkit-scrollbar-thumb {
  background-color: #e50914;
  border-radius: 4px;
}

.card {
  flex: 0 0 auto;
  width: 150px;
  border-radius: 6px;
  overflow: hidden;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.card img {
  width: 100%;
  display: block;
  border-radius: 6px;
}

.card:hover {
  transform: scale(1.1);
  z-index: 10;
}

.footer {
  text-align: center;
  padding: 20px;
  font-size: 0.9rem;
  color: #666;
  background-color: #141414;
}

@media (max-width: 700px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
    padding: 12px 20px;
  }
  .nav-links {
    gap: 14px;
    margin-top: 8px;
  }
  .content-row {
    padding: 20px 10px;
  }
  .banner-content h1 {
    font-size: 2rem;
  }
  .banner-content p {
    font-size: 1rem;
  }
}

```
## Output:
![Screenshot 2025-07-09 231516](https://github.com/user-attachments/assets/1682db6f-63ad-410e-b99c-b36b717d5ce7)


## Result:
A modern, responsive navigation bar using CSS Flexbox, mimicking real-world websites like Netflix. This helps reinforce alignment, spacing, and layout structuring using Flexbox properties is created successfully.
