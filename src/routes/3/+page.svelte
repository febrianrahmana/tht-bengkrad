<script>

	import { fade } from "svelte/transition";
    import papan from "$lib/images/papan.webp";
    import kelas from "$lib/images/kelas.webp";
    import farras from "$lib/images/farras.webp";

</script>
<div class="h-full content-center justify-center" transition:fade>
    <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight dark:text-white text-center">
        3. Jangan tinggalin akademik!
    </h1>
    <div class="grid grid-cols-3 gap-4 mx-10">
        <div>
            <img src={papan} alt="" class="object-contain">
        </div>
        <div>
            <img src={kelas} alt="" class="object-contain">
        </div>
        <div>
            <img src={farras} alt="" class="object-contain">
        </div>
    </div>
    <div class="mx-64 my-5">
        <p class="text-justify">&emsp;Di sela-sela ke-hectic-an Spektrum, gua juga tetep rajin buat akademik. Apalagi, saat itu lagi ikut SC Matrek IIA. Untungnya, banyak
            juga temen-temen yang ngambil. Jadi, selain kami berkumpul untuk rapat membahas Spektrum, kami juga belajar bareng-bareng. Kalo lagi saatnya kuis atau ujian,
            bahasan Spektrum di-stop dulu dan mulai belajar. Boleh lah tipis tipis dibahas kalo lagi kepikiran. Lagipula, ga semua mamet Spektrum ambil SC. Jadi, kami
            juga bagi tugas. Untungnya, temen-temen yang lain juga pengertian.</p>
    </div>
</div>