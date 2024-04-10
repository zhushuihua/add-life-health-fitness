<script lang="ts">
    import { getContext, onMount } from "svelte";
    import { Direction } from "./direciton";
    import type { Writable } from "svelte/store";
    import { scale } from "svelte/transition";
    let show: Writable<boolean> = getContext("show");
    export let duration = 1000;
    export let delay = 0;
    export let direction: Direction = Direction.fromTop;
</script>

<div
    class="transition-all"
    style="transition-duration: {duration}ms;transition-delay:{delay}ms"
    class:show={$show}
    class:fromTop={!$show && direction == Direction.fromTop}
    class:fromBottom={!$show && direction == Direction.fromBottom}
    class:fromLeft={!$show && direction == Direction.fromLeft}
    class:fromRight={!$show && direction == Direction.fromRight}
    class:scale-0={direction == Direction.scale && !$show}
    class:scale-full={direction == Direction.scale && $show}
>
    <slot />
</div>

<style lang="postcss">
    .show {
        @apply opacity-100 translate-x-0 translate-y-0;
    }
    .fromBottom {
        @apply opacity-0 translate-y-8;
    }
    .fromTop {
        @apply opacity-0 -translate-y-8;
    }
    .fromLeft {
        @apply opacity-0 -translate-x-8;
    }
    .fromRight {
        @apply opacity-0 translate-x-8;
    }
</style>
