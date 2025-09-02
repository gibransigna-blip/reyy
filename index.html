<!doctype html>
<html lang="id">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Telegram Bot Console — Full</title>
<style>
  :root{
    --bg:#f6f7fb; --card:#ffffff; --text:#0b1220; --muted:#6b7280; --accent:#4f46e5; --muted-bg:#f3f4f6;
  }
  [data-theme="dark"]{
    --bg:#071025; --card:#071126; --text:#e6eef8; --muted:#9aa8bf; --accent:#60a5fa; --muted-bg:#0b1220;
  }
  html,body{height:100%;margin:0;font-family:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;background:var(--bg);color:var(--text);-webkit-font-smoothing:antialiased}
  header{background:linear-gradient(90deg,var(--accent),#06b6d4);color:white;padding:14px 18px;display:flex;justify-content:space-between;align-items:center;gap:12px}
  .brand{display:flex;align-items:center;gap:12px;font-weight:700}
  .shell{max-width:1150px;margin:20px auto;padding:16px}
  .card{background:var(--card);border-radius:12px;padding:14px;box-shadow:0 8px 22px rgba(2,6,23,0.06);border:1px solid rgba(2,6,23,0.04)}
  .grid{display:grid;grid-template-columns:1fr 380px;gap:16px}
  .tabs{display:flex;gap:8px;margin-bottom:12px;flex-wrap:wrap}
  .tab{padding:8px 12px;border-radius:10px;cursor:pointer;background:#eef2ff;color:#3730a3;border:1px solid rgba(99,102,241,0.1)}
  .tab.active{background:var(--accent);color:#fff}
  label{display:block;font-size:13px;color:var(--text);margin-top:8px}
  input[type=text], input[type=password], textarea, select{width:100%;padding:10px;border-radius:8px;border:1px solid #e6edf3;background:transparent;color:var(--text)}
  textarea{min-height:90px}
  button{background:var(--accent);color:#fff;border:0;padding:8px 12px;border-radius:8px;cursor:pointer}
  button.ghost{background:transparent;border:1px solid #e6edf3;color:var(--text);padding:8px 12px}
  .muted{font-size:13px;color:var(--muted)}
  .small{font-size:12px}
  .list{max-height:420px;overflow:auto}
  .list-item{display:flex;justify-content:space-between;align-items:center;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.03);margin-bottom:8px;background:linear-gradient(180deg, rgba(0,0,0,0.01), transparent)}
  .avatar{width:72px;height:72px;border-radius:999px;object-fit:cover;border:2px solid rgba(99,102,241,0.12)}
  .log{max-height:220px;overflow:auto;background:var(--muted-bg);padding:8px;border-radius:8px;font-size:13px;white-space:pre-wrap}
  #toast{position:fixed;right:18px;bottom:18px;background:#111;color:#fff;padding:10px 14px;border-radius:8px;opacity:0;transition:opacity .25s;z-index:9999}
  #toast.show{opacity:1}
  .confirm-overlay{position:fixed;inset:0;background:rgba(2,6,23,0.45);display:flex;align-items:center;justify-content:center;visibility:hidden;z-index:9998}
  .confirm-overlay.show{visibility:visible}
  .confirm-box{background:var(--card);padding:18px;border-radius:12px;max-width:520px;width:calc(100% - 40px);color:var(--text);box-shadow:0 8px 30px rgba(2,6,23,0.15)}
  .row{display:flex;gap:8px;align-items:center}
  .col{display:flex;flex-direction:column;gap:8px}
  .right{margin-left:auto}
  .note{font-size:12px;color:var(--muted);margin-top:8px}
  .kbd{background:#f1f5f9;border-radius:6px;padding:2px 6px;font-size:12px}
  @media (max-width:980px){.grid{grid-template-columns:1fr} .tabs{overflow:auto}}
</style>
</head>
<body>
<header>
  <div class="brand">
    <div style="font-size:18px">🤖 Telegram Bot Console — Full</div>
    <div id="connectedBadge" style="display:none;background:rgba(255,255,255,0.12);padding:6px 8px;border-radius:999px;font-size:12px">Connected</div>
  </div>
  <div style="display:flex;align-items:center;gap:12px">
    <label style="color:#fff;display:flex;align-items:center;gap:8px">Dark
      <input id="themeToggle" type="checkbox" style="margin-left:6px"/>
    </label>
    <button id="logoutBtn" class="ghost" style="background:transparent;border:1px solid rgba(255,255,255,0.14);color:#fff;padding:8px 10px;border-radius:8px">Logout</button>
  </div>
</header>

<main class="shell">
  <!-- Connect -->
  <section id="connectCard" class="card">
    <div class="grid">
      <div>
        <label>Bot Token</label>
        <input id="tokenInput" type="password" placeholder="123456:ABC-DEF..." />
        <label>API Base URL (opsional — gunakan proxy jika perlu)</label>
        <input id="baseInput" type="text" placeholder="https://api.telegram.org" />
        <div style="display:flex;gap:8px;margin-top:10px">
          <button id="connectBtn">🔗 Connect</button>
          <button id="saveBtn" class="ghost">💾 Save</button>
          <button id="clearBtn" class="ghost">🗑️ Clear</button>
        </div>
        <div class="note">Jika kamu jalankan file lokal (`file://`) dan muncul <code>CORS</code>, pakai Live Server / host / atau proxy. Jika sebelumnya sudah berhasil, tinggal connect.</div>
      </div>

      <div style="width:320px">
        <div class="card" style="padding:12px">
          <div style="display:flex;gap:12px;align-items:center">
            <img id="homeAvatar" class="avatar" src="" alt="avatar" style="display:none" />
            <div>
              <div id="homeName" style="font-weight:600">—</div>
              <div id="homeHandle" class="muted">@— · ID: —</div>
            </div>
          </div>
          <div id="homeShort" class="muted" style="margin-top:8px">Short description: —</div>
          <div id="homeDesc" class="muted small" style="margin-top:8px">—</div>
        </div>
      </div>
    </div>
  </section>

  <!-- App -->
  <section id="appShell" class="card" style="margin-top:16px;display:none">
    <div class="tabs" role="tablist">
      <div class="tab tab-active" data-tab="home">Home</div>
      <div class="tab" data-tab="send">Send</div>
      <div class="tab" data-tab="edit">Edit Bot</div>
      <div class="tab" data-tab="group">Manage Group</div>
    </div>

    <!-- HOME -->
    <div id="tab-home" class="tab-panel" style="display:block">
      <div class="grid">
        <div>
          <div class="card">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div>
                <div style="font-weight:700" id="botTitle">—</div>
                <div class="muted" id="botMeta">@— · ID: —</div>
              </div>
              <div>
                <button id="refreshBtn" class="ghost">↻ Refresh</button>
                <button id="deleteWebhookBtn" class="ghost">Delete Webhook</button>
              </div>
            </div>

            <div id="botPreview" style="margin-top:12px"></div>
          </div>

          <div class="card" style="margin-top:12px">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:600">Recent Chats / Groups (dari getUpdates)</div>
              <div style="display:flex;gap:8px;align-items:center">
                <input id="searchGroups" placeholder="Cari nama / id grup..." style="padding:8px;border-radius:8px;border:1px solid #e6edf3" />
                <button id="loadUpdatesBtn" class="ghost">Load Updates</button>
              </div>
            </div>
            <div style="margin-top:10px" class="note small">Daftar group/chat disimpan otomatis dan dipersist ke <code>localStorage</code>. Jika list kosong, klik Load Updates setelah ada aktivitas di grup.</div>
            <div id="chatList" class="list" style="margin-top:12px"></div>
            <div style="display:flex;gap:8px;margin-top:10px">
              <button id="exportChats" class="ghost">Export (JSON)</button>
              <button id="importChats" class="ghost">Import (JSON)</button>
              <button id="clearSavedChats" class="ghost">Clear Saved Group Cache</button>
              <input id="fileInput" type="file" accept="application/json" style="display:none"/>
            </div>
          </div>
        </div>

        <div>
          <div class="card">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:600">Actions</div>
              <div class="muted small">Status: <span id="statusDot">Disconnected</span></div>
            </div>

            <label style="margin-top:10px">Quick Chat ID (klik list untuk autofill)</label>
            <input id="quickChatId" />

            <div style="display:flex;gap:8px;margin-top:8px">
              <button id="gotoSend" class="ghost">Go to Send</button>
              <button id="gotoGroup" class="ghost">Go to Manage Group</button>
            </div>

            <div style="margin-top:12px">
              <div style="font-weight:600">Activity Log</div>
              <pre id="activityLog" class="log"></pre>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- SEND -->
    <div id="tab-send" class="tab-panel" style="display:none;margin-top:12px">
      <div class="grid">
        <div>
          <div class="card">
            <label>Chat ID</label>
            <input id="sendChatId" />
            <label>Pesan</label>
            <textarea id="sendText"></textarea>
            <label>Parse Mode</label>
            <select id="parseMode"><option value="">none</option><option value="MarkdownV2">MarkdownV2</option><option value="HTML">HTML</option></select>
            <div style="display:flex;gap:8px;margin-top:10px">
              <button id="sendBtn">Kirim</button>
              <button id="clearSend" class="ghost">Clear</button>
            </div>
            <div id="sendResult" class="muted small" style="margin-top:8px"></div>
          </div>
        </div>

        <div>
          <div class="card">
            <div style="font-weight:600">Pesan Terkirim</div>
            <div id="sentList" class="list" style="margin-top:8px"></div>
          </div>
        </div>
      </div>
    </div>

    <!-- EDIT BOT -->
    <div id="tab-edit" class="tab-panel" style="display:none;margin-top:12px">
      <div class="grid">
        <div>
          <div class="card">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:700">Edit Bot (official API)</div>
              <div class="muted small">Note: ganti foto akun bot hanya via @BotFather. Kita bisa set chat photo untuk grup/channel.</div>
            </div>

            <label>Language Code (optional)</label>
            <input id="langCode" placeholder="e.g. id or en" />

            <label>Nama Tampilan</label>
            <input id="nameInput" />
            <div style="display:flex;gap:8px;margin-top:8px">
              <button id="getName" class="ghost">Get</button>
              <button id="setName">Set</button>
            </div>
            <div id="nameHint" class="muted small"></div>

            <label style="margin-top:10px">Short Description</label>
            <input id="shortInput" maxlength="120" />
            <div style="display:flex;gap:8px;margin-top:8px">
              <button id="getShort" class="ghost">Get</button>
              <button id="setShort">Set</button>
            </div>
            <div id="shortHint" class="muted small"></div>

            <label style="margin-top:10px">Description</label>
            <textarea id="descInput"></textarea>
            <div style="display:flex;gap:8px;margin-top:8px">
              <button id="getDesc" class="ghost">Get</button>
              <button id="setDesc">Set</button>
            </div>
            <div id="descHint" class="muted small"></div>

            <label style="margin-top:10px">Commands (JSON)</label>
            <textarea id="commandsInput" placeholder='[{"command":"start","description":"Start"}]'></textarea>
            <div style="display:flex;gap:8px;margin-top:8px">
              <button id="getCmd" class="ghost">Get</button>
              <button id="setCmd">Set</button>
            </div>
            <div id="cmdHint" class="muted small"></div>
          </div>
        </div>

        <div>
          <div class="card">
            <div style="font-weight:700">Set Chat Photo (grup/channel)</div>
            <label>Target Chat ID</label>
            <input id="photoChatId" placeholder="-1001234567890" />
            <label>Upload Image</label>
            <input id="photoFile" type="file" accept="image/*" />
            <div style="display:flex;gap:8px;margin-top:8px">
              <button id="setChatPhotoBtn">Upload & Set</button>
              <button id="clearPhoto" class="ghost">Clear</button>
            </div>
            <div id="photoHint" class="muted small" style="margin-top:8px"></div>
          </div>
        </div>
      </div>
    </div>

    <!-- GROUP TOOLS -->
    <div id="tab-group" class="tab-panel" style="display:none;margin-top:12px">
      <p class="muted">Fitur ini hanya bekerja jika bot adalah admin grup.</p>
      <div class="grid">
        <div>
          <div class="card">
            <label>Group Chat ID</label>
            <input id="groupId" />
            <div style="display:flex;gap:8px;margin-top:8px">
              <button id="loadAdmins">Load Admins</button>
              <button id="loadUpdates2" class="ghost">Load Recent Chats</button>
            </div>
            <div style="margin-top:10px"><input id="groupSearch2" placeholder="Search groups..." style="padding:8px;border-radius:8px;border:1px solid #e6edf3" /></div>

            <div id="adminsBox" class="list" style="margin-top:10px"></div>
          </div>
        </div>

        <div>
          <div class="card">
            <label>Target User ID</label>
            <input id="targetUser" />
            <div style="display:flex;gap:8px;margin-top:8px;flex-wrap:wrap">
              <button id="kickUser">Kick / Ban</button>
              <button id="unbanUser" class="ghost">Unban</button>
              <button id="promoteUser">Promote</button>
              <button id="demoteUser" class="ghost">Demote</button>
            </div>

            <div style="margin-top:12px;font-weight:600">Promote Rights</div>
            <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:8px">
              <label><input type="checkbox" id="r_change_info"/> change_info</label>
              <label><input type="checkbox" id="r_delete_msgs"/> delete_messages</label>
              <label><input type="checkbox" id="r_invite"/> invite_users</label>
              <label><input type="checkbox" id="r_restrict"/> restrict_members</label>
              <label><input type="checkbox" id="r_promote"/> promote_members</label>
              <label><input type="checkbox" id="r_pin"/> pin_messages</label>
              <label><input type="checkbox" id="r_topics"/> manage_topics</label>
            </div>

            <div id="groupHint" class="muted small" style="margin-top:10px"></div>
          </div>
        </div>
      </div>
    </div>

  </section>
</main>

<div id="toast"></div>
<div id="confirm" class="confirm-overlay"><div class="confirm-box"><div id="confirmText">Sure?</div><div style="display:flex;justify-content:center;margin-top:12px"><button id="confirmYes" style="margin-right:8px">Yes</button><button id="confirmNo" class="ghost">No</button></div></div></div>

<script>
/* Full single-file Telegram dashboard
   - Direct Telegram Bot API calls (may hit CORS if run from file://)
   - Save groups to localStorage key 'tg_chats' (auto-merge)
   - All features requested are included
*/

const $ = s => document.querySelector(s);
const $$ = s => Array.from(document.querySelectorAll(s));

const STORAGE = { token: 'tg_token', base:'tg_base', chats:'tg_chats', theme:'tg_theme' };
let state = {
  token: localStorage.getItem(STORAGE.token) || '',
  base: localStorage.getItem(STORAGE.base) || 'https://api.telegram.org',
  me: null,
  chats: new Map(),
  pendingAction: null
};

// toast & log
function toast(msg, ok=true){ const t=$('#toast'); t.textContent=msg; t.style.background = ok? '#111' : '#b91c1c'; t.classList.add('show'); setTimeout(()=>t.classList.remove('show'),3000); }
function logAct(msg){ const p=$('#activityLog'); const now=new Date().toLocaleTimeString(); p.textContent = `[${now}] ${msg}\n` + p.textContent; saveChatsToStorage(); }

// theme
(function(){
  const th = localStorage.getItem(STORAGE.theme)||'light';
  if(th==='dark') document.documentElement.setAttribute('data-theme','dark');
  $('#themeToggle').checked = th==='dark';
  $('#themeToggle').addEventListener('change', e=>{
    const t = e.target.checked ? 'dark':'light';
    if(t==='dark') document.documentElement.setAttribute('data-theme','dark'); else document.documentElement.removeAttribute('data-theme');
    localStorage.setItem(STORAGE.theme, t);
  });
})();

// utils: storage for chats
function loadChatsFromStorage(){
  try{
    const raw = localStorage.getItem(STORAGE.chats);
    if(!raw) return;
    const arr = JSON.parse(raw);
    if(Array.isArray(arr)) arr.forEach(c=> state.chats.set(c.id, c));
  }catch(e){ console.warn('loadChats err',e); }
}
function saveChatsToStorage(){
  try{
    const arr = Array.from(state.chats.values());
    localStorage.setItem(STORAGE.chats, JSON.stringify(arr));
  }catch(e){ console.warn('saveChats err',e); }
}
function mergeChats(newChats){
  for(const c of newChats){
    if(!state.chats.has(c.id)) state.chats.set(c.id, c);
    else {
      const old = state.chats.get(c.id);
      if(old.title !== c.title || old.type !== c.type) state.chats.set(c.id, c);
    }
  }
  saveChatsToStorage();
}

// apiCall supports FormData if isForm=true
async function apiCall(method, params=null, isForm=false){
  const url = `${state.base.replace(/\/$/,'')}/bot${state.token}/${method}`;
  const opts = {};
  if(isForm && params instanceof FormData){ opts.method='POST'; opts.body = params; }
  else if(params){ opts.method='POST'; opts.headers={'Content-Type':'application/json'}; opts.body = JSON.stringify(params); }
  else opts.method='GET';
  const res = await fetch(url, opts);
  const j = await res.json();
  if(!j.ok) throw new Error(j.description || JSON.stringify(j));
  return j.result;
}

// UI wiring
(function initUI(){
  // inputs initial
  $('#tokenInput').value = state.token;
  $('#baseInput').value = state.base;
  loadChatsFromStorage();
  renderChats();

  $('#saveBtn').addEventListener('click', ()=>{ state.token = $('#tokenInput').value.trim(); state.base = $('#baseInput').value.trim() || 'https://api.telegram.org'; localStorage.setItem(STORAGE.token,state.token); localStorage.setItem(STORAGE.base,state.base); toast('Saved credentials'); });
  $('#clearBtn').addEventListener('click', ()=>{ localStorage.removeItem(STORAGE.token); localStorage.removeItem(STORAGE.base); $('#tokenInput').value=''; $('#baseInput').value='https://api.telegram.org'; toast('Cleared'); });
  $('#logoutBtn').addEventListener('click', ()=>{ localStorage.removeItem(STORAGE.token); localStorage.removeItem(STORAGE.base); location.reload(); });

  $$('.tab').forEach(t=>t.addEventListener('click', ()=>{ $$('.tab').forEach(x=>x.classList.remove('active')); t.classList.add('active'); $$('.tab-panel').forEach(p=>p.style.display='none'); document.getElementById('tab-'+t.dataset.tab).style.display='block'; }));

  $('#connectBtn').addEventListener('click', ()=>{ state.token = $('#tokenInput').value.trim(); state.base = $('#baseInput').value.trim() || 'https://api.telegram.org'; if(!state.token){ toast('Token kosong',false); return; } localStorage.setItem(STORAGE.token,state.token); localStorage.setItem(STORAGE.base,state.base); connect(); });
  $('#tokenInput').addEventListener('keydown', e=>{ if(e.key==='Enter') $('#connectBtn').click(); });

  $('#refreshBtn').addEventListener('click', ()=> fillPreview().then(()=>toast('Preview refreshed')).catch(e=>toast('Preview failed: '+e.message,false)));
  $('#deleteWebhookBtn').addEventListener('click', async ()=>{ try{ await apiCall('deleteWebhook'); toast('Webhook deleted'); logAct('deleteWebhook'); }catch(e){ toast('deleteWebhook failed: '+e.message,false); } });

  $('#loadUpdatesBtn').addEventListener('click', loadUpdates);
  $('#loadChatsBtn')?.addEventListener('click', loadUpdates);
  $('#loadChatsBtn2')?.addEventListener('click', loadUpdates);

  $('#sendBtn').addEventListener('click', async ()=>{ const chat_id = $('#sendChatId').value.trim(); const text = $('#sendText').value.trim(); const parse_mode = $('#parseMode').value||undefined; if(!chat_id||!text){ toast('Isi chat id & pesan', false); return; } try{ const body = {chat_id, text}; if(parse_mode) body.parse_mode = parse_mode; const msg = await apiCall('sendMessage', body); $('#sentList').insertAdjacentHTML('afterbegin', `<div class="list-item">[${chat_id}] ${escapeHtml(text)}</div>`); $('#sendText').value=''; toast('Message sent'); logAct('Sent message to '+chat_id); }catch(e){ toast('sendMessage failed: '+e.message,false); } });

  $('#clearSend').addEventListener('click', ()=>{ $('#sendText').value=''; $('#sendResult').textContent=''; });

  // edit bot
  $('#getName').addEventListener('click', async ()=>{ try{ const r = await apiCall('getMyName'); $('#nameInput').value = r.name || ''; $('#nameHint').textContent='Loaded'; }catch(e){ $('#nameHint').textContent='Error'; toast('getMyName failed',false); }});
  $('#setName').addEventListener('click', async ()=>{ try{ const name = $('#nameInput').value.trim(); const lang = $('#langCode').value.trim()||undefined; const body = lang ? {name, language_code: lang} : {name}; await apiCall('setMyName', body); $('#nameHint').textContent='Updated'; toast('Name updated'); logAct('setMyName'); }catch(e){ $('#nameHint').textContent='Error'; toast('setMyName failed',false); }});

  $('#getShort').addEventListener('click', async ()=>{ try{ const r = await apiCall('getMyShortDescription'); $('#shortInput').value = r.short_description || ''; $('#shortHint').textContent='Loaded'; }catch(e){ $('#shortHint').textContent='Error'; toast('getMyShortDescription failed',false); }});
  $('#setShort').addEventListener('click', async ()=>{ try{ const short = $('#shortInput').value.trim(); const lang = $('#langCode').value.trim()||undefined; const body = lang? {short_description:short, language_code:lang} : {short_description:short}; await apiCall('setMyShortDescription', body); $('#shortHint').textContent='Updated'; toast('Short description updated'); logAct('setMyShortDescription'); }catch(e){ $('#shortHint').textContent='Error'; toast('setMyShortDescription failed',false); }});

  $('#getDesc').addEventListener('click', async ()=>{ try{ const r = await apiCall('getMyDescription'); $('#descInput').value = r.description || ''; $('#descHint').textContent='Loaded'; }catch(e){ $('#descHint').textContent='Error'; toast('getMyDescription failed',false); }});
  $('#setDesc').addEventListener('click', async ()=>{ try{ const d = $('#descInput').value.trim(); const lang = $('#langCode').value.trim()||undefined; const body = lang? {description:d, language_code:lang} : {description:d}; await apiCall('setMyDescription', body); $('#descHint').textContent='Updated'; toast('Description updated'); logAct('setMyDescription'); }catch(e){ $('#descHint').textContent='Error'; toast('setMyDescription failed',false); }});

  $('#getCmd').addEventListener('click', async ()=>{ try{ const r = await apiCall('getMyCommands'); $('#commandsInput').value = JSON.stringify(r||[],null,2); $('#cmdHint').textContent='Loaded'; }catch(e){ $('#cmdHint').textContent='Error'; toast('getMyCommands failed',false); }});
  $('#setCmd').addEventListener('click', async ()=>{ try{ const txt = $('#commandsInput').value.trim(); const commands = txt ? JSON.parse(txt) : []; await apiCall('setMyCommands',{commands}); $('#cmdHint').textContent='Updated'; toast('Commands updated'); logAct('setMyCommands'); }catch(e){ $('#cmdHint').textContent='Error'; toast('setMyCommands failed',false); }});

  // set chat photo
  $('#setChatPhotoBtn').addEventListener('click', async ()=>{
    try{
      const chat_id = $('#photoChatId').value.trim(); const file = $('#photoFile').files[0];
      if(!chat_id || !file) return toast('Pilih target chat dan file', false);
      const fd = new FormData(); fd.append('chat_id', chat_id); fd.append('photo', file);
      await apiCall('setChatPhoto', fd, true);
      $('#photoHint').textContent = 'Chat photo updated (jika bot admin)';
      toast('Chat photo set'); logAct('setChatPhoto '+chat_id);
    }catch(e){ $('#photoHint').textContent='Error'; toast('setChatPhoto failed',false); }
  });
  $('#clearPhoto').addEventListener('click', ()=>{ $('#photoFile').value=''; $('#photoChatId').value=''; $('#photoHint').textContent=''; });

  // group tools
  $('#loadAdmins').addEventListener('click', loadAdmins);
  $('#loadUpdates2').addEventListener('click', loadUpdates);

  $('#kickUser').addEventListener('click', ()=> promptAndConfirm('kick'));
  $('#unbanUser').addEventListener('click', ()=> promptAndConfirm('unban'));
  $('#promoteUser').addEventListener('click', ()=> promptAndConfirm('promote'));
  $('#demoteUser').addEventListener('click', ()=> promptAndConfirm('demote'));

  // confirm overlay handling
  $('#confirmYes').addEventListener('click', async ()=>{
    $('#confirm').classList.remove('show');
    if(!state.pendingAction) return;
    const p = state.pendingAction; state.pendingAction = null;
    await doGroupAction(p.action, p.chat_id, p.user_id);
  });
  $('#confirmNo').addEventListener('click', ()=>{ state.pendingAction=null; $('#confirm').classList.remove('show'); });

  // export/import chats
  $('#exportChats').addEventListener('click', ()=>{ const data = JSON.stringify(Array.from(state.chats.values()), null, 2); const blob = new Blob([data],{type:'application/json'}); const url = URL.createObjectURL(blob); const a = document.createElement('a'); a.href=url; a.download='tg_chats.json'; a.click(); URL.revokeObjectURL(url); });
  $('#importChats').addEventListener('click', ()=> $('#fileInput').click());
  $('#fileInput').addEventListener('change', e=>{
    const f = e.target.files[0]; if(!f) return;
    const reader = new FileReader(); reader.onload = ()=>{ try{ const arr = JSON.parse(reader.result); if(Array.isArray(arr)){ mergeChats(arr); renderChats(); toast('Imported chats'); } }catch(err){ toast('Invalid file', false); } }; reader.readAsText(f);
  });
  $('#clearSavedChats').addEventListener('click', ()=>{ localStorage.removeItem(STORAGE.chats); state.chats.clear(); renderChats(); toast('Saved group cache cleared'); });

  // search handlers (debounced)
  let searchTimer = null;
  $('#searchGroups').addEventListener('input', e=>{ clearTimeout(searchTimer); searchTimer=setTimeout(()=>renderChats(e.target.value.trim()),160); });
  $('#groupSearch2').addEventListener('input', e=>{ clearTimeout(searchTimer); searchTimer=setTimeout(()=>renderChats(e.target.value.trim()),160); });

  // quick nav
  $('#gotoSend').addEventListener('click', ()=> setActiveTab('send'));
  $('#gotoGroup').addEventListener('click', ()=> setActiveTab('group'));

  // auto connect if token stored
  (async ()=>{
    if(state.token){
      try{ await connect(); }catch(e){ console.warn('auto connect failed', e); }
    } else {
      // render cached chats if any
      renderChats();
    }
  })();

})(); // initUI closure end

// connect flow
async function connect(){
  try{
    state.token = state.token || $('#tokenInput').value.trim();
    state.base = state.base || $('#baseInput').value.trim() || 'https://api.telegram.org';
    $('#statusDot').textContent='Connecting...';
    const me = await apiCall('getMe');
    state.me = me;
    $('#connectedBadge').style.display='inline-block';
    $('#statusDot').textContent='Connected';
    $('#homeName').textContent = me.first_name || me.username;
    $('#homeHandle').textContent = `@${me.username} · ID: ${me.id}`;
    $('#botTitle').textContent = me.first_name || me.username;
    $('#botMeta').textContent = `@${me.username} · ID: ${me.id}`;
    $('#connectCard').style.display='none';
    $('#appShell').style.display='block';
    toast('Connected ✔️');
    logAct('Connected as @' + (me.username || me.id));
    await fillPreview();
    renderChats();
    try{ await loadUpdates(); }catch(e){ console.warn('getUpdates failed', e); }
  }catch(err){
    $('#statusDot').textContent='Disconnected';
    toast('Connect failed: ' + err.message, false);
    console.error(err);
    throw err;
  }
}

// fill preview: name, short, desc, photo
async function fillPreview(){
  try{
    const name = await apiCall('getMyName').catch(()=>({name:state.me.first_name||state.me.username}));
    const short = await apiCall('getMyShortDescription').catch(()=>({short_description:''}));
    const desc = await apiCall('getMyDescription').catch(()=>({description:''}));
    $('#homeShort').textContent = 'Short description: ' + (short.short_description || '-');
    $('#homeDesc').textContent = desc.description || '-';
    let photos = { total_count:0 };
    try{ photos = await apiCall('getUserProfilePhotos',{user_id: state.me.id, limit:1}); }catch(e){ /*ignore*/ }
    if(photos.total_count && photos.photos && photos.photos.length){
      const fileId = photos.photos[0][0].file_id;
      try{
        const file = await apiCall('getFile', {file_id: fileId});
        const fileUrl = `${state.base.replace(/\/$/,'')}/file/bot${state.token}/${file.file_path}`;
        $('#homeAvatar').src = fileUrl; $('#homeAvatar').style.display='block';
        $('#botPreview').innerHTML = `<div style="display:flex;gap:12px;align-items:center"><img src="${fileUrl}" class="avatar" /><div><div style="font-weight:700">${escapeHtml(name.name||'')}</div><div class="muted">${escapeHtml(short.short_description||'')}</div></div></div><div style="margin-top:10px" class="muted small">${escapeHtml((desc.description||'').slice(0,400))}</div>`;
      }catch(e){ console.warn('getFile failed', e); $('#botPreview').innerHTML = `<div><div style="font-weight:700">${escapeHtml(name.name||'')}</div><div class="muted">${escapeHtml(short.short_description||'')}</div></div><div class="muted small">${escapeHtml((desc.description||'').slice(0,400))}</div>`; }
    } else {
      $('#botPreview').innerHTML = `<div><div style="font-weight:700">${escapeHtml(name.name||'')}</div><div class="muted">${escapeHtml(short.short_description||'')}</div></div><div class="muted small">${escapeHtml((desc.description||'').slice(0,400))}</div>`;
    }
  }catch(e){ console.warn('fillPreview error', e); throw e; }
}

// simpan id update terakhir biar ga dobel
let lastUpdateId = 0;

// fungsi polling pesan masuk
async function pollMessages() {
  try {
    let res = await fetch(`https://api.telegram.org/bot${state.token}/getUpdates?offset=${lastUpdateId+1}`);
    let data = await res.json();

    if (data.result && data.result.length > 0) {
      data.result.forEach(upd => {
        lastUpdateId = upd.update_id;

        if (upd.message) {
          const from = upd.message.from.username || upd.message.from.first_name || upd.message.from.id;
          const text = upd.message.text || "[non-text]";

          // bikin elemen untuk log
          const div = document.createElement("div");
          div.innerHTML = `<b>${from}:</b> ${text}`;
          // kalau yang balas bukan bot sendiri, kasih warna kuning
          div.style.color = (upd.message.from.id === state.me?.id) ? "#0f0" : "#ff0";

          document.getElementById("log").appendChild(div);
          document.getElementById("log").scrollTop = document.getElementById("log").scrollHeight;
        }
      });
    }
  } catch (e) {
    console.log("Error polling:", e);
  }
}

// jalanin polling tiap 3 detik
setInterval(pollMessages, 3000);

// loadUpdates -> getUpdates -> merge chats
async function loadUpdates(){
  try{
    const updates = await apiCall('getUpdates');
    const newChats = [];
    if(Array.isArray(updates)){
      for(const u of updates){
        const msg = u.message || u.channel_post || u.edited_message || u.edited_channel_post;
        if(msg && msg.chat){
          const c = msg.chat;
          const id = c.id;
          const title = c.title || (c.first_name ? (c.first_name + (c.last_name ? ' ' + c.last_name : '')) : c.username) || String(id);
          newChats.push({id, title, type: c.type});
        }
      }
    }
    if(newChats.length){
      mergeChats(newChats);
      renderChats();
      toast('Updates loaded & merged');
      logAct('Loaded updates and merged ' + newChats.length + ' chats');
    } else {
      toast('No new updates');
    }
  }catch(e){ toast('getUpdates failed: ' + e.message, false); console.error(e); throw e; }
}

// render chats (filter optional)
function renderChats(filter=''){
  const el = $('#chatList'); el.innerHTML='';
  const rows = Array.from(state.chats.values()).filter(c => (c.title||'').toLowerCase().includes(filter.toLowerCase()) || String(c.id).includes(filter));
  if(!rows.length){ el.innerHTML = '<div class="muted">Belum ada group/chan (dari getUpdates atau cache).</div>'; return; }
  for(const c of rows){
    const node = document.createElement('div'); node.className='list-item';
    node.innerHTML = `<div><div style="font-weight:600">${escapeHtml(c.title)}</div><div class="muted small">${escapeHtml(c.type)} · ${c.id}</div></div>
      <div style="display:flex;gap:8px;align-items:center">
        <button class="ghost" data-id="${c.id}">Select</button>
        <button data-manage="${c.id}">Manage</button>
      </div>`;
    el.appendChild(node);
    node.querySelector('[data-id]').addEventListener('click', ()=>{ $('#sendChatId').value = c.id; $('#quickChatId').value = c.id; setActiveTab('send'); logAct('Selected chat ' + c.id); });
    node.querySelector('[data-manage]').addEventListener('click', ()=>{ $('#groupId').value = c.id; setActiveTab('group'); loadAdmins(); });
  }
}

// sendMessage already wired in UI init - but helper here
// loadAdmins -> getChatAdministrators
async function loadAdmins(){
  const chat_id = $('#groupId').value.trim(); if(!chat_id){ toast('Masukkan group chat id', false); return; }
  try{
    const admins = await apiCall('getChatAdministrators', { chat_id });
    const box = $('#adminsBox'); box.innerHTML = '';
    for(const a of admins){
      const name = a.user.first_name || a.user.username || '';
      const id = a.user.id;
      const node = document.createElement('div'); node.className='list-item';
      node.innerHTML = `<div><div style="font-weight:600">${escapeHtml(name)}</div><div class="muted small">${escapeHtml(a.status)} · ${id}</div></div>
        <div style="display:flex;gap:8px">
          <button class="ghost dm" data-id="${id}">DM</button>
          <button class="ghost dem" data-id="${id}">Demote</button>
        </div>`;
      box.appendChild(node);
      node.querySelector('.dm').addEventListener('click', ()=>{ $('#sendChatId').value = id; setActiveTab('send'); });
      node.querySelector('.dem').addEventListener('click', ()=> confirmAction('demote', chat_id, id));
    }
    toast('Admins loaded');
    logAct('Loaded admins for ' + chat_id);
  }catch(e){ $('#adminsBox').textContent = 'Error: ' + e.message; toast('getChatAdministrators failed: ' + e.message,false); console.error(e); }
}

// confirm and do group actions
function confirmAction(action, chat_id, user_id){
  if(!chat_id || !user_id){ toast('Chat ID atau User ID kosong', false); return; }
  state.pendingAction = { action, chat_id, user_id };
  $('#confirmText').textContent = `Yakin ingin ${action} user ${user_id} di chat ${chat_id}?`;
  $('#confirm').classList.add('show');
}

async function doGroupAction(action, chat_id, user_id){
  try{
    if(action === 'ban' || action === 'kick'){
      await apiCall('banChatMember', { chat_id, user_id });
      toast('User banned');
      logAct(`ban ${user_id} @ ${chat_id}`);
    } else if(action === 'unban'){
      await apiCall('unbanChatMember', { chat_id, user_id });
      toast('User unbanned');
      logAct(`unban ${user_id} @ ${chat_id}`);
    } else if(action === 'promote'){
      const rights = {
        can_change_info: !!$('#r_change_info').checked,
        can_delete_messages: !!$('#r_delete_msgs').checked,
        can_invite_users: !!$('#r_invite').checked,
        can_restrict_members: !!$('#r_restrict').checked,
        can_promote_members: !!$('#r_promote').checked,
        can_pin_messages: !!$('#r_pin').checked,
        can_manage_topics: !!$('#r_topics').checked
      };
      await apiCall('promoteChatMember', Object.assign({ chat_id, user_id }, rights));
      toast('User promoted');
      logAct(`promote ${user_id} @ ${chat_id}`);
    } else if(action === 'demote'){
      const rightsFalse = { can_change_info:false, can_delete_messages:false, can_invite_users:false, can_restrict_members:false, can_promote_members:false, can_pin_messages:false, can_manage_topics:false };
      await apiCall('promoteChatMember', Object.assign({ chat_id, user_id }, rightsFalse));
      toast('User demoted');
      logAct(`demote ${user_id} @ ${chat_id}`);
    }
  }catch(e){
    toast(action + ' failed: ' + e.message, false);
    console.error(e);
  }
}

// helper for prompt+confirm (for actions launched from Group UI)
function promptAndConfirm(action){
  const chat_id = $('#groupId').value.trim();
  let user_id = $('#targetUser').value.trim();
  if(!user_id) user_id = prompt('Masukkan user ID:');
  if(!chat_id || !user_id) return toast('Chat ID atau User ID kosong', false);
  state.pendingAction = { action, chat_id, user_id };
  $('#confirmText').textContent = `Yakin ingin ${action} user ${user_id} di chat ${chat_id}?`;
  $('#confirm').classList.add('show');
}

// utility to set active tab
function setActiveTab(name){
  $$('.tab').forEach(t=>t.classList.toggle('tab-active', t.dataset.tab===name));
  ['home','send','edit','group'].forEach(t=>$('#tab-'+t).style.display = (t===name ? 'block' : 'none'));
}

// merge chats helper (already defined earlier)
function escapeHtml(s){ if(s==null) return ''; return String(s).replace(/[&<>"']/g, c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])); }

// render chats based on state.chats
function renderChats(filter=''){
  const el = $('#chatList'); el.innerHTML='';
  const rows = Array.from(state.chats.values()).filter(c => (c.title||'').toLowerCase().includes(filter.toLowerCase()) || String(c.id).includes(filter));
  if(!rows.length){ el.innerHTML = '<div class="muted">Belum ada group/chan (dari getUpdates atau cache).</div>'; return; }
  for(const c of rows){
    const node = document.createElement('div'); node.className='list-item';
    node.innerHTML = `<div><div style="font-weight:600">${escapeHtml(c.title)}</div><div class="muted small">${escapeHtml(c.type)} · ${c.id}</div></div>
      <div style="display:flex;gap:8px;align-items:center">
        <button class="ghost" data-id="${c.id}">Select</button>
        <button data-manage="${c.id}">Manage</button>
      </div>`;
    el.appendChild(node);
    node.querySelector('[data-id]').addEventListener('click', ()=>{ $('#sendChatId').value = c.id; $('#quickChatId').value = c.id; setActiveTab('send'); logAct('Selected chat ' + c.id); });
    node.querySelector('[data-manage]').addEventListener('click', ()=>{ $('#groupId').value = c.id; setActiveTab('group'); loadAdmins(); });
  }
}

// load chats from storage on start
(function boot(){ loadChatsFromStorage(); renderChats(); })();

</script>
</body>
</html>
