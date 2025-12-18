# anniku
最強の魚
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Mobile Ready Site</title>

  <style>
    * {
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
    }

    html, body {
      margin: 0;
      padding: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, #0b0f1a, #141a3c);
      font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      color: #fff;
    }

    body {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .card {
      width: min(92%, 420px);
      background: rgba(20, 26, 60, 0.85);
      backdrop-filter: blur(10px);
      border-radius: 18px;
      padding: 24px;
      box-shadow: 0 20px 40px rgba(0,0,0,.4);
      text-align: center;
    }

    h1 {
      margin: 0 0 12px;
      font-size: 26px;
    }

    p {
      margin: 0 0 20px;
      opacity: 0.85;
      font-size: 15px;
    }

    button {
      width: 100%;
      padding: 16px;
      font-size: 18px;
      border-radius: 14px;
      border: none;
      background: #6cf;
      color: #000;
      font-weight: bold;
      cursor: pointer;
    }

    button:active {
      transform: scale(0.97);
    }

    .status {
      margin-top: 16px;
      font-size: 14px;
      opacity: 0.8;
    }
  </style>
</head>

<body>

  <div class="card">
    <h1>📱 モバイル対応サイト</h1>
    <p>ファイル入れるだけで公開OK</p>

    <button id="actionBtn">タップして実行</button>

    <div class="status" id="status">待機中</div>
  </div>

  <script>
    const btn = document.getElementById("actionBtn");
    const status = document.getElementById("status");

    const clickEvent = ("ontouchstart" in window) ? "touchstart" : "click";

    btn.addEventListener(clickEvent, () => {
      status.textContent = "実行された ✔";
      navigator.vibrate?.(30);
    });
  </script>

</body>
</html>
