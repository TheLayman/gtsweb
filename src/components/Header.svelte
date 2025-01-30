<script>
    export let y;

    export let tabs = [
        { name: "About Us ", link: "#about" },
        { name: "Academics", link: "#projects" },
        // { name: "Student Life :)", link: "https://www.youtube.com/watch?v=BBJa32lCaaY" },
    ];
</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid bg-[#11243C] " +
        (y > 0
            ? " py-4 border-violet-950"
            : " py-6 border-transparent")}
>
    <h1 class="font-large text-3xl">
        <b class="font-bold Jura">GTS </b> <span class="Jura">Kothavalasa</span>
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-400",
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <button
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-violet-600 text-white"
            on:click={() => document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' })}
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Admissions</h4>
        </button>
        <button
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
            on:click={() => document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' })}
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Contact Us</h4>
        </button>
    </div>
</header>