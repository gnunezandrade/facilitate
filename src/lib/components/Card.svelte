<script lang="ts">
	export let owner: 'ong' | 'individual';
</script>

{#if owner == 'ong'}
	<div class="border border-info rounded-lg flex items-stretch h-[168px]">
		<div class="flex flex-col w-1/2 p-4 justify-between">
			<div class="flex flex-col">
				<div class="badge badge-info">ONG</div>
				<span class="text-lg font-bold">Title</span>
				<span class="font-light">Location</span>
				<span>Description</span>
			</div>
			<button class="btn btn-info">facilitar</button>
		</div>
		<img
			class="w-1/2"
			src="https://blog.iprocess.com.br/wp-content/uploads/2021/11/placeholder.png"
		/>
	</div>
{:else if owner == 'individual'}
	<div class="border border-primary rounded-lg flex flex-col justify-between grow p-4 h-[168px]">
		<div class="flex flex-col">
			<div class="badge badge-primary">INDIVÍDUO</div>
			<span class="text-lg font-bold">Title</span>
			<span class="font-light">Location</span>
			<span>Description</span>
		</div>
		<button class="btn btn-primary">facilitar</button>
	</div>
{/if}
