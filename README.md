
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8D Infos</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
        }

        .container {
            max-width: 800px;
            margin: auto;
            padding: 15px;
        }

        h1 {
            text-align: center;
            margin-bottom: 5px;
        }

        .beschreibung {
            text-align: center;
            margin-bottom: 20px;
            color: #444;
        }

        .box {
            background-color: #ffffff;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .box h2 {
            margin-top: 0;
            font-size: 18px;
        }

        ul {
            padding-left: 20px;
        }

        li {
            margin-bottom: 8px;
        }

        .fach {
            font-weight: bold;
            margin-top: 10px;
        }

        a {
            color: #0066cc;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        .hinweis {
            font-size: 13px;
            color: #666;
        }

        .timer {
            font-weight: bold;
            color: #d35400;
        }
    </style>
</head>
<body>

<div class="container">

    <h1>📘 8D Infos</h1>
    <p class="beschreibung">
        Hier findest du Hausaufgaben, wichtige Infos und Links.
    </p>

    <!-- Wichtige Infos -->
    <div class="box">
        <h2>📌 Wichtige Infos</h2>
        <ul>
            <li>
                <strong>Schulausfall am 13.07.2026</strong><br>
                Aufgrund starken Wettergeschehens fällt die Schule aus.<br>
                Weitere Infos in der pCloud.
            </li>
            <li>
                Ferien in: <span id="ferien-timer" class="timer">Lade…</span>
            </li>
            <li>Hausaufgaben siehe Abschnitt „Hausaufgaben“.</li>
        </ul>
    </div>

    <!-- Hausaufgaben -->
    <div class="box">
        <h2>📚 Hausaufgaben</h2>

        <p class="fach">🇬🇧 Englisch</p>
        <ul>
            <li>Buch Seite 39 lesen</li>
            <li>Unbekannte Wörter ins Heft schreiben</li>
            <li>Wörter im Wörterbuch nachschlagen</li>
            <li>Aufgaben 2b beantworten</li>
            <li>Highlights des Schuljahres (Task 3a, Seite 39)</li>
            <li>Arbeitsheft Seite 19, Nummer 4</li>
        </ul>

        <p class="fach">💼 Wirtschaft</p>
        <ul>
            <li>
                Aufgaben als PDF:
                <a href="https://e.pcloud.link/publink/show?code=kZ8KugZPx6jOPfKhFm57MtA4Y3zdyY0jclX#/login?folder=13637671092">
                    pCloud öffnen
                </a>
            </li>
        </ul>

        <p class="fach">🇩🇪 Deutsch</p>
        <ul>
            <li>
                Aufgaben als PDF:
                <a href="https://e.pcloud.link/publink/show?code=kZ8KugZPx6jOPfKhFm57MtA4Y3zdyY0jclX#/login?folder=12151147586">
                    pCloud öffnen
                </a>
            </li>
        </ul>

        <p class="fach">➗ Mathe</p>
        <ul>
            <li>Überschrift im Heft: <strong>Oberflächeninhalt Prisma</strong></li>
            <li>Lehrbuch Seite 61 – Infotext abschreiben</li>
            <li>Lehrbuch Seite 60 – Beispiel Nr. 1 mit Lösung</li>
        </ul>
    </div>

    <!-- Externe Links -->
    <div class="box">
        <h2>🔗 Externe Links</h2>
        <ul>
            <li>
                📁 <strong>pCloud (Aufgaben & Dateien):</strong>
                <a href="https://e.pcloud.link/publink/show?code=kZ8KugZPx6jOPfKhFm57MtA4Y3zdyY0jclX#/login?folder=12151147506">
                    Zum Ordner
                </a>
            </li>
            <li>
                🏫 <strong>Schulhomepage:</strong>
                <a href="https://www.sks-voelkerfreundschaft.bildung-lsa.de/">
                    sks-voelkerfreundschaft.bildung-lsa.de
                </a>
            </li>
        </ul>
    </div>

    <!-- Hinweis -->
    <div class="box">
        <p class="hinweis">
            Hinweis: Diese Website ist ein privates Anschauungsprojekt.<br>
            Es wird keine Haftung übernommen für vergessene Arbeitsmittel,
            fehlerhafte oder unvollständige Informationen.<br>
            Verbindliche Informationen findest du ausschließlich
            auf der offiziellen Schulhomepage.
        </p>
    </div>

</div>

<!-- ✅ EINFACHER TIMER BIS ZUM 31. 00:00 -->
<script>
const timerEl = document.getElementById("ferien-timer");

function updateTimer() {
    const now = new Date();

    // Ziel: 31. dieses Monats um 00:00
    const target = new Date(
        now.getFullYear(),
        now.getMonth(),
        31,
        0, 0, 0
    );

    const diff = target - now;

    if (diff <= 0) {
        timerEl.textContent = "🎉 Ferienbeginn!";
        return;
    }

    const tage = Math.floor(diff / (1000 * 60 * 60 * 24));
    const stunden = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minuten = Math.floor((diff / (1000 * 60)) % 60);
    const sekunden = Math.floor((diff / 1000) % 60);

    timerEl.textContent =
        `${tage} Tage, ${stunden} Std, ${minuten} Min, ${sekunden} Sek`;
}

updateTimer();
setInterval(updateTimer, 1000);
</script>

</body>
</html>
