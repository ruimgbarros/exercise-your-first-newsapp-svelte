<script>
    import Card from './Card.svelte'
    import { fly } from 'svelte/transition'
    export let data;
</script>


<div class="container mx-auto px-2">
    <div class="mt-10">
		<h2 class="text-3xl mb-8">Get to know the people of interest</h2>
        <div class="grid grid-cols-6 gap-2">
            {#each data as person, i}
                <div in:fly="{{ y: 200, duration: 1000, delay: 100 * i }}">
                    <Card name={person.Name} company={person.company} jobTitle={person.position} />
                </div>
            {/each}
        </div>
	</div>
</div>

