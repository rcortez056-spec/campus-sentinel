<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Campus Sentinel — Security Operations Dashboard</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --bg: #070a10; --panel: #0f172a; --line: #1e293b; --line-2: #334155;
    --text: #f8fafc; --muted: #94a3b8; --dim: #64748b;
    --cyan: #06b6d4; --blue: #3b82f6; --emerald: #10b981; --amber: #f59e0b; --rose: #f43f5e;
  }
  body {
    font-family: system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
    background: var(--bg); color: var(--text); min-height: 100vh; display: flex; flex-direction: column;
  }
  .mono { font-family: ui-monospace, "SF Mono", Menlo, Consolas, monospace; }
  .wrap { max-width: 1280px; width: 100%; margin: 0 auto; padding: 0 1.25rem; }
  .panel { background: rgba(15,23,42,0.8); border: 1px solid var(--line); border-radius: 14px; padding: 1.25rem; }
  .label { font-size: 0.7rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; color: var(--muted); }
  .row { display: flex; align-items: center; justify-content: space-between; gap: 0.75rem; flex-wrap: wrap; }

  /* header */
  header { position: sticky; top: 0; z-index: 40; background: rgba(15,23,42,0.92); border-bottom: 1px solid var(--line); backdrop-filter: blur(8px); }
  .head { padding: 0.9rem 0; }
  .brand { display: flex; align-items: center; gap: 0.8rem; }
  .logo { width: 40px; height: 40px; border-radius: 11px; background: linear-gradient(135deg, var(--cyan), var(--blue)); display: flex; align-items: center; justify-content: center; color: #020617; font-size: 1.1rem; }
  .brand h1 { font-size: 1.2rem; font-weight: 800; letter-spacing: -0.01em; }
  .brand h1 span { color: var(--cyan); }
  .brand small { color: var(--muted); font-size: 0.75rem; }
  .pill { font-size: 0.72rem; padding: 0.4rem 0.75rem; border-radius: 999px; border: 1px solid var(--line-2); background: #0b1222; color: var(--muted); display: inline-flex; align-items: center; gap: 0.5rem; }
  .pill .dot { width: 8px; height: 8px; border-radius: 50%; background: var(--amber); }
  .pill.live { color: #6ee7b7; border-color: #065f46; }
  .pill.live .dot { background: var(--emerald); animation: blink 1.6s infinite; }
  .btn-ghost { background: var(--line); color: var(--text); border: 1px solid var(--line-2); border-radius: 9px; padding: 0.45rem 0.85rem; font-size: 0.78rem; font-family: inherit; cursor: pointer; }
  .btn-ghost:hover { background: var(--line-2); }

  /* banner */
  .banner { margin-top: 1rem; background: rgba(120,53,15,0.25); border: 1px solid rgba(180,83,9,0.5); color: #fcd34d; border-radius: 10px; padding: 0.7rem 1rem; font-size: 0.8rem; }

  /* stats */
  .stats { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1rem; margin: 1.25rem 0; }
  .stat { position: relative; overflow: hidden; }
  .stat .num { font-size: 1.7rem; font-weight: 700; font-family: ui-monospace, Menlo, monospace; margin-top: 0.4rem; }
  .stat .note { font-size: 0.72rem; color: var(--muted); margin-top: 0.2rem; }
  .stat::after { content: ""; position: absolute; bottom: 0; left: 0; right: 0; height: 3px; }
  .stat.c1::after { background: var(--cyan); } .stat.c2::after { background: var(--emerald); }
  .stat.c3::after { background: var(--rose); } .stat.c4::after { background: var(--amber); }

  /* layout */
  .grid { display: grid; grid-template-columns: 5fr 7fr; gap: 1.25rem; align-items: start; }
  .stack { display: flex; flex-direction: column; gap: 1.25rem; }

  /* form */
  .chips { display: grid; grid-template-columns: 1fr 1fr; gap: 0.5rem; margin: 0.6rem 0 1rem; }
  .chip { background: var(--line); color: #cbd5e1; border: 1px solid #293548; border-radius: 8px; padding: 0.45rem 0.6rem; font-size: 0.75rem; font-family: inherit; cursor: pointer; text-align: left; }
  .chip:hover { background: var(--line-2); }
  textarea, input[type="url"] {
    width: 100%; background: rgba(7,10,16,0.7); border: 1px solid #293548; color: var(--text);
    border-radius: 10px; padding: 0.75rem; font-family: inherit; font-size: 0.88rem; outline: none;
  }
  textarea { resize: vertical; min-height: 120px; }
  input[type="url"] { font-family: ui-monospace, Menlo, monospace; font-size: 0.78rem; }
  textarea:focus, input[type="url"]:focus { border-color: var(--cyan); box-shadow: 0 0 12px rgba(6,182,212,0.25); }
  .btn-main {
    width: 100%; margin-top: 0.8rem; padding: 0.8rem; border: none; border-radius: 10px; cursor: pointer;
    background: linear-gradient(90deg, var(--cyan), var(--blue)); color: #020617; font-weight: 700; font-size: 0.9rem; font-family: inherit;
  }
  .btn-main:disabled { opacity: 0.55; cursor: wait; }
  .processing { display: none; margin-top: 0.8rem; background: rgba(8,51,68,0.4); border: 1px solid rgba(21,94,117,0.6); border-radius: 10px; padding: 0.7rem 0.9rem; font-size: 0.78rem; color: #67e8f9; }
  .processing.on { display: block; }
  .arch { font-size: 0.78rem; color: var(--muted); display: flex; flex-direction: column; gap: 0.45rem; }
  .arch div { display: flex; justify-content: space-between; }
  .arch .ok { color: #6ee7b7; }

  /* feed */
  .feed-bar { display: flex; justify-content: space-between; align-items: center; background: rgba(15,23,42,0.6); border: 1px solid var(--line); border-radius: 12px; padding: 0.7rem 0.9rem; margin-bottom: 0.9rem; }
  .filters button { background: var(--line); color: #cbd5e1; border: 1px solid var(--line-2); border-radius: 7px; padding: 0.3rem 0.7rem; font-size: 0.75rem; font-family: inherit; cursor: pointer; margin-left: 0.3rem; }
  .filters button.on { background: var(--rose); border-color: var(--rose); color: #fff; }
  .feed { display: flex; flex-direction: column; gap: 0.75rem; max-height: 660px; overflow-y: auto; padding-right: 0.25rem; }
  .card { background: rgba(15,23,42,0.8); border: 1px solid var(--line); border-radius: 12px; padding: 0.95rem; display: flex; flex-direction: column; gap: 0.7rem; animation: fadeIn 0.35s ease-out; }
  .card-top { display: flex; justify-content: space-between; align-items: center; gap: 0.5rem; flex-wrap: wrap; border-bottom: 1px solid rgba(30,41,59,0.8); padding-bottom: 0.6rem; }
  .card-top .left { display: flex; gap: 0.5rem; align-items: center; flex-wrap: wrap; }
  .id { color: var(--cyan); font-weight: 700; font-size: 0.78rem; }
  .sev { font-size: 0.7rem; font-weight: 700; padding: 0.2rem 0.6rem; border-radius: 999px; border: 1px solid; }
  .sev.Critical { color: #fb7185; background: rgba(76,5,25,0.6); border-color: #9f1239; }
  .sev.High { color: #fbbf24; background: rgba(69,26,3,0.6); border-color: #92400e; }
  .sev.Medium { color: #fde047; background: rgba(66,32,6,0.5); border-color: #854d0e; }
  .sev.Low { color: #93c5fd; background: rgba(23,37,84,0.6); border-color: #1e40af; }
  .cat { font-size: 0.68rem; padding: 0.15rem 0.5rem; border-radius: 6px; background: var(--line); color: #cbd5e1; border: 1px solid var(--line-2); font-family: ui-monospace, Menlo, monospace; }
  .time { font-size: 0.7rem; color: var(--dim); font-family: ui-monospace, Menlo, monospace; }
  .pii { display: flex; align-items: center; gap: 0.5rem; background: rgba(2,6,23,0.6); border: 1px solid var(--line); border-radius: 8px; padding: 0.45rem 0.6rem; font-size: 0.72rem; color: var(--muted); }
  .pii b { color: #6ee7b7; font-weight: 600; }
  .summary-label { font-size: 0.7rem; font-weight: 700; color: #cbd5e1; text-transform: uppercase; letter-spacing: 0.08em; }
  .summary { font-size: 0.8rem; line-height: 1.5; color: #e2e8f0; background: rgba(15,23,42,0.7); border: 1px solid rgba(30,41,59,0.8); border-radius: 8px; padding: 0.6rem 0.7rem; margin-top: 0.3rem; }
  .card-foot { display: flex; justify-content: space-between; align-items: center; font-size: 0.72rem; color: var(--muted); }
  .card-foot strong { color: #e2e8f0; }
  .via { color: var(--dim); }
  .empty { text-align: center; color: var(--dim); font-size: 0.8rem; padding: 2rem 0; }

  footer { border-top: 1px solid var(--line); margin-top: 2rem; padding: 1rem 0; color: var(--dim); font-size: 0.75rem; }
  footer .wrap { display: flex; justify-content: space-between; flex-wrap: wrap; gap: 0.5rem; }

  /* modal */
  .modal { position: fixed; inset: 0; background: rgba(0,0,0,0.8); display: none; align-items: center; justify-content: center; padding: 1rem; z-index: 60; }
  .modal.on { display: flex; }
  .modal-box { max-width: 520px; width: 100%; padding: 1.4rem; }
  .modal-box h3 { font-size: 1rem; margin-bottom: 0.6rem; display: flex; justify-content: space-between; align-items: center; }
  .modal-box p { font-size: 0.8rem; color: var(--muted); line-height: 1.5; margin-bottom: 0.8rem; }
  .code { background: #020617; border: 1px solid var(--line); border-radius: 8px; padding: 0.6rem; font-family: ui-monospace, Menlo, monospace; font-size: 0.72rem; color: var(--muted); margin: 0.7rem 0 1rem; }
  .modal-actions { display: flex; justify-content: flex-end; gap: 0.6rem; }
  .btn-cyan { background: var(--cyan); color: #020617; border: none; border-radius: 8px; padding: 0.5rem 1rem; font-weight: 700; font-size: 0.8rem; font-family: inherit; cursor: pointer; }

  @keyframes fadeIn { from { opacity: 0; transform: translateY(-6px); } to { opacity: 1; transform: none; } }
  @keyframes blink { 0%,100% { opacity: 1; } 50% { opacity: 0.35; } }
  @media (max-width: 900px) {
    .grid { grid-template-columns: 1fr; }
    .stats { grid-template-columns: repeat(2, 1fr); }
  }
</style>
</head>
<body>

<header>
  <div class="wrap head row">
    <div class="brand">
      <div class="logo"><i class="fa-solid fa-shield-halved"></i></div>
      <div>
        <div class="row" style="justify-content:flex-start;gap:0.5rem">
          <h1 class="mono">CAMPUS<span>SENTINEL</span></h1>
          <span class="mono" style="font-size:0.68rem;padding:0.15rem 0.45rem;border-radius:5px;background:#082f49;color:#7dd3fc;border:1px solid #155e75">v3</span>
        </div>
        <small>Safety incident intake and triage</small>
      </div>
    </div>
    <div class="row" style="justify-content:flex-end">
      <div id="statusPill" class="pill"><span class="dot"></span><span id="statusText">Local rules engine</span></div>
      <button class="btn-ghost" onclick="toggleModal()"><i class="fa-solid fa-gear" style="color:var(--cyan)"></i> Webhook settings</button>
    </div>
  </div>
</header>

<main class="wrap" style="flex:1">
  <div class="banner"><strong>Simulated reports.</strong> Sample reports use invented names and numbers. Nothing here is a real incident. Student details are never displayed; the feed shows only which categories were redacted.</div>

  <div class="stats">
    <div class="panel stat c1"><div class="row"><span class="label">Processed</span><i class="fa-solid fa-list-check" style="color:var(--cyan)"></i></div><div class="num" id="statTotal">0</div><div class="note">This session</div></div>
    <div class="panel stat c2"><div class="row"><span class="label">PII categories redacted</span><i class="fa-solid fa-user-shield" style="color:var(--emerald)"></i></div><div class="num" id="statPii">0</div><div class="note">Count of categories, not values</div></div>
    <div class="panel stat c3"><div class="row"><span class="label">High / Critical</span><i class="fa-solid fa-triangle-exclamation" style="color:var(--rose)"></i></div><div class="num" id="statCrit">0</div><div class="note">Need immediate action</div></div>
    <div class="panel stat c4"><div class="row"><span class="label">Avg processing time</span><i class="fa-solid fa-bolt" style="color:var(--amber)"></i></div><div class="num" id="statTime">—</div><div class="note" id="statTimeNote">Measured in this browser</div></div>
  </div>

  <div class="grid">
    <div class="stack">
      <div class="panel">
        <div class="row" style="margin-bottom:0.8rem;padding-bottom:0.7rem;border-bottom:1px solid rgba(30,41,59,0.8)">
          <span style="font-weight:700"><i class="fa-solid fa-pen-to-square" style="color:var(--cyan)"></i>&nbsp; Ingest hazard report</span>
          <span class="mono" style="font-size:0.72rem;color:var(--muted)">Raw input</span>
        </div>
        <div class="label" style="font-weight:600;text-transform:none;letter-spacing:0">Sample templates</div>
        <div class="chips">
          <button class="chip" onclick="fillSample('lighting')"><i class="fa-solid fa-lightbulb" style="color:var(--amber)"></i> Broken walkway light</button>
          <button class="chip" onclick="fillSample('water')"><i class="fa-solid fa-droplet" style="color:#60a5fa"></i> Library pipe leak</button>
          <button class="chip" onclick="fillSample('medical')"><i class="fa-solid fa-heart-pulse" style="color:var(--rose)"></i> Medical collapse</button>
          <button class="chip" onclick="fillSample('hazard')"><i class="fa-solid fa-triangle-exclamation" style="color:var(--amber)"></i> Exposed wiring</button>
        </div>
        <form id="incidentForm">
          <label for="reportText" class="label" style="text-transform:none;letter-spacing:0;display:block;margin-bottom:0.4rem">Hazard report (may contain personal details)</label>
          <textarea id="reportText" maxlength="1500" placeholder="Type or paste the report here..."></textarea>
          <div id="processing" class="processing"><i class="fa-solid fa-circle-notch fa-spin"></i>&nbsp; <span id="processingText">Checking for personal details and rating severity...</span></div>
          <button id="submitBtn" type="button" onclick="handleSubmit(new Event('submit'))" class="btn-main"><i class="fa-solid fa-paper-plane"></i> Process incident report</button>
          <div id="answer" style="display:none;margin-top:0.9rem;background:rgba(2,6,23,0.7);border:1px solid var(--line);border-left:4px solid var(--cyan);border-radius:10px;padding:0.9rem"></div>
        </form>
      </div>

      <div class="panel arch">
        <div class="row" style="border-bottom:1px solid var(--line);padding-bottom:0.6rem;margin-bottom:0.2rem"><b style="color:#e2e8f0"><i class="fa-solid fa-diagram-project" style="color:var(--cyan)"></i>&nbsp; Processing steps</b><span class="mono" style="font-size:0.68rem;background:var(--line);padding:0.15rem 0.45rem;border-radius:5px">Privacy first</span></div>
        <div><span>1. Intake</span><span class="ok"><i class="fa-solid fa-check"></i> Active</span></div>
        <div><span>2. Personal detail redaction</span><span class="ok" id="stepRedact"><i class="fa-solid fa-check"></i> Local rules</span></div>
        <div><span>3. Severity rating and summary</span><span class="ok" id="stepTriage"><i class="fa-solid fa-check"></i> Local rules</span></div>
      </div>
    </div>

    <div>
      <div class="feed-bar">
        <span style="font-weight:700;font-size:0.9rem"><i class="fa-solid fa-satellite-dish" style="color:var(--cyan)"></i>&nbsp; Incident feed</span>
        <span class="filters">
          <button id="fAll" class="on" onclick="setFilter('all')">All</button>
          <button id="fCrit" onclick="setFilter('critical')">High / Critical</button>
        </span>
      </div>
      <div id="feed" class="feed"></div>
    </div>
  </div>
</main>

<footer>
  <div class="wrap">
    <span>Campus Sentinel &middot; SBUHacks submission &middot; Built by Ramon Cortez, AI Architect</span>
    <span class="mono">Simulated data for demonstration</span>
  </div>
</footer>

<div id="modal" class="modal" onclick="if(event.target===this)toggleModal()">
  <div class="panel modal-box">
    <h3><span><i class="fa-solid fa-link" style="color:var(--cyan)"></i>&nbsp; Webhook settings</span>
      <button onclick="toggleModal()" style="background:none;border:none;color:var(--muted);cursor:pointer;font-size:1rem"><i class="fa-solid fa-xmark"></i></button></h3>
    <p>Optional. Paste a backend or Relevance AI webhook URL to classify reports with your AI agent. Leave it blank to use the local rules engine. Never put a Gemini API key on this page; keep it on your server.</p>
    <label class="label" style="text-transform:none;letter-spacing:0;display:block;margin-bottom:0.4rem">Endpoint URL</label>
    <input type="url" id="webhookInput" placeholder="https://your-endpoint.example/triage">
    <div class="code">Request: { "params": { "report": "..." } }<br>Expected reply: { "category", "severity_level", "pii_categories", "actionable_summary" }</div>
    <div class="modal-actions">
      <button class="btn-ghost" onclick="toggleModal()">Cancel</button>
      <button class="btn-cyan" onclick="saveWebhook()">Save</button>
    </div>
  </div>
</div>

<script>
  const WEBHOOK_KEY = "sentinel_webhook_url";
  const CATEGORIES = ["Infrastructure", "Medical", "Hazard", "General"];
  const SEVERITIES = ["Critical", "High", "Medium", "Low"];

  // Sample reports are invented. They are used only to fill the form.
  const SAMPLES = {
    lighting: "Report from a student (ID 000000, phone 555-0100): the overhead light on the library walkway near the rear entrance is out and the path is dark.",
    water: "Report from a staff member (ID 000001): water is leaking from a pipe in the basement of the engineering building and is spreading toward the electrical panels.",
    medical: "Urgent call from a bystander (phone 555-0101): a student collapsed at the rec center and is barely breathing.",
    hazard: "Anonymous report: exposed electrical wiring near the fountain outside the student union, with sparks visible."
  };

  // Seed incidents so the feed is never empty. Each seed stores categories only.
  let incidents = [
    seedIncident("INC-8832", "Infrastructure", "Medium", ["Name", "Student ID", "Phone"], "Lighting outage on the library walkway near the rear entrance. Dispatch facilities to restore lighting and arrange temporary patrols.", "2 min ago"),
    seedIncident("INC-8831", "Medical", "Critical", ["Name", "Phone"], "Person collapsed in the rec center with faint breathing. Dispatch campus first responders with an AED immediately.", "9 min ago"),
    seedIncident("INC-8830", "Hazard", "High", ["Name", "Student ID", "Phone"], "Active pipe leak in the engineering basement near electrical panels. Shut off the water valve and send maintenance.", "21 min ago")
  ];

  let processed = 0, piiTotal = 0, timeTotal = 0, timeCount = 0;
  let filter = "all";
  let usingWebhook = false;

  function seedIncident(id, category, severity, piiCats, summary, ago) {
    return { id, category, severity, piiCats, summary, ago, via: "Seed data", status: "Queued for dispatch" };
  }

  const memStore = {};
  function storeGet(k) { try { return localStorage.getItem(k); } catch (e) { return memStore[k] || null; } }
  function storeSet(k, v) { try { localStorage.setItem(k, v); } catch (e) { memStore[k] = v; } }
  function storeDel(k) { try { localStorage.removeItem(k); } catch (e) { delete memStore[k]; } }

  // Escape everything that reaches the page
  function esc(s) {
    return String(s).replace(/[&<>"']/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;", "'": "&#39;" }[c]));
  }

  // Detect categories of personal detail. Values are never stored or shown.
  function detectPii(text) {
    const cats = [];
    if (/\b[A-Z][a-z]+ [A-Z][a-z]+\b/.test(text) || /\bname\b/i.test(text)) cats.push("Name");
    if (/\bID\s*\d{4,}|\b\d{6,8}\b/.test(text)) cats.push("Student ID");
    if (/\b\d{3}[-\s]?\d{3}[-\s]?\d{4}\b/.test(text)) cats.push("Phone");
    if (/[\w.+-]+@[\w-]+\.[\w.]+/.test(text)) cats.push("Email");
    return cats;
  }

  // Local rules: severity, category, summary. Summaries contain no names or numbers.
  function localTriage(text) {
    const t = text.toLowerCase();
    let category = "General", severity = "Low";
    let summary = "Report received. Send a campus safety officer to review and confirm the details.";

    if (/collapsed|breathing|unconscious|bleeding|medical|faint/.test(t)) {
      category = "Medical"; severity = "Critical";
      summary = "Person needs urgent medical attention. Dispatch campus first responders with an AED immediately.";
    } else if (/wiring|sparks|burst|leak|pipe|smoke|fire/.test(t)) {
      category = "Hazard"; severity = /sparks|fire|smoke/.test(t) ? "Critical" : "High";
      summary = "Active hazard reported. Secure the area, shut off the affected utility, and send maintenance or emergency response.";
    } else if (/light|walkway|door|stairs|broken|out/.test(t)) {
      category = "Infrastructure"; severity = "Medium";
      summary = "Infrastructure problem reported. Send facilities to repair it and arrange temporary patrols if the area is dark.";
    }
    return { category, severity_level: severity, pii_categories: detectPii(text), actionable_summary: summary };
  }

  // Validate any webhook reply against allowed values
  function normalize(raw) {
    return {
      category: CATEGORIES.includes(raw.category) ? raw.category : "General",
      severity_level: SEVERITIES.includes(raw.severity_level) ? raw.severity_level : "Medium",
      pii_categories: Array.isArray(raw.pii_categories) ? raw.pii_categories.map(String).slice(0, 6) : [],
      actionable_summary: typeof raw.actionable_summary === "string" ? raw.actionable_summary.slice(0, 400) : "Report processed."
    };
  }

  async function triage(text) {
    const url = storeGet(WEBHOOK_KEY);
    if (url) {
      try {
        const res = await fetch(url, {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify({ params: { report: text } })
        });
        if (!res.ok) throw new Error("HTTP " + res.status);
        const data = await res.json();
        const parsed = typeof data.output === "string" ? JSON.parse(data.output) : (data.output || data);
        return { result: normalize(parsed), via: "Webhook" };
      } catch (err) {
        return { result: localTriage(text), via: "Local rules (webhook failed)" };
      }
    }
    return { result: localTriage(text), via: "Local rules" };
  }

  function showAnswer(inc) {
    const box = document.getElementById("answer");
    box.style.display = "block";
    box.innerHTML =
      '<div class="label" style="margin-bottom:0.5rem">Triage answer</div>' +
      '<div style="font-size:0.9rem;margin-bottom:0.35rem"><b>Severity:</b> <span class="sev ' + esc(inc.severity) + '">' + esc(inc.severity) + '</span> &nbsp; <b>Category:</b> ' + esc(inc.category) + '</div>' +
      '<div style="font-size:0.82rem;margin-bottom:0.35rem"><b>Personal details removed:</b> ' + (inc.piiCats.length ? esc(inc.piiCats.join(", ")) : "none detected") + '</div>' +
      '<div style="font-size:0.85rem;line-height:1.5;margin-bottom:0.35rem"><b>Dispatch summary:</b> ' + esc(inc.summary) + '</div>' +
      '<div style="font-size:0.72rem;color:var(--dim)">' + esc(inc.via) + ' &middot; ' + esc(inc.id) + '</div>';
    box.scrollIntoView({ behavior: "smooth", block: "nearest" });
  }

  async function handleSubmit(e) {
    e.preventDefault();
    const box = document.getElementById("reportText");
    const text = box.value.trim();
    if (!text) {
      box.placeholder = "Paste or type a report first, then click Process.";
      box.focus();
      return;
    }

    const btn = document.getElementById("submitBtn");
    const proc = document.getElementById("processing");
    btn.disabled = true;
    proc.classList.add("on");

    let result, via, elapsed;
    try {
      const start = performance.now();
      ({ result, via } = await triage(text));
      elapsed = (performance.now() - start) / 1000;
    } catch (err) {
      result = localTriage(text);
      via = "Local rules (error recovered)";
      elapsed = 0;
    }

    processed++;
    piiTotal += result.pii_categories.length;
    timeTotal += elapsed; timeCount++;

    incidents.unshift({
      id: "INC-" + Math.floor(1000 + Math.random() * 9000),
      category: result.category,
      severity: result.severity_level,
      piiCats: result.pii_categories,
      summary: result.actionable_summary,
      ago: "Just now",
      via,
      status: "Queued for dispatch"
    });

    box.value = "";
    btn.disabled = false;
    proc.classList.remove("on");
    if (filter !== "all" && result.severity !== "Critical" && result.severity !== "High") setFilter("all");
    render();
    showAnswer(incidents[0]);
  }

  function fillSample(k) {
    document.getElementById("reportText").value = SAMPLES[k] || "";
  }

  function setFilter(f) {
    filter = f;
    document.getElementById("fAll").classList.toggle("on", f === "all");
    document.getElementById("fCrit").classList.toggle("on", f === "critical");
    render();
  }

  function sevIcon(s) {
    return { Critical: "fa-radiation", High: "fa-triangle-exclamation", Medium: "fa-circle-exclamation", Low: "fa-circle-info" }[s];
  }

  function render() {
    const feed = document.getElementById("feed");
    feed.innerHTML = "";

    const shown = incidents.filter(i => filter === "all" || i.severity === "Critical" || i.severity === "High");
    if (shown.length === 0) {
      feed.innerHTML = '<div class="empty">No incidents match this filter.</div>';
    }

    shown.forEach(i => {
      const card = document.createElement("div");
      card.className = "card";
      const piiText = i.piiCats.length ? esc(i.piiCats.join(", ")) + " removed" : "None detected";
      card.innerHTML =
        '<div class="card-top"><div class="left">' +
          '<span class="id">' + esc(i.id) + '</span>' +
          '<span class="sev ' + esc(i.severity) + '"><i class="fa-solid ' + sevIcon(i.severity) + '"></i> ' + esc(i.severity) + '</span>' +
          '<span class="cat">' + esc(i.category) + '</span></div>' +
          '<span class="time"><i class="fa-regular fa-clock"></i> ' + esc(i.ago) + '</span></div>' +
        '<div class="pii"><i class="fa-solid fa-shield-cat" style="color:var(--emerald)"></i><span>Personal details:</span><b>' + piiText + '</b></div>' +
        '<div><div class="summary-label">Dispatch summary</div><div class="summary">' + esc(i.summary) + '</div></div>' +
        '<div class="card-foot"><span>Status: <strong>' + esc(i.status) + '</strong> <span class="via">· ' + esc(i.via) + '</span></span>' +
          '<button class="btn-ghost" onclick="copySummary(\'' + esc(i.id) + '\')"><i class="fa-regular fa-copy"></i> Copy summary</button></div>';
      feed.appendChild(card);
    });

    document.getElementById("statTotal").textContent = processed;
    document.getElementById("statPii").textContent = piiTotal;
    document.getElementById("statCrit").textContent = incidents.filter(i => i.severity === "Critical" || i.severity === "High").length;
    document.getElementById("statTime").textContent = timeCount ? (timeTotal / timeCount).toFixed(2) + "s" : "—";
    document.getElementById("statTimeNote").textContent = timeCount ? "Across " + timeCount + " submission(s)" : "Submit a report to measure";
  }

  function copySummary(id) {
    const inc = incidents.find(i => i.id === id);
    if (!inc) return;
    const done = () => alert("Summary copied.");
    if (navigator.clipboard) navigator.clipboard.writeText(inc.summary).then(done, () => alert(inc.summary));
    else alert(inc.summary);
  }

  function toggleModal() {
    const m = document.getElementById("modal");
    m.classList.toggle("on");
    if (m.classList.contains("on")) document.getElementById("webhookInput").value = storeGet(WEBHOOK_KEY) || "";
  }

  function saveWebhook() {
    const url = document.getElementById("webhookInput").value.trim();
    if (url) storeSet(WEBHOOK_KEY, url);
    else storeDel(WEBHOOK_KEY);
    updateStatus();
    toggleModal();
  }

  function updateStatus() {
    usingWebhook = !!storeGet(WEBHOOK_KEY);
    const pill = document.getElementById("statusPill");
    pill.className = "pill" + (usingWebhook ? " live" : "");
    document.getElementById("statusText").textContent = usingWebhook ? "Webhook connected" : "Local rules engine";
    document.getElementById("stepTriage").innerHTML = usingWebhook
      ? '<i class="fa-solid fa-check"></i> Webhook'
      : '<i class="fa-solid fa-check"></i> Local rules';
  }

  document.getElementById("incidentForm").addEventListener("submit", handleSubmit);
  try { updateStatus(); } catch (e) { /* keep the page working */ }
  render();
</script>
</body>
</html>
