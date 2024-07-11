<script>
  import Counter from './Counter.svelte';
  import welcome from '$lib/images/svelte-welcome.webp';
  import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
  <h1>
    <span class="welcome">
      <picture>
        <source srcset={welcome} type="image/webp" />
        <img src={welcome_fallback} alt="Welcome" />
      </picture>
    </span>
    FULVO PA TODO<br />
  </h1>

  <iframe
    allow="autoplay *; encrypted-media *;"
    allowFullScreen
    class="embed-responsive-item"
    frameborder="0"
    height="420"
    id="iframe"
    name="iframe"
    scrolling="no"
    src="https://ntv.tutvlive.info/canaltv.php?ch=https://tutvlive.info/mpd/tvfhd.php?sTL1?id=123"
    width="100%"
  ></iframe>

  <Counter />
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 0.6;
  }

  h1 {
    width: 100%;
  }

  .welcome {
    display: block;
    position: relative;
    width: 100%;
    height: 0;
    padding: 0 0 calc(100% * 495 / 2048) 0;
  }

  .welcome img {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    display: block;
  }

  .embed-responsive-item {
    /* Estilos opcionales para el iframe, según necesidades */
    width: 100%;
    height: 420px; /* ajustar según el diseño */
  }
</style>
