<html>
  <head>
    <style>
      button {
        vertical-align: middle; 
        padding: 5px 10px;
        font-family: 'Courier New', monospace;
        font-size: 20px;
        background-color: #ffa952;
        color: #feffdf;
        border-radius: 5px;
        border: none;
        transition-duration: 0.4s;
      }
      button:hover {
        background-color: #ef5a5a;
      }
      body {
        background-color: #feffdf;
      }
      h1 {
        color: #ffa952;
        text-align: center;
        font-family: 'Courier New', monospace;
        font-size: 40px;
      }
      
      p {
        font-family: 'Courier New', monospace;
        font-size: 20px;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>Bilancia 2025/2026</h1>
    <div style="vertical-align: middle;">
        <div class="container-lg px-3 my-5 markdown-body" style="text-align: center;">
            <img src="{{site.url}}/images/logoBB.png" style="max-width:50%; height:auto; mix-blend-mode: multiply;">
        </div>
        <p id="oroscope"></p>
        <p id="date"></p>
        <div class="container-lg px-3 my-5 markdown-body" style="text-align: center;">
            <button onclick="Oroscopo()">Genera Oroscopo</button>
        </div>
    </div>

    <script>
        function getRandomInt(max) {
          return Math.floor(Math.random() * max); 
        }
        function Oroscopo() {
           let dd = new Date();
           document.getElementById("date").innerHTML = dd.toLocaleDateString();
           const P1 = [
             "Nelle notti di luna nuova,",
             "Quando lo ritenete opportuno,"
           ];
           const P2 = [
             "dedicatevi a",
             "affrettatevi a",
             "abbiate cura di",
             "convincete i vostri cari a"
           ];
           const P3 = [
             "rimandare ogni faccenda sgradita.",
             "parlare una lingua straniera.",
             "raccogliere le castagne di notte.",
             "praticare il parkour."
           ];
           let phrase = [P1[getRandomInt(P1.length)], P2[getRandomInt(P2.length)], P3[getRandomInt(P3.length)]].join(" "); 
           document.getElementById("oroscope").innerHTML = phrase;
        }
    </script>

  </body>
</html>
