<script lang="ts">
  import '../app.css'

  import faviconico from '$lib/assets/favicon/favicon.ico'
  import faviconsvg from '$lib/assets/favicon/favicon.svg'

  const { children } = $props()
</script>

<svelte:head>
  <link rel="icon" type="image/ico" href={faviconico} />
  <link rel="icon" type="image/svg+xml" href={faviconsvg} />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
</svelte:head>

{@render children?.()}
