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

.text-color{
    margin: auto;
    color: #b60707;
}

.text-exem {
    color: #fff;
    font-family: 'Lexend Deca', sans-serif;
    text-align: center;
    display: flex;
    width: 500px;
    height: 500px;
    margin: auto;
    margin-top: 100px;
}

.projcard-container {
  margin: 50px 0;
}

/* Actual Code: */
.projcard-container,
.projcard-container * {
  box-sizing: border-box;
}
.projcard-container {
  margin-left: auto;
  margin-right: auto;
  width: 1000px;
}

.projcard {
  position: relative;
  width: 100%;
  height: 300px;
  margin-bottom: 40px;
  border-radius: 10px;
  background-color: #fff;
  border: 2px solid #ddd;
  font-size: 18px;
  overflow: hidden;
  cursor: pointer;
  box-shadow: 0 4px 21px -12px rgba(0, 0, 0, .66);
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}

.projcard:hover {
  box-shadow: 0 34px 32px -33px rgba(0, 0, 0, .18);
  transform: translate(0px, -3px);
}
.projcard::before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-image: linear-gradient(-70deg, #424242, transparent 50%);
  opacity: 0.07;
}
.projcard:nth-child(2n)::before {
  background-image: linear-gradient(-250deg, #424242, transparent 50%);
}
.projcard-innerbox {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
.projcard-img {
  position: absolute;
  height: 300px;
  width: 400px;
  top: 0;
  left: 0;
  transition: transform 0.2s ease;
}
.projcard:nth-child(2n) .projcard-img {
  left: initial;
  right: 0;
}
.projcard:hover .projcard-img {
  transform: scale(1.05) rotate(1deg);
}
.projcard:hover .projcard-bar {
  width: 70px;
}
.projcard-textbox {
  position: absolute;
  top: 7%;
  bottom: 7%;
  left: 430px;
  width: calc(100% - 470px);
  font-size: 17px;
}
.projcard:nth-child(2n) .projcard-textbox {
  left: initial;
  right: 430px;
}

.projcard:nth-child(2n) .projcard-textbox::before {
  display: none;
}
.projcard-textbox::after {
  display: none;
  left: initial;
  right: -55px;
}
.projcard:nth-child(2n) .projcard-textbox::after {
  display: block;
}
.projcard-textbox * {
  position: relative;
}
.projcard-title {
  font-family: 'Lexend Deca', sans-serif;
  font-size: 24px;
}
.projcard-subtitle {
  font-family: 'Lexend Deca', sans-serif;
  color: #888;
}
.projcard-bar {
  left: -2px;
  width: 50px;
  height: 5px;
  margin: 10px 0;
  border-radius: 5px;
  background-color: #424242;
  transition: width 0.2s ease;
}
.projcard-blue .projcard-bar { 
    background-color: #ff0000bb; 
}

.projcard-description {
  font-family: 'Lexend Deca', sans-serif;
  z-index: 10;
  font-size: 15px;
  color: #424242;
  height: 125px;
  overflow: hidden;
  text-overflow: ellipsis;
  display: flex;
}
.projcard-tagbox {
  position: absolute;
  bottom: 3%;
  font-size: 14px;
  cursor: default;
  user-select: none;
  pointer-events: none;
}

.projcard-tag {
  display: inline-block;
  background: #E0E0E0;
  color: #777;
  border-radius: 3px 0 0 3px;
  line-height: 26px;
  padding: 0 10px 0 23px;
  position: relative;
  margin-right: 20px;
  cursor: default;
  user-select: none;
  transition: color 0.2s;
}
.projcard-tag::before {
  content: '';
  position: absolute;
  background: #fff;
  border-radius: 10px;
  box-shadow: inset 0 1px rgba(0, 0, 0, 0.25);
  height: 6px;
  left: 10px;
  width: 6px;
  top: 10px;
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

<div class="projcard-container">
    
    <div class="projcard projcard-blue">
      <div class="projcard-innerbox">
        <img class="projcard-img" src="https://static.promediateknologi.id/crop/0x0:0x0/750x500/webp/photo/2022/06/02/1094190019.jpg" />
        <div class="projcard-textbox">
          <div class="projcard-title">About me</div>
          <div class="projcard-subtitle">Take heart. When going get stuff, call for Braum.</div>
          <div class="projcard-bar"></div>
          <div class="projcard-description">Hello! My name is Kauê, I’m 23 years old and I’m from Igarassu, a charming city in Pernambuco, Brazil. Currently, I’m studying Internet Systems at the Federal Institute of Pernambuco (IFPE), where I’m acquiring valuable knowledge that will help me make a difference in the world of technology.</div>
          <div class="projcard-tagbox">
            <span class="projcard-tag">HTML</span>
            <span class="projcard-tag">CSS</span>
          </div>
        </div>
      </div>
    </div>
    
  </div>