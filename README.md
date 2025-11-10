# e-commerce<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>E-Commerce Portal</title>

<style>
  :root {
    --primary: #ff0000;
    --secondary: #000;
    --text-light: #fff;
    --border: #ff3333;
  }

  body {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    background-color: var(--secondary);
    color: var(--text-light);
  }

  nav {
    background-color: var(--primary);
    padding: 15px 20px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
    position: sticky;
    top: 0;
    z-index: 100;
  }

  nav a {
    color: var(--text-light);
    text-decoration: none;
    font-weight: bold;
    margin: 0 15px;
    padding: 8px 12px;
    border-radius: 5px;
    transition: 0.3s;
  }

  nav a:hover {
    background-color: var(--secondary);
    color: var(--primary);
    transform: scale(1.05);
  }

  section {
    padding: 40px 20px;
    max-width: 1200px;
    margin: auto;
  }

  h1, h2 {
    color: var(--primary);
    text-align: center;
  }

  p {
    text-align: center;
    color: #ddd;
  }

  /* Products */
  .product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }

  .product {
    background-color: #111;
    border: 2px solid var(--border);
    border-radius: 10px;
    padding: 15px;
    text-align: center;
    box-shadow: 0 0 10px rgba(255, 0, 0, 0.2);
    transition: 0.3s;
  }

  .product:hover {
    transform: scale(1.05);
    box-shadow: 0 0 15px rgba(255, 0, 0, 0.5);
  }

  .product img {
    width: 200px;
    height: 200px;
    object-fit: cover;
    border-radius: 10px;
  }

  .product h3 {
    margin: 10px 0 5px;
  }

  .product p {
    color: #ccc;
  }

  .btn {
    background-color: var(--primary);
    color: #fff;
    padding: 10px 15px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 10px;
  }

  .btn:hover {
    background-color: #cc0000;
  }

  /* Forms */
  form {
    max-width: 400px;
    background: rgba(255, 0, 0, 0.1);
    border: 2px solid var(--border);
    padding: 25px;
    border-radius: 12px;
    margin: 20px auto;
  }

  input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border-radius: 6px;
    border: 1px solid var(--border);
    background-color: #111;
    color: #fff;
  }

  .error {
    color: #ff6666;
    font-size: 14px;
    display: none;
  }

  button {
    width: 100%;
    background: var(--primary);
    color: white;
    padding: 12px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
  }

  button:hover {
    background-color: #cc0000;
  }

  /* Dashboard Lists */
  .list-item {
    background-color: #111;
    border: 1px solid var(--border);
    padding: 15px;
    border-radius: 8px;
    margin: 10px 0;
  }

  .action-btn {
    background-color: var(--primary);
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 6px;
    cursor: pointer;
    margin: 10px;
  }

  .action-btn:hover {
    background-color: #cc0000;
  }
</style>
</head>

<body>
  <!-- Navbar -->
  <nav>
    <a href="#home">Home</a>
    <a href="#products">Products</a>
    <a href="#register">Register</a>
    <a href="#login">Login</a>
    <a href="#dashboard">Dashboard</a>
    <a href="#about">About Us</a>
    <a href="#contact">Contact Us</a>
  </nav>

  <!-- Home -->
  <section id="home">
    <h1>Welcome to RedCart</h1>
    <p>Shop smart, shop secure — quality products at unbeatable prices!</p>
  </section>

  <!-- Products -->
  <section id="products">
    <h1>Our Top Products</h1>
    <div class="product-grid">
      <div class="product">
        <img src="https://m.media-amazon.com/images/I/71U-Q+N7PXL._SX679_.jpg" alt="Headphones">
        <h3>Wireless Headphones</h3>
        <p>₹999</p>
        <button class="btn">Add to Cart</button>
      </div>
      <div class="product">
        <img src="https://m.media-amazon.com/images/I/61nK+qjQ9DL._SX679_.jpg" alt="Smart Watch">
        <h3>Smart Watch</h3>
        <p>₹2499</p>
        <button class="btn">Add to Cart</button>
      </div>
      <div class="product">
        <img src="https://m.media-amazon.com/images/I/71kVECUOqML._SX679_.jpg" alt="Shoes">
        <h3>Running Shoes</h3>
        <p>₹1499</p>
        <button class="btn">Add to Cart</button>
      </div>
    </div>
  </section>

  <!-- Register -->
  <section id="register">
    <h1>Create Account</h1>
    <form id="registerForm">
      <input type="text" id="rname" placeholder="Full Name" required>
      <span id="rnameError" class="error">Please enter your name</span>

      <input type="email" id="remail" placeholder="Email" required>
      <span id="remailError" class="error">Enter valid email</span>

      <input type="password" id="rpass" placeholder="Password (min 6 chars)" required>
      <span id="rpassError" class="error">Password too short</span>

      <button type="submit">Register</button>
    </form>
  </section>

  <!-- Login -->
  <section id="login">
    <h1>Login</h1>
    <form id="loginForm">
      <input type="email" id="lemail" placeholder="Email" required>
      <span id="lemailError" class="error">Invalid email</span>

      <input type="password" id="lpass" placeholder="Password" required>
      <span id="lpassError" class="error">Password required</span>

      <button type="submit">Login</button>
    </form>
  </section>

  <!-- Dashboard -->
  <section id="dashboard">
    <h1>User Dashboard</h1>

    <h2>My Orders</h2>
    <div class="list-item">Order #1001 - Headphones - Delivered</div>
    <div class="list-item">Order #1002 - Smart Watch - Shipped</div>

    <h2>Wishlist</h2>
    <div class="list-item">Running Shoes</div>

    <h2>Comments & Reviews</h2>
    <div class="list-item">"Excellent Product!" - ⭐⭐⭐⭐⭐</div>
    <div class="list-item">"Fast Delivery" - ⭐⭐⭐⭐</div>

    <h2>Customer Care</h2>
    <p>Need help? We are here 24/7.</p>
    <button class="action-btn" onclick="alert('Live chat started!')">Start Chat</button>

    <h2>Reporting Options</h2>
    <p>Report any issue or feedback below.</p>
    <button class="action-btn" onclick="alert('Thank you! Your report is submitted.')">Submit Report</button>
  </section>

  <!-- About -->
  <section id="about">
    <h1>About RedCart</h1>
    <p>RedCart is a secure and fast-growing e-commerce platform, built to deliver quality and trust to every customer.</p>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h1>Contact Us</h1>
    <p>Email: support@redcart.com</p>
    <p>Phone: +91 98765 43210</p>
    <p>Customer Care: Available 24/7</p>
  </section>

  <script>
    // Registration Validation
    document.getElementById("registerForm").addEventListener("submit", function (e) {
      e.preventDefault();
      let valid = true;

      const name = document.getElementById("rname").value.trim();
      const email = document.getElementById("remail").value.trim();
      const pass = document.getElementById("rpass").value;

      if (name === "") {
        show("rnameError");
        valid = false;
      } else hide("rnameError");

      const emailRegex = /^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$/;
      if (!emailRegex.test(email)) {
        show("remailError");
        valid = false;
      } else hide("remailError");

      if (pass.length < 6) {
        show("rpassError");
        valid = false;
      } else hide("rpassError");

      if (valid) {
        alert("Registration Successful!");
        this.reset();
      }
    });

    // Login Validation
    document.getElementById("loginForm").addEventListener("submit", function (e) {
      e.preventDefault();
      let valid = true;

      const email = document.getElementById("lemail").value.trim();
      const pass = document.getElementById("lpass").value;

      const emailRegex = /^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$/;
      if (!emailRegex.test(email)) {
        show("lemailError");
        valid = false;
      } else hide("lemailError");

      if (pass === "") {
        show("lpassError");
        valid = false;
      } else hide("lpassError");

      if (valid) {
        alert("Login Successful!");
        window.location.href = "#dashboard";
      }
    });

    // Helper functions
    function show(id) {
      document.getElementById(id).style.display = "block";
    }
    function hide(id) {
      document.getElementById(id).style.display = "none";
    }
  </script>
</body>
</html>
