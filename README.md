# homeco-site
A webpage for Home&amp;Co shopping site which sells cleaning and home products
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Home&amp;Co. Shopping</title>
  <link rel="stylesheet" href="CSSstyles.css">
  <style>
    /* Reset and Base Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Arial', sans-serif;
    }

    body {
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      background-color: #f4f4f4;
    }

    /* Header Styles */
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background-color: #2c3e50;
      padding: 15px 30px;
    }

    .logo {
      font-size: 2em;
      color: #e74c3c; /* Colorful logo */
      font-weight: bold;
      letter-spacing: 1px;
    }

    nav ul {
      list-style: none;
      display: flex;
    }

    nav ul li {
      margin-left: 20px;
    }

    nav ul li a {
      color: #ecf0f1;
      text-decoration: none;
      padding: 10px 15px;
      transition: background-color 0.3s ease;
    }

    nav ul li a:hover {
      background-color: #34495e;
      border-radius: 5px;
    }

    /* Sidebar (Categories) Styles */
    .sidebar {
      background-color: #34495e;
      color: #ecf0f1;
      width: 200px;
      padding: 20px;
      position: fixed;
      top: 70px; /* below header */
      bottom: 0;
      left: 0;
      overflow-y: auto;
    }

    .sidebar h2 {
      margin-bottom: 15px;
      font-size: 1.2em;
      border-bottom: 1px solid #ecf0f1;
      padding-bottom: 5px;
    }

    .sidebar ul {
      list-style: none;
    }

    .sidebar ul li {
      margin: 10px 0;
    }

    .sidebar ul li a {
      color: #ecf0f1;
      text-decoration: none;
      padding: 8px 10px;
      display: block;
      transition: background-color 0.3s ease;
    }

    .sidebar ul li a:hover {
      background-color: #2c3e50;
      border-radius: 5px;
    }

    /* Main Content Styles */
    .content-wrapper {
      display: flex;
      margin-left: 220px; /* room for sidebar */
      padding: 20px;
      flex: 1;
    }

    main {
      flex: 1;
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    /* Product Card Styles */
    .product-card {
      background-color: #ffffff;
      border: 1px solid #ddd;
      border-radius: 10px;
      overflow: hidden;
      text-align: center;
      transition: transform 0.3s ease;
      text-decoration: none;
    }

    .product-card:hover {
      transform: translateY(-5px);
    }

    .product-image {
      position: relative;
      width: 100%;
      padding-top: 75%; /* 4:3 Aspect Ratio */
      overflow: hidden;
    }

    .product-image img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: opacity 0.3s ease;
    }

    .product-image img:last-child {
      opacity: 0;
    }

    .product-card:hover .product-image img:first-child {
      opacity: 0;
    }

    .product-card:hover .product-image img:last-child {
      opacity: 1;
    }

    .product-info {
      padding: 15px;
    }

    .product-info h3 {
      margin-bottom: 10px;
      font-size: 1.2em;
      color: #2c3e50;
    }

    .price {
      color: #e74c3c;
      font-size: 1.5em;
      font-weight: bold;
    }

    /* Add to Cart Button Styles */
    .add-to-cart {
      background-color: #e74c3c;
      color: #fff;
      border: none;
      border-radius: 5px;
      padding: 10px 15px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.3s ease;
      font-size: 1em;
      margin: 10px 0;
    }

    .add-to-cart:hover {
      background-color: #c0392b;
      transform: scale(1.05);
    }

    /* Footer Styles */
    footer {
      background-color: #2c3e50;
      color: #ecf0f1;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">Home&amp;Co.</div>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Promotion</a></li>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Sidebar for Categories -->
  <div class="sidebar">
    <h2>Categories</h2>
    <ul>
      <li><a href="#">Cleaning</a></li>
      <li><a href="#">Tools</a></li>
      <li><a href="#">Kitchen</a></li>
    </ul>
  </div>

  <div class="content-wrapper">
    <main>
      <section class="product-grid">
        <!-- Product Card 1 -->
        <div class="product-card">
          <div class="product-image">
            <img src="product1.jpg" alt="Product 1">
            <img src="product1.jpg" alt="Product 1 Hover">
          </div>
          <div class="product-info">
            <h3>Pine Gel</h3>
            <p class="price">R29.99</p>
            <button class="add-to-cart">Add to Cart</button>
          </div>
        </div>
        <!-- Product Card 2 -->
        <div class="product-card">
          <div class="product-image">
            <img src="dustpan.jpg" alt="Product 2">
            <img src="dustpan.jpg" alt="Product 2 Hover">
          </div>
          <div class="product-info">
            <h3>Dust Pan</h3>
            <p class="price">R45.50</p>
            <button class="add-to-cart">Add to Cart</button>
          </div>
        </div>
        <!-- Product Card 3 -->
        <div class="product-card">
          <div class="product-image">
            <img src="mopset.jpg" alt="Product 3">
            <img src="mopset.jpg" alt="Product 3 Hover">
          </div>
          <div class="product-info">
            <h3>Mop</h3>
            <p class="price">R499.00</p>
            <button class="add-to-cart">Add to Cart</button>
          </div>
        </div>
      </section>
    </main>![mopset](https://github.com/user-attachments/assets/5834799f-5633-41d6-ab09-e87ac7c34d0f)
![mopset](https://github.com/user-attachments/assets/101f60e4-9c13-488b-9f91-fb1656557838)
![Product1](https://github.com/user-attachments/assets/0bf44793-d576-4545-9dfc-c536bea39b4c)

  </div>

  <footer>
    <p>&copy; 2025 Home&amp;Co. All rights reserved.</p>
  </footer>
</body>
</html>
