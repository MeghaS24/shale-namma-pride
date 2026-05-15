<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet"
          href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css">

    <title>Shale Namma Pride</title>

    <style>

        :root {
          --font-sans: Arial, sans-serif;

          --color-background-primary: #ffffff;
          --color-background-secondary: #f5f5f5;

          --color-text-primary: #111111;
          --color-text-secondary: #666666;

          --color-border-tertiary: #dddddd;

          --border-radius-lg: 16px;
          --border-radius-md: 12px;
        }

        * {
          box-sizing: border-box;
          margin: 0;
          padding: 0;
        }

        body {
          font-family: var(--font-sans);
          background: #f0f0f0;
          display: flex;
          justify-content: center;
          padding: 20px;
        }

        .app {
          width: 100%;
          max-width: 380px;
          background: white;
          min-height: 100vh;
          border-radius: 20px;
          overflow: hidden;
        }

        .status-bar {
          background: #1a7a4a;
          color: white;
          font-size: 12px;
          padding: 8px 14px;
          display: flex;
          justify-content: space-between;
        }

        .header {
          background: #1a7a4a;
          color: white;
          padding: 14px;
        }

        .header-top {
          display: flex;
          justify-content: space-between;
          align-items: center;
        }

        .school-name {
          font-size: 18px;
          font-weight: bold;
        }

        .school-sub {
          font-size: 12px;
          opacity: 0.8;
        }

        .lang-toggle {
          border: none;
          background: rgba(255,255,255,0.2);
          color: white;
          padding: 6px 12px;
          border-radius: 20px;
        }

        .nav {
          display: flex;
          border-bottom: 1px solid #ddd;
        }

        .nav-btn {
          flex: 1;
          border: none;
          background: white;
          padding: 12px;
          font-size: 12px;
        }

        .nav-btn.active {
          color: #1a7a4a;
          border-bottom: 2px solid #1a7a4a;
        }

        .screen {
          display: none;
          padding: 14px;
        }

        .screen.active {
          display: block;
        }

        .notice {
          background: #e8f5ee;
          padding: 12px;
          border-radius: 12px;
          margin-bottom: 12px;
        }

        .meal-card {
          background: #f5f5f5;
          padding: 14px;
          border-radius: 16px;
        }

        .meal-img {
          font-size: 50px;
          text-align: center;
          margin-bottom: 10px;
        }

        .meal-title {
          font-size: 16px;
          font-weight: bold;
        }

        .meal-items {
          display: flex;
          flex-wrap: wrap;
          gap: 6px;
          margin-top: 10px;
        }

        .meal-item {
          background: white;
          border: 1px solid #ddd;
          border-radius: 20px;
          padding: 5px 10px;
          font-size: 12px;
        }

        .section-title {
          margin: 16px 0 10px;
          font-size: 13px;
          font-weight: bold;
        }

        .gallery-grid {
          display: grid;
          grid-template-columns: repeat(2,1fr);
          gap: 10px;
        }

        .gallery-item {
          border-radius: 12px;
          overflow: hidden;
        }

        .gallery-thumb {
          height: 100px;
          display: flex;
          justify-content: center;
          align-items: center;
          font-size: 40px;
        }

        .g-science { background: #d4eaf7; }
        .g-library { background: #f0e8fb; }
        .g-sports { background: #e8f5de; }
        .g-toilet { background: #fef0e0; }

        .gallery-label {
          background: rgba(0,0,0,0.6);
          color: white;
          padding: 6px;
          font-size: 12px;
        }

        .star-card {
          background: #f5f5f5;
          padding: 14px;
          border-radius: 16px;
          margin-bottom: 10px;
          display: flex;
          gap: 10px;
        }

        .avatar {
          width: 50px;
          height: 50px;
          border-radius: 50%;
          background: #1a7a4a;
          color: white;
          display: flex;
          align-items: center;
          justify-content: center;
          font-weight: bold;
        }

        .star-name {
          font-weight: bold;
        }

        .feedback-form {
          display: flex;
          flex-direction: column;
          gap: 10px;
        }

        textarea {
          padding: 10px;
          border-radius: 12px;
          border: 1px solid #ddd;
          height: 100px;
        }

        .submit-btn {
          background: #1a7a4a;
          color: white;
          border: none;
          padding: 12px;
          border-radius: 12px;
        }

        .lang-kn {
          display: none;
        }

        .kn-mode .lang-en {
          display: none;
        }

        .kn-mode .lang-kn {
          display: inline;
        }

        .kn-mode .lang-en-block {
          display: none;
        }

        .kn-mode .lang-kn-block {
          display: block;
        }

    </style>
</head>

<body>

<div class="app" id="app">

    <div class="status-bar">
        <span>9:17</span>
        <span>Shale Namma Pride</span>
        <span>🔋23%</span>
    </div>

    <div class="header">
        <div class="header-top">

            <div>
                <div class="school-name">
                    <span class="lang-en">GHS Konapur</span>
                    <span class="lang-kn">ಸ.ಪ್ರೌ.ಶಾಲೆ ಕೊನಾಪುರ</span>
                </div>

                <div class="school-sub">
                    <span class="lang-en">Govt High School</span>
                    <span class="lang-kn">ಸರ್ಕಾರಿ ಪ್ರೌಢಶಾಲೆ</span>
                </div>
            </div>

            <button class="lang-toggle" onclick="toggleLang()" id="langBtn">
                ಕ/E
            </button>

        </div>
    </div>

    <div class="nav">

        <button class="nav-btn active" onclick="showTab('meal',this)">
            <i class="ti ti-bowl-spoon"></i><br>
            Meal
        </button>

        <button class="nav-btn" onclick="showTab('gallery',this)">
            <i class="ti ti-photo"></i><br>
            Facility
        </button>

        <button class="nav-btn" onclick="showTab('stars',this)">
            <i class="ti ti-star"></i><br>
            Stars
        </button>

        <button class="nav-btn" onclick="showTab('feedback',this)">
            <i class="ti ti-message"></i><br>
            Feedback
        </button>

    </div>

    <div class="screen active" id="screen-meal">

        <div class="notice">
            Today's meal updated ✓
        </div>

        <div class="meal-card">

            <div class="meal-img">🍛</div>

            <div class="meal-title">
                Thursday Mid-Day Meal
            </div>

            <div class="meal-items">
                <div class="meal-item">🍚 Rice</div>
                <div class="meal-item">🫘 Sambar</div>
                <div class="meal-item">🥬 Palya</div>
                <div class="meal-item">🍌 Banana</div>
                <div class="meal-item">🥛 Milk</div>
            </div>

        </div>

    </div>

    <div class="screen" id="screen-gallery">

        <div class="section-title">
            Facilities
        </div>

        <div class="gallery-grid">

            <div class="gallery-item">
                <div class="gallery-thumb g-science">🔬</div>
                <div class="gallery-label">Science Lab</div>
            </div>

            <div class="gallery-item">
                <div class="gallery-thumb g-library">📚</div>
                <div class="gallery-label">Library</div>
            </div>

            <div class="gallery-item">
                <div class="gallery-thumb g-sports">⚽</div>
                <div class="gallery-label">Sports Ground</div>
            </div>

            <div class="gallery-item">
                <div class="gallery-thumb g-toilet">🚿</div>
                <div class="gallery-label">Washroom</div>
            </div>

        </div>

    </div>

    <div class="screen" id="screen-stars">

        <div class="star-card">

            <div class="avatar">PK</div>

            <div>
                <div class="star-name">
                    Priya Kumari
                </div>

                <div>
                    District Math Topper
                </div>
            </div>

        </div>

        <div class="star-card">

            <div class="avatar">RS</div>

            <div>
                <div class="star-name">
                    Raju Swamy
                </div>

                <div>
                    Kabaddi Champion
                </div>
            </div>

        </div>

    </div>

    <div class="screen" id="screen-feedback">

        <div class="feedback-form">

<textarea
        id="fbText"
        placeholder="Enter feedback">
</textarea>

            <button class="submit-btn" onclick="submitFeedback()">
                Submit Feedback
            </button>

            <div id="successMsg"
                 style="display:none;color:green;">
                Feedback Submitted ✓
            </div>

        </div>

    </div>

</div>

<script>

    function showTab(name,btn){

    document.querySelectorAll('.screen')
    .forEach(s=>s.classList.remove('active'));

    document.querySelectorAll('.nav-btn')
    .forEach(b=>b.classList.remove('active'));

    document.getElementById('screen-'+name)
    .classList.add('active');

    btn.classList.add('active');
    }

    let kn = false;

    function toggleLang(){

    kn=!kn;

    document.getElementById('app')
    .classList.toggle('kn-mode',kn);

    document.getElementById('langBtn')
    .innerText = kn ? 'E/ಕ' : 'ಕ/E';
    }

    function submitFeedback(){

    const text =
    document.getElementById('fbText').value;

    if(text.trim()===""){
    alert("Please enter feedback");
    return;
    }

    document.getElementById('successMsg')
    .style.display='block';

    document.getElementById('fbText').value='';

    setTimeout(()=>{
    document.getElementById('successMsg')
    .style.display='none';
    },3000);

    }

</script>

</body>
</html>

