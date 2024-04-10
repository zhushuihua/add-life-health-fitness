<script lang="ts">
    export let price = 45;
    export let type = "Basic";
    export let primary = false;
    export let domains = 1;
    export let harddisk = 100;
    export let bandwidth = "Unlimited";
    export let ssl = "Shared ssl";
    export let emails = 10;
</script>

<div class="bg-zinc-200 p-4">
    <div class="bg-white h-60 rounded-[50%] py-16 space-y-8" class:primary>
        <div>
            <p
                class="text-3xl font-bold"
                class:text-white={primary}
                class:text-zinc-950={!primary}
            >
                ${price}
            </p>
            <p>per month</p>
        </div>
        <p class="text-3xl font-bold">{type}</p>
    </div>
    <div class="py-8 space-y-4 uppercase">
        <div>
            <span class="font-bold">{domains}</span> <span>Domain</span>
        </div>
        <div>
            <span class="font-bold">{harddisk + "GB"}</span>
            <span>DISK SPACE</span>
        </div>
        <div>
            <span class="font-bold">{bandwidth}</span>
            <span>band width</span>
        </div>
        <div><p>{ssl}</p></div>
        <div>
            <span class="font-bold">{emails}</span>
            <span>email address</span>
        </div>
        <div>
            <span class="font-bold">24/7</span>
            <span>support</span>
        </div>
        <div>
            <button
                class="bg-primary text-white w-full py-2.5 transition-all hover:bg-primary/70"
                >Get It Now</button
            >
        </div>
    </div>
</div>

<style lang="postcss">
    .primary {
        @apply bg-primary text-white;
    }
</style>
