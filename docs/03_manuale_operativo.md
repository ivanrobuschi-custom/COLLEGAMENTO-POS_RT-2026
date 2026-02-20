# Manuale Operativo - Procedure Portale AdE

## Percorso di Accesso
Per accedere alle funzionalità di collegamento, seguire rigorosamente il seguente percorso nel portale "Fatture e Corrispettivi":
1.  Effettuare il login al portale con le credenziali (SPID/CIE/CNS/Entratel).
2.  Accedere alla sezione **Corrispettivi**.
3.  Selezionare l'area **Gestore ed Esercente**.
4.  Nel menu a sinistra, cliccare sulla voce **Collegamento dispositivi - POS**.
5.  Selezionare la funzionalità **Gestione collegamenti**.

## Modalità di Collegamento Puntuale

### Procedura Semplificata (fino a 5 RT)
Il sistema propone automaticamente questa modalità agli esercenti con un numero di RT attivi pari o inferiore a 5.
*   **Interfaccia:** Visualizzazione a due colonne: elenco RT a sinistra, elenco POS a destra.
*   **Operazione:** Selezionare tramite checkbox un RT e uno o più POS da associare.
*   **Dettaglio:** Cliccando su **Collega**, si procede all'inserimento dell'indirizzo dell'unità locale (se non già presente).

### Procedura Standard (oltre 5 RT)
Riservata agli esercenti con un parco macchine superiore a 5 unità.
*   **Ricerca RT:** È necessario cliccare su **Cerca** (eventualmente usando filtri) per individuare il dispositivo RT o Server RT di interesse.
*   **Selezione:** Cliccare sulla freccia di selezione in corrispondenza dell'RT.
*   **Associazione POS:** Nella schermata successiva, cliccare su **Seleziona** nel riquadro "Strumento di Pagamento Elettronico da collegare" per aprire l'elenco dei POS disponibili e procedere all'abbinamento.

## Modalità di Collegamento Massivo
Questa funzionalità è ottimizzata per gestire volumi elevati di associazioni e permette di caricare fino a **1.000 elementi** per singolo file.

### Workflow
1.  **Accesso:** Selezionare la voce **Collegamento massivo** dal menu.
2.  **Download Template:** Scaricare il file CSV modello o, se disponibile, l'elenco precompilato dei POS ("Download file Elenco Strumenti di Pagamento precompilato").
3.  **Compilazione CSV:** Il file deve essere compilato rispettando rigorosamente i seguenti campi tecnici:
    *   **TipoAcquirer:** 'IT' o 'ES'.
    *   **IdentificativoAcquirer:** CF dell'Acquirer.
    *   **DenominazioneAcquirer:** Nome dell'Acquirer.
    *   **TipoPos:** '00' (fisico), '01' (virtuale).
    *   **TerminalId:** Matricola del POS (solo per fisici).
    *   **Convenzione:** Numero contratto.
    *   **Matricola:** Matricola RT o Server RT.
    *   **Operazione:** 'I' (inserimento collegamento), 'C' (cancellazione).
    *   **Ambulante:** '1' (sì), '0' (no).
    *   **Ubicazione:** Campi indirizzo (Provincia, Comune, Indirizzo, Civico, CAP) obbligatori se Ambulante='0'.
    *   **DataFine:** Obbligatoria solo per operazione 'C'.
4.  **Upload:** Caricare il file compilato tramite il pulsante **Scegli il file** e trasmettere con **Invia**.

## Gestione Inserimento Manuale (Troubleshooting)

### POS non presenti in elenco
Se un dispositivo non compare nelle liste automatiche (alimentate dai flussi bancari):
1.  Cliccare sul pulsante **Aggiungi POS**.
2.  Selezionare l'**Acquirer** dall'elenco.
3.  Inserire manualmente **Terminal ID** e dati del contratto.
4.  Il sistema marcherà questi inserimenti con fonte **"E"** (Esercente).

### Acquirer non censito
Se anche l'Acquirer non è presente in anagrafica:
1.  Nella schermata di ricerca Acquirer, cliccare su **Aggiungi Acquirer**.
2.  Inserire **CF** e **Denominazione**.
3.  Cliccare su **Salva** per aggiungerlo all'elenco con fonte **"E"**.

## Funzioni di Servizio e Storico

### Consultazione Esiti
Accedere a **Storico richieste massive** per verificare lo stato dell'elaborazione:
*   **IN CORSO:** Elaborazione non terminata.
*   **SCARTATA:** File con errori formali o sostanziali.
*   **ELABORATA:** Acquisizione completata con successo (o con errori parziali specificati nel file di esito).

### Gestione "POS non collegati"
La sezione **POS non collegati** elenca i dispositivi comunicati dagli Acquirer ma non associati ad alcun RT.
*   **Chiusura per non titolarità:** Utilizzare l'icona del lucchetto (**Chiusura**) per dichiarare che il POS non è nella disponibilità dell'esercente (es. restituito, dismesso).
*   **Uso Escluso:** La stessa funzione si usa per dichiarare che il POS è dedicato *esclusivamente* a operazioni esonerate (es. Tabacchi), escludendolo dall'obbligo di collegamento.
*   **Parametri:** Inserire "Motivo chiusura" e "Data fine utilizzo" (o data di riferimento per l'uso escluso).

***

[Allegato 2_ Manuale Operativo](../Allegato%202_%20Manuale%20Operativo.pdf)  
  
[Torna all'Indice Generale](../README.md) 
 