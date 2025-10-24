<script lang="ts">
  import { page } from '$app/state'
</script>

<svelte:head>
  <title>404</title>
</svelte:head>

<h1>{page?.error?.message}</h1>
