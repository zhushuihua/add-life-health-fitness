<script>
    import Container from "../common/container.svelte";
    import { Direction } from "../common/direciton";
    import FromTop from "../common/fade-in.svelte";
    import FadeIn from "../common/fade-in.svelte";
    import Fade from "../common/fade-in.svelte";
    import InPortviewDetection from "../common/in-portview-detection.svelte";
    import Oval from "../common/oval.svelte";
    import Feature from "./feature.svelte";
    const data = [
        {
            title: "Aerobic",
            content:
                "Backed by some of the biggest names in the industry, Firefox OS is an open platform that fosters greater",
        },
        {
            title: "Cardio",
            content:
                "Backed by some of the biggest names in the industry, Firefox OS is an open platform that fosters greater",
        },
        {
            title: "Six Pack",
            content:
                "Morbi vitae tortor tempus, placerat leo et, suscipit lectus. Phasellus ut euismod massa, eu eleifend ipsum.",
        },
        {
            title: "Classes",
            content:
                "Morbi vitae tortor tempus, placerat leo et, suscipit lectus. Phasellus ut euismod massa, eu eleifend ipsum.",
        },
        {
            title: "Special Trainer",
            content:
                "Morbi vitae tortor tempus, placerat leo et, suscipit lectus. Phasellus ut euismod massa, eu eleifend ipsum.",
        },
        {
            title: "Health Sports",
            content:
                "Morbi vitae tortor tempus, placerat leo et, suscipit lectus. Phasellus ut euismod massa, eu eleifend ipsum.",
        },
    ];
</script>

<Container topMargin="2rem">
    <div class="text-center text-sm space-y-4">
        <InPortviewDetection>
            <FadeIn>
                <h2 class="mb-4">Whats Best For You</h2>
                <Oval></Oval>
            </FadeIn>
        </InPortviewDetection>

        <InPortviewDetection>
            <FadeIn>
                <div>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                        Praesent eget risus vitae massa
                    </p>
                    <p>semper aliquam quis mattis quam.</p>
                </div>
            </FadeIn>
        </InPortviewDetection>
        <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
            <InPortviewDetection>
                <FadeIn direction={Direction.fromBottom}>
                    <Feature {...data[0]}>
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="text-white size-8"
                            viewBox="0 0 16 16"
                        >
                            <path
                                fill-rule="evenodd"
                                d="M10.058.501a.5.5 0 0 0-.5-.501h-2.98c-.276 0-.5.225-.5.501A.5.5 0 0 1 5.582 1a.497.497 0 0 0-.497.497V2a.5.5 0 0 0 .5.5h4.968a.5.5 0 0 0 .5-.5v-.503A.497.497 0 0 0 10.555 1a.5.5 0 0 1-.497-.499"
                            />
                            <path
                                fill-rule="evenodd"
                                d="M4.174 1h-.57a1.5 1.5 0 0 0-1.5 1.5v12a1.5 1.5 0 0 0 1.5 1.5h9a1.5 1.5 0 0 0 1.5-1.5v-12a1.5 1.5 0 0 0-1.5-1.5h-.642q.084.236.085.5V2c0 .828-.668 1.5-1.492 1.5H5.581A1.496 1.496 0 0 1 4.09 2v-.5q.001-.264.085-.5Zm3.894 5.482c1.656-1.673 5.795 1.254 0 5.018-5.795-3.764-1.656-6.69 0-5.018"
                            />
                        </svg>
                    </Feature>
                </FadeIn>
            </InPortviewDetection>
            <InPortviewDetection>
                <FadeIn direction={Direction.fromBottom} delay={200}>
                    <Feature {...data[1]}>
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="text-white size-8"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="M1.475 9C2.702 10.84 4.779 12.871 8 15c3.221-2.129 5.298-4.16 6.525-6H12a.5.5 0 0 1-.464-.314l-1.457-3.642-1.598 5.593a.5.5 0 0 1-.945.049L5.889 6.568l-1.473 2.21A.5.5 0 0 1 4 9z"
                            />
                            <path
                                d="M.88 8C-2.427 1.68 4.41-2 7.823 1.143q.09.083.176.171a3 3 0 0 1 .176-.17C11.59-2 18.426 1.68 15.12 8h-2.783l-1.874-4.686a.5.5 0 0 0-.945.049L7.921 8.956 6.464 5.314a.5.5 0 0 0-.88-.091L3.732 8z"
                            />
                        </svg>
                    </Feature>
                </FadeIn>
            </InPortviewDetection>
            <InPortviewDetection>
                <FadeIn direction={Direction.fromBottom} delay={400}>
                    <Feature {...data[2]}>
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            fill="currentColor"
                            class="size-8 text-white"
                        >
                            <path
                                d="M21 6.375c0 2.692-4.03 4.875-9 4.875S3 9.067 3 6.375 7.03 1.5 12 1.5s9 2.183 9 4.875Z"
                            />
                            <path
                                d="M12 12.75c2.685 0 5.19-.586 7.078-1.609a8.283 8.283 0 0 0 1.897-1.384c.016.121.025.244.025.368C21 12.817 16.97 15 12 15s-9-2.183-9-4.875c0-.124.009-.247.025-.368a8.285 8.285 0 0 0 1.897 1.384C6.809 12.164 9.315 12.75 12 12.75Z"
                            />
                            <path
                                d="M12 16.5c2.685 0 5.19-.586 7.078-1.609a8.282 8.282 0 0 0 1.897-1.384c.016.121.025.244.025.368 0 2.692-4.03 4.875-9 4.875s-9-2.183-9-4.875c0-.124.009-.247.025-.368a8.284 8.284 0 0 0 1.897 1.384C6.809 15.914 9.315 16.5 12 16.5Z"
                            />
                            <path
                                d="M12 20.25c2.685 0 5.19-.586 7.078-1.609a8.282 8.282 0 0 0 1.897-1.384c.016.121.025.244.025.368 0 2.692-4.03 4.875-9 4.875s-9-2.183-9-4.875c0-.124.009-.247.025-.368a8.284 8.284 0 0 0 1.897 1.384C6.809 19.664 9.315 20.25 12 20.25Z"
                            />
                        </svg>
                    </Feature>
                </FadeIn>
            </InPortviewDetection>
            <InPortviewDetection>
                <FadeIn direction={Direction.fromBottom} delay={0}>
                    <Feature {...data[3]}>
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="text-white size-8"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="M1 11a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v3a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1zm5-4a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v7a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1zm5-5a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v12a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1z"
                            />
                        </svg>
                    </Feature>
                </FadeIn>
            </InPortviewDetection>
            <InPortviewDetection>
                <FadeIn direction={Direction.fromBottom} delay={200}>
                    <Feature {...data[4]}>
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="text-white size-8"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6"
                            />
                        </svg>
                    </Feature>
                </FadeIn>
            </InPortviewDetection>
            <InPortviewDetection>
                <FadeIn direction={Direction.fromBottom} delay={400}>
                    <Feature {...data[5]}>
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="text-white size-8"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="M8 1a.5.5 0 0 1 .5.5v5.243L9 7.1V4.72C9 3.77 9.77 3 10.72 3c.524 0 1.023.27 1.443.592.431.332.847.773 1.216 1.229.736.908 1.347 1.946 1.58 2.48.176.405.393 1.16.556 2.011.165.857.283 1.857.24 2.759-.04.867-.232 1.79-.837 2.33-.67.6-1.622.556-2.741-.004l-1.795-.897A2.5 2.5 0 0 1 9 11.264V8.329l-1-.715-1 .715V7.214c-.1 0-.202.03-.29.093l-2.5 1.786a.5.5 0 1 0 .58.814L7 8.329v2.935A2.5 2.5 0 0 1 5.618 13.5l-1.795.897c-1.12.56-2.07.603-2.741.004-.605-.54-.798-1.463-.838-2.33-.042-.902.076-1.902.24-2.759.164-.852.38-1.606.558-2.012.232-.533.843-1.571 1.579-2.479.37-.456.785-.897 1.216-1.229C4.257 3.27 4.756 3 5.28 3 6.23 3 7 3.77 7 4.72V7.1l.5-.357V1.5A.5.5 0 0 1 8 1m3.21 8.907a.5.5 0 1 0 .58-.814l-2.5-1.786A.5.5 0 0 0 9 7.214V8.33z"
                            />
                        </svg>
                    </Feature>
                </FadeIn>
            </InPortviewDetection>
        </div>
    </div>
</Container>
