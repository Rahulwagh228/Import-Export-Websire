<script>
    import "../app.postcss";
    import Logo from "$lib/Images/Logo.png";
    import { fade, scale } from "svelte/transition";

    // AOS.init();

    let images = [
        "https://media.istockphoto.com/id/683044558/photo/fresh-fruits-and-vegetables.webp?b=1&s=612x612&w=0&k=20&c=2eztQ0g2l1L4nRBe3pT5M5l9XQaWlJtLcB40fkrfuGo=",

        "https://cdn.pixabay.com/photo/2013/11/29/15/15/fruit-221158_640.jpg",

        "https://cdn.pixabay.com/photo/2018/04/12/23/57/still-the-fruit-bowl-of-life-3315231_640.jpg",

        "https://cdn.pixabay.com/photo/2017/11/06/18/00/food-photography-2924407_640.jpg",

        "https://cdn.pixabay.com/photo/2015/10/09/21/40/fruit-980014_640.jpg",

        "https://cdn.pixabay.com/photo/2016/08/31/09/08/apple-1632919_640.jpg",

        "https://cdn.pixabay.com/photo/2023/02/06/18/33/mixed-fruits-7772552_640.jpg",
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

<!-- <section
    class="relative bg-cover bg-center bg-no-repeat h-screen w-full;"
    style="background-image: url('{images[i]}');"
>
    .<br />
</section> -->

<section
    class="relative bg-cover bg-center bg-no-repeat h-screen w-full transition-background-image"
    style="background-image: url('{images[i]}');"
>
    <h1 class="flex text-6xl font-bold text-white text-center justify-center">
        KrushiDham The Import Export firm
    </h1>
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
    <div class="flex flex-wrap m-10 justify-evenly">
        {#each products as pr}
            <div class="  mt-8 p-4">
                <div class=" border-2 border-black-900">
                    <img
                        class="h-80 w-80 rounded-md object-cover p-4 hover:scale-110 duration-300"
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
            class="h-full w-full object-cover"
            src="http://puregointernational.in/images/category-2.jpg"
            alt="img"
        />
    </div>
    <div class="div2 h-full w-full object-cover">
        <h1 class="text-center justify-center font-bold text-5xl">
            KrushiDham Exporters
        </h1>
    </div>
    <div class="div3 h-full w-full object-cover">
        <img
            class="h-full w-full"
            src="http://puregointernational.in/images/category-4.jpg"
            alt="img"
        />
    </div>
    <div class="div4 h-full w-full object-cover">
        <img
            class="h-full w-full"
            src="https://cdn.pixabay.com/photo/2018/07/12/14/51/fruit-3533619_640.jpg"
            alt="img"
        />
    </div>
    <div class="div5 h-full w-full object-cover">
        <img
            class="h-full w-full"
            src="https://cdn.pixabay.com/photo/2018/03/09/17/46/paprika-3212163_640.jpg"
            alt="img"
        />
    </div>
    <div class="div6 h-full w-full object-cover">
        <img
            class="h-full w-full"
            src="https://cdn.pixabay.com/photo/2015/03/30/19/36/fruit-700002_640.jpg"
            alt="img"
        />
    </div>
    <div class="div7 h-full w-full">
        <img
            class="h-full w-full"
            src="https://media.istockphoto.com/id/589415708/photo/fresh-fruits-and-vegetables.webp?b=1&s=612x612&w=0&k=20&c=x2SmzKY4cn1sYt7F2MMoVD-Io0GblbJZvWFHApZs_64="
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
    @import url("https://fonts.googleapis.com/css2?family=Borel&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&family=Stylish&display=swap");

   *{
        font-family: "Stylish", sans-serif;
    }
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

    .transition-background-image {
        transition: 0.7s ease-out;
    }
</style>
