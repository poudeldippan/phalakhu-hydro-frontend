<script>
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

  <ul class="nav-links">
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
  }

  .nav-links {
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
    margin-top: 0; /* IMPORTANT: no gap */
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
  .logo img {
    height: 75px;
    padding: 0; 
    margin: 0;
    


  }
  .logo a {
    display: flex;
    align-items: center;
    gap: 10px;
    
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
  background: #08254a; /* darker than primary */
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
</style>