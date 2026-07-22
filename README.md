<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Business Card</title>

<style>
    *{
        margin:0;
        padding:0;
        box-sizing:border-box;
    }

    body{
        background:#f3f3f3;
        display:flex;
        justify-content:center;
        align-items:center;
        min-height:100vh;
        font-family:Arial, sans-serif;
    }

    .container{
        text-align:center;
    }

    img{
        width:90vw;
        max-width:700px;
        border-radius:16px;
        box-shadow:0 8px 30px rgba(0,0,0,.2);
        transition:.3s;
    }

    button{
        margin-top:20px;
        padding:14px 30px;
        border:none;
        border-radius:10px;
        background:#111;
        color:white;
        font-size:16px;
        cursor:pointer;
    }

    button:hover{
        opacity:.85;
    }
</style>
</head>

<body>

<div class="container">

    <img id="card" src="front.png" alt="Business Card">

    <br>

    <button onclick="flipCard()">뒷면 보기</button>

</div>

<script>

let front=true;

function flipCard(){

    const card=document.getElementById("card");
    const btn=document.querySelector("button");

    if(front){
        card.src="back.png";
        btn.innerText="앞면 보기";
    }else{
        card.src="front.png";
        btn.innerText="뒷면 보기";
    }

    front=!front;
}

</script>

</body>
</html>
