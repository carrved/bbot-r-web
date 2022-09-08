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
    <div class="content" in:fade="{{ duration: 2000 }}">
      <TextBlock ref="title" variant="display">bbot-r</TextBlock>
    </div>
    <div in:fade="{{ duration: 2000 }}">
      <TextBlock variant="subtitle">bitchbot, reimagined.</TextBlock>
    </div>

  <div class="buttons" in:fade="{{ duration: 2000 }}">
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
