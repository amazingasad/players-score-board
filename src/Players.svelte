<script>
    export let name;
    export let points;
    
    let toggleControl = false;
    const toggle = () => toggleControl = !toggleControl;
    const addPoint = () => points = points + 1;
    const removePoint = () => points = points - 1;
</script>
<div class="card">
    <h1>Name : {name} 
        <button on:click="{toggle}">
            {#if toggleControl}- {:else}+{/if}
        </button>
    </h1>
    <h3>Points : {points}</h3>
    {#if toggleControl}
    <button class="plus-btn" on:click="{addPoint}">+</button>
    <button class="minus-btn" on:click="{removePoint}">-</button>
    <input type="number" bind:value="{points}">
    {/if}
</div>

<style>
    .card{
        border: 1px solid black;
        background: #fcf9f9;
        width: 80%;
        padding: .7rem;
        margin:1rem auto;
    }
    button{
        height: 2rem;
        width:3rem;
        border: none;
        cursor: pointer;
        margin: 1rem;
    }
    .plus-btn{
        background: black;
        color: white;
    }
    .minus-btn{
        background: rgba(161, 161, 161, 0.411);
    }
</style>