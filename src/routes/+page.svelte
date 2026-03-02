<script>
import Gallery from "$lib/components/gallery.svelte";
</script>

<section class="hero">
 <div class="hero-content">
    <h1>Phalakhu Khola Hydropower Project</h1>
    <h2>7.29 MW Run-of-River Development</h2>
    <p>Developed by Rasuwa Hydropower Limited, contributing clean and reliable 
      energy to Nepal’s national grid.</p>
 </div>
 <div class="hero-buttons">
<a href="/about" class="btn red-btn">
  <svg
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    width="18"
    height="18"
  >
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="m11.25 11.25.041-.02a.75.75 0 0 1 1.063.852l-.708 2.836a.75.75 0 0 0 1.063.853l.041-.021M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Zm-9-3.75h.008v.008H12V8.25Z"
    />
  </svg>
  About Us
</a>
    <a href="/project-overview" class="btn blue-btn">
    <span class="icon">⚡</span>
    project overview
    </a>
 </div>
    
</section>
<div class="stats-wrapper">
  <div class="stats">

    <div class="stat-card">
      <div class="stat-icon">⚡</div>
      <h3>7.29 MW</h3>
      <p>Installed generation capacity</p>
    </div>

    <div class="stat-card">
      <div class="stat-icon">💧</div>
      <h3>38.74 GWh</h3>
      <p>Annual energy production</p>
    </div>

    <div class="stat-card">
      <div class="stat-icon">🏗</div>
      <h3>Rs 147 Crore</h3>
      <p>Total project investment</p>
    </div>

    <div class="stat-card">
      <div class="stat-icon">📍</div>
      <h3>Rasuwa District</h3>
      <p>Naukhunda Rural Municipality</p>
    </div>

  </div>
</div>
<section class="about-section">
    <div class="container">
        <div class="about-left">
            <h2>About Rasuwa Hydropower Limited</h2>
            <p>
                Rasuwa Hydropower Limited was established in 2066 B.S. to develop 
        hydropower projects in Nepal. The company is currently developing the 
        7.29 MW Phalakhu Khola Run-of-River Hydropower Project in Rasuwa District.
            </p>
            <p>
                The project contributes clean, renewable energy to Nepal’s national grid 
        while supporting regional infrastructure and economic growth.
            </p>
            <a href="/about" class="section-btn">Learn More➡️</a>
        </div>
        <div class="about-right">
            <img src="/gallery/2.jpeg" alt="About Rasuwa Hydropower Limited">
        </div>
    </div>
</section>
<section class="project-section">
    <div class="container">
        <div class="project-left">
        <img src="/gallery/3.jpeg" alt="About Phalakhu Khola Hydropower Project">

        </div>
        <div class="project-right">
            <h2>Phalakhu Khola Hydropower Project</h2>
            <p>
                The Phalakhu Khola Hydropower Project is a 7.29 MW run-of-river development
        located in Naukhunda Rural Municipality, Rasuwa District. Developed by Rasuwa Hydropower Limited, the project harnesses the flow of the Phalakhu River to generate clean and renewable energy for Nepal’s national grid. With an annual production of 38.74 GWh, the project contributes to Nepal’s sustainable energy future while supporting local economic growth and infrastructure development.
            </p>
            <div class="btn-wrapper">
            <a href="/project-overview" class="section-btn">Learn More➡️</a>

            </div>
            
        </div>
    </div>
</section>
<section class="features">
  <div class="features-container">

    <div class="feature">
      <div class="feature-icon">💧</div>
      <h3>Run-of-River Design</h3>
      <p>Environmentally friendly generation without large reservoir storage.</p>
    </div>

    <div class="feature">
      <div class="feature-icon">⚡</div>
      <h3>National Grid Connected</h3>
      <p>Interconnected to Trisuli 3B Substation via 33kV transmission line.</p>
    </div>

    <div class="feature">
      <div class="feature-icon">🌱</div>
      <h3>Clean Renewable Energy</h3>
      <p>Contributing 38.74 GWh annually to Nepal’s power system.</p>
    </div>

  </div>
</section>
<section class="homepage-gallery">
  <div class="gallery-container">

    <!-- Section Header -->
    <div class="gallery-header">
      <h2>Project Gallery</h2>
      <p>
        Explore images from the Phalakhu Khola Hydropower Project
      </p>
    </div>

    <!-- Gallery Grid -->
    <div class="gallery-content">
      <Gallery limit={8} />
    </div>

    <!-- Button -->
    <div class="gallery-footer">
      <a href="/gallery" class="gallery-btn">
        View All Images
      </a>
    </div>

  </div>
</section>
<style>
/* Homepage Gallery Section */

.homepage-gallery {
  padding: 100px 0;
  background: #f5f7fa;
}

.gallery-container {
  max-width: 1200px;
  margin: auto;
  padding: 0 20px;
  text-align: center;
}

.gallery-header {
  margin-bottom: 50px;
}

.gallery-header h2 {
  font-size: 34px;
  color: var(--primary-blue);
  margin-bottom: 15px;
}

.gallery-header p {
  max-width: 600px;
  margin: auto;
  color: #666;
  line-height: 1.6;
}

.gallery-content {
  margin-bottom: 50px;
}

/* Button */

.gallery-btn {
  display: inline-block;
  padding: 14px 32px;
  background: var(--primary-blue);
  color: white;
  text-decoration: none;
  border-radius: 8px;
  transition: all 0.3s ease;
  font-weight: 500;
  border: 2px solid var(--primary-blue);
}

.gallery-btn:hover {
  background: white;
  color: var(--primary-blue);
  border: 2px solid var(--primary-blue);
}

    .hero {
  background: linear-gradient(
      rgba(10,47,90,0.85),
      rgba(10,47,90,0.85)
    ),
    url("/gallery/1.jpeg");
  background-size: cover;
  background-position: center;
  color: white;
  padding: 140px 20px 180px 20px;
  text-align: center;
  position: relative;
  z-index: 1;
}
.hero-content {
  max-width: 850px;
  margin:auto;
}
.hero h1 {
    font-size: 44px;
    font-weight: 600;
    margin-bottom: 10px;
}
.hero h2 {
    font-size: 22px;
    font-weight: 400;
    margin-bottom: 25px;
}
.hero p{
    font-size: 16px;
  line-height: 1.6;
  margin-bottom: 35px;
}
.hero-buttons {
  display: flex;
  justify-content: center;
  gap: 18px;
  flex-wrap: wrap;
}

.btn {
  padding: 12px 28px;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 500;
  font-size: 14px;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  transition: all 0.3s ease;
  border: 2px solid;
  white-space: nowrap;
}

.red-btn {
  background: var(--primary-red);
  color: white;
  border-color: var(--primary-red);
}

.red-btn:hover {
  background: white;
  color: var(--primary-red);
  transform: scale(1.08);
}

.blue-btn {
  background: var(--primary-blue);
  color: white;
  border-color: var(--primary-blue);
}

.blue-btn:hover {
  background: white;
  color: var(--primary-blue);
  transform: scale(1.08);
}

.icon {
  font-size: 14px;
}
.stats-wrapper {
  position: relative;
  margin-top: -90px;
  padding: 0 20px 80px 20px;
  z-index: 2;
}

.stats {
  max-width: 1100px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 25px;
}

.stat-card {
  background: white;
  padding: 30px 20px;
  border-radius: 12px;
  text-align: center;
  box-shadow: 0 15px 35px rgba(0,0,0,0.08);
  transition: transform 0.3s ease;
}

.stat-card:hover {
  transform: translateY(-8px);
}

.stat-icon {
  font-size: 30px;
  margin-bottom: 15px;
  color: var(--primary-blue);
}

.stat-card h3 {
  font-size: 20px;
  margin-bottom: 8px;
  color: var(--primary-blue);
}

.stat-card p {
  font-size: 13px;
  color: #555;
}
@media (max-width: 900px) {
  .stats {
    grid-template-columns: repeat(2, 1fr);
  }

  .hero h1 {
    font-size: 32px;
  }
}

@media (max-width: 500px) {
  .stats {
    grid-template-columns: 1fr;
  }
}
.about-section{
    padding: 100px 20px;
    background-color: var(--light-bg);
}
.container{
    max-width: 1100px;
    margin: auto;
    display: flex;
    gap: 50px;
    align-items: center;
}
.about-left{
    flex:1;
}
.about-left h2{
    font-size: 28px;
    margin-bottom: 20px;
    color: var(--primary-blue);
}
.about-left p{
    font-size: 16px;
    line-height: 1.6;
    margin-bottom: 20px;
    color: #444
}
.section-btn{
    display: inline-block;
    padding: 10px 24px;
    background-color: var(--primary-blue);
    color: white;
    border-radius: 6px;
    text-decoration: none;
    transition: 0.3s ease;
}
.section-btn:hover{
    background: var(--primary-red);
}

.about-right img{
    width: 100%;
    border-radius: 12px;
}
.project-section{
    padding: 100px 20px;
    background-color: rgb(248, 249, 250);
    border-radius: 12px;
}
.project-left img{
    width: 100%;
    border-radius: 12px;
}
.project-right{
    flex:1;
}
.project-right h2{
    font-size: 28px;
    margin-bottom: 20px;
    color: var(--primary-blue);
}
.project-right p{
    font-size: 16px;
    line-height: 1.6;
    margin-bottom: 20px;
    color: #444
}
.features {
  padding: 80px 20px;
  background: white;
}

.features-container {
  max-width: 1100px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  text-align: center;
}

.feature {
  padding: 30px;
  border-radius: 12px;
  transition: 0.3s ease;
}

.feature:hover {
  box-shadow: 0 15px 30px rgba(0,0,0,0.08);
  transform: translateY(-5px);
}

.feature-icon {
  font-size: 32px;
  margin-bottom: 15px;
  color: var(--primary-blue);
}

.feature h3 {
  margin-bottom: 10px;
  color: var(--primary-blue);
}

.feature p {
  font-size: 14px;
  color: #555;
}
.btn-wrapper {
    margin-top: 30px;
    margin-right: 60px;
    display: flex;
    justify-content: flex-end;
}
</style>

