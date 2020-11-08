<script>
  import { layout, url, isActive } from "@sveltech/routify";
</script>

<nav class="header">
  {#each $layout.parent.children as { path, title }}
    <a href={$url(path)} class:active={$isActive(path)}>{title}</a>
  {/each}
</nav>

<div class="hero">
  <div>
    <h1>あさあけまち</h1>
  </div>
  <div>
    <code>
      <p>日の出を待ってる頭の中</p>
      <p>あぶくのようなはかない考えを</p>
      <p>ちょっとだけ残しておく</p>
    </code>
  </div>
  <div>
    <figure>
      <img alt="霧、つとめて" src="images/toppage/fog.jpg" />
      <figcaption>
        Illustration thanks to
        <a
          href="https://pixabay.com/ja/users/cafepampas-610842/"
          target="_blank">cafepampas</a>
      </figcaption>
    </figure>
  </div>
</div>

<!-- routify:options index=10 -->
<!-- routify:options title="home" -->
