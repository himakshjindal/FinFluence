# FinFluence
A friendly financial literacy resource for students in Class 9–12. Simple lessons, activities and tools to build healthy money habits.
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Fin-Fluence — Learn Money. Live Smart.</title>
  <meta name="description" content="Financial literacy for Class 9-12 students. Budgeting, banking, digital safety, investing, games and more." />
  <style>
    :root{--accent:#246bfb;--muted:#6b7280;--bg:#f7f9fc;--card:#ffffff}
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; margin:0; background:var(--bg); color:#0f172a; line-height:1.5}
    .container{max-width:1100px;margin:32px auto;padding:20px}
    header{display:flex;align-items:center;justify-content:space-between;gap:12px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:56px;height:56px;background:linear-gradient(135deg,var(--accent),#7c3aed);border-radius:12px;display:grid;place-items:center;color:#fff;font-weight:700}
    nav a{margin:0 8px;color:var(--muted);text-decoration:none}
    nav a:hover{color:var(--accent)}
    .hero{display:flex;gap:20px;align-items:center;margin-top:22px}
    .hero .left{flex:1}
    .card{background:var(--card);padding:18px;border-radius:14px;box-shadow:0 6px 18px rgba(12,20,40,0.06)}
    .cta{display:inline-block;background:var(--accent);color:#fff;padding:10px 14px;border-radius:10px;text-decoration:none}
    section{margin-top:18px}
    h1,h2,h3{margin:0 0 10px 0}
    p{margin:0 0 12px 0;color:#111827}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:14px}
    ul{padding-left:18px}
    .small{color:var(--muted);font-size:0.95rem}
    footer{margin:30px 0 80px 0;text-align:center;color:var(--muted)}
    /* Interactive widgets */
    .widget-row{display:flex;gap:14px;flex-wrap:wrap}
    input,select,button,textarea{font-family:inherit}
    .form-row{display:flex;gap:10px;align-items:center}
    .field{padding:8px;border-radius:8px;border:1px solid #e6e9ef;width:100%}
    .quiz .option{padding:10px;border-radius:10px;border:1px dashed #e6e9ef;margin:8px 0;cursor:pointer}
    .quiz .option:hover{border-style:solid}
    .hidden{display:none}
    @media(max-width:720px){.hero{flex-direction:column-reverse}.hero .left,.hero .right{width:100%}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">FF</div>
        <div>
          <div style="font-weight:700">Fin-Fluence</div>
          <div class="small">Learn Money. Live Smart. (Class 9–12)</div>
        </div>
      </div>
      <nav>
        <a href="#basics">Basics</a>
        <a href="#budgeting">Budgeting</a>
        <a href="#banking">Banking</a>
        <a href="#digital">Safety</a>
        <a href="#invest">Investing</a>
        <a href="#activities">Activities</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="left">
          <div class="card">
            <h1>Welcome to Fin‑Fluence</h1>
            <p class="small">A friendly financial literacy resource for students in Class 9–12. Simple lessons, activities and tools to build healthy money habits.</p>
            <p><a class="cta" href="#activities">Start Interactive Activities</a></p>
            <div style="margin-top:12px;display:flex;gap:10px">
              <div class="card small" style="padding:10px">Track pocket money</div>
              <div class="card small" style="padding:10px">Learn digital safety</div>
              <div class="card small" style="padding:10px">Try savings calculator</div>
            </div>
          </div>
        </div>
        <div class="right" style="width:360px">
          <div class="card">
            <h3>Quick Tips</h3>
            <ul class="small">
              <li>Save at least 10% of your pocket money</li>
              <li>Verify links before clicking</li>
              <li>Compare prices before buying</li>
              <li>Start SIP with small amounts</li>
            </ul>
          </div>
        </div>
      </section>

      <section id="basics">
        <div class="card">
          <h2>Basic Money Concepts</h2>
          <p class="small">Understand money, needs vs wants, income, expenses and why saving matters.</p>
          <div class="grid" style="margin-top:12px">
            <div>
              <h3>What is money?</h3>
              <p class="small">A medium to buy things and save for future needs.</p>
            </div>
            <div>
              <h3>Needs vs Wants</h3>
              <p class="small">Needs = essentials. Wants = non-essential items. Learn to prioritise.</p>
            </div>
            <div>
              <h3>Income & Expenses</h3>
              <p class="small">Money from allowance, gifts, part-time work. Track where it goes.</p>
            </div>
            <div>
              <h3>Saving</h3>
              <p class="small">Put money aside regularly — small amounts add up.</p>
            </div>
          </div>
        </div>
      </section>

      <section id="budgeting">
        <div class="card">
          <h2>Smart Budgeting & Pocket Money Management</h2>
          <p class="small">A simple monthly budget helps you reach your goals.</p>
          <div style="margin-top:10px" class="widget-row">
            <div style="flex:1;min-width:260px" class="card">
              <h3>Budget Planner</h3>
              <div class="form-row">
                <label style="min-width:120px">Total Income (₹)</label>
                <input id="income" class="field" type="number" value="1000" />
              </div>
              <div style="height:8px"></div>
              <div class="form-row">
                <label style="min-width:120px">Planned Savings (₹)</label>
                <input id="saveAmt" class="field" type="number" value="200" />
              </div>
              <div style="height:8px"></div>
              <button onclick="calcBudget()" class="cta">Calculate</button>
              <div id="budgetRes" style="margin-top:10px" class="small"></div>
            </div>

            <div style="flex:1;min-width:260px" class="card">
              <h3>Savings Goal Planner</h3>
              <div class="form-row">
                <label style="min-width:120px">Goal (₹)</label>
                <input id="goalAmt" class="field" type="number" placeholder="e.g. 5000" />
              </div>
              <div style="height:8px"></div>
              <div class="form-row">
                <label style="min-width:120px">Monthly Save (₹)</label>
                <input id="goalSave" class="field" type="number" placeholder="e.g. 300" />
              </div>
              <div style="height:8px"></div>
              <button onclick="calcGoal()" class="cta">Plan</button>
              <div id="goalRes" style="margin-top:10px" class="small"></div>
            </div>
          </div>
          <p class="small" style="margin-top:10px">Tip: Try to save 10–20% of your income each month.</p>
        </div>
      </section>

      <section id="banking">
        <div class="card">
          <h2>Banking Basics</h2>
          <p class="small">Learn about savings accounts, cards, UPI and how to stay safe.</p>
          <div class="grid" style="margin-top:12px">
            <div>
              <h3>Savings Account</h3>
              <p class="small">A safe place to keep money and earn small interest.</p>
            </div>
            <div>
              <h3>Debit & ATM</h3>
              <p class="small">Use cards carefully. Never share PINs or OTPs.</p>
            </div>
            <div>
              <h3>UPI & Netbanking</h3>
              <p class="small">Fast digital payments. Keep passwords safe and use official apps only.</p>
            </div>
            <div>
              <h3>Bank Safety</h3>
              <p class="small">Check for https://, official URLs, and avoid public Wi‑Fi for transactions.</p>
            </div>
          </div>
        </div>
      </section>

      <section id="digital">
        <div class="card">
          <h2>Digital Money & Online Safety</h2>
          <p class="small">Spot scams, protect accounts and pay safely online.</p>
          <ul class="small">
            <li>Never share OTP, PIN or password.</li>
            <li>Don’t give money for ‘free’ offers — check the source.</li>
            <li>Verify QR codes; check sender phone numbers.</li>
            <li>Update apps and your device for security fixes.</li>
          </ul>
        </div>
      </section>

      <section id="invest">
        <div class="card">
          <h2>Introduction to Investments</h2>
          <p class="small">Difference between saving and investing, and easy ways to start.</p>
          <div class="grid" style="margin-top:12px">
            <div>
              <h3>Saving vs Investing</h3>
              <p class="small">Savings = safety. Investing = growth (with risk).</p>
            </div>
            <div>
              <h3>Options to Know</h3>
              <p class="small">Mutual Funds, SIPs, Stocks (basic idea). Ask an adult before investing.</p>
            </div>
            <div>
              <h3>Power of Compounding</h3>
              <p class="small">Small monthly investments grow a lot over time.</p>
            </div>
            <div>
              <h3>Start Small</h3>
              <p class="small">You can start with small SIPs or mock stock platforms to learn.</p>
            </div>
          </div>
        </div>
      </section>

      <section id="spending">
        <div class="card">
          <h2>Smart Spending Habits</h2>
          <ul class="small">
            <li>Ask: Do I need this now?</li>
            <li>Compare prices and reviews.</li>
            <li>Watch for hidden costs and return policies.</li>
            <li>Be critical of ads and influencer recommendations.</li>
          </ul>
        </div>
      </section>

      <section id="activities">
        <div class="card">
          <h2>Interactive Activities & Games</h2>
          <p class="small">Practice makes perfect — try the tools below.</p>

          <div style="margin-top:12px" class="grid">
            <div class="card">
              <h3>Budget Calculator</h3>
              <p class="small">Enter your income and planned savings to see available spending.</p>
              <div class="small">(Try the planner in the Budgeting section above)</div>
            </div>

            <div class="card">
              <h3>Savings Growth Simulator</h3>
              <p class="small">See how monthly savings grow with compounding.</p>
              <div style="margin-top:8px">
                <div class="form-row">
                  <label style="min-width:120px">Monthly Save (₹)</label>
                  <input id="simSave" class="field" type="number" value="500" />
                </div>
                <div style="height:8px"></div>
                <div class="form-row">
                  <label style="min-width:120px">Years</label>
                  <input id="simYears" class="field" type="number" value="5" />
                </div>
                <div style="height:8px"></div>
                <div class="form-row">
                  <label style="min-width:120px">Annual Return (%)</label>
                  <input id="simRate" class="field" type="number" value="8" />
                </div>
                <div style="height:8px"></div>
                <button onclick="simulate()" class="cta">Simulate</button>
                <div id="simRes" style="margin-top:10px" class="small"></div>
              </div>
            </div>

            <div class="card quiz">
              <h3>Quick Quiz</h3>
              <div id="quizQ" class="small">Which is a need?</div>
              <div id="opts"></div>
              <div id="quizRes" class="small" style="margin-top:8px"></div>
            </div>

            <div class="card">
              <h3>Case Studies</h3>
              <ol class="small">
                <li>Saved ₹500/mo → bought a laptop in 8 months.</li>
                <li>Started ₹200 SIP/month → long-term growth after 3 years.</li>
                <li>Got scammed by fake link → learned digital safety.</li>
              </ol>
            </div>

          </div>
        </div>
      </section>

      <section id="contact">
        <div class="card">
          <h2>Contact & Footer</h2>
          <p class="small">Questions? Feedback? Want classroom materials? Reach out.</p>
          <div style="display:flex;gap:12px;flex-wrap:wrap">
            <input class="field" id="name" placeholder="Your name" style="flex:1;min-width:200px" />
            <input class="field" id="email" placeholder="Email" style="flex:1;min-width:200px" />
            <textarea class="field" id="message" placeholder="Message" style="flex-basis:100%;height:90px"></textarea>
            <button onclick="fakeSend()" class="cta">Send Message</button>
            <div id="sendRes" class="small"></div>
          </div>
        </div>
      </section>

    </main>

    <footer>
      <div class="small">Fin‑Fluence • Learn Money. Live Smart. • Built for students (Class 9–12)</div>
      <div style="margin-top:8px" class="small">Email: support@finfluence.com • Instagram • YouTube</div>
    </footer>
  </div>

  <script>
    // Budget calculation
    function calcBudget(){
      const income = Number(document.getElementById('income').value || 0);
      const save = Number(document.getElementById('saveAmt').value || 0);
      const left = income - save;
      const res = document.getElementById('budgetRes');
      if(income<=0){res.textContent='Enter a valid income.';return}
      if(save<0){res.textContent='Savings cannot be negative.';return}
      const savePct = ((save/income)*100).toFixed(1);
      res.textContent = `Available for spending: ₹${left}. Planned savings are ${savePct}% of income.`;
    }

    // Goal planner
    function calcGoal(){
      const goal = Number(document.getElementById('goalAmt').value || 0);
      const monthly = Number(document.getElementById('goalSave').value || 0);
      const out = document.getElementById('goalRes');
      if(goal<=0 || monthly<=0){out.textContent='Enter goal and monthly save in numbers.';return}
      const months = Math.ceil(goal / monthly);
      const years = (months/12).toFixed(1);
      out.textContent = `At ₹${monthly}/month you'll reach ₹${goal} in ${months} months (~${years} years).`;
    }

    // Savings simulator (compound monthly)
    function simulate(){
      const m = Number(document.getElementById('simSave').value || 0);
      const years = Number(document.getElementById('simYears').value || 0);
      const rate = Number(document.getElementById('simRate').value || 0)/100;
      const out = document.getElementById('simRes');
      if(m<=0||years<=0||rate<0){out.textContent='Enter realistic positive values.';return}
      const n = years*12;
      const monthlyRate = rate/12;
      // future value of series: m * (( (1+r)^n -1)/r )
      const fv = m * ((Math.pow(1+monthlyRate,n)-1)/monthlyRate);
      out.textContent = `Estimated value after ${years} years: ₹${fv.toFixed(0)} (assuming ${ (rate*100).toFixed(2)}% p.a.)`;
    }

    // Quick Quiz
    const quiz = {
      q: 'Which of these is a need?',
      opts: ['Brand new gaming console','School textbooks','Latest sneaker drop','Premium subscription']
    };
    function renderQuiz(){
      const opts = document.getElementById('opts');
      opts.innerHTML='';
      quiz.opts.forEach((o,i)=>{
        const div = document.createElement('div');
        div.className='option';
        div.textContent=o;
        div.onclick = ()=>{ checkAns(i)};
        opts.appendChild(div);
      })
    }
    function checkAns(idx){
      const res = document.getElementById('quizRes');
      if(idx===1){res.textContent='Correct! School textbooks are a need.'} else {res.textContent='Not quite — think about essentials vs wants.'}
    }
    renderQuiz();

    function fakeSend(){
      const name=document.getElementById('name').value.trim();
      const email=document.getElementById('email').value.trim();
      const msg=document.getElementById('message').value.trim();
      const res=document.getElementById('sendRes');
      if(!name||!email||!msg){res.textContent='Please fill name, email and message.';return}
      res.textContent='Message sent! (This is a demo page — integrate backend to actually receive messages.)';
      // reset
      document.getElementById('name').value='';
      document.getElementById('email').value='';
      document.getElementById('message').value='';
    }
  </script>
</body>
</html>

