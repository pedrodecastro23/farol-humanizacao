<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Farol — Humanização · Samarco v8</title>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<!-- Firebase SDK -->
<script type="module">
  import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js";
  import { getDatabase, ref, set, get, onValue } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-database.js";

  const firebaseConfig = {
    apiKey: "AIzaSyDaQiVHz7Tn-cXBcknkvV7r4jVGnnZ7LrM",
    authDomain: "farol---humanizacao.firebaseapp.com",
    databaseURL: "https://farol---humanizacao-default-rtdb.firebaseio.com",
    projectId: "farol---humanizacao",
    storageBucket: "farol---humanizacao.firebasestorage.app",
    messagingSenderId: "238007819045",
    appId: "1:238007819045:web:0da7382112c13ae6ac58cc"
  };

  const app = initializeApp(firebaseConfig);
  const db = getDatabase(app);

  // Expose Firebase helpers to global scope
  window._fbSet = (path, value) => set(ref(db, path), value);
  window._fbGet = (path) => get(ref(db, path)).then(snap => snap.exists() ? snap.val() : null);
  window._fbListen = (path, callback) => onValue(ref(db, path), snap => callback(snap.exists() ? snap.val() : null));
  window._firebaseReady = true;
  document.dispatchEvent(new Event('firebase-ready'));
</script>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0e1a;
    --surface: #101623;
    --card: #151e30;
    --card2: #1a2540;
    --border: rgba(255,255,255,0.06);
    --border2: rgba(255,255,255,0.12);
    --text: #e8eaf0;
    --muted: #8b93a8;
    --faint: #3d4459;

    --c-concluido: #22c55e;
    --c-concluido-bg: rgba(34,197,94,0.12);
    --c-andamento: #60a5fa;
    --c-andamento-bg: rgba(96,165,250,0.12);
    --c-programado: #a78bfa;
    --c-programado-bg: rgba(167,139,250,0.12);
    --c-previsto: #f59e0b;
    --c-previsto-bg: rgba(245,158,11,0.12);
    --c-backlog: #6b7280;
    --c-backlog-bg: rgba(107,114,128,0.12);
    --c-paralizado: #ef4444;
    --c-paralizado-bg: rgba(239,68,68,0.12);
    --c-planejado: #06b6d4;
    --c-planejado-bg: rgba(6,182,212,0.12);

    --accent: #1d4ed8;
    --accent-light: #3b82f6;
    --accent-glow: rgba(29,78,216,0.25);
    --accent-soft: rgba(59,130,246,0.12);

    --radius: 10px;
    --radius-sm: 6px;
    --shadow: 0 1px 3px rgba(0,0,0,0.4), 0 0 0 1px var(--border);
  }

  body { font-family: 'Sora', sans-serif; background: var(--bg); color: var(--text); min-height: 100vh; font-size: 14px; line-height: 1.5; }

  /* ── LOADING SCREEN ── */
  #loadingScreen {
    position: fixed; inset: 0; background: var(--bg);
    display: flex; align-items: center; justify-content: center;
    z-index: 10000; flex-direction: column; gap: 16px;
  }
  .loading-dot { width: 44px; height: 44px; border-radius: 10px; background: var(--accent); display: flex; align-items: center; justify-content: center; font-weight: 700; font-size: 18px; color: #fff; animation: pulse 1.4s ease-in-out infinite; }
  .loading-text { font-size: 13px; color: var(--muted); }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.6;transform:scale(0.95)} }

  /* ── LOGIN OVERLAY ── */
  #loginOverlay {
    position: fixed; inset: 0; background: rgba(8,11,20,0.97);
    display: flex; align-items: center; justify-content: center; z-index: 9999;
    backdrop-filter: blur(12px);
  }
  .login-box {
    background: var(--card); border: 1px solid var(--border2);
    border-radius: 18px; padding: 44px 40px; width: 380px;
    box-shadow: 0 24px 80px rgba(0,0,0,0.6), 0 0 0 1px rgba(29,78,216,0.15);
  }
  .login-logo { display: flex; align-items: center; gap: 14px; margin-bottom: 32px; }
  .login-logo-dot { width: 44px; height: 44px; border-radius: 11px; background: var(--accent); display: flex; align-items: center; justify-content: center; font-weight: 700; font-size: 18px; color: #fff; box-shadow: 0 0 20px var(--accent-glow); }
  .login-logo-text { font-size: 15px; font-weight: 600; }
  .login-logo-sub { font-size: 11px; color: var(--muted); margin-top: 2px; }
  .login-title { font-size: 20px; font-weight: 700; margin-bottom: 6px; }
  .login-sub { font-size: 12px; color: var(--muted); margin-bottom: 26px; line-height: 1.6; }
  .login-field { margin-bottom: 14px; }
  .login-field label { font-size: 11px; font-weight: 500; color: var(--muted); text-transform: uppercase; letter-spacing: 0.05em; display: block; margin-bottom: 6px; }
  .login-field input {
    width: 100%; background: var(--surface); border: 1px solid var(--border2);
    border-radius: var(--radius-sm); color: var(--text); font-family: 'Sora', sans-serif;
    font-size: 13px; padding: 10px 13px; outline: none; transition: border 0.15s;
  }
  .login-field input:focus { border-color: var(--accent-light); box-shadow: 0 0 0 3px rgba(59,130,246,0.12); }
  .login-btn {
    width: 100%; background: var(--accent); border: none; border-radius: var(--radius-sm);
    color: #fff; font-family: 'Sora', sans-serif; font-size: 13px; font-weight: 600;
    padding: 11px; cursor: pointer; transition: all 0.15s; margin-top: 8px;
    box-shadow: 0 4px 14px rgba(29,78,216,0.4);
  }
  .login-btn:hover { background: var(--accent-light); box-shadow: 0 4px 20px rgba(59,130,246,0.5); }
  .login-btn-secondary {
    width: 100%; background: var(--surface); border: 1px solid var(--border2);
    color: var(--muted); font-family: 'Sora', sans-serif; font-size: 12px; font-weight: 500;
    padding: 9px; cursor: pointer; transition: all 0.15s; margin-top: 8px; border-radius: var(--radius-sm);
  }
  .login-btn-secondary:hover { border-color: rgba(255,255,255,0.2); color: var(--text); }
  .login-error { font-size: 12px; color: var(--c-paralizado); margin-top: 10px; display: none; background: rgba(239,68,68,0.08); padding: 8px 10px; border-radius: var(--radius-sm); border: 1px solid rgba(239,68,68,0.2); }

  /* ── TOP BAR ── */
  .topbar {
    background: var(--surface); border-bottom: 1px solid var(--border);
    padding: 0 28px; height: 56px; display: flex; align-items: center;
    justify-content: space-between; position: sticky; top: 0; z-index: 100;
  }
  .topbar-left { display: flex; align-items: center; gap: 14px; }
  .logo-dot { width: 32px; height: 32px; border-radius: 8px; background: var(--accent); display: flex; align-items: center; justify-content: center; font-weight: 700; font-size: 14px; color: #fff; box-shadow: 0 0 12px var(--accent-glow); }
  .topbar-title { font-weight: 600; font-size: 15px; }
  .topbar-sub { color: var(--muted); font-size: 12px; margin-top: 1px; }
  .topbar-right { display: flex; align-items: center; gap: 10px; }
  .sync-badge { font-size: 10px; color: var(--c-concluido); display: flex; align-items: center; gap: 5px; background: rgba(34,197,94,0.08); border: 1px solid rgba(34,197,94,0.2); padding: 3px 8px; border-radius: 20px; }
  .sync-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--c-concluido); animation: blink 2s ease-in-out infinite; }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.3} }
  .topbar-btn {
    display: flex; align-items: center; gap: 6px;
    background: var(--card); border: 1px solid var(--border2);
    border-radius: var(--radius-sm); color: var(--muted); font-family: 'Sora', sans-serif;
    font-size: 11px; font-weight: 500; padding: 6px 12px; cursor: pointer; transition: all 0.15s;
  }
  .topbar-btn:hover { color: var(--text); border-color: rgba(255,255,255,0.2); }
  .add-btn {
    display: flex; align-items: center; gap: 6px;
    background: var(--accent); border: none; border-radius: var(--radius-sm);
    color: #fff; font-family: 'Sora', sans-serif; font-size: 12px; font-weight: 600;
    padding: 7px 14px; cursor: pointer; transition: all 0.15s;
    box-shadow: 0 2px 10px rgba(29,78,216,0.35);
  }
  .add-btn:hover { background: var(--accent-light); }
  .user-badge {
    display: flex; align-items: center; gap: 8px;
    background: var(--card); border: 1px solid var(--border2);
    border-radius: 20px; padding: 4px 12px 4px 6px; cursor: pointer;
    font-size: 12px; font-weight: 500; transition: border-color 0.15s;
  }
  .user-badge:hover { border-color: var(--accent-light); }
  .user-avatar { width: 24px; height: 24px; border-radius: 50%; background: var(--accent); display: flex; align-items: center; justify-content: center; font-size: 10px; font-weight: 700; color: #fff; }

  /* ── LAYOUT ── */
  .page { padding: 24px 28px; max-width: 1600px; margin: 0 auto; }

  /* ── DASHBOARD SECTION ── */
  .section-label { font-size: 10px; font-weight: 700; color: var(--accent-light); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 12px; display: flex; align-items: center; gap: 8px; }
  .section-label::after { content: ''; flex: 1; height: 1px; background: var(--border2); }

  /* ── METRICS ── */
  .metrics { display: grid; grid-template-columns: repeat(6, 1fr); gap: 10px; margin-bottom: 20px; }
  .metric-card {
    background: var(--card); border-radius: var(--radius); padding: 16px 18px;
    border: 1px solid var(--border); position: relative; overflow: hidden;
    cursor: pointer; transition: all 0.2s;
  }
  .metric-card:hover { transform: translateY(-1px); border-color: var(--border2); }
  .metric-card.active-filter { border-color: var(--accent-light); box-shadow: 0 0 0 1px var(--accent-light), 0 4px 16px var(--accent-glow); }
  .metric-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; border-radius: var(--radius) var(--radius) 0 0; }
  .metric-card.m-total::before { background: linear-gradient(90deg, var(--accent), var(--accent-light)); }
  .metric-card.m-andamento::before { background: var(--c-andamento); }
  .metric-card.m-programado::before { background: var(--c-programado); }
  .metric-card.m-concluido::before { background: var(--c-concluido); }
  .metric-card.m-backlog::before { background: var(--c-backlog); }
  .metric-card.m-paralizado::before { background: var(--c-paralizado); }
  .metric-label { font-size: 10px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.05em; font-weight: 600; margin-bottom: 8px; }
  .metric-value { font-size: 30px; font-weight: 700; line-height: 1; }
  .metric-card.m-total .metric-value { color: var(--accent-light); }
  .metric-card.m-andamento .metric-value { color: var(--c-andamento); }
  .metric-card.m-programado .metric-value { color: var(--c-programado); }
  .metric-card.m-concluido .metric-value { color: var(--c-concluido); }
  .metric-card.m-backlog .metric-value { color: var(--c-backlog); }
  .metric-card.m-paralizado .metric-value { color: var(--c-paralizado); }
  .metric-sub { font-size: 10px; color: var(--faint); margin-top: 4px; }

  /* ── CHARTS DASHBOARD ── */
  .dashboard-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 14px;
    margin-bottom: 22px;
  }
  .chart-card {
    background: var(--card); border-radius: var(--radius);
    border: 1px solid var(--border); padding: 20px 22px;
    position: relative; overflow: hidden;
  }
  .chart-card::before {
    content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, var(--accent), transparent);
  }
  .chart-title {
    font-size: 11px; font-weight: 700; color: var(--accent-light);
    text-transform: uppercase; letter-spacing: 0.07em; margin-bottom: 4px;
  }
  .chart-subtitle { font-size: 12px; color: var(--muted); margin-bottom: 16px; }
  .chart-canvas-wrap { position: relative; }
  .chart-center-label {
    position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);
    text-align: center; pointer-events: none;
  }
  .chart-center-num { font-size: 24px; font-weight: 700; color: var(--text); }
  .chart-center-txt { font-size: 10px; color: var(--muted); }
  .chart-legend { display: flex; flex-wrap: wrap; gap: 5px 10px; margin-top: 12px; }
  .chart-legend-item { display: flex; align-items: center; gap: 5px; font-size: 11px; color: var(--muted); }
  .chart-legend-dot { width: 8px; height: 8px; border-radius: 2px; flex-shrink: 0; }

  /* Big number chart card */
  .chart-card-wide { grid-column: span 1; }

  /* ── SEARCH ── */
  .search-wrap { position: relative; }
  .search-input {
    background: var(--card2); border: 1px solid var(--border2); border-radius: var(--radius-sm);
    color: var(--text); font-family: 'Sora', sans-serif; font-size: 13px;
    padding: 8px 13px 8px 36px; width: 240px; outline: none; transition: all 0.15s;
  }
  .search-input:focus { border-color: var(--accent-light); box-shadow: 0 0 0 3px var(--accent-soft); }
  .search-icon { position: absolute; left: 11px; top: 50%; transform: translateY(-50%); color: var(--muted); pointer-events: none; font-size: 14px; }

  /* ── TABLE SECTION ── */
  .table-section { background: var(--card); border-radius: var(--radius); border: 1px solid var(--border); overflow: hidden; }
  .table-header { padding: 16px 20px; border-bottom: 1px solid var(--border); display: flex; align-items: center; justify-content: space-between; gap: 12px; flex-wrap: wrap; }
  .table-header-title { font-size: 13px; font-weight: 600; }
  .table-count { font-size: 11px; color: var(--muted); font-family: 'DM Mono', monospace; }
  .table-wrap { overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; font-size: 13px; }
  thead th { padding: 10px 14px; text-align: left; font-size: 10px; font-weight: 700; color: var(--muted); text-transform: uppercase; letter-spacing: 0.07em; border-bottom: 1px solid var(--border); background: var(--surface); white-space: nowrap; cursor: pointer; user-select: none; }
  thead th:hover { color: var(--text); }
  thead th.sort-asc::after { content: ' ↑'; color: var(--accent-light); }
  thead th.sort-desc::after { content: ' ↓'; color: var(--accent-light); }
  tbody tr { border-bottom: 1px solid var(--border); transition: background 0.1s; cursor: pointer; }
  tbody tr:last-child { border-bottom: none; }
  tbody tr:hover { background: rgba(59,130,246,0.04); }
  tbody tr.expanded { background: rgba(29,78,216,0.05); }
  td { padding: 11px 14px; vertical-align: middle; }
  td.obra-col { font-weight: 500; max-width: 240px; }
  td.obra-col span { display: block; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 230px; }
  td.obra-col .obra-area { font-size: 11px; color: var(--muted); font-weight: 400; margin-top: 2px; }

  /* ── BADGES ── */
  .badge { display: inline-flex; align-items: center; gap: 5px; padding: 3px 9px; border-radius: 12px; font-size: 11px; font-weight: 500; white-space: nowrap; letter-spacing: 0.02em; }
  .badge::before { content: ''; width: 5px; height: 5px; border-radius: 50%; flex-shrink: 0; }
  .badge-concluido { background: var(--c-concluido-bg); color: var(--c-concluido); }
  .badge-concluido::before { background: var(--c-concluido); }
  .badge-andamento { background: var(--c-andamento-bg); color: var(--c-andamento); }
  .badge-andamento::before { background: var(--c-andamento); }
  .badge-programado { background: var(--c-programado-bg); color: var(--c-programado); }
  .badge-programado::before { background: var(--c-programado); }
  .badge-backlog { background: var(--c-backlog-bg); color: var(--c-backlog); }
  .badge-backlog::before { background: var(--c-backlog); }
  .badge-paralizado { background: var(--c-paralizado-bg); color: var(--c-paralizado); }
  .badge-paralizado::before { background: var(--c-paralizado); }
  .badge-previsto { background: var(--c-previsto-bg); color: var(--c-previsto); }
  .badge-previsto::before { background: var(--c-previsto); }
  .badge-planejado { background: var(--c-planejado-bg); color: var(--c-planejado); }
  .badge-planejado::before { background: var(--c-planejado); }

  /* Status inline select */
  .status-select-wrap { position: relative; display: inline-flex; }
  .status-select {
    appearance: none; background: transparent; border: none;
    font-family: 'Sora', sans-serif; font-size: 11px; font-weight: 500;
    cursor: pointer; outline: none; padding: 0 18px 0 0;
    position: relative; color: inherit;
  }
  .status-select-arrow { position: absolute; right: 2px; top: 50%; transform: translateY(-50%); font-size: 9px; color: inherit; pointer-events: none; }

  /* ── LOC PILL ── */
  .loc-pill { font-size: 10px; font-weight: 500; color: var(--muted); background: rgba(255,255,255,0.06); border-radius: 8px; padding: 2px 8px; white-space: nowrap; }

  /* ── DATE ── */
  .date-col { font-family: 'DM Mono', monospace; font-size: 12px; color: var(--muted); white-space: nowrap; }
  .date-col.overdue { color: var(--c-paralizado); font-weight: 500; }
  .date-col.soon { color: var(--c-previsto); }

  /* ── TIPO PILL ── */
  .tipo-pill { font-size: 10px; padding: 2px 7px; border-radius: 6px; background: rgba(255,255,255,0.05); color: var(--muted); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 130px; display: inline-block; }
  .tipo-hum { background: rgba(29,78,216,0.15); color: var(--accent-light); }
  .tipo-mob { background: rgba(167,139,250,0.1); color: var(--c-programado); }
  .tipo-lay { background: rgba(96,165,250,0.1); color: var(--c-andamento); }
  .tipo-plo { background: rgba(6,182,212,0.1); color: var(--c-planejado); }
  .tipo-pla { background: rgba(34,197,94,0.1); color: var(--c-concluido); }
  .tipo-pai { background: rgba(245,158,11,0.1); color: var(--c-previsto); }

  .projetista-col { font-size: 12px; color: var(--muted); white-space: nowrap; }
  .mini-progress { display: flex; gap: 2px; height: 6px; border-radius: 4px; overflow: hidden; min-width: 60px; }
  .mini-seg { flex: 1; }
  .mini-seg.conc { background: var(--c-concluido); }
  .mini-seg.and { background: var(--c-andamento); }
  .mini-seg.prev { background: rgba(255,255,255,0.15); }
  .mini-seg.plan { background: var(--c-planejado); }
  .mini-seg.na { background: rgba(255,255,255,0.06); }

  .inline-info { display: flex; gap: 16px; flex-wrap: wrap; padding: 12px 20px; font-size: 12px; border-top: 1px solid var(--border); }
  .info-item { display: flex; gap: 4px; align-items: center; }
  .info-item span:first-child { color: var(--muted); }
  .info-item span:last-child { color: var(--text); font-weight: 500; }

  .expand-arrow { transition: transform 0.2s; display: inline-block; color: var(--muted); font-size: 12px; }
  .expand-arrow.open { transform: rotate(90deg); }

  .no-results { padding: 48px; text-align: center; color: var(--muted); font-size: 13px; }

  /* ── EXPAND ROW ── */
  .expand-row td { padding: 0; background: rgba(10,14,26,0.7); }
  .expand-content { padding: 16px 20px 20px; border-top: 1px solid var(--border); display: grid; grid-template-columns: repeat(auto-fill, minmax(130px, 1fr)); gap: 10px; }
  .disc-item { background: var(--surface); border-radius: var(--radius-sm); border: 1px solid var(--border); padding: 10px 12px; text-align: center; transition: background 0.2s, border-color 0.2s; }
  .disc-name { font-size: 10px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.05em; margin-bottom: 6px; font-weight: 500; }
  .disc-select {
    background: var(--card); border: 1px solid var(--border2); border-radius: 10px;
    color: var(--text); font-family: 'Sora', sans-serif; font-size: 10px; font-weight: 500;
    padding: 3px 6px; cursor: pointer; outline: none; width: 100%; transition: border-color 0.15s;
  }
  .disc-select:focus { border-color: var(--accent-light); }

  /* ── OBSERVATIONS ── */
  .obs-section { padding: 14px 20px 18px; border-top: 1px solid var(--border); }
  .obs-header { font-size: 11px; font-weight: 600; color: var(--muted); text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 10px; display: flex; align-items: center; justify-content: space-between; }
  .obs-list { display: flex; flex-direction: column; gap: 8px; margin-bottom: 12px; }
  .obs-item { background: var(--surface); border-radius: var(--radius-sm); border: 1px solid var(--border); padding: 10px 12px; }
  .obs-meta { font-size: 10px; color: var(--faint); margin-bottom: 4px; display: flex; gap: 8px; }
  .obs-meta .obs-author { color: var(--accent-light); font-weight: 500; }
  .obs-text { font-size: 12px; color: var(--text); line-height: 1.5; }
  .obs-input-row { display: flex; gap: 8px; }
  .obs-input { flex: 1; background: var(--surface); border: 1px solid var(--border2); border-radius: var(--radius-sm); color: var(--text); font-family: 'Sora', sans-serif; font-size: 12px; padding: 7px 10px; outline: none; transition: border-color 0.15s; }
  .obs-input:focus { border-color: var(--accent-light); }
  .obs-btn { background: var(--accent); border: none; border-radius: var(--radius-sm); color: #fff; font-family: 'Sora', sans-serif; font-size: 11px; font-weight: 600; padding: 7px 14px; cursor: pointer; white-space: nowrap; }
  .obs-empty { font-size: 12px; color: var(--faint); font-style: italic; }

  /* ── FINANCIAL ── */
  .finance-section { padding: 10px 20px 14px; border-top: 1px solid var(--border); display: flex; gap: 16px; flex-wrap: wrap; }
  .finance-field { display: flex; flex-direction: column; gap: 4px; }
  .finance-field label { font-size: 10px; font-weight: 500; color: var(--faint); text-transform: uppercase; letter-spacing: 0.05em; }
  .finance-field input { background: var(--surface); border: 1px solid var(--border2); border-radius: var(--radius-sm); color: var(--text); font-family: 'DM Mono', monospace; font-size: 12px; padding: 5px 10px; outline: none; transition: border-color 0.15s; width: 200px; }
  .finance-field input:focus { border-color: var(--accent-light); }
  .finance-save { background: none; border: 1px solid var(--border2); border-radius: var(--radius-sm); color: var(--muted); font-family: 'Sora', sans-serif; font-size: 11px; padding: 5px 12px; cursor: pointer; align-self: flex-end; transition: all 0.15s; }
  .finance-save:hover { color: var(--text); border-color: rgba(255,255,255,0.25); }
  .delete-demand-btn { background: rgba(239,68,68,0.08); border: 1px solid rgba(239,68,68,0.25); border-radius: var(--radius-sm); color: #ef4444; font-family: 'Sora', sans-serif; font-size: 11px; padding: 5px 12px; cursor: pointer; align-self: flex-end; margin-left: auto; transition: all 0.15s; }
  .delete-demand-btn:hover { background: rgba(239,68,68,0.18); border-color: rgba(239,68,68,0.5); }

  /* ── AUDIT TAG ── */
  .audit-tag { font-size: 9px; background: rgba(59,130,246,0.15); color: var(--accent-light); border-radius: 4px; padding: 1px 5px; font-weight: 500; }

  /* ── FILES SECTION ── */
  .files-section { padding: 14px 20px 18px; border-top: 1px solid var(--border); }
  .files-header { font-size: 11px; font-weight: 600; color: var(--muted); text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 12px; display: flex; align-items: center; justify-content: space-between; }
  .files-list { display: flex; flex-direction: column; gap: 6px; margin-bottom: 12px; }
  .file-item {
    display: flex; align-items: center; gap: 10px;
    background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius-sm);
    padding: 8px 12px; transition: border-color 0.15s;
  }
  .file-item:hover { border-color: var(--border2); }
  .file-icon { font-size: 18px; flex-shrink: 0; width: 24px; text-align: center; }
  .file-meta { flex: 1; min-width: 0; }
  .file-name { font-size: 12px; font-weight: 500; color: var(--text); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 320px; }
  .file-info { font-size: 10px; color: var(--faint); margin-top: 2px; }
  .file-actions { display: flex; gap: 6px; flex-shrink: 0; }
  .file-btn { background: none; border: 1px solid var(--border2); border-radius: var(--radius-sm); color: var(--muted); font-family: 'Sora', sans-serif; font-size: 10px; padding: 3px 9px; cursor: pointer; transition: all 0.15s; }
  .file-btn:hover { color: var(--text); border-color: rgba(255,255,255,0.25); }
  .file-btn.danger { border-color: rgba(239,68,68,0.25); color: rgba(239,68,68,0.7); }
  .file-btn.danger:hover { background: rgba(239,68,68,0.08); border-color: rgba(239,68,68,0.5); color: #ef4444; }
  .file-upload-area {
    border: 2px dashed var(--border2); border-radius: var(--radius-sm);
    padding: 16px; text-align: center; cursor: pointer;
    transition: all 0.2s; position: relative;
  }
  .file-upload-area:hover, .file-upload-area.drag-over { border-color: var(--accent-light); background: rgba(59,130,246,0.05); }
  .file-upload-area input[type=file] { position: absolute; inset: 0; opacity: 0; cursor: pointer; width: 100%; height: 100%; }
  .file-upload-label { font-size: 12px; color: var(--muted); pointer-events: none; }
  .file-upload-label strong { color: var(--accent-light); }
  .file-empty { font-size: 12px; color: var(--faint); font-style: italic; }

  /* ── DISC COLOR STATES ── */
  .disc-item.disc-andamento { background: rgba(59,130,246,0.18); border-color: rgba(59,130,246,0.4); }
  .disc-item.disc-concluido { background: rgba(34,197,94,0.18); border-color: rgba(34,197,94,0.4); }
  .disc-item.disc-paralizado { background: rgba(239,68,68,0.18); border-color: rgba(239,68,68,0.4); }
  .disc-item.disc-previsto, .disc-item.disc-planejado { background: rgba(107,114,128,0.20); border-color: rgba(107,114,128,0.4); }

  /* ── MODAL ── */
  .modal-overlay {
    display: none; position: fixed; inset: 0; background: rgba(8,11,20,0.88);
    z-index: 500; align-items: center; justify-content: center;
    backdrop-filter: blur(6px);
  }
  .modal-overlay.open { display: flex; }
  .modal {
    background: var(--card); border: 1px solid var(--border2); border-radius: 14px;
    width: 680px; max-width: 96vw; max-height: 90vh; overflow-y: auto;
    box-shadow: 0 24px 64px rgba(0,0,0,0.7);
  }
  .modal-header { padding: 22px 24px 18px; border-bottom: 1px solid var(--border); display: flex; align-items: center; justify-content: space-between; }
  .modal-title { font-size: 15px; font-weight: 600; }
  .modal-close { background: none; border: none; color: var(--muted); font-size: 20px; cursor: pointer; padding: 4px; border-radius: 6px; transition: color 0.12s; }
  .modal-close:hover { color: var(--text); }
  .modal-body { padding: 22px 24px; }
  .modal-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .form-field { display: flex; flex-direction: column; gap: 6px; }
  .form-field label { font-size: 11px; font-weight: 500; color: var(--muted); text-transform: uppercase; letter-spacing: 0.05em; }
  .form-field input, .form-field select, .form-field textarea {
    background: var(--surface); border: 1px solid var(--border2); border-radius: var(--radius-sm);
    color: var(--text); font-family: 'Sora', sans-serif; font-size: 13px;
    padding: 8px 12px; outline: none; transition: border-color 0.15s; width: 100%;
  }
  .form-field input:focus, .form-field select:focus, .form-field textarea:focus { border-color: var(--accent-light); box-shadow: 0 0 0 3px var(--accent-soft); }
  .form-field textarea { resize: vertical; min-height: 72px; }
  .form-field select option { background: var(--card); }
  .modal-footer { padding: 18px 24px; border-top: 1px solid var(--border); display: flex; justify-content: flex-end; gap: 10px; }
  .btn-secondary { background: var(--surface); border: 1px solid var(--border2); border-radius: var(--radius-sm); color: var(--muted); font-family: 'Sora', sans-serif; font-size: 13px; padding: 8px 18px; cursor: pointer; transition: all 0.15s; }
  .btn-secondary:hover { color: var(--text); border-color: rgba(255,255,255,0.2); }
  .btn-primary { background: var(--accent); border: none; border-radius: var(--radius-sm); color: #fff; font-family: 'Sora', sans-serif; font-size: 13px; font-weight: 600; padding: 8px 20px; cursor: pointer; transition: all 0.15s; }
  .btn-primary:hover { background: var(--accent-light); }
  .section-divider-modal { font-size: 11px; font-weight: 600; color: var(--muted); text-transform: uppercase; letter-spacing: 0.07em; padding: 12px 0 6px; border-top: 1px solid var(--border); margin-top: 4px; grid-column: 1 / -1; }
  .disc-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; grid-column: 1 / -1; }
  .disc-form-item { display: flex; flex-direction: column; gap: 5px; }
  .disc-form-item label { font-size: 10px; font-weight: 500; color: var(--faint); text-transform: uppercase; letter-spacing: 0.05em; }

  /* ── VISITOR BANNER ── */
  #visitorBanner { display:none; background:rgba(107,114,128,0.1); border-bottom:1px solid var(--border2); padding:8px 28px; font-size:12px; color:var(--muted); align-items:center; gap:8px; }

  /* ── RESPONSIVE ── */
  @media (max-width:1280px) { .dashboard-grid { grid-template-columns: 1fr 1fr; } .metrics { grid-template-columns: repeat(3,1fr); } }
  @media (max-width:900px) { .dashboard-grid { grid-template-columns: 1fr; } .filter-grid { grid-template-columns: 1fr 1fr; } .page { padding: 14px; } .topbar { padding: 0 14px; } }

  /* ── SAVE TOAST ── */
  #saveToast {
    position: fixed; bottom: 24px; right: 24px; background: var(--c-concluido);
    color: #fff; font-size: 12px; font-weight: 600; padding: 10px 18px;
    border-radius: var(--radius); box-shadow: 0 4px 20px rgba(34,197,94,0.4);
    opacity: 0; transform: translateY(8px); transition: all 0.3s; z-index: 9998;
    pointer-events: none;
  }
  #saveToast.show { opacity: 1; transform: translateY(0); }
</style>
</head>
<body>

<!-- LOADING -->
<div id="loadingScreen">
  <div class="loading-dot">S</div>
  <div class="loading-text">Carregando dados…</div>
</div>

<!-- SAVE TOAST -->
<div id="saveToast">✓ Salvo e sincronizado</div>

<!-- LOGIN OVERLAY -->
<div id="loginOverlay" style="display:none;">
  <div class="login-box">
    <div class="login-logo">
      <div class="login-logo-dot">S</div>
      <div>
        <div class="login-logo-text">Farol — Humanização</div>
        <div class="login-logo-sub">Gerência de Infraestrutura · 2026</div>
      </div>
    </div>
    <div class="login-title">Acesso ao sistema</div>
    <div class="login-sub">Suas edições são salvas automaticamente e sincronizadas com todos os usuários.</div>
    <div class="login-field">
      <label>Nome de usuário</label>
      <input type="text" id="loginUser" placeholder="ex: leticia.ulhoa" autocomplete="username">
    </div>
    <div class="login-field">
      <label>Senha</label>
      <input type="password" id="loginPass" placeholder="••••••••" autocomplete="current-password">
    </div>
    <button class="login-btn" onclick="doLogin()">Entrar</button>
    <button class="login-btn-secondary" onclick="doLoginVisitor()">Entrar como Visitante (somente leitura)</button>
    <div class="login-error" id="loginError">Usuário ou senha incorretos.</div>
  </div>
</div>

<!-- VISITOR BANNER -->
<div id="visitorBanner">
  <span>👁️</span><span>Você está em modo <strong>Visitante</strong> — apenas visualização.</span>
</div>

<!-- TOP BAR -->
<div class="topbar">
  <div class="topbar-left">
    <div class="logo-dot">S</div>
    <div>
      <div class="topbar-title">Farol — Humanização</div>
      <div class="topbar-sub">Gerência de Infraestrutura · 2026</div>
    </div>
  </div>
  <div class="topbar-right">
    <div class="sync-badge"><div class="sync-dot"></div><span>Sincronizado</span></div>
    <button class="add-btn" id="addDemandBtn" onclick="openNewModal()" style="display:none;">＋ Nova demanda</button>
    <button class="topbar-btn" id="manageUsersBtn" onclick="openManageUsersModal()" style="display:none;">👥 Usuários</button>
    <button class="topbar-btn" id="changePwdBtn" onclick="showChangePasswordModal(false)" style="display:none;">🔑 Senha</button>
    <button class="topbar-btn" id="auditBtn" onclick="openAuditModal()" style="display:none;">📋 Histórico</button>
    <div class="user-badge" onclick="doLogout()">
      <div class="user-avatar" id="userAvatar">?</div>
      <span id="userNameDisplay">—</span>
      <span style="color:var(--faint);font-size:10px;">sair</span>
    </div>
  </div>
</div>

<div class="page">

  <!-- DASHBOARD METRICS -->
  <div class="section-label" style="margin-bottom:12px;">Dashboard</div>
  <div class="metrics" id="metricsRow">
    <div class="metric-card m-total" data-mfilter="todos"><div class="metric-label">Total de obras</div><div class="metric-value" id="m-total">—</div><div class="metric-sub">clique para ver todas</div></div>
    <div class="metric-card m-andamento" data-mfilter="Em andamento"><div class="metric-label">Em andamento</div><div class="metric-value" id="m-andamento">—</div><div class="metric-sub">execução em curso</div></div>
    <div class="metric-card m-programado" data-mfilter="Programado"><div class="metric-label">Programado</div><div class="metric-value" id="m-programado">—</div><div class="metric-sub">aguardando início</div></div>
    <div class="metric-card m-concluido" data-mfilter="Concluído"><div class="metric-label">Concluído</div><div class="metric-value" id="m-concluido">—</div><div class="metric-sub">entregues em 2026</div></div>
    <div class="metric-card m-backlog" data-mfilter="Backlog"><div class="metric-label">Backlog</div><div class="metric-value" id="m-backlog">—</div><div class="metric-sub">sem data prevista</div></div>
    <div class="metric-card m-paralizado" data-mfilter="Paralizado"><div class="metric-label">Paralizado</div><div class="metric-value" id="m-paralizado">—</div><div class="metric-sub">aguardando retomada</div></div>
  </div>

  <!-- CHARTS GRID -->
  <div class="dashboard-grid">
    <!-- Distribuição por Localização -->
    <div class="chart-card">
      <div class="chart-title">Distribuição por Localização</div>
      <div class="chart-subtitle">Total de obras por unidade</div>
      <div class="chart-canvas-wrap" style="height:180px;">
        <canvas id="chartLocal"></canvas>
        <div class="chart-center-label">
          <div class="chart-center-num" id="chartLocalTotal">—</div>
          <div class="chart-center-txt">obras</div>
        </div>
      </div>
      <div class="chart-legend" id="legendLocal"></div>
    </div>

    <!-- Humanização vs Longo Prazo -->
    <div class="chart-card">
      <div class="chart-title">Humanização vs Longo Prazo</div>
      <div class="chart-subtitle">Distribuição por tipo de demanda</div>
      <div class="chart-canvas-wrap" style="height:180px;">
        <canvas id="chartDemanda"></canvas>
        <div class="chart-center-label">
          <div class="chart-center-num" id="chartDemandaTotal">—</div>
          <div class="chart-center-txt">total</div>
        </div>
      </div>
      <div class="chart-legend" id="legendDemanda"></div>
    </div>

    <!-- Distribuição por Tipo -->
    <div class="chart-card">
      <div class="chart-title">Distribuição por Tipo</div>
      <div class="chart-subtitle">Categorias de projeto</div>
      <div style="position:relative;height:200px;">
        <canvas id="chartTipo"></canvas>
      </div>
    </div>

    <!-- Demandas por Projetista -->
    <div class="chart-card">
      <div class="chart-title">Demandas por Projetista</div>
      <div class="chart-subtitle">Volume de obras por responsável</div>
      <div style="position:relative;height:200px;">
        <canvas id="chartProjetista"></canvas>
      </div>
    </div>
  </div>

  <!-- TABLE -->
  <div class="table-section">
    <div class="table-header">
      <div>
        <div class="table-header-title">Demandas detalhadas</div>
        <div class="table-count" id="tableCount">—</div>
      </div>
      <div class="search-wrap">
        <span class="search-icon">🔍</span>
        <input type="text" class="search-input" id="searchInput" placeholder="Buscar obra, solicitante…">
      </div>
    </div>
    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th style="width:28px;"></th>
            <th data-sort="obra">Obra / Área</th>
            <th data-sort="local">Localização</th>
            <th data-sort="tipo">Tipo</th>
            <th>Status</th>
            <th data-sort="projetista">Projetista</th>
            <th data-sort="previsao">Previsão</th>
            <th>Disciplinas</th>
          </tr>
        </thead>
        <tbody id="tableBody"></tbody>
      </table>
      <div class="no-results" id="noResults" style="display:none;">Nenhuma demanda encontrada para os filtros selecionados.</div>
    </div>
  </div>

</div>

<!-- NEW DEMAND MODAL -->
<div class="modal-overlay" id="newModal">
  <div class="modal">
    <div class="modal-header">
      <div class="modal-title" id="modalTitle">Nova demanda</div>
      <button class="modal-close" onclick="closeModal()">✕</button>
    </div>
    <div class="modal-body">
      <div class="modal-grid">
        <div class="form-field" style="grid-column:1/-1">
          <label>Nome da obra / demanda *</label>
          <input type="text" id="f-obra" placeholder="Ex: Reforma da sala de controle">
        </div>
        <div class="form-field">
          <label>Nº RC / Pedido</label>
          <input type="text" id="f-rc" placeholder="Ex: RC-00123 ou PED-456">
        </div>
          <label>Localização *</label>
          <select id="f-local">
            <option value="">Selecione…</option>
            <option>Usina 1</option><option>Usina 2</option><option>Usina 3</option>
            <option>Mina Norte</option><option>Mina Sul</option><option>Barragem</option><option>Externo</option>
          </select>
        </div>
        <div class="form-field">
          <label>Tipo *</label>
          <select id="f-tipo">
            <option value="">Selecione…</option>
            <option>Humanização Completa</option><option>Mobiliario </option><option>Layout</option>
            <option>Plotagem</option><option>Planejados</option><option>Paisagismo</option>
          </select>
        </div>
        <div class="form-field">
          <label>Status *</label>
          <select id="f-status">
            <option>Em andamento</option><option>Programado</option><option>Previsto</option>
            <option>Planejado</option><option>Backlog</option><option>Paralizado</option><option>Concluído</option>
          </select>
        </div>
        <div class="form-field">
          <label>Demanda</label>
          <select id="f-demanda">
            <option value="">Selecione…</option>
            <option>Humanização</option><option>Longo Prazo</option><option>Momento 3</option>
          </select>
        </div>
        <div class="form-field">
          <label>Projetista</label>
          <input type="text" id="f-projetista" placeholder="Nome do projetista">
        </div>
        <div class="form-field">
          <label>Fiscal</label>
          <input type="text" id="f-fiscal" placeholder="Nome do fiscal">
        </div>
        <div class="form-field">
          <label>Solicitante</label>
          <input type="text" id="f-solicitante" placeholder="Nome do solicitante">
        </div>
        <div class="form-field">
          <label>Área</label>
          <input type="text" id="f-area" placeholder="Ex: GGA">
        </div>
        <div class="form-field">
          <label>Previsão de entrega</label>
          <input type="month" id="f-previsao">
        </div>
        <div class="form-field">
          <label>Local de débito</label>
          <input type="text" id="f-debito" placeholder="Ex: CC-1234">
        </div>
        <div class="form-field">
          <label>Conta razão</label>
          <input type="text" id="f-conta" placeholder="Ex: 5.1.01.001">
        </div>
        <div class="form-field" style="grid-column:1/-1">
          <label>Observações iniciais</label>
          <textarea id="f-obs" placeholder="Informações adicionais, contexto, restrições…"></textarea>
        </div>
        <div class="section-divider-modal">Status das disciplinas</div>
        <div class="disc-grid" id="discGrid">
        </div>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn-secondary" onclick="closeModal()">Cancelar</button>
      <button class="btn-primary" onclick="saveNewDemand()">Salvar demanda</button>
    </div>
  </div>
</div>

<!-- MANAGE USERS MODAL (admin only) -->
<div class="modal-overlay" id="manageUsersModal">
  <div class="modal" style="width:520px;">
    <div class="modal-header">
      <div class="modal-title">👥 Gerenciar usuários</div>
      <button class="modal-close" onclick="closeManageUsersModal()">✕</button>
    </div>
    <div class="modal-body">
      <div id="usersList" style="margin-bottom:20px;"></div>
      <div style="border-top:1px solid var(--border);padding-top:18px;">
        <div style="font-size:12px;font-weight:600;color:var(--accent-light);margin-bottom:14px;text-transform:uppercase;letter-spacing:0.06em;">Criar novo usuário</div>
        <div class="modal-grid">
          <div class="form-field">
            <label>Login *</label>
            <input type="text" id="nu-login" placeholder="ex: joao.silva">
          </div>
          <div class="form-field">
            <label>Nome completo *</label>
            <input type="text" id="nu-name" placeholder="ex: João Silva">
          </div>
          <div class="form-field">
            <label>Senha inicial *</label>
            <input type="password" id="nu-pass" placeholder="Mínimo 6 caracteres">
          </div>
          <div class="form-field">
            <label>Perfil</label>
            <select id="nu-admin">
              <option value="false">Usuário</option>
              <option value="true">Administrador</option>
            </select>
          </div>
        </div>
        <div id="nuError" style="font-size:12px;color:var(--c-paralizado);display:none;margin-top:8px;"></div>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn-secondary" onclick="closeManageUsersModal()">Fechar</button>
      <button class="btn-primary" onclick="createNewUser()">Criar usuário</button>
    </div>
  </div>
</div>

<!-- CHANGE PASSWORD MODAL -->
<div class="modal-overlay" id="changePwdModal">
  <div class="modal" style="width:420px;">
    <div class="modal-header">
      <div class="modal-title" id="changePwdTitle">Alterar senha</div>
      <button class="modal-close" onclick="closeChangePwdModal()">✕</button>
    </div>
    <div class="modal-body">
      <p id="changePwdInfo" style="font-size:12px;color:var(--c-previsto);margin-bottom:16px;"></p>
      <div id="oldPassGroup" class="form-field" style="margin-bottom:14px;">
        <label>Senha atual</label>
        <input type="password" id="oldPass" placeholder="Senha atual">
      </div>
      <div class="form-field" style="margin-bottom:14px;">
        <label>Nova senha</label>
        <input type="password" id="newPass" placeholder="Mínimo 6 caracteres">
      </div>
      <div class="form-field" style="margin-bottom:14px;">
        <label>Confirmar nova senha</label>
        <input type="password" id="newPass2" placeholder="Repita a nova senha">
      </div>
      <div id="changePwdError" style="font-size:12px;color:var(--c-paralizado);display:none;margin-top:4px;"></div>
    </div>
    <div class="modal-footer">
      <button class="btn-secondary" onclick="closeChangePwdModal()">Cancelar</button>
      <button class="btn-primary" onclick="saveNewPassword()">Salvar senha</button>
    </div>
  </div>
</div>

<!-- AUDIT LOG MODAL -->
<div class="modal-overlay" id="auditModal">
  <div class="modal" style="width:700px;">
    <div class="modal-header">
      <div class="modal-title">📋 Histórico de modificações</div>
      <button class="modal-close" onclick="closeAuditModal()">✕</button>
    </div>
    <div class="modal-body">
      <p style="font-size:12px;color:var(--muted);margin-bottom:16px;">Registro completo de alterações — visível apenas para leticia.ulhoa.</p>
      <div id="auditList" class="obs-list" style="max-height:60vh;overflow-y:auto;"></div>
    </div>
    <div class="modal-footer">
      <button class="btn-secondary" onclick="closeAuditModal()">Fechar</button>
    </div>
  </div>
</div>

<script>
// ══════════════════════════════════════════════
//  STORAGE LAYER — Firebase Realtime Database
// ══════════════════════════════════════════════
const FB_USERS = 'farol/users';
const FB_DATA  = 'farol/data';
const FB_AUDIT = 'farol/audit';

// Default users
const DEFAULT_USERS = {
  'leticia.ulhoa':       { name: 'Leticia Ulhoa',       pass: 'samarco', isAdmin: true },
  'mariana.mares':       { name: 'Mariana Mares',        pass: 'samarco', isAdmin: false },
  'cinthia.reis':        { name: 'Cinthia Reis',         pass: 'samarco', isAdmin: false },
  'sheila.reis':         { name: 'Sheila Reis',          pass: 'samarco', isAdmin: false },
  'augusto.ribeiro':     { name: 'Augusto Ribeiro',      pass: 'samarco', isAdmin: false },
  'fernanda.bernardes':  { name: 'Fernanda Bernardes',   pass: 'samarco', isAdmin: false },
  'bruno.fialho':        { name: 'Bruno Fialho',         pass: 'samarco', isAdmin: false },
  'sergio.pires':        { name: 'Sergio Pires',         pass: 'samarco', isAdmin: false },
};

const DEFAULT_DATA = [{"obra":"Sala de apoio Sotreq","local":"Usina 2","tipo":"Mobiliario ","solicitante":"Fernando H3M","area":"Sotreq","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-07-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Em andamento","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Área de vivência da Mina Sul","local":"Mina Sul","tipo":"Humanização Completa","solicitante":"Airton","area":"GMN","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Em andamento","fiscal":"Artur Ribeiro","previsao":"2026-05-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Em andamento","Mobiliário":"Em andamento","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Em andamento","Elétrica":"Concluído","Decoração":"Em andamento","Plotagem":"Em andamento"},"obs":[],"debito":"","conta":""},{"obra":"Reforma da Unitrol","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Nivaldo","area":"GGA","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Em andamento","fiscal":"Júlio César","previsao":"2026-05-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Previsto","Mobiliário":"Planejado","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Planejado"},"obs":[],"debito":"","conta":""},{"obra":"Laboratório e Escritório - Eixo 01","local":"Barragem","tipo":"Humanização Completa","solicitante":"Andiara","area":"GEA","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Em andamento","fiscal":"Júlio César","previsao":"2026-05-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Em andamento","Mobiliário":"Em andamento","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Em andamento"},"obs":[],"debito":"","conta":""},{"obra":"Container da Elétrica Usina 2","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Tatiana","area":"GMG","demanda":"Humanização","projetista":"","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-06-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Sala de Treinamentos interna prédio Usina 2","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Tatiana","area":"GMG","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-05-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Laboratório elétrico Usina 2","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Tatiana","area":"GMG","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-05-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Copa Container Ferramentaria","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Saiury","area":"GMG","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-05-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Concluído","Mobiliário":"Planejado","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Planejado","Elétrica":"Não se aplica","Decoração":"Planejado","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Academia Vila Samarco","local":"Externo","tipo":"Humanização Completa","solicitante":"Hilcker","area":"GGA","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-06-01","entrega":"","disciplinas":{"Layout":"Concluído","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Layout - Planejamento de Mina predio do COI (US 02)","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Thais","area":"GMN","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Roberto Amaral","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Planejado","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Vestiáro feminino da Manserv","local":"Usina 1","tipo":"Mobiliario ","solicitante":"Renata","area":"GIG","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Programado","fiscal":"Júlio César","previsao":"2026-06-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Laboratório Usina 2","local":"Usina 2","tipo":"Layout","solicitante":"Jussara","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-06-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Concluído","Civil":"Não se aplica","Persiana":"Planejado","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Sala do Social/RH - Escritório Central","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Gabriela","area":"GSS","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-07-01","entrega":"","disciplinas":{"Layout":"Concluído","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Não se aplica","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Hall de Suprimentos","local":"Usina 1","tipo":"Mobiliario ","solicitante":"Betânia","area":"GLO","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-06-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"GGA - Rhanya/Anathele","local":"Usina 1","tipo":"Layout","solicitante":"Rhanya / Anathele","area":"GGA","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-07-01","entrega":"","disciplinas":{"Layout":"Em andamento","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Não se aplica","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Restaurante Momento III","local":"Usina 1","tipo":"Plotagem","solicitante":"Natália Silva","area":"M3","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-06-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Restaurante de Camargos","local":"Externo","tipo":"Plotagem","solicitante":"Renata","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-05-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Escritório Central - Sala Stefanini e Depósito TI","local":"Usina 1","tipo":"Layout","solicitante":"Gabriela Alves","area":"GTI","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Concluído","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Não se aplica","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência - Vestiários da Usina 2","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Humanização Pró-ativa","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Em andamento","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Layout no Prédio ADM Usina 2","local":"Usina 2","tipo":"Layout","solicitante":"Adalto","area":"GBC","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Em andamento","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Previsto","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência Usina 2 - Restaurante (aguardando verba)","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Sérgio","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência Refeitório Momento 3 (aguardando verba)","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Humanização Pró-ativa","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência Momento 3 (aguardando verba)","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Humanização Pró-ativa","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Sala de controle da Filtragem","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Sérgio","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-07-01","entrega":"","disciplinas":{"Layout":"Concluído","Planejados":"Em andamento","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Não se aplica","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Área de vivência Vestiários Usina 3","local":"Usina 3","tipo":"Humanização Completa","solicitante":"Bruno Fialho","area":"US3","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"","entrega":"","disciplinas":{"Layout":"Concluído","Planejados":"Em andamento","Mobiliário":"Previsto","Pintura":"Concluído","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Planejado"},"obs":[],"debito":"","conta":""},{"obra":"Copa Montagem de Correia Mina Norte - Container","local":"Mina Norte","tipo":"Planejados","solicitante":"Suellen","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Reforma Mecânica da Mina (Sala de trabalho e Copa) - Alvenaria","local":"Mina Norte","tipo":"Humanização Completa","solicitante":"Andreza","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Reforma da Sala do Luiz - Mina Norte","local":"Mina Norte","tipo":"Humanização Completa","solicitante":"Andreza","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Reforma da Elétrica da Mina Norte","local":"Mina Norte","tipo":"Humanização Completa","solicitante":"Andreza","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Reforma da Sala da Supervisora - Mina Norte","local":"Mina Norte","tipo":"Humanização Completa","solicitante":"Andreza","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Vestiário - Mina Norte","local":"Mina Norte","tipo":"Mobiliario ","solicitante":"Andreza","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Sala da Valquíria GGA","local":"Usina 1","tipo":"Layout","solicitante":"Valquíria","area":"GGA","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Layout Suprimentos_Jefferson","local":"Usina 1","tipo":"Plotagem","solicitante":"Jeferson","area":"GLO","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Júlio César","previsao":"2026-07-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Humanização Sala Progen GGA - P4P","local":"Usina 3","tipo":"Humanização Completa","solicitante":"Walyson","area":"GGA","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência Usina 1 - Container Lanchonete (aguardando verba)","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Humanização Pró-ativa","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-09-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência Usina 1 - Restaurante (aguardando verba)","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Humanização Pró-ativa","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-09-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência Usina 3 (aguardando verba)","local":"Usina 3","tipo":"Humanização Completa","solicitante":"Humanização Pró-ativa","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-09-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Segurança do Trabalho","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Jussara","area":"GSG","demanda":"Humanização","projetista":"Leticia","status":"Em andamento","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Em andamento","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Escritório Central - Reforma Banheiros Ala das Gerências (DML)","local":"Usina 1","tipo":"Mobiliario ","solicitante":"Lea","area":"GG","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Júlio César","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Layout CMI - Erico","local":"Usina 1","tipo":"Layout","solicitante":"Erico","area":"GGO","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Júlio César","previsao":"2026-09-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Não se aplica","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Plotagem Prédio dos Bombeiros","local":"Usina 1","tipo":"Plotagem","solicitante":"Jéssica","area":"GST","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-06-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Planejado"},"obs":[],"debito":"","conta":""},{"obra":"Reforma do vestiario masculino da manutenção da Usina 02","local":"Usina 2","tipo":"Mobiliario ","solicitante":"","area":"","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-08-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Reforma Sala do CECOM","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Rômulo Mendes/ David","area":"CECOM","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-09-01","entrega":"","disciplinas":{"Layout":"Concluído","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Previsto","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Laboratório Planta Piloto - Iron Core","local":"Usina 3","tipo":"Humanização Completa","solicitante":"Arthur Klein","area":"GEA","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Programado","fiscal":"Artur Ribeiro","previsao":"2026-09-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Paisagismo Entrada Samarco","local":"Usina 1","tipo":"Paisagismo","solicitante":"Sérgio","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-09-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Área de Vivência Externa Mina Sul","local":"Mina Sul","tipo":"Humanização Completa","solicitante":"Humanização Pró-ativa","area":"GIG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-10-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Humanização Prédio Bandeirantes","local":"Usina 3","tipo":"Humanização Completa","solicitante":"Flávia","area":"GMG","demanda":"Humanização","projetista":"Leticia","status":"Programado","fiscal":"Mariana Mares","previsao":"2026-10-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Previsto","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Vestiário masculino para área de Vivência da Oficina Atlas - Mina Norte","local":"Mina Norte","tipo":"Mobiliario ","solicitante":"Airton","area":"GMN","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Programado","fiscal":"Artur Ribeiro","previsao":"2026-10-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Reforma da ERG","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Thais","area":"GMN","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Programado","fiscal":"Júlio César","previsao":"2026-10-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Área de vivencia da Manutenção - Mina Norte","local":"Mina Norte","tipo":"Humanização Completa","solicitante":"Suellen","area":"GMG","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Programado","fiscal":"Artur Ribeiro","previsao":"2026-11-01","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Layout Beneficiamento (US 03)","local":"Usina 3","tipo":"Layout","solicitante":"Adalto","area":"GBC","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Programado","fiscal":"Artur Ribeiro","previsao":"2026-11-01","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""},{"obra":"Sala de apoio ao aleitamento US 03","local":"Usina 3","tipo":"Humanização Completa","solicitante":"Bruno Fialho","area":"GIG","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Concluído","fiscal":"Artur Ribeiro","previsao":"2026-05-01","entrega":"2026-05-01","disciplinas":{"Layout":"Concluído","Planejados":"Concluído","Mobiliário":"Concluído","Pintura":"Concluído","Civil":"Concluído","Persiana":"Concluído","Elétrica":"Concluído","Decoração":"Concluído","Plotagem":"Concluído"},"obs":[],"debito":"","conta":""},{"obra":"Reforma dos banheiros coletivos do escritório central","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Lea","area":"GG","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Concluído","fiscal":"Júlio César","previsao":"2026-03-01","entrega":"2026-03-01","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Concluído","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Reforma do Meio Ambiente","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Tamires","area":"GAG","demanda":"Longo Prazo","projetista":"Augusto Ribeiro","status":"Concluído","fiscal":"Júlio César","previsao":"2026-01-01","entrega":"2026-01-01","disciplinas":{"Layout":"Não se aplica","Planejados":"Concluído","Mobiliário":"Concluído","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Concluído","Elétrica":"Não se aplica","Decoração":"Concluído","Plotagem":"Concluído"},"obs":[],"debito":"","conta":""},{"obra":"Reforma da Segurança do Trabalho","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Jussara","area":"GSG","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Concluído","fiscal":"Júlio César","previsao":"2026-04-01","entrega":"2026-04-01","disciplinas":{"Layout":"Não se aplica","Planejados":"Concluído","Mobiliário":"Concluído","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Concluído","Elétrica":"Não se aplica","Decoração":"Concluído","Plotagem":"Concluído"},"obs":[],"debito":"","conta":""},{"obra":"Sala de apoio ao aleitamento Usina 2","local":"Usina 2","tipo":"Humanização Completa","solicitante":"Bruno Fialho","area":"DEI","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Paralizado","fiscal":"Mariana Mares","previsao":"2026-04-01","entrega":"2026-04-01","disciplinas":{"Layout":"Concluído","Planejados":"Concluído","Mobiliário":"Concluído","Pintura":"Concluído","Civil":"Concluído","Persiana":"Concluído","Elétrica":"Concluído","Decoração":"Concluído","Plotagem":"Concluído"},"obs":[],"debito":"","conta":""},{"obra":"Copa da Grabber","local":"Usina 1","tipo":"Planejados","solicitante":"Mariana","area":"GIG","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Concluído","fiscal":"Mariana Mares","previsao":"2026-04-01","entrega":"2026-04-01","disciplinas":{"Layout":"Não se aplica","Planejados":"Concluído","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Copa do Hub de Mariana","local":"Externo","tipo":"Planejados","solicitante":"Mariana","area":"GIG","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Concluído","fiscal":"Mariana Mares","previsao":"2026-04-01","entrega":"2026-04-01","disciplinas":{"Layout":"Não se aplica","Planejados":"Concluído","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Concluído","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Não se aplica","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Sala da gerência da GGA","local":"Usina 1","tipo":"Humanização Completa","solicitante":"Marcelo","area":"GGA","demanda":"Humanização","projetista":"Augusto Ribeiro","status":"Concluído","fiscal":"Mariana Mares","previsao":"2026-03-01","entrega":"2026-03-01","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Concluído","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Concluído","Plotagem":"Concluído"},"obs":[],"debito":"","conta":""},{"obra":"Vestiário masculino Rede Básica","local":"Usina 1","tipo":"Mobiliario ","solicitante":"Rodrigo Mira","area":"GIG","demanda":"Longo Prazo","projetista":"Fernanda Isabella","status":"Backlog","fiscal":"Júlio César","previsao":"","entrega":"","disciplinas":{"Layout":"Não se aplica","Planejados":"Não se aplica","Mobiliário":"Não se aplica","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Não se aplica","Elétrica":"Não se aplica","Decoração":"Previsto","Plotagem":"Não se aplica"},"obs":[],"debito":"","conta":""},{"obra":"Humanização Prédio P4P","local":"Usina 3","tipo":"Humanização Completa","solicitante":"Adriano Ferrari","area":"GMG","demanda":"Momento 3","projetista":"Jeferson Braga","status":"Backlog","fiscal":"Mariana Mares","previsao":"","entrega":"","disciplinas":{"Layout":"Previsto","Planejados":"Previsto","Mobiliário":"Previsto","Pintura":"Não se aplica","Civil":"Não se aplica","Persiana":"Previsto","Elétrica":"Previsto","Decoração":"Previsto","Plotagem":"Previsto"},"obs":[],"debito":"","conta":""}];

// ══════════════════════════════════════════════
//  GLOBAL STATE
// ══════════════════════════════════════════════
let USERS = {};
let DATA = [];
let AUDIT_LOG = [];
let currentUser = null;
let isVisitor = false;
let activeFilters = { metric:'todos' };
let searchTerm = '';
let sortCol = null; let sortDir = 'asc';
let expandedRows = new Set();

// ── FIREBASE STORAGE HELPERS ──
async function saveToStorage() {
  try {
    await window._fbSet(FB_USERS, USERS);
    await window._fbSet(FB_DATA,  DATA);
    await window._fbSet(FB_AUDIT, AUDIT_LOG);
    showToast();
  } catch(e) {
    console.error('Erro ao salvar no Firebase:', e);
  }
}

function showToast() {
  const t = document.getElementById('saveToast');
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2000);
}

async function loadFromStorage() {
  try {
    const users = await window._fbGet(FB_USERS);
    const data  = await window._fbGet(FB_DATA);
    const audit = await window._fbGet(FB_AUDIT);

    USERS     = users || JSON.parse(JSON.stringify(DEFAULT_USERS));
    DATA      = data  ? Object.values(data) : JSON.parse(JSON.stringify(DEFAULT_DATA));
    AUDIT_LOG = audit ? Object.values(audit) : [];

    // Garante que o array DATA seja sempre array (Firebase armazena como objeto indexado)
    if (!Array.isArray(DATA)) DATA = Object.values(DATA);
    if (!Array.isArray(AUDIT_LOG)) AUDIT_LOG = Object.values(AUDIT_LOG);

    // Se é a primeira vez (Firebase vazio), salva os dados padrão
    if (!users) await window._fbSet(FB_USERS, USERS);
    if (!data)  await window._fbSet(FB_DATA,  DATA);

  } catch(e) {
    console.error('Erro ao carregar do Firebase:', e);
    USERS     = JSON.parse(JSON.stringify(DEFAULT_USERS));
    DATA      = JSON.parse(JSON.stringify(DEFAULT_DATA));
    AUDIT_LOG = [];
  }

  // Garante que leticia.ulhoa é sempre admin
  if (USERS['leticia.ulhoa']) USERS['leticia.ulhoa'].isAdmin = true;
}

// ── LISTENER TEMPO REAL — sincroniza automaticamente com outros usuários ──
function startRealtimeSync() {
  window._fbListen(FB_DATA, (val) => {
    if (!val || !currentUser) return;
    const newData = Array.isArray(val) ? val : Object.values(val);
    // Só atualiza se houver mudança real (evita loop ao salvar)
    if (JSON.stringify(newData) !== JSON.stringify(DATA)) {
      DATA = newData;
      updateMetrics(); buildCharts(); renderTable();
    }
  });
  window._fbListen(FB_USERS, (val) => {
    if (!val || !currentUser) return;
    USERS = val;
  });
}

// ══════════════════════════════════════════════
//  AUTH
// ══════════════════════════════════════════════
function logAudit(action, details) {
  AUDIT_LOG.push({ ts: ts(), user: currentUser ? currentUser.name : 'Visitante', action, details });
  saveToStorage();
}

function doLogin() {
  const u = document.getElementById('loginUser').value.trim().toLowerCase();
  const p = document.getElementById('loginPass').value;
  if (USERS[u] && USERS[u].pass === p) {
    currentUser = { key: u, name: USERS[u].name, isAdmin: USERS[u].isAdmin };
    isVisitor = false;
    document.getElementById('loginOverlay').style.display = 'none';
    document.getElementById('userNameDisplay').textContent = currentUser.name.split(' ')[0];
    document.getElementById('userAvatar').textContent = currentUser.name[0].toUpperCase();
    document.getElementById('changePwdBtn').style.display = 'inline-flex';
    document.getElementById('addDemandBtn').style.display = 'inline-flex';
    if (currentUser.isAdmin) {
      document.getElementById('auditBtn').style.display = 'inline-flex';
      document.getElementById('manageUsersBtn').style.display = 'inline-flex';
    }
    initApp();
    startRealtimeSync();
    if (USERS[u].pass === 'samarco') showChangePasswordModal(true);
  } else {
    document.getElementById('loginError').style.display = 'block';
  }
}

function doLoginVisitor() {
  currentUser = { key:'visitante', name:'Visitante', isAdmin:false };
  isVisitor = true;
  document.getElementById('loginOverlay').style.display = 'none';
  document.getElementById('userNameDisplay').textContent = 'Visitante';
  document.getElementById('userAvatar').textContent = 'V';
  document.getElementById('userAvatar').style.background = '#6b7280';
  document.getElementById('visitorBanner').style.display = 'flex';
  initApp();
}

function doLogout() {
  if (!confirm('Deseja sair?')) return;
  currentUser = null; isVisitor = false;
  document.getElementById('loginOverlay').style.display = 'flex';
  document.getElementById('loginUser').value = '';
  document.getElementById('loginPass').value = '';
  document.getElementById('loginError').style.display = 'none';
  document.getElementById('visitorBanner').style.display = 'none';
  document.getElementById('changePwdBtn').style.display = 'none';
  document.getElementById('addDemandBtn').style.display = 'none';
  document.getElementById('auditBtn').style.display = 'none';
  document.getElementById('manageUsersBtn').style.display = 'none';
}

document.getElementById('loginPass').addEventListener('keydown', e => { if(e.key==='Enter') doLogin(); });
document.getElementById('loginUser').addEventListener('keydown', e => { if(e.key==='Enter') doLogin(); });

// ── CHANGE PASSWORD ──
function showChangePasswordModal(isFirst) {
  document.getElementById('changePwdModal').classList.add('open');
  document.getElementById('changePwdTitle').textContent = isFirst ? 'Primeiro acesso — defina sua senha' : 'Alterar senha';
  document.getElementById('changePwdInfo').textContent = isFirst ? 'Por segurança, altere a senha padrão antes de continuar.' : '';
  document.getElementById('changePwdError').style.display = 'none';
  document.getElementById('oldPass').value = '';
  document.getElementById('newPass').value = '';
  document.getElementById('newPass2').value = '';
  document.getElementById('oldPassGroup').style.display = isFirst ? 'none' : 'block';
}
function closeChangePwdModal() { document.getElementById('changePwdModal').classList.remove('open'); }
function saveNewPassword() {
  const newP = document.getElementById('newPass').value;
  const newP2 = document.getElementById('newPass2').value;
  const errEl = document.getElementById('changePwdError');
  if (newP.length < 6) { errEl.textContent='A senha deve ter pelo menos 6 caracteres.'; errEl.style.display='block'; return; }
  if (newP !== newP2) { errEl.textContent='As senhas não coincidem.'; errEl.style.display='block'; return; }
  const oldPEl = document.getElementById('oldPassGroup');
  if (oldPEl.style.display !== 'none') {
    if (USERS[currentUser.key].pass !== document.getElementById('oldPass').value) {
      errEl.textContent='Senha atual incorreta.'; errEl.style.display='block'; return;
    }
  }
  USERS[currentUser.key].pass = newP;
  logAudit('Alteração de senha', `Usuário ${currentUser.name} alterou sua senha.`);
  closeChangePwdModal();
  alert('Senha alterada com sucesso!');
}

// ── MANAGE USERS (admin only) ──
function openManageUsersModal() {
  renderUsersList();
  document.getElementById('manageUsersModal').classList.add('open');
}
function closeManageUsersModal() { document.getElementById('manageUsersModal').classList.remove('open'); }
function renderUsersList() {
  const list = document.getElementById('usersList');
  list.innerHTML = Object.entries(USERS).map(([key, u]) => `
    <div style="display:flex;align-items:center;justify-content:space-between;padding:10px 12px;background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-sm);margin-bottom:6px;">
      <div>
        <div style="font-size:13px;font-weight:500;">${u.name}</div>
        <div style="font-size:11px;color:var(--muted);">${key}${u.isAdmin?' · <span style="color:var(--accent-light)">Admin</span>':''}</div>
      </div>
      ${key !== 'leticia.ulhoa' ? `<button onclick="removeUser('${key}')" style="background:rgba(239,68,68,0.1);border:1px solid rgba(239,68,68,0.2);color:#ef4444;font-size:11px;padding:4px 10px;border-radius:var(--radius-sm);cursor:pointer;font-family:'Sora',sans-serif;">Remover</button>` : '<span style="font-size:10px;color:var(--faint);">proprietário</span>'}
    </div>
  `).join('');
}
function removeUser(key) {
  if (!confirm(`Remover o usuário ${USERS[key]?.name}?`)) return;
  delete USERS[key];
  logAudit('Usuário removido', `Login "${key}" removido por ${currentUser.name}.`);
  renderUsersList();
}
function createNewUser() {
  const login = document.getElementById('nu-login').value.trim().toLowerCase();
  const name  = document.getElementById('nu-name').value.trim();
  const pass  = document.getElementById('nu-pass').value;
  const admin = document.getElementById('nu-admin').value === 'true';
  const err   = document.getElementById('nuError');
  if (!login || !name || pass.length < 6) {
    err.textContent = 'Preencha todos os campos. Senha mínimo 6 caracteres.';
    err.style.display = 'block'; return;
  }
  if (USERS[login]) {
    err.textContent = 'Este login já existe.';
    err.style.display = 'block'; return;
  }
  USERS[login] = { name, pass, isAdmin: admin };
  logAudit('Usuário criado', `Login "${login}" (${name}) criado por ${currentUser.name}.`);
  err.style.display = 'none';
  document.getElementById('nu-login').value = '';
  document.getElementById('nu-name').value = '';
  document.getElementById('nu-pass').value = '';
  document.getElementById('nu-admin').selectedIndex = 0;
  renderUsersList();
  alert(`Usuário ${name} criado com sucesso!`);
}

// ── AUDIT LOG ──
function openAuditModal() {
  const list = document.getElementById('auditList');
  if (AUDIT_LOG.length === 0) {
    list.innerHTML = '<div class="obs-empty">Nenhuma modificação registrada ainda.</div>';
  } else {
    list.innerHTML = [...AUDIT_LOG].reverse().map(e =>
      `<div class="obs-item"><div class="obs-meta"><span class="obs-author">${e.user}</span><span>${e.ts}</span><span class="audit-tag">${e.action}</span></div><div class="obs-text">${e.details}</div></div>`
    ).join('');
  }
  document.getElementById('auditModal').classList.add('open');
}
function closeAuditModal() { document.getElementById('auditModal').classList.remove('open'); }

// ══════════════════════════════════════════════
//  HELPERS
// ══════════════════════════════════════════════
const today = new Date('2026-05-13');

function statusClass(s) {
  const m = {'Em andamento':'andamento','Programado':'programado','Concluído':'concluido','Backlog':'backlog','Paralizado':'paralizado','Previsto':'previsto','Planejado':'planejado'};
  return 'badge-' + (m[s]||'backlog');
}
function tipoClass(t) {
  if (!t) return '';
  t = t.trim();
  if (t.includes('Humanização')||t.includes('Completa')) return 'tipo-hum';
  if (t.includes('Mobili')) return 'tipo-mob';
  if (t.includes('Layout')) return 'tipo-lay';
  if (t.includes('Plotagem')) return 'tipo-plo';
  if (t.includes('Planejados')) return 'tipo-pla';
  if (t.includes('Paisagismo')) return 'tipo-pai';
  return '';
}
function formatDate(d) {
  if (!d) return '—';
  const dt = new Date(d);
  const months = ['jan','fev','mar','abr','mai','jun','jul','ago','set','out','nov','dez'];
  return `${months[dt.getMonth()]}/${dt.getFullYear()}`;
}
function dateClass(d, status) {
  if (!d) return 'date-col';
  if (status==='Concluído') return 'date-col';
  const dt = new Date(d);
  const diff = (dt - today)/86400000;
  if (diff < 0) return 'date-col overdue';
  if (diff < 45) return 'date-col soon';
  return 'date-col';
}
function miniProgress(disc) {
  const vals = Object.values(disc);
  const segs = vals.map(v => {
    if (v==='Não se aplica') return 'na';
    if (v==='Concluído') return 'conc';
    if (v==='Em andamento') return 'and';
    if (v==='Planejado'||v==='Previsto') return 'prev';
    return 'plan';
  });
  return `<div class="mini-progress">${segs.map(s=>`<div class="mini-seg ${s}"></div>`).join('')}</div>`;
}
function ts() { return new Date().toLocaleString('pt-BR'); }

// ── FILTERS ──
function buildFilters() { /* filter tags removed */ }

function filteredData() {
  let d = [...DATA];
  if (activeFilters.metric!=='todos') d = d.filter(r=>r.status===activeFilters.metric);
  if (searchTerm) {
    const t = searchTerm.toLowerCase();
    d = d.filter(r => r.obra.toLowerCase().includes(t)||(r.solicitante||'').toLowerCase().includes(t)||(r.area||'').toLowerCase().includes(t)||r.local.toLowerCase().includes(t)||(r.projetista||'').toLowerCase().includes(t));
  }
  if (sortCol) {
    d.sort((a,b) => {
      const av=(a[sortCol]||'').toString().toLowerCase();
      const bv=(b[sortCol]||'').toString().toLowerCase();
      return sortDir==='asc' ? av.localeCompare(bv,'pt') : bv.localeCompare(av,'pt');
    });
  }
  return d;
}

// ── METRICS ──
function updateMetrics() {
  document.getElementById('m-total').textContent = DATA.length;
  document.getElementById('m-andamento').textContent = DATA.filter(r=>r.status==='Em andamento').length;
  document.getElementById('m-programado').textContent = DATA.filter(r=>r.status==='Programado').length;
  document.getElementById('m-concluido').textContent = DATA.filter(r=>r.status==='Concluído').length;
  document.getElementById('m-backlog').textContent = DATA.filter(r=>r.status==='Backlog').length;
  document.getElementById('m-paralizado').textContent = DATA.filter(r=>r.status==='Paralizado').length;
}

document.querySelectorAll('.metric-card[data-mfilter]').forEach(card => {
  card.addEventListener('click', () => {
    activeFilters.metric = card.getAttribute('data-mfilter');
    document.querySelectorAll('.metric-card').forEach(c=>c.classList.remove('active-filter'));
    card.classList.add('active-filter');
    expandedRows.clear(); renderTable();
  });
});

// ── CHARTS ──
let chartLocalInst, chartTipoInst, chartDemandaInst, chartProjetistaInst;

const NAVY_PALETTE = ['#1d4ed8','#3b82f6','#60a5fa','#93c5fd','#bfdbfe','#1e40af','#2563eb','#7c3aed'];
const STATUS_COLORS = { 'Em andamento':'#60a5fa','Programado':'#a78bfa','Concluído':'#22c55e','Backlog':'#6b7280','Paralizado':'#ef4444','Previsto':'#f59e0b','Planejado':'#06b6d4' };

function buildCharts() {
  if (chartLocalInst) chartLocalInst.destroy();
  if (chartTipoInst) chartTipoInst.destroy();
  if (chartDemandaInst) chartDemandaInst.destroy();
  if (chartProjetistaInst) chartProjetistaInst.destroy();

  Chart.defaults.color = '#8b93a8';
  Chart.defaults.font.family = "'Sora', sans-serif";

  // ── Distribuição por localização (donut) ──
  const locCounts = {};
  DATA.forEach(r => { locCounts[r.local]=(locCounts[r.local]||0)+1; });
  const locLabels = Object.keys(locCounts).sort((a,b)=>locCounts[b]-locCounts[a]);
  document.getElementById('chartLocalTotal').textContent = DATA.length;

  chartLocalInst = new Chart(document.getElementById('chartLocal'), {
    type: 'doughnut',
    data: { labels: locLabels, datasets: [{ data: locLabels.map(l=>locCounts[l]), backgroundColor: NAVY_PALETTE, borderWidth: 2, borderColor: '#151e30', hoverOffset: 6 }] },
    options: {
      responsive:true, maintainAspectRatio:false, cutout:'70%',
      plugins: { legend:{display:false}, tooltip:{ callbacks:{ label: c=>`  ${c.label}: ${c.raw} obras` }, backgroundColor:'#1a2540', padding:10, cornerRadius:8, titleFont:{size:12}, bodyFont:{size:12} } },
      animation: { animateScale: true, duration: 800 }
    }
  });
  const legLocal = document.getElementById('legendLocal');
  legLocal.innerHTML = '';
  locLabels.forEach((l,i) => {
    legLocal.innerHTML += `<div class="chart-legend-item"><div class="chart-legend-dot" style="background:${NAVY_PALETTE[i%NAVY_PALETTE.length]}"></div><span>${l} <strong style="color:var(--text)">${locCounts[l]}</strong></span></div>`;
  });

  // ── Humanização vs Longo Prazo (donut) ──
  const demandaCounts = {};
  DATA.forEach(r => { const d=r.demanda||'Outros'; demandaCounts[d]=(demandaCounts[d]||0)+1; });
  const demandaLabels = Object.keys(demandaCounts).sort((a,b)=>demandaCounts[b]-demandaCounts[a]);
  const demandaColors = ['#1d4ed8','#22c55e','#a78bfa','#f59e0b','#ef4444'];
  document.getElementById('chartDemandaTotal').textContent = DATA.length;

  chartDemandaInst = new Chart(document.getElementById('chartDemanda'), {
    type: 'doughnut',
    data: { labels: demandaLabels, datasets: [{ data: demandaLabels.map(l=>demandaCounts[l]), backgroundColor: demandaColors, borderWidth: 2, borderColor: '#151e30', hoverOffset: 6 }] },
    options: {
      responsive:true, maintainAspectRatio:false, cutout:'70%',
      plugins: { legend:{display:false}, tooltip:{ callbacks:{ label: c=>`  ${c.label}: ${c.raw}` }, backgroundColor:'#1a2540', padding:10, cornerRadius:8 } },
      animation: { animateScale: true, duration: 800 }
    }
  });
  const legDemanda = document.getElementById('legendDemanda');
  legDemanda.innerHTML = '';
  demandaLabels.forEach((l,i) => {
    const pct = Math.round(demandaCounts[l]/DATA.length*100);
    legDemanda.innerHTML += `<div class="chart-legend-item"><div class="chart-legend-dot" style="background:${demandaColors[i]}"></div><span>${l} <strong style="color:var(--text)">${demandaCounts[l]}</strong> <span style="color:var(--faint)">(${pct}%)</span></span></div>`;
  });

  // ── Distribuição por Tipo (horizontal bar) ──
  const tipoCounts = {};
  DATA.forEach(r => { const t=(r.tipo||'').trim(); tipoCounts[t]=(tipoCounts[t]||0)+1; });
  const tipoLabels = Object.keys(tipoCounts).sort((a,b)=>tipoCounts[b]-tipoCounts[a]);
  const tipoVals = tipoLabels.map(t=>tipoCounts[t]);
  const tipoMax = Math.max(...tipoVals);

  chartTipoInst = new Chart(document.getElementById('chartTipo'), {
    type: 'bar',
    data: {
      labels: tipoLabels,
      datasets: [{
        data: tipoVals,
        backgroundColor: tipoVals.map((v,i) => NAVY_PALETTE[i%NAVY_PALETTE.length]),
        borderRadius: 5, borderSkipped: false
      }]
    },
    options: {
      responsive:true, maintainAspectRatio:false, indexAxis:'y',
      plugins: { legend:{display:false}, tooltip:{ callbacks:{ label: c=>`  ${c.raw} obras` }, backgroundColor:'#1a2540', padding:10, cornerRadius:8 } },
      scales: {
        x: { grid:{color:'rgba(255,255,255,0.04)'}, ticks:{ color:'#8b93a8', font:{size:10} }, beginAtZero:true },
        y: { grid:{display:false}, ticks:{ color:'#8b93a8', font:{size:10}, callback: function(v, i){ const l=tipoLabels[i]||''; return l.length>16?l.substr(0,15)+'…':l; } } }
      },
      animation: { duration:800 }
    }
  });

  // ── Demandas por Projetista (horizontal bar) ──
  const projCounts = {};
  DATA.forEach(r => {
    const p = (r.projetista||'').trim() || 'Sem projetista';
    projCounts[p] = (projCounts[p]||0)+1;
  });
  const projLabels = Object.keys(projCounts).sort((a,b)=>projCounts[b]-projCounts[a]);
  const projVals = projLabels.map(p=>projCounts[p]);
  const projColors = ['#22c55e','#06b6d4','#a78bfa','#f59e0b','#3b82f6','#ef4444','#60a5fa','#1d4ed8'];

  chartProjetistaInst = new Chart(document.getElementById('chartProjetista'), {
    type: 'bar',
    data: {
      labels: projLabels,
      datasets: [{
        data: projVals,
        backgroundColor: projVals.map((v,i) => projColors[i%projColors.length]),
        borderRadius: 5, borderSkipped: false
      }]
    },
    options: {
      responsive:true, maintainAspectRatio:false, indexAxis:'y',
      plugins: { legend:{display:false}, tooltip:{ callbacks:{ label: c=>`  ${c.raw} demanda${c.raw!==1?'s':''}` }, backgroundColor:'#1a2540', padding:10, cornerRadius:8 } },
      scales: {
        x: { grid:{color:'rgba(255,255,255,0.04)'}, ticks:{ color:'#8b93a8', font:{size:10} }, beginAtZero:true },
        y: { grid:{display:false}, ticks:{ color:'#8b93a8', font:{size:10}, callback: function(v, i){ const l=projLabels[i]||''; return l.length>14?l.substr(0,13)+'…':l; } } }
      },
      animation: { duration:800 }
    }
  });
}

// ── DISCIPLINE COLOR ──
function applyDiscColor(el, status) {
  const colorMap = { 'Não se aplica':'','Previsto':'rgba(107,114,128,0.25)','Planejado':'rgba(107,114,128,0.25)','Em andamento':'rgba(59,130,246,0.20)','Concluído':'rgba(34,197,94,0.20)','Paralizado':'rgba(239,68,68,0.20)' };
  el.style.background = colorMap[status]||'';
  el.style.borderColor = colorMap[status]?colorMap[status].replace('0.20','0.5').replace('0.25','0.5'):'var(--border)';
}

// ── TABLE ──
const STATUS_OPTIONS = ['Em andamento','Programado','Previsto','Planejado','Backlog','Paralizado','Concluído'];

function renderTable() {
  const d = filteredData();
  const tbody = document.getElementById('tableBody');
  document.getElementById('tableCount').textContent = `${d.length} demanda${d.length!==1?'s':''} encontrada${d.length!==1?'s':''}`;

  if (d.length===0) { tbody.innerHTML=''; document.getElementById('noResults').style.display='block'; return; }
  document.getElementById('noResults').style.display='none';

  tbody.innerHTML = d.map((r, i) => {
    const isExp = expandedRows.has(r.obra);
    const canDelete = currentUser && currentUser.key === 'leticia.ulhoa';
    const canEditRC = currentUser && (currentUser.key === 'leticia.ulhoa' || currentUser.key === 'mariana.mares');

    // Status select inline
    const statusOpts = STATUS_OPTIONS.map(opt =>
      `<option value="${opt}"${opt===r.status?' selected':''}>${opt}</option>`
    ).join('');
    const statusEl = isVisitor
      ? `<span class="badge ${statusClass(r.status)}">${r.status}</span>`
      : `<div class="status-select-wrap badge ${statusClass(r.status)}" style="cursor:pointer;" title="Clique para alterar o status">
           <select class="status-select" data-obra="${r.obra.replace(/"/g,'&quot;')}" onchange="updateStatus(this)" onclick="event.stopPropagation()">
             ${statusOpts}
           </select>
           <span class="status-select-arrow">▾</span>
         </div>`;

    const obsHtml = r.obs && r.obs.length > 0
      ? r.obs.map(o=>`<div class="obs-item"><div class="obs-meta"><span class="obs-author">${o.author}</span><span>${o.ts}</span>${o.tag?`<span class="audit-tag">${o.tag}</span>`:''}</div><div class="obs-text">${o.text}</div></div>`).join('')
      : `<div class="obs-empty">Nenhuma observação registrada.</div>`;

    const discHtml = Object.entries(r.disciplinas).map(([k,v]) => {
      const colorMap={'Não se aplica':'','Previsto':'rgba(107,114,128,0.25)','Planejado':'rgba(107,114,128,0.25)','Em andamento':'rgba(59,130,246,0.20)','Concluído':'rgba(34,197,94,0.20)','Paralizado':'rgba(239,68,68,0.20)'};
      const borderMap={'Não se aplica':'var(--border)','Previsto':'rgba(107,114,128,0.5)','Planejado':'rgba(107,114,128,0.5)','Em andamento':'rgba(59,130,246,0.5)','Concluído':'rgba(34,197,94,0.5)','Paralizado':'rgba(239,68,68,0.5)'};
      return `<div class="disc-item" style="background:${colorMap[v]||'var(--surface)'};border-color:${borderMap[v]||'var(--border)'};">
        <div class="disc-name">${k}</div>
        <select class="disc-select" data-obra="${r.obra.replace(/"/g,'&quot;')}" data-disc="${k}" onchange="updateDisc(this)" ${isVisitor?'disabled':''}>
          ${['Não se aplica','Previsto','Planejado','Em andamento','Concluído','Paralizado'].map(opt=>`<option${opt===v?' selected':''}>${opt}</option>`).join('')}
        </select>
      </div>`;
    }).join('');

    const expRow = isExp ? `
      <tr class="expand-row">
        <td colspan="8">
          <div class="inline-info">
            <div class="info-item"><span>Solicitante:</span><span>${r.solicitante||'—'}</span></div>
            <div class="info-item"><span>Demanda:</span><span>${r.demanda||'—'}</span></div>
            <div class="info-item"><span>Fiscal:</span><span>${r.fiscal||'—'}</span></div>
            ${r.rc?`<div class="info-item"><span>RC / Pedido:</span><span style="color:var(--accent-light);font-family:'DM Mono',monospace">${r.rc}</span></div>`:''}
            ${r.entrega?`<div class="info-item"><span>Entrega:</span><span style="color:var(--c-concluido)">${formatDate(r.entrega)}</span></div>`:''}
          </div>
          <div class="finance-section">
            <div class="finance-field"><label>Nº RC / Pedido</label><input type="text" placeholder="Ex: RC-00123" value="${r.rc||''}" data-obra="${r.obra.replace(/"/g,'&quot;')}" data-field="rc" onblur="saveFinance(this)" ${canEditRC?'':'readonly style="opacity:0.5;cursor:not-allowed;"'}></div>
            <div class="finance-field"><label>Local de débito</label><input type="text" placeholder="Ex: CC-1234" value="${r.debito||''}" data-obra="${r.obra.replace(/"/g,'&quot;')}" data-field="debito" onblur="saveFinance(this)"></div>
            <div class="finance-field"><label>Conta razão</label><input type="text" placeholder="Ex: 5.1.01.001" value="${r.conta||''}" data-obra="${r.obra.replace(/"/g,'&quot;')}" data-field="conta" onblur="saveFinance(this)"></div>
            <button class="finance-save" onclick="saveFinanceBtnClick(this)">Salvar dados financeiros</button>
            ${canDelete ? `<button class="delete-demand-btn" onclick="deleteDemand('${r.obra.replace(/'/g,"\\'")}',event)" title="Apagar demanda">🗑️ Apagar demanda</button>` : ''}
          </div>
          <div class="expand-content">${discHtml}</div>
          <div class="files-section">
            <div class="files-header">
              <span>📎 Arquivos anexados</span>
              <span style="font-size:10px;color:var(--faint)" id="file-count-${i}">${(r.files||[]).length} arquivo${(r.files||[]).length!==1?'s':''}</span>
            </div>
            <div class="files-list" id="files-list-${i}">
              ${(r.files&&r.files.length>0) ? r.files.map((f,fi)=>`
                <div class="file-item">
                  <div class="file-icon">${fileIcon(f.name)}</div>
                  <div class="file-meta">
                    <div class="file-name" title="${f.name}">${f.name}</div>
                    <div class="file-info">${f.size} · enviado por ${f.author} · ${f.ts}</div>
                  </div>
                  <div class="file-actions">
                    <button class="file-btn" onclick="downloadFile('${r.obra.replace(/'/g,"\\'")}',${fi},event)">⬇ Baixar</button>
                    ${canDelete ? `<button class="file-btn danger" onclick="removeFile('${r.obra.replace(/'/g,"\\'")}',${fi},event)">✕</button>` : ''}
                  </div>
                </div>`).join('') : `<div class="file-empty">Nenhum arquivo anexado.</div>`}
            </div>
            ${isVisitor ? '' : `
            <div class="file-upload-area" id="upload-area-${i}"
              ondragover="event.preventDefault();this.classList.add('drag-over')"
              ondragleave="this.classList.remove('drag-over')"
              ondrop="handleFileDrop(event,'${r.obra.replace(/'/g,"\\'")}',${i})">
              <input type="file" multiple onchange="handleFileInput(this,'${r.obra.replace(/'/g,"\\'")}',${i})">
              <div class="file-upload-label">Arraste arquivos aqui ou <strong>clique para selecionar</strong><br><span style="font-size:10px;opacity:0.6">Qualquer formato · máx. 10 MB por arquivo</span></div>
            </div>`}
          </div>
          <div class="obs-section">
            <div class="obs-header">
              <span>Observações e histórico</span>
              <span style="font-size:10px;color:var(--faint)">${(r.obs||[]).length} registro${(r.obs||[]).length!==1?'s':''}</span>
            </div>
            <div class="obs-list">${obsHtml}</div>
            <div class="obs-input-row">
              ${isVisitor ? '<span style="font-size:12px;color:var(--faint);font-style:italic;">Visitantes não podem registrar observações.</span>' : `<input type="text" class="obs-input" placeholder="Escreva uma observação…" id="obs-input-${i}"><button class="obs-btn" onclick="addObs('${r.obra.replace(/'/g,"\\'")}',${i})">Registrar</button>`}
            </div>
          </div>
        </td>
      </tr>` : '';

    return `
      <tr data-obra="${r.obra.replace(/"/g,'&quot;')}" class="${isExp?'expanded':''}">
        <td><span class="expand-arrow ${isExp?'open':''}">▶</span></td>
        <td class="obra-col"><span title="${r.obra}">${r.obra}</span><span class="obra-area">${r.area||r.solicitante||''}</span></td>
        <td><span class="loc-pill">${r.local}</span></td>
        <td><span class="tipo-pill ${tipoClass(r.tipo)}" title="${r.tipo}">${(r.tipo||'').trim()}</span></td>
        <td>${statusEl}</td>
        <td class="projetista-col">${r.projetista||'—'}</td>
        <td class="${dateClass(r.previsao, r.status)}">${formatDate(r.previsao)}</td>
        <td>${miniProgress(r.disciplinas)}</td>
      </tr>
      ${expRow}`;
  }).join('');

  tbody.querySelectorAll('tr[data-obra]').forEach(tr => {
    tr.addEventListener('click', e => {
      if (e.target.tagName==='SELECT'||e.target.tagName==='INPUT'||e.target.tagName==='BUTTON') return;
      const obra = tr.getAttribute('data-obra');
      if (expandedRows.has(obra)) expandedRows.delete(obra); else expandedRows.add(obra);
      renderTable();
    });
  });
}

// ── STATUS UPDATE (inline) ──
function updateStatus(sel) {
  if (isVisitor) { alert('Acesso somente leitura.'); renderTable(); return; }
  const obra = sel.getAttribute('data-obra');
  const newVal = sel.value;
  const row = DATA.find(r=>r.obra===obra);
  if (!row) return;
  const oldVal = row.status;
  if (oldVal===newVal) return;
  row.status = newVal;
  if (!row.obs) row.obs = [];
  row.obs.push({ author: currentUser.name, ts: ts(), text: `Status alterado de "${oldVal}" → "${newVal}"`, tag:'status' });
  logAudit('Status alterado', `[${obra}] "${oldVal}" → "${newVal}"`);
  updateMetrics();
  buildCharts();
  renderTable();
}

// ── DISC UPDATE ──
function updateDisc(sel) {
  if (isVisitor) { alert('Acesso somente leitura.'); renderTable(); return; }
  const obra = sel.getAttribute('data-obra');
  const disc = sel.getAttribute('data-disc');
  const newVal = sel.value;
  const row = DATA.find(r=>r.obra===obra);
  if (!row) return;
  const oldVal = row.disciplinas[disc];
  row.disciplinas[disc] = newVal;
  if (!row.obs) row.obs = [];
  row.obs.push({ author: currentUser.name, ts: ts(), text: `Disciplina "${disc}" alterada de "${oldVal}" → "${newVal}"`, tag:'status' });
  logAudit('Status de disciplina', `[${obra}] "${disc}": "${oldVal}" → "${newVal}"`);
  const discItem = sel.closest('.disc-item');
  if (discItem) applyDiscColor(discItem, newVal);
  saveToStorage();
}

// ── FINANCE ──
function saveFinance(input) {
  const obra = input.getAttribute('data-obra');
  const field = input.getAttribute('data-field');
  // RC/Pedido only editable by leticia.ulhoa and mariana.mares
  if (field === 'rc' && currentUser && currentUser.key !== 'leticia.ulhoa' && currentUser.key !== 'mariana.mares') return;
  const row = DATA.find(r=>r.obra===obra);
  if (row) { row[field]=input.value; saveToStorage(); }
}
function saveFinanceBtnClick(btn) {
  if (isVisitor) { alert('Acesso somente leitura.'); return; }
  const section = btn.closest('.finance-section');
  section.querySelectorAll('input').forEach(i=>saveFinance(i));
  btn.textContent='Salvo ✓';
  setTimeout(()=>{btn.textContent='Salvar dados financeiros';},1500);
}

// ── FILE MANAGEMENT ──
function fileIcon(name) {
  const ext = (name.split('.').pop()||'').toLowerCase();
  const map = {
    pdf:'📄', doc:'📝', docx:'📝', xls:'📊', xlsx:'📊', ppt:'📋', pptx:'📋',
    jpg:'🖼️', jpeg:'🖼️', png:'🖼️', gif:'🖼️', webp:'🖼️', svg:'🖼️',
    mp4:'🎬', mov:'🎬', avi:'🎬', mkv:'🎬',
    mp3:'🎵', wav:'🎵',
    zip:'🗜️', rar:'🗜️', '7z':'🗜️',
    txt:'📃', csv:'📊', json:'📦', xml:'📦',
    dwg:'📐', dxf:'📐', skp:'📐',
  };
  return map[ext] || '📁';
}

function formatFileSize(bytes) {
  if (bytes < 1024) return bytes + ' B';
  if (bytes < 1024*1024) return (bytes/1024).toFixed(1) + ' KB';
  return (bytes/(1024*1024)).toFixed(1) + ' MB';
}

function processFiles(files, obra) {
  if (isVisitor) { alert('Acesso somente leitura.'); return; }
  const row = DATA.find(r => r.obra === obra);
  if (!row) return;
  if (!row.files) row.files = [];

  const MAX = 10 * 1024 * 1024; // 10 MB
  let count = 0;

  Array.from(files).forEach(file => {
    if (file.size > MAX) { alert(`"${file.name}" excede 10 MB e não foi anexado.`); return; }
    const reader = new FileReader();
    reader.onload = e => {
      row.files.push({
        name: file.name,
        type: file.type || 'application/octet-stream',
        size: formatFileSize(file.size),
        data: e.target.result, // base64 data URL
        author: currentUser.name,
        ts: ts()
      });
      count++;
      logAudit('Arquivo anexado', `[${obra}] "${file.name}" por ${currentUser.name}.`);
      // Re-render after all files processed
      if (count === files.length || row.files.length > 0) {
        expandedRows.add(obra);
        renderTable();
      }
    };
    reader.readAsDataURL(file);
  });
}

function handleFileInput(input, obra, idx) {
  if (input.files.length) processFiles(input.files, obra);
}

function handleFileDrop(event, obra, idx) {
  event.preventDefault();
  const area = document.getElementById('upload-area-' + idx);
  if (area) area.classList.remove('drag-over');
  if (event.dataTransfer.files.length) processFiles(event.dataTransfer.files, obra);
}

function downloadFile(obra, fileIdx, event) {
  event.stopPropagation();
  const row = DATA.find(r => r.obra === obra);
  if (!row || !row.files || !row.files[fileIdx]) return;
  const f = row.files[fileIdx];
  const a = document.createElement('a');
  a.href = f.data;
  a.download = f.name;
  a.click();
}

function removeFile(obra, fileIdx, event) {
  event.stopPropagation();
  if (!currentUser || currentUser.key !== 'leticia.ulhoa') { alert('Sem permissão para remover arquivos.'); return; }
  const row = DATA.find(r => r.obra === obra);
  if (!row || !row.files) return;
  const fname = row.files[fileIdx].name;
  if (!confirm(`Remover o arquivo "${fname}"?`)) return;
  row.files.splice(fileIdx, 1);
  logAudit('Arquivo removido', `[${obra}] "${fname}" removido por ${currentUser.name}.`);
  expandedRows.add(obra);
  renderTable();
}

// ── DELETE DEMAND (leticia.ulhoa only) ──
function deleteDemand(obra, e) {
  e.stopPropagation();
  if (!currentUser || currentUser.key !== 'leticia.ulhoa') { alert('Sem permissão para apagar demandas.'); return; }
  if (!confirm(`Apagar a demanda "${obra}"? Esta ação não pode ser desfeita.`)) return;
  DATA = DATA.filter(r => r.obra !== obra);
  expandedRows.delete(obra);
  logAudit('Demanda apagada', `"${obra}" apagada por ${currentUser.name}.`);
  updateMetrics(); buildCharts(); renderTable();
}

// ── OBSERVATIONS ──
function addObs(obra, idx) {
  if (isVisitor) { alert('Acesso somente leitura.'); return; }
  const input = document.getElementById(`obs-input-${idx}`);
  const text = input.value.trim();
  if (!text) return;
  const row = DATA.find(r=>r.obra===obra);
  if (!row) return;
  if (!row.obs) row.obs=[];
  row.obs.push({ author:currentUser.name, ts:ts(), text });
  logAudit('Observação adicionada', `[${obra}] "${text}"`);
  input.value='';
  expandedRows.add(obra);
  renderTable();
}

// ── NEW DEMAND ──
function buildDiscGrid() {
  const grid = document.getElementById('discGrid');
  const discs = ['Layout','Planejados','Mobiliário','Pintura','Civil','Persiana','Elétrica','Decoração','Plotagem'];
  grid.innerHTML = discs.map(d => `
    <div class="disc-form-item">
      <label>${d}</label>
      <select id="d-${d}" style="background:var(--surface);border:1px solid var(--border2);border-radius:6px;color:var(--text);font-family:'Sora',sans-serif;font-size:12px;padding:6px 8px;outline:none;">
        <option>Não se aplica</option><option>Previsto</option><option>Planejado</option><option>Em andamento</option><option>Concluído</option><option>Paralizado</option>
      </select>
    </div>`).join('');
}

function openNewModal() {
  if (isVisitor) { alert('Acesso somente leitura.'); return; }
  buildDiscGrid();
  document.getElementById('newModal').classList.add('open');
}
function closeModal() { document.getElementById('newModal').classList.remove('open'); }
function saveNewDemand() {
  const obra = document.getElementById('f-obra').value.trim();
  const local = document.getElementById('f-local').value;
  const tipo = document.getElementById('f-tipo').value;
  const status = document.getElementById('f-status').value;
  if (!obra||!local||!tipo) { alert('Preencha os campos obrigatórios: Nome, Localização e Tipo.'); return; }
  const previsaoRaw = document.getElementById('f-previsao').value;
  const previsao = previsaoRaw ? previsaoRaw+'-01' : '';
  const disciplinas = {};
  ['Layout','Planejados','Mobiliário','Pintura','Civil','Persiana','Elétrica','Decoração','Plotagem'].forEach(d => {
    disciplinas[d] = document.getElementById('d-'+d)?.value||'Não se aplica';
  });
  const obsText = document.getElementById('f-obs').value.trim();
  const obs = [];
  if (obsText) obs.push({ author:currentUser.name, ts:ts(), text:obsText, tag:'criação' });
  obs.push({ author:currentUser.name, ts:ts(), text:'Demanda criada.', tag:'criação' });
  DATA.push({ obra, local, tipo, status, rc: document.getElementById('f-rc').value.trim(), demanda:document.getElementById('f-demanda').value||'', projetista:document.getElementById('f-projetista').value.trim(), fiscal:document.getElementById('f-fiscal').value.trim(), solicitante:document.getElementById('f-solicitante').value.trim(), area:document.getElementById('f-area').value.trim(), previsao, entrega:'', debito:document.getElementById('f-debito').value.trim(), conta:document.getElementById('f-conta').value.trim(), disciplinas, obs });
  logAudit('Nova demanda criada', `"${obra}" adicionada por ${currentUser.name}.`);
  closeModal();
  updateMetrics(); buildFilters(); buildCharts(); renderTable();
}
document.getElementById('newModal').addEventListener('click', e=>{ if(e.target===e.currentTarget) closeModal(); });

// ── SEARCH ──
document.getElementById('searchInput').addEventListener('input', e => {
  searchTerm = e.target.value;
  expandedRows.clear();
  renderTable();
});

// ── SORT ──
document.querySelectorAll('thead th[data-sort]').forEach(th => {
  th.addEventListener('click', () => {
    const col = th.getAttribute('data-sort');
    if (sortCol===col) sortDir=sortDir==='asc'?'desc':'asc';
    else { sortCol=col; sortDir='asc'; }
    document.querySelectorAll('thead th').forEach(t=>t.classList.remove('sort-asc','sort-desc'));
    th.classList.add(sortDir==='asc'?'sort-asc':'sort-desc');
    renderTable();
  });
});

// ── INIT ──
function initApp() {
  updateMetrics();
  buildFilters();
  buildCharts();
  renderTable();
}

// ── BOOTSTRAP ──
async function bootstrap() {
  // Aguarda o Firebase SDK carregar (módulo async)
  await new Promise(resolve => {
    if (window._firebaseReady) return resolve();
    document.addEventListener('firebase-ready', resolve, { once: true });
  });

  await loadFromStorage();
  document.getElementById('loadingScreen').style.display = 'none';
  document.getElementById('loginOverlay').style.display = 'flex';
}

bootstrap();
</script>
</body>
</html>
