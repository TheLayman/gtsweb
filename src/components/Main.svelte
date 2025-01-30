<!-- https://www.youtube.com/watch?v=-2UjwQzxvBQ -->
<!-- Start from 27 mins -->

<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Concept-Driven Learning",
            icon: "fa-solid fa-lightbulb",
            // description:
            //     "  Smoljames Store is a a merchanising store created with Next.js, Commerce.js & Stripe! Commerce.js is a CMS for managing project and Stripe is used for all transaction handling.",
        },
        {
            name: "Future-Ready Curriculum",
            icon: "fa-solid fa-graduation-cap",
            // description:
            //     "Test for model robustness with customized test profiles and receive exhaustive reporting on the performance and potential vulnerabilities of your model.",
        },
        {
            name: "Beyond Exams",
            icon: "fa-solid fa-line-chart ",
            // description:
            //     "Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "World-Class Learning Environment",
            description:
                "A dynamic blend of academic excellence, creative exploration, and strong values, ensuring every child thrives in a nurturing yet challenging space.",
        },
        {
            name: "Future-Ready Curriculum",
            description:
                "A thoughtfully designed Montessori, Play-Based, and Traditional hybrid, fostering critical thinking, innovation, and adaptability for the ever-evolving world.",
        },
        {
            name: " Strong Community",
            description:
                "Passionate educators, inspiring mentors, and engaged parents come together to create a supportive ecosystem where every student is seen, heard, and empowered.",
        },
        {
            name: "Beyond Books",
            description:
                " From sports and leadership programs to music, drama, and debates, we cultivate confidence, resilience, and real-world skills that shape future leaders.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                We are <span class="poppins text-violet-400">Georgetown</span> School.
                <br />Kothavalasa's 
                <span class="poppins text-violet-400">Best</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                Nurturing <span class="text-violet-400">Bold</span> Thinkers, <span class="text-violet-400">Compassionate</span> Leaders, and Lifelong <span class="text-violet-400"> Learners</span>
            </p>
            <button
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
                on:click={() => document.getElementById('about')?.scrollIntoView({ behavior: 'smooth' })}
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Explore Georgetown &rarr;</h4>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"students1.webp"}
                alt="Zetane Engine"
                class="object-cover z-[2] max-h-[80vh]"
            />
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"students2.webp"}
                alt="Zetane Engine"
                class="object-cover z-[2] max-h-[80vh]"
            />
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"students3.webp"}
                alt="Zetane Engine"
                class="object-cover z-[2] max-h-[80vh]"
            />
        </div>
        <!-- <div  class="flex p-0.5 relative max-w-[700px] w-full mx-auto">
            <div
                class="absolute inset-0 overflow-hidden rounded-md flex items-center justify-center"
            >
                <div
                    class="bg-gradient-to-r absolute inset-[-20px]  from-violet-800 to-indigo-800 specialSpin"
                />
            </div>

            <img
                src={"gtsLogo.png"}
                alt="Zetane Engine"
                class="w-full h-full object-cover z-[2]"
            />
        </div> -->
    </section>
    <section
        id="about"
        class="py-10 pt-10 lg:pt-10 lg:py-22 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Why choose Georgetown?
            </h6>
            
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Because <span class="poppins text-violet-400">Excellence</span> is the Only Standard.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            We offer . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            How Georgetown <span class="text-violet-400">Stands Apart</span> 🚀
        </h5>
        <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">School A</th>
                        <th class="whitespace-nowrap p-2 px-4">School B</th>
                        <th class="whitespace-nowrap p-2 px-4">School C</th>
                        <th
                            class="bg-violet-700 text-white whitespace-nowrap p-4 px-8"
                            >GTS Kothavalasa</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Academic Excellence</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Future-Ready Curriculum</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr>
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Strong Community & Mentorship</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Beyond Academics (Leadership, Arts, Sports)</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                </tbody>
            </table>
            
        </div>
        <button
                class="blueShadow mx-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
                on:click={() => document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' })}
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Join us now &rarr;</h4>
            </button>
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Academics at <span class="poppins text-violet-400">Georgetown</span>
            </h3>
            <p>
            We believe academics should go beyond textbooks and rote learning. Our approach ensures concept mastery, real-world application, and future readiness for every student.
            </p>
        </div>
        <!-- <a
            href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a> -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    At Georgetown, we believe in <strong class="text-violet-400">
                    understanding over memorization</strong>. Our curriculum fosters deep learning through 
                    interactive discussions, hands-on experiments, and inquiry-based exploration. 
                    Students develop critical thinking skills by engaging with real-world applications.  
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Our curriculum blends <strong class="text-violet-400">
                    Montessori, Play-Based, and Traditional approaches</strong> 
                    to create a dynamic and future-proof education. 
                    With an emphasis on STEM, critical thinking, and adaptability, 
                    we prepare students for success in an ever-evolving world.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    We go beyond traditional exams by focusing on <strong class="text-violet-400">
                    skill-based assessments and holistic development</strong>. 
                    Students are evaluated through projects, portfolios, and practical applications, 
                    ensuring they are not just exam-ready, but future-ready.
                </p>
            </Step>
        </div>
        <div class="relative grid place-items-center">
            <img
                src={"gtsLogo.png"}
                alt="Zetane Engine"
                class="object-cover z-[2] max-h-[30vh]"
            />
        </div>
    </section>
</main>