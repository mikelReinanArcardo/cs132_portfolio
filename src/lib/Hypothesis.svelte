<script>
	import Icon from "@iconify/svelte";
	import HypothesisItem from "./HypothesisItem.svelte";
</script>

<section id="hypothesis" class="bg-bg3">
	<div class="mx-auto sm:px-7 px-4 max-w-screen-xl py-20">
		<div class="flex flex-col md:flex-row gap-10 items-center">
			<div class="grid gap-12 ">
				<div class="flex gap-2 text-lightblue text-4xl md:text-5xl">
					<Icon icon="material-symbols:lightbulb-2"  />
						<h2 class="font-bold ">
						<span>Hypothesis</span>
					</h2>
				</div>
				<div class="flex flex-col gap-8">
					<HypothesisItem 
						number=1
						question="Does an increase in the proportion of household sanitation facilities lead to a
							decline in Dengue cases?" 
						alt="Regions with higher proportions of households with proper sanitation facilities will have lower annual dengue case counts."
						nul="There is no significant relationship between the proportion of households with sanitation facilities and the number of dengue cases."
					/>
					<HypothesisItem 
						number=2
						question="Are there any changes in peak season in Dengue cases? How do they change over
							time?" 
						alt="The timing and magnitude of the seasonal peak in dengue cases have significantly changed over the period."
						nul="There is no significant change in the timing or magnitude of the seasonal peak dengue cases over time."
					/>
			</div>
		</div>
	</div>
</section>
