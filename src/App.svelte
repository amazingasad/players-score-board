<script>
    import Nav from "./Nav.svelte";
    import Players from "./Players.svelte";
    let players = [
        {
            name : "Siam Hossen",
            points : 69
        },
        {
            name : "Ismail Chowdhury",
            points : 6969
        },
        {
            name : "Mokarrom Also",
            points : 169
        }
    ];
</script>
<Nav/>
<div class="container">
    {#each players as player}
    <Players name={player.name} points={player.points} />
    {/each}
</div>