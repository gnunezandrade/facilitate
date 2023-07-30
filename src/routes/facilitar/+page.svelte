<script lang="ts">
	import Card from '$lib/components/Card.svelte';

	let selected = 0;

	const switchFilter = (index: number) => (selected = index);
</script>

<div class="join w-full flex">
	<button
		class={`btn btn-primary btn-lg join-item grow ${selected != 0 && 'btn-outline'}`}
		on:click={() => switchFilter(0)}>Educação</button
	>
	<button
		class={`btn btn-primary btn-lg join-item grow ${selected != 1 && 'btn-outline'}`}
		on:click={() => switchFilter(1)}>Moradia</button
	>
	<button
		class={`btn btn-primary btn-lg join-item grow ${selected != 2 && 'btn-outline'}`}
		on:click={() => switchFilter(2)}>Saúde</button
	>
	<button
		class={`btn btn-primary btn-lg join-item grow ${selected != 3 && 'btn-outline'}`}
		on:click={() => switchFilter(3)}>Combate à Fome</button
	>
</div>

<Card owner="ong" />
<div class="flex gap-4">
	<Card owner="individual" />
	<Card owner="individual" />
</div>
