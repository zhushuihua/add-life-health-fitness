<script lang="ts">
    import InPortviewDetection from "../common/in-portview-detection.svelte";

    export let title: string;
    export let content: string;
</script>

<div
    class="pl-24 pr-6 py-6 border-2 border-primary rounded-br-lg space-y-2 relative text-start"
>
    <h3>{title}</h3>

    <p class="text-sm">
        {content}
    </p>
    <div
        class="absolute top-0 left-0 -translate-x-4 -translate-y-4 p-1 size-20 bg-white"
    >
        <div
            class="w-full h-full bg-primary rounded-tl-xl rounded-br-xl grid place-content-center"
        >
            <slot />
        </div>
    </div>
</div>
