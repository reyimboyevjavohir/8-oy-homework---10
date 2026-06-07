# PsixoHelp v3

## Ishga tushirish (Docker bilan)

### 1. Loyihani clone qiling
```bash
git clone https://github.com/SIZNING_USERNAME/psixohelp.git
cd psixohelp
```

### 2. .env fayl yarating
```bash
cp .env.example .env
```
`.env` faylni oching va qiymatlarni to'ldiring:
```env
POSTGRES_PASSWORD=kuchli_parol
JWT_SECRET=maxfiy_kalit
GROQ_API_KEY=gsk_...   # https://console.groq.com
CLIENT_URL=http://localhost:3000
NEXT_PUBLIC_API_URL=http://localhost:4000/api
```

### 3. Docker bilan ishga tushiring
```bash
docker compose up --build -d
```

### 4. Manzillar
- Frontend: http://localhost:3000
- Backend:  http://localhost:4000
- Health:   http://localhost:4000/api/health

---

## Ishga tushirish (Docker siz)

### Backend
```bash
cd apps/backend
cp .env.example .env
# .env ni to'ldiring
npm install
npx prisma migrate deploy
npx prisma generate
npm run dev
```

### Frontend
```bash
cd apps/frontend
npm install --legacy-peer-deps
npm run dev
```
# 8-oy-homework---10
