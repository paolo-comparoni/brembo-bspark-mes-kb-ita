---
title: "Hypercare Preparation Training - Connect MOM, Messaggi e Integrazioni (2026-04-10)"
source_file: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_100426.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [SHARED]
---

# Hypercare Preparation Training - Connect MOM, Messaggi e Integrazioni (2026-04-10)

> Documento sorgente: `E:\BremboDocs\HyperCare Training video\Brembo - Training per preparazione Hypercare_100426.docx`  
> Tipo: Word (.docx)

## Errori di Connect MOM e casi tipici di fallimento messaggio

- Vengono discussi errori comuni emersi nei test di integrazione.
- Un caso ricorrente è l'errore sull'ordine dovuto a materiali finiti o componenti mancanti.
- Un altro caso citato è errore 500 a fronte di stato `empty` ricevuto da EWM/integrazione logistica.

## Architettura di integrazione tra MES, SAP, EWM e AGV

- Connect MOM è il punto di tracciamento delle comunicazioni tra MES e sistemi terzi.
- Nel linguaggio della sessione SAP comprende anche la parte EWM/SPI usata per la logistica.
- Il MES invia richieste e conferme ma non governa direttamente l'automazione fisica delle macchine.

## Limiti del MES come point of failure e impatto sulla tracciabilità

- Il team distingue tra continuità della produzione fisica e continuità della tracciabilità digitale.
- Anche se la linea può continuare a produrre, l'assenza di consumi, produzioni o etichette porta a disallineamento e rischio compliance.
- Il MES è quindi point of failure per visibilità, consuntivazione e integrazioni, non necessariamente per lo start macchina.

## Procedure di recovery: retry, resend e manual import

- Se il messaggio è stato generato ma non consegnato, il team cita meccanismi di retry e resend.
- È disponibile anche una cartella/processo di `manual import` per forzare il reinvio.
- Se il messaggio non viene proprio generato, il workaround non basta e serve intervento sul codice.

## Preparazione Hypercare: riconoscere l'errore e scegliere il workaround corretto

- La sessione mira a dare al team criteri pratici per capire se il problema è di generazione, comunicazione o allineamento dati.
- L'obiettivo è evitare disallineamenti con SAP e logistica durante i turni di supporto.
- La conoscenza di Connect MOM viene trattata come competenza trasversale per chi presidia il live.
