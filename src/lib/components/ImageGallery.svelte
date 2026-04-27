<script>
  export let images = [];
</script>

<div class="image-gallery">
  {#each images as img (img.src)}
    <div class="gallery-item">
      <img src={img.src} alt={img.alt} />
    </div>
  {/each}
</div>

<style>
.image-gallery {
  display: flex;
  gap: 2rem;
  justify-content: center;
  margin: 2rem 0;
}
.gallery-item img {
  width: 100%;
  max-width: 320px;
  border-radius: 16px;
  object-fit: cover;
}
</style>
