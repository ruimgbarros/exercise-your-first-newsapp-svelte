<script>
	
    let todoList = [

			{text: 'Import the Loader component to App.svelte before the Tasks component', status: false},
			{text: 'Make the Loader only show up while data is not yet imported. If data is imported, show the Tasks', status: false},
			{text: 'Make sure Tasks (or anything else you will be importing) is faded in into the page', status: false},
			{text: 'Import Title component. Figure out what does it needs and "feed" that component with the necessary props', status: false},
			{text: 'Make a new component called People. Pass all the data as a prop inside of it. Import it to app.svelte', status: false},
			{text: 'Make a card for every single person in the database (hint: you can use the Card component already created)', status: false},
			{text: 'Make cards show up side by side with css (or simply wrap all your cards with a div with "class="grid grid-cols-6 gap-2")', status: false},
			{text: 'Extra: Can you make every single card slowly enter the page?")', status: false},
			{text: 'Extra: Can you name an input menu that filters the cards by organization?")', status: false},

		];
	

</script>


<div class="mt-10 max-w-2xl mx-auto py-10 px-8 bg-emerald-300 mb-40">
	<h2 class="text-4xl mb-4">My Tasks</h2>
	{#each todoList as item, index}
	<div class="mb-4">
				<input bind:checked={item.status} type="checkbox">
			<span class:checked={item.status}>{item.text}</span>
	</div>
	{/each} 
</div>


<style> 
	.checked {
        text-decoration: line-through;
    }
</style> 


