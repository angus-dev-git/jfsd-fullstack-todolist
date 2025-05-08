
# 📝 Fullstack Todo List App

Applicazione fullstack per la gestione di una lista di cose da fare (ToDo), sviluppata con **React** per il frontend, **Node.js/Express** per il backend, e **MongoDB** come database. Supporta ambienti multipli, è pronta per la produzione e containerizzata via Docker.

---

## 🧩 Stack Tecnologico

- **Frontend**: React + Vite
- **Backend**: Node.js + Express
- **Database**: MongoDB
- **Ambiente**: Docker + Docker Compose
- **Altro**: Nginx, CORS, Gestione variabili `.env`

---

## 🚀 Avvio rapido (con Docker)

Assicurati di avere **Docker** e **Docker Compose** installati. Poi esegui:

```bash
docker-compose up --build
```

Questo avvierà:

- Backend su `http://localhost:3001`
- Frontend (React con Nginx) su `http://localhost:8080`

---

## 🔐 Variabili d’ambiente

Le variabili sono caricate da file `.env`. Non vengono versionate per sicurezza, ma un esempio è fornito.

### 📁 `.env.example` (da copiare in `.env`)

```env
PORT=8000
DB_URL=mongodb://localhost:27017/todolist
CORS_ORIGIN=http://localhost:8080
```

> ⚠️ Ricordati di creare il file `.env` nella root del backend prima di avviare il server senza Docker.

---

## 🧪 Script disponibili

### 📦 Backend (Node.js)

```bash
npm install        # Installa le dipendenze
npm run dev        # Avvia il backend in modalità sviluppo (con nodemon)
npm start          # Avvia il backend in modalità produzione
```

### 🖥️ Frontend (React)

```bash
npm install        # Installa le dipendenze
npm run dev        # Avvia l’app in sviluppo su http://localhost:5173
npm run build      # Compila la build di produzione
```

---

## 🔍 API Endpoints principali

| Metodo | Rotta            | Descrizione         |
|--------|------------------|---------------------|
| POST   | `/user/login`    | Login utente        |
| POST   | `/user/register` | Registrazione       |
| GET    | `/activity`      | Recupera i ToDo     |
| POST   | `/activity`      | Crea un nuovo ToDo  |

---

## 📦 Struttura dei container

```yaml
frontend:
  - React app compilata
  - Servita da Nginx

backend:
  - Express API
  - MongoDB connection

volumes:
  - Sincronizzazione file locali per sviluppo live
```

---

## ✅ Obiettivi e Buone pratiche usate

- [x] Separazione frontend/backend
- [x] Gestione centralizzata delle `.env`
- [x] Compatibilità con Docker
- [x] Esempio pubblico senza dati sensibili
- [x] Configurazione `CORS` sicura

---

## 📸 Screenshot

(-)

---

## 🧑‍💻 Autore

**Tuo Nome**  
👉 [GitHub](https://github.com/angus-dev-git)  
📧 [augusto.ciuccatosti(AT)gmail.com]

---

## 📄 Licenza

MIT License
