<script>
  import "fluent-svelte/theme.css";
  import Buttons from './lib/Buttons.svelte';
  import { TextBlock } from "fluent-svelte";
  import { onMount } from 'svelte';
  import { fade, scale } from 'svelte/transition';

  let ready = false;
  onMount(() => ready = true);
</script>

<main>
  {#if ready}
  <div>
    
  </div>
    <div class="content" in:fade>
      <TextBlock ref="title" variant="display">bbot-r</TextBlock>
    </div>
    <div in:fade>
      <TextBlock variant="subtitle">bitchbot, reimagined.</TextBlock>
    </div>

  <div class="buttons" in:fade>
    <p> </p>
    <hr />
    <p> </p>
    <Buttons />
  </div>
  {/if}
</main>

<style>
  :global([ref=title]) {
    font-family: monospace;
  }
</style>
