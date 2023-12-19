<script>
    import style from "../../style.css"
    
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
    

<div class="container-back">
    <div class="btn-back">
        <a class="button-back" href="/">
            <svg xmlns="http://www.w3.org/2000/svg" width="60px" height="60px" viewBox="0 0 24 24" data-name="Layer 1"><path
                d="M20.3284 11.0001V13.0001L7.50011 13.0001L10.7426 16.2426L9.32842 17.6568L3.67157 12L9.32842 6.34314L10.7426 7.75735L7.49988 11.0001L20.3284 11.0001Z"
                fill="white"/></a>
    </div>
</div>


{#if !result}
    
    <div class="show-turn-case" >
        <p class="show-turn">Your Turn:</p>
        <p id="buttons" class="show-turn-font">{turn}</p>
    </div>

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
