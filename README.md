<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Calculator Project - C#</title>
  <meta name="description" content="Basic C# Calculator (Windows Forms) demonstrating addition, subtraction, multiplication & division. GUI design, event handling & C# fundamentals — beginner friendly." />
  <style>
    :root{
      --bg:#f7f9fc; --card:#ffffff; --accent:#0b63d6; --muted:#6b7280;
      font-family: Inter, Roboto, -apple-system, "Segoe UI", "Helvetica Neue", Arial;
    }
    body{margin:0;padding:32px;background:var(--bg);color:#111;}
    .container{max-width:880px;margin:0 auto;}
    header{display:flex;align-items:center;gap:16px;margin-bottom:20px;}
    .logo{width:64px;height:64px;border-radius:8px;background:linear-gradient(135deg,var(--accent),#19a3ff);display:flex;align-items:center;justify-content:center;color:#fff;font-weight:700;font-size:20px}
    h1{margin:0;font-size:24px}
    p.lead{margin:8px 0 20px;color:var(--muted)}
    .card{background:var(--card);padding:20px;border-radius:10px;box-shadow:0 6px 20px rgba(15,23,42,0.06);margin-bottom:16px}
    ul{margin:8px 0 0;padding-left:20px;color:var(--muted)}
    code.block{display:block;background:#0f1724;color:#e6eef8;padding:12px;border-radius:6px;overflow:auto;font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", monospace}
    .buttons{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
    .btn{padding:8px 12px;border-radius:8px;border:0;background:var(--accent);color:#fff;cursor:pointer;text-decoration:none;display:inline-block}
    .secondary{background:#eef2ff;color:#0b3f91}
    footer{margin-top:18px;color:var(--muted);font-size:13px}
    @media (max-width:520px){header{flex-direction:column;align-items:flex-start}.logo{width:56px;height:56px}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">CALC</div>
      <div>
        <h1>Calculator Project — C# (Windows Forms)</h1>
        <p class="lead">A beginner-friendly desktop calculator built with C# and .NET Framework. Demonstrates GUI design, event handling, and basic arithmetic operations.</p>
      </div>
    </header>

    <section class="card">
      <h2>🔧 Features</h2>
      <ul>
        <li>Addition, Subtraction, Multiplication, Division</li>
        <li>Clear / Backspace functionality</li>
        <li>Keyboard input support (numeric & operators)</li>
        <li>Simple and responsive Windows Forms GUI</li>
      </ul>
    </section>

    <section class="card">
      <h2>💻 Technologies</h2>
      <ul>
        <li>C# (Windows Forms Application)</li>
        <li>.NET Framework (specify your target version in README)</li>
        <li>Visual Studio (recommended)</li>
      </ul>
    </section>

    <section class="card">
      <h2>⚙️ Installation & Run</h2>
      <ol>
        <li>Clone this repository to your machine.</li>
        <li>Open the solution (`.sln`) in Visual Studio.</li>
        <li>Build the solution (Build → Build Solution).</li>
        <li>Run the project (F5) to launch the calculator app.</li>
      </ol>
    </section>

    <section class="card">
      <h2>📂 Example README snippet (copy to your repo)</h2>
      <pre class="block">
Poltray C# Calculator
A simple calculator desktop app built with C# (Windows Forms). Supports basic arithmetic: + - × ÷. Good for beginners learning GUI and event-driven programming in C#.

Run:
1. Open in Visual Studio
2. Build & Run (F5)
      </pre>
    </section>

    <section class="card">
      <h2>🧾 Sample Code (button click handler)</h2>
      <pre class="block">
// Example C# event handler for '=' button
private void btnEquals_Click(object sender, EventArgs e)
{
    try {
        double a = double.Parse(txtDisplay.Tag?.ToString() ?? "0"); // previous value stored in Tag
        double b = double.Parse(txtDisplay.Text);
        string op = currentOperator; // set when user clicks + - * /
        double result = 0;

        switch(op){
            case "+": result = a + b; break;
            case "-": result = a - b; break;
            case "*": result = a * b; break;
            case "/": result = b != 0 ? a / b : throw new DivideByZeroException();
        }
        txtDisplay.Text = result.ToString();
        txtDisplay.Tag = null;
    } catch(Exception ex) {
        MessageBox.Show("Error: " + ex.Message);
    }
}
      </pre>
    </section>

    <div class="card">
      <h2>✍️ Tips</h2>
      <ul>
        <li>Include screenshots in your GitHub README for better presentation.</li>
        <li>Mention the .NET target version and Visual Studio edition used.</li>
        <li>Add keyboard support and input validation to improve UX.</li>
      </ul>
      <div class="buttons" style="margin-top:12px">
        <a class="btn" href="#" onclick="alert('Copy the README snippet from the page.')">Copy README Snippet</a>
        <a class="btn secondary" href="#" onclick="alert('Add screenshots to your repo under /screenshots')">Add Screenshots</a>
      </div>
    </div>

    <footer>
      Created for learning C# and Windows Forms. Feel free to edit the text and adapt it to your repository.
    </footer>
  </div>
</body>
</html>
