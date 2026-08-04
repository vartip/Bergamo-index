<!DOCTYPE html>
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bergamo Tip - Professional Betting Predictions</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Supabase JS Client -->
    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap');
        body { font-family: 'Plus Jakarta Sans', sans-serif; }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col selection:bg-emerald-500 selection:text-white">

    <!-- Top Navigation / Header -->
    <header class="sticky top-0 z-50 bg-slate-900/80 backdrop-blur-md border-b border-slate-800">
        <div class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <div class="bg-gradient-to-tr from-emerald-600 to-teal-400 p-2.5 rounded-xl shadow-lg shadow-emerald-900/30">
                    <i data-lucide="trophy" class="w-6 h-6 text-white"></i>
                </div>
                <div>
                    <h1 class="font-extrabold text-xl tracking-tight bg-gradient-to-r from-emerald-400 to-teal-200 bg-clip-text text-transparent">Bergamo Tip</h1>
                    <p class="text-xs text-slate-400 font-medium">Pro Betting Predictions</p>
                </div>
            </div>

            <div class="flex items-center space-x-2">
                <div id="auth-status-badge" class="px-3 py-1.5 text-xs font-bold bg-emerald-500/10 text-emerald-400 border border-emerald-500/20 rounded-lg flex items-center gap-1.5">
                    <i data-lucide="user-check" class="w-3.5 h-3.5"></i> <span id="user-label">VIP Member</span>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Container -->
    <main class="flex-1 max-w-7xl w-full mx-auto px-4 py-6">

        <!-- USER MINI APP VIEW -->
        <div id="user-app-view" class="space-y-6">
            
            <!-- Hero Banner -->
            <div class="relative overflow-hidden rounded-2xl bg-gradient-to-br from-emerald-900/40 via-slate-900 to-slate-900 border border-emerald-500/20 p-6 shadow-2xl">
                <div class="absolute -right-10 -bottom-10 w-60 h-60 bg-emerald-500/10 rounded-full blur-3xl pointer-events-none"></div>
                <div class="relative z-10 flex flex-col md:flex-row justify-between items-start md:items-center gap-4">
                    <div>
                        <span class="px-3 py-1 rounded-full text-xs font-bold bg-emerald-500/20 text-emerald-300 border border-emerald-500/30 uppercase tracking-widest">🔥 98% Accuracy Target</span>
                        <h2 class="text-2xl md:text-3xl font-extrabold mt-2 text-white">Daily Winning Accumulators & VIP Tips</h2>
                        <p class="text-slate-400 text-sm mt-1 max-w-xl">Get mathematically analyzed football and FIFA match predictions daily. Join our VIP channel for maximum returns.</p>
                    </div>
                    <a href="https://t.me/Bergam777" target="_blank" class="px-5 py-3 bg-gradient-to-r from-emerald-500 to-teal-500 hover:from-emerald-400 hover:to-teal-400 text-slate-950 font-bold rounded-xl shadow-lg shadow-emerald-500/25 flex items-center gap-2 transition transform active:scale-95 shrink-0">
                        <i data-lucide="send" class="w-4 h-4"></i> VIP Contact @Bergam777
                    </a>
                </div>
            </div>

            <!-- Navigation Tabs -->
            <div class="flex overflow-x-auto space-x-2 pb-2 scrollbar-none border-b border-slate-800">
                <button onclick="switchTab('free')" class="tab-btn px-5 py-2.5 rounded-xl text-sm font-bold transition flex items-center gap-2 bg-emerald-500 text-slate-950 shadow-md shadow-emerald-500/20" data-tab="free">
                    <i data-lucide="gift" class="w-4 h-4"></i> Free Tips
                </button>
                <button onclick="switchTab('vip')" class="tab-btn px-5 py-2.5 rounded-xl text-sm font-bold transition flex items-center gap-2 bg-slate-900 text-slate-400 hover:bg-slate-800 border border-slate-800" data-tab="vip">
                    <i data-lucide="crown" class="w-4 h-4 text-amber-400"></i> VIP Tips
                </button>
                <button onclick="switchTab('history')" class="tab-btn px-5 py-2.5 rounded-xl text-sm font-bold transition flex items-center gap-2 bg-slate-900 text-slate-400 hover:bg-slate-800 border border-slate-800" data-tab="history">
                    <i data-lucide="history" class="w-4 h-4"></i> History / Results
                </button>
            </div>

            <!-- Game Type Filter (Football vs FIFA) -->
            <div class="flex items-center gap-3">
                <span class="text-xs font-semibold text-slate-400">Filter Game Type:</span>
                <div class="inline-flex bg-slate-900 p-1 rounded-xl border border-slate-800">
                    <button onclick="filterGameType('ALL')" id="filter-all" class="px-3 py-1 text-xs font-bold rounded-lg bg-emerald-500 text-slate-950 transition">All</button>
                    <button onclick="filterGameType('Football')" id="filter-football" class="px-3 py-1 text-xs font-bold rounded-lg text-slate-400 hover:text-white transition">⚽ Football</button>
                    <button onclick="filterGameType('FIFA')" id="filter-fifa" class="px-3 py-1 text-xs font-bold rounded-lg text-slate-400 hover:text-white transition">🎮 FIFA</button>
                </div>
            </div>

            <!-- Content Panel Container -->
            <div id="predictions-container" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Dynamic Predictions Rendered Here -->
            </div>

        </div>

    </main>

    <!-- Footer -->
    <footer class="mt-auto border-t border-slate-800 py-6 bg-slate-900/50 text-center text-xs text-slate-500">
        <p>&copy; 2026 Bergamo Tip. All rights reserved. VIP Contact: <a href="https://t.me/Bergam777" target="_blank" class="text-emerald-400 font-bold hover:underline">@Bergam777</a></p>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        const SUPABASE_URL = "https://xlolsojhjxpiemaruwtd.supabase.co";
        const SUPABASE_ANON_KEY = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Inhsb2xzb2poanhwaWVtYXJ1d3RkIiwicm9sZSI6ImFub24iLCJpYXQiOjE3ODU3ODE4NDMsImV4cCI6MjEwMTM1Nzg0M30.goUjQj03XvND11T2QLL8wDGiATpSe_mYctEfsBLmauI";
        
        const { createClient } = supabase;
        const supabaseClient = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

        let currentTab = 'free';
        let currentGameFilter = 'ALL';
        let allPredictions = [];
        let isVipUser = false;

        document.addEventListener('DOMContentLoaded', async () => {
            lucide.createIcons();
            await fetchPredictions();
        });

        async function fetchPredictions() {
            const { data, error } = await supabaseClient.from('predictions').select('*').order('match_time', { ascending: false });
            if (error) {
                console.error("Error fetching predictions:", error);
                return;
            }
            allPredictions = data || [];
            renderPredictions();
        }

        function switchTab(tabName) {
            currentTab = tabName;
            document.querySelectorAll('.tab-btn').forEach(btn => {
                if (btn.dataset.tab === tabName) {
                    btn.className = "tab-btn px-5 py-2.5 rounded-xl text-sm font-bold transition flex items-center gap-2 bg-emerald-500 text-slate-950 shadow-md shadow-emerald-500/20";
                } else {
                    btn.className = "tab-btn px-5 py-2.5 rounded-xl text-sm font-bold transition flex items-center gap-2 bg-slate-900 text-slate-400 hover:bg-slate-800 border border-slate-800";
                }
            });
            renderPredictions();
        }

        function filterGameType(type) {
            currentGameFilter = type;
            ['all', 'football', 'fifa'].forEach(t => {
                const el = document.getElementById(`filter-${t}`);
                if (el) {
                    if (t === type.toLowerCase() || (type === 'ALL' && t === 'all')) {
                        el.className = "px-3 py-1 text-xs font-bold rounded-lg bg-emerald-500 text-slate-950 transition";
                    } else {
                        el.className = "px-3 py-1 text-xs font-bold rounded-lg text-slate-400 hover:text-white transition";
                    }
                }
            });
            renderPredictions();
        }

        function renderPredictions() {
            const container = document.getElementById('predictions-container');
            container.innerHTML = '';

            let filtered = allPredictions.filter(p => {
                if (currentGameFilter !== 'ALL' && p.game_type !== currentGameFilter) return false;
                
                let catLower = (p.category || '').toLowerCase();
                let isVipItem = catLower.includes('vip') || catLower.includes('combo');

                if (currentTab === 'free') return !isVipItem && p.status === 'Pending';
                if (currentTab === 'vip') return isVipItem && p.status === 'Pending';
                if (currentTab === 'history') return p.status !== 'Pending';
                return true;
            });

            if (filtered.length === 0) {
                container.innerHTML = `
                    <div class="col-span-full py-16 text-center bg-slate-900/50 rounded-2xl border border-slate-800/80">
                        <i data-lucide="folder-open" class="w-12 h-12 mx-auto text-slate-600 mb-3"></i>
                        <h3 class="text-lg font-bold text-slate-300">No predictions found in this category</h3>
                        <p class="text-xs text-slate-500 mt-1">Check back later or contact @Bergam777</p>
                    </div>
                `;
                lucide.createIcons();
                return;
            }

            filtered.forEach(item => {
                const card = document.createElement('div');
                card.className = "bg-slate-900 rounded-2xl border border-slate-800 p-5 flex flex-col justify-between shadow-xl relative overflow-hidden group hover:border-emerald-500/50 transition";
                
                let catLower = (item.category || '').toLowerCase();
                let isVipCat = catLower.includes('vip') || catLower.includes('combo');
                let badgeColor = isVipCat ? 'bg-amber-500/10 text-amber-400 border-amber-500/20' : 'bg-emerald-500/10 text-emerald-400 border-emerald-500/20';
                
                let statusBadge = '';
                if (item.status === 'Win') statusBadge = '<span class="px-2 py-0.5 text-xs font-bold bg-emerald-500/20 text-emerald-300 rounded">WIN</span>';
                else if (item.status === 'Loss') statusBadge = '<span class="px-2 py-0.5 text-xs font-bold bg-red-500/20 text-red-300 rounded">LOSS</span>';
                else statusBadge = '<span class="px-2 py-0.5 text-xs font-bold bg-amber-500/20 text-amber-300 rounded">PENDING</span>';

                // ለ VIP ካርዶች ኦድ ብቻ እና የኮንታክት አዝራር ማሳየት
                if (isVipCat && currentTab === 'vip') {
                    card.innerHTML = `
                        <div>
                            <div class="flex items-center justify-between mb-3">
                                <span class="px-2.5 py-1 text-xs font-extrabold rounded-lg border ${badgeColor}">[${item.game_type}] • ${item.category}</span>
                                <span class="px-2 py-0.5 text-xs font-bold bg-amber-500/20 text-amber-300 rounded">PENDING</span>
                            </div>
                            <div class="bg-slate-950 p-4 rounded-xl border border-slate-800/80 mb-4 text-center">
                                <span class="text-xs text-slate-400 block font-medium">VIP Locked Match</span>
                                <span class="text-xl font-black text-amber-400 tracking-wider">ODD: @${item.odds}</span>
                            </div>
                        </div>

                        <div>
                            <a href="https://t.me/Bergam777" target="_blank" class="w-full py-2.5 bg-gradient-to-r from-amber-500 to-yellow-500 hover:from-amber-400 hover:to-yellow-400 text-slate-950 font-bold rounded-xl text-xs flex items-center justify-center gap-2 shadow-lg shadow-amber-500/20 transition">
                                <i data-lucide="send" class="w-4 h-4"></i> Contact @Bergam777 for VIP
                            </a>
                        </div>
                    `;
                } else {
                    card.innerHTML = `
                        <div>
                            <div class="flex items-center justify-between mb-3">
                                <span class="px-2.5 py-1 text-xs font-extrabold rounded-lg border ${badgeColor}">[${item.game_type}] • ${item.category}</span>
                                <div class="flex items-center gap-2">
                                    <span class="text-xs text-slate-400 font-medium">${new Date(item.match_time).toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'})}</span>
                                    ${statusBadge}
                                </div>
                            </div>
                            <p class="text-xs text-emerald-400 font-semibold mb-2">${item.league}</p>
                            <div class="bg-slate-950 p-3 rounded-xl border border-slate-800/80 mb-4 flex items-center justify-between">
                                <span class="font-bold text-sm text-slate-100">${item.home_team}</span>
                                <span class="text-xs text-slate-500 font-bold px-2">VS</span>
                                <span class="font-bold text-sm text-slate-100">${item.away_team}</span>
                            </div>
                        </div>

                        <div class="bg-slate-950/60 p-3 rounded-xl border border-slate-800 flex items-center justify-between">
                            <div>
                                <span class="text-xs text-slate-400 block font-medium">Prediction Tip</span>
                                <span class="text-sm font-extrabold text-white">${item.prediction}</span>
                            </div>
                            <div class="text-right">
                                <span class="text-xs text-slate-400 block font-medium">Odds</span>
                                <span class="text-base font-extrabold text-emerald-400">@${item.odds}</span>
                            </div>
                        </div>
                    `;
                }
                container.appendChild(card);
            });
            lucide.createIcons();
        }
    </script>
</body>
</html>
