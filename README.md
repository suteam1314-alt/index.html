[index.html.html](https://github.com/user-attachments/files/28674760/index.html.html)
<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>產後落髮自測評估表｜蘇老師產康中心</title>
<meta name="description" content="2分鐘快速了解您的產後落髮程度">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
body {
  font-family: -apple-system, "Noto Sans TC", "PingFang TC", sans-serif;
  background: #fef0f4;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 0 48px;
}
.header {
  width: 100%;
  background: linear-gradient(160deg, #f9d0dc 0%, #f5b8cc 60%, #f0a0bc 100%);
  text-align: center;
  padding: 28px 16px 22px;
}
.header-brand { font-size: 10px; color: rgba(160,60,90,.7); letter-spacing: .18em; margin-bottom: 4px; display: none; }
.header-title { font-size: 19px; font-weight: 700; color: #7a2840; letter-spacing: 2px; line-height: 1.5; }
.header-title span { color: #b84060; }

.card {
  width: 100%; max-width: 520px;
  background: #fff;
  border-radius: 0 0 16px 16px;
  box-shadow: 0 2px 16px rgba(120,80,50,.08);
  overflow: hidden;
  margin: 0 16px;
}

.progress-wrap { padding: 20px 24px 0; }
.progress-meta { display: flex; justify-content: space-between; font-size: 11px; color: #c090a0; margin-bottom: 8px; }
.progress-bg { height: 4px; background: #fce8ee; border-radius: 2px; }
.progress-fill { height: 4px; background: #e06080; border-radius: 2px; transition: width .4s ease; }

.q-wrap { padding: 24px 24px 0; }
.q-num { font-size: 10px; font-weight: 700; color: #e06080; letter-spacing: .14em; margin-bottom: 8px; }
.q-text { font-size: 17px; font-weight: 700; color: #5a1830; line-height: 1.45; margin-bottom: 6px; }
.q-hint { font-size: 12px; color: #c090a0; margin-top: 4px; }

.options { display: flex; flex-direction: column; gap: 8px; padding: 16px 24px 0; }
.opt {
  display: flex; align-items: center; gap: 12px;
  border: 1.5px solid #f0c8d4; border-radius: 10px;
  padding: 12px 14px; cursor: pointer;
  transition: all .15s; background: #fef0f4;
  -webkit-tap-highlight-color: transparent; user-select: none;
}
.opt:hover { border-color: #e06080; background: #fdf0e0; }
.opt.selected { border-color: #e06080; background: #fdeedd; }
.opt-circle {
  width: 20px; height: 20px; border-radius: 50%;
  border: 2px solid #e0b0c0; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center;
  transition: all .15s;
}
.opt.selected .opt-circle { border-color: #e06080; background: #e06080; }
.opt-dot { width: 7px; height: 7px; border-radius: 50%; background: #fff; display: none; }
.opt.selected .opt-dot { display: block; }
.opt-text { font-size: 14px; color: #5a1830; line-height: 1.45; }

.btn-row { display: flex; gap: 10px; padding: 20px 24px 24px; margin-top: 8px; }
.btn-prev {
  font-size: 14px; color: #c090a0; background: none;
  border: 1.5px solid #f0c8d4; border-radius: 10px;
  padding: 13px 20px; cursor: pointer; font-family: inherit;
  transition: all .15s; white-space: nowrap;
}
.btn-prev:hover { background: #fef0f4; }
.btn-next {
  flex: 1; font-size: 14px; font-weight: 700;
  color: #fff; background: #e06080; border: none;
  border-radius: 10px; padding: 13px; cursor: pointer;
  font-family: inherit; transition: opacity .15s; letter-spacing: .04em;
}
.btn-next:hover { opacity: .88; }
.btn-next:disabled { opacity: .35; cursor: not-allowed; }

.result { display: none; }
.result-header { text-align: center; padding: 32px 24px 20px; border-bottom: 1px solid #f0e4d6; }
.result-icon { font-size: 42px; margin-bottom: 12px; }
.result-level { font-size: 22px; font-weight: 700; margin-bottom: 6px; }
.result-sub { font-size: 13px; color: #8a4858; line-height: 1.7; white-space: pre-line; }

.score-wrap { padding: 20px 24px 0; }
.score-label { display: flex; justify-content: space-between; font-size: 11px; color: #c090a0; margin-bottom: 6px; }
.score-bg { height: 10px; background: #fce8ee; border-radius: 5px; }
.score-fill { height: 10px; border-radius: 5px; transition: width 1.2s ease; }

.suggest-title { padding: 20px 24px 10px; font-size: 11px; font-weight: 700; color: #c090a0; letter-spacing: .1em; }
.suggest-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; padding: 0 24px; }
.sg { border-radius: 10px; border: 1px solid; padding: 12px 13px; }
.sg h4 { font-size: 12px; font-weight: 700; margin-bottom: 4px; }
.sg p  { font-size: 11.5px; line-height: 1.6; }
.sg-g { background: #eef6ee; border-color: #b0d4b0; }
.sg-g h4 { color: #2a5a2a; } .sg-g p { color: #3a703a; }
.sg-a { background: #fdf4e4; border-color: #e8c890; }
.sg-a h4 { color: #5a3800; } .sg-a p { color: #7a5010; }
.sg-p { background: #f4f0fa; border-color: #c0b0e0; }
.sg-p h4 { color: #3a2870; } .sg-p p { color: #504090; }
.sg-r { background: #fdf0ee; border-color: #e0b0a8; }
.sg-r h4 { color: #6a2010; } .sg-r p { color: #883020; }

.cta-block {
  margin: 20px 24px 0; background: linear-gradient(135deg, #e8607a 0%, #d04868 100%);
  border-radius: 12px; padding: 22px 20px; text-align: center;
}
.cta-title { font-size: 15px; font-weight: 700; color: #fff0f3; margin-bottom: 6px; }
.cta-desc  { font-size: 12px; color: rgba(255,248,240,.7); line-height: 1.7; margin-bottom: 16px; white-space: pre-line; }
.cta-btn {
  display: inline-block; background: #fff; color: #5a1830;
  font-size: 14px; font-weight: 700; padding: 13px 32px;
  border-radius: 8px; cursor: pointer; border: none;
  font-family: inherit; letter-spacing: .06em;
  text-decoration: none; transition: opacity .15s;
}
.cta-btn:hover { opacity: .88; }

.restart-btn {
  display: block; text-align: center; font-size: 12px; color: #c090a0;
  cursor: pointer; margin: 16px auto 28px; background: none; border: none;
  font-family: inherit; text-decoration: underline; text-underline-offset: 3px;
}

.footer { margin-top: 24px; text-align: center; font-size: 11px; color: #c08898; letter-spacing: .06em; line-height: 1.9; }

@media (max-width: 400px) {
  .suggest-grid { grid-template-columns: 1fr; }
  .q-text { font-size: 15px; }
}
</style>
</head>
<body>

<div class="header">
  <div class="header-brand-text" style="font-size:11px;color:rgba(160,60,90,.75);letter-spacing:.16em;margin-bottom:6px;">溫柔守護女人</div>
  <div class="header-title">蘇老師產康中心<br><span>產後落髮自測評估表</span></div>
  <div class="header-tagline" style="font-size:11px;color:rgba(120,40,70,.6);letter-spacing:.12em;margin-top:8px;">— 專業修護產後 —</div>
</div>

<div class="card">

  <div id="quizSection">
    <div class="progress-wrap">
      <div class="progress-meta">
        <span id="stepLabel">第 1 題，共 8 題</span>
        <span id="pctLabel">12%</span>
      </div>
      <div class="progress-bg"><div class="progress-fill" id="pFill" style="width:12%"></div></div>
    </div>
    <div class="q-wrap">
      <div class="q-num" id="qNum"></div>
      <div class="q-text" id="qText"></div>
      <div class="q-hint" id="qHint"></div>
    </div>
    <div class="options" id="optList"></div>
    <div class="btn-row">
      <button class="btn-prev" id="btnPrev" onclick="prev()" style="display:none">← 上一題</button>
      <button class="btn-next" id="btnNext" onclick="next()" disabled>下一題 →</button>
    </div>
  </div>

  <div class="result" id="resultSection">
    <div class="result-header">
      <div class="result-icon" id="rIcon"></div>
      <div class="result-level" id="rLevel"></div>
      <div class="result-sub" id="rSub"></div>
    </div>
    <div class="score-wrap">
      <div class="score-label"><span>輕微</span><span>中度</span><span>嚴重</span></div>
      <div class="score-bg"><div class="score-fill" id="sFill" style="width:0%"></div></div>
    </div>
    <div class="suggest-title">針對您的個人建議</div>
    <div class="suggest-grid" id="sgGrid"></div>
    <div class="cta-block">
      <div class="cta-title" id="ctaT"></div>
      <div class="cta-desc" id="ctaD"></div>
      <a class="cta-btn" href="https://lin.ee/WS8XKhT" target="_blank">加入 LINE 諮詢 →</a>
    </div>
    <button class="restart-btn" onclick="restart()">重新評估</button>
  </div>

</div>

<div class="footer">
  蘇老師產康中心永和店<br>
  © 2026 版權所有
</div>

<script>
var Qs = [
  { num:'Q1', text:'您目前產後幾個月？', hint:'',
    opts:[{t:'產前（懷孕中）',s:0},{t:'產後 1 個月內',s:1},{t:'產後 2–4 個月',s:3},{t:'產後 5–8 個月',s:3},{t:'產後 9 個月以上',s:2}]},
  { num:'Q2', text:'您目前每天的落髮量大概是？', hint:'洗頭或梳髮時觀察',
    opts:[{t:'50根以內（正常範圍）',s:0},{t:'50–100根（輕微增加）',s:1},{t:'100–200根（明顯增多）',s:2},{t:'200根以上（大量掉落）',s:3},{t:'不確定，但明顯比以前多',s:2}]},
  { num:'Q3', text:'落髮持續了多久了？', hint:'',
    opts:[{t:'剛開始（1–2週）',s:1},{t:'1–2 個月',s:2},{t:'3–6 個月',s:3},{t:'超過 6 個月',s:4},{t:'還沒開始但很擔心',s:0}]},
  { num:'Q4', text:'頭髮有明顯變稀疏或頭皮更容易看見嗎？', hint:'特別是髮際線、分縫處',
    opts:[{t:'沒有，髮量看起來正常',s:0},{t:'稍微感覺髮量減少',s:1},{t:'明顯變稀，分縫變寬',s:3},{t:'非常明顯，影響到日常信心',s:4}]},
  { num:'Q5', text:'您目前是否有以下任一情況？', hint:'選最符合的一項',
    opts:[{t:'仍在哺乳中',s:2},{t:'睡眠嚴重不足（每天少於 5 小時）',s:2},{t:'情緒壓力大或有產後憂鬱傾向',s:2},{t:'飲食不均衡或節食減重',s:2},{t:'以上皆無',s:0}]},
  { num:'Q6', text:'您曾做過哪些應對措施？', hint:'',
    opts:[{t:'換了洗髮精或用護髮產品',s:1},{t:'自行補充生物素或其他保健品',s:1},{t:'諮詢過醫師或做過檢查',s:0},{t:'什麼都還沒做，不知道從何開始',s:2},{t:'試過很多方法但效果不明顯',s:3}]},
  { num:'Q7', text:'您的頭皮狀況如何？', hint:'',
    opts:[{t:'頭皮正常，無不適',s:0},{t:'偶爾會癢或出油',s:1},{t:'常常頭皮癢、敏感或有屑',s:2},{t:'頭皮緊繃、循環感覺很差',s:3}]},
  { num:'Q8', text:'產後落髮對您的心情影響程度是？', hint:'',
    opts:[{t:'幾乎沒影響，只是注意到而已',s:0},{t:'有一點困擾，但還好',s:1},{t:'頗困擾，影響到自信心',s:2},{t:'非常困擾，每天都在擔心',s:3}]}
];

var cur=0, sel=new Array(Qs.length).fill(-1), sc=new Array(Qs.length).fill(0);

function render(){
  var q=Qs[cur], pct=Math.round((cur+1)/Qs.length*100);
  document.getElementById('pFill').style.width=pct+'%';
  document.getElementById('stepLabel').textContent='第'+(cur+1)+'題，共'+Qs.length+'題';
  document.getElementById('pctLabel').textContent=pct+'%';
  document.getElementById('qNum').textContent=q.num+' / Q'+Qs.length;
  document.getElementById('qText').textContent=q.text;
  var hint=document.getElementById('qHint');
  hint.textContent=q.hint||''; hint.style.display=q.hint?'block':'none';
  document.getElementById('btnPrev').style.display=cur===0?'none':'inline-block';
  var nb=document.getElementById('btnNext');
  nb.textContent=cur===Qs.length-1?'查看結果 →':'下一題 →';
  nb.disabled=sel[cur]===-1;
  var html='';
  q.opts.forEach(function(o,i){
    var s=sel[cur]===i?' selected':'';
    html+='<div class="opt'+s+'" onclick="pick('+i+','+o.s+')">'
      +'<div class="opt-circle"><div class="opt-dot"></div></div>'
      +'<div class="opt-text">'+o.t+'</div></div>';
  });
  document.getElementById('optList').innerHTML=html;
}

function pick(i,score){
  sel[cur]=i; sc[cur]=score;
  document.getElementById('btnNext').disabled=false;
  document.querySelectorAll('.opt').forEach(function(el,idx){el.classList.toggle('selected',idx===i);});
}

function next(){ if(sel[cur]===-1)return; if(cur<Qs.length-1){cur++;render();}else showResult(); }
function prev(){ if(cur>0){cur--;render();} }

function showResult(){
  var total=sc.reduce(function(a,b){return a+b;},0), max=22;
  var pct=Math.min(Math.round(total/max*100),100);
  document.getElementById('quizSection').style.display='none';
  document.getElementById('resultSection').style.display='block';
  var level,icon,color,sub,sgs,ctaT,ctaD;
  if(total<=5){
    level='輕微觀察期'; icon='🌿'; color='#c0607a';
    sub='您的落髮程度目前屬於正常範圍\n建議提早建立正確觀念，掌握黃金預防期';
    sgs=[
      {c:'sg-g',t:'賀爾蒙調節期保養',d:'充足睡眠與均衡蛋白質攝取，有助於維持頭髮正常生長週期'},
      {c:'sg-a',t:'營養補充參考',d:'鐵蛋白、生物素、鋅是哺乳期常見的落髮相關營養素，建議諮詢醫師後補充'},
      {c:'sg-p',t:'頭皮按摩習慣',d:'每週2–3次輕柔頭皮按摩促進循環，為毛囊健康打基礎'},
      {c:'sg-g',t:'提前建立知識',d:'了解落髮高峰期時間軸，才能在最需要時做出正確應對'}
    ];
    ctaT='預防勝於調理';
    ctaD='現在掌握正確知識，避免進入嚴重落髮期。\n加入蘇老師 LINE，取得「產後落髮完整指南」。';
  } else if(total<=12){
    level='中度落髮期'; icon='⚠️'; color='#c0607a';
    sub='您已進入明顯落髮階段\n建議系統性了解原因，現在是黃金調理期';
    sgs=[
      {c:'sg-a',t:'了解根本原因',d:'賀爾蒙、鐵蛋白、甲狀腺是中度落髮三大相關因素，建議先諮詢醫師做血液檢查'},
      {c:'sg-g',t:'頭皮環境調理',d:'健髮紓壓頭皮護理（90分）有助改善頭皮循環，感受頭皮狀態變化'},
      {c:'sg-p',t:'飲食調整優先',d:'每日蛋白質攝取不足是哺乳媽媽最常忽略的落髮相關因子'},
      {c:'sg-r',t:'調整日常習慣',d:'減少綁緊馬尾、過度梳髮，選擇溫和無矽靈洗髮產品'}
    ];
    ctaT='現在是調理黃金期';
    ctaD='中度落髮若未適當調理，可能持續加重。\n蘇老師協助您從賀爾蒙到頭皮全面了解自身狀況。';
  } else {
    level='嚴重落髮期'; icon='🔴'; color='#8a2030';
    sub='您的落髮已達較嚴重程度\n建議盡快諮詢專業，透過整合性調理改善';
    sgs=[
      {c:'sg-r',t:'EMS 養髮護理',d:'高階 EMS 養髮護理（120分）有助頭皮循環改善，適合落髮較嚴重的媽媽'},
      {c:'sg-a',t:'賀爾蒙整合了解',d:'嚴重落髮往往多重因素疊加，建議全面了解雌激素、甲狀腺、鐵蛋白狀況'},
      {c:'sg-p',t:'內外同步調理',d:'外部頭皮護理搭配內部營養補充與賀爾蒙調節，整合性調理效果更佳'},
      {c:'sg-g',t:'心理支持同樣重要',d:'嚴重落髮對自信影響深遠，蘇老師社群有許多走過相同歷程的媽媽支持您'}
    ];
    ctaT='需要立即專業諮詢';
    ctaD='您的評估結果顯示需要整合性調理介入。\n蘇老師提供 1:1 落髮諮詢，為您規劃個人化養髮計畫。';
  }
  document.getElementById('rIcon').textContent=icon;
  document.getElementById('rLevel').textContent=level;
  document.getElementById('rLevel').style.color=color;
  document.getElementById('rSub').textContent=sub;
  var sf=document.getElementById('sFill');
  sf.style.background=color;
  setTimeout(function(){sf.style.width=pct+'%';},100);
  var gh='';
  sgs.forEach(function(s){gh+='<div class="sg '+s.c+'"><h4>'+s.t+'</h4><p>'+s.d+'</p></div>';});
  document.getElementById('sgGrid').innerHTML=gh;
  document.getElementById('ctaT').textContent=ctaT;
  document.getElementById('ctaD').textContent=ctaD;
}

function restart(){
  cur=0; sel=new Array(Qs.length).fill(-1); sc=new Array(Qs.length).fill(0);
  document.getElementById('quizSection').style.display='block';
  document.getElementById('resultSection').style.display='none';
  render();
}

render();
</script>
</body>
</html>
