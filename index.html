<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RideFlow — Ride Log &amp; Schedule</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@500;600;700&family=Inter:wght@400;500;600&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --asphalt: #20262B;
    --panel: #2A3138;
    --panel-raised: #313943;
    --hairline: #3B444C;
    --chalk: #E9E6DE;
    --muted: #8D969D;
    --paint: #E3B23C;
    --paint-dim: #6b5a2c;
    --stop: #C1443C;
    --go: #6FA85B;
  }
  *{box-sizing:border-box;}
  body{margin:0;}
  html,body{
    background:var(--asphalt);
    color:var(--chalk);
    font-family:'Inter',sans-serif;
    min-height:100vh;
  }
  h1,h2,h3,.brand,.nav-item,.stat-label{
    font-family:'Barlow Condensed',sans-serif;
  }
  .mono{font-family:'IBM Plex Mono',monospace;}

  a{color:var(--paint);}

  .app{
    display:flex;
    min-height:100vh;
  }

  /* Sidebar */
  .sidebar{
    width:220px;
    flex-shrink:0;
    background:#1B2024;
    border-right:1px solid var(--hairline);
    display:flex;
    flex-direction:column;
    padding:24px 0;
  }
  .brand{
    font-size:26px;
    font-weight:700;
    letter-spacing:0.5px;
    color:var(--chalk);
    padding:0 24px 4px;
    line-height:1;
  }
  .brand span{color:var(--paint);}
  .tagline{
    font-size:12px;
    color:var(--muted);
    padding:0 24px 28px;
    border-bottom:1px solid var(--hairline);
    margin-bottom:12px;
  }
  .nav-item{
    font-size:19px;
    font-weight:500;
    color:var(--muted);
    padding:11px 24px;
    cursor:pointer;
    border-left:3px solid transparent;
    transition:color .15s ease, border-color .15s ease, background .15s ease;
    user-select:none;
  }
  .nav-item:hover{color:var(--chalk);}
  .nav-item.active{
    color:var(--chalk);
    border-left-color:var(--paint);
    background:rgba(227,178,60,0.08);
  }
  .sidebar-footer{
    margin-top:auto;
    padding:16px 24px 0;
    border-top:1px solid var(--hairline);
  }
  .sidebar-footer button{
    width:100%;
    margin-bottom:8px;
  }
  .sidebar-footer input[type=file]{display:none;}
  .file-hint{
    font-size:11px;
    color:var(--muted);
    line-height:1.5;
    margin-top:6px;
  }

  /* Main */
  .main{
    flex:1;
    min-width:0;
    padding:32px 40px 56px;
  }
  .view{display:none;}
  .view.active{display:block;}

  .view-title{
    font-size:32px;
    font-weight:600;
    margin:0 0 2px;
  }
  .view-sub{
    color:var(--muted);
    font-size:14px;
    margin:0 0 22px;
  }

  /* Stat strip */
  .stat-strip{
    display:flex;
    gap:0;
    border:1px solid var(--hairline);
    border-radius:4px;
    overflow:hidden;
    margin-bottom:6px;
  }
  .stat{
    flex:1;
    padding:16px 20px;
    border-right:1px solid var(--hairline);
  }
  .stat:last-child{border-right:none;}
  .stat-label{
    font-size:14px;
    color:var(--muted);
    letter-spacing:0.3px;
    margin-bottom:4px;
  }
  .stat-value{
    font-size:28px;
    font-weight:600;
    color:var(--chalk);
  }
  .stat-value.accent{color:var(--paint);}

  .elevation-divider{
    display:block;
    width:100%;
    height:34px;
    margin:0 0 28px;
  }

  /* Panels */
  .panel{
    border:1px solid var(--hairline);
    border-radius:4px;
    background:var(--panel);
    margin-bottom:24px;
  }
  .panel-head{
    display:flex;
    align-items:baseline;
    justify-content:space-between;
    padding:14px 18px;
    border-bottom:1px solid var(--hairline);
  }
  .panel-head h3{
    margin:0;
    font-size:20px;
    font-weight:600;
  }
  .panel-head .count{
    font-size:12px;
    color:var(--muted);
  }
  .panel-body{padding:6px 0;}
  .empty-state{
    padding:26px 18px;
    color:var(--muted);
    font-size:14px;
    line-height:1.6;
  }

  /* Row list (schedule / history) */
  .row{
    display:grid;
    grid-template-columns:96px 1fr auto auto;
    gap:14px;
    align-items:center;
    padding:12px 18px;
    border-bottom:1px solid var(--hairline);
  }
  .row:last-child{border-bottom:none;}
  .row-date{
    font-family:'IBM Plex Mono',monospace;
    font-size:13px;
    color:var(--muted);
  }
  .row-main .type-tag{
    display:inline-block;
    font-size:11px;
    padding:2px 7px;
    border-radius:3px;
    border:1px solid var(--hairline);
    color:var(--muted);
    margin-right:8px;
  }
  .row-main .type-tag.Race{border-color:var(--stop);color:var(--stop);}
  .row-main .type-tag.Interval{border-color:var(--paint);color:var(--paint);}
  .row-main .type-tag.Recovery{border-color:var(--go);color:var(--go);}
  .row-main .title{font-size:15px;font-weight:500;}
  .row-main .meta{font-size:12.5px;color:var(--muted);margin-top:2px;}
  .row-metric{
    font-family:'IBM Plex Mono',monospace;
    font-size:14px;
    text-align:right;
    white-space:nowrap;
  }
  .row-actions{display:flex;gap:6px;}

  /* Buttons */
  button{
    font-family:'Inter',sans-serif;
    font-size:13.5px;
    font-weight:500;
    padding:8px 14px;
    border-radius:4px;
    border:1px solid var(--hairline);
    background:var(--panel-raised);
    color:var(--chalk);
    cursor:pointer;
    transition:background .15s ease, border-color .15s ease;
  }
  button:hover{border-color:var(--muted);}
  button.primary{
    background:var(--paint);
    border-color:var(--paint);
    color:#1B2024;
    font-weight:600;
  }
  button.primary:hover{background:#eec360;}
  button.ghost{
    background:transparent;
  }
  button.danger:hover{border-color:var(--stop);color:var(--stop);}
  button.small{padding:5px 10px;font-size:12px;}

  /* Forms */
  form.card-form{
    padding:18px;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:14px;
  }
  form.card-form .field{display:flex;flex-direction:column;gap:5px;}
  form.card-form .field.span-2{grid-column:span 2;}
  form.card-form .field.span-4{grid-column:span 4;}
  label{font-size:12px;color:var(--muted);}
  input,select,textarea{
    font-family:'Inter',sans-serif;
    background:#1F262B;
    border:1px solid var(--hairline);
    color:var(--chalk);
    padding:9px 10px;
    border-radius:4px;
    font-size:14px;
  }
  input:focus,select:focus,textarea:focus{
    outline:2px solid var(--paint);
    outline-offset:1px;
    border-color:var(--paint);
  }
  textarea{resize:vertical;min-height:38px;font-family:'Inter',sans-serif;}
  .form-actions{
    grid-column:1/-1;
    display:flex;
    justify-content:flex-end;
    gap:8px;
    border-top:1px solid var(--hairline);
    padding-top:14px;
    margin-top:2px;
  }

  input[type=range]{
    -webkit-appearance:none;
    background:transparent;
    padding:0;
  }
  input[type=range]::-webkit-slider-runnable-track{
    height:4px;background:var(--hairline);border-radius:2px;
  }
  input[type=range]::-webkit-slider-thumb{
    -webkit-appearance:none;
    width:16px;height:16px;border-radius:50%;
    background:var(--paint);
    margin-top:-6px;
    cursor:pointer;
  }
  .rpe-readout{
    font-family:'IBM Plex Mono',monospace;
    font-size:13px;
    color:var(--paint);
  }

  /* Weekly bar chart */
  .bars{
    display:flex;
    align-items:flex-end;
    gap:10px;
    height:120px;
    padding:18px;
  }
  .bar-col{
    flex:1;
    display:flex;
    flex-direction:column;
    align-items:center;
    height:100%;
    justify-content:flex-end;
    gap:6px;
  }
  .bar{
    width:100%;
    max-width:34px;
    background:var(--paint-dim);
    border-radius:2px 2px 0 0;
    transition:height .3s ease;
  }
  .bar.has-ride{background:var(--paint);}
  .bar-day{font-size:11px;color:var(--muted);}

  .two-col{
    display:grid;
    grid-template-columns:1.3fr 1fr;
    gap:24px;
  }
  @media (max-width: 900px){
    .two-col{grid-template-columns:1fr;}
    form.card-form{grid-template-columns:repeat(2,1fr);}
    .app{flex-direction:column;}
    .sidebar{width:100%;flex-direction:row;flex-wrap:wrap;padding:14px 16px;}
    .brand,.tagline{padding-left:0;}
    .sidebar-footer{margin-top:12px;width:100%;}
  }

  @media (prefers-reduced-motion: reduce){
    *{transition:none !important;}
  }

  ::placeholder{color:#5b636a;}
  .toast{
    position:fixed;
    bottom:20px;right:20px;
    background:var(--panel-raised);
    border:1px solid var(--paint);
    color:var(--chalk);
    padding:10px 16px;
    border-radius:4px;
    font-size:13px;
    opacity:0;
    transform:translateY(8px);
    transition:opacity .2s ease, transform .2s ease;
    pointer-events:none;
    z-index:50;
  }
  .toast.show{opacity:1;transform:translateY(0);}
</style>
</head>
<body>

<div class="app">
  <div class="sidebar">
    <div class="brand">Ride<span>Flow</span></div>
    <div class="tagline">Ride scheduling &amp; training log</div>
    <div class="nav-item active" data-view="dashboard">Dashboard</div>
    <div class="nav-item" data-view="schedule">Schedule</div>
    <div class="nav-item" data-view="log">Log a ride</div>
    <div class="nav-item" data-view="history">History</div>

    <div class="sidebar-footer">
      <button id="exportBtn" class="ghost">Export data (.json)</button>
      <button id="importTrigger" class="ghost">Import data</button>
      <input type="file" id="importInput" accept="application/json">
      <div class="file-hint">Data lives in this browser tab only. Export before closing it, import to restore.</div>
    </div>
  </div>

  <div class="main">

    <!-- DASHBOARD -->
    <div class="view active" id="view-dashboard">
      <h1 class="view-title">Dashboard</h1>
      <p class="view-sub">Where your training stands this week.</p>

      <div class="stat-strip">
        <div class="stat">
          <div class="stat-label">This week</div>
          <div class="stat-value accent mono" id="statWeekDistance">0 km</div>
        </div>
        <div class="stat">
          <div class="stat-label">Time on the bike</div>
          <div class="stat-value mono" id="statWeekTime">0h 00m</div>
        </div>
        <div class="stat">
          <div class="stat-label">Rides logged</div>
          <div class="stat-value mono" id="statRideCount">0</div>
        </div>
        <div class="stat">
          <div class="stat-label">All-time distance</div>
          <div class="stat-value mono" id="statAllTime">0 km</div>
        </div>
      </div>

      <svg class="elevation-divider" viewBox="0 0 800 34" preserveAspectRatio="none">
        <path d="M0,26 L60,26 L100,10 L150,20 L210,4 L260,18 L320,14 L380,28 L440,8 L500,22 L560,16 L620,26 L680,6 L740,20 L800,12"
              fill="none" stroke="#3B444C" stroke-width="2"/>
      </svg>

      <div class="two-col">
        <div class="panel">
          <div class="panel-head">
            <h3>Next up</h3>
            <span class="count" id="upcomingCount">0 scheduled</span>
          </div>
          <div class="panel-body" id="upcomingPreview"></div>
        </div>

        <div class="panel">
          <div class="panel-head">
            <h3>Last 7 days</h3>
          </div>
          <div class="bars" id="weekBars"></div>
        </div>
      </div>

      <div class="panel">
        <div class="panel-head">
          <h3>Recently logged</h3>
          <span class="count" id="recentCount">0 rides</span>
        </div>
        <div class="panel-body" id="recentPreview"></div>
      </div>
    </div>

    <!-- SCHEDULE -->
    <div class="view" id="view-schedule">
      <h1 class="view-title">Schedule</h1>
      <p class="view-sub">Plan what's next. Mark it done once you've ridden it.</p>

      <div class="panel">
        <div class="panel-head"><h3>Add a planned ride</h3></div>
        <form class="card-form" id="scheduleForm">
          <div class="field">
            <label for="s-date">Date</label>
            <input type="date" id="s-date" required>
          </div>
          <div class="field">
            <label for="s-time">Time</label>
            <input type="time" id="s-time">
          </div>
          <div class="field">
            <label for="s-type">Session type</label>
            <select id="s-type">
              <option>Endurance</option>
              <option>Interval</option>
              <option>Recovery</option>
              <option>Group ride</option>
              <option>Race</option>
            </select>
          </div>
          <div class="field">
            <label for="s-distance">Target distance (km)</label>
            <input type="number" id="s-distance" min="0" step="0.1" placeholder="e.g. 40">
          </div>
          <div class="field span-4">
            <label for="s-notes">Notes</label>
            <textarea id="s-notes" placeholder="Route, intervals, who you're riding with..."></textarea>
          </div>
          <div class="form-actions">
            <button type="submit" class="primary">Add to schedule</button>
          </div>
        </form>
      </div>

      <div class="panel">
        <div class="panel-head">
          <h3>Upcoming</h3>
          <span class="count" id="scheduleCount">0 planned</span>
        </div>
        <div class="panel-body" id="scheduleList"></div>
      </div>
    </div>

    <!-- LOG A RIDE -->
    <div class="view" id="view-log">
      <h1 class="view-title">Log a ride</h1>
      <p class="view-sub">Record what actually happened.</p>

      <div class="panel">
        <form class="card-form" id="logForm">
          <div class="field">
            <label for="l-date">Date</label>
            <input type="date" id="l-date" required>
          </div>
          <div class="field">
            <label for="l-type">Session type</label>
            <select id="l-type">
              <option>Endurance</option>
              <option>Interval</option>
              <option>Recovery</option>
              <option>Group ride</option>
              <option>Race</option>
            </select>
          </div>
          <div class="field">
            <label for="l-distance">Distance (km)</label>
            <input type="number" id="l-distance" min="0" step="0.1" required>
          </div>
          <div class="field">
            <label for="l-hours">Duration</label>
            <div style="display:flex;gap:6px;">
              <input type="number" id="l-hours" min="0" placeholder="hr" style="width:50%;">
              <input type="number" id="l-minutes" min="0" max="59" placeholder="min" style="width:50%;">
            </div>
          </div>
          <div class="field">
            <label for="l-elevation">Elevation gain (m)</label>
            <input type="number" id="l-elevation" min="0" placeholder="e.g. 320">
          </div>
          <div class="field span-2">
            <label for="l-rpe">Perceived effort (RPE) — <span class="rpe-readout" id="rpeReadout">5</span>/10</label>
            <input type="range" id="l-rpe" min="1" max="10" value="5">
          </div>
          <div class="field">
            <label for="l-speed">Avg speed (km/h)</label>
            <input type="number" id="l-speed" min="0" step="0.1" placeholder="optional">
          </div>
          <div class="field span-4">
            <label for="l-notes">Notes</label>
            <textarea id="l-notes" placeholder="How did it feel? Legs, weather, anything worth remembering."></textarea>
          </div>
          <div class="form-actions">
            <button type="submit" class="primary">Save ride</button>
          </div>
        </form>
      </div>
    </div>

    <!-- HISTORY -->
    <div class="view" id="view-history">
      <h1 class="view-title">History</h1>
      <p class="view-sub">Everything you've logged, most recent first.</p>

      <div class="panel">
        <div class="panel-head">
          <h3>Rides</h3>
          <span class="count" id="historyCount">0 total</span>
        </div>
        <div class="panel-body" id="historyList"></div>
      </div>
    </div>

  </div>
</div>

<div class="toast" id="toast"></div>

<script>
  // ---------- state ----------
  let state = {
    scheduled: [],
    logs: []
  };
  let logPrefillFromId = null;

  function uid(){ return Date.now().toString(36) + Math.random().toString(36).slice(2,7); }

  // ---------- nav ----------
  document.querySelectorAll('.nav-item').forEach(item=>{
    item.addEventListener('click', ()=>{
      document.querySelectorAll('.nav-item').forEach(i=>i.classList.remove('active'));
      document.querySelectorAll('.view').forEach(v=>v.classList.remove('active'));
      item.classList.add('active');
      document.getElementById('view-'+item.dataset.view).classList.add('active');
    });
  });
  function goTo(view){
    document.querySelectorAll('.nav-item').forEach(i=>i.classList.toggle('active', i.dataset.view===view));
    document.querySelectorAll('.view').forEach(v=>v.classList.toggle('active', v.id==='view-'+view));
  }

  // ---------- helpers ----------
  function fmtDate(iso){
    const d = new Date(iso+'T00:00:00');
    return d.toLocaleDateString(undefined,{month:'short',day:'numeric'});
  }
  function fmtDuration(hours,minutes){
    const h = hours||0, m = minutes||0;
    return h+'h '+String(m).padStart(2,'0')+'m';
  }
  function totalMinutes(log){
    return (log.hours||0)*60 + (log.minutes||0);
  }
  function todayISO(){
    return new Date().toISOString().slice(0,10);
  }
  function daysAgo(n){
    const d = new Date();
    d.setDate(d.getDate()-n);
    return d.toISOString().slice(0,10);
  }
  function toast(msg){
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.classList.add('show');
    setTimeout(()=>t.classList.remove('show'), 1800);
  }

  // ---------- schedule form ----------
  document.getElementById('scheduleForm').addEventListener('submit', e=>{
    e.preventDefault();
    const item = {
      id: uid(),
      date: document.getElementById('s-date').value,
      time: document.getElementById('s-time').value,
      type: document.getElementById('s-type').value,
      distance: parseFloat(document.getElementById('s-distance').value) || null,
      notes: document.getElementById('s-notes').value.trim()
    };
    if(!item.date) return;
    state.scheduled.push(item);
    e.target.reset();
    renderAll();
    toast('Added to schedule');
  });

  // ---------- log form ----------
  const rpeInput = document.getElementById('l-rpe');
  rpeInput.addEventListener('input', ()=>{
    document.getElementById('rpeReadout').textContent = rpeInput.value;
  });

  document.getElementById('logForm').addEventListener('submit', e=>{
    e.preventDefault();
    const item = {
      id: uid(),
      date: document.getElementById('l-date').value,
      type: document.getElementById('l-type').value,
      distance: parseFloat(document.getElementById('l-distance').value) || 0,
      hours: parseInt(document.getElementById('l-hours').value) || 0,
      minutes: parseInt(document.getElementById('l-minutes').value) || 0,
      elevation: parseFloat(document.getElementById('l-elevation').value) || 0,
      rpe: parseInt(document.getElementById('l-rpe').value),
      avgSpeed: parseFloat(document.getElementById('l-speed').value) || null,
      notes: document.getElementById('l-notes').value.trim(),
      fromScheduleId: logPrefillFromId
    };
    if(!item.date || !item.distance){ toast('Date and distance are required'); return; }

    if(!item.avgSpeed){
      const mins = totalMinutes(item);
      item.avgSpeed = mins>0 ? Math.round((item.distance/(mins/60))*10)/10 : null;
    }

    state.logs.push(item);

    if(logPrefillFromId){
      state.scheduled = state.scheduled.filter(s=>s.id!==logPrefillFromId);
      logPrefillFromId = null;
    }

    e.target.reset();
    rpeInput.value = 5;
    document.getElementById('rpeReadout').textContent = '5';
    renderAll();
    toast('Ride saved');
    goTo('history');
  });

  function logFromSchedule(id){
    const s = state.scheduled.find(x=>x.id===id);
    if(!s) return;
    logPrefillFromId = id;
    document.getElementById('l-date').value = s.date;
    document.getElementById('l-type').value = s.type;
    if(s.distance) document.getElementById('l-distance').value = s.distance;
    goTo('log');
  }

  function deleteScheduled(id){
    state.scheduled = state.scheduled.filter(s=>s.id!==id);
    renderAll();
  }
  function deleteLog(id){
    state.logs = state.logs.filter(l=>l.id!==id);
    renderAll();
  }

  // ---------- rendering ----------
  function renderSchedule(){
    const sorted = [...state.scheduled].sort((a,b)=>a.date.localeCompare(b.date));
    document.getElementById('scheduleCount').textContent = sorted.length + ' planned';

    const list = document.getElementById('scheduleList');
    if(sorted.length===0){
      list.innerHTML = '<div class="empty-state">Nothing on the calendar yet. Add a planned ride above.</div>';
    } else {
      list.innerHTML = sorted.map(s=>`
        <div class="row">
          <div class="row-date">${fmtDate(s.date)}${s.time ? '<br>'+s.time : ''}</div>
          <div class="row-main">
            <span class="type-tag ${s.type}">${s.type}</span>
            <div class="title">${s.distance ? s.distance+' km target' : 'No target set'}</div>
            ${s.notes ? '<div class="meta">'+escapeHtml(s.notes)+'</div>' : ''}
          </div>
          <div></div>
          <div class="row-actions">
            <button class="small primary" onclick="logFromSchedule('${s.id}')">Log result</button>
            <button class="small danger ghost" onclick="deleteScheduled('${s.id}')">Delete</button>
          </div>
        </div>
      `).join('');
    }

    // dashboard preview: next 3
    const upcoming = sorted.filter(s=>s.date>=todayISO()).slice(0,3);
    document.getElementById('upcomingCount').textContent = sorted.filter(s=>s.date>=todayISO()).length + ' scheduled';
    const prev = document.getElementById('upcomingPreview');
    prev.innerHTML = upcoming.length===0
      ? '<div class="empty-state">No upcoming rides scheduled.</div>'
      : upcoming.map(s=>`
        <div class="row" style="grid-template-columns:96px 1fr;">
          <div class="row-date">${fmtDate(s.date)}</div>
          <div class="row-main">
            <span class="type-tag ${s.type}">${s.type}</span>
            <span class="title">${s.distance ? s.distance+' km' : s.type}</span>
          </div>
        </div>
      `).join('');
  }

  function renderHistory(){
    const sorted = [...state.logs].sort((a,b)=>b.date.localeCompare(a.date));
    document.getElementById('historyCount').textContent = sorted.length + ' total';

    const list = document.getElementById('historyList');
    if(sorted.length===0){
      list.innerHTML = '<div class="empty-state">No rides logged yet. Head to "Log a ride" to add your first one.</div>';
    } else {
      list.innerHTML = sorted.map(l=>`
        <div class="row">
          <div class="row-date">${fmtDate(l.date)}</div>
          <div class="row-main">
            <span class="type-tag ${l.type}">${l.type}</span>
            <div class="title">${l.distance} km · ${fmtDuration(l.hours,l.minutes)}</div>
            ${l.notes ? '<div class="meta">'+escapeHtml(l.notes)+'</div>' : ''}
          </div>
          <div class="row-metric mono">${l.avgSpeed ? l.avgSpeed+' km/h' : ''}${l.elevation ? '<br>'+l.elevation+' m gain' : ''}</div>
          <div class="row-actions">
            <button class="small danger ghost" onclick="deleteLog('${l.id}')">Delete</button>
          </div>
        </div>
      `).join('');
    }

    // dashboard preview: last 3
    const recent = sorted.slice(0,3);
    document.getElementById('recentCount').textContent = sorted.length + ' rides';
    const prev = document.getElementById('recentPreview');
    prev.innerHTML = recent.length===0
      ? '<div class="empty-state">Nothing logged yet.</div>'
      : recent.map(l=>`
        <div class="row" style="grid-template-columns:96px 1fr auto;">
          <div class="row-date">${fmtDate(l.date)}</div>
          <div class="row-main">
            <span class="type-tag ${l.type}">${l.type}</span>
            <span class="title">${l.distance} km · ${fmtDuration(l.hours,l.minutes)}</span>
          </div>
          <div class="row-metric mono">${l.avgSpeed ? l.avgSpeed+' km/h' : ''}</div>
        </div>
      `).join('');
  }

  function renderStats(){
    const weekStart = daysAgo(6);
    const weekLogs = state.logs.filter(l=>l.date>=weekStart);
    const weekDistance = weekLogs.reduce((sum,l)=>sum+l.distance,0);
    const weekMinutes = weekLogs.reduce((sum,l)=>sum+totalMinutes(l),0);
    const allTime = state.logs.reduce((sum,l)=>sum+l.distance,0);

    document.getElementById('statWeekDistance').textContent = round1(weekDistance) + ' km';
    document.getElementById('statWeekTime').textContent = fmtDuration(Math.floor(weekMinutes/60), weekMinutes%60);
    document.getElementById('statRideCount').textContent = state.logs.length;
    document.getElementById('statAllTime').textContent = round1(allTime) + ' km';

    // 7-day bar chart
    const bars = document.getElementById('weekBars');
    const days = [];
    for(let i=6;i>=0;i--) days.push(daysAgo(i));
    const dayDistances = days.map(d=>state.logs.filter(l=>l.date===d).reduce((s,l)=>s+l.distance,0));
    const max = Math.max(...dayDistances, 1);
    bars.innerHTML = days.map((d,i)=>{
      const dist = dayDistances[i];
      const h = Math.max((dist/max)*100, dist>0?6:2);
      const label = new Date(d+'T00:00:00').toLocaleDateString(undefined,{weekday:'narrow'});
      return `<div class="bar-col">
        <div class="bar ${dist>0?'has-ride':''}" style="height:${h}%;" title="${dist} km"></div>
        <div class="bar-day">${label}</div>
      </div>`;
    }).join('');
  }

  function round1(n){ return Math.round(n*10)/10; }
  function escapeHtml(str){
    const div = document.createElement('div');
    div.textContent = str;
    return div.innerHTML;
  }

  function renderAll(){
    renderSchedule();
    renderHistory();
    renderStats();
  }

  // ---------- export / import ----------
  document.getElementById('exportBtn').addEventListener('click', ()=>{
    const blob = new Blob([JSON.stringify(state,null,2)], {type:'application/json'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = 'cadence-data-'+todayISO()+'.json';
    a.click();
    URL.revokeObjectURL(url);
    toast('Exported');
  });

  document.getElementById('importTrigger').addEventListener('click', ()=>{
    document.getElementById('importInput').click();
  });
  document.getElementById('importInput').addEventListener('change', e=>{
    const file = e.target.files[0];
    if(!file) return;
    const reader = new FileReader();
    reader.onload = ev=>{
      try{
        const data = JSON.parse(ev.target.result);
        if(data.scheduled && data.logs){
          state = data;
          renderAll();
          toast('Data imported');
        } else {
          toast("That file doesn't look right");
        }
      }catch(err){
        toast('Could not read that file');
      }
    };
    reader.readAsText(file);
    e.target.value = '';
  });

  // ---------- init ----------
  document.getElementById('l-date').value = todayISO();
  document.getElementById('s-date').value = todayISO();

  renderAll();
</script>

</body>
</html>
