---
title: "Key User Training Line Operator Curno C1 - Sessione 2 Shop Floor e Prova Pratica - Analysis"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/Curno C1/Recording B-SPARK Key User Training Line Operator Curno (C1)-20260224_075541UTC-Meeting Recording.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [CURNO]
derived_from: "SourcesMd/TrainingBrembo/20_MES Line Operator/Curno C1/Recording B-SPARK Key User Training Line Operator Curno (C1)-20260224_075541UTC-Meeting Recording.md"
---

# Recording B-SPARK Key User Training Line Operator Curno (C1)-20260224_075541UTC-Meeting Recording_Analysis

## [CURNO] Agenda shop floor e perimetro operativo della seconda sessione

### Contenuto deterministico
- La seconda giornata riprende i concetti del giorno precedente e passa alla prova pratica.
- Il focus dichiarato è l'area produttiva / interfaccia operatore:
  - UI operatore
  - gestione ordini
  - start / pause / complete
  - consumi materiali
  - documenti
  - scarti componenti e prodotto finito
  - passaggi logistici successivi

### Tracciabilità
- Sezione origine: `Apertura della seconda giornata e agenda shop floor`

## [CURNO] Login, Work Center e lista ordini operativa

### Contenuto deterministico
- L'operatore accede con utenza generica, non personale.
- Landing page operativa: `Brembo Repetitive`.
- Se il terminale è associato a un solo Work Center, l'operatore va direttamente agli ordini.
- Se sono associati più Work Center/equipment, l'operatore deve selezionare il contesto corretto.
- La tile ordine espone:

```text
Work Order ID
Materiale finale + descrizione
Quantità startabile
Quantità in lavorazione
Quantità completata
Scrap quantity
```

### Regole di business
- La visibilità degli ordini è filtrata per Work Center/equipment associato alla postazione.
- In condizioni normali l'operatore non vede tutti gli equipment del plant, ma solo quelli pertinenti alla sua postazione.

### Tracciabilità
- Sezioni origine: `Interfaccia operatore, Work Center, lista ordini e composizione del gruppo`, `Avvio demo live: accesso, filtro ordini e selezione del Work Center`

## [CURNO] Composizione del gruppo e vincoli di avvio

### Contenuto deterministico
- Prima di lavorare un ordine bisogna inserire l'utenza nel gruppo macchina / equipment.
- L'aggiunta avviene tramite icona gruppo e pulsante `+`.
- Senza utenza nel gruppo non è possibile:
  - fare start;
  - dichiarare scarti;
  - entrare nell'operatività di dettaglio.

### Regole di business
- **Blocco hard**: lo start ordine è inibito in assenza di almeno un operatore nel team.
- Il gruppo è per equipment, quindi può essere riutilizzato per ordini diversi sullo stesso contesto macchina.

### Tracciabilità
- Sezioni origine: `Interfaccia operatore, Work Center, lista ordini e composizione del gruppo`, `Demo operatore: buffer, start ordine, quantità, consumi e scansione container`

## [CURNO] Start ordine, quantità e significato degli indicatori

### Contenuto deterministico
- Lo start può essere effettuato con quantità inferiore al pianificato.
- Esiste tolleranza configurata sull'ordine.
- La barra superiore dell'ordine distingue:

```text
Planned Quantity
Start / In lavorazione
Production Finish Good
Good Quantity
Scrap Quantity
```

- A livello icone:

```text
verde pieno / nuovo   -> ordine mai avviato
cerchio / pausa       -> ordine in pausa
attivo                -> ordine in esecuzione
```

### Regole di business
- Lo start è un'azione distinta dalla scansione materiali e distinta dal complete.
- La quantità completabile dipende dal consumo disponibile, non solo dalla quantità startata.

### Tracciabilità
- Sezioni origine: `Interfaccia operatore, Work Center, lista ordini e composizione del gruppo`, `Demo operatore: buffer, start ordine, quantità, consumi e scansione container`

## [CURNO] Casting e Cutting: regole forti di tracciabilità

### Contenuto deterministico
- Nel casting è obbligatoria la scansione dello stampo / numero seriale stampo.
- Lo stampo deve essere compatibile con l'ordine; altrimenti il sistema blocca l'operazione.
- Il casting ragiona per colate/strokes e per cavità.
- È possibile dichiarare il difetto su singola cavità; il difetto è poi considerato nel cutting.
- Nel cutting deve proseguire lo stesso lotto (`Original Batch`) lungo la catena.

### Regole di business
- **Blocco hard**: stampo non coerente con ordine -> stop operazione.
- **Regola di propagazione**: difetto cavità nel casting -> esclusione/scarto del pezzo corrispondente nelle fasi successive.
- **Regola di continuità**: Original Batch deve rimanere coerente lungo il flusso di fonderia.

### Tracciabilità
- Sezione origine: `Casting e Cutting: stampo, cavità, Original Batch e propagazione difetti`

## [CURNO] Tracciabilità materiali: Hard, Soft, No / autoconsumo

### Contenuto deterministico
- La schermata ordine mostra per ogni materiale la modalità di tracciabilità.
- Tipi espliciti:

```text
Hard -> scansione obbligatoria del container/barcode
Soft -> suggerimento sistema / consumo guidato
No   -> autoconsumo automatico
```

- L'autoconsumo può essere attivato tramite pulsante dedicato.
- Materiali `No` sono consumati automaticamente secondo logica FIFO sul buffer.
- Per i materiali `Soft` esiste la possibilità di consumo guidato a complete, ma il business ha deciso di imporre il consumo esplicito totale in molti casi.

### Regole di business ed eccezioni
- I materiali senza tracciabilità 1:1 non richiedono scansione container specifico.
- Il team sottolinea come best practice l'uso del consumo per container, per mantenere allineamento MES-SAP corretto.
- In training emerge un possibile errore di data migration quando materiali attesi `Hard` risultano `Soft`.

### Blocchi tecnici
```text
Hard  -> nessun completamento senza scansione
Soft  -> suggerimento / consumo assistito
No    -> consumo automatico FIFO da buffer
```

### Tracciabilità
- Sezioni origine: `Tracciabilità materiali, autoconsumo, staging call, scarti e chiusura Work Order`, `Demo operatore: buffer, start ordine, quantità, consumi e scansione container`, `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`

## [CURNO] Stage in Call, semaforo e rapporto con WM/SAP

### Contenuto deterministico
- Se il buffer è insufficiente, l'operatore lancia una `staging call` selezionando il buffer corretto.
- Il semaforo della chiamata materiale è per singolo materiale / singolo buffer, non globale.
- Stati del semaforo ricostruiti nella sessione:

```text
Verde  -> chiamata possibile / stock disponibile
Grigio -> chiamata inviata ma non ancora presa in carico
Giallo -> chiamata presa in carico da WM / task aperto
Rosso  -> errore / rifiuto / anomalia
```

- La stage call è agganciata al materiale che sta limitando la producibilità.

### Regole di business
- Una chiamata materiale non blocca altre chiamate su materiali o buffer diversi.
- WM / SAP elabora il task; il ritorno a verde richiede stock effettivamente reso disponibile in linea.

### Tracciabilità
- Sezioni origine: `Gestione del semaforo chiamata materiale e scarti di componente`, `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`

## [CURNO] Scrap componente, quarantena e scrap prodotto finito

### Contenuto deterministico
- Esistono due famiglie di scarto:
  1. scarto materiale di consumo / componente;
  2. scarto del prodotto finito della linea.
- Per entrambe le tipologie l'operatore può scegliere:

```text
Immediate Scrap -> da buttare via
Candidate       -> quarantena / valutazione qualità
```

- Nel caso `Candidate` si può aggiungere commento esplicativo.
- La quarantena genera container dedicato di non conformità / materiale fallito.
- Nel casting alcuni scarti sono sempre da rifusione e non usano la quarantena come caso principale.

### Regole di business
- La quarantena viene poi valutata dalla qualità per decidere rework / rilascio / scarto definitivo.
- Quando si scarta un componente consumato, la quantità disponibile e quindi completabile si riduce.

### Tracciabilità
- Sezioni origine: `Gestione del semaforo chiamata materiale e scarti di componente`, `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`

## [CURNO] Complete, Partial Complete, riuso container e AutoStart

### Contenuto deterministico
- Dopo i consumi l'operatore può:
  - dichiarare buoni (`Complete`)
  - dichiarare scrap / candidate
  - eseguire `Partial Complete`
- `Partial Complete` serve a chiudere temporaneamente un cassone non pieno, tipicamente a fine turno.
- Il partial complete stampa etichetta ma **non** invia chiusura a SAP.
- Il cassone resta in linea e può essere ripreso dal collega del turno successivo.
- È possibile riutilizzare un container parziale già esistente.
- Il sistema può essere configurato in `AutoStart` per riavviare automaticamente le quantità residue dopo un complete.

### Regole di business ed eccezioni
- **Regola**: `Complete` e `Partial Complete` sono azioni distinte.
- **Regola**: il partial complete non chiude il container a livello SAP.
- **Eccezione configurabile**: con AutoStart attivo i residui vengono restartati automaticamente; senza AutoStart l'operatore deve restartare manualmente.

### Tracciabilità
- Sezioni origine: `Tracciabilità materiali, autoconsumo, staging call, scarti e chiusura Work Order`, `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`
- Evidenze: `parshall complete`, `non manda nessuna informazione a SAP`, `autostart`

## [CURNO] Container Type, Generic Container e fattore limitante di capacità

### Contenuto deterministico
- Allo start può essere richiesto il `Container Type` da usare.
- Il Container Type limita la quantità massima inseribile nel contenitore.
- Esiste anche `Generic Container` come fallback senza limite specifico di capacità.
- Il training sconsiglia l'uso del Generic Container se è disponibile un tipo reale.

### Regole di business
- **Best practice**: usare il Container Type corretto per evitare errori di input e problemi di magazzino.
- **Regola**: la Max Quantity in complete / partial complete è limitata dalla `container capacity` e dall'eventuale quantità già presente nel container parziale.

### Blocchi tecnici
```text
Container Type -> capacità massima nota
Generic Container -> fallback, solo se master data assente / non disponibile
Max Quantity -> min(qty startata-consumabile, capacità residua container)
```

### Tracciabilità
- Sezioni origine: `Tooling, Container Type, Generic Container e limiti di capacità`, `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`

## [CURNO] Quantity bottleneck e production finish good

### Contenuto deterministico
- `Production Finish Good` rappresenta la quantità dichiarabile in base ai consumi effettivi.
- La UI mostra un'icona di `bottleneck` che identifica il materiale che in quel momento limita la producibilità.
- Se mancano materiali, l'operatore individua il bottleneck, prova a consumarlo oppure lancia stage call.

### Regole di business
- La producibilità è calcolata sul materiale limitante, non sulla sola quantità ordine.
- Il bottleneck è un aiuto decisionale operativo per sapere quale materiale blocca complete/scrap.

### Tracciabilità
- Sezione origine: `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`

## [CURNO] Quality Inspection: configurazione, frequenze e blocco operativo

### Contenuto deterministico
- In training vengono mostrate anche le entità di configurazione qualità.
- Tipi di characteristic:

```text
Attributive -> OK / Not OK
Variable    -> misura con nominale e tolleranze
Visual      -> localizzazione grafica del difetto su immagine
```

- Una inspection definition definisce anche la frequenza del controllo:

```text
100%
Time Based
Unit Based
Part Based
```

- In Italia, per il go-live, l'ipotesi principale riportata è partenza con controlli `100%`.
- Le quality inspection sono legate al codice prodotto e vengono ereditate dall'ordine tramite routing/BOP.
- Quando una quality inspection è attiva:
  - il pulsante `show quality` diventa arancione;
  - i pulsanti `complete` e `scrap` vengono disabilitati fino all'esecuzione del controllo.
- Le quality data restano nel MES e non vengono inviate a SAP.

### Regole di business
- **Blocco hard**: nessuna dichiarazione finché la quality inspection richiesta non è compilata.
- Le inspection possono essere importate massivamente; la modifica manuale è possibile ma tipicamente eccezionale.

### Blocchi tecnici
```text
Characteristic:
- attributive
- variable (nominale, lower, upper, UoM)
- visual

Inspection frequency:
- 100%
- time based
- unit based
- part based
```

### Tracciabilità
- Sezioni origine: `Configurazione Quality Inspection: caratteristiche, frequenze ed ereditarietà`, `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`

## [CURNO] Documenti, LinkerSys e differenza tra UI operatore e client amministrativo

### Contenuto deterministico
- I documenti sono raggruppati per origine: operation, material, machine/workcenter.
- Possono essere visualizzati in preview, fullscreen, download.
- È prevista integrazione con `LinkerSys` per aprire lista documenti in tab browser separato.
- Il training esplicita la differenza tra:
  1. UI reparto / `Repetitive` per dichiarazioni operative;
  2. schermate Opcenter più amministrative / d'ufficio per consultazione anagrafiche e ordini.

### Regole operative
- I documenti MES sono subito visibili nel contesto ordine/operazione.
- I documenti LinkerSys restano consultazione esterna e richiedono navigazione su tab separato.

### Tracciabilità
- Sezione origine: `Documenti, LinkerSys, stage call, quantity bottleneck e qualità bloccante`

## [CURNO] Tooling, feedback formativo e localizzazione UI

### Contenuto deterministico
- Viene introdotto il concetto di `tool` per fonderia / machining / casting: stampi e utensili da scansionare o identificare perché obbligatori per determinate produzioni.
- I partecipanti chiedono più pratica hands-on e training più vicino ai casi reali del proprio reparto.
- Viene chiarito che la UI di default nasce in inglese ma le label possono essere tradotte e adattate alla terminologia usata in Brembo / AX.
- È richiesto un lavoro di mapping terminologico per rendere la UI più comprensibile agli operatori.

### Regole operative
- Le traduzioni non sono totalmente standardizzate out-of-the-box: servono feedback dei key user per allinearle ai termini di fabbrica.
- L'efficacia del training dipende dal collegare i concetti MES alle azioni concrete che i key user dovranno poi far eseguire agli operatori.

### Tracciabilità
- Sezione origine: `Tool di fonderia, test di apprendimento e feedback formativo`
