<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        .calculator {
            border: 1px solid #000;
            padding: 10px;
            display: inline-block;
        }
        .display {
            width: 100%;
            height: 40px;
            text-align: right;
            margin-bottom: 10px;
            padding: 5px;
            font-size: 18px;
            border: 1px solid #ccc;
        }
        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }
        .buttons button {
            width: 100%;
            height: 40px;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" class="display" id="display" readonly>
        <div class="buttons">
            <button onclick="clearDisplay()">Clear</button>
            <button onclick="appendCharacter('=')">=</button>
            <button onclick="appendCharacter('(')">(</button>
            <button onclick="appendCharacter(')')">)</button>
            <button onclick="appendCharacter('*')">*</button>
            <button onclick="appendCharacter('/')">/</button>
            <button onclick="appendCharacter('+')">+</button>
            <button onclick="appendCharacter('-')">-</button>
            <button onclick="appendCharacter('.')">.</button>
            <button onclick="appendCharacter('1')">1</button>
            <button onclick="appendCharacter('2')">2</button>
            <button onclick="appendCharacter('3')">3</button>
            <button onclick="appendCharacter('4')">4</button>
            <button onclick="appendCharacter('5')">5</button>
            <button onclick="appendCharacter('6')">6</button>
            <button onclick="appendCharacter('7')">7</button>
            <button onclick="appendCharacter('8')">8</button>
            <button onclick="appendCharacter('9')">9</button>
            <button onclick="appendCharacter('0')">0</button>
        </div>
    </div>

    <script>
        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function appendCharacter(character) {
            const display = document.getElementById('display');
            if (character === '=') {
                try {
                    display.value = eval(display.value);
                } catch {
                    display.value = 'Error';
                }
            } else {
                display.value += character;
            }
        }
    </script>
</body>
</html>


[This project demonstrates how to create a simple online calculator using HTML, CSS, and JavaScript. The `eval()` function is used to evaluate mathematical expressions. This project highlights the importance of testing and error handling in web development.]
(https://docs.google.com/presentation/d/19lBrbZgdVyQwmPZIkhyvsoeiKcS-BZbdIDAJeacHu7g/edit?usp=sharing)
