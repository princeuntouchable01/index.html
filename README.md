# index.html<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TECH PRO - Learn Python & Career Journey</title>
  <style>
    body {
      font-family: "Segoe UI", sans-serif;
      background: linear-gradient(135deg, #0d0d0d, #1a1a1a);
      color: #fff;
      margin: 0;
      padding: 0;
    }
    header {
      background: #111;
      padding: 25px;
      text-align: center;
      box-shadow: 0 0 20px #00ffcc;
    }
    header h1 {
      color: #00ffcc;
      font-size: 3em;
      margin: 0;
      animation: glow 2s infinite alternate;
    }
    @keyframes glow {
      from { text-shadow: 0 0 10px #00ffcc; }
      to { text-shadow: 0 0 25px #ff0099; }
    }
    nav {
      margin-top: 15px;
    }
    nav a {
      color: #00ffcc;
      margin: 0 20px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }
    nav a:hover {
      color: #ff0099;
      text-shadow: 0 0 10px #ff0099;
    }
    section {
      padding: 50px;
      text-align: center;
    }
    section h2 {
      font-size: 2.5em;
      color: #00ffcc;
      margin-bottom: 20px;
    }
    .lesson, .career, .contact-card, .python-editor {
      background: #1a1a1a;
      margin: 20px auto;
      padding: 25px;
      border-radius: 15px;
      max-width: 700px;
      box-shadow: 0 0 15px #00ffcc;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .lesson:hover, .career:hover, .contact-card:hover, .python-editor:hover {
      transform: scale(1.03);
      box-shadow: 0 0 25px #ff0099;
    }
    pre {
      background: #0d0d0d;
      padding: 15px;
      border-radius: 8px;
      text-align: left;
      overflow-x: auto;
      color: #00ffcc;
    }
    .contact-card a {
      display: inline-block;
      margin: 10px;
      padding: 10px 20px;
      border-radius: 30px;
      background: #00ffcc;
      color: #0d0d0d;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }
    .contact-card a:hover {
      background: #ff0099;
      color: #fff;
    }
    textarea {
      width: 100%;
      height: 150px;
      background: #0d0d0d;
      color: #00ffcc;
      border: none;
      border-radius: 10px;
      padding: 10px;
      font-family: monospace;
      font-size: 16px;
      resize: vertical;
    }
    button {
      margin-top: 10px;
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      background: #00ffcc;
      color: #0d0d0d;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #ff0099;
      color: #fff;
    }
    #output {
      background: #111;
      margin-top: 15px;
      padding: 15px;
      border-radius: 10px;
      text-align: left;
      min-height: 50px;
      color: #00ffcc;
      overflow-x: auto;
    }
    footer {
      background: #111;
      padding: 20px;
      text-align: center;
      font-size: 0.9em;
      color: #888;
    }
  </style>
  <!-- Include Skulpt library -->
  <script src="https://cdn.jsdelivr.net/npm/skulpt@1.2.0/skulpt.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/skulpt@1.2.0/skulpt-stdlib.js"></script>
</head>
<body>
  <header>
    <h1>🚀 TECH PRO</h1>
    <p>Learn Python | My Journey to Becoming a Cyber Engineer</p>
    <nav>
      <a href="#home">Home</a>
      <a href="#python">Learn Python</a>
      <a href="#career">My Career</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome!</h2>
    <p>Hi, I'm <b>Prince Destiny</b> — aka <b>TECH PRO</b>.  
       This app teaches Python basics while sharing my dream of becoming a Cyber Engineer. 🚀</p>
  </section>

  <section id="python">
    <h2>Learn Python</h2>
    <div class="lesson">
      <h3>👉 Lesson 1: Print</h3>
      <pre>print("Hello World!")</pre>
    </div>
    <div class="lesson">
      <h3>👉 Lesson 2: Variables</h3>
      <pre>x = 10
y = 5
print(x + y)</pre>
    </div>
    <div class="lesson">
      <h3>👉 Lesson 3: Loops</h3>
      <pre>for i in range(5):
    print("Loop", i)</pre>
    </div>

    <div class="python-editor">
      <h3>💻 Try Python Code</h3>
      <textarea id="python-code">print("Hello from TECH PRO!")</textarea>
      <br>
      <button onclick="runPython()">Run Code</button>
      <div id="output"></div>
    </div>
  </section>

  <section id="career">
    <h2>My Career Journey</h2>
    <div class="career">
      <p>My name is <b>Prince Destiny</b>, aka <b>TECH PRO</b>.  
      I am passionate about <b>Cyber Engineering</b> — securing networks, building apps, and creating tools that solve real problems.</p>
      <p>My vision: become a leading Cyber Engineer, build software that changes lives, and train young minds in tech.  
      TECH PRO is more than a name — it’s my mission 💡.</p>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <div class="contact-card">
      <p>Let’s connect and build the future together:</p>
      <a href="#">📱 WhatsApp</a>
      <a href="#">📷 Instagram</a>
      <a href="#">📘 Facebook</a>
    </div>
  </section>

  <footer>
    <p>© 2025 TECH PRO | Built with ❤️ by Prince Destiny</p>
  </footer>

  <script>
    function builtinRead(x) {
      if (Sk.builtinFiles === undefined || Sk.builtinFiles["files"][x] === undefined)
          throw "File not found: '" + x + "'";
      return Sk.builtinFiles["files"][x];
    }

    function runPython() {
      const code = document.getElementById("python-code").value;
      const outputDiv = document.getElementById("output");
      outputDiv.innerHTML = "";
      Sk.configure({output: function(text){outputDiv.innerHTML += text}, read: builtinRead});
      (Sk.TurtleGraphics || (Sk.TurtleGraphics = {})).target = 'output';
      const myPromise = Sk.misceval.asyncToPromise(function() {
        return Sk.importMainWithBody("<stdin>", false, code, true);
      });
      myPromise.then(function(mod) {
          console.log('Code ran successfully');
      },
      function(err) {
          outputDiv.innerHTML = err.toString();
      });
    }
  </script>
</body>
</html>
