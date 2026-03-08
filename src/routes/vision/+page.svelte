<!--Hero Section-->
<section class="page-hero">
<div class="hero-container">
    <h1>Our Vision, Mission & Guiding Values</h1>
    
</div>
</section>
<!--Vision-->
<section class="vision">
<div class="container">
<h2>Our vision</h2>
<p>Make a significant impact on Nepal’s hydropower sector development.</p>
<p>Discover and develop new hydropower and clean energy projects.</p>
<p>Build the skills and resources required for independent power generation.</p>
</div>
<hr>
</section>


<!--Mission-->
<section class="mission">
<div class="container">
<h2>Our Mission</h2>
<p>Utilizing Nepal’s clean energy resources.</p>
<p>Lowering reliance on costly fossil fuels like oil and gas.</p>
<p>Supporting nation-building through energy security and export.</p>

</div>
<hr>
</section>
<!--Guiding Values-->
<section class="guiding-values">
<div class="container">
<h2>Guiding Values</h2>
<p>Developing entrepreneurship and maximizing advantages.</p>
<p>Promoting good governance, integrity, and accountability.</p>
<p>Encouraging development with local participation and social responsibility.</p>
</div>

</section>
<style>
    .page-hero{
        
         padding: 100px 110px;
        
    }
    .hero-container{
       max-width: 1100px;
      text-align: center;
    }
    .page-hero h1{
        color: var(--primary-blue);
    }
    .container{
        text-align: center;
        margin-top: 50px;
        margin-bottom: 100px;
    }
    .container h2{
        text-decoration: underline;
        color: var(--primary-blue);
    }
    .vision,.mission,.guiding-values{
        padding: 0px 120px;
    }
    
/* Responsive Design */
@media (max-width: 900px) {
  .page-hero {
    padding: 80px 50px;
  }

  .page-hero h1 {
    font-size: 28px;
  }

  .vision, .mission, .guiding-values {
    padding: 0px 60px;
  }

  .container {
    margin-top: 40px;
    margin-bottom: 60px;
  }
}

@media (max-width: 600px) {
  .page-hero {
    padding: 60px 30px;
  }

  .page-hero h1 {
    font-size: 24px;
  }

  .vision, .mission, .guiding-values {
    padding: 0px 30px;
  }

  .container h2 {
    font-size: 22px;
  }

  .container p {
    font-size: 16px;
  }
}

@media (max-width: 480px) {
  .page-hero {
    padding: 40px 20px;
  }

  .page-hero h1 {
    font-size: 20px;
  }

  .vision, .mission, .guiding-values {
    padding: 0px 20px;
  }

  .container {
    margin-top: 30px;
    margin-bottom: 40px;
  }

  .container h2 {
    font-size: 20px;
  }
}
</style>