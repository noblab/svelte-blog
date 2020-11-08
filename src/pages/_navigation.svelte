<script>
  import { layout, url, isActive } from "@sveltech/routify";
</script>

<div>
  <nav class="header">
    {#each $layout.parent.children as { path, title }}
      <a href={$url(path)} class:active={$isActive(path)}>{title}</a>
    {/each}
  </nav>
</div>
