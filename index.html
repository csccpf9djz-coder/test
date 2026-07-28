<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>18TRIP 聖地巡禮</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700&family=Shippori+Mincho:wght@400;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.css"/>
<script src="https://cdn.jsdelivr.net/npm/leaflet@1.9.4/dist/leaflet.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#f5f1ea;--bg2:#faf7f2;--bg3:#ece7df;
  --line:#e0d8cc;--line2:#cec6b8;
  --tx:#241e16;--tx2:#685e50;--tx3:#a0907e;
  --ac:#5c7a6e;--red:#b04040;--gold:#a0845c;
  --c朝班:#6292C1;--c昼班:#fbd756;--c夕班:#e48157;--c夜班:#6b5a97;--cペア:#c8a870;--cHAMA:#a0845c;
}
body{background:var(--bg);font-family:'Noto Sans TC',sans-serif;font-size:14px;color:var(--tx);min-height:100vh}
button,input,textarea,select{font-family:'Noto Sans TC',sans-serif}
a{color:var(--ac);text-decoration:none}
a:hover{text-decoration:underline}

/* ── HEADER ── */
.hdr{background:var(--bg2);border-bottom:1px solid var(--line);padding:16px 16px 0}
.hdr-inner{max-width:900px;margin:0 auto;display:flex;align-items:flex-start;justify-content:center;position:relative;padding-bottom:14px;text-align:center}
.hdr-title{font-family:'Shippori Mincho',serif;font-size:24px;font-weight:700;background:linear-gradient(135deg,#5c7a6e,#a0845c);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.hdr-sub{font-size:11px;color:var(--tx3);letter-spacing:.06em;margin-top:3px}
.lock-btn{display:flex;align-items:center;gap:5px;background:none;border:0.5px solid var(--line2);color:var(--tx3);font-size:11px;padding:5px 11px;border-radius:14px;cursor:pointer;flex-shrink:0;margin-top:2px;position:absolute;right:0;top:0}
.lock-btn:hover{background:var(--bg3)}
.lock-dot{width:7px;height:7px;border-radius:50%;background:var(--tx3);flex-shrink:0}
.lock-dot.on{background:#5aaa5a}

/* ── NAV ── */
.nav{display:flex;background:var(--bg2);border-bottom:1px solid var(--line);overflow-x:auto;scrollbar-width:none}
.nav::-webkit-scrollbar{display:none}
.nav-btn{flex:1;min-width:58px;padding:11px 4px;font-size:12px;border:none;background:none;color:var(--tx3);cursor:pointer;border-bottom:2px solid transparent;transition:color .15s,border-color .15s;white-space:nowrap;letter-spacing:.02em}
.nav-btn.on{font-weight:500;border-bottom-color:currentColor}
.nav-btn[data-t="朝班"].on{color:var(--c朝班)}
.nav-btn[data-t="昼班"].on{color:var(--c昼班)}
.nav-btn[data-t="夕班"].on{color:var(--c夕班)}
.nav-btn[data-t="夜班"].on{color:var(--c夜班)}
.nav-btn[data-t="ペア"].on{color:var(--cペア)}
.nav-btn[data-t="HAMA"].on{color:var(--cHAMA)}
.nav-btn[data-t="全部"].on{color:var(--ac)}

/* ── MAP ── */
#map-wrap{height:260px;position:relative;border-bottom:1px solid var(--line)}
#main-map{height:100%;width:100%}
.map-overlay{position:absolute;top:10px;left:0;right:0;display:flex;justify-content:center;z-index:999;padding:0 12px;pointer-events:none}
.map-search-row{display:flex;gap:6px;width:100%;max-width:500px;background:white;border-radius:10px;padding:6px 8px;box-shadow:0 2px 12px rgba(0,0,0,.18);pointer-events:all}
.map-s-inp{flex:1;border:none;outline:none;font-size:13px;color:var(--tx);background:transparent}
.map-s-inp::placeholder{color:var(--tx3)}
.map-s-btn{background:var(--ac);color:white;border:none;border-radius:7px;padding:5px 12px;font-size:12px;cursor:pointer;white-space:nowrap}
.map-s-btn:hover{background:#4a6a5e}
.leaflet-container{background:#e6e0d4 !important}

/* ── READONLY BAR ── */
.ro-bar{background:rgba(160,132,92,.08);border-bottom:0.5px solid rgba(160,132,92,.25);padding:6px 16px;font-size:12px;color:var(--gold);text-align:center;display:none}
.ro-bar.show{display:block}

/* ── LIST ── */
.page{max-width:900px;margin:0 auto;padding:18px 14px 70px}
.list-hd{display:flex;align-items:center;justify-content:space-between;margin-bottom:14px}
.list-ttl{font-family:'Shippori Mincho',serif;font-size:14px;color:var(--tx2)}
.btn-sm{display:inline-flex;align-items:center;gap:4px;background:transparent;border:0.5px solid var(--line2);color:var(--tx2);font-size:12px;padding:5px 12px;border-radius:18px;cursor:pointer;transition:background .15s}
.btn-sm:hover{background:var(--bg3)}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));gap:9px}
.ecard{background:var(--bg2);border:0.5px solid var(--line);border-radius:12px;overflow:hidden;cursor:pointer;transition:transform .18s,box-shadow .18s,border-color .18s;position:relative}
.ecard:hover{transform:translateY(-2px);box-shadow:0 4px 14px rgba(36,30,22,.07);border-color:var(--line2)}
.ecard-bar{height:3px}
.ecard-body{padding:11px 13px 10px}
.ecard-cat{font-size:10px;color:var(--tx3);margin-bottom:3px;font-family:'DM Mono',monospace}
.ecard-name{font-family:'Shippori Mincho',serif;font-size:16px;font-weight:700;margin-bottom:2px;line-height:1.3}
.ecard-story{font-size:11px;color:var(--tx2);white-space:nowrap;overflow:hidden;text-overflow:ellipsis;margin-bottom:6px}
.ecard-cnt{font-size:11px;color:var(--tx3)}
.ecard-tags{display:flex;gap:3px;flex-wrap:wrap;margin-top:5px}
.ecard-tag{font-size:10px;background:var(--bg3);color:var(--tx3);padding:1px 6px;border-radius:6px;border:0.5px solid var(--line)}
.ecard-acts{position:absolute;top:7px;right:7px;display:flex;gap:3px;opacity:0;transition:opacity .15s}
.ecard:hover .ecard-acts{opacity:1}
.ico{background:var(--bg2);border:0.5px solid var(--line);color:var(--tx3);font-size:11px;padding:2px 6px;border-radius:5px;cursor:pointer;line-height:1.4}
.ico:hover{color:var(--tx)}
.ico.del:hover{color:var(--red);border-color:var(--red)}

/* ── DETAIL ── */
.detail-pg{display:none;max-width:900px;margin:0 auto;padding:18px 14px 80px}
.detail-pg.show{display:block}
.back-btn{background:none;border:none;color:var(--tx3);font-size:13px;cursor:pointer;padding:0;margin-bottom:16px;display:flex;align-items:center;gap:5px}
.back-btn:hover{color:var(--tx)}
.dhero{background:var(--bg2);border:0.5px solid var(--line);border-radius:12px;overflow:hidden;margin-bottom:14px}
.dhero-bar{height:4px}
.dhero-body{padding:18px 20px 15px}
.dcat{font-size:10px;color:var(--tx3);font-family:'DM Mono',monospace;letter-spacing:.1em;margin-bottom:5px}
.dname{font-family:'Shippori Mincho',serif;font-size:24px;font-weight:700;line-height:1.2}
.dstory{font-size:13px;color:var(--tx2);margin-top:4px}

/* detail map */
.dmap{height:200px;border-radius:10px;overflow:hidden;border:0.5px solid var(--line);margin-bottom:14px;position:relative}
#detail-map{height:100%;width:100%}

/* cat tabs */
.ctabs{display:flex;gap:5px;margin-bottom:14px;flex-wrap:wrap}
.ctab{padding:5px 14px;border-radius:18px;font-size:12px;border:0.5px solid var(--line2);background:transparent;color:var(--tx3);cursor:pointer;transition:all .15s}
.ctab.on{background:var(--tx);color:var(--bg2);border-color:var(--tx)}

/* section */
.sec-blk{margin-bottom:22px}
.sec-ttl{font-family:'Shippori Mincho',serif;font-size:14px;color:var(--tx);margin-bottom:9px;display:flex;align-items:center;gap:7px}
.sec-ttl::before{content:'';display:inline-block;width:3px;height:13px;border-radius:2px;background:var(--ac)}
.spots{display:flex;flex-direction:column;gap:9px}

/* ── SPOT CARD ── */
.sc{background:var(--bg2);border:0.5px solid var(--line);border-radius:10px;overflow:hidden}
.sc-head{padding:12px 14px 8px;display:flex;align-items:flex-start;gap:8px}
.sc-name-wrap{flex:1;min-width:0}
.sc-name{font-family:'Shippori Mincho',serif;font-size:19px;font-weight:700;border:none;background:none;color:var(--tx);width:100%;padding:2px 4px;border-radius:4px;line-height:1.3}
.sc-name:focus{outline:none;background:var(--bg3)}
.sc-name[readonly]{pointer-events:none}
.sc-maybe{font-size:10px;background:rgba(160,132,92,.1);color:#806440;border:0.5px solid rgba(160,132,92,.28);padding:2px 7px;border-radius:8px;display:inline-block;margin-top:3px}
.sc-acts{display:flex;gap:4px;flex-shrink:0}
.sc-maybe-btn{font-size:11px;padding:3px 7px;border-radius:9px;border:0.5px solid var(--line2);background:transparent;color:var(--tx3);cursor:pointer;transition:all .15s;white-space:nowrap}
.sc-maybe-btn.on{background:rgba(160,132,92,.1);color:#806440;border-color:rgba(160,132,92,.3)}

/* images — 2 col with padding */
.sc-imgs{display:grid;grid-template-columns:repeat(2,1fr);gap:6px;padding:0 12px 10px}
.sc-img-wrap{position:relative;border-radius:8px;overflow:hidden}
.sc-img{width:100%;aspect-ratio:3/2;object-fit:cover;display:block;cursor:pointer}
.sc-img-del{position:absolute;top:5px;right:5px;background:rgba(0,0,0,.55);color:white;border:none;border-radius:50%;width:22px;height:22px;font-size:13px;cursor:pointer;display:flex;align-items:center;justify-content:center;opacity:0;transition:opacity .15s}
.sc-img-wrap:hover .sc-img-del{opacity:1}
.sc-img-add{aspect-ratio:3/2;background:var(--bg3);border:0.5px dashed var(--line2);border-radius:8px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:4px;cursor:pointer;transition:background .15s}
.sc-img-add:hover{background:var(--bg2)}
.sc-img-add-icon{font-size:20px;opacity:.3}
.sc-img-add-lbl{font-size:10px;color:var(--tx3)}

/* spot meta */
.sc-meta{padding:0 14px 12px;display:flex;flex-direction:column;gap:7px}

/* combined map/url input */
.map-combo{display:flex;flex-direction:column;gap:5px}
.map-combo-inp{width:100%;background:var(--bg3);border:0.5px solid var(--line);border-radius:7px;padding:7px 10px;font-size:12px;color:var(--tx)}
.map-combo-inp:focus{outline:none;border-color:var(--ac)}
.map-combo-inp::placeholder{color:var(--tx3)}
.map-combo-drop{background:var(--bg2);border:0.5px solid var(--line2);border-radius:8px;overflow:hidden;display:none;max-height:200px;overflow-y:auto;box-shadow:0 4px 14px rgba(36,30,22,.12)}
.map-combo-drop.open{display:block}
.mcd-item{padding:8px 11px;cursor:pointer;font-size:12px;color:var(--tx2);border-bottom:0.5px solid var(--line)}
.mcd-item:last-child{border-bottom:none}
.mcd-item:hover{background:var(--bg3)}
.mcd-item b{color:var(--tx);display:block;font-weight:500}
.mcd-item small{color:var(--tx3);font-size:10px}
.mcd-msg{padding:8px 11px;font-size:12px;color:var(--tx3);text-align:center}

/* bookmark */
.bm{display:flex;border:0.5px solid var(--line2);border-radius:8px;overflow:hidden;text-decoration:none;color:inherit;background:var(--bg2);transition:border-color .15s}
.bm:hover{border-color:var(--ac)}
.bm-ico{width:42px;flex-shrink:0;background:var(--bg3);display:flex;align-items:center;justify-content:center;font-size:16px}
.bm-body{flex:1;min-width:0;padding:7px 10px}
.bm-title{font-size:12px;font-weight:500;color:var(--tx);white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.bm-url{font-size:10px;color:var(--tx3);white-space:nowrap;overflow:hidden;text-overflow:ellipsis;font-family:'DM Mono',monospace;margin-top:1px}
.bm-del{background:none;border:none;color:var(--tx3);padding:0 10px;cursor:pointer;font-size:14px}
.bm-del:hover{color:var(--red)}
.pin-ok{font-size:11px;color:var(--ac);display:flex;align-items:center;gap:5px}
.pin-ok button{background:none;border:none;color:var(--tx3);font-size:11px;cursor:pointer;text-decoration:underline;padding:0}

/* source */
.source-row{font-size:11px;color:var(--tx3);display:flex;align-items:center;gap:5px;flex-wrap:wrap}
.source-row a{color:var(--ac);word-break:break-all}

/* tags */
.tags-row{display:flex;gap:4px;flex-wrap:wrap;align-items:center;min-height:26px}
.tag{font-size:11px;background:var(--bg3);color:var(--tx3);padding:2px 8px;border-radius:9px;border:0.5px solid var(--line);cursor:pointer;display:inline-flex;align-items:center;gap:3px}
.tag:hover{border-color:var(--ac);color:var(--ac)}
.tag-del{font-size:12px;line-height:1;opacity:.5;background:none;border:none;cursor:pointer;padding:0;color:inherit}
.tag-del:hover{opacity:1;color:var(--red)}
.tag-inp{background:none;border:none;font-size:11px;color:var(--tx2);outline:none;min-width:70px;padding:2px 3px}
.tag-inp::placeholder{color:var(--tx3)}

/* notes */
.sc-notes{width:100%;background:none;border:none;color:var(--tx2);font-size:13px;line-height:1.7;resize:none;min-height:22px;overflow:hidden;padding:2px 4px;border-radius:4px}
.sc-notes:focus{outline:none;background:var(--bg3)}
.sc-notes::placeholder{color:var(--tx3)}
.sc-notes[readonly]{pointer-events:none}

/* add row */
.add-row{display:flex;gap:7px;margin-top:7px}
.add-inp{flex:1;background:var(--bg3);border:0.5px solid var(--line);border-radius:8px;padding:8px 11px;font-size:13px;color:var(--tx)}
.add-inp:focus{outline:none;border-color:var(--ac)}
.add-inp::placeholder{color:var(--tx3)}
.add-btn{background:var(--ac);color:white;border:none;border-radius:8px;padding:8px 13px;font-size:13px;cursor:pointer;white-space:nowrap}
.add-btn:hover{background:#4a6a5e}

/* ── MODAL ── */
.ov{display:none;position:fixed;inset:0;background:rgba(36,30,22,.45);z-index:500;align-items:center;justify-content:center;padding:16px}
.ov.open{display:flex}
.modal{background:var(--bg2);border:0.5px solid var(--line2);border-radius:14px;width:100%;max-width:440px;padding:22px;position:relative;max-height:90vh;overflow-y:auto}
.modal-ttl{font-family:'Shippori Mincho',serif;font-size:17px;margin-bottom:15px;color:var(--tx)}
.modal-x{position:absolute;top:15px;right:15px;background:var(--bg3);border:0.5px solid var(--line);color:var(--tx3);width:26px;height:26px;border-radius:50%;cursor:pointer;font-size:13px;display:flex;align-items:center;justify-content:center}
.modal-x:hover{color:var(--tx)}
.fg{margin-bottom:12px}
.fl{display:block;font-size:10px;letter-spacing:.08em;text-transform:uppercase;color:var(--tx3);margin-bottom:4px}
.fi{width:100%;background:var(--bg3);border:0.5px solid var(--line2);border-radius:8px;padding:8px 10px;font-size:13px;color:var(--tx)}
.fi:focus{outline:none;border-color:var(--ac)}
.fi::placeholder{color:var(--tx3)}
select.fi option{background:var(--bg3)}
.mfoot{display:flex;gap:7px;justify-content:flex-end;margin-top:14px}
.btn-p{background:var(--ac);color:white;border:none;border-radius:8px;padding:8px 17px;font-size:13px;cursor:pointer}
.btn-p:hover{background:#4a6a5e}
.btn-g{background:transparent;border:0.5px solid var(--line2);color:var(--tx3);border-radius:8px;padding:8px 17px;font-size:13px;cursor:pointer}
.btn-g:hover{color:var(--tx)}

/* cat manage */
.cat-list{display:flex;flex-direction:column;gap:6px;margin-bottom:10px}
.cat-item{display:flex;align-items:center;gap:7px;font-size:13px;color:var(--tx2)}
.cat-item button{background:none;border:none;color:var(--tx3);cursor:pointer;font-size:13px;padding:0}
.cat-item button:hover{color:var(--red)}

/* img big */
.img-big{max-width:100%;max-height:75vh;border-radius:8px;display:block;margin:0 auto}

/* toast */
.toast{position:fixed;bottom:20px;left:50%;transform:translateX(-50%) translateY(12px);background:var(--tx);color:var(--bg2);font-size:12px;padding:6px 16px;border-radius:18px;opacity:0;transition:all .25s;z-index:999;pointer-events:none}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0)}
.file-inp{display:none}

::-webkit-scrollbar{width:4px}::-webkit-scrollbar-track{background:var(--bg3)}::-webkit-scrollbar-thumb{background:var(--line2);border-radius:2px}
</style>
</head>
<body>

<div class="ro-bar" id="ro-bar">👁 閱覽模式 — 右上角按鈕切換編輯</div>
<header class="hdr">
  <div class="hdr-inner">
    <div>
      <div class="hdr-title">18TRIP 聖地巡禮</div>
      <div class="hdr-sub">⚠ 有誤請見諒</div>
    </div>
    <button class="lock-btn" id="lock-btn" onclick="toggleLock()">
      <span class="lock-dot" id="lock-dot"></span>
      <span id="lock-lbl">閱覽</span>
    </button>
  </div>
</header>

<nav class="nav" id="nav">
  <button class="nav-btn on" data-t="全部" onclick="switchTab('全部')">全部</button>
  <button class="nav-btn" data-t="朝班" onclick="switchTab('朝班')">朝班</button>
  <button class="nav-btn" data-t="昼班" onclick="switchTab('昼班')">昼班</button>
  <button class="nav-btn" data-t="夕班" onclick="switchTab('夕班')">夕班</button>
  <button class="nav-btn" data-t="夜班" onclick="switchTab('夜班')">夜班</button>
  <button class="nav-btn" data-t="ペア" onclick="switchTab('ペア')">ペア</button>
  <button class="nav-btn" data-t="HAMA" onclick="switchTab('HAMA')">HAMA</button>
</nav>

<div id="map-wrap">
  <div id="main-map"></div>
  <div class="map-overlay">
    <div class="map-search-row">
      <input class="map-s-inp" id="map-s-inp" type="text" placeholder="輸入地名搜尋地圖（例：別府公園、大分縣）" onkeydown="if(event.key==='Enter')doMapSearch()">
      <button class="map-s-btn" onclick="doMapSearch()">搜尋</button>
    </div>
  </div>
</div>

<div id="list-pg" class="page">
  <div class="list-hd">
    <div class="list-ttl" id="list-ttl">所有聖地</div>
    <button class="btn-sm" id="btn-add-e" onclick="openAddE()" style="display:none">＋ 新增</button>
  </div>
  <div class="grid" id="grid"></div>
</div>

<div class="detail-pg" id="dp">
  <button class="back-btn" id="back-btn" onclick="backToList()">← 返回列表</button>
  <div id="di"></div>
</div>

<!-- Entry modal -->
<div class="ov" id="em">
  <div class="modal">
    <button class="modal-x" onclick="closeOv('em')">✕</button>
    <div class="modal-ttl" id="em-ttl"></div>
    <div id="em-body"></div>
  </div>
</div>

<!-- Category manage modal -->
<div class="ov" id="cat-modal">
  <div class="modal">
    <button class="modal-x" onclick="closeOv('cat-modal')">✕</button>
    <div class="modal-ttl">管理分類</div>
    <div id="cat-modal-body"></div>
  </div>
</div>

<!-- Password modal -->
<div class="ov" id="pw-modal">
  <div class="modal" style="max-width:320px">
    <button class="modal-x" onclick="closeOv('pw-modal')">✕</button>
    <div class="modal-ttl">🔑 編輯模式</div>
    <div class="fg">
      <label class="fl">密碼</label>
      <input class="fi" id="pw-inp" type="password" placeholder="輸入密碼" onkeydown="if(event.key==='Enter')checkPw()">
    </div>
    <div id="pw-err" style="font-size:12px;color:var(--red);margin-top:-6px;margin-bottom:8px;display:none">密碼錯誤</div>
    <div class="mfoot">
      <button class="btn-g" onclick="closeOv('pw-modal')">取消</button>
      <button class="btn-p" onclick="checkPw()">解鎖</button>
    </div>
  </div>
</div>

<!-- Image viewer -->
<div class="ov" id="iv">
  <div class="modal" style="max-width:760px;padding:8px;background:#181410">
    <button class="modal-x" onclick="closeOv('iv')" style="background:rgba(255,255,255,.1);border-color:rgba(255,255,255,.15);color:#ccc">✕</button>
    <img class="img-big" id="iv-img" src="" alt="">
  </div>
</div>

<div class="toast" id="toast">已儲存 ✓</div>
<input type="file" class="file-inp" id="fi" accept="image/*" multiple>

<script>
// ── 密碼 ──
var EDIT_PW = '18trip';
var isEd = false;
function toggleLock() {
  if (isEd) { isEd = false; syncLockUI(); refresh(); return; }
  document.getElementById('pw-inp').value = '';
  document.getElementById('pw-err').style.display = 'none';
  openOv('pw-modal');
  setTimeout(function(){ document.getElementById('pw-inp').focus(); }, 120);
}
function checkPw() {
  if (document.getElementById('pw-inp').value === EDIT_PW) {
    isEd = true; closeOv('pw-modal'); syncLockUI(); refresh();
  } else {
    document.getElementById('pw-err').style.display = 'block';
    document.getElementById('pw-inp').value = '';
    document.getElementById('pw-inp').focus();
  }
}
function syncLockUI() {
  document.getElementById('lock-dot').classList.toggle('on', isEd);
  document.getElementById('lock-lbl').textContent = isEd ? '編輯中' : '閱覽';
  document.getElementById('ro-bar').classList.toggle('show', !isEd);
  document.getElementById('btn-add-e').style.display = isEd ? '' : 'none';
}
function refresh() { if (curId) renderDetail(); else renderList(); }

// ── 顏色 ──
var CAT_COLOR = {'朝班':'#6292C1','昼班':'#fbd756','夕班':'#e48157','夜班':'#6b5a97','ペア':'#c8a870','HAMA':'#a0845c'};

// ── 資料 ──
function mkItem(n){ return {id:uid(),name:n,notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:[],source:''}; }
function mkSec(id,title,cat){ return {id:id,title:title,cat:cat,items:[]}; }
function mkEntry(id,cat,loc,story){
  return {id:id,cat:cat,location:loc,story:story,sections:[mkSec(id+'_0','景點','景點'),mkSec(id+'_1','美食','美食'),mkSec(id+'_2','其他','其他')]};
}

var DEF = [
  mkEntry('a1','朝班','兵庫','main story'),
  mkEntry('a2','朝班','長野','お前と往くVoyage'),
  mkEntry('a3','朝班','福岡','Glow in the dirty Rain'),
  mkEntry('a4','朝班','島根','痕跡－夢幻は宿縁となりて－'),
  mkEntry('h1','昼班','香川','main story'),
  mkEntry('h2','昼班','石川','極彩色イマジネヰション'),
  mkEntry('h3','昼班','鹿児島','リセット≠アストロノーツ'),
  mkEntry('h4','昼班','福井','ニュー・シネマ・ダイナソーズ'),
  // 大分（已有景點資料）
  {id:'y1',cat:'夕班',location:'大分',story:'main story',sections:[
    {id:'y1_0',title:'景點',cat:'景點',items:[
      {id:'i1',name:'湯煙展望台',notes:'別府湯煙全景',mapUrl:'https://maps.app.goo.gl/mqE8ssZNYjtde9f1A',lat:33.284,lng:131.499,maybe:false,images:[],tags:['展望台'],source:''},
      {id:'i2',name:'海地獄',notes:'',mapUrl:'https://maps.app.goo.gl/qgiSndStJj5fqBsi8',lat:33.287,lng:131.497,maybe:false,images:[],tags:['地獄'],source:''},
      {id:'i3',name:'血の地獄',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:['地獄'],source:''},
      {id:'i4',name:'別府公園',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:[],source:''},
      {id:'i5',name:'別府タワー',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:[],source:''},
      {id:'i6',name:'北浜公園',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:[],source:''},
      {id:'i7',name:'別府溫泉旅館',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:['住宿'],source:''}
    ]},
    {id:'y1_1',title:'美食',cat:'美食',items:[
      {id:'i8',name:'地獄蒸し食堂',notes:'豐後雞・地獄蒸布丁',mapUrl:'https://maps.app.goo.gl/DKxB1oKZ3LiRM6YY6',lat:33.287,lng:131.497,maybe:true,images:[],tags:['美食'],source:''},
      {id:'i9',name:'別府冷麵',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:['美食'],source:''},
      {id:'i10',name:'カボスアイス',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:[],source:''}
    ]},
    {id:'y1_2',title:'其他',cat:'其他',items:[
      {id:'i11',name:'別府塔打卡板',notes:'週年卡面',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:['周邊'],source:''},
      {id:'i12',name:'地獄T',notes:'紀念品商店有賣',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:['周邊'],source:''},
      {id:'i13',name:'青鬼吉祥物',notes:'找不到青鬼QQ',mapUrl:'',lat:null,lng:null,maybe:true,images:[],tags:[],source:''}
    ]}
  ]},
  mkEntry('y2','夕班','鳥取','ココロの砂像'),
  mkEntry('y3','夕班','和歌山','ちぃ的PPC。'),
  mkEntry('n1','夜班','北海道','main story'),
  mkEntry('n2','夜班','青森','アポトーシスへの誘惑'),
  mkEntry('n3','夜班','山梨','静かの海にたゆたう'),
  mkEntry('p1','ペア','蒙古','遊牧民のジャーニー'),
  mkEntry('p2','ペア','新加坡','クラスメイツ・リスタート'),
  mkEntry('p3','ペア','愛沙尼亞','TOXIC X NEIGHBOR'),
  mkEntry('p4','ペア','荷蘭','ギャル友珍道中'),
  mkEntry('p5','ペア','英國','愛と憎悪わ人間味'),
  mkEntry('p6','ペア','芬蘭','雪解けのギフト'),
  mkEntry('p7','ペア','美國','ゲーマーズ．デイラ'),
  {id:'p8',cat:'ペア',location:'澳大利亞',story:'Wild Friends Discovery',sections:[
    {id:'p8_0',title:'景點',cat:'景點',items:[
      {id:'pi1',name:'アドミラルズアーチ',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:[],source:''},
      {id:'pi2',name:'自然動物保護區',notes:'',mapUrl:'',lat:null,lng:null,maybe:false,images:[],tags:[],source:''}
    ]},
    {id:'p8_1',title:'美食',cat:'美食',items:[]},
    {id:'p8_2',title:'其他',cat:'其他',items:[]}
  ]},
  {id:'hm1',cat:'HAMA',location:'HAMA周遭',story:'',sections:[
    {id:'hm1_0',title:'景點',cat:'景點',items:[
      {id:'hmi1',name:'横浜ベイブリッジスカイウォーク',notes:'大黒可不可 常駐SSR',mapUrl:'https://maps.app.goo.gl/Hcnz7fGd5dts4gtx6',lat:35.471,lng:139.651,maybe:false,images:[],tags:['横浜'],source:'https://www.yokohama-kowan.co.jp/'}
    ]},
    {id:'hm1_1',title:'美食',cat:'美食',items:[]},
    {id:'hm1_2',title:'其他',cat:'其他',items:[
      {id:'hmi2',name:'あかいくつバス',notes:'大黒可不可 BD SSR',mapUrl:'https://www.welcome.city.yokohama.jp/transit/akaikutsu/',lat:35.445,lng:139.638,maybe:false,images:[],tags:['横浜','交通'],source:'https://www.welcome.city.yokohama.jp/transit/akaikutsu/'}
    ]}
  ]}
];

// 分類清單（可動態增減，也儲存在 localStorage）
var CATS_LIST = ['朝班','昼班','夕班','夜班','ペア','HAMA'];
var STORAGE_KEY = '18trip_v9';
var CATS_KEY = '18trip_cats_v9';

var db;
try {
  var _raw = localStorage.getItem(STORAGE_KEY);
  db = _raw ? JSON.parse(_raw) : null;
  if (!Array.isArray(db) || !db.length) throw 0;
} catch(e) { db = JSON.parse(JSON.stringify(DEF)); }

// 載入已儲存的分類清單
try {
  var _craw = localStorage.getItem(CATS_KEY);
  if (_craw) CATS_LIST = JSON.parse(_craw);
} catch(e) {}

// 確保欄位完整（舊資料相容）
db.forEach(function(e){
  if (!e.cat && e.band) e.cat = e.band;
  e.sections.forEach(function(s){
    s.items.forEach(function(it){
      if (it.lat===undefined) it.lat=null;
      if (it.lng===undefined) it.lng=null;
      if (!it.tags) it.tags=[];
      if (it.source===undefined) it.source='';
      if (!it.images) it.images=[];
    });
  });
});

// 從資料補齊 CATS_LIST
db.forEach(function(e){ if (e.cat && CATS_LIST.indexOf(e.cat)<0) CATS_LIST.push(e.cat); });

function uid(){ return 'x'+Date.now().toString(36)+Math.random().toString(36).slice(2,5); }
function save(){
  try {
    localStorage.setItem(STORAGE_KEY, JSON.stringify(db));
    localStorage.setItem(CATS_KEY, JSON.stringify(CATS_LIST));
  } catch(e) { alert('儲存失敗：localStorage 空間不足，圖片太多可能造成此問題'); return; }
  var t=document.getElementById('toast'); t.classList.add('show');
  setTimeout(function(){ t.classList.remove('show'); }, 1400);
}
function esc(s){ return (s||'').replace(/&/g,'&amp;').replace(/"/g,'&quot;').replace(/</g,'&lt;'); }
function fE(id){ for(var i=0;i<db.length;i++) if(db[i].id===id) return db[i]; return null; }
function fS(e,sid){ for(var i=0;i<e.sections.length;i++) if(e.sections[i].id===sid) return e.sections[i]; return null; }
function fI(e,iid){
  for(var i=0;i<e.sections.length;i++){
    var s=e.sections[i];
    for(var j=0;j<s.items.length;j++) if(s.items[j].id===iid) return {it:s.items[j],sec:s};
  }
  return null;
}
function getColor(cat){ return CAT_COLOR[cat]||'#a0845c'; }

// ── Leaflet 地圖 ──
var mainMap = null, mainMarkers = [];
var detailMap = null, detailMarkers = [];
var CAT_LL = {
  '兵庫':[34.69,135.19],'長野':[36.65,138.18],'福岡':[33.59,130.40],'島根':[35.47,132.90],
  '香川':[34.34,134.04],'石川':[36.59,136.62],'鹿児島':[31.56,130.55],'福井':[36.06,136.22],
  '大分':[33.24,131.61],'鳥取':[35.50,134.23],'和歌山':[34.22,135.16],
  '北海道':[43.06,141.35],'青森':[40.82,140.74],'山梨':[35.66,138.56],
  '蒙古':[47.90,106.90],'新加坡':[1.35,103.82],'愛沙尼亞':[59.43,24.75],
  '荷蘭':[52.37,4.90],'英國':[51.50,-0.12],'芬蘭':[60.17,24.94],
  '美國':[37.77,-122.41],'澳大利亞':[-25.27,133.77],'HAMA周遭':[35.44,139.64]
};

function initMainMap(){
  if(mainMap) return;
  mainMap = L.map('main-map', {zoomControl:true});
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',{
    attribution:'© <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a>',
    maxZoom:18
  }).addTo(mainMap);
  mainMap.setView([36,136],4);
}

function mkPinIcon(color, label){
  return L.divIcon({
    className:'',
    iconSize:[30,30], iconAnchor:[15,15],
    html:'<div style="width:30px;height:30px;border-radius:50%;background:'+color+';border:2.5px solid white;box-shadow:0 2px 6px rgba(0,0,0,.3);display:flex;align-items:center;justify-content:center;font-size:10px;color:white;font-weight:700;cursor:pointer">'+label+'</div>'
  });
}

function renderMainMap(){
  if(!mainMap) return;
  mainMarkers.forEach(function(m){m.remove();});
  mainMarkers=[];
  var es = curTab==='全部' ? db : db.filter(function(d){return d.cat===curTab;});
  es.forEach(function(e){
    var ll = CAT_LL[e.location];
    if(!ll) return;
    var c = getColor(e.cat);
    var n = e.sections.reduce(function(a,s){return a+s.items.length;},0);
    var m = L.marker(ll, {icon: mkPinIcon(c, n||'·')}).addTo(mainMap);
    m.bindTooltip('<b>'+e.location+'</b><br>'+e.cat+(n?' · '+n+'件':''),{direction:'top',offset:[0,-16]});
    m.on('click', (function(eid){return function(){openDetail(eid);};})(e.id));
    mainMarkers.push(m);
  });
  if(mainMarkers.length===1){
    var fe=es.find(function(x){return CAT_LL[x.location];});
    if(fe) mainMap.setView(CAT_LL[fe.location],10);
  } else if(mainMarkers.length>1){
    try{mainMap.fitBounds(L.featureGroup(mainMarkers).getBounds().pad(0.3));}catch(x){}
  } else {
    mainMap.setView([36,136],4);
  }
}

function initDetailMap(e){
  if(detailMap){detailMap.remove();detailMap=null;}
  var el=document.getElementById('detail-map');
  if(!el) return;
  detailMap=L.map('detail-map',{zoomControl:true,attributionControl:false});
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',{maxZoom:18}).addTo(detailMap);
  var centre=CAT_LL[e.location]||[36,136];
  var c=getColor(e.cat);
  var dMks=[];
  e.sections.forEach(function(sec){
    sec.items.forEach(function(it){
      if(it.lat==null||it.lng==null) return;
      var icon=L.divIcon({
        className:'',iconSize:[null,null],iconAnchor:[0,10],
        html:'<div style="background:white;border:2px solid '+c+';border-radius:8px;padding:3px 9px;font-size:11px;white-space:nowrap;box-shadow:0 2px 5px rgba(0,0,0,.15);cursor:pointer;font-family:Noto Sans TC,sans-serif;max-width:150px;overflow:hidden;text-overflow:ellipsis">'+it.name+'</div>'
      });
      var mk=L.marker([it.lat,it.lng],{icon:icon}).addTo(detailMap);
      mk.on('click',(function(iid){
  return function(){
    var card=document.getElementById('sc-'+iid);
    if(card){
      card.scrollIntoView({behavior:'smooth',block:'center'});
      card.style.boxShadow='0 0 0 2px '+c+', 0 4px 14px rgba(0,0,0,.15)';
      setTimeout(function(){ card.style.boxShadow=''; },1800);
    }
  };
})(it.id));
      dMks.push(mk);
    });
  });
  if(dMks.length>0){
    try{detailMap.fitBounds(L.featureGroup(dMks).getBounds().pad(0.5));}catch(x){detailMap.setView(centre,12);}
  } else {
    detailMap.setView(centre,12);
  }
  setTimeout(function(){if(detailMap)detailMap.invalidateSize();},80);
}

// ── Nominatim（無 User-Agent header，直接 fetch）──
function nominatimSearch(q, onSuccess, onFail){
  var url='https://nominatim.openstreetmap.org/search?format=json&limit=5&accept-language=ja,zh-TW,en&q='+encodeURIComponent(q);
  fetch(url)
    .then(function(r){return r.json();})
    .then(onSuccess)
    .catch(function(err){if(onFail)onFail(err);});
}

// ── 地圖搜尋 ──
function doMapSearch(){
  var q=(document.getElementById('map-s-inp').value||'').trim();
  if(!q)return;
  nominatimSearch(q, function(data){
    if(!data||!data.length){alert('找不到此地點，請換個關鍵字試試');return;}
    var d=data[0];
    var lat=parseFloat(d.lat),lng=parseFloat(d.lon);
    if(mainMap){mainMap.setView([lat,lng],13);L.marker([lat,lng]).addTo(mainMap).bindPopup(d.display_name).openPopup();}
  }, function(){alert('搜尋失敗，請確認網路連線');});
}

// ── 地名搜尋（景點）──
var _stimer=null;
function onSpotLocInput(iid,sid){
  clearTimeout(_stimer);
  var inp=document.getElementById('sli-'+iid);
  var drop=document.getElementById('sld-'+iid);
  if(!inp||!drop)return;
  var q=(inp.value||'').trim();
  // If it's a URL, don't search
  if(q.indexOf('http')===0){drop.classList.remove('open');return;}
  if(q.length<2){drop.classList.remove('open');return;}
  drop.classList.add('open');
  drop.innerHTML='<div class="mcd-msg">搜尋中…</div>';
  _stimer=setTimeout(function(){
    nominatimSearch(q, function(data){
      var d2=document.getElementById('sld-'+iid);
      if(!d2)return;
      if(!data||!data.length){d2.innerHTML='<div class="mcd-msg">找不到，試試其他關鍵字</div>';return;}
      d2.innerHTML=data.map(function(x){
        var nm=x.name||x.display_name.split(',')[0];
        return '<div class="mcd-item" onclick="selectSpotLoc(\''+iid+'\',\''+sid+'\','+x.lat+','+x.lon+')"><b>'+nm+'</b><small>'+x.display_name+'</small></div>';
      }).join('');
    }, function(){
      var d3=document.getElementById('sld-'+iid);
      if(d3)d3.innerHTML='<div class="mcd-msg">搜尋失敗，請確認網路</div>';
    });
  },450);
}
function selectSpotLoc(iid,sid,lat,lng){
  lat=parseFloat(lat);lng=parseFloat(lng);
  var e=fE(curId),s=fS(e,sid),it=s&&s.items.filter(function(x){return x.id===iid;})[0];
  if(!it)return;
  it.lat=lat;it.lng=lng;
  // If no mapUrl, generate OSM link as placeholder
  if(!it.mapUrl) it.mapUrl='https://www.openstreetmap.org/?mlat='+lat+'&mlon='+lng+'#map=17/'+lat+'/'+lng;
  save();
  var d=document.getElementById('sld-'+iid);if(d)d.classList.remove('open');
  renderDetail();
}
function clearSpotPin(iid,sid){
  var e=fE(curId),s=fS(e,sid),it=s&&s.items.filter(function(x){return x.id===iid;})[0];
  if(!it)return;
  it.lat=null;it.lng=null;save();renderDetail();
}

// ── TAB ──
var curTab='全部';
function switchTab(t){
  curTab=t;
  document.querySelectorAll('.nav-btn').forEach(function(b){b.classList.toggle('on',b.dataset.t===t);});
  if(t==='HAMA'){var h=db.find(function(d){return d.cat==='HAMA';});if(h){openDetail(h.id);return;}}
  backToList();
}

// ── LIST ──
function vis(){
  return curTab==='全部' ? db.slice() : db.filter(function(d){return d.cat===curTab;});
}
function getAllTags(){
  var m={};
  db.forEach(function(e){e.sections.forEach(function(s){s.items.forEach(function(it){(it.tags||[]).forEach(function(t){if(t)m[t]=(m[t]||0)+1;});});});});
  return Object.keys(m).sort();
}

function renderList(){
  var es=vis();
  document.getElementById('list-ttl').textContent=curTab==='全部'?'所有聖地（'+db.length+'筆）':curTab+'（'+es.length+'筆）';
  renderMainMap();
  document.getElementById('grid').innerHTML=es.map(function(e){
    var c=getColor(e.cat);
    var n=e.sections.reduce(function(a,s){return a+s.items.length;},0);
    var tags=[];
    e.sections.forEach(function(s){s.items.forEach(function(it){(it.tags||[]).forEach(function(t){if(t&&tags.indexOf(t)<0)tags.push(t);});});});
    var tagH=tags.slice(0,3).map(function(t){return '<span class="ecard-tag">#'+t+'</span>';}).join('');
    var acts=isEd?'<div class="ecard-acts"><button class="ico" onclick="event.stopPropagation();openEditE(\''+e.id+'\')">編輯</button><button class="ico del" onclick="event.stopPropagation();delE(\''+e.id+'\')">✕</button></div>':'';
    return '<div class="ecard" onclick="openDetail(\''+e.id+'\')">'+
      '<div class="ecard-bar" style="background:'+c+'"></div>'+
      '<div class="ecard-body">'+
        '<div class="ecard-cat">'+e.cat+'</div>'+
        '<div class="ecard-name">'+e.location+'</div>'+
        '<div class="ecard-story">'+(e.story?'📖 '+e.story:'—')+'</div>'+
        '<div class="ecard-cnt">'+(n?'📍 '+n+' 個景點':'尚未登錄')+'</div>'+
        (tagH?'<div class="ecard-tags">'+tagH+'</div>':'')+
      '</div>'+acts+'</div>';
  }).join('')||'<div style="color:var(--tx3);padding:24px 0;font-size:13px">暫無資料</div>';
}

// ── DETAIL ──
var curId=null,curCat='全部',pendImg=null;
function openDetail(id){
  curId=id;curCat='全部';
  document.getElementById('list-pg').style.display='none';
  document.getElementById('map-wrap').style.display='none';
  document.getElementById('dp').classList.add('show');
  renderDetail();
}
function backToList(){
  if(detailMap){detailMap.remove();detailMap=null;}
  curId=null;
  if(curTab==='HAMA')curTab='全部';
  document.querySelectorAll('.nav-btn').forEach(function(b){b.classList.toggle('on',b.dataset.t===curTab);});
  document.getElementById('dp').classList.remove('show');
  document.getElementById('list-pg').style.display='';
  document.getElementById('map-wrap').style.display='';
  renderList();
  setTimeout(function(){if(mainMap)mainMap.invalidateSize();},80);
}
function setCat(c){curCat=c;renderDetail();}

function renderDetail(){
  var e=fE(curId);if(!e){backToList();return;}
  var color=getColor(e.cat);
  var secs=curCat==='全部'?e.sections:e.sections.filter(function(s){return s.cat===curCat;});
  var secsH=secs.map(function(sec){
    var items=sec.items.map(function(it){return spotHTML(it,sec.id);}).join('');
    var addRow=isEd?'<div class="add-row" style="margin-top:7px"><input class="add-inp" id="ni-'+sec.id+'" type="text" placeholder="＋ 輸入景點名稱 → Enter" onkeydown="if(event.key===\'Enter\'){event.preventDefault();addSpot(\''+sec.id+'\')}"><button class="add-btn" onclick="addSpot(\''+sec.id+'\')">新增</button></div>':'';
    return '<div class="sec-blk"><div class="sec-ttl">'+sec.title+'</div><div class="spots">'+items+'</div>'+addRow+'</div>';
  }).join('');

  var editBtn=isEd?'<div style="margin-top:10px;display:flex;gap:6px"><button class="ico" onclick="openEditE(\''+e.id+'\')" style="padding:4px 10px">編輯資訊</button><button class="ico" onclick="openCatManage(\''+e.id+'\')" style="padding:4px 10px">管理分類</button></div>':'';
  var allCats=['全部'].concat(e.sections.map(function(s){return s.cat;}));
  var uniq=[];allCats.forEach(function(c){if(uniq.indexOf(c)<0)uniq.push(c);});
  var tabsH=uniq.map(function(t){return '<button class="ctab'+(curCat===t?' on':'')+'" onclick="setCat(\''+t+'\')">'+t+'</button>';}).join('');

  document.getElementById('back-btn').textContent=e.cat==='HAMA'?'← 返回全部':'← 返回列表';
  document.getElementById('di').innerHTML=
    '<div class="dhero"><div class="dhero-bar" style="background:'+color+'"></div><div class="dhero-body">'+
    '<div class="dcat">'+e.cat+'</div><div class="dname">'+e.location+'</div>'+
    (e.story?'<div class="dstory">📖 '+e.story+'</div>':'')+editBtn+'</div></div>'+
    '<div class="dmap"><div id="detail-map"></div></div>'+
    '<div class="ctabs">'+tabsH+'</div>'+secsH;

  initDetailMap(e);
}

function spotHTML(it,sid){
  var imgs=(it.images||[]).map(function(img,idx){
    var delBtn=isEd?'<button class="sc-img-del" onclick="delImg(\''+it.id+'\','+idx+')" title="刪除圖片">✕</button>':'';
    return '<div class="sc-img-wrap"><img class="sc-img" src="'+img+'" onclick="viewImg(\''+img+'\')" alt="">'+delBtn+'</div>';
  }).join('');
  var imgAdd=isEd?'<div class="sc-img-add" onclick="trigImg(\''+it.id+'\')"><span class="sc-img-add-icon">＋</span><span class="sc-img-add-lbl">新增圖片</span></div>':'';

  // Combined location / URL section
  var locH='';
  var hasPinned=it.lat!=null&&it.lng!=null;
  if(isEd){
    var bmH=it.mapUrl?'<a class="bm" href="'+esc(it.mapUrl)+'" target="_blank" rel="noopener"><div class="bm-ico">📍</div><div class="bm-body"><div class="bm-title">'+esc(it.name)+' — 地圖</div><div class="bm-url">'+esc(it.mapUrl)+'</div></div><button class="bm-del" onclick="event.preventDefault();event.stopPropagation();setItField(\''+sid+'\',\''+it.id+'\',\'mapUrl\',\'\')">✕</button></a>':'';
    var pinH=hasPinned?'<div class="pin-ok">✓ 已標示座標（'+it.lat.toFixed(4)+', '+it.lng.toFixed(4)+'）<button onclick="clearSpotPin(\''+it.id+'\',\''+sid+'\')">移除</button></div>':'';
    locH=bmH+
      '<div class="map-combo">'+
      '<input class="map-combo-inp" id="sli-'+it.id+'" type="text" placeholder="🗺 輸入地名搜尋 / 貼上 Google Maps URL" oninput="onSpotLocInput(\''+it.id+'\',\''+sid+'\');" onblur="handleUrlBlur(\''+it.id+'\',\''+sid+'\')" onkeydown="if(event.key===\'Enter\')handleUrlBlur(\''+it.id+'\',\''+sid+'\')">'+
      '<div class="map-combo-drop" id="sld-'+it.id+'"></div></div>'+pinH;
  } else {
    if(it.mapUrl) locH='<a class="bm" href="'+esc(it.mapUrl)+'" target="_blank" rel="noopener"><div class="bm-ico">📍</div><div class="bm-body"><div class="bm-title">'+esc(it.name)+' — 地圖</div><div class="bm-url">'+esc(it.mapUrl)+'</div></div></a>';
    else if(hasPinned) locH='<div class="pin-ok">📍 地圖已標示</div>';
  }

  // Source
  var srcH='';
  if(isEd){
    srcH=it.source
      ?'<div class="source-row">📎 資料來源：<a href="'+esc(it.source)+'" target="_blank">'+esc(it.source)+'</a><button onclick="setItField(\''+sid+'\',\''+it.id+'\',\'source\',\'\')" style="background:none;border:none;color:var(--tx3);cursor:pointer;font-size:11px;margin-left:4px">✕</button></div>'
      :'<input class="map-combo-inp" type="text" placeholder="📎 資料來源網址（選填）" onblur="setItField(\''+sid+'\',\''+it.id+'\',\'source\',this.value)">';
  } else if(it.source) {
    srcH='<div class="source-row">📎 資料來源：<a href="'+esc(it.source)+'" target="_blank">'+esc(it.source)+'</a></div>';
  }

  // Tags
  var tagsH='';
  var tagItems=(it.tags||[]).map(function(t){
    var del=isEd?'<button class="tag-del" onclick="removeTag(\''+sid+'\',\''+it.id+'\',\''+t+'\')">×</button>':'';
    return '<span class="tag">'+t+del+'</span>';
  }).join('');
  if(isEd){
    tagsH='<div class="tags-row">'+tagItems+'<input class="tag-inp" placeholder="＋ 新增標籤" onkeydown="addTag(event,\''+sid+'\',\''+it.id+'\')"></div>';
  } else if(tagItems){
    tagsH='<div class="tags-row">'+tagItems+'</div>';
  }

  var nameAttr=isEd?'onchange="setItField(\''+sid+'\',\''+it.id+'\',\'name\',this.value)"':'readonly';
  var notesH='';
  if(isEd){
    notesH='<textarea class="sc-notes" placeholder="備注・詳細說明…" rows="2" onchange="setItField(\''+sid+'\',\''+it.id+'\',\'notes\',this.value)" oninput="this.style.height=\'auto\';this.style.height=this.scrollHeight+\'px\'">'+esc(it.notes)+'</textarea>';
  } else if(it.notes){
    notesH='<div style="font-size:13px;color:var(--tx2);line-height:1.7;padding:2px 4px">'+esc(it.notes)+'</div>';
  }
  var actsH=isEd?'<div class="sc-acts"><button class="sc-maybe-btn'+(it.maybe?' on':'')+'" onclick="togMaybe(\''+sid+'\',\''+it.id+'\')">maybe</button><button class="ico del" onclick="delSpot(\''+sid+'\',\''+it.id+'\')">✕</button></div>':'';

  return '<div class="sc" id="sc-'+it.id+'">'+
    '<div class="sc-head"><div class="sc-name-wrap">'+
      '<input class="sc-name" value="'+esc(it.name)+'" placeholder="景點名稱" '+nameAttr+'>'+
      (it.maybe?'<span class="sc-maybe">maybe</span>':'')+
    '</div>'+actsH+'</div>'+
    (imgs||imgAdd?'<div class="sc-imgs">'+imgs+imgAdd+'</div>':'')+
    '<div class="sc-meta">'+locH+srcH+tagsH+notesH+
    '</div></div>';
}

// URL 貼入偵測
function handleUrlBlur(iid,sid){
  var inp=document.getElementById('sli-'+iid);
  if(!inp)return;
  var v=(inp.value||'').trim();
  if(!v)return;
  // If it looks like a URL, save as mapUrl
  if(v.indexOf('http')===0||v.indexOf('maps.app')>=0||v.indexOf('openstreetmap')>=0){
    var e=fE(curId),s=fS(e,sid),it=s&&s.items.filter(function(x){return x.id===iid;})[0];
    if(it){it.mapUrl=v;save();renderDetail();}
  }
  // otherwise treat as search query (onLocInput handles it)
}

function setItField(sid,iid,f,v){
  v=(v||'').trim();
  var e=fE(curId),s=fS(e,sid),it=s&&s.items.filter(function(x){return x.id===iid;})[0];
  if(it){it[f]=v;save();if(f==='mapUrl'||f==='source')renderDetail();}
}
function togMaybe(sid,iid){
  var e=fE(curId),s=fS(e,sid),it=s&&s.items.filter(function(x){return x.id===iid;})[0];
  if(it){it.maybe=!it.maybe;save();renderDetail();}
}
function addTag(event,sid,iid){
  if(event.key!=='Enter'&&event.key!==',')return;
  event.preventDefault();
  var t=(event.target.value||'').replace(/[,#]/g,'').trim();
  if(!t)return;
  var e=fE(curId),s=fS(e,sid),it=s&&s.items.filter(function(x){return x.id===iid;})[0];
  if(it){if(!it.tags)it.tags=[];if(it.tags.indexOf(t)<0)it.tags.push(t);save();renderDetail();}
  event.target.value='';
}
function removeTag(sid,iid,tag){
  var e=fE(curId),s=fS(e,sid),it=s&&s.items.filter(function(x){return x.id===iid;})[0];
  if(it){it.tags=it.tags.filter(function(t){return t!==tag;});save();renderDetail();}
}
function addSpot(sid){
  if(!isEd)return;
  var inp=document.getElementById('ni-'+sid);
  var name=(inp.value||'').trim();
  if(!name)return;

  var e=fE(curId),s=fS(e,sid);
  if(!s)return;

  var item=mkItem(name);
  s.items.push(item);

  // 自動地理編碼
  nominatimSearch(name,function(data){
    if(data&&data.length){
      item.lat=parseFloat(data[0].lat);
      item.lng=parseFloat(data[0].lon);
      item.mapUrl='https://www.openstreetmap.org/?mlat='+item.lat+'&mlon='+item.lng+'#map=17/'+item.lat+'/'+item.lng;
    }
    save();
    renderDetail();
  },function(){
    save();
    renderDetail();
  });

  inp.value='';
}
function delSpot(sid,iid){
  if(!isEd||!confirm('確定刪除？'))return;
  var e=fE(curId),s=fS(e,sid);
  if(s){s.items=s.items.filter(function(x){return x.id!==iid;});save();renderDetail();}
}

// ── 圖片 ──
function trigImg(iid){
  if(!isEd)return;
  pendImg=iid;
  var fi=document.getElementById('fi');
  fi.value=''; // reset so same file can be re-selected
  fi.click();
}
document.getElementById('fi').addEventListener('change',function(){
  var files=Array.from(this.files);
  if(!files.length||!pendImg||!curId)return;
  var savedIid=pendImg; // capture before async
  var e=fE(curId);
  if(!e)return;
  var remaining=files.length;
  files.forEach(function(f){
    if(f.size>4*1024*1024){
      alert(f.name+' 超過 4MB，請壓縮後再上傳');
      remaining--;
      return;
    }
    var r=new FileReader();
    r.onload=function(ev){
      // find item
      var found=false;
      for(var i=0;i<e.sections.length&&!found;i++){
        for(var j=0;j<e.sections[i].items.length&&!found;j++){
          if(e.sections[i].items[j].id===savedIid){
            e.sections[i].items[j].images.push(ev.target.result);
            found=true;
          }
        }
      }
      remaining--;
      if(remaining<=0){ save(); renderDetail(); }
    };
    r.onerror=function(){ remaining--; if(remaining<=0){save();renderDetail();} };
    r.readAsDataURL(f);
  });
  this.value='';
});
function delImg(iid,idx){
  if(!isEd)return;
  var e=fE(curId),res=fI(e,iid);
  if(res){res.it.images.splice(idx,1);save();renderDetail();}
}
function viewImg(src){document.getElementById('iv-img').src=src;openOv('iv');}

// ── ENTRY MODAL ──
var editId=null;
function openAddE(){if(!isEd)return;editId=null;showEM({cat:curTab==='全部'?'朝班':curTab,location:'',story:''});}
function openEditE(id){if(!isEd)return;editId=id;showEM(fE(id));}
function showEM(e){
  document.getElementById('em-ttl').textContent=editId?'編輯條目':'新增條目';
  document.getElementById('em-body').innerHTML=
    '<div class="fg"><label class="fl">分類</label>'+
    '<div style="display:flex;gap:6px"><select class="fi" id="fb" style="flex:1">'+CATS_LIST.map(function(c){return'<option value="'+c+'"'+(c===(e.cat||e.band)?' selected':'')+'>'+c+'</option>';}).join('')+'</select>'+
    '<button class="btn-g" onclick="addGlobalCat()" style="white-space:nowrap;padding:6px 10px;font-size:12px">＋ 新增</button></div></div>'+
    '<div class="fg"><label class="fl">地點 / 名稱</label><input class="fi" id="floc" type="text" value="'+esc(e.location||'')+'" placeholder="例：大分"></div>'+
    '<div class="fg"><label class="fl">📖 故事名稱</label><input class="fi" id="fstory" type="text" value="'+esc(e.story||'')+'" placeholder="故事標題（選填）"></div>'+
    '<div class="mfoot"><button class="btn-g" onclick="closeOv(\'em\')">取消</button><button class="btn-p" onclick="saveE()">儲存</button></div>';
  openOv('em');
}
function addGlobalCat(){
  var name=prompt('輸入新分類名稱：');
  if(!name||!name.trim())return;
  name=name.trim();
  if(CATS_LIST.indexOf(name)>=0){alert('此分類已存在');return;}
  CATS_LIST.push(name);
  save();
  // re-render the select
  var fb=document.getElementById('fb');
  if(fb){
    var opt=document.createElement('option');
    opt.value=name;opt.textContent=name;opt.selected=true;
    fb.appendChild(opt);
  }
}
function saveE(){
  var cat=document.getElementById('fb').value;
  var loc=document.getElementById('floc').value.trim();
  var story=document.getElementById('fstory').value.trim();
  if(!loc){alert('請輸入地點名稱');return;}

  function done(){
    save();
    closeOv('em');
    if(editId&&editId===curId) renderDetail();
    else backToList();
    editId=null;
  }

  if(editId){
    var entry=fE(editId);
    entry.cat=cat;
    entry.location=loc;
    entry.story=story;

    // 若沒有座標就自動查詢
    if(!CAT_LL[loc]){
      nominatimSearch(loc,function(data){
        if(data&&data.length){
          CAT_LL[loc]=[parseFloat(data[0].lat),parseFloat(data[0].lon)];
        }
        done();
      },done);
    }else{
      done();
    }
  }else{
    var newEntry={
      id:uid(),
      cat:cat,
      location:loc,
      story:story,
      sections:[
        mkSec(uid(),'景點','景點'),
        mkSec(uid(),'美食','美食'),
        mkSec(uid(),'其他','其他')
      ]
    };
    db.push(newEntry);

    if(!CAT_LL[loc]){
      nominatimSearch(loc,function(data){
        if(data&&data.length){
          CAT_LL[loc]=[parseFloat(data[0].lat),parseFloat(data[0].lon)];
        }
        done();
      },done);
    }else{
      done();
    }
  }
}

// ── 分類管理 ──
function openCatManage(eid){
  var e=fE(eid);
  renderCatModal(e);
  openOv('cat-modal');
}
function renderCatModal(e){
  var listH=e.sections.map(function(s){
    return '<div class="cat-item"><span style="flex:1">'+s.title+'</span>'+(e.sections.length>1?'<button onclick="delSection(\''+e.id+'\',\''+s.id+'\')">✕</button>':'')+'</div>';
  }).join('');
  document.getElementById('cat-modal-body').innerHTML=
    '<div class="cat-list">'+listH+'</div>'+
    '<div class="add-row"><input class="add-inp" id="new-sec-inp" type="text" placeholder="新分類名稱"><button class="add-btn" onclick="addSection(\''+e.id+'\')">新增</button></div>'+
    '<div class="mfoot"><button class="btn-p" onclick="closeOv(\'cat-modal\')">完成</button></div>';
}
function addSection(eid){
  var inp=document.getElementById('new-sec-inp');
  var title=(inp.value||'').trim();if(!title)return;
  var e=fE(eid);
  e.sections.push(mkSec(uid(),title,title));
  save();renderCatModal(e);renderDetail();
  inp.value='';
}
function delSection(eid,sid){
  var e=fE(eid);
  if(e.sections.length<=1){alert('至少保留一個分類');return;}
  if(!confirm('刪除此分類（包含內容）？'))return;
  e.sections=e.sections.filter(function(s){return s.id!==sid;});
  save();renderCatModal(e);renderDetail();
}

// ── OV ──
function openOv(id){document.getElementById(id).classList.add('open');}
function closeOv(id){document.getElementById(id).classList.remove('open');}
document.querySelectorAll('.ov').forEach(function(o){o.addEventListener('click',function(e){if(e.target===o)o.classList.remove('open');});});

// ── INIT ──
syncLockUI();
initMainMap();
renderList();
</script>
</body>
</html>
