<script>
    import './global.css';

    let steps = [
        { name: 'Weather App', icon: 'fa-solid fa-sun', link: 'https://github.com/karomips/weather-app2', description: 'provides real-time weather updates using a weather API.' },
        { name: 'Push Notification App', icon: 'fa-solid fa-bell', link: 'https://github.com/Dumgrammer/pushnotiftracer', description: 'allows users to receive alerts for important events and updates.' },
        { name: 'Task Tracker', icon: 'fa-solid fa-tasks', link: 'https://github.com/PickleC137/TaskTraker', description: 'helps users manage their tasks effectively and efficiently.' }
    ];
</script>

<main class="flex flex-col flex-1 p-4 container">
    <!-- Projects Section -->
    <section id="projects" class="bg-dark-green py-20 lg:py-32 flex flex-col gap-12">
        <div class="flex flex-col gap-2 text-center">
            <h1 class="text-2xl sm:text-3xl md:text-4xl font-semibold text-light">
                A few of my creative endeavors
            </h1>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-light">
                Curious to <span class="poppins text-dark-green">see</span> my work?
            </h3>
        </div>
    
        <!-- Projects Grid -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            {#each steps as step}
                <div class="project-card block p-6 bg-white rounded-lg transition-transform transform hover:scale-105 shadow-lg">
                    <i class="{step.icon} text-dark-green text-3xl mb-4"></i>
                    <p class="text-black text-lg font-medium">{step.name}</p>
                    <p class="text-black text-gray-700">{step.description}</p> <!-- Change text-gray-700 to text-black -->
                    <a href={step.link} target="_blank" class="text-black underline mt-2 inline-block">View Project</a> <!-- Change text-dark-green to text-black -->
                </div>
            {/each}
        </div>
    </section>

    <!-- Intro & About Section -->
    <section id="introPage" class="bg-dark-green py-20 lg:py-32 flex flex-col gap-12"> <!-- Change bg-dark-green to bg-black -->
        <div class="relative shadow-2xl grid place-items-center">
            <!-- Add any content or image here if needed -->
        </div>
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl text-light leading-tight">
                Hi! I'm <span class="poppins text-dark-green">Dave Justin</span> Arcilla<br />Front End
                <span class="poppins text-dark-green">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl text-black">
                My <span class="text-dark-green">favorite tech</span> includes JavaScript (SvelteKit), TailwindCSS, CSS, and HTML.
            </p>
            <a class="mx-auto lg:mr-auto text-lg px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer shadow-lg transition-transform transform hover:scale-105" href="https://www.facebook.com/djra.25/" target="_blank">
                <div class="absolute top-0 right-full w-full h-full bg-dark-green opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-10">Get in touch &rarr;</h4>
            </a>
        </div>
        <!-- About Section Content -->
        <div class="text-center lg:col-span-2">
            <h6 class="text-2xl text-white">Want to know more about me?</h6>
            <h3 class="text-4xl sm:text-5xl md:text-6xl font-semibold text-white">
                A bit <span class="poppins text-dark-green">about</span> me.
            </h3>
            <p class="text-xl sm:text-2xl text-white max-w-2xl mx-auto">
                I'm currently a student with a passion for learning and growing. I enjoy immersing myself in online games, indulging in my favorite foods, and catching up on some much-needed sleep. Life is all about balance, and I strive to enjoy every moment of it!
            </p>
        </div>
    </section>
</main>

<style>
    /* Custom CSS for dark green color */
    .text-dark-green {
        color: #246624;
    }

    h1, h3 {
        color: black;
    }

    .bg-dark-green {
        background-color: #246624;
    }

    .text-light {
        color: #f0f0f0;
    }

    .project-card {
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    /* Padding and spacing refinements */
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 2rem;
    }

    .text-lg {
        font-size: 1.125rem;
    }

    .text-black {
        color: black;
    }

    .text-xl {
        font-size: 1.25rem;
    }

    .text-2xl {
        font-size: 1.5rem;
    }

    .text-3xl {
        font-size: 1.875rem;
    }

    .text-4xl {
        font-size: 2.25rem;
    }

    .leading-tight {
        line-height: 1.2;
    }

    /* Enhanced hover effects */
    a:hover {
        color: #121212;
        background-color: #246624;
    }

    .rounded-lg {
        border-radius: 0.75rem;
    }

    .shadow-lg {
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
    }

    /* Animation and hover effects */
    .transition-transform {
        transition: transform 0.3s ease, background-color 0.3s ease, color 0.3s ease;
    }

    .hover\:scale-105:hover {
        transform: scale(1.05);
    }
</style>
