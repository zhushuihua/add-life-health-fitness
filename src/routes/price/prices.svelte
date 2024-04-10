<script>
    import Container from "../common/container.svelte";
    import { Direction } from "../common/direciton";
    import FadeIn from "../common/fade-in.svelte";
    import InPortviewDetection from "../common/in-portview-detection.svelte";
    import Oval from "../common/oval.svelte";
    import Price from "./price.svelte";
    const prices = [
        {
            price: 45,
            type: "Basic",
            hilite: false,
            domains: 1,
            harddisk: 100,
            bandwidth: "Unlimited",
            ssl: "Shared ssl",
            emails: 10,
            primary: false,
        },
        {
            price: 85,
            type: "Bronze",
            hilite: false,
            domains: 5,
            harddisk: 500,
            bandwidth: "Unlimited",
            ssl: "Shared ssl",
            emails: 30,
            primary: true,
        },
        {
            price: 125,
            type: "Silver",
            hilite: false,
            domains: 1,
            harddisk: 1000,
            bandwidth: "Unlimited",
            ssl: "Shared ssl",
            emails: 50,
            primary: false,
        },
        {
            price: 185,
            type: "Gold",
            hilite: false,
            domains: 1,
            harddisk: 2000,
            bandwidth: "Unlimited",
            ssl: "Shared ssl",
            emails: 100,
            primary: false,
        },
    ];
</script>

<Container>
    <div class="mt-16">
        <div class="text-center space-y-4">
            <InPortviewDetection>
                <FadeIn>
                    <div class="space-y-4">
                        <h2>Price</h2>
                        <Oval />
                        <div>
                            <p>
                                Lorem ipsum dolor sit amet, consectetur
                                adipiscing elit. Praesent eget risus vitae massa
                            </p>
                            <p>semper aliquam quis mattis quam.</p>
                        </div>
                    </div>
                </FadeIn>
            </InPortviewDetection>
            <div class="grid sm:grid-cols-2 md:grid-cols-4 gap-4">
                {#each prices as price, index}
                    <InPortviewDetection>
                        <FadeIn direction={Direction.scale} delay={index * 200}>
                            <Price {...price}></Price>
                        </FadeIn>
                    </InPortviewDetection>
                {/each}
            </div>
        </div>
    </div>
</Container>
