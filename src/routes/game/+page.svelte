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
                    result = buttons[winCombinations[i][0]];
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
        @import url('https://fonts.googleapis.com/css2?family=Nabla&display=swap');

        .btn {
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        justify-content: center;
        align-items: center;
        align-content: stretch;
        padding: 20px;
    }

    .button {
        font-family: 'Lexend Deca', sans-serif;
        background-color: azure;
        display: flex;
        padding: 20px 50px;
        font-size: 35px;
        margin-right: auto;
        margin-left: auto;
        font-weight: bold;
        color: #fff;
        background-color: #ff5252;
        border: 2px solid #000;
        border-radius: 10px;
        box-shadow: 5px 5px 0px #000;
        transition: all 0.3s ease;
    }

    .button:hover {
        background-color: #fff;
        color: #ff5252;
        border: 2px solid #ff5252;
        box-shadow: 5px 5px 0px #ff5252;
    }

    .button:active {
        background-color: #fcf414;
        box-shadow: none;
        transform: translateY(4px);
    }
    
    .tictac {
        width: 500px;
        height: 500px;
        display: grid;
        grid: 200px / auto auto auto;
        margin: auto;
        margin-top: 100px;
    }

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
    }

    .text-game {
        font-family: 'Lexend Deca', sans-serif;
        color: #fff;
        text-align: center;
        
    }

    .text-game-result {
        margin: 0;
        font-family: 'Nabla', sans-serif;
        font-weight: bold;
        font-size: 100px;
        color: #b60707;
        text-align: center;
    }

</style>

<div class="container-back">
    <div class="btn-back">
        <a class="button-back" href="/">
            <svg xmlns="http://www.w3.org/2000/svg" width="60px" height="60px" viewBox="0 0 24 24" data-name="Layer 1"><path
                d="M20.3284 11.0001V13.0001L7.50011 13.0001L10.7426 16.2426L9.32842 17.6568L3.67157 12L9.32842 6.34314L10.7426 7.75735L7.49988 11.0001L20.3284 11.0001Z"
                fill="white"/></a>
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
        <h1 class="text-game">GAME-OVER</h1>
        <h2 class="text-game">The winner of this round was:</h2>
        <h3 class="text-game-result">{result}</h3>
        <button class="button" on:click={restart}>
            Restart
        </button>

    </div>
{/if}
