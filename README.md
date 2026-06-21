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

        nav a{
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
    </style>
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
    <button>Login</button>
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