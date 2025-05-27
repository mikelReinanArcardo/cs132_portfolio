<script>
	import Icon from "@iconify/svelte";
</script>


<section class="bg-bg2" id="data">
	<div class="mx-auto sm:px-7 px-4 max-w-screen-xl py-20 text-white">
		<div class="mx-auto text-4xl md:text-5xl sm:px-7 px-4 gap-4 max-w-screen-xl pt-6 flex text-lightblue">
			<Icon icon="material-symbols:dataset" />

			<h2 class="font-bold">
				<span>Datasheet</span>
			</h2>
		</div>

		<p class="text-base leading-relaxed py-12 md:text-xl text-center">
			Contained below is the data tracking household sanitation improvements alongside reported
			Contained below is the data tracking household sanitation improvements alongside reported
			Dengue case numbers in Metro Manila, Philippines, between 2019 and 2022. Sourced from PSA and
			DOH reports, this dataset consolidates information intended for analyzing the potential
			relationship between the prevalence of household sanitation facilities and trends in Dengue
			cases
		</p>

		<iframe
			title="Data Repository"
			height="400"
			style="width: 60vw; display: block; margin-left: auto; margin-right: auto; border: 2px solid #00008B;"
			src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR2J-ynz4mHI7fQ9BZAYcAfXpEUoufRYd6qP6--GTFAzYKMfQ-zGLEMze9pA_EZJVtiwWKwGm8zReuc/pubhtml?widget=true&amp;headers=false"
		></iframe>

		<div class="flex justify-center pt-8">
			<a
				href="https://docs.google.com/spreadsheets/d/1pk9NmED7tb6uZbccLIJrMk5TwXZ0mBls82uCE_opgkk/edit?gid=1665090120#gid=1665090120"
				target="_blank"
				rel="noopener noreferrer"
				class="inline-block hover:opacity-90 text-white font-semibold p-4 self-center justify-center bg-hpa text-center mt-4 mx-auto transition-opacity duration-150 ease-in-out rounded-xl"
			>
				See Full Datasheet
			</a>
		</div>
	</div>
</section>
