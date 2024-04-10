<script lang="ts">
    import { getContext } from "svelte";
    export let title: string;
    export let level: number;
    import { tweened } from "svelte/motion";
    import type { Writable } from "svelte/store";
    let t = tweened(0, { duration: 1000 });
    let show: Writable<boolean> = getContext("show");
    console.log(show);
    $: if ($show) {
        setTimeout(() => ($t = level), 500);
        // alert("start to show");
    }
</script>

<div class="text-zinc-950 font-medium text-center w-24 space-y-4">
    <div
        class="size-24 rounded-full border-4 border-primary text-center place-content-center"
    >
        <p>{Math.round($t)}</p>
    </div>
    <p>{title}</p>
</div>
