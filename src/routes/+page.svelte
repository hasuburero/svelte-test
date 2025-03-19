<script lang="ts">
	type Item = {
		name: string;
	};

	let withList: Item[] = [{ name: 'Apple' }, { name: 'Orange' }];
</script>

<section>
	<div>
		<h1>✅ With List</h1>
		<div>
			<input type="text" />
			<button>Add Item</button>
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
</section>
