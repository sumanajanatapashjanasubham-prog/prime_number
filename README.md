<!DOCTYPE html>
<html>
<head>
    <title>Prime Number Checker</title>
    <style>
        body {
            font-family: Arial;
            text-align: center;
            background: #f2f2f2;
            padding-top: 100px;
        }

        .box {
            background: white;
            width: 350px;
            margin: auto;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 15px #bbb;
        }

        h2 {
            color: blue;
        }

        input, button {
            padding: 10px;
            margin: 10px;
            border-radius: 8px;
            border: 1px solid #aaa;
        }

        button {
            background: #4CAF50;
            color: white;
            cursor: pointer;
            border: none;
        }

        button:hover {
            background: #45a049;
        }

        #result {
            font-size: 18px;
            font-weight: bold;
        }
    </style>
</head>

<body>

<div class="box">
    <h2>🔢 Prime Number Checker</h2>

    <input type="number" id="num" placeholder="Enter a number">
    <button onclick="checkPrime()">Check</button>

    <p id="result"></p>
</div>

<script>
function checkPrime() {
    let n = Number(document.getElementById("num").value);
    let prime = n > 1;

    for (let i = 2; i < n; i++) {
        if (n % i == 0) {
            prime = false;
            break;
        }
    }

    let result = document.getElementById("result");

    if (prime) {
        result.innerHTML = "✅ " + n + " is Prime";
        result.style.color = "green";
    } else {
        result.innerHTML = "❌ " + n + " is Not Prime";
        result.style.color = "red";
    }
}
</script>

</body>
</html>
