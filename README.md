<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إلى معلمتي القديرة.. مس يارا ✨</title>
    <!-- خطوط عربية فاخرة من Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,700;1,700&family=Cairo:wght@400;600;700;800;900&display=swap" rel="stylesheet">
    <!-- مكتبة Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- مكتبة Confetti للاحتفال -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <!-- أيقونات FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif'],
                        amiri: ['Amiri', 'serif'],
                    },
                    colors: {
                        royal: {
                            50: '#fff1f2',
                            100: '#ffe4e6',
                            200: '#fecdd3',
                            600: '#e11d48',
                            700: '#be123c',
                            800: '#9f1239',
                            900: '#881337',
                        },
                        gold: {
                            300: '#fde68a',
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706',
                        },
                        cream: '#fffaf5',
                    }
                }
            }
        }
    </script>

    <style>
        /* تنسيقات مخصصة للحركات والرموز الرياضية الطافية */
        body {
            font-family: 'Cairo', sans-serif;
            background-color: #fffaf5;
            background-image: 
                radial-gradient(at 15% 15%, rgba(244, 63, 94, 0.08) 0px, transparent 50%),
                radial-gradient(at 85% 85%, rgba(251, 191, 36, 0.12) 0px, transparent 50%);
            overflow-x: hidden;
        }

        /* شبكة هندسية خفيفة في الخلفية تعطي طابع الرياضيات والفخامة */
        .bg-math-grid {
            background-size: 44px 44px;
            background-image: 
                linear-gradient(to right, rgba(251, 191, 36, 0.04) 1px, transparent 1px),
                linear-gradient(to bottom, rgba(251, 191, 36, 0.04) 1px, transparent 1px);
        }

        /* حركة الطفو الناعمة للرموز الرياضية الذهبية في الخلفية */
        @keyframes floatSymbol {
            0%, 100% {
                transform: translateY(0px) rotate(0deg) scale(1);
            }
            50% {
                transform: translateY(-28px) rotate(14deg) scale(1.08);
            }
        }

        .math-symbol {
            position: fixed;
            user-select: none;
            pointer-events: none;
            z-index: 0;
            animation: floatSymbol 8s ease-in-out infinite;
            opacity: 0.16;
            font-family: 'Amiri', serif;
            font-weight: bold;
            color: #fbbf24;
            text-shadow: 0 0 15px rgba(251, 191, 36, 0.4);
        }

        /* إطار ذهبي متوهج للبطاقة الرئيسية */
        .luxury-card {
            background: rgba(255, 255, 255, 0.96);
            box-shadow: 
                0 25px 60px -15px rgba(0, 0, 0, 0.65),
                0 0 0 1px rgba(251, 191, 36, 0.5),
                0 0 40px rgba(245, 158, 11, 0.18);
        }

        /* لمعة ذهبية متحركة على النصوص والعناصر المميزة */
        @keyframes shimmerGold {
            0% { background-position: 200% center; }
            100% { background-position: -200% center; }
        }
        .gold-shimmer-text {
            background: linear-gradient(90deg, #fcd34d 0%, #ffffff 35%, #f59e0b 65%, #fcd34d 100%);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: shimmerGold 4.5s linear infinite;
        }

        /* تأثير بطاقات الصفات التفاعلية */
        .trait-card {
            transition: all 0.35s cubic-bezier(0.34, 1.56, 0.64, 1);
        }
        .trait-card:hover {
            transform: translateY(-6px);
        }
        .trait-card.active {
            background: linear-gradient(135deg, #be123c 0%, #881337 100%);
            color: #ffffff;
            border-color: #fbbf24;
            transform: scale(1.03);
        }
        .trait-card.active .symbol-badge {
            background-color: #fbbf24;
            color: #881337;
        }
        .trait-card.active p {
            color: #ffe4e6;
        }
        .trait-card.active {
            background: linear-gradient(135deg, #3b0764 0%, #5b21b6 100%);
            color: #ffffff;
            border-color: #fbbf24;
            transform: translateY(-4px) scale(1.03);
            box-shadow: 0 16px 32px -8px rgba(59, 7, 100, 0.45);
        }
        .trait-card.active .symbol-badge {
            background: linear-gradient(135deg, #fde047, #f59e0b);
            color: #240046;
            box-shadow: 0 0 15px rgba(251, 191, 36, 0.6);
        }
        .trait-card.active p {
            color: #fde047;
        }

        /* تأثير نبض ذهبي لزر المفاجأة */
        @keyframes pulseGlow {
            0%, 100% {
                box-shadow: 0 10px 25px -5px rgba(245, 158, 11, 0.5), 0 0 0 0 rgba(251, 191, 36, 0.6);
            }
            50% {
                box-shadow: 0 10px 25px -5px rgba(245, 158, 11, 0.5), 0 0 0 14px rgba(251, 191, 36, 0);
            }
        }
        .btn-glow {
            animation: pulseGlow 2.4s infinite;
        }

        /* حركة ظهور الرسائل المفاجئة */
        @keyframes popIn {
            0% {
                opacity: 0;
                transform: scale(0.88) translateY(18px);
            }
            100% {
                opacity: 1;
                transform: scale(1) translateY(0);
            }
        }
        .animate-pop-in {
            animation: popIn 0.55s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        /* حركة تطاير القلوب والرموز للأعلى */
        @keyframes riseUp {
            0% {
                transform: translateY(0) scale(0.75) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-92vh) scale(1.4) rotate(25deg);
                opacity: 0;
            }
        }
        .rising-item {
            position: fixed;
            bottom: -40px;
            pointer-events: none;
            z-index: 50;
            animation: riseUp 3.2s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
            user-select: none;
        }
    </style>
</head>
<body class="min-h-screen bg-math-grid text-slate-800 relative flex flex-col items-center justify-center py-8 px-4 sm:px-6 lg:px-8">

    <!-- حاوية الرموز الرياضية الذهبية العائمة في الخلفية -->
    <div id="floating-symbols-container" aria-hidden="true"></div>

    <!-- البطاقة الرئيسية الفاخرة -->
    <main class="luxury-card relative z-10 w-full max-w-3xl rounded-[2rem] border-2 border-gold-400/80 overflow-hidden">
        
        <!-- شريط علوي ملكي مزخرف -->
        <div class="bg-gradient-to-br from-royal-950 via-royal-900 to-royal-800 px-6 py-9 sm:px-12 sm:py-12 text-center relative overflow-hidden border-b-4 border-gold-400">
            <!-- إضاءة خلفية ناعمة داخل الهيدر -->
            <div class="absolute -top-24 left-1/2 -translate-x-1/2 w-96 h-96 bg-gold-400/15 rounded-full blur-3xl pointer-events-none"></div>

            <!-- زخارف هندسية ورياضية ذهبية -->
            <div class="absolute top-4 left-7 text-gold-400/20 text-5xl sm:text-6xl font-amiri select-none">∑</div>
    <!-- البطاقة الرئيسية -->
    <main class="relative z-10 w-full max-w-3xl bg-white/95 backdrop-blur-md rounded-3xl shadow-2xl border-2 border-rose-200 overflow-hidden">
        
        <!-- شريط علوي مزخرف بألوان عيد ميلاد دافئة ومبهجة -->
        <div class="bg-gradient-to-l from-rose-600 via-pink-600 to-amber-500 px-6 py-8 sm:px-10 sm:py-10 text-center relative overflow-hidden">
            <!-- زخارف عيد الميلاد والرياضيات داخل الترويسة -->
            <div class="absolute top-3 left-6 text-white/25 text-4xl select-none">🎂</div>
            <div class="absolute bottom-2 right-8 text-white/25 text-4xl select-none">🎈</div>
            <div class="absolute top-4 right-1/4 text-white/20 text-3xl font-amiri select-none">∞</div>

            <!-- أيقونة كعكة عيد الميلاد -->
            <div class="inline-flex items-center justify-center w-16 h-16 rounded-2xl bg-white text-rose-600 shadow-lg mb-4 transform -rotate-3">
                <i class="fa-solid fa-cake-candles text-3xl"></i>
            </div>

            <p class="text-amber-100 text-sm sm:text-base font-semibold tracking-wide mb-2">
                ✨ بطاقة شكر وتقدير خاصة ✨
            </p>
            <h1 class="text-3xl sm:text-4xl md:text-5xl font-extrabold text-white leading-tight">
                إلى معلمتي الرائعة.. <span class="text-amber-200 underline decoration-amber-200/60 decoration-wavy underline-offset-8">مس يارا</span>
            </h1>
        </div>

        <!-- محتوى البطاقة -->
        <div class="p-6 sm:p-10 space-y-8 bg-gradient-to-b from-white via-royal-50/30 to-amber-50/30">
            
            <!-- رسالة التقدير الراقية -->
            <section class="bg-white rounded-3xl p-6 sm:p-8 border border-royal-100 shadow-[0_8px_30px_rgb(0,0,0,0.04)] relative">
                <div class="w-10 h-10 rounded-full bg-royal-50 text-royal-600 flex items-center justify-center absolute -top-5 right-6 border border-royal-100 shadow-sm">
                    <i class="fa-solid fa-quote-right text-lg"></i>
                </div>
                <p class="text-base sm:text-lg leading-loose text-slate-700 font-semibold text-center relative z-10">
                    معلمتي الغالية <span class="text-royal-900 font-extrabold bg-gold-200/50 px-2 py-0.5 rounded-lg">مس يارا</span>،<br>
                    شكراً لكِ من القلب على كل مجهود عظيم تبذلينه معنا. لقد استطعتِ بأسلوبكِ الراقي وصبركِ الجميل أن تحوّلي الأرقام والمعادلات من رموز صعبة إلى عالم ممتع وشيّق نفهمه ونحبه. وجود معلمة مبدعة مثلكِ يجعل من كل حصة رياضيات رحلة مليئة بالإلهام والثقة والتفوق.
                </p>
                <div class="w-10 h-10 rounded-full bg-royal-50 text-royal-600 flex items-center justify-center absolute -bottom-5 left-6 border border-royal-100 shadow-sm">
                    <i class="fa-solid fa-quote-left text-lg"></i>
                </div>
            </section>

            <!-- قسم معادلة التميز التفاعلية -->
            <section class="space-y-4 pt-2">
                <div class="text-center">
                    <h2 class="text-xl sm:text-2xl font-black text-royal-950 flex items-center justify-center gap-2">
                        <span class="text-gold-500">✦</span>
                        <span>سرّ التميّز في حصة مس يارا</span>
                        <span class="text-gold-500">✦</span>
                    </h2>
                    <p class="text-xs sm:text-sm text-slate-500 font-medium mt-1">اضغطي على كل بطاقة لاكتشاف رسالة خاصة لكِ</p>
                </div>

                <!-- شبكة البطاقات التفاعلية -->
                <div class="grid grid-cols-1 sm:grid-cols-3 gap-4" id="traits-grid">
                    <!-- بطاقة 1: الصبر -->
                    <button type="button" onclick="toggleTrait(this, 'صبركِ اللامحدود وإعادتكِ للشرح بكل حب وابتسامة حتى يفهم الجميع هو سر تفوقنا!')" 
                            class="trait-card bg-white p-5 rounded-2xl border-2 border-royal-100 shadow-sm hover:border-gold-400 focus:outline-none cursor-pointer flex flex-col items-center text-center">
                        <div class="symbol-badge w-14 h-14 rounded-2xl bg-royal-50 text-royal-900 flex items-center justify-center text-3xl font-bold font-amiri mb-3 transition-all shadow-inner">
                            ∞
                        </div>
                        <h3 class="font-extrabold text-lg text-royal-950 mb-1">الصبر والعطاء</h3>
                        <p class="text-xs text-royal-600 font-semibold">اضغطي هنا ✨</p>
                    </button>

                    <!-- بطاقة 2: الإبداع -->
                    <button type="button" onclick="toggleTrait(this, 'أسلوبكِ المبتكر في تبسيط أعقد القوانين يجعل الرياضيات سهلة وممتعة كأنها لوحة فنية!')" 
                            class="trait-card bg-white p-5 rounded-2xl border-2 border-royal-100 shadow-sm hover:border-gold-400 focus:outline-none cursor-pointer flex flex-col items-center text-center">
                        <div class="symbol-badge w-14 h-14 rounded-2xl bg-royal-50 text-royal-900 flex items-center justify-center text-3xl font-bold font-amiri mb-3 transition-all shadow-inner">
                            π
                        </div>
                        <h3 class="font-extrabold text-lg text-royal-950 mb-1">الإبداع في الشرح</h3>
                        <p class="text-xs text-royal-600 font-semibold">اضغطي هنا ✨</p>
                    </button>

                    <!-- بطاقة 3: الإلهام -->
                    <button type="button" onclick="toggleTrait(this, 'تقديرنا واحترامنا وفخرنا بكِ يساوي 100% دائماً وأبداً، فأنتِ قدوة رائعة نعتز بها!')" 
                            class="trait-card bg-white p-5 rounded-2xl border-2 border-royal-100 shadow-sm hover:border-gold-400 focus:outline-none cursor-pointer flex flex-col items-center text-center">
                        <div class="symbol-badge w-14 h-14 rounded-2xl bg-royal-50 text-royal-900 flex items-center justify-center text-xl font-black mb-3 transition-all shadow-inner">
                            100%
                        </div>
                        <h3 class="font-extrabold text-lg text-royal-950 mb-1">الإلهام والثقة</h3>
                        <p class="text-xs text-royal-600 font-semibold">اضغطي هنا ✨</p>
                    </button>
                </div>

                <!-- صندوق عرض تفاصيل الصفة المختارة -->
                <div id="trait-message-box" class="hidden bg-gradient-to-r from-amber-50 via-gold-200/40 to-amber-50 border-2 border-gold-400/60 rounded-2xl p-4 text-center text-royal-950 font-bold text-sm sm:text-base shadow-sm">
                </div>
            </section>
            <!-- المعادلة الرياضية اللطيفة -->
            <div class="bg-gradient-to-r from-rose-600 to-pink-600 rounded-2xl p-4 sm:p-5 text-center text-white shadow-inner flex flex-wrap items-center justify-center gap-3 sm:gap-4" dir="ltr">
                <span class="px-3 py-1 bg-white/15 rounded-lg font-bold text-amber-200">Math</span>
                <span class="text-xl font-bold text-amber-200">+</span>
                <span class="px-3 py-1 bg-white/15 rounded-lg font-bold text-amber-200">Ms. Yara</span>
                <span class="text-xl font-bold text-amber-200">=</span>
                <span class="px-4 py-1 bg-amber-300 text-rose-950 rounded-lg font-extrabold shadow">Pure Magic ✨</span>
            </div>

            <!-- زر المفاجأة التفاعلي -->
            <div class="text-center pt-2 flex flex-col sm:flex-row items-center justify-center gap-3 sm:gap-4">
                <button id="surprise-btn" onclick="toggleSurpriseCard()" 
                        class="btn-glow w-full sm:w-auto inline-flex items-center justify-center gap-3 bg-gradient-to-r from-pink-500 via-rose-400 to-pink-500 hover:from-pink-400 hover:to-pink-300 text-white font-extrabold text-base sm:text-lg px-7 py-4 rounded-2xl shadow-xl transition-all transform hover:scale-105 active:scale-95 cursor-pointer">
                    <i class="fa-solid fa-cake-candles text-xl"></i>
                    <span>اضغطي هنا لهدية عيد الميلاد</span>
                </button>

                <!-- زر الضغطة الإضافية -->
                <button id="extra-surprise-btn" onclick="toggleExtraSurpriseCard()" 
                        class="w-full sm:w-auto inline-flex items-center justify-center gap-2 bg-gradient-to-r from-purple-700 to-indigo-700 hover:from-purple-600 hover:to-indigo-600 text-pink-200 border-2 border-pink-300/70 font-extrabold text-base sm:text-lg px-6 py-3.5 rounded-2xl shadow-lg transition-all transform hover:scale-105 active:scale-95 cursor-pointer">
                    <i class="fa-solid fa-heart text-lg text-pink-300"></i>
                    <span>رسالة حب لـ مس يارا ❤️</span>
                </button>
            </div>

            <!-- بطاقة المفاجأة المخفية الأولى -->
            <div id="surprise-card" class="hidden animate-pop-in bg-gradient-to-br from-purple-900 via-indigo-900 to-slate-900 text-white rounded-3xl p-6 sm:p-8 border-2 border-pink-400 shadow-2xl text-center space-y-4 relative overflow-hidden">
                <div class="inline-flex items-center gap-2 bg-pink-500/20 border border-pink-400/40 text-pink-300 px-4 py-1.5 rounded-full text-xs sm:text-sm font-bold">
                    <i class="fa-solid fa-cake-candles"></i>
                    <span>كل سنة وأنتِ طيبة يا مس يارا</span>
                </div>

                <h3 class="text-2xl sm:text-3xl font-extrabold text-pink-300">
                    أفضل معلمة رياضيات في الدنيا!
                </h3>

                <!-- التقييم 10/10 -->
                <div class="inline-block bg-white/10 backdrop-blur-sm border border-pink-400/50 rounded-2xl px-6 py-3 my-2">
                    <div class="text-3xl sm:text-4xl font-black text-pink-400 tracking-wider" dir="ltr">
                        10 / 10 ⭐
                    </div>
                    <div class="text-xs text-pink-200 mt-1">التقييم النهائي بكل جدارة واستحقاق</div>
                </div>

                <p class="text-sm sm:text-base text-pink-100 max-w-lg mx-auto leading-relaxed">
                    "دمتِ لنا معلمة ملهمة تزرع حب العلم في قلوبنا، ونتمنى لكِ دائماً عيد ميلاد سعيد وحياة مليئة بالسعادة لا تنتهي كـ <span class="text-pink-300 font-bold">(∞)</span>!"
                </p>

                <div class="pt-2">
                    <button onclick="toggleSurpriseCard()" class="inline-flex items-center gap-1.5 bg-white/15 hover:bg-white/25 text-pink-300 font-bold text-xs sm:text-sm px-4 py-2 rounded-xl transition-colors cursor-pointer">
                        <i class="fa-solid fa-eye-slash"></i>
                        <span>اختفي مرة تانية</span>
                    </button>
                </div>
            </div>

            <!-- بطاقة المفاجأة الإضافية الثانية -->
            <div id="extra-surprise-card" class="hidden animate-pop-in bg-gradient-to-br from-pink-50 via-white to-purple-50 text-slate-900 rounded-3xl p-6 sm:p-8 border-2 border-pink-400 shadow-xl text-center space-y-4 relative overflow-hidden">
                
                <!-- تصميم صورة القلب الفني مع عبارة "بنحبك يا مس يارا" -->
                <div class="relative mx-auto w-64 h-56 sm:w-72 sm:h-64 flex items-center justify-center my-1">
                    <svg viewBox="0 0 320 280" class="w-full h-full drop-shadow-xl transform hover:scale-105 transition-transform duration-500" role="img" aria-label="قلب مكتوب بداخله بنحبك يا مس يارا">
                        <defs>
                            <linearGradient id="heartPinkGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#ec4899" />
                                <stop offset="50%" stop-color="#db2777" />
                                <stop offset="100%" stop-color="#9333ea" />
                            </linearGradient>
                            <linearGradient id="pinkBorderGrad" x1="0%" y1="0%" x2="100%" y2="0%">
                                <stop offset="0%" stop-color="#fbcfe8" />
                                <stop offset="50%" stop-color="#f472b6" />
                                <stop offset="100%" stop-color="#fbcfe8" />
                            </linearGradient>
                        </defs>

                        <path d="M160 258 C160 258 22 172 22 86 C22 40 58 12 98 12 C126 12 149 27 160 48 C171 27 194 12 222 12 C262 12 298 40 298 86 C298 172 160 258 160 258 Z" 
                              fill="#f472b6" opacity="0.22" transform="scale(1.04) translate(-6, -5)" />

                        <path d="M160 255 C160 255 25 170 25 85 C25 42 60 15 98 15 C125 15 148 30 160 50 C172 30 195 15 222 15 C260 15 295 42 295 85 C295 170 160 255 160 255 Z" 
                              fill="url(#heartPinkGrad)" stroke="url(#pinkBorderGrad)" stroke-width="6" />

                        <path d="M160 241 C160 241 37 162 37 86 C37 49 67 27 99 27 C123 27 144 40 160 59 C176 40 197 27 221 27 C253 27 283 49 283 86 C283 162 160 241 160 241 Z" 
                              fill="none" stroke="#fce7f3" stroke-width="1.8" stroke-dasharray="5,5" opacity="0.7" />

                        <text x="82" y="75" fill="#fce7f3" opacity="0.5" font-family="Amiri, serif" font-size="18" font-weight="bold">🎂</text>
                        <text x="238" y="75" fill="#fce7f3" opacity="0.5" font-family="Amiri, serif" font-size="18" font-weight="bold">🎈</text>
                        <text x="160" y="218" text-anchor="middle" fill="#fbcfe8" font-size="16">✨ 👑 ✨</text>

                        <text x="160" y="118" text-anchor="middle" fill="#ffffff" font-family="Cairo, sans-serif" font-size="25" font-weight="800">
                            بنحبك
                        </text>
                        <text x="160" y="156" text-anchor="middle" fill="#fbcfe8" font-family="Cairo, sans-serif" font-size="27" font-weight="800">
                            يا مس يارا
                        </text>
                        <text x="160" y="186" text-anchor="middle" fill="#fae8ff" font-family="Cairo, sans-serif" font-size="13" font-weight="700">
                            ❤️ أحلى عيد ميلاد ❤️
                        </text>
                    </svg>
                </div>

                <h3 class="text-xl sm:text-2xl font-extrabold text-purple-900">
                    كل سنة وأنتِ منورة حياتنا يا مس يارا!
                </h3>
                <p class="text-sm sm:text-base text-slate-700 max-w-lg mx-auto leading-relaxed font-medium">
                    نتمنى لكِ عاماً سعيداً مليئاً بالنجاح والبهجة، وشكراً لكونكِ معلمة رائعة وأخت غالية في قلوبنا جميعاً.
                </p>
                <div class="pt-1">
                    <button onclick="toggleExtraSurpriseCard()" class="inline-flex items-center gap-1.5 bg-pink-100 hover:bg-pink-200 text-purple-900 font-bold text-xs sm:text-sm px-4 py-2 rounded-xl transition-colors cursor-pointer">
                        <i class="fa-solid fa-eye-slash text-pink-700"></i>
                        <span>اختفي مرة تانية</span>
                    </button>
                </div>
            </div>

        </div>

        <!-- تذييل البطاقة -->
        <footer class="bg-gradient-to-r from-pink-50 via-purple-50/70 to-pink-50 border-t border-pink-300/60 px-6 py-5 text-center">
            <p class="text-sm sm:text-base text-purple-900 font-extrabold flex items-center justify-center gap-2">
                <span class="text-pink-500">✦</span>
                <span>مع خالص الحب والتقدير.. من كل التلاميذ</span>
                <span class="text-rose-500">🤍</span>
            </p>
        </footer>
    </main>

    <script>
        // 1. إنشاء الرموز الرياضية واحتفالات أعياد الميلاد العائمة في الخلفية
        function createFloatingSymbols() {
            const container = document.getElementById('floating-symbols-container');
            if (!container) return;

            const symbols = ['π', '∑', '∞', '🎂', '🎈', '🎁', '⭐', '✨', '√'];
            const count = 18;

            for (let i = 0; i < count; i++) {
                const span = document.createElement('span');
                span.className = 'math-symbol text-purple-700';
                span.textContent = symbols[i % symbols.length];

                span.style.top = `${Math.random() * 90 + 5}%`;
                span.style.left = `${Math.random() * 90 + 5}%`;
                span.style.fontSize = `${Math.floor(Math.random() * 28) + 24}px`;
                span.style.animationDelay = `${(Math.random() * 5).toFixed(1)}s`;
                span.style.animationDuration = `${(Math.random() * 4 + 6).toFixed(1)}s`;

                container.appendChild(span);
            }
        }

        // 2. التفاعل مع بطاقات الصفات الثلاث
        window.toggleTrait = function(buttonElement, message) {
            const allCards = document.querySelectorAll('.trait-card');
            const messageBox = document.getElementById('trait-message-box');
            const isAlreadyActive = buttonElement.classList.contains('active');

            allCards.forEach(card => card.classList.remove('active'));

            if (isAlreadyActive) {
                messageBox.classList.add('hidden');
            } else {
                buttonElement.classList.add('active');
                messageBox.textContent = message;
                messageBox.classList.remove('hidden');
                messageBox.classList.remove('animate-pop-in');
                void messageBox.offsetWidth;
                messageBox.classList.add('animate-pop-in');
            }
        };

        // 3. إطلاق قصاصات الاحتفال
        window.launchConfetti = function() {
            if (typeof confetti === 'function') {
                const colors = ['#ec4899', '#f43f5e', '#8b5cf6', '#fbbf24', '#ffffff'];

                confetti({
                    particleCount: 70,
                    angle: 60,
                    spread: 65,
                    origin: { x: 0.1, y: 0.7 },
                    colors: colors
                });
                confetti({
                    particleCount: 70,
                    angle: 120,
                    spread: 65,
                    origin: { x: 0.9, y: 0.7 },
                    colors: colors
                });
            }
        };

        // 4. دالة التبديل للبطاقة الأولى (إظهار وإخفاء دون حذف الأزرار)
        window.toggleSurpriseCard = function() {
            const surpriseCard = document.getElementById('surprise-card');
            const isHidden = surpriseCard.classList.contains('hidden') || surpriseCard.style.display === 'none';

            if (isHidden) {
                surpriseCard.style.display = 'block';
                surpriseCard.classList.remove('hidden');
                surpriseCard.classList.remove('animate-pop-in');
                void surpriseCard.offsetWidth;
                surpriseCard.classList.add('animate-pop-in');
                window.launchConfetti();

                setTimeout(() => {
                    surpriseCard.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
                }, 150);
            } else {
                surpriseCard.style.display = 'none';
            }
        };

        // 5. إطلاق وابل من القلوب والبالونات للأعلى
        window.launchBouquetShower = function() {
            const items = ['💜', '💖', '🎂', '🎈', '✨', '🎁', '⭐', '🌸'];
            const totalItems = 26;

            for (let i = 0; i < totalItems; i++) {
                setTimeout(() => {
                    const el = document.createElement('span');
                    el.className = 'rising-item font-amiri font-bold text-pink-600';
                    el.textContent = items[Math.floor(Math.random() * items.length)];
                    
                    el.style.left = `${Math.random() * 92 + 4}vw`;
                    el.style.fontSize = `${Math.floor(Math.random() * 18) + 22}px`;
                    el.style.animationDuration = `${(Math.random() * 1.5 + 2.5).toFixed(2)}s`;

                    document.body.appendChild(el);

                    setTimeout(() => {
                        el.remove();
                    }, 4100);
                }, i * 70);
            }
        };

        // 6. دالة التبديل للبطاقة الثانية (إظهار وإخفاء دون حذف الأزرار)
        window.toggleExtraSurpriseCard = function() {
            const extraCard = document.getElementById('extra-surprise-card');
            const isHidden = extraCard.classList.contains('hidden') || extraCard.style.display === 'none';

            if (isHidden) {
                extraCard.style.display = 'block';
                extraCard.classList.remove('hidden');
                extraCard.classList.remove('animate-pop-in');
                void extraCard.offsetWidth;
                extraCard.classList.add('animate-pop-in');
                window.launchBouquetShower();

                setTimeout(() => {
                    extraCard.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
                }, 150);
            } else {
                extraCard.style.display = 'none';
            }
        };

        if (document.readyState === 'loading') {
            document.addEventListener('DOMContentLoaded', createFloatingSymbols);
        } else {
            createFloatingSymbols();
        }
    </script>
</body>
</html>
