# Project-2
<!DOCTYPE html>
<html>
<head>
<title>Basic Calculator</title>
<!--internal CSS-->
<style>
    *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-weight: bold;
}
#container{
      background: url('https://images.unsplash.com/photo-1503264116251-35a269479413?fit=crop&w=1000&q=80') no-repeat center center fixed;
     background-size: cover;
}

#calculator {
         background: rgba(255, 255, 255, 0.1);
         backdrop-filter: blur(10px);
         box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
         border-radius: 15px;
         padding: 20px; 
         display: flex;
         flex-direction: column;            
         align-items: center;    
}

#container{
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
input{
    width: 300px;
    padding: 40px;
    background: transparent;
    border: 1px solid transparent;
    border-radius: 10px;
    text-align: right;
    margin-bottom: 10px;
    font-size: 40px;
    color: greenyellow;
    box-shadow: rgb(204, 219, 232) 3px 3px 6px 0px inset, rgba(255, 255, 255, 0.5) -3px -3px 6px 1px inset;
}
input::placeholder{
    color: greenyellow;
    font-size: 40px;
}
button {
    background: whitesmoke;
    color: black;
    width: 60px;
    height:60px;
    margin: 5px;
    font-size: 24px;
    border: none;
    border-radius: 50%;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.17) 0px -23px 25px 0px inset, rgba(0, 0, 0, 0.15) 0px -36px 30px 0px inset, rgba(0, 0, 0, 0.1) 0px -79px 40px 0px inset, rgba(0, 0, 0, 0.06) 0px 2px 1px, rgba(0, 0, 0, 0.09) 0px 4px 2px, rgba(0, 0, 0, 0.09) 0px 8px 4px, rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
}
button:hover{
    color: black;
    background: gainsboro;
    box-shadow: rgb(204, 219, 232) 3px 5px 6px 0px inset, rgba(255, 255, 255, 0.5) -3px -3px 6px 1px inset;
}
</style>
</head>
<body>

<div id="container">
    <div id="calculator">
        <input id="inputBox" type="text" placeholder="0">
        <div>
            <button class="ac-but" onclick="ac()">AC</button>
            <button class="del-but" onclick="del()">DEL</button>
            <button class="percent-but" onclick="math(event)">%</button>
            <button class="divide-but" onclick="math(event)">/</button>
        </div>
        <div>
            <button onclick="allBut(event)">7</button>
            <button onclick="allBut(event)">8</button>
            <button onclick="allBut(event)">9</button>
            <button class="multiply-but" onclick="math(event)">*</button>
        </div>
        <div>
            <button onclick="allBut(event)">4</button>
            <button onclick="allBut(event)">5</button>
            <button onclick="allBut(event)">6</button>
            <button class="subtract-but" onclick="math(event)">-</button>
        </div>
        <div>
            <button onclick="allBut(event)">1</button>
            <button onclick="allBut(event)">2</button>
            <button onclick="allBut(event)">3</button>
            <button class="add-but" onclick="math(event)">+</button>
        </div>
        <div>
            <button class="dubal0-but" onclick="allBut(event)">00</button>
            <button onclick="allBut(event)">0</button>
            <button class="dot-but" onclick="math(event)">.</button>
            <button class="eqal-but" onclick="eqal()">=</button>
        </div>
    </div>
</div>

<!--JavaScript(Internal)-->
<script>
    let display = document.getElementById(`inputBox`)
let button = ''
let calBut =''
function  ac() {
  display.value = ''
}
function del() {
  display.value = display.value.slice(0,-1);
}
function allBut(event) { 
   button = event.target.innerHTML;
   display.value += button;
}
function math(event) {
  calBut = event.target.innerHTML;
  display.value += calBut;
}
function eqal() {
   let x = display.value;
   x = eval(x);
   display.value = x;
}
</script>
</body>
</html>
