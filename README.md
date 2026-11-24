
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Trading FX Capital</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  background: #090909;
  color: white;
  font-family: Arial, sans-serif;
}
header {
  background: #151515;
  padding: 22px;
  text-align: center;
  border-bottom: 2px solid #c9a443;
}
h1, h2 { color: #d9b65c; }
nav {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  padding: 18px;
}
button {
  background: #d9b65c;
  color: #111;
  border: 0;
  padding: 12px 20px;
  border-radius: 7px;
  font-weight: bold;
  cursor: pointer;
}
main {
  max-width: 650px;
  margin: 25px auto;
  padding: 18px;
}
.card {
  background: #181818;
  border: 1px solid #80672f;
  border-radius: 12px;
  padding: 22px;
  margin-bottom: 18px;
}
.balance {
  font-size: 32px;
  color: #d9b65c;
}
input {
  width: 100%;
  padding: 13px;
  margin: 10px 0;
  background: #090909;
  color: white;
  border: 1px solid #80672f;
  border-radius: 6px;
}
.page { display: none; }
.page.active { display: block; }
footer {
  text-align: center;
  padding: 25px;
  color: #aaa;
}
</style>
</head>
<body>

<header>
  <h1>TRADING FX CAPITAL</h1>
  <p>PRECISION • DISCIPLINE • MARKETS</p>
</header>

<nav>
  <button onclick="showPage('home')">Home</button>
  <button onclick="showPage('deposit')">Deposit</button>
  <button onclick="showPage('withdraw')">Withdraw</button>
  <button onclick="showPage('account')">My Account</button>
</nav>

<main>

<section id="home" class="page active">
  <div class="card">
    <h2>Welcome to Trading FX Capital</h2>
    <p>Your financial dashboard.</p>
    <p>Demo account balance</p>
    <div class="balance">$0.00</div>
    <p>Demo preview only. No real funds are held.</p>
  </div>
  <div class="card">
    <h2>Quick Actions</h2>
    <button onclick="showPage('deposit')">Deposit Funds</button>
    <button onclick="showPage('withdraw')">Withdraw Funds</button>
  </div>
</section>

<section id="deposit" class="page">
  <div class="card">
    <h2>Deposit Funds</h2>
    <p>Enter an amount to preview a deposit request.</p>
    <input type="number" id="depositAmount" placeholder="Amount in USD" min="1">
    <button onclick="demoMessage('depositAmount','depositMessage','Deposit')">Continue</button>
    <p id="depositMessage"></p>
  </div>
</section>

<section id="withdraw" class="page">
  <div class="card">
    <h2>Withdraw Funds</h2>
    <p>Enter an amount to preview a withdrawal request.</p>
    <input type="number" id="withdrawAmount" placeholder="Amount in USD" min="1">
    <button onclick="demoMessage('withdrawAmount','withdrawMessage','Withdrawal')">Continue</button>
    <p id="withdrawMessage"></p>
  </div>
</section>

<section id="account" class="page">
  <div class="card">
    <h2>My Account</h2>
    <p>Account dashboard preview.</p>
    <p>Account type: Demo</p>
    <p>Status: Preview</p>
    <p>Secure registration and login will be added with a backend.</p>
  </div>
</section>

</main>

<footer>
  <p>Trading FX Capital</p>
  <p>Demo website. Trading involves financial risk.</p>
</footer>

<script>
function showPage(id) {
  document.querySelectorAll('.page').forEach(page => {
    page.classList.remove('active');
  });
  document.getElementById(id).classList.add('active');
}

function demoMessage(inputId, messageId, action) {
  const amount = Number(document.getElementById(inputId).value);
  const message = document.getElementById(messageId);

  if (!Number.isFinite(amount) || amount <= 0) {
    message.textContent = "Please enter a valid amount.";
    return;
  }

  message.textContent =
    action + " is currently demo only. No money was transferred.";
}
</script>

</body>
</html>
# Trading-_fx_capital
