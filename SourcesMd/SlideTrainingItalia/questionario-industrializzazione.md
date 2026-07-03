# questionario-industrializzazione

> Documento sorgente: `E:\BremboDocs\SlideTrainingItalia\questionario-industrializzazione.docx`  
> Tipo: Word (.docx)

**QUESTIONARIO INDUSTRIALIZZAZIONE**

1.  **Se si vuole consultare la sequenza di operazioni legate a un prodotto, quale app bisogna aprire?**

<!-- end list -->

1.  Material Tracking Units.

2.  Print History.

3.  BOP (Bill of Process).

4.  Equipment Hierarchy.

**Risposta corretta: c.** La BOP è la rappresentazione nel MES del Routing di SAP; qui il supervisore può arricchire il processo con ispezioni o documenti.

2.  **Dove si verifica la presenza del materiale in pre-macchina?**

<!-- end list -->

1.  Nell'app Buffer.

2.  Nell'app Container Types.

3.  Nella pagina Personnel.

4.  Nella scheda Audit Trail.

**Risposta corretta: a.** L'app Buffer mostra le Handling Unit (CDI) attualmente presenti nell'area di stoccaggio virtuale associata alla macchina.

3.  **Dove viene gestita l’associazione di un documento (es. PDF tecnico o immagine) a un materiale nel sistema?**

<!-- end list -->

1.  Esclusivamente sul Terminale Operatore durante la fase di produzione attiva.

2.  Nel Back-office, all'interno della pagina Materials (scheda Documents) o tramite la configurazione della BOP.

3.  All'interno dell'app "Print History" prima di generare le etichette.

4.  Solo tramite il sistema SAP, poiché il MES non può archiviare file locali.

**Risposta corretta: b.** L'associazione viene configurata nella pagina Materials seguendo il percorso Product and Production Configuration \> Materials. I documenti possono essere collegati anche tramite la BOP a specifiche operazioni, così che l'ordine li erediti automaticamente tramite il processo di “arricchimento”.

4.  **Per la configurazione delle stampanti, quale logica segue il sistema MES?**

<!-- end list -->

1.  Logica casuale in base alla stampante più vicina.

2.  Logica gerarchica: la configurazione a livello di Unit ha la precedenza sul Work Center.

3.  Logica temporale: l'ultima stampante installata ha la precedenza.

4.  Le stampanti possono essere configurate solo a livello di Enterprise.

**Risposta corretta: b.** Il sistema applica una precedenza gerarchica dove le proprietà configurate a livello di Unit (la singola macchina) sovrascrivono quelle impostate a livello di Work Center.

5.  **Dove devono essere caricate le immagini degli stampi (Tool) nel sistema?**

<!-- end list -->

1.  Nella pagina "Work Order"

2.  Nella pagina "Materials"

3.  Nella pagina "Tool Definition"

4.  Direttamente sul PLC della macchina

**Risposta corretta: c.** Le immagini tecniche devono essere caricate nella pagina Tool Definition per essere poi visibili all'operatore durante la produzione.

6.  **Cosa accade quando uno stampo raggiunge il "Max Usage Count" (Contatore Colpi)?**

<!-- end list -->

1.  Il sistema aumenta automaticamente la velocità di produzione.

2.  Il MES blocca la produzione per richiedere la sostituzione o revisione dello stampo.

3.  Viene stampata un'etichetta di "Rework".

4.  Il dato viene semplicemente ignorato fino a fine turno.

**Risposta corretta: b.** Al raggiungimento della soglia, il sistema blocca l’utilizzo per garantire la qualità del processo produttivo.

7.  **Riguardo ai Routing (BOP), quale delle seguenti affermazioni è corretta?**

<!-- end list -->

1.  Vengono creati e modificati direttamente all'interno del MES.

2.  Non sono necessari per la produzione in Opcenter.

3.  Vengono importati dal sistema ERP/SAP e “arricchiti” nel MES.

4.  Sono elenchi di soli documenti senza fasi operative.

**Risposta corretta: c.** I routing sono considerati Master Data strategici; vengono creati in SAP e importati nel MES, vengono poi "arricchiti" localmente solo con dettagli operativi.
