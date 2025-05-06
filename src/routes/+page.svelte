<script>
	import '../app.css';
	import LandingContent from '$lib/Landing.svelte'; // Assuming Landing.svelte is your content
	import Background from '$lib/Background.svelte'; // Use your actual component
	import Navbar from '$lib/Navbar.svelte';
	import Hypothesis from '$lib/Hypothesis.svelte';
	import Dataset from '$lib/Dataset.svelte';
	import Results from '$lib/Results.svelte';
	import Team from '$lib/Team.svelte';
</script>

<Navbar />

<div class="relative landing-container">
	<div class="sticky-background sticky top-0 h-screen -z-10 overflow-hidden"></div>

	<div
		class="background-tint landing-content-wrapper relative z-10 flex flex-col justify-center py-24 md:py-32 -mt-[100vh]"
	>
		{#key 'landing'}
			<LandingContent />
		{/key}
	</div>

	<div class="next-section-wrapper relative z-20 bg-gray-100">
		{#key 'next'}
			<Background />
		{/key}
	</div>
</div>

<Hypothesis />
<Dataset />
<Results />
<Team />

<style>
	.sticky-background::before {
		content: '';
		position: absolute;
		inset: 0;
		background-size: cover;
		background-position: center center;
		background-attachment: local;
		background-image: url('$lib/assets/water.jpg');
		filter: blur(8px) brightness(0.5);
		transform: scale(1.05);
		transition:
			transform 0.3s ease-in-out,
			filter 0.3s ease-in-out;
	}
	.landing-container:hover .sticky-background::before {
		transform: scale(1.1);
		filter: blur(8px) brightness(0.4);
	}
	.background-tint {
		background-color: rgba(47, 79, 79, 0.2);
		background-blend-mode: multiply;
	}

	:global(.text-shadow-md) {
		text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
	}
	:global(.text-shadow-lg) {
		text-shadow: 0 4px 6px rgba(0, 0, 0, 0.6);
	}
</style>
