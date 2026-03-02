<script>
</script>
<footer class="footer">
    <div class="footer-container">
        <!--Column-1: Company Info-->
        <div class="footer-column">
        <h3>Rasuwa Hydropower Limited</h3>
        <p>Established in 2066 B.S., Rasuwa Hydropower Limited is the developer of 
        the Phalakhu Khola Hydropower Project (7.29 MW), contributing to Nepal’s 
        sustainable energy development.</p>
    </div>
    <!-- Column 2: Quick Links -->
    <div class="footer-col">
      <h3>Quick Links</h3>
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About Us</a></li>
        <li><a href="/project-overview">Project</a></li>
        <li><a href="/gallery">Gallery</a></li>
        <li><a href="/downloads">Downloads</a></li>
        <li><a href="/contact">Contact</a></li>
      </ul>
    </div>

    <!-- Column 3: Contact -->
    <div class="footer-col">
      <h3>Contact</h3>
      <p>📍 Samakhusi, Kathmandu</p>
      <p>📞 01-4880041</p>
      <p>📧 rasuwahydropower@yahoo.com</p>
    </div>

    <!-- Column 4: Google Map -->
    <div class="footer-col">
        <h3>Our Location</h3>

        <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d27306.986415527863!2d85.27897856228873!3d27.730058094110507!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x39eb190009501341%3A0x63fb435bb26d3f92!2sRasuwa%20Hydropower%20Ltd!5e0!3m2!1sen!2snp!4v1772294801149!5m2!1sen!2snp"
            width="100%"
             height="200"
            style="border:0; border-radius:8px;"
            allowfullscreen
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            title="Rasuwa Hydropower Limited Location">
        </iframe>

    </div>
</div>

<div class="footer-bottom">
    <p>&copy; 2026 Rasuwa Hydropower Limited. All rights reserved.</p>
</div>
</footer>
<style>
.footer {
    background-color: var(--primary-blue);
    color: var(--white);
    padding: 20px 20px;
    margin-top: 30px;
}   
.footer-container {
    display: grid;
    grid-template-columns: 1.4fr 0.6fr 1.1fr 1.6fr;
    gap: 20px;
    padding: 30px 20px;
    max-width: 1200px;
    margin: auto;
    
}
.footer-col h3{
    margin-bottom: 15px;
    font-size: 16px;
    font-weight: 600;
} 
.footer-col p{
    font-size: 14px;
    line-height: 1.6;
}
.footer-col ul {
    list-style: none;
    padding: 0;
}
.footer-col ul li {
    margin-bottom: 8px;
}
.footer-col ul li a {
    color: var(--white);
    text-decoration: none;
    font-size: 14px;
  }

  .footer-col ul li a:hover {
    color: var(--primary-red);
  }

  .footer-bottom {
    text-align: center;
    border-radius: 3px;
    padding: 1px;
    background-color: #08254a;
    font-size: 13px;
    margin: 0px;
  }

  /* Responsive */
  @media (max-width: 900px) {
    .footer-container {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media (max-width: 600px) {
    .footer-container {
      grid-template-columns: 1fr;
    }
  }
</style>  