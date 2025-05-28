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
					value="However, in 2020, the peak season for dengue cases occurred in January. This was due to the sudden COVID-19 lockdown, which forced people to stay indoors, thereby lessening the risk of dengue infection. The pandemic had unintended consequences on dengue transmission. While reduced mobility might have led to fewer outdoor breeding grounds, it also led to a decline in routine public health surveillance and vector control programs. This dual effect—reduced exposure and weakened disease control—likely contributed to the irregular peak of dengue cases in January 2020."
				/>
				<BackgroundItem
					value="The dataset used in this study presents a limitation to the findings. A longer period is recommended to more accurately analyze the relationship between household facilities and the incidence of dengue in the country. Moreover, several other factors may have influenced the results. For example, the COVID-19 pandemic in 2022 may have affected dengue case numbers due to population lockdowns and movement restrictions. It is also recommended to explore other contributing factors to the disease, such as modes of transmission and other waterborne disease variants."
				/>
			</div>
		</div>
	</section>
</section>
