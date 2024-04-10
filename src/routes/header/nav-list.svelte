<script lang="ts">
    export let main = true;
</script>

<ul class:main class:secondary={!main}>
    <li><a href="#home">home</a></li>
    <li><a href="#classes">classes</a></li>
    <li><a href="#about">about</a></li>
    <li><a href="#trainer">trainers</a></li>
    <li><a href="#gallery">gallery</a></li>
    <li><a href="#pricing">pricing</a></li>
    <li><a href="#contact">contact</a></li>
</ul>

<style lang="postcss">
    a {
        @apply uppercase transition-all;
    }
    .main {
        @apply hidden md:flex gap-4;
    }

    .main a {
        @apply hover:text-primary;
    }
    .secondary li {
        @apply container mx-auto transition-all hover:bg-primary hover:text-white py-2;
    }
</style>
