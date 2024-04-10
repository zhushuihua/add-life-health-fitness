<script lang="ts">
    import { slide } from "svelte/transition";
    import Container from "../common/container.svelte";
    import NavList from "./nav-list.svelte";
    let showSecondary = false;
    export let height: number;
</script>

<header
    class="fixed w-screen bg-white top-0 left-0 z-10 pb-4"
    bind:clientHeight={height}
>
    <Container>
        <nav
            class="flex md:flex-col lg:flex-row items-center justify-between gap-4"
        >
            <a href="#home" class="self-start"
                ><img src="images/logo.png" alt="logo" /></a
            >
            <NavList />
            <button
                class="md:hidden"
                on:click={() => (showSecondary = !showSecondary)}
                ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-8 h-8"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
                    />
                </svg>
            </button>
        </nav>
    </Container>
    {#if showSecondary}
        <div
            transition:slide
            class=" md:hidden mx-auto absolute w-full [&_li]:px-8 bg-white py-4 border-t border-zinc-400"
        >
            <NavList main={false}></NavList>
        </div>
    {/if}
</header>
