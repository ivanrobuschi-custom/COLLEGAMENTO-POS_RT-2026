---
layout: single
title: "Guida Operativa al Collegamento Logico tra POS per pagamenti elettronici e Registratore Telematico"
permalink: /GuidaOperativa_POS-RT/
sidebar:
  nav: "docs"
---

## Sintesi Architetturale
Il collegamento tra gli strumenti di pagamento elettronico (**POS**) e i Registratori Telematici (**RT**) è definito come un'associazione **logica** e non fisica. Questa operazione si effettua esclusivamente tramite l'interfaccia web disponibile nel portale "Fatture e Corrispettivi" dell'Agenzia delle Entrate.

Le tipologie di POS supportate sono:
*   **POS Fisici:** Dispositivi hardware tradizionali (o SoftPOS installati su smartphone/tablet) che permettono la lettura della carta.
*   **POS Virtuali:** Sistemi per gestire pagamenti via internet (e-commerce).

## Specifiche di Identificazione Dispositivi
Per effettuare correttamente il matching tra i dispositivi, è necessario reperire i seguenti identificativi univoci:

| Tipologia Dispositivo | Parametri Richiesti | Note |
| :--- | :--- | :--- |
| **POS Fisico** | **Terminal ID** + **Codice Fiscale/Denominazione Acquirer** | Il Terminal ID è spesso reperibile sullo scontrino del POS o nel contratto. Se l'esercente ha due contratti con Acquirer diversi ma usa un solo POS, deve registrare due collegamenti distinti. |
| **POS Virtuale** | **Codice Fiscale** e **Denominazione Acquirer** | Non è richiesto il Terminal ID. |
| **Server RT** | Matricola Server RT | Per i punti cassa collegati a Server RT, i POS vanno abbinati alla matricola del Server, non ai singoli punti cassa. |

## Workflow di Configurazione (Step-by-Step)
La procedura di configurazione deve essere eseguita dall'esercente (o delegato) all'interno dell'area riservata del portale "Fatture e Corrispettivi".

1.  **Accesso:** Entrare nella sezione "Gestione collegamenti".
2.  **Selezione RT:** Il sistema mostrerà l'elenco delle matricole degli **RT** attivi nel mese di riferimento. Selezionare l'RT da configurare.
3.  **Selezione POS:** Selezionare il **POS** da associare all'RT scelto. Il sistema proporrà i POS rilevati dai flussi mensili degli Acquirer.
4.  **Dati Obbligatori:** Per ogni collegamento è obbligatorio specificare l'**indirizzo dell'unità locale** presso la quale i due strumenti vengono utilizzati.
    *   *Nota:* Nel caso di selezione di POS fisici oggetto di precedenti collegamenti, l'indirizzo verrà acquisito automaticamente.

## Casi Particolari e Troubleshooting

### POS non in elenco o dati errati
Se il **POS** non compare automaticamente nell'elenco fornito dall'Agenzia:
*   L'esercente deve inserire **manualmente** i dati identificativi (**Terminal ID**, **Acquirer**).
*   Se l'esercente non è il titolare del POS (es. comodato d'uso atipico), deve dichiararne la "non titolarità" tramite l'apposita funzione. **Attenzione:** questa operazione è irreversibile.

### Attività Miste (es. Tabaccai)
*   **Vendite esonerate:** Se un POS è utilizzato *esclusivamente* per incassare vendite esonerate (es. tabacchi, lotterie), l'esercente deve dichiarare tale uso esclusivo per escluderlo dall'obbligo di collegamento.
*   **Uso Promiscuo:** Se il POS viene usato *anche* per vendite soggette a certificazione (es. cancelleria in tabaccheria), **il collegamento è obbligatorio**.

### Scambio Importo
È fondamentale che il software di cassa e il POS dialoghino tramite protocolli di "scambio importo". Questo garantisce che il dato di pagamento memorizzato dall'RT coincida esattamente con la transazione elettronica, evitando errori manuali e sanzioni.

## Termini e Scadenze a Regime
Per i **POS** attivati o modificati successivamente alla fase di avvio (gennaio 2026):
*   Il collegamento deve essere effettuato tra il **sesto giorno** e l'**ultimo giorno** del secondo mese successivo all'attivazione o variazione.
    *   *Esempio:* Un nuovo POS attivato il 19 marzo dovrà essere collegato tra il 6 ed il 31 maggio.

***

[GuidaOperativa_POS-RT](../GuidaOperativa_POS-RT.pdf)  

[Torna all'Indice Generale](../index.md)  
