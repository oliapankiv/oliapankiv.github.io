<script lang="ts">
  import type { Component } from 'svelte'

  import avatar from '$lib/assets/images/avatar.png'

  import instagram from '$lib/ui/icons/instagram.svelte'
  import github from '$lib/ui/icons/github.svelte'
  import linkedin from '$lib/ui/icons/linkedin.svelte'

  type Link = {
    href: string
    logo: Component
    label: string
  }

  const links: Link[] = [
    {
      href: 'https://www.instagram.com/_olha_13_?igsh=MTc2eHlsNGVqMHl1eg%3D%3D&utm_source=qr',
      logo: instagram,
      label: 'Instagram',
    },
    { href: 'https://github.com/oliapankiv', logo: github, label: 'Github' },
    {
      href: 'https://www.linkedin.com/in/olia-pankiv-192ab5196?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app',
      logo: linkedin,
      label: 'Linkedin',
    },
  ]
</script>

{#snippet link(props: Link)}
  <a href={props.href} class="px-2 transition-all duration-300 hover:text-hover" aria-label={props.label}>
    <props.logo class="h-6 w-6" />
  </a>
{/snippet}

<section class="flex grow flex-col items-center justify-center gap-1">
  <img width="230" height="306" src={avatar} alt="Olha's profile picture" class="h-[150px] w-[150px] rounded-full" />

  <h3 class="text-4xl font-semibold">Olha Pankiv</h3>

  <h4 class="text-xl">Front end developer</h4>

  <div class="mt-3 flex gap-1">
    {#each links as item}
      {@render link(item)}
    {/each}
  </div>
</section>
