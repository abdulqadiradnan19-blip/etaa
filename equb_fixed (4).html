<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ticket Selling System</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
  <style>
    :root[data-theme="dark"] {
      --bg:#080d18;
      --surface:#0e1525;
      --card:#111b2e;
      --cardB:#162038;
      --border:#1d2e47;
      --text:#dce8f8;
      --muted:#7a96b8;
      --faint:#3d5070;
      --accent:#4d7cfe;
      --accentD:#3a64e8;
      --accentSoft:#0d1e3f;
      --green:#1fd16f;
      --greenSoft:#091f17;
      --orange:#fb923c;
      --orangeSoft:#201008;
      --red:#f45b5b;
      --redSoft:#200808;
      --purple:#b89aff;
      --purpleSoft:#160f2e;
      --inp:#080d18;
      --inpB:#1d2e47;
      --shadow:0 8px 32px rgba(0,0,0,.6);
      --hdr:rgba(8,13,24,.93);
    }
    :root[data-theme="light"] {
      --bg:#eef2fb;
      --surface:#f5f8ff;
      --card:#fff;
      --cardB:#f8faff;
      --border:#dbe4f4;
      --text:#0d1626;
      --muted:#566a85;
      --faint:#a0b2c8;
      --accent:#3561f0;
      --accentD:#2548d4;
      --accentSoft:#e5edff;
      --green:#15a558;
      --greenSoft:#e6f9ee;
      --orange:#d96a0a;
      --orangeSoft:#fff3e6;
      --red:#d42b2b;
      --redSoft:#fde8e8;
      --purple:#6b30d4;
      --purpleSoft:#ede7ff;
      --inp:#f5f8ff;
      --inpB:#c8d4e8;
      --shadow:0 4px 20px rgba(53,97,240,.07);
      --hdr:rgba(238,242,251,.93);
    }
    *{ margin:0; padding:0; box-sizing:border-box; }
    body{ background:var(--bg); color:var(--text); font-family:'Inter','Segoe UI',sans-serif; min-height:100vh; transition:.25s; }
    header{ background:var(--hdr); border-bottom:1px solid var(--border); backdrop-filter:blur(12px); position:sticky; top:0; z-index:100; }
    .header-container{ max-width:1160px; margin:auto; height:60px; padding:0 20px; display:flex; justify-content:space-between; align-items:center; }
    main{ max-width:1160px; margin:auto; padding:28px 20px; }
    .card{ background:var(--card); border:1px solid var(--border); border-radius:14px; padding:22px 24px; box-shadow:var(--shadow); margin-bottom:16px; }
    .grid-2{ display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:16px; }
    .grid-stats{ display:grid; grid-template-columns:repeat(auto-fit,minmax(190px,1fr)); gap:14px; margin-bottom:26px; }
    .btn{ border:none; border-radius:10px; padding:11px 22px; font-size:14px; font-weight:600; cursor:pointer; display:inline-flex; align-items:center; justify-content:center; gap:6px; transition:.15s; }
    .btn:hover{ opacity:.9; }
    .btn-primary{ background:var(--accent); color:#fff; }
    .btn-green{ background:var(--green); color:#fff; }
    .btn-red{ background:var(--red); color:#fff; }
    .btn-orange{ background:var(--orange); color:#fff; }
    .btn-ghost{ background:transparent; border:1px solid var(--border); color:var(--muted); }
    .btn-sm{ padding:5px 12px; font-size:12px; border-radius:7px; }
    .lbl{ display:block; margin-bottom:6px; font-size:11px; font-weight:700; color:var(--muted); text-transform:uppercase; }
    .inp{ width:100%; background:var(--inp); border:1px solid var(--inpB); border-radius:10px; padding:11px 14px; font-size:14px; color:var(--text); outline:none; margin-bottom:14px; }
    .badge{ padding:3px 10px; border-radius:20px; font-size:11px; font-weight:700; }
    .badge-available{ background:var(--greenSoft); color:var(--green); }
    .badge-checking{ background:var(--orangeSoft); color:var(--orange); }
    .badge-sold{ background:var(--redSoft); color:var(--red); }
    .announcement-banner{ display:none; padding:9px 20px; text-align:center; background:var(--accentSoft); color:var(--accent); border-bottom:1px solid rgba(77,124,254,.2); }
    .ticket-grid{ display:grid; grid-template-columns:repeat(auto-fill,minmax(58px,1fr)); gap:5px; }
    .ticket-cell{ border-radius:8px; padding:6px 3px; text-align:center; cursor:pointer; border:1.5px solid transparent; transition:.15s; }
    .ticket-cell:hover{ transform:scale(1.03); }
    .ticket-dot{ width:5px; height:5px; border-radius:50%; margin:3px auto 0; }
    .table-responsive{ overflow-x:auto; }
    table{ width:100%; border-collapse:collapse; font-size:14px; }
    th{ padding:12px 16px; text-align:left; font-size:11px; color:var(--muted); text-transform:uppercase; }
    td{ padding:11px 16px; }
    tr{ border-bottom:1px solid var(--border); }
    .modal-backdrop{ position:fixed; inset:0; background:rgba(0,0,0,.55); display:none; align-items:center; justify-content:center; z-index:200; padding:20px; }
    .loading-view{ min-height:100vh; display:flex; justify-content:center; align-items:center; text-align:center; }
    .hidden{ display:none !important; }
    footer{ border-top:1px solid var(--border); padding:22px; text-align:center; color:var(--faint); margin-top:48px; font-size:13px; }
    @media(max-width:768px){
      .header-container{ flex-direction:column; gap:10px; height:auto; padding:15px; }
      .grid-2, .grid-stats{ grid-template-columns:1fr; }
      .ticket-grid{ grid-template-columns:repeat(auto-fill,minmax(48px,1fr)); }
      .btn{ width:100%; }
    }
  </style>
</head>
<body>

  <div id="loadingView" class="loading-view">
    <div>
      <div style="font-size: 48px; margin-bottom: 12px;">🎟️</div>
      <p style="color: var(--muted); font-size: 16px;" id="loadingText">Connecting to database…</p>
    </div>
  </div>

  <div id="appShell" class="hidden">
    
    <div id="announcementBanner" class="announcement-banner"></div>

    <header id="publicHeader">
      <div class="header-container">
        <div style="display: flex; align-items: center; gap: 10px;">
          <div style="width: 34px; height: 34px; background: var(--accent); border-radius: 9px; display: flex; align-items: center; justify-content: center; font-size: 17px;">🎟️</div>
          <div>
            <div style="font-weight: 800; font-size: 15px; letter-spacing: -0.4px;">Ticket Selling System</div>
            <div style="font-size: 10px; color: var(--muted);">Official Lottery Platform</div>
          </div>
        </div>
        <div style="display: flex; align-items: center; gap: 4px;">
          <button class="btn btn-ghost btn-sm nav-btn" data-target="home">🏠 Home</button>
          <button class="btn btn-ghost btn-sm nav-btn" data-target="buy">🛒 Buy</button>
          <button class="btn btn-ghost btn-sm nav-btn" data-target="tickets">🗂️ Tickets</button>
          <button class="btn btn-ghost" style="width:34px; height:34px; font-size:15px; padding:0" id="toAdminBtn">🛡️</button>
          <button class="btn btn-ghost theme-toggle" style="width:34px; height:34px; font-size:16px; padding:0">☀️</button>
        </div>
      </div>
    </header>

    <header id="adminHeader" class="hidden">
      <div class="header-container">
        <div style="display: flex; align-items: center; gap: 10px;">
          <div style="width: 34px; height: 34px; background: var(--red); border-radius: 9px; display: flex; align-items: center; justify-content: center; font-size: 16px;">🛡️</div>
          <div>
            <div style="font-weight: 800; font-size: 14px; letter-spacing: -0.4px;">Admin Control Panel</div>
            <div style="font-size: 10px; color: var(--muted);">Ticket Selling System</div>
          </div>
        </div>
        <div style="display: flex; align-items: center; gap: 4px;" id="adminNavOptions" class="hidden">
          <button class="btn btn-ghost btn-sm admin-nav-btn" data-tab="dashboard">📊 Dashboard</button>
          <button class="btn btn-ghost btn-sm admin-nav-btn" data-tab="buyers">👥 Buyers</button>
          <button class="btn btn-ghost btn-sm admin-nav-btn" data-tab="grid">🎟️ Tickets</button>
          <button class="btn btn-ghost btn-sm admin-nav-btn" data-tab="settings">⚙️ Settings</button>
          <button class="btn btn-ghost btn-sm" id="exitAdminBtn" style="color: var(--red); border-color: rgba(244,91,91,0.27)">✕ Exit</button>
          <button class="btn btn-ghost theme-toggle" style="width:34px; height:34px; font-size:16px; padding:0">☀️</button>
        </div>
      </div>
    </header>

    <main>
      <div id="flashAlert" class="card hidden" style="padding:10px 16px; color: var(--accent); background: var(--accentSoft); border-color: rgba(77,124,254,0.27); display:flex; justify-content:space-between; align-items:center;">
        <span id="flashText"></span>
        <button id="closeFlash" style="background:none; border:none; color:var(--muted); cursor:pointer; font-size:16px;">✕</button>
      </div>

      <!-- HOME -->
      <div id="view-home" class="public-view">
        <div style="text-align: center; padding: 46px 0 36px;">
          <div style="font-size: 58px; margin-bottom: 14px;">🎟️</div>
          <h1 style="font-size: 36px; font-weight: 900; margin: 0 0 10px; letter-spacing: -1.5px;">Win Big Today!</h1>
          <p style="color: var(--muted); font-size: 16px; margin: 0 0 28px;">2,500 tickets · 2,500 Birr each · Total pool 6,250,000 Birr</p>
          <button class="btn btn-primary" style="padding: 13px 38px; font-size:16px; font-weight:800;" onclick="switchView('buy')">Buy Your Ticket →</button>
        </div>
        <div class="grid-stats" id="publicStatsGrid"></div>
        <div class="grid-2">
          <div class="card">
            <h3 style="margin-bottom: 16px; font-size:15px;">💳 Payment Details</h3>
            <!-- CBE Payment -->
            <div style="background: var(--bg); border-radius: 10px; padding: 14px; margin-bottom: 10px;">
              <div style="font-size: 11px; color: var(--muted); text-transform: uppercase; margin-bottom: 4px;">Option 1 — Bank Transfer</div>
              <div style="font-weight: 600; font-size: 14px; margin-bottom:8px;">Commercial Bank of Ethiopia (CBE)</div>
              <div style="display: flex; align-items: center; gap: 10px; margin-bottom:4px;">
                <span style="font-weight: 800; font-size: 18px; color: var(--accent); letter-spacing: 1.5px;" id="cbeAccountDisplay"></span>
                <button class="btn btn-ghost btn-sm" id="copyCbeBtn">Copy</button>
              </div>
            </div>
            <!-- Telebirr Payment -->
            <div style="background: var(--bg); border-radius: 10px; padding: 14px; margin-bottom: 10px; border: 1px solid var(--border);">
              <div style="font-size: 11px; color: var(--muted); text-transform: uppercase; margin-bottom: 4px;">Option 2 — Telebirr</div>
              <div style="font-weight: 600; font-size: 14px; margin-bottom:6px;">📱 Telebirr Mobile Payment</div>
              <div id="telebirrShortCodeBlock" style="display:none;">
                <div style="font-size:11px; color:var(--muted); margin-bottom:2px;">Short Code</div>
                <span id="telebirrShortCodeDisplay" style="font-weight:800; font-size:18px; color:var(--purple); letter-spacing:1.5px;"></span>
              </div>
              <div id="telebirrComingSoon" style="font-size:13px; color:var(--orange);">⏳ Coming Soon — Credentials pending</div>
            </div>
            <div style="background: var(--greenSoft); border-radius: 10px; padding: 12px 14px;">
              <div style="font-size: 11px; color: var(--muted); text-transform: uppercase; margin-bottom: 4px;">Amount</div>
              <div style="font-weight: 800; font-size: 22px; color: var(--green);">2,500 Birr</div>
            </div>
          </div>
          <div class="card">
            <h3 style="margin-bottom: 16px; font-size:15px;">📋 How It Works</h3>
            <div style="display:flex; gap:12px; margin-bottom:14px; align-items:flex-start;">
              <div style="width:24px; height:24px; border-radius:50%; background:rgba(77,124,254,0.13); color:var(--accent); display:flex; align-items:center; justify-content:center; font-size:11px; font-weight:800; flex-shrink:0;">1</div>
              <p style="margin:0; font-size:14px; color:var(--muted); line-height:1.55;">Transfer 2,500 Birr to the CBE account above</p>
            </div>
            <div style="display:flex; gap:12px; margin-bottom:14px; align-items:flex-start;">
              <div style="width:24px; height:24px; border-radius:50%; background:rgba(184,154,255,0.13); color:var(--purple); display:flex; align-items:center; justify-content:center; font-size:11px; font-weight:800; flex-shrink:0;">2</div>
              <p style="margin:0; font-size:14px; color:var(--muted); line-height:1.55;">Screenshot your payment confirmation</p>
            </div>
            <div style="display:flex; gap:12px; margin-bottom:14px; align-items:flex-start;">
              <div style="width:24px; height:24px; border-radius:50%; background:rgba(31,209,111,0.13); color:var(--green); display:flex; align-items:center; justify-content:center; font-size:11px; font-weight:800; flex-shrink:0;">3</div>
              <p style="margin:0; font-size:14px; color:var(--muted); line-height:1.55;">Enter your name, phone & chosen ticket number</p>
            </div>
            <div style="display:flex; gap:12px; align-items:flex-start;">
              <div style="width:24px; height:24px; border-radius:50%; background:rgba(251,146,60,0.13); color:var(--orange); display:flex; align-items:center; justify-content:center; font-size:11px; font-weight:800; flex-shrink:0;">4</div>
              <p style="margin:0; font-size:14px; color:var(--muted); line-height:1.55;">Upload screenshot — AI verifies instantly</p>
            </div>
          </div>
        </div>
      </div>

      <!-- BUY -->
      <div id="view-buy" class="public-view hidden">
        <div style="max-width: 560px; margin: 0 auto;">
          <h2 style="font-size:24px; font-weight:800; margin-bottom:22px;">🛒 Purchase a Ticket</h2>
          <div id="purchaseFormCard" class="card">
            <!-- Payment Method Selector -->
            <div style="margin-bottom:18px;">
              <label class="lbl">Payment Method / የክፍያ ዘዴ</label>
              <div style="display:flex; gap:10px;">
                <button id="pmCBE" onclick="selectPaymentMethod('cbe')" class="btn btn-primary" style="flex:1; font-size:13px;">🏦 CBE Bank</button>
                <button id="pmTelebirr" onclick="selectPaymentMethod('telebirr')" class="btn btn-ghost" style="flex:1; font-size:13px; position:relative;">📱 Telebirr <span style="position:absolute;top:-6px;right:-4px;background:var(--orange);color:#fff;font-size:9px;padding:2px 5px;border-radius:8px;">Soon</span></button>
              </div>
            </div>
            <!-- CBE Pay Info -->
            <div id="payInfoCBE" style="background: var(--bg); border-radius:11px; padding:16px; margin-bottom:22px; border:1px solid var(--border);">
              <div style="font-size:11px; color:var(--muted); text-transform:uppercase; margin-bottom:4px;">Pay first to:</div>
              <div style="font-weight:600; font-size:14px; margin-bottom:8px;">Commercial Bank of Ethiopia (CBE)</div>
              <div style="display:flex; align-items:center; gap:10px; margin-bottom:6px;">
                <span style="font-weight:800; font-size:18px; color:var(--accent); letter-spacing:1px;" class="cbe-text-node"></span>
              </div>
              <div style="font-weight:700; color:var(--green); font-size:14px;">Amount: 2,500 Birr</div>
            </div>
            <!-- Telebirr Pay Info -->
            <div id="payInfoTelebirr" style="display:none; background: var(--bg); border-radius:11px; padding:16px; margin-bottom:22px; border:1px solid var(--purple);">
              <div style="font-size:11px; color:var(--muted); text-transform:uppercase; margin-bottom:4px;">Pay via Telebirr:</div>
              <div style="font-weight:600; font-size:14px; margin-bottom:8px;">📱 Send to Merchant Short Code</div>
              <div style="font-weight:800; font-size:20px; color:var(--purple); margin-bottom:6px;" id="telebirrCodeInForm">— Coming Soon —</div>
              <div style="font-weight:700; color:var(--green); font-size:14px;">Amount: 2,500 Birr</div>
              <div style="margin-top:10px; padding:10px; background:var(--orangeSoft); border-radius:8px; font-size:12px; color:var(--orange);">⏳ Telebirr integration coming soon. Use CBE for now.</div>
            </div>
            <div style="margin-bottom:16px;">
              <label class="lbl">Full Name / ሙሉ ስም</label>
              <input type="text" id="form-name" placeholder="Enter your full name" class="inp">
            </div>
            <div style="margin-bottom:16px;">
              <label class="lbl">Phone Number / ስልክ ቁጥር</label>
              <input type="tel" id="form-phone" placeholder="e.g. 0912345678" class="inp">
            </div>
            <div style="margin-bottom:16px;">
              <label class="lbl">Ticket Number (1–2500) / የቲኬት ቁጥር</label>
              <input type="number" id="form-ticket" placeholder="Choose a ticket number" min="1" max="2500" class="inp">
              <div id="ticketAvailabilityFeedback" style="margin-top:5px; font-size:12px;"></div>
            </div>
            <div style="margin-bottom:16px;">
              <label class="lbl">FIN Number</label>
              <input type="text" id="form-fin" placeholder="Enter FIN number" class="inp">
            </div>
            <div style="margin-bottom:20px; padding: 16px; background: var(--cardB); border: 1px dashed var(--border); border-radius: 12px; text-align: center;">
              <label class="lbl" style="margin-bottom:10px;">የባንክ ማረጋገጫ ስክሪንሻት ያስገቡ (Receipt Image)</label>
              <input type="file" id="receiptInput" accept="image/*" style="width: 100%; margin-bottom: 10px; color: var(--text);">
              <div id="uploadPreviewContainer"></div>
            </div>
            <button id="submitPurchaseBtn" class="btn btn-primary" style="width:100%; padding:13px; font-size:15px;">✅ Submit & Verify Payment</button>
            <div id="statusMessage" style="margin-top: 15px; padding: 12px; border-radius: 8px; font-size: 14px; white-space: pre-line; display: none; border: 1px solid var(--border); background: var(--bg);"></div>
          </div>
          <div id="purchaseResultCard" class="card hidden" style="text-align: center;">
            <div id="resultIcon" style="font-size:56px; margin-bottom:14px;"></div>
            <h3 id="resultTitle" style="margin: 0 0 8px; font-size:21px; font-weight:800;"></h3>
            <p id="resultDesc" style="color: var(--muted); margin-bottom:6px;"></p>
            <p id="resultReason" style="font-size:13px; color:var(--faint); margin-bottom:22px;"></p>
            <button class="btn btn-primary" id="resultActionBtn"></button>
          </div>
        </div>
      </div>

      <!-- TICKETS -->
      <div id="view-tickets" class="public-view hidden">
        <div style="display:flex; flex-wrap:wrap; gap:12px; align-items:center; margin-bottom:20px;">
          <h2 style="margin:0; font-weight:800; font-size:22px; flex:1;">🗂️ All Tickets</h2>
          <div style="display:flex; gap:6px; flex-wrap:wrap;" id="publicFilterContainer"></div>
          <input placeholder="Search #" id="publicSearchInput" class="inp" style="width:100px;">
        </div>
        <div class="ticket-grid" id="publicTicketGridContainer"></div>
        <div style="display:flex; gap:6px; justify-content:center; flex-wrap:wrap;" id="publicPaginationContainer"></div>
        <p style="color:var(--faint); font-size:13px; text-align:center; margin-top:12px;" id="publicPaginationMetrics"></p>
      </div>

      <!-- ADMIN LOGIN -->
      <div id="admin-login-view" class="admin-view hidden" style="max-width:380px; margin:60px auto;">
        <div class="card" style="text-align:center;">
          <div style="font-size: 48px; margin-bottom: 14px;">🔐</div>
          <h2 style="margin: 0 0 8px; font-weight:800; font-size:22px;">Admin Login</h2>
          <p style="color: var(--muted); font-size:14px; margin-bottom:22px;">Enter password to access the control panel</p>
          <input type="password" id="adminPassInput" placeholder="Admin password" class="inp" style="margin-bottom:12px; text-align:center;">
          <button class="btn btn-primary" style="width:100%" id="adminLoginSubmit">Login →</button>
        </div>
      </div>

      <!-- ADMIN PANEL -->
      <div id="admin-panel-view" class="admin-view hidden">
        
        <!-- DASHBOARD TAB -->
        <div id="admin-tab-dashboard" class="admin-tab-content">
          <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:22px; flex-wrap:wrap; gap:10px;">
            <h2 style="margin:0; font-weight:800; font-size:22px;">📊 Dashboard</h2>
            <button class="btn btn-ghost btn-sm" id="refreshDashboardBtn">🔄 Refresh</button>
          </div>
          <div class="grid-stats" id="adminStatsGrid"></div>
          <div class="card">
            <div style="display:flex; justify-content:space-between; margin-bottom:10px;">
              <span style="font-weight:700;">Sales Progress</span>
              <span style="color:var(--muted); font-size:13px;" id="progressBarText"></span>
            </div>
            <div style="height:12px; background:var(--border); border-radius:99px; overflow:hidden; margin-bottom:8px; display:flex;">
              <div id="barSold" style="background:var(--green); height:100%; transition:.4s;"></div>
              <div id="barChecking" style="background:var(--orange); height:100%; transition:.4s;"></div>
            </div>
            <p style="font-size:12px; color:var(--muted); margin:0;">Green = Sold · Orange = Pending review</p>
          </div>
        </div>

        <!-- BUYERS TAB -->
        <div id="admin-tab-buyers" class="admin-tab-content hidden">
          <div style="display:flex; flex-wrap:wrap; gap:12px; align-items:center; margin-bottom:20px;">
            <h2 style="margin:0; font-weight:800; font-size:22px; flex:1;">👥 Buyer Management</h2>
            <input placeholder="Search name, phone, ticket #" id="adminBuyerSearch" class="inp" style="width:240px;">
            <div style="display:flex; gap:6px;" id="adminBuyerFilterRow"></div>
          </div>
          <div class="card" style="padding:0; overflow:hidden;">
            <div class="table-responsive">
              <table>
                <thead>
                  <tr>
                    <th>Ticket #</th>
                    <th>Name</th>
                    <th>Phone</th>
                    <th>FIN</th>
                    <th>Status</th>
                    <th>Date / Time</th>
                    <th>Actions</th>
                  </tr>
                </thead>
                <tbody id="adminBuyerTableBody"></tbody>
              </table>
            </div>
            <div style="padding:10px 16px; border-top:1px solid var(--border); color:var(--muted); font-size:13px;" id="adminBuyerCountMetrics"></div>
          </div>
        </div>

        <!-- GRID TAB -->
        <div id="admin-tab-grid" class="admin-tab-content hidden">
          <h2 style="margin: 0 0 18px; font-weight:800; font-size:22px;">🎟️ All Tickets</h2>
          <div class="ticket-grid" id="adminGridTicketContainer"></div>
          <div style="display:flex; gap:20px; margin-top:18px; flex-wrap:wrap;" id="adminGridLegend"></div>
        </div>

        <!-- SETTINGS TAB -->
        <div id="admin-tab-settings" class="admin-tab-content hidden" style="max-width:580px;">
          <h2 style="margin: 0 0 22px; font-weight:800; font-size:22px;">⚙️ Settings</h2>
          <div class="card">
            <h3 style="margin: 0 0 12px; font-weight:700; font-size:15px;">📢 Announcement Banner</h3>
            <p style="color:var(--muted); font-size:13px; margin-bottom:12px;">Shown to all visitors on the home page. Leave empty to hide.</p>
            <textarea id="announcementInput" placeholder="Enter announcement…" class="inp" style="min-height:72px; resize:vertical; margin-bottom:12px;"></textarea>
            <button class="btn btn-primary" id="saveAnnouncementBtn">Save Announcement</button>
          </div>
          <div class="card">
            <h3 style="margin: 0 0 12px; font-weight:700; font-size:15px;">📤 Export Buyers CSV</h3>
            <p style="color:var(--muted); font-size:13px; margin-bottom:12px;">Download all buyer data as a spreadsheet.</p>
            <button class="btn btn-ghost" id="exportCsvBtn">⬇️ Download CSV</button>
          </div>
          <div class="card" style="border:1px solid rgba(244,91,91,0.33); background:var(--redSoft);">
            <h3 style="margin: 0 0 10px; font-weight:700; font-size:15px; color:var(--red);">⚠️ Danger Zone</h3>
            <p style="color:var(--muted); font-size:13px; margin-bottom:14px;">Reset ALL ticket data. This cannot be undone.</p>
            <p id="resetWarningText" style="color:var(--orange); font-size:13px; font-weight:700; margin-bottom:10px;" class="hidden">⚠️ Click again to confirm full reset!</p>
            <div style="display:flex; gap:10px;">
              <button class="btn btn-red" id="systemResetBtn">🗑️ Reset All Tickets</button>
              <button class="btn btn-ghost hidden" id="cancelResetBtn">Cancel</button>
            </div>
          </div>
        </div>
      </div>
    </main>

    <footer>
      © 2026 Ticket Selling System · Powered by AI Verification & Supabase · All rights reserved
    </footer>
  </div>

  <!-- TICKET MODAL -->
  <div class="modal-backdrop" id="ticketDetailModal">
    <div class="card" style="min-width:270px; max-width:330px; margin:0;" id="modalCardInternalTarget"></div>
  </div>

  <script>
    // ============================================================
    // CONFIGURATION
    // ============================================================
    const TOTAL       = 2500;
    const PRICE       = 2500;
    const CBE         = "1000646770867";
    const ADMIN_PASS  = "admin2025";
    const PER_PAGE    = 250;
    const GEMINI_KEY  = "AIzaSyBmP8DzudpHvv8iqXzn-DnFaKu4nObkrgc";

    // ============================================================
    // TELEBIRR CONFIG — plug in your credentials here when ready
    // ============================================================
    const TELEBIRR = {
      enabled: false,
      shortCode: "YOUR_SHORT_CODE",
      appKey: "YOUR_APP_KEY",
      appSecret: "YOUR_APP_SECRET",
      merchantName: "Equb Lottery"
    };

    // ============================================================
    // SUPABASE SETUP
    // ============================================================
    const SUPABASE_URL = "https://shpuzxjtnnxxxjmjxwcs.supabase.co";
    const SUPABASE_KEY = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InNocHV6eGp0bm54eHhqbWp4d2NzIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzkxMzQwNzksImV4cCI6MjA5NDcxMDA3OX0.qY8MhSgbuF0cf1sOjTOSyKbpidSD1_zgghHwfEC1tfc";

    let sbClient;
    try {
      sbClient = window.supabase.createClient(SUPABASE_URL, SUPABASE_KEY);
    } catch(e) {
      console.error("Supabase init failed:", e);
    }

    // ============================================================
    // APP STATE
    // ============================================================
    let state = {
      dark: true,
      tickets: {},          // ticketNum -> { status, name, phone, fin, time, id }
      meta: { announcement: "" },
      currentView: "home",
      adminAuthed: false,
      currentAdminTab: "dashboard",
      publicFilter: "all",
      publicSearch: "",
      publicPage: 0,
      adminBuyerFilter: "all",
      adminBuyerSearch: "",
      confirmResetActive: false,
      formState: { name: "", phone: "", fin: "", ticket: "", previewBase64: null, fileType: null }
    };

    const SC = { available: "green", checking: "orange", sold: "red" };
    const SL = { available: "Available", checking: "Checking", sold: "Sold" };
    const fmt = n => Number(n).toLocaleString();

    // ============================================================
    // SUPABASE DATA LAYER
    // ============================================================

    async function dbLoadAll() {
      try {
        const { data: tickets, error: te } = await sbClient
          .from('tickets')
          .select('*');

        if (te) throw te;

        state.tickets = {};
        (tickets || []).forEach(row => {
          state.tickets[row.ticket_number] = {
            id: row.id,
            status: row.status,
            name: row.name,
            phone: row.phone,
            fin: row.fin || "",
            time: new Date(row.created_at).getTime()
          };
        });

        const { data: metaRows, error: me } = await sbClient
          .from('settings')
          .select('*')
          .eq('key', 'announcement')
          .single();

        if (!me && metaRows) {
          state.meta.announcement = metaRows.value || "";
        }
      } catch (err) {
        console.error("DB load error:", err);
        // Fallback to localStorage
        try {
          const t = localStorage.getItem('tss_v3_tickets');
          if (t) state.tickets = JSON.parse(t);
          const m = localStorage.getItem('tss_v3_meta');
          if (m) state.meta = JSON.parse(m);
        } catch(e2){}
      }
    }

    async function dbInsertTicket(num, data) {
      try {
        const { data: row, error } = await sbClient
          .from('tickets')
          .insert({
            ticket_number: num,
            status: data.status,
            name: data.name,
            phone: data.phone,
            fin: data.fin || ""
          })
          .select()
          .single();

        if (error) throw error;
        state.tickets[num] = {
          id: row.id,
          status: row.status,
          name: row.name,
          phone: row.phone,
          fin: row.fin || "",
          time: new Date(row.created_at).getTime()
        };
        return true;
      } catch(err) {
        console.error("DB insert error:", err);
        state.tickets[num] = { ...data, time: Date.now() };
        localStorage.setItem('tss_v3_tickets', JSON.stringify(state.tickets));
        return false;
      }
    }

    async function dbUpdateTicket(num, updates) {
      try {
        const existing = state.tickets[num];
        if (!existing?.id) throw new Error("No id");

        const { error } = await sbClient
          .from('tickets')
          .update(updates)
          .eq('id', existing.id);

        if (error) throw error;
        Object.assign(state.tickets[num], updates);
        return true;
      } catch(err) {
        console.error("DB update error:", err);
        Object.assign(state.tickets[num], updates);
        localStorage.setItem('tss_v3_tickets', JSON.stringify(state.tickets));
        return false;
      }
    }

    async function dbDeleteTicket(num) {
      try {
        const existing = state.tickets[num];
        if (existing?.id) {
          const { error } = await sbClient
            .from('tickets')
            .delete()
            .eq('id', existing.id);
          if (error) throw error;
        }
        delete state.tickets[num];
        return true;
      } catch(err) {
        console.error("DB delete error:", err);
        delete state.tickets[num];
        localStorage.setItem('tss_v3_tickets', JSON.stringify(state.tickets));
        return false;
      }
    }

    async function dbDeleteAll() {
      try {
        const { error } = await sbClient
          .from('tickets')
          .delete()
          .neq('id', 0); // delete all rows
        if (error) throw error;
        state.tickets = {};
        return true;
      } catch(err) {
        console.error("DB delete all error:", err);
        state.tickets = {};
        localStorage.removeItem('tss_v3_tickets');
        return false;
      }
    }

    async function dbSaveMeta(key, value) {
      try {
        const { error } = await sbClient
          .from('settings')
          .upsert({ key, value }, { onConflict: 'key' });
        if (error) throw error;
        return true;
      } catch(err) {
        console.error("DB meta save error:", err);
        state.meta.announcement = value;
        localStorage.setItem('tss_v3_meta', JSON.stringify(state.meta));
        return false;
      }
    }

    // ============================================================
    // PAYMENT METHOD SELECTOR
    // ============================================================
    let selectedPaymentMethod = "cbe";

    function selectPaymentMethod(method) {
      selectedPaymentMethod = method;
      document.getElementById("pmCBE").className = method === "cbe" ? "btn btn-primary" : "btn btn-ghost";
      document.getElementById("pmTelebirr").className = method === "telebirr" ? "btn btn-primary" : "btn btn-ghost";
      document.getElementById("payInfoCBE").style.display = method === "cbe" ? "block" : "none";
      document.getElementById("payInfoTelebirr").style.display = method === "telebirr" ? "block" : "none";
      // Update receipt upload label
      const receiptLabel = document.querySelector('label[class="lbl"][style*="margin-bottom:10px"]');
      if (receiptLabel) {
        receiptLabel.textContent = method === "telebirr"
          ? "Upload Telebirr Screenshot / ስክሪንሻት ያስገቡ"
          : "የባንክ ማረጋገጫ ስክሪንሻት ያስገቡ (Receipt Image)";
      }
    }

    // Initialize Telebirr display
    function initTelebirrDisplay() {
      if (TELEBIRR.enabled && TELEBIRR.shortCode !== "YOUR_SHORT_CODE") {
        const shortCodeBlock = document.getElementById("telebirrShortCodeBlock");
        const comingSoon = document.getElementById("telebirrComingSoon");
        const codeInForm = document.getElementById("telebirrCodeInForm");
        if (shortCodeBlock) { shortCodeBlock.style.display = "block"; }
        if (comingSoon) { comingSoon.style.display = "none"; }
        if (codeInForm) { codeInForm.textContent = TELEBIRR.shortCode; }
        document.getElementById("telebirrShortCodeDisplay").textContent = TELEBIRR.shortCode;
        // Remove "Soon" badge from button
        const badge = document.querySelector("#pmTelebirr span");
        if (badge) badge.remove();
      }
    }

    // Subscribe to real-time changes
    function setupRealtimeSubscription() {
      try {
        sbClient
          .channel('tickets-changes')
          .on('postgres_changes', { event: '*', schema: 'public', table: 'tickets' }, payload => {
            if (payload.eventType === 'INSERT' || payload.eventType === 'UPDATE') {
              const row = payload.new;
              state.tickets[row.ticket_number] = {
                id: row.id,
                status: row.status,
                name: row.name,
                phone: row.phone,
                fin: row.fin || "",
                time: new Date(row.created_at).getTime()
              };
            } else if (payload.eventType === 'DELETE') {
              const num = payload.old.ticket_number;
              delete state.tickets[num];
            }
            // Re-render current view silently
            if (state.currentView === 'home') renderHomeView();
            if (state.currentView === 'tickets') renderTicketsView();
            if (state.currentView === 'admin' && state.adminAuthed) renderAdminTabs();
          })
          .subscribe();
      } catch(e) {
        console.warn("Realtime subscription failed:", e);
      }
    }

    // ============================================================
    // AI VERIFICATION
    // ============================================================
    async function verifyAI(base64Data, clientName, ticketNum, fileType) {
      const prompt = `Analyze this Commercial Bank of Ethiopia (CBE) bank receipt screenshot for ticket #${ticketNum} by "${clientName}". Check if the payment status is successful, verify if the amount is exactly ${PRICE} Birr, and double-check if it's a valid receipt. Respond strictly in valid JSON format matching this schema: {"verified": true, "reason": "Your Amharic summary explanation here"}`;

      const response = await fetch(
        `https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=${GEMINI_KEY}`,
        {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({
            contents: [{
              parts: [
                { text: prompt },
                { inlineData: { mimeType: fileType || "image/jpeg", data: base64Data } }
              ]
            }]
          })
        }
      );

      const data = await response.json();
      const textOutput = data.candidates?.[0]?.content?.parts?.[0]?.text || "";
      try {
        return JSON.parse(textOutput.replace(/```json|```/g, "").trim());
      } catch(err) {
        const text = textOutput.toLowerCase();
        const isVerified = text.includes("ተረጋግጧል") || text.includes("true") || text.includes("successful");
        return { verified: isVerified, reason: textOutput || "የክፍያ ማረጋገጫ ሂደት ተጠናቋል።" };
      }
    }

    // ============================================================
    // STATS
    // ============================================================
    function calculateStats() {
      const values = Object.values(state.tickets);
      const checking = values.filter(t => t.status === "checking").length;
      const sold = values.filter(t => t.status === "sold").length;
      const activeCount = values.length;
      return {
        available: TOTAL - activeCount,
        checking,
        sold,
        revenue: sold * PRICE
      };
    }

    // ============================================================
    // THEME
    // ============================================================
    function syncThemeDOM() {
      document.documentElement.setAttribute("data-theme", state.dark ? "dark" : "light");
      document.querySelectorAll(".theme-toggle").forEach(el => {
        el.textContent = state.dark ? "☀️" : "🌙";
      });
    }

    function showFlash(msg, type = "info") {
      const alertBox = document.getElementById("flashAlert");
      const flashText = document.getElementById("flashText");
      flashText.textContent = msg;
      alertBox.classList.remove("hidden");
      if(type === "error") {
        alertBox.style.color = "var(--red)";
        alertBox.style.background = "var(--redSoft)";
        alertBox.style.borderColor = "rgba(244,91,91,0.27)";
      } else {
        alertBox.style.color = "var(--accent)";
        alertBox.style.background = "var(--accentSoft)";
        alertBox.style.borderColor = "rgba(77,124,254,0.27)";
      }
      setTimeout(() => alertBox.classList.add("hidden"), 5000);
    }

    // ============================================================
    // VIEW ROUTING
    // ============================================================
    function switchView(target) {
      state.currentView = target;
      document.getElementById("publicHeader").classList.add("hidden");
      document.getElementById("adminHeader").classList.add("hidden");
      document.querySelectorAll(".public-view").forEach(el => el.classList.add("hidden"));
      document.querySelectorAll(".admin-view").forEach(el => el.classList.add("hidden"));

      if (target === "admin") {
        document.getElementById("adminHeader").classList.remove("hidden");
        if (!state.adminAuthed) {
          document.getElementById("admin-login-view").classList.remove("hidden");
          document.getElementById("adminNavOptions").classList.add("hidden");
        } else {
          document.getElementById("admin-panel-view").classList.remove("hidden");
          document.getElementById("adminNavOptions").classList.remove("hidden");
          renderAdminTabs();
        }
      } else {
        document.getElementById("publicHeader").classList.remove("hidden");
        document.getElementById(`view-${target}`).classList.remove("hidden");
        document.querySelectorAll(".nav-btn").forEach(btn => {
          if (btn.getAttribute("data-target") === target) {
            btn.style.background = "var(--accent)";
            btn.style.color = "#fff";
          } else {
            btn.style.background = "transparent";
            btn.style.color = "var(--muted)";
          }
        });
        if (target !== "buy") resetFormState();
        if (target === "home") renderHomeView();
        if (target === "tickets") renderTicketsView();
      }
    }

    // ============================================================
    // HOME VIEW
    // ============================================================
    function renderHomeView() {
      const stats = calculateStats();
      const container = document.getElementById("publicStatsGrid");
      container.innerHTML = "";
      const config = [
        { label: "Available", val: fmt(stats.available), acc: "green", icon: "🟢" },
        { label: "Under Review", val: fmt(stats.checking), acc: "orange", icon: "🟠" },
        { label: "Sold", val: fmt(stats.sold), acc: "red", icon: "🔴" },
        { label: "Revenue", val: fmt(stats.revenue) + " Birr", acc: "purple", icon: "💰" }
      ];
      config.forEach(c => {
        const item = document.createElement("div");
        item.className = "card";
        item.style.borderLeft = `3px solid var(--${c.acc})`;
        item.innerHTML = `
          <div style="font-size:11px; color:var(--muted); margin-bottom:7px; text-transform:uppercase; letter-spacing:0.7px;">${c.icon} ${c.label}</div>
          <div style="font-size:26px; font-weight:800; color:var(--${c.acc})">${c.val}</div>
        `;
        container.appendChild(item);
      });
    }

    // ============================================================
    // TICKETS VIEW
    // ============================================================
    function renderTicketsView() {
      const stats = calculateStats();
      const filterRow = document.getElementById("publicFilterContainer");
      filterRow.innerHTML = "";
      const options = ["all", "available", "checking", "sold"];
      options.forEach(opt => {
        const btn = document.createElement("button");
        btn.className = "btn btn-ghost btn-sm";
        let label = opt === "all" ? `All (${TOTAL})` : `${SL[opt]} (${opt === 'available' ? stats.available : stats[opt]})`;
        btn.textContent = label;
        if (state.publicFilter === opt) {
          btn.style.color = "var(--accent)";
          btn.style.borderColor = "var(--accent)";
        }
        btn.onclick = () => { state.publicFilter = opt; state.publicPage = 0; renderTicketsView(); };
        filterRow.appendChild(btn);
      });

      const filtered = [];
      for (let i = 1; i <= TOTAL; i++) {
        const ticket = state.tickets[i];
        const status = ticket ? ticket.status : "available";
        if (state.publicFilter !== "all" && status !== state.publicFilter) continue;
        if (state.publicSearch && !String(i).includes(state.publicSearch)) continue;
        filtered.push(i);
      }

      const pagesCount = Math.ceil(filtered.length / PER_PAGE);
      const startIdx = state.publicPage * PER_PAGE;
      const paginatedSlice = filtered.slice(startIdx, startIdx + PER_PAGE);

      const gridContainer = document.getElementById("publicTicketGridContainer");
      gridContainer.innerHTML = "";
      paginatedSlice.forEach(num => {
        const t = state.tickets[num];
        const s = t ? t.status : "available";
        const colorVar = `var(--${SC[s]})`;
        const cell = document.createElement("div");
        cell.className = "ticket-cell";
        cell.style.background = `var(--${SC[s]}Soft)`;
        cell.style.borderColor = `${colorVar}33`;
        cell.title = t ? `${t.name} · ${t.phone}` : "Available";
        cell.innerHTML = `
          <div style="font-size:10px; font-weight:800; color:${colorVar}">${num}</div>
          <div class="ticket-dot" style="background:${colorVar}"></div>
        `;
        cell.onclick = () => openTicketModal(num);
        gridContainer.appendChild(cell);
      });

      const pagContainer = document.getElementById("publicPaginationContainer");
      pagContainer.innerHTML = "";
      if (pagesCount > 1) {
        for (let i = 0; i < pagesCount; i++) {
          const pBtn = document.createElement("button");
          pBtn.className = `btn btn-sm ${state.publicPage === i ? 'btn-primary' : 'btn-ghost'}`;
          pBtn.textContent = `${i * PER_PAGE + 1}–${Math.min((i + 1) * PER_PAGE, filtered.length)}`;
          pBtn.onclick = () => { state.publicPage = i; renderTicketsView(); };
          pagContainer.appendChild(pBtn);
        }
      }
      document.getElementById("publicPaginationMetrics").textContent = `Showing ${paginatedSlice.length} of ${filtered.length} tickets`;
    }

    // ============================================================
    // TICKET MODAL
    // ============================================================
    function openTicketModal(num) {
      const t = state.tickets[num];
      const s = t ? t.status : "available";
      const container = document.getElementById("modalCardInternalTarget");
      container.innerHTML = `
        <div style="display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:16px;">
          <div>
            <div style="font-size:12px; color:var(--muted); margin-bottom:3px;">TICKET</div>
            <div style="font-size:36px; font-weight:900; letter-spacing:-1px;">#${num}</div>
          </div>
          <span class="badge badge-${s}">${SL[s]}</span>
        </div>
        <div id="modalInternalBody"></div>
        <button class="btn btn-ghost" style="width:100%; margin-top:14px;" onclick="closeTicketModal()">Close</button>
      `;
      const bodyTarget = container.querySelector("#modalInternalBody");
      if (t) {
        bodyTarget.innerHTML = `
          <div style="background:var(--bg); border-radius:10px; padding:14px;">
            <div style="margin-bottom:8px;"><span style="color:var(--muted); font-size:12px;">Name: </span><span style="font-weight:700;">${t.name}</span></div>
            <div style="margin-bottom:8px;"><span style="color:var(--muted); font-size:12px;">Phone: </span><span style="font-weight:700;">${t.phone}</span></div>
            ${t.fin ? `<div style="margin-bottom:8px;"><span style="color:var(--muted); font-size:12px;">FIN: </span><span style="font-weight:700;">${t.fin}</span></div>` : ''}
            ${t.time ? `<div style="font-size:11px; color:var(--faint);">${new Date(t.time).toLocaleString()}</div>` : ''}
          </div>
        `;
      } else {
        bodyTarget.innerHTML = `
          <div style="text-align:center; padding:8px 0 4px;">
            <p style="color:var(--green); font-weight:600; margin-bottom:14px;">This ticket is available!</p>
            <button class="btn btn-primary" id="modalBuyActionBtn">Buy Ticket #${num}</button>
          </div>
        `;
        container.querySelector("#modalBuyActionBtn").onclick = () => {
          closeTicketModal();
          switchView("buy");
          document.getElementById("form-ticket").value = num;
          triggerTicketInputFeedback(num);
        };
      }
      document.getElementById("ticketDetailModal").style.display = "flex";
    }

    function closeTicketModal() {
      document.getElementById("ticketDetailModal").style.display = "none";
    }

    // ============================================================
    // BUY FORM
    // ============================================================
    function resetFormState() {
      state.formState = { name: "", phone: "", fin: "", ticket: "", previewBase64: null, fileType: null };
      ["form-name", "form-phone", "form-ticket", "form-fin"].forEach(id => {
        const el = document.getElementById(id);
        if (el) el.value = "";
      });
      document.getElementById("receiptInput").value = "";
      document.getElementById("ticketAvailabilityFeedback").innerHTML = "";
      document.getElementById("uploadPreviewContainer").innerHTML = "";
      const statusMsg = document.getElementById("statusMessage");
      statusMsg.style.display = "none";
      statusMsg.innerText = "";
      document.getElementById("purchaseFormCard").classList.remove("hidden");
      document.getElementById("purchaseResultCard").classList.add("hidden");
      const submitBtn = document.getElementById("submitPurchaseBtn");
      submitBtn.disabled = false;
      submitBtn.textContent = "✅ Submit & Verify Payment";
    }

    function triggerTicketInputFeedback(val) {
      const feedback = document.getElementById("ticketAvailabilityFeedback");
      const num = parseInt(val);
      if (!num || num < 1 || num > 2500) { feedback.innerHTML = ""; return; }
      const t = state.tickets[num];
      if (t) {
        feedback.style.color = `var(--${SC[t.status]})`;
        feedback.textContent = `⚠️ Ticket is ${SL[t.status]}`;
      } else {
        feedback.style.color = "var(--green)";
        feedback.textContent = "✓ Available!";
      }
    }

    // ============================================================
    // ADMIN TABS
    // ============================================================
    function setAdminTab(tabName) {
      state.currentAdminTab = tabName;
      document.querySelectorAll(".admin-tab-content").forEach(el => el.classList.add("hidden"));
      document.getElementById(`admin-tab-${tabName}`).classList.remove("hidden");
      document.querySelectorAll(".admin-nav-btn").forEach(btn => {
        if (btn.getAttribute("data-tab") === tabName) {
          btn.style.color = "var(--accent)";
          btn.style.borderColor = "var(--accent)";
        } else {
          btn.style.color = "var(--muted)";
          btn.style.borderColor = "var(--border)";
        }
      });
      renderAdminTabs();
    }

    function renderAdminTabs() {
      const stats = calculateStats();

      if (state.currentAdminTab === "dashboard") {
        const container = document.getElementById("adminStatsGrid");
        container.innerHTML = "";
        const config = [
          { label: "Total Tickets", val: fmt(TOTAL), acc: "accent", icon: "🎟️" },
          { label: "Available", val: fmt(stats.available), acc: "green", icon: "🟢" },
          { label: "Under Review", val: fmt(stats.checking), acc: "orange", icon: "🟠" },
          { label: "Sold", val: fmt(stats.sold), acc: "red", icon: "🔴" },
          { label: "Revenue", val: fmt(stats.revenue) + " Birr", acc: "purple", icon: "💰" },
          { label: "Completion", val: ((stats.sold / TOTAL) * 100).toFixed(1) + "%", acc: "accent", icon: "📈" }
        ];
        config.forEach(c => {
          const item = document.createElement("div");
          item.className = "card";
          item.style.borderLeft = `3px solid var(--${c.acc})`;
          item.innerHTML = `
            <div style="font-size:11px; color:var(--muted); margin-bottom:6px; text-transform:uppercase; letter-spacing:0.7px;">${c.icon} ${c.label}</div>
            <div style="font-size:24px; font-weight:800; color:var(--${c.acc})">${c.val}</div>
          `;
          container.appendChild(item);
        });
        document.getElementById("progressBarText").textContent = `${stats.sold} / ${TOTAL}`;
        document.getElementById("barSold").style.width = `${(stats.sold / TOTAL) * 100}%`;
        document.getElementById("barChecking").style.width = `${(stats.checking / TOTAL) * 100}%`;
      }

      if (state.currentAdminTab === "buyers") {
        const fRow = document.getElementById("adminBuyerFilterRow");
        fRow.innerHTML = "";
        ["all", "checking", "sold"].forEach(f => {
          const btn = document.createElement("button");
          btn.className = "btn btn-ghost btn-sm";
          btn.textContent = f === "all" ? "All" : f === "checking" ? "⏳ Pending" : "✅ Sold";
          if (state.adminBuyerFilter === f) {
            btn.style.color = "var(--accent)";
            btn.style.borderColor = "var(--accent)";
          }
          btn.onclick = () => { state.adminBuyerFilter = f; renderAdminTabs(); };
          fRow.appendChild(btn);
        });

        const rows = Object.entries(state.tickets).filter(([n, t]) => {
          if (state.adminBuyerFilter !== "all" && t.status !== state.adminBuyerFilter) return false;
          if (state.adminBuyerSearch) {
            const term = state.adminBuyerSearch.toLowerCase();
            if (!n.includes(term) && !t.name?.toLowerCase().includes(term) && !t.phone?.includes(term) && !t.fin?.includes(term)) return false;
          }
          return true;
        }).sort(([, a], [, b]) => (b.time || 0) - (a.time || 0));

        const tbody = document.getElementById("adminBuyerTableBody");
        tbody.innerHTML = "";
        if (rows.length === 0) {
          tbody.innerHTML = `<tr><td colspan="7" style="padding:32px; text-align:center; color:var(--muted);">No records found.</td></tr>`;
        } else {
          rows.forEach(([num, t]) => {
            const tr = document.createElement("tr");
            let actionMarkup = "";
            if (t.status === "checking") {
              actionMarkup = `
                <button class="btn btn-green btn-sm" onclick="handleAdminAction(${num}, 'approve')">✓ Approve</button>
                <button class="btn btn-red btn-sm" onclick="handleAdminAction(${num}, 'reject')">✗ Reject</button>
              `;
            } else if (t.status === "sold") {
              actionMarkup = `<button class="btn btn-ghost btn-sm" onclick="handleAdminAction(${num}, 'release')">Release</button>`;
            }
            tr.innerHTML = `
              <td style="font-weight:800; color:var(--accent)">#${num}</td>
              <td style="font-weight:600;">${t.name}</td>
              <td style="color:var(--muted);">${t.phone}</td>
              <td style="color:var(--muted);">${t.fin || "—"}</td>
              <td><span class="badge badge-${t.status}">${SL[t.status]}</span></td>
              <td style="color:var(--muted); font-size:12px; white-space:nowrap;">${t.time ? new Date(t.time).toLocaleString() : "—"}</td>
              <td><div style="display:flex; gap:6px;">${actionMarkup}</div></td>
            `;
            tbody.appendChild(tr);
          });
        }
        document.getElementById("adminBuyerCountMetrics").textContent = `${rows.length} record${rows.length !== 1 ? 's' : ''}`;
      }

      if (state.currentAdminTab === "grid") {
        const container = document.getElementById("adminGridTicketContainer");
        container.innerHTML = "";
        for (let i = 1; i <= TOTAL; i++) {
          const t = state.tickets[i];
          const s = t ? t.status : "available";
          const colorVar = `var(--${SC[s]})`;
          const cell = document.createElement("div");
          cell.className = "ticket-cell";
          cell.style.background = `var(--${SC[s]}Soft)`;
          cell.style.border = `1.5px solid ${colorVar}33`;
          cell.style.padding = "5px 2px";
          cell.title = t ? `${t.name} · ${t.phone}` : "Available";
          cell.innerHTML = `
            <div style="font-size:9px; font-weight:800; color:${colorVar}">${i}</div>
            <div style="width:4px; height:4px; border-radius:50%; background:${colorVar}; margin:2px auto 0;"></div>
          `;
          container.appendChild(cell);
        }
        const legend = document.getElementById("adminGridLegend");
        legend.innerHTML = "";
        ["available", "checking", "sold"].forEach(s => {
          legend.innerHTML += `
            <div style="display:flex; align-items:center; gap:8px;">
              <div style="width:11px; height:11px; border-radius:3px; background:var(--${SC[s]})"></div>
              <span style="font-size:13px; color:var(--muted);">${SL[s]}: ${s === 'available' ? stats.available : stats[s]}</span>
            </div>
          `;
        });
      }

      if (state.currentAdminTab === "settings") {
        document.getElementById("announcementInput").value = state.meta.announcement || "";
      }
    }

    async function handleAdminAction(num, action) {
      if (action === "approve") {
        await dbUpdateTicket(num, { status: "sold" });
        showFlash(`✓ Ticket #${num} approved`);
      } else if (action === "reject" || action === "release") {
        await dbDeleteTicket(num);
        showFlash(action === "reject" ? `✗ Ticket #${num} rejected` : `Ticket #${num} released`);
      }
      renderAdminTabs();
    }

    // ============================================================
    // SQL SETUP HELPER — shown once on first load if tables missing
    // ============================================================
    function showSQLSetupModal() {
      const sql = `-- Run this SQL in your Supabase SQL Editor:

CREATE TABLE IF NOT EXISTS tickets (
  id BIGSERIAL PRIMARY KEY,
  ticket_number INTEGER UNIQUE NOT NULL,
  status TEXT NOT NULL DEFAULT 'checking',
  name TEXT NOT NULL,
  phone TEXT NOT NULL,
  fin TEXT DEFAULT '',
  created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE TABLE IF NOT EXISTS settings (
  key TEXT PRIMARY KEY,
  value TEXT DEFAULT ''
);

-- Enable Row Level Security (RLS) and allow all access (adjust for production)
ALTER TABLE tickets ENABLE ROW LEVEL SECURITY;
ALTER TABLE settings ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Allow all" ON tickets FOR ALL USING (true) WITH CHECK (true);
CREATE POLICY "Allow all" ON settings FOR ALL USING (true) WITH CHECK (true);

-- Enable realtime
ALTER PUBLICATION supabase_realtime ADD TABLE tickets;`;

      const backdrop = document.createElement("div");
      backdrop.style.cssText = "position:fixed;inset:0;background:rgba(0,0,0,0.7);z-index:999;display:flex;align-items:center;justify-content:center;padding:20px;";
      backdrop.innerHTML = `
        <div style="background:var(--card);border:1px solid var(--border);border-radius:14px;padding:24px;max-width:600px;width:100%;max-height:90vh;overflow-y:auto;">
          <h2 style="margin:0 0 10px;font-size:18px;font-weight:800;color:var(--orange);">⚠️ Database Setup Required</h2>
          <p style="color:var(--muted);font-size:13px;margin-bottom:16px;">Your Supabase database needs these tables. Run this SQL in your <a href="https://supabase.com/dashboard" target="_blank" style="color:var(--accent)">Supabase SQL Editor</a>, then refresh the page.</p>
          <pre style="background:var(--bg);border:1px solid var(--border);border-radius:10px;padding:16px;font-size:12px;overflow-x:auto;white-space:pre-wrap;color:var(--green);margin-bottom:16px;">${sql}</pre>
          <div style="display:flex;gap:10px;flex-wrap:wrap;">
            <button onclick="navigator.clipboard.writeText(document.querySelector('pre').textContent); this.textContent='✓ Copied!'; setTimeout(()=>this.textContent='📋 Copy SQL',2000);" class="btn btn-primary btn-sm">📋 Copy SQL</button>
            <button onclick="this.closest('[style*=fixed]').remove(); document.getElementById('loadingView').classList.add('hidden'); document.getElementById('appShell').classList.remove('hidden'); syncThemeDOM(); switchView('home');" class="btn btn-ghost btn-sm">Continue Anyway (uses localStorage)</button>
          </div>
        </div>
      `;
      document.body.appendChild(backdrop);
    }

    // ============================================================
    // INIT
    // ============================================================
    window.addEventListener("DOMContentLoaded", async () => {
      document.getElementById("loadingText").textContent = "Connecting to database…";

      // Check connection and show error on screen
      let tablesExist = false;
      try {
        const { data, error } = await sbClient.from('tickets').select('id').limit(1);
        if (error) {
          console.error("DB error:", error);
        } else {
          tablesExist = true;
          document.getElementById("loadingText").textContent = "Connected!";
        }
      } catch(e) {
        console.error("Connection failed:", e);
      }
      // Always continue even if DB fails - use localStorage fallback
      try {
        await Promise.race([
          dbLoadAll(),
          new Promise((_, reject) => setTimeout(() => reject(new Error("timeout")), 5000))
        ]);
      } catch(e) {
        console.warn("DB load timed out, using localStorage");
        try {
          const t = localStorage.getItem('tss_v3_tickets');
          if (t) state.tickets = JSON.parse(t);
          const m = localStorage.getItem('tss_v3_meta');
          if (m) state.meta = JSON.parse(m);
        } catch(e2) {}
      }
      setupRealtimeSubscription();
      initTelebirrDisplay();

      // Setup DOM
      document.querySelectorAll(".cbe-text-node").forEach(el => el.textContent = CBE);
      document.getElementById("cbeAccountDisplay").textContent = CBE;

      if (state.meta.announcement) {
        const banner = document.getElementById("announcementBanner");
        banner.textContent = `📢 ${state.meta.announcement}`;
        banner.style.display = "block";
      }

      document.getElementById("loadingView").classList.add("hidden");
      document.getElementById("appShell").classList.remove("hidden");
      syncThemeDOM();
      switchView("home");

      // --- EVENT LISTENERS ---

      document.querySelectorAll(".nav-btn").forEach(btn => {
        btn.addEventListener("click", e => switchView(e.target.getAttribute("data-target")));
      });

      document.querySelectorAll(".admin-nav-btn").forEach(btn => {
        btn.addEventListener("click", e => setAdminTab(e.target.getAttribute("data-tab")));
      });

      document.querySelectorAll(".theme-toggle").forEach(btn => {
        btn.addEventListener("click", () => { state.dark = !state.dark; syncThemeDOM(); });
      });

      document.getElementById("toAdminBtn").addEventListener("click", () => switchView("admin"));
      document.getElementById("exitAdminBtn").addEventListener("click", () => { state.adminAuthed = false; switchView("home"); });
      document.getElementById("closeFlash").addEventListener("click", () => document.getElementById("flashAlert").classList.add("hidden"));

      document.getElementById("copyCbeBtn").addEventListener("click", e => {
        navigator.clipboard.writeText(CBE);
        e.target.textContent = "✓ Copied";
        e.target.className = "btn btn-green btn-sm";
        setTimeout(() => { e.target.textContent = "Copy"; e.target.className = "btn btn-ghost btn-sm"; }, 2000);
      });

      document.getElementById("form-ticket").addEventListener("input", e => triggerTicketInputFeedback(e.target.value));

      document.getElementById("receiptInput").addEventListener("change", e => {
        const file = e.target.files[0];
        if (!file) return;
        const reader = new FileReader();
        reader.onload = ev => {
          state.formState.previewBase64 = ev.target.result;
          state.formState.fileType = file.type;
          document.getElementById("uploadPreviewContainer").innerHTML = `
            <img src="${ev.target.result}" style="max-height:150px; max-width:100%; border-radius:8px; margin-top:8px;" />
            <div style="font-size:12px; color:var(--green); margin-top:4px;">✓ Uploaded / ተጭኗል</div>
          `;
        };
        reader.readAsDataURL(file);
      });

      document.getElementById("submitPurchaseBtn").addEventListener("click", async () => {
        const nameVal = document.getElementById("form-name").value.trim();
        const phoneVal = document.getElementById("form-phone").value.trim();
        const ticketVal = document.getElementById("form-ticket").value;
        const finVal = document.getElementById("form-fin").value.trim();
        const statusMessage = document.getElementById("statusMessage");
        const num = parseInt(ticketVal);

        if (!nameVal || !phoneVal || !ticketVal || !state.formState.previewBase64) {
          statusMessage.style.display = "block";
          statusMessage.style.color = "var(--red)";
          statusMessage.innerText = "❌ እባክዎ ሁሉንም መረጃዎች ይሙሉ እና ስክሪንሻት ይጫኑ! (Fill all fields and upload screenshot.)";
          return;
        }
        if (isNaN(num) || num < 1 || num > TOTAL) { alert("Ticket must be 1–2500."); return; }
        if (state.tickets[num]) { alert(`Ticket #${num} is ${SL[state.tickets[num].status]}.`); return; }

        const submitBtn = document.getElementById("submitPurchaseBtn");
        submitBtn.disabled = true;
        submitBtn.textContent = "🔍 AI Verifying Payment…";
        statusMessage.style.display = "block";
        statusMessage.style.color = "var(--orange)";
        statusMessage.innerText = "⏳ ክፍያው በነጻው የላቀ AI እየተረጋገጠ ነው... እባክዎ ይጠብቁ...";

        // Optimistic lock in DB
        await dbInsertTicket(num, { status: "checking", name: nameVal, phone: phoneVal, fin: finVal });

        const formCard = document.getElementById("purchaseFormCard");
        const resCard = document.getElementById("purchaseResultCard");
        const rIcon = document.getElementById("resultIcon");
        const rTitle = document.getElementById("resultTitle");
        const rDesc = document.getElementById("resultDesc");
        const rReason = document.getElementById("resultReason");
        const rAction = document.getElementById("resultActionBtn");

        try {
          const rawBase64 = state.formState.previewBase64.split(",")[1];
          const aiResult = await verifyAI(rawBase64, nameVal, num, state.formState.fileType);

          formCard.classList.add("hidden");
          resCard.classList.remove("hidden");

          if (aiResult.verified) {
            await dbUpdateTicket(num, { status: "sold" });
            resCard.style.borderColor = "var(--green)";
            rIcon.textContent = "✅";
            rTitle.textContent = "ክፍያው ተረጋግጧል! (Verified)";
            rTitle.style.color = "var(--green)";
            rDesc.textContent = `🎉 Ticket #${num} is now yours!`;
            rReason.textContent = `AI: ${aiResult.reason}`;
            rAction.textContent = "Buy Another / ሌላ ግዛ";
            rAction.className = "btn btn-primary";
            rAction.onclick = () => resetFormState();
          } else {
            await dbDeleteTicket(num);
            resCard.style.borderColor = "var(--red)";
            rIcon.textContent = "❌";
            rTitle.textContent = "ክፍያው አልተረጋገጠም (Failed)";
            rTitle.style.color = "var(--red)";
            rDesc.textContent = `Ticket #${num} released. Try again with a valid screenshot.`;
            rReason.textContent = `AI: ${aiResult.reason}`;
            rAction.textContent = "Try Again / እንደገና ሞክር";
            rAction.className = "btn btn-primary";
            rAction.onclick = () => resetFormState();
          }
        } catch(e) {
          // Keep as "checking" — admin will review
          formCard.classList.add("hidden");
          resCard.classList.remove("hidden");
          resCard.style.borderColor = "var(--orange)";
          rIcon.textContent = "⏳";
          rTitle.textContent = "Under Review / በመጠበቅ ላይ";
          rTitle.style.color = "var(--orange)";
          rDesc.textContent = `Ticket #${num} is reserved while admin reviews.`;
          rReason.textContent = "AI System Notification: Pending manual verification fallback.";
          rAction.textContent = "Back to Safety";
          rAction.className = "btn btn-primary";
          rAction.onclick = () => resetFormState();
        }
      });

      document.getElementById("adminLoginSubmit").addEventListener("click", () => {
        const pass = document.getElementById("adminPassInput").value;
        if (pass === ADMIN_PASS) {
          state.adminAuthed = true;
          document.getElementById("adminPassInput").value = "";
          switchView("admin");
        } else {
          alert("Wrong password.");
        }
      });

      document.getElementById("adminPassInput").addEventListener("keydown", e => {
        if (e.key === "Enter") document.getElementById("adminLoginSubmit").click();
      });

      document.getElementById("adminBuyerSearch").addEventListener("input", e => {
        state.adminBuyerSearch = e.target.value;
        renderAdminTabs();
      });

      document.getElementById("publicSearchInput").addEventListener("input", e => {
        state.publicSearch = e.target.value;
        state.publicPage = 0;
        renderTicketsView();
      });

      document.getElementById("refreshDashboardBtn").addEventListener("click", async () => {
        document.getElementById("refreshDashboardBtn").textContent = "⏳ Refreshing…";
        await dbLoadAll();
        renderAdminTabs();
        document.getElementById("refreshDashboardBtn").textContent = "🔄 Refresh";
        showFlash("Data refreshed from Supabase.");
      });

      document.getElementById("saveAnnouncementBtn").addEventListener("click", async () => {
        const val = document.getElementById("announcementInput").value.trim();
        state.meta.announcement = val;
        await dbSaveMeta("announcement", val);
        const banner = document.getElementById("announcementBanner");
        if (val) { banner.textContent = `📢 ${val}`; banner.style.display = "block"; }
        else { banner.style.display = "none"; }
        showFlash("Announcement saved.");
      });

      document.getElementById("exportCsvBtn").addEventListener("click", () => {
        const rows = [["Ticket#", "Name", "Phone", "FIN", "Status", "Time"]];
        Object.entries(state.tickets).forEach(([n, t]) => {
          rows.push([n, t.name, t.phone, t.fin || "", t.status, t.time ? new Date(t.time).toLocaleString() : ""]);
        });
        const csvContent = rows.map(r => r.map(x => `"${x}"`).join(",")).join("\n");
        const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
        const url = URL.createObjectURL(blob);
        const link = document.createElement("a");
        link.href = url;
        link.setAttribute("download", "buyers_export.csv");
        link.click();
      });

      const resetBtn = document.getElementById("systemResetBtn");
      const cancelResetBtn = document.getElementById("cancelResetBtn");
      const warningText = document.getElementById("resetWarningText");

      resetBtn.addEventListener("click", async () => {
        if (!state.confirmResetActive) {
          state.confirmResetActive = true;
          warningText.classList.remove("hidden");
          cancelResetBtn.classList.remove("hidden");
          resetBtn.textContent = "⚠️ CONFIRM RESET";
        } else {
          await dbDeleteAll();
          state.confirmResetActive = false;
          warningText.classList.add("hidden");
          cancelResetBtn.classList.add("hidden");
          resetBtn.textContent = "🗑️ Reset All Tickets";
          showFlash("All tickets reset.");
          renderAdminTabs();
        }
      });

      cancelResetBtn.addEventListener("click", () => {
        state.confirmResetActive = false;
        warningText.classList.add("hidden");
        cancelResetBtn.classList.add("hidden");
        resetBtn.textContent = "🗑️ Reset All Tickets";
      });

      document.getElementById("ticketDetailModal").addEventListener("click", e => {
        if (e.target === document.getElementById("ticketDetailModal")) closeTicketModal();
      });
    });
  </script>
</body>
</html>
