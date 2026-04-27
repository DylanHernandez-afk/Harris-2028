<script>
  export let logoSrc = "";
  export let alt = "";
</script>

<footer class="footer">
  <img src={logoSrc} alt={alt} class="footer-logo" />
</footer>

<style>
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0;
  background: var(--background-secondary);
}
.footer-logo {
  height: 78px;
  width: auto;
}
</style>
