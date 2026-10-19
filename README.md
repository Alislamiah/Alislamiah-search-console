<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#06101f">
  <title>Alislamiah Search Console</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: Arial, Tahoma, sans-serif; min-height: 100vh; background: #06101f; color: #ffffff; display: flex; align-items: center; justify-content: center; padding: 20px; }
    .container { width: 100%; max-width: 720px; text-align: center; }
    .logo { width: 82px; height: 82px; margin: 0 auto 24px; border-radius: 22px; object-fit: cover; box-shadow: 0 10px 35px rgba(0,0,0,.45); }
    .brand { font-size: 17px; color: #6fa8ff; font-weight: bold; letter-spacing: .5px; margin-bottom: 14px; }
    h1 { font-size: 32px; line-height: 1.4; margin-bottom: 18px; font-weight: 800; }
    .description { color: #aebdce; font-size: 17px; line-height: 1.9; max-width: 600px; margin: 0 auto 32px; }
    .card { background: #091a30; border: 1px solid #163252; border-radius: 24px; padding: 35px 28px; box-shadow: 0 18px 55px rgba(0,0,0,.35); }
    .icon { width: 64px; height: 64px; margin: 0 auto 20px; border-radius: 18px; background: #0d2948; display: flex; align-items: center; justify-content: center; font-size: 30px; }
    .card h2 { font-size: 22px; margin-bottom: 13px; }
    .card p { color: #aebdce; font-size: 15px; line-height: 1.8; margin-bottom: 25px; }
    .whatsapp { display: inline-flex; align-items: center; justify-content: center; gap: 10px; width: 100%; max-width: 420px; padding: 16px 25px; border-radius: 14px; background: #168f55; color: white; text-decoration: none; font-size: 17px; font-weight: bold; transition: .2s; border: 0; cursor: pointer; font-family: inherit; }
    .whatsapp:hover { background: #20a965; transform: translateY(-2px); }
    .whatsapp-icon { font-size: 23px; }
    .divider { height: 1px; background: #17324f; margin: 32px 0; }
    .english { direction: ltr; text-align: center; }
    .english h2 { font-size: 21px; margin-bottom: 12px; }
    .english p { color: #aebdce; line-height: 1.8; font-size: 15px; }
    footer { margin-top: 25px; color: #61758d; font-size: 13px; }
    .lookup-card { margin-top: 22px; text-align: right; }
    .lookup-card .icon { margin-left: auto; margin-right: auto; }
    .url-label { display: block; color: #dce8f6; font-size: 14px; font-weight: bold; margin: 0 0 9px; }
    .url-input { width: 100%; padding: 15px 14px; border: 1px solid #234568; border-radius: 12px; background: #061426; color: #fff; font: 15px Arial,sans-serif; direction: ltr; text-align: left; outline: none; }
    .url-input:focus { border-color: #6fa8ff; box-shadow: 0 0 0 3px rgba(111,168,255,.12); }
    .check-btn { display: block; width: 100%; margin-top: 12px; padding: 15px; background: #1769d2; color: #fff; border: 0; border-radius: 13px; font-size: 16px; font-weight: bold; cursor: pointer; }
    .check-btn:hover { background: #237ce9; }
    .message { display: none; margin-top: 16px; padding: 14px; border-radius: 12px; line-height: 1.8; font-size: 14px; }
    .message.show { display: block; }
    .message.bad { color: #ffd4dd; background: #3a1720; border: 1px solid #793044; }
    .message.good { color: #bdf7df; background: #0d332a; border: 1px solid #1d7557; }
    .stats { display: none; margin-top: 18px; }
    .stats.show { display: block; }
    .stats-top { display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 10px; margin-bottom: 12px; }
    .stats-top h3 { font-size: 18px; }
    .status { display: inline-block; border-radius: 999px; padding: 7px 11px; font-size: 12px; font-weight: bold; }
    .status.indexed { color: #bdf7df; background: #0d332a; border: 1px solid #1d7557; }
    .status.not-indexed { color: #ffd4dd; background: #3a1720; border: 1px solid #793044; }
    .checked-url { background: #061426; border: 1px solid #17324f; border-radius: 11px; padding: 12px; margin-bottom: 12px; direction: ltr; text-align: left; overflow-wrap: anywhere; color: #9fc6ff; font-size: 13px; }
    .metric-grid { display: grid; grid-template-columns: repeat(2,minmax(0,1fr)); gap: 10px; }
    .metric { background: #061426; border: 1px solid #17324f; border-radius: 14px; padding: 16px 12px; min-width: 0; }
    .metric-label { color: #aebdce; font-size: 13px; line-height: 1.6; margin-bottom: 8px; }
    .metric-value { color: #fff; font-size: 27px; font-weight: 800; overflow-wrap: anywhere; }
    .metric-sub { color: #7189a4; font-size: 11px; line-height: 1.6; margin-top: 5px; }
    .keywords { margin-top: 18px; }
    .keywords h3 { font-size: 16px; margin-bottom: 10px; }
    .keyword-row { display: flex; justify-content: space-between; gap: 12px; padding: 11px 4px; border-bottom: 1px solid #17324f; font-size: 14px; color: #dce8f6; }
    .keyword-row span:first-child { overflow-wrap: anywhere; }
    .keyword-empty { color: #91a5bd; font-size: 13px; line-height: 1.8; }
    .note { margin-top: 14px; color: #91a5bd; font-size: 12px; line-height: 1.8; }
    @media (max-width: 600px) { h1 { font-size: 26px; } .description { font-size: 15px; } .card { padding: 28px 20px; } .metric-grid { gap: 8px; } .metric { padding: 14px 10px; } .metric-value { font-size: 24px; } }
  </style>
</head>
<body>
  <main class="container">
    <img src="icon.png" alt="Alislamiah AI" class="logo">
    <div class="brand">Alislamiah AI</div>

    <h1>مرحباً بك في مركز فهرسة المواقع</h1>
    <p class="description">
      لدى <strong>Alislamiah AI</strong><br>
      يمكنك إرسال طلب لإضافة موقعك إلى فهرس البحث الخاص بنا.
    </p>

    <!-- المحتوى الأصلي محفوظ؛ زر واتساب يرسل الرابط الذي أدخله المستخدم في البطاقة أدناه -->
    <section class="card">
      <div class="icon">🔎</div>
      <h2>طلب فهرسة موقعك</h2>
      <p>
        اضغط على الزر أدناه للانتقال إلى WhatsApp،
        ثم أرسل لنا <strong>رابط موقعك ووصفاً مختصراً عنه</strong>.
        سيقوم فريق Alislamiah AI بمراجعة طلبك.
      </p>
      <a id="whatsappRequest" class="whatsapp" href="https://wa.me/213777543015" target="_blank" rel="noopener noreferrer">
        <span class="whatsapp-icon">💬</span>
        إرسال طلب الفهرسة عبر WhatsApp
      </a>
      <div class="divider"></div>
      <div class="english">
        <h2>Website Indexing Request</h2>
        <p>
          Welcome to the <strong>Alislamiah AI Website Indexing Center</strong>.
          To request the indexing of your website in our search index,
          click the WhatsApp button above and send us your
          <strong>website URL and a short description</strong>.
        </p>
      </div>
    </section>

    <!-- بطاقة التحقق من الرابط والإحصائيات: أضيفت أسفل المحتوى الأصلي -->
    <section class="card lookup-card">
      <div class="icon">📊</div>
      <h2>التحقق من الفهرسة والإحصائيات</h2>
      <p>أدخل رابط الصفحة لمعرفة هل هي مفهرسة في Alislamiah AI، ثم عرض إحصائياتها إذا كانت مفهرسة.</p>
      <label class="url-label" for="siteUrl">رابط الصفحة / Page URL</label>
      <input class="url-input" id="siteUrl" type="url" inputmode="url" placeholder="https://example.com/page" autocomplete="url">
      <button class="check-btn" id="checkBtn" type="button">التحقق وعرض الإحصائيات</button>
      <div id="resultMessage" class="message" role="status" aria-live="polite"></div>

      <div id="statsPanel" class="stats">
        <div class="stats-top">
          <h3>إحصائيات الصفحة</h3>
          <span id="indexStatus" class="status">—</span>
        </div>
        <div id="checkedUrl" class="checked-url"></div>
        <div class="metric-grid">
          <div class="metric">
            <div class="metric-label">Indexed</div>
            <div class="metric-value" id="indexedValue">0</div>
            <div class="metric-sub">حالة الفهرسة</div>
          </div>
          <div class="metric">
            <div class="metric-label">Not indexed</div>
            <div class="metric-value" id="notIndexedValue">0</div>
            <div class="metric-sub">حالة عدم الفهرسة</div>
          </div>
          <div class="metric">
            <div class="metric-label">Clicks — آخر 7 أيام</div>
            <div class="metric-value" id="clicks7">0</div>
          </div>
          <div class="metric">
            <div class="metric-label">Clicks — آخر 28 يوماً</div>
            <div class="metric-value" id="clicks28">0</div>
          </div>
          <div class="metric">
            <div class="metric-label">عدد الزيارات</div>
            <div class="metric-value" id="visitsValue">0</div>
          </div>
          <div class="metric">
            <div class="metric-label">مرات البحث عن اسم الموقع</div>
            <div class="metric-value" id="searchesValue">0</div>
          </div>
        </div>
        <div class="keywords">
          <h3>الكلمات التي بحث بها المستخدمون</h3>
          <div id="keywordList" class="keyword-empty">لا توجد بيانات كلمات بحث مسجلة.</div>
        </div>
        <p class="note" id="statsNote">تظهر هنا بيانات الصفحة المسجلة في إعدادات الكود.</p>
      </div>
    </section>

    <footer>© 2026 Alislamiah AI — Website Indexing Center</footer>
  </main>

  <script>
    /*
      مساحة التفعيل اليدوي والإحصائيات:
      1) أضف رابط الصفحة إلى indexedPages لتصبح Indexed.
      2) ضع أرقام الإحصائيات المسجلة فعلياً في الحقول.
      3) أي رابط غير موجود في indexedPages تظهر له حالة Not indexed وكل الأرقام صفراً.
      ملاحظة: هذه النسخة الأمامية لا تجمع تلقائياً زيارات كل المستخدمين؛ الأرقام هنا تُدخل يدوياً.
    */
    const indexedPages = [
      /*
      مثال — احذف التعليق وأدخل بياناتك الحقيقية:
      {
        url: "https://example.com/",
        clicks7: 12,
        clicks28: 48,
        visits: 120,
        searches: 31,
        keywords: [
          { word: "اسم الموقع", count: 18 },
          { word: "خدمات الموقع", count: 13 }
        ]
      }
      */
    ];

    const urlInput = document.getElementById("siteUrl");
    const checkBtn = document.getElementById("checkBtn");
    const resultMessage = document.getElementById("resultMessage");
    const statsPanel = document.getElementById("statsPanel");
    const whatsappRequest = document.getElementById("whatsappRequest");

    function normalizeUrl(value) {
      const parsed = new URL(value);
      if (!["http:", "https:"].includes(parsed.protocol)) throw new Error("protocol");
      parsed.hash = "";
      parsed.hostname = parsed.hostname.toLowerCase();
      if (parsed.pathname.length > 1) parsed.pathname = parsed.pathname.replace(/\/+$/, "");
      return parsed.href;
    }

    function showMessage(text, kind) {
      resultMessage.textContent = text;
      resultMessage.className = "message show " + kind;
    }

    function displayStats(url, entry) {
      const indexed = Boolean(entry);
      document.getElementById("checkedUrl").textContent = url;
      const status = document.getElementById("indexStatus");
      status.textContent = indexed ? "Indexed page" : "Not indexed page";
      status.className = "status " + (indexed ? "indexed" : "not-indexed");

      document.getElementById("indexedValue").textContent = indexed ? "1" : "0";
      document.getElementById("notIndexedValue").textContent = indexed ? "0" : "1";
      document.getElementById("clicks7").textContent = indexed ? (Number(entry.clicks7) || 0).toLocaleString("en-US") : "0";
      document.getElementById("clicks28").textContent = indexed ? (Number(entry.clicks28) || 0).toLocaleString("en-US") : "0";
      document.getElementById("visitsValue").textContent = indexed ? (Number(entry.visits) || 0).toLocaleString("en-US") : "0";
      document.getElementById("searchesValue").textContent = indexed ? (Number(entry.searches) || 0).toLocaleString("en-US") : "0";

      const keywordList = document.getElementById("keywordList");
      keywordList.replaceChildren();
      if (indexed && Array.isArray(entry.keywords) && entry.keywords.length) {
        keywordList.className = "";
        entry.keywords.forEach(item => {
          const row = document.createElement("div");
          row.className = "keyword-row";
          const word = document.createElement("span");
          word.textContent = item.word;
          const count = document.createElement("strong");
          count.textContent = (Number(item.count) || 0).toLocaleString("en-US") + " مرة";
          row.append(word, count);
          keywordList.appendChild(row);
        });
      } else {
        keywordList.className = "keyword-empty";
        keywordList.textContent = indexed ? "لم تُضف كلمات بحث لهذه الصفحة بعد." : "لا توجد كلمات بحث؛ الصفحة غير مفهرسة.";
      }
      document.getElementById("statsNote").textContent = indexed
        ? "هذه هي الأرقام المدخلة في إعدادات الكود لهذه الصفحة."
        : "هذه الصفحة غير موجودة في قائمة indexedPages؛ لذلك جميع الإحصائيات صفر.";
      statsPanel.classList.add("show");
    }

    function findIndexedPage(normalized) {
      return indexedPages.find(page => {
        try { return normalizeUrl(page.url) === normalized; }
        catch (_) { return false; }
      }) || null;
    }

    checkBtn.addEventListener("click", () => {
      const raw = urlInput.value.trim();
      statsPanel.classList.remove("show");
      resultMessage.className = "message";
      if (!raw) {
        showMessage("أدخل رابط الصفحة أولاً.", "bad");
        urlInput.focus();
        return;
      }
      let normalized;
      try {
        normalized = normalizeUrl(raw);
      } catch (_) {
        showMessage("الرابط غير صالح. أدخل رابطاً كاملاً يبدأ بـ https:// أو http://", "bad");
        return;
      }
      const entry = findIndexedPage(normalized);
      displayStats(normalized, entry);
      showMessage(entry ? "تم العثور على الرابط في قائمة الصفحات المفهرسة." : "هذه الصفحة غير مفهرسة حالياً في قائمة Alislamiah AI.", entry ? "good" : "bad");
    });

    whatsappRequest.addEventListener("click", (event) => {
      const raw = urlInput.value.trim();
      if (!raw) return; // يظل زر واتساب يعمل حتى إن لم يُدخل الرابط في البطاقة.
      let normalized;
      try { normalized = normalizeUrl(raw); }
      catch (_) { return; }
      event.preventDefault();
      const message = "السلام عليكم، أطلب فهرسة موقعي في Alislamiah AI.\nرابط الموقع: " + normalized + "\nالوصف المختصر: ";
      window.open("https://wa.me/213777543015?text=" + encodeURIComponent(message), "_blank", "noopener,noreferrer");
    });

    urlInput.addEventListener("keydown", event => {
      if (event.key === "Enter") checkBtn.click();
    });
  </script>
</body>
</html>
