# Index.html-Do-Marcos
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cálculo da Média Aritmética</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Calcular Média</h1>
        <div class="form-group">
            <label for="num1">Número 1:</label>
            <input type="number" id="num1" required>
        </div>
        <div class="form-group">
            <label for="num2">Número 2:</label>
            <input type="number" id="num2" required>
        </div>
        <div class="form-group">
            <label for="num3">Número 3:</label>
            <input type="number" id="num3" required>
        </div>
        <div class="form-group">
            <label for="num4">Número 4:</label>
            <input type="number" id="num4" required>
        </div>
        <button onclick="calcularMedia()">Calcular Média</button>
        <div class="result" id="resultado"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>


body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f4f4f9;
}

.container {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 300px;
}

h1 {
    text-align: center;
    margin-bottom: 20px;
}

.form-group {
    margin-bottom: 15px;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
}

.form-group input {
    width: 100%;
    padding: 8px;
    box-sizing: border-box;
    border: 1px solid #ddd;
    border-radius: 4px;
}

.result {
    font-weight: bold;
    text-align: center;
}

button {
    width: 100%;
    padding: 10px;
    border: none;
    border-radius: 4px;
    background-color: #28a745;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
    margin-top: 10px;
}

button:hover {
    background-color: #218838;
}


function calcularMedia() {
    // Obtém os valores dos inputs
    var num1 = parseFloat(document.getElementById('num1').value);
    var num2 = parseFloat(document.getElementById('num2').value);
    var num3 = parseFloat(document.getElementById('num3').value);
    var num4 = parseFloat(document.getElementById('num4').value);

    // Verifica se todos os valores são números válidos
    if (isNaN(num1) || isNaN(num2) || isNaN(num3) || isNaN(num4)) {
        document.getElementById('resultado').innerText = 'Por favor, insira todos os números corretamente.';
        return;
    }

    // Calcula a média
    var media = (num1 + num2 + num3 + num4) / 4;

    // Exibe o resultado
    document.getElementById('resultado').innerText = 'A média aritmética é: ' + media.toFixed(2);
}
