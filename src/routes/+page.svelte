<script lang="ts">
	interface Item {
		name: string;
	}

	let withList: Item[] = [{ name: 'Apple' }, { name: 'Orange' }];

	let adding_item: Item = { name: '' };
	function AddItem() {
		if (adding_item.name === 'Svelte') {
			console.log('This is Svelte');
		} else if (adding_item.name == 'Hello') {
			console.log('Hello World!!');
		} else {
			console.log('other');
		}
		withList.push(adding_item);
		console.log(withList);
		adding_item.name = '';
	}
</script>

<main>
	<div>
		<h1>✅ With List</h1>
		<p>
			Visit the <a href="http://www.dlab.ise.shibaura-it.ac.jp/nextcloud">NextCloud</a> !!
		</p>
		<div>
			<input bind:value={adding_item.name} type="text" />
			<button on:click={AddItem}>Add Item</button>
		</div>
		<ul>
			{#each withList as item}
				<li>
					<p><span>✔</span><span>{item.name}</span></p>
					<button>🗑️</button>
				</li>
			{/each}
		</ul>
	</div>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
