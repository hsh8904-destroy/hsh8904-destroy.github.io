# hsh8904-destroy.github.io
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>연남세탁 · 세탁물 접수</title>
<style>
:root{--wine:#7A1F2B;--bg:#0f0b0d;--card:#1b1316;--line:#4a1a22;--txt:#E9E9E6;--sub:#B58A90}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--txt);font-family:system-ui,-apple-system,"Noto Sans KR",sans-serif;line-height:1.55}
.wrap{max-width:720px;margin:0 auto;padding:28px 18px 60px}
h1{font-size:20px;font-weight:600;letter-spacing:.08em;margin:0 0 4px}
.sub{color:var(--sub);font-size:13px;margin-bottom:22px}
.deok{background:var(--card);border-left:3px solid var(--wine);padding:10px 14px;font-size:13px;color:#d9c3c7;margin-bottom:22px}
fieldset{border:1px solid var(--line);border-radius:8px;padding:14px 16px;margin:0 0 16px}
legend{padding:0 8px;color:var(--sub);font-size:12px;letter-spacing:.15em}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:10px}
label{font-size:12px;color:var(--sub);display:block;margin-bottom:4px}
input,select{width:100%;background:#120d0f;border:1px solid var(--line);color:var(--txt);padding:8px 10px;border-radius:6px;font-size:14px}
input:focus,select:focus{outline:none;border-color:var(--wine)}
.opts{display:flex;flex-wrap:wrap;gap:14px;margin-top:10px;font-size:13px;color:#d9c3c7}
.opts label{display:flex;align-items:center;gap:6px;margin:0;color:#d9c3c7}
.opts input{width:auto}
button{background:var(--wine);color:#fff;border:0;padding:11px 20px;border-radius:6px;font-size:14px;cursor:pointer;letter-spacing:.05em}
button.ghost{background:transparent;border:1px solid var(--line);color:var(--sub)}
button:hover{filter:brightness(1.15)}
.tag{background:var(--card);border:1px solid var(--line);border-radius:10px;padding:18px;margin-top:22px;position:relative}
.tag:before{content:"";position:absolute;left:50%;top:-8px;width:14px;height:14px;border-radius:50%;background:var(--bg);border:1px solid var(--line);transform:translateX(-50%)}
.tag .who{font-size:11px;letter-spacing:.2em;color:var(--sub);text-align:center;margin-bottom:12px}
.pillars{display:grid;grid-template-columns:repeat(4,1fr);gap:8px}
.pil{background:#120d0f;border:1px solid #2e161b;border-radius:6px;padding:10px 4px;text-align:center}
.pil.day{border-color:var(--wine);background:#1f1216}
.pil .lab{font-size:11px;color:var(--sub);margin-bottom:6px}
.pil .ch{font-size:30px;line-height:1.15;font-weight:500}
.pil .kr{font-size:11px;color:#a08287;margin-top:4px}
.pil .el{font-size:10px;margin-top:2px;opacity:.85}
.ilgan{text-align:center;margin-top:12px;font-size:13px;color:#d9c3c7}
.meta{font-size:11px;color:#8a6a70;text-align:center;margin-top:8px}
pre{background:#0a0708;border:1px dashed var(--line);border-radius:6px;padding:12px;font-size:13px;white-space:pre-wrap;word-break:break-all;margin:14px 0 8px;color:#f1dfe2}
.row{display:flex;gap:8px;flex-wrap:wrap;align-items:center}
.note{font-size:12px;color:#8a6a70;margin-top:26px;line-height:1.7}
.hidden{display:none}
</style>
</head>
<body>
<div class="wrap">
  <h1>연남세탁 · 세탁물 접수</h1>
  <div class="sub">2번 세탁기 옆 건조기 — 비취 앞으로</div>
  <div class="deok">덕이: 생년월일시 넣으시면 태그 뽑아드려요. 코인은 하나. 상대 것도 뽑으실 거면 아래 '상대' 고르고 한 번 더요. 뽑은 건 그대로 복사해서 안에 붙이시면 돼요. 비취 언니는 계산 안 하니까.</div>

  <fieldset>
    <legend>누구 것</legend>
    <div class="opts">
      <label><input type="radio" name="who" value="me" checked> 본인</label>
      <label><input type="radio" name="who" value="partner"> 상대</label>
    </div>
  </fieldset>

  <fieldset>
    <legend>생년월일시 (양력)</legend>
    <div class="grid">
      <div><label>년</label><input id="y" type="number" min="1900" max="2100" placeholder="1988"></div>
      <div><label>월</label><input id="m" type="number" min="1" max="12" placeholder="6"></div>
      <div><label>일</label><input id="d" type="number" min="1" max="31" placeholder="10"></div>
      <div><label>시</label><input id="hh" type="number" min="0" max="23" placeholder="10"></div>
      <div><label>분</label><input id="mi" type="number" min="0" max="59" placeholder="0" value="0"></div>
      <div><label>출생지</label>
        <select id="loc">
          <option value="126.98">서울 (126.98°E)</option>
          <option value="129.08">부산 (129.08°E)</option>
          <option value="128.60">대구 (128.60°E)</option>
          <option value="126.71">인천 (126.71°E)</option>
          <option value="126.85">광주 (126.85°E)</option>
          <option value="127.38">대전 (127.38°E)</option>
          <option value="129.31">울산 (129.31°E)</option>
          <option value="126.53">제주 (126.53°E)</option>
          <option value="127.5">기타 국내 (127.5°E)</option>
        </select>
      </div>
    </div>
    <div class="opts">
      <label><input type="checkbox" id="unknown"> 태어난 시간 모름 (시주 생략)</label>
      <label><input type="checkbox" id="solar" checked> 진태양시 보정 (경도)</label>
      <label><input type="checkbox" id="eot"> 균시차까지 보정</label>
      <label><input type="checkbox" id="jaja" checked> 23시 이후는 다음 날 일주</label>
    </div>
  </fieldset>

  <div class="row">
    <button id="go">태그 뽑기</button>
    <button class="ghost" id="sample">샘플 (1988-06-10 10:00)</button>
  </div>

  <div id="out" class="tag hidden">
    <div class="who" id="whoLab">본인</div>
    <div class="pillars" id="pillars"></div>
    <div class="ilgan" id="ilgan"></div>
    <div class="meta" id="meta"></div>
    <pre id="block"></pre>
    <div class="row">
      <button id="copy">블록 복사</button>
      <span id="copied" style="font-size:12px;color:var(--sub)"></span>
    </div>
  </div>

  <div class="note">
    · 표기는 비취 방 규칙대로 <b>시·일·월·년</b> 순입니다.<br>
    · 월주·년주는 절기(태양 황경) 기준. 입춘 전 출생은 전년도 년주로 잡힙니다.<br>
    · 한국 표준시(UTC+9), 1954~61년 UTC+8:30, 서머타임(1948~60·1987~88)은 자동 반영됩니다.<br>
    · 절기 경계 ±수 분 이내 출생은 오차가 있을 수 있습니다. 음력은 양력 변환 후 입력하세요.<br>
    · 이 페이지는 아무것도 저장하지 않습니다. 계산은 브라우저 안에서만 이뤄집니다.
  </div>
</div>

<script>
(function(){
const GAN=['甲','乙','丙','丁','戊','己','庚','辛','壬','癸'];
const GANK=['갑','을','병','정','무','기','경','신','임','계'];
const JI=['子','丑','寅','卯','辰','巳','午','未','申','酉','戌','亥'];
const JIK=['자','축','인','묘','진','사','오','미','신','유','술','해'];
const GEL=['목','목','화','화','토','토','금','금','수','수'];
const JEL=['수','토','목','목','토','화','화','토','금','금','토','수'];
const GHAN={목:'木',화:'火',토:'土',금:'金',수:'水'};
const COL={목:'#3E8E5A',화:'#C0392B',토:'#C9962B',금:'#E9E9E6',수:'#5C7A99'};
const RAD=Math.PI/180;

function jdFromMs(ms){return ms/86400000+2440587.5;}
function norm(a){return ((a%360)+360)%360;}
function sunLon(jd){
  const T=(jd-2451545)/36525;
  const L0=norm(280.46646+36000.76983*T+0.0003032*T*T);
  const M=norm(357.52911+35999.05029*T-0.0001537*T*T);
  const C=(1.914602-0.004817*T-0.000014*T*T)*Math.sin(M*RAD)+(0.019993-0.000101*T)*Math.sin(2*M*RAD)+0.000289*Math.sin(3*M*RAD);
  const Om=(125.04-1934.136*T)*RAD;
  return norm(L0+C-0.00569-0.00478*Math.sin(Om));
}
function eqTime(jd){ // minutes
  const T=(jd-2451545)/36525;
  const L0=norm(280.46646+36000.76983*T+0.0003032*T*T)*RAD;
  const M=norm(357.52911+35999.05029*T-0.0001537*T*T)*RAD;
  const e=0.016708634-0.000042037*T;
  const eps=(23.439291-0.0130042*T)*RAD;
  const y=Math.tan(eps/2)**2;
  const E=y*Math.sin(2*L0)-2*e*Math.sin(M)+4*e*y*Math.sin(M)*Math.cos(2*L0)-0.5*y*y*Math.sin(4*L0)-1.25*e*e*Math.sin(2*M);
  return E/RAD*4;
}
// 표준시 오프셋(시간) — 한국
function stdOffset(y,m,d){
  const t=Date.UTC(y,m-1,d);
  if(t<Date.UTC(1912,0,1))return 8.5;
  if(t>=Date.UTC(1954,2,21)&&t<Date.UTC(1961,7,10))return 8.5;
  return 9;
}
// 서머타임 — 해당 벽시계 시각이 DST 구간이면 1
function dstHours(y,m,d,h,mi){
  const t=Date.UTC(y,m-1,d,h,mi);
  const R=[[1948,5,1,0,1948,8,13,0],[1949,3,3,0,1949,8,11,0],[1950,3,1,0,1950,8,10,0],[1951,4,6,0,1951,8,9,0],
           [1955,4,5,0,1955,8,9,0],[1956,4,20,0,1956,8,30,0],[1957,4,5,0,1957,8,22,0],[1958,4,4,0,1958,8,21,0],
           [1959,4,3,0,1959,8,20,0],[1960,4,1,0,1960,8,18,0],[1987,4,10,2,1987,9,11,3],[1988,4,8,2,1988,9,9,3]];
  for(const r of R){if(t>=Date.UTC(r[0],r[1],r[2],r[3])&&t<Date.UTC(r[4],r[5],r[6],r[7]))return 1;}
  return 0;
}
function jdn(y,m,d){ // 정오 기준 정수 JDN
  if(m<=2){y-=1;m+=12;}
  const A=Math.floor(y/100),B=2-A+Math.floor(A/4);
  return Math.floor(365.25*(y+4716))+Math.floor(30.6001*(m+1))+d+B-1524;
}
function pad(n){return String(n).padStart(2,'0');}

function calc(y,m,d,h,mi,lon,opt){
  const off=stdOffset(y,m,d);
  const dst=opt.unknown?0:dstHours(y,m,d,h,mi);
  const hh=opt.unknown?12:h, mm=opt.unknown?0:mi;
  const clockMs=Date.UTC(y,m-1,d,hh,mm);
  const stdMs=clockMs-dst*3600000;
  const utcMs=stdMs-off*3600000;
  const jd=jdFromMs(utcMs);
  const lonSun=sunLon(jd);
  const sector=Math.floor(norm(lonSun-315)/30); // 0=인월 … 11=축월

  // 진태양시
  let corr=0;
  if(opt.solar)corr+=(lon-off*15)*4;
  if(opt.eot)corr+=eqTime(jd);
  const appMs=stdMs+corr*60000;
  const ap=new Date(appMs);
  let ay=ap.getUTCFullYear(),am=ap.getUTCMonth()+1,ad=ap.getUTCDate(),ah=ap.getUTCHours(),ami=ap.getUTCMinutes();

  // 년주
  const sd=new Date(stdMs);
  const cy=sd.getUTCFullYear(),cm=sd.getUTCMonth()+1;
  const sajuYear=(cm<=2&&sector>=10)?cy-1:cy;
  const yi=((sajuYear-4)%60+60)%60;
  const yg=yi%10, yj=yi%12;

  // 월주
  const mj=(2+sector)%12;
  const mg=(((yg%5)*2+2)+sector)%10;

  // 일주
  let J=jdn(ay,am,ad);
  if(!opt.unknown&&opt.jaja&&ah>=23)J+=1;
  const di=((J-2451545+54)%60+60)%60;
  const dg=di%10, dj=di%12;

  // 시주
  let hg=null,hj=null;
  if(!opt.unknown){
    hj=Math.floor(((ah+1)%24)/2);
    hg=((dg%5)*2+hj)%10;
  }
  return {yg,yj,mg,mj,dg,dj,hg,hj,off,dst,corr,ay,am,ad,ah,ami,lonSun};
}

function pil(lab,g,j,day){
  if(g===null)return `<div class="pil${day?' day':''}"><div class="lab">${lab}</div><div class="ch" style="color:#5a3a40">—<br>—</div><div class="kr">모름</div></div>`;
  return `<div class="pil${day?' day':''}"><div class="lab">${lab}</div>
    <div class="ch"><span style="color:${COL[GEL[g]]}">${GAN[g]}</span><br><span style="color:${COL[JEL[j]]}">${JI[j]}</span></div>
    <div class="kr">${GANK[g]}${JIK[j]}</div><div class="el">${GEL[g]}·${JEL[j]}</div></div>`;
}

function render(){
  const y=+document.getElementById('y').value,m=+document.getElementById('m').value,d=+document.getElementById('d').value;
  const h=+document.getElementById('hh').value||0,mi=+document.getElementById('mi').value||0;
  if(!y||!m||!d){alert('년·월·일을 넣어주세요.');return;}
  const opt={unknown:document.getElementById('unknown').checked,solar:document.getElementById('solar').checked,eot:document.getElementById('eot').checked,jaja:document.getElementById('jaja').checked};
  const lon=+document.getElementById('loc').value;
  const locName=document.getElementById('loc').selectedOptions[0].text.split(' ')[0];
  const r=calc(y,m,d,h,mi,lon,opt);
  const who=document.querySelector('input[name=who]:checked').value;
  document.getElementById('whoLab').textContent=who==='me'?'본인':'상대';
  document.getElementById('pillars').innerHTML=pil('시',r.hg,r.hj)+pil('일',r.dg,r.dj,true)+pil('월',r.mg,r.mj)+pil('년',r.yg,r.yj);
  document.getElementById('ilgan').innerHTML=`일간 <b style="color:${COL[GEL[r.dg]]}">${GAN[r.dg]}${GHAN[GEL[r.dg]]}</b> (${GANK[r.dg]}${GEL[r.dg]})`;
  const metaBits=[];
  if(r.dst)metaBits.push('서머타임 -1h');
  if(r.off!==9)metaBits.push('표준시 UTC+'+r.off);
  if(!opt.unknown&&opt.solar)metaBits.push('진태양시 '+(r.corr>=0?'+':'')+Math.round(r.corr)+'분');
  if(!opt.unknown)metaBits.push('보정 후 '+pad(r.ah)+':'+pad(r.ami));
  document.getElementById('meta').textContent=metaBits.join(' · ');

  const label=who==='me'?'[사주]':'[사주](상대)';
  const timeStr=opt.unknown?'시간 모름':pad(h)+':'+pad(mi);
  const hStr=r.hg===null?'시:모름':'시:'+GANK[r.hg]+JIK[r.hj];
  const block=`${label} ${y}-${pad(m)}-${pad(d)} ${timeStr} (양력, ${locName})
${hStr} 일:${GANK[r.dg]}${JIK[r.dj]} 월:${GANK[r.mg]}${JIK[r.mj]} 년:${GANK[r.yg]}${JIK[r.yj]} / 일간:${GANK[r.dg]}(${GAN[r.dg]}${GHAN[GEL[r.dg]]})`;
  document.getElementById('block').textContent=block;
  document.getElementById('out').classList.remove('hidden');
  document.getElementById('copied').textContent='';
  document.getElementById('out').scrollIntoView({behavior:'smooth',block:'start'});
}

document.getElementById('go').onclick=render;
document.getElementById('sample').onclick=function(){
  document.getElementById('y').value=1988;document.getElementById('m').value=6;document.getElementById('d').value=10;
  document.getElementById('hh').value=10;document.getElementById('mi').value=0;document.getElementById('unknown').checked=false;render();
};
document.getElementById('copy').onclick=function(){
  const t=document.getElementById('block').textContent;
  const done=()=>{document.getElementById('copied').textContent='복사됐어요. 채팅에 그대로 붙이세요.';};
  if(navigator.clipboard)navigator.clipboard.writeText(t).then(done);
  else{const ta=document.createElement('textarea');ta.value=t;document.body.appendChild(ta);ta.select();document.execCommand('copy');ta.remove();done();}
};
document.getElementById('unknown').onchange=function(){
  const dis=this.checked;document.getElementById('hh').disabled=dis;document.getElementById('mi').disabled=dis;
};
})();
</script>
</body>
</html>
