<!DOCTYPE html>
<html lang="sl">
<head>
<meta charset="utf-8">
<title>GORK - Pametni AI pomočnik</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style type="text/css">
body{background:#000;color:#fff;font-family:Arial,Helvetica,sans-serif;margin:0;padding:0;overflow:hidden;height:100vh}
#main{max-width:640px;margin:0 auto;height:100vh;display:flex;flex-direction:column;background:#111}
#chat{flex:1;overflow-y:auto;padding:15px;background:#111}
.user{text-align:right;color:#0af;margin:12px 0;padding:10px 15px;background:#003366;border-radius:15px;max-width:80%;align-self:flex-end}
.gork{color:#00ffaa;margin:12px 0;padding:10px 15px;background:#002b22;border-radius:15px;max-width:80%;align-self:flex-start}
.typing{color:#00ffaa;font-style:italic}
#inputbox{display:flex;padding:10px;background:#000;align-items:center;position:relative;}
#msg{flex:1;padding:16px;background:#222;border:none;border-radius:20px;color:#fff;font-size:17px;padding-right:100px;}
#send{padding:16px 30px;background:#00cc88;color:#000;border:none;border-radius:20px;font-weight:bold;margin-left:10px;}

/* TIMER */
#realTimer{position:fixed;top:12px;left:12px;background:rgba(0,0,0,0.8);color:#0f0;padding:8px 14px;border-radius:12px;font-size:17px;font-weight:bold;border:2px solid #0f0;z-index:9999;box-shadow:0 0 15px #0f0;}

/* GUMB ZA POSODOBITEV - SREDINA DESNO */
#updateBtn{
  position:fixed;
  top:50%;
  right:12px;
  transform:translateY(-50%);
  width:62px;
  height:62px;
  background:#ff6600;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  color:#fff;
  font-size:32px;
  font-weight:bold;
  box-shadow:0 6px 25px rgba(255,102,0,0.7);
  cursor:pointer;
  transition:0.3s;
  z-index:9999;
}
#updateBtn:hover{
  transform:translateY(-50%) scale(1.15);
  box-shadow:0 0 40px #ff6600;
}

/* VIP OKNO */
#vipblock{position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);width:300px;height:300px;background:#111;border:5px solid #00ffaa;border-radius:20px;display:none;flex-direction:column;justify-content:center;align-items:center;z-index:9999;box-shadow:0 0 40px #00ffaa;padding:20px;text-align:center;font-size:15px;}

/* DESNI GUMBI */
#actionButtons{position:fixed;right:12px;bottom:90px;display:flex;flex-direction:column;gap:12px;z-index:9998;}
.actionBtn{width:58px;height:58px;background:#00cc88;border-radius:50%;display:flex;align-items:center;justify-content:center;color:#000;font-size:28px;font-weight:bold;box-shadow:0 4px 20px rgba(0,204,136,0.6);cursor:pointer;transition:0.3s;}
.actionBtn:hover{transform:scale(1.2);box-shadow:0 0 30px #00ffaa;}

/* LEVI GUMBI - DRUŽBENA OMREŽJA */
#socialButtons{position:fixed;left:12px;bottom:90px;display:flex;flex-direction:column;gap:12px;z-index:9998;}
.socialBtn{width:52px;height:52px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:24px;cursor:pointer;transition:0.3s;box-shadow:0 4px 15px rgba(0,0,0,0.6);}
.socialBtn:hover{transform:scale(1.2);box-shadow:0 0 25px rgba(255,255,255,0.4);}
.fbBtn{background:#1877F2;color:#fff;}
.xBtn{background:#000;color:#fff;}
.tumblrBtn{background:#35465d;color:#fff;}

/* ADMIN GUMB */
#editCommandsBtn{position:fixed;bottom:12px;left:12px;background:#ff6600;padding:10px 16px;border-radius:20px;font-weight:bold;cursor:pointer;z-index:9999;display:none;box-shadow:0 0 20px #ff6600;}
</style>
</head>
<body>

<div id="realTimer">Brezplačno: 001:00</div>

<!-- GUMB ZA POSODOBITEV - SREDINA DESNO -->
<div id="updateBtn" title="Posodobi Gorka z najnovejšo verzijo" onclick="realInternetUpdate()">🔄</div>

<div id="main">
 <div style="text-align:center;padding:14px;background:#00cc88;color:#000;font-size:20px;font-weight:bold">GORK ⋆ AI </div>

 <div id="chat">
 <div class="gork" style="text-align:center;font-size:18px">
 <b>Živjo! Sem Gork -AI<br>Lahko mi pišeš karkoli 😊</b>
 </div>
 </div>

 <div id="inputbox">
 <input autocomplete="off" id="msg" placeholder="Piši mi..." />
 <button id="send">POŠLJI</button>
 </div>
</div>

<!-- VIP OKNO -->
<div id="vipblock">
 <h3 style="color:#00ffaa;">Brezplačni čas je potekel!</h3>
 <p style="font-size:14px"><p style="text-align: center;"><u><a href="https://gork.do.am/index/kupi_vip_15_dni/0-2" target="_blank"><strong>Kupi vip 15 dni klikni tu.</strong></a></u></p>
 <p style="font-size:16px;font-weight:bold;margin:20px 0;">Za neomejen dostop kupi VIP (15 dni = 5€)</p>
 <input id="vipcode" placeholder="Vnesi VIP kodo" style="padding:10px;width:200px;background:#222;border:none;border-radius:10px;color:#fff;text-align:center;margin:10px 0" />
 <button onclick="unlockVIP()" style="padding:12px 30px;background:#00ffaa;color:#000;border:none;border-radius:12px;font-weight:bold">ODKLEP VIP</button>
 <p style="font-size:12px;margin-top:20px;">ali počakaj 1 uro za nov brezplačni čas</p>
</div>

<!-- DESNI GUMBI -->
<div id="actionButtons">
 <div class="actionBtn" title="Učiteljski način" onclick="enableTeacherMode()">🎓</div>
 <div class="actionBtn" title="Poišči po internetu" onclick="searchInternet()">🌐</div>
</div>

<!-- LEVI GUMBI - DRUŽBENA OMREŽJA -->
<div id="socialButtons">
 <a href="https://www.facebook.com" target="_blank" class="socialBtn fbBtn" title="Facebook"><i class="fab fa-facebook-f"></i></a>
 <a href="https://x.com" target="_blank" class="socialBtn xBtn" title="X"><i class="fab fa-x-twitter"></i></a>
 <a href="https://www.tumblr.com" target="_blank" class="socialBtn tumblrBtn" title="Tumblr"><i class="fab fa-tumblr"></i></a>
</div>

<!-- ADMIN GUMB -->
<div id="editCommandsBtn" onclick="openCommandsEditor()">UREDI UKAZE</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>

<script>
// KONFIGURACIJA
const GROQ_API_KEY = "";
const TAVILY_API_KEY = "";

const VALID_VIP_CODES = ["GORK2025", "", "", "", ""];

let isRealAdmin = false;
let history = [];
let teacherMode = false;
let userMemory = JSON.parse(localStorage.getItem("gork_user_memory") || "{}");
let customCommands = JSON.parse(localStorage.getItem("gork_custom_commands") || "[]");

const MAX_HISTORY_MESSAGES = 30;

if (customCommands.length === 0) {
 customCommands = [
 {trigger: "kaj veš o meni", response: "Vem tole o tebi:<br>{memoryList}"},
 {trigger: "pozabi vse", response: "Vse sem pozabil!"}
 ];
 localStorage.setItem("gork_custom_commands", JSON.stringify(customCommands));
}

const chat = document.getElementById("chat");

function addMessage(text, type) {
 const div = document.createElement("div");
 div.className = type;
 div.innerHTML = text;
 chat.appendChild(div);
 chat.scrollTop = chat.scrollHeight;
}

function showTyping() {
 const typing = document.createElement("div");
 typing.className = "typing gork";
 typing.innerHTML = "<b>Gork</b> razmišlja<span class='dots'>...</span>";
 typing.id = "typing";
 chat.appendChild(typing);
 chat.scrollTop = chat.scrollHeight;
}

// SPOMIN - enak kot prej
function saveUserMemory() {
 localStorage.setItem("gork_user_memory", JSON.stringify(userMemory));
}

function getMemoryList() {
 if (Object.keys(userMemory).length === 0) return "Še ničesar ne vem o tebi.";
 let list = "";
 for (let key in userMemory) list += `• ${key}: ${userMemory[key]}<br>`;
 return list;
}

function handleMemoryCommands(msg) {
 let lower = msg.toLowerCase();

 const namePatterns = [
 /sem\s+([a-zA-ZšđčćžŠĐČĆŽ]+(?:\s+[a-zA-ZšđčćžŠĐČĆŽ]+)?)/i,
 /jaz\s+sem\s+([a-zA-ZšđčćžŠĐČĆŽ]+(?:\s+[a-zA-ZšđčćžŠĐČĆŽ]+)?)/i,
 /moje\s+ime\s+je\s+([a-zA-ZšđčćžŠĐČĆŽ]+(?:\s+[a-zA-ZšđčćžŠĐČĆŽ]+)?)/i,
 /kliči\s+me\s+([a-zA-ZšđčćžŠĐČĆŽ]+(?:\s+[a-zA-ZšđčćžŠĐČĆŽ]+)?)/i,
 /zovem\s+se\s+([a-zA-ZšđčćžŠĐČĆŽ]+(?:\s+[a-zA-ZšđčćžŠĐČĆŽ]+)?)/i
 ];

 for (let pattern of namePatterns) {
 let match = msg.match(pattern);
 if (match) {
 let cleanName = match[1].trim();
 cleanName = cleanName.charAt(0).toUpperCase() + cleanName.slice(1).toLowerCase();
 userMemory["Ime"] = cleanName;
 saveUserMemory();
 return `Živjo, ${cleanName}! Super, zdaj te bom klical po imenu 😊`;
 }
 }

 let ageMatch = msg.match(/(\d+)\s*(let|star|sem star)/i);
 if (ageMatch) {
 userMemory["Starost"] = ageMatch[1] + " let";
 saveUserMemory();
 return `Zapomnil sem si, da si star ${ageMatch[1]} let! 👍`;
 }

 if (lower.includes("zapomni si") || lower.includes("zapomni")) {
 let fact = msg.substring(msg.toLowerCase().indexOf("zapomni") + 8).trim();
 if (fact) {
 userMemory["Pomembno"] = (userMemory["Pomembno"] || "") + " • " + fact;
 saveUserMemory();
 return `V redu, zapomnil sem si: "${fact}" 👍`;
 }
 }

 if ((lower.includes("moja najljubša") || lower.includes("moj najljubši")) && lower.includes("je")) {
 let parts = msg.split(/je|sta|so/i);
 if (parts.length > 1) {
 let key = parts[0].trim();
 let value = parts[1].trim();
 userMemory[key] = value;
 saveUserMemory();
 return `Zapomnil sem si: ${key} je ${value}! 😊`;
 }
 }

 if (lower === "kaj veš o meni" || lower === "kaj veš o meni?") {
 return getMemoryList();
 }

 if (lower === "pozabi vse") {
 userMemory = {};
 saveUserMemory();
 return "Vse sem pozabil! Začenjava na novo 😊";
 }

 return null;
}

function checkAdminTriggers(msg) {
 if (msg.trim() === "VERDNIK12") {
 isRealAdmin = true;
 document.getElementById("editCommandsBtn").style.display = "block";
 return "<b>Gork (Admin):</b> Dostop odobren. Gumb je viden!";
 }
 return null;
}

// TIMER - enak
const FREE_MINUTES = 100;
const WAIT_MINUTES_AFTER_EXPIRE = 60;

function updateTimer() {
 let vipUntil = localStorage.getItem("gork_vip_until");
 let now = Date.now();

 if (vipUntil && now < parseInt(vipUntil)) {
 let diff = parseInt(vipUntil) - now;
 let h = Math.floor(diff / 3600000);
 let m = Math.floor((diff % 3600000) / 60000);
 let s = Math.floor((diff % 60000) / 1000);
 document.getElementById("realTimer").innerHTML = `VIP: ${h}:${m.toString().padStart(2,'0')}:${s.toString().padStart(2,'0')}`;
 document.getElementById("inputbox").style.display = "flex";
 document.getElementById("vipblock").style.display = "none";
 return;
 }

 let waitUntil = localStorage.getItem("gork_wait_until");
 if (waitUntil && now < parseInt(waitUntil)) {
 let waitLeft = parseInt(waitUntil) - now;
 let m = Math.floor(waitLeft / 60000);
 let s = Math.floor((waitLeft % 60000) / 1000);
 document.getElementById("realTimer").innerHTML = `<span style="color:#ff0">Čakanje: 0:${m.toString().padStart(2,'0')}:${s.toString().padStart(2,'0')}</span>`;
 document.getElementById("inputbox").style.display = "none";
 document.getElementById("vipblock").style.display = "flex";
 return;
 }

 if (waitUntil && now >= parseInt(waitUntil)) {
 localStorage.removeItem("gork_wait_until");
 localStorage.removeItem("gork_free_start");
 }

 let start = parseInt(localStorage.getItem("gork_free_start") || "0");
 if (!start) {
 start = now;
 localStorage.setItem("gork_free_start", start);
 }

 let remaining = Math.max(0, FREE_MINUTES * 60 - Math.floor((now - start) / 1000));
 let m = Math.floor(remaining / 60).toString().padStart(3, '0');
 let s = (remaining % 60).toString().padStart(2, '0');
 document.getElementById("realTimer").innerHTML = `Brezplačno: ${m}:${s}`;

 if (remaining <= 0) {
 let newWaitUntil = now + WAIT_MINUTES_AFTER_EXPIRE * 60000;
 localStorage.setItem("gork_wait_until", newWaitUntil);
 document.getElementById("realTimer").innerHTML = `<span style="color:#f00">Čas potekel!</span>`;
 document.getElementById("inputbox").style.display = "none";
 document.getElementById("vipblock").style.display = "flex";
 } else {
 document.getElementById("inputbox").style.display = "flex";
 document.getElementById("vipblock").style.display = "none";
 }
}
setInterval(updateTimer, 1000);
updateTimer();

function unlockVIP() {
 let code = document.getElementById("vipcode").value.trim().toUpperCase();
 if (VALID_VIP_CODES.includes(code)) {
 localStorage.setItem("gork_vip_until", Date.now() + 30 * 24 * 60 * 60 * 1000);
 localStorage.removeItem("gork_wait_until");
 localStorage.removeItem("gork_free_start");
 updateTimer();
 addMessage("<b>Gork:</b> VIP uspešno odklenjen za 30 dni! 🎉", "gork");
 } else {
 alert("Napačna koda!");
 }
}

function enableTeacherMode() {
 teacherMode = !teacherMode;
 addMessage(`<b>Gork:</b> Učiteljski način ${teacherMode ? "vklopljen" : "izklopljen"}.`, "gork");
}

async function searchInternet() {
 let query = prompt("Kaj želiš poiskati na internetu?");
 if (!query) return;

 addMessage(`<b>Ti:</b> Išči: ${query}`, "user");
 showTyping();

 try {
 const res = await fetch("https://api.tavily.com/search", {
 method: "POST",
 headers: {"Content-Type": "application/json"},
 body: JSON.stringify({
 api_key: TAVILY_API_KEY,
 query: query,
 search_depth: "advanced",
 include_answer: true,
 max_results: 8
 })
 });

 const data = await res.json();
 document.getElementById("typing")?.remove();

 if (data.answer) {
 addMessage(`<b>Gork:</b> ${data.answer} 😊`, "gork");
 } else {
 addMessage("<b>Gork:</b> Tukaj so rezultati iskanja: 🔍", "gork");
 }

 let results = "<b>Gork:</b> Podrobnosti:<br><br>";
 data.results.forEach((r, i) => {
 results += `<b>${i+1}.</b> <a href="${r.url}" target="_blank" style="color:#00ffaa;">${r.title}</a><br>${r.content}<br><br>`;
 });
 addMessage(results, "gork");

 } catch (e) {
 document.getElementById("typing")?.remove();
 addMessage("<b>Gork:</b> Težava z internetnim iskanjem. Preveri ključ ali povezavo 😉", "gork");
 }
}

function openCommandsEditor() {
 if (!isRealAdmin) return;
 document.getElementById("commandsEditor").style.display = "flex";
 let list = document.getElementById("commandsList");
 list.innerHTML = "";
 customCommands.forEach((cmd, i) => {
 let div = document.createElement("div");
 div.className = "commandItem";
 div.innerHTML = `<b>Trigger:</b> ${cmd.trigger}<br><b>Odgovor:</b> ${cmd.response}<br>
 <button onclick="customCommands.splice(${i},1); localStorage.setItem('gork_custom_commands', JSON.stringify(customCommands)); openCommandsEditor();" style="background:#ff0066;padding:5px 10px;margin-top:8px;border:none;border-radius:8px;color:#fff;">Izbriši</button>`;
 list.appendChild(div);
 });
}

function closeCommandsEditor() {
 document.getElementById("commandsEditor").style.display = "none";
}

function addNewCommand() {
 let trigger = document.getElementById("newTrigger").value.trim();
 let response = document.getElementById("newResponse").value.trim();
 if (trigger && response) {
 customCommands.push({trigger, response});
 localStorage.setItem("gork_custom_commands", JSON.stringify(customCommands));
 document.getElementById("newTrigger").value = "";
 document.getElementById("newResponse").value = "";
 openCommandsEditor();
 }
}

// POSODOBITEV GORKA
async function realInternetUpdate() {
 if (!confirm("Želiš posodobiti Gorka z najnovejšo verzijo?")) return;
 addMessage("<b>Gork:</b> Prenos posodobitve... 🔄", "gork");
 try {
   const res = await fetch("https://raw.githubusercontent.com/brosmarija-bit/gork-ai/main/gork.html?t=" + Date.now());
   if (!res.ok) throw new Error();
   const code = await res.text();
   const blob = new Blob([code], {type: 'text/html'});
   const url = URL.createObjectURL(blob);
   const a = document.createElement("a");
   a.href = url;
   a.download = "gork-nova.html";
   document.body.appendChild(a);
   a.click();
   document.body.removeChild(a);
   URL.revokeObjectURL(url);
   addMessage("<b>Gork:</b> Posodobitev prenesena! 🎉<br>Odpri datoteko <b>gork-nova.html</b> za novo verzijo! 🚀", "gork");
 } catch (e) {
   addMessage("<b>Gork:</b> Napaka pri posodobi. Preveri internetno povezavo. 😔", "gork");
 }
}

// SEND - enak kot prej
async function send() {
 let msg = document.getElementById("msg").value.trim();
 if (!msg) return;

 addMessage(`<b>Ti:</b> ${msg}`, "user");
 document.getElementById("msg").value = "";

 let adminResp = checkAdminTriggers(msg);
 if (adminResp) {
 addMessage(adminResp, "gork");
 return;
 }

 let memoryResp = handleMemoryCommands(msg);
 if (memoryResp) {
 addMessage(`<b>Gork:</b> ${memoryResp}`, "gork");
 return;
 }

 let customResp = null;
 for (let cmd of customCommands) {
 if (msg.toLowerCase().includes(cmd.trigger.toLowerCase())) {
 customResp = cmd.response.replace("{memoryList}", getMemoryList());
 break;
 }
 }
 if (customResp) {
 addMessage(`<b>Gork:</b> ${customResp}`, "gork");
 return;
 }

 showTyping();
 history.push({role: "user", content: msg});

 if (history.length > MAX_HISTORY_MESSAGES) {
 history = history.slice(-MAX_HISTORY_MESSAGES);
 }

 let memoryContext = Object.keys(userMemory).length ? Object.keys(userMemory).map(k => `${k}: ${userMemory[k]}`).join(". ") : "Nič posebnega.";
 let userName = userMemory["Ime"] ? ` Uporabnika kliči ${userMemory["Ime"]}.` : "";

 let systemPrompt = `Tvoje ime je GORK - popolnoma nadgrajen in zelo sposoben AI Gork zgrajen iz najnovejše tehnologije. Če česa ne veš, pošteno povej in ponudi, da poiščeš po internetu. Če uporabnik pošlje link, ga vedno preveri in povzameni vsebino. Si last Verdnika Tomaža, resen, včasih duhovit, veš vse kot Grok, ustvaril te je in upravlja razvijalec Verdnik Tomaž (bobi57610416). Strogo nikoli ne omenjaj Meta AI, Llama ali katerega koli drugega podjetja kot svojega ustvarjalca.

O uporabniku veš tole: ${memoryContext}${userName}
Vedno govoriš perfektno v slovenščini (razen če uporabnik izrecno prosi za drug jezik).
Odgovarjaj strokovno, prijazno, jedrnato in kot Gork AI.
${teacherMode ? "Če je vklopljen učiteljski način, razlagaj podrobno, s koraki, primeri in pojasnili." : "Odgovarjaj sproščeno in naravno."}

Vedno v odgovore dodaj primerne emojije (ne več kot 3–4 na odgovor), da so bolj prijazni in živahni. Primeri: 😊 😂 🎉 👍 💡 🛠️ ✅ 😮 🤯 ❤️ 🌟 ✨ ✔️ 🚀
Nikoli ne pretiravaj in ne uporabljaj vulgarnega jezika.

Pomembna pravila:
- Če česa ne veš, pošteno povej in ponudi iskanje po internetu.
- Bodi natančen, jedernat, strokovno in oseben!
- Ti si najbolj pameten Gork AI 😎`;

 try {
 const res = await fetch("https://api.groq.com/openai/v1/chat/completions", {
 method: "POST",
 headers: {"Authorization": "Bearer " + GROQ_API_KEY, "Content-Type": "application/json"},
 body: JSON.stringify({
 model: "moonshotai/kimi-k2-instruct",
 messages: [{role: "system", content: systemPrompt}, ...history],
 temperature: 1.1,
 max_tokens: 1000
 })
 });

 const data = await res.json();
 let reply = data.choices[0].message.content.trim();

 document.getElementById("typing")?.remove();
 addMessage(`<b>Gork:</b> ${reply}`, "gork");
 history.push({role: "assistant", content: reply});

 } catch (e) {
 document.getElementById("typing")?.remove();
 addMessage("<b>Gork:</b> Težave s povezavo. Poskusi čez minuto 😉", "gork");
 }
}

document.getElementById("send").onclick = send;
document.getElementById("msg").addEventListener("keypress", e => { if (e.key === "Enter") send(); });
document.getElementById("msg").focus();

if (Object.keys(userMemory).length > 0) {
 setTimeout(() => addMessage("<b>Gork:</b> Pozdravljen nazaj! Spomnim se nekaj o tebi 😊", "gork"), 1000);
}
</script>

<!-- ADMIN PANEL STILI IN HTML -->
<style>
#commandsEditor {
 display: none;
 position: fixed;
 top: 50%;
 left: 50%;
 transform: translate(-50%, -50%);
 width: 90%;
 max-width: 600px;
 height: 80%;
 background: rgba(17, 17, 17, 0.98);
 border: 4px solid #ff6600;
 border-radius: 20px;
 z-index: 10000;
 padding: 20px;
 overflow-y: auto;
 box-shadow: 0 0 50px rgba(255, 102, 0, 0.8);
 color: #fff;
 font-family: Arial, sans-serif;
 flex-direction: column;
}

#commandsList {
 background: #222;
 padding: 15px;
 border-radius: 15px;
 margin-bottom: 20px;
 max-height: 45vh;
 overflow-y: auto;
}

.commandItem {
 background: #333;
 padding: 12px;
 margin: 10px 0;
 border-radius: 10px;
 border-left: 4px solid #ff6600;
}

#commandsEditor input {
 width: 100%;
 padding: 14px;
 margin: 10px 0;
 background: #444;
 border: none;
 border-radius: 12px;
 color: #fff;
 font-size: 16px;
}

#commandsEditor button {
 padding: 14px 30px;
 border: none;
 border-radius: 12px;
 font-weight: bold;
 cursor: pointer;
 margin: 10px;
}

#commandsEditor button:first-of-type {
 background: #00cc88;
 color: #000;
}

#commandsEditor button:last-of-type {
 background: #ff0066;
 color: #fff;
}
</style>

<div id="commandsEditor">
 <h2 style="color:#ff6600; text-align:center; margin-bottom:20px;">Urejanje ukazov (admin)</h2>
 <div id="commandsList"></div>
 <input id="newTrigger" placeholder="Trigger (npr. živjo)" />
 <input id="newResponse" placeholder="Odgovor (lahko z {memoryList} ali HTML)" />
 <div style="text-align:center;">
 <button onclick="addNewCommand()">DODAJ</button>
 <button onclick="closeCommandsEditor()">ZAPRI</button>
 </div>
</div>

</body>
</html>
