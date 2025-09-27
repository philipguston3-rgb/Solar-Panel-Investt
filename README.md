# Solar-Panel-Investt
Solar-Panel-Invest
<!DOCTYPE html><html lang="ro">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Investițiți în Panouri Solare</title>
  <link rel="stylesheet" href="style.css">
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f7fa;
      color: #333;
    }
    header {
      background: linear-gradient(to right, #00aaff, #0077cc);
      color: white;
      padding: 60px 20px;
      text-align: center;
    }
    header h1 {
      margin: 0 0 10px;
      font-size: 2.5em;
    }
    header p {
      font-size: 1.2em;
      margin-bottom: 20px;
    }
    .cta-btn {
      background: #ffcc00;
      color: #333;
      padding: 15px 30px;
      border: none;
      border-radius: 8px;
      font-size: 1.1em;
      cursor: pointer;
      transition: 0.3s;
    }
    .cta-btn:hover {
      background: #ffaa00;
    }
    .container {
      max-width: 1000px;
      margin: 40px auto;
      padding: 20px;
    }
    .section {
      background: white;
      padding: 30px;
      margin-bottom: 40px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .section h2 {
      margin-top: 0;
      color: #0077cc;
    }
    .calculator input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1em;
    }
    .calculator button {
      width: 100%;
      padding: 14px;
      background: #00aaff;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 1.1em;
      cursor: pointer;
      transition: 0.3s;
    }
    .calculator button:hover {
      background: #0077cc;
    }
    .result {
      margin-top: 20px;
      font-weight: bold;
      font-size: 1.2em;
      color: #333;
      text-align: center;
    }
    footer {
      background: #333;
      color: #eee;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Investește în Energie Verde</h1>
    <p>Cumpără un panou solar și câștigă din energia produsă!</p>
    <button class="cta-btn" onclick="document.getElementById('calculator').scrollIntoView({behavior:'smooth'});">Calculează Profitul</button>
  </header>  <div class="container">
    <div class="section">
      <h2>Cum Funcționează</h2>
      <p>1. Alegi câte panouri cumperi<br>
         2. Noi le instalăm în parcul fotovoltaic<br>
         3. Primești lunar profit direct în contul tău</p>
    </div><div class="section calculator" id="calculator">
  <h2>Calculator de Profit</h2>
  <label for="investitie">Sumă investită (€)</label>
  <input type="number" id="investitie" placeholder="Ex: 1000">
  <button onclick="calculeazaProfit()">Calculează</button>
  <div class="result" id="rezultat"></div>
</div>

<div class="section">
  <h2>Contact</h2>
  <p>Pentru a investi sau pentru detalii suplimentare, trimite-ne un email la <a href="mailto:invest@panouri-solar.ro">invest@panouri-solar.ro</a>.</p>
</div>

  </div>  <footer>
    &copy; 2025 Investițiți Panouri Solare. Toate drepturile rezervate.
  </footer>  <script>
    function calculeazaProfit(){
      const investitie = parseFloat(document.getElementById('investitie').value);
      const rezultat = document.getElementById('rezultat');
      if(isNaN(investitie) || investitie <= 0){
        rezultat.innerText = "Introduceți o sumă validă!";
        return;
      }
      // Exemplu: profit anual ~10% din investiție, lunar ~0.83%
      const profitLunar = investitie * 0.0083;
      const profitAnual = investitie * 0.10;
      rezultat.innerText = `Profit estimat: ~${profitLunar.toFixed(2)} €/lună sau ${profitAnual.toFixed(2)} €/an`;
    }
  </script></body>
</html>
