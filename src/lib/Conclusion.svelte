<script>
	import Icon from "@iconify/svelte";
	import BackgroundItem from './BackgroundItem.svelte';
</script>

<section class="bg-bg3" id="conclusion">
	<div class="mx-auto text-4xl md:text-5xl sm:px-7 px-4 gap-4 max-w-screen-xl pb-12 pt-20 flex text-lightblue">
		<Icon icon="material-symbols:chat" />
		<h2 class="font-bold ">
            Conclusion
		</h2>
	</div>
	<section>
		<div class="mx-auto sm:px-7 px-4 max-w-screen-xl pb-20">
			<div
				class="flex flex-col gap-10"
			>
				<BackgroundItem
					value="The study focuses on the correlation between household sanitation facilities and the number of dengue cases across all 17 regions of the Philippines. In the dot plot above, it is shown that more than 90% of households have improved sanitation facilities; however, the proportion of dengue cases by population is spread out and shows no clear relationship with the presence of sanitation facilities. Furthermore, the statistical findings in the results section further prove that household facilities have no relationship with dengue cases. A shortcoming of this study is the limited availability of data on household sanitation facilities; only the years 2019 to 2022 were included and correlated with dengue case numbers."
				/>
				<BackgroundItem
					value="In contrast, a possible explanation is that the breeding grounds of mosquitoes and their mode of disease transmission occur outside of household facilities. Sanitation facilities of individual households are restricted within the boundaries of their homes, making people vulnerable to diseases as soon as they step out of their houses"
					source="Stoddard et al., 2012"
					link="https://doi.org/10.1073/pnas.1213349110"
				/>
				<BackgroundItem
					value="To better understand the nature of the disease, the multi-line graph shows the peak month of dengue cases each year over these four years and was also examined to observe seasonal trends. In August of 2019 and July of 2021 and 2022, dengue cases peaked. This coincides with the start of the rainy season in the Philippines, potentially creating breeding grounds for mosquitoes and increasing their numbers"
					source="Seposo et al., 2024"
					link="https://doi.org/10.3389/fpubh.2024.1420457"
				/>
				<BackgroundItem
					value="The study focuses on the correlation between household sanitation facilities and the number of dengue cases across all 17 regions of the Philippines. In the dot plot above, it is shown that more than 90% of households have improved sanitation facilities; however, the proportion of dengue cases by population is spread out and shows no clear relationship with the presence of sanitation facilities. Furthermore, the statistical findings in the results section further prove that household facilities have no relationship with dengue cases. A shortcoming of this study is the limited availability of data on household sanitation facilities; only the years 2019 to 2022 were included and correlated with dengue case numbers."
				/>
			</div>
		</div>
	</section>
</section>
