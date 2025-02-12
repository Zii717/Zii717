<!DOCTYPE html>
<html lang="mn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Нууц үг шалгах</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: linear-gradient(120deg, #89f7fe, #66a6ff);
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        h1 {
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        input, button {
            padding: 10px;
            font-size: 18px;
            margin: 10px;
        }
        button {
            background: #66a6ff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }
        button:hover {
            background: #4c8cf7;
        }
        #result {
            font-size: 24px;
            font-weight: bold;
            margin-top: 20px;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <h1>Нууц үгээ оруулна уу:</h1>
    <div class="container">
        <input type="text" id="secretInput" placeholder="Энд бич...">
        <button onclick="checkSecret()">Шалгах</button>
        <p id="result" class="hidden"></p>
    </div>

    <script>
        function checkSecret() {
            var input = document.getElementById("secretInput").value.trim().toLowerCase();
            var result = document.getElementById("result");

            if (input === "зилфэрон") {
                result.innerText = "Чи маш хөөрхөн!";
                result.style.color = "green";
                result.classList.remove("hidden");
            } else {
                result.innerText = "Буруу нууц үг!";
                result.style.color = "red";
                result.classList.remove("hidden");
            }
        }
    </script>

</body>
</html>
