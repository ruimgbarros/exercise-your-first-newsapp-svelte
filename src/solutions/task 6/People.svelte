<script>
    import Card from './Card.svelte'
    export let data;
</script>


{#each data as person}
    <Card name={person.Name} company={person.company} jobTitle={person.position} />
{/each}


