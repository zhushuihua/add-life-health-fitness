<script>
    import { fade, scale } from "svelte/transition";
    import Container from "../common/container.svelte";
    import Oval from "../common/oval.svelte";
    import InPortviewDetection from "../common/in-portview-detection.svelte";
    import FadeIn from "../common/fade-in.svelte";
    let show = false;
    let selectedIndex = 0;
</script>

<div
    class="mt-16 bg-[url(images/img3.jpg)] text-center py-16 space-y-4
"
>
    <InPortviewDetection>
        <FadeIn>
            <div class="space-y-4">
                <h2>Gallery</h2>

                <Oval></Oval>
                <div class="text-sm px-8 max-w-3xl space-y-2 mx-auto">
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                        Praesent eget risus vitae massa
                    </p>
                    <p>semper aliquam quis mattis quam.</p>
                </div>
            </div>
        </FadeIn>
    </InPortviewDetection>
    <Container>
        <div class="grid grid-cols-4 gap-4">
            {#each [1, 2, 3, 4, 5, 6, 7, 8] as index}
                <div class="group relative">
                    <img src={"images/portfolio/0" + index + ".jpg"} alt="" />
                    <div class="h-1 bg-primary"></div>
                    <div
                        class="absolute bg-black/45 inset-0 opacity-0 hover:opacity-100 transition-all grid place-content-center"
                    >
                        <button
                            class="p-2 border-2 border-white rounded-full"
                            on:click={() => {
                                show = true;
                                selectedIndex = index;
                            }}
                            ><svg
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 24 24"
                                fill="currentColor"
                                class="w-6 h-6 text-primary"
                            >
                                <path d="M12 15a3 3 0 1 0 0-6 3 3 0 0 0 0 6Z" />
                                <path
                                    fill-rule="evenodd"
                                    d="M1.323 11.447C2.811 6.976 7.028 3.75 12.001 3.75c4.97 0 9.185 3.223 10.675 7.69.12.362.12.752 0 1.113-1.487 4.471-5.705 7.697-10.677 7.697-4.97 0-9.186-3.223-10.675-7.69a1.762 1.762 0 0 1 0-1.113ZM17.25 12a5.25 5.25 0 1 1-10.5 0 5.25 5.25 0 0 1 10.5 0Z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </button>
                    </div>
                </div>
            {/each}
        </div>
    </Container>
</div>
{#if show}
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <div
        class="fixed inset-0 flex justify-center items-center bg-black/55 p-8 z-10"
        on:click={() => (show = false)}
        transition:fade
    >
        <div
            class="max-w-3xl grow p-1 bg-zinc-50 rounded-lg"
            transition:scale
            on:click|stopPropagation
        >
            <div>
                <img
                    src={"images/portfolio/0" + selectedIndex + ".jpg"}
                    alt=""
                    class="rounded-t-md"
                />
                <div class="text-end pt-2">
                    <button on:click={() => (show = false)}
                        ><svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke-width="1.5"
                            stroke="currentColor"
                            class="w-6 h-6"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                d="m9.75 9.75 4.5 4.5m0-4.5-4.5 4.5M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
                            />
                        </svg>
                    </button>
                </div>
            </div>
        </div>
    </div>
{/if}
