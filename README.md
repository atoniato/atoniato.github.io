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
             "Quando lo ritenete opportuno,",
             "A patto che vi sembri una buona idea,",
             "Senza la minima esitazione,",
             "Con una certa dose di sfacciataggine,",
             "Prendendo ad esempio il vostro idolo preferito,",
             "Contando prima fino a tre,",
             "Usando tutto il vostro savoir-che,",
             "Avendo con voi il vostro portafortuna,",
             "Senza dire ah né bah,",
             "Con il vostro miglior atteggiamento zen,",
             "Con uno slancio di generosità,",
             "Senza pensarci due volte,",
             "Mettendo in atto il vostro charme,",
             "Senza temere le conseguenze,"
           ];
           const P2 = [
             "affrettatevi a",
             "abbiate cura di",
             "convincete i vostri cari a",
             "prendete l'iniziativa di",
             "concedetevi la gioia di",
             "liberate un'ora di tempo per",
             "non lasciatevi convincere a",
             "sappiate rinunciare all'idea di",
             "entusiasmatevi a",
             "raccogliete le vostre forze per",
             "realizzate il sogno di",
             "apprestatevi a"
           ];
           const P3 = [
             "rimandare ogni faccenda sgradita.",
             "parlare una lingua straniera.",
             "raccogliere le castagne di notte.",
             "praticare il parkour.",
             "animare una festa a sorpresa.",
             "giocare a un gioco di quando eravate bambina.",
             "riunire a cena un gruppo di vecchi amici.",
             "sorprendere tutti con un'azione inattesa.",
             "partecipare a un concorso di vostra scelta.",
             "mettervi alla guida di un veicolo sconosciuto.",
             "assumere un ruolo di guida sul posto di lavoro.",
             "criticare apertamente ciò che non va.",
             "costruire una rete di solidarietà con persone insospettate.",
             "ampliare il vostro background nella cultura pop.",
             "fare una lezione di prova di un nuovo sport.",
             "organizzare un concerto domestico.",
             "condividere con qualcuno le vostre astuzie.",
             "trasmettere le vostre conoscenze sulla respirazione circolare.",
             "sfatare alcuni luoghi comuni.",
             "ergervi a difensore delle idee sottovalutate."
           ];
           let phrase = [P1[getRandomInt(P1.length)], P2[getRandomInt(P2.length)], P3[getRandomInt(P3.length)]].join(" "); 
           document.getElementById("oroscope").innerHTML = phrase;
        }
    </script>

  </body>
</html>
