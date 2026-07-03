---
title: "Hypercare Preparation Training - Log, Event Viewer e Root Cause Analysis (2026-04-28)"
source_file: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_280426.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [SHARED]
---

# Hypercare Preparation Training - Log, Event Viewer e Root Cause Analysis (2026-04-28)

> Documento sorgente: `E:\BremboDocs\HyperCare Training video\Brembo - Training per preparazione Hypercare_280426.docx`  
> Tipo: Word (.docx)

## Event Viewer, application service log e lettura del tracciato tecnico

- La sessione mostra come leggere i log tecnici del sistema partendo dall'Event Viewer/application service log.
- Viene chiarito che il tracciato nativo è molto ricco ma difficile da seguire su più macchine.
- L'obiettivo è insegnare al team a risalire al punto di rottura dell'elaborazione.

## Database centralizzato dei log e reverse engineering degli errori

- È citato un database creato per aggregare i log di tutte le macchine.
- Questo repository consente di fare reverse engineering senza dover consultare macchina per macchina.
- Il team usa timestamp, record ID e nome computer per ricostruire la sequenza degli eventi.

## Relazione tra Connect MOM, errore parlante e analisi di secondo livello

- Se Connect MOM mostra un errore parlante, l'analisi può fermarsi lì.
- Se il messaggio non è abbastanza esplicativo, si passa al database log di dettaglio.
- Il troubleshooting segue quindi un percorso a due livelli: middleware e log infrastrutturale.

## Bug noti, problemi di refresh e verifiche emerse dal training

- Viene discusso un bug noto di refresh dopo dichiarazione scarto sul prodotto finito.
- Il problema impatta i contatori in testata ma non necessariamente il dato persistito.
- In alcuni casi il semplice refresh della pagina consente il recupero della visualizzazione corretta.

## Anomalie su utente, work order e container type duplicati

- Sono citati casi di mismatch utente, gestione work order cutting e duplicazione apparente di container type.
- Il team ragiona su cause possibili come dato non refreshato o oggetti non eliminati correttamente.
- Le verifiche vengono collegate a impianto, work center e cronologia di creazione degli oggetti.

## Metodo Hypercare per classificare e analizzare un incidente

- La sessione propone un metodo pratico: partire dal sintomo, localizzare l'orario, verificare Connect MOM e poi scendere sul log centralizzato.
- L'analisi deve distinguere tra bug noto, problema di refresh, errore di dato e difetto reale di processo.
- L'obiettivo finale è ridurre il tempo di diagnosi durante il supporto live.
