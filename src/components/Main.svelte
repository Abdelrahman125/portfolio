<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Shop",
            icon: "fa-solid fa-martini-glass",
            description:
                "",
        },
        {
            name: "E-commerce Web Application",
            icon: "fa-solid fa-dollar",
            description:
                "",
        },
        {
            name: "Coming Soon",
            icon: "fa-solid fa-history",
            description:
                "",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "Front End Web Developer",
            description:
                "Using React Js I am able to create fast and responsive web pages",
        },
        {
            name: "Back End Web Developer",
            description:
                "ASP.NET dev making robust, scalable and secure web applications",
        },
        {
            name: "Penetration Tester",
            description:
                "Did security research for some websites and discovered some interesting vulnerabilities",
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
                Hi! I'm <span class="poppins text-violet-400">Abdelrahman</span> Alnagar
                <br />
                
            </h2>
            <button
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <a href="https://wa.me/+201065117821"><h4 class="relative z-9">Get in touch &rarr;</h4><a/>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"assets/profile.jpg"}
                alt="Abdelrahman Alnagar"
                class="rounded-full z-[2] max-h-[70vh]"
            />
        </div>
   
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <a
            href="#"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                      I developed a fully functional website that offers users a seamless shopping experience. The website allows customers to browse products, add items to their cart, and complete purchases through a secure checkout process.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                I developed a robust and scalable backend for an e-commerce platform designed to handle high traffic, support multiple payment gateways, and provide seamless integration with various third-party services. The system is optimized for performance and security, ensuring a smooth shopping experience for users.   
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    <br>
                    <br>
                    <br>
                  soon
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
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
        
    </section>
</main>
