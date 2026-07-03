---
title: "BackOffice MES - Materiali, Equipment, BOP e Tooling (20260312) - Analysis"
source_file: "SourcesMd/Sessioni Training 11-12 Marzo 2026/20260312-BackOffice-Juela-Ndoka.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [CURNO, MAPELLO]
derived_from: "SourcesMd/Sessioni Training 11-12 Marzo 2026/20260312-BackOffice-Juela-Ndoka.md"
---

# 20260312-BackOffice-Juela-Ndoka_Analysis

## [SHARED] Perimetro del training backoffice MES

### Contenuto deterministico
- La sessione copre i principali oggetti MES con impatto sulla produzione: materiali, buffer, equipment, routing/BOP, documenti e work order.
- L'obiettivo è spiegare la manutenzione backoffice degli oggetti master e i relativi legami operativi.
- L'ambiente mostrato è di test, distinto dall'ambiente produttivo futuro.

### Tracciabilità
- Fonte: sezione `Introduzione e agenda del training backoffice`

## [SHARED] Material master: provenienza ERP e proprietà rilevanti

### Contenuto deterministico
- L'anagrafica materiali in MES arriva da ERP e viene aggiornata periodicamente da job di sincronizzazione.
- L'Unique Identifier del materiale combina codice e revisione.
- Tra le proprietà rilevanti figurano qualità, safety, simboli di etichetta ed expiration date.

### Regole operative
- Le proprietà dei materiali sono principalmente in sola lettura per il backoffice operativo perché governate da ERP.
- L'uso tipico lato backoffice riguarda soprattutto la consultazione e l'eventuale associazione di documenti.

### Tracciabilità
- Fonte: sezione `Anagrafica materiali e sincronizzazione ERP`

## [SHARED] Strategia documentale: MES locale, Linksys e contesto operatore

### Contenuto deterministico
- I documenti possono essere associati ai materiali direttamente in MES oppure resi disponibili tramite Linksys.
- Linksys è la piattaforma di riferimento per molta documentazione di produzione e viene richiamata con query di contesto work center + prodotto.
- I documenti specifici non presenti in Linksys possono essere caricati direttamente in MES.

### Regole di business ed eccezioni
- La scelta repository privilegia Linksys per evitare duplicazioni e semplificare la manutenzione documentale.
- In MES vanno mantenuti solo i documenti realmente necessari in preview sul terminale operatore.

### Tracciabilità
- Fonte: sezione `Documenti materiali e integrazione con Linksys`

## [SHARED] Buffer / pre-macchina: struttura, creazione e legame con il work center

### Contenuto deterministico
- I buffer rappresentano il pre-macchina fisico dove viene allocato il materiale da consumare.
- I buffer visibili in MES sono stati creati tramite import massivo e possono contenere stock disponibile proveniente da ERP.
- In dettaglio buffer sono presenti identificativo, descrizione, stato, definizione e work center/area associata.

### Regole operative
- Per essere utilizzabile il buffer deve essere in stato Released.
- La creazione di un nuovo buffer richiede un identificativo coerente con SAP e l'associazione a un equipment già esistente.

### Tracciabilità
- Fonte: sezione `Buffer e pre-macchina`

## [SHARED] Equipment configuration e gerarchia plant

### Contenuto deterministico
- L'equipment è il contenitore logico di plant, area, work center e unit.
- Prima si crea l'equipment in equipment configuration, poi lo si colloca nella plant hierarchy.
- La gerarchia determina ereditarietà di alcune proprietà operative, come l'uso dei buffer di area.

### Regole operative
- Un equipment creato ma non posizionato nella hierarchy non è ancora utilizzabile lato produzione.
- Ogni plant ha una propria hierarchy e un proprio link applicativo separato.

### Tracciabilità
- Fonte: sezione `Equipment configuration e equipment hierarchy configuration`

## [SHARED] Proprietà equipment e flag di comportamento runtime

### Contenuto deterministico
- Le proprietà del work center governano comportamenti come autostart dell'operazione successiva, multi-instance, AGV, automazione, original batch e stampanti.
- Alcuni flag sono specifici di processo, ad esempio le macchine automatizzate con contapezzi o i work center con original batch.
- È presente anche la proprietà `SendGoodReceiptForScrapAndQuarantine`, differenziata per la fonderia rispetto agli altri processi.

### Regole di business ed eccezioni
- In fonderia `SendGoodReceiptForScrapAndQuarantine` deve essere False per convertire lo scarto in chili di ritorno anziché giacenza di materiale scarto.
- Le proprietà ereditate dal template vanno comunque verificate e valorizzate sul singolo equipment.

### Tracciabilità
- Fonte: sezione `Properties del work center e flag di configurazione`

## [SHARED] Sequenza operativa per introdurre una nuova macchina

### Contenuto deterministico
- Il processo discusso parte dalla creazione del premacchina/buffer in SAP.
- Successivamente si crea il work center/equipment in SAP e in MES, lo si posiziona nella hierarchy e si crea il buffer associato.
- Il training richiama anche il ruolo di una nomenclatura centralizzata fra plant e sistemi.

### Regole operative
- La sequenza corretta è: equipment configuration -> hierarchy -> buffer.
- La codifica deve restare coerente con i sistemi sorgente e con la convenzione centrale adottata.

### Tracciabilità
- Fonte: sezione `Processo per nuova macchina o nuovo work center`

## [SHARED] BOP / routing: origine ERP, operazioni e limiti dell'interfaccia

### Contenuto deterministico
- Le BOP/routing arrivano da ERP e rappresentano la sequenza di operazioni necessarie a produrre un materiale.
- Il group identifier e il group counter SAP sono esposti nel modello BOP di MES.
- Nei dettagli operazione sono presenti dipendenze, machine/work center, materiali consumati, by-product e tool.

### Regole di business ed eccezioni
- La manutenzione diretta della BOP non è un'attività ordinaria di backoffice locale, salvo enrichment come quality inspection o documenti.
- L'interfaccia non consente un filtro semplice per product nella lista BOP; il training segnala il limite come noto.

### Tracciabilità
- Fonte: sezione `BOP, operazioni e provenienza SAP`

## [SHARED] Tool definition, immagini di cavità e gestione seriali

### Contenuto deterministico
- Tool definition e tool seriali arrivano da ERP e contengono dati usati in start ordine e scarto cavità.
- La max usage count è un attributo critico: se mancante può impedire lo start ordine.
- Le immagini della conchiglia/famiglia tool vengono caricate nei documenti della tool definition.

### Regole operative
- L'immagine di riferimento per lo scarto cavità va associata alla family/tool definition, non al materiale.
- I codici delle cavità e lo stroke ratio vengono invece valorizzati nelle proprietà materiale pertinenti.
- Il contatore di utilizzo può essere azzerato o corretto sul singolo seriale tool quando necessario.

### Tracciabilità
- Fonte: sezione `Tool definition, documenti tool e configurazione cavità`

## [SHARED] App complementari e metriche operative a bordo macchina

### Contenuto deterministico
- Oltre a Opcenter MES sono richiamate altre web application operative per avanzamento, Andon e manutenzione.
- Le metriche mostrate includono actual cycle time, ideal cycle time, pezzi buoni e stato di avanzamento.
- Alcune informazioni derivano dalle dichiarazioni MES, altre dai contapezzi o da sistemi complementari.

### Regole operative
- Le app complementari non sostituiscono MES: gli scarti e le dichiarazioni produttive restano nel flusso Opcenter.
- Le causali fermo macchina sono gestite nell'app dedicata di avanzamento/Andon.

### Tracciabilità
- Fonte: sezione `Schermate di avanzamento, Andon e strumenti correlati`

## [SHARED] Chiusura training e chiarimento finale su immagini e proprietà

### Contenuto deterministico
- In chiusura viene ribadito che l'immagine delle figure va caricata sulla tool family.
- I codici/part number delle cavità e le proprietà di ratio vanno gestiti nell'anagrafica materiale/proprietà pertinenti.
- Il team richiede di aggiungere slide esplicative dedicate a questa distinzione.

### Tracciabilità
- Fonte: sezione `Riepilogo finale su immagine tool e codici cavità`
