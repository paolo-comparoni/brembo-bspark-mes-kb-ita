# 01_Overview

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\20_MES Line Operator\01_Overview.pptx`  
> Tipo: PowerPoint (.pptx) · Slide: 17


## Slide 1: BENVENUTI IN OPCENTER

- BENVENUTI IN OPCENTER

- PREPARARE LE PERSONE ALL'ECCELLENZA OPERATIVA

- Febbraio 2026

- OPCENTER MES TRAINING - OVERVIEW


## Slide 2: Modalità di training

- Brembo Rollout Italia

- 2

- Modalità di training

- OPCENTER MES TRAINING - OVERVIEW

- 02. Italy Roll-Out

- Quali documenti avrò a disposizione

- General | Ishango_Learning HUB | Microsoft Teams

- at

- Navigator_Training Material

- A chi posso chiedere supporto?

- Brembo – ISHANGO_KU INFO_ITALY_W1

- plus

- La partecipazione alle sessione di training ricevute è da ritenersi Obbligatoria


## Slide 3: Cos’è il MES

- Opcenter è il software MES (Manufacturing Execution System) che gestisce e monitora il processo produttivo in tempo reale, dal rilascio dell'ordine alla realizzazione del prodotto finito.
- Trasforma gli ordini dell’ERP (SAP) in istruzioni operative per personale e macchine e riporta all’ERP le informazioni di produzione.

- Brembo Rollout Italia

- 3

- Cos’è il MES

- OPCENTER MES TRAINING - OVERVIEW


## Slide 4: Vantaggi

- Pianificazione chiara delle operazioni
- Monitoraggio in tempo reale
- Tracciabilità
- Controllo Qualità
- Riduzione degli errori
- Acquisizione dati semplificata
- Meno carta e burocrazia
- Istruzioni digitali chiare
- Riconoscimento della produttività

- Brembo Rollout Italia

- 4

- Vantaggi

- OPCENTER MES TRAINING - OVERVIEW


## Slide 5: I livelli della produzione

- 👉 LIVELLO 4: ERP - PIANIFICAZIONE
- Direzione, pianificazione, supply chain, amministrazione.
- Decidono cosa produrre, quanto e quando, in base a ordini, costi e strategia.
- 👉 LIVELLO 3: MES – COORDINAMENTO
- Produzione, qualità, manutenzione, responsabili di reparto.
- Trasformano le decisioni aziendali in azioni concrete in produzione e monitorano che tutto avvenga come stabilito.
- 👉 LIVELLI 1–2: OPERATORI E AUTOMAZIONE - ESECUZIONE
- Operatori di linea, macchine e impianti.
- Eseguono fisicamente il processo produttivo.

- Brembo Rollout Italia

- 5

- I livelli della produzione

- OPCENTER MES TRAINING - OVERVIEW


## Slide 6: Come il MES «conosce» la produzione

- Il Plant Modeling è la rappresentazione della struttura fisica della produzione («dove avvengono le cose»). Definisce la gerarchia degli asset fisici: sito, aree di produzione, linee, celle di lavoro e singole macchine o postazioni manuali.
- Il sistema Opcenter riflette la struttura della produzione attraverso la gerarchia:
- Enterprise: il gruppo Brembo.
- Sito produttivo: Lo stabilimento specifico (es. «Mapello» o «Curno»).
- Production Lines: Le linee di produzione all’interno dello stabilimento (es. «Casting D Line»).
- Work Center / Equipment: Le singole unità produttive, stazioni di lavoro, buffer, ecc.

- Il Process Modeling è la definizione logica di come un prodotto deve essere realizzato («come avvengono le cose»).
- Definisce:
- Le sequenze di operazioni (BOP)
- La lista dei materiali necessari per ogni fase (BOM)
- I tool necessari
- Le istruzioni (Work Instructions) per gli operatori
- I controlli di qualità da eseguire.
- …

- Brembo Rollout Italia

- 6

- Come il MES «conosce» la produzione

- OPCENTER MES TRAINING - OVERVIEW


## Slide 7: Come il MES «conosce» la produzione

- Il layout dello stabilimento viene configurato manualmente in Opcenter e rispecchia la struttura produttiva reale.
- Nei Work Center gli operatori eseguono le attività di produzione coadiuvati e guidati dal MES. Ogni attività è legata a uno specifico Work Order (ordine di produzione/lavorazione).

- Brembo Rollout Italia

- 7

- Come il MES «conosce» la produzione

- OPCENTER MES TRAINING - OVERVIEW


## Slide 8: Materiali

- Brembo Rollout Italia

- 8

- Materiali

- OPCENTER MES TRAINING - OVERVIEW

- L’Anagrafica dei Materiali, che contiene le definizioni dei materiali, viene ricevuta tramite SAP.
- All’Anagrafica dei materiali sono associati tutti i lotti relativi a:
- Materie prime
- Prodotti finiti
- Semilavorati
- Materiali di consumo

**Note del relatore:**

L’inserimento manuale, seppur possibile, non è una buona pratica perché crea disallineamenti tra i sistemi.


## Slide 9: Container

- Brembo Rollout Italia

- 9

- Container

- OPCENTER MES TRAINING - OVERVIEW

- I lotti vengono mossi all’interno dello stabilimento attraverso i Container.
- Ogni container deriva da un Container Type (Modello di Contenitore) da cui eredita le caratteristiche, tra cui: la quantità massima di unità dello specifico materiale che può contenere.
- L’Anagrafica dei Container viene ricevuta tramite SAP.
- Il Container corrisponde alla Handling Unit in SAP.

**Note del relatore:**

L’inserimento manuale, seppur possibile, non è una buona pratica perché crea disallineamenti tra i sistemi.


## Slide 10: Container

- Brembo Rollout Italia

- 10

- Container

- OPCENTER MES TRAINING - OVERVIEW

- I lotti di materiale necessari alla produzione, quando richiesto, vengono recapitati in contenitori presso il buffer (PSA/Staging Area) associato al Work Center.
- Il buffer corrisponde alla definizione PSA in SAP.
- I lotti vengono «consumati» tramite la lettura del codice associato (scansione con barcode reader). Nel momento della scansione, il lotto viene "consumato" nel sistema, aggiornando le giacenze in tempo reale.
- Il MES verifica istantaneamente se quel lotto è quello corretto per l'ordine in corso (evitando errori).
- Durante la lavorazione, i nuovi lotti prodotti vengono  progressivamente caricati in nuovi contenitori.
- Una volta raggiunta la quantità stabilità, il MES stampa automaticamente un'etichetta per il nuovo contenitore e lo dichiara pronto per la fase successiva.


## Slide 11: Buffer

- Brembo Rollout Italia

- 11

- Buffer

- OPCENTER MES TRAINING - OVERVIEW

- Per consumare il materiale associato al contenitore, è necessario che sia presente in uno dei buffer associati al Work Center in cui viene eseguita l'operazione.
- La funzionalità «Verifica Disponibilità» (Availability Check), che verrà introdotta più avanti, consente di verificare se la quantità di materiale disponibile nel buffer è sufficiente per la produzione richiesta.
- Se la quantità non è sufficiente, è possibile eseguire una "Richiesta Materiale" a SAP per richiedere il materiale.
- I buffer vengono creati manualmente in Opcenter.


## Slide 12: Bill of Materials (BOM) / Distinta Base

- Brembo Rollout Italia

- 12

- Bill of Materials (BOM) / Distinta Base

- OPCENTER MES TRAINING - OVERVIEW

- La Bill of Materials (BOM), o distinta base, rappresenta l'elenco gerarchico di tutte le materie prime, componenti e semilavorati necessari per la fabbricazione di un prodotto finito.
- Ogni voce specifica la quantità esatta richiesta per completare l'unità produttiva.
- Strutturata tipicamente ad 'albero', la BOM guida il processo di prelievo e consumo dei materiali, garantendo che ogni componente sia correttamente tracciato durante le fasi di assemblaggio.


## Slide 13: Bill of Process (BOP) - Distinta dei Processi

- Le As-Planned BOP (Processi Pianificati) sono strutture che contengono uno o più processi raggruppati gerarchicamente per definire l'esecuzione di specifiche attività manifatturiere, suddivise in Operazioni.
- All’interno del BOP si definiscono le singole fasi, i macchinari necessari e i materiali di input/output.
- La BOP nel MES corrisponde al Routing di SAP.

- Brembo Rollout Italia

- 13

- Bill of Process (BOP) - Distinta dei Processi

- OPCENTER MES TRAINING - OVERVIEW


## Slide 14: Operazioni

- Ogni Operazione è composta da una serie di Attività correlate, da svolgere durante il ciclo produttivo.
- Per procedere all'esecuzione, l'operatore deve avviare l'operazione nel sistema e dichiarare la quantità di pezzi da lavorare.
- Una volta completate le attività per una determinata quantità (incluse quelle avviate parzialmente), l'operazione viene registrata come Completata.
- Se l’Operazione è l’ultima della BOP, la quantità prodotta viene automaticamente caricata nel container di uscita.

- Brembo Rollout Italia

- 14

- Operazioni

- OPCENTER MES TRAINING - OVERVIEW


## Slide 15: Work Order – Ordine di Produzione

- Il punto di partenza nell'esecuzione del processo di produzione è il Work Order, che collega tutte le informazioni.
- Solitamente i Work Order vengono trasmessi al MES da SAP, secondo il piano di produzione e definiscono cosa produrre: quantità, materiali necessari, attrezzi, istruzioni operative e controlli qualità.
- Per iniziare la produzione richiesta, l’operatore avvia (Start) il Work Order ed al termine ne registra la conclusione, permettendo il backflush (scarico automatico dei consumi) dei dati verso SAP.

- Brembo Rollout Italia

- 15

- Work Order – Ordine di Produzione

- OPCENTER MES TRAINING - OVERVIEW


## Slide 16: Team Management - Gestione del Gruppo di Lavoro

- Durante il processo produttivo, ogni operatore viene assegnato a un Team (Gruppo di lavoro) specifico.
- Prima di iniziare le proprie attività, l'operatore si unisce al Team specifico.
- I team sono flessibili e creabili "on the fly" (L'operatore può essere associato all'operazione in tempo reale , es. per operazioni che richiedono due persone). Un membro del team può avviare/mettere in pausa l'operazione per l'intero gruppo.
- Al termine delle attività, l'operatore lascia il Team.

- Brembo Rollout Italia

- 16

- Team Management - Gestione del Gruppo di Lavoro

- OPCENTER MES TRAINING - OVERVIEW


## Slide 17: Grazie per l’attenzione.

- Annalisa Casciaro

- Technical Development
- Software Development Specialist

- Grazie per l’attenzione.

- OPCENTER MES TRAINING - OVERVIEW
