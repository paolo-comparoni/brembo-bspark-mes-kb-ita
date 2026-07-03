---
title: "Hypercare Preparation Training - AGV, Baie e Flussi Logistici (2026-04-14)"
source_file: "SourcesMd/HyperCare Training video/Brembo - Training per preparazione Hypercare_140426.md"
project: "Brembo B-Spark"
scope: "Operational_KT"
plants: [SHARED]
---

# Hypercare Preparation Training - AGV, Baie e Flussi Logistici (2026-04-14)

> Documento sorgente: `E:\BremboDocs\HyperCare Training video\Brembo - Training per preparazione Hypercare_140426.docx`  
> Tipo: Word (.docx)

## Contesto di plant: machining Curno e gestione AGV

- La sessione usa il machining di Curno come caso di riferimento.
- La GV/AGV è descritta come trasporto automatico dei contenitori all'interno dell'impianto.
- In questo contesto il processo dipende fortemente da chiamate e ritorni verso AGV.

## Attivazione AGV a livello Work Center

- L'abilitazione AGV è configurata sul work center/equipment.
- Il parametro citato è `ISA_Gv_Enabled`.
- Se la proprietà è vuota il comportamento di default è equivalente a `false`.

## Chiamate operative AGV da interfaccia Repetitive

- Una volta abilitata la funzionalità compare nell'interfaccia un set di azioni operative.
- Le azioni mostrate sono:
  - call empty,
  - return empty,
  - call alveolari,
  - return alveolari,
  - return chip container.
- Ogni azione corrisponde a una specifica necessità logistica di linea.

## Baie, buffer, packaging specification e materiali di confezionamento

- Le baie rappresentano aree geolocalizzate della linea in cui l'AGV deposita o ritira i contenitori.
- Per funzionare, una baia deve essere associata a buffer e pack material.
- La configurazione permette anche di filtrare i tipi container ammessi in quella baia.

## Semaforo chiamata AGV e scambio con sistema logistico

- Dopo l'invio della chiamata, l'interfaccia mostra un semaforo di stato.
- Il sistema attende una risposta dal layer logistico/EWM prima di aggiornare l'esito.
- La sessione collega esplicitamente il comportamento del semaforo ai messaggi osservabili su Connect MOM.

## Backoffice Mendix e transizione dalle pagine Basic

- Le nuove configurazioni AGV sono mostrate su pagine Mendix/production engineer.
- Le pagine Basic restano usate per ampiezza funzionale, ma gli sviluppi nuovi sono stati portati in Mendix.
- Il training prepara quindi il team a muoversi tra backoffice legacy e nuove pagine applicative.
