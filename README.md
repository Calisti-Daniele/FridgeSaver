# 🥦 FridgeSaver

> Riduci lo spreco alimentare in casa — scansiona, tieni traccia e cucina in modo intelligente.

FridgeSaver è un'app Android che aiuta gli utenti a ridurre lo spreco alimentare tenendo traccia di cosa c'è nel frigo, avvisando prima che i prodotti scadano e generando ricette anti-spreco tramite una pipeline LLM multi-step.

Sviluppata come progetto universitario per dimostrare lo sviluppo Android moderno con **MVVM**, **Jetpack Compose**, **Room**, **Coroutines**, **Flows** e molto altro.

---

## ✨ Funzionalità

- 📷 **Scansione foto del frigo** — ML Kit Vision riconosce automaticamente gli alimenti da una fotografia
- 🔍 **Scansione barcode** — recupera i metadati del prodotto tramite OpenFoodFacts API
- ✏️ **Inserimento manuale** — fallback per i prodotti non presenti nel database
- 🔔 **Notifiche di scadenza** — WorkManager schedula controlli giornalieri e invia notifiche locali (urgente / promemoria)
- 🤖 **Ricette LLM multi-step** — genera ricette anti-spreco dagli ingredienti disponibili, con raffinamento opzionale tramite follow-up
- ❤️ **Ricette salvate** — salva i preferiti in locale con Room
- 🏆 **Gamification** — punti, streak giornalieri e badge per aver consumato gli alimenti prima della scadenza

## 🛠️ Stack tecnologico

| Area | Tecnologia |
|---|---|
| UI | Jetpack Compose · Material 3 · Navigation Compose |
| Gestione stato | StateFlow · SharedFlow · sealed class UiState |
| Asincronia | Kotlin Coroutines · viewModelScope |
| Database | Room · Flow DAO · TypeConverters |
| Lavoro in background | WorkManager · CoroutineWorker |
| Rete | Retrofit · OpenFoodFacts API |
| Visione artificiale | ML Kit Vision API |
| Intelligenza artificiale | Pipeline LLM multi-step |
| Testing | JUnit4 |


## 🚀 Come iniziare

### Prerequisiti

- Android Studio
- Android SDK 26+
- Una chiave API valida per il provider LLM scelto

### Configurazione

1. Clona la repository
   ```bash
   git clone https://github.com/tuo-username/fridgesaver.git
   ```

2. Apri il progetto in Android Studio

3. Aggiungi le chiavi API in `local.properties`:
   ```
   LLM_API_KEY=la_tua_chiave
   ```

4. Esegui su emulatore o dispositivo fisico (API 26+)

---

## 📋 Requisiti

- **SDK minimo**: Android 8.0 (API 26)
- **SDK target**: Android 14 (API 34)
- Connessione internet richiesta per: ricerca barcode, ML Kit, pipeline LLM
- Permesso fotocamera richiesto per: scansione foto e barcode
- Permesso notifiche richiesto per: avvisi di scadenza

---

## 🧪 Testing

Il testing viene condotto in parallelo allo sviluppo, verificando ogni componente in isolamento nel momento in cui viene implementato. La suite di test utilizza **JUnit4**, integrato nativamente con Android Studio e l'intero stack Jetpack.

---

## 👥 Autori

- **Daniele Calisti** — [@Calisti-Daniele](https://github.com/Calisti-Daniele)
- **Silvio Grieco** — [@silviogrieco](https://github.com/silviogrieco)

---

## 📄 Licenza

Questo progetto è sviluppato a scopo accademico.
