<script>
    import { onMount } from "svelte";

    let photos = [];

    onMount(async()=>{
        console.log('onMount');
        const response = await fetch('https://fakestoreapi.com/products')
        photos = await response.json();
    });
</script>
<style>
    .photo{
        height: 250px;
        width: 250px;
    }
</style>
<div class="Photos">
    {#each photos as photo}
        <figure>
            <img class="photo" src={photo.image} alt={photo.title}>
            <figcaption>{photo.category}</figcaption>
        </figure>
    {:else}
        <p>Loading . . .</p>
    {/each}
</div>


