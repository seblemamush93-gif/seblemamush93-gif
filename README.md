<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>seblemamush93 · attractive github profile</title>
    <!-- Font Awesome 6 (free) + Google Fonts for premium look -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0b1017;  /* dark space-like background */
            font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
            display: flex;
            justify-content: center;
            padding: 2rem 1.5rem;
            min-height: 100vh;
            background-image: radial-gradient(circle at 25% 30%, rgba(45, 156, 219, 0.08) 0%, transparent 30%),
                              radial-gradient(circle at 75% 70%, rgba(145, 70, 255, 0.06) 0%, transparent 35%);
        }

        /* main profile card – glassmorphic + subtle border */
        .github-card {
            max-width: 1100px;
            width: 100%;
            background: rgba(18, 24, 31, 0.85);
            backdrop-filter: blur(16px) saturate(200%);
            -webkit-backdrop-filter: blur(16px);
            border-radius: 3rem;
            border: 1px solid rgba(255, 255, 255, 0.03);
            box-shadow: 0 30px 60px -20px #000000cc, 0 0 0 1px rgba(62, 128, 240, 0.2) inset;
            padding: 2.5rem;
        }

        /* HEADER section: avatar + title + meta */
        .profile-head {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            align-items: center;
            margin-bottom: 2.2rem;
        }

        .avatar-container {
            position: relative;
        }

        .avatar-ring {
            width: 120px;
            height: 120px;
            border-radius: 50% 40% 60% 40% / 40% 50% 50% 60%;
            background: linear-gradient(125deg, #1f8efa, #a371f7);
            padding: 3px;
            box-shadow: 0 20px 30px -10px #1f8efa80;
            transition: transform 0.3s ease;
        }

        .avatar-ring:hover {
            transform: rotate(3deg) scale(1.02);
        }

        .avatar-img {
            width: 100%;
            height: 100%;
            border-radius: inherit;
            background: #1a212b;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.8rem;
            font-weight: 600;
            color: #ced5df;
            border: 2px solid rgba(0, 0, 0, 0.2);
        }

        .status-badge {
            position: absolute;
            bottom: 12px;
            right: 12px;
            width: 20px;
            height: 20px;
            background: #3fb950;
            border-radius: 50%;
            border: 3px solid #0f151c;
            box-shadow: 0 0 0 2px #3fb95060;
        }

        .head-details h1 {
            font-size: 3.2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(140deg, #ffffff, #b7cbee);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.1;
        }

        .head-details .user-handle {
            font-size: 1.3rem;
            font-weight: 400;
            color: #949fa8;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin: 0.2rem 0 0.8rem 0;
        }

        .user-handle i {
            color: #6e8699;
        }

        .follow-pill {
            background: rgba(31, 142, 250, 0.1);
            border: 1px solid #1f8efa30;
            color: #7cb3ff;
            padding: 0.6rem 2rem;
            border-radius: 40px;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            backdrop-filter: blur(6px);
            transition: 0.15s;
            cursor: default;
            font-size: 0.95rem;
        }

        .follow-pill i {
            font-size: 1rem;
        }

        /* stats row with modern cards */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem 2.5rem;
            background: rgba(8, 14, 21, 0.6);
            border-radius: 2.5rem;
            padding: 1.5rem 2.2rem;
            margin: 2.2rem 0 2rem 0;
            border: 1px solid #303b48;
            backdrop-filter: blur(8px);
        }

        .stat-block {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .stat-icon {
            width: 48px;
            height: 48px;
            background: #101a24;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: #7fb7f0;
            border: 1px solid #2e4b6b;
        }

        .stat-numbers {
            display: flex;
            flex-direction: column;
        }

        .stat-num {
            font-size: 2rem;
            font-weight: 700;
            color: #edf3f8;
            line-height: 1.3;
        }

        .stat-label {
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: #8f9daa;
        }

        /* repository section heading */
        .repo-section-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin: 2.8rem 0 1.6rem 0;
        }

        .repo-section-header i {
            font-size: 2rem;
            color: #d29922;
        }

        .repo-section-header h2 {
            font-size: 1.9rem;
            font-weight: 600;
            color: #e6edf3;
        }

        .repo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
        }

        /* repo card – clean and pinned style */
        .repo-card {
            background: rgba(16, 22, 29, 0.8);
            backdrop-filter: blur(8px);
            border: 1px solid #2f3a48;
            border-radius: 2rem;
            padding: 1.5rem 1.4rem 1.4rem 1.6rem;
            transition: 0.2s;
            box-shadow: 0 10px 20px -8px #00000060;
        }

        .repo-card:hover {
            border-color: #4588d0;
            transform: translateY(-5px);
            background: #1a2330;
        }

        .repo-name {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            margin-bottom: 0.5rem;
        }

        .repo-name i {
            color: #6e8699;
            font-size: 1.1rem;
        }

        .repo-name a {
            font-weight: 600;
            font-size: 1.3rem;
            color: #58a6ff;
            text-decoration: none;
        }

        .repo-name a:hover {
            text-decoration: underline;
        }

        .repo-badge {
            background: #2d4053;
            font-size: 0.7rem;
            padding: 0.2rem 0.7rem;
            border-radius: 20px;
            color: #b1c9e0;
            margin-left: 0.5rem;
            font-weight: 500;
            letter-spacing: -0.2px;
        }

        .repo-description {
            color: #abb7c4;
            font-size: 0.9rem;
            line-height: 1.5;
            margin: 0.8rem 0 1.2rem 0;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .repo-footer {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 1.2rem;
            font-size: 0.8rem;
            color: #99a7b5;
        }

        .lang-tag {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .color-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #f1e05a; /* default */
        }

        .star-count, .fork-count {
            display: flex;
            align-items: center;
            gap: 4px;
        }

        /* custom pin message based on your png */
        .pin-note {
            background: #131c26;
            border-radius: 3rem;
            padding: 0.8rem 2rem;
            display: flex;
            align-items: center;
            gap: 15px;
            flex-wrap: wrap;
            margin: 2rem 0 1rem 0;
            border: 1px dashed #3b4d5e;
        }

        .pin-note i {
            color: #f1b44c;
            font-size: 1.3rem;
        }

        .pin-note span {
            color: #ccdcec;
            font-weight: 400;
        }

        .pin-note .badge {
            background: #1e5c8b30;
            color: #6cb2f2;
            padding: 0.3rem 1.2rem;
            border-radius: 30px;
            border: 1px solid #236b9c;
            font-size: 0.9rem;
            margin-left: auto;
        }

        /* bottom meta (popular / customize pins) */
        .footer-extra {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin-top: 3rem;
            border-top: 1px solid #2e3845;
            padding-top: 2rem;
        }

        .social-links a {
            color: #8696a8;
            font-size: 1.6rem;
            margin-right: 2rem;
            transition: 0.1s;
        }

        .social-links a:hover {
            color: #7cb3ff;
        }

        .tip {
            color: #8393a3;
            font-size: 0.9rem;
            background: #1a232f;
            padding: 0.5rem 1.5rem;
            border-radius: 40px;
            border: 1px solid #3e4d5d;
        }

        .tip i {
            color: #dbb13b;
        }

        /* responsive */
        @media (max-width: 700px) {
            .github-card { padding: 1.8rem; }
            .head-details h1 { font-size: 2.5rem; }
        }
    </style>
</head>
<body>
    <div class="github-card">
        <!-- header area with avatar + handle + follow -->
        <div class="profile-head">
            <div class="avatar-container">
                <div class="avatar-ring">
                    <div class="avatar-img">
                        SM
                    </div>
                </div>
                <div class="status-badge" title="active"></div>
            </div>
            <div class="head-details">
                <div class="user-handle">
                    <i class="fab fa-github"></i> seblemamush93-gif
                </div>
                <h1>Seble Mamush</h1>
                <div style="margin-top: 1rem;">
                    <span class="follow-pill"><i class="fas fa-user-plus"></i> Follow</span>
                </div>
            </div>
        </div>

        <!-- stats row (based on typical GitHub numbers) -->
        <div class="stats-row">
            <div class="stat-block">
                <div class="stat-icon"><i class="fas fa-code-branch"></i></div>
                <div class="stat-numbers">
                    <span class="stat-num">37</span>
                    <span class="stat-label">repositories</span>
                </div>
            </div>
            <div class="stat-block">
                <div class="stat-icon"><i class="fas fa-star"></i></div>
                <div class="stat-numbers">
                    <span class="stat-num">192</span>
                    <span class="stat-label">stars</span>
                </div>
            </div>
            <div class="stat-block">
                <div class="stat-icon"><i class="fas fa-users"></i></div>
                <div class="stat-numbers">
                    <span class="stat-num">84</span>
                    <span class="stat-label">followers</span>
                </div>
            </div>
            <div class="stat-block">
                <div class="stat-icon"><i class="fas fa-heart"></i></div>
                <div class="stat-numbers">
                    <span class="stat-num">23</span>
                    <span class="stat-label">following</span>
                </div>
            </div>
        </div>

        <!-- Popular repositories + customize your pins (exactly like your png vibe) -->
        <div class="repo-section-header">
            <i class="fas fa-thumbtack fa-rotate-45"></i>
            <h2>Popular repositories</h2>
            <span style="margin-left: auto; background: #263340; padding: 0.3rem 1.2rem; border-radius: 30px; color: #b1cef0; font-size: 0.85rem;"><i class="fas fa-pencil-alt"></i> customize pins</span>
        </div>

        <!-- pinned repos grid – based on your screenshot names (new, wev, mon, your, wer.html) plus modern twist -->
        <div class="repo-grid">
            <!-- new (HTML) -->
            <div class="repo-card">
                <div class="repo-name">
                    <i class="far fa-repository"></i>
                    <a href="#">new</a>
                    <span class="repo-badge">Public</span>
                </div>
                <div class="repo-description">
                    Fresh HTML5 boilerplate with accessibility and modern meta tags.
                </div>
                <div class="repo-footer">
                    <span class="lang-tag"><span class="color-dot" style="background: #e34c26;"></span> HTML</span>
                    <span class="star-count"><i class="far fa-star"></i> 24</span>
                    <span class="fork-count"><i class="fas fa-code-branch"></i> 8</span>
                </div>
            </div>

            <!-- wev (HTML) -->
            <div class="repo-card">
                <div class="repo-name">
                    <i class="far fa-repository"></i>
                    <a href="#">wev</a>
                    <span class="repo-badge">Public</span>
                </div>
                <div class="repo-description">
                    Experimental web components & custom elements – lightweight.
                </div>
                <div class="repo-footer">
                    <span class="lang-tag"><span class="color-dot" style="background: #e34c26;"></span> HTML</span>
                    <span class="star-count"><i class="far fa-star"></i> 17</span>
                    <span class="fork-count"><i class="fas fa-code-branch"></i> 3</span>
                </div>
            </div>

            <!-- mon (HTML) -->
            <div class="repo-card">
                <div class="repo-name">
                    <i class="far fa-repository"></i>
                    <a href="#">mon</a>
                    <span class="repo-badge">Public</span>
                </div>
                <div class="repo-description">
                    Monitoring dashboard – simple uptime checker with plain HTML/CSS/JS.
                </div>
                <div class="repo-footer">
                    <span class="lang-tag"><span class="color-dot" style="background: #e34c26;"></span> HTML</span>
                    <span class="star-count"><i class="far fa-star"></i> 9</span>
                    <span class="fork-count"><i class="fas fa-code-branch"></i> 2</span>
                </div>
            </div>

            <!-- your (CSS)  (your – CSS) -->
            <div class="repo-card">
                <div class="repo-name">
                    <i class="far fa-repository"></i>
                    <a href="#">your</a>
                    <span class="repo-badge">Public</span>
                </div>
                <div class="repo-description">
                    Personal design tokens & CSS utility classes – a tiny style system.
                </div>
                <div class="repo-footer">
                    <span class="lang-tag"><span class="color-dot" style="background: #563d7c;"></span> CSS</span>
                    <span class="star-count"><i class="far fa-star"></i> 42</span>
                    <span class="fork-count"><i class="fas fa-code-branch"></i> 6</span>
                </div>
            </div>

            <!-- wer.html (HTML)  (special) -->
            <div class="repo-card">
                <div class="repo-name">
                    <i class="far fa-repository"></i>
                    <a href="#">wer.html</a>
                    <span class="repo-badge">Public</span>
                </div>
                <div class="repo-description">
                    Single‑file HTML generative art piece – canvas + noise algorithm.
                </div>
                <div class="repo-footer">
                    <span class="lang-tag"><span class="color-dot" style="background: #e34c26;"></span> HTML</span>
                    <span class="star-count"><i class="far fa-star"></i> 33</span>
                    <span class="fork-count"><i class="fas fa-code-branch"></i> 5</span>
                </div>
            </div>

            <!-- extra sixth pin (like seblemamush93-gif repo itself as a bonus) -->
            <div class="repo-card">
                <div class="repo-name">
                    <i class="far fa-repository"></i>
                    <a href="#">seblemamush93-gif</a>
                    <span class="repo-badge">✨ special</span>
                </div>
                <div class="repo-description">
                    The one and only – profile README with animated GIFs & fun.
                </div>
                <div class="repo-footer">
                    <span class="lang-tag"><span class="color-dot" style="background: #f18a5a;"></span> MDX</span>
                    <span class="star-count"><i class="far fa-star"></i> 77</span>
                    <span class="fork-count"><i class="fas fa-code-branch"></i> 12</span>
                </div>
            </div>
        </div>

        <!-- additional line: "Customize your pins" exactly as in your PNG but nicer -->
        <div class="pin-note">
            <i class="fas fa-boxes-packing"></i>
            <span>⭐ <strong>Customize your pins</strong> — drag and drop your favorite repositories here.</span>
            <span class="badge"><i class="fas fa-sync-alt"></i> 6 pinned</span>
        </div>

        <!-- extra meta / social footer + tip -->
        <div class="footer-extra">
            <div class="social-links">
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fas fa-envelope"></i></a>
                <a href="#"><i class="fas fa-globe"></i></a>
            </div>
            <div class="tip">
                <i class="fas fa-magic"></i> seblemamush93-gif / README.md
            </div>
        </div>

        <!-- small decorative: contribution vibe -->
        <div style="margin-top: 1.8rem; display: flex; justify-content: flex-end; font-size: 0.85rem; color: #68788a;">
            <span><i class="fas fa-code"></i> 841 contributions in the last year </span>
        </div>
    </div>
</body>
</html>
