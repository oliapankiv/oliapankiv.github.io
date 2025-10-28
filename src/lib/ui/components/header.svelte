<script lang="ts">
  type Link = {
    href: string
    label: string
  }

  const links: Link[] = [
    { href: 'https://medium.com/@olia.pankiv', label: 'Blog' },
    { href: 'mailto:olha@pankiv.me', label: 'Contact' },
    { href: 'https://cv.pankiv.me', label: 'Resume' },
  ]
</script>

{#snippet link({ href, label }: Link)}
  <a {href} class="px-5 py-4 font-semibold transition-all duration-300 hover:text-hover">
    {label}
  </a>
{/snippet}

<header class="flex flex-col justify-between p-6 sm:flex-row">
  {@render link({ href: '/', label: 'Olha Pankiv' })}

  <nav class="flex gap-4">
    {#each links as item}
      {@render link(item)}
    {/each}
  </nav>
</header>
