# LINCOLN-GROUP-CO.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Lincoln Group & Co.</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #f9f9f9;
    }

    header {
      background-color: #ffffff;
      padding: 15px;
      border-bottom: 1px solid #ddd;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
    }

    .logo {
      font-weight: bold;
      color: #00bcd4;
      font-size: 1.2rem;
    }

    .menu-toggle {
      display: none;
      font-size: 1.5rem;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .menu-toggle.open {
      transform: rotate(90deg);
    }

    nav {
      flex: 1;
      transition: all 0.3s ease;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: flex-end;
      flex-wrap: wrap;
      gap: 10px;
      transition: all 0.4s ease;
    }

    nav ul li {
      position: relative;
    }

    nav ul li a {
      text-decoration: none;
      color: #333;
      font-weight: bold;
      transition: color 0.3s ease;
      padding: 8px;
      display: inline-block;
    }

    nav ul li a:hover {
      color: #00bcd4;
    }

    nav ul li ul {
      display: none;
      position: absolute;
      top: 100%;
      left: 0;
      background: white;
      padding: 10px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      animation: dropdown 0.3s ease forwards;
      opacity: 0;
      transform: translateY(-10px);
    }

    @keyframes dropdown {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    nav ul li:hover ul,
    nav ul li:focus-within ul {
      display: block;
    }

    .apply-btn {
      background: #00bcd4;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .apply-btn:hover {
      background-color: #0097a7;
    }

    main.content {
      padding: 40px;
      background: white;
      margin: 20px;
      border-radius: 8px;
      animation: fadeInUp 0.5s ease-in-out;
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Responsive Styles */
    @media (max-width: 768px) {
      .menu-toggle {
        display: block;
      }

      nav {
        display: none;
        width: 100%;
      }

      nav.active {
        display: block;
        animation: fadeInUp 0.4s ease;
      }

      nav ul {
        flex-direction: column;
        align-items: flex-start;
      }

      nav ul li {
        width: 100%;
      }

      nav ul li ul {
        position: relative;
        box-shadow: none;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">Lincoln Group & Co.</div>
    <div class="menu-toggle" onclick="toggleMenu()">☰</div>
    <nav id="main-nav" aria-label="Main navigation">
      <ul>
        <li><a href="#">HOME</a></li>
        <li>
          <a href="#" aria-haspopup="true" aria-expanded="false">ABOUT US</a>
          <ul>
            <li><a href="#">About Us</a></li>
            <li><a href="#">History</a></li>
            <li><a href="#">Mission</a></li>
            <li><a href="#">Consultants</a></li>
            <li><a href="#">Affiliates</a></li>
            <li><a href="#">Founder's Message</a></li>
          </ul>
        </li>
        <li><a href="#">STUDY VISA</a></li>
        <li><a href="#">OTHER VISA</a></li>
        <li><a href="#">EXAMINATIONS</a></li>
        <li><a href="#">ADMISSIONS</a></li>
        <li><a href="#">GALLERY</a></li>
        <li><a href="#">JOBS</a></li>
        <li><a href="#">CONTACT US</a></li>
      </ul>
    </nav>
    <button class="apply-btn">Apply Now</button>
  </header>

  <main class="content">
    <h1>Welcome to Lincoln Group & Co.</h1>
    <p>This is a placeholder page. You can edit this content easily using any text editor or VS Code.</p>
  </main>

  <script>
    function toggleMenu() {
      const nav = document.getElementById("main-nav");
      const toggle = document.querySelector(".menu-toggle");
      nav.classList.toggle("active");
      toggle.classList.toggle("open");
    }
  </script>
</body>
</html>
