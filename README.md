# 🎨 Drawing Board: Interactive HTML5 Canvas Vector Engine

Foydalanuvchiga real vaqt rejimida rang va chiziq qalinligini erkin sozlagan holda grafik chizmalar yaratish imkonini beruvchi interaktiv veb-ilova. Loyiha HTML5 Canvas API va JavaScript manipulyatsiyalari yordamida yuqori unumdorlikda ishlovchi silliq vektorli chizish mexanizmiga asoslangan.

---

## 📝 Loyiha haqida

Ushbu dastur brauzer muhitida ishlovchi raqamli chizish taxtasidir. Yuqori qismda joylashgan boshqaruv paneli (Toolbar) orqali kiber-neon uslubidagi ranglarni tanlash, cho'tka o'lchamini o'zgartirish va yagona tugma yordamida butun maydonni tozalash imkoniyatlari mavjud. Dastur minimal kod bilan maksimal funksionallikni ta'minlaydi.

---

## 📐 Chizish Algoritmi va Matematikasi (DOM Event Architecture)

Dastur sichqonchaning harakat koordinatalarini uzluksiz kuzatib boradi va Canvas yuzasidagi chiziqlarni quyidagi mantiqiy zanjir asosida render qiladi:

1. [ mousedown ] ──► Chizish holatini faollashtirish (painting = true) va nuqtani boshlash.
2. [ mousemove ] ──► Agar faol bo'lsa, joriy kursor nuqtasiga chiziq tortish (ctx.lineTo).
3. [ Y o'qi siljishi ] ──► Toolbar balandligini kompensatsiya qilish uchun (e.clientY - 70px) formulasi qo'llaniladi.
4. [ mouseup ] ──► Chizishni to'xtatish (painting = false) va vektor yo'lini yakunlash (ctx.beginPath).

---

## ⚡ Asosiy xususiyatlari (Features)

* 🖌️ **Smooth Vector Brush:** `ctx.lineCap = 'round'` xususiyati yordamida chiziq burchaklarini yumshatish va uzilishlarsiz, silliq render hosil qilish.
* 🎨 **Dynamic Palette Input:** Brauzerning ichki ranglar palitrasi tizimi bilan integratsiya qilingan har qanday rang rejimini qo'llab-quvvatlash.
* 📏 **Adaptive Range Slider:** Cho'tka o'lchamini 1 pikseldan 50 pikselgacha real vaqt rejimida dinamik o'zgartira olish paneli.
* 🧼 **Instant Vector Clear:** Canvas kontekstining `clearRect()` funksiyasi yordamida tezkor xotira tozalash algoritmi.
* 💻 **Viewport Responsive Layout:** Ekran o'lchamlariga qarab ishchi maydonni (`canvas.width` va `canvas.height`) brauzer oynasiga moslab hisoblash.

---

## 🛠️ Texnologiyalar (Tech Stack)

* **HTML5 Canvas** — Grafik yo'llarni chizish uchun 2D renderlash konteksti (`getContext('2d')`).
* **CSS3 UI Stylings** — To'q kiber-fon, neon soyalar (`box-shadow`) va moslashuvchan Toolbar elementlari.
* **Vanilla JavaScript (ES6+)** — Hodisalarni tinglash (`addEventListener`), sichqoncha koordinatalari monitoringi va chizish holati boshqaruvi (`boolean flags`).

---

## 🚀 Ishga tushirish (How to Run)

Loyiha hech qanday tashqi kutubxonalarga yoki plaginlarga bog'liq emas:

1. Repozitoriyni kompyuterga yuklab oling:
   ```bash
   git clone [https://github.com/orgkamolbek/drawing-board.git](https://github.com/orgkamolbek/drawing-board.git)
