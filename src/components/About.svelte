<script>
    let someText = `Frontend developer at platzi`;
    let count = 0;
    let styles = { darkMode: false};

    function handleClick(){
        count += 1;
    }

    function reset(){
        count = 0;
    }

    function toggle(){
        styles.darkMode = !styles.darkMode;
        window.document.body.classList.toggle("dark-mode");
    }
</script>

<style>
    p{
        color: var(--theme-color);
        font-size: 30px;
    }
</style>

<div class="About">
    <!--Using conditionals-->
    {#if !styles.darkMode}
        <p>{someText}</p>
    {:else }
        <p>
            <span>Hello dark mode</span>
        </p>
    {/if}
    <p>{count}</p>
    <button on:click={handleClick}>Click</button>
    <button on:click={reset}>Reset</button>
    <button on:click={toggle}>Dark Mode</button>
</div>