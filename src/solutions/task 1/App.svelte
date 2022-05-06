<script>
	import Tasks from "./Tasks.svelte";
	import { csv } from "d3-fetch";
	import Loader from "./Loader.svelte";


	// To make our life easier, I've already imported the data. 
	// First we say that data is null
	let data = null;
	// Then we fetch the data (as res) and assign it to data
	csv("data.csv").then((res) => {
  		data = res;
	});


</script>

<main>

	<Loader />

	<!-- Just a simple tasks component with everything we will be doing -->
	<Tasks />
	
</main>

