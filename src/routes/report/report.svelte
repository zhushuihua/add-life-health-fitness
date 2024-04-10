<script>
    import Container from "../common/container.svelte";
    import { Direction } from "../common/direciton";
    import FadeIn from "../common/fade-in.svelte";
    import InPortviewDetection from "../common/in-portview-detection.svelte";
    import Oval from "../common/oval.svelte";
    import OneReport from "./one-report.svelte";
    const data = [
        {
            title: "Clients",
            level: 6850,
        },
        {
            title: "Trainer",
            level: 1465,
        },
        {
            title: "Programs",
            level: 4325,
        },
        {
            title: "Sucess",
            level: 2568,
        },
    ];
</script>

<Container>
    <div class="mt-16 text-center space-y-4">
        <InPortviewDetection>
            <FadeIn>
                <div class="space-y-4">
                    <h2>Healthy Report</h2>
                    <Oval />
                    <div class="space-y-2">
                        <p>
                            Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit. Praesent eget risus vitae massa
                        </p>
                        <p>semper aliquam quis mattis quam.</p>
                    </div>
                </div>
            </FadeIn>
        </InPortviewDetection>
        <InPortviewDetection>
            <FadeIn direction={Direction.fromBottom}>
                <div class="grid sm:grid-cols-2 md:grid-cols-4 mx-auto">
                    {#each data as item}
                        <div class="grid place-content-center">
                            <OneReport {...item}></OneReport>
                        </div>
                    {/each}
                </div>
            </FadeIn>
        </InPortviewDetection>
    </div>
</Container>
