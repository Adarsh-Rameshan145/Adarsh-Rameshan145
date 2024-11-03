<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be Mine?</title>
    <style>
        body {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://source.unsplash.com/1600x900/?romantic,stars');
            background-size: cover;
            color: #fff;
            text-align: center;
        }
        #container {
            background-color: rgba(0, 0, 0, 0.7);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        h1 {
            font-size: 2.5em;
        }
        p {
            font-size: 1.2em;
            margin: 20px 0;
        }
        button {
            padding: 15px 30px;
            font-size: 1em;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }
        .yes-button {
            background-color: #28a745;
            color: #fff;
        }
        .no-button {
            background-color: #dc3545;
            color: #fff;
            position: relative;
        }
        .no-button:hover {
            position: absolute;
            top: calc(50vh * (Math.random() - 0.5));
            left: calc(50vw * (Math.random() - 0.5));
            transition: 0.2s;
        }
        #result {
            font-size: 1.5em;
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>
    <div id="container">
        <h1>Will You Be Mine?</h1>
        <p>I've waited a long time to say this, and now, I can't wait any longer. Will you be my love, my heart, and my forever?</p>
        <button class="yes-button" onclick="showResult(true)">Yes 💖</button>
        <button class="no-button" onmouseover="moveNoButton()">No 💔</button>
        <div id="result"></div>
    </div>

    <script>
        function showResult(isYes) {
            const result = document.getElementById('result');
            if (isYes) {
                result.textContent = "You’ve made me the happiest person alive! 💍✨";
                result.style.color = "#28a745";
            }
            result.style.display = "block";
        }

        function moveNoButton() {
            const noButton = document.querySelector('.no-button');
            noButton.style.top = `${Math.random() * 80}vh`;
            noButton.style.left = `${Math.random() * 80}vw`;
        }
    </script>
</body>
</html>
