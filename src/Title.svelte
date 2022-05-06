<script>
    export let Title = "People of interest"
    export let AuthorName;
    export let AuthorUrl;
    export let updateDate;
    export let openingText = "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis vitae quaerat quidem officiis provident ut, possimus odit, dignissimos aspernatur fugiat quibusdam dolorum consequatur laudantium. Blanditiis totam a aliquam dolores impedit!"
</script>

<div class="container mx-auto px-2">
    <h1 id='firstIcon'>👤</h1>
    <h1 class="font-sans text-7xl -mt-8">{Title}</h1>
    <p class="mt-2 tex-xs opacity-50"><a href="{AuthorUrl}" target="_blank" class="hover:underline" >{AuthorName} </a> - updated in {updateDate}.</p>
    <h3 class="mt-2 max-w-6xl text-xl opacity-70">{openingText}</h3>
</div>

<style>
	#firstIcon {
		font-size: 7rem;
	}
</style>