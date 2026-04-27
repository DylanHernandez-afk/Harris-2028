<script>
  export let src = "";
  export let alt = "";
</script>

<div class="main-image">
  <img src={src} alt={alt} />
</div>

<style>
.main-image img {
  width: 100%;
  max-width: 700px;
  border-radius: 24px;
  object-fit: cover;
  display: block;
  margin: 0 auto;
}
</style>
