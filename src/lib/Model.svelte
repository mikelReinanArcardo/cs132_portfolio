<script>
	import Icon from "@iconify/svelte";
	import ModelItem from "./ModelItem.svelte";
	import model from '$lib/assets/model.png';

    const data = [
        {
            question: "Why the SARIMAX model was chosen",
            answer: "We chose the SARIMAX model due to its ability to handle time series data with both trend and seasonal variables, which aligns with the seasonal peaks in dengue cases as proven by our hypothesis testing. Additionally, SARIMAX supports the inclusion of other variables that could affect the trend in this case, the proportion of households with sanitation facilities. "
        },
        {
            question: "Limitations of the model",
            answer: "Dengue cases are reported monthly, while sanitation data is only available annually and has to be repeated across months. This limits the model’s sensitivity to short-term changes in sanitation conditions. Furthermore, the coefficient for sanitation proportions was not statistically significant (p = 0.854), indicating that the model did not find strong evidence of a relationship. The presence of high standard errors and a near-singular covariance matrix suggests that multicollinearity or data sparsity may also affect model reliability."
        },
        {
            question: "Discussion of model's results",
            answer: "Based on our model's results, it indicated a reasonable fit for a time series of this scale. However, the coefficient for sanitation proportions was large but not statistically significant, implying that sanitation did not have a meaningful impact on monthly dengue cases. On the other hand, the autoregressive term was significant, suggesting that historical values of dengue cases are a strong predictor of future values."
        },
    ]
</script>

<section id="model" class="bg-bg2">
	<div class="mx-auto sm:px-7 px-4 max-w-screen-xl py-20">
		<div class="flex flex-col md:flex-row items-center">
			<div class="grid gap-12 w-full">
				<div class="flex gap-2 text-lightblue text-4xl md:text-5xl">
					<Icon icon="material-symbols:network-intelligence"  />
						<h2 class="font-bold ">
						<span>Model</span>
					</h2>
				</div>
				<img
					class="w-[80vw] md:w-[70vw] mx-auto block border border-gray-600 rounded shadow-md"
					src={model}
					alt="Model Graph"
					loading="lazy"
				/>
				<div class="flex flex-col gap-8">
                    {#each data as item}
                        <ModelItem question={item.question} answer={item.answer} />
                    {/each}
                </div>
                <div class="flex justify-center">
                    <a
                        href="https://colab.research.google.com/drive/1nzQJ-hFTTm4j6NpwCDZfPCRs00z93Cl1?usp=sharing"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="inline-block hover:opacity-90 text-white font-semibold p-4 self-center justify-center bg-hpa text-center  mx-auto transition-opacity duration-150 ease-in-out rounded-xl"
                    >
                        Try Out our Model
                    </a>
                </div>
			</div>
		</div>
	</div>
</section>
