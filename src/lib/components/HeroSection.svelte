<script>
  export let title = "";
  export let subtitle = "";
  export let highlight = "";
</script>

<section class="hero-section">
  <h1 class="hero-title">{title}</h1>
  {#if highlight}
    <h2 class="hero-highlight">{highlight}</h2>
  {/if}
  {#if subtitle}
    <p class="hero-subtitle">{subtitle}</p>
  {/if}
</section>

<style>
.hero-section {
  text-align: left;
  margin-bottom: 2rem;
}
.hero-title {
  font-family: var(--font-accent);
  font-size: var(--heading-hero);
  color: var(--text-inverse);
  margin: 0;
}
.hero-highlight {
  font-family: var(--font-primary);
  font-size: var(--heading-large);
  color: var(--brand-700);
  font-style: italic;
  margin: 0.5rem 0 0 0;
}
.hero-subtitle {
  font-family: var(--font-secondary);
  font-size: var(--body-large);
  color: var(--text-primary);
  margin: 1rem 0 0 0;
}
</style>
