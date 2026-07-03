# spiegazione mold

> Documento sorgente: `E:\BremboDocs\SlideTrainingItalia\spiegazione mold.docx`  
> Tipo: Word (.docx)

La Mold come "Tool" (Risorsa di Produzione)

Nel MES, durante le operazioni di **Casting** (Fusione), la mold è gestita attraverso le funzionalità di **Tool Management**.

  - **Tool Definition:** Esiste una definizione astratta della mold (es. il tipo o codice tecnico come S20E93800\_042) che funge da modello.

  - **Tool Instance (Seriale):** Ogni stampo fisico è un'istanza specifica del "Tool Definition" ed è identificato da un **Serial Number** unico (es. S20E93800ST01).

  - **Utilizzo e Manutenzione:** Come tutti i Tool nel sistema, la mold ha un **Usage Counter** (chiamato anche "Strikes Counter") che conta quante colate sono state effettuate per segnalare quando è necessaria la manutenzione preventiva.

2\. La Mold come "Materiale" (Per la Logistica e SAP)

Sebbene nel MES operi come un Tool, esiste una dualità dovuta all'integrazione con l'ERP (SAP/Dynamics AX):

  - **Oggetto di Lavoro:** Per le fasi di **Mold Preparation** (preparazione, verniciatura, sabbiatura), la mold è trattata come se fosse il "materiale" da lavorare in un ordine di produzione monofase dedicato. In questo contesto, ha un suo **P/N (Part Number)** e viene emesso un cartellino (CDI) specifico per la sua movimentazione.

  - **Anagrafica:** Viene citata la presenza di un "Mold Master Data" anche in sistemi paralleli come TESAR per la gestione della qualità e dei piani di controllo.
