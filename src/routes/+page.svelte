<script>
    import "../app.postcss";
    import Logo from "$lib/Images/Logo.png";
    import { fade, scale } from "svelte/transition";

    let images = [
        "https://images.unsplash.com/photo-1579113800032-c38bd7635818?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OHx8dmVnZXRhYmxlc3xlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=500&q=60",
        "https://images.unsplash.com/photo-1598030304671-5aa1d6f21128?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTd8fHZlZ2V0YWJsZXN8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=500&q=60",
        "https://images.unsplash.com/photo-1488459716781-31db52582fe9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTh8fHZlZ2V0YWJsZXN8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=500&q=60",
        "https://media.istockphoto.com/id/1524823226/photo/colorful-raw-fruits-and-vegetables-varied-vegan-food-vivid-rainbow-arrangement.webp?b=1&s=170667a&w=0&k=20&c=S5dNqLRpZc0WNlgtxgQAFj1x41_qsM1bL9qioqtHIxw=",
        "https://media.istockphoto.com/id/1347540778/photo/leaves-of-different-sizes-and-colors-close-up.webp?b=1&s=170667a&w=0&k=20&c=-dto-2w3V3v_CZZuErUSHwAHr2QS_CEVq2VN3jm341k=",
        "https://media.istockphoto.com/id/1474498534/photo/female-dietitian-doctor-writing-meal-plan.webp?b=1&s=170667a&w=0&k=20&c=XXSbxmBKN-zMQgXfr79NapN1UqbtU0klPe1Ovxm5qLA=",
        "https://www.shutterstock.com/image-photo/fresh-healthy-vegitables-fruits-260nw-1569804757.jpg",
    ];

    let i = 0;

    setInterval(() => {
        if (i === images.length - 1) {
            i = 0;
        }
        i++;
    }, 3000);

    let navs = [
        {
            name: "Home",
            link: "#",
        },
        {
            name: "About Us",
            link: "#",
        },
        {
            name: "Products",
            link: "#",
        },
        {
            name: "Contact Us",
            link: "#",
        },
        {
            name: "Our Speaciality",
            link: "#",
        },
    ];

    let products = [
        {
            img: "http://puregointernational.in/images/onion.png",
            name: "Onion",
        },
        {
            img: "http://puregointernational.in/images/banana.png",
            name: "Banana",
        },
        {
            img: "http://puregointernational.in/images/grapes.png",
            name: "Grapes",
        },
        {
            img: "http://puregointernational.in/images/tomatoes.png",
            name: "Tomatoes",
        },
        {
            img: "http://puregointernational.in/images/mangoes.png",
            name: "Mangos",
        },
        {
            img: "http://puregointernational.in/images/product-many.jpg",
            name: "And Many More",
        },
    ];

    // AOS.init();
</script>

<!-- <div class="flex justify-center">

    {#key i}

    <div class="w-full h-auto">
        <img src={navs[i]} class="w-full h-full" alt= "img" />
    </div>
    {/key }
    
</div> -->
<nav class=" flex bg-slate-300 justify-between px-40">
    <img src={Logo} class="w-20 h-20" alt="Logo" />
    <ul class=" flex gap-7 justify-center py-8">
        {#each navs as nav}
            <li
                class="font-semibold hover:scale-125 transition duration-500 hover:font-bold"
            >
                <a href={nav.link}>
                    {nav.name}
                </a>
            </li>
        {/each}
    </ul>
</nav>

<section
    class="relative bg-cover bg-center bg-no-repeat h-screen w-full;"
    style="background-image: url('{images[i]}');"
>
    .<br />
</section>

<section data-aos="fade-up" class="bg-white">
    <div class="mx-auto max-w-screen-xl px-4 py-12 sm:px-6 md:py-16 lg:px-8">
        <div class="mx-auto max-w-3xl text-center">
            <h2 class="text-3xl font-bold text-gray-900 sm:text-4xl">
                Our Service
            </h2>

            <p class="mt-4 text-gray-500 sm:text-xl">
                krushidham is a trusted by lots of foreign builders
            </p>
        </div>

        <div class="mt-8 sm:mt-12">
            <dl class="grid grid-cols-1 gap-4 sm:grid-cols-3">
                <div
                    class="flex flex-col rounded-lg bg-blue-100 px-4 py-8 text-center"
                >
                    <dt class="order-last text-lg font-medium text-gray-500">
                        Total Sales
                    </dt>

                    <dd
                        class="text-4xl font-extrabold text-blue-600 md:text-5xl"
                    >
                        $4.8m
                    </dd>
                </div>

                <div
                    class="flex flex-col rounded-lg bg-blue-100 px-4 py-8 text-center"
                >
                    <dt class="order-last text-lg font-medium text-gray-500">
                        Countries Served
                    </dt>

                    <dd
                        class="text-4xl font-extrabold text-blue-600 md:text-5xl"
                    >
                        6
                    </dd>
                </div>

                <div
                    class="flex flex-col rounded-lg bg-blue-100 px-4 py-8 text-center"
                >
                    <dt class="order-last text-lg font-medium text-gray-500">
                        Registered Farmer
                    </dt>

                    <dd
                        class="text-4xl font-extrabold text-blue-600 md:text-5xl"
                    >
                        23
                    </dd>
                </div>
            </dl>
        </div>
    </div>
</section>

<section class="md:h-full items-center">
    <div>
        <h1 class="font-bold text-6xl text-center">Our Products</h1>
    </div>
    <div class="flex flex-wrap m-10 px-36">
        {#each products as pr}
            <div class="  mt-8 p-4">
                <div class=" border-2 border-black-900">
                    <img
                        class="h-80 w-80 rounded-md p-4 hover:scale-110 duration-300"
                        src={pr.img}
                        alt={pr.name}
                    />

                    <p class=" text-center font-semibold text-2xl p-4">
                        {pr.name}
                    </p>
                </div>
            </div>
        {/each}
    </div>
</section>
<div data-aos="fade-up" class="parent h-screen">
    <div class="div1 h-full w-full">
        <img
            class="h-full w-full"
            src="http://puregointernational.in/images/category-2.jpg"
            alt="img"
        />
    </div>
    <div class="div2 h-full w-full">
       <h1 class="text-center justify-center font-bold text-5xl ">KrushiDham Exporters </h1>
    </div>
    <div class="div3 h-full w-full">
        <img
            class="h-full w-full"
            src="http://puregointernational.in/images/category-4.jpg"
            alt="img"
        />
    </div>
    <div class="div4 h-full w-full">
        <img
            class="h-full w-full"
            src="https://www.shutterstock.com/image-photo/fresh-healthy-vegitables-fruits-260nw-1569804757.jpg"
            alt="img"
        />
    </div>
    <div class="div5 h-full w-full">
        <img
            class="h-full w-full"
            src="https://www.shutterstock.com/image-photo/fresh-healthy-vegitables-fruits-260nw-1569804757.jpg"
            alt="img"
        />
    </div>
    <div class="div6 h-full w-full">
        <img
            class="h-full w-full"
            src="https://www.shutterstock.com/image-photo/fresh-healthy-vegitables-fruits-260nw-1569804757.jpg"
            alt="img"
        />
    </div>
    <div class="div7 h-full w-full">
        <img
            class="h-full w-full"
            src="https://www.shutterstock.com/image-photo/fresh-healthy-vegitables-fruits-260nw-1569804757.jpg"
            alt="img"
        />
    </div>
    <div class="div8 h-full w-full">
        <img
            class="h-full w-full"
            src="https://www.shutterstock.com/image-photo/fresh-healthy-vegitables-fruits-260nw-1569804757.jpg"
            alt="img"
        />
    </div>
</div>

<section />

<slot />

<style>
    .parent {
        display: grid;
        grid-template-columns: repeat(8, 1fr);
        grid-template-rows: repeat(8, 1fr);
        grid-column-gap: 20px;
        grid-row-gap: 20px;
    }

    .div1 {
        grid-area: 1 / 1 / 4 / 4;
    }
    .div2 {
        grid-area: 1 / 4 / 5 / 6;
    }
    .div3 {
        grid-area: 1 / 6 / 4 / 9;
    }
    .div4 {
        grid-area: 4 / 6 / 7 / 9;
    }
    .div5 {
        grid-area: 7 / 6 / 9 / 9;
    }
    .div6 {
        grid-area: 5 / 4 / 9 / 6;
    }
    .div7 {
        grid-area: 4 / 1 / 7 / 4;
    }
    .div8 {
        grid-area: 7 / 1 / 9 / 4;
    }
</style>
