<script>
  import Gallery from '$lib/components/gallery.svelte';
</script>

<!--Hero section-->
<section class="page-hero">
  <div class="hero-container">
    <h1>Gallery</h1>
    <p>Explore the visual journey of our hydropower projects and infrastructure development.</p>
  </div>
</section>

<!--Gallery section-->
<section class="gallery-section">
  <div class="container">
    <Gallery />
  </div>
</section>

<style>
  .page-hero {
    padding: 50px 20px;
    text-align: center;
    background: linear-gradient(#fff, #f5f7fa);
  }

  .page-hero h1 {
    font-size: 42px;
    color: var(--primary-blue);
    margin-bottom: 20px;
  }

  .page-hero p {
    max-width: 700px;
    margin: auto;
    color: #555;
    text-decoration: underline;
  }

  .gallery-section {
    padding: 50px 20px;
  }

  .container {
    max-width: 1100px;
    margin: auto;
    padding: 10px 0px;
  }
</style>