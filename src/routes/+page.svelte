<style>
@import url('https://fonts.googleapis.com/css2?family=Londrina+Solid&family=Vina+Sans&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Lexend+Deca&display=swap');

:global(html){
    margin: 0;
    padding: 0;
    border-radius: 0;
    background-color: #141414;
}

.tittle {
    font-family: 'Lexend Deca', sans-serif;
    font-size: 100px;
    text-align: center;
    color: white;
}

.btn{
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
    display: inline-block;
    padding: 20px 50px;
    font-size: 35px;
    margin: 10px;
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

.button-ab {
    font-family: 'Lexend Deca', sans-serif;
    background-color: azure;
    display: inline-block;
    padding: 20px 35px;
    font-size: 35px;
    margin: 10px;
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

.button-ab:hover {
    background-color: #fff;
    color: #ff5252;
    border: 2px solid #ff5252;
    box-shadow: 5px 5px 0px #ff5252;
}

.button-ab:active {
    background-color: #fcf414;
    box-shadow: none;
    transform: translateY(4px);
}

</style>


<div class="container">
    <div>
        <h1 class="tittle">TIC-TAC-TOE</h1>
    </div>

    <div class="btn">
        <a class="button" href="../game">PLAY</a>
        <a class="button" href="../help">HELP</a>
        <a class="button-ab" href="../about">ABOUT</a>

    </div>
</div>s