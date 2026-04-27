<script>
  export let paragraphs = [];
</script>

<section class="text-section">
  {#each paragraphs as p (p)}
    <p class="text-paragraph">{p}</p>
  {/each}
</section>

<style>
.text-section {
  margin: 2rem 0;
}
.text-paragraph {
  font-family: var(--font-secondary);
  font-size: var(--body-large);
  color: var(--text-primary);
  margin-bottom: 1.5rem;
}
</style>
