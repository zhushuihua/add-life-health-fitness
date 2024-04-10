<script lang="ts">
    import { onMount, setContext } from "svelte";
    import { writable } from "svelte/store";
    import Fade from "./fade-in.svelte";

    let div: HTMLDivElement;
    export let offsetPercent = 0.5;
    export let show = writable(false);
    setContext("show", show);
    onMount(() => {
        detechScrolling();
        window.addEventListener("scroll", detechScrolling);
        window.addEventListener("resize", detechScrolling);
    });
    function detechScrolling() {
        const clientRect = div.getBoundingClientRect();
        const height = clientRect.height * offsetPercent;
        const top = clientRect.top;
        $show = window.innerHeight > top + height;
        if ($show) {
            window.removeEventListener("scroll", detechScrolling);
            window.removeEventListener("resize", detechScrolling);
        }
    }
</script>

<div bind:this={div}>
    <div>
        <slot />
    </div>
</div>
