# B-Spark_Golden set_W1_template per SIT-UAT — Foglio: PURCHASING_Stand_Alone

> Documento sorgente: `E:\BremboDocs\GoldenSet\B-Spark_Golden set_W1_template per SIT-UAT.xlsx`  
> Tipo: Excel (.xlsx) · Foglio: **PURCHASING_Stand_Alone** · Righe dati: 26 · Colonne: 15

|  |  |  |  |  |  |  |  | INDIRECT PRCUREMENT |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  | PO for PPAP <br>(ZCAM) | PO for prototype <br>(ZPRO) | PO reworking <br>(ZREW) | PO Intercompany <br>(ZICC) |  |  | Curno - 0111 | Curno - 0111 | Mapello - 0121 | Mapello - 0121 | Stezzano - 0100 | Stezzano - 0100 | Stezzano - 0100 |
|  |  |  |  |  |  | PR/Purchase order Ariba <br>(ZARB) | Scenario | Generic Purchase - Good | Generic Purchase - Service | Catalogue items | Purchase Intercompany | Order Legal Services | Order Consultant Services | Order ADV Services |
| SCENARIO F1<br> | Vendor |  |  |  |  |  | Vendor | LEGGERI ATTREZZERIA MECCANICA SRL | LEGGERI ATTREZZERIA MECCANICA SRL | F.LLI VEDANI S.R.L. | Brembo CZ | JACOBACCI & PARTNERS S.p.a. | 7Layers S.r.l. | 2R PUBBLICITA' S.R.L. |
|  | Materials | Nuovo codice |  |  |  |  | Material Group | AMRO007 | AFM0031 | (viene recuperato in automatico) | AINT002 | APS0013 | APS0020 | ASMK001 |
|  | Record Info |  |  |  |  |  | Accounting Type (Cost Center/WBS/Asset) | Cost Center | Cost Center | Cost Center | Cost Center | Cost Center | Cost Center | WBS |
|  | Contract |  |  |  |  |  | Cost Center/WBS/Asset | BB011R1001 | BB011R1001 | BB01GO0037 | BB01GO0037 | BB011R1009 | BB011R1009 | BB011R1009 |
| SCENARIO F2 | Vendor |  |  |  |  | PR/PO for Asset <br>(ZASS) | Scenario | PR for asset | PR for asset | PR for asset | PR for asset | PR for asset | PR for asset | PR for asset |
|  | Materials |  |  |  |  |  | Vendor | PRADELLA & MATEGO S.p.A. | TMD FRICTION SERVICES GMBH | LEGGERI ATTREZZERIA MECCANICA SRL | LEGGERI ATTREZZERIA MECCANICA SRL | D.A.U. S.R.L. | D.A.U. S.R.L. | D.A.U. S.R.L. |
|  |  |  |  |  |  |  | Material Group | AMCE020 | AMCE020 | AMCE002 | AMCE002 | AFM0003 | AFM0003 | AFM0003 |
|  | Record Info |  |  |  |  |  | Accounting Type (Cost Center/WBS/Asset) | 24012POXC14548 | 25012POXB54099 | 2501BPOXD87995 | 2501BPOXD71422 | 25BRTPOXA24517 | 25BRTPOXA24517 | 25BRTPOXA24517 |
|  | Contract |  |  |  |  |  | Accounting code | SP00001DRI | SP00001DRI | SP00001DRI | SP00001DRI | SP561015IN | SP561015IN | SP561015IN |
| SCENARIO F3<br> | Vendor |  |  |  |  | PO training course <br>(ZHR) | Scenario |  |  |  |  |  |  |  |
|  | Materials |  |  |  |  |  | Vendor |  |  |  |  |  |  |  |
|  | Record Info |  |  |  |  |  | Material Group |  |  |  |  |  |  |  |
|  | Contract |  |  |  |  |  | Accounting Type (Cost Center/WBS/Asset) |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  | Accounting code |  |  |  |  |  |  |  |
| SCENARIO F4<br> | Vendor |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Materials |  |  |  |  | PR/Purchase order SAP <br>(Codificati AUX) | Scenario | PR per codice nuovo | PR per rilavorazione (subcontracting) | PR per acquisto codificato aux | PR per acquisto codificato aux |  |  |  |
|  | Record Info |  |  |  |  |  | Vendor | FIUDI S.R.L. | FIUDI S.R.L. | F.LLI VEDANI S.R.L. | TIPOLITOGRAFIA CRESPI SRL | / | / | / |
|  | Contract |  |  |  |  |  | Material | 53869900I | CL0RG53869900IN (non conosciamo la ricodifica SAP senza CL) | AUX0164 | AUX0040 |  |  |  |
|  |  |  |  |  |  |  | Accounting Type (Cost Center/WBS/Asset) | Cost Center | Cost Center | Cost Center | Cost Center |  |  |  |
| SCENARIO F5<br> | Vendor |  |  |  |  |  | Cost Center/WBS/Asset | (Autoamticamente recuperato da material) | (Autoamticamente recuperato da material) | (Autoamticamente recuperato da material) | (Autoamticamente recuperato da material) |  |  |  |
|  | Materials |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Record Info |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Contract |  |  |  |  |  |  |  |  |  |  |  |  |  |
