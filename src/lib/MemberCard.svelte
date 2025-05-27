<script>
    let { name, imgSrc, description, links } = $props()

    const linkedin = $derived(links.find((link) => link.type === "LinkedIn"));
    const github = $derived(links.find((link) => link.type === "GitHub"));
    const email = $derived(links.find((link) => link.type === "Email"));

    console.log(links)
    console.log(linkedin)
    console.log(github)
</script>

<div class="bg-[#1a344a] p-8 rounded-xl shadow-lg max-w-sm w-full mx-auto my-8">
    <div class="flex  justify-center mb-6">
        <img
            src={imgSrc}
            alt="Profile Picture of {name}"
            class="w-32 h-32 md:w-64 md:h-64 rounded-full border-4 border-blue-500 object-cover"
        >
    </div>

    <h1 class="text-white text-2xl font-bold text-center mb-2">{name}</h1>

    <p class="text-lightblue text-lg text-center mb-4">2nd Year BS CS Student</p>

    <p class="text-white text-base text-center leading-relaxed mb-6 px-4">
        {description}
    </p>

    <div class="flex justify-center space-x-6">
        {#if linkedin !== undefined}
            <a href={linkedin.url} target="_blank" class="text-lightblue hover:text-bg2 transition-colors duration-200" aria-label="LinkedIn Profile">
                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
                </svg>
            </a>
        {/if}
        {#if github !== undefined}
            <a href={github.url} target="_blank" class="text-lightblue hover:text-bg2 transition-colors duration-200" aria-label="GitHub Profile">
                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.08-.731.084-.716.084-.716 1.192.085 1.816 1.29 1.816 1.29 1.066 1.816 2.808 1.29 3.492.986.108-.761.416-1.29.76-1.589-2.671-.304-5.483-1.333-5.483-5.926 0-1.31.465-2.381 1.235-3.221-.124-.303-.535-1.524.117-3.176 0 0 1-.322 3.293 1.235.957-.266 1.983-.399 3.003-.404 1.02.005 2.046.138 3.003.404 2.292-1.557 3.292-1.235 3.292-1.235.653 1.653.242 2.873.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.601-2.813 5.62-5.492 5.918.424.364.793 1.092.793 2.201v3.291c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
            </a>
        {/if}
        {#if email !== undefined}
            <a href="mailto:{email.url}" class="text-lightblue hover:text-bg2 transition-colors duration-200" aria-label="GitHub Profile">
                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <rect x="2" y="5" width="20" height="14" rx="2" ry="2"/>
                    <polyline points="2,7 12,13 22,7"/>
                </svg>
            </a>
        {/if}
    </div>
</div>