# Aqliy hisob — Telegram Mini App'ni ishga tushirish

Ilova bitta fayl: `index.html`. Server, domen va ma'lumotlar bazasi kerak emas:
- **Hosting:** GitHub Pages, bepul. Manzil `https://<login>.github.io/aqliy-hisob/` ko'rinishida bo'ladi.
- **Sinxron:** Telegram CloudStorage, bepul. Natijalar Telegram akkauntingizga bog'lanadi. Telefon va PC'dagi Telegram'da bir xil bo'ladi.

## 1. Saytni GitHub Pages'ga joylash (bir marta)
1. GitHub'da yangi **public** repo oching, masalan `aqliy-hisob`.
2. `index.html` faylini repo'ga yuklang: **Add file → Upload files**.
3. **Settings → Pages** bo'limiga kiring. **Source:** `Deploy from a branch`, **Branch:** `main`, papka `/ (root)` → **Save**.
4. 1–2 daqiqadan keyin sahifa ochiladi: `https://<login>.github.io/aqliy-hisob/`.

> Repo'da faqat ilova kodi turadi. Sizning natijalaringiz u yerda saqlanmaydi, ular Telegram bulutida.

## 2. Telegram bot va Mini App (bir marta)
1. Telegram'da **@BotFather**'ni oching va `/newbot` yuboring. Nom bering, masalan "Aqliy hisob", va username bering, masalan `aqliy_hisob_meniki_bot`.
2. `/mybots` → botingizni tanlang → **Bot Settings → Menu Button → Configure menu button**.
3. URL sifatida GitHub Pages manzilini yuboring, tugma nomi uchun esa `Mashq`.
4. Ixtiyoriy: `/newapp` buyrug'i bilan to'liq Mini App ro'yxatdan o'tkazsangiz, `t.me/<bot>/<app>` havolasi paydo bo'ladi.

Endi botni oching va pastdagi **Mashq** tugmasini bosing. Telefonda ham, Telegram Desktop'da ham ilova ochiladi.

## 3. Sinxron qanday ishlaydi
- Har bir mashq tugaganda natija Telegram bulutiga yoziladi. Ilova ochilganda yoki qayta faollashganda bulutdan o'qiladi.
- Ikkala qurilmada ham internetsiz o'ynagan bo'lsangiz, natijalar **birlashtiriladi**: eng yaxshi yulduzlar va rekordlar saqlanadi, kunlar qo'shiladi.
- Bosh sahifaning pastida holat ko'rinadi: "Bulut bilan sinxron (telefon va PC)".
- Ilovani oddiy brauzerda ochsangiz ham ishlaydi, lekin natijalar faqat o'sha brauzerda qoladi.

## 4. Eski natijalarni ko'chirish (`aqliy-hisob.html` faylidan)
1. Eski `aqliy-hisob.html` faylini o'sha brauzerda oching.
2. `F12` → **Console** bo'limiga quyidagini yozing va Enter bosing:
   ```
   copy(localStorage.getItem('aqliy-hisob-v1'))
   ```
3. Telegram'dagi ilovada: bosh sahifa → **Zaxira nusxa va natijalarni ko'chirish** → **Tiklash** maydoniga joylang → **Tiklash**.

Darajalar, yulduzlar, 60 soniya rekordi va yechilgan savollar soni ko'chadi. Eski faylda kunlik tarix yo'q edi, shuning uchun "Before/After" statistikasi shu kundan boshlanadi.

## 5. Ilovani yangilash
`index.html`ning yangi versiyasini o'sha repo'ga qayta yuklang. 1–2 daqiqada Telegram'da ham yangilanadi. Natijalar o'chmaydi.

## Mavzu (qorong'i rejim)
Bosh sahifaning yuqori o'ng burchagidagi tugma bosilganda mavzu navbat bilan almashadi: 🌗 Avto → 🌙 Qorong'i → ☀️ Yorug'. "Avto" rejimida Telegram'ning (yoki tizimning) mavzusi ishlatiladi. Tanlov har bir qurilmada alohida saqlanadi.

## Tez qaror mashqlari nimaga asoslangan
- **Tezkor ko'rish.** Bu "Useful Field of View" tezlik mashqining soddalashgan ko'rinishi.
  - Dalil darajasi kuchli. ACTIVE randomizatsiyalangan tadqiqotida 2 800 dan ortiq kishi qatnashgan.
  - Mashq ishlov berish tezligini oshirgan va vaqt chegaralangan kundalik vazifalarga ko'chgan.
  - 10 yillik kuzatuvda bu guruhda demensiya xavfi ~29% kamroq bo'lgan (Edwards va boshq., 2017).
  - Ishtirokchilar asosan 65 yoshdan katta bo'lgan.
- **Tez qaror.** 32 ta qaror, 4 xil topshiriq. Hammasi har safar tasodifiy yaratiladi. Ketma-ket 2 ta to'g'ri javobdan keyin daraja oshadi, xatodan keyin pasayadi. Xato qilsangiz, sababi ko'rsatiladi.
  - 🌀 **Harakat yo'nalishi** (random-dot motion). Dalil darajasi o'rtacha. Mashq bilan harakatni ajratish yaxshilangan va oylab saqlangan (Ball va Sekuler, 1982). Tez qaror mashqidan keyin odamlar aynan shu sinovda aniqlikni yo'qotmasdan tezlashgan (Green va boshq., 2010). Oddiy qarorlarda ortiqcha ehtiyotkorlik kamaygan (Dutilh va boshq., 2009).
  - ⚫ **Qaysi ko'p** va ➕ **Taxminiy qo'shish** (son sezgisi). Dalil darajasi o'rtacha. Kattalarda 10 seans taxminiy qo'shish mashqi oddiy arifmetikani ham yaxshilagan (Park va Brannon, 2013).
  - 🛒 **Arzonini topish** — bir xil mahsulotning ikki o'rami. Bu hayotiy mashq, ilmiy dalili yo'q. Narxlar taxminiy.
- **"Yetarlicha yaxshi" qoidasi.** Dalil darajasi: kuzatuv tadqiqoti. Har doim "eng zo'rini" qidiradiganlar ko'proq afsuslanishi va kamroq qoniqishi aniqlangan (Schwartz va boshq., 2002).

## Xotira mashqlari nimaga asoslangan
- **Takrorlash.** Xato misollar 1, 3, 7, 14, 30 kundan keyin qayta so'raladi. *Distributed practice* (vaqt bo'yicha taqsimlangan takrorlash) va *practice testing* (o'zini sinash) eslab qolishning eng samarali usullari deb baholangan. Manba: Dunlosky va hamkorlar, 2013.
- **Raqam xotirasi.** Ishchi xotira hajmining klassik o'lchovi (digit span). Bu yerda u Before/After ko'rsatkichi sifatida ham ishlatiladi.
- **Rasm xotirasi.** Rasm va uning joyini eslab qolish. Maslahat sifatida "joylar usuli" (method of loci) beriladi.

## Mnemonika o'yinlari (har birida 8 ta daraja, oddiydan murakkabga)
Har o'yinning birinchi darajalarida tayyor sahna yoki hikoya beriladi. Keyingi darajalarda uni o'zingiz to'qiysiz, narsalar soni ko'payadi. Keyingi daraja oldingisi o'tilgandan keyin ochiladi. Tavsiya etilgan tartib: Juftliklar → Hikoya zanjiri → Xotira saroyi; Bo'laklash → Raqam-shakl.
- **🔗 Juftliklar** — ikki narsani bitta g'alati sahnada bog'lash. Dalil darajasi kuchli. Bower, 1970. Tasavvuri kuchsiz odamlar ham shuncha foyda ko'rgan: Thomas va boshq., 2023.
- **📖 Hikoya zanjiri** — rasmlarni ketma-ket hikoyaga ulash. Klassik tajriba: Bower va Clark, 1969.
- **🏠 Xotira saroyi** — joylar usuli. Dalil darajasi kuchli:
  - oddiy odamlar 6 hafta mashq qilib, 72 so'zdan eslaganlari ~26 tadan ~62 taga oshgan, natija 4 oydan keyin ham saqlangan (Dresler va boshq., 2017, *Neuron*);
  - tartib bilan eslashda eng samarali usullardan biri (Roediger, 1980);
  - 2025-yilgi tizimli sharh va meta-tahlil ham samaradorligini tasdiqlagan.
- **🧩 Bo'laklash** — uzun raqamni 2–3 xonali bo'laklarga bo'lish. Dalil darajasi kuchli:
  - ishchi xotira hajmi bo'laklar bilan o'lchanadi (Miller, 1956; Cowan, 2001);
  - bir talaba mashq qilib, raqam eslash hajmini 7 tadan ~80 taga yetkazgan (Ericsson, Chase, Faloon, 1980).
- **🥚 Raqam-shakl** — raqamli ilgak (peg) tizimi: 0 🥚, 1 🕯️, 2 🦢, 3 🚦, 4 🚗, 5 🖐️, 6 🐌, 7 🌈, 8 ⛄, 9 🎈.
  - Dalil darajasi o'rtacha: Roediger, 1980; Bugelski va boshq., 1968.
  - Rasmlar to'plami ilova uchun moslashtirilgan.
- N-back qo'shilmadi: meta-tahlillarga ko'ra uning foydasi asosan o'sha mashqning o'zi bilan cheklanadi.
