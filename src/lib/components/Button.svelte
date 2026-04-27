<script>
  export let label = "";
  export let onClick = () => {};
  export let variant = "primary";
</script>

<button class="btn {variant}" on:click={onClick}>
  {label}
</button>

<style>
.btn {
  font-family: var(--font-primary);
  font-size: var(--body-large);
  padding: 1rem 2.5rem;
  border-radius: 16px;
  border: none;
  cursor: pointer;
  background: var(--brand-100);
  color: var(--text-inverse);
  font-style: italic;
  transition: background 0.2s;
}
.btn.primary {
  background: var(--brand-700);
}
.btn.secondary {
  background: var(--brand-100);
  color: var(--brand-900);
}
.btn:active {
  background: var(--brand-900);
  color: var(--text-inverse);
}
</style>
