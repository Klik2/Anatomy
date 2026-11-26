<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0" />
  <meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self' 'unsafe-inline' https://sdk.minepi.com https://cdn.tailwindcss.com https://unpkg.com https://cdnjs.cloudflare.com https://cdn.jsdelivr.net https://translate.google.com https://translate.googleapis.com; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com https://translate.googleapis.com; font-src 'self' https://fonts.gstatic.com; img-src 'self' data: blob: https://raw.githubusercontent.com https://www.gstatic.com https://translate.googleapis.com; connect-src 'self' https://socialchain.app https://backend.appstudio-u7cm9zhmha0ruwv8.piappengine.com https://translate.googleapis.com; frame-src 'self' https://*.minepi.com https://*.pinet.com https://translate.google.com;" />
  <title>HUMAN ANATOMY 3D — Laboratorium Virtual Anatomi Tubuh Manusia 3D</title>

  <!-- Pi Network SDK -->
  <script src="https://sdk.minepi.com/pi-sdk.js"></script>

  <!-- Google Fonts: Space Grotesk, Inter, JetBrains Mono -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:ital,wght@0,400;0,500;0,600;1,400&family=Space+Grotesk:wght@500;600;700&display=swap" rel="stylesheet" />

  <!-- Tailwind CSS via CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            display: ['"Space Grotesk"', 'sans-serif'],
            sans: ['Inter', 'sans-serif'],
            mono: ['"JetBrains Mono"', 'monospace'],
          },
          colors: {
            holo: {
              bg: '#050B16',
              secondary: '#0B1728',
              sidebar: '#0D1B2F',
              card: '#102039',
              blue: '#0EA5E9',
              cyan: '#22D3EE',
              green: '#10B981',
              text: '#F8FAFC',
              muted: '#94A3B8',
              warn: '#F59E0B',
              err: '#F43F5E',
            },
          },
        },
      },
    };
  </script>

  <!-- Lucide Icons via CDN -->
  <script src="https://unpkg.com/lucide@0.378.0/dist/umd/lucide.min.js"></script>

  <!-- Three.js r128 + OrbitControls + GLTFLoader via CDN -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/loaders/GLTFLoader.js"></script>

  <style>
    :root {
      --bg-main: #050B16;
      --bg-secondary: #0B1728;
      --bg-sidebar: #0B1728;
      --bg-card: #0B1728;
      --border-holo: rgba(34, 211, 238, 0.28);
      --glow-holo: 0 0 24px rgba(14, 165, 233, 0.18);
      --text-primary: #F8FAFC;
      --text-secondary: #94A3B8;
      --accent-blue: #0EA5E9;
      --accent-cyan: #22D3EE;
      --accent-green: #10B981;
    }

    html.light-theme {
      --bg-main: #F8FAFC;
      --bg-secondary: #E2E8F0;
      --bg-sidebar: #FFFFFF;
      --bg-card: #F1F5F9;
      --border-holo: rgba(14, 165, 233, 0.35);
      --glow-holo: 0 4px 20px rgba(14, 165, 233, 0.12);
      --text-primary: #050B16;
      --text-secondary: #475569;
    }

    * {
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
    }

    html, body {
      margin: 0;
      padding: 0;
      width: 100%;
      height: 100%;
      background-color: var(--bg-main);
      color: var(--text-primary);
      font-family: 'Inter', sans-serif;
      overflow: hidden;
      user-select: none;
    }

    .font-display { font-family: 'Space Grotesk', sans-serif; }
    .font-mono { font-family: 'JetBrains Mono', monospace; }

    /* Glassmorphism & Holographic Panels */
    .holo-panel {
      background: color-mix(in srgb, var(--bg-sidebar) 92%, transparent);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid var(--border-holo);
      box-shadow: var(--glow-holo);
    }

    .holo-card {
      background: color-mix(in srgb, var(--bg-card) 88%, transparent);
      border: 1px solid var(--border-holo);
      transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
    }

    .holo-card:hover {
      border-color: #22D3EE;
      box-shadow: 0 0 18px rgba(34, 211, 238, 0.22);
    }

    .holo-card.active {
      background: linear-gradient(135deg, rgba(14, 165, 233, 0.26), rgba(34, 211, 238, 0.14));
      border-color: #22D3EE;
      box-shadow: 0 0 22px rgba(34, 211, 238, 0.32);
    }

    @keyframes pulseHeartbeat {
      0%, 100% { transform: scale(1); filter: drop-shadow(0 0 18px rgba(34, 211, 238, 0.45)); }
      15% { transform: scale(1.06); filter: drop-shadow(0 0 32px rgba(244, 63, 94, 0.75)); }
      30% { transform: scale(0.99); }
      45% { transform: scale(1.04); filter: drop-shadow(0 0 28px rgba(34, 211, 238, 0.8)); }
    }

    @keyframes radarSpinSlow {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }

    .welcome-heart-pulse {
      animation: pulseHeartbeat 1.8s infinite ease-in-out;
    }

    .welcome-radar-ring {
      animation: radarSpinSlow 24s linear infinite;
    }

    /* Animated Holographic Scanline Overlay */
    .scan-grid {
      background-image:
        linear-gradient(to right, rgba(34, 211, 238, 0.04) 1px, transparent 1px),
        linear-gradient(to bottom, rgba(34, 211, 238, 0.04) 1px, transparent 1px);
      background-size: 40px 40px;
    }

    @keyframes holoSweep {
      0% { transform: translateY(-100%); opacity: 0; }
      20% { opacity: 0.45; }
      80% { opacity: 0.45; }
      100% { transform: translateY(100vh); opacity: 0; }
    }

    .holo-sweep-line {
      position: absolute;
      left: 0;
      right: 0;
      height: 2px;
      background: linear-gradient(90deg, transparent, #22D3EE, #0EA5E9, #22D3EE, transparent);
      box-shadow: 0 0 15px #22D3EE;
      pointer-events: none;
      animation: holoSweep 7s linear infinite;
      z-index: 4;
    }

    /* Custom Scrollbars */
    .custom-scroll {
      overflow-y: auto;
      touch-action: pan-y;
      scrollbar-width: thin;
      scrollbar-color: rgba(34, 211, 238, 0.35) transparent;
    }
    .custom-scroll::-webkit-scrollbar { width: 5px; height: 5px; }
    .custom-scroll::-webkit-scrollbar-track { background: transparent; }
    .custom-scroll::-webkit-scrollbar-thumb {
      background: rgba(34, 211, 238, 0.35);
      border-radius: 9999px;
    }

    /* 3D Canvas Touch Rules */
    #webgl-container {
      touch-action: none;
      position: relative;
      width: 100%;
      height: 100%;
    }
    #webgl-container canvas {
      display: block;
      width: 100% !important;
      height: 100% !important;
      outline: none;
      touch-action: none;
    }

    /* Numbered 3D Hotspot Pins */
    .hotspot-pin {
      position: absolute;
      transform: translate(-50%, -50%);
      width: 36px;
      height: 36px;
      border-radius: 9999px;
      background: radial-gradient(circle at 30% 30%, #0EA5E9, #050B16);
      border: 2px solid #22D3EE;
      color: #F8FAFC;
      font-family: 'JetBrains Mono', monospace;
      font-weight: 700;
      font-size: 13px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      box-shadow: 0 0 14px rgba(34, 211, 238, 0.65), inset 0 0 8px rgba(34, 211, 238, 0.4);
      transition: transform 0.18s ease, background 0.2s ease, box-shadow 0.2s ease, opacity 0.2s ease;
      z-index: 15;
    }

    .hotspot-pin::after {
      content: '';
      position: absolute;
      inset: -5px;
      border-radius: 9999px;
      border: 1px solid rgba(34, 211, 238, 0.45);
      animation: pinPulse 2.2s infinite ease-out;
      pointer-events: none;
    }

    @keyframes pinPulse {
      0% { transform: scale(0.9); opacity: 0.9; }
      100% { transform: scale(1.45); opacity: 0; }
    }

    .hotspot-pin:hover, .hotspot-pin.selected {
      transform: translate(-50%, -50%) scale(1.22);
      background: radial-gradient(circle at 30% 30%, #22D3EE, #0284C7);
      color: #050B16;
      box-shadow: 0 0 22px #22D3EE;
      z-index: 20;
    }

    .hotspot-pin.quiz-correct {
      background: #10B981 !important;
      border-color: #A7F3D0 !important;
      color: #050B16 !important;
      box-shadow: 0 0 25px #10B981 !important;
    }

    .hotspot-pin.quiz-wrong {
      background: #F43F5E !important;
      border-color: #FECDD3 !important;
      color: #FFFFFF !important;
      box-shadow: 0 0 25px #F43F5E !important;
    }

    /* Device Preview Simulation Frame */
    #app-shell {
      transition: max-width 0.35s ease, height 0.35s ease, border-radius 0.35s ease;
    }
    #app-shell.preview-tablet {
      max-width: 900px;
      margin: 0 auto;
      border-left: 1px solid rgba(34, 211, 238, 0.35);
      border-right: 1px solid rgba(34, 211, 238, 0.35);
    }
    #app-shell.preview-mobile {
      max-width: 430px;
      margin: 0 auto;
      border-left: 1px solid rgba(34, 211, 238, 0.35);
      border-right: 1px solid rgba(34, 211, 238, 0.35);
    }
    #app-shell.preview-tv {
      font-size: 1.08rem;
    }

    /* Forced Drawer Layout when simulating Tablet/Mobile on a large screen */
    #app-shell.preview-tablet #left-sidebar,
    #app-shell.preview-mobile #left-sidebar {
      position: fixed;
      top: 0;
      bottom: 0;
      left: 0;
      z-index: 40;
    }
    #app-shell.preview-tablet #right-panel,
    #app-shell.preview-mobile #right-panel {
      position: fixed;
      top: 0;
      bottom: 0;
      right: 0;
      z-index: 40;
    }

    /* Smart TV Remote Focus Ring */
    .tv-focus-mode button:focus,
    .tv-focus-mode select:focus,
    .tv-focus-mode input:focus {
      outline: 3px solid #22D3EE !important;
      outline-offset: 2px;
      box-shadow: 0 0 20px rgba(34, 211, 238, 0.8) !important;
    }

    /* Touch target minimum */
    .touch-btn {
      min-height: 40px;
      min-width: 40px;
    }
    @media (pointer: coarse) {
      .touch-btn {
        min-height: 44px;
        min-width: 44px;
      }
    }

    /* Light Theme Contrast Adjustments */
    html.light-theme .text-white {
      color: #0F172A !important;
    }
    html.light-theme .text-slate-200,
    html.light-theme .text-slate-300 {
      color: #334155 !important;
    }
    html.light-theme .text-slate-400 {
      color: #475569 !important;
    }
    html.light-theme select,
    html.light-theme input[type="text"],
    html.light-theme input[type="url"] {
      background-color: #FFFFFF !important;
      color: #0F172A !important;
    }
    html.light-theme .hotspot-pin {
      color: #F8FAFC !important;
    }

    /* Hide Google Translate Top Banner if injected */
    .goog-te-banner-frame.skiptranslate { display: none !important; }
    body { top: 0px !important; }
  </style>
</head>
<body class="h-screen w-screen overflow-hidden flex flex-col bg-[#050B16] text-[#F8FAFC]">

  <!-- ===================================================================== -->
  <!-- 1. WELCOME PAGE OVERLAY (ANIMATED HOLOGRAPHIC HEART SPLASH SCREEN)    -->
  <!-- ===================================================================== -->
  <section id="welcome-screen" class="fixed inset-0 z-50 flex flex-col items-center justify-between p-5 sm:p-8 bg-[#050B16] scan-grid overflow-hidden transition-opacity duration-500">
    <!-- Top Museum Status & Language Selector Dropdown -->
    <div class="w-full max-w-4xl flex items-center justify-between z-20 gap-2">
      <div class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-[#0B1728]/90 border border-[#22D3EE]/40">
        <span class="w-2 h-2 rounded-full bg-[#10B981] animate-ping"></span>
        <span class="text-[11px] font-mono tracking-widest uppercase text-[#22D3EE]">MEDICAL HOLOGRAPHIC LAB 3D</span>
      </div>

      <!-- Language Selector Dropdown with Flag Icons -->
      <div class="relative" id="welcome-lang-wrapper">
        <button id="btn-welcome-lang" type="button" class="touch-btn flex items-center gap-2 px-3 py-1.5 rounded-full bg-[#0B1728]/95 hover:bg-[#0EA5E9]/20 border border-[#22D3EE]/45 text-xs font-medium text-[#F8FAFC] shadow-[0_0_15px_rgba(34,211,238,0.2)] transition cursor-pointer" aria-label="Select Language">
          <i data-lucide="globe" class="w-3.5 h-3.5 text-[#22D3EE]"></i>
          <span id="welcome-lang-flag" class="text-sm leading-none">🇬🇧</span>
          <span id="welcome-lang-label" class="font-mono text-[11px] text-[#22D3EE]">EN</span>
          <i data-lucide="chevron-down" class="w-3.5 h-3.5 text-[#94A3B8]"></i>
        </button>

        <div id="welcome-lang-dropdown" class="hidden absolute right-0 mt-2 w-52 max-h-72 overflow-y-auto custom-scroll rounded-2xl holo-panel bg-[#0B1728] border border-[#22D3EE]/45 p-1.5 shadow-[0_12px_35px_rgba(5,11,22,0.9)] z-50 space-y-0.5 text-xs">
          <button type="button" data-wlang="en" data-flag="🇬🇧" data-code="EN" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇬🇧</span><span>English</span>
          </button>
          <button type="button" data-wlang="id" data-flag="🇮🇩" data-code="ID" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇮🇩</span><span>Indonesia</span>
          </button>
          <button type="button" data-wlang="de" data-flag="🇩🇪" data-code="DE" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇩🇪</span><span>German (Deutsch)</span>
          </button>
          <button type="button" data-wlang="fr" data-flag="🇫🇷" data-code="FR" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇫🇷</span><span>France (Français)</span>
          </button>
          <button type="button" data-wlang="es" data-flag="🇪🇸" data-code="ES" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇪🇸</span><span>Spain (Español)</span>
          </button>
          <button type="button" data-wlang="ru" data-flag="🇷🇺" data-code="RU" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇷🇺</span><span>Russian (Русский)</span>
          </button>
          <button type="button" data-wlang="zh-CN" data-flag="🇨🇳" data-code="ZH" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇨🇳</span><span>Chinese (中文)</span>
          </button>
          <button type="button" data-wlang="ko" data-flag="🇰🇷" data-code="KO" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇰🇷</span><span>Korean (한국어)</span>
          </button>
          <button type="button" data-wlang="ja" data-flag="🇯🇵" data-code="JA" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇯🇵</span><span>Japanese (日本語)</span>
          </button>
          <button type="button" data-wlang="vi" data-flag="🇻🇳" data-code="VI" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇻🇳</span><span>Vietnamese (Tiếng Việt)</span>
          </button>
          <button type="button" data-wlang="th" data-flag="🇹🇭" data-code="TH" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇹🇭</span><span>Thai (ไทย)</span>
          </button>
          <button type="button" data-wlang="hi" data-flag="🇮🇳" data-code="HI" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇮🇳</span><span>Hindi (हिन्दी)</span>
          </button>
          <button type="button" data-wlang="ar" data-flag="🇸🇦" data-code="AR" class="w-full flex items-center gap-2.5 px-2.5 py-2 rounded-xl hover:bg-[#0EA5E9]/25 text-left text-[#F8FAFC] transition cursor-pointer">
            <span class="text-base">🇸🇦</span><span>Arabic (العربية)</span>
          </button>
        </div>
      </div>
    </div>

    <!-- Wisdom Slogan Quote Below Header & Above Animated Heart Logo -->
    <div class="w-full max-w-2xl text-center z-10 px-3 pt-2">
      <p id="welcome-quote-text" class="text-sm sm:text-base font-normal italic text-white leading-relaxed drop-shadow-[0_0_12px_rgba(34,211,238,0.28)]">
        &ldquo;There is a piece of flesh in the body: when it is sound, the whole body is sound, and when it is corrupt, the whole body is corrupt&mdash;and that piece is the heart.&rdquo;
      </p>
    </div>

    <!-- Center Animated Holographic Heart & HUD Rings -->
    <div class="relative flex flex-col items-center justify-center my-auto z-10 max-w-md w-full text-center">
      <!-- Rotating HUD Reticle -->
      <div class="relative w-56 h-56 sm:w-72 sm:h-72 flex items-center justify-center">
        <svg class="absolute inset-0 w-full h-full welcome-radar-ring opacity-75" viewBox="0 0 300 300">
          <circle cx="150" cy="150" r="140" fill="none" stroke="#0EA5E9" stroke-width="1.2" stroke-dasharray="10 6" />
          <circle cx="150" cy="150" r="122" fill="none" stroke="#22D3EE" stroke-width="2" stroke-dasharray="45 18 8 18" />
          <circle cx="150" cy="150" r="98" fill="none" stroke="#10B981" stroke-width="1" stroke-dasharray="4 8" />
        </svg>

        <!-- Glowing Holographic Heart Emblem -->
        <div class="relative w-40 h-40 sm:w-48 sm:h-48 flex items-center justify-center welcome-heart-pulse">
          <svg viewBox="0 0 220 240" class="w-full h-full">
            <defs>
              <radialGradient id="heartGlow" cx="50%" cy="50%" r="50%">
                <stop offset="0%" stop-color="#22D3EE" stop-opacity="0.45" />
                <stop offset="100%" stop-color="#050B16" stop-opacity="0" />
              </radialGradient>
              <linearGradient id="myoGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" stop-color="#F43F5E" />
                <stop offset="55%" stop-color="#B91C1C" />
                <stop offset="100%" stop-color="#0EA5E9" />
              </linearGradient>
              <linearGradient id="aortaGrad" x1="0%" y1="0%" x2="100%" y2="0%">
                <stop offset="0%" stop-color="#0EA5E9" />
                <stop offset="100%" stop-color="#22D3EE" />
              </linearGradient>
            </defs>
            <circle cx="110" cy="125" r="95" fill="url(#heartGlow)" />
            <!-- Superior Vena Cava & Aortic Arch -->
            <path d="M74 34 L74 86 C74 96 88 96 88 86 L88 34 Z" fill="url(#aortaGrad)" opacity="0.9" />
            <path d="M98 78 L98 44 C98 20 144 20 144 48 L144 88 L128 88 L128 50 C128 38 114 38 114 50 L114 78 Z" fill="#E11D48" stroke="#22D3EE" stroke-width="1.5" />
            <path d="M108 26 L108 12 M122 24 L122 10 M135 28 L135 14" stroke="#22D3EE" stroke-width="4" stroke-linecap="round" />
            <!-- Pulmonary Trunk -->
            <path d="M94 94 C94 74 148 70 162 84 C154 96 122 94 112 106 Z" fill="#38BDF8" stroke="#F8FAFC" stroke-width="1" />
            <!-- Main Cardiac Chambers -->
            <path d="M62 116 C48 148 76 196 124 214 C162 194 176 142 154 106 C136 86 80 86 62 116 Z" fill="url(#myoGrad)" stroke="#22D3EE" stroke-width="2" />
            <!-- Holographic Wireframe Grid & Coronary Vessels -->
            <path d="M72 135 Q115 148 158 128 M68 160 Q115 174 152 156" fill="none" stroke="#22D3EE" stroke-width="1" opacity="0.65" />
            <path d="M108 106 C112 138 118 172 124 206 M112 134 L88 156 M115 148 L142 168" fill="none" stroke="#22D3EE" stroke-width="2.4" stroke-linecap="round" />
          </svg>
        </div>
      </div>

      <!-- Metallic Holographic Title -->
      <div class="mt-1 space-y-1.5">
        <h1 class="font-display font-bold text-3xl sm:text-5xl tracking-wider text-[#F8FAFC] drop-shadow-[0_0_20px_rgba(34,211,238,0.5)]">
          HUMAN <span class="text-[#22D3EE]">ANATOMY</span>
        </h1>
        <div class="inline-block px-5 py-1 rounded-xl bg-[#0B1728] border-2 border-[#22D3EE] shadow-[0_0_20px_rgba(34,211,238,0.4)]">
          <span class="font-display font-bold text-2xl sm:text-3xl tracking-widest text-[#22D3EE]">3D</span>
        </div>
        <p id="welcome-subtitle-text" class="text-xs sm:text-sm text-[#94A3B8] pt-1.5 max-w-sm mx-auto leading-relaxed">
          Interactive 3D Human Anatomy Virtual Laboratory &mdash; Explore Organ Structures, Physiology Simulations &amp; Medical Quizzes.
        </p>
      </div>

      <!-- Enter Button to Login / Lab Gate -->
      <div class="mt-5 flex flex-col sm:flex-row items-center gap-3 w-full justify-center">
        <button id="btn-enter-lab" type="button" class="touch-btn w-full sm:w-auto px-7 py-3.5 rounded-2xl bg-gradient-to-r from-[#0EA5E9] to-[#22D3EE] text-[#050B16] font-display font-bold text-sm sm:text-base tracking-wide shadow-[0_0_28px_rgba(34,211,238,0.55)] hover:brightness-110 transition flex items-center justify-center gap-2 cursor-pointer">
          <span id="welcome-enter-btn-text">ENTER LABORATORY</span>
          <i data-lucide="arrow-right" class="w-5 h-5"></i>
        </button>
      </div>
    </div>

    <!-- Bottom Welcome Footer -->
    <div class="w-full max-w-4xl flex items-center justify-between text-[11px] font-mono text-[#94A3B8] z-10">
      <span id="welcome-footer-left">32 INTERACTIVE ORGAN SPECIMENS</span>
      <span>by Te-eR Inovative @2026</span>
    </div>
  </section>

  <!-- ===================================================================== -->
  <!-- 2. USER LOGIN GATE OVERLAY (SIGN IN WITH PI OR CONTINUE AS GUEST)     -->
  <!-- ===================================================================== -->
  <section id="login-screen" class="hidden fixed inset-0 z-40 flex items-center justify-center p-4 bg-[#050B16]/95 backdrop-blur-xl scan-grid">
    <div class="holo-panel rounded-3xl max-w-md w-full p-6 sm:p-7 border-[#22D3EE]/50 bg-[#0B1728] shadow-[0_0_45px_rgba(14,165,233,0.28)] space-y-5 text-center">
      <div class="w-14 h-14 mx-auto rounded-2xl bg-[#050B16] border border-[#22D3EE]/50 flex items-center justify-center shadow-[0_0_20px_rgba(34,211,238,0.3)]">
        <i data-lucide="user-check" class="w-7 h-7 text-[#22D3EE]"></i>
      </div>

      <div class="space-y-1">
        <span id="login-badge-text" class="px-2.5 py-0.5 rounded-full text-[10px] font-mono uppercase tracking-widest bg-[#0EA5E9]/20 text-[#22D3EE] border border-[#22D3EE]/30">
          USER ACCESS
        </span>
        <h2 id="login-title-text" class="font-display font-bold text-xl sm:text-2xl text-[#F8FAFC]">
          Sign In to HUMAN ANATOMY 3D
        </h2>
        <p id="login-desc-text" class="text-xs text-[#94A3B8] leading-relaxed">
          Sign in with your Pi Network account to save your learning identity, or continue as a Guest without a Pi account.
        </p>
      </div>

      <div class="space-y-3 pt-1">
        <!-- Option 1: Sign in with Pi Network -->
        <button id="btn-login-pi" type="button" class="touch-btn w-full py-3.5 px-4 rounded-2xl bg-gradient-to-r from-amber-500 to-amber-400 text-[#050B16] font-display font-bold text-sm shadow-[0_0_24px_rgba(245,158,11,0.4)] hover:brightness-110 transition flex items-center justify-center gap-2.5 cursor-pointer">
          <i data-lucide="shield-check" class="w-5 h-5"></i>
          <span id="login-pi-btn-label">Sign in with Pi</span>
        </button>

        <div class="flex items-center gap-2 text-[11px] font-mono text-[#94A3B8]">
          <span class="flex-1 h-px bg-[#22D3EE]/20"></span>
          <span id="login-or-text">OR</span>
          <span class="flex-1 h-px bg-[#22D3EE]/20"></span>
        </div>

        <!-- Option 2: Continue as Guest -->
        <div class="space-y-2 text-left">
          <label id="login-guest-label" for="input-guest-name" class="block text-[10px] font-mono uppercase tracking-wider text-[#22D3EE]">
            GUEST DISPLAY NAME (OPTIONAL)
          </label>
          <input id="input-guest-name" type="text" placeholder="e.g., Medical Student / Guest 01" class="w-full px-3.5 py-2.5 rounded-xl bg-[#050B16] border border-[#22D3EE]/35 text-xs text-[#F8FAFC] placeholder-[#94A3B8] focus:outline-none focus:border-[#22D3EE]" />
        </div>

        <button id="btn-login-guest" type="button" class="touch-btn w-full py-3 px-4 rounded-2xl holo-card border-[#22D3EE]/45 text-xs sm:text-sm font-semibold text-[#22D3EE] hover:text-white flex items-center justify-center gap-2 cursor-pointer">
          <i data-lucide="user" class="w-4 h-4"></i>
          <span id="login-guest-btn-text">Continue as Guest (No Pi Account)</span>
        </button>
      </div>

      <div class="pt-2 border-t border-[#22D3EE]/15 flex items-center justify-between text-[11px] text-[#94A3B8]">
        <button id="btn-back-welcome" type="button" class="hover:text-[#22D3EE] transition cursor-pointer">← Back to Welcome</button>
        <span id="login-footer-right" class="font-mono text-[10px]">Open Education Mode</span>
      </div>
    </div>
  </section>

  <!-- ===================================================================== -->
  <!-- 3. MAIN 3D LABORATORY APPLICATION SHELL                               -->
  <!-- ===================================================================== -->
  <div id="app-shell" class="w-full h-full flex flex-col overflow-hidden">
    <!-- MAIN HEADER BAR -->
    <header class="holo-panel z-30 shrink-0 px-2.5 sm:px-4 py-1.5 sm:py-2 border-b border-cyan-500/25 flex items-center justify-between gap-2">
      <!-- Left: Brand & Museum Identity -->
      <div class="flex items-center gap-2 sm:gap-3 min-w-0">
        <button id="btn-logo-welcome" type="button" class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-gradient-to-br from-[#0EA5E9]/30 to-[#22D3EE]/20 border border-[#22D3EE]/50 flex items-center justify-center shrink-0 shadow-[0_0_15px_rgba(34,211,238,0.25)] cursor-pointer" title="Kembali ke Welcome Page">
          <i data-lucide="activity" class="w-5 h-5 sm:w-6 sm:h-6 text-[#22D3EE]"></i>
        </button>

        <div class="min-w-0">
          <div class="flex items-center gap-1.5 flex-wrap">
            <span class="px-1.5 py-0.5 text-[10px] font-mono font-semibold tracking-wider uppercase rounded bg-[#22D3EE]/15 text-[#22D3EE] border border-[#22D3EE]/30" data-i18n="badge_museum">MUSEUM MEDIS 3D</span>
            <span class="hidden sm:inline-block px-1.5 py-0.5 text-[10px] font-mono font-semibold tracking-wider uppercase rounded bg-[#10B981]/15 text-[#10B981] border border-[#10B981]/30">3D INTERACTIVE</span>
          </div>
          <h1 class="font-display font-bold text-sm sm:text-base md:text-lg tracking-tight leading-tight truncate text-[#0EA5E9]">
            HUMAN ANATOMY 3D
          </h1>
        </div>
      </div>

      <!-- Center: Student / Teacher Mode Toggle -->
      <div class="flex items-center gap-1.5 sm:gap-2">
        <button id="btn-role-mode" class="touch-btn hidden md:flex items-center gap-1.5 px-2.5 py-1.5 rounded-xl holo-card text-xs font-medium text-[#10B981] border-[#10B981]/30" title="Switch Student / Teacher Mode">
          <i data-lucide="graduation-cap" class="w-4 h-4"></i>
          <span id="role-label">Student</span>
        </button>
      </div>

      <!-- Right: Active Specimen Pill + User Session Badge + Settings Gear Dropdown + Anatomical Catalog (📥) -->
      <div class="flex items-center gap-1.5 sm:gap-2 relative">
        <!-- Active Specimen Info Badge -->
        <div class="hidden 2xl:flex flex-col items-end pr-2 border-r border-[#22D3EE]/20">
          <div class="flex items-center gap-1.5">
            <span class="text-[10px] font-mono uppercase tracking-wider text-[#22D3EE]" data-i18n="active_specimen">ACTIVE SPECIMEN</span>
            <span id="header-organ-system" class="px-1.5 py-0.2 rounded text-[10px] font-mono bg-[#0EA5E9]/20 text-[#22D3EE]">Cardiovascular</span>
          </div>
          <div class="text-xs font-semibold truncate max-w-[260px]">
            <span id="header-name-en">Heart</span> • <span id="header-name-id" class="text-[#22D3EE]">Jantung</span>
            <span id="header-latin" class="font-mono italic text-[11px] text-[var(--text-secondary)] ml-1">(Cor)</span>
          </div>
        </div>

        <!-- Active User Session Status Pill (Opens Login Gate to Switch Pi / Guest) -->
        <button id="btn-pi-auth" class="touch-btn flex items-center gap-1.5 px-2.5 py-1.5 rounded-xl holo-card text-xs font-semibold text-[#10B981] border-[#10B981]/40 hover:border-[#22D3EE] transition" title="Status Login Pengguna (Pi Network / Guest)">
          <i data-lucide="user-check" class="w-4 h-4"></i>
          <span id="pi-auth-label" class="max-w-[110px] truncate">Guest</span>
        </button>

        <!-- SETTINGS GEAR BUTTON (CONSOLIDATES VIEW MODES, LANGUAGE, THEME, DEVICE PREVIEW, FULLSCREEN & PHYSIOLOGY SIM) -->
        <div class="relative">
          <button id="btn-header-settings" type="button" class="touch-btn flex items-center justify-center gap-1.5 rounded-xl holo-card px-2.5 text-[#22D3EE] hover:text-white border-[#22D3EE]/40" aria-label="Pengaturan Tampilan" title="Pengaturan (Layer 3D, Bahasa, Layar, Tema, Physiology Sim)">
            <i data-lucide="settings" class="w-4 h-4"></i>
            <span class="hidden sm:inline text-xs font-medium" data-i18n="settings_btn">Setting</span>
            <i data-lucide="chevron-down" class="w-3.5 h-3.5 opacity-75"></i>
          </button>

          <!-- SETTINGS DROPDOWN MENU -->
          <div id="header-settings-dropdown" class="hidden absolute right-0 mt-2 w-80 max-h-[85vh] overflow-y-auto custom-scroll rounded-2xl holo-panel bg-[#0B1728] border border-[#22D3EE]/45 p-3.5 shadow-[0_12px_40px_rgba(5,11,22,0.92)] z-50 space-y-3 text-xs">
            <div class="flex items-center justify-between border-b border-[#22D3EE]/20 pb-2">
              <span class="font-display font-bold text-xs tracking-wider uppercase text-[#22D3EE] flex items-center gap-1.5">
                <i data-lucide="sliders" class="w-3.5 h-3.5"></i>
                <span data-i18n="settings_title">PENGATURAN TAMPILAN</span>
              </span>
              <button id="btn-close-settings" type="button" class="text-[#94A3B8] hover:text-white p-1" aria-label="Tutup Pengaturan">✕</button>
            </div>

            <!-- 1. Layer 3D Specimen / Full Body / Split Mode Switcher -->
            <div class="space-y-1.5">
              <span class="flex items-center gap-1.5 text-[11px] font-mono text-[#94A3B8]">
                <i data-lucide="layers" class="w-3.5 h-3.5 text-[#22D3EE]"></i>
                <span data-i18n="opt_view_layer">Mode Layer 3D (Organ / Full Body / Split)</span>
              </span>
              <div class="grid grid-cols-3 gap-1 rounded-xl bg-[#050B16]/90 p-1 border border-[#22D3EE]/30">
                <button id="mode-organ" type="button" class="touch-btn px-2 py-1.5 rounded-lg text-[11px] font-medium transition bg-[#0EA5E9]/25 text-[#22D3EE] border border-[#22D3EE]/40 flex items-center justify-center gap-1" title="Single Organ View">
                  <i data-lucide="box" class="w-3.5 h-3.5"></i>
                  <span data-i18n="view_organ">Organ</span>
                </button>
                <button id="mode-fullbody" type="button" class="touch-btn px-2 py-1.5 rounded-lg text-[11px] font-medium transition text-[var(--text-secondary)] hover:text-[#22D3EE] flex items-center justify-center gap-1" title="Full Body Interactive Anatomy">
                  <i data-lucide="person-standing" class="w-3.5 h-3.5"></i>
                  <span data-i18n="view_fullbody">Full Body</span>
                </button>
                <button id="mode-split" type="button" class="touch-btn px-2 py-1.5 rounded-lg text-[11px] font-medium transition text-[var(--text-secondary)] hover:text-[#22D3EE] flex items-center justify-center gap-1" title="Side-by-Side Split Comparison">
                  <i data-lucide="columns-2" class="w-3.5 h-3.5"></i>
                  <span data-i18n="view_split">Split</span>
                </button>
              </div>
            </div>

            <!-- 2. Pilihan Bahasa -->
            <div class="space-y-1">
              <label for="select-lang" class="flex items-center gap-1.5 text-[11px] font-mono text-[#94A3B8]">
                <i data-lucide="globe" class="w-3.5 h-3.5 text-[#22D3EE]"></i>
                <span data-i18n="opt_language">Pilihan Bahasa</span>
              </label>
              <select id="select-lang" aria-label="Language Selector" class="w-full rounded-xl bg-[#050B16] border border-[#22D3EE]/35 px-2.5 py-2 text-xs font-medium text-[#F8FAFC] cursor-pointer focus:border-[#22D3EE] focus:outline-none">
                <option value="en" selected>🇬🇧 English (EN)</option>
                <option value="id">🇮🇩 Indonesia (ID)</option>
                <option value="de">🇩🇪 German (DE)</option>
                <option value="fr">🇫🇷 France (FR)</option>
                <option value="es">🇪🇸 Spain (ES)</option>
                <option value="ru">🇷🇺 Russian (RU)</option>
                <option value="zh-CN">🇨🇳 Chinese (ZH)</option>
                <option value="ko">🇰🇷 Korean (KO)</option>
                <option value="ja">🇯🇵 Japanese (JA)</option>
                <option value="vi">🇻🇳 Vietnamese (VI)</option>
                <option value="th">🇹🇭 Thai (TH)</option>
                <option value="hi">🇮🇳 Hindi (HI)</option>
                <option value="ar">🇸🇦 Arabic (AR)</option>
              </select>
            </div>

            <!-- 3. Pilihan Layar Cerah / Gelap / Otomatis -->
            <div class="space-y-1">
              <label for="select-theme" class="flex items-center gap-1.5 text-[11px] font-mono text-[#94A3B8]">
                <i data-lucide="sun-moon" class="w-3.5 h-3.5 text-[#0EA5E9]"></i>
                <span data-i18n="opt_theme">Tema Layar (Gelap / Cerah / Otomatis)</span>
              </label>
              <select id="select-theme" aria-label="Appearance Theme" class="w-full rounded-xl bg-[#050B16] border border-[#22D3EE]/35 px-2.5 py-2 text-xs font-medium text-[#F8FAFC] cursor-pointer focus:border-[#22D3EE] focus:outline-none">
                <option value="dark">Gelap (Medical Holographic Dark)</option>
                <option value="light">Cerah (Light Mode)</option>
                <option value="auto">Otomatis (Ikuti Sistem)</option>
              </select>
            </div>

            <!-- 4. Mode Pilihan Layar (Viewport Device Profile) -->
            <div class="space-y-1">
              <label for="select-device" class="flex items-center gap-1.5 text-[11px] font-mono text-[#94A3B8]">
                <i data-lucide="monitor-smartphone" class="w-3.5 h-3.5 text-[#10B981]"></i>
                <span data-i18n="opt_screen_mode">Mode Pilihan Layar</span>
              </label>
              <select id="select-device" aria-label="Viewport Layout Preview" class="w-full rounded-xl bg-[#050B16] border border-[#22D3EE]/35 px-2.5 py-2 text-xs font-medium text-[#F8FAFC] cursor-pointer focus:border-[#22D3EE] focus:outline-none">
                <option value="desktop">Desktop / Smartboard</option>
                <option value="laptop">Laptop</option>
                <option value="tablet">Tablet</option>
                <option value="mobile">Smartphone</option>
                <option value="tv">Smart TV (Remote)</option>
              </select>
            </div>

            <!-- 5. Perbesar Layar (Fullscreen) & Google Translate -->
            <div class="pt-0.5 flex flex-col gap-2">
              <button id="btn-fullscreen" type="button" class="touch-btn w-full py-2 px-3 rounded-xl bg-[#0EA5E9]/20 hover:bg-[#0EA5E9]/35 border border-[#22D3EE]/45 text-xs font-semibold text-[#F8FAFC] flex items-center justify-center gap-2 cursor-pointer transition">
                <i data-lucide="maximize-2" class="w-4 h-4 text-[#22D3EE]"></i>
                <span data-i18n="opt_fullscreen">Perbesar Layar (Fullscreen)</span>
              </button>

              <button id="btn-gtranslate" type="button" class="touch-btn w-full py-1.5 px-3 rounded-xl bg-[#050B16] hover:bg-[#0EA5E9]/15 border border-[#22D3EE]/25 text-[11px] text-[#94A3B8] hover:text-[#22D3EE] flex items-center justify-center gap-1.5 cursor-pointer transition">
                <i data-lucide="languages" class="w-3.5 h-3.5"></i>
                <span>Google Translate Widget</span>
              </button>
            </div>
          </div>
        </div>

        <!-- Mobile/Tablet Right Info Panel Toggle -->
        <button id="btn-toggle-right" class="touch-btn lg:hidden flex items-center justify-center rounded-xl holo-card px-2.5 text-cyan-400 hover:text-white" aria-label="Toggle Information Panel" title="Educational & Clinical Info">
          <i data-lucide="panel-right" class="w-5 h-5"></i>
        </button>

        <!-- Anatomical Catalog Toggle Button (📥) at Top-Right Corner -->
        <button id="btn-toggle-left" type="button" class="touch-btn flex items-center justify-center gap-1.5 rounded-xl holo-card px-2.5 text-cyan-300 hover:text-white border-[#22D3EE]/40" aria-label="Toggle Anatomical Catalog" title="Anatomical Catalog (📥)">
          <span class="text-base leading-none">📥</span>
          <span class="hidden xl:inline text-xs font-medium" data-i18n="catalog_short">Catalog</span>
        </button>
      </div>
    </header>

    <!-- Google Translate Widget Container (Hidden by default) -->
    <div id="gtranslate-box" class="hidden absolute top-14 right-4 z-50 holo-panel rounded-xl p-3 shadow-2xl">
      <div class="flex items-center justify-between gap-4 mb-2">
        <span class="text-xs font-mono text-cyan-300">GOOGLE TRANSLATE (OPTIONAL)</span>
        <button id="btn-close-gt" class="text-xs text-slate-400 hover:text-white">✕</button>
      </div>
      <div id="google_translate_element" class="text-xs"></div>
      <p class="text-[10px] text-slate-400 mt-1.5 max-w-[220px]">Uses built-in offline EN/ID dictionary if external service is unreachable.</p>
    </div>

    <!-- MAIN WORKSPACE: LEFT CATALOG + CENTER 3D VIEWPORT + RIGHT INFO PANEL -->
    <div class="relative flex-1 flex overflow-hidden">

      <!-- LEFT SIDEBAR: ANATOMICAL ORGAN CATALOG -->
      <aside id="left-sidebar" class="holo-panel fixed lg:static inset-y-0 left-0 z-40 w-[295px] xl:w-[305px] shrink-0 flex flex-col border-r border-cyan-500/25 transform -translate-x-full lg:translate-x-0 transition-transform duration-300 ease-out">
        <!-- Catalog Header -->
        <div class="p-3 border-b border-cyan-500/20">
          <div class="flex items-center justify-between mb-2">
            <div class="flex items-center gap-2">
              <i data-lucide="layers" class="w-4 h-4 text-cyan-400"></i>
              <h2 class="font-display font-bold text-xs tracking-wider uppercase text-cyan-300" data-i18n="catalog_title">ANATOMICAL CATALOG</h2>
            </div>
            <div class="flex items-center gap-1.5">
              <span id="catalog-count" class="px-2 py-0.5 rounded-full text-[11px] font-mono bg-cyan-500/15 text-cyan-300 border border-cyan-400/30">32</span>
              <button id="btn-close-left" class="lg:hidden p-1.5 rounded-lg text-slate-400 hover:text-white" aria-label="Close Catalog">
                <i data-lucide="x" class="w-4 h-4"></i>
              </button>
            </div>
          </div>

          <!-- Search Input (Indonesian, English, Latin) -->
          <div class="relative">
            <i data-lucide="search" class="w-4 h-4 text-cyan-400/70 absolute left-3 top-1/2 -translate-y-1/2 pointer-events-none"></i>
            <input id="catalog-search" type="text" placeholder="Search EN / ID / Latin..." class="w-full pl-9 pr-8 py-2 rounded-xl bg-slate-950/70 border border-cyan-500/25 text-xs text-[var(--text-primary)] placeholder-slate-400 focus:outline-none focus:border-cyan-400" />
            <button id="btn-clear-search" class="hidden absolute right-2.5 top-1/2 -translate-y-1/2 text-slate-400 hover:text-white text-xs" aria-label="Clear Search">✕</button>
          </div>

          <!-- Category Filter Pills -->
          <div id="category-filters" class="flex gap-1.5 overflow-x-auto custom-scroll pt-2.5 pb-1">
            <!-- Populated dynamically -->
          </div>
        </div>

        <!-- Organ Cards List -->
        <div id="catalog-list" class="flex-1 custom-scroll p-2.5 space-y-2">
          <!-- Populated dynamically -->
        </div>

        <!-- Custom GLB/GLTF Loader Bar -->
        <div class="p-2.5 border-t border-cyan-500/20 bg-slate-950/40">
          <div class="flex items-center justify-between gap-1.5">
            <button id="btn-open-glb-modal" class="touch-btn flex-1 py-1.5 px-2.5 rounded-xl holo-card text-[11px] font-mono text-cyan-300 hover:text-white flex items-center justify-center gap-1.5">
              <i data-lucide="upload-cloud" class="w-3.5 h-3.5"></i>
              <span data-i18n="load_glb">Load Validated GLB/GLTF</span>
            </button>
            <button id="btn-teacher-dashboard" class="touch-btn py-1.5 px-2.5 rounded-xl holo-card text-[11px] font-mono text-emerald-300 hover:text-white flex items-center justify-center gap-1" title="Teacher & Student Analytics">
              <i data-lucide="clipboard-list" class="w-3.5 h-3.5"></i>
            </button>
          </div>
        </div>
      </aside>

      <!-- CENTER 3D WEBGL VIEWPORT -->
      <main class="relative flex-1 flex flex-col overflow-hidden scan-grid bg-gradient-to-b from-[#050B16] via-[#081326] to-[#050B16]">
        <!-- Subtle Holographic Sweep Line -->
        <div class="holo-sweep-line"></div>

        <!-- Top-Left Viewport Overlay: Active Specimen Banner + Full Body Controls -->
        <div class="absolute top-3 left-3 z-20 flex flex-col gap-2 pointer-events-none max-w-[65%]">
          <div class="holo-panel rounded-xl px-3 py-2 pointer-events-auto inline-flex flex-col">
            <div class="flex items-center gap-2">
              <span class="w-2 h-2 rounded-full bg-cyan-400 animate-pulse"></span>
              <span id="vp-system-badge" class="text-[10px] font-mono uppercase tracking-wider text-cyan-300">Cardiovascular</span>
            </div>
            <div class="font-display font-bold text-sm sm:text-base text-white leading-snug">
              <span id="vp-title-en">Heart</span>
              <span class="text-cyan-300 font-normal"> / </span>
              <span id="vp-title-id" class="text-cyan-300">Jantung</span>
            </div>
            <div id="vp-title-latin" class="font-mono italic text-[11px] text-slate-300">Cor / Cardia</div>
          </div>

          <!-- Full Body Layer Controls (Visible only in Full Body Mode) -->
          <div id="fullbody-controls" class="hidden holo-panel rounded-xl p-2.5 pointer-events-auto flex-col gap-2">
            <div class="flex items-center justify-between gap-2">
              <span class="text-[10px] font-mono uppercase text-cyan-300">FULL BODY LAYERS</span>
              <button id="btn-zoom-selected-organ" class="px-2 py-0.5 rounded bg-sky-500/30 border border-cyan-400/50 text-[10px] font-mono text-cyan-200 hover:bg-sky-500/50">
                Inspect Organ
              </button>
            </div>
            <div class="flex flex-wrap gap-2 text-xs">
              <label class="flex items-center gap-1.5 cursor-pointer">
                <input type="checkbox" id="chk-body-shell" checked class="accent-cyan-400" />
                <span>Body Shell</span>
              </label>
              <label class="flex items-center gap-1.5 cursor-pointer">
                <input type="checkbox" id="chk-body-skeleton" checked class="accent-cyan-400" />
                <span>Skeleton</span>
              </label>
            </div>
            <div class="flex items-center gap-2 text-xs">
              <span class="text-slate-400">Pelvis:</span>
              <select id="select-body-sex" class="rounded bg-slate-900 border border-cyan-500/30 px-2 py-0.5 text-xs text-cyan-300">
                <option value="female">Female</option>
                <option value="male">Male</option>
              </select>
            </div>
            <p class="text-[10px] text-slate-400">Tap any organ inside the 3D body to inspect.</p>
          </div>
        </div>

        <!-- Top-Right Viewport Overlay: Physiology Simulation Selector & Split Compare Selector -->
        <div class="absolute top-3 right-3 z-20 flex flex-col items-end gap-2 pointer-events-none">
          <!-- Physiology Simulation Selector -->
          <div class="holo-panel rounded-xl px-2.5 py-2 pointer-events-auto">
            <div class="flex items-center gap-2">
              <span class="text-[10px] font-mono uppercase text-cyan-300" data-i18n="phys_sim">PHYSIOLOGY SIM</span>
              <select id="select-phys-sim" aria-label="Physiology Simulation Mode" class="rounded-lg bg-slate-900/90 border border-cyan-500/30 px-2 py-1 text-xs text-white cursor-pointer">
                <option value="auto" data-i18n="phys_auto">Auto (Organ)</option>
                <option value="blood" data-i18n="phys_blood">Blood Flow</option>
                <option value="respiration" data-i18n="phys_resp">Respiration</option>
                <option value="digestion" data-i18n="phys_dig">Digestion</option>
                <option value="nervous" data-i18n="phys_nerv">Nervous Signal</option>
                <option value="off" data-i18n="phys_off">Off</option>
              </select>
            </div>
            <div class="flex items-center gap-3 mt-1 text-[10px] font-mono">
              <span class="flex items-center gap-1 text-rose-400"><span class="w-1.5 h-1.5 rounded-full bg-rose-400"></span><span data-i18n="phys_arterial">Arterial (O₂)</span></span>
              <span class="flex items-center gap-1 text-sky-400"><span class="w-1.5 h-1.5 rounded-full bg-sky-400"></span><span data-i18n="phys_venous">Venous (CO₂)</span></span>
            </div>
          </div>

          <!-- Split-Screen Comparison Controls (Visible only in Split Mode) -->
          <div id="split-controls" class="hidden holo-panel rounded-xl px-2.5 py-2 pointer-events-auto flex items-center gap-2">
            <button id="btn-sync-orbit" class="px-2 py-1 rounded-lg bg-cyan-500/25 border border-cyan-400/50 text-xs text-cyan-200 flex items-center gap-1" title="Synchronize or Independent Camera Rotation">
              <i data-lucide="link" class="w-3.5 h-3.5"></i>
              <span id="sync-orbit-label">Sync Orbit</span>
            </button>
            <span class="text-xs font-mono text-slate-400">R:</span>
            <select id="select-split-right" aria-label="Right Comparison Organ" class="rounded-lg bg-slate-900/90 border border-cyan-500/30 px-2 py-1 text-xs text-cyan-300 max-w-[150px]">
              <!-- Populated dynamically -->
            </select>
          </div>
        </div>

        <!-- Quiz Active Banner on Viewport (Visible during Quiz) -->
        <div id="viewport-quiz-banner" class="hidden absolute top-24 left-1/2 -translate-x-1/2 z-20 holo-panel rounded-2xl px-4 py-2.5 border-cyan-400/60 text-center max-w-[90%] shadow-2xl">
          <div class="text-[10px] font-mono uppercase tracking-widest text-cyan-400">3D ANATOMY QUIZ</div>
          <div id="vp-quiz-prompt" class="text-xs sm:text-sm font-semibold text-white mt-0.5">Click the pin identifying the Aortic Arch.</div>
        </div>

        <!-- Split Screen Center Divider Line -->
        <div id="split-divider" class="hidden absolute inset-y-0 left-1/2 w-[2px] bg-gradient-to-b from-transparent via-cyan-400 to-transparent z-10 pointer-events-none">
          <span class="absolute top-16 -left-16 px-2 py-0.5 rounded bg-slate-900/90 border border-cyan-500/40 text-[10px] font-mono text-cyan-300">L: Primary</span>
          <span class="absolute top-16 left-3 px-2 py-0.5 rounded bg-slate-900/90 border border-cyan-500/40 text-[10px] font-mono text-emerald-300">R: Compare</span>
        </div>

        <!-- 3D WebGL Canvas Mount -->
        <div id="webgl-container" class="flex-1">
          <!-- Three.js Canvas Injected Here -->
        </div>

        <!-- 2D Projected Hotspot Pins Layer -->
        <div id="hotspots-overlay" class="absolute inset-0 pointer-events-none overflow-hidden z-10">
          <!-- Dynamic Hotspot Pins 1..5 injected here -->
        </div>

        <!-- WebGL Loading / Error Overlay -->
        <div id="viewport-status" class="hidden absolute inset-0 z-30 bg-slate-950/80 backdrop-blur-md flex flex-col items-center justify-center p-6 text-center">
          <div class="w-12 h-12 rounded-full border-2 border-cyan-400 border-t-transparent animate-spin mb-3"></div>
          <p id="viewport-status-text" class="text-sm font-mono text-cyan-300">Initializing WebGL Medical Hologram...</p>
        </div>

        <!-- FLOATING BOTTOM CONTROL DOCK -->
        <div class="absolute bottom-2.5 left-1/2 -translate-x-1/2 z-20 flex flex-col items-center gap-1.5 w-[96%] max-w-[920px] pointer-events-none">
          <!-- Expandable Sub-Panel for Section Clipping & Exploded View Sliders -->
          <div id="dock-sliders-drawer" class="hidden holo-panel rounded-2xl px-3.5 py-2.5 pointer-events-auto flex flex-wrap items-center justify-center gap-4 text-xs shadow-xl">
            <!-- Anatomical Clipping Plane Controls -->
            <div class="flex items-center gap-2">
              <i data-lucide="scissors" class="w-4 h-4 text-cyan-400"></i>
              <span class="font-mono text-[11px] text-cyan-300" data-i18n="clipping">Section:</span>
              <select id="select-clip-plane" class="rounded-lg bg-slate-900 border border-cyan-500/30 px-2 py-1 text-xs text-white">
                <option value="none">Nonaktif (Off)</option>
                <option value="axial">Axial — Y (Transverse)</option>
                <option value="sagittal">Sagittal — X (Left/Right)</option>
                <option value="coronal">Coronal — Z (Anterior/Posterior)</option>
              </select>
              <input id="slider-clip-dist" type="range" min="-1.5" max="1.5" step="0.05" value="0.2" class="w-24 sm:w-28 accent-cyan-400 cursor-pointer" title="Clipping Distance" />
              <button id="btn-anim-clip" class="px-2 py-1 rounded-lg holo-card text-[11px] font-mono text-cyan-300 hover:text-white flex items-center gap-1" title="Automated Volumetric Scan Sweep">
                <i data-lucide="scan-line" class="w-3.5 h-3.5"></i>
                <span>Scan</span>
              </button>
            </div>

            <!-- Exploded Anatomy Slider -->
            <div class="flex items-center gap-2 border-l border-cyan-500/20 pl-3">
              <i data-lucide="expand" class="w-4 h-4 text-emerald-400"></i>
              <span class="font-mono text-[11px] text-emerald-300" data-i18n="explode">Explode:</span>
              <input id="slider-explode" type="range" min="0" max="1" step="0.02" value="0" class="w-24 sm:w-28 accent-emerald-400 cursor-pointer" title="Exploded Anatomy Separation" />
              <span id="explode-val" class="font-mono text-[11px] text-slate-300 w-8">0%</span>
            </div>
          </div>

          <!-- Toggle Dock Visibility Pill (Compact on small screens) -->
          <button id="btn-toggle-dock" class="pointer-events-auto px-3 py-1 rounded-full holo-panel text-[11px] font-mono text-cyan-300 hover:text-white flex items-center gap-1.5 shadow-lg">
            <i data-lucide="sliders-horizontal" class="w-3 h-3"></i>
            <span id="dock-toggle-text">Hide Controls</span>
          </button>

          <!-- Main Control Buttons Row -->
          <div id="bottom-dock-bar" class="holo-panel rounded-2xl p-1.5 pointer-events-auto flex items-center gap-1 sm:gap-1.5 overflow-x-auto max-w-full shadow-2xl">
            <!-- Section / Explode Drawer Toggle -->
            <button id="dock-btn-section" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="3D Section Clipping & Exploded Anatomy">
              <i data-lucide="scissors" class="w-4 h-4 text-cyan-400"></i>
              <span class="hidden sm:inline" data-i18n="btn_section">Section / Explode</span>
            </button>

            <!-- Holographic Volumetric Scan -->
            <button id="dock-btn-holoscan" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="Holographic Volumetric Scan Sweep">
              <i data-lucide="radar" class="w-4 h-4 text-cyan-400"></i>
              <span class="hidden md:inline" data-i18n="btn_holoscan">Holo Scan</span>
            </button>

            <!-- X-Ray Mode -->
            <button id="dock-btn-xray" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="Medical X-Ray Translucent Visualization">
              <i data-lucide="eye" class="w-4 h-4 text-sky-400"></i>
              <span class="hidden sm:inline" data-i18n="btn_xray">X-Ray</span>
            </button>

            <!-- Wireframe Mode -->
            <button id="dock-btn-wireframe" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="Mesh Wireframe Overlay">
              <i data-lucide="grid" class="w-4 h-4 text-indigo-400"></i>
              <span class="hidden md:inline" data-i18n="btn_wireframe">Wireframe</span>
            </button>

            <!-- Hotspots Toggle -->
            <button id="dock-btn-hotspots" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card active text-xs flex items-center gap-1.5 shrink-0" title="Show/Hide Numbered Anatomical Hotspots">
              <i data-lucide="map-pin" class="w-4 h-4 text-cyan-300"></i>
              <span class="hidden sm:inline" data-i18n="btn_hotspots">Hotspots</span>
            </button>

            <!-- Auto Rotate -->
            <button id="dock-btn-rotate" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="Smooth Auto-Rotation">
              <i data-lucide="rotate-cw" class="w-4 h-4 text-amber-400"></i>
              <span class="hidden md:inline" data-i18n="btn_rotate">Rotate</span>
            </button>

            <!-- Living Physiology (Heart Beat / Lung Respiration / Organ Pulse) -->
            <button id="dock-btn-physiology" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card active text-xs flex items-center gap-1.5 shrink-0" title="Toggle Rhythmic Physiological Animation">
              <i data-lucide="heart-pulse" class="w-4 h-4 text-rose-400"></i>
              <span class="hidden sm:inline" data-i18n="btn_physiology">Living Pulse</span>
            </button>

            <!-- Export High-Res PNG Study Snapshot -->
            <button id="dock-btn-snapshot" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="Save High-Resolution PNG Study Note">
              <i data-lucide="camera" class="w-4 h-4 text-emerald-400"></i>
              <span class="hidden lg:inline" data-i18n="btn_snapshot">PNG Note</span>
            </button>

            <!-- WebXR VR / AR Mode -->
            <button id="dock-btn-xr" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="Enter WebXR VR / AR Immersive Mode">
              <i data-lucide="glasses" class="w-4 h-4 text-purple-400"></i>
              <span class="hidden lg:inline">VR / AR</span>
            </button>

            <!-- Reset Camera -->
            <button id="dock-btn-reset" class="touch-btn px-2.5 py-1.5 rounded-xl holo-card text-xs flex items-center gap-1.5 shrink-0" title="Reset Camera Position & Zoom">
              <i data-lucide="refresh-ccw" class="w-4 h-4 text-cyan-300"></i>
              <span class="hidden sm:inline" data-i18n="btn_reset">Reset</span>
            </button>
          </div>
        </div>
      </main>

      <!-- RIGHT INFORMATION PANEL (STRUCTURE / CLINICAL / 3D QUIZ) -->
      <aside id="right-panel" class="holo-panel fixed lg:static inset-y-0 right-0 z-40 w-[320px] sm:w-[345px] shrink-0 flex flex-col border-l border-cyan-500/25 transform translate-x-full lg:translate-x-0 transition-transform duration-300 ease-out">
        <!-- Panel Tabs Header -->
        <div class="p-2.5 border-b border-cyan-500/20 flex items-center justify-between gap-1.5">
          <div class="grid grid-cols-3 gap-1 flex-1 bg-slate-950/60 p-1 rounded-xl border border-cyan-500/20">
            <button id="tab-btn-structure" class="touch-btn py-1.5 px-2 rounded-lg text-xs font-semibold bg-sky-500/25 text-cyan-300 border border-cyan-400/40 transition" data-i18n="tab_structure">
              Structure
            </button>
            <button id="tab-btn-clinical" class="touch-btn py-1.5 px-2 rounded-lg text-xs font-semibold text-[var(--text-secondary)] hover:text-cyan-300 transition" data-i18n="tab_clinical">
              Clinical
            </button>
            <button id="tab-btn-quiz" class="touch-btn py-1.5 px-2 rounded-lg text-xs font-semibold text-[var(--text-secondary)] hover:text-cyan-300 transition" data-i18n="tab_quiz">
              3D Quiz
            </button>
          </div>
          <button id="btn-close-right" class="lg:hidden p-2 rounded-xl holo-card text-slate-400 hover:text-white" aria-label="Close Info Panel">
            <i data-lucide="x" class="w-4 h-4"></i>
          </button>
        </div>

        <!-- Text-To-Speech Audio Narration Control Strip -->
        <div class="px-3 py-2 border-b border-cyan-500/20 bg-slate-950/40 flex flex-col gap-1.5">
          <div class="flex items-center justify-between gap-1.5">
            <div class="flex items-center gap-1.5 text-[11px] font-mono text-cyan-300">
              <i data-lucide="volume-2" class="w-3.5 h-3.5"></i>
              <span data-i18n="tts_title">AUDIO NARRATION</span>
            </div>
            <div class="flex items-center gap-1">
              <button id="tts-play" class="px-2 py-1 rounded-lg holo-card text-[11px] text-cyan-300 hover:text-white flex items-center gap-1" title="Read Active Tab Aloud">
                <i data-lucide="play" class="w-3 h-3"></i>
                <span data-i18n="tts_read">Read</span>
              </button>
              <button id="tts-pause" class="px-2 py-1 rounded-lg holo-card text-[11px] text-amber-300 hover:text-white" title="Pause / Resume">
                <i data-lucide="pause" class="w-3 h-3"></i>
              </button>
              <button id="tts-stop" class="px-2 py-1 rounded-lg holo-card text-[11px] text-rose-400 hover:text-white" title="Stop">
                <i data-lucide="square" class="w-3 h-3"></i>
              </button>
            </div>
          </div>
          <div class="flex items-center gap-2 text-[11px]">
            <select id="tts-voice" aria-label="Speech Voice" class="flex-1 rounded-lg bg-slate-900 border border-cyan-500/25 px-2 py-1 text-[11px] text-slate-200 truncate">
              <option value="">Default Browser Voice</option>
            </select>
            <span class="font-mono text-slate-400">Rate</span>
            <input id="tts-rate" type="range" min="0.6" max="1.6" step="0.1" value="1.0" class="w-14 accent-cyan-400" />
            <span id="tts-rate-val" class="font-mono text-cyan-300 w-6">1.0</span>
          </div>
        </div>

        <!-- TAB CONTENT CONTAINER -->
        <div class="flex-1 custom-scroll p-3 space-y-3">

          <!-- TAB A: STRUCTURE -->
          <div id="tab-content-structure" class="space-y-3">
            <!-- Brain Multi-View Anatomical Atlas Reference Card (Shown when Brain is active) -->
            <div id="brain-multiview-card" class="hidden holo-card rounded-xl p-2.5 border-[#22D3EE]/45 bg-[#050B16]/80 space-y-2">
              <div class="flex items-center justify-between">
                <span class="text-[10px] font-mono uppercase tracking-wider text-[#22D3EE]">MULTI-VIEW CEREBRAL ATLAS</span>
                <span class="text-[10px] font-mono text-[#10B981]">6 PROJECTIONS</span>
              </div>
              <canvas id="brain-atlas-canvas" width="480" height="240" class="w-full h-auto rounded-lg border border-[#22D3EE]/25 bg-[#050B16]"></canvas>
              <p class="text-[10px] text-[#94A3B8] leading-tight">
                Proyeksi anatomi otak: Anterior, Posterior, Lateral Kiri/Kanan, Superior (Dorsal), dan Inferior (Ventral / Chiasma Optikum).
              </p>
            </div>

            <!-- Scientific Approximation Notice -->
            <div class="rounded-xl p-2.5 bg-amber-500/10 border border-amber-400/35 text-[11px] text-amber-200 leading-relaxed">
              <span id="model-source-badge" class="font-semibold">Illustrative 3D procedural approximation</span> — hotspot anchors are mapped to schematic geometry unless a validated medical GLB model is loaded.
            </div>

            <!-- Anatomical Overview -->
            <div class="space-y-1">
              <h3 class="text-[11px] font-mono uppercase tracking-wider text-cyan-400" data-i18n="sec_overview">ANATOMICAL OVERVIEW</h3>
              <p id="info-overview" class="text-xs leading-relaxed text-[var(--text-primary)]"></p>
            </div>

            <!-- Main Physiological Function -->
            <div class="space-y-1">
              <h3 class="text-[11px] font-mono uppercase tracking-wider text-cyan-400" data-i18n="sec_function">MAIN PHYSIOLOGICAL FUNCTION</h3>
              <p id="info-physiology" class="text-xs leading-relaxed text-[var(--text-primary)]"></p>
            </div>

            <!-- Anatomical Terminology Box -->
            <div class="holo-card rounded-xl p-2.5 space-y-1">
              <div class="text-[10px] font-mono uppercase tracking-wider text-cyan-400" data-i18n="sec_terminology">ANATOMICAL TERMINOLOGY</div>
              <div class="text-xs">
                <span class="text-slate-400">ID:</span> <span id="term-id" class="font-semibold"></span>
                <span class="mx-1.5 text-slate-500">•</span>
                <span class="text-slate-400">EN:</span> <span id="term-en" class="font-semibold"></span>
              </div>
              <div class="text-xs font-mono italic text-cyan-300">
                Latin (TA2): <span id="term-latin"></span>
              </div>
              <div id="term-system" class="text-[11px] text-slate-400"></div>
            </div>

            <!-- Four Biometric Information Cards -->
            <div>
              <h3 class="text-[11px] font-mono uppercase tracking-wider text-cyan-400 mb-1.5" data-i18n="sec_biometrics">REFERENCE BIOMETRICS</h3>
              <div id="biometric-cards" class="grid grid-cols-2 gap-2">
                <!-- 4 Cards Populated Dynamically -->
              </div>
            </div>

            <!-- Active Hotspot Inspector -->
            <div class="space-y-1.5">
              <div class="flex items-center justify-between">
                <h3 class="text-[11px] font-mono uppercase tracking-wider text-cyan-400" data-i18n="sec_hotspots">HOTSPOTS (1–5)</h3>
                <span class="text-[10px] font-mono text-slate-400" data-i18n="tap_pin">Tap pin to inspect</span>
              </div>
              <div id="hotspot-pills" class="flex flex-wrap gap-1.5">
                <!-- Hotspot quick buttons -->
              </div>
              <div id="active-hotspot-card" class="holo-card rounded-xl p-3 border-cyan-400/40 bg-sky-950/30">
                <p class="text-xs text-slate-400" data-i18n="hotspot_placeholder">Click any numbered pin (1–5) on the 3D model or above to inspect its anatomical structure, location, and function.</p>
              </div>
            </div>

            <!-- Five Key Anatomical Learning Points -->
            <div class="space-y-1.5">
              <h3 class="text-[11px] font-mono uppercase tracking-wider text-cyan-400" data-i18n="sec_learning_points">KEY ANATOMICAL LEARNING POINTS</h3>
              <ol id="learning-points-list" class="space-y-1.5 text-xs leading-relaxed">
                <!-- 5 Points Populated Dynamically -->
              </ol>
            </div>
          </div>

          <!-- TAB B: CLINICAL -->
          <div id="tab-content-clinical" class="hidden space-y-3">
            <div class="rounded-xl p-2.5 bg-amber-500/10 border border-amber-400/40 text-[11px] text-amber-200 leading-relaxed">
              <strong data-i18n="clinical_disclaimer_title">Educational Notice:</strong>
              <span data-i18n="clinical_disclaimer">This clinical overview is strictly for medical education and does not provide medical diagnosis or individual treatment advice.</span>
            </div>

            <div class="holo-card rounded-xl p-3 space-y-1">
              <h4 class="text-[11px] font-mono uppercase tracking-wider text-cyan-400" data-i18n="clin_diseases">COMMON CONDITIONS & CLINICAL CONTEXT</h4>
              <p id="clin-diseases" class="text-xs leading-relaxed"></p>
            </div>

            <div class="holo-card rounded-xl p-3 space-y-1">
              <h4 class="text-[11px] font-mono uppercase tracking-wider text-amber-400" data-i18n="clin_causes">CAUSES & RISK FACTORS</h4>
              <p id="clin-causes" class="text-xs leading-relaxed"></p>
            </div>

            <div class="holo-card rounded-xl p-3 space-y-1">
              <h4 class="text-[11px] font-mono uppercase tracking-wider text-rose-400" data-i18n="clin_symptoms">TYPICAL SYMPTOMS</h4>
              <p id="clin-symptoms" class="text-xs leading-relaxed"></p>
            </div>

            <div class="holo-card rounded-xl p-3 space-y-1">
              <h4 class="text-[11px] font-mono uppercase tracking-wider text-sky-400" data-i18n="clin_effects">EFFECTS ON THE BODY</h4>
              <p id="clin-effects" class="text-xs leading-relaxed"></p>
            </div>

            <div class="holo-card rounded-xl p-3 space-y-1 border-emerald-500/30">
              <h4 class="text-[11px] font-mono uppercase tracking-wider text-emerald-400" data-i18n="clin_prevention">PREVENTION & HEALTH EDUCATION</h4>
              <p id="clin-prevention" class="text-xs leading-relaxed"></p>
            </div>
          </div>

          <!-- TAB C: 3D QUIZ -->
          <div id="tab-content-quiz" class="hidden space-y-3">
            <!-- Visual Quiz Progress Bar -->
            <div class="holo-card rounded-xl p-3 space-y-2">
              <div class="flex items-center justify-between text-xs">
                <span class="font-mono text-cyan-300" data-i18n="quiz_progress">QUIZ PROGRESS</span>
                <span id="quiz-progress-pct" class="font-mono font-bold text-emerald-400">0%</span>
              </div>
              <div class="w-full h-2.5 rounded-full bg-slate-950 overflow-hidden border border-cyan-500/25">
                <div id="quiz-progress-bar" class="h-full bg-gradient-to-r from-sky-500 via-cyan-400 to-emerald-400 transition-all duration-300" style="width: 0%"></div>
              </div>
              <div class="grid grid-cols-2 gap-2 pt-1">
                <div class="rounded-lg bg-slate-950/60 p-2 border border-cyan-500/20">
                  <div class="text-[10px] font-mono text-slate-400">SCORE</div>
                  <div id="quiz-score-val" class="font-display font-bold text-base text-emerald-400">0 / 5</div>
                </div>
                <div class="rounded-lg bg-slate-950/60 p-2 border border-cyan-500/20">
                  <div class="text-[10px] font-mono text-slate-400">ATTEMPTS</div>
                  <div id="quiz-attempts-val" class="font-display font-bold text-base text-cyan-300">0</div>
                </div>
              </div>
            </div>

            <!-- Active Question Card -->
            <div id="quiz-question-box" class="holo-card rounded-xl p-3.5 border-cyan-400/50 space-y-2.5">
              <div class="flex items-center justify-between">
                <span class="text-[10px] font-mono uppercase tracking-wider text-cyan-400" data-i18n="quiz_target">TARGET IDENTIFICATION</span>
                <button id="btn-quiz-audio" class="text-xs text-cyan-300 hover:text-white flex items-center gap-1" title="Read Question Aloud">
                  <i data-lucide="volume-2" class="w-3.5 h-3.5"></i>
                </button>
              </div>
              <p id="quiz-question-text" class="text-sm font-semibold text-white leading-snug">
                Click the pin identifying the Aortic Arch.
              </p>
              <p class="text-[11px] text-slate-400" data-i18n="quiz_instruction">
                Click the matching numbered pin (1–5) directly on the 3D hologram or use the pin selector below:
              </p>
              <div id="quiz-pin-buttons" class="grid grid-cols-5 gap-1.5 pt-1">
                <!-- Pins 1..5 -->
              </div>
            </div>

            <!-- Feedback Message -->
            <div id="quiz-feedback" class="hidden rounded-xl p-3 text-xs font-medium"></div>

            <!-- Final Quiz Summary & Retry -->
            <div id="quiz-complete-box" class="hidden holo-card rounded-xl p-3.5 border-emerald-400/50 bg-emerald-950/25 space-y-2.5">
              <div class="font-display font-bold text-sm text-emerald-300">Session Complete!</div>
              <p id="quiz-summary-text" class="text-xs text-slate-200"></p>
              <div class="flex gap-2">
                <button id="btn-quiz-retry" class="touch-btn flex-1 py-2 px-3 rounded-xl bg-cyan-500/25 border border-cyan-400/50 text-xs font-semibold text-cyan-200 hover:bg-cyan-500/40">
                  Retry Quiz
                </button>
                <button id="btn-quiz-save-report" class="touch-btn py-2 px-3 rounded-xl bg-emerald-500/25 border border-emerald-400/50 text-xs font-semibold text-emerald-200 hover:bg-emerald-500/40">
                  Log Result
                </button>
              </div>
            </div>
          </div>

        </div>
      </aside>
    </div>

    <!-- APPLICATION FOOTER -->
    <footer class="holo-panel z-30 shrink-0 px-3 py-1.5 border-t border-cyan-500/25 flex flex-wrap items-center justify-between gap-2 text-[11px]">
      <!-- Left: Support & Contact Buttons -->
      <div class="flex items-center gap-2 flex-wrap">
        <!-- Button 1: BUY ME A KO-FI -->
        <a href="https://ko-fi.com/syukran/tip" target="_blank" rel="noopener noreferrer" class="inline-flex items-center rounded-lg overflow-hidden border border-amber-300/40 hover:border-amber-300 transition shadow-sm bg-[#F5EFE6] px-1.5 py-0.5" title="Buy Me a Ko-fi">
          <img src="https://raw.githubusercontent.com/vandratop/Yuk/872daa6f963613ba58fc4ff71f886beed94ff15d/support_me_on_kofi_beige.png" alt="Buy Me a Ko-fi" class="h-5 w-auto object-contain" onerror="this.style.display='none'; this.nextElementSibling.style.display='inline-flex';" />
          <span style="display:none;" class="items-center gap-1 px-1.5 py-0.5 text-[10px] font-bold text-slate-900">☕ BUY ME A KO-FI</span>
        </a>

        <!-- Button 2: SUPPORT US -->
        <a href="https://sociabuzz.com/syukrankatsiron/tribe" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-1 px-2.5 py-1 rounded-lg bg-emerald-500/15 hover:bg-emerald-500/25 text-emerald-300 border border-emerald-400/35 font-semibold tracking-wide transition">
          <span>SUPPORT US</span>
        </a>

        <!-- Contact Us -->
        <a href="mailto:hijr.time+anatomi@gmail.com" class="inline-flex items-center gap-1 px-2.5 py-1 rounded-lg holo-card text-cyan-300 hover:text-white font-medium transition">
          <span>📩</span>
          <span data-i18n="contact_us">CONTACT US</span>
        </a>
      </div>

      <!-- Right: References Modal Trigger & Credit -->
      <div class="flex items-center gap-3 text-[var(--text-secondary)]">
        <button id="btn-open-refs" class="underline decoration-cyan-500/50 hover:text-cyan-300 transition cursor-pointer" data-i18n="refs_link">
          References &amp; Known Limitations
        </button>
        <span>•</span>
        <span class="font-mono text-slate-400">by Te-eR Inovative @2026</span>
      </div>
    </footer>

  </div>

  <!-- MODAL 1: REFERENCES, SETUP & KNOWN LIMITATIONS -->
  <div id="modal-refs" class="hidden fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-md flex items-center justify-center p-4">
    <div class="holo-panel rounded-2xl max-w-2xl w-full max-h-[85vh] flex flex-col border-cyan-400/40 shadow-2xl">
      <div class="p-4 border-b border-cyan-500/20 flex items-center justify-between">
        <h3 class="font-display font-bold text-base text-cyan-300">Anatomical References, Setup &amp; Known Limitations</h3>
        <button id="btn-close-refs" class="p-1.5 rounded-lg holo-card text-slate-300 hover:text-white" aria-label="Close References">
          <i data-lucide="x" class="w-4 h-4"></i>
        </button>
      </div>
      <div class="p-4 custom-scroll space-y-4 text-xs leading-relaxed text-slate-200">
        <div>
          <h4 class="font-mono font-semibold text-cyan-400 mb-1">1. Primary Anatomical &amp; Educational References</h4>
          <ul class="list-disc pl-5 space-y-1 text-slate-300">
            <li><strong>Terminologia Anatomica (TA2)</strong> — Federative International Programme for Anatomical Terminology (FIPAT), International Federation of Associations of Anatomists.</li>
            <li><strong>OpenStax Anatomy and Physiology 2e</strong> — Rice University (CC BY 4.0) for organ physiology, biometric ranges, and system classifications.</li>
            <li><strong>Gray's Anatomy for Students</strong> &amp; <strong>Netter's Atlas of Human Anatomy</strong> — Standard regional relationships and structural terminology.</li>
            <li><strong>WHO / CDC / Kemenkes RI Educational Materials</strong> — General preventive health and disease overview context.</li>
          </ul>
        </div>

        <div>
          <h4 class="font-mono font-semibold text-amber-400 mb-1">2. Hybrid Procedural + Validated GLB Architecture</h4>
          <p class="text-slate-300">
            Built-in 3D procedural meshes and hotspot anchor coordinates are <strong>illustrative educational approximations</strong>. For medical-grade realism, combine procedural fallbacks with validated, properly licensed GLB/GLTF models (e.g., BodyParts3D CC-BY-SA, NIH 3D Exchange CC0) via the <strong>Load Validated GLB/GLTF</strong> tool.
          </p>
        </div>

        <div>
          <h4 class="font-mono font-semibold text-emerald-400 mb-1">3. Platform &amp; Technical Implementation Matrix</h4>
          <div class="overflow-x-auto rounded-xl border border-cyan-500/25">
            <table class="w-full text-left border-collapse text-[11px]">
              <thead class="bg-slate-900/90 text-cyan-300 font-mono">
                <tr>
                  <th class="p-2 border-b border-cyan-500/20">Feature / Platform</th>
                  <th class="p-2 border-b border-cyan-500/20">Implementation Note</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-cyan-500/15 text-slate-300">
                <tr><td class="p-2 font-semibold">Single HTML</td><td class="p-2">All UI, 32-organ dataset, 3D procedural builders, quiz, and WebXR logic reside in <code>index.html</code>.</td></tr>
                <tr><td class="p-2 font-semibold">Offline PWA</td><td class="p-2">Requires a separate Service Worker (<code>sw.js</code>) and Web App Manifest over HTTPS/HTTP.</td></tr>
                <tr><td class="p-2 font-semibold">Google Translate</td><td class="p-2">Optional online widget paired with built-in offline EN/ID dictionary fallback.</td></tr>
                <tr><td class="p-2 font-semibold">Android / iOS TTS</td><td class="p-2">Uses browser Web Speech API; native Android TTS or iOS AVSpeechSynthesizer requires a native wrapper.</td></tr>
                <tr><td class="p-2 font-semibold">Samsung / Huawei</td><td class="p-2">Verify compatibility separately on Samsung Internet / Tizen and Huawei Browser / HarmonyOS.</td></tr>
                <tr><td class="p-2 font-semibold">Smart TV</td><td class="p-2">Includes Smart TV Remote Mode (D-pad arrows, Enter, WASD orbit, +/- zoom) and large focus indicators.</td></tr>
                <tr><td class="p-2 font-semibold">VR / AR</td><td class="p-2">Uses standard WebXR (<code>immersive-vr</code> / <code>immersive-ar</code>) on compatible headsets and browsers.</td></tr>
              </tbody>
            </table>
          </div>
        </div>

        <div>
          <h4 class="font-mono font-semibold text-sky-400 mb-1">4. Local Execution Instructions</h4>
          <p class="text-slate-300">
            Serve <code>index.html</code> over a local HTTP server (e.g. <code>python3 -m http.server 8080</code> or VS Code Live Server) and open <code>http://localhost:8080</code>. Browser features like WebXR, ES module workers, and external GLB loading require HTTP/HTTPS rather than <code>file://</code> URLs.
          </p>
        </div>
      </div>
    </div>
  </div>

  <!-- MODAL 2: LOAD VALIDATED GLB / GLTF MODEL -->
  <div id="modal-glb" class="hidden fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-md flex items-center justify-center p-4">
    <div class="holo-panel rounded-2xl max-w-lg w-full p-4 border-cyan-400/40 shadow-2xl space-y-3">
      <div class="flex items-center justify-between border-b border-cyan-500/20 pb-2">
        <h3 class="font-display font-bold text-sm text-cyan-300">Load Validated Medical GLB / GLTF Model</h3>
        <button id="btn-close-glb" class="p-1.5 rounded-lg holo-card text-slate-300 hover:text-white" aria-label="Close GLB Modal">
          <i data-lucide="x" class="w-4 h-4"></i>
        </button>
      </div>
      <p class="text-xs text-slate-300 leading-relaxed">
        Replace the active procedural specimen with an externally hosted or local validated GLB/GLTF anatomical mesh. Supports embedded hotspot metadata (<code>userData.hotspotIndex</code>) or named mesh nodes.
      </p>
      <div class="space-y-2">
        <label class="block text-[11px] font-mono text-cyan-300">GLB / GLTF Asset URL (HTTPS or Local HTTP)</label>
        <input id="input-glb-url" type="url" placeholder="https://example.org/models/validated_heart.glb" class="w-full px-3 py-2 rounded-xl bg-slate-950/80 border border-cyan-500/30 text-xs text-white focus:outline-none focus:border-cyan-400" />
      </div>
      <div class="space-y-2">
        <label class="block text-[11px] font-mono text-cyan-300">Or Select Local .glb / .gltf File</label>
        <input id="input-glb-file" type="file" accept=".glb,.gltf" class="w-full text-xs text-slate-300 file:mr-3 file:py-1.5 file:px-3 file:rounded-lg file:border-0 file:text-xs file:font-semibold file:bg-cyan-500/25 file:text-cyan-200 hover:file:bg-cyan-500/40" />
      </div>
      <div id="glb-load-status" class="text-xs font-mono text-slate-400">Ready.</div>
      <div class="flex justify-end gap-2 pt-2">
        <button id="btn-restore-procedural" class="touch-btn px-3 py-1.5 rounded-xl holo-card text-xs text-amber-300 hover:text-white">Restore Procedural</button>
        <button id="btn-submit-glb" class="touch-btn px-4 py-1.5 rounded-xl bg-sky-500/30 border border-cyan-400/60 text-xs font-semibold text-white hover:bg-sky-500/50">Load 3D Model</button>
      </div>
    </div>
  </div>

  <!-- MODAL 3: TEACHER & STUDENT MODE DASHBOARD -->
  <div id="modal-teacher" class="hidden fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-md flex items-center justify-center p-4">
    <div class="holo-panel rounded-2xl max-w-2xl w-full max-h-[85vh] flex flex-col border-emerald-400/40 shadow-2xl">
      <div class="p-4 border-b border-cyan-500/20 flex items-center justify-between">
        <div class="flex items-center gap-2">
          <i data-lucide="graduation-cap" class="w-5 h-5 text-emerald-400"></i>
          <h3 class="font-display font-bold text-base text-emerald-300">Teacher &amp; Student Learning Lab</h3>
        </div>
        <button id="btn-close-teacher" class="p-1.5 rounded-lg holo-card text-slate-300 hover:text-white" aria-label="Close Learning Lab">
          <i data-lucide="x" class="w-4 h-4"></i>
        </button>
      </div>
      <div class="p-4 custom-scroll space-y-4 text-xs">
        <!-- Student Profile & Role Switch -->
        <div class="holo-card rounded-xl p-3 flex flex-wrap items-center justify-between gap-3">
          <div class="flex items-center gap-2">
            <span class="font-mono text-cyan-300">LEARNER NAME:</span>
            <input id="input-student-name" type="text" value="Student 01" class="px-2.5 py-1 rounded-lg bg-slate-950 border border-cyan-500/30 text-xs text-white" />
          </div>
          <div class="flex items-center gap-2">
            <span class="font-mono text-emerald-300">ACTIVE ROLE:</span>
            <select id="select-modal-role" class="px-2.5 py-1 rounded-lg bg-slate-950 border border-emerald-500/30 text-xs text-emerald-300">
              <option value="student">Student Mode</option>
              <option value="teacher">Teacher Mode (Question Bank &amp; Reports)</option>
            </select>
          </div>
        </div>

        <!-- Teacher Custom Question Builder -->
        <div id="teacher-builder-panel" class="holo-card rounded-xl p-3 space-y-2 border-emerald-500/30">
          <h4 class="font-mono font-semibold text-emerald-400">TEACHER QUESTION BANK (ACTIVE ORGAN: <span id="tb-organ-name">Heart</span>)</h4>
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-2">
            <select id="tb-hotspot-select" class="rounded-lg bg-slate-950 border border-cyan-500/30 px-2 py-1.5 text-xs text-white"></select>
            <input id="tb-prompt-input" type="text" placeholder="Custom prompt (e.g., Identify the Left Ventricle)..." class="sm:col-span-2 rounded-lg bg-slate-950 border border-cyan-500/30 px-2.5 py-1.5 text-xs text-white" />
          </div>
          <button id="btn-add-custom-q" class="px-3 py-1.5 rounded-lg bg-emerald-500/25 border border-emerald-400/50 text-emerald-200 font-semibold hover:bg-emerald-500/40">
            + Add Question to Active Session
          </button>
        </div>

        <!-- Learning Progress & Quiz Results Report -->
        <div class="holo-card rounded-xl p-3 space-y-2">
          <div class="flex items-center justify-between">
            <h4 class="font-mono font-semibold text-cyan-300">QUIZ RESULTS &amp; LEARNING REPORT</h4>
            <button id="btn-export-report" class="px-2.5 py-1 rounded-lg holo-card text-[11px] font-mono text-cyan-300 hover:text-white">Copy CSV Report</button>
          </div>
          <div id="report-table-wrap" class="overflow-x-auto">
            <table class="w-full text-left text-[11px]">
              <thead class="text-slate-400 border-b border-cyan-500/20 font-mono">
                <tr>
                  <th class="py-1.5">Student</th>
                  <th class="py-1.5">Organ</th>
                  <th class="py-1.5">Score</th>
                  <th class="py-1.5">Attempts</th>
                  <th class="py-1.5">Time</th>
                </tr>
              </thead>
              <tbody id="report-tbody" class="divide-y divide-cyan-500/10 text-slate-200">
                <tr><td colspan="5" class="py-3 text-center text-slate-400">No quiz sessions logged yet. Complete a 3D Quiz to record results.</td></tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- NON-BLOCKING TOAST NOTIFICATION -->
  <div id="toast-banner" class="hidden fixed bottom-20 left-1/2 -translate-x-1/2 z-50 holo-panel rounded-xl px-4 py-2 text-xs font-medium text-cyan-200 border-cyan-400/60 shadow-2xl"></div>

  <!-- COMPLETE APPLICATION SCRIPT -->
  <script>
    (() => {
      'use strict';

      /* =========================================================================
       * 1. MULTILINGUAL I18N DICTIONARY (ALL 13 SUPPORTED LANGUAGES)
       * ========================================================================= */
      const translations = {
        en: {
          badge_museum: '3D MEDICAL MUSEUM',
          settings_btn: 'Setting',
          settings_title: 'DISPLAY SETTINGS',
          opt_view_layer: '3D Layer Mode (Organ / Full Body / Split)',
          opt_language: 'Language Selection',
          opt_theme: 'Screen Theme (Dark / Light / Auto)',
          opt_screen_mode: 'Screen Layout Mode',
          opt_fullscreen: 'Fullscreen Mode',
          catalog_short: 'Catalog',
          view_organ: 'Organ',
          view_fullbody: 'Full Body',
          view_split: 'Split',
          active_specimen: 'ACTIVE SPECIMEN',
          catalog_title: 'ANATOMICAL CATALOG',
          load_glb: 'Load Validated GLB/GLTF',
          phys_sim: 'PHYSIOLOGY SIM',
          phys_auto: 'Auto (Organ)',
          phys_blood: 'Blood Flow',
          phys_resp: 'Respiration',
          phys_dig: 'Digestion',
          phys_nerv: 'Nervous Signal',
          phys_off: 'Off',
          phys_arterial: 'Arterial (O₂)',
          phys_venous: 'Venous (CO₂)',
          clipping: 'Section:',
          explode: 'Explode:',
          btn_section: 'Section / Explode',
          btn_holoscan: 'Holo Scan',
          btn_xray: 'X-Ray',
          btn_wireframe: 'Wireframe',
          btn_hotspots: 'Hotspots',
          btn_rotate: 'Rotate',
          btn_physiology: 'Living Pulse',
          btn_snapshot: 'PNG Note',
          btn_reset: 'Reset',
          tab_structure: 'Structure',
          tab_clinical: 'Clinical',
          tab_quiz: '3D Quiz',
          tts_title: 'AUDIO NARRATION',
          tts_read: 'Read',
          sec_overview: 'ANATOMICAL OVERVIEW',
          sec_function: 'MAIN PHYSIOLOGICAL FUNCTION',
          sec_terminology: 'ANATOMICAL TERMINOLOGY',
          sec_biometrics: 'REFERENCE BIOMETRICS',
          sec_hotspots: 'HOTSPOTS (1–5)',
          tap_pin: 'Tap pin to inspect',
          hotspot_placeholder: 'Click any numbered pin (1–5) on the 3D model or above to inspect its anatomical structure, location, and function.',
          sec_learning_points: 'KEY ANATOMICAL LEARNING POINTS',
          clinical_disclaimer_title: 'Educational Notice:',
          clinical_disclaimer: 'This clinical overview is strictly for medical education and does not provide medical diagnosis or individual treatment advice.',
          clin_diseases: 'COMMON CONDITIONS & CLINICAL CONTEXT',
          clin_causes: 'CAUSES & RISK FACTORS',
          clin_symptoms: 'TYPICAL SYMPTOMS',
          clin_effects: 'EFFECTS ON THE BODY',
          clin_prevention: 'PREVENTION & HEALTH EDUCATION',
          quiz_progress: 'QUIZ PROGRESS',
          quiz_target: 'TARGET IDENTIFICATION',
          quiz_instruction: 'Click the matching numbered pin (1–5) directly on the 3D hologram or use the pin selector below:',
          quiz_prompt_tpl: 'Click the pin identifying the {name} ({latin}).',
          contact_us: 'CONTACT US',
          refs_link: 'References & Known Limitations',
          cat_all: 'All Organs',
          cat_nervous: 'Nervous & Senses',
          cat_thorax: 'Thorax',
          cat_cardio: 'Cardiovascular',
          cat_resp: 'Respiratory',
          cat_digestive: 'Digestive',
          cat_urinary: 'Urinary',
          cat_repro: 'Reproductive',
          cat_musculo: 'Musculoskeletal',
          cat_integ: 'Integumentary',
        },
        id: {
          badge_museum: 'MUSEUM MEDIS 3D',
          settings_btn: 'Pengaturan',
          settings_title: 'PENGATURAN TAMPILAN',
          opt_view_layer: 'Mode Layer 3D (Organ / Tubuh Utuh / Split)',
          opt_language: 'Pilihan Bahasa',
          opt_theme: 'Layar (Gelap / Cerah / Otomatis)',
          opt_screen_mode: 'Mode Pilihan Layar',
          opt_fullscreen: 'Perbesar Layar',
          catalog_short: 'Katalog',
          view_organ: 'Organ',
          view_fullbody: 'Tubuh Utuh',
          view_split: 'Bandingkan',
          active_specimen: 'SPESIMEN AKTIF',
          catalog_title: 'KATALOG ANATOMI',
          load_glb: 'Muat GLB/GLTF Tervalidasi',
          phys_sim: 'SIMULASI FISIOLOGI',
          phys_auto: 'Otomatis (Organ)',
          phys_blood: 'Aliran Darah',
          phys_resp: 'Pernapasan',
          phys_dig: 'Pencernaan',
          phys_nerv: 'Sinyal Saraf',
          phys_off: 'Nonaktif',
          phys_arterial: 'Arteri (O₂)',
          phys_venous: 'Vena (CO₂)',
          clipping: 'Potongan:',
          explode: 'Urai:',
          btn_section: 'Potongan / Urai',
          btn_holoscan: 'Pindai Holo',
          btn_xray: 'X-Ray',
          btn_wireframe: 'Rangka Mesh',
          btn_hotspots: 'Titik Pin',
          btn_rotate: 'Putar',
          btn_physiology: 'Detak Hidup',
          btn_snapshot: 'Simpan PNG',
          btn_reset: 'Reset',
          tab_structure: 'Struktur',
          tab_clinical: 'Klinis',
          tab_quiz: 'Kuis 3D',
          tts_title: 'NARASI AUDIO',
          tts_read: 'Baca',
          sec_overview: 'GAMBARAN ANATOMI',
          sec_function: 'FUNGSI FISIOLOGIS UTAMA',
          sec_terminology: 'TERMINOLOGI ANATOMI',
          sec_biometrics: 'BIOMETRIK REFERENSI',
          sec_hotspots: 'TITIK HOTSPOT (1–5)',
          tap_pin: 'Ketuk pin untuk memeriksa',
          hotspot_placeholder: 'Klik pin bernomor (1–5) pada model 3D atau di atas untuk memeriksa struktur anatomi, lokasi, dan fungsinya.',
          sec_learning_points: 'POIN PEMBELAJARAN ANATOMI UTAMA',
          clinical_disclaimer_title: 'Pemberitahuan Edukasi:',
          clinical_disclaimer: 'Ringkasan klinis ini khusus untuk pendidikan medis dan tidak memberikan diagnosis medis atau saran pengobatan individu.',
          clin_diseases: 'KONDISI UMUM & KONTEKS KLINIS',
          clin_causes: 'PENYEBAB & FAKTOR RISIKO',
          clin_symptoms: 'GEJALA KHAS',
          clin_effects: 'DAMPAK PADA TUBUH',
          clin_prevention: 'PENCEGAHAN & EDUKASI KESEHATAN',
          quiz_progress: 'PROGRES KUIS',
          quiz_target: 'IDENTIFIKASI TARGET',
          quiz_instruction: 'Klik pin bernomor yang sesuai (1–5) langsung pada hologram 3D atau gunakan pemilih pin di bawah:',
          quiz_prompt_tpl: 'Klik pin yang menunjukkan {name} ({latin}).',
          contact_us: 'HUBUNGI KAMI',
          refs_link: 'Referensi & Batasan Teknis',
          cat_all: 'Semua Organ',
          cat_nervous: 'Saraf & Indra',
          cat_thorax: 'Toraks',
          cat_cardio: 'Kardiovaskular',
          cat_resp: 'Pernapasan',
          cat_digestive: 'Pencernaan',
          cat_urinary: 'Urinaria',
          cat_repro: 'Reproduksi',
          cat_musculo: 'Muskuloskeletal',
          cat_integ: 'Integumen',
        },
        de: {
          badge_museum: '3D-MEDIZINMUSEUM',
          settings_btn: 'Einstellungen',
          settings_title: 'ANZEIGEEINSTELLUNGEN',
          opt_view_layer: '3D-Ebenenmodus (Organ / Ganzkörper / Split)',
          opt_language: 'Sprachauswahl',
          opt_theme: 'Bildschirmthema (Dunkel / Hell / Auto)',
          opt_screen_mode: 'Bildschirm-Layoutmodus',
          opt_fullscreen: 'Vollbildmodus',
          catalog_short: 'Katalog',
          view_organ: 'Organ',
          view_fullbody: 'Ganzkörper',
          view_split: 'Vergleich',
          active_specimen: 'AKTIVES PRÄPARAT',
          catalog_title: 'ANATOMISCHER KATALOG',
          load_glb: 'Validiertes GLB/GLTF laden',
          phys_sim: 'PHYSIOLOGIE-SIM',
          phys_auto: 'Auto (Organ)',
          phys_blood: 'Blutfluss',
          phys_resp: 'Atmung',
          phys_dig: 'Verdauung',
          phys_nerv: 'Nervensignal',
          phys_off: 'Aus',
          phys_arterial: 'Arteriell (O₂)',
          phys_venous: 'Venös (CO₂)',
          clipping: 'Schnitt:',
          explode: 'Zerlegen:',
          btn_section: 'Schnitt / Zerlegen',
          btn_holoscan: 'Holo-Scan',
          btn_xray: 'Röntgen',
          btn_wireframe: 'Drahtgitter',
          btn_hotspots: 'Hotspots',
          btn_rotate: 'Drehen',
          btn_physiology: 'Lebendpuls',
          btn_snapshot: 'PNG-Notiz',
          btn_reset: 'Zurücksetzen',
          tab_structure: 'Struktur',
          tab_clinical: 'Klinisch',
          tab_quiz: '3D-Quiz',
          tts_title: 'AUDIO-ERZÄHLUNG',
          tts_read: 'Vorlesen',
          sec_overview: 'ANATOMISCHER ÜBERBLICK',
          sec_function: 'HAUPTPHYSIOLOGISCHE FUNKTION',
          sec_terminology: 'ANATOMISCHE TERMINOLOGIE',
          sec_biometrics: 'REFERENZ-BIOMETRIE',
          sec_hotspots: 'HOTSPOTS (1–5)',
          tap_pin: 'Pin antippen zum Prüfen',
          hotspot_placeholder: 'Klicken Sie auf einen nummerierten Pin (1–5) am 3D-Modell, um Struktur, Lage und Funktion zu untersuchen.',
          sec_learning_points: 'WICHTIGE ANATOMISCHE LERNPUNKTE',
          clinical_disclaimer_title: 'Bildungshinweis:',
          clinical_disclaimer: 'Diese klinische Übersicht dient ausschließlich der medizinischen Ausbildung und ersetzt keine ärztliche Diagnose.',
          clin_diseases: 'HÄUFIGE ERKRANKUNGEN & KLINISCHER KONTEXT',
          clin_causes: 'URSACHEN & RISIKOFAKTOREN',
          clin_symptoms: 'TYPISCHE SYMPTOME',
          clin_effects: 'AUSWIRKUNGEN AUF DEN KÖRPER',
          clin_prevention: 'PRÄVENTION & GESUNDHEITSBILDUNG',
          quiz_progress: 'QUIZ-FORTSCHRITT',
          quiz_target: 'ZIELIDENTIFIKATION',
          quiz_instruction: 'Klicken Sie auf den passenden Pin (1–5) direkt auf dem 3D-Hologramm oder wählen Sie unten:',
          quiz_prompt_tpl: 'Klicken Sie auf den Pin für {name} ({latin}).',
          contact_us: 'KONTAKT',
          refs_link: 'Referenzen & Einschränkungen',
          cat_all: 'Alle Organe',
          cat_nervous: 'Nerven & Sinne',
          cat_thorax: 'Thorax',
          cat_cardio: 'Herz-Kreislauf',
          cat_resp: 'Atmung',
          cat_digestive: 'Verdauung',
          cat_urinary: 'Harnwege',
          cat_repro: 'Fortpflanzung',
          cat_musculo: 'Bewegungsapparat',
          cat_integ: 'Hautsystem',
        },
        fr: {
          badge_museum: 'MUSÉE MÉDICAL 3D',
          settings_btn: 'Paramètres',
          settings_title: 'PARAMÈTRES D’AFFICHAGE',
          opt_view_layer: 'Mode Calque 3D (Organe / Corps / Divisé)',
          opt_language: 'Choix de la langue',
          opt_theme: 'Thème d’écran (Sombre / Clair / Auto)',
          opt_screen_mode: 'Mode d’affichage écran',
          opt_fullscreen: 'Plein écran',
          catalog_short: 'Catalogue',
          view_organ: 'Organe',
          view_fullbody: 'Corps entier',
          view_split: 'Comparer',
          active_specimen: 'SPÉCIMEN ACTIF',
          catalog_title: 'CATALOGUE ANATOMIQUE',
          load_glb: 'Charger GLB/GLTF validé',
          phys_sim: 'SIM PHYSIOLOGIE',
          phys_auto: 'Auto (Organe)',
          phys_blood: 'Flux sanguin',
          phys_resp: 'Respiration',
          phys_dig: 'Digestion',
          phys_nerv: 'Signal nerveux',
          phys_off: 'Désactivé',
          phys_arterial: 'Artériel (O₂)',
          phys_venous: 'Veineux (CO₂)',
          clipping: 'Coupe :',
          explode: 'Éclater :',
          btn_section: 'Coupe / Éclater',
          btn_holoscan: 'Scan Holo',
          btn_xray: 'Rayons X',
          btn_wireframe: 'Filaire',
          btn_hotspots: 'Points clés',
          btn_rotate: 'Rotation',
          btn_physiology: 'Pouls vivant',
          btn_snapshot: 'Note PNG',
          btn_reset: 'Réinitialiser',
          tab_structure: 'Structure',
          tab_clinical: 'Clinique',
          tab_quiz: 'Quiz 3D',
          tts_title: 'NARRATION AUDIO',
          tts_read: 'Lire',
          sec_overview: 'APERÇU ANATOMIQUE',
          sec_function: 'FONCTION PHYSIOLOGIQUE PRINCIPALE',
          sec_terminology: 'TERMINOLOGIE ANATOMIQUE',
          sec_biometrics: 'BIOMÉTRIE DE RÉFÉRENCE',
          sec_hotspots: 'POINTS REPÈRES (1–5)',
          tap_pin: 'Touchez un repère pour inspecter',
          hotspot_placeholder: 'Cliquez sur un repère numéroté (1–5) sur le modèle 3D pour inspecter sa structure et sa fonction.',
          sec_learning_points: 'POINTS CLÉS D’APPRENTISSAGE',
          clinical_disclaimer_title: 'Avis éducatif :',
          clinical_disclaimer: 'Cet aperçu clinique est strictement destiné à l’enseignement médical et ne constitue pas un diagnostic.',
          clin_diseases: 'AFFECTIONS COURANTES & CONTEXTE CLINIQUE',
          clin_causes: 'CAUSES & FACTEURS DE RISQUE',
          clin_symptoms: 'SYMPTÔMES TYPIQUES',
          clin_effects: 'EFFETS SUR L’ORGANISME',
          clin_prevention: 'PRÉVENTION & ÉDUCATION SANTÉ',
          quiz_progress: 'PROGRESSION DU QUIZ',
          quiz_target: 'IDENTIFICATION DE CIBLE',
          quiz_instruction: 'Cliquez sur le repère numéroté (1–5) correspondant sur l’hologramme 3D ou ci-dessous :',
          quiz_prompt_tpl: 'Cliquez sur le repère identifiant : {name} ({latin}).',
          contact_us: 'NOUS CONTACTER',
          refs_link: 'Références & Limites connues',
          cat_all: 'Tous les organes',
          cat_nervous: 'Nerfs & Sens',
          cat_thorax: 'Thorax',
          cat_cardio: 'Cardiovasculaire',
          cat_resp: 'Respiratoire',
          cat_digestive: 'Digestif',
          cat_urinary: 'Urinaire',
          cat_repro: 'Reproducteur',
          cat_musculo: 'Musculosquelettique',
          cat_integ: 'Tégumentaire',
        },
        es: {
          badge_museum: 'MUSEO MÉDICO 3D',
          settings_btn: 'Ajustes',
          settings_title: 'CONFIGURACIÓN DE PANTALLA',
          opt_view_layer: 'Modo Capa 3D (Órgano / Cuerpo / Dividido)',
          opt_language: 'Selección de idioma',
          opt_theme: 'Tema de pantalla (Oscuro / Claro / Auto)',
          opt_screen_mode: 'Modo de diseño de pantalla',
          opt_fullscreen: 'Pantalla completa',
          catalog_short: 'Catálogo',
          view_organ: 'Órgano',
          view_fullbody: 'Cuerpo entero',
          view_split: 'Dividir',
          active_specimen: 'ESPECIMEN ACTIVO',
          catalog_title: 'CATÁLOGO ANATÓMICO',
          load_glb: 'Cargar GLB/GLTF validado',
          phys_sim: 'SIM FISIOLOGÍA',
          phys_auto: 'Auto (Órgano)',
          phys_blood: 'Flujo sanguíneo',
          phys_resp: 'Respiración',
          phys_dig: 'Digestión',
          phys_nerv: 'Señal nerviosa',
          phys_off: 'Apagado',
          phys_arterial: 'Arterial (O₂)',
          phys_venous: 'Venoso (CO₂)',
          clipping: 'Corte:',
          explode: 'Explotar:',
          btn_section: 'Corte / Explotar',
          btn_holoscan: 'Escaneo Holo',
          btn_xray: 'Rayos X',
          btn_wireframe: 'Malla',
          btn_hotspots: 'Puntos',
          btn_rotate: 'Rotar',
          btn_physiology: 'Pulso vivo',
          btn_snapshot: 'Nota PNG',
          btn_reset: 'Reiniciar',
          tab_structure: 'Estructura',
          tab_clinical: 'Clínica',
          tab_quiz: 'Quiz 3D',
          tts_title: 'NARRACIÓN DE AUDIO',
          tts_read: 'Leer',
          sec_overview: 'RESUMEN ANATÓMICO',
          sec_function: 'FUNCIÓN FISIOLÓGICA PRINCIPAL',
          sec_terminology: 'TERMINOLOGÍA ANATÓMICA',
          sec_biometrics: 'BIOMETRÍA DE REFERENCIA',
          sec_hotspots: 'PUNTOS CLAVE (1–5)',
          tap_pin: 'Toque un pin para inspeccionar',
          hotspot_placeholder: 'Haga clic en cualquier pin numerado (1–5) en el modelo 3D para inspeccionar su estructura y función.',
          sec_learning_points: 'PUNTOS CLAVE DE APRENDIZAJE',
          clinical_disclaimer_title: 'Aviso educativo:',
          clinical_disclaimer: 'Este resumen clínico es estrictamente educativo y no proporciona diagnóstico ni tratamiento médico.',
          clin_diseases: 'AFECCIONES COMUNES Y CONTEXTO CLÍNICO',
          clin_causes: 'CAUSAS Y FACTORES DE RIESGO',
          clin_symptoms: 'SÍNTOMAS TÍPICOS',
          clin_effects: 'EFECTOS EN EL CUERPO',
          clin_prevention: 'PREVENCIÓN Y EDUCACIÓN SANITARIA',
          quiz_progress: 'PROGRESO DEL QUIZ',
          quiz_target: 'IDENTIFICACIÓN DE OBJETIVO',
          quiz_instruction: 'Haga clic en el pin numerado correspondiente (1–5) en el holograma 3D o abajo:',
          quiz_prompt_tpl: 'Haga clic en el pin que identifica: {name} ({latin}).',
          contact_us: 'CONTÁCTANOS',
          refs_link: 'Referencias y limitaciones',
          cat_all: 'Todos los órganos',
          cat_nervous: 'Nervioso y sentidos',
          cat_thorax: 'Tórax',
          cat_cardio: 'Cardiovascular',
          cat_resp: 'Respiratorio',
          cat_digestive: 'Digestivo',
          cat_urinary: 'Urinario',
          cat_repro: 'Reproductor',
          cat_musculo: 'Musculoesquelético',
          cat_integ: 'Tegumentario',
        },
        ru: {
          badge_museum: '3D МЕДИЦИНСКИЙ МУЗЕЙ',
          settings_btn: 'Настройки',
          settings_title: 'НАСТРОЙКИ ЭКРАНА',
          opt_view_layer: 'Режим 3D-слоя (Орган / Тело / Сравнение)',
          opt_language: 'Выбор языка',
          opt_theme: 'Тема экрана (Тёмная / Светлая / Авто)',
          opt_screen_mode: 'Режим макета экрана',
          opt_fullscreen: 'Полный экран',
          catalog_short: 'Каталог',
          view_organ: 'Орган',
          view_fullbody: 'Всё тело',
          view_split: 'Сравнить',
          active_specimen: 'АКТИВНЫЙ ОБРАЗЕЦ',
          catalog_title: 'АНАТОМИЧЕСКИЙ КАТАЛОГ',
          load_glb: 'Загрузить GLB/GLTF',
          phys_sim: 'СИМ. ФИЗИОЛОГИИ',
          phys_auto: 'Авто (Орган)',
          phys_blood: 'Кровоток',
          phys_resp: 'Дыхание',
          phys_dig: 'Пищеварение',
          phys_nerv: 'Нервный импульс',
          phys_off: 'Выкл',
          phys_arterial: 'Артериальная (O₂)',
          phys_venous: 'Венозная (CO₂)',
          clipping: 'Срез:',
          explode: 'Разбор:',
          btn_section: 'Срез / Разбор',
          btn_holoscan: 'Голо-скан',
          btn_xray: 'Рентген',
          btn_wireframe: 'Сетка',
          btn_hotspots: 'Точки',
          btn_rotate: 'Вращение',
          btn_physiology: 'Пульсация',
          btn_snapshot: 'Снимок PNG',
          btn_reset: 'Сброс',
          tab_structure: 'Структура',
          tab_clinical: 'Клиника',
          tab_quiz: '3D-Тест',
          tts_title: 'АУДИООЗВУЧКА',
          tts_read: 'Читать',
          sec_overview: 'АНАТОМИЧЕСКИЙ ОБЗОР',
          sec_function: 'ОСНОВНАЯ ФИЗИОЛОГИЧЕСКАЯ ФУНКЦИЯ',
          sec_terminology: 'АНАТОМИЧЕСКАЯ ТЕРМИНОЛОГИЯ',
          sec_biometrics: 'СПРАВОЧНАЯ БИОМЕТРИЯ',
          sec_hotspots: 'ТОЧКИ ИНТЕРЕСА (1–5)',
          tap_pin: 'Нажмите на метку для осмотра',
          hotspot_placeholder: 'Нажмите на любую пронумерованную метку (1–5) на 3D-модели, чтобы изучить её структуру и функцию.',
          sec_learning_points: 'КЛЮЧЕВЫЕ УЧЕБНЫЕ ПУНКТЫ',
          clinical_disclaimer_title: 'Образовательное примечание:',
          clinical_disclaimer: 'Этот клинический обзор предназначен исключительно для медицинского образования и не является диагнозом.',
          clin_diseases: 'РАСПРОСТРАНЁННЫЕ ЗАБОЛЕВАНИЯ',
          clin_causes: 'ПРИЧИНЫ И ФАКТОРЫ РИСКА',
          clin_symptoms: 'ТИПИЧНЫЕ СИМПТОМЫ',
          clin_effects: 'ВЛИЯНИЕ НА ОРГАНИЗМ',
          clin_prevention: 'ПРОФИЛАКТИКА И ОБРАЗОВАНИЕ',
          quiz_progress: 'ПРОГРЕСС ТЕСТА',
          quiz_target: 'ОПРЕДЕЛЕНИЕ СТРУКТУРЫ',
          quiz_instruction: 'Нажмите соответствующую метку (1–5) на 3D-голограмме или выберите ниже:',
          quiz_prompt_tpl: 'Нажмите на метку, обозначающую: {name} ({latin}).',
          contact_us: 'СВЯЗАТЬСЯ С НАМИ',
          refs_link: 'Источники и ограничения',
          cat_all: 'Все органы',
          cat_nervous: 'Нервная и чувства',
          cat_thorax: 'Грудная клетка',
          cat_cardio: 'Сердечно-сосудистая',
          cat_resp: 'Дыхательная',
          cat_digestive: 'Пищеварительная',
          cat_urinary: 'Мочевыделительная',
          cat_repro: 'Репродуктивная',
          cat_musculo: 'Опорно-двигательная',
          cat_integ: 'Покровная',
        },
        'zh-CN': {
          badge_museum: '3D 医学博物馆',
          settings_btn: '设置',
          settings_title: '显示设置',
          opt_view_layer: '3D 图层模式（器官 / 全身 / 分屏）',
          opt_language: '语言选择',
          opt_theme: '屏幕主题（深色 / 浅色 / 自动）',
          opt_screen_mode: '屏幕布局模式',
          opt_fullscreen: '全屏显示',
          catalog_short: '目录',
          view_organ: '单器官',
          view_fullbody: '全身模型',
          view_split: '分屏对比',
          active_specimen: '当前标本',
          catalog_title: '解剖学目录',
          load_glb: '加载已验证 GLB/GLTF',
          phys_sim: '生理模拟',
          phys_auto: '自动（按器官）',
          phys_blood: '血液流动',
          phys_resp: '呼吸运动',
          phys_dig: '消化蠕动',
          phys_nerv: '神经信号',
          phys_off: '关闭',
          phys_arterial: '动脉血 (O₂)',
          phys_venous: '静脉血 (CO₂)',
          clipping: '剖面：',
          explode: '分解：',
          btn_section: '剖面 / 分解',
          btn_holoscan: '全息扫描',
          btn_xray: 'X光透视',
          btn_wireframe: '网格线框',
          btn_hotspots: '标注点',
          btn_rotate: '自动旋转',
          btn_physiology: '生理律动',
          btn_snapshot: '保存 PNG',
          btn_reset: '重置视角',
          tab_structure: '结构',
          tab_clinical: '临床',
          tab_quiz: '3D 测验',
          tts_title: '语音朗读',
          tts_read: '朗读',
          sec_overview: '解剖学概述',
          sec_function: '主要生理功能',
          sec_terminology: '解剖学术语',
          sec_biometrics: '参考生理指标',
          sec_hotspots: '解剖标注点 (1–5)',
          tap_pin: '点击数字标点查看详情',
          hotspot_placeholder: '点击 3D 模型或上方的任意编号标点 (1–5)，查看其解剖结构、位置与功能。',
          sec_learning_points: '核心解剖学学习要点',
          clinical_disclaimer_title: '医学教育声明：',
          clinical_disclaimer: '本临床概述仅供医学教学参考，不构成任何临床诊断或个人治疗建议。',
          clin_diseases: '常见疾病与临床背景',
          clin_causes: '病因与危险因素',
          clin_symptoms: '典型临床表现',
          clin_effects: '对机体的影响',
          clin_prevention: '预防与健康宣教',
          quiz_progress: '测验进度',
          quiz_target: '目标结构识别',
          quiz_instruction: '请直接在 3D 全息模型上点击对应的编号标点 (1–5)，或使用下方按钮：',
          quiz_prompt_tpl: '请点击标注以下结构的数字标点：{name} ({latin})。',
          contact_us: '联系我们',
          refs_link: '参考文献与技术说明',
          cat_all: '全部器官',
          cat_nervous: '神经与感官',
          cat_thorax: '胸部',
          cat_cardio: '心血管系统',
          cat_resp: '呼吸系统',
          cat_digestive: '消化系统',
          cat_urinary: '泌尿系统',
          cat_repro: '生殖系统',
          cat_musculo: '运动系统',
          cat_integ: '皮肤系统',
        },
        ko: {
          badge_museum: '3D 의학 박물관',
          settings_btn: '설정',
          settings_title: '화면 설정',
          opt_view_layer: '3D 레이어 모드 (장기 / 전신 / 분할)',
          opt_language: '언어 선택',
          opt_theme: '화면 테마 (다크 / 라이트 / 자동)',
          opt_screen_mode: '화면 레이아웃 모드',
          opt_fullscreen: '전체 화면',
          catalog_short: '카탈로그',
          view_organ: '단일 장기',
          view_fullbody: '전신 인체',
          view_split: '분할 비교',
          active_specimen: '활성 표본',
          catalog_title: '해부학 카탈로그',
          load_glb: '검증된 GLB/GLTF 불러오기',
          phys_sim: '생리 시뮬레이션',
          phys_auto: '자동 (장기별)',
          phys_blood: '혈류 흐름',
          phys_resp: '호흡 운동',
          phys_dig: '소화 운동',
          phys_nerv: '신경 신호',
          phys_off: '끄기',
          phys_arterial: '동맥혈 (O₂)',
          phys_venous: '정맥혈 (CO₂)',
          clipping: '단면:',
          explode: '분해:',
          btn_section: '단면 / 분해',
          btn_holoscan: '홀로 스캔',
          btn_xray: '엑스레이',
          btn_wireframe: '와이어프레임',
          btn_hotspots: '핫스팟',
          btn_rotate: '자동 회전',
          btn_physiology: '생리 박동',
          btn_snapshot: 'PNG 저장',
          btn_reset: '초기화',
          tab_structure: '구조',
          tab_clinical: '임상',
          tab_quiz: '3D 퀴즈',
          tts_title: '음성 해설',
          tts_read: '읽기',
          sec_overview: '해부학적 개요',
          sec_function: '주요 생리학적 기능',
          sec_terminology: '해부학 용어',
          sec_biometrics: '기준 생체 지표',
          sec_hotspots: '해부학 핀 (1–5)',
          tap_pin: '핀을 탭하여 상세 보기',
          hotspot_placeholder: '3D 모델 또는 위의 번호 핀(1–5)을 클릭하여 해부학적 구조, 위치 및 기능을 확인하세요.',
          sec_learning_points: '핵심 해부학 학습 포인트',
          clinical_disclaimer_title: '교육 안내:',
          clinical_disclaimer: '이 임상 개요는 의학 교육 전용이며 의학적 진단이나 개인 치료 조언을 제공하지 않습니다.',
          clin_diseases: '주요 질환 및 임상적 맥락',
          clin_causes: '원인 및 위험 요인',
          clin_symptoms: '전형적인 증상',
          clin_effects: '신체에 미치는 영향',
          clin_prevention: '예방 및 건강 교육',
          quiz_progress: '퀴즈 진행률',
          quiz_target: '목표 구조 식별',
          quiz_instruction: '3D 홀로그램에서 일치하는 번호 핀(1–5)을 직접 클릭하거나 아래 버튼을 선택하세요:',
          quiz_prompt_tpl: '{name} ({latin})을(를) 나타내는 핀을 클릭하세요.',
          contact_us: '문의하기',
          refs_link: '참고 문헌 및 제한 사항',
          cat_all: '모든 장기',
          cat_nervous: '신경 및 감각',
          cat_thorax: '흉부',
          cat_cardio: '심혈관계',
          cat_resp: '호흡기계',
          cat_digestive: '소화기계',
          cat_urinary: '비뇨기계',
          cat_repro: '생식기계',
          cat_musculo: '근골격계',
          cat_integ: '피부계',
        },
        ja: {
          badge_museum: '3D 医学ミュージアム',
          settings_btn: '設定',
          settings_title: '表示設定',
          opt_view_layer: '3Dレイヤーモード（臓器 / 全身 / 分割）',
          opt_language: '言語選択',
          opt_theme: '画面テーマ（ダーク / ライト / 自動）',
          opt_screen_mode: '画面レイアウトモード',
          opt_fullscreen: '全画面表示',
          catalog_short: 'カタログ',
          view_organ: '単一臓器',
          view_fullbody: '全身モデル',
          view_split: '分割比較',
          active_specimen: '選択中の標本',
          catalog_title: '解剖学カタログ',
          load_glb: '検証済みGLB/GLTF読込',
          phys_sim: '生理シミュレーション',
          phys_auto: '自動（臓器別）',
          phys_blood: '血流',
          phys_resp: '呼吸',
          phys_dig: '消化',
          phys_nerv: '神経信号',
          phys_off: 'オフ',
          phys_arterial: '動脈血 (O₂)',
          phys_venous: '静脈血 (CO₂)',
          clipping: '断面:',
          explode: '分解:',
          btn_section: '断面 / 分解',
          btn_holoscan: 'ホロスキャン',
          btn_xray: 'X線透過',
          btn_wireframe: 'ワイヤーフレーム',
          btn_hotspots: 'ピン表示',
          btn_rotate: '自動回転',
          btn_physiology: '生理拍動',
          btn_snapshot: 'PNG保存',
          btn_reset: 'リセット',
          tab_structure: '構造',
          tab_clinical: '臨床',
          tab_quiz: '3Dクイズ',
          tts_title: '音声ナレーション',
          tts_read: '読み上げ',
          sec_overview: '解剖学的概要',
          sec_function: '主な生理学的機能',
          sec_terminology: '解剖学用語',
          sec_biometrics: '基準生体データ',
          sec_hotspots: 'ホットスポット (1–5)',
          tap_pin: 'ピンをタップして詳細表示',
          hotspot_placeholder: '3Dモデルまたは上の番号ピン(1–5)をクリックすると、構造・位置・機能が表示されます。',
          sec_learning_points: '重要な解剖学学習ポイント',
          clinical_disclaimer_title: '教育上の注意:',
          clinical_disclaimer: 'この臨床概要は医学教育専用であり、医療診断や個別の治療助言を提供するものではありません。',
          clin_diseases: '主な疾患と臨床的背景',
          clin_causes: '原因と危険因子',
          clin_symptoms: '典型的な症状',
          clin_effects: '身体への影響',
          clin_prevention: '予防と健康教育',
          quiz_progress: 'クイズ進捗',
          quiz_target: 'ターゲット識別',
          quiz_instruction: '3Dホログラム上の該当する番号ピン(1–5)をクリックするか、下から選択してください:',
          quiz_prompt_tpl: '{name} ({latin}) を示すピンをクリックしてください。',
          contact_us: 'お問い合わせ',
          refs_link: '参考文献と制限事項',
          cat_all: 'すべての臓器',
          cat_nervous: '神経・感覚器',
          cat_thorax: '胸部',
          cat_cardio: '循環器系',
          cat_resp: '呼吸器系',
          cat_digestive: '消化器系',
          cat_urinary: '泌尿器系',
          cat_repro: '生殖器系',
          cat_musculo: '筋骨格系',
          cat_integ: '外皮系',
        },
        vi: {
          badge_museum: 'BẢO TÀNG Y KHOA 3D',
          settings_btn: 'Cài đặt',
          settings_title: 'CÀI ĐẶT HIỂN THỊ',
          opt_view_layer: 'Chế độ lớp 3D (Cơ quan / Toàn thân / Chia đôi)',
          opt_language: 'Chọn ngôn ngữ',
          opt_theme: 'Giao diện màn hình (Tối / Sáng / Tự động)',
          opt_screen_mode: 'Chế độ bố cục màn hình',
          opt_fullscreen: 'Toàn màn hình',
          catalog_short: 'Danh mục',
          view_organ: 'Cơ quan',
          view_fullbody: 'Toàn thân',
          view_split: 'So sánh',
          active_specimen: 'MẪU ĐANG XEM',
          catalog_title: 'DANH MỤC GIẢI PHẪU',
          load_glb: 'Tải GLB/GLTF đã xác thực',
          phys_sim: 'MÔ PHỎNG SINH LÝ',
          phys_auto: 'Tự động (Cơ quan)',
          phys_blood: 'Dòng máu',
          phys_resp: 'Hô hấp',
          phys_dig: 'Tiêu hóa',
          phys_nerv: 'Tín hiệu thần kinh',
          phys_off: 'Tắt',
          phys_arterial: 'Động mạch (O₂)',
          phys_venous: 'Tĩnh mạch (CO₂)',
          clipping: 'Mặt cắt:',
          explode: 'Tách lớp:',
          btn_section: 'Mặt cắt / Tách',
          btn_holoscan: 'Quét Holo',
          btn_xray: 'X-Quang',
          btn_wireframe: 'Khung lưới',
          btn_hotspots: 'Điểm chốt',
          btn_rotate: 'Tự xoay',
          btn_physiology: 'Nhịp sinh lý',
          btn_snapshot: 'Lưu PNG',
          btn_reset: 'Đặt lại',
          tab_structure: 'Cấu trúc',
          tab_clinical: 'Lâm sàng',
          tab_quiz: 'Đố vui 3D',
          tts_title: 'THUYẾT MINH ÂM THANH',
          tts_read: 'Đọc',
          sec_overview: 'TỔNG QUAN GIẢI PHẪU',
          sec_function: 'CHỨC NĂNG SINH LÝ CHÍNH',
          sec_terminology: 'THUẬT NGỮ GIẢI PHẪU',
          sec_biometrics: 'CHỈ SỐ SINH TRẮC THAM KHẢO',
          sec_hotspots: 'ĐIỂM GIẢI PHẪU (1–5)',
          tap_pin: 'Chạm ghim để kiểm tra',
          hotspot_placeholder: 'Nhấp vào bất kỳ ghim đánh số nào (1–5) trên mô hình 3D để xem cấu trúc, vị trí và chức năng.',
          sec_learning_points: 'ĐIỂM HỌC TẬP GIẢI PHẪU CHÍNH',
          clinical_disclaimer_title: 'Lưu ý giáo dục:',
          clinical_disclaimer: 'Tổng quan lâm sàng này chỉ phục vụ giáo dục y khoa và không thay thế chẩn đoán hay điều trị y tế.',
          clin_diseases: 'BỆNH LÝ THƯỜNG GẶP & BỐI CẢNH LÂM SÀNG',
          clin_causes: 'NGUYÊN NHÂN & YẾU TỐ NGUY CƠ',
          clin_symptoms: 'TRIỆU CHỨNG ĐIỂN HÌNH',
          clin_effects: 'TÁC ĐỘNG LÊN CƠ THỂ',
          clin_prevention: 'PHÒNG NGỪA & GIÁO DỤC SỨC KHỎE',
          quiz_progress: 'TIẾN ĐỘ BÀI KIỂM TRA',
          quiz_target: 'XÁC ĐỊNH MỤC TIÊU',
          quiz_instruction: 'Nhấp vào ghim đánh số tương ứng (1–5) trực tiếp trên mô hình 3D hoặc chọn bên dưới:',
          quiz_prompt_tpl: 'Nhấp vào ghim xác định {name} ({latin}).',
          contact_us: 'LIÊN HỆ',
          refs_link: 'Tài liệu tham khảo & Giới hạn',
          cat_all: 'Tất cả cơ quan',
          cat_nervous: 'Thần kinh & Giác quan',
          cat_thorax: 'Lồng ngực',
          cat_cardio: 'Tim mạch',
          cat_resp: 'Hô hấp',
          cat_digestive: 'Tiêu hóa',
          cat_urinary: 'Tiết niệu',
          cat_repro: 'Sinh sản',
          cat_musculo: 'Cơ xương khớp',
          cat_integ: 'Da liễu',
        },
        th: {
          badge_museum: 'พิพิธภัณฑ์การแพทย์ 3 มิติ',
          settings_btn: 'ตั้งค่า',
          settings_title: 'การตั้งค่าการแสดงผล',
          opt_view_layer: 'โหมดเลเยอร์ 3 มิติ (อวัยวะ / เต็มตัว / แบ่งหน้าจอ)',
          opt_language: 'เลือกภาษา',
          opt_theme: 'ธีมหน้าจอ (มืด / สว่าง / อัตโนมัติ)',
          opt_screen_mode: 'โหมดเค้าโครงหน้าจอ',
          opt_fullscreen: 'เต็มหน้าจอ',
          catalog_short: 'แคตตาล็อก',
          view_organ: 'อวัยวะ',
          view_fullbody: 'เต็มตัว',
          view_split: 'เปรียบเทียบ',
          active_specimen: 'ตัวอย่างที่เลือก',
          catalog_title: 'แคตตาล็อกกายวิภาค',
          load_glb: 'โหลด GLB/GLTF ที่ตรวจสอบแล้ว',
          phys_sim: 'จำลองสรีรวิทยา',
          phys_auto: 'อัตโนมัติ (ตามอวัยวะ)',
          phys_blood: 'การไหลเวียนเลือด',
          phys_resp: 'การหายใจ',
          phys_dig: 'การย่อยอาหาร',
          phys_nerv: 'สัญญาณประสาท',
          phys_off: 'ปิด',
          phys_arterial: 'เลือดแดง (O₂)',
          phys_venous: 'เลือดดำ (CO₂)',
          clipping: 'ภาพตัด:',
          explode: 'แยกส่วน:',
          btn_section: 'ภาพตัด / แยกส่วน',
          btn_holoscan: 'สแกนโฮโล',
          btn_xray: 'เอกซเรย์',
          btn_wireframe: 'โครงลวด',
          btn_hotspots: 'จุดหมุด',
          btn_rotate: 'หมุนอัตโนมัติ',
          btn_physiology: 'จังหวะมีชีวิต',
          btn_snapshot: 'บันทึก PNG',
          btn_reset: 'รีเซ็ต',
          tab_structure: 'โครงสร้าง',
          tab_clinical: 'คลินิก',
          tab_quiz: 'แบบทดสอบ 3D',
          tts_title: 'เสียงบรรยาย',
          tts_read: 'อ่าน',
          sec_overview: 'ภาพรวมทางกายวิภาค',
          sec_function: 'หน้าที่ทางสรีรวิทยาหลัก',
          sec_terminology: 'คำศัพท์ทางกายวิภาค',
          sec_biometrics: 'ข้อมูลชีวมาตรอ้างอิง',
          sec_hotspots: 'จุดสำคัญทางกายวิภาค (1–5)',
          tap_pin: 'แตะหมุดเพื่อตรวจสอบ',
          hotspot_placeholder: 'คลิกที่หมุดหมายเลข (1–5) บนโมเดล 3 มิติเพื่อตรวจสอบโครงสร้าง ตำแหน่ง และหน้าที่',
          sec_learning_points: 'จุดเรียนรู้กายวิภาคที่สำคัญ',
          clinical_disclaimer_title: 'ประกาศเพื่อการศึกษา:',
          clinical_disclaimer: 'ภาพรวมทางคลินิกนี้จัดทำขึ้นเพื่อการศึกษาทางการแพทย์เท่านั้น ไม่ใช่การวินิจฉัยโรค',
          clin_diseases: 'ภาวะที่พบบ่อยและบริบททางคลินิก',
          clin_causes: 'สาเหตุและปัจจัยเสี่ยง',
          clin_symptoms: 'อาการทั่วไป',
          clin_effects: 'ผลกระทบต่อร่างกาย',
          clin_prevention: 'การป้องกันและสุขศึกษา',
          quiz_progress: 'ความคืบหน้าแบบทดสอบ',
          quiz_target: 'การระบุเป้าหมาย',
          quiz_instruction: 'คลิกหมุดหมายเลขที่ตรงกัน (1–5) บนโฮโลแกรม 3 มิติโดยตรง หรือเลือกด้านล่าง:',
          quiz_prompt_tpl: 'คลิกหมุดที่ระบุตำแหน่งของ {name} ({latin})',
          contact_us: 'ติดต่อเรา',
          refs_link: 'เอกสารอ้างอิงและข้อจำกัด',
          cat_all: 'อวัยวะทั้งหมด',
          cat_nervous: 'ประสาทและประสาทสัมผัส',
          cat_thorax: 'ทรวงอก',
          cat_cardio: 'หัวใจและหลอดเลือด',
          cat_resp: 'ระบบหายใจ',
          cat_digestive: 'ระบบย่อยอาหาร',
          cat_urinary: 'ระบบทางเดินปัสสาวะ',
          cat_repro: 'ระบบสืบพันธุ์',
          cat_musculo: 'ระบบกล้ามเนื้อและกระดูก',
          cat_integ: 'ระบบผิวหนัง',
        },
        hi: {
          badge_museum: '3D चिकित्सा संग्रहालय',
          settings_btn: 'सेटिंग्स',
          settings_title: 'डिस्प्ले सेटिंग्स',
          opt_view_layer: '3D लेयर मोड (अंग / पूरा शरीर / विभाजित)',
          opt_language: 'भाषा चयन',
          opt_theme: 'स्क्रीन थीम (डार्क / लाइट / ऑटो)',
          opt_screen_mode: 'स्क्रीन लेआउट मोड',
          opt_fullscreen: 'फुलस्क्रीन मोड',
          catalog_short: 'कैटलॉग',
          view_organ: 'अंग',
          view_fullbody: 'पूरा शरीर',
          view_split: 'तुलना',
          active_specimen: 'सक्रिय नमूना',
          catalog_title: 'शरीर रचना कैटलॉग',
          load_glb: 'सत्यापित GLB/GLTF लोड करें',
          phys_sim: 'फिजियोलॉजी सिमुलेशन',
          phys_auto: 'ऑटो (अंग अनुसार)',
          phys_blood: 'रक्त प्रवाह',
          phys_resp: 'श्वसन',
          phys_dig: 'पाचन',
          phys_nerv: 'तंत्रिका संकेत',
          phys_off: 'बंद',
          phys_arterial: 'धमनी (O₂)',
          phys_venous: 'शिरापरक (CO₂)',
          clipping: 'अनुभाग:',
          explode: 'विस्तार:',
          btn_section: 'अनुभाग / विस्तार',
          btn_holoscan: 'होलो स्कैन',
          btn_xray: 'एक्स-रे',
          btn_wireframe: 'वायरफ्रेम',
          btn_hotspots: 'हॉटस्पॉट',
          btn_rotate: 'घुमाएं',
          btn_physiology: 'जीवंत स्पंदन',
          btn_snapshot: 'PNG सहेजें',
          btn_reset: 'रीसेट',
          tab_structure: 'संरचना',
          tab_clinical: 'नैदानिक',
          tab_quiz: '3D क्विज़',
          tts_title: 'ऑडियो विवरण',
          tts_read: 'पढ़ें',
          sec_overview: 'शारीरिक अवलोकन',
          sec_function: 'मुख्य शारीरिक कार्य',
          sec_terminology: 'शारीरिक शब्दावली',
          sec_biometrics: 'संदर्भ बायोमेट्रिक्स',
          sec_hotspots: 'हॉटस्पॉट (1–5)',
          tap_pin: 'जांचने के लिए पिन टैप करें',
          hotspot_placeholder: 'संरचना, स्थान और कार्य देखने के लिए 3D मॉडल पर किसी भी क्रमांकित पिन (1–5) पर क्लिक करें।',
          sec_learning_points: 'मुख्य शारीरिक शिक्षण बिंदु',
          clinical_disclaimer_title: 'शैक्षिक सूचना:',
          clinical_disclaimer: 'यह नैदानिक अवलोकन केवल चिकित्सा शिक्षा के लिए है और चिकित्सा निदान प्रदान नहीं करता है।',
          clin_diseases: 'सामान्य स्थितियां और नैदानिक संदर्भ',
          clin_causes: 'कारण और जोखिम कारक',
          clin_symptoms: 'सामान्य लक्षण',
          clin_effects: 'शरीर पर प्रभाव',
          clin_prevention: 'रोकथाम और स्वास्थ्य शिक्षा',
          quiz_progress: 'क्विज़ प्रगति',
          quiz_target: 'लक्ष्य पहचान',
          quiz_instruction: '3D होलोग्राम पर सीधे मिलान करने वाले पिन (1–5) पर क्लिक करें या नीचे चुनें:',
          quiz_prompt_tpl: '{name} ({latin}) की पहचान करने वाले पिन पर क्लिक करें।',
          contact_us: 'संपर्क करें',
          refs_link: 'संदर्भ और सीमाएं',
          cat_all: 'सभी अंग',
          cat_nervous: 'तंत्रिका और इंद्रियां',
          cat_thorax: 'वक्ष',
          cat_cardio: 'हृदय प्रणाली',
          cat_resp: 'श्वसन प्रणाली',
          cat_digestive: 'पाचन प्रणाली',
          cat_urinary: 'मूत्र प्रणाली',
          cat_repro: 'प्रजनन प्रणाली',
          cat_musculo: 'मस्कुलोस्केलेटल',
          cat_integ: 'त्वचा प्रणाली',
        },
        ar: {
          badge_museum: 'المتحف الطبي ثلاثي الأبعاد',
          settings_btn: 'الإعدادات',
          settings_title: 'إعدادات العرض',
          opt_view_layer: 'وضع الطبقة 3D (عضو / الجسم الكامل / مقسم)',
          opt_language: 'اختيار اللغة',
          opt_theme: 'مظهر الشاشة (داكن / فاتح / تلقائي)',
          opt_screen_mode: 'وضع تخطيط الشاشة',
          opt_fullscreen: 'ملء الشاشة',
          catalog_short: 'الفهرس',
          view_organ: 'العضو',
          view_fullbody: 'الجسم الكامل',
          view_split: 'مقارنة',
          active_specimen: 'العينة النشطة',
          catalog_title: 'فهرس التشريح',
          load_glb: 'تحميل نموذج GLB/GLTF',
          phys_sim: 'محاكاة الفسيولوجيا',
          phys_auto: 'تلقائي (حسب العضو)',
          phys_blood: 'تدفق الدم',
          phys_resp: 'التنفس',
          phys_dig: 'الهضم',
          phys_nerv: 'الإشارة العصبية',
          phys_off: 'إيقاف',
          phys_arterial: 'شرياني (O₂)',
          phys_venous: 'وريدي (CO₂)',
          clipping: 'المقطع:',
          explode: 'تفكيك:',
          btn_section: 'مقطع / تفكيك',
          btn_holoscan: 'مسح هولوغرافي',
          btn_xray: 'أشعة سينية',
          btn_wireframe: 'شبكة هيكلية',
          btn_hotspots: 'نقاط التحديد',
          btn_rotate: 'تدوير',
          btn_physiology: 'نبض حي',
          btn_snapshot: 'حفظ PNG',
          btn_reset: 'إعادة ضبط',
          tab_structure: 'البنية',
          tab_clinical: 'سريري',
          tab_quiz: 'اختبار 3D',
          tts_title: 'السرد الصوتي',
          tts_read: 'قراءة',
          sec_overview: 'نظرة عامة تشريحية',
          sec_function: 'الوظيفة الفسيولوجية الرئيسية',
          sec_terminology: 'المصطلحات التشريحية',
          sec_biometrics: 'القياسات الحيوية المرجعية',
          sec_hotspots: 'نقاط التحديد (1–5)',
          tap_pin: 'انقر على الدبوس للفحص',
          hotspot_placeholder: 'انقر على أي دبوس مرقم (1–5) على النموذج ثلاثي الأبعاد لفحص بنيته وموقعه ووظيفته.',
          sec_learning_points: 'نقاط التعلم التشريحية الرئيسية',
          clinical_disclaimer_title: 'تنويه تعليمي:',
          clinical_disclaimer: 'هذه النظرة السريرية مخصصة للتعليم الطبي فقط ولا تقدم تشخيصاً طبياً أو نصيحة علاجية فردية.',
          clin_diseases: 'الحالات الشائعة والسياق السريري',
          clin_causes: 'الأسباب وعوامل الخطر',
          clin_symptoms: 'الأعراض النموذجية',
          clin_effects: 'التأثيرات على الجسم',
          clin_prevention: 'الوقاية والتثقيف الصحي',
          quiz_progress: 'تقدم الاختبار',
          quiz_target: 'تحديد الهدف',
          quiz_instruction: 'انقر على الدبوس المرقم المطابق (1–5) مباشرة على المجسم ثلاثي الأبعاد أو اختر أدناه:',
          quiz_prompt_tpl: 'انقر على الدبوس الذي يحدد: {name} ({latin}).',
          contact_us: 'اتصل بنا',
          refs_link: 'المراجع والقيود التقنية',
          cat_all: 'جميع الأعضاء',
          cat_nervous: 'الأعصاب والحواس',
          cat_thorax: 'الصدر',
          cat_cardio: 'القلب والأوعية',
          cat_resp: 'الجهاز التنفسي',
          cat_digestive: 'الجهاز الهضمي',
          cat_urinary: 'الجهاز البولي',
          cat_repro: 'الجهاز التناسلي',
          cat_musculo: 'العضلي الهيكلي',
          cat_integ: 'الجلدي',
        },
      };

      /* =========================================================================
       * 2. ANATOMICAL EDUCATIONAL DATASET (32 SPECIMENS WITH 5 HOTSPOTS EACH)
       * ========================================================================= */
      const CATEGORIES = [
        { id: 'all', key: 'cat_all' },
        { id: 'Nervous System & Special Senses', key: 'cat_nervous' },
        { id: 'Thorax', key: 'cat_thorax' },
        { id: 'Cardiovascular', key: 'cat_cardio' },
        { id: 'Respiratory', key: 'cat_resp' },
        { id: 'Digestive', key: 'cat_digestive' },
        { id: 'Urinary', key: 'cat_urinary' },
        { id: 'Reproductive', key: 'cat_repro' },
        { id: 'Musculoskeletal', key: 'cat_musculo' },
        { id: 'Integumentary', key: 'cat_integ' },
      ];

      function makeSpecimen(cfg) {
        return {
          ...cfg,
          hotspots: cfg.hotspots.map((h, idx) => ({
            id: idx + 1,
            name_en: h[0],
            name_id: h[1],
            latin: h[2],
            location: h[3],
            func: h[4],
            desc: h[5],
            pos: h[6],
            quiz_enabled: true,
          })),
        };
      }

      const SPECIMENS = [
        makeSpecimen({
          id: 'heart',
          name_en: 'Heart',
          name_id: 'Jantung',
          latin: 'Cor / Cardia',
          organ_system: 'Cardiovascular',
          categories: ['Cardiovascular', 'Thorax'],
          builder: 'heart',
          phys_default: 'blood',
          body_pos: [0.08, 1.32, 0.08],
          overview_en: 'A four-chambered fibromuscular pump located in the middle mediastinum of the thorax, enclosed within the pericardial sac.',
          overview_id: 'Pompa fibromuskular empat ruang yang terletak di mediastinum tengah toraks, terbungkus di dalam kantung perikardium.',
          physiology_en: 'Generates pressure gradients via coordinated systole and diastole to propel deoxygenated blood to the lungs and oxygenated blood throughout systemic circulation.',
          physiology_id: 'Menghasilkan gradien tekanan melalui sistol dan diastol terkoordinasi untuk memompa darah terdeoksigenasi ke paru-paru dan darah beroksigen ke seluruh tubuh.',
          metrics: [
            { label: 'ADULT WEIGHT', val: '250–350 g', sub: 'Adult reference range' },
            { label: 'CARDIAC OUTPUT', val: '~5.0 L/min', sub: 'Resting adult average' },
            { label: 'HEART RATE', val: '60–100 bpm', sub: 'Normal resting sinus' },
            { label: 'WALL LAYERS', val: '3 Layers', sub: 'Epi-, Myo-, Endocardium' },
          ],
          learning_points: [
            'The right side drives low-pressure pulmonary circulation; the left ventricle drives high-pressure systemic circulation.',
            'Atrioventricular (tricuspid, mitral) and semilunar (pulmonary, aortic) valves enforce unidirectional blood flow.',
            'The sinoatrial (SA) node acts as the primary physiological pacemaker initiating cardiac depolarization.',
            'Coronary arteries branching from the ascending aorta perfuse the myocardium primarily during ventricular diastole.',
            'Three histological wall layers—epicardium, myocardium, and endocardium—coordinate mechanical contraction.',
          ],
          clinical: {
            diseases: 'Coronary artery disease (CAD), myocardial infarction, heart failure, arrhythmias, and valvular stenosis or regurgitation.',
            causes: 'Atherosclerosis, chronic hypertension, dyslipidemia, smoking, diabetes mellitus, and genetic cardiomyopathies.',
            symptoms: 'Chest pressure or angina, dyspnea on exertion, palpitations, orthopnea, and peripheral ankle edema.',
            effects: 'Reduced tissue perfusion, pulmonary venous congestion, systemic hypoxia, and neurohormonal fluid retention.',
            prevention: 'Regular aerobic activity, balanced heart-healthy nutrition, blood pressure/lipid monitoring, and tobacco avoidance.',
          },
          hotspots: [
            ['Aortic Arch', 'Lengkung Aorta', 'Arcus aortae', 'Superior mediastinum', 'Distributes oxygenated blood to head, neck, upper limbs, and descending aorta.', 'Gives rise to the brachiocephalic trunk, left common carotid, and left subclavian arteries.', [0.18, 1.25, -0.02]],
            ['Superior Vena Cava', 'Vena Kava Superior', 'Vena cava superior', 'Right superior mediastinum', 'Returns deoxygenated venous blood from upper body to right atrium.', 'Formed by union of left and right brachiocephalic veins.', [-0.52, 1.15, -0.03]],
            ['Pulmonary Trunk', 'Trunkus Pulmonalis', 'Truncus pulmonalis', 'Anterior to ascending aorta', 'Carries deoxygenated blood from right ventricle toward the lungs.', 'Bifurcates beneath the aortic arch into left and right pulmonary arteries.', [0.05, 0.76, 0.28]],
            ['Right Atrium', 'Atrium Kanan', 'Atrium dextrum', 'Right border of heart', 'Receives systemic venous return from SVC, IVC, and coronary sinus.', 'Contains the sinoatrial (SA) node near the SVC opening.', [-0.62, 0.24, 0.14]],
            ['Left Ventricle & Apex', 'Ventrikel Kiri & Apeks', 'Ventriculus sinister', 'Inferolateral cardiac apex', 'Pumps oxygenated blood through aortic valve into systemic circulation.', 'Features the thickest myocardial wall (~10–15 mm) to overcome systemic vascular resistance.', [0.46, -0.45, 0.35]],
          ],
        }),

        makeSpecimen({
          id: 'brain',
          name_en: 'Brain',
          name_id: 'Otak',
          latin: 'Encephalon / Cerebrum',
          organ_system: 'Nervous System & Special Senses',
          categories: ['Nervous System & Special Senses'],
          builder: 'brain',
          phys_default: 'nervous',
          body_pos: [0, 2.35, 0],
          overview_en: 'The central command organ of the central nervous system housed within the neurocranium, comprising the cerebrum, diencephalon, cerebellum, and brainstem.',
          overview_id: 'Organ pusat kendali sistem saraf pusat yang terlindung di dalam neurokranium, terdiri atas serebrum, diensefalon, serebelum, dan batang otak.',
          physiology_en: 'Integrates sensory afferents, coordinates voluntary and autonomic motor outputs, and sustains cognition, memory, emotion, and homeostasis.',
          physiology_id: 'Mengintegrasikan sinyal sensorik aferen, mengoordinasikan respons motorik somatik maupun otonom, serta mengatur kognisi, memori, dan homeostasis.',
          metrics: [
            { label: 'ADULT MASS', val: '1,300–1,400 g', sub: '~2% of body weight' },
            { label: 'BLOOD FLOW', val: '~750 mL/min', sub: '~15% cardiac output' },
            { label: 'NEURONS', val: '~86 Billion', sub: 'Supported by glial cells' },
            { label: 'CSF VOLUME', val: '~150 mL', sub: 'Cushions CNS structures' },
          ],
          learning_points: [
            'The cerebral cortex is divided into frontal, parietal, temporal, and occipital lobes separated by sulci and fissures.',
            'The longitudinal fissure separates left and right cerebral hemispheres, connected by the corpus callosum.',
            'The cerebellum coordinates fine motor precision, posture, and vestibular balance.',
            'The brainstem (midbrain, pons, medulla oblongata) regulates vital respiratory and cardiovascular centers.',
            'The blood-brain barrier (BBB) selectively regulates molecular transport into neural parenchyma.',
          ],
          clinical: {
            diseases: 'Ischemic and hemorrhagic stroke, epilepsy, neurodegenerative disorders (Alzheimer, Parkinson), meningitis, and migraine.',
            causes: 'Cerebrovascular occlusion, uncontrolled hypertension, traumatic brain injury, autoimmune inflammation, or infection.',
            symptoms: 'Focal motor weakness, aphasia, sudden severe headache, seizures, memory impairment, or altered consciousness.',
            effects: 'Loss of motor/sensory pathways, cognitive decline, autonomic dysregulation, or elevated intracranial pressure.',
            prevention: 'Vascular risk control, head injury protection, cognitive engagement, restorative sleep, and balanced nutrition.',
          },
          hotspots: [
            ['Frontal Lobe', 'Lobus Frontalis', 'Lobus frontalis', 'Anterior cranial fossa', 'Governs executive function, voluntary motor control, and expressive speech.', 'Contains the primary motor cortex (precentral gyrus) and Broca area.', [0.28, 0.42, 0.68]],
            ['Parietal Lobe', 'Lobus Parietalis', 'Lobus parietalis', 'Superior lateral cerebrum', 'Processes somatosensory touch, spatial orientation, and proprioception.', 'Located posterior to the central sulcus (postcentral gyrus).', [-0.36, 0.62, -0.15]],
            ['Temporal Lobe', 'Lobus Temporalis', 'Lobus temporalis', 'Middle cranial fossa', 'Processes auditory input, language comprehension, and declarative memory.', 'Houses the primary auditory cortex and deep hippocampal structures.', [0.54, 0.02, 0.14]],
            ['Cerebellum', 'Otak Kecil', 'Cerebellum', 'Posterior cranial fossa', 'Coordinates motor timing, balance, equilibrium, and motor learning.', 'Connected to the brainstem via superior, middle, and inferior cerebellar peduncles.', [-0.32, -0.46, -0.52]],
            ['Brainstem (Pons & Medulla)', 'Batang Otak', 'Truncus encephali', 'Inferior base of brain', 'Relays ascending/descending tracts and controls heart rate and breathing.', 'Contains cranial nerve nuclei III–XII and vital autonomic centers.', [0.0, -0.74, -0.12]],
          ],
        }),

        makeSpecimen({
          id: 'eye',
          name_en: 'Eye',
          name_id: 'Mata',
          latin: 'Bulbus oculi',
          organ_system: 'Nervous System & Special Senses',
          categories: ['Nervous System & Special Senses'],
          builder: 'eye',
          phys_default: 'nervous',
          body_pos: [0.12, 2.32, 0.25],
          overview_en: 'A specialized paired sensory organ situated within the bony orbit that focuses light onto a photosensitive neural retina.',
          overview_id: 'Organ indra penglihatan berpasangan di dalam rongga orbita yang memfokuskan cahaya ke retina saraf fotosensitif.',
          physiology_en: 'Refracts incoming photons through the cornea and crystalline lens, converting optical images into action potentials via rod and cone photoreceptors.',
          physiology_id: 'Membiaskan cahaya melalui kornea dan lensa kristalina, mengubah citra optik menjadi potensial aksi melalui fotoreseptor batang dan kerucut.',
          metrics: [
            { label: 'AXIAL LENGTH', val: '~24 mm', sub: 'Emmetropic adult globe' },
            { label: 'REFRACTIVE POWER', val: '~60 Diopters', sub: 'Cornea ~43D + Lens ~17D' },
            { label: 'PHOTORECEPTORS', val: '~126 Million', sub: '120M rods, 6M cones' },
            { label: 'IOP RANGE', val: '10–21 mmHg', sub: 'Intraocular pressure' },
          ],
          learning_points: [
            'Three concentric tunics form the eyeball: fibrous (sclera/cornea), vascular uvea (choroid/ciliary body/iris), and neural retina.',
            'The iris regulates pupillary aperture diameter via sphincter and dilator pupillae smooth muscles.',
            'Ciliary muscle contraction relaxes zonular fibers, increasing lens curvature for near accommodation.',
            'The macula lutea and fovea centralis provide highest cone-mediated visual acuity.',
            'Retinal ganglion cell axons exit at the optic disc (blind spot) to form Cranial Nerve II.',
          ],
          clinical: {
            diseases: 'Refractive errors (myopia, hyperopia), cataract, glaucoma, age-related macular degeneration, and diabetic retinopathy.',
            causes: 'Aging lens protein denaturation, elevated intraocular pressure, microvascular diabetes damage, and UV exposure.',
            symptoms: 'Blurred vision, halos around lights, peripheral visual field loss, eye strain, or floaters.',
            effects: 'Progressive visual impairment or irreversible optic nerve neuropathy if untreated.',
            prevention: 'Routine comprehensive eye exams, UV-blocking eyewear, glycemic control, and screen break ergonomics.',
          },
          hotspots: [
            ['Cornea', 'Kornea', 'Cornea', 'Anterior fibrous tunic', 'Provides primary fixed optical refraction (~70% of focusing power) and protection.', 'Avascular transparent dome nourished by tear film and aqueous humor.', [0.0, 0.0, 1.02]],
            ['Iris & Pupil', 'Iris & Pupil', 'Iris et Pupilla', 'Anterior to crystalline lens', 'Controls light entry into the posterior segment by adjusting pupil size.', 'Pigmented smooth muscle diaphragm dividing anterior and posterior chambers.', [0.28, 0.12, 0.88]],
            ['Crystalline Lens', 'Lensa Kristalina', 'Lens', 'Posterior to iris', 'Fine-tunes focal length (accommodation) onto the retina.', 'Transparent biconvex structure suspended by ciliary zonules.', [0.0, 0.25, 0.64]],
            ['Retina & Macula', 'Retina & Makula', 'Retina', 'Posterior inner lining', 'Transduces light energy into neural signals via rods and cones.', 'Contains ten histological layers culminating in optic nerve fibers.', [-0.65, 0.25, -0.45]],
            ['Optic Nerve (CN II)', 'Saraf Optik', 'Nervus opticus', 'Posterior pole of globe', 'Transmits visual action potentials from retina to lateral geniculate nucleus.', 'Surrounded by meningeal sheaths continuous with the brain.', [-0.08, -0.1, -1.18]],
          ],
        }),

        makeSpecimen({
          id: 'ear',
          name_en: 'Ear',
          name_id: 'Telinga',
          latin: 'Auris',
          organ_system: 'Nervous System & Special Senses',
          categories: ['Nervous System & Special Senses'],
          builder: 'ear',
          phys_default: 'nervous',
          body_pos: [0.28, 2.28, 0.0],
          overview_en: 'An auditory and vestibular sensory organ divided into external, middle, and internal compartments within the temporal bone.',
          overview_id: 'Organ indra pendengaran dan keseimbangan yang terbagi menjadi telinga luar, tengah, dan dalam di dalam tulang temporal.',
          physiology_en: 'Captures airborne acoustic waves, amplifies mechanical vibrations via ossicles, and transduces fluid motion into auditory and equilibrium nerve impulses.',
          physiology_id: 'Menangkap gelombang suara, memperkuat getaran mekanis melalui tulang pendengaran, dan mengubah gerakan cairan menjadi impuls saraf.',
          metrics: [
            { label: 'AUDIBLE RANGE', val: '20–20,000 Hz', sub: 'Human frequency spectrum' },
            { label: 'OSSICLES', val: '3 Bones', sub: 'Malleus, Incus, Stapes' },
            { label: 'COCHLEAR TURNS', val: '2.75 Turns', sub: 'Spiral organ of Corti' },
            { label: 'SEMICIRCULAR CANALS', val: '3 Orthogonal', sub: 'Angular acceleration' },
          ],
          learning_points: [
            'The auricle (pinna) and external acoustic meatus funnel sound waves to the tympanic membrane.',
            'The auditory ossicles (malleus, incus, stapes) match acoustic impedance between air and cochlear perilymph.',
            'The auditory (Eustachian) tube equalizes middle ear pressure with the nasopharynx.',
            'Hair cells in the cochlear organ of Corti exhibit tonotopic organization from high-frequency base to low-frequency apex.',
            'Semicircular canals, utricle, and saccule detect angular and linear head acceleration.',
          ],
          clinical: {
            diseases: 'Otitis media, otitis externa, sensorineural hearing loss, benign paroxysmal positional vertigo (BPPV), and tinnitus.',
            causes: 'Upper respiratory infections, chronic noise exposure, ototoxic medications, cerumen impaction, or otolith displacement.',
            symptoms: 'Otalgia, conductive or sensorineural hypoacusis, spinning vertigo, tinnitus, or ear fullness.',
            effects: 'Communication barriers, balance instability, and increased fall risk in vestibular dysfunction.',
            prevention: 'Hearing protection in loud environments, safe ear hygiene without cotton swabs, and prompt infection care.',
          },
          hotspots: [
            ['Auricle (Pinna)', 'Daun Telinga', 'Auricula', 'Lateral head surface', 'Collects and localizes directional sound waves into ear canal.', 'Elastic cartilage framework covered by tightly adherent skin.', [-0.88, 0.25, 0.25]],
            ['Tympanic Membrane', 'Gendang Telinga', 'Membrana tympanica', 'Medial end of ear canal', 'Vibrates in response to acoustic pressure waves, driving the malleus.', 'Translucent fibrous partition separating outer and middle ear.', [-0.14, 0.0, 0.12]],
            ['Auditory Ossicles', 'Tulang Pendengaran', 'Ossicula auditus', 'Tympanic cavity', 'Amplifies mechanical vibrations and transmits them to the oval window.', 'Smallest bones in the human body: malleus, incus, and stapes.', [0.14, 0.18, 0.06]],
            ['Semicircular Canals', 'Kanalis Semisirkularis', 'Canales semicirculares', 'Superior inner ear labyrinth', 'Detects rotational head movements in three perpendicular planes.', 'Contains endolymph stimulating hair cells in each ampulla.', [0.58, 0.42, -0.08]],
            ['Cochlea', 'Koklea (Rumah Siput)', 'Cochlea', 'Anterior inner ear labyrinth', 'Transduces fluid pressure waves into frequency-specific auditory signals.', 'Spiral bony canal housing scala vestibuli, media, and tympani.', [0.76, -0.22, 0.16]],
          ],
        }),

        makeSpecimen({
          id: 'nose',
          name_en: 'Nose',
          name_id: 'Hidung',
          latin: 'Nasus',
          organ_system: 'Respiratory',
          categories: ['Respiratory', 'Nervous System & Special Senses'],
          builder: 'nose',
          phys_default: 'respiration',
          body_pos: [0, 2.25, 0.28],
          overview_en: 'The external nasal pyramid and paired internal nasal cavities forming the upper entry of the respiratory tract and housing olfactory neuroepithelium.',
          overview_id: 'Piramida hidung luar dan rongga hidung internal berpasangan yang membentuk pintu masuk saluran napas atas serta epitel olfaktorius.',
          physiology_en: 'Warms, humidifies, and filters inhaled air via turbulent conchal airflow while detecting volatile odorants via Cranial Nerve I.',
          physiology_id: 'Menghangatkan, melembapkan, dan menyaring udara inspirasi melalui aliran turbulen konka serta mendeteksi molekul bau melalui Saraf Kranial I.',
          metrics: [
            { label: 'TURBINATES', val: '3 Pairs', sub: 'Superior, middle, inferior' },
            { label: 'AIR HUMIDIFICATION', val: '~95–98% RH', sub: 'By nasopharynx entry' },
            { label: 'PARANASAL SINUSES', val: '4 Pairs', sub: 'Frontal, ethmoid, sphenoid, maxillary' },
            { label: 'OLFACTORY AREA', val: '~5 cm²', sub: 'Superior nasal roof' },
          ],
          learning_points: [
            'The nasal septum divides the nasal cavity into right and left fossae via septal cartilage, vomer, and perpendicular ethmoid plate.',
            'Superior, middle, and inferior nasal conchae increase mucosal surface area for air conditioning.',
            'Pseudostratified ciliated columnar epithelium traps particulates in mucus and sweeps them toward the pharynx.',
            'Paranasal sinuses lighten the skull, resonate voice, and drain into nasal meatuses.',
            'Olfactory receptor neuron axons traverse the cribriform plate to synapse in the olfactory bulb.',
          ],
          clinical: {
            diseases: 'Allergic rhinitis, acute/chronic rhinosinusitis, nasal septum deviation, epistaxis, and anosmia.',
            causes: 'Aeroallergens, viral/bacterial mucosal infection, dry air trauma at Kiesselbach plexus, or nasal polyps.',
            symptoms: 'Nasal congestion, rhinorrhea, sneezing, facial sinus pressure, nosebleeds, or reduced smell.',
            effects: 'Mouth breathing, sleep-disordered breathing, impaired olfaction/taste, and sinus ostial obstruction.',
            prevention: 'Saline nasal irrigation, indoor humidity balance, allergen avoidance, and avoiding digital nasal trauma.',
          },
          hotspots: [
            ['Nasal Bridge & Dorsum', 'Punggung Hidung', 'Dorsum nasi', 'Superior external nose', 'Provides structural bony-cartilaginous support to the external nose.', 'Formed superiorly by paired nasal bones and inferiorly by lateral cartilages.', [0.0, 0.35, 0.48]],
            ['Nasal Septum', 'Septum Nasi', 'Septum nasi', 'Midline nasal cavity', 'Divides left and right nasal passages and supports the nasal tip.', 'Rich anterior vascular anastomosis (Kiesselbach area) is a common epistaxis site.', [0.0, -0.05, 0.25]],
            ['Nasal Conchae (Turbinates)', 'Konka Nasalis', 'Conchae nasales', 'Lateral nasal wall', 'Creates turbulent airflow to warm, humidify, and filter inspired air.', 'Covered by highly vascular mucoperiosteum capable of engorgement.', [0.28, 0.02, -0.05]],
            ['Olfactory Epithelium', 'Epitel Olfaktorius', 'Regio olfactoria', 'Roof of nasal cavity', 'Detects airborne odorant molecules and initiates smell perception.', 'Bipolar sensory neurons project cilia into surface mucus layer.', [0.0, 0.56, -0.12]],
            ['Nasopharynx & Choanae', 'Koana & Nasofaring', 'Choanae', 'Posterior nasal aperture', 'Conducts conditioned air from nasal cavities into the pharynx.', 'Paired posterior openings bordered by vomer and medial pterygoid plates.', [0.0, -0.25, -0.52]],
          ],
        }),

        makeSpecimen({
          id: 'tongue',
          name_en: 'Tongue',
          name_id: 'Lidah',
          latin: 'Lingua',
          organ_system: 'Digestive',
          categories: ['Digestive', 'Nervous System & Special Senses'],
          builder: 'tongue',
          phys_default: 'digestion',
          body_pos: [0, 2.15, 0.24],
          overview_en: 'A highly mobile muscular hydrostat anchored to the floor of the oral cavity, mandible, and hyoid bone.',
          overview_id: 'Organ hidrostat muskular yang sangat lincah dan melekat pada dasar rongga mulut, mandibula, serta tulang hioid.',
          physiology_en: 'Manipulates food boluses during mastication and deglutition, articulates speech consonants, and mediates gustation via taste buds.',
          physiology_id: 'Memanipulasi bolus makanan saat mengunyah dan menelan, membentuk artikulasi bicara, serta mempersepsikan rasa melalui kuncup pengecap.',
          metrics: [
            { label: 'INTRINSIC MUSCLES', val: '4 Pairs', sub: 'Alter tongue shape' },
            { label: 'EXTRINSIC MUSCLES', val: '4 Pairs', sub: 'Alter tongue position' },
            { label: 'TASTE BUDS', val: '2,000–8,000', sub: 'Sweet, salty, sour, bitter, umami' },
            { label: 'MOTOR NERVE', val: 'CN XII', sub: 'Hypoglossal nerve' },
          ],
          learning_points: [
            'Intrinsic muscles (superior/inferior longitudinal, transverse, vertical) reshape the tongue without bony attachments.',
            'Extrinsic muscles (genioglossus, hyoglossus, styloglossus, palatoglossus) protrude, retract, depress, and elevate the tongue.',
            'Lingual papillae include filiform (tactile), fungiform, foliate, and circumvallate (rich in taste buds).',
            'Anterior two-thirds taste travels via chorda tympani (CN VII); posterior one-third via glossopharyngeal (CN IX).',
            'Motor innervation to almost all tongue muscles is supplied by the hypoglossal nerve (CN XII).',
          ],
          clinical: {
            diseases: 'Glossitis, oral candidiasis, geographic tongue, leukoplakia, and squamous cell carcinoma.',
            causes: 'Nutritional deficiencies (B12, iron, folate), tobacco/alcohol exposure, fungal overgrowth, or local trauma.',
            symptoms: 'Lingual soreness, erythema, depapillation, white/red mucosal plaques, or dysgeusia.',
            effects: 'Painful mastication, dysphagia, impaired speech articulation, or delayed malignancy detection.',
            prevention: 'Daily oral and tongue hygiene, tobacco/alcohol cessation, balanced micronutrient intake, and dental checkups.',
          },
          hotspots: [
            ['Apex (Tip) of Tongue', 'Ujung Lidah', 'Apex linguae', 'Anterior mobile tip', 'Provides high tactile sensitivity and fine articulatory contact.', 'Rests against the lingual surface of the lower incisor teeth at rest.', [0.0, 0.02, 0.98]],
            ['Dorsum & Filiform Papillae', 'Punggung Lidah', 'Dorsum linguae', 'Superior mucosal surface', 'Provides abrasive friction to grip and manipulate food boluses.', 'Keratinized filiform papillae give the dorsum its velvety texture.', [0.0, 0.28, 0.25]],
            ['Circumvallate Papillae', 'Papila Sirkumvalata', 'Papillae vallatae', 'Anterior to sulcus terminalis', 'Houses numerous taste buds innervated by the glossopharyngeal nerve.', 'Arranged in a V-shaped row of 8–12 large dome-shaped papillae.', [0.0, 0.32, -0.25]],
            ['Lingual Tonsil', 'Tonsil Lingualis', 'Tonsilla lingualis', 'Posterior pharyngeal root', 'Provides mucosal immune surveillance as part of Waldeyer tonsillar ring.', 'Nodular lymphoid aggregations on the posterior one-third of the tongue.', [0.25, 0.18, -0.62]],
            ['Genioglossus & Frenulum', 'Otot Genioglosus & Frenulum', 'Musculus genioglossus', 'Inferior ventral surface', 'Protrudes the tongue and prevents posterior airway collapse.', 'Frenulum linguae tethers the ventral midline to the floor of the mouth.', [0.0, -0.32, -0.15]],
          ],
        }),

        makeSpecimen({
          id: 'lungs',
          name_en: 'Lungs',
          name_id: 'Paru-paru',
          latin: 'Pulmones',
          organ_system: 'Respiratory',
          categories: ['Respiratory', 'Thorax'],
          builder: 'lungs',
          phys_default: 'respiration',
          body_pos: [0, 1.35, 0.02],
          overview_en: 'Paired spongy, elastic organs of respiration occupying the left and right pleural cavities of the thorax, flanking the mediastinum.',
          overview_id: 'Organ pernapasan berpasangan yang elastis dan berongga, menempati rongga pleura kanan dan kiri toraks di samping mediastinum.',
          physiology_en: 'Facilitates alveolar gas exchange (O₂ uptake and CO₂ elimination) across the thin respiratory membrane driven by diaphragmatic and intercostal mechanics.',
          physiology_id: 'Memfasilitasi pertukaran gas alveolar (penyerapan O₂ dan pembuangan CO₂) melintasi membran respirasi yang digerakkan diafragma dan otot interkostal.',
          metrics: [
            { label: 'TOTAL CAPACITY', val: '~6.0 L', sub: 'Adult male/female ~4.2–6.0 L' },
            { label: 'TIDAL VOLUME', val: '~500 mL', sub: 'Quiet resting breath' },
            { label: 'ALVEOLI COUNT', val: '~300–500M', sub: '~70 m² gas exchange area' },
            { label: 'LOBES', val: '3 R / 2 L', sub: 'Cardiac notch on left lung' },
          ],
          learning_points: [
            'The right lung has three lobes (superior, middle, inferior); the left lung has two lobes and a cardiac notch.',
            'Conducting airways branch hierarchically from trachea to primary bronchi, lobar/segmental bronchi, and bronchioles.',
            'Type I alveolar cells form the thin gas-exchange barrier; Type II cells secrete pulmonary surfactant to reduce surface tension.',
            'Visceral and parietal pleurae enclose a negative-pressure pleural cavity preventing alveolar collapse.',
            'Dual blood supply: pulmonary arteries bring deoxygenated blood for gas exchange; bronchial arteries perfuse airway tissue.',
          ],
          clinical: {
            diseases: 'Asthma, chronic obstructive pulmonary disease (COPD), pneumonia, tuberculosis, and pulmonary embolism.',
            causes: 'Tobacco smoke, airborne particulates, respiratory pathogens, allergic airway hyperresponsiveness, or deep vein thrombosis.',
            symptoms: 'Shortness of breath (dyspnea), wheezing, productive or dry cough, pleuritic chest pain, and hypoxemia.',
            effects: 'Impaired alveolar ventilation-perfusion matching, respiratory acidosis, and right ventricular strain (cor pulmonale).',
            prevention: 'Smoke-free lifestyle, clean indoor air, recommended vaccinations (influenza, pneumococcal), and regular aerobic exercise.',
          },
          hotspots: [
            ['Trachea', 'Trakea (Batang Tenggorok)', 'Trachea', 'Midline superior mediastinum', 'Conducts air between larynx and primary bronchi.', 'Reinforced by 16–20 C-shaped hyaline cartilage rings.', [0.0, 1.15, 0.05]],
            ['Right Superior & Middle Lobes', 'Lobus Atas & Tengah Kanan', 'Pulmo dexter', 'Right hemithorax', 'Performs ventilation and gas exchange in right upper/middle zones.', 'Separated by the horizontal and oblique fissures.', [-0.64, 0.35, 0.25]],
            ['Left Superior Lobe & Cardiac Notch', 'Lobus Atas Kiri & Takik Jantung', 'Incisura cardiaca', 'Left anterior hemithorax', 'Accommodates the apex of the heart while ventilating left upper zone.', 'Inferior projection forms the lingula.', [0.64, 0.28, 0.26]],
            ['Primary Bronchi & Hilum', 'Bronkus Utama & Hilus', 'Bronchi principales', 'Medial lung root', 'Entry point for bronchi, pulmonary arteries/veins, and lymphatics.', 'Right main bronchus is wider, shorter, and more vertical than the left.', [-0.26, 0.32, 0.05]],
            ['Alveolar Base & Diaphragmatic Surface', 'Basis Paru & Permukaan Diafragma', 'Basis pulmonis', 'Inferior concave base', 'Rests on the diaphragm dome to maximize inspiratory expansion.', 'Rich in terminal respiratory bronchioles and alveolar sacs.', [0.64, -0.48, 0.15]],
          ],
        }),

        makeSpecimen({
          id: 'liver',
          name_en: 'Liver',
          name_id: 'Hati',
          latin: 'Hepar',
          organ_system: 'Digestive',
          categories: ['Digestive'],
          builder: 'liver',
          phys_default: 'digestion',
          body_pos: [-0.22, 1.02, 0.14],
          overview_en: 'The largest internal solid organ and gland in the human body, situated in the right upper quadrant beneath the diaphragm.',
          overview_id: 'Organ padat dan kelenjar internal terbesar dalam tubuh manusia, terletak di kuadran kanan atas abdomen tepat di bawah diafragma.',
          physiology_en: 'Performs over 500 metabolic functions including bile synthesis, glycogen storage, plasma protein production, and xenobiotic detoxification.',
          physiology_id: 'Menjalankan lebih dari 500 fungsi metabolik termasuk sintesis empedu, penyimpanan glikogen, produksi protein plasma, dan detoksifikasi.',
          metrics: [
            { label: 'ADULT WEIGHT', val: '1,200–1,500 g', sub: 'Largest internal organ' },
            { label: 'BILE OUTPUT', val: '600–1,000 mL/d', sub: 'Emulsifies dietary lipids' },
            { label: 'DUAL BLOOD SUPPLY', val: '75% Portal', sub: '25% Hepatic artery' },
            { label: 'ANATOMICAL LOBES', val: '4 Lobes', sub: 'Right, left, caudate, quadrate' },
          ],
          learning_points: [
            'The falciform ligament divides the liver externally into a larger right lobe and smaller left lobe.',
            'Portal triads in hepatic lobules contain branches of the hepatic portal vein, hepatic artery, and bile duct.',
            'Hepatocytes synthesize albumin, clotting factors, cholesterol, and conjugate bilirubin for biliary excretion.',
            'Kupffer cells lining hepatic sinusoids phagocytose aged erythrocytes and gut-derived pathogens.',
            'The liver possesses remarkable regenerative capacity following partial parenchymal injury.',
          ],
          clinical: {
            diseases: 'Viral hepatitis (A, B, C), metabolic dysfunction-associated steatotic liver disease (MASLD), cirrhosis, and gallstones.',
            causes: 'Hepatotropic viruses, excessive alcohol intake, insulin resistance/obesity, and hepatotoxic drug exposure.',
            symptoms: 'Jaundice (scleral icterus), right upper quadrant discomfort, fatigue, pruritus, ascites, and coagulopathy.',
            effects: 'Portal hypertension, hepatic encephalopathy, hypoalbuminemia, and impaired drug metabolism.',
            prevention: 'Hepatitis A/B vaccination, limiting alcohol, maintaining healthy metabolic weight, and cautious medication dosing.',
          },
          hotspots: [
            ['Right Hepatic Lobe', 'Lobus Hati Kanan', 'Lobus hepatis dexter', 'Right hypochondrium', 'Accounts for ~60% of functional hepatocyte metabolic mass.', 'Molded superiorly to the right dome of the diaphragm.', [-0.48, 0.12, 0.25]],
            ['Left Hepatic Lobe', 'Lobus Hati Kiri', 'Lobus hepatis sinister', 'Epigastric region', 'Extends across midline superior to the anterior stomach wall.', 'Separated from right lobe by the falciform ligament.', [0.58, 0.12, 0.22]],
            ['Falciform Ligament', 'Ligamentum Falsiformis', 'Ligamentum falciforme', 'Anterior midline surface', 'Attaches liver to anterior abdominal wall and diaphragm.', 'Free inferior margin contains the round ligament (ligamentum teres).', [0.08, 0.22, 0.45]],
            ['Gallbladder & Cystic Duct', 'Kantung Empedu', 'Vesica biliaris', 'Visceral fossa of right lobe', 'Stores and concentrates hepatic bile between meals.', 'Contracts in response to cholecystokinin (CCK) to release bile into duodenum.', [-0.32, -0.35, 0.28]],
            ['Porta Hepatis (Hepatic Hilum)', 'Porta Hepatis', 'Porta hepatis', 'Inferior visceral surface', 'Neurovascular gateway for hepatic artery, portal vein, and hepatic ducts.', 'Framed posteriorly by caudate lobe and anteriorly by quadrate lobe.', [0.05, -0.22, -0.22]],
          ],
        }),

        makeSpecimen({
          id: 'stomach',
          name_en: 'Stomach',
          name_id: 'Lambung',
          latin: 'Gaster',
          organ_system: 'Digestive',
          categories: ['Digestive'],
          builder: 'stomach',
          phys_default: 'digestion',
          body_pos: [0.18, 0.98, 0.14],
          overview_en: 'A J-shaped muscular dilation of the gastrointestinal tract located in the epigastric and left hypochondriac regions between the esophagus and duodenum.',
          overview_id: 'Pelebaran saluran cerna berbentuk huruf J yang terletak di regio epigastrium dan hipokondrium kiri di antara esofagus dan duodenum.',
          physiology_en: 'Mechanically churns ingested food into acidic chyme and initiates protein digestion via pepsin and hydrochloric acid.',
          physiology_id: 'Mengaduk makanan secara mekanis menjadi kimus asam dan memulai pencernaan protein melalui enzim pepsin dan asam klorida.',
          metrics: [
            { label: 'CAPACITY', val: '1.0–1.5 L', sub: 'Distensible gastric rugae' },
            { label: 'GASTRIC pH', val: '1.5–3.5', sub: 'Parietal cell HCl secretion' },
            { label: 'MUSCLE LAYERS', val: '3 Layers', sub: 'Longitudinal, circular, oblique' },
            { label: 'EMPTYING TIME', val: '2–4 Hours', sub: 'Regulated by pyloric sphincter' },
          ],
          learning_points: [
            'Four anatomical regions: cardia, fundus, body (corpus), and pyloric part (antrum and canal).',
            'An inner oblique smooth muscle layer enhances mechanical mixing beyond standard circular and longitudinal coats.',
            'Parietal cells secrete HCl and intrinsic factor (essential for vitamin B12 absorption); chief cells secrete pepsinogen.',
            'A bicarbonate-rich mucus barrier protects gastric mucosa from autodigestion.',
            'The pyloric sphincter meters small aliquots of chyme into the duodenal bulb.',
          ],
          clinical: {
            diseases: 'Gastritis, peptic ulcer disease (PUD), gastroesophageal reflux disease (GERD), and gastric adenocarcinoma.',
            causes: 'Helicobacter pylori infection, chronic NSAID use, smoking, excessive alcohol, and bile reflux.',
            symptoms: 'Epigastric burning pain, early satiety, nausea, postprandial bloating, heartburn, or melena.',
            effects: 'Mucosal erosion, iron-deficiency anemia, upper GI bleeding, or gastric outlet obstruction.',
            prevention: 'Prompt H. pylori eradication when indicated, judicious NSAID use, balanced meals, and avoiding smoking.',
          },
          hotspots: [
            ['Cardia & Lower Esophageal Sphincter', 'Kardia Lambung', 'Pars cardiaca', 'Esophagogastric junction', 'Regulates bolus entry from esophagus and prevents acid reflux.', 'Surrounded by cardiac glands secreting protective mucus.', [-0.15, 0.65, 0.05]],
            ['Gastric Fundus', 'Fundus Lambung', 'Fundus gastricus', 'Superior dome left of cardia', 'Accumulates swallowed gases and stores food temporarily.', 'Abuts the left dome of the diaphragm.', [0.32, 0.62, 0.04]],
            ['Body & Gastric Rugae', 'Badan Lambung & Rugae', 'Corpus gastricum', 'Central main chamber', 'Primary site of acid/pepsin secretion and mechanical churning.', 'Internal mucosal folds (rugae) flatten as the stomach distends.', [0.28, 0.05, 0.32]],
            ['Greater & Lesser Curvatures', 'Kurvatura Mayor & Minor', 'Curvatura major', 'Lateral and medial borders', 'Anchor greater and lesser omenta and carry gastroepiploic/gastric vessels.', 'Greater curvature forms the convex left/inferior border.', [0.45, -0.28, 0.15]],
            ['Pyloric Antrum & Sphincter', 'Antrum & Sfingter Pilorus', 'Pylorus', 'Distal gastroduodenal junction', 'Grinds solids and regulates metered emptying of chyme into duodenum.', 'Thickened circular smooth muscle ring forms the pyloric sphincter.', [-0.55, -0.38, 0.08]],
          ],
        }),

        makeSpecimen({
          id: 'pancreas',
          name_en: 'Pancreas',
          name_id: 'Pankreas',
          latin: 'Pancreas',
          organ_system: 'Digestive',
          categories: ['Digestive'],
          builder: 'pancreas',
          phys_default: 'digestion',
          body_pos: [0.05, 0.90, 0.04],
          overview_en: 'A retroperitoneal elongated lobulated gland spanning transversely from the C-loop of the duodenum to the splenic hilum.',
          overview_id: 'Kelenjar memanjang berlobus di ruang retroperitoneal yang membentang melintang dari lengkung duodenum hingga hilus limpa.',
          physiology_en: 'Functions as a dual exocrine digestive gland (secreting amylase, lipase, proteases, and bicarbonate) and endocrine regulator (insulin and glucagon).',
          physiology_id: 'Berfungsi ganda sebagai kelenjar eksokrin pencernaan (amilase, lipase, protease, bikarbonat) dan regulator endokrin (insulin dan glukagon).',
          metrics: [
            { label: 'LENGTH', val: '15–20 cm', sub: 'Retroperitoneal transverse span' },
            { label: 'EXOCRINE SHARE', val: '~98–99%', sub: 'Acinar & ductal juice (~1.5 L/d)' },
            { label: 'ISLETS OF LANGERHANS', val: '~1–2 Million', sub: 'Alpha, beta, delta endocrine cells' },
            { label: 'MAIN DUCT', val: 'Wirsung Duct', sub: 'Joins bile duct at ampulla of Vater' },
          ],
          learning_points: [
            'Divided into head (with uncinate process), neck, body, and tail abutting the spleen.',
            'Acinar cells secrete inactive zymogens (trypsinogen, chymotrypsinogen) activated safely inside the duodenal lumen.',
            'Ductal cells secrete alkaline HCO₃⁻ to neutralize acidic gastric chyme.',
            'Pancreatic islet beta cells secrete insulin to lower blood glucose; alpha cells secrete glucagon to raise it.',
            'The main pancreatic duct joins the common bile duct at the hepatopancreatic ampulla (of Vater).',
          ],
          clinical: {
            diseases: 'Type 1 and Type 2 diabetes mellitus, acute and chronic pancreatitis, and pancreatic ductal adenocarcinoma.',
            causes: 'Gallstone duct obstruction, heavy alcohol use, autoimmune beta-cell destruction, or metabolic insulin resistance.',
            symptoms: 'Severe epigastric pain radiating to the back, steatorrhea, hyperglycemia, polyuria, and unintentional weight loss.',
            effects: 'Malabsorption of fats/fat-soluble vitamins, systemic microvascular complications, and autodigestive tissue necrosis.',
            prevention: 'Healthy glycemic and lipid control, alcohol moderation, smoking cessation, and balanced physical activity.',
          },
          hotspots: [
            ['Head of Pancreas', 'Kepala Pankreas', 'Caput pancreatis', 'Nestled in duodenal C-loop', 'Collects converging pancreatic ducts and surrounds distal bile duct.', 'Includes the hook-like uncinate process posterior to superior mesenteric vessels.', [-0.62, -0.18, 0.12]],
            ['Neck of Pancreas', 'Leher Pankreas', 'Collum pancreatis', 'Anterior to portal vein formation', 'Bridges the pancreatic head and body over major mesenteric vessels.', 'Superior mesenteric vein and splenic vein unite posterior to the neck.', [-0.28, -0.05, 0.15]],
            ['Body of Pancreas', 'Badan Pankreas', 'Corpus pancreatis', 'Crosses L1–L2 vertebra', 'Synthesizes digestive enzymes and endocrine hormones.', 'Anterior surface forms part of the stomach bed.', [0.15, 0.08, 0.14]],
            ['Tail of Pancreas', 'Ekor Pankreas', 'Cauda pancreatis', 'Intraperitoneal in splenorenal ligament', 'Rich in endocrine islets of Langerhans; extends to splenic hilum.', 'Closely related to splenic artery and vein.', [0.68, 0.22, -0.04]],
            ['Main Pancreatic Duct', 'Duktus Pankreatikus Utama', 'Ductus pancreaticus', 'Traverses full gland length', 'Delivers bicarbonate and enzyme-rich pancreatic juice into duodenum.', 'Opens at the major duodenal papilla guarded by the sphincter of Oddi.', [-0.15, -0.04, 0.22]],
          ],
        }),

        makeSpecimen({
          id: 'kidneys',
          name_en: 'Kidneys',
          name_id: 'Ginjal',
          latin: 'Renes',
          organ_system: 'Urinary',
          categories: ['Urinary'],
          builder: 'kidneys',
          phys_default: 'blood',
          body_pos: [0, 0.85, -0.06],
          overview_en: 'Paired bean-shaped retroperitoneal organs flanking the T12–L3 vertebral column, with the right kidney slightly lower due to the liver.',
          overview_id: 'Organ retroperitoneal berpasangan berbentuk kacang di samping tulang belakang T12–L3, dengan ginjal kanan sedikit lebih rendah karena hati.',
          physiology_en: 'Filters blood plasma through millions of nephrons to regulate fluid volume, electrolyte balance, acid-base pH, blood pressure (renin), and erythropoiesis (EPO).',
          physiology_id: 'Menyaring plasma darah melalui jutaan nefron untuk mengatur volume cairan, elektrolit, pH asam-basa, tekanan darah (renin), dan eritropoiesis (EPO).',
          metrics: [
            { label: 'NEPHRONS', val: '~1.0–1.3M / kidney', sub: 'Functional filtration units' },
            { label: 'NORMAL GFR', val: '90–120 mL/min', sub: 'Glomerular filtration rate' },
            { label: 'URINE OUTPUT', val: '1.0–2.0 L/day', sub: 'Concentrated from ~180 L filtrate' },
            { label: 'RENAL BLOOD FLOW', val: '~20–25% CO', sub: '~1,100 mL/min total' },
          ],
          learning_points: [
            'Internal parenchyma consists of an outer renal cortex and inner renal medulla organized into renal pyramids.',
            'Each nephron comprises a renal corpuscle (glomerulus + Bowman capsule) and renal tubule (PCT, loop of Henle, DCT).',
            'Urine drains from renal papillae into minor calyces, major calyces, renal pelvis, and ureters.',
            'Juxtaglomerular apparatus secretes renin to activate the renin-angiotensin-aldosterone system (RAAS).',
            'Cortical peritubular cells secrete erythropoietin (EPO) in response to hypoxia and activate vitamin D (calcitriol).',
          ],
          clinical: {
            diseases: 'Chronic kidney disease (CKD), nephrolithiasis (kidney stones), pyelonephritis, glomerulonephritis, and acute kidney injury.',
            causes: 'Diabetic nephropathy, uncontrolled hypertension, dehydration, urinary tract obstruction, or nephrotoxic medications.',
            symptoms: 'Flank colicky pain, hematuria, foamy proteinuric urine, periorbital/pedal edema, and fatigue.',
            effects: 'Uremic toxin accumulation, hyperkalemia, metabolic acidosis, renal anemia, and secondary hyperparathyroidism.',
            prevention: 'Adequate daily hydration, blood pressure and blood glucose control, moderate sodium intake, and avoiding NSAID overuse.',
          },
          hotspots: [
            ['Renal Cortex', 'Korteks Ginjal', 'Cortex renalis', 'Outer parenchymal layer', 'Houses renal corpuscles and convoluted tubules for filtration and reabsorption.', 'Projects inward between pyramids as renal columns.', [-0.62, 0.22, 0.16]],
            ['Renal Medulla & Pyramids', 'Medula & Piramida Ginjal', 'Medulla renalis', 'Inner striated cone zones', 'Maintains corticomedullary osmotic gradient via loops of Henle.', 'Apices form renal papillae draining into minor calyces.', [-0.48, -0.05, 0.18]],
            ['Renal Pelvis & Calyces', 'Pelvis Renalis & Kaliks', 'Pelvis renalis', 'Funnel-shaped sinus cavity', 'Collects urine from major calyces and funnels it into the ureter.', 'Lined by stretch-tolerant transitional epithelium (urothelium).', [-0.34, -0.02, 0.12]],
            ['Renal Artery & Vein', 'Arteri & Vena Renalis', 'Arteria et Vena renalis', 'Medial renal hilum', 'Delivers high-pressure arterial blood for filtration and returns filtered venous blood.', 'Renal veins drain directly into the inferior vena cava.', [0.08, 0.12, 0.08]],
            ['Ureter', 'Ureter', 'Ureter', 'Descending retroperitoneal duct', 'Propels urine from renal pelvis to urinary bladder via peristalsis.', 'Courses inferiorly along the anterior surface of the psoas major muscle.', [0.42, -0.62, 0.06]],
          ],
        }),

        makeSpecimen({
          id: 'small_intestine',
          name_en: 'Small intestine',
          name_id: 'Usus halus',
          latin: 'Intestinum tenue',
          organ_system: 'Digestive',
          categories: ['Digestive'],
          builder: 'small_intestine',
          phys_default: 'digestion',
          body_pos: [0, 0.65, 0.14],
          overview_en: 'A coiled 6-meter tubular organ extending from the pyloric sphincter to the ileocecal valve, comprising the duodenum, jejunum, and ileum.',
          overview_id: 'Organ saluran berliku sepanjang ±6 meter dari sfingter pilorus hingga katup ileosekal, terdiri atas duodenum, jejunum, dan ileum.',
          physiology_en: 'Completes enzymatic chemical digestion and absorbs ~90% of nutrients, water, and electrolytes across specialized villi and microvilli.',
          physiology_id: 'Menyelesaikan pencernaan kimiawi enzimatik dan menyerap ±90% nutrisi, air, serta elektrolit melalui vili dan mikrovili.',
          metrics: [
            { label: 'AVERAGE LENGTH', val: '5.5–6.5 m', sub: 'Duodenum, jejunum, ileum' },
            { label: 'SURFACE AREA', val: '~30–32 m²', sub: 'Plicae, villi, microvilli' },
            { label: 'ABSORPTION SHARE', val: '~90%', sub: 'Macronutrients & water' },
            { label: 'TRANSIT TIME', val: '3–5 Hours', sub: 'Segmentation & peristalsis' },
          ],
          learning_points: [
            'Circular folds (plicae circulares), mucosal villi, and enterocyte brush-border microvilli amplify absorptive area.',
            'The C-shaped duodenum receives pancreatic enzymes and bile via the hepatopancreatic ampulla.',
            'The jejunum features thick walls, prominent plicae, and long vasa recta for maximal nutrient absorption.',
            'The ileum contains aggregated lymphoid nodules (Peyer patches) and absorbs vitamin B12 and bile salts.',
            'Lacteal lymphatic capillaries within each villus absorb dietary chylomicrons.',
          ],
          clinical: {
            diseases: 'Celiac disease, Crohn disease, small bowel obstruction, gastroenteritis, and malabsorption syndromes.',
            causes: 'Autoimmune gluten sensitivity, transmural IBD inflammation, postoperative adhesions, or enteric pathogens.',
            symptoms: 'Periumbilical cramping, osmotic diarrhea, steatorrhea, abdominal distension, and micronutrient deficiencies.',
            effects: 'Weight loss, iron/B12 anemia, electrolyte depletion, and compromised mucosal barrier integrity.',
            prevention: 'Safe food/water hygiene, targeted dietary management (e.g. gluten-free in celiac), and adequate hydration.',
          },
          hotspots: [
            ['Duodenum (C-Loop)', 'Duodenum', 'Duodenum', 'Retroperitoneal proximal segment', 'Neutralizes gastric acid and mixes chyme with bile and pancreatic enzymes.', 'Subdivided into superior, descending, horizontal, and ascending parts.', [-0.28, 0.52, 0.14]],
            ['Jejunum', 'Jejunum (Usus Kosong)', 'Jejunum', 'Upper-left intraperitoneal coils', 'Primary site of carbohydrate, amino acid, and lipid absorption.', 'Characterized by deep red vascularity and tall plicae circulares.', [0.35, 0.22, 0.24]],
            ['Ileum', 'Ileum (Usus Penyerapan)', 'Ileum', 'Lower-right intraperitoneal coils', 'Absorbs vitamin B12, intrinsic factor complexes, and conjugated bile salts.', 'Contains abundant gut-associated lymphoid tissue (Peyer patches).', [-0.28, -0.28, 0.24]],
            ['Mesentery & Superior Mesenteric Vessels', 'Mesenterium', 'Mesenterium', 'Fan-shaped peritoneal fold', 'Suspends jejunum and ileum from posterior abdominal wall and carries vessels.', 'Prevents intestinal torsion while permitting peristaltic mobility.', [0.05, 0.02, -0.15]],
            ['Ileocecal Junction', 'Katup Ileosekal', 'Ostium ileale', 'Right iliac fossa', 'Regulates chyme entry into cecum and limits colonic bacterial reflux.', 'Formed by thickened smooth muscle lips protruding into the cecum.', [-0.36, -0.48, 0.14]],
          ],
        }),

        makeSpecimen({
          id: 'large_intestine',
          name_en: 'Large intestine',
          name_id: 'Usus besar',
          latin: 'Intestinum crassum',
          organ_system: 'Digestive',
          categories: ['Digestive'],
          builder: 'large_intestine',
          phys_default: 'digestion',
          body_pos: [0, 0.68, 0.12],
          overview_en: 'A 1.5-meter frame-like terminal segment of the GI tract surrounding the small intestine, comprising the cecum, appendix, colon, rectum, and anal canal.',
          overview_id: 'Segmen terminal saluran cerna sepanjang ±1,5 meter yang membingkai usus halus, meliputi sekum, apendiks, kolon, rektum, dan kanalis analis.',
          physiology_en: 'Reabsorbs residual water and electrolytes, hosts symbiotic gut microbiota producing vitamins K and B, and compacts feces for elimination.',
          physiology_id: 'Menyerap kembali sisa air dan elektrolit, menjadi habitat mikrobiota usus penghasil vitamin K dan B, serta memadatkan feses.',
          metrics: [
            { label: 'AVERAGE LENGTH', val: '~1.5 m', sub: 'Wider diameter than small bowel' },
            { label: 'WATER RECOVERY', val: '~1.0–1.5 L/d', sub: 'Solidifies luminal contents' },
            { label: 'MICROBIOME', val: '>10¹³ Microbes', sub: 'Synthesizes SCFAs & Vit K' },
            { label: 'TRANSIT TIME', val: '12–48 Hours', sub: 'Haustral churning & mass movements' },
          ],
          learning_points: [
            'Distinctive macroscopic features include teniae coli (three longitudinal muscle bands), haustra, and epiploic appendages.',
            'The colon consists of ascending, transverse, descending, and sigmoid segments.',
            'Goblet cells secrete abundant lubricating mucus to ease passage of dehydrated fecal matter.',
            'Fermentation of dietary fiber by commensal bacteria yields beneficial short-chain fatty acids (butyrate).',
            'Mass peristaltic movements triggered by the gastrocolic reflex propel feces into the rectum.',
          ],
          clinical: {
            diseases: 'Colorectal polyps and adenocarcinoma, ulcerative colitis, diverticulitis, appendicitis, and irritable bowel syndrome.',
            causes: 'Low-fiber diet, processed meat intake, chronic mucosal inflammation, luminal appendiceal obstruction, or genetic risk.',
            symptoms: 'Altered bowel habits, hematochezia, lower abdominal pain, tenesmus, or unexplained iron-deficiency anemia.',
            effects: 'Fluid/electrolyte imbalance, bowel perforation or peritonitis in acute inflammation, or neoplastic obstruction.',
            prevention: 'High-fiber whole-plant diet, regular hydration, physical activity, and age-appropriate colorectal screening.',
          },
          hotspots: [
            ['Cecum & Vermiform Appendix', 'Sekum & Apendiks', 'Caecum et Appendix', 'Right iliac fossa', 'Receives ileal chyme; appendix serves as lymphoid/microbial reservoir.', 'McBurney point marks the classic surface projection of the appendix base.', [-0.62, -0.68, 0.18]],
            ['Ascending Colon', 'Kolon Asendens', 'Colon ascendens', 'Right lateral abdomen', 'Absorbs water and electrolytes as contents ascend to right colic flexure.', 'Secondarily retroperitoneal along the right paracolic gutter.', [-0.68, 0.08, 0.12]],
            ['Transverse Colon', 'Kolon Transversum', 'Colon transversum', 'Upper-middle abdomen', 'Spans from hepatic flexure to splenic flexure suspended by transverse mesocolon.', 'Most mobile intraperitoneal segment of the large intestine.', [0.02, 0.56, 0.24]],
            ['Descending Colon', 'Kolon Desendens', 'Colon descendens', 'Left lateral abdomen', 'Stores and progressively dehydrates fecal residue toward the pelvis.', 'Secondarily retroperitoneal down the left paracolic gutter.', [0.68, 0.06, 0.12]],
            ['Sigmoid Colon & Rectosigmoid Junction', 'Kolon Sigmoid', 'Colon sigmoideum', 'Left iliac fossa to S3', 'S-shaped reservoir regulating controlled fecal delivery into the rectum.', 'Possesses a mobile mesentery (sigmoid mesocolon).', [0.32, -0.62, 0.16]],
          ],
        }),

        makeSpecimen({
          id: 'spleen',
          name_en: 'Spleen',
          name_id: 'Limpa',
          latin: 'Splen / Lien',
          organ_system: 'Cardiovascular',
          categories: ['Cardiovascular', 'Thorax'],
          builder: 'spleen',
          phys_default: 'blood',
          body_pos: [0.35, 1.02, -0.05],
          overview_en: 'The largest secondary lymphoid organ in the body, tucked beneath the left 9th–11th ribs in the left hypochondriac region.',
          overview_id: 'Organ limfoid sekunder terbesar dalam tubuh yang terlindung di bawah tulang rusuk ke-9 hingga ke-11 di regio hipokondrium kiri.',
          physiology_en: 'Filters bloodborne pathogens via white pulp immune surveillance and removes senescent erythrocytes and platelets via red pulp macrophages.',
          physiology_id: 'Menyaring patogen dalam darah melalui pulpa putih serta menyingkirkan sel darah merah dan trombosit tua melalui makrofag pulpa merah.',
          metrics: [
            { label: 'ADULT WEIGHT', val: '150–200 g', sub: 'Fist-sized lymphoid organ' },
            { label: 'RIB PROTECTION', val: 'Ribs 9–11', sub: 'Left midaxillary line' },
            { label: 'PLATELET RESERVE', val: '~30% Pool', sub: 'Stored in red pulp cords' },
            { label: 'PULP ZONES', val: 'White & Red', sub: 'Immune vs erythrocyte filtration' },
          ],
          learning_points: [
            'White pulp consists of periarteriolar lymphoid sheaths (T cells) and lymphoid follicles (B cells) around central arterioles.',
            'Red pulp contains splenic cords (of Billroth) and venous sinusoids that cull rigid, aged red blood cells.',
            'Recycles hemoglobin iron back to transferrin and converts heme to bilirubin.',
            'Peritoneal ligaments (gastrosplenic and splenorenal) anchor the spleen while permitting respiratory excursion.',
            'A thin fibroelastic capsule makes the spleen vulnerable to blunt left-upper-quadrant trauma.',
          ],
          clinical: {
            diseases: 'Splenomegaly, splenic rupture (blunt trauma), hypersplenism, and functional hyposplenism.',
            causes: 'Portal hypertension, hematologic malignancies, infectious mononucleosis, malaria, or high-impact trauma.',
            symptoms: 'Left upper quadrant fullness/pain, referred left shoulder pain (Kehr sign), early satiety, or cytopenias.',
            effects: 'Increased susceptibility to encapsulated bacteria (Streptococcus pneumoniae, Neisseria meningitidis) post-splenectomy.',
            prevention: 'Protective gear in contact sports, vaccination against encapsulated organisms if asplenic, and treating underlying liver/blood disorders.',
          },
          hotspots: [
            ['Diaphragmatic Surface', 'Permukaan Diafragmatika', 'Facies diaphragmatica', 'Convex posterolateral aspect', 'Conforms smoothly to the inferior concavity of the left hemidiaphragm.', 'Separated from ribs 9–11 by the costodiaphragmatic recess.', [0.28, 0.25, -0.25]],
            ['Superior Notched Border', 'Tepi Atas Bertakik', 'Margo superior', 'Anterosuperior margin', 'Clinical palpation landmark bearing characteristic fetal lobulation notches.', 'Becomes palpable below left costal margin during splenomegaly.', [0.12, 0.48, 0.25]],
            ['Splenic Hilum', 'Hilus Limpa', 'Hilum splenicum', 'Medial visceral surface', 'Entry/exit site for tortuous splenic artery, splenic vein, and lymphatics.', 'Closely related to the tail of the pancreas.', [-0.28, 0.0, 0.22]],
            ['White Pulp (Immune Nodules)', 'Pulpa Putih', 'Pulpa alba', 'Periarteriolar lymphoid tissue', 'Mounts adaptive B- and T-lymphocyte responses against bloodborne antigens.', 'Surrounds central arterioles branching from trabecular arteries.', [0.05, 0.12, 0.25]],
            ['Red Pulp (Sinusoids & Cords)', 'Pulpa Merah', 'Pulpa rubra', 'Parenchymal filtration matrix', 'Phagocytoses aged erythrocytes and stores reserve platelets.', 'Filters blood slowly through fenestrated splenic sinusoids.', [-0.12, -0.35, 0.22]],
          ],
        }),

        makeSpecimen({
          id: 'skin',
          name_en: 'Skin',
          name_id: 'Kulit',
          latin: 'Cutis / Integumentum commune',
          organ_system: 'Integumentary',
          categories: ['Integumentary'],
          builder: 'skin',
          phys_default: 'nervous',
          body_pos: [0.38, 1.35, 0.18],
          overview_en: 'The largest organ of the human body by surface area and mass, forming a multi-layered waterproof barrier interface with the external environment.',
          overview_id: 'Organ terbesar tubuh manusia berdasarkan luas permukaan dan massa, membentuk sawar berlapis kedap air terhadap lingkungan luar.',
          physiology_en: 'Protects against microbial, UV, and mechanical injury, regulates core temperature via sweat and vasomotion, synthesizes vitamin D₃, and transduces somatosensation.',
          physiology_id: 'Melindungi dari mikroba, sinar UV, dan cedera mekanis, mengatur suhu tubuh melalui keringat dan aliran darah, menyintesis vitamin D₃, serta menerima rangsang sentuh.',
          metrics: [
            { label: 'SURFACE AREA', val: '1.5–2.0 m²', sub: 'Adult external coverage' },
            { label: 'TOTAL MASS', val: '~15% Body Wt', sub: 'Heaviest organ system' },
            { label: 'TURNOVER CYCLE', val: '~28–40 Days', sub: 'Basal to stratum corneum' },
            { label: 'MAIN LAYERS', val: '3 Tiers', sub: 'Epidermis, Dermis, Hypodermis' },
          ],
          learning_points: [
            'The epidermis is stratified squamous keratinized epithelium containing keratinocytes, melanocytes, Langerhans, and Merkel cells.',
            'The dermis comprises papillary loose connective tissue and reticular dense irregular collagen/elastin fibers.',
            'Eccrine sweat glands mediate evaporative thermoregulation; sebaceous glands secrete protective sebum.',
            'Cutaneous mechanoreceptors (Meissner, Pacinian, Ruffini, Merkel) encode touch, pressure, and vibration.',
            'UVB radiation converts 7-dehydrocholesterol in epidermal keratinocytes into cholecalciferol (vitamin D₃).',
          ],
          clinical: {
            diseases: 'Atopic dermatitis (eczema), psoriasis, acne vulgaris, cellulitis, and skin cancers (basal cell, squamous cell, melanoma).',
            causes: 'Ultraviolet radiation, genetic barrier mutations, immune dysregulation, bacterial/fungal invasion, or thermal burns.',
            symptoms: 'Erythema, pruritus, scaling plaques, vesicles, ulceration, or asymmetric pigmented lesions (ABCDE criteria).',
            effects: 'Barrier fluid loss, thermoregulatory failure, secondary systemic infection, or metastatic malignancy.',
            prevention: 'Broad-spectrum sun protection, gentle skin hydration, wound antisepsis, and regular mole surveillance.',
          },
          hotspots: [
            ['Epidermis & Stratum Corneum', 'Epidermis', 'Epidermis', 'Superficial avascular layer', 'Forms waterproof keratinized barrier and houses UV-absorbing melanocytes.', 'Five strata in thick skin: basale, spinosum, granulosum, lucidum, corneum.', [0.0, 0.54, 0.35]],
            ['Dermis (Papillary & Reticular)', 'Dermis', 'Dermis / Corium', 'Middle connective tissue layer', 'Provides tensile strength, elasticity, capillary nutrition, and sensory endings.', 'Interlocks with epidermis via dermal papillae.', [0.35, 0.12, 0.35]],
            ['Hair Follicle & Arrector Pili', 'Folikel Rambut', 'Folliculus pili', 'Dermal invagination', 'Produces hair shafts and elevates hair during cold or sympathetic arousal.', 'Houses epithelial stem cells critical for wound re-epithelialization.', [-0.36, 0.42, 0.14]],
            ['Sebaceous & Eccrine Sweat Glands', 'Kelenjar Keringat & Sebasea', 'Glandulae sudoriferae', 'Reticular dermis & border', 'Secretes sebum to lubricate skin and sweat for evaporative cooling.', 'Eccrine ducts open directly onto epidermal sweat pores.', [0.42, -0.05, 0.28]],
            ['Hypodermis (Subcutis)', 'Hipodermis (Subkutis)', 'Tela subcutanea', 'Deepest adipose layer', 'Insulates against heat loss, cushions impact, and stores triglycerides.', 'Anchors skin loosely to underlying deep fascia.', [0.0, -0.36, 0.35]],
          ],
        }),

        makeSpecimen({
          id: 'spine',
          name_en: 'Spine',
          name_id: 'Tulang belakang',
          latin: 'Columna vertebralis',
          organ_system: 'Musculoskeletal',
          categories: ['Musculoskeletal', 'Nervous System & Special Senses'],
          builder: 'spine',
          phys_default: 'nervous',
          body_pos: [0, 1.25, -0.14],
          overview_en: 'An articulated axial column of 33 vertebrae (24 presacral movable + fused sacrum and coccyx) cushioned by fibrocartilaginous intervertebral discs.',
          overview_id: 'Kolom aksial beruas yang terdiri atas 33 vertebra (24 bergerak + sakrum dan koksiks menyatu) dengan bantalan diskus intervertebralis.',
          physiology_en: 'Supports head and trunk axial loads, enables multi-planar flexibility, and encases the spinal cord and emerging spinal nerve roots.',
          physiology_id: 'Menopang beban aksial kepala dan batang tubuh, memungkinkan fleksibilitas multi-bidang, serta melindungi sumsum tulang belakang.',
          metrics: [
            { label: 'VERTEBRAE', val: '33 Bones', sub: '7 C, 12 T, 5 L, 5 S, 4 Co' },
            { label: 'PHYSIOLOGIC CURVES', val: '4 Curves', sub: 'Cervical/Lumbar lordosis' },
            { label: 'DISC COMPOSITION', val: 'Annulus + Nucleus', sub: 'Hydrostatic shock absorber' },
            { label: 'SPINAL NERVES', val: '31 Pairs', sub: 'Exit intervertebral foramina' },
          ],
          learning_points: [
            'Four sagittal curves (cervical lordosis, thoracic kyphosis, lumbar lordosis, sacral kyphosis) distribute axial shock.',
            'Intervertebral discs consist of a tough outer annulus fibrosus surrounding a hydrated nucleus pulposus.',
            'Vertebral bodies increase in size inferiorly from C3 to L5 to bear progressively greater weight.',
            'The vertebral foramen of stacked vertebrae forms the protective vertebral canal for the spinal cord.',
            'Ligamenta flava, anterior/posterior longitudinal ligaments, and facet joints stabilize intersegmental motion.',
          ],
          clinical: {
            diseases: 'Intervertebral disc herniation, lumbar spondylosis, spinal stenosis, scoliosis, and vertebral compression fractures.',
            causes: 'Degenerative disc dehydration, improper heavy lifting mechanics, osteoporosis, or congenital asymmetry.',
            symptoms: 'Axial neck or low back pain, radicular sciatica, paresthesia, myotomal weakness, or neurogenic claudication.',
            effects: 'Nerve root compression, restricted spinal mobility, or spinal cord myelopathy in severe canal narrowing.',
            prevention: 'Core and paraspinal muscle strengthening, ergonomic posture, safe lifting technique, and bone density maintenance.',
          },
          hotspots: [
            ['Cervical Spine (C1–C7)', 'Vertebra Servikalis', 'Vertebrae cervicales', 'Neck region', 'Supports cranium and allows wide rotation (atlas C1 and axis C2).', 'Distinguished by transverse foramina transmitting vertebral arteries.', [0.0, 0.85, 0.12]],
            ['Thoracic Spine (T1–T12)', 'Vertebra Torakalis', 'Vertebrae thoracicae', 'Upper/mid back', 'Articulates with 12 pairs of ribs to form the protective thoracic cage.', 'Features long downward-sloping spinous processes and costal facets.', [0.0, 0.35, -0.05]],
            ['Lumbar Spine (L1–L5)', 'Vertebra Lumbalis', 'Vertebrae lumbales', 'Lower back', 'Bears greatest upper-body compressive load with massive kidney-shaped bodies.', 'Sagittal facet orientation favors flexion and extension.', [0.0, -0.25, 0.12]],
            ['Intervertebral Disc', 'Diskus Intervertebralis', 'Discus intervertebralis', 'Between adjacent vertebral bodies', 'Absorbs compressive shock and allows controlled intervertebral motion.', 'Hydrated nucleus pulposus redistributes axial pressure radially.', [0.16, -0.05, 0.18]],
            ['Sacrum & Coccyx', 'Sakrum & Tulang Ekor', 'Os sacrum et Coccyx', 'Posterior pelvic wedge', 'Transmits axial spine weight across sacroiliac joints to the pelvic girdle.', 'Formed by five fused sacral vertebrae and four fused coccygeal segments.', [0.0, -0.88, -0.05]],
          ],
        }),

        makeSpecimen({
          id: 'skeletal_system',
          name_en: 'Skeletal system',
          name_id: 'Sistem rangka',
          latin: 'Systema skeletale',
          organ_system: 'Musculoskeletal',
          categories: ['Musculoskeletal'],
          builder: 'skeletal',
          phys_default: 'blood',
          body_pos: [0, 1.15, 0],
          overview_en: 'The internal osteocartilaginous framework of 206 adult bones divided into axial (skull, spine, thoracic cage) and appendicular (limbs, girdles) divisions.',
          overview_id: 'Kerangka osteokartilaginosa internal yang terdiri atas 206 tulang dewasa, terbagi menjadi rangka aksial dan rangka apendikular.',
          physiology_en: 'Provides structural leverage for locomotion, shields vital viscera, houses hematopoietic red bone marrow, and stores 99% of body calcium and phosphorus.',
          physiology_id: 'Memberikan tuas struktural untuk gerak, melindungi organ vital, menampung sumsum tulang merah hematopoietik, dan menyimpan 99% kalsium tubuh.',
          metrics: [
            { label: 'ADULT BONES', val: '206 Bones', sub: '80 Axial + 126 Appendicular' },
            { label: 'CALCIUM STORE', val: '~99% Body Ca²⁺', sub: 'Hydroxyapatite mineral matrix' },
            { label: 'HEMATOPOIESIS', val: 'Red Marrow', sub: 'RBCs, WBCs, and platelets' },
            { label: 'REMODELING', val: '~10% / Year', sub: 'Osteoblast vs Osteoclast balance' },
          ],
          learning_points: [
            'Bone tissue comprises compact cortical bone (osteons/Haversian systems) and trabecular spongy bone.',
            'Osteoblasts deposit osteoid matrix, osteocytes maintain mechanosensation, and osteoclasts resorb bone.',
            'Endochondral ossification lengthens long bones at epiphyseal growth plates until skeletal maturity.',
            'Synovial joints feature articular cartilage, joint capsule, and lubricating synovial fluid.',
            'Parathyroid hormone (PTH) and calcitonin tightly regulate serum calcium via bone remodeling.',
          ],
          clinical: {
            diseases: 'Osteoporosis, osteoarthritis, fractures, osteomalacia/rickets, and osteomyelitis.',
            causes: 'Postmenopausal estrogen decline, aging, vitamin D/calcium deficiency, mechanical trauma, or joint wear.',
            symptoms: 'Bone pain, fragility fractures (hip, wrist, spine), joint stiffness, crepitus, or postural height loss.',
            effects: 'Impaired mobility, chronic pain, loss of independence, and systemic mineral imbalance.',
            prevention: 'Weight-bearing resistance exercise, adequate calcium and vitamin D intake, fall prevention, and smoking cessation.',
          },
          hotspots: [
            ['Cranium & Facial Skeleton', 'Tengkorak', 'Cranium', 'Superior axial skeleton', 'Encloses and protects the brain and houses special sense organs.', 'Joined by immovable fibrous sutures except the temporomandibular joint.', [0.0, 1.02, 0.14]],
            ['Thoracic Cage (Ribs & Sternum)', 'Rangka Dada', 'Cavea thoracis', 'Thoracic wall', 'Protects heart and lungs while expanding dynamically during inspiration.', '12 pairs of ribs (7 true, 3 false, 2 floating) articulate with sternum and spine.', [0.22, 0.42, 0.22]],
            ['Pelvic Girdle', 'Gelang Panggul', 'Cingulum pelvicum', 'Inferior trunk base', 'Transfers upper body weight to lower limbs and protects pelvic viscera.', 'Formed by paired hip bones (ilium, ischium, pubis), sacrum, and coccyx.', [-0.28, -0.05, 0.18]],
            ['Femur (Thigh Bone)', 'Tulang Paha', 'Femur', 'Proximal lower limb', 'Longest and strongest bone in the human body supporting stance and gait.', 'Articulates proximally at hip acetabulum and distally at knee joint.', [0.24, -0.55, 0.08]],
            ['Humerus & Upper Limb', 'Tulang Lengan Atas', 'Humerus', 'Proximal upper limb', 'Provides wide multi-axial reach at the glenohumeral shoulder joint.', 'Articulates distally with radius and ulna at the elbow.', [-0.46, 0.32, 0.05]],
          ],
        }),

        makeSpecimen({
          id: 'muscular_system',
          name_en: 'Muscular system',
          name_id: 'Sistem otot',
          latin: 'Systema musculare',
          organ_system: 'Musculoskeletal',
          categories: ['Musculoskeletal'],
          builder: 'muscular',
          phys_default: 'nervous',
          body_pos: [0, 1.15, 0.05],
          overview_en: 'Over 600 skeletal muscles attached to bones via tendons, complemented by cardiac and visceral smooth muscle tissues.',
          overview_id: 'Lebih dari 600 otot rangka yang melekat pada tulang melalui tendon, dilengkapi jaringan otot jantung dan otot polos viseral.',
          physiology_en: 'Converts ATP chemical energy into mechanical tension via actin-myosin cross-bridge cycling to drive locomotion, posture, venous return, and thermogenesis.',
          physiology_id: 'Mengubah energi kimia ATP menjadi gaya mekanis melalui siklus jembatan silang aktin-miosin untuk gerak, postur, aliran balik vena, dan termogenesis.',
          metrics: [
            { label: 'SKELETAL MUSCLES', val: '>600 Muscles', sub: 'Voluntary striated fibers' },
            { label: 'BODY MASS SHARE', val: '~35–42%', sub: 'Metabolically active tissue' },
            { label: 'THERMOGENESIS', val: '~85% Heat', sub: 'Maintains 37°C core temperature' },
            { label: 'MOTOR UNIT', val: '1 α-Neuron', sub: 'Innervates muscle fiber group' },
          ],
          learning_points: [
            'Sarcomeres are the functional contractile units bounded by Z-discs containing thick myosin and thin actin filaments.',
            'Excitation-contraction coupling releases Ca²⁺ from the sarcoplasmic reticulum upon acetylcholine neuromuscular transmission.',
            'Agonist-antagonist muscle pairs (e.g., biceps brachii and triceps brachii) coordinate smooth joint control.',
            'Type I slow-twitch oxidative fibers resist fatigue; Type II fast-twitch fibers generate rapid peak power.',
            'Skeletal muscle contraction compresses deep veins, assisting venous blood return to the heart.',
          ],
          clinical: {
            diseases: 'Muscle strains, tendinopathy, sarcopenia, muscular dystrophies, and myasthenia gravis.',
            causes: 'Overload eccentric tearing, repetitive overuse, aging disuse, genetic dystrophin mutations, or autoimmune AChR antibodies.',
            symptoms: 'Localized myalgia, swelling, cramping, progressive proximal weakness, or rapid fatigability.',
            effects: 'Reduced functional strength, joint instability, metabolic insulin resistance, and increased fall risk.',
            prevention: 'Progressive resistance and flexibility training, adequate dietary protein, warm-up routines, and hydration.',
          },
          hotspots: [
            ['Pectoralis Major', 'Otot Dada Besar', 'Musculus pectoralis major', 'Anterior superior chest wall', 'Adducts, flexes, and medially rotates the humerus at the shoulder.', 'Fan-shaped superficial muscle converging on the intertubercular sulcus.', [-0.22, 0.48, 0.25]],
            ['Biceps Brachii', 'Otot Bisep Lengan', 'Musculus biceps brachii', 'Anterior arm compartment', 'Supinates the forearm and flexes the elbow and shoulder joints.', 'Two-headed fusiform muscle innervated by the musculocutaneous nerve.', [0.46, 0.28, 0.12]],
            ['Rectus Abdominis', 'Otot Perut Lurus', 'Musculus rectus abdominis', 'Anterior abdominal wall', 'Flexes the lumbar spine, compresses abdominal viscera, and stabilizes pelvis.', 'Segmented by tendinous intersections and enclosed in the rectus sheath.', [0.0, 0.04, 0.24]],
            ['Quadriceps Femoris', 'Otot Paha Depan', 'Musculus quadriceps femoris', 'Anterior thigh compartment', 'Primary extensor of the knee joint; rectus femoris also flexes the hip.', 'Four heads unite into the patellar tendon inserting on tibial tuberosity.', [-0.24, -0.52, 0.18]],
            ['Gastrocnemius & Calf', 'Otot Betis', 'Musculus gastrocnemius', 'Posterior leg compartment', 'Plantarflexes the ankle during walking/running and assists knee flexion.', 'Inserts via the calcaneal (Achilles) tendon onto the calcaneus.', [0.24, -0.78, -0.08]],
          ],
        }),

        /* --- REPRODUCTIVE & PELVIC ANATOMY (NEUTRAL MEDICAL EDUCATION) --- */
        makeSpecimen({
          id: 'penis',
          name_en: 'Penis',
          name_id: 'Penis',
          latin: 'Penis',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'penis',
          phys_default: 'blood',
          body_pos: [0, 0.42, 0.18],
          overview_en: 'The external male copulatory and urinary organ consisting of a root, cylindrical shaft (body), and distal glans containing three erectile tissue columns.',
          overview_id: 'Organ reproduksi eksternal dan saluran kemih pria yang terdiri atas akar, batang silindris, dan glans distal dengan tiga kolom jaringan erektil.',
          physiology_en: 'Conducts urine from the spongy urethra during micturition and achieves vascular engorgement (erection) via parasympathetic nitric oxide vasodilation.',
          physiology_id: 'Menyalurkan urine melalui uretra spongiosa saat berkemih serta mengalami pembesaran vaskular (ereksi) melalui vasodilatasi parasimpatis.',
          metrics: [
            { label: 'ERECTILE COLUMNS', val: '3 Cylinders', sub: '2 Corpora cavernosa + 1 spongiosum' },
            { label: 'URETHRAL SEGMENT', val: 'Spongy Urethra', sub: 'Terminates at external meatus' },
            { label: 'VASCULAR MEDIATOR', val: 'Nitric Oxide', sub: 'cGMP smooth muscle relaxation' },
            { label: 'SENSORY NERVE', val: 'Dorsal Nerve', sub: 'Branch of pudendal nerve (S2–S4)' },
          ],
          learning_points: [
            'Paired dorsal corpora cavernosa and a single ventral corpus spongiosum are encased in tough tunica albuginea.',
            'The corpus spongiosum surrounds the spongy urethra and expands distally to form the glans penis.',
            'Parasympathetic pelvic splanchnic nerves (S2–S4) trigger helicine artery dilation and venous compression.',
            'Sympathetic innervation (L1–L2) mediates emission and detumescence.',
            'Internal pudendal artery branches supply deep, dorsal, and bulbourethral penile vasculature.',
          ],
          clinical: {
            diseases: 'Erectile dysfunction, Peyronie disease, phimosis/paraphimosis, balanitis, and urethral stricture.',
            causes: 'Endothelial vascular disease, diabetes mellitus, fibrous tunica plaques, local infection, or trauma.',
            symptoms: 'Difficulty achieving/maintaining erection, penile curvature, dysuria, or localized inflammation.',
            effects: 'Urinary outflow obstruction or impaired sexual/reproductive function; vascular ED can herald cardiovascular disease.',
            prevention: 'Cardiovascular risk control, regular hygiene, safe sexual practices, and prompt urological evaluation.',
          },
          hotspots: [
            ['Corpora Cavernosa', 'Korpus Kavernosum', 'Corpora cavernosa penis', 'Dorsal paired erectile columns', 'Fills with arterial blood under high pressure to produce penile rigidity.', 'Surrounded by thick fibrous tunica albuginea.', [-0.14, 0.15, 0.15]],
            ['Corpus Spongiosum', 'Korpus Spongiosum', 'Corpus spongiosum penis', 'Ventral midline column', 'Protects the spongy urethra from compression during erection.', 'Expands proximally into the bulb and distally into the glans.', [0.0, 0.0, 0.24]],
            ['Spongy (Penile) Urethra', 'Uretra Spongiosa', 'Urethra spongiosa', 'Central lumen of corpus spongiosum', 'Shared terminal conduit for urine and seminal fluid.', 'Opens externally at the slit-like external urethral orifice.', [0.0, -0.25, 0.22]],
            ['Glans Penis & Corona', 'Glans Penis', 'Glans penis', 'Distal conical expansion', 'Richly innervated sensory cap cushioning the distal corpora cavernosa.', 'Separated from the shaft by the neck and corona glandis.', [0.0, -0.58, 0.24]],
            ['Root (Crura & Bulb)', 'Akar Penis', 'Radix penis', 'Superficial perineal pouch', 'Anchors the penis firmly to the ischiopubic rami and perineal membrane.', 'Covered by ischiocavernosus and bulbospongiosus muscles.', [0.14, 0.45, 0.05]],
          ],
        }),

        makeSpecimen({
          id: 'testes',
          name_en: 'Testes',
          name_id: 'Testis',
          latin: 'Testis / Orchis',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'testes',
          phys_default: 'blood',
          body_pos: [0, 0.32, 0.14],
          overview_en: 'Paired ovoid male gonads suspended within the scrotum by the spermatic cords, encased in a dense white fibrous capsule (tunica albuginea).',
          overview_id: 'Kelenjar gonad pria berpasangan berbentuk oval yang tergantung di dalam skrotum oleh korda spermatika dan terbungkus tunika albuginea.',
          physiology_en: 'Produces haploid spermatozoa via spermatogenesis in seminiferous tubules and secretes testosterone from interstitial Leydig cells.',
          physiology_id: 'Menghasilkan spermatozoa haploid melalui spermatogenesis di tubulus seminiferus serta menyekresikan testosteron dari sel Leydig interstisial.',
          metrics: [
            { label: 'DIMENSIONS', val: '~4 × 3 × 2.5 cm', sub: 'Adult ovoid volume ~15–25 mL' },
            { label: 'SPERM OUTPUT', val: '~100–200M / day', sub: '64–74 day maturation cycle' },
            { label: 'OPTIMAL TEMP', val: '~34–35 °C', sub: '2–3°C below core body temp' },
            { label: 'KEY HORMONES', val: 'Testosterone & Inhibin', sub: 'Regulated by LH and FSH' },
          ],
          learning_points: [
            'Internal septa divide each testis into ~250 lobules housing tightly coiled seminiferous tubules.',
            'Sertoli sustentacular cells form the blood-testis barrier and nourish developing germ cells.',
            'Interstitial Leydig cells synthesize testosterone under luteinizing hormone (LH) stimulation.',
            'Sperm mature and gain motility while traversing the head, body, and tail of the posterior epididymis.',
            'The pampiniform venous plexus acts as a countercurrent heat exchanger cooling testicular arterial blood.',
          ],
          clinical: {
            diseases: 'Varicocele, testicular torsion, epididymo-orchitis, cryptorchidism, and testicular germ cell tumors.',
            causes: 'Pampiniform plexus valve incompetence, spermatic cord twisting, ascending bacterial infection, or developmental maldescent.',
            symptoms: 'Sudden severe acute scrotal pain (surgical emergency in torsion), painless firm nodule, or dull dragging ache.',
            effects: 'Impaired spermatogenesis, subfertility, hypogonadism, or ischemic testicular infarction if torsion is delayed.',
            prevention: 'Periodic testicular self-awareness, protective athletic cups, and immediate emergency care for acute scrotal pain.',
          },
          hotspots: [
            ['Seminiferous Tubules & Lobules', 'Tubulus Seminiferus', 'Tubuli seminiferi contorti', 'Internal testicular lobules', 'Site of meiotic spermatogenesis supported by Sertoli cells.', 'Converge via straight tubules into the mediastinum testis.', [-0.45, -0.05, 0.25]],
            ['Tunica Albuginea', 'Tunika Albuginea', 'Tunica albuginea testis', 'Dense fibrous outer capsule', 'Maintains structural integrity and sends septa into the parenchyma.', 'Covered anteriorly and laterally by visceral tunica vaginalis.', [-0.45, -0.32, 0.18]],
            ['Epididymis (Head, Body, Tail)', 'Epididimis', 'Epididymis', 'Posterolateral surface of testis', 'Stores spermatozoa and supports physiological maturation and motility.', 'Tail continues inferiorly as the muscular ductus (vas) deferens.', [0.54, -0.05, -0.12]],
            ['Ductus (Vas) Deferens', 'Vas Deferens', 'Ductus deferens', 'Ascends within spermatic cord', 'Propels mature sperm via peristalsis toward the ejaculatory duct.', 'Passes through inguinal canal over pelvic brim to posterior bladder.', [0.40, 0.55, -0.05]],
            ['Spermatic Cord & Pampiniform Plexus', 'Korda Spermatika', 'Funiculus spermaticus', 'Suspends testis from inguinal ring', 'Houses testicular artery, pampiniform venous plexus, nerves, and lymphatics.', 'Countercurrent heat exchange keeps testes cooler than core temperature.', [-0.40, 0.55, 0.05]],
          ],
        }),

        makeSpecimen({
          id: 'scrotum',
          name_en: 'Scrotum',
          name_id: 'Kantung zakar',
          latin: 'Scrotum',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'scrotum',
          phys_default: 'blood',
          body_pos: [0, 0.30, 0.14],
          overview_en: 'A cutaneous fibromuscular pouch inferior to the pubic symphysis, divided internally by a midline septum into two compartments.',
          overview_id: 'Kantung fibromuskular berkulit di inferior simfisis pubis yang terbagi secara internal oleh septum garis tengah menjadi dua kompartemen.',
          physiology_en: 'Protects the testes and regulates testicular temperature via reflexive contraction/relaxation of the dartos and cremaster muscles.',
          physiology_id: 'Melindungi testis dan mengatur suhu testis melalui kontraksi/relaksasi refleks otot dartos dan otot kremaster.',
          metrics: [
            { label: 'COMPARTMENTS', val: '2 Chambers', sub: 'Divided by scrotal septum' },
            { label: 'THERMAL OFFSET', val: '-2 to -3 °C', sub: 'Below 37°C core temp' },
            { label: 'THERMOREGULATORS', val: '2 Muscles', sub: 'Dartos & Cremaster' },
            { label: 'MIDLINE RIDGE', val: 'Raphe Seam', sub: 'External embryologic fusion line' },
          ],
          learning_points: [
            'The superficial dartos smooth muscle wrinkles scrotal skin to reduce heat loss in cold conditions.',
            'The skeletal cremaster muscle elevates the testes toward the warm body wall when cold or startled.',
            'A dense sweat gland distribution aids evaporative cooling in warm environments.',
            'The external scrotal raphe marks the embryonic fusion of the labioscrotal swellings.',
            'Two separate internal cavities limit localized fluid or infection from crossing sides.',
          ],
          clinical: {
            diseases: 'Hydrocele, scrotal dermatitis, inguinal-scrotal hernia, and scrotal edema.',
            causes: 'Fluid accumulation in the tunica vaginalis, patent processus vaginalis, fungal/contact irritation, or systemic fluid retention.',
            symptoms: 'Painless smooth swelling (transilluminating in hydrocele), itching, redness, or reducible bulge.',
            effects: 'Local discomfort, heat retention affecting sperm quality, or bowel strangulation in complicated hernia.',
            prevention: 'Keep area clean and dry, wear breathable cotton underwear, and seek evaluation for persistent swelling.',
          },
          hotspots: [
            ['Scrotal Skin & Median Raphe', 'Kulit Skrotum & Rafe', 'Raphe scroti', 'External midline ridge', 'Provides protective cutaneous covering and marks bilateral fusion.', 'Thin, pigmented, rugated skin rich in sebaceous and sweat glands.', [0.0, -0.35, 0.42]],
            ['Dartos Muscle Layer', 'Otot Dartos', 'Tunica dartos', 'Subcutaneous fascia layer', 'Contracts in cold temperatures to wrinkle skin and conserve heat.', 'Smooth muscle sheet continuous with superficial perineal (Colles) fascia.', [0.45, -0.15, 0.25]],
            ['Scrotal Septum', 'Septum Skrotum', 'Septum scroti', 'Internal midline partition', 'Separates left and right testes into distinct anatomical compartments.', 'Formed by inward extension of the dartos tunic.', [0.0, 0.05, 0.12]],
            ['Cremaster Muscle & Fascia', 'Otot Kremaster', 'Musculus cremaster', 'Surrounds spermatic cord & testis', 'Elevates testes closer to pelvic warmth via the cremasteric reflex (L1–L2).', 'Derived from internal abdominal oblique muscle fibers.', [-0.42, 0.35, 0.08]],
            ['Tunica Vaginalis Cavity', 'Rongga Tunika Vaginalis', 'Tunica vaginalis testis', 'Serous pouch around testis', 'Allows frictionless mobility of the testis within the scrotal sac.', 'Closed peritoneal remnant with parietal and visceral serous layers.', [0.32, -0.05, 0.15]],
          ],
        }),

        makeSpecimen({
          id: 'prostate',
          name_en: 'Prostate',
          name_id: 'Prostat',
          latin: 'Prostata',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'prostate',
          phys_default: 'blood',
          body_pos: [0, 0.48, 0.06],
          overview_en: 'A walnut-sized fibromuscular accessory sex gland situated inferior to the urinary bladder neck and anterior to the rectum, encircling the prostatic urethra.',
          overview_id: 'Kelenjar aksesori reproduksi fibromuskular seukuran kacang kenari di inferior leher kandung kemih dan anterior rektum yang mengelilingi uretra prostatika.',
          physiology_en: 'Secretes slightly alkaline, milky prostatic fluid (~30% of semen volume) containing citric acid, zinc, and prostate-specific antigen (PSA) to liquefy semen and support sperm motility.',
          physiology_id: 'Menyekresikan cairan prostat agak basa (±30% volume semen) yang mengandung asam sitrat, seng, dan PSA untuk mencairkan semen dan mendukung motilitas sperma.',
          metrics: [
            { label: 'NORMAL WEIGHT', val: '~18–25 g', sub: 'Young adult walnut size' },
            { label: 'SEMEN CONTRIBUTION', val: '~25–30%', sub: 'Alkaline proteolytic fluid' },
            { label: 'ANATOMICAL ZONES', val: '3 Main Zones', sub: 'Peripheral, central, transition' },
            { label: 'URETHRAL PATH', val: 'Prostatic Urethra', sub: 'Receives ejaculatory ducts' },
          ],
          learning_points: [
            'Clinically divided into peripheral (70%, posterior), central (25%), and transition (5%, periurethral) zones.',
            'Ejaculatory ducts traverse the central zone to open onto the seminal colliculus (verumontanum).',
            'Smooth muscle in the fibromuscular stroma contracts during ejaculation to expel prostatic secretions.',
            'Posterior surface abuts the rectal ampulla, allowing palpation during clinical digital examination.',
            'Androgen (dihydrotestosterone, DHT) signaling regulates prostatic growth throughout adult life.',
          ],
          clinical: {
            diseases: 'Benign prostatic hyperplasia (BPH), acute/chronic prostatitis, and prostate adenocarcinoma.',
            causes: 'Age-related DHT-driven transition zone hyperplasia, bacterial urinary reflux, or genetic/age risk factors.',
            symptoms: 'Urinary frequency, nocturia, weak urinary stream, hesitancy, incomplete bladder emptying, or dysuria.',
            effects: 'Bladder outlet obstruction, detrusor hypertrophy, urinary retention, or recurrent urinary tract infections.',
            prevention: 'Healthy weight, regular physical activity, balanced diet rich in vegetables, and age-appropriate medical screening.',
          },
          hotspots: [
            ['Base & Bladder Neck Interface', 'Basis Prostat', 'Basis prostatae', 'Superior surface below bladder', 'Continuous with the internal urethral sphincter of the urinary bladder.', 'Surrounds the proximal entry of the prostatic urethra.', [0.0, 0.42, 0.12]],
            ['Peripheral Zone', 'Zona Perifer', 'Zona peripherica', 'Posterior & lateral gland', 'Comprises ~70% of glandular tissue; palpable posteriorly against rectum.', 'Most frequent site of focal prostatic adenocarcinomas.', [0.35, 0.05, -0.32]],
            ['Transition Zone (Periurethral)', 'Zona Transisi', 'Zona transitionalis', 'Surrounds proximal urethra', 'Surrounds the prostatic urethra proximal to the seminal colliculus.', 'Primary site of age-related benign prostatic hyperplasia (BPH).', [-0.25, 0.12, 0.25]],
            ['Prostatic Urethra & Verumontanum', 'Uretra Prostatika', 'Urethra prostatica', 'Central vertical channel', 'Merges urinary and reproductive pathways at the seminal colliculus.', 'Receives openings of ejaculatory ducts and prostatic ductules.', [0.0, -0.05, 0.18]],
            ['Apex of Prostate', 'Apeks Prostat', 'Apex prostatae', 'Inferior tip on pelvic floor', 'Rests on the superior fascia of the urogenital diaphragm (external sphincter).', 'Point where the membranous urethra exits inferiorly.', [0.0, -0.45, 0.12]],
          ],
        }),

        makeSpecimen({
          id: 'seminal_vesicles',
          name_en: 'Seminal vesicles',
          name_id: 'Vesikula seminalis',
          latin: 'Vesiculae seminales / Glandulae vesiculosae',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'seminal_vesicles',
          phys_default: 'blood',
          body_pos: [0, 0.52, 0.02],
          overview_en: 'Paired lobulated, coiled tubular glands ~5 cm long located posterior to the urinary bladder fundus and superior to the prostate.',
          overview_id: 'Kelenjar tubuler berliku berpasangan sepanjang ±5 cm yang terletak di posterior fundus kandung kemih dan superior prostat.',
          physiology_en: 'Produces ~60–70% of total seminal plasma volume, rich in fructose (ATP energy for sperm), prostaglandins, and coagulating proteins.',
          physiology_id: 'Menghasilkan ±60–70% total volume plasma semen yang kaya fruktosa (sumber energi ATP sperma), prostaglandin, dan protein koagulasi.',
          metrics: [
            { label: 'SEMEN VOLUME', val: '~60–70%', sub: 'Majority of ejaculate fluid' },
            { label: 'GLAND LENGTH', val: '~5 cm Coiled', sub: '~15 cm if uncoiled' },
            { label: 'PRIMARY SUGAR', val: 'Fructose', sub: 'Sperm mitochondrial fuel' },
            { label: 'FLUID pH', val: '7.2–7.8', sub: 'Buffers acidic vaginal tract' },
          ],
          learning_points: [
            'Despite the historical term "vesicles," they secrete fluid rather than storing spermatozoa.',
            'Each gland duct joins the ipsilateral ampulla of the ductus deferens to form an ejaculatory duct.',
            'High fructose concentration provides essential metabolic substrate for flagellar sperm motility.',
            'Alkaline secretions neutralize residual urethral acidity and vaginal acidity.',
            'Situated immediately anterior to the rectum, separated by rectovesical fascia (Denonvilliers fascia).',
          ],
          clinical: {
            diseases: 'Seminal vesiculitis, seminal vesicle cysts, ejaculatory duct obstruction, and hematospermia.',
            causes: 'Ascending genitourinary bacterial infections, congenital Wolffian duct anomalies, or calculi.',
            symptoms: 'Hematospermia (blood in semen), painful ejaculation, pelvic/perineal discomfort, or low-volume azoospermia.',
            effects: 'Reduced seminal fluid volume, acidic semen pH, impaired sperm motility, or obstructive subfertility.',
            prevention: 'Prompt treatment of urinary/prostatic infections and safe sexual health practices.',
          },
          hotspots: [
            ['Right Glandular Body', 'Vesikula Seminalis Kanan', 'Glandula vesiculosa dextra', 'Posterior right bladder base', 'Synthesizes fructose- and prostaglandin-rich alkaline seminal fluid.', 'Coiled sacculated tube lined by pseudostratified secretory epithelium.', [-0.38, 0.22, -0.02]],
            ['Left Glandular Body', 'Vesikula Seminalis Kiri', 'Glandula vesiculosa sinistra', 'Posterior left bladder base', 'Contributes symmetrical seminal plasma volume during emission.', 'Supplied by inferior vesical and middle rectal arteries.', [0.38, 0.22, -0.02]],
            ['Ampulla of Ductus Deferens', 'Ampula Vas Deferens', 'Ampulla ductus deferentis', 'Medial to each seminal vesicle', 'Terminal dilated reservoir of the vas deferens prior to duct union.', 'Curves medially over the ureter to reach the posterior bladder.', [-0.15, 0.32, 0.08]],
            ['Excretory Duct Junction', 'Pertemuan Duktus Ekskretorius', 'Ductus excretorius', 'Inferior pole of gland', 'Unites with the ductus deferens ampulla at the superior border of the prostate.', 'Marks the anatomical origin of the ejaculatory duct.', [0.15, -0.14, 0.06]],
            ['Ejaculatory Ducts', 'Duktus Ejakulatorius', 'Ductus ejaculatorius', 'Traverses posterior prostate', 'Delivers combined sperm and seminal fluid into the prostatic urethra.', 'Sympathetic contraction expels contents during the emission phase.', [0.0, -0.35, 0.08]],
          ],
        }),

        makeSpecimen({
          id: 'vulva',
          name_en: 'Vulva',
          name_id: 'Vulva',
          latin: 'Vulva / Pudendum femininum',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'vulva',
          phys_default: 'blood',
          body_pos: [0, 0.38, 0.14],
          overview_en: 'The external female genital structures situated in the anterior urogenital triangle of the perineum, encompassing the mons pubis, labia, clitoris, and vestibule.',
          overview_id: 'Struktur genitalia eksternal wanita pada segitiga urogenital anterior perineum, meliputi mons pubis, labia, klitoris, dan vestibulum.',
          physiology_en: 'Protects the internal urethral and vaginal orifices, provides lubricating secretions, and mediates sensory sexual arousal.',
          physiology_id: 'Melindungi muara uretra dan vagina internal, menghasilkan sekresi pelumas, serta memediasi respons sensorik.',
          metrics: [
            { label: 'VESTIBULAR ORIFICES', val: '2 Openings', sub: 'Urethral & vaginal orifices' },
            { label: 'LUBRICATING GLANDS', val: 'Bartholin & Skene', sub: 'Greater & lesser vestibular' },
            { label: 'ERECTILE TISSUE', val: 'Clitoris & Bulbs', sub: 'Internal crura & vestibular bulbs' },
            { label: 'INNERVATION', val: 'Pudendal Nerve', sub: 'S2–S4 somatic & autonomic' },
          ],
          learning_points: [
            'Labia majora are adipose-rich cutaneous folds homologous to the male scrotum; labia minora are hairless mucosal folds.',
            'The clitoris consists of glans, body, and paired internal crura composed of erectile corpora cavernosa.',
            'The vaginal vestibule houses the external urethral orifice anteriorly and the vaginal orifice posteriorly.',
            'Greater vestibular (Bartholin) glands open posterolaterally to lubricate the lower vestibule.',
            'Pudendal nerve branches (dorsal nerve of clitoris, perineal nerves) supply rich sensory innervation.',
          ],
          clinical: {
            diseases: 'Vulvovaginal candidiasis, contact dermatitis, Bartholin duct cyst/abscess, lichen sclerosus, and vulvar intraepithelial neoplasia.',
            causes: 'Fungal/bacterial dysbiosis, harsh fragranced hygiene products, Bartholin duct blockage, or HPV infection.',
            symptoms: 'Pruritus, erythema, localized vestibular swelling, dyspareunia, or mucosal irritation.',
            effects: 'Local pain, discomfort during urination or sitting, and disruption of protective mucosal flora.',
            prevention: 'Gentle fragrance-free hygiene, breathable cotton garments, HPV vaccination, and regular gynecological care.',
          },
          hotspots: [
            ['Mons Pubis & Anterior Commissure', 'Mons Pubis', 'Mons pubis', 'Anterior to pubic symphysis', 'Cushions the pubic symphysis with subcutaneous adipose tissue.', 'Covered by skin and post-pubertal hair.', [0.0, 0.52, 0.22]],
            ['Labia Majora', 'Labia Mayora', 'Labia majora pudendi', 'Outer longitudinal folds', 'Encloses and protects the pudendal cleft and inner vestibular structures.', 'Contains adipose tissue, dartos-like smooth muscle, and sebaceous glands.', [-0.34, 0.0, 0.14]],
            ['Labia Minora', 'Labia Minora', 'Labia minora pudendi', 'Inner hairless mucosal folds', 'Surrounds the vestibule and splits anteriorly to form the clitoral prepuce and frenulum.', 'Rich in elastic fibers, blood vessels, and sensory nerve endings.', [0.18, -0.02, 0.22]],
            ['Clitoris (Glans & Crura)', 'Klitoris', 'Clitoris', 'Anterior apex of vestibule', 'Primary neurovascular sensory organ of female sexual arousal.', 'Internal crura anchor along the ischiopubic rami alongside vestibular bulbs.', [0.0, 0.34, 0.24]],
            ['Vestibule & Bartholin Glands', 'Vestibulum & Kelenjar Bartholin', 'Vestibulum vaginae', 'Cleft between labia minora', 'Contains urethral meatus, vaginal introitus, and lubricating vestibular ducts.', 'Bartholin glands reside deep to the posterior vestibular bulbs.', [0.0, -0.25, 0.22]],
          ],
        }),

        makeSpecimen({
          id: 'vagina',
          name_en: 'Vagina',
          name_id: 'Vagina',
          latin: 'Vagina',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'vagina',
          phys_default: 'blood',
          body_pos: [0, 0.44, 0.08],
          overview_en: 'An elastic fibromuscular canal (~8–10 cm long) extending posterosuperiorly from the vestibule to the uterine cervix between the bladder and rectum.',
          overview_id: 'Saluran fibromuskular elastis (±8–10 cm) yang membentang ke posterosuperior dari vestibulum menuju serviks uteri di antara kandung kemih dan rektum.',
          physiology_en: 'Serves as the menstrual outflow tract, copulatory receptacle, and inferior birth canal while maintaining an acidic antimicrobial microbiome.',
          physiology_id: 'Berfungsi sebagai saluran keluar darah menstruasi, organ kopulasi, dan jalan lahir bagian bawah sambil mempertahankan mikrobioma asam pelindung.',
          metrics: [
            { label: 'CANAL LENGTH', val: '7.5–10 cm', sub: 'Anterior vs posterior wall' },
            { label: 'HEALTHY pH', val: '3.8–4.5', sub: 'Lactobacillus lactic acid' },
            { label: 'EPITHELIUM', val: 'Non-keratinized', sub: 'Stratified squamous glycogen-rich' },
            { label: 'FORNICES', val: '4 Recesses', sub: 'Anterior, posterior, 2 lateral' },
          ],
          learning_points: [
            'Transverse mucosal folds (vaginal rugae) permit substantial circumferential expansion during childbirth.',
            'The uterine cervix projects into the upper vagina, forming anterior, posterior, and lateral fornices.',
            'The posterior fornix lies directly adjacent to the rectouterine pouch (pouch of Douglas).',
            'Estrogen-stimulated glycogen in epithelial cells is metabolized by Lactobacillus species into protective lactic acid.',
            'Supported inferiorly by the levator ani pelvic floor muscles and perineal body.',
          ],
          clinical: {
            diseases: 'Bacterial vaginosis, vulvovaginal candidiasis, trichomoniasis, atrophic vaginitis, and pelvic organ prolapse.',
            causes: 'Microbiome pH disruption, antibiotic use, postmenopausal hypoestrogenism, or obstetric pelvic floor laxity.',
            symptoms: 'Altered discharge, odor, mucosal dryness, pruritus, dyspareunia, or pelvic pressure.',
            effects: 'Increased vulnerability to ascending pelvic infections or urinary symptoms.',
            prevention: 'Avoid internal douching (preserves natural Lactobacillus pH), practice safe sex, and perform pelvic floor exercises.',
          },
          hotspots: [
            ['Posterior & Lateral Fornices', 'Forniks Vagina', 'Fornix vaginae', 'Superior recess around cervix', 'Surrounds the intravaginal cervix; posterior fornix abuts the rectouterine pouch.', 'Important anatomical landmark during pelvic examination.', [0.0, 0.56, -0.02]],
            ['Cervical Os Interface', 'Muara Serviks', 'Ostium uteri', 'Apex of vaginal canal', 'Channel connecting the uterine endocervical canal with the vaginal lumen.', 'Permits passage of menstrual fluid and spermatozoa.', [0.0, 0.48, 0.12]],
            ['Vaginal Rugae (Mucosal Folds)', 'Rugae Vagina', 'Rugae vaginales', 'Anterior & posterior walls', 'Provides distensible reserve surface area for childbirth and coitus.', 'Lined by glycogen-rich stratified squamous epithelium.', [0.16, 0.05, 0.22]],
            ['Fibromuscular Wall & Pelvic Floor', 'Dinding Fibromuskular', 'Tunica muscularis vaginae', 'Middle smooth muscle coat', 'Provides structural tone supported laterally by pubococcygeus fibers.', 'Supplied by vaginal branches of internal iliac and uterine arteries.', [-0.24, -0.15, 0.12]],
            ['Vaginal Orifice (Introitus)', 'Orifisium Vagina', 'Ostium vaginae', 'Inferior vestibular opening', 'Opens into the posterior vestibule guarded by the bulbospongiosus muscle.', 'Surrounded by erectile vestibular bulbs.', [0.0, -0.58, 0.18]],
          ],
        }),

        makeSpecimen({
          id: 'uterus',
          name_en: 'Uterus',
          name_id: 'Rahim',
          latin: 'Uterus',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'uterus',
          phys_default: 'blood',
          body_pos: [0, 0.56, 0.06],
          overview_en: 'A thick-walled, pear-shaped hollow muscular organ in the true pelvis, typically anteverted and anteflexed superior to the urinary bladder.',
          overview_id: 'Organ otot berongga berbentuk buah pir berdinding tebal di rongga panggul sejati, umumnya dalam posisi anteversi di atas kandung kemih.',
          physiology_en: 'Undergoes cyclic endometrial proliferation and shedding (menstruation), supports blastocyst implantation, nourishes fetal development, and generates labor contractions.',
          physiology_id: 'Mengalami siklus proliferasi dan peluruhan endometrium (menstruasi), mendukung implantasi embrio, menutrisi janin, serta menghasilkan kontraksi persalinan.',
          metrics: [
            { label: 'NON-PREGNANT SIZE', val: '~7.5 × 5 × 2.5 cm', sub: 'Nulliparous adult weight ~50–80 g' },
            { label: 'WALL LAYERS', val: '3 Layers', sub: 'Peri-, Myo-, Endometrium' },
            { label: 'CYCLE LENGTH', val: '~28 Days', sub: 'Menstrual, proliferative, secretory' },
            { label: 'LIGAMENTS', val: 'Broad & Round', sub: 'Plus cardinal & uterosacral' },
          ],
          learning_points: [
            'Anatomical subdivisions include the dome-shaped fundus, main body (corpus), isthmus, and cylindrical cervix.',
            'The endometrium comprises a cyclic stratum functionalis and a regenerative stratum basalis.',
            'The myometrium consists of three interlacing smooth muscle layers responsive to oxytocin and prostaglandins.',
            'Cardinal (transverse cervical) and uterosacral ligaments provide primary passive support against prolapse.',
            'Uterine arteries anastomose with ovarian arteries along the lateral borders within the broad ligament.',
          ],
          clinical: {
            diseases: 'Uterine leiomyomas (fibroids), endometriosis, adenomyosis, abnormal uterine bleeding, and endometrial or cervical cancer.',
            causes: 'Hormonal estrogen/progesterone sensitivity, retrograde menstruation, persistent high-risk HPV infection (cervix), or metabolic factors.',
            symptoms: 'Menorrhagia, dysmenorrhea, intermenstrual bleeding, pelvic pressure, or subfertility.',
            effects: 'Iron-deficiency anemia from heavy bleeding, chronic pelvic pain, or obstetric complications.',
            prevention: 'HPV vaccination, routine Pap/HPV cervical screening, healthy weight maintenance, and timely gynecologic evaluation.',
          },
          hotspots: [
            ['Uterine Fundus', 'Fundus Uteri', 'Fundus uteri', 'Superior dome above tubal ostia', 'Forms the upper muscular dome where blastocyst implantation commonly occurs.', 'Rises out of the true pelvis into the abdomen during pregnancy.', [0.0, 0.68, 0.14]],
            ['Uterine Cavity & Endometrium', 'Rongga Rahim & Endometrium', 'Cavitas uteri / Endometrium', 'Triangular central mucosal lining', 'Prepares vascularized secretory mucosa for implantation or sheds during menses.', 'Progesterone maintains the secretory stratum functionalis.', [0.0, 0.25, 0.28]],
            ['Myometrium', 'Miometrium', 'Myometrium', 'Thick middle smooth muscle wall', 'Generates coordinated expulsive contractions during parturition and hemostasis.', 'Spiral arteries traverse the myometrium to supply the endometrium.', [-0.36, 0.22, 0.16]],
            ['Internal Os & Isthmus', 'Ostium Uteri Internum', 'Isthmus uteri', 'Junction of body and cervix', 'Narrows into the cervical canal and forms the lower uterine segment in pregnancy.', 'Maintains mechanical closure throughout gestation.', [0.0, -0.18, 0.16]],
            ['Uterine Cervix & External Os', 'Serviks Uteri', 'Cervix uteri', 'Inferior cylindrical neck', 'Produces cyclic cervical mucus regulating sperm entry and pathogen barrier.', 'Squamocolumnar transformation zone is monitored via Pap screening.', [0.0, -0.52, 0.14]],
          ],
        }),

        makeSpecimen({
          id: 'ovaries',
          name_en: 'Ovaries',
          name_id: 'Indung telur',
          latin: 'Ovaria',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'ovaries',
          phys_default: 'blood',
          body_pos: [0.22, 0.62, 0.02],
          overview_en: 'Paired almond-shaped female gonads suspended in the ovarian fossa of the lateral pelvic wall by the mesovarium, suspensory, and proper ovarian ligaments.',
          overview_id: 'Kelenjar gonad wanita berpasangan berbentuk kacang almond yang tergantung pada dinding panggul lateral oleh mesovarium dan ligamentum ovarii.',
          physiology_en: 'Maturing follicles release secondary oocytes during ovulation and secrete cyclic estradiol, progesterone, inhibin, and small amounts of androgens.',
          physiology_id: 'Mematangkan folikel untuk melepaskan oosit sekunder saat ovulasi serta menyekresikan hormon estradiol, progesteron, dan inhibin secara siklik.',
          metrics: [
            { label: 'DIMENSIONS', val: '~3.5 × 2 × 1 cm', sub: 'Almond-shaped paired gonads' },
            { label: 'OVULATION CYCLE', val: '~Day 14', sub: 'Triggered by mid-cycle LH surge' },
            { label: 'KEY HORMONES', val: 'Estrogen & Progesterone', sub: 'Follicular vs Luteal phases' },
            { label: 'BLOOD SUPPLY', val: 'Ovarian Arteries', sub: 'Direct branches of abdominal aorta' },
          ],
          learning_points: [
            'The outer ovarian cortex houses primordial, primary, secondary, and mature Graafian follicles.',
            'Following ovulation, the ruptured follicle transforms into the progesterone-secreting corpus luteum.',
            'If fertilization does not occur, the corpus luteum involutes into a fibrous corpus albicans.',
            'The suspensory ligament of the ovary conducts the ovarian artery, vein, and plexus from the pelvic brim.',
            'Covered by simple cuboidal germinal epithelium rather than typical squamous mesothelium.',
          ],
          clinical: {
            diseases: 'Polycystic ovary syndrome (PCOS), functional ovarian cysts, ovarian torsion, and epithelial/germ-cell ovarian neoplasms.',
            causes: 'Hypothalamic-pituitary-ovarian endocrine imbalance, follicular persistence, adnexal mobility twisting, or BRCA/genetic factors.',
            symptoms: 'Oligomenorrhea, unilateral pelvic pain, acute severe abdominal pain (torsion), bloating, or hyperandrogenism.',
            effects: 'Anovulatory subfertility, metabolic insulin resistance (PCOS), or ovarian ischemia in adnexal torsion.',
            prevention: 'Regular menstrual cycle tracking, metabolic health management, and prompt evaluation of persistent pelvic pain.',
          },
          hotspots: [
            ['Ovarian Cortex & Developing Follicles', 'Korteks Ovarium & Folikel', 'Cortex ovarii', 'Outer peripheral parenchyma', 'Houses oocytes in progressive stages of folliculogenesis.', 'Granulosa cells aromatize androgens into 17β-estradiol under FSH control.', [-0.55, 0.12, 0.18]],
            ['Mature Graafian Follicle', 'Folikel Graaf Matang', 'Folliculus ovaricus vesiculosus', 'Bulging cortical surface', 'Ruptures at ovulation in response to the pituitary LH surge.', 'Releases secondary oocyte surrounded by corona radiata into peritoneal cavity.', [-0.48, -0.08, 0.25]],
            ['Corpus Luteum', 'Korpus Luteum', 'Corpus luteum', 'Post-ovulatory cortical gland', 'Secretes high progesterone and estradiol to sustain secretory endometrium.', 'Maintained by hCG if pregnancy occurs.', [0.55, 0.08, 0.22]],
            ['Ovarian Medulla & Hilum', 'Medula & Hilus Ovarium', 'Medulla ovarii', 'Central vascular connective core', 'Contains tortuous helicine blood vessels, lymphatics, and autonomic nerves.', 'Receives ovarian vessels entering via the mesovarium.', [0.48, -0.15, -0.08]],
            ['Suspensory & Proper Ovarian Ligaments', 'Ligamentum Suspensorium Ovarii', 'Ligamentum suspensorium ovarii', 'Lateral and medial poles', 'Suspends ovary to pelvic wall (carrying vessels) and anchors it to uterus.', 'Proper ovarian ligament is a remnant of the embryonic gubernaculum.', [-0.72, 0.22, -0.05]],
          ],
        }),

        makeSpecimen({
          id: 'fallopian_tubes',
          name_en: 'Fallopian tubes',
          name_id: 'Tuba falopi',
          latin: 'Tubae uterinae / Salpinges',
          organ_system: 'Reproductive',
          categories: ['Reproductive'],
          builder: 'fallopian_tubes',
          phys_default: 'blood',
          body_pos: [0.16, 0.65, 0.04],
          overview_en: 'Paired muscular tubes (~10–12 cm long) extending laterally from the uterine horns within the superior margin (mesosalpinx) of the broad ligament toward the ovaries.',
          overview_id: 'Saluran otot berpasangan (±10–12 cm) yang membentang ke lateral dari kornu uteri di dalam mesosalpinks ligamentum latum menuju ovarium.',
          physiology_en: 'Captures ovulated oocytes via sweeping fimbriae, provides the physiological site of fertilization in the ampulla, and transports the zygote to the uterus.',
          physiology_id: 'Menangkap oosit yang berovulasi melalui fimbriae, menjadi lokasi utama fertilisasi di ampula, dan mengangkut zigot menuju rongga rahim.',
          metrics: [
            { label: 'TUBE LENGTH', val: '10–12 cm', sub: 'Four anatomical segments' },
            { label: 'FERTILIZATION SITE', val: 'Ampulla', sub: 'Widest distal-middle segment' },
            { label: 'MUCOSAL LINING', val: 'Ciliated + Peg', sub: 'Estrogen-driven ciliary beat' },
            { label: 'TRANSIT DURATION', val: '3–4 Days', sub: 'Zygote reaches uterine cavity' },
          ],
          learning_points: [
            'Four segments from lateral to medial: infundibulum (with fimbriae), ampulla, isthmus, and intramural (uterine) part.',
            'Finger-like fimbriae sweep over the ovarian surface at ovulation to guide the oocyte into the abdominal ostium.',
            'Coordinated ciliary beating and smooth muscle peristalsis propel the early embryo toward the uterus.',
            'Non-ciliated peg cells secrete nutrient-rich tubal fluid supporting capacitated sperm and cleavage-stage embryos.',
            'The narrow isthmus acts as a physiological sphincter regulating embryo entry into the uterus.',
          ],
          clinical: {
            diseases: 'Ectopic (tubal) pregnancy, salpingitis / pelvic inflammatory disease (PID), hydrosalpinx, and tubal factor infertility.',
            causes: 'Ascending Chlamydia trachomatis or Neisseria gonorrhoeae infection, prior pelvic surgery, or endometriosis scarring.',
            symptoms: 'Unilateral lower quadrant pain, abnormal vaginal bleeding, acute peritoneal signs if ectopic rupture occurs.',
            effects: 'Ciliary damage impairing embryo transport, tubal occlusion, or life-threatening intraperitoneal hemorrhage in ruptured ectopic pregnancy.',
            prevention: 'Barrier contraception, routine STI screening and prompt antibiotic treatment, and early prenatal ultrasound localization.',
          },
          hotspots: [
            ['Fimbriae & Abdominal Ostium', 'Fimbriae Tuba', 'Fimbriae tubae uterinae', 'Distal funnel fringe near ovary', 'Sweeps across the ovary to capture the ovulated oocyte-cumulus complex.', 'Ovarian fimbria attaches directly to the tubal pole of the ovary.', [-0.85, 0.08, 0.12]],
            ['Infundibulum', 'Infundibulum Tuba', 'Infundibulum tubae uterinae', 'Funnel-shaped lateral opening', 'Channels captured oocytes from the peritoneal cavity into the ampulla.', 'Opens via the abdominal ostium (~2–3 mm diameter).', [-0.72, 0.28, 0.08]],
            ['Ampulla (Fertilization Zone)', 'Ampula Tuba', 'Ampulla tubae uterinae', 'Widest, longest tortuous segment', 'Usual anatomical site where sperm fertilizes the secondary oocyte.', 'Features intricate branching longitudinal mucosal folds.', [-0.48, 0.38, 0.05]],
            ['Isthmus of Uterine Tube', 'Istmus Tuba', 'Isthmus tubae uterinae', 'Narrow thick-walled medial segment', 'Regulates sperm ascent and delays zygote entry until endometrium is receptive.', 'Enters the uterine wall at the superior lateral uterine horn.', [0.35, 0.32, 0.05]],
            ['Intramural (Uterine) Part & Mesosalpinx', 'Bagian Intramural', 'Pars uterina', 'Pierces myometrium at uterine horn', 'Opens into the superior lateral angle of the uterine cavity.', 'Supported inferiorly by the vascular mesosalpinx fold.', [0.22, 0.22, 0.05]],
          ],
        }),

        /* --- GLUTEAL & ANAL ANATOMY (NEUTRAL MEDICAL EDUCATION) --- */
        makeSpecimen({
          id: 'buttocks',
          name_en: 'Buttocks',
          name_id: 'Pantat (Regio Glutea)',
          latin: 'Regio glutea',
          organ_system: 'Musculoskeletal',
          categories: ['Musculoskeletal'],
          builder: 'buttocks',
          phys_default: 'nervous',
          body_pos: [0, 0.48, -0.16],
          overview_en: 'The posterolateral pelvic region bounded superiorly by the iliac crest, inferiorly by the gluteal fold, and medially by the intergluteal cleft.',
          overview_id: 'Regio panggul posterolateral yang dibatasi krista iliaka di superior, lipatan gluteal di inferior, dan celah intergluteal di medial.',
          physiology_en: 'Provides upright bipedal pelvic stabilization, hip propulsion, load-bearing adipose cushioning while seated, and neurovascular passage from pelvis to lower limb.',
          physiology_id: 'Memberikan stabilisasi panggul saat berdiri bipedal, propulsi pinggul, bantalan adiposa saat duduk, serta jalur neurovaskular ke tungkai bawah.',
          metrics: [
            { label: 'MUSCLE TIERS', val: 'Superficial & Deep', sub: 'Gluteals + deep lateral rotators' },
            { label: 'SAFE IM QUADRANT', val: 'Upper-Outer', sub: 'Avoids medial-inferior sciatic nerve' },
            { label: 'MAJOR NERVE', val: 'Sciatic Nerve', sub: 'Exits greater sciatic foramen' },
            { label: 'BONY LANDMARK', val: 'Ischial Tuberosity', sub: 'Weight-bearing sitting bone' },
          ],
          learning_points: [
            'Superficial abductors (gluteus medius and minimus) prevent contralateral pelvic drop (Trendelenburg sign) during single-leg stance.',
            'Deep lateral rotators (piriformis, obturator internus, gemelli, quadratus femoris) stabilize the femoral head in the acetabulum.',
            'The piriformis muscle divides the greater sciatic foramen into suprapiriform and infrapiriform neurovascular compartments.',
            'The sciatic nerve emerges inferior to the piriformis in the lower-medial gluteal quadrant.',
            'Subcutaneous fibro-fatty septa and ischial bursae cushion weight over the ischial tuberosities when seated.',
          ],
          clinical: {
            diseases: 'Piriformis syndrome / sciatica, greater trochanteric pain syndrome, ischial bursitis, and pressure injuries.',
            causes: 'Prolonged sitting pressure, sciatic nerve entrapment, gluteal tendinopathy, or improper intramuscular injection placement.',
            symptoms: 'Deep gluteal ache, radiating posterior thigh pain, lateral hip tenderness, or localized skin erythema over bony prominences.',
            effects: 'Altered Trendelenburg gait, radicular lower-limb paresthesia, or soft-tissue pressure ischemia in immobilized patients.',
            prevention: 'Regular standing/movement breaks, gluteal strengthening, ergonomic seating, and strict upper-outer quadrant IM technique.',
          },
          hotspots: [
            ['Iliac Crest & Gluteus Medius', 'Krista Iliaka & Gluteus Medius', 'Crista iliaca / M. gluteus medius', 'Superolateral gluteal quadrant', 'Abducts the hip and stabilizes the level pelvis during walking.', 'Safe anatomical zone for dorsogluteal/ventrogluteal intramuscular injections.', [-0.42, 0.32, 0.16]],
            ['Piriformis Muscle', 'Otot Piriformis', 'Musculus piriformis', 'Deep central gluteal landmark', 'Laterally rotates the extended thigh and abducts the flexed thigh.', 'Key anatomical landmark exiting the greater sciatic foramen.', [-0.28, 0.08, 0.12]],
            ['Sciatic Nerve Pathway', 'Saraf Ischiadikus (Sciatic)', 'Nervus ischiadicus', 'Inferior to piriformis, inferomedial', 'Largest nerve in the body supplying posterior thigh and all leg/foot muscles.', 'Courses midway between ischial tuberosity and greater trochanter.', [-0.25, -0.25, 0.12]],
            ['Ischial Tuberosity & Gluteal Fold', 'Tuber Ischiadikum', 'Tuber ischiadicum', 'Inferomedial weight-bearing prominence', 'Supports trunk weight in the seated position and anchors hamstring origins.', 'Covered by gluteus maximus when standing and uncovered when hip is flexed.', [0.28, -0.35, 0.18]],
            ['Intergluteal Cleft & Subcutaneous Cushion', 'Celah Intergluteal', 'Crena analis', 'Midline posterior groove', 'Separates left and right gluteal prominences overlying sacrum and coccyx.', 'Dense fibro-adipose lobules absorb compressive sitting forces.', [0.0, -0.05, 0.25]],
          ],
        }),

        makeSpecimen({
          id: 'gluteus_maximus',
          name_en: 'Gluteus maximus',
          name_id: 'Otot bokong besar',
          latin: 'Musculus gluteus maximus',
          organ_system: 'Musculoskeletal',
          categories: ['Musculoskeletal'],
          builder: 'gluteus_maximus',
          phys_default: 'nervous',
          body_pos: [0.16, 0.48, -0.15],
          overview_en: 'The largest, heaviest, and most superficial muscle of the gluteal region, forming the characteristic bulk and contour of the human buttock.',
          overview_id: 'Otot terbesar, terberat, dan paling superfisial di regio gluteal yang membentuk massa utama serta kontur bokong manusia.',
          physiology_en: 'Generates powerful hip extension (rising from sitting, stair climbing, running) and lateral rotation while tensioning the iliotibial tract to stabilize the knee.',
          physiology_id: 'Menghasilkan ekstensi pinggul yang kuat (berdiri dari duduk, naik tangga, berlari) dan rotasi lateral serta menegangkan traktus iliotibialis.',
          metrics: [
            { label: 'MUSCLE RANK', val: 'Heaviest Single', sub: 'Largest muscle by volume/mass' },
            { label: 'INNERVATION', val: 'Inferior Gluteal N.', sub: 'L5, S1, S2 nerve roots' },
            { label: 'UPPER INSERTION', val: 'Iliotibial Tract', sub: '~75% superficial fibers' },
            { label: 'LOWER INSERTION', val: 'Gluteal Tuberosity', sub: '~25% deep fibers on femur' },
          ],
          learning_points: [
            'Originates broadly from the posterior gluteal line of ilium, dorsal sacrum/coccyx, and sacrotuberous ligament.',
            'Fibers slope inferolaterally at ~45° toward the femur and fascia lata.',
            'Three-quarters of fibers insert into the iliotibial (IT) tract, stabilizing the extended knee joint.',
            'Deep inferior fibers insert onto the gluteal tuberosity of the proximal posterior femur.',
            'Innervated exclusively by the inferior gluteal nerve (L5–S2) and perfused by superior and inferior gluteal arteries.',
          ],
          clinical: {
            diseases: 'Gluteus maximus strain, gluteal amnesia (deconditioning), inferior gluteal nerve palsy, and trochanteric bursitis.',
            causes: 'Explosive sprinting overload, prolonged sedentary sitting, pelvic surgery/trauma, or tight iliotibial band friction.',
            symptoms: 'Difficulty climbing stairs or rising from a chair, deep buttock soreness, and compensatory lumbar hyperextension.',
            effects: 'Reduced hip extension torque, anterior pelvic tilt, and secondary lower-back mechanical overload.',
            prevention: 'Hip-hinge strength exercises (squats, bridges, step-ups), dynamic hip flexor stretching, and active posture breaks.',
          },
          hotspots: [
            ['Iliac & Sacral Origin', 'Origo Iliaka & Sakralis', 'Origo musculi', 'Posterior ilium, sacrum & coccyx', 'Anchors broad proximal muscle fibers to the axial pelvic skeleton.', 'Includes attachment to the strong sacrotuberous ligament.', [-0.15, 0.35, 0.16]],
            ['Superficial Muscle Belly', 'Badan Otot Gluteus Maximus', 'Venter musculi', 'Coarse oblique fascicles', 'Generates peak hip extension power during stair climbing and running.', 'Coarse parallel fiber bundles separated by fibrous septa.', [0.34, 0.05, 0.25]],
            ['Iliotibial (IT) Tract Insertion', 'Insersi Traktus Iliotibialis', 'Tractus iliotibialis', 'Superolateral fascia lata', 'Transmits tensile force down the lateral thigh to stabilize the knee.', 'Receives ~75% of superficial gluteus maximus fibers.', [0.62, -0.25, 0.08]],
            ['Femoral Gluteal Tuberosity Insertion', 'Tuberositas Glutealis Femur', 'Tuberositas glutea', 'Deep proximal posterior femur', 'Provides direct bony leverage for powerful hip extension and external rotation.', 'Protected from bony friction by the trochanteric bursa.', [0.28, -0.42, 0.05]],
            ['Inferior Gluteal Neurovascular Pedicle', 'Saraf & Pembuluh Gluteus Inferior', 'N. et A. glutea inferior', 'Deep central muscle surface', 'Supplies motor innervation (L5–S2) and rich arterial perfusion to the muscle.', 'Enters the deep surface inferior to the piriformis muscle.', [-0.15, -0.05, 0.12]],
          ],
        }),

        makeSpecimen({
          id: 'anus',
          name_en: 'Anus',
          name_id: 'Dubur',
          latin: 'Anus / Canalis analis',
          organ_system: 'Digestive',
          categories: ['Digestive'],
          builder: 'anus',
          phys_default: 'digestion',
          body_pos: [0, 0.36, -0.06],
          overview_en: 'The terminal 3–4 cm outlet of the gastrointestinal tract passing through the pelvic floor from the anorectal junction to the external perineal anal verge.',
          overview_id: 'Saluran keluar terminal sepanjang ±3–4 cm dari saluran pencernaan yang menembus dasar panggul dari sambungan anorektal menuju tepi anal eksternal.',
          physiology_en: 'Maintains fecal continence at rest via tonic internal and external anal sphincters and coordinates voluntary relaxation during defecation.',
          physiology_id: 'Mempertahankan kontinensia feses saat istirahat melalui sfingter ani internal dan eksternal serta berelaksasi secara terkoordinasi saat defekasi.',
          metrics: [
            { label: 'ANAL CANAL LENGTH', val: '2.5–4.0 cm', sub: 'Anorectal ring to anal verge' },
            { label: 'SPHINCTER SYSTEM', val: '2 Sphincters', sub: 'Involuntary internal + voluntary external' },
            { label: 'LANDMARK LINE', val: 'Pectinate Line', sub: 'Divides visceral vs somatic zones' },
            { label: 'CONTINENCE ANGLE', val: '~90° Sling', sub: 'Puborectalis muscle pull' },
          ],
          learning_points: [
            'The internal anal sphincter is thickened involuntary circular smooth muscle under autonomic control.',
            'The external anal sphincter is voluntary striated skeletal muscle innervated by the inferior rectal nerve (pudendal, S2–S4).',
            'The pectinate (dentate) line marks the embryologic junction between endodermal hindgut and ectodermal proctodeum.',
            'Above the pectinate line, innervation is visceral (insensitive to sharp pain); below it, innervation is somatic (pain-sensitive).',
            'Vascular anal cushions (internal and external venous plexuses) contribute to airtight resting continence.',
          ],
          clinical: {
            diseases: 'Internal and external hemorrhoids, anal fissure, perianal abscess/fistula, and pruritus ani.',
            causes: 'Chronic constipation and straining, low-fiber diet, prolonged toilet sitting, or anal crypt gland infection.',
            symptoms: 'Bright red painless bleeding (internal hemorrhoids), sharp tearing pain on defecation (fissure), or perianal swelling.',
            effects: 'Local pain, mucosal prolapse, iron-deficiency anemia from chronic bleeding, or sphincter spasm.',
            prevention: 'High-fiber diet (25–35 g/day), adequate water intake, avoiding prolonged straining, and gentle hygiene.',
          },
          hotspots: [
            ['Anorectal Junction & Puborectalis Sling', 'Sambungan Anorektal', 'Junctio anorectalis', 'Superior pelvic floor entry', 'Creates an ~90° anorectal angle essential for gross fecal continence.', 'Puborectalis U-sling relaxes during squatting/defecation to straighten the canal.', [0.0, 0.45, 0.05]],
            ['Internal Anal Sphincter', 'Sfingter Ani Internal', 'Musculus sphincter ani internus', 'Inner involuntary smooth muscle ring', 'Provides ~70–85% of resting anal canal tone to prevent involuntary leakage.', 'Relaxes reflexively via the rectoanal inhibitory reflex upon rectal distension.', [-0.22, -0.32, 0.08]],
            ['Pectinate (Dentate) Line & Anal Columns', 'Linea Pektinata', 'Linea pectinata', 'Mid-canal mucosal transition', 'Separates visceral autonomic mucosa above from somatic squamous skin below.', 'Anal sinuses at the base of Morgagni columns contain mucus-secreting anal glands.', [0.0, -0.15, 0.22]],
            ['External Anal Sphincter', 'Sfingter Ani Eksternal', 'Musculus sphincter ani externus', 'Outer voluntary skeletal muscle cuff', 'Allows conscious voluntary squeeze to defer defecation.', 'Comprises deep, superficial, and subcutaneous striated muscle bands.', [0.24, -0.38, 0.06]],
            ['Anal Verge & Perianal Margin', 'Tepi Anal (Anal Verge)', 'Margo analis', 'External cutaneous opening', 'Marks the transition from non-keratinized anoderm to pigmented perianal skin.', 'Richly innervated by somatic inferior rectal sensory fibers.', [0.0, -0.56, 0.08]],
          ],
        }),

        makeSpecimen({
          id: 'rectum',
          name_en: 'Rectum',
          name_id: 'Rektum',
          latin: 'Rectum',
          organ_system: 'Digestive',
          categories: ['Digestive'],
          builder: 'rectum',
          phys_default: 'digestion',
          body_pos: [0, 0.46, -0.06],
          overview_en: 'The fixed ~12–15 cm pelvic continuation of the sigmoid colon descending along the anterior concavity of the sacrum and coccyx to the anal canal.',
          overview_id: 'Kelanjutan kolon sigmoid di rongga panggul sepanjang ±12–15 cm yang turun mengikuti lengkung anterior sakrum dan koksiks menuju kanalis analis.',
          physiology_en: 'Serves as a compliant temporary storage reservoir for feces and initiates the defecation reflex via stretch mechanoreceptors.',
          physiology_id: 'Berfungsi sebagai reservoir penyimpanan sementara yang lentur bagi feses dan memicu refleks defekasi melalui mekanoreseptor regang.',
          metrics: [
            { label: 'LENGTH', val: '12–15 cm', sub: 'S3 vertebra to pelvic floor' },
            { label: 'TRANSVERSE FOLDS', val: '3 Valves', sub: 'Houston transverse rectal folds' },
            { label: 'DISTAL RESERVOIR', val: 'Rectal Ampulla', sub: 'Compliant fecal storage zone' },
            { label: 'ARTERIAL SUPPLY', val: '3 Rectal Arteries', sub: 'Superior, middle, inferior' },
          ],
          learning_points: [
            'Lacks teniae coli, haustra, and epiploic appendages, possessing instead a complete outer longitudinal smooth muscle coat.',
            'Three internal crescentic transverse rectal folds (valves of Houston) support fecal mass weight.',
            'The dilated lower third (rectal ampulla) stretches to accommodate stool prior to defecation.',
            'In males, the anterior rectum lies behind the bladder, seminal vesicles, and prostate; in females, behind the uterus and vagina.',
            'Dual venous drainage links portal (superior rectal vein) and systemic (middle/inferior rectal veins) circulations.',
          ],
          clinical: {
            diseases: 'Rectal adenocarcinoma, proctitis, rectal prolapse, and solitary rectal ulcer syndrome.',
            causes: 'Adenomatous polyp progression, inflammatory bowel disease, pelvic floor weakness, or chronic straining.',
            symptoms: 'Hematochezia, tenesmus (feeling of incomplete evacuation), narrow-caliber stools, or rectal mucus discharge.',
            effects: 'Local pelvic invasion if neoplastic, iron-deficiency anemia, or fecal incontinence.',
            prevention: 'High-fiber nutrition, physical exercise, avoiding tobacco/excessive alcohol, and timely colonoscopy/FIT screening.',
          },
          hotspots: [
            ['Rectosigmoid Junction', 'Sambungan Rektosigmoid', 'Junctio rectosigmoidea', 'Level of S3 vertebra', 'Marks transition from mobile sigmoid mesocolon to fixed subperitoneal rectum.', 'End of teniae coli and epiploic appendages.', [0.0, 0.62, -0.08]],
            ['Transverse Rectal Folds (Houston Valves)', 'Katup Rektal Transversa', 'Plicae transversae recti', 'Superior, middle & inferior lumen', 'Supports fecal column weight and separates flatus from solid stool.', 'Three crescentic submucosal folds (superior/inferior left, middle right).', [-0.14, 0.25, 0.16]],
            ['Rectal Ampulla', 'Ampula Rekti', 'Ampulla recti', 'Dilated inferior pelvic segment', 'Distends to store fecal mass and triggers stretch-mediated defecation urge.', 'Supported posteriorly by the sacrum, coccyx, and anococcygeal ligament.', [0.0, -0.18, 0.22]],
            ['Peritoneal Reflection (Pouch)', 'Refleksi Peritoneum', 'Excavatio rectovesicalis / rectouterina', 'Anterior upper-to-middle third', 'Forms lowest point of peritoneal cavity (rectovesical in male, rectouterine in female).', 'Clinical site for dependent pelvic fluid accumulation.', [0.0, 0.12, 0.24]],
            ['Anorectal Ring & Pelvic Floor', 'Cincin Anorektal', 'Junctio anorectalis', 'Inferior pelvic diaphragm exit', 'Junction where rectal ampulla narrows sharply into the anal canal.', 'Encircled by puborectalis sling and upper internal anal sphincter.', [0.0, -0.58, 0.04]],
          ],
        }),
      ];

      /* =========================================================================
       * 3. GLOBAL APPLICATION STATE
       * ========================================================================= */
      const state = {
        lang: 'en',
        locale: 'en',
        theme: 'dark',
        device: 'desktop',
        role: 'student',
        viewMode: 'organ', // 'organ' | 'fullbody' | 'split'
        activeId: 'heart',
        splitRightId: 'brain',
        syncOrbit: true,
        selectedCategory: 'all',
        searchQuery: '',
        activeTab: 'structure',
        selectedHotspotId: null,
        showHotspots: true,
        xray: false,
        wireframe: false,
        autoRotate: false,
        livingPhysiology: true,
        holoScan: false,
        clipPlaneAxis: 'none',
        clipDist: 0.2,
        animClip: false,
        explodeFactor: 0,
        physSimMode: 'auto',
        showBodyShell: true,
        showBodySkeleton: true,
        bodySex: 'female',
        customModelLoaded: false,
        // Quiz state
        quizQueue: [],
        quizIndex: 0,
        quizScore: 0,
        quizAttempts: 0,
        quizAnsweredCurrent: false,
        customQuestions: {},
        quizReports: [],
        // Pi Network & Guest Verified Session State (in-memory only)
        piSession: {
          sdkReady: false,
          authenticating: false,
          sessionToken: null,
          user: null,
          isGuest: false,
          guestName: 'Guest',
        },
      };

      /* =========================================================================
       * 3B. WELCOME PAGE, LOGIN GATE & PI NETWORK USER AUTHENTICATION
       * ========================================================================= */
      const PI_APP_STUDIO_LOGIN_URL = 'https://backend.appstudio-u7cm9zhmha0ruwv8.piappengine.com/pi/auth/v1/login';

      function showWelcomeScreen() {
        const welcome = document.getElementById('welcome-screen');
        const login = document.getElementById('login-screen');
        if (login) login.classList.add('hidden');
        if (welcome) {
          welcome.classList.remove('hidden', 'opacity-0', 'pointer-events-none');
        }
      }

      function showLoginScreen() {
        const welcome = document.getElementById('welcome-screen');
        const login = document.getElementById('login-screen');
        if (welcome) welcome.classList.add('hidden');
        if (login) login.classList.remove('hidden');
        updatePiAuthUI();
      }

      function enterMainWorkspace() {
        const welcome = document.getElementById('welcome-screen');
        const login = document.getElementById('login-screen');
        if (welcome) welcome.classList.add('hidden');
        if (login) login.classList.add('hidden');
        setTimeout(onViewportResize, 60);
      }

      function continueAsGuest() {
        const guestInput = document.getElementById('input-guest-name');
        const customName = guestInput && guestInput.value.trim() ? guestInput.value.trim() : 'Guest';
        state.piSession.sessionToken = null;
        state.piSession.user = null;
        state.piSession.isGuest = true;
        state.piSession.guestName = customName;
        updatePiAuthUI();
        enterMainWorkspace();
        showToast(`Signed in as ${customName}`);
      }

      function onIncompletePaymentFound(payment) {
        if (payment && payment.identifier) {
          console.info('Incomplete Pi payment detected:', payment.identifier);
        }
      }

      async function initPiNetworkSDK() {
        if (!window.Pi) {
          updatePiAuthUI();
          return false;
        }
        if (state.piSession.sdkReady) return true;

        // Detect if running inside Pi Browser or embedded Pi iframe; avoid 120s timeout in regular desktop browsers
        const isPiBrowser = /PiBrowser/i.test(navigator.userAgent || '') || window.parent !== window;
        if (!isPiBrowser) {
          updatePiAuthUI();
          return false;
        }

        try {
          await Promise.race([
            window.Pi.init({ version: '2.0' }),
            new Promise((_, reject) => setTimeout(() => reject(new Error('Pi SDK init timeout')), 6000)),
          ]);
          state.piSession.sdkReady = true;
          updatePiAuthUI();
          return true;
        } catch (err) {
          console.warn('Pi SDK unavailable in this browser context:', err && err.message ? err.message : err);
          updatePiAuthUI();
          return false;
        }
      }

      function updatePiAuthUI() {
        const btn = document.getElementById('btn-pi-auth');
        const label = document.getElementById('pi-auth-label');
        const loginBtn = document.getElementById('btn-login-pi');
        const loginBtnLabel = document.getElementById('login-pi-btn-label');
        const studentInput = document.getElementById('input-student-name');
        if (!btn || !label) return;

        if (state.piSession.authenticating) {
          label.textContent = 'Signing in...';
          btn.disabled = true;
          if (loginBtn) loginBtn.disabled = true;
          if (loginBtnLabel) loginBtnLabel.textContent = 'Connecting to Pi Network...';
          return;
        }

        btn.disabled = false;
        if (loginBtn) loginBtn.disabled = false;
        if (loginBtnLabel) loginBtnLabel.textContent = 'Sign in with Pi';

        if (state.piSession.sessionToken && state.piSession.user && state.piSession.user.username) {
          label.textContent = `@${state.piSession.user.username}`;
          btn.classList.remove('text-amber-300', 'border-amber-400/40');
          btn.classList.add('text-[#10B981]', 'border-[#10B981]/50');
          btn.title = `Authenticated Pi Pioneer: @${state.piSession.user.username} (Click to switch account / sign out)`;
          if (studentInput) {
            studentInput.value = `@${state.piSession.user.username}`;
          }
        } else {
          const guestLabel = state.piSession.guestName || 'Guest';
          label.textContent = guestLabel;
          btn.classList.remove('text-amber-300', 'border-amber-400/40');
          btn.classList.add('text-[#22D3EE]', 'border-[#22D3EE]/40');
          btn.title = 'Click to open Pi Network or Guest Sign-In menu';
          if (studentInput) {
            studentInput.value = guestLabel;
          }
        }
      }

      function signOutPiUser() {
        state.piSession.sessionToken = null;
        state.piSession.user = null;
        state.piSession.isGuest = true;
        state.piSession.guestName = 'Guest';
        updatePiAuthUI();
        showLoginScreen();
        showToast('Pi Network session closed.');
      }

      async function authenticateWithPi() {
        if (state.piSession.authenticating) return;

        if (!window.Pi) {
          showToast('Pi SDK is unavailable in this browser. You can continue as a Guest.');
          return;
        }

        state.piSession.authenticating = true;
        updatePiAuthUI();

        try {
          const ready = await initPiNetworkSDK();
          if (!ready) {
            throw new Error('Open this app inside Pi Browser to Sign in with Pi, or continue as a Guest.');
          }

          // STEP 1: Authenticate in browser and keep ONLY accessToken (ignore browser-supplied uid/username)
          const authResult = await window.Pi.authenticate(['username'], onIncompletePaymentFound);
          const accessToken = authResult && authResult.accessToken;
          if (!accessToken) {
            throw new Error('No accessToken returned by Pi.authenticate.');
          }

          // STEP 2: Exchange accessToken with App Studio backend for trusted sessionToken and verified user identity
          const response = await fetch(PI_APP_STUDIO_LOGIN_URL, {
            method: 'POST',
            headers: {
              'Content-Type': 'application/json',
            },
            body: JSON.stringify({ accessToken }),
          });

          if (!response.ok) {
            throw new Error(`App Studio verification failed (HTTP ${response.status}).`);
          }

          const verified = await response.json();
          if (!verified || !verified.sessionToken || !verified.user || !verified.user.uid || !verified.user.username) {
            throw new Error('Invalid verification payload from App Studio.');
          }

          // Store only the verified sessionToken and App Studio returned user identity in memory
          state.piSession.sessionToken = verified.sessionToken;
          state.piSession.user = {
            uid: String(verified.user.uid),
            username: String(verified.user.username),
          };
          state.piSession.isGuest = false;

          enterMainWorkspace();
          showToast(`Successfully signed in as @${state.piSession.user.username}`);
        } catch (err) {
          console.error('Pi authentication error:', err);
          state.piSession.sessionToken = null;
          state.piSession.user = null;
          showToast(`Pi Auth: ${err && err.message ? err.message : 'Authentication cancelled'}`);
        } finally {
          state.piSession.authenticating = false;
          updatePiAuthUI();
        }
      }

      /* =========================================================================
       * 4. WEB AUDIO SYNTHESIZER FOR QUIZ & UI SOUND EFFECTS (NO EXTERNAL URLS)
       * ========================================================================= */
      let audioCtx = null;
      function playToneFeedback(type) {
        try {
          if (!audioCtx) {
            const Ctx = window.AudioContext || window.webkitAudioContext;
            if (Ctx) audioCtx = new Ctx();
          }
          if (!audioCtx) return;
          if (audioCtx.state === 'suspended') audioCtx.resume();

          const now = audioCtx.currentTime;
          const osc = audioCtx.createOscillator();
          const gain = audioCtx.createGain();
          osc.connect(gain);
          gain.connect(audioCtx.destination);

          if (type === 'success') {
            osc.type = 'sine';
            osc.frequency.setValueAtTime(523.25, now); // C5
            osc.frequency.setValueAtTime(659.25, now + 0.09); // E5
            osc.frequency.setValueAtTime(783.99, now + 0.18); // G5
            gain.gain.setValueAtTime(0.14, now);
            gain.gain.exponentialRampToValueAtTime(0.001, now + 0.42);
            osc.start(now);
            osc.stop(now + 0.42);
          } else if (type === 'error') {
            osc.type = 'triangle';
            osc.frequency.setValueAtTime(220, now);
            osc.frequency.linearRampToValueAtTime(145, now + 0.28);
            gain.gain.setValueAtTime(0.14, now);
            gain.gain.exponentialRampToValueAtTime(0.001, now + 0.32);
            osc.start(now);
            osc.stop(now + 0.32);
          } else {
            osc.type = 'sine';
            osc.frequency.setValueAtTime(440, now);
            gain.gain.setValueAtTime(0.05, now);
            gain.gain.exponentialRampToValueAtTime(0.001, now + 0.08);
            osc.start(now);
            osc.stop(now + 0.08);
          }
        } catch (e) {
          // Audio blocked or unsupported
        }
      }

      /* =========================================================================
       * 5. PROCEDURAL ORGANIC TEXTURE GENERATOR & 3D ANATOMICAL MODEL BUILDERS
       * ========================================================================= */
      function createOrganicTexture(baseHex, veinHex, noiseScale = 1) {
        const canvas = document.createElement('canvas');
        canvas.width = 256;
        canvas.height = 256;
        const ctx = canvas.getContext('2d');
        ctx.fillStyle = baseHex;
        ctx.fillRect(0, 0, 256, 256);

        // Subtle organic mottling
        for (let i = 0; i < 420; i++) {
          const x = Math.random() * 256;
          const y = Math.random() * 256;
          const r = (4 + Math.random() * 16) * noiseScale;
          ctx.fillStyle = i % 2 === 0 ? 'rgba(255,255,255,0.035)' : 'rgba(0,0,0,0.05)';
          ctx.beginPath();
          ctx.arc(x, y, r, 0, Math.PI * 2);
          ctx.fill();
        }

        // Fine vascular / fibrous striations
        ctx.strokeStyle = veinHex;
        ctx.lineWidth = 1.4;
        ctx.globalAlpha = 0.26;
        for (let i = 0; i < 28; i++) {
          ctx.beginPath();
          let x = Math.random() * 256;
          let y = Math.random() * 256;
          ctx.moveTo(x, y);
          for (let s = 0; s < 5; s++) {
            x += (Math.random() - 0.5) * 48;
            y += (Math.random() - 0.5) * 48;
            ctx.lineTo(x, y);
          }
          ctx.stroke();
        }
        const tex = new THREE.CanvasTexture(canvas);
        tex.wrapS = THREE.RepeatWrapping;
        tex.wrapT = THREE.RepeatWrapping;
        return tex;
      }

      const texCache = {};
      function getTissueMat(key, color, roughness = 0.42, clearcoat = 0.28, vein = '#581c1c') {
        if (!texCache[key]) {
          texCache[key] = createOrganicTexture(color, vein);
        }
        return new THREE.MeshPhysicalMaterial({
          map: texCache[key],
          color: new THREE.Color(color),
          roughness,
          metalness: 0.04,
          clearcoat,
          clearcoatRoughness: 0.35,
          side: THREE.DoubleSide,
        });
      }

      // Helper to mark sub-parts for Exploded Anatomy Mode
      function tagExplode(obj, dirVec, mag = 0.65) {
        obj.userData.basePos = obj.position.clone();
        obj.userData.explodeDir = dirVec.clone().normalize().multiplyScalar(mag);
        return obj;
      }

      /* --- REQUIRED PROCEDURAL MODEL BUILDERS --- */

      function createHeartModel() {
        const group = new THREE.Group();
        group.name = 'HeartModel';

        const myoMat = getTissueMat('heart_myo', '#b93842', 0.38, 0.45, '#4c0519');
        const rvMat = getTissueMat('heart_rv', '#c94a53', 0.4, 0.42, '#7f1d1d');
        const atriumMat = getTissueMat('heart_atr', '#9f2b36', 0.42, 0.35, '#450a0a');
        const aortaMat = getTissueMat('heart_aorta', '#e05a5a', 0.35, 0.5, '#991b1b');
        const venaMat = getTissueMat('heart_vena', '#3b82f6', 0.38, 0.45, '#1e3a8a');
        const pulmMat = getTissueMat('heart_pulm', '#60a5fa', 0.38, 0.45, '#1d4ed8');
        const fatMat = getTissueMat('heart_fat', '#eab308', 0.55, 0.2, '#a16207');

        // Left Ventricle (thick muscular cone tilted toward apex)
        const lvGeo = new THREE.SphereGeometry(0.76, 36, 32);
        lvGeo.scale(0.86, 1.32, 0.84);
        const lv = new THREE.Mesh(lvGeo, myoMat);
        lv.position.set(0.24, -0.22, 0.06);
        lv.rotation.z = -0.28;
        lv.name = 'LeftVentricle';
        tagExplode(lv, new THREE.Vector3(0.7, -0.5, 0.4), 0.6);
        group.add(lv);

        // Right Ventricle (crescent anterior wrap)
        const rvGeo = new THREE.SphereGeometry(0.66, 32, 28);
        rvGeo.scale(0.84, 1.15, 0.78);
        const rv = new THREE.Mesh(rvGeo, rvMat);
        rv.position.set(-0.24, -0.18, 0.22);
        rv.rotation.z = -0.18;
        rv.name = 'RightVentricle';
        tagExplode(rv, new THREE.Vector3(-0.7, -0.4, 0.6), 0.6);
        group.add(rv);

        // Right Atrium + Auricle
        const raGeo = new THREE.SphereGeometry(0.46, 28, 24);
        raGeo.scale(0.88, 1.05, 0.88);
        const ra = new THREE.Mesh(raGeo, atriumMat);
        ra.position.set(-0.56, 0.26, 0.08);
        ra.name = 'RightAtrium';
        tagExplode(ra, new THREE.Vector3(-0.9, 0.3, 0.2), 0.65);
        group.add(ra);

        // Left Atrium
        const laGeo = new THREE.SphereGeometry(0.44, 28, 24);
        const la = new THREE.Mesh(laGeo, atriumMat);
        la.position.set(0.38, 0.34, -0.24);
        la.name = 'LeftAtrium';
        tagExplode(la, new THREE.Vector3(0.7, 0.4, -0.7), 0.65);
        group.add(la);

        // Aortic Arch + 3 Superior Branches (TubeGeometry)
        const archCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(0.04, 0.35, 0.05),
          new THREE.Vector3(0.02, 0.92, 0.06),
          new THREE.Vector3(0.18, 1.25, -0.02),
          new THREE.Vector3(0.38, 1.05, -0.22),
          new THREE.Vector3(0.32, -0.45, -0.35),
        ]);
        const aorta = new THREE.Mesh(new THREE.TubeGeometry(archCurve, 44, 0.17, 20, false), aortaMat);
        aorta.name = 'AorticArch';
        tagExplode(aorta, new THREE.Vector3(0.2, 1.0, -0.2), 0.75);
        group.add(aorta);

        // Brachiocephalic, Left Common Carotid, Left Subclavian branches
        const branchOffsets = [
          [0.06, 1.18, 0.04, -0.08, 1.56, 0.05],
          [0.18, 1.25, -0.02, 0.14, 1.60, -0.02],
          [0.29, 1.20, -0.09, 0.34, 1.56, -0.10],
        ];
        branchOffsets.forEach((b, idx) => {
          const bc = new THREE.CatmullRomCurve3([
            new THREE.Vector3(b[0], b[1], b[2]),
            new THREE.Vector3(b[3], b[4], b[5]),
          ]);
          const bm = new THREE.Mesh(new THREE.TubeGeometry(bc, 12, 0.055, 12, false), aortaMat);
          tagExplode(bm, new THREE.Vector3(0.1 * (idx - 1), 1.1, 0), 0.8);
          group.add(bm);
        });

        // Superior & Inferior Vena Cava
        const svcCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(-0.52, 1.48, -0.04),
          new THREE.Vector3(-0.52, 0.65, 0.02),
        ]);
        const svc = new THREE.Mesh(new THREE.TubeGeometry(svcCurve, 20, 0.14, 18, false), venaMat);
        svc.name = 'SuperiorVenaCava';
        tagExplode(svc, new THREE.Vector3(-0.8, 0.8, 0), 0.7);
        group.add(svc);

        const ivcCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(-0.48, -0.22, -0.08),
          new THREE.Vector3(-0.48, -1.05, -0.12),
        ]);
        const ivc = new THREE.Mesh(new THREE.TubeGeometry(ivcCurve, 16, 0.14, 18, false), venaMat);
        tagExplode(ivc, new THREE.Vector3(-0.7, -0.8, -0.2), 0.65);
        group.add(ivc);

        // Pulmonary Trunk Bifurcation
        const pulmCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(-0.12, 0.25, 0.34),
          new THREE.Vector3(0.05, 0.76, 0.28),
          new THREE.Vector3(0.55, 0.84, 0.14),
        ]);
        const pulm = new THREE.Mesh(new THREE.TubeGeometry(pulmCurve, 28, 0.135, 18, false), pulmMat);
        pulm.name = 'PulmonaryTrunk';
        tagExplode(pulm, new THREE.Vector3(0.4, 0.7, 0.7), 0.7);
        group.add(pulm);

        const rightPulmCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(0.05, 0.76, 0.28),
          new THREE.Vector3(-0.68, 0.78, 0.06),
        ]);
        const rPulm = new THREE.Mesh(new THREE.TubeGeometry(rightPulmCurve, 18, 0.11, 16, false), pulmMat);
        tagExplode(rPulm, new THREE.Vector3(-0.6, 0.7, 0.4), 0.7);
        group.add(rPulm);

        // Anterior Interventricular (LAD) Coronary Artery + Epicardial Fat Cushion
        const ladCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(0.02, 0.32, 0.48),
          new THREE.Vector3(0.08, -0.12, 0.62),
          new THREE.Vector3(0.24, -0.68, 0.52),
        ]);
        const lad = new THREE.Mesh(new THREE.TubeGeometry(ladCurve, 28, 0.026, 10, false), aortaMat);
        tagExplode(lad, new THREE.Vector3(0.1, -0.2, 0.95), 0.65);
        group.add(lad);

        const fat = new THREE.Mesh(new THREE.TubeGeometry(ladCurve, 24, 0.055, 10, false), fatMat);
        tagExplode(fat, new THREE.Vector3(0.1, -0.2, 0.92), 0.65);
        group.add(fat);

        // Exposable rhythmic cardiac contraction loop on the Heart model
        group.userData.updateCardiacCycle = (elapsed, active = true) => {
          if (!active) {
            lv.scale.set(1, 1, 1);
            rv.scale.set(1, 1, 1);
            ra.scale.set(1, 1, 1);
            la.scale.set(1, 1, 1);
            aorta.scale.set(1, 1, 1);
            return;
          }
          // Double-peaked lub-dub physiological waveform (~72 bpm = 1.2 Hz)
          const phase = (elapsed * 1.2) % 1.0;
          const atrialSystole = Math.exp(-Math.pow((phase - 0.12) / 0.06, 2));
          const ventSystole = Math.exp(-Math.pow((phase - 0.32) / 0.09, 2));
          const aScale = 1 + 0.07 * atrialSystole - 0.03 * ventSystole;
          const vScale = 1 - 0.085 * ventSystole + 0.04 * atrialSystole;
          const aortaPulse = 1 + 0.05 * Math.exp(-Math.pow((phase - 0.38) / 0.08, 2));

          ra.scale.set(aScale, aScale, aScale);
          la.scale.set(aScale, aScale, aScale);
          lv.scale.set(vScale, 1 - 0.05 * ventSystole, vScale);
          rv.scale.set(vScale, 1 - 0.05 * ventSystole, vScale);
          aorta.scale.set(aortaPulse, 1, aortaPulse);
        };

        return group;
      }

      function createBrainModel() {
        const group = new THREE.Group();
        group.name = 'BrainModel';

        // Realistic Cortical Gyri/Sulci Tissue Palette matching the 6-view anatomical reference
        const cortexMat = getTissueMat('brain_cortex_v2', '#d4948e', 0.44, 0.36, '#7f1d1d');
        const cerebMat = getTissueMat('brain_cereb_v2', '#b87670', 0.52, 0.28, '#5c1916');
        const stemMat = getTissueMat('brain_stem_v2', '#e7cfc8', 0.38, 0.4, '#94746c');
        const chiasmMat = new THREE.MeshPhysicalMaterial({ color: 0xf5ebe6, roughness: 0.3, clearcoat: 0.45 });

        // Left & Right Cerebral Hemispheres with pronounced Gyri, Sulci & Sylvian Lateral Fissure
        [-1, 1].forEach((side) => {
          const hemiGeo = new THREE.SphereGeometry(0.88, 56, 44);
          const pos = hemiGeo.attributes.position;
          const v = new THREE.Vector3();
          for (let i = 0; i < pos.count; i++) {
            v.fromBufferAttribute(pos, i);
            // Flatten medial longitudinal fissure face cleanly
            if (side === -1 && v.x > 0) v.x *= 0.1;
            if (side === 1 && v.x < 0) v.x *= 0.1;

            // Multi-octave convoluted gyri & sulci folding
            const g1 = Math.sin(v.x * 13 + v.y * 8) * Math.cos(v.z * 12 - v.y * 7);
            const g2 = Math.sin(v.z * 21 + v.x * 15) * 0.45;
            const fold = 0.042 * (g1 + g2);

            // Lateral Sylvian fissure indentation
            const sylvianDist = Math.hypot((v.y + 0.06) * 2.4, (v.z - 0.12) * 1.1);
            const sylvianIndent = Math.abs(v.x) > 0.42 && sylvianDist < 0.42 ? -0.09 * (1 - sylvianDist / 0.42) : 0;

            v.multiplyScalar(1 + fold + sylvianIndent);
            v.x *= 0.68;
            v.y *= 0.86;
            v.z *= 1.22;
            if (v.y < -0.25) v.y *= 0.72;
            pos.setXYZ(i, v.x, v.y, v.z);
          }
          hemiGeo.computeVertexNormals();
          const hemi = new THREE.Mesh(hemiGeo, cortexMat);
          hemi.position.set(side * 0.045, 0.22, 0.04);
          tagExplode(hemi, new THREE.Vector3(side * 0.9, 0.35, 0), 0.65);
          group.add(hemi);
        });

        // Cerebellum (bilateral horizontally striated folia hemispheres)
        const cerebGeo = new THREE.SphereGeometry(0.47, 42, 30);
        const cPos = cerebGeo.attributes.position;
        for (let i = 0; i < cPos.count; i++) {
          const y = cPos.getY(i);
          const x = cPos.getX(i);
          const folia = 1 + 0.048 * Math.sin(y * 46);
          const vermisNotch = 1 - 0.12 * Math.exp(-(x * x) * 18);
          cPos.setX(i, x * 1.38 * folia);
          cPos.setY(i, y * 0.66);
          cPos.setZ(i, cPos.getZ(i) * 0.86 * folia * vermisNotch);
        }
        cerebGeo.computeVertexNormals();
        const cerebellum = new THREE.Mesh(cerebGeo, cerebMat);
        cerebellum.position.set(0, -0.46, -0.42);
        tagExplode(cerebellum, new THREE.Vector3(0, -0.6, -0.8), 0.7);
        group.add(cerebellum);

        // Ventral Optic Chiasm & Olfactory Tracts (visible in inferior view)
        [-1, 1].forEach((s) => {
          const optic = new THREE.Mesh(new THREE.CylinderGeometry(0.028, 0.032, 0.38, 12), chiasmMat);
          optic.position.set(s * 0.08, -0.26, 0.24);
          optic.rotation.set(1.25, 0, s * -0.45);
          group.add(optic);
        });

        // Brainstem (Pons bulge + Medulla Oblongata)
        const pons = new THREE.Mesh(new THREE.SphereGeometry(0.26, 26, 22), stemMat);
        pons.scale.set(1.06, 0.9, 1.15);
        pons.position.set(0, -0.42, -0.06);
        tagExplode(pons, new THREE.Vector3(0, -0.8, 0.1), 0.65);
        group.add(pons);

        const medulla = new THREE.Mesh(new THREE.CylinderGeometry(0.17, 0.125, 0.68, 22), stemMat);
        medulla.position.set(0, -0.78, -0.12);
        medulla.rotation.x = 0.18;
        tagExplode(medulla, new THREE.Vector3(0, -1.0, -0.1), 0.7);
        group.add(medulla);

        return group;
      }

      // Render 6-View Cerebral Multi-Projection Atlas Thumbnail for Brain Specimen
      function renderBrainMultiViewAtlas() {
        const canvas = document.getElementById('brain-atlas-canvas');
        if (!canvas) return;
        const ctx = canvas.getContext('2d');
        const w = canvas.width;
        const h = canvas.height;
        ctx.fillStyle = '#050B16';
        ctx.fillRect(0, 0, w, h);

        // Holographic grid lines
        ctx.strokeStyle = 'rgba(34, 211, 238, 0.14)';
        ctx.lineWidth = 1;
        ctx.beginPath();
        ctx.moveTo(w / 3, 0); ctx.lineTo(w / 3, h);
        ctx.moveTo((w * 2) / 3, 0); ctx.lineTo((w * 2) / 3, h);
        ctx.moveTo(0, h / 2); ctx.lineTo(w, h / 2);
        ctx.stroke();

        const views = [
          { label: 'ANTERIOR', cx: w * 0.167, cy: h * 0.24, rx: 34, ry: 36, mode: 'front' },
          { label: 'POSTERIOR', cx: w * 0.5, cy: h * 0.24, rx: 34, ry: 36, mode: 'back' },
          { label: 'LATERAL R', cx: w * 0.833, cy: h * 0.24, rx: 44, ry: 32, mode: 'sideR' },
          { label: 'LATERAL L', cx: w * 0.167, cy: h * 0.74, rx: 44, ry: 32, mode: 'sideL' },
          { label: 'SUPERIOR', cx: w * 0.5, cy: h * 0.74, rx: 32, ry: 42, mode: 'top' },
          { label: 'INFERIOR', cx: w * 0.833, cy: h * 0.74, rx: 32, ry: 42, mode: 'bottom' },
        ];

        views.forEach((v) => {
          ctx.save();
          ctx.translate(v.cx, v.cy);

          // Cerebellum & Brainstem silhouette for front/back/side
          if (v.mode === 'front' || v.mode === 'back' || v.mode === 'sideR' || v.mode === 'sideL') {
            ctx.fillStyle = '#9e5d58';
            ctx.beginPath();
            const offX = v.mode === 'sideR' ? -10 : v.mode === 'sideL' ? 10 : 0;
            ctx.ellipse(offX, 24, v.rx * 0.65, 13, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = '#d8b7b0';
            ctx.fillRect(offX - 5, 28, 10, 18);
          }

          // Main Cerebral Cortex silhouette
          const grad = ctx.createRadialGradient(-8, -10, 4, 0, 0, v.rx * 1.15);
          grad.addColorStop(0, '#ebb5ae');
          grad.addColorStop(0.65, '#c9827b');
          grad.addColorStop(1, '#854540');
          ctx.fillStyle = grad;
          ctx.strokeStyle = '#22D3EE';
          ctx.lineWidth = 1;
          ctx.beginPath();
          ctx.ellipse(0, -2, v.rx, v.ry, 0, 0, Math.PI * 2);
          ctx.fill();
          ctx.stroke();

          // Longitudinal fissure or lateral sulcus
          ctx.strokeStyle = '#5c2320';
          ctx.lineWidth = 1.8;
          ctx.beginPath();
          if (v.mode === 'front' || v.mode === 'back' || v.mode === 'top' || v.mode === 'bottom') {
            ctx.moveTo(0, -v.ry + 2);
            ctx.lineTo(0, v.ry - 2);
          } else {
            const dir = v.mode === 'sideR' ? 1 : -1;
            ctx.moveTo(-dir * 12, 4);
            ctx.quadraticCurveTo(dir * 6, 0, dir * 24, -10);
          }
          ctx.stroke();

          // Gyri sulci folds
          ctx.strokeStyle = 'rgba(92, 35, 32, 0.55)';
          ctx.lineWidth = 1.1;
          for (let i = -2; i <= 2; i++) {
            ctx.beginPath();
            ctx.arc(i * 10, -4 + (i % 2) * 6, 8, 0.2, Math.PI * 1.15);
            ctx.stroke();
          }

          // Optic chiasm X on inferior projection
          if (v.mode === 'bottom') {
            ctx.strokeStyle = '#F8FAFC';
            ctx.lineWidth = 2.2;
            ctx.beginPath();
            ctx.moveTo(-10, -14); ctx.lineTo(10, 4);
            ctx.moveTo(10, -14); ctx.lineTo(-10, 4);
            ctx.stroke();
          }

          ctx.fillStyle = '#22D3EE';
          ctx.font = '600 9px "JetBrains Mono", monospace';
          ctx.textAlign = 'center';
          ctx.fillText(v.label, 0, 48);
          ctx.restore();
        });
      }

      /* =========================================================================
       * 6. REMAINING PROCEDURAL ANATOMICAL BUILDERS & FULL BODY SCENE
       * ========================================================================= */
      function createEyeModel() {
        const group = new THREE.Group();
        group.name = 'EyeModel';
        const scleraMat = getTissueMat('eye_sclera', '#f8fafc', 0.25, 0.7, '#dc2626');
        const corneaMat = new THREE.MeshPhysicalMaterial({ color: 0xe0f2fe, transparent: true, opacity: 0.35, roughness: 0.08, clearcoat: 1.0 });
        const irisMat = new THREE.MeshStandardMaterial({ color: 0x0284c7, roughness: 0.4 });
        const pupilMat = new THREE.MeshBasicMaterial({ color: 0x050b16 });
        const lensMat = new THREE.MeshPhysicalMaterial({ color: 0xfef9c3, transparent: true, opacity: 0.65, roughness: 0.1 });
        const nerveMat = getTissueMat('eye_nerve', '#f1f5f9', 0.45, 0.3, '#94a3b8');

        const globe = new THREE.Mesh(new THREE.SphereGeometry(0.95, 40, 32), scleraMat);
        tagExplode(globe, new THREE.Vector3(0, 0, -0.3), 0.5);
        group.add(globe);

        const cornea = new THREE.Mesh(new THREE.SphereGeometry(0.45, 32, 24), corneaMat);
        cornea.position.set(0, 0, 0.78);
        tagExplode(cornea, new THREE.Vector3(0, 0, 1), 0.8);
        group.add(cornea);

        const iris = new THREE.Mesh(new THREE.RingGeometry(0.14, 0.36, 32), irisMat);
        iris.position.set(0, 0, 0.88);
        tagExplode(iris, new THREE.Vector3(0, 0, 0.9), 0.7);
        group.add(iris);

        const pupil = new THREE.Mesh(new THREE.CircleGeometry(0.14, 24), pupilMat);
        pupil.position.set(0, 0, 0.885);
        group.add(pupil);

        const lens = new THREE.Mesh(new THREE.SphereGeometry(0.32, 24, 18), lensMat);
        lens.scale.set(1, 1, 0.52);
        lens.position.set(0, 0, 0.62);
        tagExplode(lens, new THREE.Vector3(0, 0.2, 0.75), 0.65);
        group.add(lens);

        const opticCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(-0.08, -0.06, -0.9),
          new THREE.Vector3(-0.14, -0.14, -1.55),
        ]);
        const opticNerve = new THREE.Mesh(new THREE.TubeGeometry(opticCurve, 16, 0.13, 16, false), nerveMat);
        tagExplode(opticNerve, new THREE.Vector3(0, 0, -1), 0.7);
        group.add(opticNerve);

        return group;
      }

      function createEarModel() {
        const group = new THREE.Group();
        group.name = 'EarModel';
        const skinMat = getTissueMat('ear_skin', '#e2a78f', 0.48, 0.25, '#9a3412');
        const boneMat = getTissueMat('ear_bone', '#f1f5f9', 0.35, 0.4, '#94a3b8');
        const cochleaMat = getTissueMat('ear_cochlea', '#38bdf8', 0.3, 0.6, '#0369a1');
        const drumMat = new THREE.MeshPhysicalMaterial({ color: 0xfde68a, transparent: true, opacity: 0.75, roughness: 0.25, side: THREE.DoubleSide });

        // Auricle / Pinna
        const pinna = new THREE.Mesh(new THREE.TorusGeometry(0.45, 0.14, 16, 36, Math.PI * 1.45), skinMat);
        pinna.position.set(-0.88, 0.08, 0.15);
        pinna.rotation.set(0.1, 0.9, 0.4);
        tagExplode(pinna, new THREE.Vector3(-1, 0, 0), 0.7);
        group.add(pinna);

        // External Acoustic Meatus
        const canal = new THREE.Mesh(new THREE.CylinderGeometry(0.12, 0.11, 0.72, 20, 1, true), skinMat);
        canal.rotation.z = Math.PI / 2;
        canal.position.set(-0.48, 0, 0.12);
        group.add(canal);

        // Tympanic Membrane
        const drum = new THREE.Mesh(new THREE.CircleGeometry(0.16, 24), drumMat);
        drum.rotation.y = Math.PI / 2;
        drum.position.set(-0.12, 0, 0.12);
        tagExplode(drum, new THREE.Vector3(-0.3, 0, 0), 0.6);
        group.add(drum);

        // Ossicles (Malleus, Incus, Stapes)
        const ossicle = new THREE.Mesh(new THREE.BoxGeometry(0.28, 0.06, 0.06), boneMat);
        ossicle.position.set(0.08, 0.06, 0.1);
        tagExplode(ossicle, new THREE.Vector3(0, 0.6, 0), 0.65);
        group.add(ossicle);

        // 3 Semicircular Canals
        [
          [0, 0, 0],
          [Math.PI / 2, 0, 0],
          [0, Math.PI / 2, 0],
        ].forEach((rot, idx) => {
          const sc = new THREE.Mesh(new THREE.TorusGeometry(0.22, 0.032, 12, 28, Math.PI * 1.3), cochleaMat);
          sc.position.set(0.55, 0.34, -0.05);
          sc.rotation.set(rot[0] + idx * 0.2, rot[1], rot[2]);
          tagExplode(sc, new THREE.Vector3(0.7, 0.7, 0), 0.65);
          group.add(sc);
        });

        // Cochlea Spiral
        const pts = [];
        for (let i = 0; i <= 60; i++) {
          const t = (i / 60) * Math.PI * 5.2;
          const r = 0.28 * (1 - i / 75);
          pts.push(new THREE.Vector3(0.68 + Math.cos(t) * r, -0.18 + (i / 60) * 0.22, 0.14 + Math.sin(t) * r));
        }
        const cochlea = new THREE.Mesh(new THREE.TubeGeometry(new THREE.CatmullRomCurve3(pts), 64, 0.048, 12, false), cochleaMat);
        tagExplode(cochlea, new THREE.Vector3(0.9, -0.4, 0.2), 0.7);
        group.add(cochlea);

        return group;
      }

      function createNoseModel() {
        const group = new THREE.Group();
        group.name = 'NoseModel';
        const cartMat = getTissueMat('nose_cart', '#f1c2b0', 0.45, 0.3, '#be123c');
        const mucosaMat = getTissueMat('nose_muc', '#e11d48', 0.35, 0.55, '#881337');

        const pyramid = new THREE.Mesh(new THREE.ConeGeometry(0.52, 1.05, 4), cartMat);
        pyramid.position.set(0, 0.1, 0.22);
        pyramid.rotation.set(-0.35, Math.PI / 4, 0);
        tagExplode(pyramid, new THREE.Vector3(0, 0.3, 0.8), 0.65);
        group.add(pyramid);

        const septum = new THREE.Mesh(new THREE.BoxGeometry(0.05, 0.78, 0.85), mucosaMat);
        septum.position.set(0, 0.04, -0.05);
        group.add(septum);

        [-1, 1].forEach((side) => {
          [-0.18, 0.05, 0.26].forEach((yOff) => {
            const concha = new THREE.Mesh(new THREE.CylinderGeometry(0.065, 0.065, 0.65, 16), mucosaMat);
            concha.rotation.x = Math.PI / 2;
            concha.position.set(side * 0.24, yOff, -0.08);
            tagExplode(concha, new THREE.Vector3(side * 0.8, 0, 0), 0.6);
            group.add(concha);
          });
        });

        return group;
      }

      function createTongueModel() {
        const group = new THREE.Group();
        group.name = 'TongueModel';
        const tongueMat = getTissueMat('tongue_mat', '#e15b64', 0.44, 0.48, '#881337');
        const papillaMat = new THREE.MeshStandardMaterial({ color: 0xfda4af, roughness: 0.4 });

        const bodyGeo = new THREE.SphereGeometry(0.75, 36, 28);
        bodyGeo.scale(0.72, 0.36, 1.38);
        const body = new THREE.Mesh(bodyGeo, tongueMat);
        group.add(body);

        // V-shaped Circumvallate Papillae
        for (let i = -3; i <= 3; i++) {
          const p = new THREE.Mesh(new THREE.SphereGeometry(0.045, 12, 12), papillaMat);
          p.position.set(i * 0.12, 0.27, -0.25 - Math.abs(i) * 0.06);
          group.add(p);
        }

        const root = new THREE.Mesh(new THREE.CylinderGeometry(0.32, 0.38, 0.45, 20), tongueMat);
        root.position.set(0, -0.22, -0.35);
        tagExplode(root, new THREE.Vector3(0, -0.8, -0.3), 0.6);
        group.add(root);

        return group;
      }

      function createLungsModel() {
        const group = new THREE.Group();
        group.name = 'LungsModel';
        const lungMat = getTissueMat('lung_mat', '#f49097', 0.44, 0.38, '#9f1239');
        const trachMat = getTissueMat('trach_mat', '#e2e8f0', 0.35, 0.45, '#64748b');

        // Trachea & Cartilage Rings
        const trachea = new THREE.Mesh(new THREE.CylinderGeometry(0.13, 0.14, 1.15, 22), trachMat);
        trachea.position.set(0, 0.95, 0);
        tagExplode(trachea, new THREE.Vector3(0, 0.9, 0), 0.6);
        group.add(trachea);

        // Right & Left Lungs
        const rightLungGeo = new THREE.SphereGeometry(0.74, 34, 28);
        rightLungGeo.scale(0.72, 1.38, 0.78);
        const rightLung = new THREE.Mesh(rightLungGeo, lungMat);
        rightLung.position.set(-0.66, 0.02, 0.04);
        tagExplode(rightLung, new THREE.Vector3(-0.9, 0, 0), 0.7);
        group.add(rightLung);

        const leftLungGeo = new THREE.SphereGeometry(0.72, 34, 28);
        leftLungGeo.scale(0.68, 1.36, 0.76);
        const leftLung = new THREE.Mesh(leftLungGeo, lungMat);
        leftLung.position.set(0.66, 0.02, 0.04);
        tagExplode(leftLung, new THREE.Vector3(0.9, 0, 0), 0.7);
        group.add(leftLung);

        group.userData.updateRespiration = (elapsed, active = true) => {
          if (!active) {
            rightLung.scale.set(1, 1, 1);
            leftLung.scale.set(1, 1, 1);
            return;
          }
          const breath = 1 + 0.055 * Math.sin(elapsed * 1.5);
          rightLung.scale.set(breath, 1 + 0.03 * Math.sin(elapsed * 1.5), breath);
          leftLung.scale.set(breath, 1 + 0.03 * Math.sin(elapsed * 1.5), breath);
        };

        return group;
      }

      function createDigestiveSystemModel(focus = 'stomach') {
        const group = new THREE.Group();
        group.name = `Digestive_${focus}`;

        if (focus === 'liver') {
          const liverMat = getTissueMat('liver_mat', '#8c332b', 0.34, 0.55, '#450a0a');
          const gbMat = getTissueMat('gb_mat', '#10b981', 0.35, 0.6, '#065f46');
          const rightLobe = new THREE.Mesh(new THREE.SphereGeometry(0.78, 34, 26), liverMat);
          rightLobe.scale.set(1.15, 0.74, 0.76);
          rightLobe.position.set(-0.32, 0.05, 0.05);
          tagExplode(rightLobe, new THREE.Vector3(-0.7, 0.2, 0), 0.6);
          group.add(rightLobe);

          const leftLobe = new THREE.Mesh(new THREE.SphereGeometry(0.55, 28, 22), liverMat);
          leftLobe.scale.set(1.25, 0.56, 0.65);
          leftLobe.position.set(0.52, 0.1, 0.06);
          tagExplode(leftLobe, new THREE.Vector3(0.8, 0.2, 0), 0.6);
          group.add(leftLobe);

          const gb = new THREE.Mesh(new THREE.SphereGeometry(0.16, 20, 16), gbMat);
          gb.scale.set(0.75, 1.5, 0.75);
          gb.position.set(-0.28, -0.35, 0.24);
          tagExplode(gb, new THREE.Vector3(-0.3, -0.8, 0.4), 0.6);
          group.add(gb);
        } else if (focus === 'stomach') {
          const stomMat = getTissueMat('stom_mat', '#e69d94', 0.42, 0.45, '#9f1239');
          const curve = new THREE.CatmullRomCurve3([
            new THREE.Vector3(-0.15, 0.75, 0.04),
            new THREE.Vector3(0.24, 0.38, 0.12),
            new THREE.Vector3(0.32, -0.15, 0.16),
            new THREE.Vector3(-0.15, -0.45, 0.12),
            new THREE.Vector3(-0.62, -0.35, 0.06),
          ]);
          const body = new THREE.Mesh(new THREE.TubeGeometry(curve, 36, 0.34, 22, false), stomMat);
          group.add(body);
          const fundus = new THREE.Mesh(new THREE.SphereGeometry(0.36, 26, 22), stomMat);
          fundus.position.set(0.28, 0.54, 0.06);
          group.add(fundus);
        } else if (focus === 'pancreas') {
          const pancMat = getTissueMat('panc_mat', '#f3c677', 0.48, 0.32, '#b45309');
          const curve = new THREE.CatmullRomCurve3([
            new THREE.Vector3(-0.62, -0.22, 0.08),
            new THREE.Vector3(-0.25, -0.05, 0.12),
            new THREE.Vector3(0.22, 0.08, 0.1),
            new THREE.Vector3(0.72, 0.24, -0.04),
          ]);
          const gland = new THREE.Mesh(new THREE.TubeGeometry(curve, 32, 0.2, 18, false), pancMat);
          group.add(gland);
        } else if (focus === 'small_intestine') {
          const siMat = getTissueMat('si_mat', '#f2aba0', 0.42, 0.45, '#be123c');
          const pts = [];
          for (let i = 0; i <= 90; i++) {
            const t = i / 90;
            pts.push(new THREE.Vector3(Math.sin(t * Math.PI * 9) * 0.45, 0.55 - t * 1.1, Math.cos(t * Math.PI * 5) * 0.22));
          }
          const coils = new THREE.Mesh(new THREE.TubeGeometry(new THREE.CatmullRomCurve3(pts), 110, 0.13, 14, false), siMat);
          group.add(coils);
        } else if (focus === 'large_intestine') {
          const liMat = getTissueMat('li_mat', '#d98a7c', 0.44, 0.4, '#881337');
          const colonCurve = new THREE.CatmullRomCurve3([
            new THREE.Vector3(-0.62, -0.68, 0.12),
            new THREE.Vector3(-0.68, 0.52, 0.08),
            new THREE.Vector3(0.0, 0.58, 0.18),
            new THREE.Vector3(0.68, 0.5, 0.08),
            new THREE.Vector3(0.64, -0.52, 0.08),
            new THREE.Vector3(0.18, -0.65, 0.12),
            new THREE.Vector3(0.0, -0.92, 0.02),
          ]);
          const colon = new THREE.Mesh(new THREE.TubeGeometry(colonCurve, 64, 0.19, 18, false), liMat);
          group.add(colon);
        } else {
          // Rectum & Anus
          const recMat = getTissueMat('rec_mat', '#c96f6b', 0.45, 0.4, '#7f1d1d');
          const sphMat = getTissueMat('sph_mat', '#9f1239', 0.5, 0.3, '#4c0519');
          const canal = new THREE.Mesh(new THREE.CylinderGeometry(0.24, 0.18, 1.25, 24), recMat);
          group.add(canal);
          const sph = new THREE.Mesh(new THREE.TorusGeometry(0.24, 0.07, 14, 28), sphMat);
          sph.rotation.x = Math.PI / 2;
          sph.position.set(0, -0.38, 0);
          group.add(sph);
        }

        return group;
      }

      function createReproductiveSystemModel(focus = 'uterus') {
        const group = new THREE.Group();
        group.name = `Repro_${focus}`;
        const tissueMat = getTissueMat('repro_mat', '#df858d', 0.42, 0.45, '#881337');
        const gonadMat = getTissueMat('gonad_mat', '#f8fafc', 0.35, 0.5, '#cbd5e1');
        const ductMat = getTissueMat('duct_mat', '#e2b698', 0.45, 0.35, '#9a3412');

        if (focus === 'uterus' || focus === 'ovaries' || focus === 'fallopian_tubes' || focus === 'vagina' || focus === 'vulva') {
          const uterus = new THREE.Mesh(new THREE.ConeGeometry(0.48, 0.95, 28), tissueMat);
          uterus.rotation.x = Math.PI;
          uterus.position.set(0, 0.22, 0.08);
          tagExplode(uterus, new THREE.Vector3(0, 0.5, 0.2), 0.6);
          group.add(uterus);

          const vagina = new THREE.Mesh(new THREE.CylinderGeometry(0.2, 0.22, 0.72, 22), tissueMat);
          vagina.position.set(0, -0.45, 0.08);
          group.add(vagina);

          [-1, 1].forEach((side) => {
            const tubeCurve = new THREE.CatmullRomCurve3([
              new THREE.Vector3(side * 0.28, 0.52, 0.08),
              new THREE.Vector3(side * 0.62, 0.45, 0.05),
              new THREE.Vector3(side * 0.85, 0.14, 0.08),
            ]);
            const tube = new THREE.Mesh(new THREE.TubeGeometry(tubeCurve, 24, 0.045, 12, false), tissueMat);
            tagExplode(tube, new THREE.Vector3(side * 0.8, 0.5, 0), 0.6);
            group.add(tube);

            const ovary = new THREE.Mesh(new THREE.SphereGeometry(0.18, 22, 18), gonadMat);
            ovary.scale.set(1.25, 0.85, 0.75);
            ovary.position.set(side * 0.68, 0.06, 0.12);
            tagExplode(ovary, new THREE.Vector3(side * 0.9, -0.2, 0.2), 0.65);
            group.add(ovary);
          });
        } else {
          // Male Reproductive & Pelvic Organs (Testes, Scrotum, Penis, Prostate, Seminal Vesicles)
          if (focus === 'prostate' || focus === 'seminal_vesicles') {
            const gland = new THREE.Mesh(new THREE.SphereGeometry(0.45, 28, 22), tissueMat);
            gland.scale.set(1.15, 0.95, 0.95);
            group.add(gland);
            [-1, 1].forEach((side) => {
              const sv = new THREE.Mesh(new THREE.CylinderGeometry(0.08, 0.06, 0.45, 14), ductMat);
              sv.position.set(side * 0.34, 0.28, -0.05);
              sv.rotation.z = side * -0.45;
              tagExplode(sv, new THREE.Vector3(side * 0.7, 0.6, 0), 0.6);
              group.add(sv);
            });
          } else if (focus === 'penis') {
            const shaft = new THREE.Mesh(new THREE.CylinderGeometry(0.22, 0.24, 1.05, 24), tissueMat);
            shaft.position.set(0, -0.05, 0.15);
            group.add(shaft);
            const glans = new THREE.Mesh(new THREE.SphereGeometry(0.25, 24, 18), tissueMat);
            glans.position.set(0, -0.58, 0.15);
            group.add(glans);
          } else {
            // Testes & Scrotum
            if (focus === 'scrotum') {
              const sacMat = new THREE.MeshPhysicalMaterial({ color: 0xc29b87, transparent: true, opacity: 0.35, roughness: 0.55, side: THREE.DoubleSide });
              const sac = new THREE.Mesh(new THREE.SphereGeometry(0.95, 32, 24), sacMat);
              sac.scale.set(1.05, 1.02, 0.85);
              group.add(sac);
            }
            const septum = new THREE.Mesh(new THREE.BoxGeometry(0.04, 1.25, 0.65), ductMat);
            septum.position.set(0, -0.1, 0);
            group.add(septum);

            [-1, 1].forEach((side) => {
              const testis = new THREE.Mesh(new THREE.SphereGeometry(0.36, 26, 20), gonadMat);
              testis.scale.set(0.84, 1.25, 0.86);
              testis.position.set(side * 0.45, -0.1, 0.06);
              tagExplode(testis, new THREE.Vector3(side * 0.8, 0, 0), 0.6);
              group.add(testis);

              const cord = new THREE.Mesh(new THREE.CylinderGeometry(0.065, 0.065, 0.85, 14), ductMat);
              cord.position.set(side * 0.4, 0.55, 0);
              group.add(cord);
            });
          }
        }
        return group;
      }

      function createSupplementaryModel(id) {
        const group = new THREE.Group();
        group.name = `Supp_${id}`;
        const boneMat = getTissueMat('supp_bone', '#f1f5f9', 0.36, 0.4, '#94a3b8');
        const muscleMat = getTissueMat('supp_muscle', '#b91c1c', 0.46, 0.32, '#450a0a');
        const renalMat = getTissueMat('supp_renal', '#993b3b', 0.38, 0.5, '#450a0a');
        const skinMat = getTissueMat('supp_skin', '#e0a98f', 0.5, 0.25, '#9a3412');

        if (id === 'kidneys') {
          [-1, 1].forEach((side) => {
            const k = new THREE.Mesh(new THREE.SphereGeometry(0.45, 28, 22), renalMat);
            k.scale.set(0.75, 1.25, 0.65);
            k.position.set(side * 0.52, side === -1 ? -0.06 : 0.06, 0);
            tagExplode(k, new THREE.Vector3(side * 0.8, 0, 0), 0.6);
            group.add(k);

            const ureter = new THREE.Mesh(new THREE.CylinderGeometry(0.032, 0.028, 1.1, 12), boneMat);
            ureter.position.set(side * 0.38, -0.58, 0.04);
            group.add(ureter);
          });
        } else if (id === 'spleen') {
          const sp = new THREE.Mesh(new THREE.SphereGeometry(0.65, 32, 24), renalMat);
          sp.scale.set(0.68, 1.15, 0.88);
          group.add(sp);
        } else if (id === 'skin') {
          const epi = new THREE.Mesh(new THREE.BoxGeometry(1.4, 0.18, 1.1), skinMat);
          epi.position.y = 0.48;
          tagExplode(epi, new THREE.Vector3(0, 0.9, 0), 0.6);
          const derm = new THREE.Mesh(new THREE.BoxGeometry(1.4, 0.48, 1.1), muscleMat);
          derm.position.y = 0.12;
          const hypo = new THREE.Mesh(new THREE.BoxGeometry(1.4, 0.36, 1.1), new THREE.MeshStandardMaterial({ color: 0xfacc15, roughness: 0.55 }));
          hypo.position.y = -0.34;
          tagExplode(hypo, new THREE.Vector3(0, -0.9, 0), 0.6);
          group.add(epi, derm, hypo);
        } else if (id === 'spine') {
          for (let i = 0; i < 14; i++) {
            const y = 0.95 - i * 0.145;
            const z = Math.sin((i / 13) * Math.PI * 2) * 0.12;
            const vert = new THREE.Mesh(new THREE.CylinderGeometry(0.18, 0.19, 0.1, 18), boneMat);
            vert.position.set(0, y, z);
            group.add(vert);
          }
        } else if (id === 'skeletal' || id === 'muscular' || id === 'buttocks' || id === 'gluteus_maximus') {
          const mat = id === 'skeletal' ? boneMat : muscleMat;
          const torso = new THREE.Mesh(new THREE.CylinderGeometry(0.44, 0.38, 1.1, 24), mat);
          torso.position.y = 0.25;
          const leftLimb = new THREE.Mesh(new THREE.CylinderGeometry(0.18, 0.14, 0.95, 18), mat);
          leftLimb.position.set(-0.24, -0.62, 0);
          const rightLimb = new THREE.Mesh(new THREE.CylinderGeometry(0.18, 0.14, 0.95, 18), mat);
          rightLimb.position.set(0.24, -0.62, 0);
          group.add(torso, leftLimb, rightLimb);
        } else {
          const fallback = new THREE.Mesh(new THREE.SphereGeometry(0.75, 28, 22), renalMat);
          group.add(fallback);
        }

        return group;
      }

      function buildModelForSpecimen(spec) {
        switch (spec.builder) {
          case 'heart': return createHeartModel();
          case 'brain': return createBrainModel();
          case 'eye': return createEyeModel();
          case 'ear': return createEarModel();
          case 'nose': return createNoseModel();
          case 'tongue': return createTongueModel();
          case 'lungs': return createLungsModel();
          case 'liver':
          case 'stomach':
          case 'pancreas':
          case 'small_intestine':
          case 'large_intestine':
          case 'anus':
          case 'rectum':
            return createDigestiveSystemModel(spec.builder);
          case 'penis':
          case 'testes':
          case 'scrotum':
          case 'prostate':
          case 'seminal_vesicles':
          case 'vulva':
          case 'vagina':
          case 'uterus':
          case 'ovaries':
          case 'fallopian_tubes':
            return createReproductiveSystemModel(spec.builder);
          default:
            return createSupplementaryModel(spec.builder);
        }
      }

      function createFullBodySceneGroup(sex = 'female') {
        const root = new THREE.Group();
        root.name = 'FullBodyRoot';

        const shellLayer = new THREE.Group();
        shellLayer.name = 'BodyShellLayer';
        shellLayer.visible = state.showBodyShell;
        const shellMat = new THREE.MeshPhysicalMaterial({
          color: 0x38bdf8,
          transparent: true,
          opacity: 0.2,
          roughness: 0.25,
          depthWrite: false,
          side: THREE.DoubleSide,
        });

        const headShell = new THREE.Mesh(new THREE.SphereGeometry(0.32, 24, 20), shellMat);
        headShell.position.set(0, 1.38, 0);
        const torsoShell = new THREE.Mesh(new THREE.CylinderGeometry(0.46, 0.4, 1.25, 24), shellMat);
        torsoShell.position.set(0, 0.45, 0);
        shellLayer.add(headShell, torsoShell);

        [-1, 1].forEach((s) => {
          const arm = new THREE.Mesh(new THREE.CylinderGeometry(0.11, 0.09, 1.05, 16), shellMat);
          arm.position.set(s * 0.62, 0.42, 0);
          const leg = new THREE.Mesh(new THREE.CylinderGeometry(0.15, 0.11, 1.35, 16), shellMat);
          leg.position.set(s * 0.22, -0.85, 0);
          shellLayer.add(arm, leg);
        });
        root.add(shellLayer);

        const skeletonLayer = new THREE.Group();
        skeletonLayer.name = 'BodySkeletonLayer';
        skeletonLayer.visible = state.showBodySkeleton;
        const skelMat = new THREE.MeshStandardMaterial({ color: 0xe2e8f0, transparent: true, opacity: 0.55 });
        for (let i = 0; i < 10; i++) {
          const rib = new THREE.Mesh(new THREE.TorusGeometry(0.34, 0.018, 8, 24, Math.PI * 1.4), skelMat);
          rib.rotation.x = Math.PI / 2;
          rib.rotation.z = -Math.PI * 0.2;
          rib.position.set(0, 0.92 - i * 0.055, 0);
          skeletonLayer.add(rib);
        }
        root.add(skeletonLayer);

        // Interactive Tappable Organs Inside Body
        const organsLayer = new THREE.Group();
        organsLayer.name = 'BodyOrgansLayer';
        const placements = [
          { id: 'brain', pos: [0, 1.42, 0], scale: 0.24, color: 0xd4948e },
          { id: 'lungs', pos: [0, 0.78, 0.02], scale: 0.34, color: 0xf49097 },
          { id: 'heart', pos: [0.06, 0.74, 0.12], scale: 0.18, color: 0xe11d48 },
          { id: 'liver', pos: [-0.16, 0.46, 0.12], scale: 0.24, color: 0x8c332b },
          { id: 'stomach', pos: [0.16, 0.44, 0.12], scale: 0.2, color: 0xe69d94 },
          { id: 'kidneys', pos: [0, 0.34, -0.08], scale: 0.2, color: 0x993b3b },
          { id: 'small_intestine', pos: [0, 0.16, 0.12], scale: 0.25, color: 0xf2aba0 },
          { id: 'large_intestine', pos: [0, 0.18, 0.08], scale: 0.28, color: 0xd98a7c },
          { id: sex === 'male' ? 'prostate' : 'uterus', pos: [0, -0.08, 0.06], scale: 0.18, color: 0xdf858d },
        ];

        placements.forEach((p) => {
          const mesh = new THREE.Mesh(
            new THREE.SphereGeometry(p.scale, 20, 16),
            new THREE.MeshPhysicalMaterial({ color: p.color, roughness: 0.38, clearcoat: 0.4 })
          );
          mesh.position.set(p.pos[0], p.pos[1], p.pos[2]);
          mesh.userData.organId = p.id;
          organsLayer.add(mesh);
        });
        root.add(organsLayer);

        return root;
      }

      /* =========================================================================
       * 7. THREE.JS SCENE, LIGHTING, HOLOGRAPHIC PEDESTAL & PHYSIOLOGY PARTICLES
       * ========================================================================= */
      const container = document.getElementById('webgl-container');
      let scene, camera, renderer, controls;
      let splitCameraRight, splitControlsRight;
      let activeOrganGroup = null;
      let splitRightOrganGroup = null;
      let fullBodyGroup = null;
      let physParticleGroup = null;
      let physParticles = [];
      let holoScanPlaneMesh = null;
      let clippingPlanes = [];
      let raycaster, clock;
      let animFrameId = false;
      let isContextLost = false;

      function initThreeJS() {
        try {
          clock = new THREE.Clock();
          raycaster = new THREE.Raycaster();
          clippingPlanes = [new THREE.Plane(new THREE.Vector3(0, -1, 0), 0.2)];

          scene = new THREE.Scene();
          scene.fog = new THREE.FogExp2(0x050b16, 0.045);

          const w = container.clientWidth || 800;
          const h = container.clientHeight || 600;

          camera = new THREE.PerspectiveCamera(42, w / h, 0.1, 100);
          camera.position.set(0, 0.35, 3.6);

          splitCameraRight = new THREE.PerspectiveCamera(42, (w * 0.5) / h, 0.1, 100);
          splitCameraRight.position.set(12, 0.35, 3.6);

          renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true, preserveDrawingBuffer: true });
          renderer.setPixelRatio(Math.min(window.devicePixelRatio || 1, 2));
          renderer.setSize(w, h);
          renderer.localClippingEnabled = true;
          renderer.xr.enabled = true;
          container.innerHTML = '';
          container.appendChild(renderer.domElement);

          // WebGL Context Loss Recovery
          renderer.domElement.addEventListener('webglcontextlost', (e) => {
            e.preventDefault();
            isContextLost = true;
            showViewportStatus('WebGL context interrupted. Restoring holographic renderer...');
          });
          renderer.domElement.addEventListener('webglcontextrestored', () => {
            isContextLost = false;
            hideViewportStatus();
          });

          // OrbitControls (One-finger rotate, two-finger zoom/pan, mouse drag/wheel)
          controls = new THREE.OrbitControls(camera, renderer.domElement);
          controls.enableDamping = true;
          controls.dampingFactor = 0.07;
          controls.minDistance = 1.3;
          controls.maxDistance = 8.5;

          // Guard against Three.js r128 OrbitControls multi-touch race condition where state stays DOLLY_PAN with < 2 touches
          let orbitTouchCount = 0;
          renderer.domElement.addEventListener(
            'touchstart',
            (e) => {
              orbitTouchCount = e.touches ? e.touches.length : 0;
            },
            { capture: true, passive: true }
          );
          renderer.domElement.addEventListener(
            'touchend',
            (e) => {
              orbitTouchCount = e.touches ? e.touches.length : 0;
            },
            { capture: true, passive: true }
          );
          renderer.domElement.addEventListener(
            'touchcancel',
            () => {
              orbitTouchCount = 0;
            },
            { capture: true, passive: true }
          );
          renderer.domElement.addEventListener(
            'touchmove',
            (e) => {
              const touches = e.touches;
              const count = touches ? touches.length : 0;
              if (count === 0 || (orbitTouchCount >= 2 && count < 2)) {
                e.stopImmediatePropagation();
                orbitTouchCount = count;
                return;
              }
              if (count >= 2 && (!touches[0] || !touches[1])) {
                e.stopImmediatePropagation();
                return;
              }
              orbitTouchCount = count;
            },
            { capture: true, passive: true }
          );

          splitControlsRight = new THREE.OrbitControls(splitCameraRight, renderer.domElement);
          splitControlsRight.enableDamping = true;
          splitControlsRight.enableZoom = false;
          splitControlsRight.enablePan = false;
          splitControlsRight.enabled = false;
          splitControlsRight.target.set(12, 0, 0);

          // Three-Point Medical Studio Lighting
          const hemiLight = new THREE.HemisphereLight(0xe0f2fe, 0x0b1728, 0.95);
          scene.add(hemiLight);

          const keyLight = new THREE.DirectionalLight(0xffffff, 1.15);
          keyLight.position.set(3.5, 5.0, 4.5);
          scene.add(keyLight);

          const rimLight = new THREE.DirectionalLight(0x22d3ee, 0.85);
          rimLight.position.set(-4.0, 2.5, -3.5);
          scene.add(rimLight);

          // Glowing Cyan Holographic Pedestal
          const pedGroup = new THREE.Group();
          const disc = new THREE.Mesh(
            new THREE.CylinderGeometry(1.45, 1.55, 0.06, 48),
            new THREE.MeshStandardMaterial({ color: 0x0b1728, roughness: 0.4, metalness: 0.6 })
          );
          disc.position.y = -1.35;
          const ringOuter = new THREE.Mesh(
            new THREE.RingGeometry(1.46, 1.52, 64),
            new THREE.MeshBasicMaterial({ color: 0x22d3ee, side: THREE.DoubleSide })
          );
          ringOuter.rotation.x = -Math.PI / 2;
          ringOuter.position.y = -1.31;
          pedGroup.add(disc, ringOuter);
          scene.add(pedGroup);

          // Holographic Scan Sweep Disc
          holoScanPlaneMesh = new THREE.Mesh(
            new THREE.RingGeometry(0.02, 1.35, 48),
            new THREE.MeshBasicMaterial({ color: 0x22d3ee, transparent: true, opacity: 0.28, side: THREE.DoubleSide })
          );
          holoScanPlaneMesh.rotation.x = -Math.PI / 2;
          holoScanPlaneMesh.visible = false;
          scene.add(holoScanPlaneMesh);

          // Tap/Click Raycast inside Full Body Mode
          renderer.domElement.addEventListener('pointerup', (e) => {
            if (state.viewMode === 'fullbody') {
              handleFullBodyRaycast(e);
            }
          });

          window.addEventListener('resize', onViewportResize);
          hideViewportStatus();
          startAnimationLoop();
        } catch (err) {
          showViewportStatus(`WebGL Initialization Error: ${err.message}`);
        }
      }

      /* =========================================================================
       * 8. PHYSIOLOGY FLOW SIMULATION PARTICLES (BLOOD, RESPIRATION, DIGESTION, NERVE)
       * ========================================================================= */
      function buildPhysiologyParticles() {
        if (physParticleGroup) {
          scene.remove(physParticleGroup);
          disposeObject3D(physParticleGroup);
          physParticleGroup = null;
        }
        physParticles = [];

        const spec = SPECIMENS.find((s) => s.id === state.activeId);
        const mode = state.physSimMode === 'auto' ? (spec ? spec.phys_default : 'blood') : state.physSimMode;
        if (mode === 'off') return;

        physParticleGroup = new THREE.Group();
        scene.add(physParticleGroup);

        const arterialCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(-0.35, -0.75, 0.25),
          new THREE.Vector3(-0.15, 0.2, 0.35),
          new THREE.Vector3(0.18, 0.95, 0.1),
          new THREE.Vector3(0.45, -0.45, -0.2),
        ]);
        const venousCurve = new THREE.CatmullRomCurve3([
          new THREE.Vector3(0.35, -0.65, -0.25),
          new THREE.Vector3(0.05, 0.35, -0.28),
          new THREE.Vector3(-0.42, 0.75, 0.05),
          new THREE.Vector3(-0.32, -0.55, 0.22),
        ]);

        const colorA = mode === 'nervous' ? 0xfacc15 : mode === 'digestion' ? 0x10b981 : mode === 'respiration' ? 0x38bdf8 : 0xf43f5e;
        const colorB = mode === 'nervous' ? 0x22d3ee : mode === 'digestion' ? 0xf59e0b : 0x38bdf8;

        const matA = new THREE.MeshBasicMaterial({ color: colorA });
        const matB = new THREE.MeshBasicMaterial({ color: colorB });
        const sphereGeo = new THREE.SphereGeometry(0.028, 10, 10);

        for (let i = 0; i < 22; i++) {
          const m1 = new THREE.Mesh(sphereGeo, matA);
          physParticleGroup.add(m1);
          physParticles.push({ mesh: m1, curve: arterialCurve, offset: i / 22, speed: 0.24 });

          const m2 = new THREE.Mesh(sphereGeo, matB);
          physParticleGroup.add(m2);
          physParticles.push({ mesh: m2, curve: venousCurve, offset: i / 22, speed: 0.21 });
        }
      }

      /* =========================================================================
       * 9. SPECIMEN 3D MODEL LOADING, DISPOSAL, MATERIAL MODES & RAYCASTING
       * ========================================================================= */
      function disposeObject3D(obj) {
        if (!obj) return;
        obj.traverse((child) => {
          if (child.isMesh) {
            if (child.geometry) child.geometry.dispose();
            if (child.material) {
              const mats = Array.isArray(child.material) ? child.material : [child.material];
              mats.forEach((m) => {
                if (m && m.dispose) m.dispose();
              });
            }
          }
        });
      }

      function applyMaterialModes() {
        const targets = [];
        if (activeOrganGroup) targets.push(activeOrganGroup);
        if (splitRightOrganGroup) targets.push(splitRightOrganGroup);

        // Configure anatomical clipping plane
        const clipEnabled = state.clipPlaneAxis !== 'none' || state.holoScan;
        const axis = state.clipPlaneAxis !== 'none' ? state.clipPlaneAxis : 'axial';
        if (clippingPlanes.length > 0) {
          if (axis === 'axial') clippingPlanes[0].normal.set(0, -1, 0);
          else if (axis === 'sagittal') clippingPlanes[0].normal.set(-1, 0, 0);
          else if (axis === 'coronal') clippingPlanes[0].normal.set(0, 0, -1);
          clippingPlanes[0].constant = state.clipDist;
        }

        if (holoScanPlaneMesh) {
          holoScanPlaneMesh.visible = state.holoScan || state.animClip;
          if (axis === 'axial') {
            holoScanPlaneMesh.rotation.set(-Math.PI / 2, 0, 0);
            holoScanPlaneMesh.position.set(0, state.clipDist, 0);
          } else if (axis === 'sagittal') {
            holoScanPlaneMesh.rotation.set(0, Math.PI / 2, 0);
            holoScanPlaneMesh.position.set(state.clipDist, 0, 0);
          } else {
            holoScanPlaneMesh.rotation.set(0, 0, 0);
            holoScanPlaneMesh.position.set(0, 0, state.clipDist);
          }
        }

        targets.forEach((group) => {
          group.traverse((child) => {
            if (!child.isMesh || !child.material) return;
            const mats = Array.isArray(child.material) ? child.material : [child.material];
            mats.forEach((mat) => {
              if (!mat.userData.origProps) {
                mat.userData.origProps = {
                  transparent: mat.transparent,
                  opacity: mat.opacity !== undefined ? mat.opacity : 1,
                  depthWrite: mat.depthWrite !== undefined ? mat.depthWrite : true,
                };
              }
              mat.wireframe = state.wireframe;
              mat.clippingPlanes = clipEnabled ? clippingPlanes : [];
              mat.clipShadows = clipEnabled;

              if (state.xray) {
                mat.transparent = true;
                mat.opacity = Math.min(mat.userData.origProps.opacity, 0.34);
                mat.depthWrite = false;
              } else {
                mat.transparent = mat.userData.origProps.transparent;
                mat.opacity = mat.userData.origProps.opacity;
                mat.depthWrite = mat.userData.origProps.depthWrite;
              }
              mat.needsUpdate = true;
            });
          });
        });
      }

      function applyExplodedOffset() {
        const targets = [];
        if (activeOrganGroup) targets.push(activeOrganGroup);
        if (splitRightOrganGroup) targets.push(splitRightOrganGroup);

        targets.forEach((group) => {
          group.traverse((child) => {
            if (child.userData && child.userData.basePos && child.userData.explodeDir) {
              child.position
                .copy(child.userData.basePos)
                .addScaledVector(child.userData.explodeDir, state.explodeFactor);
            }
          });
        });
        updateHotspotScreenPositions();
      }

      function loadSpecimenModel(id) {
        if (!scene) return;
        const spec = SPECIMENS.find((s) => s.id === id);
        if (!spec) return;

        if (activeOrganGroup) {
          scene.remove(activeOrganGroup);
          disposeObject3D(activeOrganGroup);
          activeOrganGroup = null;
        }

        state.customModelLoaded = false;
        activeOrganGroup = buildModelForSpecimen(spec);
        activeOrganGroup.visible = state.viewMode !== 'fullbody';
        scene.add(activeOrganGroup);

        applyExplodedOffset();
        applyMaterialModes();
        buildPhysiologyParticles();
        renderHotspotPins();
      }

      function loadSplitRightModel(id) {
        if (!scene) return;
        const spec = SPECIMENS.find((s) => s.id === id);
        if (!spec) return;

        if (splitRightOrganGroup) {
          scene.remove(splitRightOrganGroup);
          disposeObject3D(splitRightOrganGroup);
          splitRightOrganGroup = null;
        }

        splitRightOrganGroup = buildModelForSpecimen(spec);
        splitRightOrganGroup.position.set(12, 0, 0);
        splitRightOrganGroup.visible = state.viewMode === 'split';
        scene.add(splitRightOrganGroup);

        applyExplodedOffset();
        applyMaterialModes();
      }

      function loadCustomGLB(url) {
        return new Promise((resolve, reject) => {
          const statusEl = document.getElementById('glb-load-status');
          if (!window.THREE || !window.THREE.GLTFLoader) {
            const err = new Error('GLTFLoader is unavailable.');
            if (statusEl) statusEl.textContent = err.message;
            showToast(err.message);
            reject(err);
            return;
          }

          if (statusEl) statusEl.textContent = 'Loading GLB/GLTF model...';
          const loader = new THREE.GLTFLoader();
          loader.load(
            url,
            (gltf) => {
              const model = gltf.scene;
              const box = new THREE.Box3().setFromObject(model);
              const size = box.getSize(new THREE.Vector3());
              const maxDim = Math.max(size.x, size.y, size.z) || 1;
              const scaleFactor = 1.85 / maxDim;
              model.scale.setScalar(scaleFactor);

              box.setFromObject(model);
              const center = box.getCenter(new THREE.Vector3());
              model.position.sub(center);

              if (activeOrganGroup) {
                scene.remove(activeOrganGroup);
                disposeObject3D(activeOrganGroup);
              }

              activeOrganGroup = new THREE.Group();
              activeOrganGroup.name = 'CustomGLBSpecimen';
              activeOrganGroup.add(model);
              scene.add(activeOrganGroup);

              state.customModelLoaded = true;
              applyMaterialModes();
              renderHotspotPins();
              updateInfoPanel();

              if (statusEl) statusEl.textContent = 'Custom GLB/GLTF loaded successfully.';
              document.getElementById('modal-glb').classList.add('hidden');
              showToast('Custom 3D GLB/GLTF model loaded!');
              resolve(model);
            },
            undefined,
            (err) => {
              const msg = `Failed to load GLB/GLTF: ${err && err.message ? err.message : 'Network or format error'}`;
              if (statusEl) statusEl.textContent = msg;
              showToast(msg);
              reject(err);
            }
          );
        });
      }

      function handleFullBodyRaycast(event) {
        if (!fullBodyGroup || !camera || !raycaster) return;
        const rect = renderer.domElement.getBoundingClientRect();
        const pointer = new THREE.Vector2(
          ((event.clientX - rect.left) / rect.width) * 2 - 1,
          -((event.clientY - rect.top) / rect.height) * 2 + 1
        );
        raycaster.setFromCamera(pointer, camera);
        const organsLayer = fullBodyGroup.getObjectByName('BodyOrgansLayer');
        if (!organsLayer) return;

        const hits = raycaster.intersectObjects(organsLayer.children, true);
        if (hits.length > 0 && hits[0].object.userData.organId) {
          const organId = hits[0].object.userData.organId;
          const spec = SPECIMENS.find((s) => s.id === organId);
          selectSpecimen(organId, false);
          if (spec) {
            showToast(`Selected inside Full Body: ${spec.name_en} / ${spec.name_id}`);
          }
        }
      }

      /* =========================================================================
       * 10. 3D-TO-2D HOTSPOT PROJECTION & INTERACTION
       * ========================================================================= */
      const hotspotsOverlay = document.getElementById('hotspots-overlay');
      let hotspotPinElements = [];

      function renderHotspotPins() {
        hotspotsOverlay.innerHTML = '';
        hotspotPinElements = [];

        const spec = SPECIMENS.find((s) => s.id === state.activeId);
        if (!spec || !state.showHotspots || state.viewMode === 'fullbody') return;

        spec.hotspots.forEach((hs) => {
          const btn = document.createElement('button');
          btn.type = 'button';
          btn.className = 'hotspot-pin pointer-events-auto';
          btn.textContent = String(hs.id);
          btn.setAttribute('aria-label', `Hotspot ${hs.id}: ${hs.name_en}`);
          btn.dataset.hotspotId = String(hs.id);

          if (state.selectedHotspotId === hs.id) {
            btn.classList.add('selected');
          }

          btn.addEventListener('click', (e) => {
            e.stopPropagation();
            onHotspotClicked(hs.id);
          });

          hotspotsOverlay.appendChild(btn);
          hotspotPinElements.push({ el: btn, hotspot: hs });
        });

        updateHotspotScreenPositions();
      }

      function updateHotspotScreenPositions() {
        if (!hotspotPinElements.length || !camera || !activeOrganGroup) return;
        const w = container.clientWidth;
        const h = container.clientHeight;
        const halfW = state.viewMode === 'split' ? w * 0.5 : w;
        const vec = new THREE.Vector3();

        hotspotPinElements.forEach(({ el, hotspot }) => {
          vec.set(hotspot.pos[0], hotspot.pos[1], hotspot.pos[2]);
          // Apply exploded factor if active
          vec.multiplyScalar(1 + state.explodeFactor * 0.35);
          // Transform by activeOrganGroup rotation/matrix
          vec.applyMatrix4(activeOrganGroup.matrixWorld);
          vec.project(camera);

          if (vec.z > 1) {
            el.style.opacity = '0';
            el.style.pointerEvents = 'none';
            return;
          }

          const x = (vec.x * 0.5 + 0.5) * halfW;
          const y = (-vec.y * 0.5 + 0.5) * h;

          if (x < 0 || x > halfW || y < 0 || y > h) {
            el.style.opacity = '0.25';
            el.style.pointerEvents = 'none';
          } else {
            el.style.opacity = '1';
            el.style.pointerEvents = 'auto';
          }
          el.style.left = `${x}px`;
          el.style.top = `${y}px`;
        });
      }

      function onHotspotClicked(hotspotId) {
        const spec = SPECIMENS.find((s) => s.id === state.activeId);
        if (!spec) return;
        const hs = spec.hotspots.find((h) => h.id === hotspotId);
        if (!hs) return;

        // If 3D Quiz Tab is active, validate answer!
        if (state.activeTab === 'quiz') {
          validateQuizAnswer(hotspotId);
          return;
        }

        playToneFeedback('click');
        state.selectedHotspotId = hotspotId;
        hotspotPinElements.forEach(({ el, hotspot }) => {
          el.classList.toggle('selected', hotspot.id === hotspotId);
        });

        // Switch to Structure tab if on Clinical
        if (state.activeTab !== 'structure') {
          switchRightTab('structure');
        }
        renderActiveHotspotDetail(hs);
      }

      function renderActiveHotspotDetail(hs) {
        const card = document.getElementById('active-hotspot-card');
        if (!hs) {
          card.innerHTML = `<p class="text-xs text-slate-400">Click any numbered pin (1–5) on the 3D model or above to inspect its anatomical structure, location, and function.</p>`;
          return;
        }
        const title = state.lang === 'id' ? hs.name_id : hs.name_en;
        const subTitle = state.lang === 'id' ? hs.name_en : hs.name_id;
        card.innerHTML = `
          <div class="flex items-center justify-between gap-2 mb-1">
            <span class="px-2 py-0.5 rounded-full bg-cyan-500/25 border border-cyan-400/50 text-[11px] font-mono font-bold text-cyan-300">PIN #${hs.id}</span>
            <span class="font-mono italic text-[11px] text-cyan-300">${hs.latin}</span>
          </div>
          <div class="font-display font-bold text-sm text-white">${title} <span class="text-xs font-normal text-slate-400">(${subTitle})</span></div>
          <div class="mt-2 space-y-1 text-xs">
            <div><span class="font-mono text-[10px] text-cyan-400 uppercase">Location:</span> <span class="text-slate-200">${hs.location}</span></div>
            <div><span class="font-mono text-[10px] text-emerald-400 uppercase">Function:</span> <span class="text-slate-200">${hs.func}</span></div>
            <p class="text-slate-300 pt-1 leading-relaxed">${hs.desc}</p>
          </div>
        `;
      }

      /* =========================================================================
       * 11. RENDERING LOOP, VIEWPORT RESIZE & SPLIT-SCREEN / WEBXR RENDERING
       * ========================================================================= */
      function onViewportResize() {
        if (!renderer || !camera) return;
        const w = container.clientWidth || 1;
        const h = container.clientHeight || 1;
        renderer.setSize(w, h);
        if (state.viewMode === 'split') {
          camera.aspect = (w * 0.5) / h;
          splitCameraRight.aspect = (w * 0.5) / h;
          splitCameraRight.updateProjectionMatrix();
        } else {
          camera.aspect = w / h;
        }
        camera.updateProjectionMatrix();
        updateHotspotScreenPositions();
      }

      function startAnimationLoop() {
        if (animFrameId) return;
        animFrameId = true;
        renderer.setAnimationLoop(() => {
          if (isContextLost) return;
          const elapsed = clock.getElapsedTime();

          // Smooth auto-rotation
          if (state.autoRotate) {
            if (activeOrganGroup && state.viewMode !== 'fullbody') activeOrganGroup.rotation.y += 0.006;
            if (splitRightOrganGroup && state.viewMode === 'split') splitRightOrganGroup.rotation.y += 0.006;
            if (fullBodyGroup && state.viewMode === 'fullbody') fullBodyGroup.rotation.y += 0.004;
          }

          // Living Physiology Animations (Heart systolic/diastolic beat, Lungs respiration, subtle pulse)
          if (activeOrganGroup) {
            if (activeOrganGroup.userData.updateCardiacCycle) {
              activeOrganGroup.userData.updateCardiacCycle(elapsed, state.livingPhysiology);
            } else if (activeOrganGroup.userData.updateRespiration) {
              activeOrganGroup.userData.updateRespiration(elapsed, state.livingPhysiology);
            } else if (state.livingPhysiology && state.viewMode !== 'fullbody') {
              const s = 1 + 0.018 * Math.sin(elapsed * 2.2);
              activeOrganGroup.scale.setScalar(s);
            } else if (!state.customModelLoaded) {
              activeOrganGroup.scale.setScalar(1);
            }
          }

          // Automated Holographic Volumetric Scan or Animate Clipping Sweep
          if (state.animClip || state.holoScan) {
            state.clipDist = Math.sin(elapsed * 1.1) * 1.15;
            document.getElementById('slider-clip-dist').value = state.clipDist.toFixed(2);
            applyMaterialModes();
          }

          // Animate Physiology Flow Particles
          if (physParticleGroup) {
            physParticleGroup.visible = state.viewMode !== 'split' && state.viewMode !== 'fullbody';
          }
          if (physParticles.length > 0 && state.viewMode === 'organ') {
            physParticles.forEach((p) => {
              const u = (elapsed * p.speed + p.offset) % 1.0;
              p.curve.getPointAt(u, p.mesh.position);
            });
          }

          controls.update();
          if (state.viewMode === 'split') {
            if (state.syncOrbit) {
              // Mirror primary camera relative offset to right comparison organ at X=12
              splitCameraRight.position.set(camera.position.x + 12, camera.position.y, camera.position.z);
              splitCameraRight.lookAt(12, 0, 0);
            } else {
              splitControlsRight.update();
            }
          }

          // Render Single or Split Viewport
          const w = container.clientWidth;
          const h = container.clientHeight;
          if (state.viewMode === 'split' && !renderer.xr.isPresenting) {
            renderer.setScissorTest(true);
            // Left Viewport
            renderer.setViewport(0, 0, w * 0.5, h);
            renderer.setScissor(0, 0, w * 0.5, h);
            renderer.render(scene, camera);
            // Right Viewport
            renderer.setViewport(w * 0.5, 0, w * 0.5, h);
            renderer.setScissor(w * 0.5, 0, w * 0.5, h);
            renderer.render(scene, splitCameraRight);
            renderer.setScissorTest(false);
          } else {
            renderer.setViewport(0, 0, w, h);
            renderer.render(scene, camera);
          }

          updateHotspotScreenPositions();
        });
      }

      /* =========================================================================
       * 12. CATALOG SEARCH, CATEGORY FILTERS & SPECIMEN SELECTION
       * ========================================================================= */
      function renderCategoryFilters() {
        const wrap = document.getElementById('category-filters');
        wrap.innerHTML = '';
        const dict = translations[state.locale] || translations[state.lang] || translations.en;
        CATEGORIES.forEach((cat) => {
          const btn = document.createElement('button');
          btn.type = 'button';
          const active = state.selectedCategory === cat.id;
          btn.className = `px-2.5 py-1 rounded-lg text-[11px] font-medium whitespace-nowrap transition shrink-0 ${
            active
              ? 'bg-cyan-500/25 text-cyan-200 border border-cyan-400/60'
              : 'holo-card text-[var(--text-secondary)] hover:text-cyan-300'
          }`;
          btn.textContent = dict[cat.key] || cat.id;
          btn.addEventListener('click', () => {
            state.selectedCategory = cat.id;
            renderCategoryFilters();
            renderCatalogList();
          });
          wrap.appendChild(btn);
        });
      }

      function renderCatalogList() {
        const listEl = document.getElementById('catalog-list');
        const countEl = document.getElementById('catalog-count');
        const q = state.searchQuery.trim().toLowerCase();

        const filtered = SPECIMENS.filter((spec) => {
          const catMatch = state.selectedCategory === 'all' || spec.categories.includes(state.selectedCategory);
          if (!catMatch) return false;
          if (!q) return true;
          return (
            spec.name_en.toLowerCase().includes(q) ||
            spec.name_id.toLowerCase().includes(q) ||
            spec.latin.toLowerCase().includes(q) ||
            spec.organ_system.toLowerCase().includes(q)
          );
        });

        countEl.textContent = String(filtered.length);
        listEl.innerHTML = '';

        if (!filtered.length) {
          listEl.innerHTML = `<div class="p-4 text-center text-xs text-slate-400">No matching anatomical specimens found.</div>`;
          return;
        }

        filtered.forEach((spec) => {
          const isSelected = spec.id === state.activeId;
          const card = document.createElement('button');
          card.type = 'button';
          card.className = `w-full text-left p-2.5 rounded-xl holo-card flex items-center gap-2.5 ${isSelected ? 'active' : ''}`;

          const brainThumbHtml = spec.id === 'brain'
            ? `<div class="w-11 h-11 rounded-lg bg-[#050B16] border border-[#22D3EE]/50 flex items-center justify-center shrink-0 overflow-hidden shadow-[0_0_10px_rgba(34,211,238,0.25)]" title="Brain 6-View Reference">
                <svg viewBox="0 0 64 64" class="w-10 h-10">
                  <ellipse cx="22" cy="30" rx="13" ry="18" fill="#d4948e" stroke="#22D3EE" stroke-width="1.2"/>
                  <ellipse cx="42" cy="30" rx="13" ry="18" fill="#c9827b" stroke="#22D3EE" stroke-width="1.2"/>
                  <path d="M16 22 Q24 26 18 34 M48 22 Q40 26 46 34" fill="none" stroke="#6b2622" stroke-width="1.5"/>
                  <ellipse cx="32" cy="48" rx="14" ry="6" fill="#9e5d58"/>
                </svg>
              </div>`
            : '';

          card.innerHTML = `
            ${brainThumbHtml}
            <div class="flex-1 min-w-0 flex flex-col gap-1">
              <div class="flex items-center justify-between gap-2">
                <span class="font-display font-bold text-xs text-white truncate">${spec.name_en}</span>
                <span class="px-1.5 py-0.5 rounded text-[10px] font-mono bg-[#22D3EE]/15 text-[#22D3EE] shrink-0">${spec.hotspots.length} pins</span>
              </div>
              <div class="text-[11px] text-[#22D3EE]/90 truncate">
                ${spec.name_id} <span class="text-slate-400">•</span> <span class="font-mono italic text-slate-300">${spec.latin}</span>
              </div>
              <div class="text-[10px] font-mono uppercase tracking-wider text-slate-400 truncate">${spec.organ_system}</div>
            </div>
          `;
          card.addEventListener('click', () => {
            selectSpecimen(spec.id, true);
            // Auto-close mobile/simulated drawer
            if (window.innerWidth < 1024 || state.device === 'tablet' || state.device === 'mobile') {
              document.getElementById('left-sidebar').classList.add('-translate-x-full');
            }
          });
          listEl.appendChild(card);
        });
      }

      function populateSplitRightSelector() {
        const sel = document.getElementById('select-split-right');
        sel.innerHTML = '';
        SPECIMENS.forEach((s) => {
          const opt = document.createElement('option');
          opt.value = s.id;
          opt.textContent = `${s.name_en} / ${s.name_id}`;
          if (s.id === state.splitRightId) opt.selected = true;
          sel.appendChild(opt);
        });
      }

      function selectSpecimen(id, switchToOrganView = false) {
        const spec = SPECIMENS.find((s) => s.id === id);
        if (!spec) return;

        state.activeId = id;
        state.selectedHotspotId = null;

        if (switchToOrganView && state.viewMode === 'fullbody') {
          setViewMode('organ');
        }

        // Update Header & Viewport Labels
        document.getElementById('header-organ-system').textContent = spec.organ_system;
        document.getElementById('header-name-en').textContent = spec.name_en;
        document.getElementById('header-name-id').textContent = spec.name_id;
        document.getElementById('header-latin').textContent = `(${spec.latin})`;

        document.getElementById('vp-system-badge').textContent = spec.organ_system;
        document.getElementById('vp-title-en').textContent = spec.name_en;
        document.getElementById('vp-title-id').textContent = spec.name_id;
        document.getElementById('vp-title-latin').textContent = spec.latin;

        renderCatalogList();
        loadSpecimenModel(id);
        updateInfoPanel();
        initQuizForSpecimen(id);
        populateTeacherQuestionSelect();
      }

      /* =========================================================================
       * 13. RIGHT INFORMATION PANEL (STRUCTURE, CLINICAL & 3D QUIZ ENGINE)
       * ========================================================================= */
      function updateInfoPanel() {
        const spec = SPECIMENS.find((s) => s.id === state.activeId);
        if (!spec) return;

        // Toggle 6-View Cerebral Atlas Card specifically for Brain specimen
        const brainAtlasCard = document.getElementById('brain-multiview-card');
        if (brainAtlasCard) {
          const isBrain = spec.id === 'brain';
          brainAtlasCard.classList.toggle('hidden', !isBrain);
          if (isBrain) renderBrainMultiViewAtlas();
        }

        document.getElementById('model-source-badge').textContent = state.customModelLoaded
          ? 'Custom GLB/GLTF model loaded'
          : 'Illustrative 3D procedural approximation';

        document.getElementById('info-overview').textContent = state.lang === 'id' ? spec.overview_id : spec.overview_en;
        document.getElementById('info-physiology').textContent = state.lang === 'id' ? spec.physiology_id : spec.physiology_en;

        document.getElementById('term-id').textContent = spec.name_id;
        document.getElementById('term-en').textContent = spec.name_en;
        document.getElementById('term-latin').textContent = spec.latin;
        document.getElementById('term-system').textContent = spec.organ_system;

        // 4 Biometric Information Cards
        const bioWrap = document.getElementById('biometric-cards');
        bioWrap.innerHTML = '';
        spec.metrics.forEach((m) => {
          const card = document.createElement('div');
          card.className = 'holo-card rounded-xl p-2.5';
          card.innerHTML = `
            <div class="text-[10px] font-mono uppercase text-cyan-400 truncate">${m.label}</div>
            <div class="font-display font-bold text-sm text-white mt-0.5">${m.val}</div>
            <div class="text-[10px] text-slate-400 leading-tight mt-0.5">${m.sub}</div>
          `;
          bioWrap.appendChild(card);
        });

        // Hotspot Quick Pills
        const pillsWrap = document.getElementById('hotspot-pills');
        pillsWrap.innerHTML = '';
        spec.hotspots.forEach((hs) => {
          const b = document.createElement('button');
          b.type = 'button';
          b.className = 'px-2.5 py-1 rounded-lg holo-card text-[11px] font-mono text-cyan-200 hover:text-white';
          b.textContent = `${hs.id}. ${state.lang === 'id' ? hs.name_id : hs.name_en}`;
          b.addEventListener('click', () => onHotspotClicked(hs.id));
          pillsWrap.appendChild(b);
        });

        renderActiveHotspotDetail(null);

        // Five Anatomical Learning Points
        const lpList = document.getElementById('learning-points-list');
        lpList.innerHTML = '';
        spec.learning_points.forEach((pt, i) => {
          const li = document.createElement('li');
          li.className = 'flex items-start gap-2 text-slate-200';
          li.innerHTML = `<span class="font-mono font-bold text-cyan-400 shrink-0">${i + 1}.</span><span>${pt}</span>`;
          lpList.appendChild(li);
        });

        // Tab B: Clinical
        document.getElementById('clin-diseases').textContent = spec.clinical.diseases;
        document.getElementById('clin-causes').textContent = spec.clinical.causes;
        document.getElementById('clin-symptoms').textContent = spec.clinical.symptoms;
        document.getElementById('clin-effects').textContent = spec.clinical.effects;
        document.getElementById('clin-prevention').textContent = spec.clinical.prevention;
      }

      function switchRightTab(tab) {
        state.activeTab = tab;
        ['structure', 'clinical', 'quiz'].forEach((t) => {
          const btn = document.getElementById(`tab-btn-${t}`);
          const pane = document.getElementById(`tab-content-${t}`);
          const isActive = t === tab;
          btn.className = isActive
            ? 'touch-btn py-1.5 px-2 rounded-lg text-xs font-semibold bg-sky-500/25 text-cyan-300 border border-cyan-400/40 transition'
            : 'touch-btn py-1.5 px-2 rounded-lg text-xs font-semibold text-[var(--text-secondary)] hover:text-cyan-300 transition';
          pane.classList.toggle('hidden', !isActive);
        });

        document.getElementById('viewport-quiz-banner').classList.toggle('hidden', tab !== 'quiz');
        if (tab === 'quiz') {
          renderCurrentQuizQuestion();
        }
      }

      /* --- 3D INTERACTIVE QUIZ ENGINE --- */
      function initQuizForSpecimen(specimenId) {
        const spec = SPECIMENS.find((s) => s.id === specimenId);
        if (!spec) return;
        const dict = translations[state.locale] || translations[state.lang] || translations.en;
        const tpl = dict.quiz_prompt_tpl || 'Click the pin identifying the {name} ({latin}).';

        const baseQuestions = spec.hotspots.map((hs) => {
          const hsName = state.lang === 'id' ? hs.name_id : hs.name_en;
          return {
            hotspotId: hs.id,
            prompt: tpl.replace('{name}', hsName).replace('{latin}', hs.latin),
          };
        });

        const extras = state.customQuestions[specimenId] || [];
        const combined = [...baseQuestions, ...extras];

        // Fisher-Yates shuffle
        for (let i = combined.length - 1; i > 0; i--) {
          const j = Math.floor(Math.random() * (i + 1));
          [combined[i], combined[j]] = [combined[j], combined[i]];
        }

        state.quizQueue = combined;
        state.quizIndex = 0;
        state.quizScore = 0;
        state.quizAttempts = 0;
        state.quizAnsweredCurrent = false;

        document.getElementById('quiz-complete-box').classList.add('hidden');
        document.getElementById('quiz-feedback').classList.add('hidden');
        updateQuizProgressUI();
        renderCurrentQuizQuestion();
      }

      function updateQuizProgressUI() {
        const total = state.quizQueue.length || 5;
        const pct = Math.round((state.quizIndex / total) * 100);
        document.getElementById('quiz-progress-bar').style.width = `${pct}%`;
        document.getElementById('quiz-progress-pct').textContent = `${pct}%`;
        document.getElementById('quiz-score-val').textContent = `${state.quizScore} / ${total}`;
        document.getElementById('quiz-attempts-val').textContent = String(state.quizAttempts);
      }

      function renderCurrentQuizQuestion() {
        const total = state.quizQueue.length;
        const pinBtns = document.getElementById('quiz-pin-buttons');
        pinBtns.innerHTML = '';

        // Reset pin colors
        hotspotPinElements.forEach(({ el }) => {
          el.classList.remove('quiz-correct', 'quiz-wrong');
        });

        if (state.quizIndex >= total) {
          document.getElementById('quiz-question-box').classList.add('hidden');
          document.getElementById('quiz-complete-box').classList.remove('hidden');
          document.getElementById('quiz-summary-text').textContent = `You scored ${state.quizScore} out of ${total} in ${state.quizAttempts} total attempts.`;
          document.getElementById('vp-quiz-prompt').textContent = `Quiz Completed! Score: ${state.quizScore}/${total}`;
          return;
        }

        document.getElementById('quiz-question-box').classList.remove('hidden');
        const q = state.quizQueue[state.quizIndex];
        document.getElementById('quiz-question-text').textContent = q.prompt;
        document.getElementById('vp-quiz-prompt').textContent = q.prompt;
        state.quizAnsweredCurrent = false;

        for (let i = 1; i <= 5; i++) {
          const b = document.createElement('button');
          b.type = 'button';
          b.className = 'touch-btn py-1.5 rounded-lg holo-card font-mono text-xs font-bold text-cyan-300 hover:text-white';
          b.textContent = `#${i}`;
          b.addEventListener('click', () => validateQuizAnswer(i));
          pinBtns.appendChild(b);
        }
      }

      function validateQuizAnswer(selectedPinId) {
        if (state.quizIndex >= state.quizQueue.length || state.quizAnsweredCurrent) return;
        const currentQ = state.quizQueue[state.quizIndex];
        state.quizAttempts++;

        const fb = document.getElementById('quiz-feedback');
        fb.classList.remove('hidden');

        if (selectedPinId === currentQ.hotspotId) {
          state.quizAnsweredCurrent = true;
          state.quizScore++;
          playToneFeedback('success');

          fb.className = 'rounded-xl p-3 text-xs font-medium bg-emerald-500/20 border border-emerald-400/50 text-emerald-200';
          fb.textContent = `Correct! Pin #${selectedPinId} identified accurately.`;

          const pinObj = hotspotPinElements.find((p) => p.hotspot.id === selectedPinId);
          if (pinObj) pinObj.el.classList.add('quiz-correct');

          state.quizIndex++;
          updateQuizProgressUI();
          setTimeout(() => {
            fb.classList.add('hidden');
            renderCurrentQuizQuestion();
          }, 1150);
        } else {
          playToneFeedback('error');
          fb.className = 'rounded-xl p-3 text-xs font-medium bg-rose-500/20 border border-rose-400/50 text-rose-200';
          fb.textContent = `Incorrect (Pin #${selectedPinId}). Try again to locate the requested structure.`;

          const pinObj = hotspotPinElements.find((p) => p.hotspot.id === selectedPinId);
          if (pinObj) pinObj.el.classList.add('quiz-wrong');
          updateQuizProgressUI();
        }
      }

      /* =========================================================================
       * 14. VIEW MODES (ORGAN / FULL BODY / SPLIT), SNAPSHOT & WEBXR VR/AR
       * ========================================================================= */
      function setViewMode(mode) {
        state.viewMode = mode;

        ['organ', 'fullbody', 'split'].forEach((m) => {
          const btn = document.getElementById(`mode-${m}`);
          const active = m === mode;
          btn.className = active
            ? 'touch-btn px-2.5 py-1 rounded-lg text-xs font-medium transition bg-sky-500/25 text-cyan-300 border border-cyan-400/40 flex items-center gap-1.5'
            : 'touch-btn px-2.5 py-1 rounded-lg text-xs font-medium transition text-[var(--text-secondary)] hover:text-cyan-300 flex items-center gap-1.5';
        });

        document.getElementById('fullbody-controls').classList.toggle('hidden', mode !== 'fullbody');
        document.getElementById('fullbody-controls').classList.toggle('flex', mode === 'fullbody');
        document.getElementById('split-controls').classList.toggle('hidden', mode !== 'split');
        document.getElementById('split-divider').classList.toggle('hidden', mode !== 'split');

        if (mode === 'fullbody') {
          if (activeOrganGroup) activeOrganGroup.visible = false;
          if (splitRightOrganGroup) splitRightOrganGroup.visible = false;
          if (!fullBodyGroup) {
            fullBodyGroup = createFullBodySceneGroup(state.bodySex);
            scene.add(fullBodyGroup);
          }
          fullBodyGroup.visible = true;
          camera.position.set(0, 0.25, 4.4);
          controls.target.set(0, 0.1, 0);
        } else {
          if (fullBodyGroup) fullBodyGroup.visible = false;
          if (activeOrganGroup) activeOrganGroup.visible = true;
          if (mode === 'split') {
            loadSplitRightModel(state.splitRightId);
            if (splitRightOrganGroup) splitRightOrganGroup.visible = true;
          } else if (splitRightOrganGroup) {
            splitRightOrganGroup.visible = false;
          }
          camera.position.set(0, 0.35, 3.6);
          controls.target.set(0, 0, 0);
        }

        onViewportResize();
        renderHotspotPins();
      }

      function exportStudySnapshotPNG() {
        try {
          if (!renderer || !scene || !camera) return;
          const w = container.clientWidth;
          const h = container.clientHeight;
          if (state.viewMode === 'split') {
            renderer.setScissorTest(true);
            renderer.setViewport(0, 0, w * 0.5, h);
            renderer.setScissor(0, 0, w * 0.5, h);
            renderer.render(scene, camera);
            renderer.setViewport(w * 0.5, 0, w * 0.5, h);
            renderer.setScissor(w * 0.5, 0, w * 0.5, h);
            renderer.render(scene, splitCameraRight);
            renderer.setScissorTest(false);
          } else {
            renderer.setViewport(0, 0, w, h);
            renderer.render(scene, camera);
          }
          const dataURL = renderer.domElement.toDataURL('image/png');
          const spec = SPECIMENS.find((s) => s.id === state.activeId);
          const link = document.createElement('a');
          link.download = `HumanAnatomy3D_${spec ? spec.id : 'specimen'}_${Date.now()}.png`;
          link.href = dataURL;
          document.body.appendChild(link);
          link.click();
          document.body.removeChild(link);
          showToast('High-resolution PNG study snapshot saved!');
        } catch (err) {
          showToast('Snapshot export unavailable in current context.');
        }
      }

      async function enterWebXRMode() {
        if (!navigator.xr) {
          showToast('WebXR is not supported by this browser. Use a WebXR-compatible headset or browser.');
          return;
        }
        try {
          const vrSupported = await navigator.xr.isSessionSupported('immersive-vr');
          const arSupported = await navigator.xr.isSessionSupported('immersive-ar');
          if (!vrSupported && !arSupported) {
            showToast('No VR/AR headset detected. Connect a WebXR headset to enter immersive mode.');
            return;
          }
          const sessionMode = vrSupported ? 'immersive-vr' : 'immersive-ar';
          const session = await navigator.xr.requestSession(sessionMode, {
            optionalFeatures: ['local-floor', 'bounded-floor'],
          });
          await renderer.xr.setSession(session);
          showToast(`Entered WebXR (${sessionMode}) mode.`);
        } catch (err) {
          showToast(`WebXR session notice: ${err.message}`);
        }
      }

      /* =========================================================================
       * 15. TEXT-TO-SPEECH (WEB SPEECH API WITH GRACEFUL FALLBACK)
       * ========================================================================= */
      function initSpeechVoices() {
        if (!('speechSynthesis' in window)) return;
        const populate = () => {
          const voices = window.speechSynthesis.getVoices();
          const sel = document.getElementById('tts-voice');
          if (!voices.length) return;
          sel.innerHTML = '<option value="">Default Browser Voice</option>';
          voices.forEach((v, idx) => {
            const opt = document.createElement('option');
            opt.value = String(idx);
            opt.textContent = `${v.name} (${v.lang})`;
            sel.appendChild(opt);
          });
        };
        populate();
        window.speechSynthesis.onvoiceschanged = populate;
      }

      function speakActiveTab() {
        if (!('speechSynthesis' in window)) {
          showToast('Browser Text-to-Speech API is unavailable on this device.');
          return;
        }
        window.speechSynthesis.cancel();
        const spec = SPECIMENS.find((s) => s.id === state.activeId);
        if (!spec) return;

        let text = '';
        if (state.activeTab === 'structure') {
          const ov = state.lang === 'id' ? spec.overview_id : spec.overview_en;
          const ph = state.lang === 'id' ? spec.physiology_id : spec.physiology_en;
          text = `${spec.name_en}. ${spec.latin}. ${ov} ${ph}`;
        } else if (state.activeTab === 'clinical') {
          text = `Clinical Overview for ${spec.name_en}. ${spec.clinical.diseases}. Causes: ${spec.clinical.causes}. Prevention: ${spec.clinical.prevention}`;
        } else {
          text = document.getElementById('quiz-question-text').textContent;
        }

        const utter = new SpeechSynthesisUtterance(text);
        utter.lang = state.lang === 'id' ? 'id-ID' : 'en-US';
        utter.rate = parseFloat(document.getElementById('tts-rate').value) || 1.0;

        const voiceIdx = document.getElementById('tts-voice').value;
        const voices = window.speechSynthesis.getVoices();
        if (voiceIdx !== '' && voices[Number(voiceIdx)]) {
          utter.voice = voices[Number(voiceIdx)];
        }
        window.speechSynthesis.speak(utter);
      }

      /* =========================================================================
       * 16. I18N UI UPDATER, THEME & DEVICE PREVIEW PROFILES, SMART TV REMOTE
       * ========================================================================= */
      const WELCOME_LOCALES = {
        en: {
          flag: '🇬🇧',
          code: 'EN',
          quote: '“There is a piece of flesh in the body: when it is sound, the whole body is sound, and when it is corrupt, the whole body is corrupt—and that piece is the heart.”',
          subtitle: 'Interactive 3D Human Anatomy Virtual Laboratory — Explore Organ Structures, Physiology Simulations & Medical Quizzes.',
          enterBtn: 'ENTER LABORATORY',
          footerLeft: '32 INTERACTIVE ORGAN SPECIMENS',
          loginBadge: 'USER ACCESS',
          loginTitle: 'Sign In to HUMAN ANATOMY 3D',
          loginDesc: 'Sign in with your Pi Network account to save your learning identity, or continue as a Guest without a Pi account.',
          loginPiBtn: 'Sign in with Pi',
          loginOr: 'OR',
          guestLabel: 'GUEST DISPLAY NAME (OPTIONAL)',
          guestPlaceholder: 'e.g., Medical Student / Guest 01',
          guestBtn: 'Continue as Guest (No Pi Account)',
          backBtn: '← Back to Welcome',
          loginFooterRight: 'Open Education Mode',
        },
        id: {
          flag: '🇮🇩',
          code: 'ID',
          quote: '“Di dalam tubuh terdapat segumpal daging: apabila ia baik, maka baiklah seluruh tubuh, dan apabila ia rusak, maka rusaklah seluruh tubuh—ketahuilah bahwa segumpal daging itu adalah jantung.”',
          subtitle: 'Laboratorium Virtual Anatomi Tubuh Manusia 3D Interaktif — Eksplorasi Struktur Organ, Simulasi Fisiologi & Kuis Medis.',
          enterBtn: 'MASUK KE LABORATORIUM',
          footerLeft: '32 ORGAN SPESIMEN INTERAKTIF',
          loginBadge: 'AKSES PENGGUNA',
          loginTitle: 'Login ke HUMAN ANATOMY 3D',
          loginDesc: 'Masuk menggunakan akun Pi Network untuk menyimpan identitas pembelajaran Anda, atau lanjutkan sebagai Tamu (Guest) tanpa akun Pi.',
          loginPiBtn: 'Masuk dengan Pi Network',
          loginOr: 'ATAU',
          guestLabel: 'NAMA TAMPILAN GUEST (OPSIONAL)',
          guestPlaceholder: 'Contoh: Mahasiswa Kedokteran / Guest 01',
          guestBtn: 'Masuk sebagai Guest (Tanpa Akun Pi)',
          backBtn: '← Kembali ke Welcome',
          loginFooterRight: 'Mode Edukasi Terbuka',
        },
        de: {
          flag: '🇩🇪',
          code: 'DE',
          quote: '„Im Körper gibt es ein Stück Fleisch: Wenn es gesund ist, ist der ganze Körper gesund, und wenn es verdorben ist, ist der ganze Körper verdorben – und dieses Stück ist das Herz.“',
          subtitle: 'Interaktives virtuelles 3D-Labor für menschliche Anatomie — Organstrukturen, Physiologie-Simulationen & medizinische Quizze entdecken.',
          enterBtn: 'LABOR BETRETEN',
          footerLeft: '32 INTERAKTIVE ORGANPRÄPARATE',
          loginBadge: 'BENUTZERZUGANG',
          loginTitle: 'Bei HUMAN ANATOMY 3D anmelden',
          loginDesc: 'Melden Sie sich mit Ihrem Pi-Network-Konto an, um Ihre Lernidentität zu speichern, oder fahren Sie als Gast fort.',
          loginPiBtn: 'Mit Pi anmelden',
          loginOr: 'ODER',
          guestLabel: 'GAST-ANZEIGENAME (OPTIONAL)',
          guestPlaceholder: 'z. B. Medizinstudent / Gast 01',
          guestBtn: 'Als Gast fortfahren (ohne Pi-Konto)',
          backBtn: '← Zurück zur Startseite',
          loginFooterRight: 'Offener Bildungsmodus',
        },
        fr: {
          flag: '🇫🇷',
          code: 'FR',
          quote: '« Il y a dans le corps un morceau de chair : s’il est sain, tout le corps est sain, et s’il est corrompu, tout le corps est corrompu — et ce morceau est le cœur. »',
          subtitle: 'Laboratoire virtuel interactif d’anatomie humaine 3D — Explorez les structures des organes, simulations physiologiques et quiz médicaux.',
          enterBtn: 'ENTRER AU LABORATOIRE',
          footerLeft: '32 SPÉCIMENS D’ORGANES INTERACTIFS',
          loginBadge: 'ACCÈS UTILISATEUR',
          loginTitle: 'Connexion à HUMAN ANATOMY 3D',
          loginDesc: 'Connectez-vous avec votre compte Pi Network pour enregistrer votre identité d’apprentissage, ou continuez en tant qu’invité.',
          loginPiBtn: 'Se connecter avec Pi',
          loginOr: 'OU',
          guestLabel: 'NOM D’AFFICHAGE INVITÉ (OPTIONNEL)',
          guestPlaceholder: 'ex. Étudiant en médecine / Invité 01',
          guestBtn: 'Continuer en tant qu’invité (sans compte Pi)',
          backBtn: '← Retour à l’accueil',
          loginFooterRight: 'Mode Éducation Ouverte',
        },
        es: {
          flag: '🇪🇸',
          code: 'ES',
          quote: '“Hay en el cuerpo un trozo de carne: si está sano, todo el cuerpo está sano, y si está corrupto, todo el cuerpo está corrupto; y ese trozo es el corazón.”',
          subtitle: 'Laboratorio virtual interactivo de anatomía humana 3D — Explora estructuras de órganos, simulaciones fisiológicas y cuestionarios médicos.',
          enterBtn: 'ENTRAR AL LABORATORIO',
          footerLeft: '32 ESPECÍMENES DE ÓRGANOS INTERACTIVOS',
          loginBadge: 'ACCESO DE USUARIO',
          loginTitle: 'Iniciar sesión en HUMAN ANATOMY 3D',
          loginDesc: 'Inicia sesión con tu cuenta de Pi Network para guardar tu identidad de aprendizaje, o continúa como invitado sin cuenta Pi.',
          loginPiBtn: 'Iniciar sesión con Pi',
          loginOr: 'O',
          guestLabel: 'NOMBRE DE INVITADO (OPCIONAL)',
          guestPlaceholder: 'ej. Estudiante de Medicina / Invitado 01',
          guestBtn: 'Continuar como invitado (sin cuenta Pi)',
          backBtn: '← Volver a la bienvenida',
          loginFooterRight: 'Modo Educación Abierta',
        },
        ru: {
          flag: '🇷🇺',
          code: 'RU',
          quote: '«В теле есть кусочек плоти: если он здоров, то здорово и всё тело, а если он испорчен, то испорчено и всё тело — и этот кусочек есть сердце».',
          subtitle: 'Интерактивная виртуальная лаборатория 3D-анатомии человека — изучайте строение органов, физиологические симуляции и медицинские тесты.',
          enterBtn: 'ВОЙТИ В ЛАБОРАТОРИЮ',
          footerLeft: '32 ИНТЕРАКТИВНЫХ ОБРАЗЦА ОРГАНОВ',
          loginBadge: 'ДОСТУП ПОЛЬЗОВАТЕЛЯ',
          loginTitle: 'Вход в HUMAN ANATOMY 3D',
          loginDesc: 'Войдите с помощью аккаунта Pi Network, чтобы сохранить профиль обучения, или продолжите как гость.',
          loginPiBtn: 'Войти через Pi',
          loginOr: 'ИЛИ',
          guestLabel: 'ИМЯ ГОСТЯ (НЕОБЯЗАТЕЛЬНО)',
          guestPlaceholder: 'например, Студент-медик / Гость 01',
          guestBtn: 'Продолжить как гость (без аккаунта Pi)',
          backBtn: '← Назад на главную',
          loginFooterRight: 'Открытый образовательный режим',
        },
        'zh-CN': {
          flag: '🇨🇳',
          code: 'ZH',
          quote: '“人体内有一块肉，它若健全，全身皆健全；它若败坏，全身皆败坏——这块肉便是心脏。”',
          subtitle: '交互式 3D 人体解剖学虚拟实验室 — 探索器官结构、生理模拟与医学测验。',
          enterBtn: '进入实验室',
          footerLeft: '32 个交互式器官标本',
          loginBadge: '用户登录',
          loginTitle: '登录 HUMAN ANATOMY 3D',
          loginDesc: '使用您的 Pi Network 账户登录以保存学习身份，或无需 Pi 账户以访客身份继续。',
          loginPiBtn: '使用 Pi 账户登录',
          loginOr: '或',
          guestLabel: '访客显示名称（可选）',
          guestPlaceholder: '例如：医学生 / 访客 01',
          guestBtn: '以访客身份继续（无需 Pi 账户）',
          backBtn: '← 返回欢迎页',
          loginFooterRight: '开放教育模式',
        },
        ko: {
          flag: '🇰🇷',
          code: 'KO',
          quote: '“몸 안에는 한 조각의 살이 있으니, 그것이 건강하면 온몸이 건강하고 그것이 병들면 온몸이 병드나니, 그 조각은 바로 심장이다.”',
          subtitle: '대화형 3D 인체 해부학 가상 실험실 — 장기 구조, 생리학 시뮬레이션 및 의학 퀴즈를 탐구하세요.',
          enterBtn: '실험실 입장',
          footerLeft: '32개 대화형 장기 표본',
          loginBadge: '사용자 접속',
          loginTitle: 'HUMAN ANATOMY 3D 로그인',
          loginDesc: 'Pi Network 계정으로 로그인하여 학습 프로필을 저장하거나, Pi 계정 없이 게스트로 계속하세요.',
          loginPiBtn: 'Pi로 로그인',
          loginOr: '또는',
          guestLabel: '게스트 표시 이름 (선택 사항)',
          guestPlaceholder: '예: 의대생 / 게스트 01',
          guestBtn: '게스트로 계속하기 (Pi 계정 불필요)',
          backBtn: '← 환영 화면으로 돌아가기',
          loginFooterRight: '개방형 교육 모드',
        },
        ja: {
          flag: '🇯🇵',
          code: 'JA',
          quote: '「体の中には一つの肉塊があり、それが健全であれば全身が健全となり、それが損なわれれば全身が損なわれる。その肉塊とは心臓である。」',
          subtitle: 'インタラクティブ3D人体解剖学バーチャルラボ — 臓器構造・生理シミュレーション・医学クイズを体験。',
          enterBtn: 'ラボに入る',
          footerLeft: '32種類のインタラクティブ臓器標本',
          loginBadge: 'ユーザーアクセス',
          loginTitle: 'HUMAN ANATOMY 3D にログイン',
          loginDesc: 'Pi Networkアカウントでログインして学習IDを保存するか、Piアカウントなしでゲストとして続行してください。',
          loginPiBtn: 'Pi でサインイン',
          loginOr: 'または',
          guestLabel: 'ゲスト表示名（任意）',
          guestPlaceholder: '例：医学生 / ゲスト 01',
          guestBtn: 'ゲストとして続行（Piアカウント不要）',
          backBtn: '← ウェルカム画面に戻る',
          loginFooterRight: 'オープン教育モード',
        },
        vi: {
          flag: '🇻🇳',
          code: 'VI',
          quote: '“Trong cơ thể có một miếng thịt: khi nó lành mạnh thì toàn thân lành mạnh, khi nó hư hỏng thì toàn thân hư hỏng — và miếng thịt đó chính là trái tim.”',
          subtitle: 'Phòng thí nghiệm ảo Giải phẫu Người 3D Tương tác — Khám phá cấu trúc cơ quan, mô phỏng sinh lý & trắc nghiệm y khoa.',
          enterBtn: 'VÀO PHÒNG THÍ NGHIỆM',
          footerLeft: '32 MẪU CƠ QUAN TƯƠNG TÁC',
          loginBadge: 'TRUY CẬP NGƯỜI DÙNG',
          loginTitle: 'Đăng nhập HUMAN ANATOMY 3D',
          loginDesc: 'Đăng nhập bằng tài khoản Pi Network để lưu danh tính học tập, hoặc tiếp tục với tư cách Khách.',
          loginPiBtn: 'Đăng nhập bằng Pi',
          loginOr: 'HOẶC',
          guestLabel: 'TÊN HIỂN THỊ KHÁCH (TÙY CHỌN)',
          guestPlaceholder: 'VD: Sinh viên Y khoa / Khách 01',
          guestBtn: 'Tiếp tục với tư cách Khách (Không cần Pi)',
          backBtn: '← Quay lại trang chào mừng',
          loginFooterRight: 'Chế độ Giáo dục Mở',
        },
        th: {
          flag: '🇹🇭',
          code: 'TH',
          quote: '“ในร่างกายมีก้อนเนื้ออยู่ก้อนหนึ่ง หากมันดี ร่างกายทั้งหมดก็จะดี และหากมันเสื่อมเสีย ร่างกายทั้งหมดก็จะเสื่อมเสีย — และก้อนเนื้อนั้นคือหัวใจ”',
          subtitle: 'ห้องปฏิบัติการเสมือนจริงกายวิภาคศาสตร์มนุษย์ 3 มิติ — สำรวจโครงสร้างอวัยวะ การจำลองสรีรวิทยา และแบบทดสอบทางการแพทย์',
          enterBtn: 'เข้าสู่ห้องปฏิบัติการ',
          footerLeft: 'ตัวอย่างอวัยวะเชิงโต้ตอบ 32 ชิ้น',
          loginBadge: 'การเข้าถึงของผู้ใช้',
          loginTitle: 'เข้าสู่ระบบ HUMAN ANATOMY 3D',
          loginDesc: 'เข้าสู่ระบบด้วยบัญชี Pi Network เพื่อบันทึกข้อมูลการเรียนรู้ หรือดำเนินการต่อในฐานะผู้เยี่ยมชมโดยไม่ต้องใช้บัญชี Pi',
          loginPiBtn: 'เข้าสู่ระบบด้วย Pi',
          loginOr: 'หรือ',
          guestLabel: 'ชื่อที่แสดงของผู้เยี่ยมชม (ไม่บังคับ)',
          guestPlaceholder: 'เช่น นักศึกษาแพทย์ / ผู้เยี่ยมชม 01',
          guestBtn: 'ดำเนินการต่อในฐานะผู้เยี่ยมชม (ไม่ต้องใช้บัญชี Pi)',
          backBtn: '← กลับสู่หน้าต้อนรับ',
          loginFooterRight: 'โหมดการศึกษาแบบเปิด',
        },
        hi: {
          flag: '🇮🇳',
          code: 'HI',
          quote: '“शरीर में मांस का एक टुकड़ा है: जब वह स्वस्थ होता है तो पूरा शरीर स्वस्थ रहता है, और जब वह विकृत होता है तो पूरा शरीर विकृत हो जाता है — और वह टुकड़ा हृदय है।”',
          subtitle: 'इंटरैक्टिव 3D मानव शरीर रचना वर्चुअल प्रयोगशाला — अंग संरचनाओं, शरीर क्रिया विज्ञान सिमुलेशन और चिकित्सा क्विज़ का अन्वेषण करें।',
          enterBtn: 'प्रयोगशाला में प्रवेश करें',
          footerLeft: '32 इंटरैक्टिव अंग नमूने',
          loginBadge: 'उपयोगकर्ता पहुंच',
          loginTitle: 'HUMAN ANATOMY 3D में साइन इन करें',
          loginDesc: 'अपनी शिक्षण पहचान सहेजने के लिए अपने Pi Network खाते से साइन इन करें, या बिना Pi खाते के अतिथि के रूप में जारी रखें।',
          loginPiBtn: 'Pi के साथ साइन इन करें',
          loginOr: 'या',
          guestLabel: 'अतिथि प्रदर्शन नाम (वैकल्पिक)',
          guestPlaceholder: 'उदा. मेडिकल छात्र / अतिथि 01',
          guestBtn: 'अतिथि के रूप में जारी रखें (बिना Pi खाते के)',
          backBtn: '← स्वागत पृष्ठ पर वापस जाएं',
          loginFooterRight: 'मुक्त शिक्षा मोड',
        },
        ar: {
          flag: '🇸🇦',
          code: 'AR',
          quote: '«أَلَا وَإِنَّ فِي الْجَسَدِ مُضْغَةً: إِذَا صَلَحَتْ صَلَحَ الْجَسَدُ كُلُّهُ، وَإِذَا فَسَدَتْ فَسَدَ الْجَسَدُ كُلُّهُ، أَلَا وَهِيَ الْقَلْبُ.»',
          subtitle: 'المختبر الافتراضي التفاعلي للتشريح البشري ثلاثي الأبعاد — استكشف بنية الأعضاء والمحاكاة الفسيولوجية والاختبارات الطبية.',
          enterBtn: 'ادخل إلى المختبر',
          footerLeft: '32 عينة أعضاء تفاعلية',
          loginBadge: 'دخول المستخدم',
          loginTitle: 'تسجيل الدخول إلى HUMAN ANATOMY 3D',
          loginDesc: 'سجّل الدخول بحساب Pi Network لحفظ هويتك التعليمية، أو تابع كضيف بدون حساب Pi.',
          loginPiBtn: 'تسجيل الدخول عبر Pi',
          loginOr: 'أو',
          guestLabel: 'اسم عرض الضيف (اختياري)',
          guestPlaceholder: 'مثال: طالب طب / ضيف 01',
          guestBtn: 'المتابعة كضيف (بدون حساب Pi)',
          backBtn: '← العودة إلى شاشة الترحيب',
          loginFooterRight: 'وضع التعليم المفتوح',
        },
      };

      function triggerGoogleTranslateLanguage(targetLang) {
        if (!targetLang || targetLang === 'en') {
          const combo = document.querySelector('.goog-te-combo');
          if (combo) {
            combo.value = 'en';
            combo.dispatchEvent(new Event('change'));
          }
          return;
        }
        const applyCombo = () => {
          const combo = document.querySelector('.goog-te-combo');
          if (combo) {
            combo.value = targetLang;
            combo.dispatchEvent(new Event('change'));
          }
        };
        if (document.querySelector('.goog-te-combo')) {
          applyCombo();
        } else {
          const box = document.getElementById('gtranslate-box');
          if (box && !box.dataset.loaded) {
            box.dataset.loaded = '1';
            window.googleTranslateElementInit = function () {
              if (window.google && window.google.translate) {
                new window.google.translate.TranslateElement(
                  { pageLanguage: 'en', includedLanguages: 'en,id,de,fr,es,ru,zh-CN,ko,ja,vi,th,hi,ar' },
                  'google_translate_element'
                );
                setTimeout(applyCombo, 400);
              }
            };
            const s = document.createElement('script');
            s.src = 'https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit';
            s.onerror = () => {};
            document.body.appendChild(s);
          }
        }
      }

      function applyLanguage(lang) {
        const chosenLocale = translations[lang] ? lang : 'en';
        const baseLang = lang === 'id' ? 'id' : 'en';
        state.locale = chosenLocale;
        state.lang = baseLang;
        const dict = translations[chosenLocale] || translations.en;

        document.querySelectorAll('[data-i18n]').forEach((el) => {
          const key = el.getAttribute('data-i18n');
          if (dict[key]) el.textContent = dict[key];
        });

        // Update Welcome Page & Login Page Texts & Flag Indicator
        const loc = WELCOME_LOCALES[chosenLocale] || WELCOME_LOCALES.en;
        const enFallback = WELCOME_LOCALES.en;
        const flagEl = document.getElementById('welcome-lang-flag');
        const codeEl = document.getElementById('welcome-lang-label');
        if (flagEl) flagEl.textContent = loc.flag;
        if (codeEl) codeEl.textContent = loc.code;

        const qEl = document.getElementById('welcome-quote-text');
        const subEl = document.getElementById('welcome-subtitle-text');
        const enterEl = document.getElementById('welcome-enter-btn-text');
        const footLeftEl = document.getElementById('welcome-footer-left');
        if (qEl) qEl.textContent = loc.quote || enFallback.quote;
        if (subEl) subEl.textContent = loc.subtitle || enFallback.subtitle;
        if (enterEl) enterEl.textContent = loc.enterBtn || enFallback.enterBtn;
        if (footLeftEl) footLeftEl.textContent = loc.footerLeft || enFallback.footerLeft;

        const lBadge = document.getElementById('login-badge-text');
        const lTitle = document.getElementById('login-title-text');
        const lDesc = document.getElementById('login-desc-text');
        const lPiBtn = document.getElementById('login-pi-btn-label');
        const lOr = document.getElementById('login-or-text');
        const lGuestLbl = document.getElementById('login-guest-label');
        const lGuestInp = document.getElementById('input-guest-name');
        const lGuestBtn = document.getElementById('login-guest-btn-text');
        const lBackBtn = document.getElementById('btn-back-welcome');
        const lFootR = document.getElementById('login-footer-right');
        if (lBadge) lBadge.textContent = loc.loginBadge || enFallback.loginBadge;
        if (lTitle) lTitle.textContent = loc.loginTitle || enFallback.loginTitle;
        if (lDesc) lDesc.textContent = loc.loginDesc || enFallback.loginDesc;
        if (lPiBtn) lPiBtn.textContent = loc.loginPiBtn || enFallback.loginPiBtn;
        if (lOr) lOr.textContent = loc.loginOr || enFallback.loginOr;
        if (lGuestLbl) lGuestLbl.textContent = loc.guestLabel || enFallback.guestLabel;
        if (lGuestInp) lGuestInp.placeholder = loc.guestPlaceholder || enFallback.guestPlaceholder;
        if (lGuestBtn) lGuestBtn.textContent = loc.guestBtn || enFallback.guestBtn;
        if (lBackBtn) lBackBtn.textContent = loc.backBtn || enFallback.backBtn;
        if (lFootR) lFootR.textContent = loc.loginFooterRight || enFallback.loginFooterRight;

        const mainLangSelect = document.getElementById('select-lang');
        if (mainLangSelect && mainLangSelect.value !== chosenLocale) {
          mainLangSelect.value = chosenLocale;
        }

        if (chosenLocale !== 'en' && chosenLocale !== 'id') {
          triggerGoogleTranslateLanguage(chosenLocale);
        } else {
          triggerGoogleTranslateLanguage('en');
        }

        renderCategoryFilters();
        renderCatalogList();
        updateInfoPanel();
        initQuizForSpecimen(state.activeId);
      }

      function applyTheme(mode) {
        state.theme = mode;
        const html = document.documentElement;
        if (mode === 'light') {
          html.classList.add('light-theme');
        } else if (mode === 'dark') {
          html.classList.remove('light-theme');
        } else {
          const prefersLight = window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches;
          html.classList.toggle('light-theme', prefersLight);
        }
      }

      function applyDevicePreview(profile) {
        state.device = profile;
        const shell = document.getElementById('app-shell');
        const leftSb = document.getElementById('left-sidebar');
        const rightPn = document.getElementById('right-panel');

        shell.classList.remove('preview-tablet', 'preview-mobile', 'preview-tv', 'tv-focus-mode');

        if (profile === 'tablet' || profile === 'mobile') {
          shell.classList.add(profile === 'tablet' ? 'preview-tablet' : 'preview-mobile');
          leftSb.classList.add('-translate-x-full');
          rightPn.classList.add('translate-x-full');
          showToast(`Layout Preview: ${profile === 'tablet' ? 'Tablet' : 'Smartphone'} profile`);
        } else if (profile === 'tv') {
          shell.classList.add('preview-tv', 'tv-focus-mode');
          showToast('Layout Preview: Smart TV (Use Arrow Keys, Enter, WASD & +/-)');
        } else {
          showToast(`Layout Preview: ${profile === 'laptop' ? 'Laptop' : 'Desktop / Smartboard'} profile`);
        }
        setTimeout(onViewportResize, 360);
      }

      /* =========================================================================
       * 17. TEACHER & STUDENT MODE ANALYTICS
       * ========================================================================= */
      function populateTeacherQuestionSelect() {
        const spec = SPECIMENS.find((s) => s.id === state.activeId);
        if (!spec) return;
        document.getElementById('tb-organ-name').textContent = spec.name_en;
        const sel = document.getElementById('tb-hotspot-select');
        sel.innerHTML = '';
        spec.hotspots.forEach((h) => {
          const opt = document.createElement('option');
          opt.value = String(h.id);
          opt.textContent = `Pin #${h.id}: ${h.name_en}`;
          sel.appendChild(opt);
        });
      }

      function renderQuizReportsTable() {
        const tbody = document.getElementById('report-tbody');
        if (!state.quizReports.length) {
          tbody.innerHTML = `<tr><td colspan="5" class="py-3 text-center text-slate-400">No quiz sessions logged yet.</td></tr>`;
          return;
        }
        tbody.innerHTML = state.quizReports
          .map(
            (r) => `
          <tr>
            <td class="py-1.5 font-medium">${r.student}</td>
            <td class="py-1.5 text-cyan-300">${r.organ}</td>
            <td class="py-1.5 text-emerald-400 font-mono">${r.score}</td>
            <td class="py-1.5 font-mono">${r.attempts}</td>
            <td class="py-1.5 text-slate-400">${r.time}</td>
          </tr>`
          )
          .join('');
      }

      /* =========================================================================
       * 18. UI EVENT BINDINGS & TOAST HELPERS
       * ========================================================================= */
      let toastTimer = null;
      function showToast(msg) {
        const el = document.getElementById('toast-banner');
        el.textContent = msg;
        el.classList.remove('hidden');
        clearTimeout(toastTimer);
        toastTimer = setTimeout(() => el.classList.add('hidden'), 3200);
      }

      function showViewportStatus(msg) {
        const el = document.getElementById('viewport-status');
        document.getElementById('viewport-status-text').textContent = msg;
        el.classList.remove('hidden');
      }

      function hideViewportStatus() {
        document.getElementById('viewport-status').classList.add('hidden');
      }

      function bindUIEvents() {
        // Welcome Page & User Login Gate Navigation
        document.getElementById('btn-enter-lab').addEventListener('click', showLoginScreen);
        document.getElementById('btn-logo-welcome').addEventListener('click', showWelcomeScreen);
        document.getElementById('btn-back-welcome').addEventListener('click', showWelcomeScreen);
        document.getElementById('btn-login-pi').addEventListener('click', authenticateWithPi);
        document.getElementById('btn-login-guest').addEventListener('click', continueAsGuest);

        // Welcome Page Language Dropdown with Flag Icons
        const wLangBtn = document.getElementById('btn-welcome-lang');
        const wLangDropdown = document.getElementById('welcome-lang-dropdown');
        if (wLangBtn && wLangDropdown) {
          wLangBtn.addEventListener('click', (e) => {
            e.stopPropagation();
            wLangDropdown.classList.toggle('hidden');
          });
          wLangDropdown.querySelectorAll('button[data-wlang]').forEach((item) => {
            item.addEventListener('click', (e) => {
              e.stopPropagation();
              const chosenLang = item.getAttribute('data-wlang');
              wLangDropdown.classList.add('hidden');
              applyLanguage(chosenLang);
            });
          });
          document.addEventListener('click', () => {
            if (!wLangDropdown.classList.contains('hidden')) {
              wLangDropdown.classList.add('hidden');
            }
          });
        }

        // Header User Pill -> Opens Login Gate (or signs out Pi user if active)
        document.getElementById('btn-pi-auth').addEventListener('click', () => {
          if (state.piSession.sessionToken && state.piSession.user) {
            signOutPiUser();
          } else {
            showLoginScreen();
          }
        });

        // Header Settings Gear Dropdown Toggle & Outside Click Close
        const settingsBtn = document.getElementById('btn-header-settings');
        const settingsDropdown = document.getElementById('header-settings-dropdown');
        settingsBtn.addEventListener('click', (e) => {
          e.stopPropagation();
          settingsDropdown.classList.toggle('hidden');
        });
        document.getElementById('btn-close-settings').addEventListener('click', () => {
          settingsDropdown.classList.add('hidden');
        });
        settingsDropdown.addEventListener('click', (e) => e.stopPropagation());
        document.addEventListener('click', () => {
          if (!settingsDropdown.classList.contains('hidden')) {
            settingsDropdown.classList.add('hidden');
          }
        });

        // Mobile / Tablet Drawers
        document.getElementById('btn-toggle-left').addEventListener('click', () => {
          document.getElementById('left-sidebar').classList.toggle('-translate-x-full');
        });
        document.getElementById('btn-close-left').addEventListener('click', () => {
          document.getElementById('left-sidebar').classList.add('-translate-x-full');
        });
        document.getElementById('btn-toggle-right').addEventListener('click', () => {
          document.getElementById('right-panel').classList.toggle('translate-x-full');
        });
        document.getElementById('btn-close-right').addEventListener('click', () => {
          document.getElementById('right-panel').classList.add('translate-x-full');
        });

        // View Modes
        document.getElementById('mode-organ').addEventListener('click', () => setViewMode('organ'));
        document.getElementById('mode-fullbody').addEventListener('click', () => setViewMode('fullbody'));
        document.getElementById('mode-split').addEventListener('click', () => setViewMode('split'));

        // Full Body Controls
        document.getElementById('btn-zoom-selected-organ').addEventListener('click', () => setViewMode('organ'));
        document.getElementById('chk-body-shell').addEventListener('change', (e) => {
          state.showBodyShell = e.target.checked;
          if (fullBodyGroup) {
            const s = fullBodyGroup.getObjectByName('BodyShellLayer');
            if (s) s.visible = state.showBodyShell;
          }
        });
        document.getElementById('chk-body-skeleton').addEventListener('change', (e) => {
          state.showBodySkeleton = e.target.checked;
          if (fullBodyGroup) {
            const sk = fullBodyGroup.getObjectByName('BodySkeletonLayer');
            if (sk) sk.visible = state.showBodySkeleton;
          }
        });
        document.getElementById('select-body-sex').addEventListener('change', (e) => {
          state.bodySex = e.target.value;
          if (fullBodyGroup) {
            scene.remove(fullBodyGroup);
            disposeObject3D(fullBodyGroup);
            fullBodyGroup = createFullBodySceneGroup(state.bodySex);
            scene.add(fullBodyGroup);
          }
        });

        // Split Screen Controls
        document.getElementById('btn-sync-orbit').addEventListener('click', () => {
          state.syncOrbit = !state.syncOrbit;
          document.getElementById('sync-orbit-label').textContent = state.syncOrbit ? 'Sync Orbit' : 'Independent';
          controls.enabled = true;
          splitControlsRight.enabled = !state.syncOrbit;
        });
        document.getElementById('select-split-right').addEventListener('change', (e) => {
          state.splitRightId = e.target.value;
          loadSplitRightModel(state.splitRightId);
        });

        // Physiology Simulation Selector
        document.getElementById('select-phys-sim').addEventListener('change', (e) => {
          state.physSimMode = e.target.value;
          buildPhysiologyParticles();
        });

        // Header Utility Controls
        document.getElementById('select-theme').addEventListener('change', (e) => applyTheme(e.target.value));
        document.getElementById('select-device').addEventListener('change', (e) => applyDevicePreview(e.target.value));
        document.getElementById('select-lang').addEventListener('change', (e) => applyLanguage(e.target.value));

        document.getElementById('btn-fullscreen').addEventListener('click', () => {
          if (!document.fullscreenElement) {
            document.documentElement.requestFullscreen().catch(() => showToast('Fullscreen blocked by browser policy.'));
          } else {
            document.exitFullscreen().catch(() => {});
          }
        });

        // Optional Google Translate Popover
        document.getElementById('btn-gtranslate').addEventListener('click', () => {
          const box = document.getElementById('gtranslate-box');
          box.classList.toggle('hidden');
          if (!box.dataset.loaded) {
            box.dataset.loaded = '1';
            window.googleTranslateElementInit = function () {
              if (window.google && window.google.translate) {
                new window.google.translate.TranslateElement({ pageLanguage: 'en', includedLanguages: 'en,id,ar,es,fr,de,ja,zh-CN' }, 'google_translate_element');
              }
            };
            const s = document.createElement('script');
            s.src = 'https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit';
            s.onerror = () => {
              document.getElementById('google_translate_element').textContent = 'Offline fallback active (EN / ID dictionary).';
            };
            document.body.appendChild(s);
          }
        });
        document.getElementById('btn-close-gt').addEventListener('click', () => {
          document.getElementById('gtranslate-box').classList.add('hidden');
        });

        // Catalog Search
        const searchInput = document.getElementById('catalog-search');
        const clearBtn = document.getElementById('btn-clear-search');
        searchInput.addEventListener('input', (e) => {
          state.searchQuery = e.target.value;
          clearBtn.classList.toggle('hidden', !state.searchQuery);
          renderCatalogList();
        });
        clearBtn.addEventListener('click', () => {
          state.searchQuery = '';
          searchInput.value = '';
          clearBtn.classList.add('hidden');
          renderCatalogList();
        });

        // Bottom Floating Control Dock Buttons
        document.getElementById('btn-toggle-dock').addEventListener('click', () => {
          const bar = document.getElementById('bottom-dock-bar');
          const hidden = bar.classList.toggle('hidden');
          document.getElementById('dock-toggle-text').textContent = hidden ? 'Show Controls' : 'Hide Controls';
        });

        document.getElementById('dock-btn-section').addEventListener('click', (e) => {
          e.currentTarget.classList.toggle('active');
          document.getElementById('dock-sliders-drawer').classList.toggle('hidden');
        });

        document.getElementById('select-clip-plane').addEventListener('change', (e) => {
          state.clipPlaneAxis = e.target.value;
          applyMaterialModes();
        });

        document.getElementById('slider-clip-dist').addEventListener('input', (e) => {
          state.clipDist = parseFloat(e.target.value);
          applyMaterialModes();
        });

        document.getElementById('btn-anim-clip').addEventListener('click', (e) => {
          state.animClip = !state.animClip;
          if (state.animClip && state.clipPlaneAxis === 'none') {
            state.clipPlaneAxis = 'axial';
            document.getElementById('select-clip-plane').value = 'axial';
          }
          e.currentTarget.classList.toggle('active', state.animClip);
          applyMaterialModes();
        });

        document.getElementById('dock-btn-holoscan').addEventListener('click', (e) => {
          state.holoScan = !state.holoScan;
          e.currentTarget.classList.toggle('active', state.holoScan);
          applyMaterialModes();
          showToast(state.holoScan ? 'Holographic Volumetric Scan enabled' : 'Holographic Volumetric Scan off');
        });

        document.getElementById('slider-explode').addEventListener('input', (e) => {
          state.explodeFactor = parseFloat(e.target.value);
          document.getElementById('explode-val').textContent = `${Math.round(state.explodeFactor * 100)}%`;
          applyExplodedOffset();
        });

        document.getElementById('dock-btn-xray').addEventListener('click', (e) => {
          state.xray = !state.xray;
          e.currentTarget.classList.toggle('active', state.xray);
          applyMaterialModes();
        });

        document.getElementById('dock-btn-wireframe').addEventListener('click', (e) => {
          state.wireframe = !state.wireframe;
          e.currentTarget.classList.toggle('active', state.wireframe);
          applyMaterialModes();
        });

        document.getElementById('dock-btn-hotspots').addEventListener('click', (e) => {
          state.showHotspots = !state.showHotspots;
          e.currentTarget.classList.toggle('active', state.showHotspots);
          renderHotspotPins();
        });

        document.getElementById('dock-btn-rotate').addEventListener('click', (e) => {
          state.autoRotate = !state.autoRotate;
          e.currentTarget.classList.toggle('active', state.autoRotate);
        });

        document.getElementById('dock-btn-physiology').addEventListener('click', (e) => {
          state.livingPhysiology = !state.livingPhysiology;
          e.currentTarget.classList.toggle('active', state.livingPhysiology);
        });

        document.getElementById('dock-btn-snapshot').addEventListener('click', exportStudySnapshotPNG);
        document.getElementById('dock-btn-xr').addEventListener('click', enterWebXRMode);

        document.getElementById('dock-btn-reset').addEventListener('click', () => {
          camera.position.set(0, 0.35, state.viewMode === 'fullbody' ? 4.4 : 3.6);
          controls.target.set(0, state.viewMode === 'fullbody' ? 0.1 : 0, 0);
          if (activeOrganGroup) activeOrganGroup.rotation.set(0, 0, 0);
          if (fullBodyGroup) fullBodyGroup.rotation.set(0, 0, 0);
          state.explodeFactor = 0;
          document.getElementById('slider-explode').value = '0';
          document.getElementById('explode-val').textContent = '0%';
          applyExplodedOffset();
          controls.update();
          showToast('Camera & anatomical orientation reset.');
        });

        // Right Info Panel Tabs
        document.getElementById('tab-btn-structure').addEventListener('click', () => switchRightTab('structure'));
        document.getElementById('tab-btn-clinical').addEventListener('click', () => switchRightTab('clinical'));
        document.getElementById('tab-btn-quiz').addEventListener('click', () => switchRightTab('quiz'));

        // TTS Audio Controls
        document.getElementById('tts-play').addEventListener('click', speakActiveTab);
        document.getElementById('tts-pause').addEventListener('click', () => {
          if (!('speechSynthesis' in window)) return;
          if (window.speechSynthesis.paused) window.speechSynthesis.resume();
          else window.speechSynthesis.pause();
        });
        document.getElementById('tts-stop').addEventListener('click', () => {
          if ('speechSynthesis' in window) window.speechSynthesis.cancel();
        });
        document.getElementById('tts-rate').addEventListener('input', (e) => {
          document.getElementById('tts-rate-val').textContent = parseFloat(e.target.value).toFixed(1);
        });

        // Quiz Retry & Log Report
        document.getElementById('btn-quiz-audio').addEventListener('click', speakActiveTab);
        document.getElementById('btn-quiz-retry').addEventListener('click', () => initQuizForSpecimen(state.activeId));
        document.getElementById('btn-quiz-save-report').addEventListener('click', () => {
          const spec = SPECIMENS.find((s) => s.id === state.activeId);
          state.quizReports.unshift({
            student: document.getElementById('input-student-name').value || 'Student 01',
            organ: spec ? spec.name_en : state.activeId,
            score: `${state.quizScore}/${state.quizQueue.length}`,
            attempts: state.quizAttempts,
            time: new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' }),
          });
          renderQuizReportsTable();
          showToast('Quiz result logged to Teacher & Student Report.');
        });

        // Modals: References, GLB Loader, Teacher/Student Mode
        document.getElementById('btn-open-refs').addEventListener('click', () => {
          document.getElementById('modal-refs').classList.remove('hidden');
        });
        document.getElementById('btn-close-refs').addEventListener('click', () => {
          document.getElementById('modal-refs').classList.add('hidden');
        });

        document.getElementById('btn-open-glb-modal').addEventListener('click', () => {
          document.getElementById('modal-glb').classList.remove('hidden');
        });
        document.getElementById('btn-close-glb').addEventListener('click', () => {
          document.getElementById('modal-glb').classList.add('hidden');
        });
        document.getElementById('btn-restore-procedural').addEventListener('click', () => {
          loadSpecimenModel(state.activeId);
          updateInfoPanel();
          showToast('Restored built-in procedural anatomical model.');
        });
        document.getElementById('btn-submit-glb').addEventListener('click', () => {
          const urlVal = document.getElementById('input-glb-url').value.trim();
          const fileInput = document.getElementById('input-glb-file');
          if (fileInput.files && fileInput.files[0]) {
            const objUrl = URL.createObjectURL(fileInput.files[0]);
            loadCustomGLB(objUrl).catch(() => {});
          } else if (urlVal) {
            loadCustomGLB(urlVal).catch(() => {});
          } else {
            showToast('Enter a valid GLB/GLTF URL or choose a local file.');
          }
        });

        // Teacher / Student Modal
        const openTeacherModal = () => {
          populateTeacherQuestionSelect();
          renderQuizReportsTable();
          document.getElementById('modal-teacher').classList.remove('hidden');
        };
        document.getElementById('btn-role-mode').addEventListener('click', openTeacherModal);
        document.getElementById('btn-teacher-dashboard').addEventListener('click', openTeacherModal);
        document.getElementById('btn-close-teacher').addEventListener('click', () => {
          document.getElementById('modal-teacher').classList.add('hidden');
        });
        document.getElementById('select-modal-role').addEventListener('change', (e) => {
          state.role = e.target.value;
          document.getElementById('role-label').textContent = state.role === 'teacher' ? 'Teacher' : 'Student';
        });
        document.getElementById('btn-add-custom-q').addEventListener('click', () => {
          const hsId = Number(document.getElementById('tb-hotspot-select').value);
          const prompt = document.getElementById('tb-prompt-input').value.trim();
          if (!prompt) {
            showToast('Enter a custom question prompt first.');
            return;
          }
          if (!state.customQuestions[state.activeId]) state.customQuestions[state.activeId] = [];
          state.customQuestions[state.activeId].push({ hotspotId: hsId, prompt });
          document.getElementById('tb-prompt-input').value = '';
          initQuizForSpecimen(state.activeId);
          showToast('Added custom question to active organ quiz!');
        });
        document.getElementById('btn-export-report').addEventListener('click', () => {
          const rows = ['Student,Organ,Score,Attempts,Time', ...state.quizReports.map((r) => `${r.student},${r.organ},${r.score},${r.attempts},${r.time}`)];
          const ta = document.createElement('textarea');
          ta.value = rows.join('\n');
          document.body.appendChild(ta);
          ta.select();
          document.execCommand('copy');
          document.body.removeChild(ta);
          showToast('CSV learning report copied to clipboard.');
        });

        // Keyboard / Smart TV Remote Navigation (WASD Orbit, +/- Zoom)
        window.addEventListener('keydown', (e) => {
          if (['INPUT', 'TEXTAREA', 'SELECT'].includes(document.activeElement.tagName)) return;
          if (e.key === 'a' || e.key === 'A') {
            if (activeOrganGroup) activeOrganGroup.rotation.y -= 0.12;
          } else if (e.key === 'd' || e.key === 'D') {
            if (activeOrganGroup) activeOrganGroup.rotation.y += 0.12;
          } else if (e.key === 'w' || e.key === 'W') {
            if (activeOrganGroup) activeOrganGroup.rotation.x -= 0.12;
          } else if (e.key === 's' || e.key === 'S') {
            if (activeOrganGroup) activeOrganGroup.rotation.x += 0.12;
          } else if (e.key === '+' || e.key === '=') {
            camera.position.z = Math.max(1.4, camera.position.z - 0.3);
          } else if (e.key === '-') {
            camera.position.z = Math.min(8.0, camera.position.z + 0.3);
          }
        });
      }

      /* =========================================================================
       * 19. BOOTSTRAP APPLICATION ON WINDOW LOAD
       * ========================================================================= */
      window.addEventListener('load', async () => {
        if (window.lucide) {
          window.lucide.createIcons();
        }
        renderCategoryFilters();
        renderCatalogList();
        populateSplitRightSelector();
        bindUIEvents();
        initSpeechVoices();
        initThreeJS();
        selectSpecimen('heart', false);

        // Initialize Pi Network SDK only when inside Pi Browser context
        await initPiNetworkSDK();

        // Respect prefers-reduced-motion
        if (window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
          state.livingPhysiology = false;
          state.autoRotate = false;
          document.getElementById('dock-btn-physiology').classList.remove('active');
        }
      });
    })();
  </script>
</body>
</html>