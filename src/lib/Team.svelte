<script>
	import arcardo from '$lib/assets/arcardo.jpg';
	import paulo from '$lib/assets/paulo.jpg';
	import mislang from '$lib/assets/mislang.jpg';

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

<section class="py-16" aria-labelledby="team-heading" id="team">
	<div class="container mx-auto px-4 md:px-6">
		<h2 id="team-heading" class="text-3xl md:text-4xl font-bold text-center text-gray-800 mb-12">
			Meet The Team
		</h2>

		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
			{#each teamMembers as member (member.id)}
				<div
					class="bg-white rounded-lg shadow-lg overflow-hidden border border-gray-100 flex flex-col"
				>
					<img
						class="w-full h-90 object-cover object-center"
						src={member.imgSrc}
						alt={member.name}
						loading="lazy"
					/>
					<div class="p-6 flex flex-col flex-grow">
						<h3 class="text-2xl font-semibold mb-2 text-gray-900">
							{member.name}
						</h3>
						<p class="text-gray-600 text-base mb-4 flex-grow">
							{member.description}
						</p>
						<div class="mt-auto pt-4 border-t border-gray-200">
							<div class="flex items-center space-x-4">
								{#each member.links as link (link.type)}
									{#if link.type !== 'Email'}
										<a
											href={link.url}
											target="_blank"
											rel="noopener noreferrer"
											class="text-blue-600 hover:text-blue-800 hover:underline text-sm font-medium transition duration-150 ease-in-out"
											aria-label="{member.name}'s {link.type}"
										>
											{link.type === 'Email' ? 'Email: ' + link.url : link.type}
										</a>
									{:else}
										<p>
											{link.type === 'Email' ? 'Email: ' + link.url : link.type}
										</p>
									{/if}
								{/each}
							</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	/* Add any component-specific styles here if needed,
     though Tailwind is used for most styling. */
	.container {
		max-width: 1280px; /* Optional: You might have this defined globally */
	}
</style>
