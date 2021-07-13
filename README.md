# CoffeeMachine
project of Coffee Machine alived with js
<!DOCTYPE html>
<html lang="ru" dir="ltr">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-+0n0xVW2eSR5OomGNYDnhzAbDsOXxcvSN1TPprVMTNDbiYZCxYbOOl7+AMvyTG2x" crossorigin="anonymous">
    
    <link rel="stylesheet" href="Final_style.css">

    <title>Coffee Machine</title>

    <style>
      @import url('https://fonts.googleapis.com/css2?family=Lobster&family=Mali:wght@200&family=Marck+Script&family=Pacifico&display=swap');
      @import url('https://fonts.googleapis.com/css2?family=Kosugi+Maru&display=swap');
      
      .backgroundField {
  margin: auto;
  margin-top: 40px;
  background: rgba(0,0,0,0.5);
  width: 80%;
  height: 650px;
  position: relative;
  border: solid 1px black;
  border-radius: 10px;
  box-shadow: 0 5px 20px black;
}

h2 {
  text-align: center;
  font-family: 'Lobster', cursive;
  color: Snow;
  text-shadow: 1px 1px 2px black;
  font-size: 50px;
  margin-bottom: 5px;
}

.leftPart {
  text-align: center;
  width: 50%;
  padding: 5px;
}

.coffee_name {
  width: 80%;
  height: 57px;
  background: rgb(222, 184, 135, 0.3);
  border: solid 2px #696969;
  display: inline-block;
  color: Snow;
  box-shadow: inset 0 0 5px Snow;
  font-family: 'Pacifico', cursive;
  font-size: 30px;
}

.choice {
  width: 60px;
  height: 60px;
  border-radius: 30px;
  border: solid 5px rgba(222, 184, 135);
  position: relative;
  top: -5px;
  right: 30px;
  cursor: pointer;
}
.choice:hover {
  background-color: rgba(222, 184, 135, .8);
  border: solid 1px Silver;
  box-shadow: 0 0 5px DarkGray;
}

.centralPart{
  width: 30%;
  margin: 0;
  padding: 0;
}
#cup{
  position: absolute;
  top: 175px;
  left: 50%;
  padding: 0;
  border-radius: 175px;
  cursor: pointer;
}
#cup:hover{
  filter: contrast(150%);
}
#coffeeReady{
  position: absolute;
  top: 415px;
  left: 55%;
  text-align: center;
  color: Seashell;
  font-size: 20px;
  font-family: 'Pacifico', cursive;
}

.rightPart {
  position: absolute;
  width: 20%;
  top: 5px;
  right: 10px;

}
.menu {
  position: absolute;
  padding-left: 5%;
  padding-top: 5px;
  left: auto;
  right: auto;
  text-align: left;
  color: Seashell;
  width: 200px;
  height: 160px;
  background: rgb(222, 184, 135, 0.6);
  border: solid 3px #696969;
  box-shadow: inset 0 0 5px Snow;
  font-size: 20px;
  font-family: 'Kosugi Maru', sans-serif;
}
#progress{
  width: 90%;
  margin-left: 3%;

}
#progressBar{

}

.bill_acc {
  position: absolute;
  top: 175px;
  left: auto;
  right: auto;
}

#drop-off-button {
  width: 200px;
  height: 40px;
  border: double 3px rgb(105, 105, 105);
  border-radius: 10px;
  margin: 5px;
  font-weight: bold;
}
#drop-off-button:hover {
  background-color: Silver;
  box-shadow: 0 0 3px black;
}

#moneyField {
  position: relative;
  top: 460px;
  left: auto;
  right: auto;
  color: Seashell;
  width: 200px;
  height: 160px;
  background: rgb(222, 184, 135, 0.6);
  border: solid 3px #696969;
  box-shadow: inset 0 0 5px Snow;
}

.money {
  position: absolute;
  top: 600px;
  bottom: 5px;
  left: 10px;
  cursor: pointer;
}

.money.half {
  left: 200px;
}
.money.one {
  left: 100px;
}
[src$="rub.png"]{
  width: 50px;
  position: absolute;
  cursor: pointer;
}
[src$="rub.png"]:hover{
  filter: contrast(150%);
}

      
    </style>

    

    <script src="https://kit.fontawesome.com/639fd8898f.js" crossorigin="anonymous"></script>
  </head>
  <body background="coffee_1.jpg">
      <div class="backgroundField">
        

        <div class="leftPart">
          <h2>Coffee time</h2>
          <div class="coffee_name">Капучино - 58</div>
          <button type="button" class="choice" onclick="getCoffee('Капучино', 58)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
          <div class="coffee_name">Латте - 61</div>
          <button type="button" class="choice" onclick="getCoffee('Латте', 61)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
          <div class="coffee_name">Эспрессо - 47</div>
          <button type="button" class="choice" onclick="getCoffee('Эспрессо', 47)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
          <div class="coffee_name">Американо - 42</div>
          <button type="button" class="choice" onclick="getCoffee('Американо', 42)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
          <div class="coffee_name">Лунго - 44</div>
          <button type="button" class="choice" onclick="getCoffee('Лунго', 44)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
          <div class="coffee_name">Флэт-уайт - 55</div>
          <button type="button" class="choice" onclick="getCoffee('Флэт-уайт', 55)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
          <div class="coffee_name">Глиссе - 71</div>
          <button type="button" class="choice" onclick="getCoffee('Глиссе', 71)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
          <div class="coffee_name">Раф - 84</div>
          <button type="button" class="choice" onclick="getCoffee('Раф', 84)">
            <i class="fas fa-mug-hot fa-lg"></i>
          </button>
        </div>


        <div class="centralPart" id="centralPart" hidden>
          <img id="cup" src="cup_circle.jpg" onclick="newSession()">
          <p id="coffeeReady">Ваш кофе готов!</p>
        </div> 


        <div class="rightPart">
          <div class="menu">
            <p id="display">Выберите кофе</p>
            <p>Баланс: <span id="balance">0</span>руб.</p>
            <div class="progress" id="progress" hidden>
              <div id="progressBar" class="progress-bar progress-bar-striped progress-bar-animated bg-warning" role="progressbar" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100" style="width: 0%">
              </div>
            </div>
            <input type="text" id="cash" hidden><br>
          </div>
          <div class="bill_acc">
            <img src="bill-acc.png" alt="Аппарат для приёма денег" id="billAcc">
            <br>
            <button type="button" id="drop-off-button" onclick="getChange(cash.value)">Получить сдачу</button>
          </div>
          <div id="moneyField"></div>  
        </div>
      </div>
      <img src="500rub.jpg" alt="Купюра номиналом 500 рублей" class="money five" data-balance="500">
      <img src="100rub.jpg" alt="Купюра номиналом 100 рублей" class="money one" data-balance="100">
      <img src="50rub.jpg" alt="Купюра номиналом 50 рублей" class="money half" data-balance="50">
    
    <script>
    
      let cash = document.getElementById("cash");
      let display = document.getElementById("display");
      let bills = document.querySelectorAll(`[src$="rub.jpg"]`);
      let balance = document.getElementById("balance");
      let progressBar = document.getElementById("progressBar");
      let displayInfo = document.getElementById("displayInfo");
      let moneyField = document.getElementById("moneyField");
      let centralPart = document.getElementById("centralPart");

      for(let i=0; i<bills.length; i++){
        let img = bills[i];
        img.onmousedown = function(event){
          img.ondragstart = function(){return false;}
          img.style = "transform: rotate(-90deg)";
          img.style.position = "absolute";
          img.style.top = event.clientY-img.height/2+"px";
          img.style.left = event.clientX-img.width/2+"px";
          document.onmousemove = function(e){
            img.style.top = e.clientY-img.height/2+"px";
            img.style.left = e.clientX-img.width/2+"px";
          }
          img.onmouseup = function(e){
            document.onmousemove = function(){return false;}
            let billAccTop = billAcc.getBoundingClientRect().top; 
            let billAccBottom = billAcc.getBoundingClientRect().bottom; 
            let billAccleft = billAcc.getBoundingClientRect().left; 
            let billAccRight = billAcc.getBoundingClientRect().right; 
            if(e.clientY < billAccBottom  
              && e.clientX < billAccRight         
              && e.clientX > billAccleft){  
            console.log('Координаты совпали.');
            img.hidden = true;
            cash.value = +cash.value + (+img.dataset.balance);
            balance.innerHTML = cash.value;
            }
          }
        }
      }      

      function getCoffee(coffeeName, price){
        if(cash.value>=price){
          progressBar.parentElement.hidden = false;
          cash.value -= price;
          display.innerHTML = `Кофе ${coffeeName} готов`;
          balance.innerHTML = cash.value;
          display.innerHTML = "Ожидайте..."
          let n=0;
          let timerId = setInterval(function(){
            progressBar.style.width = (++n)+"%"; // Заполняем прогресс бар
            if(n>125){ // Когда прогресс бар полностью заполнится
              clearInterval(timerId); // Удаляем setInterval
              display.innerHTML = "Кофе "+coffeeName+" готов";
              centralPart.hidden = false;
              progressBar.parentElement.hidden = true; // Прячем прогресс бар
              progressBar.style.width = 0+"%"; // Устанавливаем ширину в ноль, для того, чтобы слелующий раз прогресс бар шел с нуля
            }
          }, 40)
        }else{
          display.innerHTML = "Недостаточно средств";
        }
      }
      
      function getChange(num){
        let top = getRandom(0, 160-50);
        let left = getRandom(0, moneyField.getBoundingClientRect().width - 50);
        let coin = 0;
        if(num>=10){coin = 10;}
        else if(num>=5){coin = 5;}
        else if(num>=2){coin = 2;}
        else if(num>=1){coin = 1;}
        if(coin!=0){
          console.log(coin);
          moneyField.innerHTML = moneyField.innerHTML + `<img onclick="this.hidden = true" 
            style="top:${top}px; left:${left}px;" 
            src="${coin}rub.png">`;
          getChange(num - coin);
        }else{
          cash.value = 0;
          balance.innerHTML = cash.value;
        }
      }

      function getRandom(min,max){
        return Math.random()*(max-min)+min;
      }
      
      function newSession(){
        display.innerHTML = "Выберите кофе";
        centralPart.hidden = true;
      }

    </script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-gtEjrD/SeCtmISkJkNUaaKMoLD0//ElJ19smozuHV6z3Iehds+3Ulb9Bn9Plx0x4" crossorigin="anonymous"></script>
  </body>
</html>
