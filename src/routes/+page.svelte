<style>
@import url('https://fonts.googleapis.com/css2?family=Londrina+Solid&family=Vina+Sans&display=swap');

:global(html){
    margin: 0;
    padding: 0;
    border-radius: 0;
    background-color: aquamarine;
}

.tittle {
    font-family: 'Vina Sans', sans-serif;
    font-size: 100px;
    text-align: center;
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
    font-family: 'Vina Sans', sans-serif;
    background-color: azure;
}

</style>


<div class="container">
    <div>
        <h1 class="tittle">TIC-TAC-TOE</h1>
    </div>

    <div class="btn">
        <a class="button" href="../game">PLAY</a>
        <a class="button" href="/">HELP</a>

    </div>
</div>









<!-- <h1>Welcome to SvelteKit</h1>
<p>Visit <a href="../game">kit.svelte.dev</a> to read the documentation</p> -->
