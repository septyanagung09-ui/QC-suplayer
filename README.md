# QC-suplayer<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Factory Tracker - Sunchang, DWSM, Raisa | Good & NG (Bundle & Pcs)</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: system-ui, 'Segoe UI', 'Inter', 'Roboto', sans-serif;
        }

        body {
            background: #e9f0f5;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        /* Container utama */
        .dashboard {
            max-width: 1400px;
            width: 100%;
            background: white;
            border-radius: 2rem;
            box-shadow: 0 20px 35px -12px rgba(0,0,0,0.2);
            overflow: hidden;
            padding: 1.8rem 2rem 2rem 2rem;
            transition: all 0.2s;
        }

        h1 {
            font-size: 1.8rem;
            font-weight: 700;
            margin: 0 0 0.25rem 0;
            color: #1a3e50;
            display: flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
            justify-content: space-between;
        }

        h1 small {
            font-size: 0.85rem;
            font-weight: normal;
            background: #eef2ff;
            padding: 6px 14px;
            border-radius: 40px;
            color: #1f5e7e;
        }

        .sub {
            color: #4a6272;
            border-left: 4px solid #ffb74d;
            padding-left: 12px;
            margin: 8px 0 24px 0;
            font-weight: 500;
        }

        /* grid produk 3 kolom */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(330px, 1fr));
            gap: 1.8rem;
            margin-bottom: 2rem;
        }

        /* kartu produk */
        .product-card {
            background: #ffffff;
            border-radius: 1.5rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.05);
            border: 1px solid #e2edf2;
            overflow: hidden;
            transition: transform 0.1s ease;
        }

        .card-header {
            background: linear-gradient(105deg, #f8fafc 0%, #ffffff 100%);
            padding: 1rem 1.5rem;
            border-bottom: 2px solid #e0edf3;
        }

        .product-title {
            font-size: 1.7rem;
            font-weight: 800;
            letter-spacing: -0.3px;
            margin: 0;
            display: flex;
            align-items: baseline;
            justify-content: space-between;
        }

        .product-title span:first-child {
            background: linear-gradient(135deg, #1f5e7e, #2c8eb3);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .badge-pcs {
            font-size: 0.7rem;
            background: #eef2fa;
            padding: 4px 12px;
            border-radius: 30px;
            font-weight: 500;
            color: #2c5a6e;
        }

        /* area hitungan utama */
        .counter-area {
            padding: 1.2rem 1.5rem 1.5rem;
        }

        .stats-row {
            display: flex;
            justify-content: space-between;
            background: #f8fafc;
            border-radius: 1.2rem;
            padding: 0.8rem 1rem;
            margin-bottom: 1.2rem;
            gap: 12px;
            flex-wrap: wrap;
        }

        .stat-good, .stat-ng {
            flex: 1;
            text-align: center;
            background: white;
            border-radius: 1rem;
            padding: 10px 6px;
            box-shadow: 0 1px 2px rgba(0,0,0,0.03);
        }

        .stat-good .label {
            color: #2b7e3a;
            font-weight: 600;
            font-size: 0.75rem;
            text-transform: uppercase;
        }

        .stat-ng .label {
            color: #c23d22;
            font-weight: 600;
            font-size: 0.75rem;
            text-transform: uppercase;
        }

        .stat-value {
            font-size: 2.2rem;
            font-weight: 800;
            line-height: 1;
            margin: 6px 0 4px;
        }

        .bundle-info {
            font-size: 0.7rem;
            background: #eef2ff;
            display: inline-block;
            padding: 2px 10px;
            border-radius: 20px;
            color: #1e4663;
        }

        /* tombol + / - */
        .btn-group {
            display: flex;
            gap: 12px;
            margin: 12px 0 16px;
            justify-content: center;
        }

        button {
            border: none;
            font-weight: 600;
            border-radius: 60px;
            cursor: pointer;
            transition: all 0.15s;
            font-size: 0.9rem;
            padding: 8px 18px;
            background: #f1f5f9;
            box-shadow: 0 1px 2px rgba(0,0,0,0.05);
        }

        .btn-good {
            background: #e0f2e4;
            color: #1f6e2f;
            border: 1px solid #bdddc5;
        }

        .btn-good:active {
            background: #c0e0c8;
            transform: scale(0.96);
        }

        .btn-ng {
            background: #ffe6e0;
            color: #bc4e2c;
            border: 1px solid #fad1c4;
        }

        .btn-ng:active {
            background: #fcd5c9;
            transform: scale(0.96);
        }

        .btn-reset {
            background: #eef2fa;
            color: #4f6f8a;
            font-size: 0.7rem;
            padding: 5px 12px;
            border-radius: 30px;
            margin-top: 8px;
        }

        .btn-reset:active {
            background: #e0e6f0;
        }

        /* area bundle & pcs terperinci */
        .breakdown {
            background: #fefcf5;
            border-radius: 1rem;
            padding: 12px 16px;
            margin-top: 12px;
            border: 1px solid #f0e9da;
        }

        .breakdown p {
            margin: 6px 0;
            font-size: 0.85rem;
            display: flex;
            justify-content: space-between;
            font-weight: 500;
        }

        .breakdown span {
            font-family: monospace;
            font-weight: 700;
            background: white;
            padding: 2px 10px;
            border-radius: 40px;
        }

        hr {
            margin: 14px 0;
            border-color: #e9edf2;
        }

        /* Total ringkasan semua produk */
        .summary-global {
            background: #1e2f3a;
            color: white;
            border-radius: 1.5rem;
            padding: 1.2rem 1.8rem;
            margin-top: 1rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
        }

        .summary-total {
            display: flex;
            gap: 28px;
            flex-wrap: wrap;
        }

        .summary-item {
            background: #2c4453;
            border-radius: 2rem;
            padding: 6px 18px;
            text-align: center;
        }

        .summary-item .label {
            font-size: 0.7rem;
            opacity: 0.8;
        }

        .summary-item .value {
            font-size: 1.5rem;
            font-weight: 800;
            line-height: 1.2;
        }

        .btn-reset-all {
            background: #f3b33d;
            color: #1e2f2f;
            padding: 10px 18px;
            font-weight: bold;
            border-radius: 40px;
            border: none;
            cursor: pointer;
            transition: 0.1s;
        }

        .btn-reset-all:active {
            background: #e09d28;
            transform: scale(0.97);
        }

        footer {
            text-align: center;
            font-size: 0.7rem;
            color: #7c93a3;
            margin-top: 2rem;
            border-top: 1px solid #e2edf2;
            padding-top: 1.2rem;
        }

        @media (max-width: 700px) {
            .dashboard {
                padding: 1.2rem;
            }
            .stat-value {
                font-size: 1.6rem;
            }
            .product-title {
                font-size: 1.4rem;
            }
            .btn-group button {
                padding: 6px 14px;
            }
        }
    </style>
</head>
<body>
<div class="dashboard">
    <h1>
        📦 PRODUCTION TRACKER
        <small>Good & NG · Bundle + Pcs</small>
    </h1>
    <div class="sub">⚙️ Satuan per PCS | 1 Bundle = 20 PCS (sesuai standar pabrik)</div>

    <div class="products-grid" id="productsGrid"></div>

    <!-- Ringkasan global -->
    <div class="summary-global" id="summaryGlobal">
        <!-- diisi javascript -->
    </div>
    <footer>
        🔄 Hitungan per PCS | Good (Produk Baik) & NG (Reject) | Otomatis konversi ke Bundle + Sisa PCS <br>
        Klik tombol + Good / + NG untuk menambah produksi per pcs. Tekan tombol reset masing-masing produk untuk mengatur ulang.
    </footer>
</div>

<script>
    // Definisi produk: Sunchang, DWSM, Raisa
    const PRODUCTS = [
        { id: 'sunchang', name: 'SUNCHANG', baseColor: '#e9f3f7' },
        { id: 'dwsm', name: 'DWSM', baseColor: '#f3f1eb' },
        { id: 'raisa', name: 'RAISA', baseColor: '#fef0e7' }
    ];

    // Konstanta bundle size
    const BUNDLE_SIZE = 20;  // 1 bundle = 20 pcs

    // Data state : { goodPcs, ngPcs }
    let productionData = {
        sunchang: { goodPcs: 0, ngPcs: 0 },
        dwsm: { goodPcs: 0, ngPcs: 0 },
        raisa: { goodPcs: 0, ngPcs: 0 }
    };

    // Fungsi helper untuk konversi dari pcs ke bundle + sisa pcs
    function convertPcsToBundleAndPcs(totalPcs) {
        const bundle = Math.floor(totalPcs / BUNDLE_SIZE);
        const remainingPcs = totalPcs % BUNDLE_SIZE;
        return { bundle, remainingPcs };
    }

    // Mendapatkan total produksi (good+ng) per produk
    function getTotalPcs(productId) {
        const prod = productionData[productId];
        return prod.goodPcs + prod.ngPcs;
    }

    // Render semua UI: produk grid + summary global
    function renderAll() {
        renderProductCards();
        renderGlobalSummary();
    }

    // Render masing-masing kartu produk
    function renderProductCards() {
        const container = document.getElementById('productsGrid');
        if (!container) return;

        container.innerHTML = PRODUCTS.map(prod => {
            const data = productionData[prod.id];
            const goodPcs = data.goodPcs;
            const ngPcs = data.ngPcs;
            const totalPcs = goodPcs + ngPcs;
            
            const goodBundleObj = convertPcsToBundleAndPcs(goodPcs);
            const ngBundleObj = convertPcsToBundleAndPcs(ngPcs);
            const totalBundleObj = convertPcsToBundleAndPcs(totalPcs);
            
            // persentase good
            const goodPercent = totalPcs === 0 ? 0 : ((goodPcs / totalPcs) * 100).toFixed(1);
            
            return `
                <div class="product-card" data-product="${prod.id}">
                    <div class="card-header">
                        <div class="product-title">
                            <span>${prod.name}</span>
                            <span class="badge-pcs">per PCS</span>
                        </div>
                        <div style="font-size:0.7rem; color:#497e9a;">1 bundle = 20 pcs</div>
                    </div>
                    <div class="counter-area">
                        <div class="stats-row">
                            <div class="stat-good">
                                <div class="label">✅ GOOD (PCS)</div>
                                <div class="stat-value">${goodPcs.toLocaleString()}</div>
                                <div class="bundle-info">📦 ${goodBundleObj.bundle} bundle  +  ${goodBundleObj.remainingPcs} pcs</div>
                            </div>
                            <div class="stat-ng">
                                <div class="label">⚠️ NG (PCS)</div>
                                <div class="stat-value">${ngPcs.toLocaleString()}</div>
                                <div class="bundle-info">📦 ${ngBundleObj.bundle} bundle  +  ${ngBundleObj.remainingPcs} pcs</div>
                            </div>
                        </div>
                        
                        <div class="breakdown">
                            <p>📊 TOTAL Produksi <span>${totalPcs.toLocaleString()} pcs</span></p>
                            <p>📦 Total Bundle + Pcs <span>${totalBundleObj.bundle} bundle + ${totalBundleObj.remainingPcs} pcs</span></p>
                            <p>✨ Yield Good <span>${goodPercent}%</span></p>
                        </div>
                        
                        <div class="btn-group">
                            <button class="btn-good" data-action="incGood" data-product="${prod.id}">➕ +1 Good (PCS)</button>
                            <button class="btn-ng" data-action="incNg" data-product="${prod.id}">⚠️ +1 NG (PCS)</button>
                        </div>
                        <div style="display: flex; justify-content: flex-end;">
                            <button class="btn-reset" data-action="resetProduct" data-product="${prod.id}">🗑️ Reset semua (Good+NG)</button>
                        </div>
                    </div>
                </div>
            `;
        }).join('');

        // Pasang event listener untuk tombol dinamis (delegasi)
        attachProductEvents();
    }

    // event delegation untuk klik tombol-tombol di kartu produk
    function attachProductEvents() {
        const grid = document.getElementById('productsGrid');
        if (!grid) return;
        
        // Hapus listener lama jika ada, gunakan event delegation baru
        grid.removeEventListener('click', productClickHandler);
        grid.addEventListener('click', productClickHandler);
    }

    function productClickHandler(e) {
        const btn = e.target.closest('button');
        if (!btn) return;
        
        const action = btn.getAttribute('data-action');
        const productId = btn.getAttribute('data-product');
        if (!productId || !productionData.hasOwnProperty(productId)) return;
        
        if (action === 'incGood') {
            // tambah 1 good pcs
            productionData[productId].goodPcs += 1;
            renderAll();
        } 
        else if (action === 'incNg') {
            productionData[productId].ngPcs += 1;
            renderAll();
        }
        else if (action === 'resetProduct') {
            // reset good dan ng untuk produk tersebut
            productionData[productId].goodPcs = 0;
            productionData[productId].ngPcs = 0;
            renderAll();
        }
    }

    // Ringkasan global semua produk (total good, total ng, total seluruh pcs, total bundle, dll)
    function renderGlobalSummary() {
        const summaryDiv = document.getElementById('summaryGlobal');
        if (!summaryDiv) return;
        
        let totalGoodPcs = 0;
        let totalNgPcs = 0;
        
        for (let prodId in productionData) {
            totalGoodPcs += productionData[prodId].goodPcs;
            totalNgPcs += productionData[prodId].ngPcs;
        }
        
        const totalOverallPcs = totalGoodPcs + totalNgPcs;
        const overallBundleObj = convertPcsToBundleAndPcs(totalOverallPcs);
        const goodBundleObj = convertPcsToBundleAndPcs(totalGoodPcs);
        const ngBundleObj = convertPcsToBundleAndPcs(totalNgPcs);
        
        const globalYield = totalOverallPcs === 0 ? 0 : ((totalGoodPcs / totalOverallPcs) * 100).toFixed(1);
        
        // Data breakdown per produk untuk ringkasan cepat
        let perProductRows = '';
        for (let prodId of ['sunchang', 'dwsm', 'raisa']) {
            const prodName = prodId === 'sunchang' ? 'SUNCHANG' : (prodId === 'dwsm' ? 'DWSM' : 'RAISA');
            const good = productionData[prodId].goodPcs;
            const ng = productionData[prodId].ngPcs;
            const totalProd = good + ng;
            perProductRows += `
                <div style="display: flex; justify-content: space-between; font-size:0.75rem; background:#243b48; padding:6px 12px; border-radius: 30px;">
                    <span>${prodName}</span>
                    <span>👍 ${good.toLocaleString()}  |  ❌ ${ng.toLocaleString()}  |  📦 total: ${totalProd.toLocaleString()} pcs</span>
                </div>
            `;
        }
        
        summaryDiv.innerHTML = `
            <div style="display: flex; flex-direction: column; gap: 12px; width: 100%;">
                <div style="display: flex; justify-content: space-between; flex-wrap: wrap; align-items: center; gap: 12px;">
                    <div class="summary-total">
                        <div class="summary-item">
                            <div class="label">✅ TOTAL GOOD</div>
                            <div class="value">${totalGoodPcs.toLocaleString()} pcs</div>
                            <div style="font-size:0.65rem;">📦 ${goodBundleObj.bundle} bdl + ${goodBundleObj.remainingPcs} pcs</div>
                        </div>
                        <div class="summary-item">
                            <div class="label">⚠️ TOTAL NG</div>
                            <div class="value">${totalNgPcs.toLocaleString()} pcs</div>
                            <div style="font-size:0.65rem;">📦 ${ngBundleObj.bundle} bdl + ${ngBundleObj.remainingPcs} pcs</div>
                        </div>
                        <div class="summary-item">
                            <div class="label">📈 TOTAL PRODUKSI</div>
                            <div class="value">${totalOverallPcs.toLocaleString()} pcs</div>
                            <div style="font-size:0.65rem;">📦 ${overallBundleObj.bundle} bundle + ${overallBundleObj.remainingPcs} pcs</div>
                        </div>
                        <div class="summary-item">
                            <div class="label">🏆 YIELD GLOBAL</div>
                            <div class="value">${globalYield}%</div>
                        </div>
                    </div>
                    <button class="btn-reset-all" id="resetAllBtn">🔄 RESET SEMUA DATA</button>
                </div>
                <div style="display: flex; flex-wrap: wrap; gap: 8px; justify-content: space-between; background: #1a3442; padding: 10px 16px; border-radius: 1rem;">
                    <div style="font-weight: 600; font-size:0.7rem;">📋 RINCIAN PER PRODUK (Good / NG)</div>
                    <div style="display: flex; flex-direction: column; gap: 5px; width: 100%;">
                        ${perProductRows}
                    </div>
                </div>
            </div>
        `;
        
        // Pasang event reset global
        const resetAllBtn = document.getElementById('resetAllBtn');
        if (resetAllBtn) {
            // Hapus listener lama untuk menghindari duplikasi
            const newBtn = resetAllBtn.cloneNode(true);
            resetAllBtn.parentNode.replaceChild(newBtn, resetAllBtn);
            newBtn.addEventListener('click', () => {
                if (confirm('⚠️ Reset semua data produksi Sunchang, DWSM, dan Raisa? Semua hitungan Good & NG akan menjadi 0.')) {
                    productionData = {
                        sunchang: { goodPcs: 0, ngPcs: 0 },
                        dwsm: { goodPcs: 0, ngPcs: 0 },
                        raisa: { goodPcs: 0, ngPcs: 0 }
                    };
                    renderAll();
                }
            });
        }
    }
    
    // tambahan untuk tombol reset-all tanpa bentrok event: sudah diatas menggunakan cloning
    
    // inisialisasi awal (bisa ditambah contoh data demo ringan jika ingin menunjukkan konsep)
    // optional: memberikan contoh kecil agar tabel tidak kosong (tapi lebih baik nol)
    // Uncomment jika ingin demo awal, tapi jangan ganggu UX:
    // (biarkan user memulai dari nol)
    
    // Jika ingin demo 2 bundle Good untuk Sunchang sebagai ilustrasi (bisa diaktifkan/dinonaktifkan)
    // Saya akan set data awal 0 biar user menikmati interaksi murni, tapi bisa juga beri contoh agar menarik.
    // Biarkan data kosong, tapi tampilkan contoh singkat fitur.
    // Supaya pengguna langsung paham bundle: saya beri sedikit data dummy agar terlihat konversi langsung.
    // Tapi tidak memaksa, tapi lebih baik beri contoh ringan? Diperbolehkan untuk memudahkan preview.
    // Untuk memenuhi kebutuhan "menghitung good dan ng dengan hitungan bundle dan pcs", lebih baik ada contoh data awal agar terlihat konversi bundle. 
    // Karena klien lihat langsung konversi bundle 20 pcs. Saya set data awal misal Sunchang Good 23 pcs, NG 5 pcs => Good 1 bundle 3 pcs, NG 0 bundle 5 pcs
    // DWSM 40 pcs good, 2 ng => good 2 bundle 0 pcs, Raisa 17 good 3 ng => good 0 bundle 17pcs.
    // Tapi agar tidak mengganggu persepsi, kita tambahkan tombol "reset" mudah. Saya akan set data contoh awal (pre-filled) supaya fungsi bundle langsung terlihat.
    // Namun tetap user bisa reset.
    
    // Fungsi untuk set data awal demonstrasi (opsional tapi membantu memahami bundle)
    function setInitialDemoData() {
        // jika data masih kosong semua (0 total) maka isi demo ringan. Tapi tidak mengganggu user, mereka bisa reset.
        // cek jika total semua pcs masih 0
        const totalAll = productionData.sunchang.goodPcs + productionData.sunchang.ngPcs +
                         productionData.dwsm.goodPcs + productionData.dwsm.ngPcs +
                         productionData.raisa.goodPcs + productionData.raisa.ngPcs;
        if (totalAll === 0) {
            // beri contoh: Sunchang Good=23, NG=5 ; DWSM Good=40, NG=2 ; Raisa Good=17, NG=3
            productionData.sunchang = { goodPcs: 23, ngPcs: 5 };
            productionData.dwsm = { goodPcs: 40, ngPcs: 2 };
            productionData.raisa = { goodPcs: 17, ngPcs: 3 };
        }
        renderAll();
    }
    
    // panggil render awal, lalu set demo hanya jika memang user belum ada data (kosong) supaya bundle langsung terlihat
    // namun user bebas reset kapan saja.
    renderAll();
    // setelah render pertama, set demo jika semua masih 0 (dengan delay tipis agar tidak bentrok event)
    setTimeout(() => {
        const totalCheck = productionData.sunchang.goodPcs + productionData.sunchang.ngPcs +
                           productionData.dwsm.goodPcs + productionData.dwsm.ngPcs +
                           productionData.raisa.goodPcs + productionData.raisa.ngPcs;
        if (totalCheck === 0) {
            productionData.sunchang = { goodPcs: 23, ngPcs: 5 };
            productionData.dwsm = { goodPcs: 40, ngPcs: 2 };
            productionData.raisa = { goodPcs: 17, ngPcs: 3 };
            renderAll();
        }
    }, 10);
    
    // Final: menyediakan object global untuk debugging tidak diperlukan
</script>
</body>
</html>
