<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gigi's Gelato Samples</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #fefcfb;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
      font-size: 2.5em;
      color: #e64b3c;
    }
    h2 {
      text-align: center;
      color: #333;
    }
    .card {
      background: #fff;
      border-radius: 16px;
      padding: 20px;
      margin: 20px auto;
      max-width: 700px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    button {
      background: #ff6b6b;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      margin-top: 10px;
    }
    button:hover {
      background: #e64b3c;
    }
    p.result {
      margin-top: 15px;
      font-size: 18px;
      font-weight: bold;
      color: #444;
    }
    ul {
      line-height: 1.6;
    }
    textarea {
      width: 100%;
      height: 100px;
      margin-top: 10px;
      border-radius: 8px;
      padding: 10px;
      font-size: 14px;
      border: 1px solid #ddd;
    }
    .icecream-row {
      text-align: center;
      font-size: 2em;
      margin: 10px 0;
    }
  </style>
</head>
<body>
  <h1>🍦 Gigi's Gelato Samples 🍦</h1>
  <div class="icecream-row">🍨 🍧 🍦 🍩 🍦 🍧 🍨</div>

  <div class="card">
    <h2>🎯 Topic of the Week</h2>
    <p>Enter upsell/cross-sell opportunities (one per line):</p>
    <textarea id="topicsInput">Upsell → Plus
Upsell → Premium
Cross-sell → Health Insurance
Cross-sell → 401(k)
Cross-sell → Time Tracking
Cross-sell → Next-Day Direct Deposit
Cross-sell → HR Resources Add-on
Cross-sell → Priority Support Add-on</textarea>
    <br/>
    <button onclick="spinTopic()">Spin Topic Wheel</button>
    <p id="topicResult" class="result"></p>
  </div>

  <div class="card">
    <h2>🛞 Teammate Spotlight</h2>
    <p>Enter teammate names (one per line):</p>
    <textarea id="teammatesInput">Brian Aylward
Britt Humxn
ChyAnne Braxton
Ely Ganzhina
Fallon Short
Juan Zamorano
Kaylynn Cervantes
Khadijah Crittenden
Laura Rodosky
Shaylen Piper
Stephanie Ha</textarea>
    <br/>
    <button onclick="spinTeammate()">Spin Teammate Wheel</button>
    <p id="teammateResult" class="result"></p>
  </div>

  <div class="card">
    <h2>📋 Call Review Template</h2>
    <ul>
      <li><strong>Call Context:</strong> Who was the customer? What product(s) were discussed?</li>
      <li><strong>Topic Lens:</strong> Did the rep recognize the upsell/cross-sell opportunity? Was it positioned clearly?</li>
      <li><strong>Strengths:</strong> What went well?</li>
      <li><strong>Opportunities:</strong> Where could it be stronger?</li>
      <li><strong>Takeaway:</strong> One best practice for the team.</li>
    </ul>
  </div>

  <div class="icecream-row">🍦 🍨 🍧 🍦 🍩 🍧 🍨 🍦</div>

  <script>
    function spinTopic() {
      const topicsText = document.getElementById("topicsInput").value.trim();
      const topics = topicsText.split(/\n/).map(t => t.trim()).filter(t => t);
      if (topics.length === 0) {
        alert("Please enter at least one topic.");
        return;
      }
      const choice = topics[Math.floor(Math.random() * topics.length)];
      document.getElementById("topicResult").textContent = "👉 " + choice;
    }

    function spinTeammate() {
      const teammatesText = document.getElementById("teammatesInput").value.trim();
      const teammates = teammatesText.split(/\n/).map(t => t.trim()).filter(t => t);
      if (teammates.length === 0) {
        alert("Please enter at least one teammate.");
        return;
      }
      const choice = teammates[Math.floor(Math.random() * teammates.length)];
      document.getElementById("teammateResult").textContent = "🎤 " + choice;
    }
  </script>
</body>
</html>
