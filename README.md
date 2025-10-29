<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Abdelrahman — PanCakeeYT — Precision Over Hype</title>

  <!-- Font -->
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700;900&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg1:#03040a;
      --bg2:#07121a;
      --neon1:#00ffd1;
      --neon2:#00b3ff;
      --muted:#87a2b8;
      --card:#0b1220;
      --glass: rgba(255,255,255,0.03);
      --accent: #00ffd1;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: "JetBrains Mono", monospace;
      background:
        radial-gradient(800px 400px at 10% 10%, rgba(0,255,209,0.04), transparent 5%),
        radial-gradient(700px 350px at 90% 90%, rgba(0,179,255,0.03), transparent 5%),
        linear-gradient(180deg,var(--bg1),var(--bg2));
      color:#cfeef7;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:32px;
      display:flex;
      justify-content:center;
      align-items:flex-start;
      gap:28px;
      min-height:100vh;
    }

    /* Layout */
    .container{
      width:1100px;
      max-width:calc(100% - 48px);
      display:grid;
      grid-template-columns: 520px 1fr;
      gap:22px;
      align-items:start;
    }

    /* HERO */
    .hero{
      background: linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
      border-radius:12px;
      padding:22px;
      box-shadow: 0 8px 30px rgba(0,0,0,0.6), inset 0 1px 0 rgba(255,255,255,0.02);
      border:1px solid rgba(255,255,255,0.03);
      position:relative;
      overflow:hidden;
    }

    .hero::before{
      content:"";
      position:absolute;
      inset:0;
      background-image: linear-gradient(90deg, rgba(255,255,255,0.02) 0%, rgba(255,255,255,0.00) 25%, rgba(255,255,255,0.02) 50%, rgba(255,255,255,0.00) 75%, rgba(255,255,255,0.02) 100%);
      background-size: 400% 100%;
      animation: sheen 8s linear infinite;
      pointer-events:none;
      mix-blend-mode:overlay;
      opacity:0.6;
    }

    @keyframes sheen { from {background-position:0 0} to {background-position:400% 0} }

    .title{
      display:flex;
      gap:14px;
      align-items:center;
      justify-content:space-between;
      margin-bottom:6px;
    }
    .title h1{
      margin:0;
      font-size:28px;
      letter-spacing: -0.5px;
      color:var(--neon1);
      text-shadow: 0 0 18px rgba(0,255,209,0.12), 0 0 6px rgba(0,179,255,0.06);
      font-weight:900;
    }
    .subtitle{
      color:var(--muted);
      font-size:12px;
      text-transform:uppercase;
      letter-spacing:1.8px;
    }

    /* Typing strip */
    .typing-wrap{
      margin-top:12px;
      background: linear-gradient(180deg, rgba(255,255,255,0.01), transparent);
      border-radius:8px;
      padding:18px;
      min-height:140px;
      display:flex;
      align-items:center;
      gap:18px;
    }

    .wave{
      width:84px;
      height:84px;
      display:flex;
      align-items:center;
      justify-content:center;
      border-radius:10px;
      background:linear-gradient(180deg, rgba(0,255,209,0.04), rgba(0,179,255,0.02));
      box-shadow: 0 6px 18px rgba(0,0,0,0.6);
      border:1px solid rgba(0,255,209,0.06);
      flex-shrink:0;
    }

    /* simple animated waveform svg */
    .wave svg{ width:60px; height:60px; display:block; filter: drop-shadow(0 8px 12px rgba(0,0,0,0.7)); }

    .typing{
      flex:1;
      font-size:14px;
      line-height:1.6;
      color:#bfeff0;
      min-height:80px;
      display:flex;
      flex-direction:column;
      justify-content:center;
      gap:8px;
      white-space:pre-wrap;
    }
    .typing .line{ font-weight:600; color: #e9ffff; letter-spacing:0.2px; font-size:15px; }

    .cursor{
      display:inline-block;
      width:10px;
      height:18px;
      background:linear-gradient(180deg,var(--neon1),var(--neon2));
      margin-left:6px;
      border-radius:2px;
      animation: blink 1s steps(2,start) infinite;
      vertical-align:middle;
      transform-origin:center;
    }
    @keyframes blink { 50% { opacity:0.08 } 100% { opacity:1 } }

    /* right column (cards) */
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:10px;
      padding:18px;
      border:1px solid rgba(255,255,255,0.03);
      box-shadow: 0 6px 30px rgba(0,0,0,0.6);
    }

    h2{ margin:6px 0 12px 0; color: #bfeff0; font-size:16px; font-weight:700; }
    p.small{ margin:0; color:var(--muted); font-size:13px; line-height:1.45; }

    /* two-column inside right card */
    .split{ display:grid; grid-template-columns:1fr 1fr; gap:12px; align-items:start; }

    table{ width:100%; border-collapse:collapse; font-size:13px; }
    table td, table th{ padding:8px 6px; border-bottom:1px dashed rgba(255,255,255,0.03); text-align:left; color:#cbeff2; vertical-align:top;}
    table th{ color:var(--muted); font-weight:600; font-size:12px; text-transform:uppercase; letter-spacing:1px; }

    .badges{ display:flex; flex-wrap:wrap; gap:8px; margin-top:10px; }
    .badges img{ height:26px; }

    pre.cmd{
      background:rgba(0,0,0,0.25);
      padding:10px;
      border-radius:8px;
      font-size:13px;
      overflow:auto;
      color:#dffcff;
      border:1px solid rgba(0,255,209,0.05);
    }

    .footer-stats{
      display:flex;
      gap:12px;
      align-items:center;
      margin-top:14px;
    }
    .stat-img{ width:46%; border-radius:8px; border:1px solid rgba(255,255,255,0.03); }
    .visit-badge{ margin-top:10px; display:inline-block; }

    /* responsive */
    @media (max-width:1000px){
      .container{ grid-template-columns: 1fr; }
      .hero{ order:0 }
    }

    /* subtle floating scanlines */
    .scanlines{
      pointer-events:none;
      position:absolute;
      inset:0;
      background-image: linear-gradient(transparent 90%, rgba(255,255,255,0.01) 100%);
      background-size:100% 6px;
      mix-blend-mode:overlay;
      opacity:0.5;
    }
  </style>
</head>
<body>
  <div class="container">

    <!-- LEFT: hero + typing -->
    <div class="hero">
      <div class="title">
        <div>
          <h1>Abdelrahman — PanCakeeYT</h1>
          <div class="subtitle">Precision Over Hype</div>
        </div>

        <!-- small dynamic badges (images update externally) -->
        <div style="display:flex;gap:10px;align-items:center;">
          <img src="https://img.shields.io/badge/ESP32-Embedded-00ffd1?style=flat-square&logo=espressif" alt="ESP32" height="28"/>
          <img src="https://img.shields.io/badge/Real-Time-LowLatency-00b3ff?style=flat-square" alt="Realtime" height="28"/>
        </div>
      </div>

      <div class="typing-wrap">
        <div class="wave" aria-hidden>
          <!-- Animated waveform (pure SVG animation) -->
          <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
            <defs>
              <linearGradient id="g1" x1="0" x2="1">
                <stop offset="0" stop-color="#00ffd1" stop-opacity="0.9"/>
                <stop offset="1" stop-color="#00b3ff" stop-opacity="0.7"/>
              </linearGradient>
            </defs>
            <path id="s" d="M0,60 Q20,30 40,60 T100,60" fill="none" stroke="url(#g1)" stroke-width="3" stroke-linecap="round" />
            <animate xlink:href="#s" attributeName="d" dur="2.2s" repeatCount="indefinite"
              values="M0,60 Q20,30 40,60 T100,60;
                      M0,60 Q20,70 40,60 T100,60;
                      M0,60 Q20,40 40,60 T100,60;
                      M0,60 Q20,30 40,60 T100,60" />
          </svg>
        </div>

        <div class="typing">
          <div class="line" id="type-line" aria-live="polite"></div>
          <div style="display:flex;gap:12px;align-items:center;">
            <div class="cursor" id="cursor" aria-hidden></div>
            <div style="color:var(--muted);font-size:12px">ESP32 • FreeRTOS • MPU6050 • TDA2030A • LEDC • ESP-NOW</div>
          </div>
        </div>
      </div>

      <div style="margin-top:14px; display:flex; gap:12px; align-items:center; justify-content:space-between;">
        <div style="flex:1">
          <div style="color:var(--muted); font-size:13px; margin-bottom:6px">Core focus</div>
          <div style="font-weight:700; color:#eafffb; font-size:14px">Real-time stabilization, modular firmware, audio-driven EES, low-latency comms</div>
        </div>

        <div style="text-align:right; min-width:170px;">
          <!-- profile views counter (image service) -->
          <img class="visit-badge" src="https://komarev.com/ghpvc/?username=PanCakeeYT&label=Profile+Views&color=00ffd1&style=flat-square" alt="profile views"/>
        </div>
      </div>

      <div class="scanlines" aria-hidden></div>
    </div>

    <!-- RIGHT: project cards -->
    <div style="display:flex;flex-direction:column;gap:18px;">

      <!-- Projects card -->
      <div class="card">
        <h2>Active Projects</h2>
        <table>
          <thead>
            <tr><th>Repo</th><th>Role / Focus</th><th>Status</th></tr>
          </thead>
          <tbody>
            <tr><td><strong>rc-firmware</strong></td><td>TX / RX / EES — comms, servo/motor control, lighting, failsafe, telemetry</td><td>In Development</td></tr>
            <tr><td><strong>ees-audio</strong></td><td>Dedicated EES node — pitch/load mapping, sample streaming, amp control (TDA2030A)</td><td>Prototype</td></tr>
            <tr><td><strong>rc-ui</strong></td><td>TFT_eSPI UI — drive info, input debug, steering angle graphic, voltage readout</td><td>Design</td></tr>
          </tbody>
        </table>

        <div style="margin-top:12px" class="badges">
          <!-- skill icons -->
          <img src="https://skillicons.dev/icons?i=arduino,cpp,py,react,git,vscode&theme=dark" alt="stack" />
        </div>
      </div>

      <!-- Tech + Hardware card -->
      <div class="card split">
        <div>
          <h2>Tech Stack</h2>
          <p class="small">
            Firmware / Embedded: <strong>ESP32</strong> • Arduino • C++ • FreeRTOS • I2C (400kHz+) • SPI • UART • PWM (LEDC)<br>
            Backend / Tools: Python • Flask • FastAPI • WebSocket • GitHub Actions<br>
            Audio / Media: PCM / WAV playback • Real-time pitch shift • TDA2030A amp control
          </p>

          <h2 style="margin-top:14px">Hardware</h2>
          <p class="small">
            ESP32 ×3 (TX / RX / EES), MPU6050 (gyro/accel), L298N motor driver, TDA2030A amplifier + speaker, servos, joystick, TFT, 9–12V packs, voltage dividers, MOSFETs.
          </p>
        </div>

        <div>
          <h2>Architecture</h2>
          <pre class="cmd">
[TX ESP32] <--ESP-NOW--> [RX ESP32] ---> L298N, servos, lights
                                  |
                                  +--> [EES ESP32] --> TDA2030A amp + speaker
[TFT (TX)] -> UI/Control -> Joystick / Pots / Buttons
          </pre>

          <h2 style="margin-top:12px">Goals</h2>
          <p class="small">
            Ultra-low-latency stabilization (<5ms), clean audio sync to engine state, modular OTA-friendly firmware, robust power domain separation.
          </p>
        </div>
      </div>

      <!-- Features + Commands -->
      <div class="card">
        <h2>Features & Build</h2>
        <table>
          <tbody>
            <tr><th>Features</th><td>Dual-stage lighting, gyro-based steering correction, engine sound mapping (RPM+throttle), OTA-ready modules, WebSocket telemetry.</td></tr>
            <tr><th>Dev Notes</th><td>Hardware timers for control loops; use ledcWrite() for precise PWM; minimize I2C transactions; isolate motor & logic power domains.</td></tr>
          </tbody>
        </table>

        <div style="margin-top:12px">
          <div style="color:var(--muted);font-size:13px;margin-bottom:6px">Build & Flash</div>
          <pre class="cmd">
make rx-build && esptool.py --port /dev/ttyUSB0 write_flash 0x10000 build/rx.bin

python -m serial.tools.miniterm COM4 115200

cd dashboard && python -m flask run --host=0.0.0.0
          </pre>
        </div>

        <div class="footer-stats">
          <!-- live stats images -->
          <img class="stat-img" src="https://github-readme-stats.vercel.app/api?username=PanCakeeYT&show_icons=true&theme=tokyonight" alt="github stats">
          <img class="stat-img" src="https://github-readme-stats.vercel.app/api/top-langs/?username=PanCakeeYT&layout=compact&theme=tokyonight" alt="top langs">
        </div>
      </div>

      <!-- contact only: GitHub handle (no other personal details) -->
      <div class="card" style="display:flex;justify-content:space-between;align-items:center;">
        <div>
          <div style="color:var(--muted); font-size:12px; text-transform:uppercase; letter-spacing:1px">Public handle</div>
          <div style="font-weight:700; font-size:14px; margin-top:6px;"><a href="https://github.com/PanCakeeYT" target="_blank" style="color:#eafffb;text-decoration:none">github.com/PanCakeeYT</a></div>
        </div>

        <div style="text-align:right">
          <div style="color:var(--muted); font-size:12px">Live</div>
          <div style="font-weight:700; font-size:13px; color:var(--accent); margin-top:6px">ESP32 • Firmware • Audio</div>
        </div>
      </div>

    </div>

  </div>

  <script>
    /* TYPING effect - no external libs, fully contained. 
       Cycles through long lines, keeps full content (no cutoff).
    */
    (function(){
      const lines = [
        "Embedded firmware engineer — ESP32, FreeRTOS, tight control loops, hardware timers, LEDC PWM.",
        "1:10 RC platform: TX / RX / EES architecture, ESP-NOW comms, modular OTA-ready firmware.",
        "MPU6050 stabilization: DMP when possible, ISR-driven loops, <5ms reaction target for drift corrections.",
        "EES (Engine Exhaust Sound): pitch & load mapping → real-time audio + TDA2030A amplifier sync.",
        "TFT UI: Drive info, input visualizers, steering angle graphic, real battery voltage via dividers.",
        "Dev rules: isolate power domains, minimize I2C work per loop, use ledcWrite() for consistent servo timing.",
        "Workflow: full, polished firmware when parts arrive — complete end-to-end builds; dark UI, fast updates."
      ];

      const output = document.getElementById('type-line');
      const cursor = document.getElementById('cursor');

      let lineIndex = 0;
      let charIndex = 0;
      let deleting = false;
      const typeSpeed = 18; // ms per char
      const delSpeed = 10;
      const pauseBetween = 900;

      function tick(){
        const current = lines[lineIndex];
        if(!deleting){
          output.textContent = current.slice(0,charIndex+1);
          charIndex++;
          if(charIndex === current.length){
            deleting = true;
            setTimeout(tick, pauseBetween);
            return;
          }
          setTimeout(tick, typeSpeed);
        } else {
          // keep full text visible for a short moment, then delete a chunk quickly
          output.textContent = current.slice(0,charIndex-2);
          charIndex -= 2;
          if(charIndex <= 0){
            deleting = false;
            lineIndex = (lineIndex + 1) % lines.length;
            charIndex = 0;
            setTimeout(tick, 220);
            return;
          }
          setTimeout(tick, delSpeed);
        }
      }

      // start after small delay so first render looks deliberate
      setTimeout(tick, 600);

      // cursor blink subtle handling (restore if focus)
      document.addEventListener('visibilitychange', () => {
        cursor.style.animation = document.hidden ? 'none' : 'blink 1s steps(2,start) infinite';
      });
    })();
  </script>
</body>
</html>
