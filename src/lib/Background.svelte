<script>
	import Icon from "@iconify/svelte";
	import BackgroundItem from './BackgroundItem.svelte';
</script>

<section class="bg-bg2" id="background">
	<div class="mx-auto text-4xl md:text-5xl sm:px-7 px-4 gap-4 max-w-screen-xl py-12 md:py-20 flex text-lightblue">
		<Icon icon="material-symbols:book-ribbon-rounded" />
		<h2 class="font-bold ">
			Background of the Study
		</h2>
	</div>
	<section>
		<div class="mx-auto sm:px-7 px-4 max-w-screen-xl pb-20">
			<div
				class="flex flex-col gap-10"
			>
				<!-- TODO: add some functionalities for citations e.g. add anchor tags -->
				<BackgroundItem
					value="Dengue, the world's most important water-borne disease that originates from mosquitos, is endemic in the Philippines. A report from the Department of Health showed an annual average of 117,065 cases in the country, placing the Philippines as fourth in dengue burden in Southeast Asia"
					source="Edillo et al., 2015"
					link="https://doi.org/10.4269/ajtmh.14-0139"
				/>
				<BackgroundItem
					value="Mosquitoes lay their eggs in water, specifically in dirty stagnant water such as ponds, marshes, sewers, and more. Even small accumulation of water in different objects like tires, open drums, canals found in communities can be a breeding ground for these insects"
				/>
				<BackgroundItem
					value="Mosquitoes also thrive in hot and humid environments which are common in tropical countries like the Philippines. As such, regular water sanitation is important in preventing mosquito breeding and  spreading waterborne diseases like dengue. It is preferable to have sanitation facilities in individual households to minimize mosquito growth over the community, possibly lessening the cases of dengue"
					source="Orkin, 2024"
					link="https://www.orkin.com/pests/mosquitoes/mosquito-habitats"
				/>
			</div>
		</div>
	</section>
</section>
