<'james_mlbb>
<html lang="kk">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ML Almaz — Mobile Legends Алмаз Сату</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
  <style>
    .hero-bg { background: linear-gradient(135deg, #4f46e5, #7c3aed); }
    .card-hover:hover { transform: translateY(-8px); }
  </style>
</head>
<body class="bg-gray-950 text-white scroll-smooth">

  <!-- НАСТРОЙКА: ТӨМЕНДЕГІ 'СІЗДІҢ_ЛОГИН' ДЕГЕН ЖЕРГЕ ӨЗ ТЕЛЕГРАМЫҢДЫ ЖАЗ (МЫСАЛЫ: 'Alihan_pro') -->
  <script>
    const TELEGRAM_USERNAME = 'СІЗДІҢ_ЛОГИН';

    // Telegram-ға тапсырыс жіберу функциясы
    function buyDiamonds(amount, price) {
      const gameId = document.getElementById('game_id').value.trim();
      const serverId = document.getElementById('server_id').value.trim();

      if (!gameId || !serverId) {
        alert('Өтініш, алдымен Game ID және Server ID енгізіңіз!');
        document.getElementById('id-section').scrollIntoView({ behavior: 'smooth' });
        return;
      }

      // Telegram-ға жіберілетін дайын мәтін
      const message = `Сәлеметсіз бе! Тапсырыс бергім келеді:\n\n💎 Пакет: ${amount} Алмаз\n💰 Бағасы: ${price}\n🆔 Game ID: ${gameId}\n🌐 Server ID: ${serverId}`;
      
      // Сілтеме жасау және өту
      const telegramUrl = `https://t.me/${TELEGRAM_USERNAME}?text=${encodeURIComponent(message)}`;
      window.open(telegramUrl, '_blank');
    }
  </script>

  <!-- Navbar -->
  <nav class="bg-black/80 backdrop-blur-md fixed w-full z-50 border-b border-gray-800">
    <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
      <h1 class="text-2xl font-bold text-violet-500 tracking-wider">ML <span class="text-white">ALMAZ</span></h1>
      <a href="#id-section" class="bg-violet-600 hover:bg-violet-700 px-5 py-2 rounded-full font-semibold flex items-center gap-2 text-sm transition">
        <i class="fas fa-shopping-cart"></i> Тапсырыс беру
      </a>
    </div>
  </nav>

  <!-- Hero -->
  <section class="hero-bg pt-32 pb-20 text-center px-4">
    <div class="max-w-4xl mx-auto">
      <span class="bg-black/30 text-yellow-400 text-sm font-bold px-4 py-1.5 rounded-full uppercase tracking-wider">Лезде және Қауіпсіз</span>
      <h2 class="text-4xl md:text-6xl font-extrabold mb-4 mt-4 leading-tight">Mobile Legends Алмаздары</h2>
      <p class="text-xl md:text-2xl text-violet-100 mb-8 max-w-2xl mx-auto">ID-іңізді жазыңыз, пакетті таңдаңыз және 5 минутта алмаз алыңыз!</p>
      <a href="#id-section" class="inline-block bg-yellow-400 text-black font-extrabold text-lg px-8 py-4 rounded-2xl hover:bg-yellow-300 shadow-lg shadow-yellow-500/20 transition transform hover:scale-105">
        Бастау <i class="fas fa-arrow-down ml-2"></i>
      </a>
    </div>
  </section>

  <!-- БҰЛ БӨЛІМДЕ КЛИЕНТ ӨЗ ID-ІН ЖАЗАДЫ -->
  <section id="id-section" class="py-12 bg-gray-900 border-b border-gray-800">
    <div class="max-w-xl mx-auto px-6">
      <div class="bg-gray-950 p-8 rounded-3xl border border-gray-800 shadow-xl">
        <h3 class="text-xl font-bold text-center mb-6 text-violet-400 flex items-center justify-center gap-2">
          <i class="fas fa-user-tag"></i> 1-ҚАДАМ: Деректерді енгізіңіз
        </h3>
        
        <div class="grid grid-cols-2 gap-4">
          <div>
            <label class="block text-xs text-gray-400 font-semibold uppercase tracking-wider mb-2">Game ID</label>
            <input type="number" id="game_id" placeholder="123456789" 
                   class="w-full bg-gray-900 border border-gray-700 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-violet-500 font-mono tracking-wide">
          </div>
          <div>
            <label class="block text-xs text-gray-400 font-semibold uppercase tracking-wider mb-2">Server ID</label>
            <input type="number" id="server_id" placeholder="1234" 
                   class="w-full bg-gray-900 border border-gray-700 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-violet-500 font-mono tracking-wide">
          </div>
        </div>
        <p class="text-gray-500 text-xs mt-3 text-center"><i class="fas fa-info-circle"></i> ID-ді қатесіз жазыңыз. Ол сіздің профиліңізде көрсетілген.</p>
      </div>
    </div>
  </section>

  <!-- Packages -->
  <section id="packages" class="py-16 bg-gray-950">
    <div class="max-w-6xl mx-auto px-6">
      <div class="text-center mb-12">
        <h2 class="text-3xl font-bold mb-2">2-ҚАДАМ: Алмаз пакетін таңдаңыз</h2>
        <p class="text-gray-400 text-sm">Керекті көлемді таңдап, "Сатып алу" батырмасын басыңыз</p>
      </div>
      
      <div class="grid grid-cols-2 md:grid-cols-3 gap-4 md:gap-6">
        <!-- 100 Diamonds -->
        <div class="bg-gray-900 border border-gray-800 rounded-2xl p-5 card-hover transition flex flex-col justify-between">
          <div>
            <h3 class="text-2xl font-bold text-violet-400 flex items-center gap-1.5"><i class="fas fa-gem text-lg"></i> 100</h3>
            <p class="text-gray-400 text-xs mt-1">Diamonds</p>
            <p class="text-2xl font-extrabold mt-4 text-white">1 290 ₸</p>
          </div>
          <button onclick="buyDiamonds('100', '1 290 ₸')" class="block w-full text-center mt-4 bg-violet-600 hover:bg-violet-700 py-2.5 rounded-xl font-semibold text-sm transition">Сатып алу</button>
        </div>

        <!-- 300 Diamonds -->
        <div class="bg-gray-900 border border-yellow-500/50 rounded-2xl p-5 card-hover transition flex flex-col justify-between relative shadow-lg shadow-yellow-500/5">
          <span class="absolute -top-2.5 right-4 bg-yellow-500 text-black text-[10px] font-extrabold px-2 py-0.5 rounded-full uppercase">Хит</span>
          <div>
            <h3 class="text-2xl font-bold text-yellow-400 flex items-center gap-1.5"><i class="fas fa-gem text-lg"></i> 300</h3>
            <p class="text-gray-400 text-xs mt-1">Diamonds</p>
            <p class="text-2xl font-extrabold mt-4 text-white">3 490 ₸</p>
          </div>
          <button onclick="buyDiamonds('300', '3 490 ₸')" class="block w-full text-center mt-4 bg-yellow-500 hover:bg-yellow-400 text-black py-2.5 rounded-xl font-extrabold text-sm transition">Сатып алу</button>
        </div>

        <!-- 500 Diamonds -->
        <div class="bg-gray-900 border border-gray-800 rounded-2xl p-5 card-hover transition flex flex-col justify-between">
          <div>
            <h3 class="text-2xl font-bold text-violet-400 flex items-center gap-1.5"><i class="fas fa-gem text-lg"></i> 500</h3>
            <p class="text-gray-400 text-xs mt-1">Diamonds</p>
            <p class="text-2xl font-extrabold mt-4 text-white">5 690 ₸</p>
          </div>
          <button onclick="buyDiamonds('500', '5 690 ₸')" class="block w-full text-center mt-4 bg-violet-600 hover:bg-violet-700 py-2.5 rounded-xl font-semibold text-sm transition">Сатып алу</button>
        </div>

        <!-- 1000 Diamonds -->
        <div class="bg-gray-900 border border-gray-800 rounded-2xl p-5 card-hover transition flex flex-col justify-between">
          <div>
            <h3 class="text-2xl font-bold text-violet-400 flex items-center gap-1.5"><i class="fas fa-gem text-lg"></i> 1000</h3>
            <p class="text-gray-400 text-xs mt-1">Diamonds</p>
            <p class="text-2xl font-extrabold mt-4 text-white">10 900 ₸</p>
          </div>
          <button onclick="buyDiamonds('1000', '10 900 ₸')" class="block w-full text-center mt-4 bg-violet-600 hover:bg-violet-700 py-2.5 rounded-xl font-semibold text-sm transition">Сатып алу</button>
        </div>

        <!-- 1500 Diamonds -->
        <div class="bg-gray-900 border border-gray-800 rounded-2xl p-5 card-hover transition flex flex-col justify-between">
          <div>
            <h3 class="text-2xl font-bold text-violet-400 flex items-center gap-1.5"><i class="fas fa-gem text-lg"></i> 1500</h3>
            <p class="text-gray-400 text-xs mt-1">Diamonds</p>
            <p class="text-2xl font-extrabold mt-4 text-white">15 900 ₸</p>
          </div>
          <button onclick="buyDiamonds('1500', '15 900 ₸')" class="block w-full text-center mt-4 bg-violet-600 hover:bg-violet-700 py-2.5 rounded-xl font-semibold text-sm transition">Сатып алу</button>
        </div>

        <!-- 3000 Diamonds -->
        <div class="bg-gray-900 border border-gray-800 rounded-2xl p-5 card-hover transition flex flex-col justify-between">
          <div>
            <h3 class="text-2xl font-bold text-violet-400 flex items-center gap-1.5"><i class="fas fa-gem text-lg"></i> 3000</h3>
            <p class="text-gray-400 text-xs mt-1">Diamonds</p>
            <p class="text-2xl font-extrabold mt-4 text-white">30 500 ₸</p>
          </div>
          <button onclick="buyDiamonds('3000', '30 500 ₸')" class="block w-full text-center mt-4 bg-violet-600 hover:bg-violet-700 py-2.5 rounded-xl font-semibold text-sm transition">Сатып алу</button>
        </div>
      </div>
    </div>
  </section>

  <!-- FAQ Section -->
  <section class="py-16 bg-gray-900 border-t border-gray-800">
    <div class="max-w-3xl mx-auto px-6">
      <h2 class="text-2xl font-bold text-center mb-8">Жиі қойылатын сұрақтар</h2>
      <div class="space-y-4">
        <div class="p-5 bg-gray-950 rounded-2xl border border-gray-800">
          <h4 class="font-bold text-violet-400 mb-1">Алмаз қанша уақытта түседі?</h4>
          <p class="text-gray-400 text-sm">Төлем расталғаннан кейін 1-5 минут ішінде сіздің аккаунтыңызға тікелей жіберіледі.</p>
        </div>
        <div class="p-5 bg-gray-950 rounded-2xl border border-gray-800">
          <h4 class="font-bold text-violet-400 mb-1">Бұл қауіпсіз бе? Бұғаттау (Бан) болмай ма?</h4>
          <p class="text-gray-400 text-sm">Толықтай қауіпсіз. Алмаздар тек ресми Game ID арқылы жүктелетіндіктен, аккаунтыңызға ешқандай қауіп төнбейді.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-black py-8 text-center border-t border-gray-900">
    <p class="text-gray-500 text-xs px-4">Бұл сайт Mobile Legends ойынының ресми өкілі емес. Барлық сауда-саттық кепілдікпен орындалады.</p>
    <p class="mt-4 text-violet-500 font-medium text-sm">© 2026 ML Almaz. Барлық құқықтар қорғалған.</p>
  </footer>

</body>
</html>
