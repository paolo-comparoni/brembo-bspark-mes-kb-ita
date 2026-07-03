---
title: "Training Operatori di Linea Mapello (PDF)"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/2026-04-23 Materiale per Training Line Operator/Training-Operatori-Linea-Mapello (PDF).md"
project: "Brembo B-Spark"
scope: "Operational_Training_Material"
plants: [MAPELLO]
---

# Training Operatori di Linea Mapello (PDF)

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\20_MES Line Operator\2026-04-23 Materiale per Training Line Operator\Training-Operatori-Linea-Mapello.pdf`  
> Tipo: PDF · Pagine: 39


## Pagina 1

1


## Pagina 2

LINE OPERATOR TRAINING

OPERATORI DI LINEA


## Pagina 3

INTRODUZIONE

AGENDA

In questa lezione analizzeremo alcuni casi d’uso reali per dimostrare il
funzionamento del sistema e le operazioni.

➢

USE CASE 1 - CASTING: Ciclo completo dell’ordine di lavorazione
utilizzando a modello il Casting.

➢

USE CASE 2 - CUTTING: Esecuzione di un ordine di Cutting con focus
sulla dichiarazione dei co-product.

➢

BACK OFFICE: Spiegazione delle aree del sistema dove è possibile

monitorare anagrafica, ordini di lavorazione, ristampare etichette.
➢

DOMANDE E RISPOSTE

3


## Pagina 4

4

USE CASE 1: CASTING

ACCESSO AL SISTEMA

Repetitive Mapello: https://it-qlt.mes.brembo.com/situi/Mapello/DSBasic.BremboRepetitive_Mapello


## Pagina 5

5

USE CASE 1: CASTING

ACCESSO AL SISTEMA

Sulla postazione in linea di produzione il login avverrà tramite lettura badge.
L’accesso con le credenziali, username e password, sarà riservato agli operatori di back-office.


## Pagina 6

6

USE CASE 1: CASTING

USE CASE 1: CASTING

A scopo dimostrativo verrà presa a modello l’esecuzione di un ordine di lavorazione nell’area di Casting.
Le operazioni elencate sono in larga parte comuni anche alle altre aree.


## Pagina 7

7

USE CASE 1: CASTING

INTRODUZIONE

SELEZIONE
WORK CENTER

SELEZIONE E
AVVIO WORK
ORDER

CHIAMATA
MATERIALI

VALIDAZIONE
STAMPO

CONSUMO
MATERIALI

ISPEZIONE
QUALITÀ

DICHIARAZIONE
DI PRODUZIONE

DICHIARAZIONE
DIFETTI

Alcune operazioni che richiedono l’integrazione con SAP/EWM (es. flusso materiali
da un’area all’altra) non potranno essere mostrate.
Le schermate del sistema mostrate in questa presentazione saranno in inglese,
mentre in produzione saranno disponibili in italiano e con la terminologia
comunemente utilizzata in Brembo.

ATTIVITÀ NON
PRODUTTIVE

CHIUSURA
ORDINE


## Pagina 8

8

USE CASE 1: CASTING

SELEZIONE DEL WORK CENTER

La «Repetitive» è la pagina che accoglie l’operatore
dopo il login e mostra gli Equipment associati alla
postazione di lavoro «Work Center».
Se il terminale è associato a una sola macchina, il
sistema visualizzerà direttamente la lista degli
ordini di lavorazione per quella macchina nella
pagina «Operator Landing».
Se il PC gestisce più macchine, il sistema
visualizzerà la pagina «Equipment Selection»,
dove l'operatore dovrà selezionare il Work Center
specifico (es. GUGCL231) su cui intende operare
dalla lista proposta e cliccare su "Save".

NOTA: In condizioni di normale produzione solo un
ordine di lavorazione può essere attivo sul Work
Center (salvo macchine in grado di produrre in
parallelo).
Durante il training questo limite è disabilitato per
permettere di esercitarsi.
NOTA: Nel sistema attuale non esiste ancora l’associazione Work
Center/Equipment, per cui tutte le postazioni di lavoro sono tutti visibili.


## Pagina 9

9

USE CASE 1: CASTING

DATI PER GLI STUDENTI

Mentre gli istruttori spiegano, i partecipanti provano ad

eseguire le stesse operazioni in parallelo.


## Pagina 10

11

USE CASE 1: CASTING

SELEZIONE DELL’ORDINE DI LAVORAZIONE

Ogni macchina ha il suo gruppo di Lavoro.
Prima di avviare qualsiasi Work Order (ordine
di produzione) o operazione sulla macchina, è

fondamentale che l'operatore si registri
correttamente nel gruppo di lavoro (Team)
associato alla postazione. Questa operazione
garantisce la corretta tracciabilità delle attività
e la sicurezza del processo.

Scansione Badge: La modalità più rapida

Il sistema non permette di avviare o gestire

consiste nello scansionare il proprio badge

ordini se non c'è almeno un operatore

(barcode); il sistema riconoscerà

registrato nel team della stazione.

automaticamente l'utente e lo aggiungerà al
gruppo di lavoro


## Pagina 11

12

USE CASE 1: CASTING

SELEZIONE DELL’ORDINE DI LAVORAZIONE

Il sistema MES è sincronizzato con il
gestionale centrale ERP «SAP».
Quando l'ufficio pianificazione approva e
rilascia un ordine di produzione, tutte le
informazioni necessarie vengono
trasmesse alla postazione di lavoro.
In termini pratici, troverete l'ordine già
pronto sul monitor con tutti i dettagli
necessari per iniziare: il tipo di
materiale, le quantità da produrre e la
sequenza delle operazioni da seguire.


## Pagina 12

13

USE CASE 1: CASTING

STATO DELL’ORDINE DI LAVORAZIONE

I TRE NUMERI: Ogni riquadro mostra tre quantità:
•

Pezzi ancora da avviare

•

Pezzi in lavorazione

•

Pezzi completati.

STATO OPERAZIONE:
•

Stato iniziale: l’operazione non è ancora pronta per l’avvio (dipendenze
precedenti non soddisfatte).

•

Operazione pronta per l’esecuzione: tutte le dipendenze (es. AfterEnd o
AfterStart) sono state completate con successo.

•

Operazione attualmente in esecuzione: il lavoro su questa fase è stato
avviato dall’operatore.

•

Esecuzione parziale: tipico di produzioni serializzate o a lotti flessibili dove solo
parte della quantità è stata lavorata.

•

Stato di blocco preventivo: impostato spesso automaticamente (es. per
dichiarazione di non conformità) per fermare il flusso al raggiungimento di
questa fase.

•

Operazione conclusa con successo: tutti i task previsti per la fase sono
terminati.

•

Operazione non eseguita; si verifica se una fase opzionale viene saltata o se
l’ordine viene annullato (abort) o modificato escludendo tale fase.

•

Segnala la presenza di una Non-Conformità aperta associata all’operazione.

•

Segnala che è necessaria o imminente un’ispezione di qualità.

E’ possibile ordinare la visualizzazione dei riquadri in base allo stato.


## Pagina 13

14

USE CASE 1: CASTING

AVVIO DELL’ORDINE DI LAVORAZIONE

Visualizzazione dettagli ordine di lavorazione.


## Pagina 14

USE CASE 1: CASTING

AVVIO DELL’ORDINE DI LAVORAZIONE

15


## Pagina 15

16

USE CASE 1: CASTING

AVVIO DELL’ORDINE DI LAVORAZIONE – CON CONTENITORE PARZIALE

Se all’avvio di un ordine il sistema rileva la presenza di
un container parziale, il MES segnala all'operatore
che per quell'ordine esiste un cassone in sospeso e
suggerisce di completare quello per primo.
Questa funzione è pensata per gestire i cambi turno:
l'operatore che entra nel turno può "agganciarsi" al
cassone lasciato a metà dal collega del turno

precedente, terminare il cassone e generare l'etichetta
definitiva.


## Pagina 16

17

USE CASE 1: CASTING

AVVIO DELL’ORDINE DI LAVORAZIONE - CON CONTENITORE PARZIALE

Se il supervisore decide che quel cassone non deve
essere ulteriormente riempito (ad esempio per un
cambio materiale urgente), l'operatore può utilizzare la
funzione Close Partial Container per chiuderlo
definitivamente con la quantità ridotta attuale e inviare
l'informazione a SAP


## Pagina 17

18

USE CASE 1: CASTING

AVVIO DELL’ORDINE DI LAVORAZIONE

Avvio ordine di lavorazione (senza contenitori parziali già presenti)

NOTA: Se si cerca di
avviare una
quantità superiore
a quella pianificata,
il sistema potrebbe
bloccare o
permettere l'avvio
in base alla
tolleranza
impostata in fase di
pianificazione.


## Pagina 18

19

USE CASE 1: CASTING

AVVIO DELL’ORDINE DI LAVORAZIONE

Stato e Avanzamento
Questa parte mostra i dati dell'ordine e le
quantità prodotte:
• Final Material & Description: Visualizza il
codice tecnico e la descrizione del prodotto
in lavorazione.
• Production Finish Good: Indica la quantità
massima che puoi completare in base ai
materiali effettivamente
consumati/scansionati.
• Good Quantity (Buoni): Il totale dei pezzi
conformi già completati per l’operazione.
• Scrap Quantity (Scarti): Il totale dei pezzi
dichiarati scarti o difettosi.

Visualizzazione ordine avviato.


## Pagina 19

USE CASE 1: CASTING

AVVIO DELL’ORDINE DI LAVORAZIONE

Quantità Richiesta: il totale necessario
per completare l'ordine.
Quantità Disponibile/Mancante: il
sistema evidenzia eventuali mancanze
con icone di avviso per segnalare la
necessità di nuovi approvvigionamenti

20


## Pagina 20

21

USE CASE 1: CASTING

CHIAMATA MATERIALI
Semaforo di stato chiamata:
• Grigio: inviata ma non presa in carico.
• Giallo: presa in carico dal magazzino.
• Verde: disponibile.
• Rosso: errore o movimentazione bloccata.


## Pagina 21

22

USE CASE 1: CASTING

VALIDAZIONE STAMPO

Ogni stampo è identificato da un numero seriale
univoco.

Prima di produrre, l'operatore deve validare lo stampo
inserendo o scansionando il suo numero seriale.
Il sistema controlla abbinamento ordine di
lavorazione/stampo per evitare errori.

Ogni stampo ha un contatore di utilizzi (Strokes
Counter) che viene incrementato ad ogni colata,
permettendo di tracciarne l’usura e sostituirlo per
mantenere la qualità della produzione.


## Pagina 22

USE CASE 1: MACHINING

CONSUMO MATERIALI

Tracciabilità «Hard»: L’operatore deve scansionare o inserire
manualmente l'identificativo del barcode. Con un'unica azione,
il sistema acquisisce automaticamente codice materiale, lotto

e quantità. Il materiale scansionato viene "scalato" dal buffer
di linea e associato alla produzione in corso.
In caso di materiali "Hard Traced", il sistema bloccherà la
dichiarazione finale di produzione se tutti i componenti
obbligatori non sono stati scansionati correttamente.
Tracciabilità «Soft»: Scansione opzionale (consigliata),
altrimenti il sistema consuma quel materiale con logica FIFO al
momento della chiusura.
Nessuna tracciabilità: L'operatore visualizza i materiali ma
non deve inserire dati manualmente. Il sistema esegue il
consumo automatico in base alle quantità prodotte dichiarate
al termine dell'operazione.

23


## Pagina 23

USE CASE 1: CASTING

DICHIARAZIONE DI PRODUZIONE

Pulsante COMPLETE per dichiarare la produzione dei pezzi
buoni.
Si seleziona il Container Type (tipo di imballo) corretto per
istruire SAP sui materiali di confezionamento (coperchi, layer).
Viene attribuito l’«Original Batch» (lotto di colata) che
garantirà la tracciabilità totale fino a fine processo. Questo
identificatore è cruciale poiché il sistema bloccherà qualsiasi
tentativo di mescolare lotti diversi, all’interno dello stesso
cassone, nelle fasi di lavorazione successive.

24


## Pagina 24

USE CASE 1: CASTING

SELEZIONE DELL’ORDINE DI LAVORAZIONE

25


## Pagina 25

26

USE CASE 1: CASTING

DICHIARAZIONE DIFETTI

Pulsante Declare NC per aprire una Non-Conformità.
• Scarto Immediato
• Quarantena
• Scarto di Cavità: È possibile scartare una singola cavità della
mold segnandola con una "X". Il sistema erediterà questo scarto
nella fase successiva (Cutting), dove il pezzo sarà eliminato
automaticamente.

Quando l'operatore del
taglio «consumerà» il
ragno nella fase di
cutting, il MES genererà
automaticamente lo scarto
per le cavità che erano
state marcate con la X.


## Pagina 26

USE CASE 1: CASTING

ATTIVITÀ NON PRODUTTIVE

Le attività non produttive (N-P Activities) sono compiti che, pur essendo necessari, non
contribuiscono direttamente alla produzione fisica dei pezzi.
Includono mansioni come la pulizia dell'area di lavoro, la manutenzione degli utensili, le
attività di formazione o il setup delle macchine.
L'operatore interagisce con queste attività tramite la Operator Landing Page seguendo
questi passaggi:
• Accede tramite il pulsante N-P Activities sulla barra dei comandi.
• Sceglie una o più attività dalla lista preimpostata.

• Può associare l'attività non produttiva a un contesto specifico, ad esempio collegandola
a un determinato ordine di lavorazione, a un'operazione, a una macchina o a un
cassone.
• Il sistema registra l'ora di inizio. Se necessario può inserire anche attività svolte nel
passato, se non sono state registrate al momento dell'effettivo inizio.
• Al termine, seleziona l'attività e la dichiara come completata, registrando così la data e
l'ora correnti nel log di sistema

27


## Pagina 27

28

USE CASE 1: CASTING

CHIUSURA ORDINE

Chiusura Totale: L'ordine passa in stato "Complete".
Chiusura Parziale: Utile a fine turno per stampare un'etichetta
temporanea e permettere al collega subentrante di completare il

cassone.
Shadow Movement: Una volta completato, il MES informa SAP che
sposta virtualmente il materiale verso la fase successiva (es. Cutting)
senza interventi manuali.


## Pagina 28

29

USE CASE 2: CUTTING

USE CASE 2: CUTTING

In questo use case eseguiremo un ordine di cutting.
Le slide contengono un focus sulle specificità di questa area dal punto di vista MES.


## Pagina 29

30

USE CASE 2: CUTTING

USE CASE 2: CUTTING – DICHIARAZIONE DEI COPRODOTTI

Parliamo di coprodotti (co-products) quando da un unico
materiale di input si ottengono più prodotti distinti
durante la stessa operazione.
E’ il caso del cutting dove da una «mold» si possono
ottenere più prodotti, ad esempio semi-pinza destra e
semi-pinza sinistra.


## Pagina 30

31

USE CASE 2: CUTTING

USE CASE 2: CUTTING – DICHIARAZIONE DEI CO-PRODUCT

L'operatore preme Complete nella barra laterale destra.
Nell'interfaccia di completamento, il sistema visualizza distintamente i codici di tutti i
prodotti previsti, ad es. il prodotto principale 20E93800 e coprodotto 20E93900.
• L'operatore deve inserire la quantità di pezzi buoni prodotti per ciascun
codice.
• È possibile dichiarare anche eventuali scarti specifici per il co-prodotto
selezionando la relativa voce nel pannello dei difetti di qualità.

Non è obbligatorio seguire un ordine fisso (si può dichiarare prima il prodotto
principale e poi il coprodotto o viceversa. Ma non è possibile completare interamente
la produzione del prodotto principale se rimangono quantità residue di coprodotto
non dichiarate; il sistema impone la gestione di entrambi i flussi per mantenere
l'allineamento con SAP.


## Pagina 31

32

BACK-OFFICE LINEA

BACK-OFFICE DI LINEA


## Pagina 32

BACK-OFFICE LINEA

DS BASIC: APPLICAZIONI DI SUPERVISIONE

➢ Print History
➢ Work Orders
➢ Work Order in Progress
➢ Container Types
➢ Buffer

DSBasic Mapello: https://it-qlt.mes.brembo.com/sit-ui/mapello/DSBasic.Siemens_OPC_EXDSBasic/#/screen/home.homeCard

33


## Pagina 33

34

BACK-OFFICE LINEA

WORK IN PROGRESS APP

Print History
Questa funzionalità permette di monitorare e gestire l'attività di etichettatura del sistema.
•

L'attività principale per un supervisore è la consultazione dello storico delle stampe che

consente la ristampa di etichette (CDI) smarrite o danneggiate.


## Pagina 34

BACK-OFFICE LINEA

WORK ORDERS

Work Orders
Permette di visualizzare lo stato degli
ordini di lavorazione.

•

Visualizzare la lista degli ordini di
lavorazione che sono stati ricevuti.

•

Il supervisore può visualizzare la
genealogia as-built.

•

La lista delle quality inspections.

•

Lista non-conformances.

•

Cancellare gli ordini non più necessari
(abort)

35


## Pagina 35

BACK-OFFICE LINEA

WORK ORDER IN PROGRESS

Work Order in Progress (WIP)
È l'applicazione dedicata al monitoraggio
in tempo reale dell'avanzamento della

produzione.
•

Consente di vedere quali ordini sono
in lavorazione, la loro percentuale di
completamento e su quali macchine
specifiche si trovano.

•

Il supervisore monitora le quantità
effettive prodotte rispetto a quelle
scartate o messe in quarantena.

•

Permette di prendere decisioni
repentine per ottimizzare il flusso o

ripianificare le operazioni per evitare
tempi morti.

36


## Pagina 36

37

BACK-OFFICE LINEA

CONTAINER TYPES

Container Types
Definisce le caratteristiche del contenitore, come la capacità massima di pezzi per ogni
materiale compatibile e la proprietà di riutilizzabilità.


## Pagina 37

38

BACK-OFFICE LINEA

BUFFER (PRE-MACCHINA)

Buffer
Aree di stoccaggio nell’impianto.
Il supervisore:
•

Può creare, modificare e cancellare i buffer definiti per l'impianto.

•

Può cambiare lo stato del buffer.

•

Può visualizzare quali MTU sono contenute in un determinato buffer e aggiungerne di nuove
manualmente se necessario


## Pagina 38

39

TRAINING LINE OPERATOR - MAPELLO

DOMANDE E RISPOSTE

Spazio alle vostre domande.


## Pagina 39

TRAINING LINE OPERATOR - MAPELLO

Grazie per l’attenzione.
EMANUELE MERLO
