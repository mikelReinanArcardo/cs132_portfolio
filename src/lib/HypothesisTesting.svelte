<script>
	import chart1 from '$lib/assets/chart1.png';
	import chart2 from '$lib/assets/chart2.png';
	import nutshell from '$lib/assets/nutshell.png';

	const darkGradientBg =
		'bg-[radial-gradient(145.05%_100%_at_50%_0%,#1D2B41_0%,#020509_57.38%,#0F1A29_88.16%)]';

	const tabs = [
		{
			id: 'nutshell',
			name: 'Nutshell',
			title: 'Linking Households with Sanitation Access to Dengue Trends in the Philippines',
			imgSrc: nutshell,
			description:
				'The plot explores the relationship between the yearly number of households with sanitation facilities and monthly dengue cases from 2019 to 2022. It addresses two key questions: whether increased sanitation correlates with fewer dengue cases and whether dengue case peaks shift over time. \n\nThe blue line represents the number of households with sanitation facilities, showing a steady increase each year, reflecting improvements in sanitation. The purple line tracks monthly dengue cases, with distinct peaks, especially in 2019, followed by a notable decline in subsequent years.\n\nThe plot highlights seasonal peaks in January, July, and August. Despite the difference in time frames—monthly dengue data and yearly sanitation data—the plot suggests an inverse relationship, with higher sanitation levels possibly linked to fewer dengue cases. However, other factors may also influence these trends, and sanitation alone may not be the sole factor in controlling waterborne diseases.'
		},
		{
			id: 'rq1',
			name: 'Research Question 1',
			title:
				'Research Question 1: Does an increase in the proportion of household sanitation facilities lead to a decline in Dengue cases?',
			imgSrc: chart1,
			description:
				"To test this hypothesis, we applied Pearson's Correlation and Simple Linear Regression to assess the relationship between the proportion of households with sanitation facilities and the normalized number of dengue cases from 2019 to 2022. \n\nThe results from Pearson's Correlation showed an R-value of 0.1663 with a p-value of 0.17517, indicating a weak, positive correlation that is not statistically significant at the 0.05 level. \n\nThe Linear Regression results produced a slope of 257.8338 and an intercept of -11019.8318, with an R value of 0.1663 and a p-value of 0.17517. This further supports the finding that there is no significant linear relationship between sanitation proportions and dengue cases. \n\nSince the p-value is greater than 0.05, we fail to reject the Null Hypothesis, suggesting there is no statistically significant relationship between the proportion of households with sanitation facilities and the number of dengue cases."
		},
		{
			id: 'rq2',
			name: 'Research Question 2',
			title:
				'Research Question 2: Are there any changes in peak season in Dengue cases? How do they change over time?',
			imgSrc: chart2,
			description: 'Placeholder description for Spearman Correlation...'
		}
	];

	let activeTab = tabs[0].id;

	$: activeTabData = tabs.find((tab) => tab.id === activeTab);

	function selectTab(tabId) {
		activeTab = tabId;
	}
</script>

<section
	id="hypothesis-testing"
	aria-labelledby="hypothesis-heading"
	class="w-screen py-8 min-h-screen flex flex-col"
>
	<h2 id="hypothesis-heading" class="text-2xl font-bold sm:text-6xl text-center">
		<span>Results</span>
	</h2>

	<div
		class="flex flex-wrap border-b-2 border-gray-300 mb-0 px-4 md:px-6"
		role="tablist"
		aria-label="Hypothesis testing methods"
	>
		{#each tabs as tab (tab.id)}
			<button
				role="tab"
				aria-selected={activeTab === tab.id}
				aria-controls="tab-content-{tab.id}"
				id="tab-button-{tab.id}"
				on:click={() => selectTab(tab.id)}
				class="py-2 px-4 cursor-pointer border-b-0 mr-1 rounded-t-md transition duration-200 ease-in-out focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-1
                    {activeTab === tab.id
					? `${darkGradientBg} font-semibold text-white`
					: 'bg-gray-200 border border-transparent text-gray-600 hover:bg-gray-300 hover:text-gray-800 mb-[-2px]'}"
			>
				{tab.name}
			</button>
		{/each}
	</div>

	{#if activeTabData}
		<div
			class="px-4 md:px-6 py-6 md:py-8 focus:outline-none {darkGradientBg} flex-grow"
			role="tabpanel"
			id="tab-content-{activeTabData.id}"
			aria-labelledby="tab-button-{activeTabData.id}"
			tabindex="0"
		>
			<h3 class="text-2xl md:text-3xl font-bold text-center mb-6 text-gray-100">
				{activeTabData.title}
			</h3>

			<img
				class="w-[60vw] mx-auto block mb-8 border border-gray-600 rounded shadow-md"
				src={activeTabData.imgSrc}
				alt="{activeTabData.title} - Placeholder Image"
			/>

			{#if activeTabData.description}
				{#each activeTabData.description.split('\n\n') as paragraph}
					{#if paragraph.trim() !== ''}
						<p class="text-lg text-gray-300 leading-relaxed w-[85%] mx-auto text-justify mb-4">
							{paragraph}
						</p>
					{/if}
				{/each}
			{/if}

			<p class="text-lg text-gray-300 leading-relaxed w-[85%] mx-auto text-justify">
				{activeTabData.description}
			</p>
		</div>
	{:else}
		<p class="p-4 text-center text-gray-500 flex-grow">
			Please select a hypothesis testing method.
		</p>
	{/if}
</section>
