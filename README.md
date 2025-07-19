# ClickFood

Minimalistický, hravý průvodce tím, **co dnes jíst**.  
Frontend React + Vite, backend Express. Záměrem je rychle poradit, uvařit nebo doporučit podnik – a u toho se bavit.

---

## ✨ Klíčové vlastnosti

| Modul | Funkčnost | Stav |
|-------|-----------|------|
| **Web (React/Vite)** | Interaktivní UI, maskot, hlavní tlačítko „Co dnes jíst?“ | 🚧 MVP |
| **API (Express)** | `/health`, `/suggest` – zatím mock dat | 🚧 MVP |
| **Rozšiřitelné** | OpenAI × recepty, Google Places, mobilní app (Expo) | 🔜 |

---

## 🛠 Technologický stack

- **Frontend:** Vite + React 18, moderní ESM
- **Backend:** Express 4, čisté ESM (Node 20)
- **Dev:** npm, Concurrently, nodemon
- **Testy:** zatím none → plán jest Vitest/Jest
- **Licence:** MIT

---

## ⚡ Rychlý start

> **Požadavky:** Node >= 20, npm >= 9 (nebo pnpm/yarn), git.

```bash
# 1) Klon repozitáře
git clone https://github.com/<user>/clickfood.git
cd clickfood

# 2) Instalace root dev závislostí (concurrently)
npm install

# 3) Frontend
cd web
npm install             # poprvé
npm run dev             # http://localhost:5173
# 4) Backend (nové okno / terminál)
cd ../api
npm install             # pokud ještě nebylo
npm run dev             # http://localhost:4000/health

# Build statických souborů webu
cd web && npm run build && cd ..
# Spouštíme API + statické soubory (volitelně přes nginx / serve)
node api/index.js

clickfood/
├─ web/             # React/Vite frontend
│  ├─ src/
│  ├─ public/
│  ├─ vite.config.js
│  └─ package.json
├─ api/             # Express backend (ESM)
│  ├─ index.js
│  └─ package.json
├─ .gitignore
├─ .env.example
├─ package.json     # root – dev scripts, concurrently
├─ README.md
└─ LICENSE

# Backend
PORT=4000

# Budoucí integrace
# OPENAI_API_KEY=
# GOOGLE_PLACES_API_KEY=


---

### ✅ Co dál

* **Commit + push:**  
  ```bash
  git add README.md .gitignore
  git commit -m "docs: complete README and add .gitignore"
  git push

---

## 📋 Checklist po inicializaci projektu

1. **Vytvoř (nebo zkopíruj) `.gitignore` do rootu repozitáře**
   - Ujisti se, že obsahuje alespoň:
     ```
     node_modules/
     dist/
     .env
     /web/node_modules/
     /api/node_modules/
     ```
2. **Zkontroluj, že složky `web/` a případně `api/` jsou commitnuté**
   - Ověř, že je v repozitáři vše potřebné (včetně zdrojového kódu a konfiguračních souborů).
   - Pro kontrolu spusť:
     ```bash
     git status
     ```

3. **Commitni a pushni všechny změny**
   - Přidej nové nebo upravené soubory:
     ```bash
     git add .
     git commit -m "feat: add .gitignore and scaffold folders"
     git push
     ```

---

> **Po těchto krocích je repozitář připravený pro další vývoj, spolupráci i nasazení!**

---

## ✅ Kontrola & uložení změn

Po dokončení úprav README.md doporučujeme:

1. **Zkontrolovat správnost formátování**  
   - Prohlédni si náhled (např. na GitHubu nebo v editoru s podporou Markdownu).
   - Ověř, že jsou všechny sekce přehledně oddělené a odkazy fungují.

2. **Commitnout a pushnout změny**  
   ```bash
   git add README.md
   git commit -m "docs: update and finalize README"
   git push
