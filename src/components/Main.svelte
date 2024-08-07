<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "OWASP Juice Shop",
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
            name: "Bug Bounty Hunter",
            description:
                "I’ve successfully reported 0 of critical vulnerabilities, earning recognition and rewards from HackerOne, Bugcrowd",
        },
        {
            name: "CTF Player",
            description:
                "ranked on top 99.9% at TryHackMe and HackTheBox",
        },
        {
            name: "Pentration Tester",
            description:
                "Did pentest for my friend, I destroyed his database and he started cursing me",
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
                <span class="poppins text-violet-400">Penetration</span> Tester
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My motive is breaking complex systems
            </p>
            <button
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
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
            href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Conducted comprehensive security assessments of the <span class="text-violet-400">OWASP Juice Shop</span>, a modern vulnerable web application used for training, demonstrating, and testing web application security tools.
                    Identified and exploited various vulnerabilities, including but not limited to <span class="text-violet-400">SQL Injection, Cross-Site Scripting</span> (<span class="text-violet-400">XSS</span>), <span class="text-violet-400">Broken Authentication</span>, and Insecure Direct Object References (<span class="text-violet-400">IDOR</span>).                    
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Conducted an in-depth security assessment of a large-scale e-commerce web application to identify and mitigate potential security vulnerabilities.
                    Discovered critical vulnerabilities such as Cross-Site Request Forgery (<span class="text-violet-400">CSRF</span>), Insecure Deserialization, Server-Side Request Forgery (<span class="text-violet-400">SSRF</span>), and <span class="text-violet-400">Security Misconfigurations</span>.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    <br>
                    <br>
                    <br>
                  maybe
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