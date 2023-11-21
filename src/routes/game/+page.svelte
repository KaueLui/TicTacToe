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
    [2,4,6]



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
        width: 500px;
        height: 500px;
        display: grid;
        grid: 200px / auto auto auto;
        margin: auto;
        margin-top: 100px;
        
    }

    /* .tictac button {
        width: 100px;
        height: 100px;
        margin: 0;
        
    } */

    .tictac button {

        width: 200px;
        height: 200px; 
        margin: 0;
        display: inline-block;
        padding: 10px 20px;
        font-size: 50px;
        font-weight: bold;
        text-align: center;
        text-decoration: none;
        color: #fff;
        background-color: #ff5252;
        border: 2px solid #000;
        border-radius: 10px;
        box-shadow: 5px 5px 0px #000;
        transition: all 0.3s ease;
    }

    .tictac button:active {

        background-color: #fcf414;
        box-shadow: none;
        transform: translateY(4px);
        
    }

    .btn-back {
        padding: 20px;
        background-image: ("https://fonts.googleapis.com/icon?family=arrow_back");
    }

</style>

<div class="container-back">
    <div class="btn-back">
        <a class="button-back" href="/">BACK</a>
    </div>
</div>


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
