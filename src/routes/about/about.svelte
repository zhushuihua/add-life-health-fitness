<script>
    import Container from "../common/container.svelte";
    import { Direction } from "../common/direciton";
    import FadeIn from "../common/fade-in.svelte";
    import InPortviewDetection from "../common/in-portview-detection.svelte";
    import Oval from "../common/oval.svelte";
</script>

<div
    class="py-16 text-center bg-cover bg-[url(images/img2.jpg)] text-white mt-8"
>
    <Container>
        <div>
            <InPortviewDetection>
                <FadeIn>
                    <header class="space-y-4 flex flex-col gap-4 mb-4">
                        <h2>Who We Are</h2>
                        <Oval />

                        <p class="max-w-2xl px-8 mx-auto">
                            Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit. Praesent eget risus vitae massa semper aliquam
                            quis mattis quam.
                        </p>
                    </header>
                </FadeIn>
            </InPortviewDetection>
            <div class="text-start grid gap-4 md:grid-cols-2">
                <InPortviewDetection>
                    <FadeIn direction={Direction.fromLeft}>
                        <img
                            src="images/about.png"
                            alt=""
                            class="sm:h-full xl:h-auto object-cover"
                        />
                    </FadeIn></InPortviewDetection
                >
                <InPortviewDetection>
                    <FadeIn direction={Direction.fromRight}>
                        <div class="space-y-4">
                            <h3 class="text-white pb-4 border-b border-white">
                                Our Fitness Studio
                            </h3>
                            <p>
                                Lorem ipsum dolor sit amet, consectetur
                                adipiscing elit. Praesent eget risus vitae massa
                                semper aliquam quis mattis quam. Morbi vitae
                                tortor tempus, placerat leo et, suscipit lectus.
                                Phasellus ut euismod massa, eu eleifend ipsum.
                            </p>
                            <p>
                                Lorem ipsum dolor sit amet, consectetur
                                adipiscing elit. Praesent eget risus vitae massa
                                semper aliquam quis mattis quam adipiscing elit.
                                Praesent eget risus vitae massa.
                            </p>
                            <div class="text-sm">
                                {#each ["Aerobic", "Cardio", "Abdomen", "Special Trainer", "Round the clock"] as item}
                                    <p class="flex gap-2 items-center">
                                        <svg
                                            xmlns="http://www.w3.org/2000/svg"
                                            fill="none"
                                            viewBox="0 0 24 24"
                                            stroke-width="1.5"
                                            stroke="currentColor"
                                            class="w-4 h-4 text-primary"
                                        >
                                            <path
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                                d="m5.25 4.5 7.5 7.5-7.5 7.5m6-15 7.5 7.5-7.5 7.5"
                                            />
                                        </svg>

                                        <span>{item}</span>
                                    </p>
                                {/each}
                            </div>
                        </div>
                    </FadeIn></InPortviewDetection
                >
            </div>
        </div>
    </Container>
</div>
