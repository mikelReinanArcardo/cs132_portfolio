<script>
	import Icon from "@iconify/svelte";

	let isOpen = $state(false);
</script>


<nav class=" bg-bg1 sticky top-0 z-50">
	<div class="px-12 md:px-16 flex flex-wrap items-center justify-between w-full p-4">
		<a href="#" class="flex items-center space-x-3 rtl:space-x-reverse">
			<!-- PUT LOGO HERE -->

			<div class=" text-lightblue flex gap-2">
				<Icon icon="material-symbols:water-drop" width="24" height="24" class="self-center"/>
				<span class="hidden sm:block self-center text-2xl font-semibold whitespace-nowrap"
					>Make Me Lose My Breath, Make Me Water</span
				>
			</div>
		</a>
		<div class="hidden md:block md:w-auto">
			<ul
				class="font-medium flex p-4 md:p-0  items-center"
			>
				<li>
					<a
						href="#background"
						class="block py-2 px-3 text-white rounded-sm"
						aria-current="page">Background</a
					>
				</li>
				<li>
					<a
						href="#hypothesis"
						class="block py-2 px-3 text-white rounded-sm"
						aria-current="page">Hypothesis</a
					>
				</li>
				<li>
					<a
						href="#data"
						class="block py-2 px-3 text-white rounded-sm"
						aria-current="page">Data</a
					>
				</li>
				<li>
					<a
						href="#results"
						class="block py-2 px-3 text-white rounded-sm"
						aria-current="page">Results</a
					>
				</li>
				<li>
					<a
						href="#model"
						class="block py-2 px-3 text-white rounded-sm"
						aria-current="page">Model</a
					>
				</li>
				<li>
					<a
						href="#conclusion"
						class="block py-2 px-3 text-white rounded-sm"
						aria-current="page">Conclusion</a
					>
				</li>
				<li>
					<a
						href="#team"
						class="block py-2 px-3 text-white rounded-sm"
						aria-current="page">Team</a
					>
				</li>
			</ul>
		</div>
	</div>
</nav>

<style lang="postcss">
	@reference "tailwindcss";
	:global(html) {
		background-color: theme(--color-gray-100);
	}
</style>
