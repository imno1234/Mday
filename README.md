<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>오늘 날짜 표시</title>
  <style>
    body {
      font-family: "Noto Sans KR", sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f2f2f2;
    }
    h1 {
      color: #333;
    }
    .date {
      font-size: 1.8em;
      color: #0078d7;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <h1>QR 코드 인식 결과</h1>
  <div class="date" id="today"></div>

  <script>
    const now = new Date();
    const formatted = now.getFullYear() + "-" +
      String(now.getMonth()+1).padStart(2, '0') + "-" +
      String(now.getDate()).padStart(2, '0');
    document.getElementById("today").innerText = `오늘 날짜: ${formatted}`;
  </script>
</body>
</html>
