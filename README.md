<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#06101f">
  <title>Alislamiah Search Console</title>
  <style>
    *{box-sizing:border-box;margin:0;padding:0}
    body{font-family:Arial,Tahoma,sans-serif;min-height:100vh;background:#06101f;color:#fff;display:flex;align-items:center;justify-content:center;padding:20px}
    .container{width:100%;max-width:720px;text-align:center}
    .logo{width:82px;height:82px;margin:0 auto 24px;border-radius:22px;object-fit:cover;box-shadow:0 10px 35px rgba(0,0,0,.45)}
    .brand{font-size:17px;color:#6fa8ff;font-weight:bold;letter-spacing:.5px;margin-bottom:14px}
    h1{font-size:32px;line-height:1.4;margin-bottom:18px;font-weight:800}
    .description{color:#aebdce;font-size:17px;line-height:1.9;max-width:600px;margin:0 auto 32px}
    .card{background:#091a30;border:1px solid #163252;border-radius:24px;padding:35px 28px;box-shadow:0 18px 55px rgba(0,0,0,.35);text-align:center}
    .icon{width:64px;height:64px;margin:0 auto 20px;border-radius:18px;background:#0d2948;display:flex;align-items:center;justify-content:center;font-size:30px}
    .card h2{font-size:22px;margin-bottom:13px}
    .card p{color:#aebdce;font-size:15px;line-height:1.8;margin-bottom:25px}
    .whatsapp{display:inline-flex;align-items:center;justify-content:center;gap:10px;width:100%;max-width:420px;padding:16px 25px;border-radius:14px;background:#168f55;color:#fff;text-decoration:none;font-size:17px;font-weight:bold;transition:.2s;border:0;cursor:pointer}
    .whatsapp:hover{background:#20a965;transform:translateY(-2px)}
    .divider{height:1px;background:#17324f;margin:32px 0}
    .english{direction:ltr;text-align:center}
    .english h2{font-size:21px;margin-bottom:12px}
    .english p{color:#aebdce;line-height:1.8;font-size:15px}
    footer{margin-top:25px;color:#61758d;font-size:13px}
    .lookup-card{margin-top:22px;text-align:right}
    .url-label{display:block;color:#dce8f6;font-size:14px;font-weight:bold;margin:0 0 9px}
    .url-input{width:100%;padding:15px 14px;border:1px solid #234568;border-radius:12px;background:#061426;color:#fff;font:15px Arial,sans-serif;direction:ltr;text-align:left;outline:none}
    .url-input:focus{border-color:#6fa8ff;box-shadow:0 0 0 3px rgba(111,168,255,.12)}
    .check-btn{display:block;width:100%;margin-top:12px;padding:15px;background:#1769d2;color:#fff;border:0;border-radius:13px;font-size:16px;font-weight:bold;cursor:pointer}
    .check-btn:disabled{opacity:.6;cursor:not-allowed}
    .message{display:none;margin-top:16px;padding:14px;border-radius:12px;line-height:1.8;font-size:14px;text-align:right}
    .message.show{display:block}.message.bad{color:#ffd4dd;background:#3a1720;border:1px solid #793044}.message.good{color:#bdf7df;background:#0d332a;border:1px solid #1d7557}
    .stats{display:none;margin-top:18px;text-align:right}.stats.show{display:block}
    .stats-top{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-bottom:12px}
    .status{display:inline-block;border-radius:999px;padding:7px 11px;font-size:12px;font-weight:bold}.status.indexed{color:#bdf7df;background:#0d332a;border:1px solid #1d7557}.status.not-indexed{color:#ffd4dd;background:#3a1720;border:1px solid #793044}
    .checked-url{background:#061426;border:1px solid #17324f;border-radius:11px;padding:12px;margin-bottom:12px;direction:ltr;text-align:left;color:#9fc6ff;font-size:13px;overflow-wrap:anywhere}
    .metric-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px}.metric{background:#061426;border:1px solid #17324f;border-radius:14px;padding:16px 12px;text-align:center}.metric-label{color:#aebdce;font-size:13px;margin-bottom:8px}.metric-value{color:#fff;font-size:27px;font-weight:800}.metric-sub{color:#7189a4;font-size:11px;margin-top:5px}
    .keywords{margin-top:18px}.keyword-row{display:flex;justify-content:space-between;gap:12px;padding:11px 4px;border-bottom:1px solid #17324f;font-size:14px}.keyword-empty{color:#91a5bd;font-size:13px;line-height:1.8}
    .note{margin-top:14px;color:#91a5bd;font-size:12px;line-height:1.8}
  </style>
</head>
<body>
  <main class="container">
    <img src="icon.png" alt="Alislamiah AI" class="logo">
    <div class="brand">Alislamiah AI</div>
    <h1>مرحباً بك في مركز فهرسة المواقع</h1>
    <p class="description">لدى <strong>Alislamiah AI</strong><br>يمكنك إرسال طلب لإضافة موقعك إلى فهرس البحث الخاص بنا.</p>
    <section class="card">
      <div class="icon">🔎</div>
      <h2>طلب فهرسة موقعك</h2>
      <p>اضغط على الزر أدناه للانتقال إلى WhatsApp، ثم أرسل لنا <strong>رابط موقعك ووصفاً مختصراً عنه</strong>.</p>
      <a id="whatsappRequest" class="whatsapp" href="https://wa.me/213777543015" target="_blank" rel="noopener">💬 إرسال طلب الفهرسة عبر WhatsApp</a>
      <div class="divider"></div>
      <div class="english"><h2>Website Indexing Request</h2><p>Welcome to the <strong>Alislamiah AI Website Indexing Center</strong>.</p></div>
    </section>
    <section class="card lookup-card">
      <div class="icon">📊</div>
      <h2>التحقق من الفهرسة والإحصائيات</h2>
      <p>أدخل رابط الصفحة لمعرفة هل هي مفهرسة في Alislamiah AI.</p>
      <label class="url-label" for="siteUrl">رابط الصفحة / Page URL</label>
      <input class="url-input" id="siteUrl" type="url" placeholder="https://example.com/page">
      <button class="check-btn" id="checkBtn" type="button">التحقق وعرض الإحصائيات</button>
      <div id="resultMessage" class="message"></div>
      <div id="statsPanel" class="stats">
        <div class="stats-top"><h3>إحصائيات الصفحة</h3><span id="indexStatus" class="status">—</span></div>
        <div id="checkedUrl" class="checked-url"></div>
        <div class="metric-grid">
          <div class="metric"><div class="metric-label">Indexed</div><div class="metric-value" id="indexedValue">0</div><div class="metric-sub">من results.html</div></div>
          <div class="metric"><div class="metric-label">Not indexed</div><div class="metric-value" id="notIndexedValue">0</div></div>
          <div class="metric"><div class="metric-label">Clicks — 7 أيام</div><div class="metric-value" id="clicks7">0</div></div>
          <div class="metric"><div class="metric-label">Clicks — 28 يوماً</div><div class="metric-value" id="clicks28">0</div></div>
          <div class="metric"><div class="metric-label">عدد الزيارات</div><div class="metric-value" id="visitsValue">0</div></div>
          <div class="metric"><div class="metric-label">مرات البحث</div><div class="metric-value" id="searchesValue">0</div></div>
        </div>
        <div class="keywords"><h3>الكلمات التي بحث بها المستخدمون</h3><div id="keywordList" class="keyword-empty">لا توجد بيانات.</div></div>
        <p class="note" id="statsNote"></p>
      </div>
    </section>
    <footer>© 2026 Alislamiah AI — Website Indexing Center</footer>
  </main>
  <script>
    const activatedPages = [];
    const RESULTS_PAGE_URL = "https://Alislamiah.github.io/Alislamiah-AI/results.html";
    const ANALYTICS_KEY = "alislamiah_search_analytics_v1";
    const urlInput = document.getElementById("siteUrl");
    const checkBtn = document.getElementById("checkBtn");
    const resultMessage = document.getElementById("resultMessage");
    const statsPanel = document.getElementById("statsPanel");
    const whatsappRequest = document.getElementById("whatsappRequest");
    function normalizeUrl(v){const u=new URL(v.trim());if(!["http:","https:"].includes(u.protocol))throw new Error();u.hash="";u.hostname=u.hostname.toLowerCase();if(u.pathname.length>1)u.pathname=u.pathname.replace(/\/+$/,"");return u.href}
    function showMessage(t,k){resultMessage.textContent=t;resultMessage.className="message show "+k}
    function isActivated(url){return activatedPages.some(i=>{try{return normalizeUrl(i)===url}catch(_){return false}})}
    function getEvents(){try{const a=JSON.parse(localStorage.getItem(ANALYTICS_KEY)||"[]");return Array.isArray(a)?a:[]}catch(_){return[]}}
    function setNumber(id,v){document.getElementById(id).textContent=(Number(v)||0).toLocaleString("en-US")}
    function displayStats(url,isIndexed,events){
      document.getElementById("checkedUrl").textContent=url;
      const s=document.getElementById("indexStatus");s.textContent=isIndexed?"Indexed page":"Not indexed page";s.className="status "+(isIndexed?"indexed":"not-indexed");
      setNumber("indexedValue",isIndexed?1:0);setNumber("notIndexedValue",isIndexed?0:1);
      const rel=events.filter(e=>{try{return normalizeUrl(e.url)===url}catch(_){return false}});
      const now=Date.now(),d7=now-7*24*60*60*1000,d28=now-28*24*60*60*1000;
      setNumber("clicks7",rel.filter(e=>e.type==="click"&&Number(e.timestamp)>=d7).length);
      setNumber("clicks28",rel.filter(e=>e.type==="click"&&Number(e.timestamp)>=d28).length);
      setNumber("visitsValue",rel.filter(e=>e.type==="visit").length);
      setNumber("searchesValue",rel.filter(e=>e.type==="search").length);
      const counts=new Map();rel.filter(e=>e.type==="search"&&e.query).forEach(e=>counts.set(e.query,(counts.get(e.query)||0)+1));
      const list=document.getElementById("keywordList");list.replaceChildren();
      const words=[...counts.entries()].sort((a,b)=>b[1]-a[1]).slice(0,20);
      if(words.length){list.className="";words.forEach(([w,c])=>{const r=document.createElement("div");r.className="keyword-row";const l=document.createElement("span");l.textContent=w;const a=document.createElement("strong");a.textContent=c+" مرة";r.append(l,a);list.appendChild(r)})}
      else{list.className="keyword-empty";list.textContent=isIndexed?"لا توجد بيانات بحث مسجلة لهذه الصفحة بعد.":"لا توجد كلمات بحث؛ الصفحة غير مفهرسة."}
      document.getElementById("statsNote").textContent=isIndexed?"تم العثور على الرابط في results.html — مفهرس.":"الرابط مفعّل للدخول لكنه غير موجود في فهرس results.html — غير مفهرس.";
      statsPanel.classList.add("show");
    }
    async function checkPage(url){
      if(!isActivated(url)){statsPanel.classList.remove("show");showMessage("⛔ هذا الرابط غير مفعّل. لا تملك صلاحية الدخول للوحة. تواصل واتساب لتفعيله.","bad");return}
      checkBtn.disabled=true;checkBtn.textContent="جارٍ التحقق...";
      try{
        const res=await fetch(RESULTS_PAGE_URL,{cache:"no-store"});if(!res.ok)throw new Error();
        const html=await res.text();const m=html.match(/const\s+library\s*=\s*(\[[\s\S]*?\])\s*;?/);if(!m)throw new Error();
        let lib;try{lib=(new Function("return ("+m[1]+")"))()}catch(_){throw new Error()}
        const isIndexed=Array.isArray(lib)&&lib.some(i=>{try{return i.url&&normalizeUrl(i.url)===url}catch(_){return false}});
        displayStats(url,isIndexed,getEvents());
        showMessage(isIndexed?"✅ صلاحية الدخول موجودة، والموقع مفهرس حالياً.":"⚠️ لديك صلاحية الدخول، لكن الموقع غير مفهرس بعد في results.html.",isIndexed?"good":"bad");
      }catch(e){statsPanel.classList.remove("show");showMessage("تعذر قراءة results.html. تأكد أنها منشورة وتسمح بالوصول.","bad")}
      finally{checkBtn.disabled=false;checkBtn.textContent="التحقق وعرض الإحصائيات"}
    }
    checkBtn.addEventListener("click",async()=>{
      const raw=urlInput.value.trim();resultMessage.className="message";statsPanel.classList.remove("show");
      if(!raw){showMessage("أدخل رابط الصفحة أولاً.","bad");urlInput.focus();return}
      let norm;try{norm=normalizeUrl(raw)}catch(_){showMessage("الرابط غير صالح. يبدأ بـ https://","bad");return}
      await checkPage(norm);
    });
    whatsappRequest.addEventListener("click",(e)=>{
      const raw=urlInput.value.trim();if(!raw)return;let norm;try{norm=normalizeUrl(raw)}catch(_){return}
      e.preventDefault();const msg="السلام عليكم، أطلب فهرسة موقعي في Alislamiah AI.\nرابط الموقع: "+norm+"\nالوصف: ";
      window.open("https://wa.me/213777543015?text="+encodeURIComponent(msg),"_blank","noopener");
    });
    urlInput.addEventListener("keydown",e=>{if(e.key==="Enter")checkBtn.click()});
  </script>
</body>
</html>