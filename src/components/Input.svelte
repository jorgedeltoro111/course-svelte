<script>
    import { listen, validate_each_argument } from "svelte/internal";

    export let name = 'World';
</script>
<!--Bind is listening the name value argument and then update-->
<div class='Input'>
    <input type='text' bind:value={name}>
    <p>Hello {name}!</p>
</div>