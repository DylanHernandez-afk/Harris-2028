<script>
  export let logoSrc = "";
  export let alt = "Logo";
  export let tagline = "";
</script>

<header class="logo-header">
  <img src={logoSrc} alt={alt} class="logo" />
  {#if tagline}
    <span class="tagline">{tagline}</span>
  {/if}
</header>

<style>
.logo-header {
  display: flex;
  align-items: center;
  gap: 1rem;
}
.logo {
  height: 45px;
  width: auto;
}
.tagline {
  font-family: var(--font-secondary);
  font-size: var(--body-medium);
  color: var(--brand-700);
}
</style>
