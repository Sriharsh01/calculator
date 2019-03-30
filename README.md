
<html>
<head>
    <title>Calculator</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<style>
@import url('https://fonts.googleapis.com/css?family=Rochester');
@import url('https://fonts.googleapis.com/css?family=Permanent+Marker');
@import url('https://fonts.googleapis.com/css?family=Charm');
@import url('https://fonts.googleapis.com/css?family=Oswald');
body{
    margin: 0;
    padding: 0;
    background-color: rgb(230, 255, 255);
}
header{
    margin: 5px 10px 0 10px;
}
/*header h5{
    display: inline-block;
    padding: 0;
    margin: 0;
    font-size: 18px;
    font-weight: bold;
    letter-spacing: 15px;
    color: rgb(31, 184, 119);
    font-family: 'Permanent Marker',sans-serif;
}*/
header div{
    display: inline;
}
header div span:nth-child(1){
    display: inline-block;
    overflow: hidden;
    content: '';
    width: 15px;
    height: 15px;
    border-radius: 50%;
    margin-top: 10px;
    background-color: #fd544d;
}
header div span:nth-child(2){
    display: inline-block;
    overflow: hidden;
    content: '';
    width: 15px;
    height: 15px;
    border-radius: 50%;
    margin-top: 10px;
    background-color: #ffc02f;
}
header div span:nth-child(3){
    display: inline-block;
    overflow: hidden;
    content: '';
    width: 15px;
    height: 15px;
    border-radius: 50%;
    margin-top: 10px;
    background-color: #28ca40;
}
header label{
    float: right;
    margin-top: 3px;
}
.switch {
  position: relative;
  display: inline-block;
  width: 50px;
  height: 24px;
}
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #aaa;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 16px;
  width: 16px;
  left: 4px;
  bottom: 4px;
  background-color: red;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked + .slider {
    background-color: rgb(31, 184, 119);
}

input:focus + .slider {
  box-shadow: 0 0 1px #2196F3;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}

other form radius.harsh
.container form input{
    width: 100%;
    height: 100px;
    border: 0;
    outline: 0;
    pointer-events: none;
    background-color: transparent;
    text-align: right;
    font-size: 55px;
    color: #252525;
    overflow-x: auto;
    box-sizing: border-box;
    padding: 0 10px 0 0;
}
.btn{
    position: relative;
    display: grid;
    background-color: white;
    padding: 10px;
    box-sizing: border-box;
    grid-template-columns: repeat(4, auto);
    grid-template-rows: repeat(5, auto);
    grid-row-gap: 15px;
    margin-top: 10px;
}
.btn-num{
    display: inline-block;
    font-family: 'Oswald', sans-serif;
    text-align: center;
    padding: 5px 0 0 0;
    color: #252525;
    border-radius: 50%;
    font-size: 40px;
    box-sizing: border-box;
    width: 72px;
    height: 72px;
    transition: all 0.3s ease;
}
.btn-clr{
    display: inline-block;
    font-family: 'Oswald', sans-serif;
    text-align: center;
    padding: 5px 0 0 0;
    color: #252525;
    border-radius: 50%;
    font-size: 40px;
    box-sizing: border-box;
    width: 72px;
    height: 72px;
    background-color: rgb(230, 255, 255);
    transition: all 0.3s ease;
}
.btn-clr1{
    display: inline-block;
    font-family: 'Oswald', sans-serif;
    text-align: center;
    padding: 5px 0 0 0;
    border-radius: 50%;
    color: white;
    font-size: 40px;
    box-sizing: border-box;
    color: #fff;
    width: 72px;
    height: 72px;
    background-color: rgb(16, 158, 124);
    transition: all 0.3s ease;
}
.btn-num:hover, .btn-clr:hover, .btn-clr1:hover{
    box-shadow: 0 0 10px rgb(16, 158, 124);
}
footer{
    position: relative;
    width: 100%;
    height: 55px;
    background-color: white;
    color: #252525;
    font-family: 'Rochester', sans-serif;
    font-weight: 900;
    text-align: right;
    padding: 20px 10px 0 0 ;
    box-sizing: border-box;
    font-size: 18px;
    letter-spacing: 1px;
}
</style>
<body>
    <header>
        <div>
            <span></span>
            <span></span>
            <span></span>
        </div>
        <label class="switch">
            <input type="checkbox" id="toggle" onchange="toggles(this)">
            <span class="slider round"></span>
        </label>
    </header>

    <div class="container">
        <form>
            <input type="text" name="text" id="output">
        </form>
        <div class="btn">
            <div class="btn-clr" onclick="clr()">AC</div>
            <div class="btn-clr" onclick="back()">C</div>
            <div class="btn-clr" onclick="inp('%')">%</div>
            <div class="btn-clr" onclick="inp('/')">/</div>

            <div class="btn-num" onclick="inp('7')">7</div>
            <div class="btn-num" onclick="inp('8')">8</div>
            <div class="btn-num" onclick="inp('9')">9</div>
            <div class="btn-clr" onclick="inp('*')">X</div>

            <div class="btn-num" onclick="inp('4')">4</div>
            <div class="btn-num" onclick="inp('5')">5</div>
            <div class="btn-num" onclick="inp('6')">6</div>
            <div class="btn-clr" onclick="inp('-')">-</div>

            <div class="btn-num" onclick="inp('1')">1</div>
            <div class="btn-num" onclick="inp('2')">2</div>
            <div class="btn-num" onclick="inp('3')">3</div>
            <div class="btn-clr" onclick="inp('+')">+</div>

            <div class="btn-num" onclick="inp('0')">0</div>
            <div class="btn-num" onclick="inp('.')">.</div>
            <span><!--Empty Block--></span>
            <div class="btn-clr1" onclick="result()">=</div>
        </div>
    </div>
    <footer><span>Design & Developed By: Sriharsh</span></footer>


</body>
<script>
alert("Enable Dark Mode From Top Right Toggle Button \n Give me Suggestion Also if you want");
function toggles(id){
    if (id.checked) {
        document.querySelector("body").style.backgroundColor = "#212b41";
        document.querySelector(".btn").style.backgroundColor = "#2e3951";
        document.querySelector("#output").style.color = "#18d4a3";
        document.querySelector(".btn-clr1").style.color = "#212b41";
        var btn_clr = document.querySelectorAll(".btn-clr");
        for(var i=0; i<btn_clr.length; i++){
            btn_clr[i].style.color = "#18d4a3";
            btn_clr[i].style.backgroundColor = "#212b41";
        }

        var btn_num = document.querySelectorAll(".btn-num");
        for(var i=0; i<btn_num.length; i++){
            btn_num[i].style.color = "#869794";
        }

        document.querySelector("footer").style.color = "#869794";
        document.querySelector("footer").style.backgroundColor = "#2e3951";
    }
    else{

        document.querySelector("body").style.backgroundColor = "#e6ffff";
        document.querySelector(".btn").style.backgroundColor = "#fff";
        document.querySelector("#output").style.color = "#252525";
        document.querySelector(".btn-clr1").style.color = "#fff";
        var btn_clr = document.querySelectorAll(".btn-clr");
        for(var i=0; i<btn_clr.length; i++){
            btn_clr[i].style.color = "#252525";
            btn_clr[i].style.backgroundColor = "#e6ffff";
        }

        var btn_num = document.querySelectorAll(".btn-num");
        for(var i=0; i<btn_num.length; i++){
            btn_num[i].style.color = "#252525";
        }

        document.querySelector("footer").style.color = "#252525";
        document.querySelector("footer").style.backgroundColor = "#fff";
    }
}

function inp(val){
    var output = document.querySelector("#output");
    output.value -=val;
}
function clr(){
    document.querySelector("#output").value = "";
}
function result(){
    var output = document.querySelector("#output");
    if(output.value=="")
    {
        output.value= "No Output";
    }
    else
    {
        var result = eval(output.value);
        output.value = result;
    }

}
function back(){
    var output = document.querySelector("#output");
    var number = output.value;
    var len = number.length - 1;
    var newNumber = number.substring( 0, len );
    output.value = newNumber;
}
</script>
</html>
