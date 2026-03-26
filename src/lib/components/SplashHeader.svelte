<script>
  export let kicker = '';
  export let headline = '';
  export let deck = '';
  export let pubDate = '';
</script>

<header class="splash-header">
  <span class="kicker">{kicker}</span>
  <h1>{headline}</h1>
  <hr class="rule" />
  <p class="deck">{deck}</p>
  <p class="pubdate">{pubDate}</p>
</header>

<style lang="scss">
  @use '$lib/styles' as *;

  .splash-header {
    text-align: center;
    padding: var(--spacing-xxl) var(--spacing-md);
  }

  .kicker {
    display: block;
    font-family: var(--font-sans);
    font-size: var(--font-size-xs);
    text-transform: uppercase;
    letter-spacing: 0.15em;
    color: var(--color-accent);
    margin-bottom: var(--spacing-sm);
  }

  h1 {
    font-family: var(--font-serif);
    font-size: var(--font-size-5xl);
    line-height: var(--leading-tight);
    color: var(--color-dark);
    margin: 0 0 var(--spacing-sm);
  }

  .rule {
    border: none;
    border-top: var(--border-width-accent) solid var(--color-accent);
    width: 60px;
    margin: 0 auto var(--spacing-sm);
  }

  .deck {
    font-family: var(--font-serif);
    font-size: var(--font-size-lg);
    line-height: var(--leading-normal);
    color: var(--color-text);
    max-width: 480px;
    margin: 0 auto var(--spacing-sm);
  }

  .pubdate {
    font-family: var(--font-sans);
    font-size: var(--font-size-sm);
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: var(--color-medium-gray);
    margin: 0;
  }

  @include mobile {
    h1 {
      font-size: var(--font-size-3xl);
    }

    .deck {
      font-size: var(--font-size-lg);
    }
  }
</style>