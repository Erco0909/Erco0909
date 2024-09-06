<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sayı Tahmin Oyunu</title>
</head>
<body>
    <h1>Sayı Tahmin Oyunu</h1>
    <p>1 ile 100 arasında bir sayı tahmin edin:</p>
    <input type="number" id="guess" />
    <button onclick="checkGuess()">Tahmin Et</button>
    <p id="result"></p>

    <script>
        const number = Math.floor(Math.random() * 100) + 1;

        function checkGuess() {
            const guess = parseInt(document.getElementById('guess').value);
            const result = document.getElementById('result');
            
            if (guess < number) {
                result.textContent = 'Daha büyük bir sayı tahmin et!';
            } else if (guess > number) {
                result.textContent = 'Daha küçük bir sayı tahmin et!';
            } else {
                result.textContent = `Tebrikler! Doğru tahmin. Sayı ${number} idi.`;
            }
        }
    </script>
</body>
</html>

