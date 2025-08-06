<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Deity AI - Iron Companies</title>
  <style>
    body {
      font-family: "Segoe UI", sans-serif;
      background: #0d0f14;
      color: white;
      margin: 0;
      padding: 0;
    }

    header {
      text-align: center;
      padding: 40px 20px;
      background: #1a1f2b;
    }

    .subtitle {
      color: #aaa;
      margin: 10px 0;
    }

    button {
      background: #1e90ff;
      border: none;
      color: white;
      padding: 10px 18px;
      margin-top: 10px;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px;
    }

    .chat-container {
      max-width: 600px;
      margin: 40px auto;
      padding: 20px;
      background: #1a1a1a;
      border-radius: 10px;
    }

    #chat-log {
      max-height: 300px;
      overflow-y: auto;
      margin-bottom: 10px;
      background: #121212;
      padding: 10px;
      border-radius: 6px;
    }

    textarea {
      width: 100%;
      height: 80px;
      resize: none;
      border-radius: 6px;
      border: none;
      padding: 10px;
      font-size: 14px;
    }

    footer {
      text-align: center;
      padding: 20px;
      color: #777;
      background: #0d0f14;
    }

    .deity-tag {
      color: #1e90ff;
    }

    .message {
      margin: 5px 0;
    }
  </style>
</head>
<body>

  <header>
    <h1>Deity AI Assistant</h1>
    <p class="subtitle">Explain your app. Get it generated. No code needed.</p>
    <button onclick="location.href='#'">Learn Ironscript</button>
  </header>

  <main>
    <div class="chat-container">
      <div id="chat-log"></div>
      <textarea id="user-input" placeholder="Describe your app idea..."></textarea>
      <button onclick="handleUserInput()">Send</button>
    </div>
  </main>

  <footer>
    <p>&copy; 2025 Iron Companies — Powered by <span class="deity-tag">Deity AI</span></p>
  </footer>

  <script>
    function handleUserInput() {
      const inputBox = document.getElementById("user-input");
      const chatLog = document.getElementById("chat-log");
      const userMessage = inputBox.value.trim();

      if (!userMessage) return;

      // Show user message
      chatLog.innerHTML += `<div class="message"><strong>You:</strong> ${userMessage}</div>`;

      // Simulated Deity AI response (placeholder for now)
      const deityResponse = generateAppStub(userMessage);
      setTimeout(() => {
        chatLog.innerHTML += `<div class="message"><strong>Deity:</strong> ${deityResponse}</div>`;
        chatLog.scrollTop = chatLog.scrollHeight;
      }, 600);

      inputBox.value = "";
    }

    function generateAppStub(idea) {
      // This is just a mock. Replace with real AI later.
      return `Building your "<em>${idea}</em>" app...<br>🧠 Deity is designing the structure, code, and features now. Stay tuned!`;
    }
  </script>

</body>
</html>
