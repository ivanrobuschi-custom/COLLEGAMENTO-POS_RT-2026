# Best Practice - Organizzazione Multi-Punto Vendita

## Strategia di Ricognizione Preliminare
Per gli esercenti che gestiscono più Registratori Telematici (RT) distribuiti su diversi punti vendita, è fondamentale eseguire una **ricognizione fisica** prima di accedere al portale dell'Agenzia delle Entrate. Questo censimento preventivo riduce drasticamente il rischio di errori di associazione.

### Metodologia di Raccolta Dati
1.  **Scansione QR Code:** Per ogni RT, scansionare il QR Code applicato sul dispositivo in fase di installazione per recuperare la **Matricola RT** esatta.
2.  **Geolocalizzazione:** Associare univocamente ogni matricola all'**indirizzo fisico** dell'unità locale in cui è operativa.
3.  **Mapping POS:** Annotare quali POS (fisici o virtuali) sono fisicamente presenti e utilizzati in abbinamento a ciascun RT.

## Gestione Flussi Operativi Misti
È necessario mappare non solo i dispositivi fisici, ma anche le modalità operative software.

*   **Documento Commerciale on line:** Identificare se per alcune operazioni (es. prestazioni a domicilio, e-commerce, interventi esterni) viene utilizzata la procedura web del portale AdE invece dell'RT fisico.
*   **Prospetto Analitico (Snapshot Gennaio 2026):** Creare una tabella di raccordo che rispecchi la situazione reale operativa del mese di riferimento per l'avvio dell'obbligo.

### Esempio di Prospetto di Ricognizione

| Matricola RT / Procedura | Indirizzo Punto Vendita | Tipo POS | CF Acquirer | Denominazione Acquirer | Terminal ID (Fisici) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **99IE0012345** | Via Roma 10, Milano | Fisico | 12345678901 | NEXI PAYMENTS SPA | 87654321 |
| **99IE0012345** | Via Roma 10, Milano | Virtuale | 98765432109 | PAYPAL EUROPE | N/A |
| **DOC. COMM. ONLINE** | - | Fisico | 11223344556 | SUMUP LTD | 11223344 |

## Verifica Integrità Dati POS
Prima di procedere all'abbinamento, validare i dati in possesso confrontandoli con le evidenze ufficiali.

### Strumenti di Audit
1.  **Portale AdE:** Consultare la sezione **"POS non collegati"** o scaricare il file CSV **"Elenco Strumenti di Pagamento precompilato"** per verificare quali dispositivi risultano già censiti dai flussi bancari.
2.  **Fonti di Verità:**
    *   **Contratti di Convenzionamento:** Verificare i dati originali sottoscritti con l'Acquirer.
    *   **Report Mensili:** Controllare gli estratti conto o i report riepilogativi inviati dall'Acquirer per confermare Terminal ID e dati fiscali attuali.

## Alert per il Supporto (Troubleshooting)

### Variazioni Societarie Acquirer
**Attenzione:** I contratti di convenzionamento datati potrebbero non riflettere l'attuale ragione sociale o Codice Fiscale dell'Acquirer, a causa di **fusioni, acquisizioni o cambi di denominazione** avvenuti nel tempo.
*   **Azione:** Se i dati a portale differiscono dal vecchio contratto cartaceo, fare riferimento ai report mensili più recenti.

### Discrepanze Dati
In caso di disallineamento bloccante tra i dati presenti sul portale "Fatture e Corrispettivi" e la documentazione in possesso dell'esercente:
*   **NON procedere** con associazioni incerte.
*   **Contattare** immediatamente il servizio clienti dell'operatore finanziario (Acquirer) per ottenere i dati aggiornati e allineati con l'Anagrafe Tributaria.

***

  

[Suggerimenti pratici POS-rt](../Allegato%201_%20Suggerimenti%20pratici%20POS-rt.pdf)  

[Torna all'Indice Generale](../README.md)
