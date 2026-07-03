# B-Spark_Golden set_W1_template per SIT-UAT — Foglio: PLANNINGv2

> Documento sorgente: `E:\BremboDocs\GoldenSet\B-Spark_Golden set_W1_template per SIT-UAT.xlsx`  
> Tipo: Excel (.xlsx) · Foglio: **PLANNINGv2** · Righe dati: 459 · Colonne: 23

| FOUNDRY |  |  | BOM |  |  |  | PLANNING FIELDS |  |  |  |  |  |  |  |  |  |  | ROUTING |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SCENARIO F1<br>monoblocco Porsche<br><br>20D49901 | Process phase |  | MATERIAL | IN--HOUSE/SUBCO | QTY | MEASURE UNIT | LOT  SIZING PROCEDURE [regola accorpamento fabbisogni proposte] | MINIMUM LOT SIZE | MAXIMUM LOT SIZE | FIXED LOT SIZE | REORDER POINT [non usato] | ROUNDING VALUE | SAFETY STOCK [pezzi] | SAFETY TIME (Workdays) | OVERLAPPING REQUIRED [Y/N] | Min qty  Ovearlapping | CO-PRODUCT PRESENT [Y/N] | OEPRATION # | WORK CENTER | BASE QTY | MACHINE TIME (min) | overlapping presente: tra casting e cutting , tra cutting ed htt , tra htt e finishing (codici monofase) |
|  | Core shop | BB00018J |  |  |  |  | 450 | 450 | 1400 | \\ | \\ | \\ | 0 |  | Y |  | Y |  | G802002 | 100 | 1.05 |  |
|  | Phantom Assembly | BB00018K_PH | BB009900 | in house | 0.2 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Phantom Assembly | BB00018L_PH | BB009900 | in house | 0.2 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Casting | 20D49901_011 |  |  | 1 |  | 850 | 190 | 1100 | \\ | \\ | \\ | 0 | 2 | Y | 144 | N |  | Isola N - G118002 | 1 | 6.75 |  |
|  |  | P00800000_PH | Alsi7P | SUBCO | 11.86 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | BB00018J | CORE ASSEMBLY 20D499 | in house | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | BB010002_PH | RETE FILTRAGGIO H.80 L.130 AL308 F | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Cutting | 20D49901_CUT |  | in house | 1 | nr | 850 | 190 | 1100 | \\ | \\ | \\ | 0 | 1 | Y | 144 | N |  | G219002 |  | 0.83 |  |
|  |  | P00190000 | Alsi7P SFRIDO ALLUMINIO | in house | -0.0364 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | BB000020 | Alsi7P SCARTI FUSIONE | in house | -6.3272 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20D49901_011 | CORPO PINZA FUSO | in house | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Heat Treatment | 20D49901_HTT | Alsi7P | in house | 1 |  | 850 | 190 | 1100 | \\ | \\ | \\ | 0 | 2 | Y | 144 | N |  | G303032 | 144 | 70 |  |
|  |  | 20D49901_CUT |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Finishing | 20D49901 |  | SUBCO | 1 | nr | 850 | 190 | 1100 | \\ | \\ | \\ | 0 | 3 | N | 144 | N |  | G500100 |  |  |  |
|  |  | BB000010 | Alsi7P SFRIDO LAVORAZIONI ESTERNE |  | -0.0364 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20D49901_HTT |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | X-ray | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Shot blasting | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| FOUNDRY |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F3<br>Stampo in gravità 4 cavità e 2 codici <br>SUBARU<br>20E22202/20E22302<br> | Core shop | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0010 |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0020 |  |  |  |  |
|  | Casting | 20E22302_042 |  |  |  |  | 1900 | 380 | 2200 | \\ | \\ | \\ | 0 | 2 | Y | 120 | Y |  | Isola M - G117002 | 2 | 1.55 |  |
|  |  | BB000022 | G-AL SI 7 MG TI BDS - 06.08 |  | 3.59 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | BB010002_PH | RETE FILTRAGGIO H.80 L.130 AL308 F | buy | 0.25 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Cutting | 20E22202_CUT |  |  | 2 |  | 1900 | 380 | 2200 | \\ | \\ | \\ | 0 | 1 | Y | 120 | Y |  | G219002 |  | 0.33 |  |
|  |  | P00190000 | SFRIDO ALLUMINIO | in house | -0.0164 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | P00880000_PH | G-AL SI 7  SFRIDO ALL.TAB.06.08 | in house | -1.2538 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20E22302_042 | MELTED HALF CALIPER | in house | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20E22302_CUT |  | in house | -2 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Cutting | 20E22302_CUT |  | in house | 2 |  | 1900 | 380 | 2200 | \\ | \\ | \\ | 0 | 1 | Y | 120 | Y |  | G219002 |  | 0.33 |  |
|  |  | P00190000 | SFRIDO ALLUMINIO | in house | -0.0135 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | P00880000_PH | G-AL SI 7  SFRIDO ALL.TAB.06.08 | in house | -1.0313 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20E22302_042 | MELTED HALF CALIPER | in house | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20E22202_CUT |  |  | -2 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Heat Treatment | 20E22202_HTT | Alsi7P | in house | 1 |  | 1900 | 380 | 2200 | \\ | \\ | \\ | 0 | 2 | Y | 624 | N |  | G303032 | 624 | 70 |  |
|  |  | 20E22202_CUT |  |  | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Heat Treatment | 20E22302_HTT | Alsi7P | in house | 1 |  | 1900 | 380 | 2200 | \\ | \\ | \\ | 0 | 2 | Y | 720 | N |  | G303032 | 720 | 70 |  |
|  |  | 20E22302_CUT |  |  | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Finishing | 20E22202 | Alsi7P | SUBCO | 1 |  | 1900 | 380 | 2200 | \\ | \\ | \\ | 0 | 3 | Y | 624 | N |  | G500100 |  | ? |  |
|  |  | BB000010 | SFRIDO LAVORAZIONI ESTERNE |  | -0.0164 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20E22202_HTT |  |  | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Finishing | 20E22203 | Alsi7P | SUBCO | 1 |  | 1900 | 380 | 2200 | \\ | \\ | \\ | 0 | 3 | Y | 720 | N |  | G500100 |  | ? |  |
|  |  | BB000010 | SFRIDO LAVORAZIONI ESTERNE |  | -0.0135 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20E22302_HTT |  |  | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| FOUNDRY |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F5<br>Cofuso <br><br>19D41120 | Core shop | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0010 |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0020 |  |  |  |  |
|  | Casting | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Cutting | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Heat Treatment | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Finishing | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | X-ray | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Shot blasting | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| FRICTION |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F2<br><br>Mixing complesso 1 [PORSCHE ??]<br>To be defined | Mixing | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0010 |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0020 |  |  |  |  |
|  | Molding & Heat Treatment | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Grinding & Scorching | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Sandblasting & Painting | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Component |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Metal sheet application<br>SUBCONTRACTING | Manufactured Product |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| MACHINING |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F2<br>PORSCHE<br><br>20D49837/38 | First Machining |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0010 |  |  |  |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0020 |  |  |  |  |
|  | First & Second Machining w/o Washing | 20D49937_LSM |  | MAKE |  |  | 10 | 1 | 800 |  |  | 80 |  | 3 |  |  |  | OP0010 | A598002 | 1 | 2.25 |  |
|  |  | 20D49901 | CORPO PINZA GREZZO SX | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | P00190000 | SFRIDO ALLUMINIO |  | -0.561 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | First & Second Machining w/o Washing | 20D49938_LSM |  | MAKE |  |  | 10 | 1 | 800 |  |  | 80 |  | 3 |  |  |  | OP0010 | A598002 | 1 | 2.25 |  |
|  |  | 20D49902 | CORPO PINZA GREZZO DX | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | P00190000 | SFRIDO ALLUMINIO |  | -0.561 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Washing | 20D49937_WSH |  | MAKE |  |  | 10 | 1 | 800 |  |  | 80 |  | 1 |  |  |  | OP0010 | A601002 | 1 | 1.7 |  |
|  |  | 20D49937_LSM |  | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Washing | 20D49938_WSH |  | MAKE |  |  | 10 | 1 | 800 |  |  | 80 |  | 1 |  |  |  | OP0010 | A601002 | 1 | 1.7 |  |
|  |  | 20D49938_LSM |  | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Oxidation | 20D49937_OXD |  | MAKE |  |  | 10 | 1 | 800 |  |  | 80 |  | 3 |  |  |  | OP0010 | A319002 | 80 | 10.5 |  |
|  |  | 20D49937_WSH |  | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Oxidation | 20D49938_OXD |  | MAKE |  |  | 10 | 1 | 800 |  |  | 80 |  | 3 |  |  |  | OP0010 | A319002 | 80 | 10.5 |  |
|  |  | 20D49938_WSH |  | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Cleaning | 20D49937 |  | MAKE |  |  | 5 | 1 | 400 |  |  | 40 |  | 1 |  |  |  | OP0010 | A799502 | 1 | 2.5 |  |
|  |  | 20D49937_OXD | CORPO PINZA GREZZO SX | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  |  | SFRIDO ALLUMINIO |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Cleaning | 20D49938 |  | MAKE |  |  | 5 | 1 | 400 |  |  | 40 |  | 1 |  |  |  | OP0010 | A799502 | 1 | 2.5 |  |
|  |  | 20D49938_OXD | CORPO PINZA GREZZO DX | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  |  | SFRIDO ALLUMINIO |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ASSEMBLY | Pre-Assembly |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0010 |  |  |  |  |
| SCENARIO F2<br>Porsche<br><br>20D49835/6<br> |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0020 |  |  |  |  |
|  | First Assembly |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Painting | 20D499AU |  | MAKE |  |  | 5 | 1 | 400 |  |  | 40 |  | 5 |  |  |  | OP0010 | A800002 | 1 | 0.4 |  |
|  |  | 20D49937 | CORPO PINZA FINITO SX | MAKE | 1 | nr |  | 1 | 1 |  |  | 1 |  |  |  |  |  | OP0020 | A800102 | 1 | 0.72 |  |
|  |  | 1PAN | VERNICE GIALLA 1PAN | BUY | 60 | g |  | 200 | 2000 |  |  | 2000 |  |  |  |  |  |  |  |  |  |  |
|  |  | 04E80391 | BOLLINO TERMOCROMICO IRREVERSIBILE | BUY | 1 | nr |  | 102 | 1020 |  |  | 1020 |  |  |  |  |  |  |  |  |  |  |
|  | Painting | 20D499BU |  | MAKE |  |  | 5 | 1 | 400 |  |  | 40 |  | 5 |  |  |  | OP0010 | A800002 | 1 | 0.4 |  |
|  |  | 20D49938 | CORPO PINZA FINITO DX | MAKE | 1 | nr |  | 1 | 1 |  |  | 1 |  |  |  |  |  | OP0020 | A800102 | 1 | 0.72 |  |
|  |  | 1PAN | VERNICE GIALLA 1PAN | BUY | 60 | g |  | 200 | 2000 |  |  | 2000 |  |  |  |  |  |  |  |  |  |  |
|  |  | 04E80391 | BOLLINO TERMOCROMICO IRREVERSIBILE | BUY | 1 | nr |  | 102 | 1020 |  |  | 1020 |  |  |  |  |  |  |  |  |  |  |
|  | Full Assembly | 20D49835 |  | MAKE |  |  | 3 | 1 | 240 |  |  | 24 |  | 1 | NO |  | NO | OP0010 | A425402 | 1 | 2.5 |  |
|  |  | 20D499AU | CORPO PINZA LAVORATO | MAKE |  |  | 5 | 1 | 360 |  |  | 36 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05B03387 | VITE | BUY | 4 | nr | 5 | 1 | 200 |  |  | 200 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 04D80212 | DISTANZIALE | BUY | 1 | nr | 5 | 1 | 500 |  |  | 500 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 20487237 | CUFFIA PARAPOLVERE | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | D10419000 | Grasso Kluberbeta RM 47-102 | BUY | 0.25 | g | 5 | 1 | 250 |  |  | 250 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 | 150 |  |  | 150 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 07D50012 | PASTIGLIA | BUY | 2 | nr | 3 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | D10105000 | FLUIDO BREOX B-225 | BUY | 0.24 | g | 5 | 1 | 410 |  |  | 410 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 06213519 | TAPPO | BUY | 2 | nr | 5 | 1 | 100 |  |  | 1 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20697749 | PISTONE | BUY | 6 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05C33240 | MOLLA | BUY | 2 | nr | 0 | 2500 | 250 |  |  | 250 |  | 0 |  |  |  |  |  |  |  |  |
|  |  | 20487238 | CUFFIA PARAPOLVERE DIAM.24 | BUY | 6 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05C87616 | GUARNIZIONE DI TENUTA | BUY | 6 | nr | 5 | 1 | 150 |  |  | 150 |  | 20 |  |  |  |  |  |  |  |  |
|  |  | 20697748 | PISTONE | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05150220 | PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 100 |  |  | 100 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 06C39093 | TUBO RIGIDO COMPLETO | MAKE | 1 | nr | 1 | 1 | 100 |  |  | 1 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05C87615 | GUARNIZIONE DI TENUTA | BUY | 4 | nr | 5 | 1 | 150 |  |  | 150 |  | 20 |  |  |  |  |  |  |  |  |
|  |  | 20668823 | SPINOTTO ZIGRINATO | BUY | 4 | nr | 5 | 1 | 200 |  |  | 200 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05281228 | TAPPO DI SPURGO | BUY | 2 | nr | 5 | 1200 | 120 |  |  | 120 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 07D08942 | SEGNALATORE DI USURA | BUY | 1 | nr | 5 | 500 | 500 |  |  | 500 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 98499933 | ETICHETTA | BUY | 1 | nr | 5 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 98512698 | ETICHETTA AUTOADESIVA BIANCA | BUY | 1 | nr | 5 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  | Full Assembly | 20D49836 |  | MAKE |  |  | 3 | 1 | 240 |  |  | 24 |  | 1 | NO |  | NO | OP0010 | A425402 | 1 | 2.5 |  |
|  |  | 20D499BU | CORPO PINZA LAVORATO | MAKE | 1 | nr | 5 | 1 | 360 |  |  | 36 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05B03387 | VITE | BUY | 4 | nr | 5 | 1 | 200 |  |  | 200 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 04D80212 | DISTANZIALE | BUY | 1 | nr | 5 | 1 | 500 |  |  | 500 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 20487237 | CUFFIA PARAPOLVERE | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | D10419000 | Grasso Kluberbeta RM 47-102 | BUY | 0.25 | g | 5 | 1 | 250 |  |  | 250 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 | 150 |  |  | 150 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 07D50012 | PASTIGLIA | BUY | 2 | nr | 3 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | D10105000 | FLUIDO BREOX B-225 | BUY | 0.24 | g | 5 | 1 | 410 |  |  | 410 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 06213519 | TAPPO | BUY | 2 | nr | 5 | 1 | 100 |  |  | 1 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20697749 | PISTONE | BUY | 6 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05C33240 | MOLLA | BUY | 2 | nr | 0 | 1 | 250 |  |  | 250 |  | 0 |  |  |  |  |  |  |  |  |
|  |  | 20487238 | CUFFIA PARAPOLVERE DIAM.24 | BUY | 6 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05C87616 | GUARNIZIONE DI TENUTA | BUY | 6 | nr | 5 | 1 | 150 |  |  | 150 |  | 20 |  |  |  |  |  |  |  |  |
|  |  | 20697748 | PISTONE | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05150220 | PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 100 |  |  | 100 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 06C39093 | TUBO RIGIDO COMPLETO | MAKE | 1 | nr | 1 | 1 | 100 |  |  | 1 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05C87615 | GUARNIZIONE DI TENUTA | BUY | 4 | nr | 5 | 1 | 150 |  |  | 150 |  | 20 |  |  |  |  |  |  |  |  |
|  |  | 20668823 | SPINOTTO ZIGRINATO | BUY | 4 | nr | 5 | 1 | 200 |  |  | 200 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05281228 | TAPPO DI SPURGO | BUY | 2 | nr | 5 | 1 | 120 |  |  | 120 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 07D08942 | SEGNALATORE DI USURA | BUY | 1 | nr | 5 | 500 | 500 |  |  | 500 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 98499933 | ETICHETTA | BUY | 1 | nr | 5 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 98512698 | ETICHETTA AUTOADESIVA BIANCA | BUY | 1 | nr | 5 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  | Full Assembly | 06C39093 |  | MAKE |  |  | 5 | 50 | 2500 |  |  | 250 |  | 3 |  |  | NO | OP0010 | A480002 | 1 | 0.28 |  |
|  |  | 06228864 | RACCORDO | BUY | 2 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 06385246 | GUAINA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 06401812 | TUBO RIGIDO BUNDY+PVF | BUY | 0.25 | m |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| MACHINING |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F4<br>SUBARU<br><br>20E22231/32<br>20E22331/32 | First Machining |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0010 |  |  |  |  |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | OP0020 |  |  |  |  |
|  | Second Machining |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | First & Second Machining w/o Washing | 20E22231_LSM |  |  |  |  | 10 | 1 | 800 |  |  | 80 |  | 3 |  |  | YES | OP0010 | A596002 | 1 | 2.05 |  |
|  |  | 20E22202 | SEMIPINZA C.O. GREZZA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | P00190000 | SFRIDO ALLUMINIO |  | -0.56 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | CONSUTE_PH | CONSUTE_PH |  | 14.4 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Washing | 20E22231_WSH |  |  |  |  | 10 | 1 | 800 |  |  | 80 |  | 1 |  |  | YES | OP0010 | A601002 | 1 | 0.5 |  |
|  |  | 20E22231_LSM |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Oxidation | 20E22231 |  |  |  |  | 10 | 1 | 800 |  |  | 80 |  | 3 |  |  | YES | OP0010 | A319002 | 160 | 10.5 |  |
|  |  | 20E22231_WSH |  | MAKE |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05385106 | TAPPO DI PROTEZIONE | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Cleaning |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Finishing body |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ASSEMBLY |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F4<br>SUBARU<br><br>20E22121/22 | First Assembly | 20E221AA |  | MAKE |  |  | 5 | 1 | 480 |  |  | 48 |  | 3 |  |  | NO | OP0010 | A402202 | 1 | 1.75 |  |
|  |  | 20E22231 | semipinza | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  | YES |  |  |  |  |  |
|  |  | 20E22331 | semipinza | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  | YES |  |  |  |  |  |
|  |  | 05223220 | GUARNIZIONE | BUY | 1 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05281228 | TAPPO DI SPURGO | BUY | 2 | nr | 5 | 1200 | 120 |  |  | 120 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05385113 | TAPPO A PERDERE | BUY | 1 | nr | 5 | 1 | 600 |  |  | 600 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05401160 | GUARNIZIONE | BUY | 1 | nr | 5 | 1 | 200 |  |  | 200 |  | 15 |  |  |  |  |  |  |  |  |
|  |  | 05547473 | BOCCOLA | BUY | 2 | nr | 5 | 1 | 300 |  |  | 300 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05595518 | GUARNIZIONE DI TENUTA | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05877463 | VITE TE M12X1,75X80 | BUY | 4 | nr | 5 | 1 | 120 |  |  | 120 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 06213519 | TAPPO | BUY | 2 | nr | 5 | 1 | 100 |  |  | 1 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20487246 | CUFFIA PARAPOLVERE | BUY | 4 | nr | 5 | 1 | 700 |  |  | 700 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20C80207 | PISTONE | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | D10105000 |  | BUY | 0.2 | g | 5 | 1 | 410 |  |  | 410 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | D10419000 |  | BUY | 0.27 | g | 5 | 1 | 250 |  |  | 25000 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 98512698 |  | BUY | 2 | nr | 5 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  | First Assembly | 20E221BA |  | MAKE |  |  | 5 | 1 | 480 |  |  | 48 |  | 3 |  |  | NO | OP0010 | A402202 | 1 | 1.75 |  |
|  |  | 20E22232 | semipinza | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  | YES |  |  |  |  |  |
|  |  | 20E22332 | semipinza | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  | YES |  |  |  |  |  |
|  |  | 05223220 | GUARNIZIONE | BUY | 1 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05281228 | TAPPO DI SPURGO | BUY | 2 | nr | 5 | 1200 | 120 |  |  | 120 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05385113 | TAPPO A PERDERE | BUY | 1 | nr | 5 | 1 | 600 |  |  | 600 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05401160 | GUARNIZIONE | BUY | 1 | nr | 5 | 1 | 200 |  |  | 200 |  | 15 |  |  |  |  |  |  |  |  |
|  |  | 05547473 | BOCCOLA | BUY | 2 | nr | 5 | 1 | 300 |  |  | 300 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05595518 | GUARNIZIONE DI TENUTA | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05877463 | VITE TE M12X1,75X80 | BUY | 4 | nr | 5 | 1 | 120 |  |  | 120 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 06213519 | TAPPO | BUY | 2 | nr | 5 | 1 | 100 |  |  | 1 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20487246 | CUFFIA PARAPOLVERE | BUY | 4 | nr | 5 | 1 | 700 |  |  | 700 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20C80207 | PISTONE | BUY | 4 | nr | 5 | 1 | 100 |  |  | 1 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | D10105000 |  | BUY | 0.2 | g | 5 | 1 | 410 |  |  | 410 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | D10419000 |  | BUY | 0.27 | g | 5 | 1 | 250 |  |  | 250 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 98512698 |  | BUY | 2 | nr | 5 | 1 | 100 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  | Painting | 20E221AC |  | SUBCO |  |  | 5 | 1 | 480 |  |  | 48 |  | 10 |  |  | NO | OP0010 | A500160 | 1 |  |  |
|  |  | 20E221AA | caliper | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Painting | \\ |  | SUBCO |  |  | 5 |  | 480 |  |  | 48 |  | 10 |  |  | NO | OP0010 | A500160 | 1 |  |  |
|  |  | 20E221BA | caliper | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Second Assembly | 20E22121 |  | MAKE |  |  | 3 | 1 | 800 |  |  | 80 |  | 1 | NO |  | NO | OP0010 | A402I02 | 1 | 2.3 |  |
|  |  | 20E221AC | caliper | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  | OP0020 | A409002 | 1 | 0.01 |  |
|  |  | 47E67310 | pad | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 47E67312 | pad | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05150220 | PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 100 |  |  | 100 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 | 150 |  |  | 150 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05442461 | VITE | BUY | 4 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05454227 | COPIGLIA | BUY | 2 | nr | 5 | 1 | 140 |  |  | 140 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 20419665 | MOLLA | BUY | 1 | nr | 5 | 1 | 170 |  |  | 170 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20451769 | LAMIERINO | BUY | 4 | nr | 5 | 1 | 900 |  |  | 900 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20490811 | PERNO | BUY | 2 | nr | 5 | 1 | 500 |  |  | 500 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | D10416000 | GRASSO MOLYKOTE CU7439 V1 | BUY | 2,34 | g | 5 | 1 | 180 |  |  | 180 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 98499933 | ETICHETTA | BUY | 1 | nr | 5 | 1 | 1 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  | Second Assembly | 20E22122 |  | MAKE |  |  | 3 | 1 | 800 |  |  | 80 |  | 1 | NO |  | NO | OP0010 | A402I02 | 1 | 2.3 | 0.75 |
|  |  | 20E221BC | caliper | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  | OP0020 | A409002 | 1 | 0.01 | 0.75 |
|  |  | 47E67311 | pad | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 47E67313 | pad | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05150220 | PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 100 |  |  | 100 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 | 150 |  |  | 150 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05442461 | VITE | BUY | 4 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05454227 | COPIGLIA | BUY | 2 | nr | 5 | 1 | 140 |  |  | 140 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 20419665 | MOLLA | BUY | 1 | nr | 5 | 1 | 170 |  |  | 170 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20451769 | LAMIERINO | BUY | 4 | nr | 5 | 1 | 900 |  |  | 900 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 20490811 | PERNO | BUY | 2 | nr | 5 | 1 | 500 |  |  | 500 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | D10416000 | GRASSO MOLYKOTE CU7439 V1 | BUY | 2,34 | g | 5 | 1 | 180 |  |  | 180 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 98499933 | ETICHETTA | BUY | 1 | nr | 5 | 1 | 1 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
| FRICTION |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F4<br><br>Mixing complesso 1 [SUBARU]<br>47E67310/11/12/13 | Mixing | MMLA0014 |  | MAKE |  | kg | 5 | 1 | 1650 |  |  | 165 |  | 1 | NO |  | NO | OP0010 | F100002 | 1 | 1.5 | 0.75 |
|  |  | AG023000 | IDROSSIDO DI CALCIO 1 | BUY | 0.02 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LG013000 | GRAFITE 6 | BUY | 0.05 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | MP026000 | POLVERE DI FERRO-STAGNO-BISMUTO 1 | BUY | 0.057 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AH002000 | OSSIDO DI ALLUMINIO 4 | BUY | 0.009 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LK003000 | COKE 3 | BUY | 0.07 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | RP002000 | RESINA FENOLICA 4 | BUY | 0.065 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AG008000 | ZINCO OSSIDO 1 | BUY | 0.02 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LG003000 | GRAFITE 3 | BUY | 0.01 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | MF004000 | FIBRA ACCIAIO 3 | BUY | 0.14 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AG004000 | CROMITE 1 | BUY | 0.06 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AH015000 | CARBURO DI SILICIO 4 | BUY | 0.017 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LS004000 | SOLFURO MISTO 2 | BUY | 0.06 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AH003000 | CARBURO DI SILICIO 3 | BUY | 0.002 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LK008000 | COKE 4 | BUY | 0.04 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | RP008000 | POLVERE DI FRIZIONE 2 | BUY | 0.015 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AG006000 | OSSIDO DI MAGNESIO 1 | BUY | 0.06 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | FB005000 | FIBRA ARAMIDICA 1 | BUY | 0.03 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LS015000 | SOLFURO DI ZINCO 2 | BUY | 0.03 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AG013000 | PFTE 2 | BUY | 0.01 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LG009000 | GRAFITE 5 | BUY | 0.03 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | MP011000 | POLVERE DI ZINCO 1 | BUY | 0.04 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AG002000 | VERMICULITE 2 | BUY | 0.05 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AH005000 | OSSIDO DI ALLUMINIO 5 | BUY | 0.06 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | LS003000 | SOLFURO DI FERRO 1 | BUY | 0.03 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | RP028000 | POLVERE DI FRIZIONE 3 | BUY | 0.025 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Mixing | MULA0001 |  | MAKE |  |  | 5 | 1 | 60 |  |  | 6 |  | 1 | NO |  | NO | OP0010 | F110002 | 1 | 4 | 0.75 |
|  |  | RB001000 | NBR 1 | BUY | 0.06 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | RP006000 | RESINA FENOLICA 3 | BUY | 0.04 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | MF003000 | FIBRA ACCIAIO 2 | BUY | 0.6 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | FB004000 | FIBRA ARAMIDICA 2 | BUY | 0.1 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | AG018000 | BARITE 1 | BUY | 0.195 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Mixing | 47E67300SA | PIASTRINA CON COLLA | SUBCO |  |  | 5 | 1 | 42500 |  |  | 4250 |  | 5 | NO |  | NO | OP0010 | A500580 | 1 |  |  |
|  |  | 47E67300 | PIASTRINA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | gluing | 47E67300CO | PIASTRINA CON COLLA | MAKE |  |  | 5 | 1 | 5000 |  |  | 500 |  | 1 | NO |  | NO | OP0010 | F150002 | 1 | 0.1 | 0.75 |
|  |  | 47E67300SA | PIASTRINA SABBIATA | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | VF048000 | COLLA 4 | BUY | 0.01 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Molding & Heat Treatment | 47E67310_MHT |  |  |  |  | 5 | 1 | 5000 |  |  | 500 |  | 3 | YES (per passare alla fase successiva) | 500 | NO | OP0010 | F173002 | 1 | 1.75 | 0.75 |
|  |  | 47E67300CO | PIASTRINA CON COLLA | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  | OP0020 | F330002 | 1 | 0.5 | 0.75 |
|  |  | MMLA0014 | Mescola BRM0018 GG e /1 | MAKE | 0.135 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | MULA0001 | UL001_001 UNDER LAYER | MAKE | 0.05 | kg |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Grinding & Scorching | 47E67310_GSC |  | MAKE |  |  | 5 | 1 | 5000 |  |  | 500 |  | 4 | YES (per passare alla fase successiva) | 480 | NO | OP0010 | F580002 | 1 | 0.2 | 0.75 |
|  |  | 47E67310_MHT |  | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  | OP0020 | F361002 | 1 | 0.39 | 0.75 |
|  | Shot blasting & Painting | 47E67310_SBP |  | MAKE |  |  | 5 | 1 | 5000 |  |  | 500 |  | 3 | YES (per passare alla fase successiva) | 460 | NO | OP0010 | F621002 | 1 | 0.3 | 0.75 |
|  |  | 47E67310_GSC |  | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  | OP0020 | F990002 | 1 | 0.25 | 0.75 |
|  | Metal sheet application<br>SUBCONTRACTING | 47E67310 | PAD | SUBCO |  |  | 5 | 1 | 5000 |  |  | 500 |  | 5 | YES | 450 | NO | OP0010 | A500830 | 1 |  |  |
|  |  | 47E67310_SBP | PAD | MAKE | 1 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 04B52764 | ETICHETTA | BUY | 1 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 07355190 | SEGNALATORE ACUSTICO | BUY | 1 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20E67122 | LAMIERA ANTIRUMORE | BUY | 1 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ASSEMBLY |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SCENARIO F1<br>FERRARI<br><br>26D66814 | First Assembly | 20C837CA |  | MAKE |  |  | 5 | 1 | 480 |  |  | 48 |  | 1 |  |  |  | OP0010 | A403302 | 1 | 2.3 |  |
|  |  | 20B93291 | CORPO PINZA FINITO SX | MAKE | 1 | nr | 5 | 1 | 500 |  |  | 50 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 06B26442 | TUBO RIGIDO COMPLETO | MAKE | 1 | nr | 3 | 1 | 2500 |  |  | 250 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05281228 | TAPPO DI SPURGO | BUY | 2 | nr | 5 | 12 | 120 |  |  | 120 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05769145 | GUARNIZIONE DI TENUTA | BUY | 2 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20487245 | CUFFIA PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 800 |  |  | 800 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05769143 | GUARNIZIONE DI TENUTA | BUY | 2 | nr | 5 | 1 | 200 |  |  | 200 |  | 15 |  |  |  |  |  |  |  |  |
|  |  | 20487243 | CUFFIA PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 100 |  |  | 100 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05B03367 | VITE | BUY | 3 | nr | 5 | 1 | 100 |  |  | 100 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20668822 | SPINOTTO DIAM.14 ZIGRINATO | BUY | 4 | nr | 5 | 1 | 128 |  |  | 128 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | D10105000 | FLUIDO BREOX B-225 | BUY | 0.16 | g | 5 | 1 | 410 |  |  | 410 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05385113 | TAPPO A PERDERE | BUY | 1 | nr | 5 | 1 | 600 |  |  | 600 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05223220 | GUARNIZIONE | BUY | 1 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20A27724 | PISTONE COMPLETO DIAM.34 | BUY | 2 | nr | 5 | 1 | 54 |  |  | 54 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 20A27726 | PISTONE COMPLETO DIAM.38 | BUY | 2 | nr | 5 | 1 | 54 |  |  | 54 |  | 2 |  |  |  |  |  |  |  |  |
|  | First Assembly | 20C837DA |  | MAKE |  |  | 5 | 1 | 480 |  |  | 48 |  | 1 |  |  |  | OP0010 | A403302 | 1 | 2.3 |  |
|  |  | 20B93292 | CORPO PINZA FINITO SX | MAKE | 1 | nr | 5 | 1 | 500 |  |  | 50 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 06B26452 | TUBO RIGIDO COMPLETO | MAKE | 1 | nr | 3 | 1 | 2500 |  |  | 250 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05281228 | TAPPO DI SPURGO | BUY | 2 | nr | 5 | 12 | 120 |  |  | 120 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05769145 | GUARNIZIONE DI TENUTA | BUY | 2 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20487245 | CUFFIA PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 800 |  |  | 800 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05769143 | GUARNIZIONE DI TENUTA | BUY | 2 | nr | 5 | 1 | 200 |  |  | 200 |  | 15 |  |  |  |  |  |  |  |  |
|  |  | 20487243 | CUFFIA PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 100 |  |  | 100 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05B03367 | VITE | BUY | 3 | nr | 5 | 1 | 100 |  |  | 100 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20668822 | SPINOTTO DIAM.14 ZIGRINATO | BUY | 4 | nr | 5 | 1 | 128 |  |  | 128 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | D10105000 | FLUIDO BREOX B-225 | BUY | 0.16 | g | 5 | 1 | 410 |  |  | 410 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05385113 | TAPPO A PERDERE | BUY | 1 | nr | 5 | 1 | 600 |  |  | 600 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05223220 | GUARNIZIONE | BUY | 1 | nr | 5 | 1 | 250 |  |  | 250 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 20A27724 | PISTONE COMPLETO DIAM.34 | BUY | 2 | nr | 5 | 1 | 54 |  |  | 54 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 20A27726 | PISTONE COMPLETO DIAM.38 | BUY | 2 | nr | 5 | 1 | 54 |  |  | 54 |  | 2 |  |  |  |  |  |  |  |  |
|  | Painting | 20C837CF |  | SUBCO |  |  | 5 | 1 | 360 |  |  | 36 |  | 10 |  |  | NO | OP0010 | A500160 | 1 |  |  |
|  |  | 20C837CA | caliper | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Painting | 20C837DF |  | SUBCO |  |  | 5 |  | 360 |  |  | 36 |  | 10 |  |  | NO | OP0010 | A500160 | 1 |  |  |
|  |  | 20C837DA | caliper | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | First Assembly | 22C0402E |  | MAKE |  |  | 5 |  | 360 |  |  | 36 |  | 10 | YES (con la fase successiva) | 36 | NO | OP0010 | A401302 | 1 | 2.5 |  |
|  |  | 22B93433 | CORPOPINZAFINITOSX | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 40B81306 | MOTO-RIDUTTORE | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | A60201025 | ANELLO ELASTICO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05394113 | DISTANZIALE IN POLISTIROLO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10414000 | GRASSO KLUEBER GLK1PF | BUY | 0.01 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | A60101015 | ANELLO ELASTICO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20487244 | CUFFIA PARAPOLVERE | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484255 | RONDELLA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05595596 | GUARNIZIONE DI TENUTA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10428000 | GRASSO NYE RHEOLUBE 380 | BUY | 0.15 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484253 | RALLA | BUY | 2 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484321 | GABBIA A RULLINI | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484254 | MOLLA ONDULATA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05B03302 | VITE PER FISSAGGIO MASSE F142/F150 | BUY | 3 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05255451 | O-RING | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22461040 | MADREVITE | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22460920 | VITE DI MANOVRA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 06213580 | PERNO ANTIROTAZIONE | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10407000 | PASTA AL SILICONE TKM 1011 | BUY | 0.08 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20668850 | GUIDA SECONDARIA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22B93531 | REAZIONE FINITA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05998705 | VITE M10X1,5X70 | BUY | 2 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22592351 | PISTONE FINITO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | First Assembly | 22C0402F |  | MAKE |  |  | 5 |  | 360 |  |  | 36 |  | 5 | YES (con la fase successiva) | 36 | NO | OP0010 | A401302 | 1 | 2.5 |  |
|  |  | 22B93434 | CORPOPINZAFINITOSX | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 40B81306 | MOTO-RIDUTTORE | SUBCO | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | A60201025 | ANELLO ELASTICO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05394113 | DISTANZIALE IN POLISTIROLO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10414000 | GRASSO KLUEBER GLK1PF | BUY | 0.01 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | A60101015 | ANELLO ELASTICO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20487244 | CUFFIA PARAPOLVERE | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484255 | RONDELLA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05595596 | GUARNIZIONE DI TENUTA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10428000 | GRASSO NYE RHEOLUBE 380 | BUY | 0.15 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484253 | RALLA | BUY | 2 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484321 | GABBIA A RULLINI | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22484254 | MOLLA ONDULATA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05B03302 | VITE PER FISSAGGIO MASSE F142/F150 | BUY | 3 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05255451 | O-RING | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22461040 | MADREVITE | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22460920 | VITE DI MANOVRA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 06213580 | PERNO ANTIROTAZIONE | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10407000 | PASTA AL SILICONE TKM 1011 | BUY | 0.08 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20668850 | GUIDA SECONDARIA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22B93531 | REAZIONE FINITA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05998705 | VITE M10X1,5X70 | BUY | 2 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22592351 | PISTONE FINITO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Second Assembly | 22C04027 |  | MAKE |  |  | 5 |  | 360 |  |  | 36 |  | 5 | YES (con la fase precedente) | 36 | NO | OP0010 | A401202 | 1 | 1.7 |  |
|  |  | 22C0402E | 1° MONTAGGIO EP 173 | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 47C12311 | PASTIGLIA Ferrari ECM Post BRM0004 GG | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 47C12313 | PASTIGLIA Ferrari ECM Post BRM0004 GG | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20451951 | MOLLA A FILO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20451952 | MOLLA A FILO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10414000 | GRASSO KLUEBER GLK1PF | BUY | 0.01 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22464641 | CUFFIA PARAPOLVERE | BUY | 2 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22464581 | BUSSOLA GUIDA PRIMARIA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05454227 | COPIGLIA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22483895 | PERNO LAVORATO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 98512698 | ETICHETTA AUTOADESIVA BIANCA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Second Assembly | 22C04028 |  | MAKE |  |  | 5 |  | 360 |  |  | 36 |  | 5 | YES (con la fase precedente) | 36 | NO | OP0010 | A401202 | 1 | 1.7 |  |
|  |  | 22C0402F | 1° MONTAGGIO EP 173 | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 47C12311 | PASTIGLIA Ferrari ECM Post BRM0004 GG | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 47C12313 | PASTIGLIA Ferrari ECM Post BRM0004 GG | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20451951 | MOLLA A FILO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 20451952 | MOLLA A FILO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | D10414000 | GRASSO KLUEBER GLK1PF | BUY | 0.01 | g |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22464641 | CUFFIA PARAPOLVERE | BUY | 2 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22464581 | BUSSOLA GUIDA PRIMARIA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 05454227 | COPIGLIA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 22483895 | PERNO LAVORATO | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 98512698 | ETICHETTA AUTOADESIVA BIANCA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Second Assembly | 20D66647 |  | MAKE |  |  | 3 | 1 |  |  |  |  |  |  |  |  | NO | OP0010 | A403902 | 1 | 3.5 |  |
|  |  | 20C837CF | PINZA MT 4.34 /38 GIALLO SX | SUBCO | 1 | nr | 5 | 1 | 360 |  |  | 36 |  | 10 |  |  |  |  |  |  |  |  |
|  |  | 22C04027 | PINZA EP SX | MAKE | 1 | nr | 1 | 1 | 360 |  |  | 36 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 747B94918 | PASTIGLIA BRM0004 GG | MAKE | 1 | nr | 1 | 1 | 240 |  |  | 24 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 747B94919 | PASTIGLIA BRM0004 GG | MAKE | 1 | nr | 1 | 1 | 240 |  |  | 24 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05150210 | PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 200 |  |  | 200 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05894889 | MOLLA COMPLETA | BUY | 2 | nr | 5 | 1 | 500 |  |  | 500 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 | 150 |  |  | 150 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 98499933 | ETICHETTA | BUY | 1 | nr | 5 | 1 | 900 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 07A76208 | SEGNALATORE D'USURA | BUY | 1 | nr | 3 | 200 | 200 |  |  | 200 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | D10414000 | GRASSO KLUEBER GLK1PF | BUY | 0.05 | g | 5 | 1 | 250 |  |  | 250 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 22464880 | BUSHING GUIDA SECONDARIA | BUY | 1 | nr | 5 | 1 | 500 |  |  | 500 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05385180 | TAPPO | BUY | 1 | nr | 5 | 1 | 200 |  |  | 200 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05B03345 | VITE M8X80 | BUY | 1 | nr | 5 | 1 | 100 |  |  | 100 |  | 0 |  |  |  |  |  |  |  |  |
|  |  | 05877403 | VITE | BUY | 1 | nr | 5 | 1 | 250 |  |  | 250 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05894896 | MOLLA COMPLETA | BUY | 1 | nr | 5 | 1 | 900 |  |  | 900 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 20990904 | BLOCCHETTO | BUY | 1 | nr | 5 | 1 | 900 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 98512698 | ETICHETTA AUTOADESIVA BIANCA | BUY | 1 | nr | 5 | 1 | 900 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  | Second Assembly | 20D66648 |  | MAKE |  |  | 3 | 1 |  |  |  |  |  |  |  |  | NO | OP0010 | A403902 | 1 | 3.5 |  |
|  |  | 20C837DF | PINZA MT 4.34 /38 GIALLO SX | SUBCO | 1 | nr | 5 | 1 | 360 |  |  | 36 |  | 10 |  |  |  |  |  |  |  |  |
|  |  | 22C04028 | PINZA EP SX | MAKE | 1 | nr | 1 | 1 | 360 |  |  | 36 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 747B94918 | PASTIGLIA BRM0004 GG | MAKE | 1 | nr | 1 | 1 | 240 |  |  | 24 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 747B94919 | PASTIGLIA BRM0004 GG | MAKE | 1 | nr | 1 | 1 | 240 |  |  | 24 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05150210 | PARAPOLVERE | BUY | 2 | nr | 5 | 1 | 200 |  |  | 200 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05894889 | MOLLA COMPLETA | BUY | 2 | nr | 5 | 1 | 500 |  |  | 500 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 | 150 |  |  | 150 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 98499933 | ETICHETTA | BUY | 1 | nr | 5 | 1 | 900 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 07A76208 | SEGNALATORE D'USURA | BUY | 1 | nr | 3 | 200 | 200 |  |  | 200 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | D10414000 | GRASSO KLUEBER GLK1PF | BUY | 0.05 | g | 5 | 1 | 250 |  |  | 250 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 22464880 | BUSHING GUIDA SECONDARIA | BUY | 1 | nr | 5 | 1 | 500 |  |  | 500 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05385180 | TAPPO | BUY | 1 | nr | 5 | 1 | 200 |  |  | 200 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05B03345 | VITE M8X80 | BUY | 1 | nr | 5 | 1 | 100 |  |  | 100 |  | 0 |  |  |  |  |  |  |  |  |
|  |  | 05877403 | VITE | BUY | 1 | nr | 5 | 1 | 250 |  |  | 250 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 05894896 | MOLLA COMPLETA | BUY | 1 | nr | 5 | 1 | 900 |  |  | 900 |  | 5 |  |  |  |  |  |  |  |  |
|  |  | 20990904 | BLOCCHETTO | BUY | 1 | nr | 5 | 1 | 900 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 98512698 | ETICHETTA AUTOADESIVA BIANCA | BUY | 1 | nr | 5 | 1 | 900 |  |  | 1 |  | 3 |  |  |  |  |  |  |  |  |
|  | PHANTOM Assembly | 28D66727_PH | KIT VETTURA | MAKE |  |  | 3 | 1 | 10 |  |  | 1 |  | 1 |  |  |  |  |  |  |  |  |
|  |  | 20D66647 | PINZA ECM - MT4.34/38 + EP SX | MAKE | 1 | nr | 5 | 1 |  |  |  |  |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 28E184AA | SEMI MODULO POST F171 SX | MAKE | 1 | nr | 3 | 1 | 80 |  |  | 8 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 |  |  |  | 1500 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05877421 | VITE | BUY | 3 | nr | 5 | 1 |  |  |  | 3500 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 06466702 | SUPPORTO CAVO ABS       178938 | BUY | 1 | nr | 5 | 1 |  |  |  | 450 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 28B99335 | SUPPORTO CAVI COMPLETO | BUY | 1 | nr | 5 | 1 |  |  |  | 200 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05877413 | VITE TCEI M12X1.5X95 | BUY | 2 | nr | 5 | 1 |  |  |  | 100 |  | 5 |  |  |  |  |  |  |  |  |
|  | PHANTOM Assembly | 28D66728_PH | KIT VETTURA | MAKE |  |  | 3 | 1 | 10 |  |  | 1 |  | 1 |  |  |  |  |  |  |  |  |
|  |  | 20D66648 | PINZA ECM - MT4.34/38 + EP DX | MAKE | 1 | nr | 5 | 1 |  |  |  |  |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 28E184BA | SEMI MODULO POST F171 DX | MAKE | 1 | nr | 3 | 1 | 80 |  |  | 8 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 05385110 | TAPPO | BUY | 1 | nr | 5 | 1 |  |  |  | 1500 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 05877421 | VITE | BUY | 3 | nr | 5 | 1 |  |  |  | 3500 |  | 8 |  |  |  |  |  |  |  |  |
|  |  | 06466702 | SUPPORTO CAVO ABS       178938 | BUY | 1 | nr | 5 | 1 |  |  |  | 450 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 28B99336 | SUPPORTO CAVI COMPLETO | BUY | 1 | nr | 5 | 1 |  |  |  | 200 |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 05877413 | VITE TCEI M12X1.5X95 | BUY | 2 | nr | 5 | 1 |  |  |  | 100 |  | 5 |  |  |  |  |  |  |  |  |
|  | PHANTOM Assembly | 28D66527_PH | KIT VETTURA | MAKE |  |  | 3 | 1 | 10 |  |  | 1 |  | 1 |  |  |  |  |  |  |  |  |
|  |  | 20D66447 | PINZA M6.28/32/36 SX | MAKE | 1 | nr | 5 | 1 |  |  |  |  |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 28D665CA | SEMI MODULO ANT F171 SX | MAKE | 1 | nr | 3 | 1 | 80 |  |  | 8 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 05877413 | VITE TCEI M12X1.5X95 | BUY | 2 | nr | 5 | 1 |  |  |  | 100 |  | 5 |  |  |  |  |  |  |  |  |
|  | PHANTOM Assembly | 28D66528_PH | KIT VETTURA | MAKE |  |  | 3 | 1 | 10 |  |  | 1 |  | 1 |  |  |  |  |  |  |  |  |
|  |  | 20D66448 | PINZA M6.28/32/36 DX | MAKE | 1 | nr | 5 | 1 |  |  |  |  |  | 2 |  |  |  |  |  |  |  |  |
|  |  | 28D665DA | SEMI MODULO ANT F171 DX | MAKE | 1 | nr | 3 | 1 | 80 |  |  | 8 |  | 3 |  |  |  |  |  |  |  |  |
|  |  | 05877413 | VITE TCEI M12X1.5X95 | BUY | 2 | nr | 5 | 1 |  |  |  | 100 |  | 5 |  |  |  |  |  |  |  |  |
|  | Full Assembly | 26D66814 | KIT VETTURA | MAKE |  |  | 3 | 1 | 10 |  |  | 1 |  | 1 | NO |  |  | OP10 | A428002 | 1 | 13.6 | 0.75 |
|  |  | 28D66727_PH | Modulo post sx | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 28D66528_PH | Modulo ant dx | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 28D66527_PH | Modulo ant sx | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 28D66728_PH | Modulo post dx | MAKE | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | 98512698 | ETICHETTA AUTOADESIVA BIANCA | BUY | 1 | nr |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
