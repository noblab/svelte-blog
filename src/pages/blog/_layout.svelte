<!-- routify:options index=20 -->
<script>
  import { layout, url, isActive } from "@sveltech/routify";
</script>

<nav class="header">
  {#each $layout.parent.parent.children as { path, title }}
    <a href={$url(path)} class:active={$isActive(path)}>{title}</a>
  {/each}
</nav>

<slot />
