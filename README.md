<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nextradeinvest</title>

    <style>
        body{
            margin:0;
            font-family:Arial,sans-serif;
            background:#f4f4f4;
        }

        header{
            background:#111;
            color:white;
            padding:20px;
            text-align:center;
        }

        nav a{<a onclick="showAdmin()">Admin</a>
            color:white;
            margin:10px;
            text-decoration:none;
            cursor:pointer;
        }

        .hero{
            text-align:center;
            padding:50px 20px;
            background:white;
        }

        .features{
            display:flex;
            flex-wrap:wrap;
            justify-content:center;
            gap:20px;
            padding:30px;
        }

        .box{
            background:white;
            padding:20px;
            width:250px;
            border-radius:10px;
        }

        footer{
            background:#111;
            color:white;
            text-align:center;
            padding:10px;
        }

        /* LOGIN / REGISTER */
        .form-box{
            display:none;
            background:white;
            width:300px;
            margin:20px auto;
            padding:20px;
            border-radius:10px;
        }

        .form-box input{
            width:100%;
            padding:10px;
            margin:10px 0;
        }

        .form-box button{
            width:100%;
            padding:10px;
            background:black;
            color:white;
            border:none;
        }
    </style>button{
    padding:10px;
    margin:5px 0;
    width:100%;
    border:none;
    background:#000;
    color:#fff;
    border-radius:5px;
    cursor:pointer;
}
</head>

<body>

<header>
    <h1>Nextradeinvest</h1>
    <nav>
        <a onclick="showHome()">Home</a>
        <a onclick="showLogin()">Login</a>
        <a onclick="showRegister()">Register</a>
    </nav>
</header>

<!-- HOME -->
<div id="home">

    <div class="hero">
        <h2>Grow Your Money With Smart Investment</h2>
        <p>Secure platform with daily returns and referral system.</p>
    </div>

    <div class="features">
        <div class="box">
            <h3>Deposit</h3>
            <p>Fast crypto deposit system.</p>
        </div>

        <div class="box">
            <h3>Withdraw</h3>
            <p>Easy withdrawal anytime.</p>
        </div>

        <div class="box">
            <h3>Referral</h3>
            <p>Earn by inviting friends.</p>
        </div>
    </div>

</div>

<!-- LOGIN -->
<div class="form-box" id="login">
    <h3>Login</h3>
    <input type="text" placeholder="Username">
    <input type="password" placeholder="Password">
    <button>Login</button><button onclick="showDashboard()">Login</button>
</div>

<!-- REGISTER -->
<div class="form-box" id="register">
    <h3>Register</h3>
    <input type="text" placeholder="Username">
    <input type="email" placeholder="Email">
    <input type="password" placeholder="Password">
    <button>Register</button>
</div>

<footer>
    <p>© 2026 Nextradeinvest</p>
</footer>

<script>
let balance = localStorage.getItem("balance") 
    ? parseFloat(localStorage.getItem("balance")) : 0;

let referralEarnings = localStorage.getItem("referralEarnings") 
    ? parseFloat(localStorage.getItem("referralEarnings")) : 0;

let totalUsers = localStorage.getItem("totalUsers") 
    ? parseInt(localStorage.getItem("totalUsers")) : 1;

let platformBalance = localStorage.getItem("platformBalance") 
    ? parseFloat(localStorage.getItem("platformBalance")) : 0;
function saveData(){
    localStorage.setItem("balance", balance);
    localStorage.setItem("referralEarnings", referralEarnings);
    localStorage.setItem("totalUsers", totalUsers);
    localStorage.setItem("platformBalance", platformBalance);
}

function showAdmin(){
    document.getElementById("home").style.display="none";
    document.getElementById("login").style.display="none";
    document.getElementById("register").style.display="none";
    document.getElementById("dashboard").style.display="none";
    document.getElementById("adminPanel").style.display="block";
}

function adminAddBalance(){
    function adminAddBalance(){
    let amount = parseFloat(document.getElementById("adminAdd").value);

    if(isNaN(amount) || amount <= 0){
        alert("Invalid amount");
        return;
    }

    platformBalance += amount;
    saveData();

    document.getElementById("platformBalance").innerText =
        platformBalance.toFixed(2);
}
    }

    platformBalance += amount;
    document.getElementById("platformBalance").innerText = platformBalance.toFixed(2);

    alert("Balance added to platform!");
}

function resetSystem(){
    if(confirm("Reset everything?")){
        balance = 0;
        referralEarnings = 0;
        platformBalance = 0;

        document.getElementById("platformBalance").innerText = "0.00";
        document.getElementById("refEarn").innerText = "0.00";

        alert("System reset completed!");
    }
}
function showDashboard(){<div class="form-box" id="dashboard">
    <h2>Dashboard</h2>

    <p><b>Balance:</b> $0.00</p>
    <p><b>Total Invested:</b> $0.00</p>
    <p><b>Referral Earnings:</b> $0.00</p>

    <hr>
let balance = 0;
let referralEarnings = 0;

function generateReferral(){
    let userId = Math.floor(Math.random() * 100000);
    let link = window.location.href + "?ref=" + userId;

    document.getElementById("refLink").value = link;

    alert("Referral link generated!");
}

// Simulation function (lè yon moun "envite")
function addReferralBonus(){
    let bonus = 5; // chak referral = $5 bonus
    referralEarnings += bonus;

    document.getElementById("refEarn").innerText = referralEarnings.toFixed(2);

    alert("You received $5 referral bonus!");
}
function deposit(){
    let amount = parseFloat(document.getElementById("depositAmount").value);

    if(isNaN(amount) || amount <= 0){
        alert("Enter valid amount");
        return;
    }

    balance += amount;
    alert("Deposit successful: $" + amount);
    updateUI();
}

function withdraw(){
function withdraw(){
    let amount = parseFloat(document.getElementById("withdrawAmount").value);

    if(isNaN(amount) || amount <= 0){
        alert("Enter valid amount");
        return;
    }

    let fee = amount * 0.10;
    let total = amount + fee;

    if(total > balance){
        alert("Not enough balance");
        return;
    }

    balance -= total;
    saveData();
    updateUI();

    alert("Withdraw successful");
}
    updateUI();
<h3>Referral System</h3>

<p><b>Your Referral Link:</b></p>
<input type="text" id="refLink" readonly>

<button onclick="generateReferral()">Generate Link</button>

<p><b>Referral Earnings:</b> $<span id="refEarn">0.00</span></p>
}

function updateUI(){
    document.querySelector("#dashboard p").innerHTML = "<b>Balance:</b> $" + balance.toFixed(2);
}

    <h3>Deposit</h3>
    <input type="number" id="depositAmount" placeholder="Enter amount">
    <button onclick="deposit()">Deposit</button>

    <h3>Withdraw</h3>
    <input type="number" id="withdrawAmount" placeholder="Enter amount">
    <button onclick="withdraw()">Withdraw</button>

    <hr>

    <h3>Actions</h3>
    <button onclick="alert('Referral system coming soon')">Referral</button>
</div>
    document.getElementById("home").style.display="none";
    document.getElementById("login").style.display="none";
    document.getElementById("register").style.display="none";
    document.getElementById("dashboard").style.display="block";
}
function showHome(){
    document.getElementById("home").style.display="block";
    document.getElementById("login").style.display="none";
    document.getElementById("register").style.display="none";
}

function showLogin(){
    document.getElementById("home").style.display="none";
    document.getElementById("login").style.display="block";
    document.getElementById("register").style.display="none";
}

function showRegister(){
    document.getElementById("home").style.display="none";
    document.getElementById("login").style.display="none";
    document.getElementById("register").style.display="block";
}

showHome();
</script>

</body>
</html>
<!-- DASHBOARD -->
<div class="form-box" id="adminPanel">
    <h2>Admin Panel</h2>

    <p><b>Total Users:</b> <span id="totalUsers">1</span></p>
    <p><b>Total Platform Balance:</b> $<span id="platformBalance">0.00</span></p>

    <hr>

    <h3>Manual Add Balance</h3>
    <input type="number" id="adminAdd" placeholder="Amount">
    <button onclick="adminAddBalance()">Add</button>

    <h3>Reset System</h3>
    <button onclick="resetSystem()">Reset All</button>
</div>
<div class="form-box" id="dashboard">
    <h2>Dashboard</h2>

    <p><b>Balance:</b> $0.00</p>
    <p><b>Total Invested:</b> $0.00</p>
    <p><b>Referral Earnings:</b> $0.00</p>

    <hr>

    <h3>Quick Actions</h3>

    <button onclick="alert('Deposit system coming soon')">Deposit</button>
    <button onclick="alert('Withdrawal system coming soon')">Withdraw</button>
    <button onclick="alert('Referral link coming soon')">Referral</button>
</div>
window.onload = function(){
    let urlParams = new URLSearchParams(window.location.search);
    if(urlParams.get("ref")){
        addReferralBonus();
    }function addReferralBonus(){
    referralEarnings += 5;
    saveData();

    document.getElementById("refEarn").innerText =
        referralEarnings.toFixed(2);
}
}