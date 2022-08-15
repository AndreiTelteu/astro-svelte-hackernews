<script>
  let open = true;
</script>

<div class={`toggle ${open ? 'open' : ''}`}>
  <!-- svelte-ignore a11y-missing-attribute -->
  <a on:click={(event) => (open = !open)}>
    {open ? '[-]' : '[+] comments collapsed'}
  </a>
</div>
<ul class="comment-children" style={`display: ${open ? 'block' : 'none'}`}>
  <slot />
</ul>
