<script>
  let isMenuOpen = false;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }

  function closeMenu() {
    isMenuOpen = false;
  }
</script>

<!--Top info bar-->
<div class="top-bar">
    <div class="top-left">
    <p>📞 01-4880041</p>
    <p>📧 rasuwahydropower@yahoo.com</p>
    <p>📍Samakhusi, Kathmandu</p>
    </div>
</div>

<nav class="navbar">
  <div class="logo">
    <a href="/" class="logo-link">
    <img src="/logo.png" alt="Rasuwa Hydropower">
    <span>Rasuwa Hydropower Limited</span>
</a>
  </div>

  <!-- Hamburger Menu Button -->
  <button class="hamburger" on:click={toggleMenu} aria-label="Toggle menu">
    <span class="hamburger-line"></span>
    <span class="hamburger-line"></span>
    <span class="hamburger-line"></span>
  </button>

  <!-- Desktop Navigation -->
  <ul class="nav-links desktop-nav">
    <li><a href="/">Home</a></li>

    <!-- ABOUT -->
    <li class="dropdown-parent">
      <span>About Us ▾</span>
      <ul class="dropdown">
        <li><a href="/about">About</a></li>
        <li><a href="/vision">Vision</a></li>
        <li><a href="/team">Team</a></li>
      </ul>
    </li>

    <!-- PROJECT -->
    <li class="dropdown-parent">
      <span>Project ▾</span>
      <ul class="dropdown">
        <li><a href="/project-overview">Overview</a></li>
        <li><a href="/salient-features">Salient Features</a></li>
        <li><a href="/present-status">Present Status</a></li>
      </ul>
    </li>

    <li><a href="/news">News</a></li>
    <li><a href="/gallery">Gallery</a></li>
    <li><a href="/contact">Contact</a></li>
    <li><a href="/downloads">Downloads</a></li>
  </ul>

  <!-- Mobile Navigation Menu -->
  <div class="mobile-menu" class:open={isMenuOpen}>
    <ul class="nav-links mobile-nav">
      <li><a href="/" on:click={closeMenu}>Home</a></li>

      <!-- ABOUT MOBILE -->
      <li class="mobile-dropdown">
        <span>About Us</span>
        <ul class="mobile-dropdown-content">
          <li><a href="/about" on:click={closeMenu}>About</a></li>
          <li><a href="/vision" on:click={closeMenu}>Vision</a></li>
          <li><a href="/team" on:click={closeMenu}>Team</a></li>
        </ul>
      </li>

      <!-- PROJECT MOBILE -->
      <li class="mobile-dropdown">
        <span>Project</span>
        <ul class="mobile-dropdown-content">
          <li><a href="/project-overview" on:click={closeMenu}>Overview</a></li>
          <li><a href="/salient-features" on:click={closeMenu}>Salient Features</a></li>
          <li><a href="/present-status" on:click={closeMenu}>Present Status</a></li>
        </ul>
      </li>

      <li><a href="/news" on:click={closeMenu}>News</a></li>
      <li><a href="/gallery" on:click={closeMenu}>Gallery</a></li>
      <li><a href="/contact" on:click={closeMenu}>Contact</a></li>
      <li><a href="/downloads" on:click={closeMenu}>Downloads</a></li>
    </ul>
  </div>

  <div class="nav-right">
  <a href="/contact" class="contact-btn">Contact Us 📞</a>
</div>
</nav>

<style>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 5px 15px;
    background-color: var(--primary-blue);
    position: relative;
    z-index: 1000;
  }

  .logo a {
    color: var(--white);
    font-weight: bold;
    text-decoration: none;
    font-size: 18px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .logo img {
    height: 75px;
    padding: 0;
    margin: 0;
  }

  /* Hamburger Menu Button */
  .hamburger {
    display: none;
    flex-direction: column;
    background: none;
    border: none;
    cursor: pointer;
    padding: 8px;
    z-index: 1001;
  }

  .hamburger-line {
    width: 25px;
    height: 3px;
    background-color: var(--white);
    margin: 3px 0;
    transition: 0.3s;
    border-radius: 2px;
  }

  /* Desktop Navigation */
  .nav-links.desktop-nav {
    list-style: none;
    display: flex;
    gap: 25px;
    align-items: center;
    position: absolute;
    left: 50%;
    transform: translateX(-40%);
  }

  .nav-links a,
  .nav-links span {
    color: var(--white);
    text-decoration: none;
    font-size: 14px;
    cursor: pointer;
  }

  .nav-links > li {
    position: relative;
  }

  /* Dropdown container */
  .dropdown {
    position: absolute;
    top: 100%;
    left: 0;
    margin-top: 0;
    background: var(--white);
    list-style: none;
    padding: 8px 0;
    min-width: 200px;
    border-radius: 6px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    opacity: 0;
    visibility: hidden;
    transform: translateY(8px);
    transition: all 0.2s ease;
    z-index: 1000;
  }

  /* Show dropdown */
  .dropdown-parent:hover .dropdown {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
  }

  .dropdown li {
    padding: 8px 15px;
  }

  .dropdown li:hover {
    background-color: #f3f3f3;
  }

  .dropdown a {
    color: black;
  }

  .nav-links > li:hover > span,
  .nav-links > li > a:hover {
    opacity: 0.85;
    color: #b88f8f;
  }

  /* Mobile Menu */
  .mobile-menu {
    position: fixed;
    top: 0;
    left: -100%;
    width: 280px;
    height: 100vh;
    background-color: var(--primary-blue);
    transition: left 0.3s ease;
    z-index: 999;
    padding-top: 120px;
    box-shadow: 2px 0 10px rgba(0,0,0,0.3);
  }

  .mobile-menu.open {
    left: 0;
  }

  .nav-links.mobile-nav {
    list-style: none;
    padding: 0 20px;
    margin: 0;
  }

  .mobile-nav li {
    margin-bottom: 10px;
  }

  .mobile-nav a,
  .mobile-nav span {
    color: var(--white);
    text-decoration: none;
    font-size: 16px;
    display: block;
    padding: 12px 15px;
    border-radius: 6px;
    transition: background 0.3s ease;
  }

  .mobile-nav a:hover,
  .mobile-nav span:hover {
    background-color: rgba(255, 255, 255, 0.1);
  }

  /* Mobile Dropdown */
  .mobile-dropdown {
    position: relative;
  }

  .mobile-dropdown-content {
    list-style: none;
    padding: 0;
    margin: 5px 0 0 20px;
    background-color: rgba(255, 255, 255, 0.05);
    border-radius: 6px;
    overflow: hidden;
  }

  .mobile-dropdown-content li a {
    padding: 10px 15px;
    font-size: 14px;
    border-radius: 0;
  }

  .mobile-dropdown-content li a:hover {
    background-color: rgba(255, 255, 255, 0.1);
  }

  .nav-right {
    display: flex;
  }

  .contact-btn {
    background: var(--primary-red);
    color: var(--white);
    padding: 8px 18px;
    border-radius: 12px;
    text-decoration: none;
    font-size: 14px;
    font-weight: 500;
    border: 1px solid var(--primary-red);
    transition: all 0.3s ease;
  }

  .contact-btn:hover {
    opacity: 0.9;
    border: 1px solid var(--primary-red);
    background:#f3f3f3;
    color: var(--primary-red);
    border-radius: 12px;
    transition: all 0.3s ease;
  }

  .top-bar {
    background: #08254a;
    color: var(--white);
    font-size: 14px;
    padding: 0px 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    z-index: 1000;
  }

  .top-left {
    display: flex;
    gap: 20px;
    align-items: center;
  }

  /* Responsive Design */
  @media (max-width: 1024px) {
    .nav-links.desktop-nav {
      gap: 20px;
      font-size: 13px;
    }
  }

  @media (max-width: 900px) {
    .hamburger {
      display: flex;
    }

    .nav-links.desktop-nav {
      display: none;
    }

    .nav-right {
      display: none;
    }

    .top-bar {
      padding: 8px 15px;
    }

    .top-left {
      flex-wrap: wrap;
      gap: 15px;
      font-size: 13px;
    }

    .navbar {
      padding: 10px 15px;
    }

    .logo span {
      display: none;
    }
  }

  @media (max-width: 600px) {
    .top-left {
      flex-direction: column;
      align-items: flex-start;
      gap: 5px;
    }

    .mobile-menu {
      width: 250px;
    }

    .nav-links.mobile-nav {
      padding: 0 15px;
    }
  }

  @media (max-width: 480px) {
    .top-bar {
      padding: 5px 10px;
      font-size: 12px;
    }

    .navbar {
      padding: 8px 10px;
    }

    .logo img {
      height: 60px;
    }

    .mobile-menu {
      width: 100%;
      padding-top: 100px;
    }
  }
</style>