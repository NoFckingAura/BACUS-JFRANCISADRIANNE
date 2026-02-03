<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Advanced JavaScript Interaction</title>

    <style>
        :root {
            --primary: #7c3aed;
            --secondary: #0f172a;
            --accent: #22d3ee;
            --light: #f8fafc;
        }

        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            height: 100vh;
            font-family: "Inter", Arial, sans-serif;
            background: radial-gradient(circle at top left, #1e1b4b, #020617);
            display: flex;
            justify-content: center;
            align-items: center;
            color: var(--light);
        }

        .app {
            width: 460px;
            background: linear-gradient(145deg, #020617, #0f172a);
            border-radius: 20px;
            padding: 35px;
            box-shadow:
                0 25px 50px rgba(0,0,0,0.7),
                inset 0 0 0 1px rgba(255,255,255,0.05);
        }

        .app-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .app-header h1 {
            margin: 0;
            font-size: 22px;
            color: var(--accent);
            letter-spacing: 1px;
        }

        .divider {
            height: 1px;
            background: linear-gradient(to right, transparent, var(--primary), transparent);
            margin: 18px 0;
        }

        .block {
            margin-bottom: 22px;
        }

        .block-title {
            font-size: 13px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #a5b4fc;
            margin-bottom: 8px;
        }

        button {
            width: 100%;
            padding: 12px;
            border-radius: 12px;
            border: none;
            background: linear-gradient(135deg, var(--primary), #9333ea);
            color: white;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.15s ease, box-shadow 0.15s ease;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(124,58,237,0.5);
        }

        input {
            width: 100%;
            padding: 11px;
            border-radius: 10px;
            border: 1px solid #334155;
            background-color: #020617;
            color: var(--light);
            margin-bottom: 10px;
            font-size: 14px;
        }

        input:focus {
            outline: none;
            border-color: var(--accent);
        }

        #output {
            min-height: 24px;
            padding: 8px;
            border-radius: 8px;
            background-color: #020617;
            border: 1px dashed #475569;
            color: var(--accent);
            font-weight: 600;
        }

        #hoverText {
            text-align: center;
            padding: 14px;
            border-radius: 12px;
            background: linear-gradient(135deg, #020617, #0f172a);
            transition: all 0.3s ease;
            border: 1px solid #1e293b;
        }
    </style>
</head>
<body>

    <div class="app">

        <div class="app-header">
            <h1>JavaScript Practice</h1>
        </div>

        <div class="divider"></div>

        <div class="block">
            <div class="block-title">Alert Feature</div>
            <button onclick="triggerAlert()">Execute Alert</button>
        </div>

        <div class="block">
            <div class="block-title">Input Processing</div>
            <input type="text" id="userInput" placeholder="Enter any value">
            <button onclick="processInput()">Process Input</button>
            <div id="output"></div>
        </div>

        <div class="block">
            <div class="block-title">Hover Interaction</div>
            <p id="hoverText">Hover your mouse over this panel</p>
        </div>

    </div>

    <script>
        function triggerAlert() {
            alert("Advanced JavaScript alert executed successfully.");
        }

        function processInput() {
            let inputValue = document.getElementById("userInput").value;
            document.getElementById("output").innerText = inputValue;
        }

        document.getElementById("hoverText").onmouseover = function () {
            this.style.color = "#020617";
            this.style.background = "#22d3ee";
            this.style.fontWeight = "700";
        };
    </script>

</body>
</html>
