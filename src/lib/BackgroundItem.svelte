<script>
	let { value = '', source = '', link = '' } = $props();
</script>

<div>
	<p class="text-white text-sm md:text-xl text-justify">
		{value}
		{#if source}
			<a target="_blank" class="underline text-white text-sm md:text-xl text-justify" href={link}>({source})</a>
		{/if}
	</p>
</div>
