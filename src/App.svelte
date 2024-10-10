<script>
    import Step from "./Step.svelte";
    import './global.css';

    let steps = [
        { name: 'Weather App', icon: 'fa-solid fa-sun', link: 'https://github.com/karomips/weather-app2', description: 'provides real-time weather updates using a weather API.' },
        { name: 'Push Notification App', icon: 'fa-solid fa-bell', link: 'https://github.com/Dumgrammer/pushnotiftracer', description: 'allows users to receive alerts for important events and updates.' },
        { name: 'Task Tracker', icon: 'fa-solid fa-tasks', link: 'https://github.com/PickleC137/TaskTraker', description: 'helps users manage their tasks effectively and efficiently.' }
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="projects" class="bg-dark-green py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl font-semibold text-light">
                A few of my creative endeavors
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-light">
                Curious to <span class="poppins text-dark-green">see</span> my work?
            </h3>
        </div>
        
        <a href="https://www.youtube.com/watch?v=RXKabdUBiWM" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 hover:border-dark-green duration-200">
            <i class="fa-regular fa-circle-play text-white"></i>
            <p class="text-white">Watch the video</p>
        </a>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12">
            {#each steps as step}
                <Step step={step}>
                    <a href={step.link} target="_blank" class="block p-4 bg-white rounded-lg transition-transform transform hover:scale-105 shadow-lg">
                        <p class="text-black">The {step.name} {step.description}</p>
                    </a>
                </Step>
            {/each}
        </div>
    </section>

    <section id="introPage" class="bg-dark-green grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/id-pic-trans.png"} alt="Profile Image" class="object-cover z-[2] max-h-[70vh] rounded-lg shadow-lg" />
        </div>
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl text-light">
                Hi! I'm <span class="poppins text-dark-green">Dave Justin</span> Arcilla<br />Front End
                <span class="poppins text-dark-green">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl text-light">
                My <span class="text-dark-green">favorite tech</span> includes JavaScript (SvelteKit), TailwindCSS, CSS, and HTML.
            </p>
            <a class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer shadow-lg transition-transform transform hover:scale-105" href="https://www.facebook.com/djra.25/" target="_blank">
                <div class="absolute top-0 right-full w-full h-full bg-dark-green opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-10">Get in touch &rarr;</h4>
            </a>            
        </div>
    </section>

    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative">
            <h6 class="text-lg sm:text-xl md:text-2xl text-white">Want to know more about me?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-white">
                A bit <span class="poppins text-dark-green">about</span> me.
            </h3>
        </div>
        <h1 class="text-lg sm:text-xl md:text-2xl text-center text-white">
            I'm currently a student with a passion for learning and growing. I enjoy immersing myself in online games during my free time, where I can unwind and connect with friends. When I'm not gaming, you'll often find me indulging in my favorite foods or catching up on some much-needed sleep. Life is all about balance, and I strive to enjoy every moment of it!
        </h1>
    </section>
</main>

<style>
    /* Custom CSS for dark green color */
    .text-dark-green {
        color: #246624; /* Dark green color */
    }

    .bg-dark-green {
        background-color: #246624; /* Dark green background */
    }

    .text-light {
        color: #f0f0f0; /* Light text color for contrast */
    }
</style>
