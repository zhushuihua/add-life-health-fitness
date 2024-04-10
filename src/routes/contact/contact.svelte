<script>
    import Container from "../common/container.svelte";
    import Oval from "../common/oval.svelte";
</script>

<div class="mt-16 text-center">
    <Container>
        <div class="space-y-4">
            <h2>Contact US</h2>
            <Oval />
            <div>
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                    Praesent eget risus vitae massa
                </p>
                <p>semper aliquam quis mattis quam.</p>
            </div>
        </div>
        <div
            class="bg-primary text-start px-8 py-16 flex flex-col gap-4 md:flex-row"
        >
            <div class=" text-zinc-950 grow-[1]">
                <p class="text-2xl font-bold">Contact Info</p>
                <p>Amazing Company, Inc</p>
                <p>Singapore 760803</p>
                <p>P:(65) 67596888</p>
            </div>
            <form
                class="[&_input]:p-2 [&_textarea]:p-2 flex flex-col gap-4 grow-[5]"
            >
                <input type="text" placeholder="Name" />
                <input type="email" placeholder="Your Email" />
                <textarea placeholder="Message" class="h-28" />
                <button
                    class="bg-[#d9390F] transition-all hover:bg-[#d9390F]/80 text-white self-start !px-8 !py-2.5 rounded-lg"
                    >Send Message</button
                >
            </form>
        </div>
    </Container>
</div>
