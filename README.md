<h1 align="center">🌟 ALPHA LC — O'quv Markazi Ekotizimi</h1>

<p align="center">
  Zamonaviy til o'quv markazlari uchun to'liq avtomatlashtirilgan boshqaruv tizimi — <strong>Telegram Bot</strong>, <strong>Web App</strong> va sun'iy intellekt imkoniyatlari bir platformada.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/FastAPI-backend-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Aiogram-3.21-2CA5E0?style=flat-square&logo=telegram&logoColor=white" alt="Aiogram"/>
  <img src="https://img.shields.io/badge/React-19-149ECA?style=flat-square&logo=react" alt="React"/>
  <img src="https://img.shields.io/badge/PostgreSQL-16-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Docker-ready-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
</p>

---

## Mundarija

- [Umumiy Ko'rinish](#umumiy-korinish)
- [Asosiy Imkoniyatlar](#asosiy-imkoniyatlar)
- [Texnologik Stack](#texnologik-stack)
- [Loyiha Tuzilishi](#loyiha-tuzilishi)
- [Lokal O'rnatish va Ishga Tushirish](#lokal-ornatish-va-ishga-tushirish)
- [Docker Orqali Ishga Tushirish](#docker-orqali-ishga-tushirish)
- [Litsenziya](#litsenziya)

---

## Umumiy Ko'rinish

**ALPHA LC** — o'quv markazlari (IELTS/CEFR yo'nalishi) uchun mo'ljallangan integratsiyalashgan boshqaruv tizimi. Talabalar Telegram bot va Web App orqali ro'yxatdan o'tadi, kurslarga yoziladi, testlardan o'tadi va to'lovlarini kuzatib boradi; o'qituvchi va adminlar esa alohida panel orqali guruhlar, davomat, uy vazifalari va to'lovlarni boshqaradi.

## Asosiy Imkoniyatlar

### Talabalar uchun
- **Ko'p tillilik**: O'zbek, Rus, Ingliz tillarida ro'yxatdan o'tish va interfeys.
- **Kurslar katalogi**: Jadval, daraja (A1–C2) va guruhlar bo'yicha ko'rish.
- **Bepul sinov darsi**: Daraja aniqlash testi + birinchi bosgan o'qituvchiga avtomatik biriktirish.
- **Referal dasturi**: Har bir taklif uchun kumulyativ chegirma, jami 100% gacha.
- **Gamifikatsiya**: Xarakter nishonlari (badges), XP tizimi, 7 kunlik streak, avtomatik PDF sertifikatlar.
- **To'lovlar**: Click, Payme, Uzum orqali to'lov so'rovi yuborish (admin/o'qituvchi tasdiqlaydi).

### O'qituvchi va Admin uchun
- **QR-kod orqali davomat** nazorati.
- **Uy vazifalarini** yuklash va tekshirish, 3 soatlik javobsizlikda avtomatik adminga eskalatsiya.
- **AI PDF Test Generator**: PDF fayldan savol, variant va javoblarni AI yordamida avtomatik ajratib olish — qo'lda kiritishga hojat qolmaydi.
- **Jonli KPI dashboard**: guruhlar, talabalar va to'lovlar bo'yicha umumiy nazorat.
- **Ommaviy xabar yuborish (broadcast)** — maqsadli auditoriyalarga.

---

## Texnologik Stack

| Qatlam | Texnologiyalar |
|---|---|
| **Backend** | Python 3.12, FastAPI, SQLAlchemy, PostgreSQL 16 |
| **Bot** | Aiogram 3.21 |
| **Frontend (WebApp)** | React 19, Vite, Tailwind CSS v4 |
| **Deployment** | Docker, Nginx, Cloudflare Tunnel |

---

## Loyiha Tuzilishi

```
english_center/
├── app/            # Telegram bot handlerlari va logikasi
├── backend/        # FastAPI backend (API)
├── webapp/         # React + Vite frontend (Telegram Mini App)
├── locales/        # Ko'p tillilik tarjima fayllari
├── middlewares/    # Aiogram middleware'lari
├── nginx/          # Reverse proxy konfiguratsiyasi
├── scripts/        # Yordamchi skriptlar
├── init_db.py      # Ma'lumotlar bazasini boshlang'ich to'ldirish
├── main.py         # Bot kirish nuqtasi
└── docker-compose.yml
```

---

## Lokal O'rnatish va Ishga Tushirish

### 1. Repositoryni yuklab oling va paketlarni o'rnating
```bash
git clone https://github.com/zemeisteer/english_center.git
cd english_center
pip install -r requirements.txt
```

### 2. Muhit o'zgaruvchilarini sozlang
```bash
cp .env.example .env
```
`.env` faylida quyidagilarni to'ldiring: `BOT_TOKEN` ([@BotFather](https://t.me/BotFather)dan), `ADMINS`, PostgreSQL ulanish ma'lumotlari, `WEBAPP_URL`.

### 3. Ma'lumotlar bazasini tayyorlang
```bash
python init_db.py
```

### 4. Botni ishga tushiring
```bash
python main.py
```

### 5. Frontend (WebApp)ni ishga tushiring
```bash
cd webapp
npm install
npm run dev
```

---

## Docker Orqali Ishga Tushirish

Loyiha to'liq konteynerlashtirilgan — PostgreSQL, FastAPI backend, bot, React frontend va Nginx bitta buyruq bilan ishga tushadi:

```bash
cp .env.example .env   # va to'ldiring
docker compose up -d --build
```

Bu quyidagilarni ishga tushiradi: `postgres`, `backend` (FastAPI), `bot` (Aiogram), `frontend` (React) va `nginx` (reverse proxy, 80-port).

---

## Litsenziya

Bu — buyurtma asosida ishlab chiqilgan proprietar (yopiq) loyiha. Barcha huquqlar himoyalangan © 2026.
