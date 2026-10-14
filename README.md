
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LKPD Interaktif - Belajar Variable JavaScript (D - Z)</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .code-font { font-family: 'Fira Code', 'Courier New', Courier, monospace; }
        @media print {
            .no-print { display: none !important; }
            body { background-color: white !important; }
            .shadow-sm, .shadow-md, .shadow-lg { box-shadow: none !important; }
            .border { border-color: #cbd5e1 !important; }
        }
    </style>
</head>
<body class="bg-slate-100 text-slate-800 font-sans min-h-screen pb-12">

    <!-- Header -->
    <header class="bg-indigo-600 text-white py-6 px-4 shadow-lg sticky top-0 z-50 no-print">
        <div class="max-w-4xl mx-auto flex justify-between items-center">
            <div>
                <h1 class="text-2xl font-bold">LKPD Interaktif: Pemrograman JavaScript</h1>
                <p class="text-indigo-200 text-sm">Materi Lengkap: Mengenal Variable, Tipe Data, & Aturan Penamaan</p>
            </div>
            <button onclick="window.print()" class="bg-indigo-700 hover:bg-indigo-800 text-white px-4 py-2 rounded-lg text-sm font-semibold transition flex items-center gap-2">
                <i class="fas fa-print"></i> Cetak / Simpan PDF
            </button>
        </div>
    </header>

    <div class="max-w-4xl mx-auto px-4 mt-8 space-y-8">

        <!-- D. APERSEPSI -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">D. APERSEPSI</h2>
            <p class="mb-3 text-slate-700">Bayangkan kamu sedang membuat aplikasi data siswa.</p>
            <p class="mb-2 font-medium">Program perlu mengetahui:</p>
            <ul class="list-disc pl-6 mb-4 text-slate-600 text-sm space-y-1">
                <li>Nama siswa</li>
                <li>Kelas</li>
                <li>Umur</li>
                <li>Nilai</li>
                <li>Jurusan</li>
            </ul>
            
            <div class="bg-slate-50 border-l-4 border-indigo-500 p-4 rounded mb-4">
                <p class="font-semibold text-slate-700 mb-1">Contoh data:</p>
                <div class="code-font text-sm text-slate-800 space-y-1">
                    <p>Nama siswa = "Budi"</p>
                    <p>Kelas = "XI RPL 1"</p>
                    <p>Umur = 16</p>
                    <p>Nilai = 85</p>
                </div>
            </div>

            <label class="block font-semibold mb-2 text-slate-800">Menurutmu, bagaimana cara menyimpan informasi tersebut di dalam program? Tuliskan dugaanmu:</label>
            <textarea class="w-full p-3 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" rows="3">Informasi tersebut disimpan di dalam variabel (tempat penyimpanan data sementara di memori komputer) dengan memberikan nama tempat (nama variabel) dan mengisi nilainya menggunakan tanda sama dengan (=).</textarea>
        </section>

        <!-- E. AKTIVITAS 1 - MENGAMATI -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">E. AKTIVITAS 1 – MENGAMATI</h2>
            <p class="mb-3 text-slate-700">Perhatikan kode berikut:</p>

            <div class="bg-slate-900 text-slate-100 p-4 rounded-lg code-font text-sm mb-4 leading-relaxed">
                <span class="text-purple-400">let</span> nama = <span class="text-emerald-400">"Budi"</span>;<br>
                <span class="text-purple-400">let</span> umur = <span class="text-amber-400">16</span>;<br>
                <span class="text-purple-400">let</span> nilai = <span class="text-amber-400">85</span>;<br><br>
                <span class="text-blue-400">console</span>.log(nama);<br>
                <span class="text-blue-400">console</span>.log(umur);<br>
                <span class="text-blue-400">console</span>.log(nilai);
            </div>
            <p class="text-sm text-slate-500 italic mb-6">Jalankan kode tersebut menggunakan browser.</p>

            <h3 class="font-bold text-lg mb-4 text-slate-800">Pertanyaan & Jawaban:</h3>
            <div class="space-y-4">
                <div>
                    <label class="block font-semibold mb-1 text-slate-700">1. Apa yang ditampilkan pada Console?</label>
                    <div class="bg-slate-900 text-green-400 p-3 rounded-lg code-font text-sm">
                        > Budi<br>
                        > 16<br>
                        > 85
                    </div>
                </div>

                <div>
                    <label class="block font-semibold mb-1 text-slate-700">2. Menurutmu, apa fungsi <code class="code-font text-indigo-600 bg-slate-100 px-1 rounded">nama</code>, <code class="code-font text-indigo-600 bg-slate-100 px-1 rounded">umur</code>, dan <code class="code-font text-indigo-600 bg-slate-100 px-1 rounded">nilai</code>?</label>
                    <textarea class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" rows="2">Fungsinya adalah sebagai nama variabel (label identifier) yang menampung dan merujuk nilai data yang disimpan.</textarea>
                </div>

                <div>
                    <label class="block font-semibold mb-1 text-slate-700">3. Apa yang terjadi jika kode berikut dijalankan?</label>
                    <div class="bg-slate-900 text-slate-100 p-2.5 rounded-lg code-font text-sm mb-2">
                        <span class="text-blue-400">console</span>.log(nama);
                    </div>
                    <textarea class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" rows="2">Browser akan mencetak isi dari variabel nama ke dalam konsol, yaitu teks "Budi".</textarea>
                </div>

                <div>
                    <label class="block font-semibold mb-1 text-slate-700">4. Menurut dugaanmu, apa yang dimaksud dengan variable?</label>
                    <textarea class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" rows="2">Variable adalah wadah/tempat di dalam memori komputer yang digunakan untuk menyimpan nilai data yang dapat dipanggil atau diubah kembali oleh program.</textarea>
                </div>
            </div>
        </section>

        <!-- F. AKTIVITAS 2 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">F. AKTIVITAS 2 – MENGENAL VARIABLE</h2>
            <h3 class="font-bold text-lg mb-2 text-slate-800">1. Apa itu Variable?</h3>
            <p class="mb-4 text-slate-600">Variable dapat dianggap sebagai <strong>tempat untuk menyimpan sebuah data</strong> agar data tersebut dapat digunakan kembali oleh program.</p>
            
            <p class="font-medium text-sm text-slate-500 mb-1">Contoh:</p>
            <div class="bg-slate-900 text-emerald-400 p-4 rounded-lg code-font text-sm mb-4">
                let nama = "Andi";
            </div>

            <p class="mb-2 font-semibold text-slate-700">Struktur Sintaks:</p>
            <div class="overflow-x-auto mb-4">
                <table class="w-full text-left border-collapse border border-slate-200">
                    <thead>
                        <tr class="bg-slate-50">
                            <th class="border border-slate-200 p-2.5 font-semibold">Bagian</th>
                            <th class="border border-slate-200 p-2.5 font-semibold">Fungsi</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-200">
                        <tr><td class="border border-slate-200 p-2.5 code-font text-indigo-600 font-bold">let</td><td class="border border-slate-200 p-2.5">Membuat variable</td></tr>
                        <tr><td class="border border-slate-200 p-2.5 code-font text-indigo-600 font-bold">nama</td><td class="border border-slate-200 p-2.5">Nama variable</td></tr>
                        <tr><td class="border border-slate-200 p-2.5 code-font text-indigo-600 font-bold">=</td><td class="border border-slate-200 p-2.5">Memberikan nilai (Assignment)</td></tr>
                        <tr><td class="border border-slate-200 p-2.5 code-font text-indigo-600 font-bold">"Andi"</td><td class="border border-slate-200 p-2.5">Nilai yang disimpan</td></tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- G. AKTIVITAS 3 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">G. AKTIVITAS 3 – PRAKTIK MEMBUAT VARIABLE</h2>
            <p class="mb-2 text-slate-700">Buat file: <code class="bg-slate-100 px-2 py-1 rounded code-font text-indigo-600 font-semibold">variable.html</code></p>
            <p class="mb-4 text-slate-700">Kemudian masukkan kode berikut:</p>

            <div class="bg-slate-900 text-slate-100 p-4 rounded-lg code-font text-sm mb-4 leading-relaxed">
                &lt;!DOCTYPE html&gt;<br>
                &lt;html&gt;<br>
                &lt;head&gt;<br>
                &nbsp;&nbsp;&lt;title&gt;Belajar Variable&lt;/title&gt;<br>
                &lt;/head&gt;<br>
                &lt;body&gt;<br>
                &nbsp;&nbsp;&lt;script&gt;<br>
                &nbsp;&nbsp;&nbsp;&nbsp;<span class="text-purple-400">let</span> nama = <span class="text-emerald-400">"Budi"</span>;<br>
                &nbsp;&nbsp;&nbsp;&nbsp;<span class="text-purple-400">let</span> kelas = <span class="text-emerald-400">"XI RPL 1"</span>;<br>
                &nbsp;&nbsp;&nbsp;&nbsp;<span class="text-purple-400">let</span> umur = <span class="text-amber-400">16</span>;<br><br>
                &nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-400">console</span>.log(nama);<br>
                &nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-400">console</span>.log(kelas);<br>
                &nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-400">console</span>.log(umur);<br>
                &nbsp;&nbsp;&lt;/script&gt;<br>
                &lt;/body&gt;<br>
                &lt;/html&gt;
            </div>

            <div class="bg-indigo-50 border border-indigo-200 rounded-lg p-4 mt-4">
                <h4 class="font-bold text-indigo-900 mb-2">Hasil Pengamatan (Console Browser):</h4>
                <div class="bg-slate-900 text-green-400 p-3 rounded font-mono text-sm space-y-1">
                    <p>> Budi</p>
                    <p>> XI RPL 1</p>
                    <p>> 16</p>
                </div>
            </div>
        </section>

        <!-- H. AKTIVITAS 4 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">H. AKTIVITAS 4 – EKSPERIMEN</h2>
            <p class="mb-4 text-slate-700">Sekarang ubahlah program sebelumnya dengan data kamu sendiri, lalu jawab pertanyaan berikut:</p>

            <div class="space-y-4">
                <div>
                    <label class="block font-semibold mb-1 text-slate-700">1. Apakah hasil pada Console berubah?</label>
                    <input type="text" class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" value="Ya, hasil tampilan pada console berubah sesuai dengan isi data baru yang dimasukkan.">
                </div>
                <div>
                    <label class="block font-semibold mb-1 text-slate-700">2. Bagian kode mana yang kamu ubah?</label>
                    <input type="text" class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" value="Bagian nilai (value) di dalam tanda kutip / sebelah kanan tanda sama dengan (=).">
                </div>
                <div>
                    <label class="block font-semibold mb-1 text-slate-700">3. Mengapa program dapat menampilkan data yang baru?</label>
                    <textarea class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" rows="2">Karena isi/nilai dari variable telah ditimpa (diperbarui) dengan nilai yang baru sebelum perintah console.log() dijalankan.</textarea>
                </div>
            </div>
        </section>

        <!-- I. AKTIVITAS 5 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">I. AKTIVITAS 5 – VARIABLE UNTUK MENYIMPAN BERBAGAI DATA</h2>
            <p class="mb-4 text-slate-700">JavaScript dapat menyimpan berbagai jenis data. Perhatikan dan identifikasi jenis data berikut:</p>

            <div class="overflow-x-auto mb-6">
                <table class="w-full text-left border-collapse border border-slate-200">
                    <thead>
                        <tr class="bg-slate-50">
                            <th class="border border-slate-200 p-2.5 font-semibold">Variable</th>
                            <th class="border border-slate-200 p-2.5 font-semibold">Nilai</th>
                            <th class="border border-slate-200 p-2.5 font-semibold">Jenis Data (Tipe Data)</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-200">
                        <tr>
                            <td class="border border-slate-200 p-2.5 code-font">nama</td>
                            <td class="border border-slate-200 p-2.5 code-font text-emerald-600">"Andi"</td>
                            <td class="border border-slate-200 p-2.5 font-medium text-indigo-600">String (Teks)</td>
                        </tr>
                        <tr>
                            <td class="border border-slate-200 p-2.5 code-font">umur</td>
                            <td class="border border-slate-200 p-2.5 code-font text-amber-600">17</td>
                            <td class="border border-slate-200 p-2.5 font-medium text-indigo-600">Number (Angka)</td>
                        </tr>
                        <tr>
                            <td class="border border-slate-200 p-2.5 code-font">tinggi</td>
                            <td class="border border-slate-200 p-2.5 code-font text-amber-600">170</td>
                            <td class="border border-slate-200 p-2.5 font-medium text-indigo-600">Number (Angka)</td>
                        </tr>
                        <tr>
                            <td class="border border-slate-200 p-2.5 code-font">aktif</td>
                            <td class="border border-slate-200 p-2.5 code-font text-blue-600">true</td>
                            <td class="border border-slate-200 p-2.5 font-medium text-indigo-600">Boolean (True/False)</td>
                        </tr>
                    </tbody>
                </table>
            </div>

            <div class="bg-slate-50 p-4 rounded-lg border border-slate-200 space-y-3">
                <h4 class="font-bold text-slate-800">Kesimpulan Jenis Data:</h4>
                <p>Data yang ditulis menggunakan tanda kutip seperti <code class="code-font text-emerald-600 font-bold">"Andi"</code> merupakan data: <strong class="text-indigo-600">String (Teks)</strong></p>
                <p>Sedangkan data angka tanpa kutip seperti <code class="code-font text-amber-600 font-bold">17</code> merupakan data: <strong class="text-indigo-600">Number (Angka)</strong></p>
            </div>
        </section>

        <!-- J. AKTIVITAS 6 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">J. AKTIVITAS 6 – MENGENAL let DAN const</h2>
            
            <div class="mb-6">
                <h4 class="font-bold text-slate-800 mb-3">Perbedaan Penggunaan:</h4>
                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse border border-slate-200">
                        <thead>
                            <tr class="bg-slate-50">
                                <th class="border border-slate-200 p-2.5 font-semibold">Keyword</th>
                                <th class="border border-slate-200 p-2.5 font-semibold">Nilai Dapat Diubah?</th>
                                <th class="border border-slate-200 p-2.5 font-semibold">Kegunaan Sederhana</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-slate-200">
                            <tr>
                                <td class="border border-slate-200 p-2.5 code-font font-bold text-purple-600">let</td>
                                <td class="border border-slate-200 p-2.5 text-emerald-600 font-bold">Ya (Bisa)</td>
                                <td class="border border-slate-200 p-2.5">Untuk data yang masih mungkin berubah.</td>
                            </tr>
                            <tr>
                                <td class="border border-slate-200 p-2.5 code-font font-bold text-amber-600">const</td>
                                <td class="border border-slate-200 p-2.5 text-rose-600 font-bold">Tidak (Tetap)</td>
                                <td class="border border-slate-200 p-2.5">Untuk data yang tidak perlu diubah (konstanta).</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <div class="bg-amber-50 border-l-4 border-amber-400 p-4 rounded">
                <p class="font-semibold text-amber-900">Apa yang terjadi saat mengubah nilai pada <code class="code-font font-bold">const</code>?</p>
                <p class="text-amber-800 text-sm mt-1">Program akan menghasilkan error: <code class="code-font font-bold text-rose-600">Uncaught TypeError: Assignment to constant variable.</code></p>
            </div>
        </section>

        <!-- K. AKTIVITAS 7 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">K. AKTIVITAS 7 – ATURAN PENAMAAN VARIABLE</h2>
            <p class="mb-3 text-slate-700">Beberapa aturan dasar penamaan variable di JavaScript:</p>

            <div class="grid md:grid-cols-2 gap-4 mb-4">
                <div class="bg-emerald-50 border border-emerald-200 p-4 rounded-lg">
                    <h4 class="font-bold text-emerald-800 mb-2"><i class="fas fa-check-circle text-emerald-600"></i> Diperbolehkan:</h4>
                    <ul class="code-font text-sm text-slate-700 space-y-1">
                        <li>let nama;</li>
                        <li>let namaSiswa; <span class="text-xs text-slate-500">(camelCase)</span></li>
                        <li>let nama_siswa; <span class="text-xs text-slate-500">(snake_case)</span></li>
                        <li>let umur2;</li>
                    </ul>
                </div>

                <div class="bg-rose-50 border border-rose-200 p-4 rounded-lg">
                    <h4 class="font-bold text-rose-800 mb-2"><i class="fas fa-times-circle text-rose-600"></i> Tidak Diperbolehkan:</h4>
                    <ul class="code-font text-sm text-slate-700 space-y-1">
                        <li>let 1nama; <span class="text-xs text-slate-500">(Diawali angka)</span></li>
                        <li>let nama siswa; <span class="text-xs text-slate-500">(Menggunakan spasi)</span></li>
                        <li>let nama-siswa; <span class="text-xs text-slate-500">(Menggunakan strip)</span></li>
                    </ul>
                </div>
            </div>
            
            <p class="text-sm text-slate-600"><strong>Catatan Penting:</strong> JavaScript bersifat <em>case-sensitive</em> (membedakan huruf besar dan kecil). <code class="code-font text-indigo-600">nama</code> tidak sama dengan <code class="code-font text-indigo-600">Nama</code>.</p>
        </section>

        <!-- L. AKTIVITAS 8 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">L. AKTIVITAS 8 – MANA YANG BENAR?</h2>
            <p class="mb-4 text-slate-700">Evaluasi kebenaran penamaan nama variable berikut:</p>

            <div class="grid md:grid-cols-2 gap-4">
                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse border border-slate-200 text-sm">
                        <thead>
                            <tr class="bg-slate-50">
                                <th class="border p-2">No</th>
                                <th class="border p-2">Nama Variable</th>
                                <th class="border p-2">Status</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr><td class="border p-2">1</td><td class="border p-2 code-font">nama</td><td class="border p-2 text-emerald-600 font-bold">✓ Benar</td></tr>
                            <tr><td class="border p-2">2</td><td class="border p-2 code-font">namaSiswa</td><td class="border p-2 text-emerald-600 font-bold">✓ Benar</td></tr>
                            <tr><td class="border p-2">3</td><td class="border p-2 code-font">nama_siswa</td><td class="border p-2 text-emerald-600 font-bold">✓ Benar</td></tr>
                            <tr><td class="border p-2">4</td><td class="border p-2 code-font">2nama</td><td class="border p-2 text-rose-600 font-bold">✗ Salah</td></tr>
                            <tr><td class="border p-2">5</td><td class="border p-2 code-font">nama siswa</td><td class="border p-2 text-rose-600 font-bold">✗ Salah</td></tr>
                        </tbody>
                    </table>
                </div>

                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse border border-slate-200 text-sm">
                        <thead>
                            <tr class="bg-slate-50">
                                <th class="border p-2">No</th>
                                <th class="border p-2">Nama Variable</th>
                                <th class="border p-2">Status</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr><td class="border p-2">6</td><td class="border p-2 code-font">nilaiAkhir</td><td class="border p-2 text-emerald-600 font-bold">✓ Benar</td></tr>
                            <tr><td class="border p-2">7</td><td class="border p-2 code-font">nilai1</td><td class="border p-2 text-emerald-600 font-bold">✓ Benar</td></tr>
                            <tr><td class="border p-2">8</td><td class="border p-2 code-font">nilai-akhir</td><td class="border p-2 text-rose-600 font-bold">✗ Salah</td></tr>
                            <tr><td class="border p-2">9</td><td class="border p-2 code-font">Alamat</td><td class="border p-2 text-emerald-600 font-bold">✓ Benar</td></tr>
                            <tr><td class="border p-2">10</td><td class="border p-2 code-font">alamatSiswa</td><td class="border p-2 text-emerald-600 font-bold">✓ Benar</td></tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <div class="mt-4 bg-slate-50 p-4 rounded-lg border">
                <h4 class="font-bold mb-2 text-slate-800">Perbaikan Nama Variable yang Salah:</h4>
                <ul class="list-disc pl-5 space-y-1 text-sm text-slate-700">
                    <li><code class="code-font text-rose-600">2nama</code> ➔ Menjadi: <code class="code-font text-emerald-600 font-bold">nama2</code> / <code class="code-font text-emerald-600 font-bold">namaSiswa</code></li>
                    <li><code class="code-font text-rose-600">nama siswa</code> ➔ Menjadi: <code class="code-font text-emerald-600 font-bold">namaSiswa</code> / <code class="code-font text-emerald-600 font-bold">nama_siswa</code></li>
                    <li><code class="code-font text-rose-600">nilai-akhir</code> ➔ Menjadi: <code class="code-font text-emerald-600 font-bold">nilaiAkhir</code> / <code class="code-font text-emerald-600 font-bold">nilai_akhir</code></li>
                </ul>
            </div>
        </section>

        <!-- M & N. TANTANGAN DATA DIRI & LEVEL 2 -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">M & N. AKTIVITAS 9 & 10 – TANTANGAN DATA DIRI</h2>
            <p class="mb-3 text-slate-700">Buat program JavaScript yang menyimpan data diri siswa dan nilai mata pelajaran:</p>

            <div class="bg-slate-900 text-slate-100 p-4 rounded-lg code-font text-sm mb-4 leading-relaxed">
                <span class="text-purple-400">let</span> nama = <span class="text-emerald-400">"Budi"</span>;<br>
                <span class="text-purple-400">let</span> kelas = <span class="text-emerald-400">"XI RPL 1"</span>;<br>
                <span class="text-purple-400">let</span> jurusan = <span class="text-emerald-400">"Rekayasa Perangkat Lunak"</span>;<br>
                <span class="text-purple-400">let</span> umur = <span class="text-amber-400">17</span>;<br>
                <span class="text-purple-400">let</span> hobi = <span class="text-emerald-400">"Bermain game"</span>;<br>
                <span class="text-purple-400">let</span> bahasaIndonesia = <span class="text-amber-400">80</span>;<br>
                <span class="text-purple-400">let</span> matematika = <span class="text-amber-400">85</span>;<br>
                <span class="text-purple-400">let</span> produktif = <span class="text-amber-400">90</span>;<br><br>
                <span class="text-blue-400">console</span>.log(nama);<br>
                <span class="text-blue-400">console</span>.log(bahasaIndonesia);<br>
                <span class="text-blue-400">console</span>.log(matematika);<br>
                <span class="text-blue-400">console</span>.log(produktif);
            </div>
        </section>

        <!-- O. AKTIVITAS 11 (DEBUGGING) -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">O. AKTIVITAS 11 – DEBUGGING</h2>
            
            <p class="font-semibold text-rose-600 mb-2">Program Salah (Awal):</p>
            <div class="bg-slate-900 text-slate-100 p-3 rounded code-font text-sm mb-4">
                let nama siswa = "Budi";<br>
                let umur = 16;<br>
                let 2kelas = "XI RPL";<br><br>
                console.log(nama siswa);<br>
                console.log(umur);<br>
                console.log(2kelas);
            </div>

            <p class="font-semibold text-emerald-600 mb-2">Program yang Sudah Diperbaiki:</p>
            <div class="bg-slate-900 text-emerald-400 p-3 rounded code-font text-sm mb-4">
                let namaSiswa = "Budi";<br>
                let umur = 16;<br>
                let kelas2 = "XI RPL";<br><br>
                console.log(namaSiswa);<br>
                console.log(umur);<br>
                console.log(kelas2);
            </div>

            <h4 class="font-bold mb-2 text-slate-800">Kesalahan yang Ditemukan:</h4>
            <ol class="list-decimal pl-5 text-sm space-y-1 text-slate-700">
                <li>Penggunaan spasi pada nama variable <code class="code-font text-rose-600">nama siswa</code>.</li>
                <li>Nama variable <code class="code-font text-rose-600">2kelas</code> diawali angka.</li>
                <li>Pemanggilan <code class="code-font text-rose-600">console.log()</code> menggunakan nama variable yang salah.</li>
            </ol>
        </section>

        <!-- P & Q. CHALLENGE & THINK PAIR SHARE -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">P & Q. AKTIVITAS 12 & 13 – THINK PAIR SHARE</h2>
            
            <div class="space-y-4">
                <div>
                    <label class="block font-semibold mb-1 text-slate-800">Think (Menurutmu, mengapa programmer membutuhkan variable?):</label>
                    <textarea class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" rows="2">Programmer membutuhkan variable untuk menyimpan data secara dinamis di memori agar nilai data dapat diakses kembali, diolah, dan diperbarui dengan mudah di berbagai bagian program.</textarea>
                </div>
                <div>
                    <label class="block font-semibold mb-1 text-slate-800">Share (Kesimpulan Diskusi Kelompok):</label>
                    <textarea class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" rows="2">Variable memudahkan pengelolaan data dalam program. Penamaan variable harus mengikuti aturan yang benar agar tidak error dan mudah dibaca oleh tim pengembang lain.</textarea>
                </div>
            </div>
        </section>

        <!-- R, S, T. REFLEKSI & KESIMPULAN -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">T. KESIMPULAN</h2>
            <div class="space-y-3 text-sm text-slate-700">
                <p><strong>Variable adalah:</strong> Wadah tempat menyimpan data sementara di dalam memori komputer agar dapat digunakan kembali oleh program.</p>
                <p><strong><code class="code-font text-purple-600">let</code> digunakan untuk:</strong> Mendeklarasikan variable yang nilainya dapat diubah kembali selama program berjalan.</p>
                <p><strong><code class="code-font text-amber-600">const</code> digunakan untuk:</strong> Mendeklarasikan variable bernilai tetap (konstanta) yang nilainya tidak boleh diubah.</p>
                <p><strong>Untuk menampilkan isi variable ke Console kita dapat menggunakan:</strong> <code class="code-font bg-slate-100 px-2 py-1 rounded text-indigo-600 font-bold">console.log(nama_variable);</code></p>
            </div>
        </section>

        <!-- U. TUGAS INDIVIDU -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">U. TUGAS INDIVIDU – "Data Produk Sederhana"</h2>
            <p class="mb-3 text-slate-700">Program JavaScript minimal 6 variable:</p>

            <div class="bg-slate-900 text-slate-100 p-4 rounded-lg code-font text-sm mb-4 leading-relaxed">
                <span class="text-purple-400">const</span> namaProduk = <span class="text-emerald-400">"Keyboard Mechanical"</span>;<br>
                <span class="text-purple-400">const</span> kategori = <span class="text-emerald-400">"Perangkat Komputer"</span>;<br>
                <span class="text-purple-400">const</span> harga = <span class="text-amber-400">150000</span>;<br>
                <span class="text-purple-400">let</span> stok = <span class="text-amber-400">10</span>;<br>
                <span class="text-purple-400">const</span> merek = <span class="text-emerald-400">"Keychron"</span>;<br>
                <span class="text-purple-400">const</span> tersedia = <span class="text-blue-400">true</span>;<br><br>

                <span class="text-blue-400">console</span>.log(namaProduk);<br>
                <span class="text-blue-400">console</span>.log(kategori);<br>
                <span class="text-blue-400">console</span>.log(harga);<br>
                <span class="text-blue-400">console</span>.log(stok);<br>
                <span class="text-blue-400">console</span>.log(merek);<br>
                <span class="text-blue-400">console</span>.log(tersedia);
            </div>
        </section>

        <!-- V. PENILAIAN -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">V. PENILAIAN</h2>
            
            <div class="mb-6">
                <h3 class="font-bold text-lg mb-3 text-slate-800">1. Penilaian Pengetahuan</h3>
                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse border border-slate-200">
                        <thead>
                            <tr class="bg-slate-50">
                                <th class="border border-slate-200 p-2 font-semibold">Indikator</th>
                                <th class="border border-slate-200 p-2 font-semibold w-24 text-center">Skor</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-slate-200">
                            <tr><td class="p-2">Menjelaskan pengertian variable</td><td class="p-2 text-center font-medium">20</td></tr>
                            <tr><td class="p-2">Menjelaskan fungsi variable</td><td class="p-2 text-center font-medium">15</td></tr>
                            <tr><td class="p-2">Membedakan <code class="code-font text-purple-600">let</code> dan <code class="code-font text-amber-600">const</code></td><td class="p-2 text-center font-medium">20</td></tr>
                            <tr><td class="p-2">Menjelaskan aturan penamaan variable</td><td class="p-2 text-center font-medium">15</td></tr>
                            <tr><td class="p-2">Menjelaskan jenis data sederhana</td><td class="p-2 text-center font-medium">10</td></tr>
                            <tr class="bg-indigo-50 font-bold"><td class="p-2">Total</td><td class="p-2 text-center text-indigo-700">80</td></tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <div class="mb-2">
                <h3 class="font-bold text-lg mb-3 text-slate-800">2. Penilaian Keterampilan</h3>
                <div class="overflow-x-auto mb-3">
                    <table class="w-full text-left border-collapse border border-slate-200">
                        <thead>
                            <tr class="bg-slate-50">
                                <th class="border border-slate-200 p-2 font-semibold">Aspek</th>
                                <th class="border border-slate-200 p-2 font-semibold text-center w-12">1</th>
                                <th class="border border-slate-200 p-2 font-semibold text-center w-12">2</th>
                                <th class="border border-slate-200 p-2 font-semibold text-center w-12">3</th>
                                <th class="border border-slate-200 p-2 font-semibold text-center w-12">4</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-slate-200">
                            <tr><td class="p-2">Membuat variable</td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center">✓</td></tr>
                            <tr><td class="p-2">Penamaan variable</td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center">✓</td></tr>
                            <tr><td class="p-2">Penggunaan <code class="code-font text-purple-600">let</code> / <code class="code-font text-amber-600">const</code></td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center">✓</td></tr>
                            <tr><td class="p-2">Menampilkan data</td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center">✓</td></tr>
                            <tr><td class="p-2">Ketepatan kode</td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center">✓</td></tr>
                            <tr><td class="p-2">Debugging</td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center"></td><td class="p-2 text-center">✓</td></tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </section>

        <!-- W & X. SIKAP & RUBRIK -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-4 pb-2 border-b">X. RUBRIK HASIL PROGRAM</h2>
            <div class="overflow-x-auto">
                <table class="w-full text-left border-collapse border border-slate-200">
                    <thead>
                        <tr class="bg-slate-50">
                            <th class="border border-slate-200 p-2 font-semibold">Kriteria</th>
                            <th class="border border-slate-200 p-2 font-semibold text-center w-24">Bobot</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-200">
                        <tr><td class="p-2">Program dapat dijalankan</td><td class="p-2 text-center font-medium">20%</td></tr>
                        <tr><td class="p-2">Penggunaan variable benar</td><td class="p-2 text-center font-medium">20%</td></tr>
                        <tr><td class="p-2">Penamaan variable benar</td><td class="p-2 text-center font-medium">15%</td></tr>
                        <tr><td class="p-2">Penggunaan <code class="code-font text-purple-600">let</code> dan <code class="code-font text-amber-600">const</code> tepat</td><td class="p-2 text-center font-medium">15%</td></tr>
                        <tr><td class="p-2">Data yang digunakan sesuai</td><td class="p-2 text-center font-medium">10%</td></tr>
                        <tr><td class="p-2">Output berhasil ditampilkan</td><td class="p-2 text-center font-medium">10%</td></tr>
                        <tr><td class="p-2">Kerapian kode</td><td class="p-2 text-center font-medium">10%</td></tr>
                        <tr class="bg-indigo-50 font-bold"><td class="p-2">Total</td><td class="p-2 text-center text-indigo-700">100%</td></tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- Y. EXIT TICKET -->
        <section class="bg-white rounded-xl p-6 shadow-sm border border-slate-200">
            <h2 class="text-xl font-bold text-indigo-700 mb-2 pb-2 border-b">Y. EXIT TICKET</h2>
            <p class="text-sm text-slate-600 mb-4">Sebelum meninggalkan kelas, jawab tiga pertanyaan berikut.</p>

            <div class="space-y-4">
                <div>
                    <label class="block font-semibold mb-1 text-slate-700">1. Apa itu variable?</label>
                    <input type="text" class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" value="Variable adalah tempat atau wadah untuk menyimpan data di memori komputer agar bisa digunakan kembali.">
                </div>
                <div>
                    <label class="block font-semibold mb-1 text-slate-700">2. Apa perbedaan let dan const?</label>
                    <input type="text" class="w-full p-2.5 border border-slate-300 rounded-lg focus:ring-2 focus:ring-indigo-400 outline-none text-slate-800 bg-amber-50/30" value="let nilainya dapat diubah kembali (dinamis), sedangkan const nilainya tetap dan tidak dapat diubah (konstanta).">
                </div>
                <div>
                    <label class="block font-semibold mb-1 text-slate-700">3. Tuliskan satu contoh variable JavaScript.</label>
                    <div class="bg-slate-900 text-emerald-400 p-3 rounded-lg code-font text-sm">
                        let namaSiswa = "Satria Rippana PPLG 2"
                    </div>
                </div>
            </div>
        </section>

        <!-- Z. PESAN UNTUK PESERTA DIDIK -->
        <section class="bg-gradient-to-br from-indigo-600 to-purple-700 text-white rounded-xl p-6 shadow-md text-center">
            <h2 class="text-2xl font-bold mb-4">Z. PESAN UNTUK PESERTA DIDIK</h2>
            <div class="max-w-2xl mx-auto space-y-3 text-indigo-100 font-medium">
                <p class="text-lg text-white font-semibold">Jangan takut ketika program menghasilkan error.</p>
                <p>Error bukan berarti kamu gagal.</p>
                <p>Error adalah petunjuk bahwa programmu perlu diperbaiki.</p>
                <p class="pt-3 text-amber-200 font-bold border-t border-indigo-400/50">
                    Programmer yang baik bukan programmer yang tidak pernah mengalami error, tetapi programmer yang mampu mencari dan memperbaiki error.
                </p>
            </div>
        </section>

    </div>

    <footer class="text-center text-slate-500 text-xs py-6 mt-8 no-print">
        LKPD Interaktif Pemrograman Web Dasar - Kunci Jawaban Lengkap (D - Z)
    </footer>

</body>
</html>

