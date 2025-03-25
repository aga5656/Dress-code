<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Losowanie opcji</title>
    <script>
        function losujOpcje() {
            const imieNazwisko = document.getElementById("imieNazwisko").value.trim();
            if (!imieNazwisko) {
                alert("Proszę wpisać swoje imię i nazwisko.");
                return;
            }

            const opcje = ["Star Wars", "Wiosna"];
            const wylosowana = opcje[Math.floor(Math.random() * opcje.length)];
            document.getElementById("wynik").innerHTML = `
                <p><strong>${imieNazwisko}</strong>, wylosowałeś(aś):</p>
                <p style="font-size: 1.5rem; color: blue; font-weight: bold;">${wylosowana}</p>
            `;
        }
    </script>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
            background-color: #f9f9f9;
        }
        input, button {
            padding: 10px;
            font-size: 1rem;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <h1>Losowanie opcji</h1>
    <p>Wpisz swoje imię i nazwisko, a następnie kliknij "Losuj".</p>
    <input type="text" id="imieNazwisko" placeholder="Imię i nazwisko">
    <br>
    <button onclick="losujOpcje()">Losuj</button>
    <div id="wynik" style="margin-top: 20px;"></div>
</body>
</html>
