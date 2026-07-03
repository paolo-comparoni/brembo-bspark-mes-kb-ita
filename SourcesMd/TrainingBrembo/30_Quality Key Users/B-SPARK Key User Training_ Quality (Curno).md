---
title: "Key User Training Quality Curno - Sessione Operativa e Sentencing"
source_file: "SourcesMd/TrainingBrembo/30_Quality Key Users/B-SPARK Key User Training_ Quality (Curno).md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [CURNO]
---

# Key User Training Quality Curno - Sessione Operativa e Sentencing

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\30_Quality Key Users\B-SPARK Key User Training_ Quality (Curno).docx`  
> Tipo: Word (.docx)

## Apertura training, obiettivi e perimetro qualità

- Sessione dedicata ai key user qualità con focus su tracciabilità, dichiarazione scarti e gestione ispezioni.
- Viene esplicitato il confronto tra processo precedente (AX) e processo target su Opcenter MES + reporting Power BI.
- Obiettivo dichiarato: portare i partecipanti dal risultato operativo finale ai dettagli di configurazione e backoffice.
- È richiesto ai partecipanti di interrompere la sessione in caso di dubbi terminologici per allineare linguaggio business e linguaggio MES.

## Architettura applicativa: ERP, MES, automazione e reporting

- Il MES è presentato come layer intermedio tra SAP (pianificazione/logistica), automazione di impianto e strumenti di reportistica.
- La piattaforma raccoglie eventi da linea e da SAP, li struttura e li rende disponibili per analisi operative e qualità.
- Viene chiarito che i report futuri saranno alimentati tramite Power BI con estrazione dal database Opcenter.

## Modalità di accesso e ambienti operativi

- Sono usati due ambienti principali: produzione qualità e ambiente di test/pilot.
- Login con credenziali Windows sugli URL forniti al team.
- Accesso tramite applicazione web enterprise con utenti profilati.
- In caso di errore licenza o autenticazione è previsto supporto amministrativo centralizzato.

## Due interfacce: quality manager (basic) e operatore bordo linea (repetitive)

- Interfaccia **Basic**: schermate standard Siemens per entità di prodotto e master data.
- Interfaccia **Repetitive**: applicazione touch (Mendix) ottimizzata per l'operatore di linea.
- La Basic è usata per sentencing, quality inspection e gestione parametri qualità.
- La Repetitive supporta dichiarazioni manuali, monitoraggio flusso, visualizzazione documenti e avanzamento operativo.

## Flusso operativo di quality: casi d'uso e percorso didattico

- Approccio didattico top-down: prima il risultato finale visibile all'utente qualità, poi i passaggi operativi che lo generano.
- Casi discussi: machining, washing, assembly e gestione batch/container in quarantena.
- Viene mostrata la sequenza: dichiarazione evento linea -> cattura dato MES -> valutazione qualità -> esito operativo.

## Dichiarazione scarti, quarantena e processo di sentencing

- Lo scarto può essere classificato come eliminazione immediata o candidato a valutazione qualità.
- I pezzi in dubbio vengono instradati in contenitori di quarantena.
- Il quality user applica azioni di sentencing:
  - rilascio in linea,
  - invio a rework,
  - conferma scarto definitivo.
- Le decisioni vengono tracciate nel sistema e propagate ai flussi successivi.

## Tracciabilità end-to-end: lotto, contenitore, ispezione

- L'operatività qualità è centrata sulla catena lotto -> contenitore -> operazione -> ispezione.
- Le quality inspection sono collegate al materiale/processo e possono pilotare blocchi o autorizzazioni di avanzamento.
- Ogni evento rilevante è storicizzato per audit e analisi difettosità.

## Configurazione backoffice qualità e responsabilità key user

- Il sistema è dichiarato altamente configurabile per prodotto, linea e regole qualità.
- I key user qualità devono governare:
  - setup regole di difettosità,
  - attributi ispezione,
  - modalità di input operatore,
  - criteri decisionali del sentencing.
- La parte finale del training entra nel dettaglio delle schermate di configurazione necessarie alla gestione autonoma.

## Chiusura sessione e prossime attività

- Confermata la necessità di completare i test di accesso agli ambienti.
- Confermata la continuità formativa su casi reali di impianto.
- Output atteso dal team qualità: uso operativo quotidiano + capacità di risoluzione eventi in quarantena.
