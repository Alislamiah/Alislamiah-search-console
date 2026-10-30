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
    .english{direction:ltr;text-align:center}.english h2{font-size:21px;margin-bottom:12px}.english p{color:#aebdce;line-height:1.8;font-size:15px}
    footer{margin-top:25px;color:#61758d;font-size:13px}
    .lookup-card{margin-top:22px;text-align:right}
    .url-label{display:block;color:#dce8f6;font-size:14px;font-weight:bold;margin:0 0 9px}
    .url-input{width:100%;padding:15px 14px;border:1px solid #234568;border-radius:12px;background:#061426;color:#fff;font:15px Arial,sans-serif;direction:ltr;text-align:left;outline:none}
    .check-btn{display:block;width:100%;margin-top:12px;padding:15px;background:#1769d2;color:#fff;border:0;border-radius:13px;font-size:16px;font-weight:bold;cursor:pointer}
    .message{display:none;margin-top:16px;padding:14px;border-radius:12px;line-height:1.8;font-size:14px;text-align:right}
    .message.show{display:block}.message.bad{color:#ffd4dd;background:#3a1720;border:1px solid #793044}
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
      <a id="whatsappRequest" class="whatsapp" href="https://wa.me/213777543015" target="_blank" rel="noopener noreferrer">💬 إرسال طلب الفهرسة عبر WhatsApp</a>
      <div class="divider"></div>
      <div class="english"><h2>Website Indexing Request</h2><p>Welcome to the <strong>Alislamiah AI Website Indexing Center</strong>.</p></div>
    </section>
    <section class="card lookup-card">
      <div class="icon">📊</div>
      <h2>التحقق من الفهرسة والإحصائيات</h2>
      <p>أدخل رابط الصفحة لمعرفة هل هي مفهرسة.</p>
      <label class="url-label" for="siteUrl">رابط الصفحة / Page URL</label>
      <input class="url-input" id="siteUrl" type="url" placeholder="https://example.com/page">
      <button class="check-btn" id="checkBtn" type="button">التحقق وعرض الإحصائيات</button>
      <div id="resultMessage" class="message"></div>
    </section>
    <footer>© 2026 Alislamiah AI</footer>
  </main>
  <script>
    const activatedPages = [
      "https://alislamiah.github.io/Alislamiah-_net/"
    ];
    function normalizeUrl(v){const u=new URL(v.trim());u.hash="";u.hostname=u.hostname.toLowerCase();if(u.pathname.length>1)u.pathname=u.pathname.replace(/\/+$/,"");return u.href}
    function isActivated(url){return activatedPages.some(i=>{try{return normalizeUrl(i)===url}catch(_){return false}})}
    function checkPage(url){
      if(!isActivated(url)){
        const m=document.getElementById("resultMessage");
        m.textContent="⛔ هذا الرابط غير مفعّل.";
        m.className="message show bad";
        return;
      }
      window.location.href = "Analytics.html?url=" + encodeURIComponent(url);
    }
    document.getElementById("checkBtn").addEventListener("click",()=>{
      const raw=document.getElementById("siteUrl").value.trim();
      if(!raw){document.getElementById("resultMessage").textContent="أدخل رابط الصفحة أولاً.";document.getElementById("resultMessage").className="message show bad";return}
      let norm;try{norm=normalizeUrl(raw)}catch(_){document.getElementById("resultMessage").textContent="الرابط غير صالح.";document.getElementById("resultMessage").className="message show bad";return}
      checkPage(norm);
    });
  </script>
</body>
</html>