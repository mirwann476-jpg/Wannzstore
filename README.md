# Wannzstore
<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wannz Store - Top Up Diamond Cepat & Aman</title>
    
    <!-- Memuat Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Memuat Font Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* Menggunakan font Inter sebagai default */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0F172A; /* bg-slate-900 */
            color: #F1F5F9; /* text-slate-100 */
        }
        /* Style kustom untuk item yang dipilih */
        .selectable-item.selected {
            background-color: #3B82F6; /* bg-blue-600 */
            color: #FFFFFF;
            border-color: #60A5FA; /* border-blue-400 */
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.5); /* Efek fokus biru */
        }
        /* Style untuk pesan notifikasi */
        #message-box {
            display: none;
            padding: 1rem;
            border-radius: 0.5rem;
            margin-top: 1.5rem;
            font-weight: 500;
            white-space: pre-wrap; /* Penting untuk baris baru di notifikasi DANA */
        }
        #message-box.success {
            display: block;
            background-color: #10B981; /* bg-emerald-500 */
            color: #FFFFFF;
        }
        #message-box.error {
            display: block;
            background-color: #EF4444; /* bg-red-500 */
            color: #FFFFFF;
        }
        /* Style khusus untuk info DANA */
        #dana-info {
            display: none;
        }
        .dana-active #dana-info {
            display: block;
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header / Navigasi -->
    <header class="bg-slate-800/50 backdrop-blur-sm sticky top-0 z-50 shadow-lg">
        <nav class="container mx-auto px-4 sm:px-6 lg:px-8 flex justify-between items-center h-16">
            <div class="flex-shrink-0">
                <a href="#" class="text-2xl font-bold text-blue-400">
                    Wannz Store
                </a>
            </div>
            <div class="hidden sm:flex space-x-6">
                <a href="#" class="text-slate-200 hover:text-blue-400 transition-colors">Home</a>
                <a href="#harga" class="text-slate-200 hover:text-blue-400 transition-colors">Daftar Harga</a>
                <a href="#cara-beli" class="text-slate-200 hover:text-blue-400 transition-colors">Cara Beli</a>
            </div>
            <div class="sm:hidden">
                <!-- Tombol menu mobile (bisa ditambahkan fungsionalitasnya) -->
                <button class="text-slate-200 focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
                </button>
            </div>
        </nav>
    </header>

    <!-- Konten Utama -->
    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-12">
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            
            <!-- Kolom Kiri: Detail Game & Input ID -->
            <div class="lg:col-span-2 space-y-6">
                
                <!-- Detail Game (Menggunakan Logo MLBB Placeholder) -->
                <div class="bg-slate-800 rounded-lg shadow-xl p-6 flex items-center space-x-6">
                    <!-- Logo Mobile Legends (Placeholder) -->
                    <img src="https://placehold.co/100x100/1D4ED8/FDE047?text=MLBB" alt="Logo Mobile Legends" class="w-24 h-24 rounded-md object-cover border-2 border-yellow-400">
                    <div>
                        <h1 class="text-3xl font-bold text-white">Top Up Diamond Mobile Legends</h1>
                        <p class="text-slate-400 mt-1">Layanan instan, aman, dan terpercaya untuk para Legends.</p>
                        <span class="inline-block mt-3 px-3 py-1 bg-green-500/10 text-green-400 rounded-full text-sm font-medium">Buka 24 Jam</span>
                    </div>
                </div>

                <!-- Langkah 1: Masukkan ID Pengguna -->
                <div id="cara-beli" class="bg-slate-800 rounded-lg shadow-xl p-6">
                    <h2 class="text-xl font-semibold text-white mb-4 border-l-4 border-blue-400 pl-3">
                        <span class="bg-blue-600 text-white rounded-full w-6 h-6 inline-flex items-center justify-center mr-2">1</span>
                        Masukkan Data Akun Anda
                    </h2>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label for="user_id" class="block text-sm font-medium text-slate-300 mb-1">User ID</label>
                            <input type="text" id="user_id" name="user_id" class="w-full bg-slate-700 border border-slate-600 rounded-lg px-3 py-2 text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="12345678">
                        </div>
                        <div>
                            <label for="zone_id" class="block text-sm font-medium text-slate-300 mb-1">Zone ID</label>
                            <input type="text" id="zone_id" name="zone_id" class="w-full bg-slate-700 border border-slate-600 rounded-lg px-3 py-2 text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="(2109)">
                        </div>
                    </div>
                    <p class="text-xs text-slate-400 mt-3">
                        Untuk menemukan ID Anda, klik pada ikon profil Anda di dalam game. User ID dan Zone ID Anda akan terlihat di bawah nama profil Anda. Contoh: 12345678 (2109).
                    </p>
                </div>

                <!-- Langkah 2: Pilih Nominal -->
                <div id="harga" class="bg-slate-800 rounded-lg shadow-xl p-6">
                    <h2 class="text-xl font-semibold text-white mb-4 border-l-4 border-blue-400 pl-3">
                        <span class="bg-blue-600 text-white rounded-full w-6 h-6 inline-flex items-center justify-center mr-2">2</span>
                        Pilih Nominal Top Up
                    </h2>
                    <div id="diamond-list" class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4">
                        <!-- Item akan ditambahkan oleh JavaScript -->
                    </div>
                </div>

            </div>

            <!-- Kolom Kanan: Detail Pembayaran -->
            <div class="lg:col-span-1 space-y-6 lg:sticky lg:top-24">
                
                <!-- Langkah 3: Pilih Pembayaran -->
                <div class="bg-slate-800 rounded-lg shadow-xl p-6">
                    <h2 class="text-xl font-semibold text-white mb-4 border-l-4 border-blue-400 pl-3">
                        <span class="bg-blue-600 text-white rounded-full w-6 h-6 inline-flex items-center justify-center mr-2">3</span>
                        Pilih Metode Pembayaran
                    </h2>
                    <div id="payment-list" class="space-y-3">
                        <!-- Item akan ditambahkan oleh JavaScript -->
                    </div>
                    
                    <!-- Kotak Khusus Info DANA (Nomor disamarkan menjadi nama) -->
                    <div id="dana-info" class="mt-6 p-4 bg-blue-900/50 rounded-lg border border-blue-600 text-center">
                        <h3 class="text-base font-bold text-white mb-2">Transfer DANA Langsung</h3>
                        <p class="text-sm text-blue-200 mb-3">
                            Setelah klik 'Beli Sekarang', transfer sejumlah nominal ke akun DANA atas nama:
                        </p>
                        <div class="bg-slate-700 p-3 rounded-md border border-blue-500 inline-block">
                            <span id="dana-display-name" class="text-xl font-extrabold text-yellow-300 tracking-wider">
                                <!-- Nama akan diisi oleh JS -->
                            </span>
                        </div>
                        <p class="text-xs text-blue-300 mt-3">
                            **PENTING:** Nomor tujuan DANA (0851...) akan diberitahu di notifikasi setelah klik 'Beli Sekarang'.
                        </p>
                    </div>
                </div>

                <!-- Langkah 4: Beli -->
                <div class="bg-slate-800 rounded-lg shadow-xl p-6">
                    <h2 class="text-xl font-semibold text-white mb-4 border-l-4 border-blue-400 pl-3">
                        <span class="bg-blue-600 text-white rounded-full w-6 h-6 inline-flex items-center justify-center mr-2">4</span>
                        Konfirmasi Pembelian
                    </h2>
                    
                    <div class="space-y-2 text-sm text-slate-300 mb-4">
                        <div class="flex justify-between">
                            <span>Item:</span>
                            <span id="summary-item" class="font-medium text-white">-</span>
                        </div>
                        <div class="flex justify-between">
                            <span>Pembayaran:</span>
                            <span id="summary-payment" class="font-medium text-white">-</span>
                        </div>
                        <div class="flex justify-between text-lg font-bold text-blue-400 pt-2 border-t border-slate-700 mt-2">
                            <span>Total Bayar:</span>
                            <span id="summary-price">Rp 0</span>
                        </div>
                    </div>

                    <!-- ✨ Fitur Gemini API -->
                    <div id="gemini-feature" class="mt-4 hidden">
                        <button id="gemini-button" class="w-full bg-indigo-500 hover:bg-indigo-600 text-white font-medium py-2 px-4 rounded-lg text-sm transition-all flex items-center justify-center space-x-2 disabled:opacity-50">
                            <span id="gemini-button-text">✨ Dapatkan Ide Penggunaan Diamond</span>
                            <!-- Ikon Loading -->
                            <svg id="gemini-loader" class="animate-spin h-4 w-4 text-white hidden" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                                <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                                <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                            </svg>
                        </button>
                        <div id="gemini-result" class="mt-3 p-3 bg-slate-700 rounded-lg text-sm text-slate-200 hidden whitespace-pre-wrap"></div>
                    </div>
                    <!-- ✨ Akhir Fitur Gemini API -->

                    <div class="mt-4">
                        <label for="email" class="block text-sm font-medium text-slate-300 mb-1">Email (Untuk bukti pembayaran)</label>
                        <input type="email" id="email" name="email" class="w-full bg-slate-700 border border-slate-600 rounded-lg px-3 py-2 text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="email@anda.com">
                    </div>

                    <button id="buy-button" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 rounded-lg mt-6 text-lg transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-4 focus:ring-blue-500/50">
                        Beli Sekarang
                    </button>
                    
                    <!-- Kotak Pesan Notifikasi -->
                    <div id="message-box"></div>
                </div>

                <!-- Kartu Kontak Customer Service Baru -->
                <div class="bg-slate-800 rounded-lg shadow-xl p-6 text-center">
                    <h3 class="text-lg font-semibold text-white mb-3">Laporan Keluhan / Customer Service</h3>
                    <p class="text-slate-400 mb-4 text-sm">Butuh bantuan atau ada kendala transaksi? Hubungi CS kami:</p>
                    <a href="https://wa.me/6288212310510?text=Halo%20Wannz%20Store%2C%20saya%20ingin%20melaporkan%20kendala%20pesanan."
                       target="_blank" 
                       class="inline-flex items-center justify-center w-full bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-4 rounded-lg text-md transition-all duration-300 transform hover:scale-[1.02] focus:outline-none">
                       <svg class="w-5 h-5 mr-2" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M12.04 2c-5.45 0-9.91 4.46-9.91 9.91 0 1.63.4 3.2 1.15 4.6l-1.18 4.35 4.44-1.17c1.35.73 2.87 1.12 4.09 1.12h.01c5.45 0 9.91-4.46 9.91-9.91s-4.46-9.91-9.91-9.91zM8.33 7.37c-.12 0-.17.06-.24.16-.07.1-.15.24-.16.29-.02.05-.18.23-.21.27-.03.04-.07.1-.02.19.05.1.18.29.28.47.1.18.2.33.31.43.11.1.25.18.39.23.14.05.3.06.41.02.11-.04.34-.14.47-.29.13-.16.2-.28.26-.37.05-.1.11-.12.18-.08.08.04.55.27.67.33.12.06.2.09.23.14.03.05.03.3.01.44-.02.15-.09.31-.19.47-.1.16-.62.61-.72.69-.1.08-.22.18-.32.25-.1.07-.21.14-.4.29-.18.15-.37.28-.56.44-.19.16-.38.31-.57.44-.19.13-.39.26-.54.33-.15.07-.3.12-.45.15-.15.03-.27.03-.49-.06-.22-.1-.58-.22-.76-.3-.18-.08-.34-.14-.52-.2-.17-.06-.35-.07-.53-.07-.18 0-.35.05-.51.2-.16.15-.55.61-.55.61l-.01.01.03-.02s.03.04.04.05c0 .01-.01.03-.01.04.01.03.02.06.02.09l.04.14c.05.16.12.35.25.53.13.18.25.33.42.5.17.17.33.29.5.42.17.13.3.25.46.38.16.13.31.25.5.38.19.13.35.25.55.37.2.12.44.23.68.32.24.1.51.17.8.17.29 0 .56-.05.81-.13.25-.08.49-.2.69-.35.21-.15.39-.33.58-.51.18-.18.36-.39.53-.61.18-.21.34-.44.5-.68.15-.24.31-.5.44-.73.13-.23.23-.46.32-.7.09-.23.14-.46.16-.65.02-.19-.01-.36-.03-.53-.02-.17-.08-.34-.16-.51-.08-.18-.17-.33-.28-.47-.11-.14-.24-.26-.41-.35-.16-.09-.38-.13-.56-.06z"></path></svg>
                       CS: 0882-1231-0510 (WhatsApp)
                    </a>
                </div>

            </div>

        </div>

    </main>

    <!-- Footer -->
    <footer class="bg-slate-900 mt-16 border-t border-slate-700">
        <div class="container mx-auto px-6 py-8 text-center text-slate-400 text-sm">
            © 2025 Wannz Store. Didukung oleh teknologi canggih.
            <p class="mt-2 text-xs">Butuh bantuan? Hubungi <a href="https://wa.me/6288212310510?text=Halo%20Wannz%20Store%2C%20saya%20ingin%20melaporkan%20kendala%20pesanan." target="_blank" class="text-blue-400 hover:text-blue-300 font-medium">Customer Service kami</a>.</p>
            <p class="mt-1 text-xs">Semua merek dagang adalah milik dari pemiliknya masing-masing.</p>
        </div>
    </footer>

    <script>
        // Data produk (contoh)
        const diamondPackages = [
            { id: 'd22', name: '22 Diamonds', price: 6570, price_text: 'Rp 6.570' },
            { id: 'd28', name: '28 Diamonds', price: 8200, price_text: 'Rp 8.200' },
            { id: 'd30', name: '30 Diamonds', price: 8700, price_text: 'Rp 8.700' },
            { id: 'd36', name: '36 Diamonds', price: 10200, price_text: 'Rp 10.200' },
            { id: 'd42', name: '42 Diamonds', price: 12120, price_text: 'Rp 12.120' },
            { id: 'd45', name: '45 Diamonds', price: 13200, price_text: 'Rp 13.200' },
            { id: 'd46', name: '46 Diamonds', price: 13275, price_text: 'Rp 13.275' },
            { id: 'd54', name: '54 Diamonds', price: 15132, price_text: 'Rp 15.132' },
            { id: 'd60', name: '60 Diamonds', price: 17305, price_text: 'Rp 17.305' },
            { id: 'd64', name: '64 Diamonds', price: 17650, price_text: 'Rp 17.650' },
            { id: 'd67', name: '67 Diamonds', price: 18734, price_text: 'Rp 18.734' },
            { id: 'd71', name: '71 Diamonds', price: 19665, price_text: 'Rp 19.665' },
            { id: 'd74', name: '74 Diamonds', price: 20444, price_text: 'Rp 20.444' },
            { id: 'd75', name: '75 Diamonds', price: 21896, price_text: 'Rp 21.896' },
            { id: 'd80', name: '80 Diamonds', price: 22313, price_text: 'Rp 22.313' },
            { id: 'd85', name: '85 Diamonds', price: 23177, price_text: 'Rp 23.177' },
            { id: 'd88', name: '88 Diamonds', price: 24514, price_text: 'Rp 24.514' },
            { id: 'd89', name: '89 Diamonds', price: 24752, price_text: 'Rp 24.752' },
            { id: 'd113', name: '113 Diamonds', price: 31205, price_text: 'Rp 31.205' },
            { id: 'd116', name: '116 Diamonds', price: 32541, price_text: 'Rp 32.541' },
            { id: 'd129', name: '129 Diamonds', price: 35218, price_text: 'Rp 35.218' },
            { id: 'd148', name: '148 Diamonds', price: 40788, price_text: 'Rp 40.788' },
            { id: 'd170', name: '170 Diamonds', price: 46253, price_text: 'Rp 46.253' },
            { id: 'd176', name: '176 Diamonds', price: 48928, price_text: 'Rp 48.928' },
            { id: 'd184', name: '184 Diamonds', price: 52205, price_text: 'Rp 52.205' },
            { id: 'd222', name: '222 Diamonds', price: 61031, price_text: 'Rp 61.031' },
            { id: 'd240', name: '240 Diamonds', price: 65179, price_text: 'Rp 65.179' },
            { id: 'd277', name: '277 Diamonds', price: 76388, price_text: 'Rp 76.388' },
            { id: 'd284', name: '284 Diamonds', price: 77220, price_text: 'Rp 77.220' },
            { id: 'd296', name: '296 Diamonds', price: 80180, price_text: 'Rp 80.180' },
            { id: 'd305', name: '305 Diamonds', price: 84528, price_text: 'Rp 84.528' },
            { id: 'd370', name: '370 Diamonds', price: 101816, price_text: 'Rp 101.816' },
            { id: 'd384', name: '384 Diamonds', price: 105886, price_text: 'Rp 105.886' },
            { id: 'd408', name: '408 Diamonds', price: 110233, price_text: 'Rp 110.233' },
            { id: 'd518', name: '518 Diamonds', price: 142504, price_text: 'Rp 142.504' },
            { id: 'd568', name: '568 Diamonds', price: 150215, price_text: 'Rp 150.215' },
            { id: 'd716', name: '716 Diamonds', price: 191002, price_text: 'Rp 191.002' },
            { id: 'd750', name: '750 Diamonds', price: 199978, price_text: 'Rp 199.978' },
            { id: 'd790', name: '790 Diamonds', price: 211345, price_text: 'Rp 211.345' },
            { id: 'd875', name: '875 Diamonds', price: 230351, price_text: 'Rp 230.351' },
            { id: 'd966', name: '966 Diamonds', price: 254389, price_text: 'Rp 254.389' },
            { id: 'd1048', name: '1048 Diamonds', price: 282547, price_text: 'Rp 282.547' },
            { id: 'd1067', name: '1067 Diamonds', price: 287532, price_text: 'Rp 287.532' },
            { id: 'd1136', name: '1136 Diamonds', price: 300529, price_text: 'Rp 300.529' },
            { id: 'd1358', name: '1358 Diamonds', price: 361559, price_text: 'Rp 361.559' },
            { id: 'd1506', name: '1506 Diamonds', price: 402244, price_text: 'Rp 402.244' }
        ];

        // Data metode pembayaran (sudah diperbarui)
        const paymentMethods = [
            { id: 'dana', name: 'DANA Transfer (a/n Wannz Store)' }, // Disamarkan menjadi nama
            { id: 'qris', name: 'QRIS (Semua E-Wallet)' },
            { id: 'gopay', name: 'GoPay' },
        ];

        // Variabel untuk menyimpan pilihan
        let selectedDiamond = null;
        let selectedPayment = paymentMethods[0]; // DANA dipilih secara default
        const DANA_NUMBER = '085147283512'; // Nomor tujuan DANA (tetap di JS untuk notifikasi)
        const DANA_ACCOUNT_NAME = 'Wannz Store'; // Nama pengganti nomor

        // Referensi Elemen DOM
        const diamondListEl = document.getElementById('diamond-list');
        const paymentListEl = document.getElementById('payment-list');
        const summaryItemEl = document.getElementById('summary-item');
        const summaryPaymentEl = document.getElementById('summary-payment');
        const summaryPriceEl = document.getElementById('summary-price');
        const buyButtonEl = document.getElementById('buy-button');
        const messageBoxEl = document.getElementById('message-box');
        const paymentContainerEl = document.querySelector('.lg\\:col-span-1.space-y-6.lg\\:sticky.lg\\:top-24 > div:nth-child(1)'); // Container Langkah 3
        const danaInfoEl = document.getElementById('dana-info'); // Kotak info DANA

        // Referensi Fitur Gemini
        const geminiFeatureEl = document.getElementById('gemini-feature');
        const geminiButtonEl = document.getElementById('gemini-button');
        const geminiButtonTextEl = document.getElementById('gemini-button-text');
        const geminiLoaderEl = document.getElementById('gemini-loader');
        const geminiResultEl = document.getElementById('gemini-result');
        const danaDisplayNameEl = document.getElementById('dana-display-name');

        // Fungsi untuk format mata uang
        function formatCurrency(number) {
            return new Intl.NumberFormat('id-ID', { style: 'currency', currency: 'IDR', minimumFractionDigits: 0 }).format(number);
        }

        // Fungsi untuk membuat item yang bisa dipilih
        function createSelectableItem(item, type) {
            const div = document.createElement('div');
            const isSelected = type === 'payment' && item.id === selectedPayment.id;
            
            const diamondClass = type === 'diamond' ? 'text-xs sm:text-sm' : ''; 

            div.className = `selectable-item bg-slate-700 p-4 rounded-lg cursor-pointer border-2 border-slate-600 hover:border-blue-500 transition-all ${diamondClass} ${isSelected ? 'selected' : ''}`;
            div.dataset.id = item.id;
            
            if (type === 'diamond') {
                div.innerHTML = `
                    <div class="font-bold text-white">${item.name}</div>
                    <div class="text-sm text-blue-300 mt-1">${item.price_text}</div>
                `;
                div.addEventListener('click', () => selectDiamond(div, item));
            } else if (type === 'payment') {
                div.innerHTML = `<div class="font-medium text-white">${item.name}</div>`;
                div.addEventListener('click', () => selectPayment(div, item));
            }
            return div;
        }

        // Fungsi untuk memilih diamond
        function selectDiamond(element, item) {
            // Hapus 'selected' dari semua item diamond
            diamondListEl.querySelectorAll('.selectable-item').forEach(el => el.classList.remove('selected'));
            // Tambah 'selected' ke item yang diklik
            element.classList.add('selected');
            // Simpan pilihan
            selectedDiamond = item;
            updateSummary();

            // Tampilkan fitur Gemini
            geminiFeatureEl.classList.remove('hidden');
            geminiResultEl.classList.add('hidden'); // Sembunyikan hasil lama
            geminiResultEl.textContent = '';
            geminiButtonTextEl.textContent = `✨ Dapatkan Ide Penggunaan ${item.name}`;
            setGeminiLoading(false); // Pastikan tombol tidak dalam keadaan loading saat paket diubah
        }

        // Fungsi untuk memilih pembayaran
        function selectPayment(element, item) {
            // Hapus 'selected' dari semua item pembayaran
            paymentListEl.querySelectorAll('.selectable-item').forEach(el => el.classList.remove('selected'));
            // Tambah 'selected' ke item yang diklik
            element.classList.add('selected');
            // Simpan pilihan
            selectedPayment = item;
            updateSummary();
            
            // Tampilkan/sembunyikan info DANA
            if (item.id === 'dana') {
                paymentContainerEl.classList.add('dana-active');
            } else {
                paymentContainerEl.classList.remove('dana-active');
            }
        }

        // Fungsi untuk update ringkasan pesanan
        function updateSummary() {
            if (selectedDiamond) {
                summaryItemEl.textContent = selectedDiamond.name;
                summaryPriceEl.textContent = formatCurrency(selectedDiamond.price);
            } else {
                summaryItemEl.textContent = '-';
                summaryPriceEl.textContent = 'Rp 0';
            }

            if (selectedPayment) {
                summaryPaymentEl.textContent = selectedPayment.name;
            } else {
                summaryPaymentEl.textContent = '-';
            }
            
            // Update nama DANA di kotak info khusus (Langkah 3)
            if (selectedPayment && selectedPayment.id === 'dana') {
                 danaDisplayNameEl.textContent = DANA_ACCOUNT_NAME;
            }
        }

        // Fungsi untuk menampilkan pesan
        function showMessage(message, type = 'error') {
            messageBoxEl.textContent = message;
            messageBoxEl.className = type === 'success' ? 'success' : 'error'; 
            // Sembunyikan pesan setelah 8 detik
            setTimeout(() => {
                messageBoxEl.className = '';
                messageBoxEl.style.display = 'none';
            }, 8000);
        }

        // Fungsi Gemini API (tidak ada perubahan)
        function setGeminiLoading(isLoading) {
            if (isLoading) {
                geminiButtonEl.disabled = true;
                geminiButtonTextEl.classList.add('hidden');
                geminiLoaderEl.classList.remove('hidden');
            } else {
                geminiButtonEl.disabled = false;
                geminiButtonTextEl.classList.remove('hidden');
                if (selectedDiamond) {
                    geminiButtonTextEl.textContent = `✨ Dapatkan Ide Penggunaan ${selectedDiamond.name}`;
                }
                geminiLoaderEl.classList.add('hidden');
            }
        }

        async function getGeminiIdeas() {
            if (!selectedDiamond) {
                showMessage('Pilih paket diamond terlebih dahulu.', 'error');
                return;
            }

            setGeminiLoading(true);
            geminiResultEl.classList.add('hidden');
            geminiResultEl.textContent = '';
            
            geminiButtonTextEl.textContent = `Memuat ide...`;

            const apiKey = ""; 
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
            
            const systemPrompt = "Anda adalah asisten gaming yang kreatif dan antusias di 'Wannz Store'. Berikan ide penggunaan diamond khusus untuk game Mobile Legends: Bang Bang (MLBB).";
            const userQuery = `Saya ingin membeli "${selectedDiamond.name}" MLBB. Berikan saya 3 ide singkat, seru, dan unik (masing-masing 1-2 kalimat) tentang cara menggunakan diamond ini di MLBB. Gunakan bahasa yang santai dan menarik. Mulailah dengan judul seperti '--- Ide Seru untuk ${selectedDiamond.name} MLBB ---'.`;

            const payload = {
                contents: [{ parts: [{ text: userQuery }] }],
                systemInstruction: {
                    parts: [{ text: systemPrompt }]
                },
            };

            let retries = 3;
            let delay = 1000; 
            let response = null;

            for (let i = 0; i < retries; i++) {
                try {
                    response = await fetch(apiUrl, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(payload)
                    });

                    if (!response.ok) {
                        throw new Error(`HTTP error! status: ${response.status}`);
                    }

                    const result = await response.json();
                    const candidate = result.candidates?.[0];

                    if (candidate && candidate.content?.parts?.[0]?.text) {
                        const text = candidate.content.parts[0].text;
                        geminiResultEl.textContent = text;
                        geminiResultEl.classList.remove('hidden');
                    } else {
                        throw new Error('Respons API tidak valid atau tidak ada konten.');
                    }
                    
                    setGeminiLoading(false);
                    return; 

                } catch (error) {
                    console.error(`Attempt ${i + 1} failed:`, error);
                    if (i < retries - 1) {
                        await new Promise(resolve => setTimeout(resolve, delay));
                        delay *= 2; 
                    } else {
                        geminiResultEl.textContent = 'Maaf, terjadi kesalahan saat mengambil ide. Coba lagi nanti.';
                        geminiResultEl.classList.remove('hidden');
                        setGeminiLoading(false);
                    }
                }
            }
        }
        
        // Fungsi Inisialisasi
        function init() {
            // Tampilkan daftar diamond
            diamondPackages.forEach(pkg => {
                diamondListEl.appendChild(createSelectableItem(pkg, 'diamond'));
            });

            // Tampilkan daftar pembayaran
            paymentMethods.forEach(method => {
                paymentListEl.appendChild(createSelectableItem(method, 'payment'));
            });

            // Set state awal untuk DANA info
            if (selectedPayment.id === 'dana') {
                 paymentContainerEl.classList.add('dana-active');
            }
            updateSummary();

            // Tambahkan event listener ke tombol Gemini
            geminiButtonEl.addEventListener('click', getGeminiIdeas);

            // Tambahkan event listener ke tombol Beli
            buyButtonEl.addEventListener('click', () => {
                const userId = document.getElementById('user_id').value;
                const zoneId = document.getElementById('zone_id').value;
                const email = document.getElementById('email').value;

                // Validasi sederhana
                if (!userId || !zoneId) {
                    showMessage('Harap masukkan User ID dan Zone ID Anda.', 'error');
                    return;
                }
                if (!selectedDiamond) {
                    showMessage('Harap pilih nominal top up.', 'error');
                    return;
                }
                if (!selectedPayment) {
                    showMessage('Harap pilih metode pembayaran.', 'error');
                    return;
                }
                if (!email) {
                    showMessage('Harap masukkan email Anda untuk bukti pembayaran.', 'error');
                    return;
                }

                // Logika Khusus DANA Transfer
                if (selectedPayment.id === 'dana') {
                    const priceFormatted = formatCurrency(selectedDiamond.price);
                    
                    // Pesan khusus untuk DANA - Sekarang mencantumkan nomor yang tadinya disembunyikan
                    const danaMessage = `✅ Pesanan ${selectedDiamond.name} berhasil dibuat!
                    
Silakan transfer **tepat sebesar ${priceFormatted}**
ke nomor DANA: **${DANA_NUMBER}**
atas nama **${DANA_ACCOUNT_NAME}**.
                    
Diamond akan dikirimkan otomatis setelah transfer dikonfirmasi. Bukti pembayaran akan dikirimkan ke email: ${email}.
                    
Harap segera lakukan transfer!`;

                    // Tampilkan pesan sukses DANA
                    showMessage(danaMessage, 'success');

                } else {
                    // Pesan untuk metode non-DANA
                    showMessage(`Pesanan ${selectedDiamond.name} berhasil! Cek email ${email} untuk instruksi pembayaran via ${selectedPayment.name}.`, 'success');
                }
                
            });
        }

        // Jalankan inisialisasi saat dokumen siap
        document.addEventListener('DOMContentLoaded', init);

    </script>
</body>
</html>
