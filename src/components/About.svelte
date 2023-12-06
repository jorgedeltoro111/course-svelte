<script>
let someText = `Frontend developer at platzi`;
let count = 0;
function handleClick(){
    count += 1;
}
function reset(){
    count = 0;
}
</script>

<style>
    p{
        color: var(--theme-color);
        font-size: 30px;
    }
</style>

<div class="About">
    <p>{someText}</p>
    <p>{count}</p>
    <button on:click={handleClick}>Click</button>
    <button on:click={reset}>Reset</button>
</div>