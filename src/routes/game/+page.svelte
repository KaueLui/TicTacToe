<script>
    let buttons = new Array(9).fill(null);
    let result = null;
    let turn = 'X';

    function setValue(i){
        buttons[i] = turn;
        buttons = [...buttons];
        turn = turn == 'X'?'O' : 'X';
    }
</script>
    
<style>
    .tictac {
        width: 300px;
        height: 300px;
        display: flex;
        flex-wrap: wrap;
    }

    .tictac button {
        width: 100px;
        height: 100px;
        margin: 0;
    }
</style>


{#if !result}
    <div class="tictac">
        {#each buttons as button,i}
        <button on:click={( )=>{setValue(i)}}>
            {button?button:""}
        </button>
        {/each}

    </div>

    {:else}

    <div>


    </div>
{/if}
