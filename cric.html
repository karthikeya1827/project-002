<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Live Cricket Scoreboard Enhanced</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: #f0f0f0;
            color: #333; 
            margin: 0;
            padding: 20px;
        }
        .scoreboard-container {
            background: #fff;
            border-radius: 20px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            padding: 20px;
            max-width: 800px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: 460px;
        }
        .scoreboard {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-grow: 1;
        }
        .team {
            font-size: 24px;
            font-weight: bold;
            display: flex;
            align-items: center;
            margin: 0 10px;
        }
        .team img {
            width: 50px;
            height: 50px;
            margin-right: 10px;
        }
        .score {
            font-size: 30px;
            margin: 0 20px;
            white-space: nowrap;
        }
        .highlight {
            font-size: 28px;
            font-weight: bold;
            display: none;
            margin-top: 10px;
        }
        .four-animation { color: blue; }
        .six-animation { color: green; }
        .wicket-animation { color: red; }
        .freehit-animation { color: orange; }
        .wide-animation { color: purple; }
        .noball-animation { color: darkorange; }
        .player-info {
            margin-top: 20px;
            font-size: 18px;
        }
        .run-rate {
            margin-top: 10px;
            font-size: 16px;
            color: #555;
        }
        button {
            padding: 10px 16px;
            margin: 5px 8px;
            font-size: 16px;
            cursor: pointer;
            background: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            min-width: 90px;
            transition: background 0.3s ease;
        }
        button:hover {
            background: #0056b3;
        }
        .buttons-container {
            margin-top: auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 5px 12px;
        }
        .extra-wicket-buttons {
            margin: 10px auto 0 auto;
            display: none;
            flex-wrap: wrap;
            justify-content: center;
            gap: 5px 12px;
        }
        .extra-wicket-buttons button {
            background: #dc3545;
        }
        .extra-wicket-buttons button:hover {
            background: #a71d2a;
        }
    </style>
</head>
<body>

    <h1>Live Cricket Scoreboard</h1>
    <div class="scoreboard-container">
        <div class="scoreboard" aria-label="Match score">
            <div class="team" aria-label="India">
                <img src="./indiac-logo-png-transparent.png" alt="India Logo"> 
                <span>IND</span>
            </div>
            <span class="score" id="runs" aria-live="polite">0</span>/<span class="score" id="wickets" aria-live="polite">0</span> 
            (Overs: <span id="overs" aria-live="polite">0.0</span>)
            <div class="team" aria-label="Australia">
                <img src="./OIP.jpeg" alt="Australia Logo"> 
                <span>AUS</span>
            </div>
        </div>

        <div class="player-info" aria-label="Player information">
            <p>Batsmen: Rohit Sharma (IND), Virat Kohli (IND)</p>
            <p>Bowler: Mitchell Starc (AUS)</p>
        </div>

        <div class="run-rate" aria-live="polite">
            Run Rate: <span id="runRate">0.00</span>
        </div>

        <p id="fourAnimation" class="highlight four-animation" role="alert" aria-live="assertive">FOUR! 🔵</p>
        <p id="sixAnimation" class="highlight six-animation" role="alert" aria-live="assertive">SIX! 🟢</p>
        <p id="wicketAnimation" class="highlight wicket-animation" role="alert" aria-live="assertive">WICKET! 🏏</p>
        <p id="freeHitAnimation" class="highlight freehit-animation" role="alert" aria-live="assertive">FREE HIT! ⚡</p>
        <p id="wideAnimation" class="highlight wide-animation" role="alert" aria-live="assertive">WIDE! ⚠️</p>
        <p id="noBallAnimation" class="highlight noball-animation" role="alert" aria-live="assertive">NO BALL! 🚫</p>

        <div class="buttons-container" role="group" aria-label="Score update controls">
            <button id="runs1Btn" onclick="updateScore(1, 'run')" aria-label="Add 1 run">1 Run</button>
            <button id="runs2Btn" onclick="updateScore(2, 'run')" aria-label="Add 2 runs">2 Runs</button>
            <button id="runs3Btn" onclick="updateScore(3, 'run')" aria-label="Add 3 runs">3 Runs</button>
            <button id="runs4Btn" onclick="updateScore(4, 'run')" aria-label="Add 4 runs">4 Runs</button>
            <button id="runs6Btn" onclick="updateScore(6, 'run')" aria-label="Add 6 runs">6 Runs</button>
            <button id="wicketBtn" onclick="showExtraWicketButtons()" aria-label="Wicket">Wicket</button>
            <button id="wideBtn" onclick="updateScore(1, 'wide')" aria-label="Wide ball">Wide</button>
            <button id="noBallBtn" onclick="updateScore(1, 'noball')" aria-label="No ball">No Ball</button>
        </div>

        <div id="extraWicketBtns" class="extra-wicket-buttons" role="group" aria-label="Wicket plus runs options">
            <button onclick="handleExtraWicketRun(0)" aria-label="Wicket plus 0 runs">Wicket +0 Runs</button>
            <button onclick="handleExtraWicketRun(1)" aria-label="Wicket plus 1 run">Wicket +1 Run</button>
            <button onclick="handleExtraWicketRun(2)" aria-label="Wicket plus 2 runs">Wicket +2 Runs</button>
            <button onclick="handleExtraWicketRun(3)" aria-label="Wicket plus 3 runs">Wicket +3 Runs</button>
            <button onclick="hideExtraWicketButtons()" aria-label="Cancel wicket adjustment" style="background:#6c757d;">Cancel</button>
        </div>
    </div>

    <script>
        let totalRuns = 0, totalBalls = 0, totalOvers = 0, totalWickets = 0;
        let freeHit = false;
        let noBallTimeout = null;
        let waitingWicketExtraInput = false; // When wicket button clicked to show extra buttons

        const extraWicketContainer = document.getElementById('extraWicketBtns');
        const buttonsContainer = document.querySelector('.buttons-container');
        const wicketBtn = document.getElementById('wicketBtn');

        function updateScore(value, type) {
            if (waitingWicketExtraInput) {
                // Disable all other updates while waiting for extra wicket input
                return;
            }
            clearTimeout(noBallTimeout);
            switch(type) {
                case 'run':
                    totalRuns += value;
                    totalBalls++;
                    if (value === 4) animateEvent("fourAnimation");
                    else if (value === 6) animateEvent("sixAnimation");
                    if (totalBalls % 6 === 0) totalOvers++;
                    if(freeHit) {
                        freeHit = false;
                        animateEvent("freeHitAnimation", false);
                    }
                    break;
                case 'wicket':
                    if(freeHit) {
                        // On a free hit ball, wicket is not allowed, treated as 0 runs though user must click extra wicket+runs buttons to add runs
                        waitingWicketExtraInput = true;
                        showExtraWicketButtons();
                        animateEvent("wicketAnimation");
                    } else {
                        totalWickets++;
                        totalBalls++;
                        animateEvent("wicketAnimation");
                        if (totalBalls % 6 === 0) totalOvers++;
                        waitingWicketExtraInput = true;
                        showExtraWicketButtons();
                    }
                    break;
                case 'wide':
                    totalRuns += value; // 1 run extra
                    animateEvent("wideAnimation");
                    // Wide doesn't count as ball or affect freeHit
                    break;
                case 'noball':
                    totalRuns += value; // 1 run extra
                    animateEvent("noBallAnimation");
                    noBallTimeout = setTimeout(() => {
                        freeHit = true;
                        animateEvent("freeHitAnimation");
                    }, 1000);
                    break;
            }
            updateDisplay();
        }

        function updateDisplay() {
            document.getElementById("runs").innerText = totalRuns;
            document.getElementById("wickets").innerText = totalWickets;
            let overs = totalOvers + "." + (totalBalls % 6);
            document.getElementById("overs").innerText = overs;

            let runRate = totalBalls > 0 ? (totalRuns / (totalBalls / 6)).toFixed(2) : "0.00";
            document.getElementById("runRate").innerText = runRate;
        }

        function animateEvent(elementId, show = true) {
            const element = document.getElementById(elementId);
            if(show) {
                element.style.display = "block";
                setTimeout(() => element.style.display = "none", 2000);
            } else {
                element.style.display = "none";
            }
        }

        function showExtraWicketButtons() {
            buttonsContainer.style.display = 'none';
            extraWicketContainer.style.display = 'flex';
        }

        function hideExtraWicketButtons() {
            extraWicketContainer.style.display = 'none';
            buttonsContainer.style.display = 'flex';
            waitingWicketExtraInput = false;
        }

        function handleExtraWicketRun(extraRuns) {
            if (freeHit) {
                // During free hit ball wicket cannot fall
                // Add extra runs only, no wicket increment
                totalRuns += extraRuns;
                // free hit ends after this ball
                freeHit = false;
                animateEvent("freeHitAnimation", false);
            } else {
                // Normal ball wicket + extra runs
                totalWickets++;
                totalRuns += extraRuns;
                // increment balls for the ball on which wicket happened (already incremented in main wicket click)
                // So we do not increment ball count here again
                animateEvent("wicketAnimation");
            }
            hideExtraWicketButtons();
            updateDisplay();
        }
    </script>

</body>
</html>
