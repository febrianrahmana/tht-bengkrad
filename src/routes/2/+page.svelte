<script>

	import { fade } from "svelte/transition";
    import rapat1 from "$lib/images/rapat1.webp"
    import rapat2 from "$lib/images/rapat2.webp"
    import rapat3 from "$lib/images/rapat3.webp"
    import tragedi from "$lib/images/tragedi.webp"

</script>
<div class="h-full content-center justify-center" transition:fade>
    <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight dark:text-white text-center">
        2. Rapat, Rapat, Rapat, dan Tragedi
    </h1>
    <div class="grid grid-cols-4 gap-4 mx-10">
        <div>
            <img src={rapat1} alt="" class="object-contain">
        </div>
        <div>
            <img src={rapat2} alt="" class="object-contain">
        </div>
        <div>
            <img src={rapat3} alt="" class="object-contain">
        </div>
        <div>
            <img src={tragedi} alt="" class="object-contain">
        </div>
    </div>
    <div class="mx-64 my-5">
        <p class="text-justify">&emsp;Setelah itu, kami (hampir) setiap hari bertemu offline untuk rapat. Ga cuma sama divisi Mamet, kami juga ngobrol sama divisi lain buat nyari
            aspirasi. Kadang-kadang produktif, kadang-kadang engga. Setidaknya, tetep pada ngumpul bareng buat ngebahas sesuatu meskipun kadang ga berprogress. Entah tempatnya di kafe,
            ataupun di kos Farras. Sialnya, waktu lagi hectic-hecticnya, laptop gua rusak. Kabel monitornya putus dan hampir copot seutuhnya. Sebenarnya udah dari lama laptop ini agak rusak.
            Engselnya udah keliatan rada-rada dan sering dijadiin bahan becandaan. Tapi kali ini, lumayan nyesek karena jadi gabisa kerja. Akhirnya, dipinjemin laptop dari Belva dan Shafwan
            buat lanjut ngerjain.</p>
    </div>
</div>