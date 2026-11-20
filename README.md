# Perang Abadi

Permainan RPG teks fantasi yang boleh dimainkan melalui pelayar web dan dipasang sebagai PWA.

## Ciri permainan

- Tiga kelas watak dengan gaya pertempuran berbeza.
- Pertempuran, naik tahap, XP dan ganjaran emas.
- Haiwan teman yang boleh membantu dalam pertempuran.
- Kelengkapan, barang rampasan, inventori dan sistem jual beli.
- Pokok kemahiran, tukang besi, pembuatan dan bahan sumber.
- Dungeon, bos dunia dan papan misi.
- Simpanan automatik, sandaran, eksport dan import data permainan.
- Antara muka Bahasa Melayu Malaysia dengan istilah RPG Inggeris yang biasa digunakan.

## Cara bermain

Buka `index.html` melalui GitHub Pages atau pelayan web statik. Untuk pengalaman seperti aplikasi telefon, gunakan pilihan **Add to Home Screen** pada pelayar yang menyokong PWA.

## Nota pembangunan

Projek ini menggunakan HTML, CSS dan JavaScript tanpa rangka kerja luaran. Data permainan disimpan secara setempat dalam pelayar pengguna.


## Combat System V4

- Kesan status dalam pertempuran: bleed, burn dan poison; kesan berterusan memberi kerosakan mengikut giliran.
- Bos mempunyai dua fasa. Apabila HP jatuh ke 50%, bos memasuki fasa mengamuk dengan serangan dan pertahanan lebih tinggi.
- Musuh menggunakan AI asas: pulih HP apabila lemah, bertahan untuk menyerap serangan pemain, atau melancarkan serangan berat.
- Aksi pemain baharu: mengelak (peluang 75% untuk elak serangan seterusnya) dan counter (serangan balas apabila musuh menyerang).
- Kemahiran serangan kini menggunakan cooldown mengikut giliran, bukan lagi terhad sekali setiap pertempuran: Tebasan Perkasa 3 giliran dan Amukan Naga 4 giliran. Cooldown berkurang setiap kali pemain mengambil tindakan.
- Save schema dinaikkan ke versi 4. Save versi terdahulu dimigrasikan; status pertempuran sementara direset dengan selamat ketika load.

### Senarai semak ujian manual

1. Load save lama dan pastikan watak, level, gear, inventory, quest, pet dan gold kekal.
2. Mulakan pertempuran dan uji Serang, Kemahiran, Bertahan, Mengelak, Counter, Ramuan dan Kabur.
3. Pastikan bleed/burn pada musuh dan poison pada pemain mengurangkan HP mengikut giliran.
4. Uji musuh yang menggunakan heal, guard dan heavy attack.
5. Uji bos sehingga HP 50% atau kurang dan sahkan fasa kedua diaktifkan sekali sahaja.
6. Menang/kalah, kemudian mulakan pertempuran baharu dan pastikan status lama tidak terbawa.
7. Uji dungeon dan World Boss serta eksport/import save.
