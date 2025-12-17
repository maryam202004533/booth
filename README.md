<!doctype html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover" />
  <title>Interact with Aja</title>

  <style>
    :root{
      --bg1:#02061a;
      --bg2:#000b3d;
      --aja:#0baaff;
      --aja2:#56d6ff;
      --text:#f4f8ff;
    }

    *{box-sizing:border-box}
    html,body{height:100%}

    body{
      margin:0;
      font-family: "Tajawal", system-ui, Arial, sans-serif;
      background:
        radial-gradient(1200px 700px at 20% 20%, rgba(11,170,255,.25), transparent 60%),
        radial-gradient(900px 600px at 85% 40%, rgba(86,214,255,.25), transparent 55%),
        linear-gradient(135deg, var(--bg1), var(--bg2));
      color:var(--text);
      overflow:hidden;
      display:flex;
      align-items:center;
      justify-content:center;
    }

    /* شبكة خفيفة */
    .grid{
      position:absolute;
      inset:0;
      background:
        linear-gradient(rgba(255,255,255,.06) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.06) 1px, transparent 1px);
      background-size:60px 60px;
      opacity:.25;
      animation: move 8s linear infinite;
    }

    @keyframes move{
      from{transform:translateY(0)}
      to{transform:translateY(60px)}
    }

    /* أيقونات طافية */
    .float{
      position:absolute;
      font-size:40px;
      animation: float 3s ease-in-out infinite;
      filter: drop-shadow(0 10px 15px rgba(0,0,0,.4));
    }
    .f1{left:10%; top:18%}
    .f2{right:12%; top:22%; animation-duration:2.6s}
    .f3{left:14%; bottom:18%; animation-duration:3.4s}
    .f4{right:16%; bottom:16%; animation-duration:2.9s}

    @keyframes float{
      0%,100%{transform:translateY(0)}
      50%{transform:translateY(-14px)}
    }

    /* الكرت */
    .card{
      position:relative;
      z-index:2;
      width:min(900px,92%);
      padding:50px 40px;
      border-radius:28px;
      background:rgba(0,12,55,.45);
      border:1px solid rgba(86,214,255,.3);
      backdrop-filter: blur(10px);
      text-align:center;
      box-shadow:0 30px 80px rgba(0,0,0,.45);
    }

    .badge{
      display:inline-flex;
      align-items:center;
      gap:10px;
      padding:10px 18px;
      border-radius:999px;
      background:rgba(11,170,255,.12);
      border:1px solid rgba(86,214,255,.35);
      font-weight:700;
      margin-bottom:20px;
    }

    .dot{
      width:10px;
      height:10px;
      border-radius:50%;
      background:var(--aja);
      box-shadow:0 0 16px var(--aja);
      animation:pulse 1.2s infinite;
    }

    @keyframes pulse{
      0%,100%{transform:scale(1)}
      50%{transform:scale(1.4)}
    }

    h1{
      font-size:clamp(38px,5vw,64px);
      margin:10px 0;
      font-weight:800;
      animation:title 3s ease-in-out infinite;
    }

    @keyframes title{
      0%,100%{transform:translateY(0)}
      50%{transform:translateY(-8px)}
    }

    .sub{
      font-size:clamp(18px,2.4vw,26px);
      margin-bottom:34px;
      opacity:.95;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      gap:12px;
      padding:16px 26px;
      font-size:clamp(18px,2.2vw,24px);
      font-weight:800;
      color:#00152e;
      background:linear-gradient(90deg, var(--aja), var(--aja2));
      border-radius:16px;
      box-shadow:0 20px 50px rgba(11,170,255,.3);
      animation: btn 1.6s infinite;
      user-select:none;
    }

    @keyframes btn{
      0%,100%{transform:scale(1)}
      50%{transform:scale(1.05)}
    }

  </style>
</head>

<body>

  <div class="grid"></div>

  <div class="float f1">🎮</div>
  <div class="float f2">📘</div>
  <div class="float f3">🏆</div>
  <div class="float f4">🎁</div>

  <div class="card">
    <div class="badge">
      <span class="dot"></span>
      Interact with Aja
    </div>

    <h1>ابدأ تجربتك الآن</h1>
    <div class="sub">واكسب هديتك 🎁</div>

    <div class="btn">ابدأ الآن ⚡</div>
  </div>

</body>
</html>
