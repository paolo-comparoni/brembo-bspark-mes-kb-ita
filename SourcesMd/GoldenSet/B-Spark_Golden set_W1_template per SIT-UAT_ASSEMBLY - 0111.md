# B-Spark_Golden set_W1_template per SIT-UAT — Foglio: ASSEMBLY - 0111

> Documento sorgente: `E:\BremboDocs\GoldenSet\B-Spark_Golden set_W1_template per SIT-UAT.xlsx`  
> Tipo: Excel (.xlsx) · Foglio: **ASSEMBLY - 0111** · Righe dati: 45 · Colonne: 19

|  |  | ASSEMBLY & PAINTING -  Curno (plant 0111) |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  | Bedding |  | First Assembly<br><br>MES - "After-end" (Z007) |  | External Painting<br><br>(Z005) |  | Logo Printing (Tampography)<br><br>(Z006) |  | Second Assembly<br><br>MES - "After-end" (Z007) |  | Full Assembly<br><br>MES - "After-end" (Z007) |  | Modules Assembly<br><br>MES - "After-end" (Z007) |  |  |  |  |
|  |  | Material staging | Material production | Material staging | Material production | Material staging | Material production | Material staging | Material production | Material staging | Material production | Material staging | Material production | Material staging | Material production |  |  |  |
| SCENARIO F1 (7)<br>Ferrari<br>Car set<br><br>26D66814 | PSA |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Work center |  |  |  |  | external | SUBCO |  |  |  | SACSA005 |  | SAKNL008 |  | SAMAL002 |  |  |  |
|  | Pinza |  |  | 20B93291 | 20C837CF_FSA<br>20C837DF_FSA | 20C837CF_FSA / *_RB / _*RP<br>20C837DF_FSA / *_RB / _*RP | 20C837CF<br>20C837DF |  |  |  | 20D66647<br>20D66648 |  |  |  |  |  |  |  |
|  | Semi-modulo |  |  |  |  |  |  |  |  |  |  |  | 28E184AA |  |  |  |  |  |
|  | Modulo |  |  |  |  |  |  |  |  |  |  |  |  |  | 26D66814 |  | 20B93291 |  |
|  | Pastiglie |  |  |  |  |  |  |  |  | 47C12311 |  |  |  |  |  |  | 20C837CF |  |
|  | Pastiglie rodate |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20D66647 |  |
|  | Materials |  |  | check BOM |  |  |  |  |  | 22C04027 | check BOM |  |  |  |  |  | 28E184AA |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 26D66814 |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20D499AU |  |
| SCENARIO F2 (9)<br>Porsche<br><br>20D49835/6<br> | PSA |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20D499BU |  |
|  | Work center |  |  |  |  | Routing 2 phase - Painting + extracontrol | SPCPL001<br>SQMAN008 |  |  |  |  | SPCPL001+<br>SQMAN008 | SAMCL008 |  |  |  | 20D499AU |  |
|  | Pinza SX |  |  |  |  |  | 20D499AU |  |  |  |  | 20D499AU | 20D49835 |  |  |  | 20D499BU |  |
|  | Pinza DX |  |  |  |  |  | 20D499BU |  |  |  |  | 20D499BU | 20D49836 |  |  |  | 20D49835 |  |
|  | Materials |  |  |  |  |  |  |  |  |  |  | check BOM |  |  |  |  | 20D49836 |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20C71735 |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20C71736 |  |
| SCENARIO F3 (10)<br>BMW<br><br>20D77459-R/60-R | PSA |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20C718GG_FSA |  |
|  | Work center |  |  |  | SAMFA005 | external | SUBCO |  | SLPPC01M |  | SACSA007 |  |  |  |  |  | 20C718HG_FSA |  |
|  | Pinza sx |  |  | 20C71735 | 20C718GG_FSA |  | 20C718GG_PNT |  | 20C718GG | 20C718GG | 20D77459-R |  |  |  |  | unico imballo per i due codici | 20C718GG_PNT | SUBCO |
|  | Pinza sx |  |  | 20C71736 | 20C718HG_FSA |  | 20C718HG_PNT |  | 20C718HG | 20C718HG | 20D77460-R |  |  |  |  |  | 20C718HG_PNT | SUBCO |
|  | Materials |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20C718GG |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20C718HG |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20C718GG |  |
| SCENARIO F4 (11)<br>SUBARU<br><br>20E22121/2 | PSA |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20C718HG |  |
|  | Work center |  |  |  | SAHFA002 | external | SUBCO |  |  | Routing 2 phase - assy + extracontrol<br>SAHFA002 + <br>SQMAN01M | SACSA025<br>SQMAN01M |  |  |  |  |  | 20D77459-R |  |
|  | Pinza SX |  |  |  | 20E221AC_FSA |  | 20E221AC |  |  | 20E221AC | 20E22121 |  |  |  |  |  | 20D77460-R |  |
|  | Pinza DX |  |  |  | 20E221BC_FSA |  | 20E221BC |  |  | 20E221BC | 20E22122 |  |  |  |  |  | 20E22231 |  |
|  | Pastiglie SX |  |  |  |  |  |  |  |  | 47E67310/12 |  |  |  |  |  |  | 20E22331 |  |
|  | Pastiglie DX |  |  |  |  |  |  |  |  | 47E67311/13 |  |  |  |  |  |  | 20E22232 |  |
|  | Semipinza SXCO |  |  | 20E22231 |  |  |  |  |  | check BOM |  |  |  |  |  |  | 20E22332 |  |
|  | Semipinza SXSO |  |  | 20E22331 |  |  |  |  |  |  |  |  |  |  |  |  | 20E221AC_FSA |  |
|  | Semipinza DXCO |  |  | 20E22232 |  |  |  |  |  |  |  |  |  |  |  |  | 20E221BC_FSA |  |
|  | Semipinza DXSO |  |  | 20E22332 |  |  |  |  |  |  |  |  |  |  |  |  | 20E221AC | SUBCO |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 20E221BC | SUBCO |
| SCENARIO F5 (14)<br>Ferrari<br>Bedding<br>Pastiglie Ferrari:<br>749T25910 - set rodato anteriore con pastiglie rodate 747B94918/19<br><br>749T35210 - set rodato posteriore con con pastiglie rodate 747D66912/13 | PSA |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Work center |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Friction bedded |  | 749T25910 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Materials |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Materials |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Materials |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Materials |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
