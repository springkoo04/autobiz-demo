<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#10182c" />
  <title>AutoBiz 6.2 | AI 콘텐츠 · 개인용 대시보드</title>
  <style>
    :root{font-family:system-ui,-apple-system,"Apple SD Gothic Neo","Malgun Gothic",sans-serif;color:#15223b;background:#f5f7fb;font-size:15px}
    *{box-sizing:border-box}body{margin:0}button,input,textarea,select{font:inherit}button{cursor:pointer}button:disabled{opacity:.5;cursor:not-allowed}
    .shell{max-width:1100px;margin:auto;padding:24px 20px 75px}.top{display:flex;align-items:center;justify-content:space-between;gap:14px;margin-bottom:24px}.logo{display:flex;gap:12px;align-items:center}.mark{width:44px;height:44px;border-radius:14px;background:linear-gradient(135deg,#2563eb,#7452e8);display:grid;place-items:center;color:#fff;font-size:21px;font-weight:850}.brand{font-size:20px;font-weight:850;letter-spacing:-.5px}.sub{color:#65738a;font-size:13px;margin-top:3px}.pill{border-radius:99px;background:#e9f1ff;color:#2056bc;padding:8px 12px;font-size:12px;font-weight:750}
    .hero{background:linear-gradient(125deg,#142445,#233b70);border-radius:23px;color:white;padding:28px;display:flex;align-items:center;justify-content:space-between;gap:20px;box-shadow:0 12px 35px #101c3820}.hero h1{font-size:25px;margin:0 0 9px}.hero p{margin:0;color:#d6e2fb;line-height:1.7;max-width:670px}.hero .symbol{font-size:54px;opacity:.65}
    .notice{background:#fffaf0;border:1px solid #f1daa4;border-radius:13px;padding:12px 15px;margin:17px 0;color:#78591e;font-size:13px;line-height:1.6}
    nav{display:flex;gap:9px;flex-wrap:wrap;margin:23px 0}.tab{border:1px solid #dce4f0;background:white;color:#455773;padding:12px 16px;border-radius:12px;font-weight:700}.tab.active{background:#2259d2;color:white;border-color:#2259d2}
    .panel{display:none}.panel.active{display:block}.section-title{display:flex;align-items:center;justify-content:space-between;gap:12px;margin:0 0 14px}.section-title h2{font-size:20px;margin:0}.muted{color:#69778d;font-size:13px;line-height:1.55}.card{background:white;border:1px solid #e4e9f3;border-radius:18px;padding:23px;box-shadow:0 3px 15px #14213d08;margin-bottom:16px}.card h3{margin:0 0 17px;font-size:16px}.cols{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:17px}.two{display:grid;grid-template-columns:1fr 1fr;gap:15px}.three{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}.stat{background:#fff;border:1px solid #e5eaf4;border-radius:17px;padding:19px}.stat .name{color:#71809a;font-size:13px;margin-bottom:10px}.stat .val{font-size:26px;font-weight:850;letter-spacing:-1px;overflow-wrap:anywhere}.stat .val.blue{color:#225ad2}.stat .val.green{color:#0a8a64}
    label{display:block;color:#44536b;font-size:13px;font-weight:700;margin-bottom:7px}.field{margin-bottom:15px}input,textarea,select{width:100%;border:1px solid #d6dfed;border-radius:11px;padding:12px 13px;background:white;outline:none;min-width:0}input:focus,textarea:focus,select:focus{border-color:#4677ee;box-shadow:0 0 0 3px #4677ee20}textarea{resize:vertical;min-height:92px}.btn{border:0;border-radius:11px;padding:11px 16px;background:#245edb;color:white;font-weight:750}.btn:hover{filter:brightness(.97)}.btn.alt{background:#eaf1fd;color:#1e55b8}.btn.ghost{background:white;border:1px solid #d7e0ee;color:#415371}.btn.red{background:#fff1f2;color:#bc2946}.actions{display:flex;flex-wrap:wrap;gap:9px;margin-top:6px}.result{white-space:pre-wrap;line-height:1.75;background:#f6f8fd;border:1px solid #e3e9f5;border-radius:14px;padding:18px;min-height:130px;font-size:14px}.info{background:#edf5ff;color:#2355a1;border-radius:11px;padding:11px 13px;margin:12px 0;font-size:13px;line-height:1.6}.status{min-height:20px;margin-top:10px;font-size:13px;color:#366ba7}.status.err{color:#b52e4c}.tblwrap{overflow:auto}.tbl{width:100%;border-collapse:collapse;font-size:13px;min-width:570px}.tbl th{text-align:left;background:#f4f7fc;color:#64738b;padding:13px 10px}.tbl td{border-top:1px solid #e8edf6;padding:13px 10px}.tbl th.num,.tbl td.num{text-align:right;font-variant-numeric:tabular-nums}.tbl .del{border:0;background:#fff0f1;color:#b82640;border-radius:8px;padding:6px 10px}.empty{text-align:center;color:#8a97aa;padding:28px}.section-bottom{margin-top:19px}canvas{width:100%;height:270px;display:block}.hint{font-size:12px;color:#71829b;line-height:1.6}.badge{background:#e8f6f0;color:#117651;border-radius:7px;padding:3px 7px;font-size:11px;font-weight:800}.footer{text-align:center;color:#718098;font-size:12px;padding:20px}
    @media(max-width:730px){.shell{padding:16px 12px 54px}.hero{padding:22px}.hero .symbol{display:none}.hero h1{font-size:21px}.top .pill{display:none}.cols,.two,.three{grid-template-columns:1fr}.card{padding:17px}.stat .val{font-size:23px}.tab{font-size:13px;padding:11px 12px}}
  </style>
</head>
<body>
<div class="shell">
  <header class="top"><div class="logo"><div class="mark">A</div><div><div class="brand">AutoBiz <span style="color:#3a6de4">6.2</span></div><div class="sub">개인용 비즈니스 관리 웹앱</div></div></div><span class="pill">판매 기록: 브라우저 저장</span></header>
  <section class="hero"><div><h1>반복 업무를 더 간단하게.</h1><p>판매 내역을 기록하고 수익을 계산하세요. 지원 브라우저에서는 AI 모델을 기기에 내려받아 콘텐츠 초안을 생성할 수도 있습니다.</p></div><div class="symbol" aria-hidden="true">▤</div></section>
  <div class="notice"><b>개인 테스트용 안내</b> — 판매 데이터는 이 브라우저에만 저장되며 다른 기기와 자동 동기화되지 않습니다. <b>AI 기능은 WebGPU 지원 기기에서만 사용 가능</b>하며 최초 모델 다운로드에 많은 데이터와 메모리가 필요할 수 있습니다. AI 문장은 틀릴 수 있으므로 반드시 검토하세요. 로그인·결제 기능은 없고, 실제 고객 정보는 입력하지 마세요.</div>
  <nav aria-label="기능 선택">
    <button class="tab active" data-tab="dashboard">📊 대시보드</button><button class="tab" data-tab="sales">🧾 매출 관리</button><button class="tab" data-tab="content">🤖 콘텐츠 제작</button><button class="tab" data-tab="analysis">📈 상품 분석</button><button class="tab" data-tab="backup">💾 백업/복원</button>
  </nav>
  <section id="dashboard" class="panel active">
    <div class="section-title"><h2>매출 대시보드</h2><span class="muted">이 브라우저의 기록 기준</span></div>
    <div class="three"><div class="stat"><div class="name">총매출</div><div class="val blue" id="totalRevenue">0원</div></div><div class="stat"><div class="name">총 예상 이익</div><div class="val green" id="totalProfit">0원</div></div><div class="stat"><div class="name">전체 예상 이익률</div><div class="val" id="totalMargin">0.0%</div></div></div>
    <div class="card section-bottom"><h3>판매 기록별 누적 변화</h3><canvas id="chart" role="img" aria-label="누적 매출 및 예상 이익 그래프"></canvas><div class="hint">파랑: 누적 매출 · 초록: 누적 예상 이익 · 기록 순서 기준</div></div>
    <div class="card"><h3>최근 판매 기록</h3><div id="recent"></div></div>
  </section>
  <section id="sales" class="panel">
    <div class="section-title"><h2>판매 기록 관리</h2><span class="muted">가상 데이터로 테스트해 보세요</span></div>
    <div class="cols"><div class="card"><h3>새 판매 기록</h3><form id="saleForm"><div class="field"><label for="saleName">상품 이름</label><input id="saleName" required maxlength="90" value="무선 미니 선풍기" /></div><div class="two"><div class="field"><label for="salePrice">판매가 (원)</label><input id="salePrice" type="number" min="0" step="1" value="15000" required /></div><div class="field"><label for="saleCost">원가 (원)</label><input id="saleCost" type="number" min="0" step="1" value="9000" required /></div><div class="field"><label for="saleQty">수량</label><input id="saleQty" type="number" min="1" step="1" value="5" required /></div><div class="field"><label for="saleShip">건당 배송비 (원)</label><input id="saleShip" type="number" min="0" step="1" value="0" required /></div><div class="field"><label for="saleFee">수수료 (%)</label><input id="saleFee" type="number" min="0" max="100" step="0.1" value="0" required /></div></div><button type="submit" class="btn">판매 기록 추가</button><div class="status" id="saleStatus" role="status"></div></form></div>
      <div class="card"><h3>계산 방식</h3><p class="muted">매출 = 판매가 × 수량</p><p class="muted">예상 이익 = 매출 − (원가 × 수량) − (배송비 × 수량) − 판매 수수료</p><div class="info">세금, 광고비, 포장비, 환불 등 추가 비용은 포함되지 않습니다. 실제 회계용 장부가 아닌 실험용 계산기입니다.</div><p class="muted">같은 입력값을 2분 이내 연속 제출하면 중복으로 기록되지 않도록 합니다.</p></div></div>
    <div class="card"><h3>판매 내역 <span id="count" class="badge">0건</span></h3><div class="tblwrap"><table class="tbl"><thead><tr><th>상품</th><th class="num">수량</th><th class="num">매출</th><th class="num">예상 이익</th><th>관리</th></tr></thead><tbody id="salesRows"></tbody></table></div></div>
  </section>
  <section id="content" class="panel">
    <div class="section-title"><h2>상품 콘텐츠 제작</h2><span class="badge">템플릿 + 기기 내 AI(지원 브라우저)</span></div>
    <div class="cols"><div class="card"><h3>상품 정보 입력</h3><div class="field"><label for="cName">상품명</label><input id="cName" value="무선 미니 선풍기" maxlength="90" /></div><div class="field"><label for="cFeature">검증된 특징</label><textarea id="cFeature">가볍고 휴대하기 편리함</textarea></div><div class="field"><label for="cTarget">대상</label><input id="cTarget" value="학생" maxlength="90" /></div><div class="field"><label for="cPrice">가격 (원)</label><input id="cPrice" type="number" min="0" value="15000" /></div><button class="btn" id="generateContent">안정적인 템플릿 초안 만들기</button>
        <div class="info" style="margin-top:18px"><b>선택 기능 — 브라우저 AI (실험)</b><p style="margin:6px 0">첫 실행 시 Qwen2.5 0.5B 모델을 외부에서 다운로드합니다. 다운로드 후 생성 계산은 브라우저의 GPU에서 수행합니다. 기기 성능에 따라 불가능하거나 느릴 수 있으며, 공개 웹사이트에 API 키를 넣지 않습니다.</p></div>
        <div class="actions"><button class="btn alt" id="loadLocalAI" type="button">1. 로컬 AI 모델 불러오기</button><button class="btn" id="generateLocalAI" type="button" disabled>2. 실제 AI로 글 생성</button></div>
        <div class="status" id="aiStatus" role="status" aria-live="polite">AI 준비 전 · 데스크톱 Chrome/Edge의 WebGPU 환경 권장</div>
        <div class="status" id="contentStatus" role="status"></div></div>
      <div class="card"><h3>생성된 초안</h3><div class="result" id="contentResult">상품 정보를 입력한 후 템플릿 버튼 또는 AI 버튼을 눌러 보세요.</div><div class="actions"><button class="btn alt" id="copyContent">복사</button><button class="btn ghost" id="saveContent">텍스트 파일 다운로드</button></div><p class="hint">템플릿은 입력한 내용만 사용하지만 AI는 성능·후기·링크를 지어낼 수 있습니다. 두 방식 모두 게시 전 직접 사실을 확인하세요.</p></div></div>
  </section>
  <section id="analysis" class="panel"><div class="section-title"><h2>상품별 분석</h2><span class="muted">정확한 계산 기반</span></div><div class="three"><div class="stat"><div class="name">상품 종류</div><div class="val" id="productCount">0종</div></div><div class="stat"><div class="name">매출 1위 상품</div><div class="val" id="bestProduct" style="font-size:18px">없음</div></div><div class="stat"><div class="name">판매 기록</div><div class="val" id="salesCount">0건</div></div></div><div class="card section-bottom"><h3>상품별 매출과 이익</h3><div class="tblwrap"><table class="tbl"><thead><tr><th>상품</th><th class="num">수량</th><th class="num">매출</th><th class="num">예상 이익</th><th class="num">이익률</th></tr></thead><tbody id="productRows"></tbody></table></div></div><div class="info">이 분석은 파이썬이나 AI 추측이 아니라 브라우저에서 정확한 산술 계산으로 만듭니다. 실제 경영 의사결정에 사용하기 전에 별도 검증이 필요합니다.</div></section>
  <section id="backup" class="panel"><div class="section-title"><h2>데이터 백업 및 복원</h2><span class="muted">기기 간 이동은 파일로</span></div><div class="card"><h3>파일 내려받기</h3><p class="muted">브라우저 기록을 JSON 파일로 백업하거나 Excel에서 열 수 있는 CSV 파일로 내보낼 수 있어요.</p><div class="actions"><button class="btn" id="exportJson">JSON 백업 다운로드</button><button class="btn alt" id="exportCsv">CSV 다운로드</button></div></div><div class="card"><h3>백업 복원하기</h3><p class="muted">이 앱에서 내보낸 JSON 파일을 불러옵니다. 현재 이 브라우저 기록은 교체되므로 먼저 백업하세요.</p><input type="file" id="importJson" accept="application/json,.json" /><div class="actions"><button class="btn red" id="restoreJson">JSON 파일로 복원</button></div><div class="status" id="backupStatus" role="status"></div></div><div class="card"><h3>기존 AutoBiz CSV 불러오기</h3><p class="muted">이전 Colab 버전에서 다운로드한 CSV 중 <b>상품명, 수량, 매출, 예상 이익</b> 형식의 파일을 가져올 수 있습니다. 새로 가져온 기록은 기존 기록 뒤에 추가됩니다.</p><input type="file" id="importCsv" accept="text/csv,.csv" /><div class="actions"><button class="btn alt" id="loadCsv">CSV 기록 가져오기</button></div><p class="hint">CSV는 단순 형식의 파일만 지원합니다. 복잡한 따옴표·줄바꿈 데이터는 JSON 백업을 권장합니다.</p></div></section>
  <footer class="footer">AutoBiz 6.0 · 개인 학습용 시제품 · 데이터는 이 브라우저의 localStorage에만 저장됩니다.</footer>
</div>
<script>
(() => {
'use strict';
const KEY='autobiz6_sales_v1';
const $=id=>document.getElementById(id);
const currency=n=>Math.round(n).toLocaleString('ko-KR')+'원';
const safeNum=v=>Number.isFinite(Number(v))?Number(v):0;
let sales=[];
let lastSubmission=null;
let lastSubmissionAt=0;
const emptyRow=cols=>`<tr><td colspan="${cols}" class="empty">아직 판매 기록이 없습니다.</td></tr>`;
const escapeHtml=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
function normalize(row){
 const name=String(row.name||'').trim().slice(0,90);
 const qty=Number(row.qty), revenue=Number(row.revenue), profit=Number(row.profit);
 if(!name||![qty,revenue,profit].every(Number.isFinite)||qty<=0||!Number.isInteger(qty)||revenue<0||Math.abs(revenue)>1e14||Math.abs(profit)>1e14)throw Error('판매 기록 형식이 잘못되었습니다.');
 return {id: String(row.id||crypto.randomUUID()),name,qty,revenue,profit,created:String(row.created||new Date().toISOString()),fingerprint:String(row.fingerprint||'')};
}
function store(){try{localStorage.setItem(KEY,JSON.stringify(sales));return true;}catch(e){alert('브라우저 저장 실패: 저장 공간 또는 설정을 확인하세요. JSON 백업을 권장합니다.');return false;}}
function load(){try{const raw=JSON.parse(localStorage.getItem(KEY)||'[]');sales=Array.isArray(raw)?raw.map(normalize):[];}catch(e){sales=[];alert('저장된 데이터를 읽지 못했습니다. 이전 JSON 백업으로 복원하세요.');}}
function setStatus(id,msg,error=false){$(id).textContent=msg;$(id).classList.toggle('err',error);}
function group(){const map=new Map();for(const s of sales){const p=map.get(s.name)||{name:s.name,qty:0,revenue:0,profit:0};p.qty+=s.qty;p.revenue+=s.revenue;p.profit+=s.profit;map.set(s.name,p);}return Array.from(map.values()).sort((a,b)=>b.revenue-a.revenue);}
function render(){
 const revenue=sales.reduce((a,x)=>a+x.revenue,0),profit=sales.reduce((a,x)=>a+x.profit,0);
 $('totalRevenue').textContent=currency(revenue);$('totalProfit').textContent=currency(profit);$('totalMargin').textContent=(revenue?profit/revenue*100:0).toFixed(1)+'%';$('count').textContent=sales.length+'건';$('salesCount').textContent=sales.length+'건';
 const grouped=group();$('productCount').textContent=grouped.length+'종';$('bestProduct').textContent=grouped[0]?.name||'없음';
 $('salesRows').innerHTML=sales.length?sales.map(s=>`<tr><td>${escapeHtml(s.name)}</td><td class="num">${s.qty}</td><td class="num">${currency(s.revenue)}</td><td class="num">${currency(s.profit)}</td><td><button class="del" data-id="${escapeHtml(s.id)}" aria-label="${escapeHtml(s.name)} 기록 삭제">삭제</button></td></tr>`).join(''):emptyRow(5);
 $('productRows').innerHTML=grouped.length?grouped.map(p=>`<tr><td>${escapeHtml(p.name)}</td><td class="num">${p.qty}</td><td class="num">${currency(p.revenue)}</td><td class="num">${currency(p.profit)}</td><td class="num">${(p.revenue?p.profit/p.revenue*100:0).toFixed(1)}%</td></tr>`).join(''):emptyRow(5);
 const recent=sales.slice(-3).reverse();$('recent').innerHTML=recent.length?recent.map(s=>`<div style="padding:12px 0;border-top:1px solid #edf1f8;display:flex;justify-content:space-between;gap:12px"><div><b>${escapeHtml(s.name)}</b><div class="muted">${s.qty}개 판매</div></div><b>${currency(s.revenue)}</b></div>`).join(''):'<p class="muted">판매 기록을 추가하면 여기에 나타납니다.</p>';
 drawChart();
}
function drawChart(){const canvas=$('chart');const ctx=canvas.getContext('2d');if(!ctx)return;const rect=canvas.getBoundingClientRect();const w=Math.max(300,rect.width||600),h=270;canvas.width=Math.round(w*devicePixelRatio);canvas.height=Math.round(h*devicePixelRatio);ctx.setTransform(devicePixelRatio,0,0,devicePixelRatio,0,0);ctx.clearRect(0,0,w,h);const L=65,R=18,T=20,B=42;const iw=w-L-R,ih=h-T-B;let rev=0,profit=0;const data=sales.map(s=>({r:rev+=s.revenue,p:profit+=s.profit}));const values=data.flatMap(x=>[x.r,x.p]);const min=Math.min(0,...values),max=Math.max(1,...values);ctx.font='12px system-ui';ctx.lineWidth=1;ctx.strokeStyle='#e8edf6';ctx.fillStyle='#71809a';for(let i=0;i<=4;i++){const y=T+ih*i/4;ctx.beginPath();ctx.moveTo(L,y);ctx.lineTo(w-R,y);ctx.stroke();const v=max-(max-min)*i/4;ctx.fillText(Math.round(v).toLocaleString('ko-KR'),3,y+4)}if(!data.length){ctx.fillStyle='#99a5b7';ctx.textAlign='center';ctx.fillText('판매 기록을 추가하면 그래프가 표시됩니다.',w/2,h/2);ctx.textAlign='left';return;}const x=i=>L+(data.length===1?iw/2:iw*i/(data.length-1));const y=v=>T+ih-(v-min)/(max-min)*ih;for(const [k,color] of [['r','#2c67e4'],['p','#0c956b']]){ctx.strokeStyle=color;ctx.fillStyle=color;ctx.lineWidth=2.5;ctx.beginPath();data.forEach((d,i)=>i?ctx.lineTo(x(i),y(d[k])):ctx.moveTo(x(i),y(d[k])));ctx.stroke();for(let i=0;i<data.length;i++){ctx.beginPath();ctx.arc(x(i),y(data[i][k]),3.5,0,Math.PI*2);ctx.fill();}}ctx.fillStyle='#74839a';ctx.textAlign='center';ctx.fillText('판매 기록 순서 →',L+iw/2,h-8);ctx.textAlign='left';}
function download(name,text,mime){const blob=new Blob([text],{type:mime});const u=URL.createObjectURL(blob);const a=document.createElement('a');a.href=u;a.download=name;document.body.appendChild(a);a.click();a.remove();setTimeout(()=>URL.revokeObjectURL(u),1500);}
function backup(){download('AutoBiz6_backup_'+new Date().toISOString().slice(0,10)+'.json',JSON.stringify({version:1,records:sales},null,2),'application/json;charset=utf-8');}
document.querySelectorAll('.tab').forEach(b=>b.addEventListener('click',()=>{document.querySelectorAll('.tab').forEach(x=>x.classList.toggle('active',x===b));document.querySelectorAll('.panel').forEach(p=>p.classList.toggle('active',p.id===b.dataset.tab));if(b.dataset.tab==='dashboard')drawChart();}));
$('saleForm').addEventListener('submit',e=>{e.preventDefault();try{const name=$('saleName').value.trim(),price=+$('salePrice').value,cost=+$('saleCost').value,qty=+$('saleQty').value,ship=+$('saleShip').value,fee=+$('saleFee').value;if(!name||name.length>90||![price,cost,qty,ship,fee].every(Number.isFinite)||[price,cost,qty,ship,fee].some(x=>x<0)||!Number.isInteger(qty)||qty<1||fee>100)throw Error('입력값을 확인해 주세요.');const fingerprint=JSON.stringify([name,price,cost,qty,ship,fee]);const now=Date.now();if(lastSubmission===fingerprint&&now-lastSubmissionAt<120000)throw Error('같은 기록의 연속 입력을 막았습니다.');const prev=sales[sales.length-1];if(prev?.fingerprint===fingerprint&&now-Date.parse(prev.created)<120000)throw Error('최근에 같은 기록이 이미 저장되었습니다.');const revenue=price*qty,profit=revenue-cost*qty-ship*qty-revenue*fee/100;if(![revenue,profit].every(Number.isFinite)||Math.abs(revenue)>1e14||Math.abs(profit)>1e14)throw Error('금액이 너무 큽니다.');sales.push(normalize({name,qty,revenue:Math.round(revenue*100)/100,profit:Math.round(profit*100)/100,created:new Date().toISOString(),fingerprint}));store();lastSubmission=fingerprint;lastSubmissionAt=now;render();setStatus('saleStatus','✅ 기록이 추가됐습니다. 매출 '+currency(revenue)+' / 예상 이익 '+currency(profit));}catch(err){setStatus('saleStatus','⚠️ '+err.message,true);}});
$('salesRows').addEventListener('click',e=>{const btn=e.target.closest('button[data-id]');if(!btn)return;const s=sales.find(x=>x.id===btn.dataset.id);if(!s)return;if(!confirm(`'${s.name}' 기록을 삭제할까요?\n삭제 전 JSON 백업 다운로드를 권장합니다.`))return;sales=sales.filter(x=>x.id!==btn.dataset.id);store();render();setStatus('saleStatus','선택한 기록을 삭제했습니다.');});
$('generateContent').addEventListener('click',()=>{const name=$('cName').value.trim(),feature=$('cFeature').value.trim(),target=$('cTarget').value.trim()||'관심 있는 분',p=Number($('cPrice').value);if(!name||!feature||!Number.isFinite(p)||p<0){setStatus('contentStatus','상품명, 특징, 가격을 확인해 주세요.',true);return;}const result=`[인스타그램 게시글]\n📦 ${name} 소개!\n${target}이 관심을 가질 만한 상품입니다.\n✅ 주요 특징: ${feature}\n💰 표기 가격: ${currency(p)}\n구매 전 상세 정보를 확인하세요.\n\n[블로그 소개 글]\n오늘 소개할 상품은 ${name}입니다.\n제공된 주요 특징은 다음과 같습니다. ${feature}\n표기 가격은 ${currency(p)}이며, 구매 전 구성과 조건을 직접 확인하는 것이 좋습니다.\n\n[30초 쇼츠 대본 초안]\n[시작] 오늘 살펴볼 상품은 ${name}입니다.\n[제품 설명] 이 상품의 특징은 ${feature}입니다.\n[마무리] 상세 사양과 구매 조건을 꼭 확인해 보세요.`;$('contentResult').textContent=result;setStatus('contentStatus','✅ 템플릿 초안 생성 완료 — 실제 AI 생성 기능은 아닙니다.');});
$('copyContent').addEventListener('click',async()=>{try{await navigator.clipboard.writeText($('contentResult').textContent);setStatus('contentStatus','복사했어요.');}catch(e){setStatus('contentStatus','복사 권한이 없어 직접 선택해서 복사해 주세요.',true);}});
$('saveContent').addEventListener('click',()=>download('AutoBiz6_콘텐츠초안.txt',$('contentResult').textContent,'text/plain;charset=utf-8'));
$('exportJson').addEventListener('click',backup);
$('exportCsv').addEventListener('click',()=>{const esc=s=>'"'+String(s).replaceAll('"','""')+'"';const lines=[['상품명','수량','매출','예상 이익'].map(esc).join(',')].concat(sales.map(s=>[s.name,s.qty,s.revenue,s.profit].map(esc).join(',')));download('AutoBiz6_sales.csv','\ufeff'+lines.join('\r\n'),'text/csv;charset=utf-8');});
$('restoreJson').addEventListener('click',async()=>{try{const f=$('importJson').files[0];if(!f)throw Error('JSON 백업 파일을 선택하세요.');if(f.size>5_000_000)throw Error('파일 크기가 너무 큽니다.');const parsed=JSON.parse(await f.text());if(parsed.version!==1||!Array.isArray(parsed.records)||parsed.records.length>10000)throw Error('AutoBiz 6.0 백업 파일이 아닙니다.');const next=parsed.records.map(normalize);if(!confirm('현재 이 브라우저의 판매 기록을 백업 내용으로 교체할까요?'))return;sales=next;store();render();setStatus('backupStatus',`✅ ${sales.length}건 복원했습니다.`);}catch(e){setStatus('backupStatus','⚠️ '+e.message,true);}});
function splitCSV(line){const out=[];let field='',quoted=false;for(let i=0;i<line.length;i++){const c=line[i];if(c==='"'){if(quoted&&line[i+1]==='"'){field+='"';i++;}else quoted=!quoted;}else if(c===','&&!quoted){out.push(field);field='';}else field+=c;}out.push(field);return out;}
$('loadCsv').addEventListener('click',async()=>{try{const f=$('importCsv').files[0];if(!f)throw Error('CSV 파일을 선택하세요.');if(f.size>2_000_000)throw Error('파일 크기가 너무 큽니다.');const lines=(await f.text()).replace(/^\ufeff/,'').trim().split(/\r?\n/);if(lines.length<2)throw Error('데이터가 없는 CSV입니다.');const heads=splitCSV(lines[0]).map(x=>x.trim().replace(/^\ufeff/,''));const find=arr=>arr.map(x=>heads.indexOf(x)).find(x=>x!==-1);const idx=[find(['상품명','상품 이름']),find(['수량','판매 수량']),find(['매출']),find(['예상 이익','예상이익'])];if(idx.some(x=>x===undefined))throw Error('필수 열(상품명/수량/매출/예상 이익)을 찾지 못했습니다.');const next=lines.slice(1).filter(Boolean).map(line=>{const cells=splitCSV(line);return normalize({name:cells[idx[0]],qty:Number(cells[idx[1]]),revenue:Number(cells[idx[2]]),profit:Number(cells[idx[3]])});});if(next.length>10000)throw Error('기록이 너무 많습니다.');if(!confirm(`CSV 기록 ${next.length}건을 추가할까요? 기존 기록과 중복될 수 있습니다.`))return;sales=[...sales,...next];store();render();setStatus('backupStatus',`✅ CSV 기록 ${next.length}건을 추가했습니다.`);}catch(e){setStatus('backupStatus','⚠️ '+e.message,true);}});
load();render();window.addEventListener('resize',()=>{if($('dashboard').classList.contains('active'))drawChart();});
})();
</script>
<script type="module">
// AutoBiz 6.2 - 선택형 브라우저 AI. 원본 판매 기록 코드는 수정하지 않습니다.
const byId = (id) => document.getElementById(id);
const loadBtn = byId('loadLocalAI');
const genBtn = byId('generateLocalAI');
const status = byId('aiStatus');
let generator = null;
let loading = false;
let generating = false;
const setAiStatus = (message, isError = false) => {
  status.textContent = message;
  status.classList.toggle('err', isError);
};
const checkSupport = async () => {
  if (!window.isSecureContext || !navigator.gpu) {
    return '이 브라우저에는 WebGPU를 사용할 수 없습니다. 데스크톱의 최신 Chrome/Edge와 HTTPS 주소에서 시도해 보세요.';
  }
  try {
    const adapter = await navigator.gpu.requestAdapter();
    if (!adapter) return 'WebGPU 장치를 찾지 못했습니다. 이 기기는 AI 실행이 어려울 수 있어요.';
  } catch (err) {
    return 'WebGPU 점검 실패: ' + String(err?.message || err);
  }
  return null;
};
(async () => {
  const issue = await checkSupport();
  if (issue) { loadBtn.disabled = true; setAiStatus(issue + ' 템플릿 방식은 계속 사용할 수 있습니다.', true); }
  else setAiStatus('WebGPU 사용 가능 · AI 모델 불러오기 버튼을 눌러 시작하세요.');
})();
loadBtn.addEventListener('click', async () => {
  if (loading || generator) return;
  loading = true;
  loadBtn.disabled = true;
  setAiStatus('AI 라이브러리 및 모델 다운로드를 시작합니다. 네트워크 상태를 확인하세요.');
  try {
    const { pipeline } = await import('https://cdn.jsdelivr.net/npm/@huggingface/transformers@3.8.1');
    generator = await pipeline('text-generation', 'onnx-community/Qwen2.5-0.5B-Instruct', {
      device: 'webgpu',
      dtype: 'q4',
      progress_callback: (event) => {
        const pct = Number(event.progress);
        if (event.status === 'progress' && Number.isFinite(pct)) {
          setAiStatus('AI 모델 다운로드 중: ' + Math.round(pct) + '% (파일별 진행률)');
        } else if (event.status === 'initiate' || event.status === 'download') {
          setAiStatus('AI 모델 파일을 다운로드하고 있습니다. 첫 실행에는 시간이 걸릴 수 있습니다.');
        }
      }
    });
    genBtn.disabled = false;
    loadBtn.textContent = 'AI 모델 준비 완료';
    setAiStatus('✅ AI 모델 준비 완료! 상품 정보를 입력한 후 실제 AI로 글 생성 버튼을 누르세요.');
  } catch (error) {
    loadBtn.disabled = false;
    setAiStatus('AI 모델 불러오기 실패: ' + String(error?.message || error) + '. 템플릿 초안 버튼을 사용할 수 있습니다.', true);
  } finally { loading = false; }
});

genBtn.addEventListener('click', async () => {
  if (!generator || generating) return;
  const name = byId('cName').value.trim();
  const feature = byId('cFeature').value.trim();
  const target = byId('cTarget').value.trim() || '일반 고객';
  const price = Number(byId('cPrice').value);
  if (!name || !feature || !Number.isFinite(price) || price < 0) {
    setAiStatus('상품명·검증된 특징·가격을 입력해 주세요.', true); return;
  }
  generating = true;
  genBtn.disabled = true;
  loadBtn.disabled = true;
  setAiStatus('로컬 AI가 글을 생성하고 있습니다. 완료될 때까지 이 페이지를 열어 두세요.');
  try {
    const messages = [
      { role: 'system', content: '당신은 한국어 콘텐츠 초안 작성 도우미입니다. 주어진 사실만 사용하고 확인되지 않은 성능, 후기, 할인, 링크는 작성하지 마세요.' },
      { role: 'user', content: `아래 상품 정보만 사용해 한국어 콘텐츠 초안을 작성해 주세요. 항목별로 서로 다르게 작성하고 중복을 피하세요.\n상품명: ${name}\n검증된 특징: ${feature}\n대상 고객: ${target}\n\n[인스타그램 게시글]\n[블로그 소개 글]\n[30초 쇼츠 대본] 순서로 작성하세요. 가격이나 다른 숫자, URL은 넣지 마세요.` }
    ];
    const output = await generator(messages, { max_new_tokens: 300, do_sample: false, repetition_penalty: 1.15 });
    const generated = output?.[0]?.generated_text;
    let result = typeof generated === 'string' ? generated : (Array.isArray(generated) ? generated.at(-1)?.content : '');
    result = String(result || '').trim();
    if (!result) throw Error('모델이 빈 결과를 반환했습니다.');
    const warns = [];
    if (/https?:\/\/|www\./i.test(result)) warns.push('링크를 생성했습니다. 링크의 진위를 확인하세요.');
    if (/\d/.test(result)) warns.push('숫자를 생성했습니다. 금액과 수치가 정확한지 확인하세요.');
    if (!result.includes('인스타그램') || !result.includes('블로그') || !result.includes('쇼츠')) warns.push('일부 콘텐츠 항목이 누락됐을 수 있습니다.');
    const header = `[브라우저 AI 초안 — 사실 확인 필요]\n입력한 가격: ${price.toLocaleString('ko-KR')}원\n\n`;
    byId('contentResult').textContent = header + result;
    setAiStatus('✅ AI 생성 완료.' + (warns.length ? ' ⚠️ ' + warns.join(' ') : ' 게시 전 사실을 직접 확인하세요.'));
  } catch (error) {
    setAiStatus('AI 생성 실패: ' + String(error?.message || error) + '. 템플릿 방식은 정상 사용할 수 있습니다.', true);
  } finally {
    generating = false;
    genBtn.disabled = false;
    loadBtn.disabled = false;
  }
});
</script>
</body>
</html>

