<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KSZ Group | Faheem OS v4.0</title>
    <style>
        :root { --primary: #0f172a; --accent: #d4af37; --success: #15803d; --bg: #f1f5f9; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: var(--bg); margin: 0; display: flex; flex-direction: column; height: 100vh; overflow: hidden; }
        header { background: var(--primary); color: white; padding: 12px; display: flex; justify-content: space-between; align-items: center; border-bottom: 3px solid var(--accent); }
        .tabs { display: flex; background: #cbd5e1; padding: 4px; gap: 4px; }
        .tab-btn { flex: 1; padding: 12px; border: none; cursor: pointer; font-weight: bold; font-size: 11px; border-radius: 4px; text-transform: uppercase; }
        .active-tab { background: white; color: var(--primary); box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
        
        #chat-section, #admin-section, #finance-section { flex: 1; overflow-y: auto; padding: 15px; display: none; }
        .active-section { display: flex !important; flex-direction: column; gap: 12px; }
        
        .msg { max-width: 88%; padding: 14px; border-radius: 12px; font-size: 14px; line-height: 1.6; animation: fadeIn 0.3s; }
        .faheem { background: white; align-self: flex-start; border-left: 5px solid var(--accent); box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1); }
        .user { background: var(--primary); color: white; align-self: flex-end; }
        
        table { width: 100%; border-collapse: collapse; background: white; font-size: 12px; border-radius: 8px; overflow: hidden; }
        th, td { padding: 12px; text-align: left; border-bottom: 1px solid #e2e8f0; }
        th { background: var(--primary); color: white; }

        .input-box { background: white; padding: 15px; display: flex; gap: 10px; border-top: 1px solid #e2e8f0; }
        input { flex: 1; border: 1px solid #cbd5e1; padding: 12px; border-radius: 8px; outline: none; font-size: 14px; }
        button#send-btn { background: var(--primary); color: white; border: none; padding: 10px 20px; border-radius: 8px; font-weight: bold; }
        
        .report-btn { background: var(--accent); color: var(--primary); border: none; padding: 15px; border-radius: 8px; font-weight: bold; margin-bottom: 10px; cursor: pointer; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(5px); } to { opacity: 1; transform: translateY(0); } }
    </style>
</head>
<body>

<header>
    <div><strong>KSZ GROUP</strong> | Assistant Faheem</div>
    <div id="header-stats" style="color: var(--accent); font-weight: bold; font-size: 12px;">Total: Rs. 0</div>
</header>

<div class="tabs">
    <button class="tab-btn active-tab" onclick="switchTab('chat', this)">💬 FAHEEM</button>
    <button class="tab-btn" onclick="switchTab('admin', this)">📋 REGISTRY</button>
    <button class="tab-btn" onclick="switchTab('finance', this)">💰 FINANCE</button>
</div>

<div id="chat-section" class="active-section">
    <div class="msg faheem">🌸 Assalam-o-Alaikum, Zabeehullah! Everything is set. I am ready to handle students, manage the KSZ Group funds, and generate content.</div>
</div>

<div id="admin-section">
    <button class="report-btn" onclick="generateReport()">📋 GENERATE DAILY REPORT</button>
    <table id="reg-table"><thead><tr><th>Name</th><th>Email</th><th>Phone</th></tr></thead><tbody></tbody></table>
</div>

<div id="finance-section">
    <div style="background:white; padding:15px; border-radius:10px; margin-bottom:15px; border: 1px solid #ddd;">
        <h4 style="margin-top:0">Record New Support</h4>
        <input type="text" id="don-name" placeholder="Supporter Name">
        <input type="number" id="don-amount" placeholder="Amount (PKR)">
        <button onclick="addDonation()" style="background:var(--success); color:white; border:none; width:100%; padding:12px; border-radius:6px; font-weight:bold; margin-top:5px;">Confirm Donation</button>
    </div>
    <table id="fin-table"><thead><tr><th>Partner</th><th>Amount</th><th>Date</th></tr></thead><tbody></tbody></table>
</div>

<div class="input-box">
    <input type="text" id="userInput" placeholder="Ask Faheem anything...">
    <button id="send-btn" onclick="processInput()">Send</button>
</div>

<script>
    const API_KEY = "AIzaSyCZWBEg1QBPTymZtkw36LCICkDCxCGlISg";
    
    function switchTab(tab, btn) {
        document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active-tab'));
        btn.classList.add('active-tab');
        ['chat', 'admin', 'finance'].forEach(t => document.getElementById(t + '-section').classList.remove('active-section'));
        document.getElementById(tab + '-section').classList.add('active-section');
        if(tab === 'admin') loadRegistry();
        if(tab === 'finance') loadFinance();
    }

    function addDonation() {
        const name = document.getElementById('don-name').value;
        const amt = document.getElementById('don-amount').value;
        if(!name || !amt) return alert("Please enter name and amount.");
        let fin = JSON.parse(localStorage.getItem('bunyaad_finance') || "[]");
        fin.push({ name, amt, date: new Date().toLocaleDateString() });
        localStorage.setItem('bunyaad_finance', JSON.stringify(fin));
        document.getElementById('don-name').value = ''; document.getElementById('don-amount').value = '';
        loadFinance();
        renderMsg(`Faheem Alert: Success! Registered a donation of Rs. ${amt} from ${name}. I have updated the ledger.`, 'faheem');
    }

    function loadFinance() {
        const tbody = document.querySelector('#fin-table tbody');
        const data = JSON.parse(localStorage.getItem('bunyaad_finance') || "[]");
        let total = 0;
        tbody.innerHTML = data.reverse().map(d => {
            total += parseInt(d.amt);
            return `<tr><td>${d.name}</td><td>Rs. ${d.amt}</td><td>${d.date}</td></tr>`;
        }).join('');
        document.getElementById('header-stats').innerText = `Total: Rs. ${total}`;
    }

    function loadRegistry() {
        const tbody = document.querySelector('#reg-table tbody');
        const data = JSON.parse(localStorage.getItem('bunyaad_registry') || "[]");
        tbody.innerHTML = data.reverse().map(s => `<tr><td>${s.name}</td><td>${s.email}</td><td>${s.phone}</td></tr>`).join('');
    }

    async function generateReport() {
        const students = JSON.parse(localStorage.getItem('bunyaad_registry') || "[]");
        const finance = JSON.parse(localStorage.getItem('bunyaad_finance') || "[]");
        const total = finance.reduce((sum, item) => sum + parseInt(item.amt), 0);
        
        const reportText = `📊 BUNYAAD DAILY REPORT\nDate: ${new Date().toLocaleDateString()}\n---\n👥 New Students: ${students.length}\n💰 Total Support: Rs. ${total}\n🔥 Mission: Empowering Pakistan.\nProject of KSZ Group.`;
        
        renderMsg(reportText, 'faheem');
        alert("Report Generated in Chat! You can copy it now.");
        switchTab('chat', document.querySelector('.tab-btn'));
    }

    async function processInput() {
        const input = document.getElementById('userInput');
        const text = input.value.trim();
        if(!text) return;
        renderMsg(text, 'user');
        input.value = '';

        const donations = localStorage.getItem('bunyaad_finance') || "[]";
        const systemPrompt = `You are Faheem, Senior Registrar at Bunyaad. 
        FINANCIAL LEDGER: ${donations}.
        MISSION: Follow the "Assalam-o-Alaikum" protocol for newcomers. If a user is a donor found in the ledger, thank them specifically for their support to KSZ Group. 
        CATALOG: Use your official WhatsApp links for courses (Canva, Video, CS, etc). 
        TONE: Professional, Visionary, Mentor. Urdu/English mixed as per user style.`;

        try {
            const res = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${API_KEY}`, {
                method: "POST",
                headers: {"Content-Type": "application/json"},
                body: JSON.stringify({
                    contents: [{role: "user", parts: [{text: text}]}],
                    systemInstruction: { parts: [{text: systemPrompt}] }
                })
            });
            const data = await res.json();
            renderMsg(data.candidates[0].content.parts[0].text, 'faheem');
            autoRegister(text);
        } catch(e) { renderMsg("Faheem connection error. Check internet or API key.", 'faheem'); }
    }

    function renderMsg(text, sender) {
        const div = document.createElement('div');
        div.className = `msg ${sender}`;
        div.innerText = text;
        const chat = document.getElementById('chat-section');
        chat.appendChild(div);
        chat.scrollTop = chat.scrollHeight;
    }

    function autoRegister(text) {
        const email = text.match(/[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}/);
        const phone = text.match(/(03|0092|\+92)[0-9]{9,10}/);
        if(email || phone) {
            let reg = JSON.parse(localStorage.getItem('bunyaad_registry') || "[]");
            reg.push({ name: "Student Prospect", email: email?.[0], phone: phone?.[0] });
            localStorage.setItem('bunyaad_registry', JSON.stringify(reg));
        }
    }
</script>
</body>
</html>

