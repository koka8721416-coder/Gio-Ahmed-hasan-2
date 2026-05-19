<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>أساسيات علم الحشرات</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Tahoma, Arial;
}

body{
    background:linear-gradient(135deg,#0f172a,#1e293b);
    min-height:100vh;
    color:white;
}

header{
    width:100%;
    padding:25px;
    text-align:center;
    background:rgba(255,255,255,0.05);
    backdrop-filter:blur(10px);
    box-shadow:0 4px 15px rgba(0,0,0,0.3);
}

header h1{
    font-size:32px;
    color:#38bdf8;
}

.container{
    display:flex;
    justify-content:center;
    align-items:center;
    gap:30px;
    flex-wrap:wrap;
    padding:50px 20px;
}

.card{
    width:320px;
    height:180px;
    background:rgba(255,255,255,0.08);
    border:1px solid rgba(255,255,255,0.1);
    border-radius:25px;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    cursor:pointer;
    transition:0.3s;
    box-shadow:0 10px 25px rgba(0,0,0,0.3);
}

.card:hover{
    transform:translateY(-8px) scale(1.03);
    background:#0ea5e9;
}

.card h2{
    font-size:28px;
    margin-bottom:10px;
}

.card p{
    font-size:16px;
}

.viewer{
    width:100%;
    height:80vh;
    margin-top:20px;
    display:none;
}

iframe{
    width:100%;
    height:100%;
    border:none;
    background:white;
}

.backBtn{
    display:none;
    margin:20px auto;
    padding:12px 30px;
    border:none;
    border-radius:12px;
    background:#ef4444;
    color:white;
    font-size:18px;
    cursor:pointer;
    transition:0.3s;
}

.backBtn:hover{
    background:#dc2626;
}
</style>
</head>

<body>

<header>
    <h1>منصة أساسيات علم الحشرات</h1>
</header>

<div class="container" id="menu">

    <div class="card" onclick="openPage('https://koka8721416-coder.github.io/koka2/')">
        <h2>امتحان سابق</h2>
        <p>اضغط للدخول</p>
    </div>

    <div class="card" onclick="openPage('https://koka8721416-coder.github.io/koka/')">
        <h2>بنك أسئلة 100 سؤال</h2>
        <p>اضغط للدخول</p>
    </div>

</div>

<button class="backBtn" id="backBtn" onclick="goBack()">⬅ الرجوع للرئيسية</button>

<div class="viewer" id="viewer">
    <iframe id="frame"></iframe>
</div>

<script>

function openPage(link){
    document.getElementById("frame").src = link;
    document.getElementById("viewer").style.display = "block";
    document.getElementById("backBtn").style.display = "block";
    document.getElementById("menu").style.display = "none";
}

function goBack(){
    document.getElementById("viewer").style.display = "none";
    document.getElementById("backBtn").style.display = "none";
    document.getElementById("menu").style.display = "flex";
    document.getElementById("frame").src = "";
}

</script>

</body>
</html>
