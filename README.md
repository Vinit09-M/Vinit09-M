<div align="center">
  <style>
    .gh-shell {
      width: 100%;
      max-width: 1200px;
      border: 1px solid #d0d7de;
      border-radius: 18px;
      overflow: hidden;
      background: #f6f8fa;
      box-shadow: 0 8px 30px rgba(0,0,0,0.08);
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
      margin: 24px auto;
    }

    .gh-topbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      background: #f1f3f5;
      border-bottom: 1px solid #d0d7de;
      padding: 10px 16px;
      height: 54px;
      box-sizing: border-box;
    }

    .browser-left {
      display: flex;
      align-items: center;
      gap: 12px;
      min-width: 120px;
    }

    .traffic {
      display: flex;
      gap: 8px;
    }

    .dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      display: inline-block;
    }

    .dot.red { background: #ff5f57; }
    .dot.yellow { background: #ffbd2e; }
    .dot.green { background: #28c840; }

    .addressbar {
      flex: 1;
      max-width: 700px;
      height: 32px;
      background: #fff;
      border: 1px solid #d0d7de;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #5c6470;
      font-size: 14px;
      font-weight: 500;
      padding: 0 12px;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
    }

    .browser-right {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .browser-icon {
      width: 28px;
      height: 28px;
      border: 1px solid #d0d7de;
      border-radius: 8px;
      background: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #57606a;
      font-size: 12px;
    }

    .gh-tabs {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 12px 16px;
      background: #f6f8fa;
      border-bottom: 1px solid #d0d7de;
      gap: 16px;
      flex-wrap: wrap;
    }

    .nav-tabs {
      display: flex;
      align-items: center;
      gap: 18px;
      flex-wrap: wrap;
      font-size: 14px;
      color: #24292f;
    }

    .nav-tab {
      display: flex;
      align-items: center;
      gap: 6px;
      padding: 6px 8px;
      border-radius: 8px;
      font-weight: 500;
      opacity: 0.9;
    }

    .nav-tab.active {
      background: #ffffff;
      border: 1px solid #d0d7de;
    }

    .searchbox {
      display: flex;
      align-items: center;
      gap: 8px;
      border: 1px solid #d0d7de;
      background: #fff;
      border-radius: 8px;
      padding: 7px 11px;
      min-width: 240px;
      max-width: 300px;
      flex: 1;
      justify-content: flex-end;
    }

    .searchbox input {
      border: none;
      outline: none;
      background: transparent;
      font-size: 14px;
      width: 100%;
      color: #57606a;
    }

    .gh-main {
      display: grid;
      grid-template-columns: 290px 1fr;
      background: #ffffff;
    }

    .profile-sidebar {
      padding: 24px 18px 18px 18px;
      background: #f6f8fa;
      border-right: 1px solid #d0d7de;
    }

    .profile-avatar-wrap {
      display: flex;
      justify-content: center;
    }

    .profile-avatar {
      width: 220px;
      height: 220px;
      border-radius: 50%;
      border: 4px solid #1f2328;
      object-fit: cover;
      background: #fff;
      box-shadow: inset 0 0 0 2px rgba(0,0,0,0.05);
    }

    .profile-name {
      margin-top: 18px;
      font-size: 22px;
      font-weight: 700;
      color: #24292f;
      text-align: left;
    }

    .username {
      margin-top: 6px;
      font-size: 18px;
      color: #57606a;
      text-align: left;
    }

    .follow-btn {
      margin-top: 18px;
      width: 100%;
      height: 38px;
      border: 1px solid #d0d7de;
      background: #f6f8fa;
      border-radius: 8px;
      font-size: 15px;
      font-weight: 600;
      color: #24292f;
      cursor: pointer;
    }

    .bio {
      margin-top: 18px;
      font-size: 18px;
      line-height: 1.6;
      color: #24292f;
      text-align: left;
      font-style: italic;
    }

    .followers {
      margin-top: 18px;
      color: #57606a;
      font-size: 14px;
      text-align: left;
    }

    .sidebar-divider {
      border-top: 1px solid #d0d7de;
      margin-top: 18px;
      padding-top: 18px;
      color: #24292f;
      font-weight: 600;
      font-size: 14px;
      text-align: left;
    }

    .main-panel {
      padding: 22px 28px 20px 28px;
      background: #fff;
    }

    .file-title {
      font-size: 14px;
      color: #57606a;
      margin-bottom: 12px;
      font-weight: 500;
      text-align: left;
    }

    .header-block {
      padding: 14px 18px;
      background: #f6f8fa;
      border: 1px solid #d0d7de;
      border-radius: 12px;
      text-align: center;
    }

    .tag-row {
      display: flex;
      gap: 10px;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 10px;
      margin-bottom: 12px;
    }

    .tag {
      display: inline-block;
      padding: 7px 12px;
      border-radius: 8px;
      font-size: 12px;
      font-weight: 700;
      color: white;
      background: #1f2328;
      letter-spacing: 0.08em;
    }

    .tag.star { background: linear-gradient(90deg, #f59e0b, #f97316); }
    .tag.follow { background: linear-gradient(90deg, #10b981, #3b82f6); }

    .name-green {
      font-size: 54px;
      font-weight: 700;
      font-family: "Georgia", serif;
      letter-spacing: 0.02em;
      color: #00d76a;
      margin: 6px 0 0;
      text-shadow: 0 0 1px rgba(0,0,0,0.08);
    }

    .contrib-box {
      margin-top: 18px;
      background: #f6f8fa;
      border: 1px solid #d0d7de;
      border-radius: 12px;
      padding: 14px 16px 8px;
    }

    .contrib-grid {
      display: grid;
      grid-template-columns: repeat(52, 11px);
      grid-auto-rows: 11px;
      gap: 3px;
      justify-content: center;
      margin-top: 10px;
      margin-bottom: 6px;
    }

    .cell {
      width: 11px;
      height: 11px;
      background: #ebedf0;
      border-radius: 2px;
    }

    .cell.l1 { background: #9be9a8; }
    .cell.l2 { background: #40c463; }
    .cell.l3 { background: #30a14e; }
    .cell.l4 { background: #216e39; }

    .legend {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      gap: 8px;
      margin-top: 8px;
      color: #57606a;
      font-size: 12px;
    }

    .legend-swatch {
      width: 10px;
      height: 10px;
      border-radius: 2px;
      display: inline-block;
      background: #ebedf0;
    }

    .legend-swatch.l1 { background: #9be9a8; }
    .legend-swatch.l2 { background: #40c463; }
    .legend-swatch.l3 { background: #30a14e; }
    .legend-swatch.l4 { background: #216e39; }

    .section-title {
      margin-top: 18px;
      background: #f6f8fa;
      border: 1px solid #d0d7de;
      border-radius: 12px;
      padding: 12px 18px;
      font-size: 18px;
      font-weight: 700;
      color: #24292f;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, minmax(180px, 1fr));
      gap: 14px;
      margin-top: 18px;
    }

    .mini-card {
      border: 1px solid #d0d7de;
      border-radius: 12px;
      background: #fff;
      padding: 16px;
      text-align: left;
      box-shadow: 0 1px 0 rgba(31,35,40,0.04);
    }

    .mini-card h4 {
      margin: 0 0 8px;
      font-size: 15px;
      color: #24292f;
    }

    .mini-card p {
      margin: 0;
      color: #57606a;
      line-height: 1.5;
      font-size: 13px;
    }

    @media (max-width: 980px) {
      .gh-main {
        grid-template-columns: 1fr;
      }
      .profile-sidebar {
        border-right: none;
        border-bottom: 1px solid #d0d7de;
      }
      .cards {
        grid-template-columns: 1fr;
      }
      .name-green {
        font-size: 36px;
      }
    }
  </style>

  <div class="gh-shell">
    <div class="gh-topbar">
      <div class="browser-left">
        <div class="traffic">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
        </div>
      </div>

      <div class="addressbar">
        https://github.com/usualdork
      </div>

      <div class="browser-right">
        <div class="browser-icon">⌂</div>
        <div class="browser-icon">＋</div>
        <div class="browser-icon">⚙</div>
      </div>
    </div>

    <div class="gh-tabs">
      <div class="nav-tabs">
        <div class="nav-tab active">📁 Repositories <strong>(21)</strong></div>
        <div class="nav-tab">📦 Projects</div>
        <div class="nav-tab">📦 Packages</div>
        <div class="nav-tab">⭐ Stars <strong>(1)</strong></div>
      </div>

      <div class="searchbox">
        <span>🔍</span>
        <input type="text" value="Type / to search" aria-label="Search" />
      </div>
    </div>

    <div class="gh-main">
      <aside class="profile-sidebar">
        <div class="profile-avatar-wrap">
          <img
            class="profile-avatar"
            src="https://avatars.githubusercontent.com/u/131380708?v=4"
            alt="usualdork avatar"
          />
        </div>

        <div class="profile-name">Manish Tripathy</div>
        <div class="username">usualdork</div>

        <button class="follow-btn">Follow</button>

        <div class="bio">
          I’ve got 99 problems, but a compiler ain’t one.
        </div>

        <div class="followers">
          <strong>23</strong> followers · <strong>0</strong> following
        </div>

        <div class="sidebar-divider">Achievements</div>
      </aside>

      <main class="main-panel">
        <div class="file-title">usualdork / README.md</div>

        <div class="header-block">
          <div class="tag-row">
            <span class="tag">OWASP</span>
            <span class="tag">OSINT STANDARD (PROJECT LEADER) | MARITIME SECURITY</span>
          </div>

          <div class="tag-row">
            <span class="tag star">⭐ STARS 149</span>
            <span class="tag follow">👥 FOLLOWERS 23</span>
          </div>

          <div class="name-green">Manish Trip</div>
        </div>

        <div class="contrib-box">
          <div class="contrib-grid">
            <span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l2"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell"></span><span class="cell"></span>

            <span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span>

            <span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l2"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell l2"></span><span class="cell l1"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell"></span><span class="cell l1"></span><span class="cell l2"></span><span class="cell l3"></span><span class="cell"></span><span class="cell"></span>
          </div>

          <div class="legend">
            <span class="legend-swatch"></span>
            <span class="legend-swatch l1"></span>
            <span class="legend-swatch l2"></span>
            <span class="legend-swatch l3"></span>
            <span class="legend-swatch l4"></span>
          </div>
        </div>

        <div class="section-title">🛡️ Professional Contributions</div>

        <div class="cards">
          <div class="mini-card">
            <h4>OWASP</h4>
            <p>Project leadership in Open Source Intelligence Standard and Maritime Security research initiatives.</p>
          </div>

          <div class="mini-card">
            <h4>AI / ML</h4>
            <p>Research-focused work in intelligent systems, automation, and threat analytics.</p>
          </div>

          <div class="mini-card">
            <h4>OSINT</h4>
            <p>Security-focused exploration of digital identity, cyber deception, and surveillance.</p>
          </div>
        </div>
      </main>
    </div>
  </div>
</div>

# About Me

I’m Manish Tripathy, also known as `usualdork`.

- Cybersecurity researcher
- AI/ML practitioner
- OSINT and digital intelligence enthusiast
- Open-source contributor
- Researcher in cyber deception and security analytics

## Featured Projects

- [SecRecon](https://github.com/usualdork/SecRecon)
- [APIScanner](https://github.com/usualdork/APIScanner)
- [surfaceaudit](https://github.com/usualdork/surfaceaudit)
- [InstagramOSINT](https://github.com/usualdork/InstagramOSINT)
- [VANGUARD](https://github.com/usualdork/VANGUARD)
- [EndlessClaude](https://github.com/usualdork/EndlessClaude)
- [AIWhisper](https://github.com/usualdork/AIWhisper)
- [AI-Chat-Assistant](https://github.com/usualdork/AI-Chat-Assistant)
- [ATT-CKforge](https://github.com/usualdork/ATT-CKforge)

## Research & Publications

- OSINT and SOCMINT analysis
- Social engineering and deceptive digital identities
- Threat actor attribution and cyber deception frameworks
- AI-driven security analytics and autonomous red teaming
- Computer vision and strategic pattern detection

## Tech Stack

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS" />
  <img src="https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="Azure" />
  <img src="https://img.shields.io/badge/Kali_Linux-268BEE?style=for-the-badge&logo=kalilinux&logoColor=white" alt="Kali Linux" />
  <img src="https://img.shields.io/badge/OWASP-000000?style=for-the-badge&logo=owasp&logoColor=white" alt="OWASP" />
</p>

## Connect

- GitHub: [@usualdork](https://github.com/usualdork)
- LinkedIn: [Manish Tripathy](https://linkedin.com/in/manishtripathy1)
- Website: [manishtripathy.ct.ws](http://manishtripathy.ct.ws/)
- Email: [manishyash.tripathy@gmail.com](mailto:manishyash.tripathy@gmail.com)

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=usualdork&show_icons=true&theme=radical&hide_border=true" />
</p>
