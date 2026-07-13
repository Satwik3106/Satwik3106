<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="1180" height="610">
    <defs>
        <radialGradient id="bg-glow-1" cx="20%" cy="20%" r="50%">
            <stop offset="0%" stop-color="#7C3AED" stop-opacity="0.15">
                <animate attributeName="stop-color" values="#7C3AED;#22D3EE;#7C3AED" dur="8s" repeatCount="indefinite"/>
            </stop>
            <stop offset="100%" stop-color="transparent" stop-opacity="0"/>
        </radialGradient>
        <radialGradient id="bg-glow-2" cx="80%" cy="80%" r="50%">
            <stop offset="0%" stop-color="#10B981" stop-opacity="0.1">
                <animate attributeName="stop-color" values="#10B981;#22D3EE;#10B981" dur="10s" repeatCount="indefinite"/>
            </stop>
            <stop offset="100%" stop-color="transparent" stop-opacity="0"/>
        </radialGradient>

        <linearGradient id="accent-grad" x1="0%" y1="0%" x2="100%" y2="100%">
            <stop offset="0%" stop-color="#7C3AED">
                <animate attributeName="stop-color" values="#7C3AED;#22D3EE;#10B981;#7C3AED" dur="6s" repeatCount="indefinite"/>
            </stop>
            <stop offset="100%" stop-color="#22D3EE">
                <animate attributeName="stop-color" values="#22D3EE;#10B981;#7C3AED;#22D3EE" dur="6s" repeatCount="indefinite"/>
            </stop>
        </linearGradient>

        <linearGradient id="border-shimmer" x1="0%" y1="0%" x2="100%" y2="100%">
            <stop offset="0%" stop-color="rgba(255,255,255,0.02)"/>
            <stop offset="50%" stop-color="rgba(255,255,255,0.2)"/>
            <stop offset="100%" stop-color="rgba(255,255,255,0.02)"/>
            <animateTransform attributeName="gradientTransform" type="translate" values="-1 -1; 1 1" dur="4s" repeatCount="indefinite"/>
        </linearGradient>

        <mask id="typing-mask">
            <rect x="0" y="0" width="0" height="40" fill="white">
                <animate attributeName="width" values="0; 300; 300; 0; 0" keyTimes="0; 0.3; 0.7; 0.9; 1" dur="4s" repeatCount="indefinite"/>
            </rect>
        </mask>

        <mask id="ascii-mask">
            <rect x="0" y="0" width="400" height="0" fill="white">
                <animate attributeName="height" from="0" to="500" dur="2s" fill="freeze"/>
            </rect>
        </mask>

        <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
            <feGaussianBlur stdDeviation="8" result="blur"/>
            <feMerge>
                <feMergeNode in="blur"/>
                <feMergeNode in="SourceGraphic"/>
            </feMerge>
        </filter>
        
        <filter id="noise">
            <feTurbulence type="fractalNoise" baseFrequency="0.65" numOctaves="3" stitchTiles="stitch"/>
            <feColorMatrix type="matrix" values="1 0 0 0 0, 0 1 0 0 0, 0 0 1 0 0, 0 0 0 0.05 0" />
        </filter>
    </defs>

    <style>
        .text-primary { fill: #F8FAFC; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }
        .text-muted { fill: #94A3B8; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }
        .font-mono { font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace; }
        .font-bold { font-weight: 700; }
        .font-semibold { font-weight: 600; }
        
        /* Hover Effects */
        .pill { transition: all 0.3s ease; cursor: pointer; }
        .pill:hover rect { fill: rgba(255,255,255,0.1); stroke: url(#accent-grad); stroke-width: 1.5; transform: scale(1.05); transform-origin: center; }
        .pill:hover text { fill: #fff; }
        
        .social-icon { transition: all 0.3s ease; cursor: pointer; opacity: 0.7; }
        .social-icon:hover { opacity: 1; filter: drop-shadow(0 0 8px rgba(34, 211, 238, 0.6)); transform: translateY(-2px); }

        /* Cursor Blink */
        @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
        .cursor { animation: blink 1s step-end infinite; }
    </style>

    <rect width="1180" height="610" rx="20" fill="#030712"/>
    <rect width="1180" height="610" rx="20" fill="url(#bg-glow-1)"/>
    <rect width="1180" height="610" rx="20" fill="url(#bg-glow-2)"/>
    <rect width="1180" height="610" rx="20" style="pointer-events:none;" filter="url(#noise)"/>

    <g fill="url(#accent-grad)" opacity="0.3">
        <circle cx="100" cy="500" r="2">
            <animateMotion path="M0,0 Q30,-50 0,-100 T0,-200" dur="15s" repeatCount="indefinite"/>
            <animate attributeName="opacity" values="0;0.5;0" dur="15s" repeatCount="indefinite"/>
        </circle>
        <circle cx="1050" cy="150" r="1.5">
            <animateMotion path="M0,0 Q-20,40 -40,10 T-80,0" dur="12s" repeatCount="indefinite"/>
            <animate attributeName="opacity" values="0;0.4;0" dur="12s" repeatCount="indefinite"/>
        </circle>
        <circle cx="600" cy="550" r="2.5">
            <animateMotion path="M0,0 Q50,-30 20,-80 T-10,-150" dur="18s" repeatCount="indefinite"/>
            <animate attributeName="opacity" values="0;0.3;0" dur="18s" repeatCount="indefinite"/>
        </circle>
    </g>

    <g transform="translate(24, 24)">
        <rect width="430" height="562" rx="16" fill="#0F172A" stroke="url(#border-shimmer)" stroke-width="1.5" />
        
        <polygon points="0,0 200,0 0,400" fill="rgba(255,255,255,0.015)" style="pointer-events:none;"/>

        <g mask="url(#ascii-mask)" font-size="10.5" letter-spacing="1" class="font-mono font-bold" transform="translate(18, 50)">
            <animateTransform attributeName="transform" type="translate" values="18,50; 18,45; 18,50" dur="6s" repeatCount="indefinite"/>
            
            <text fill="url(#accent-grad)">
                <tspan x="0" dy="1.2em">      _,.-------.,_        </tspan>
                <tspan x="0" dy="1.2em">  ,;~'             '~;,    </tspan>
                <tspan x="0" dy="1.2em">,;                     ;,  </tspan>
                <tspan x="0" dy="1.2em">;      .--.     .--.      ;</tspan>
                <tspan x="0" dy="1.2em">;     (    )   (    )     ;</tspan>
                <tspan x="0" dy="1.2em">;      '--'     '--'      ;</tspan>
                <tspan x="0" dy="1.2em">;                         ;</tspan>
                <tspan x="0" dy="1.2em">;          .---.          ;</tspan>
                <tspan x="0" dy="1.2em"> ;         \___/         ; </tspan>
                <tspan x="0" dy="1.2em">  ;                     ;  </tspan>
                <tspan x="0" dy="1.2em">   ;,                 ,;   </tspan>
                <tspan x="0" dy="1.2em">     ';,.         .,;'     </tspan>
                <tspan x="0" dy="1.2em">         '-------'         </tspan>
                <tspan x="0" dy="1.2em">                           </tspan>
                <tspan x="0" dy="1.2em">  [ TERMINAL CONNECTED ]   </tspan>
                <tspan x="0" dy="1.2em">  > STATUS: ONLINE         </tspan>
                <tspan x="0" dy="1.2em">  > SYNC: 100%             </tspan>
            </text>
        </g>
        
        <rect x="0" y="0" width="430" height="2" fill="rgba(34, 211, 238, 0.2)" filter="url(#glow)">
            <animate attributeName="y" from="-10" to="572" dur="3s" repeatCount="indefinite"/>
        </rect>
    </g>

    <g transform="translate(470, 24)">
        <rect width="686" height="562" rx="16" fill="#0F172A" stroke="url(#border-shimmer)" stroke-width="1.5" />
        
        <circle cx="24" cy="24" r="6" fill="#EF4444" />
        <circle cx="44" cy="24" r="6" fill="#EAB308" />
        <circle cx="64" cy="24" r="6" fill="#22C55E" />
        <line x1="0" y1="48" x2="686" y2="48" stroke="rgba(255,255,255,0.05)" stroke-width="1" />

        <g transform="translate(40, 90)">
            
            <text class="text-primary font-bold" font-size="36">
                Hi 👋 I'm <tspan fill="url(#accent-grad)">{YOUR_NAME}</tspan>
            </text>

            <g transform="translate(0, 45)">
                <text class="text-primary font-mono" font-size="20">> </text>
                
                <g mask="url(#typing-mask)" transform="translate(20, 0)">
                    <text class="text-primary font-mono" font-size="20">
                        <animate attributeName="opacity" values="1;1;0;0;0;0;0;0" keyTimes="0;0.25;0.251;0.5;0.501;0.75;0.751;1" dur="16s" repeatCount="indefinite"/>
                        Full Stack Developer
                    </text>
                    <text class="text-primary font-mono" font-size="20">
                        <animate attributeName="opacity" values="0;0;1;1;0;0;0;0" keyTimes="0;0.25;0.251;0.5;0.501;0.75;0.751;1" dur="16s" repeatCount="indefinite"/>
                        Open Source Contributor
                    </text>
                    <text class="text-primary font-mono" font-size="20">
                        <animate attributeName="opacity" values="0;0;0;0;1;1;0;0" keyTimes="0;0.25;0.251;0.5;0.501;0.75;0.751;1" dur="16s" repeatCount="indefinite"/>
                        UI / UX Engineer
                    </text>
                    <text class="text-primary font-mono" font-size="20">
                        <animate attributeName="opacity" values="0;0;0;0;0;0;1;1" keyTimes="0;0.25;0.251;0.5;0.501;0.75;0.751;1" dur="16s" repeatCount="indefinite"/>
                        AI Enthusiast
                    </text>
                </g>
                <rect class="cursor" x="25" y="-18" width="10" height="22" fill="#22D3EE">
                    <animate attributeName="x" values="20; 250; 250; 20; 20" keyTimes="0; 0.3; 0.7; 0.9; 1" dur="4s" repeatCount="indefinite"/>
                </rect>
            </g>

            <g class="text-muted font-mono" font-size="15" transform="translate(0, 110)">
                <g opacity="0"><animate attributeName="opacity" from="0" to="1" begin="0.5s" dur="0.8s" fill="freeze"/>
                    <text y="0">📍 <tspan x="30" class="text-primary">Location:</tspan> <tspan x="140">San Francisco, CA</tspan></text>
                </g>
                <g opacity="0"><animate attributeName="opacity" from="0" to="1" begin="1.0s" dur="0.8s" fill="freeze"/>
                    <text y="35">🎓 <tspan x="30" class="text-primary">Education:</tspan> <tspan x="140">BSc Computer Science</tspan></text>
                </g>
                <g opacity="0"><animate attributeName="opacity" from="0" to="1" begin="1.5s" dur="0.8s" fill="freeze"/>
                    <text y="70">🔭 <tspan x="30" class="text-primary">Current:</tspan> <tspan x="140">Building open-source tools</tspan></text>
                </g>
                <g opacity="0"><animate attributeName="opacity" from="0" to="1" begin="2.0s" dur="0.8s" fill="freeze"/>
                    <text y="105">🌐 <tspan x="30" class="text-primary">Portfolio:</tspan> <tspan x="140">https://your-portfolio.dev</tspan></text>
                </g>
                <g opacity="0"><animate attributeName="opacity" from="0" to="1" begin="2.5s" dur="0.8s" fill="freeze"/>
                    <text y="140">✉️ <tspan x="30" class="text-primary">Email:</tspan> <tspan x="140">hello@example.com</tspan></text>
                </g>
            </g>

            <g transform="translate(0, 310)">
                <text class="text-primary font-bold" font-size="18" y="-15">Tech Stack</text>
                
                <g class="pill" transform="translate(0, 0)">
                    <rect width="80" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="40" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">React</text>
                </g>
                <g class="pill" transform="translate(90, 0)">
                    <rect width="90" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="45" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Next.js</text>
                </g>
                <g class="pill" transform="translate(190, 0)">
                    <rect width="110" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="55" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">TypeScript</text>
                </g>
                <g class="pill" transform="translate(310, 0)">
                    <rect width="90" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="45" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Tailwind</text>
                </g>
                <g class="pill" transform="translate(410, 0)">
                    <rect width="80" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="40" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Node.js</text>
                </g>

                <g class="pill" transform="translate(0, 42)">
                    <rect width="80" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="40" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Python</text>
                </g>
                <g class="pill" transform="translate(90, 42)">
                    <rect width="80" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="40" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Docker</text>
                </g>
                <g class="pill" transform="translate(180, 42)">
                    <rect width="90" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="45" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Postgres</text>
                </g>
                <g class="pill" transform="translate(280, 42)">
                    <rect width="60" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="30" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">AWS</text>
                </g>
                <g class="pill" transform="translate(350, 42)">
                    <rect width="60" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="30" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Git</text>
                </g>
                <g class="pill" transform="translate(420, 42)">
                    <rect width="70" height="32" rx="8" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.1)" stroke-width="1"/>
                    <text x="35" y="21" text-anchor="middle" class="text-muted font-semibold" font-size="13">Figma</text>
                </g>
            </g>

            <g transform="translate(490, 435)">
                <g class="social-icon" transform="translate(0, 0)">
                    <path fill="#94A3B8" d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.603-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.462-1.11-1.462-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.831.092-.646.35-1.086.636-1.336-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0112 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.578.688.48C19.138 20.161 22 16.418 22 12c0-5.523-4.477-10-10-10z"/>
                </g>
                <g class="social-icon" transform="translate(40, 0)">
                    <path fill="#94A3B8" d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </g>
                <g class="social-icon" transform="translate(80, 0)">
                    <path fill="#94A3B8" d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
                </g>
            </g>
        </g>
    </g>
</svg>
