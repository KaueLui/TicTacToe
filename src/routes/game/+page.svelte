<script>
    let buttons = new Array(9).fill(null);
    let result = null;
    let turn = 'X';
    const winCombinations = [

    [0,1,2],
    [3,4,5],
    [6,7,8],
    [0,3,6],
    [1,4,7],
    [2,5,8],
    [0,4,8],
    [2,4,2]



    ];

    function setValue(i){
        buttons[i] = turn;
        buttons = [...buttons];
        turn = turn == 'X'?'O' : 'X';

        if(!buttons.includes(null)) {
            result = "Match Draw";

        }else {
            checkWinner();
        }
    }

    function checkWinner() {
        for (let i=0;i<winCombinations.length;i++) {
            if(buttons[winCombinations[i][0]] != null) {
                if(buttons[winCombinations[i][0]] == buttons[winCombinations[i][1]] && buttons[winCombinations[i][1]] == buttons[winCombinations[i][2]]){
                    result = "Winner: " + buttons[winCombinations[i][0]];
                    break;
                }
            }
        }
    }

    function restart(){
       buttons = new Array(9).fill(null);
       result = null;
       turn = 'X';
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
        {result}
        <button on:click={restart}>
            Restart
        </button>

    </div>
{/if}
