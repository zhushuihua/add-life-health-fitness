<script>
    import Container from "../common/container.svelte";
    import { Direction } from "../common/direciton";
    import FadeIn from "../common/fade-in.svelte";
    import InPortviewDetection from "../common/in-portview-detection.svelte";
    import Oval from "../common/oval.svelte";
    import Trainer from "./trainer.svelte";
    const trainers = [
        { img: "01.jpg", name: "Mikey Deo", position: "Founder" },
        { img: "02.jpg", name: "Mike Timbobbs", position: "Sr. Trainer" },
        { img: "03.jpg", name: "Remo Silvaus", position: "Sr. Trainer" },
        { img: "04.jpg", name: "Niscal Deon", position: "Jr. Trainer" },
    ];
</script>

<Container>
    <div class="text-center space-y-4">
        <InPortviewDetection>
            <FadeIn direction={Direction.fromTop}>
                <div class="mt-16 space-y-4">
                    <h2 class="uppercase">our trainers</h2>
                    <Oval></Oval>
                    <div class="space-y-2">
                        <p>
                            Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit. Praesent eget risus vitae massa
                        </p>
                        <p>semper aliquam quis mattis quam.</p>
                    </div>
                </div>
            </FadeIn></InPortviewDetection
        >
        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-4">
            {#each trainers as trainer, index}
                <InPortviewDetection>
                    <FadeIn
                        delay={index * 100}
                        direction={Direction.fromBottom}
                    >
                        <Trainer {...trainer} />
                    </FadeIn>
                </InPortviewDetection>
            {/each}
        </div>
    </div>
</Container>
