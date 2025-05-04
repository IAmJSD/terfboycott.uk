<script lang="ts">
	import EntitiesPanel from "./EntitiesPanel.svelte";
</script>

<svelte:head>
	<title>UK TERF Entities Boycott List</title>
	<meta
		name="description"
		content="A list of entities that support TERFs and the transphobic movement. Since the Supreme Court ruling, a number of entities have taken to supporting the transphobic judgement and guidance. This is the list of entities that have done so."
	/>
	<meta property="og:title" content="UK TERF Entities Boycott List" />
	<meta
		property="og:description"
		content="A list of entities that support TERFs and the transphobic movement. Since the Supreme Court ruling, a number of entities have taken to supporting the transphobic judgement and guidance. This is the list of entities that have done so."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:site_name" content="UK TERF Entities Boycott List" />
</svelte:head>

<main>
	<div
		class="w-full bg-gradient-to-b from-blue-300 to-pink-300 p-5 dark:from-blue-900 dark:to-pink-900"
	>
		<h1 class="text-center text-4xl font-bold">UK TERF Entities Boycott List</h1>
		<p class="mx-auto mt-2 max-w-screen-md text-center text-lg">
			A list of entities that support TERFs and the transphobic movement. Since the <a
				class="underline"
				href="https://www.theguardian.com/society/2025/apr/16/critics-of-trans-rights-win-uk-supreme-court-case-over-definition-of-woman"
				target="_blank"
				rel="noopener noreferrer"
			>
				Supreme Court ruling
			</a>, a number of entities have taken to supporting the transphobic judgement and guidance.
			This is the list of entities that have done so.
		</p>
		<a
			href="https://docs.google.com/forms/d/e/1FAIpQLScuMDsNI11BLj0YXnTY_gt0q2aM8zFQuSit7GETe_T11IyE6Q/viewform?usp=dialog"
			class="mt-2 block text-center text-lg underline"
			target="_blank"
			rel="noopener noreferrer"
		>
			Add a company to the list
		</a>
	</div>

	<EntitiesPanel />
</main>
