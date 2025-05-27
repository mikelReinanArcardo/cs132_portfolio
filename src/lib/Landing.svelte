<script>
	// Contains only the logic needed for *this* component's animations
	import { onMount } from 'svelte';

	// --- Using Intersection Observer (No Library) ---
	let headerIsVisible = false;
	let h1IsVisible = false;
	let headerElement;
	let h1Element;

	onMount(() => {
		const options = { root: null, rootMargin: '0px', threshold: 0.1 };
		const observerCallback = (entries, observer) => {
			entries.forEach((entry) => {
				if (entry.isIntersecting) {
					// Use entry.target.id or other means to identify
					if (entry.target.id === 'landing-header-text') {
						headerIsVisible = true;
					} else if (entry.target.id === 'landing-h1') {
						h1IsVisible = true;
					}
					observer.unobserve(entry.target);
				}
			});
		};
		const observer = new IntersectionObserver(observerCallback, options);
		// Observe elements within this component
		if (headerElement) observer.observe(headerElement);
		if (h1Element) observer.observe(h1Element);
		return () => {
			if (observer) observer.disconnect();
		};
	});
</script>

<div class="flex flex-col justify-center">
	<section class="w-full">
		<div class="max-w-7xl mx-auto sm:px-6 px-4 pt-10 md:pt-10 lg:pt-10 pb-20">
			<div class="flex items-center">
				<div
					id="landing-header-text"
					class="flex text-4xl md:text-5xl font-bold mx-auto nycd text-white text-shadow-md
                           opacity-0 translate-y-[30px] transition-all duration-[800ms] ease-out
                           opacity-100 translate-y-0"
				>
					Make Me Lose My Breath, Make me Water
				</div>
			</div>
		</div>

		<div class="max-w-7xl mx-auto flex flex-col gap-10 sm:px-6 px-4 py-10 md:pt-10 md:pb-10">
			<h1
				bind:this={h1Element}
				id="landing-h1"
				class="text-3xl md:text-5xl lg:text-6xl flex flex-col text-center text-white text-shadow-lg
                       opacity-0 translate-y-[30px] transition-all duration-[800ms] ease-out delay-300
                       {h1IsVisible ? 'opacity-100 translate-y-0' : ''}"
			>
				<span>
					Relation of the proportion of <strong>households with sanitation facilities</strong>
					and
					<strong>dengue cases</strong> per month
				</span>
				<style>
					h1 strong {
						color: theme('colors.yellow.300');
						font-weight: 600;
					}
				</style>
			</h1>
		</div>
	</section>
</div>
