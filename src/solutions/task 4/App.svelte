<script>
	import Tasks from "./Tasks.svelte";
	import { csv } from "d3-fetch";
	import Loader from "./Loader.svelte";
	import { fade } from "svelte/transition";

	import Title from "./Title.svelte";


	// To make our life easier, I've already imported the data. 
	// First we say that data is null
	let data = null;
	// Then we fetch the data (as res) and assign it to data
	csv("data.csv").then((res) => {
  		data = res;
	});


</script>

<main>

	{#if data}
		<div in:fade>
			<Title
				Title="People of interest" 
		 		AuthorName='Rui Barros' 
				AuthorUrl='https://twitter.com/rui_barros17' 
				updateDate={ new Date().toLocaleDateString() } 
				openingText='Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis vitae quaerat quidem officiis provident ut, possimus odit, dignissimos aspernatur fugiat quibusdam dolorum consequatur laudantium. Blanditiis totam a aliquam dolores impedit!'
			/>
			<Tasks />
		</div>
	{:else}
		<Loader />
	{/if}

</main>

