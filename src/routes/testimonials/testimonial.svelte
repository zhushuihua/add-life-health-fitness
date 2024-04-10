<script lang="ts">
    export let img: string;
    export let name: string;
    export let content: string;
</script>

<div class="space-y-2">
    <div class="border rounded-lg p-4">
        {content}
    </div>
    <div class="flex gap-4 items-center">
        <img src="images/{img}" alt="" class="rounded-full" />
        <div class="text-start">
            <p class="text-primary font-bold">{name}</p>
            <div>Loyal Customer</div>
        </div>
    </div>
</div>
