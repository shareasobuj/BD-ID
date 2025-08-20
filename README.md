 BD-ID

<html lang="bn">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>বাংলাদেশ তথ্য ভাণ্ডার</title>
<style>
  :root{
    --bg:#0f1724; --card:#0f1724; --panel:#0b1f2a;
    --accent:#0ea5a3; --muted:#94a3b8; --surface:#0b1220;
    --success:#16a34a; --danger:#ef4444; --glass: rgba(255,255,255,0.03);
    --text:#e6eef6;
  }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;color:var(--text);background:linear-gradient(180deg,yellow 0%,#081826 80%);}
  header{background:linear-gradient(90deg,green,red);padding:18px 20px;position:sticky;top:0;z-index:40;border-bottom:1px solid rgba(255,255,255,0.04);}
  .brand{display:flex;align-items:center;gap:14px}
  .brand .logo{width:44px;height:44px;border-radius:8px;background:linear-gradient(45deg,#06b6d4,#34d399);box-shadow:0 6px 30px rgba(2,6,23,0.6)}
  .container{max-width:1100px;margin:18px auto;padding:0 16px}
  nav{display:flex;gap:10px;flex-wrap:wrap;align-items:center}
  .tabs{display:flex;gap:8px;flex-wrap:wrap}
  .tab{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:8px 12px;border-radius:10px;color:var(--text);cursor:pointer}
  .tab.active{border-color:var(--accent);box-shadow:inset 0 0 0 2px rgba(14,165,163,0.08)}
  .right{margin-left:auto;display:flex;gap:8px;align-items:center}
  .pill{padding:6px 10px;border-radius:999px;background:rgba(255,255,255,0.03);border:1px solid rgba(255,255,255,0.04)}
  .btn{background:linear-gradient(90deg,var(--accent),#06b6d4);border:none;padding:8px 12px;border-radius:10px;color:#012;cursor:pointer}
  .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--text)}
  main{padding:18px 0}
  section.page{display:none;background:linear-gradient(180deg,#071428,#081a2b);padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.03);margin-bottom:18px}
  section.page.active{display:block}
  .grid{display:grid;gap:16px}
  .g2{grid-template-columns:1fr 380px}
  @media(max-width:980px){.g2{grid-template-columns:1fr}}
  .card{background:linear-gradient(180deg,#061220,#071828);padding:14px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
  h1,h2,h3{margin:6px 0}
  p{color:rgba(230,238,246,0.9);line-height:1.6}
  label{display:block;color:var(--muted);margin-top:8px}
  input,textarea,select{width:100%;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:rgba(255,255,255,0.02);color:var(--text);margin-top:6px}
  table{width:100%;border-collapse:collapse}
  th,td{padding:8px;border-bottom:1px dashed rgba(255,255,255,0.03);text-align:left}
  footer{color:var(--muted);text-align:center;padding:12px;margin-top:8px}
  .notice{background:rgba(14,165,163,0.06);padding:10px;border-radius:8px;border:1px solid rgba(14,165,163,0.06);color:var(--muted)}
  small.muted{color:var(--muted)}
  .toolbar{display:flex;gap:8px;flex-wrap:wrap;margin-top:10px}
  .danger{background:linear-gradient(90deg,#fb7185,#ef4444);color:#fff;border:none;padding:8px 10px;border-radius:10px}
  .success{background:linear-gradient(90deg,#34d399,#16a34a);color:#012;border:none;padding:8px 10px;border-radius:10px}
  pre {white-space:pre-wrap;word-break:break-word;background:rgba(255,255,255,0.02);padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.03)}
</style>
</head>
<body>
<header>
  <div class="container" style="display:flex;align-items:center;gap:16px">
    <div class="brand">
      <div class="logo" aria-hidden="true"></div>
      <div>
        <div style="font-weight:700">বাংলাদেশ তথ্য ভাণ্ডার</div>
        <div style="font-size:12px;color:var(--muted)">Bnagladesh</div>
      </div>
    </div>
  </div>
</header>

<div class="container">
  <nav style="display:flex;align-items:center;gap:8px;margin-top:12px">
    <div class="tabs" id="tabs">
      <button class="tab" data-route="home">হোম</button>
      <button class="tab" data-route="area">আয়তন</button>
      <button class="tab" data-route="border">সীমান্ত</button>
      <button class="tab" data-route="geo">ভূগোল</button>
      <button class="tab" data-route="admin_info">প্রশাসন</button>
      <button class="tab" data-route="economy">অর্থনীতি</button>
      <button class="tab" data-route="culture">সংস্কৃতি</button>
      <button class="tab" data-route="tourism">পর্যটন</button>
      <button class="tab" data-route="dashboard">ড্যাশবোর্ড</button>
      <button class="tab" data-route="feedback">ফিডব্যাক</button>
      <button class="tab" data-route="admin" id="adminTab" style="display:none">অ্যাডমিন প্যানেল</button>
    </div>
    <div class="right">
      <div class="pill" id="userBadge">Guest</div>
      <button class="btn ghost" id="openLogin">লগইন/সাইনআপ</button>
      <button class="btn" id="logoutBtn" style="display:none">লগআউট</button>
    </div>
  </nav>

  <main>
    <!-- HOME -->
    <section id="home" class="page active">
      <div class="grid g2">
        <div>
          <h1>বাংলাদেশ — সংক্ষিপ্ত পরিচিতি</h1>
          <p>
            বাংলাদেশ দক্ষিণ এশিয়ায় অবস্থিত একটি স্বাধীন দেশ। ১৯৭১ সালের মুক্তিযুদ্ধের মাধ্যমে পাকিস্তান থেকে স্বাধীনতা লাভ করে
            বাংলাদেশ। রাজধানী ঢাকা। জাতীয় ভাষা: বাংলা। বাংলাদেশের ভৌগোলিক বৈশিষ্ট্য, জনগণের সাংস্কৃতিক ঐতিহ্য ও কৃষি-ভিত্তিক অর্থনীতি এটি একটি অনন্য পরিচয় দেয়।
          </p>

          <h3>ঐতিহাসিক সংক্ষিপ্ত রূপরেখা</h3>
          <p>
            প্রাচীনকালে এই অঞ্চল বঙ্গ বা বাঙ্গাল নামে পরিচিত ছিল। মুসলিম শাসন, মুগল সাম্রাজ্য, ব্রিটিশ উপনিবেশ, ও অবশেষে ১৯৭১ সালে স্বাধীনতা—এই ধারার মধ্য দিয়ে দেশটির ইতিহাস গঠিত হয়েছে।
          </p>

          <h3>বাস্তুতন্ত্র ও নদীনির্ভর জীবন</h3>
          <p>
            বাংলাদেশে নদীমাধ্যমিক পরিবেশ বেশি; গঙ্গা–ব্রহ্মপুত্র–মেঘনা নদী জোড়ার তলা-বাঁকে বিস্তীর্ণ প্লাবনভূমি গড়ে উঠেছে। বর্ষাকালে বন্যা ও জলবায়ুর পরিবর্তন কৃষি ও বসতি উভয়কে প্রভাবিত করে।
          </p>

          <h3>গুরুত্বপূর্ণ তথ্য</h3>
          <ul>
            <li>রাষ্ট্রীয় গঠন: সংসদীয় গণতন্ত্র</li>
            <li>রাজধানী: ঢাকা</li>
            <li>মুদ্রা: বাংলাদেশি টাকা (৳)</li>
            <li>আবহাওয়া: উষ্ণ আর্দ্র উৎসতুর (ট্রপিক্যাল)</li>
          </ul>
        </div>

        <aside>
          <div class="card">
            <h3>দ্রুত পরিসংখ্যান</h3>
            <table>
              <tr><th>সূচক</th><th>মান</th></tr>
              <tr><td>মোট আয়তন</td><td id="stat_area">—</td></tr>
              <tr><td>স্থল সীমান্ত (মোট)</td><td id="stat_land">—</td></tr>
              <tr><td>ভারত সীমান্ত</td><td id="stat_india">—</td></tr>
              <tr><td>মিয়ানমার সীমান্ত</td><td id="stat_myanmar">—</td></tr>
              <tr><td>উপকূলরেখা</td><td id="stat_coast">—</td></tr>
              <tr><td>রাজধানী</td><td>ঢাকা</td></tr>
            </table>
            <div style="margin-top:10px" class="notice">
              <strong>অ্যাডমিন:</strong> অ্যাডমিন প্যানেল থেকে এই মান গুলো সম্পাদন করা যাবে।
            </div>
          </div>
        </aside>
      </div>
    </section>

    <!-- AREA -->
    <section id="area" class="page">
      <div class="card">
        <h2>আয়তন</h2>
        <p>
          বাংলাদেশের মোট আয়তন প্রায় <strong id="about_area_display">148,460</strong> বর্গ কিলোমিটার (প্রায়)। এটি একটি তুলনামূলকভাবে ছোট দেশ হলেও অত্যন্ত জনবহুল এবং কৃষি-ভিত্তিক অর্থনীতি বিশিষ্ট।
        </p>

        <h3>বিস্তৃত ব্যাখ্যা</h3>
        <p>
          বাংলাদেশের ভূখণ্ডের বেশিরভাগই সমতল ও প্লাবনভূমি। নদীর তলা ও বানিজ্যিক নদীনালার পলি জমাটের কারণে মাটি উর্বর। দেশের আয়তন ও জনসংখ্যার কারণে জমির ব্যবহার অত্যন্ত ঘন; ফলে নগরায়ন, কৃষি ও অবকাঠামোগত চ্যালেঞ্জগুলো গুরুত্বপূর্ণ।
        </p>

        <h3>আয়তন সম্পর্কিত বিষয়</h3>
        <ul>
          <li>ভূখণ্ড: প্রধানত প্লাবনভূমি</li>
          <li>মাটি: নদীর পলি দ্বারা উর্বর</li>
          <li>চ্যালেঞ্জ: বন্যা, নদীভাঙন</li>
        </ul>
      </div>
    </section>

    <!-- BORDER -->
    <section id="border" class="page">
      <div class="card">
        <h2>সীমান্ত দৈর্ঘ্য</h2>
        <p>
          বাংলাদেশের মোট স্থলসীমান্ত প্রায় <strong id="about_land_display">4,413</strong> কিলোমিটার। এর মধ্যে ভারতের সাথে প্রায় <strong id="about_india_display">4,096</strong> কিমি ও মিয়ানমারের সাথে প্রায় <strong id="about_myanmar_display">271</strong> কিমি সীমান্ত রয়েছে। উপকূলরেখা প্রায় <strong id="about_coast_display">580</strong> কিলোমিটার।
        </p>

        <h3>বিস্তারিত</h3>
        <p>
          ভারতের সাথে সীমান্তটি দেশের উত্তর, পশ্চিম এবং পূর্ব সীমান্তসংলগ্ন এলাকাগুলো জুড়ে বিস্তৃত। মিয়ানমারের সাথে সীমান্তটি দক্ষিণ-পূর্ব দিকে অবস্থিত। দুই দেশের সীমান্ত এলাকায় প্রায়শই কৃষি, পণ্যবহন ও পারস্পরিক সামাজিক সম্পর্কের বৈচিত্র্য দেখা যায়।
        </p>
      </div>
    </section>

    <!-- GEO -->
    <section id="geo" class="page">
      <div class="card">
        <h2>ভূগোল</h2>
        <p id="geo_text">
          বাংলাদেশ মূলত সমতল প্লাবনভূমির দেশ। গঙ্গা–ব্রহ্মপুত্র–মেঘনা নদীগুলো দেশের ভূপ্রকৃতির প্রধান উপাদান। দেশের দক্ষিণাংশে বঙ্গোপসাগরের উপকূল এবং সুন্দরবন ম্যানগ্রোভ বন রয়েছে; সিলেট ও পার্বত্য চট্টগ্রামে উঁচু ভূমি ও পাহাড় দেখা যায়।
        </p>

        <h3>নদী ও জলবায়ু</h3>
        <p>
          নদী ব্যবস্থার কারণে বাংলাদেশ বন্যা প্রবণ। বর্ষাকালে প্রচুর বৃষ্টি হয়। জলবায়ু সাধারণত উষ্ণ ও আর্দ্র, ঋতু হিসেবে বর্ষা, সরত, শীত ইত্যাদি দেশীয় রীতিতে দেখা যায়।
        </p>

        <h3>জিওগ্রাফিক চ্যালেঞ্জ</h3>
        <ul>
          <li>নদী ভাঙন (river erosion)</li>
          <li>বন্যা এবং সৃষ্টিকৃত প্লাবন</li>
          <li>উত্তরাঞ্চলের শীতল অঞ্চল ও দক্ষিণাঞ্চলের উপকূলীয় লবণাক্ত মাটি</li>
        </ul>
      </div>
    </section>

    <!-- ADMIN INFO -->
    <section id="admin_info" class="page">
      <div class="card">
        <h2>প্রশাসন ও রাজনীতি</h2>
        <p>
          বাংলাদেশ একটি সংসদীয় গণতন্ত্র। রাষ্ট্রপতি রাষ্ট্রের প্রধান হলেও প্রধান কার্যত নির্বাহী ক্ষমতা প্রধানমন্ত্রীর উপর নির্ভরশীল। কেন্দ্রীয় সরকার, স্থানীয় সরকার (উপজেলা, পৌরসভা, জেলা) ইত্যাদি প্রশাসনিক একক রয়েছে।
        </p>

        <h3>প্রধান সংবিধানগত উপাদান</h3>
        <ul>
          <li>সংবিধান: ১৯৭২ সালে গৃহীত (কিছু সংশোধনী হয়েছে)</li>
          <li>প্রধানমন্ত্রীর কার্যাবলী: নির্বাহী ও প্রশাসনিক নেতৃত্ব</li>
          <li>নির্বাচন: জাতীয় সংসদ নির্বাচন ও স্থানীয় নির্বাচন</li>
        </ul>
      </div>
    </section>

    <!-- ECONOMY -->
    <section id="economy" class="page">
      <div class="card">
        <h2>অর্থনীতি</h2>
        <p id="eco_text">
          বাংলাদেশের অর্থনীতি গত কয়েক দশকে দ্রুত বৃদ্ধি করেছে। কৃষি ঐতিহ্য আছে; কিন্তু রপ্তানীমুখী তৈরি পোশাক (RMG) শিল্প, রেমিট্যান্স, এবং সেবাখাত অর্থনীতিকে উল্লেখযোগ্যভাবে এগিয়ে সাহায্য করেছে।
        </p>

        <h3>প্রধান খাত</h3>
        <ul>
          <li>কৃষি: ধান, পাট, সবজি, চা, মৎস্য</li>
          <li>শিল্প: তৈরি পোশাক (RMG), চামড়া, ওষুধ</li>
          <li>সেবা: ব্যাংকিং, টেলিকম, আইটি/আইটিইএস</li>
          <li>রেমিট্যান্স: প্রবাসী শ্রমিকদের প্রেরিত অর্থ অর্থনীতিতে বড় অবদান রাখে</li>
        </ul>

        <h3>চ্যালেঞ্জ ও সম্ভাবনা</h3>
        <p>
          অবকাঠামো উন্নয়ন, বেকারত্ব হ্রাস, শিক্ষা ও দক্ষতা বৃদ্ধি এবং পরিবেশগত ঝুঁকি মোকাবিলা—এসব মূল চ্যালেঞ্জ। আইটি, সবুজ শক্তি ও রপ্তানি-বৃদ্ধি সম্ভাব্য ক্ষেত্র।
        </p>
      </div>
    </section>

    <!-- CULTURE -->
    <section id="culture" class="page">
      <div class="card">
        <h2>সংস্কৃতি</h2>
        <p id="cul_text">
          বাংলা ভাষা, সাহিত্য, সংগীত, নাচ ও রীতিবিবরণ বাংলাদেশের আত্মা। ভাষা আন্দোলন ও ২১শে ফেব্রুয়ারি (একুশে ফেব্রুয়ারি) একটি গৌরবোজ্জ্বল অধ্যায়; পহেলা বৈশাখ (নতুন বাংলা বছর) জাতীয় উৎসব হিসেবে ব্যাপকভাবে পালিত হয়।
        </p>

        <h3>উৎসব ও খাদ্য</h3>
        <ul>
          <li>পহেলা বৈশাখ: বাংলা নববর্ষ</li>
          <li>একুশে ফেব্রুয়ারি: ভাষা শহীদ দিবস</li>
          <li>ঈদ, দুর্গাপূজা: প্রধান ধর্মীয় উৎসব</li>
          <li>খাদ্যসংস্কৃতি: ইলিশ মাছ, পান্তা ভাত, মিষ্টি ও লোকাল রান্না</li>
        </ul>
      </div>
    </section>

    <!-- TOURISM -->
    <section id="tourism" class="page">
      <div class="card">
        <h2>পর্যটন</h2>
        <p id="tour_text">
          বাংলাদেশে পর্যটনের জন্য অসাধারণ স্থান রয়েছে। কক্সবাজার বিশ্বের দীর্ঘতম প্রাকৃতিক সমুদ্রসৈকত; সুন্দরবন রয়েল বেঙ্গল টাইগারের আবাস; সিলেটের চা-বাগান, জাফলং-এর পাথর-নদীপথ; পার্বত্য চট্টগ্রামের পাহাড় ও বান্দরবান—
          প্রত্যেকটিই স্বতন্ত্র আকর্ষণ।
        </p>

        <h3>প্রধান দর্শনীয় স্থান</h3>
        <ul>
          <li>কক্সবাজার সমুদ্র সৈকত</li>
          <li>সুন্দরবন (ম্যানগ্রোভ বন)</li>
          <li>কেপ সেন্ট মার্টিন</li>
          <li>চা বাগান (সিলেট)</li>
          <li>বান্দরবান, রাঙ্গামাটি (পার্বত্য এলাকা)</li>
        </ul>
      </div>
    </section>

    <!-- DASHBOARD -->
    <section id="dashboard" class="page">
      <div class="card">
        <h2>ড্যাশবোর্ড</h2>
        <div class="grid" style="grid-template-columns:repeat(3,1fr)">
          <div class="card"><h3>মোট ভিজিট</h3><p id="kpiVisits">0</p></div>
          <div class="card"><h3>রেজিস্টার্ড ইউজার</h3><p id="kpiUsers">0</p></div>
          <div class="card"><h3>ফিডব্যাক মোট</h3><p id="kpiFeedback">0</p></div>
        </div>

        <h3 style="margin-top:12px">সাম্প্রতিক ফিডব্যাক</h3>
        <div id="recentFb"></div>
      </div>
    </section>

    <!-- FEEDBACK -->
    <section id="feedback" class="page">
      <div class="card">
        <h2>ফিডব্যাক</h2>
        <label>আপনার মন্তব্য / পরামর্শ</label>
        <textarea id="fbInput" rows="4" placeholder="আপনার মতামত লিখুন..."></textarea>
        <div class="toolbar"><button class="btn success" id="saveFbBtn">সেভ করুন</button><button class="btn ghost" id="exportFbBtn">CSV ডাউনলোড</button></div>

        <h3 style="margin-top:12px">সকল ফিডব্যাক</h3>
        <div id="fbList"></div>
      </div>
    </section>

    <!-- ADMIN PANEL -->
    <section id="admin" class="page" style="display:none">
      <div class="card">
        <h2>অ্যাডমিন প্যানেল — কনটেন্ট এডিট</h2>

        <div class="grid" style="grid-template-columns:1fr 1fr">
          <div>
            <label>মোট আয়তন (কিমি²)</label>
            <input id="ad_area" type="number" />
            <label>স্থল সীমান্ত মোট (কিমি)</label>
            <input id="ad_land" type="number" />
            <label>ভারত সীমান্ত (কিমি)</label>
            <input id="ad_india" type="number" />
            <label>মিয়ানমার সীমান্ত (কিমি)</label>
            <input id="ad_myanmar" type="number" />
            <label>উপকূলরেখা (কিমি)</label>
            <input id="ad_coast" type="number" />
          </div>

          <div>
            <label>আবাউট বর্ণনা (হোম পেজ)</label>
            <textarea id="ad_about_desc" rows="4"></textarea>
            <label>ভূগোল বর্ণনা</label>
            <textarea id="ad_geo_desc" rows="3"></textarea>
          </div>
        </div>

        <label style="margin-top:8px">অর্থনীতি বর্ণনা</label>
        <textarea id="ad_eco_desc" rows="2"></textarea>
        <label>সংস্কৃতি বর্ণনা</label>
        <textarea id="ad_cul_desc" rows="2"></textarea>
        <label>পর্যটন বর্ণনা</label>
        <textarea id="ad_tour_desc" rows="2"></textarea>

        <div class="toolbar" style="margin-top:12px">
          <button class="btn success" id="saveAdminBtn">সেভ করুন</button>
          <button class="btn ghost" id="exportJsonBtn">JSON ডাউনলোড</button>
          <button class="btn danger" id="resetBtn">রিসেট (ডেমো)</button>
        </div>

        <h3 style="margin-top:12px">ইউজার ম্যানেজমেন্ট</h3>
        <div id="userTableWrap" style="max-height:220px;overflow:auto;border:1px solid rgba(255,255,255,0.03);padding:8px;border-radius:8px"></div>
      </div>
    </section>

  </main>

  <footer>© <span id="year"></span> বাংলাদেশ তথ্য ভাণ্ডার -2025 &copy; Developed By SHAREA SOBJ SHISHIR</footer>
</div>

<script>
/* ===== Keys & default data ===== */
const KEYS = {
  data:'bd_data_complete_v1',
  users:'bd_users_complete_v1',
  session:'bd_session_complete_v1',
  fb:'bd_fb_complete_v1',
  visits:'bd_visits_complete_v1'
};

function defaultData(){
  return {
    about: {
      area: 148460,
      land: 4413,
      india: 4096,
      myanmar: 271,
      coast: 580,
      desc: 'বাংলাদেশ একটি ছোট অথচ ঘনবসতিপূর্ণ দেশ, নদীনির্ভর প্লাবনভূমি ও বৈচিত্র্যময় ভূগোল দ্বারা পরিপূর্ণ।'
    },
    geo: {
      desc: 'দেশটি গঙ্গা–ব্রহ্মপুত্র–মেঘনা নদী অনুঘটকে গঠিত প্লাবনভূমি; দক্ষিণে বঙ্গোপসাগরের উপকূল, উত্তর-পূর্বে চট্রগ্রাম পাহাড়ীয় অঞ্চল ও সিলেটের চা-বাগান রয়েছে।'
    },
    economy: { desc: 'প্রধান ভিত্তি কৃষি; রপ্তানি-নির্ভর তৈরি পোশাক শিল্প (RMG) দেশের আয়ের বড় উৎস। রেমিট্যান্স ও সেবা খাতও গুরুত্বপূর্ণ।' },
    culture: { desc: 'ভাষা-সংস্কৃতি, সাহিত্য ও লোকসংস্কৃতির সমৃদ্ধ ঐতিহ্য; পহেলা বৈশাখ, একুশে ফেব্রুয়ারি ইত্যাদি জাতীয় স্মৃতিসমূহ।' },
    tourism: { desc: 'কক্সবাজার, সুন্দরবন, কেপ সেন্ট মার্টিন, সিলেটের চা বাগান, পার্বত্য চট্টগ্রামের হ্রদ-চূড়া দর্শনীয়।' }
  };
}

/* ===== storage helpers ===== */
function read(key, fallback=null){
  try{
    const v = localStorage.getItem(key);
    return v ? JSON.parse(v) : fallback;
  }catch(e){ return fallback; }
}
function write(key, val){
  try{ localStorage.setItem(key, JSON.stringify(val)); }catch(e){}
}

/* ===== seed demo ===== */
function seed(){
  if(!read(KEYS.data)) write(KEYS.data, defaultData());
  if(!read(KEYS.users)) write(KEYS.users, [{ name:'Administrator', email:'admin@bd.gov', password:'123456', role:'admin' }]);
  if(read(KEYS.visits)===null) write(KEYS.visits, 0);
}

/* ===== formatting helpers ===== */
function bnFormat(n){
  try{ return Number(n).toLocaleString('bn-BD'); }catch(e){ return n; }
}

/* ===== UI routing ===== */
const tabs = document.querySelectorAll('.tab');
function go(route){
  document.querySelectorAll('section.page').forEach(s => s.classList.remove('active'));
  const el = document.getElementById(route);
  if(el) el.classList.add('active');
  tabs.forEach(t => t.classList.toggle('active', t.dataset.route === route));
  location.hash = route;
  render(); // refresh content
}

tabs.forEach(t => t.addEventListener('click', ()=> go(t.dataset.route)));

/* ===== auth ===== */
function currentUser(){ return read(KEYS.session, null); }
function updateAuthUI(){
  const u = currentUser();
  document.getElementById('userBadge').textContent = u ? (u.role === 'admin' ? 'Admin: '+u.name : 'User: '+u.name) : 'Guest';
  document.getElementById('logoutBtn').style.display = u ? 'inline-block' : 'none';
  // admin tab visibility
  const adminTabBtn = document.getElementById('adminTab');
  if(u && u.role === 'admin'){
    adminTabBtn.style.display = 'inline-block';
    document.getElementById('admin').style.display = 'block';
  } else {
    adminTabBtn.style.display = 'none';
    document.getElementById('admin').style.display = 'none';
  }
}

/* Simple modal-like login/signup using prompt (keeps UI simple) */
document.getElementById('openLogin').addEventListener('click', ()=> {
  const action = prompt('লগইন বা সাইনআপ? লিখুন: login / signup','login');
  if(!action) return;
  if(action === 'signup'){
    const name = prompt('নাম লিখুন (বিকল্প):','');
    const email = prompt('ইমেইল লিখুন:','');
    const pass = prompt('পাসওয়ার্ড লিখুন:','');
    if(!email || !pass){ alert('ইমেইল ও পাসওয়ার্ড দিতে হবে'); return; }
    const users = read(KEYS.users,[]);
    if(users.find(u => u.email === email)){ alert('এই ইমেইল ইতোমধ্যে আছে'); return; }
    users.push({ name: name || email.split('@')[0], email, password: pass, role:'user' });
    write(KEYS.users, users);
    alert('সাইনআপ সফল। এখন লগইন করুন।');
  } else {
    const email = prompt('ইমেইল:','');
    const pass = prompt('পাসওয়ার্ড:','');
    const users = read(KEYS.users, []);
    const u = users.find(x => x.email === email && x.password === pass);
    if(!u){ alert('ইমেইল/পাসওয়ার্ড মেলেনি'); return; }
    write(KEYS.session, { name: u.name, email: u.email, role: u.role, lastLogin: new Date().toLocaleString() });
    updateAuthUI();
    alert('লগইন সফল: ' + u.name);
    go('dashboard');
  }
});

document.getElementById('logoutBtn').addEventListener('click', ()=> {
  localStorage.removeItem(KEYS.session);
  updateAuthUI();
  go('home');
});

/* ===== render page content ===== */
function render(){
  const data = read(KEYS.data, defaultData());
  // stats quick
  document.getElementById('stat_area').textContent = bnFormat(data.about.area) + ' কিমি²';
  document.getElementById('stat_land').textContent = bnFormat(data.about.land) + ' কিমি';
  document.getElementById('stat_india').textContent = bnFormat(data.about.india) + ' কিমি';
  document.getElementById('stat_myanmar').textContent = bnFormat(data.about.myanmar) + ' কিমি';
  document.getElementById('stat_coast').textContent = bnFormat(data.about.coast) + ' কিমি';

  // area page
  document.getElementById('about_area_display').textContent = bnFormat(data.about.area);
  // border page
  document.getElementById('about_land_display').textContent = bnFormat(data.about.land);
  document.getElementById('about_india_display').textContent = bnFormat(data.about.india);
  document.getElementById('about_myanmar_display').textContent = bnFormat(data.about.myanmar);
  document.getElementById('about_coast_display').textContent = bnFormat(data.about.coast);

  // geo/econ/culture/tourism texts
  document.getElementById('geo_text').textContent = data.geo.desc;
  document.getElementById('eco_text').textContent = data.economy.desc;
  document.getElementById('cul_text').textContent = data.culture.desc;
  document.getElementById('tour_text').textContent = data.tourism.desc;

  // KPIs
  document.getElementById('kpiVisits').textContent = read(KEYS.visits,0) || 0;
  document.getElementById('kpiUsers').textContent = (read(KEYS.users,[]).length);
  document.getElementById('kpiFeedback').textContent = (read(KEYS.fb,[]).length);

  // recent feedback
  const fbs = read(KEYS.fb, []);
  const recent = fbs.slice(-5).reverse();
  document.getElementById('recentFb').innerHTML = recent.map(f => `<div style="padding:8px;border-bottom:1px solid rgba(255,255,255,0.03)"><small class="muted">${f.by} — ${new Date(f.time).toLocaleString()}</small><div>${escapeHtml(f.text)}</div></div>`).join('') || '<div class="muted">কোনো ফিডব্যাক নেই</div>';

  // full feedback list
  loadFeedbacks();

  // admin preload
  preloadAdminInputs();

  // user table
  renderUserTable();
}

/* ===== feedback functions ===== */
document.getElementById('saveFbBtn').addEventListener('click', ()=> {
  const text = document.getElementById('fbInput').value.trim();
  if(!text){ alert('ফিডব্যাক লিখুন'); return; }
  const arr = read(KEYS.fb, []);
  arr.push({ text, by: currentUser()?.email || 'Guest', time: new Date().toISOString() });
  write(KEYS.fb, arr);
  document.getElementById('fbInput').value = '';
  loadFeedbacks();
  render();
});

function loadFeedbacks(){
  const arr = read(KEYS.fb, []);
  const html = arr.map(f => `<div style="padding:8px;border-bottom:1px solid rgba(255,255,255,0.03)"><small class="muted">${f.by} — ${new Date(f.time).toLocaleString()}</small><div>${escapeHtml(f.text)}</div></div>`).reverse().join('');
  document.getElementById('fbList').innerHTML = html || '<div class="muted">কোনো ফিডব্যাক নেই</div>';
}

document.getElementById('exportFbBtn').addEventListener('click', ()=> {
  const arr = read(KEYS.fb, []);
  const rows = [['by','text','time'], ...arr.map(x => [x.by, x.text.replace(/\n/g,' '), x.time])];
  const csv = rows.map(r => r.map(v => `"${String(v||'').replace(/"/g,'""')}"`).join(',')).join('\n');
  const blob = new Blob([csv], { type: 'text/csv' });
  const url = URL.createObjectURL(blob); const a = document.createElement('a'); a.href = url; a.download = 'feedback.csv'; a.click(); URL.revokeObjectURL(url);
});

/* ===== admin edit/save ===== */
function preloadAdminInputs(){
  const d = read(KEYS.data, defaultData());
  if(!document.getElementById('ad_area')) return;
  document.getElementById('ad_area').value = d.about.area;
  document.getElementById('ad_land').value = d.about.land;
  document.getElementById('ad_india').value = d.about.india;
  document.getElementById('ad_myanmar').value = d.about.myanmar;
  document.getElementById('ad_coast').value = d.about.coast;
  document.getElementById('ad_about_desc').value = d.about.desc;
  document.getElementById('ad_geo_desc').value = d.geo.desc;
  document.getElementById('ad_eco_desc').value = d.economy.desc;
  document.getElementById('ad_cul_desc').value = d.culture.desc;
  document.getElementById('ad_tour_desc').value = d.tourism.desc;
}

document.getElementById('saveAdminBtn').addEventListener('click', ()=> {
  const d = read(KEYS.data, defaultData());
  d.about.area = Number(document.getElementById('ad_area').value || 0);
  d.about.land = Number(document.getElementById('ad_land').value || 0);
  d.about.india = Number(document.getElementById('ad_india').value || 0);
  d.about.myanmar = Number(document.getElementById('ad_myanmar').value || 0);
  d.about.coast = Number(document.getElementById('ad_coast').value || 0);
  d.about.desc = document.getElementById('ad_about_desc').value.trim();
  d.geo.desc = document.getElementById('ad_geo_desc').value.trim();
  d.economy.desc = document.getElementById('ad_eco_desc').value.trim();
  d.culture.desc = document.getElementById('ad_cul_desc').value.trim();
  d.tourism.desc = document.getElementById('ad_tour_desc').value.trim();
  write(KEYS.data, d);
  alert('কনটেন্ট আপডেট করা হয়েছে');
  render();
});

document.getElementById('exportJsonBtn').addEventListener('click', ()=> {
  const data = read(KEYS.data, defaultData());
  const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
  const url = URL.createObjectURL(blob); const a = document.createElement('a'); a.href = url; a.download = 'bd_data.json'; a.click(); URL.revokeObjectURL(url);
});

document.getElementById('resetBtn').addEventListener('click', ()=> {
  if(!confirm('সব ডাটা রিসেট হবে — নিশ্চিত?')) return;
  localStorage.removeItem(KEYS.data);
  localStorage.removeItem(KEYS.users);
  localStorage.removeItem(KEYS.session);
  localStorage.removeItem(KEYS.fb);
  localStorage.removeItem(KEYS.visits);
  seed();
  location.reload();
});

/* ===== users table for admin ===== */
function renderUserTable(){
  const users = read(KEYS.users, []);
  const sess = currentUser();
  if(!document.getElementById('userTableWrap')) return;
  if(users.length === 0){ document.getElementById('userTableWrap').innerHTML = '<div class="muted">কোনো ইউজার নেই</div>'; return; }
  const rows = users.map((u,i) => {
    const self = sess && sess.email === u.email;
    return `<div style="display:flex;gap:8px;align-items:center;padding:8px;border-bottom:1px solid rgba(255,255,255,0.03)">
      <div style="flex:1"><b>${escapeHtml(u.name)}</b><div class="muted">${escapeHtml(u.email)}</div></div>
      <div style="display:flex;gap:6px">${self?'<div class="muted">নিজ একাউন্ট</div>':`<button class="btn ghost" onclick="toggleRole(${i})">রোল টগল</button><button class="btn danger" onclick="deleteUser(${i})">ডিলিট</button>`}</div>
    </div>`;
  }).join('');
  document.getElementById('userTableWrap').innerHTML = rows;
}

window.toggleRole = function(i){
  const users = read(KEYS.users, []);
  if(!users[i]) return;
  users[i].role = users[i].role === 'admin' ? 'user' : 'admin';
  write(KEYS.users, users);
  renderUserTable();
  render();
}
window.deleteUser = function(i){
  if(!confirm('ইউজার মুছবেন?')) return;
  const users = read(KEYS.users, []);
  users.splice(i,1);
  write(KEYS.users, users);
  renderUserTable();
  render();
}

/* ===== util ===== */
function escapeHtml(s){ if(!s) return ''; return s.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }

/* ===== init ===== */
function init(){
  seed();
  // bump visits
  write(KEYS.visits, (read(KEYS.visits,0) || 0) + 1);
  document.getElementById('year').textContent = new Date().getFullYear();
  // default route from hash
  const start = location.hash.replace('#','') || 'home';
  go(start);
  updateAuthUI();
  render();
  loadFeedbacks();
}

// Expose admin go if clicked tab
document.getElementById('adminTab').addEventListener('click', ()=> {
  // admin tab visible only when admin
  const u = currentUser();
  if(!u || u.role !== 'admin'){ alert('শুধুমাত্র অ্যাডমিন অ্যাকসেস'); return; }
  go('admin');
});

init();
</script>

