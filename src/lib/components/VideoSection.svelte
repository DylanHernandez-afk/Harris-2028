<script>
  export let videoSrc = "";
  export let poster = "";
  export let title = "";
</script>

<section class="video-section">
  {#if title}
    <h2 class="video-title">{title}</h2>
  {/if}
  <video controls poster={poster} class="video-player">
    <source src={videoSrc} type="video/mp4" />
    Your browser does not support the video tag.
  </video>
</section>

<style>
.video-section {
  margin: 3rem 0;
  text-align: center;
}
.video-title {
  font-family: var(--font-primary);
  font-size: var(--heading-small);
  color: var(--brand-700);
  margin-bottom: 1rem;
}
.video-player {
  width: 100%;
  max-width: 800px;
  border-radius: 16px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.12);
}
</style>
