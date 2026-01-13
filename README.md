[PixelBD.Dev.txt](https://github.com/user-attachments/files/24590997/PixelBD.Dev.txt)
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PixelBD Developers | Bangladesh</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(180deg, #006a4e, #f42a41);
      color: #fff;
    }
    header {
      text-align: center;
      padding: 40px 20px;
      background: rgba(0,0,0,0.4);
    }
    header h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    .card {
      background: rgba(0,0,0,0.5);
      border-radius: 16px;
      padding: 25px;
      margin-bottom: 30px;
    }
    h2 { color: #ffd700; }
    a { color: #00eaff; text-decoration: none; }
    .links a {
      display: inline-block;
      margin-right: 15px;
      margin-top: 10px;
      padding: 10px 15px;
      background: #000;
      border-radius: 10px;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
    }
    th, td {
      padding: 12px;
      border-bottom: 1px solid #555;
      text-align: left;
    }
    th { background: rgba(255,255,255,0.1); }
    footer {
      text-align: center;
      padding: 20px;
      background: rgba(0,0,0,0.6);
    }
    .donate-box span {
      display: block;
      margin: 8px 0;
      font-size: 1.1rem;
    }
  </style>
</head>
<body><header>
  <h1>🇧🇩 PixelBD Developers</h1>
  <p>Roblox Game Developers for Bangladesh Players</p>
</header><section>
  <div class="card">
    <h2>আমাদের সম্পর্কে</h2>
    <p>
      আমরা <b>PixelBD Developers</b> — আমরা Roblox এ গেম বানাই বাংলাদেশের প্লেয়ারদের জন্য।
      আমাদের লক্ষ্য হচ্ছে বাংলাদেশি Roblox কমিউনিটিকে আরও বড় করা।
      আপনাদের সহযোগিতায় আমরা আরও ভালো গেম, ভালো সার্ভার এবং নতুন আইডিয়া নিয়ে সামনে এগিয়ে যেতে চাই। ❤️
    </p>
  </div>  <div class="card links">
    <h2>আমাদের লিংক</h2>
    <a href="https://youtube.com/@pixelbddevelopers?si=rsp9ovhmA047eP9N" target="_blank">📺 YouTube</a>
    <a href="https://discord.gg/KQkqYVmEA" target="_blank">💬 Discord</a>
  </div>  <div class="card donate-box">
    <h2>ডোনেট করুন (Support Us)</h2>
    <p>আপনি নিচের যেকোনো মাধ্যমে আমাদের ডোনেট করতে পারেন:</p>
    <span>📱 <b>bKash:</b> YOUR_NUMBER_HERE</span>
    <span>📱 <b>Nagad:</b> YOUR_NUMBER_HERE</span>
    <span>📱 <b>Upay:</b> YOUR_NUMBER_HERE</span>
    <span>📱 <b>Rocket:</b> YOUR_NUMBER_HERE</span>
    <p><i>ডোনেট করার পর আমাদের Discord এ স্ক্রিনশট দিলে আমরা লিস্টে যোগ করবো।</i></p>
  </div>  <div class="card">
    <h2>ডোনেশন লিডারবোর্ড (Auto)</h2>
    <table>
      <tr><th>Rank</th><th>Name</th><th>Amount (BDT)</th></tr>
      <tbody id="donationRows"></tbody>
    </table>
    <p style="margin-top:10px;">মোট ডোনেশন: <b id="totalDonation">0 BDT</b></p><hr style="margin:20px 0;">
<h3>Admin Add Donation</h3>
<input id="dname" placeholder="Donator Name" style="padding:8px;width:45%"> 
<input id="damount" placeholder="Amount" type="number" style="padding:8px;width:45%">
<br><br>
<button onclick="addDonation()" style="padding:10px 20px;border-radius:10px;border:none;cursor:pointer">Add</button>

  </div>
</section><footer>
  <p>© 2026 PixelBD Developers | Made with ❤️ in Bangladesh</p>
</footer>  <script>
    let donations = JSON.parse(localStorage.getItem('donations')) || [];

    function renderTable() {
      const table = document.getElementById('donationRows');
      table.innerHTML = '';
      let total = 0;
      donations.sort((a,b)=>b.amount-a.amount);
      donations.forEach((d,i)=>{
        total += d.amount;
        table.innerHTML += `<tr><td>${i+1}</td><td>${d.name}</td><td>${d.amount}</td></tr>`;
      });
      document.getElementById('totalDonation').innerText = total + ' BDT';
    }

    function addDonation() {
      const name = document.getElementById('dname').value;
      const amount = parseInt(document.getElementById('damount').value);
      if(!name || !amount) return alert('Fill all fields');
      donations.push({name, amount});
      localStorage.setItem('donations', JSON.stringify(donations));
      renderTable();
    }

    renderTable();
  </script></body>
</html>
