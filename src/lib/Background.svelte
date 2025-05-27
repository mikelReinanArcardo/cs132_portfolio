<script>
	import BackgroundItem from './BackgroundItem.svelte';
</script>

<section
	class="bg-[radial-gradient(145.05%_100%_at_50%_0%,#1D2B41_0%,#020509_57.38%,#0F1A29_88.16%)]"
	id="background"
>
	<div class="mx-auto sm:px-7 px-4 max-w-screen-xl py-20 flex flex-col">
		<h2 class="font-bold text-3xl sm:text-6xl flex flex-col text-center text-white">
			Background of the Study
		</h2>
	</div>
	<section>
		<div class="mx-auto sm:px-7 px-4 max-w-screen-xl py-20">
			<div
				class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-x-16 lg:gap-x-24 gap-y-10 sm:gap-y-20"
			>
				<!-- TODO: add some functionalities for citations e.g. add anchor tags -->
				<BackgroundItem
					value="Dengue, the world's most important water-borne disease that originates from mosquitos, is endemic in the Philippines. A report from the Department of Health showed an annual average of 117,065 cases in the country, placing the Philippines as fourth in dengue burden in Southeast Asia."
					source="Edillo et al. (2015)"
					link="https://doi.org/10.4269/ajtmh.14-0139"
				/>
				<BackgroundItem
					value="Mosquitoes lay their eggs in water, specifically in dirty stagnant water such as ponds, marshes, sewers, and more. Even small accumulation of water in different objects like tires, open drums, canals found in communities can be a breeding ground for these insects."
				/>
				<BackgroundItem
					value="Mosquitoes also thrive in hot and humid environments which are common in tropical countries like the Philippines. As such, regular water sanitation is important in preventing mosquito breeding and  spreading waterborne diseases like dengue. It is preferable to have sanitation facilities in individual households to minimize mosquito growth over the community, possibly lessening the cases of dengue."
					source="Orkin (2024)"
					link="https://www.orkin.com/pests/mosquitoes/mosquito-habitats"
				/>
			</div>
		</div>
	</section>
</section>
