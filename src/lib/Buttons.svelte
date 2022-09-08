<script>
    import { fade, scale } from 'svelte/transition';
    import * as Fluent from "fluent-svelte";

    const openScript = () => {
        window.open("https://raw.githubusercontent.com/z4xi/bbot-r/main/load");
    }

    const openDiscord = () => {
        window.open("https://discord.gg/Cgbpmksee4");
    }

    const openSource = () => {
        window.open("https://github.com/z4xi/bbot-r/");
    }
</script>
<div in:fade>
    <Fluent.Button on:click={openScript}>
        script
    </Fluent.Button>

    <Fluent.Button on:click={openDiscord}>
        discord
    </Fluent.Button>

    <Fluent.Button on:click={openSource}>
        source
    </Fluent.Button>
</div>