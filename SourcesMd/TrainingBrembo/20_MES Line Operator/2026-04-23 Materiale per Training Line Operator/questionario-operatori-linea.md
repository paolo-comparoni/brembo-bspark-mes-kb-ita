---
title: "Questionario operatori di linea"
source_file: "SourcesMd/TrainingBrembo/20_MES Line Operator/2026-04-23 Materiale per Training Line Operator/questionario-operatori-linea.md"
project: "Brembo B-Spark"
scope: "Operational_Training_Material"
plants: [SHARED]
---

# Questionario operatori di linea

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\20_MES Line Operator\2026-04-23 Materiale per Training Line Operator\questionario-operatori-linea.docx`  
> Tipo: Word (.docx)

## Domande di verifica

1.  **Perché è obbligatorio che l’operatore si registri nel “Team” (Gruppo di Lavoro) di una postazione prima di operare?**

<!-- end list -->

1.  Per attivare il calcolo automatico della produzione.

2.  Per consentire la visualizzazione dei documenti tecnici.

3.  Per garantire la tracciabilità delle attività e delle persone sul Work Center.

4.  È una procedura facoltativa utile solo in caso di straordinari.

**Risposta corretta: c.** La registrazione è fondamentale per sapere chi sta operando sulla macchina in ogni momento; senza operatori nel gruppo, il sistema blocca azioni come lo Start o la Pausa.

2.  **Nell’interfaccia degli ordini (Work Orders), cosa indica l’icona circolare con una lunetta blu?**

<!-- end list -->

1.  Un ordine nuovo mai avviato.

2.  Un ordine attivo attualmente in fase di esecuzione.

3.  Un ordine messo in pausa per cambio turno.

4.  Un ordine completato che attende la chiusura di SAP.

**Risposta corretta: b.** Il sistema utilizza icone colorate per indicare lo stato degli ordini di lavorazione: verde per i nuovi ordini, cerchio vuoto/grigio per la pausa e lunetta blu per l’ordine attivo.

3.  **Cosa segnala la comparsa di un triangolo giallo (o arancione) su un ordine o su una operazione?**

<!-- end list -->

1.  Un guasto meccanico imminente della macchina.

2.  La presenza di una Non-Conformità.

3.  Che l’ordine ha superato la data di consegna prevista.

4.  Che il materiale nel buffer è andato in esaurimento.

**Risposta corretta: b.** Questi indicatori segnalano anomalie, pezzi in quarantena o ispezioni obbligatorie pianificate che richiedono l’attenzione dell’operatore o della Qualità.

4.  **Qual è la funzione specifica del comando “Close Partial Container”?**

<!-- end list -->

1.  Svuotare virtualmente il buffer della stazione di lavoro.

2.  Ristampare un’etichetta CDI danneggiata senza generare nuovi dati.

3.  Chiudere definitivamente un contenitore non pieno (es. per cambio materiale) inviando la quantità reale a SAP.

4.  Mettere in pausa l’ordine salvando i pezzi prodotti fino a quel momento.

**Risposta corretta: c.** Serve a chiudere un cassone incompleto in modo definitivo, permettendone il trasferimento alla fase successiva, a differenza del “Partial Complete” che lo lascia appeso per il collega del turno dopo.

5.  **Qual è la differenza operativa principale tra tracciabilità “Hard” e “Soft” dei materiali?**

<!-- end list -->

1.  Nella “Hard” la scansione del barcode (CDI) è obbligatoria per poter procedere con la produzione.

2.  Nella “Soft” il sistema non tiene traccia del lotto di provenienza.

3.  La “Hard” viene utilizzata esclusivamente per i sottoprodotti (By-products).

4.  Non c’è differenza, sono termini usati per distinguere materiali plastici da metallici.

**Risposta corretta: a.** La tracciabilità “Hard” impone il blocco del sistema se il materiale corretto non viene scansionato, mentre la “Soft” suggerisce il consumo ma non è vincolante per l’avanzamento.

6.  **Quale applicazione del Back-office permette al supervisore di monitorare l’avanzamento in tempo reale della produzione (WIP)?**

<!-- end list -->

1.  Print History.

2.  Container Types.

3.  Work in Progress.

4.  Buffer Management.

**Risposta corretta: c.** L’app **Work in Progress** è dedicata specificamente al monitoraggio real-time dello stato degli ordini in produzione.

7.  **In quale sezione del sistema bisogna entrare per ristampare un’etichetta CDI?**

<!-- end list -->

5.  Material Tracking Units.

6.  Work Orders.

7.  Print History.

8.  Equipment Hierarchy.

**Risposta corretta: c.** La sezione **Print History** (Storico Stampe) raccoglie tutte le etichette generate e permette di effettuarne la ristampa in caso di necessità.
