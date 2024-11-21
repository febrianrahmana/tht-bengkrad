<script>

	import { fade } from "svelte/transition";
    import pusing from "$lib/images/pusing.webp"
    import kucing from "$lib/images/kucing.webp"
    import makan from "$lib/images/makan.webp"
    import * as Carousel from "$lib/components/ui/carousel/index.js"

</script>
<div class="h-full content-center justify-center" transition:fade>
    <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight dark:text-white text-center">
        4. The Last Straw
    </h1>
    <div class="flex w-1/5 mx-auto">
        <Carousel.Root opts={{
            align: "center",
            loop: "true",
        }}>
            <Carousel.Content>
                <Carousel.Item class="content-center">
                    <img loading="lazy" src={pusing} alt="" class="object-scale-down">
                </Carousel.Item>
                <Carousel.Item class="content-center">
                    <img loading="lazy" src={kucing} alt="" class="object-scale-down">
                </Carousel.Item>
                <Carousel.Item class="content-center">
                    <img loading="lazy" src={makan} alt="" class="object-scale-down">
                </Carousel.Item>
            </Carousel.Content>
            <Carousel.Previous />
            <Carousel.Next />
        </Carousel.Root>
    </div>
    <div class="mx-64 my-5">
        <p class="text-justify">&emsp;
            Setelah SC selesai (Alhamdulillah lulus semua), kami lanjut fokus ngurusin Spektrum. Entah kenapa, terasa lebih
            berat dibandingkan waktu awal-awal. Udah gaada kerjaan lain, tapi kerasa berat aja. Mulai banyak drama-drama antarpanitia, drama-drama dengan anak 23,
            gangguan, kesalahan, keanehan, semuanya campur-aduk. Mana semester baru juga udah mulai.
            Tapi, masih kerasa motivasinya buat ngelanjutin. Bahkan, lebih kuat rasanya setelah mengenal adik-adik ET 23.
            </p>
    </div>
</div>