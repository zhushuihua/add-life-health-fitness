<script lang="ts">
    import Container from "../common/container.svelte";
    import FadeIn from "../common/fade-in.svelte";
    import InPortviewDetection from "../common/in-portview-detection.svelte";
    import Oval from "../common/oval.svelte";
    import Testimonial from "./testimonial.svelte";
    const data = [
        {
            img: "pic1.jpg",
            name: "John Bond",
            content:
                "Sontrary to popular belief, Lorem Ipsuis no simply random text. It has roots in a piece of classical Layears old. belief, Lorem Ipsuis not simply",
        },
        {
            img: "pic2.jpg",
            name: "Bill Doe",
            content:
                "Aontrary to popular belief, Lorem Ipsuis no simply random text. It has roots in a piece of classical Layears old. belief, Lorem Ipsuis not simply",
        },
        {
            img: "pic1.jpg",
            name: "Jane Well",
            content:
                "Tontrary to popular belief, Lorem Ipsuis no simply random text. It has roots in a piece of classical Layears old. belief, Lorem Ipsuis not simply",
        },
    ];
</script>

<div class="text-center object-cover bg-[url(images/img4.jpg)] mt-16">
    <Container>
        <div class="space-y-4 py-16">
            <InPortviewDetection>
                <FadeIn>
                    <div class="space-y-4">
                        <h2 class="text-white">Testimonials</h2>
                        <Oval></Oval>
                        <div class="text-white">
                            <p>
                                Lorem ipsum dolor sit amet, consectetur
                                adipiscing elit. Praesent eget risus vitae massa
                            </p>
                            <p>semper aliquam quis mattis quam.</p>
                        </div>
                    </div>
                </FadeIn>
            </InPortviewDetection>
            <div class="flex flex-col gap-6 md:flex-row">
                {#each data as item}
                    <Testimonial {...item}></Testimonial>
                {/each}
            </div>
        </div>
    </Container>
</div>
