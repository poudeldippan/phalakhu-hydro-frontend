<script>
  import { browser } from '$app/environment';
  export let limit = null;

  // Load all images from folder
  const modules = import.meta.glob(
    '$lib/assets/gallery/*.{jpg,jpeg,png,webp}',
    { eager: true }
  );

  const allImages = Object.values(modules).map((m) => m.default);

  // Reactive limit logic
  $: images = limit ? allImages.slice(0, limit) : allImages;

  let show = false;
  let current = 0;

  function open(i) {
    current = i;
    show = true;
  }

  function close() {
    show = false;
  }

  function next() {
    current = (current + 1) % images.length;
  }

  function prev() {
    current = (current - 1 + images.length) % images.length;
  }

  // Lock background scroll when lightbox is open
  $: if (browser) {
    document.body.style.overflow = show ? 'hidden' : '';
    // prevent ancestor transforms affecting fixed positioning
    document.body.classList.toggle('lightbox-open', show);
  }
</script>

<!-- Gallery Grid -->
<div class="gallery-grid">
  {#each images as img, i}
    <button
      class="gallery-item"
      on:click={() => open(i)}
      aria-label={`Open image ${i + 1}`}
    >
      <img src={img} alt={`Gallery image ${i + 1}`} />
    </button>
  {/each}
</div>

<!-- Lightbox -->
{#if show}
  <div class="lightbox" on:click={close}>
    <div class="lightbox-content" on:click|stopPropagation>
      <button class="close-btn" on:click={close} aria-label="Close">
        ×
      </button>

      <button class="prev-btn" on:click={prev} aria-label="Previous">
        ‹
      </button>

      <img src={images[current]} alt={`Gallery image ${current + 1}`} />

      <button class="next-btn" on:click={next} aria-label="Next">
        ›
      </button>
    </div>
  </div>
{/if}

<style>
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 15px;
  }

  .gallery-item {
    cursor: pointer;
    overflow: hidden;
    border-radius: 10px;
    padding: 0;
    border: none;
    background: none;
  }

  .gallery-item img {
    width: 100%;
    aspect-ratio: 4/3;
    object-fit: cover;
    transition: transform 0.4s ease;
    display: block;
  }

  .gallery-item:hover img {
    transform: scale(1.08);
  }

  /* Lightbox */

  .lightbox {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, 0.9);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 3000;
  }

  .lightbox-content {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    /* fixed dimensions to enforce uniform size */
    width: 85vw;
    height: 70vh;
    max-width: 900px;
    max-height: 600px;
  }

  .lightbox img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 10px;
  }

  .close-btn,
  .prev-btn,
  .next-btn {
    position: absolute;
    background: rgba(255, 255, 255, 0.1);
    border: none;
    color: white;
    font-size: 2rem;
    cursor: pointer;
    padding: 10px 15px;
    border-radius: 6px;
    transition: background 0.3s ease;
    z-index: 2;
  }

  .close-btn:hover,
  .prev-btn:hover,
  .next-btn:hover {
    background: rgba(255, 255, 255, 0.25);
  }

  .close-btn {
    top: 10px;
    right: 10px;
  }

  .prev-btn {
    left: -60px;
    top: 50%;
    transform: translateY(-50%);
  }

  .next-btn {
    right: -60px;
    top: 50%;
    transform: translateY(-50%);
  }

  /* Responsive */

  @media (max-width: 900px) {
    .gallery-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 500px) {
    .gallery-grid {
      grid-template-columns: 1fr;
    }

    .prev-btn,
    .next-btn {
      left: 10px;
      right: 10px;
    }
  }

  /* when lightbox open remove transforms applied for reveal animation to preserve fixed positioning */
  :global(body.lightbox-open .reveal) {
    transform: none !important;
  }
</style>