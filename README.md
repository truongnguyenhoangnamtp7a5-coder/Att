<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thử Thách Mạng Máy Tính: Router & Modem</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Canvas Confetti for celebrations -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <!-- Google Fonts Inter & Outfit -->
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700;800&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 50%, #311042 100%);
            min-height: 100vh;
        }
        .heading-font {
            font-family: 'Outfit', sans-serif;
        }
        /* Custom Glassmorphism Styling */
        .glass-panel {
            background: rgba(30, 41, 59, 0.7);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        /* Custom Button Hover animations */
        .btn-glow {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 0 15px rgba(99, 102, 241, 0.3);
        }
        .btn-glow:hover {
            transform: translateY(-2px);
            box-shadow: 0 0 25px rgba(99, 102, 241, 0.6);
        }
        /* Custom pulse animation for status badges */
        @keyframes pulse-subtle {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.85; transform: scale(1.02); }
        }
        .pulse-active {
            animation: pulse-subtle 2s infinite ease-in-out;
        }
    </style>
</head>
<body class="text-slate-100 min-h-screen flex flex-col justify-between items-center p-4 md:p-6 relative overflow-x-hidden">

    <!-- Header / Branding Bar -->
    <header class="w-full max-w-4xl flex justify-between items-center py-4 px-6 glass-panel rounded-2xl shadow-xl mb-6 z-10">
        <div class="flex items-center space-x-3">
            <div class="w-10 h-10 rounded-xl bg-indigo-600 flex items-center justify-center text-white shadow-lg shadow-indigo-500/30">
                <i class="fa-solid fa-network-wired text-xl"></i>
            </div>
            <div>
                <h1 class="heading-font font-bold text-lg md:text-xl tracking-wide bg-clip-text text-transparent bg-gradient-to-r from-indigo-300 via-purple-300 to-pink-300">
                    NetMaster Quiz
                </h1>
                <p class="text-xs text-slate-400">Kiến thức Router & Modem</p>
            </div>
        </div>
        <div class="flex items-center space-x-2 bg-slate-800/80 px-3 py-1.5 rounded-full border border-slate-700/50">
            <i class="fa-solid fa-graduation-cap text-indigo-400 text-sm"></i>
            <span class="text-xs font-semibold text-slate-300">Tin Học Bài 3 & 4</span>
        </div>
    </header>

    <!-- Main Content Container -->
    <main class="w-full max-w-4xl flex-1 flex flex-col justify-center items-center z-10 my-2">

        <!-- 1. START SCREEN -->
        <div id="start-screen" class="w-full glass-panel p-6 md:p-10 rounded-3xl shadow-2xl text-center transition-all duration-300">
            <div class="w-20 h-20 bg-gradient-to-tr from-indigo-500 to-purple-600 rounded-3xl mx-auto flex items-center justify-center shadow-lg shadow-indigo-500/40 mb-6 pulse-active">
                <i class="fa-solid fa-gamepad text-4xl text-white"></i>
            </div>
            <h2 class="heading-font text-3xl md:text-4xl font-extrabold text-white mb-3">
                Thử Thách: Router & Modem
            </h2>
            <p class="text-slate-300 text-sm md:text-base max-w-xl mx-auto mb-8 leading-relaxed">
                Củng cố toàn bộ kiến thức về bộ định tuyến Router, các cổng kết nối LAN/WAN, chức năng Modem và quá trình chuyển đổi tín hiệu qua trò chơi tương tác 10 câu hỏi!
            </p>

            <!-- Quiz Highlights Grid -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-8 text-left max-w-2xl mx-auto">
                <div class="glass-card p-4 rounded-2xl border border-slate-700/50 flex items-center space-x-3">
                    <div class="p-3 bg-indigo-500/20 text-indigo-400 rounded-xl">
                        <i class="fa-solid fa-list-check text-xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xs text-slate-400 font-medium">Số lượng</h4>
                        <p class="text-sm font-bold text-white">10 Câu Hỏi Trắc Nghiệm</p>
                    </div>
                </div>
                <div class="glass-card p-4 rounded-2xl border border-slate-700/50 flex items-center space-x-3">
                    <div class="p-3 bg-amber-500/20 text-amber-400 rounded-xl">
                        <i class="fa-solid fa-clock text-xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xs text-slate-400 font-medium">Thời gian</h4>
                        <p class="text-sm font-bold text-white">15 Giây / Câu</p>
                    </div>
                </div>
                <div class="glass-card p-4 rounded-2xl border border-slate-700/50 flex items-center space-x-3">
                    <div class="p-3 bg-emerald-500/20 text-emerald-400 rounded-xl">
                        <i class="fa-solid fa-award text-xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xs text-slate-400 font-medium">Giải thích</h4>
                        <p class="text-sm font-bold text-white">Chi Tiết Mỗi Câu</p>
                    </div>
                </div>
            </div>

            <button id="btn-start" onclick="quizApp.startQuiz()" class="btn-glow px-8 py-4 bg-gradient-to-r from-indigo-500 via-purple-600 to-pink-600 text-white font-bold rounded-2xl text-lg hover:brightness-110 active:scale-95 transition-all duration-200">
                <i class="fa-solid fa-play mr-2"></i> Bắt Đầu Ngay
            </button>
        </div>

        <!-- 2. QUIZ INTERFACE SCREEN -->
        <div id="quiz-screen" class="w-full glass-panel p-6 md:p-8 rounded-3xl shadow-2xl hidden flex-col justify-between">
            <!-- Top Status Bar: Progress, Timer, Score -->
            <div>
                <div class="flex justify-between items-center mb-4">
                    <!-- Question Counter -->
                    <span class="text-xs md:text-sm font-semibold text-indigo-300 bg-indigo-950/60 px-3 py-1.5 rounded-full border border-indigo-800/40">
                        Câu hỏi <span id="current-question-num" class="text-white font-bold">1</span>/<span id="total-questions-num">10</span>
                    </span>

                    <!-- Score Indicator -->
                    <div class="flex items-center space-x-2 bg-slate-800/80 px-3 py-1.5 rounded-full border border-slate-700">
                        <i class="fa-solid fa-star text-amber-400 text-sm"></i>
                        <span class="text-xs text-slate-400 font-medium">Điểm:</span>
                        <span id="current-score" class="text-sm font-bold text-emerald-400">0</span>
                    </div>

                    <!-- Countdown Timer -->
                    <div id="timer-box" class="flex items-center space-x-2 bg-slate-800/80 px-3 py-1.5 rounded-full border border-slate-700 text-amber-400">
                        <i class="fa-solid fa-stopwatch text-sm"></i>
                        <span id="timer-count" class="text-sm font-bold">15</span>s
                    </div>
                </div>

                <!-- Progress Bar Container -->
                <div class="w-full bg-slate-800/80 rounded-full h-2.5 mb-6 overflow-hidden p-0.5 border border-slate-700/50">
                    <div id="quiz-progress-bar" class="bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 h-full rounded-full transition-all duration-300" style="width: 10%;"></div>
                </div>

                <!-- Question Text -->
                <div class="mb-6">
                    <span id="question-category" class="inline-block px-2.5 py-1 text-[11px] font-bold text-indigo-300 bg-indigo-900/50 rounded-md uppercase tracking-wider mb-2">Chủ đề: Router</span>
                    <h3 id="question-text" class="heading-font text-lg md:text-xl font-bold text-slate-100 leading-snug">
                        Nội dung câu hỏi sẽ hiển thị ở đây?
                    </h3>
                </div>

                <!-- Options List -->
                <div id="options-container" class="space-y-3 mb-6">
                    <!-- Options injected via JavaScript -->
                </div>
            </div>

            <!-- Explanation Box (Initially Hidden) -->
            <div id="explanation-card" class="hidden glass-card p-4 rounded-2xl border border-indigo-500/30 bg-indigo-950/40 mb-6 animate-fade-in">
                <div class="flex items-start space-x-3">
                    <div id="explanation-icon" class="p-2 rounded-lg bg-emerald-500/20 text-emerald-400 mt-0.5">
                        <i class="fa-solid fa-circle-check"></i>
                    </div>
                    <div>
                        <h4 id="explanation-title" class="text-sm font-bold text-white mb-1">Giải thích chi tiết:</h4>
                        <p id="explanation-text" class="text-xs md:text-sm text-slate-300 leading-relaxed">
                            Nội dung giải thích dựa trên SGK Tin Học.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Bottom Actions -->
            <div class="flex justify-end pt-2 border-t border-slate-800">
                <button id="btn-next" onclick="quizApp.nextQuestion()" class="hidden btn-glow px-6 py-2.5 bg-gradient-to-r from-indigo-500 to-purple-600 text-white font-semibold rounded-xl text-sm flex items-center hover:brightness-110 active:scale-95 transition-all">
                    <span>Câu Tiếp Theo</span>
                    <i class="fa-solid fa-arrow-right ml-2"></i>
                </button>
            </div>
        </div>

        <!-- 3. RESULTS SCREEN -->
        <div id="result-screen" class="w-full glass-panel p-6 md:p-8 rounded-3xl shadow-2xl hidden text-center">
            <div id="result-badge" class="w-20 h-20 bg-emerald-500/20 border-2 border-emerald-500 text-emerald-400 rounded-full mx-auto flex items-center justify-center text-3xl mb-4">
                <i class="fa-solid fa-trophy"></i>
            </div>
            
            <h2 class="heading-font text-2xl md:text-3xl font-extrabold text-white mb-1">Hoàn Thành Bài Kiểm Tra!</h2>
            <p id="result-feedback" class="text-slate-300 text-sm mb-6">Bạn đã thể hiện sự hiểu biết rất tốt về bài học.</p>

            <!-- Final Score Summary Cards -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-3 mb-6">
                <div class="glass-card p-3.5 rounded-2xl border border-slate-700/60">
                    <p class="text-xs text-slate-400 mb-1">Tổng điểm</p>
                    <p id="final-score-text" class="text-2xl font-black text-amber-400">80/100</p>
                </div>
                <div class="glass-card p-3.5 rounded-2xl border border-slate-700/60">
                    <p class="text-xs text-slate-400 mb-1">Trả lời đúng</p>
                    <p id="correct-count-text" class="text-2xl font-black text-emerald-400">8/10</p>
                </div>
                <div class="glass-card p-3.5 rounded-2xl border border-slate-700/60">
                    <p class="text-xs text-slate-400 mb-1">Trả lời sai</p>
                    <p id="wrong-count-text" class="text-2xl font-black text-rose-400">2/10</p>
                </div>
                <div class="glass-card p-3.5 rounded-2xl border border-slate-700/60">
                    <p class="text-xs text-slate-400 mb-1">Tỷ lệ chính xác</p>
                    <p id="accuracy-text" class="text-2xl font-black text-indigo-400">80%</p>
                </div>
            </div>

            <!-- Review Answer Section -->
            <div class="text-left mb-6">
                <h3 class="text-base font-bold text-white mb-3 flex items-center">
                    <i class="fa-solid fa-magnifying-glass-chart mr-2 text-indigo-400"></i> Xem lại danh sách câu hỏi
                </h3>
                <div id="review-list" class="space-y-3 max-h-64 overflow-y-auto pr-2 custom-scrollbar">
                    <!-- Review items injected via JS -->
                </div>
            </div>

            <!-- Action buttons -->
            <div class="flex justify-center space-x-4">
                <button onclick="quizApp.restartQuiz()" class="btn-glow px-6 py-3 bg-gradient-to-r from-indigo-500 to-purple-600 text-white font-bold rounded-xl text-sm flex items-center hover:brightness-110 active:scale-95 transition-all">
                    <i class="fa-solid fa-rotate-right mr-2"></i> Chơi Lại Trò Chơi
                </button>
            </div>
        </div>

    </main>

    <!-- Footer -->
    <footer class="w-full max-w-4xl text-center py-3 text-slate-500 text-xs z-10">
        Trò chơi học tập tương tác • Nội dung dựa trên SGK Tin Học (Nối Mạng Máy Tính & Thiết Bị Mạng)
    </footer>

    <!-- Audio FX Synthesizer using Web Audio API -->
    <script>
        // Audio Synth Helper for Web Audio API sound effects without external MP3 files
        class SoundFX {
            constructor() {
                this.ctx = null;
            }
            init() {
                if (!this.ctx) {
                    this.ctx = new (window.AudioContext || window.webkitAudioContext)();
                }
            }
            playCorrect() {
                this.init();
                const now = this.ctx.currentTime;
                const osc1 = this.ctx.createOscillator();
                const osc2 = this.ctx.createOscillator();
                const gain = this.ctx.createGain();

                osc1.type = 'sine';
                osc2.type = 'triangle';
                osc1.frequency.setValueAtTime(523.25, now); // C5
                osc1.frequency.exponentialRampToValueAtTime(659.25, now + 0.1); // E5
                osc1.frequency.exponentialRampToValueAtTime(783.99, now + 0.2); // G5

                gain.gain.setValueAtTime(0.2, now);
                gain.gain.exponentialRampToValueAtTime(0.01, now + 0.35);

                osc1.connect(gain);
                osc2.connect(gain);
                gain.connect(this.ctx.destination);

                osc1.start(now);
                osc2.start(now);
                osc1.stop(now + 0.35);
                osc2.stop(now + 0.35);
            }
            playWrong() {
                this.init();
                const now = this.ctx.currentTime;
                const osc = this.ctx.createOscillator();
                const gain = this.ctx.createGain();

                osc.type = 'sawtooth';
                osc.frequency.setValueAtTime(220, now); // A3
                osc.frequency.exponentialRampToValueAtTime(130, now + 0.25); // C3

                gain.gain.setValueAtTime(0.2, now);
                gain.gain.exponentialRampToValueAtTime(0.01, now + 0.3);

                osc.connect(gain);
                gain.connect(this.ctx.destination);

                osc.start(now);
                osc.stop(now + 0.3);
            }
            playTimerTick() {
                this.init();
                const now = this.ctx.currentTime;
                const osc = this.ctx.createOscillator();
                const gain = this.ctx.createGain();

                osc.type = 'sine';
                osc.frequency.setValueAtTime(800, now);

                gain.gain.setValueAtTime(0.03, now);
                gain.gain.exponentialRampToValueAtTime(0.001, now + 0.05);

                osc.connect(gain);
                gain.connect(this.ctx.destination);

                osc.start(now);
                osc.stop(now + 0.05);
            }
        }

        const soundFX = new SoundFX();
    </script>

    <script>
        // Quiz Data extracted directly from the provided textbook material
        const quizQuestions = [
            {
                id: 1,
                category: "ROUTER (BỘ ĐỊNH TUYẾN)",
                question: "Thiết bị mạng nào được sử dụng để kết nối hai hay nhiều mạng LAN khác nhau qua môi trường Internet?",
                options: [
                    "Hub",
                    "Switch",
                    "Router (Bộ định tuyến)",
                    "Cáp mạng LAN"
                ],
                correct: 2,
                explanation: "Theo bài học, khi kết nối hai máy tính thuộc hai mạng LAN khác nhau qua Internet, người ta không thể dùng Hub hay Switch mà cần sử dụng Router (Bộ định tuyến) để chuyển tiếp dữ liệu."
            },
            {
                id: 2,
                category: "CỔNG KẾT NỐI ROUTER",
                question: "Cổng nào trên Router có nhiệm vụ kết nối trực tiếp vào mạng LAN nội bộ?",
                options: [
                    "Cổng WAN",
                    "Cổng LAN",
                    "Cổng Quang",
                    "Cổng Điện thoại"
                ],
                correct: 1,
                explanation: "Mỗi router có một số cổng có thể kết nối trực tiếp vào mạng LAN được gọi là Cổng LAN. Còn cổng dùng kết nối với các router khác (mạng diện rộng) gọi là Cổng WAN."
            },
            {
                id: 3,
                category: "CỔNG KẾT NỐI ROUTER",
                question: "Cổng nào trên Router dùng để kết nối với các router khác bên ngoài mạng diện rộng?",
                options: [
                    "Cổng LAN",
                    "Cổng USB",
                    "Cổng WAN",
                    "Cổng Console"
                ],
                correct: 2,
                explanation: "Dữ liệu muốn chuyển ra ngoài mạng LAN khác phải đi qua cổng WAN để tới các router trung chuyển trên môi trường Internet."
            },
            {
                id: 4,
                category: "ĐỊNH TUYẾN (ROUTING)",
                question: "Thuật ngữ 'Định tuyến' (Routing) trong mạng máy tính có nghĩa là gì?",
                options: [
                    "Sửa chữa đường dây điện thoại bị hỏng",
                    "Chọn đường / chọn cổng thích hợp để chuyển dữ liệu đi tới đích",
                    "Chuyển đổi tín hiệu mạng từ sóng radio sang điện",
                    "Tăng tốc độ truy cập Internet cho mạng nội bộ"
                ],
                correct: 1,
                explanation: "Thuật ngữ 'định tuyến' (routing) hàm ý router phải chọn một cổng thích hợp để gửi dữ liệu đi sao cho tới được LAN của máy nhận."
            },
            {
                id: 5,
                category: "ROUTER WI-FI GIA ĐÌNH",
                question: "Thông thường, Router Wi-Fi dùng trong gia đình có cấu hình cổng kết nối phổ biến như thế nào?",
                options: [
                    "Nhiều cổng WAN và 1 cổng LAN",
                    "Chỉ có các cổng WAN, không có cổng LAN",
                    "Có 1 cổng WAN (kết nối ISP) và 4 cổng LAN, tích hợp phát Wi-Fi",
                    "Không có cổng kết nối vật lý nào"
                ],
                correct: 2,
                explanation: "Các router mạng gia đình thường chỉ có 1 cổng WAN kết nối đến nhà cung cấp dịch vụ Internet (ISP) mà không cần định tuyến phức tạp, kèm theo 4 cổng LAN và tích hợp bộ thu phát Wi-Fi."
            },
            {
                id: 6,
                category: "MODEM - CHỨC NĂNG",
                question: "Chức năng cốt lõi của thiết bị Modem là gì?",
                options: [
                    "Chỉ chọn hướng luồng dữ liệu chứ không đổi tín hiệu",
                    "Chuyển đổi tín hiệu 2 chiều giữa tín hiệu số (digital) và tín hiệu tương tự (analog)",
                    "Làm thay đổi bản chất và nội dung của dữ liệu truyền đi",
                    "Tạo đường dây điện thoại mới cho hộ gia đình"
                ],
                correct: 1,
                explanation: "Modem thực hiện chuyển đổi tín hiệu số (biểu diễn 0 hoặc 1) thành tín hiệu tương tự (analog - quang, sóng điện từ...) và ngược lại. Router chỉ hướng luồng dữ liệu chứ không chuyển đổi tín hiệu."
            },
            {
                id: 7,
                category: "ĐẶC ĐIỂM MODEM",
                question: "Khi Modem thực hiện chuyển đổi tín hiệu, bản chất của dữ liệu được mang qua Modem có bị thay đổi không?",
                options: [
                    "Có, dữ liệu bị mã hoá thành ngôn ngữ khác",
                    "Có, dữ liệu bị nén bớt dung lượng",
                    "Không, Modem chỉ thay đổi dạng tín hiệu chứ không làm thay đổi dữ liệu",
                    "Tùy thuộc vào tốc độ đường truyền Internet"
                ],
                correct: 2,
                explanation: "SGK ghi rõ: 'Modem chỉ thay đổi tín hiệu mà không làm thay đổi dữ liệu được mang bởi tín hiệu'."
            },
            {
                id: 8,
                category: "CÁC LOẠI MODEM",
                question: "Loại Modem nào sử dụng SIM để truy cập Internet qua hệ thống điện thoại di động và phát lại qua sóng Wi-Fi?",
                options: [
                    "Modem quay số (Dial-up)",
                    "Modem ADSL",
                    "Modem GSM (3G, 4G, 5G...)",
                    "Modem cáp quang độc lập"
                ],
                correct: 2,
                explanation: "Modem GSM 3G, 4G, 5G,... có cắm SIM để truy cập Internet qua mạng di động và phát lại bằng sóng Wi-Fi hoặc nối qua cáp mạng."
            },
            {
                id: 9,
                category: "QUÁ TRÌNH TRUYỀN DỮ LIỆU",
                question: "Theo sơ đồ truyền dữ liệu qua Internet, dữ liệu gửi từ máy gửi ở LAN A đến máy nhận ở LAN B phải trải qua lộ trình nào?",
                options: [
                    "Đi thẳng từ Cổng WAN -> Cổng LAN -> Máy nhận mà không qua Router",
                    "Qua cổng LAN của router xuất phát -> ra cổng WAN -> trung chuyển qua các Router -> tới cổng LAN của router cuối -> đến máy nhận",
                    "Đi từ Modem -> Switch -> Máy tính mà không qua cổng LAN",
                    "Trực tiếp chuyển thành sóng Wi-Fi tới máy nhận"
                ],
                correct: 1,
                explanation: "Dữ liệu từ máy tính ở LAN chuyển qua cổng LAN của router -> ra ngoài qua cổng WAN -> qua nhiều router trung chuyển -> tới router cuối cùng -> chuyển qua cổng LAN để tới máy nhận."
            },
            {
                id: 10,
                category: "XU HƯỚNG CÔNG NGHỆ",
                question: "Tại sao ngày nay chúng ta ít khi nhìn thấy các thiết bị Modem nằm độc lập rời rạc?",
                options: [
                    "Vì Modem đã bị khai tử và không còn cần thiết",
                    "Vì chức năng Modem ngày nay thường được tích hợp ngay vào bên trong Router",
                    "Vì tất cả máy tính hiện đại đều tự trang bị sẵn Modem bên trong CPU",
                    "Vì cáp quang không cần chuyển đổi tín hiệu nữa"
                ],
                correct: 1,
                explanation: "Thời kỳ đầu modem tách rời router, nhưng sau này chức năng modem đã được tích hợp ngay vào bên trong router nên chúng ta ít thấy các modem độc lập."
            }
        ];

        class QuizApp {
            constructor(questions) {
                this.questions = questions;
                this.currentIndex = 0;
                this.score = 0;
                this.answersHistory = []; // Tracks user answers for review
                this.timer = null;
                this.timeLeft = 15;
                this.isAnswered = false;

                // Elements
                this.startScreen = document.getElementById('start-screen');
                this.quizScreen = document.getElementById('quiz-screen');
                this.resultScreen = document.getElementById('result-screen');

                this.currentQuestionNumEl = document.getElementById('current-question-num');
                this.totalQuestionsNumEl = document.getElementById('total-questions-num');
                this.currentScoreEl = document.getElementById('current-score');
                this.timerCountEl = document.getElementById('timer-count');
                this.progressBarEl = document.getElementById('quiz-progress-bar');
                this.questionCategoryEl = document.getElementById('question-category');
                this.questionTextEl = document.getElementById('question-text');
                this.optionsContainerEl = document.getElementById('options-container');

                this.explanationCard = document.getElementById('explanation-card');
                this.explanationTitle = document.getElementById('explanation-title');
                this.explanationText = document.getElementById('explanation-text');
                this.explanationIcon = document.getElementById('explanation-icon');

                this.btnNext = document.getElementById('btn-next');
            }

            startQuiz() {
                this.currentIndex = 0;
                this.score = 0;
                this.answersHistory = [];
                this.totalQuestionsNumEl.innerText = this.questions.length;

                this.startScreen.classList.add('hidden');
                this.resultScreen.classList.add('hidden');
                this.quizScreen.classList.remove('hidden');
                this.quizScreen.classList.add('flex');

                this.loadQuestion();
            }

            loadQuestion() {
                this.isAnswered = false;
                this.explanationCard.classList.add('hidden');
                this.btnNext.classList.add('hidden');

                const currentQ = this.questions[this.currentIndex];

                // Update UI Header
                this.currentQuestionNumEl.innerText = this.currentIndex + 1;
                this.currentScoreEl.innerText = this.score;
                this.questionCategoryEl.innerText = currentQ.category;
                this.questionTextEl.innerText = currentQ.question;

                // Update Progress Bar
                const progressPercent = ((this.currentIndex + 1) / this.questions.length) * 100;
                this.progressBarEl.style.width = `${progressPercent}%`;

                // Render Options Buttons
                this.optionsContainerEl.innerHTML = '';
                const optionLetters = ['A', 'B', 'C', 'D'];

                currentQ.options.forEach((optText, index) => {
                    const btn = document.createElement('button');
                    btn.className = `option-btn w-full text-left p-4 rounded-2xl glass-card border border-slate-700/70 hover:border-indigo-500/80 hover:bg-slate-800/80 transition-all duration-200 flex items-center space-x-3 group relative overflow-hidden`;
                    btn.onclick = () => this.selectAnswer(index);

                    btn.innerHTML = `
                        <span class="w-8 h-8 rounded-xl bg-slate-800 border border-slate-600 flex items-center justify-center font-bold text-xs text-indigo-300 group-hover:bg-indigo-600 group-hover:text-white transition-colors shrink-0">
                            ${optionLetters[index]}
                        </span>
                        <span class="text-xs md:text-sm text-slate-200 font-medium group-hover:text-white flex-1">
                            ${optText}
                        </span>
                        <span class="status-icon text-lg hidden"></span>
                    `;
                    this.optionsContainerEl.appendChild(btn);
                });

                // Reset and start countdown timer
                this.resetTimer();
            }

            resetTimer() {
                clearInterval(this.timer);
                this.timeLeft = 15;
                this.timerCountEl.innerText = this.timeLeft;
                this.timerCountEl.parentElement.classList.remove('text-rose-500', 'animate-pulse');
                this.timerCountEl.parentElement.classList.add('text-amber-400');

                this.timer = setInterval(() => {
                    this.timeLeft--;
                    this.timerCountEl.innerText = this.timeLeft;

                    if (this.timeLeft <= 5 && this.timeLeft > 0) {
                        soundFX.playTimerTick();
                        this.timerCountEl.parentElement.classList.remove('text-amber-400');
                        this.timerCountEl.parentElement.classList.add('text-rose-500', 'animate-pulse');
                    }

                    if (this.timeLeft <= 0) {
                        clearInterval(this.timer);
                        this.handleTimeOut();
                    }
                }, 1000);
            }

            handleTimeOut() {
                if (this.isAnswered) return;
                this.selectAnswer(-1); // -1 indicates timeout
            }

            selectAnswer(selectedIndex) {
                if (this.isAnswered) return;
                this.isAnswered = true;
                clearInterval(this.timer);

                const currentQ = this.questions[this.currentIndex];
                const optionButtons = this.optionsContainerEl.querySelectorAll('.option-btn');
                const isCorrect = selectedIndex === currentQ.correct;

                // Save to history
                this.answersHistory.push({
                    question: currentQ.question,
                    userSelectedIndex: selectedIndex,
                    correctIndex: currentQ.correct,
                    isCorrect: isCorrect,
                    explanation: currentQ.explanation
                });

                if (isCorrect) {
                    this.score += 10;
                    this.currentScoreEl.innerText = this.score;
                    soundFX.playCorrect();
                } else {
                    soundFX.playWrong();
                }

                // Highlight buttons based on correctness
                optionButtons.forEach((btn, idx) => {
                    btn.disabled = true;
                    btn.classList.remove('hover:border-indigo-500/80', 'hover:bg-slate-800/80');

                    const iconEl = btn.querySelector('.status-icon');
                    iconEl.classList.remove('hidden');

                    if (idx === currentQ.correct) {
                        // Mark Correct
                        btn.classList.add('bg-emerald-950/80', 'border-emerald-500', 'text-emerald-200');
                        iconEl.innerHTML = '<i class="fa-solid fa-circle-check text-emerald-400"></i>';
                    } else if (idx === selectedIndex) {
                        // Mark Wrong Selection
                        btn.classList.add('bg-rose-950/80', 'border-rose-500', 'text-rose-200');
                        iconEl.innerHTML = '<i class="fa-solid fa-circle-xmark text-rose-400"></i>';
                    } else {
                        btn.classList.add('opacity-40');
                    }
                });

                // Display Detailed Explanation
                this.explanationCard.classList.remove('hidden');
                if (isCorrect) {
                    this.explanationCard.className = "glass-card p-4 rounded-2xl border border-emerald-500/40 bg-emerald-950/30 mb-6 animate-fade-in";
                    this.explanationIcon.className = "p-2 rounded-lg bg-emerald-500/20 text-emerald-400 mt-0.5";
                    this.explanationIcon.innerHTML = '<i class="fa-solid fa-circle-check text-xl"></i>';
                    this.explanationTitle.innerText = "Chính xác!";
                    this.explanationTitle.className = "text-sm font-bold text-emerald-300 mb-1";
                } else {
                    this.explanationCard.className = "glass-card p-4 rounded-2xl border border-rose-500/40 bg-rose-950/30 mb-6 animate-fade-in";
                    this.explanationIcon.className = "p-2 rounded-lg bg-rose-500/20 text-rose-400 mt-0.5";
                    this.explanationIcon.innerHTML = selectedIndex === -1 ? '<i class="fa-solid fa-hourglass-end text-xl"></i>' : '<i class="fa-solid fa-triangle-exclamation text-xl"></i>';
                    this.explanationTitle.innerText = selectedIndex === -1 ? "Hết thời gian trả lời!" : "Chưa chính xác!";
                    this.explanationTitle.className = "text-sm font-bold text-rose-300 mb-1";
                }
                this.explanationText.innerText = currentQ.explanation;

                // Show Next Button
                this.btnNext.classList.remove('hidden');
            }

            nextQuestion() {
                this.currentIndex++;
                if (this.currentIndex < this.questions.length) {
                    this.loadQuestion();
                } else {
                    this.showResults();
                }
            }

            showResults() {
                this.quizScreen.classList.add('hidden');
                this.resultScreen.classList.remove('hidden');

                const total = this.questions.length;
                const correctCount = this.answersHistory.filter(a => a.isCorrect).length;
                const wrongCount = total - correctCount;
                const accuracy = Math.round((correctCount / total) * 100);

                // Populate Summary
                document.getElementById('final-score-text').innerText = `${this.score}/${total * 10}`;
                document.getElementById('correct-count-text').innerText = `${correctCount}/${total}`;
                document.getElementById('wrong-count-text').innerText = `${wrongCount}/${total}`;
                document.getElementById('accuracy-text').innerText = `${accuracy}%`;

                // Feedback Badge & Text
                const badgeEl = document.getElementById('result-badge');
                const feedbackEl = document.getElementById('result-feedback');

                if (accuracy >= 80) {
                    badgeEl.className = "w-20 h-20 bg-emerald-500/20 border-2 border-emerald-500 text-emerald-400 rounded-full mx-auto flex items-center justify-center text-3xl mb-4";
                    badgeEl.innerHTML = '<i class="fa-solid fa-trophy"></i>';
                    feedbackEl.innerText = "Xuất sắc! Bạn đã nắm vững toàn bộ kiến thức bài Router & Modem!";
                    
                    // Confetti explosion on high score
                    confetti({
                        particleCount: 100,
                        spread: 70,
                        origin: { y: 0.6 }
                    });
                } else if (accuracy >= 50) {
                    badgeEl.className = "w-20 h-20 bg-amber-500/20 border-2 border-amber-500 text-amber-400 rounded-full mx-auto flex items-center justify-center text-3xl mb-4";
                    badgeEl.innerHTML = '<i class="fa-solid fa-medal"></i>';
                    feedbackEl.innerText = "Khá tốt! Hãy ôn lại một vài câu trả lời sai bên dưới để đạt điểm tối đa nhé.";
                } else {
                    badgeEl.className = "w-20 h-20 bg-rose-500/20 border-2 border-rose-500 text-rose-400 rounded-full mx-auto flex items-center justify-center text-3xl mb-4";
                    badgeEl.innerHTML = '<i class="fa-solid fa-book-open"></i>';
                    feedbackEl.innerText = "Bạn nên đọc lại kiến thức bài học trong SGK và bấm Chơi Lại để thử sức nhé!";
                }

                // Render Answer Review List
                const reviewListEl = document.getElementById('review-list');
                reviewListEl.innerHTML = '';

                this.answersHistory.forEach((item, idx) => {
                    const card = document.createElement('div');
                    card.className = `p-3.5 rounded-xl border ${item.isCorrect ? 'bg-emerald-950/20 border-emerald-800/40' : 'bg-rose-950/20 border-rose-800/40'} text-left text-xs`;
                    
                    card.innerHTML = `
                        <div class="flex items-start justify-between mb-1.5">
                            <p class="font-bold text-slate-200">Câu ${idx + 1}: ${item.question}</p>
                            <span class="px-2 py-0.5 rounded-full text-[10px] font-bold shrink-0 ml-2 ${item.isCorrect ? 'bg-emerald-500/20 text-emerald-400' : 'bg-rose-500/20 text-rose-400'}">
                                ${item.isCorrect ? 'Đúng' : 'Sai'}
                            </span>
                        </div>
                        <p class="text-slate-400 mb-1"><span class="font-semibold text-slate-300">Giải thích:</span> ${item.explanation}</p>
                    `;
                    reviewListEl.appendChild(card);
                });
            }

            restartQuiz() {
                this.startQuiz();
            }
        }

        // Initialize Global App Instance
        let quizApp;
        window.addEventListener('DOMContentLoaded', () => {
            quizApp = new QuizApp(quizQuestions);
        });
    </script>
</body>
</html>
