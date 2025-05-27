<script>
	import arcardo from '$lib/assets/arcardo.jpg';
	import paulo from '$lib/assets/paulo.jpg';
	import mislang from '$lib/assets/mislang.jpg';
	import Icon from "@iconify/svelte";
	import MemberCard from './MemberCard.svelte';

	const teamMembers = [
		{
			id: 1,
			name: 'Mikel Reinan B. Arcardo',
			imgSrc: arcardo,
			description: 'description',
			links: [
				{
					type: 'LinkedIn',
					url: 'https://www.linkedin.com/in/mikel-reinan-arcardo-194680296/?originalSubdomain=ph'
				},
				{ type: 'GitHub', url: 'https://github.com/mikelReinanArcardo' },
				{ type: 'Email', url: 'mikeljuly28@gmail.com' }
			]
		},
		{
			id: 2,
			name: 'Lian Nicoli M. Paulo',
			imgSrc: paulo,
			description: 'description',
			links: [
				{ type: 'GitHub', url: 'https://github.com/lian-nicoli' },
				{ type: 'Email', url: 'lianpaulo27@gmail.com' }
			]
		},
		{
			id: 3,
			name: 'Gabriel M. Mislang',
			imgSrc: mislang,
			description: 'description',
			links: [
				{
					type: 'LinkedIn',
					url: 'https://www.linkedin.com/in/gabrielmislang/'
				},
				{ type: 'GitHub', url: 'https://github.com/meezlung' },
				{ type: 'Email', url: '' }
			]
		}
	];
</script>

<section class="py-16 bg-bg2" aria-labelledby="team-heading" id="team">
	<div class="container mx-auto px-4 md:px-6">
		<div class="mx-auto text-4xl md:text-5xl sm:px-7 px-4 gap-4 max-w-screen-xl flex text-lightblue">
			<Icon icon="material-symbols:groups-rounded" />
			<h2 class="font-bold">
				<span>Meet The Team</span>
			</h2>
		</div>

		<div class="flex flex-col md:flex-row gap-2 md:gap-8 pt-8">
			{#each teamMembers as member (member.id)}
				<MemberCard name={member.name} imgSrc={member.imgSrc} description={member.description} links={member.links} />
			{/each}
		</div>
	</div>
</section>

<style>
	.container {
		max-width: 1280px;
	}
</style>
