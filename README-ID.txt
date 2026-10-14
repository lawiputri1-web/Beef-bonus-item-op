BEEF BONUS — Minecraft Java 1.21 / Fabric Loader

Setiap kali makan steak, hadiah acak diberikan. Daftar hadiah dibuat beragam:
- Makanan, buah, kue, golden apple
- Blok bangunan dan material dekorasi
- Tools dan perlengkapan
- Weapon, panah, roket
- Armor, Elytra, Wolf Armor
- Resource seperti iron/gold/diamond/emerald/ender pearl
- Utility/loot seperti name tag, saddle, shulker shell, beacon, totem
- Enchanted book dengan enchantment dan level acak
- Potion dan item langka
- Netherite ingot dan Netherite Upgrade Smithing Template sangat langka
- Jackpot super langka: netherite gear atau enchanted golden apple

Probabilitas kategori berbobot di kode; item langka memang jauh lebih jarang.
Jika inventori penuh, hadiah dijatuhkan ke tanah.

STATUS: Proyek sumber saja, belum JAR siap pasang dan belum dites. Build butuh JDK 21
serta koneksi internet ke repositori Fabric/Maven. Jalankan `gradle build` dari folder
proyek; hasil di `build/libs/beefbonus-1.0.0.jar`. Pasang Fabric Loader + Fabric API
untuk Minecraft Java 1.21.


BUILD VIA GITHUB ACTIONS (dari HP):
1. Buat repository baru di github.com, misalnya BeefBonus-Fabric-1.21.
2. Upload seluruh isi ZIP proyek ke repository (termasuk folder .github).
3. Buka tab Actions dan izinkan Actions jika GitHub meminta.
4. Workflow "Build Beef Bonus Fabric 1.21" akan jalan otomatis setelah push.
   Bisa juga buka Actions > pilih workflow > Run workflow.
5. Buka hasil run yang selesai hijau, lalu download artifact "BeefBonus-Fabric-1.21".
6. Ekstrak artifact ZIP; ambil beefbonus-1.0.0.jar dan taruh di folder mods.
Jika build merah/gagal, buka log workflow dan periksa pesan error.

Workflow GitHub Actions: .github/workflows/main.yml. Workflow memasang Gradle 8.10.2 dan JDK 21, lalu menjalankan `clean remapJar` agar yang diunggah adalah JAR mod hasil remapping Fabric (bukan sources JAR).
