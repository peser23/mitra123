
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Random Number Display</title>
<style>
    body {
        background: #111827;
        color: white;
        font-family: Arial, sans-serif;
        text-align: center;
        padding-top: 30px;
    }

    .section {
        font-size: 20px;
        color: #9CA3AF;
        margin-top: 10px;
    }

    .number {
        font-size: 100px;
        font-weight: bold;
        margin: 5px;
    }

    #number2 {
        color: #60A5FA;
    }
</style>
</head>
<body>

<div class="section">SECTION 1</div>
<div class="number" id="number1">30</div>

<div class="section">SECTION 2</div>
<div class="number" id="number2">1:25</div>

<script>
function updateNumbers() {
    document.getElementById("number1").textContent =
        Math.floor(Math.random() * 15) + 30;

    let seconds = Math.floor(Math.random() * 26) + 85;
    let minutes = Math.floor(seconds / 60);
    let remaining = seconds % 60;

    document.getElementById("number2").textContent =
        minutes + ":" + String(remaining).padStart(2, "0");
}

updateNumbers();
setInterval(updateNumbers, 500);
</script>

</body>
</html>
