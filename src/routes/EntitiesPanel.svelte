<script lang="ts">
	import { data } from "$lib";

	let query = $state("");

	const filter = $derived(
		Object.values(data)
			.filter((company) => company.name.toLowerCase().includes(query.toLowerCase().trim()))
			.sort((a, b) => a.name.localeCompare(b.name)),
	);
</script>

<div class="mx-auto mt-4 max-w-screen-md">
	<input
		type="text"
		bind:value={query}
		placeholder="Search for a company or entity..."
		aria-controls="entities"
		class="w-full rounded-none border-2 border-gray-300 p-2 focus:border-transparent focus:outline-none focus:ring-2 focus:ring-blue-500 md:rounded-md dark:border-gray-700 dark:bg-gray-800 dark:text-white dark:placeholder-gray-400"
	/>

	<div
		id="entities"
		class="mt-0 grid grid-cols-1 md:mt-4 md:grid-cols-2 md:gap-4"
		aria-live="polite"
		aria-atomic="true"
	>
		{#each filter as company}
			<div
				class="not-md:max-w-md flex gap-4 rounded-none bg-gray-100 p-2 drop-shadow-lg md:rounded-md dark:bg-gray-900"
			>
				<img
					draggable="false"
					src={company.iconUrl}
					alt={company.name}
					class="mx-auto h-20 w-20 flex-col rounded-md"
				/>
				<div class="select-none flex-col">
					<p class="text-lg font-bold">{company.name}</p>
					<p class="mt-2 text-sm">{company.description}</p>
					<p>
						<a
							href={company.referenceUrl}
							target="_blank"
							rel="noopener noreferrer"
							class="my-2 inline-block rounded-md border border-gray-700 p-2 dark:border-gray-300"
						>
							View Article
						</a>
					</p>
				</div>
			</div>
		{/each}
	</div>
</div>
