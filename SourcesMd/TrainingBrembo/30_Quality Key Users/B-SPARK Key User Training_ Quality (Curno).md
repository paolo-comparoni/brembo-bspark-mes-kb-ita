# B-SPARK Key User Training_ Quality (Curno)

> Documento sorgente: `E:\BremboDocs\TrainingBrembo\30_Quality Key Users\B-SPARK Key User Training_ Quality (Curno).docx`  
> Tipo: Word (.docx)

**B-SPARK Key User Training Quality (Curno)-20260619\_090329-Registrazione della riunione**

19 giugno 2026, 07:03AM

3 h 57 m 54 s

_[immagine]_**  
Paolo Comparoni** trascrizione avviata

_[immagine]_**  
Paolo Comparoni** 0:16  
Baba.  
But.  
Tanya, the other.  
That's some equal data.  
In your detail to be perfect.

_[immagine]_**  
Spreafico Paolo** 1:49  
Solo una cosa, quando parleremo di tracciabilità sarà.  
Per capire un attimo perché c'è la parte di qualità clienti che è interessata principalmente a quello e gli ho detto di partecipare.  
Sono.  
Ovviamente sta.  
No, praticamente faremo vedere diciamo introduciamo facendo vedere tutti diciamo i pezzi che compongono di tutti i pezzi che compongono il modulo qualità e quindi per far vedere praticamente.  
Come era prima con AX, cioè come sarà adesso, quindi con il match e con Power BI, quindi quella patria introduttiva potremo vedere e poi andremo nello specifico poi dopo che.  
Diciamo abbiamo dell'attività di scatto di dichiarazione, poi andiamo a vedere nello specifico la traccia del.  
La Francia per la geometra.  
Subito, quasi subito e poi una parte finale, invece, più nel dettaglio.  
Va bene.  
C'è il link alla riunione, giusto? Se dico Mattia collega dell'inizio, poi magari OK.  
Sì.  
Paolo, scusami, faccio una premessa, se posso.  
No ragazzi, voi conoscete, sapete che sono la tua \*\*\*\*\*\*\*\*\*\*.  
I ragazzi si occupano del MES rispetto a oggi che noi siamo abituati, c'è avanzamento di fabbrica sul MES e il centrale, ne abbiamo quattro di sei tempi.  
Quindi abbiamo il centrale che si chiama SAP.  
Quello che gestisce il magazzino.  
Che si chiama TWM.  
C'è questo signore qua che è il MES che sostituisce l'avanzamento di fabbrica e c'è la parte di reportistica.  
OK, tutti questi tre sistemi sparano i dati sulla parte di reportistica. Lo scopo di oggi è farvi capire a livello globale come funziona il MES, che potenzialità ci dà il MES?  
Cosa era prima su avanzamento di fabbrica e cosa sarà domani sul MES?  
Questo anche allo scopo dei ragazzi, se avete dubbi, domande, perplessi, car.  
Si fermate se non se non ci difendiamo con i termini. Io son qui, mi faccio il traduttore fra il MES e il Trendese, non fatevi problemi.  
Dubbi che chiudiamo subito.  
OK.  
In modo tale che ci siamo allineati tutti.  
Ultima cosa, signor mio.  
Nel MES ci sono due modalità che ho chiesto di mostrarvi, la modalità operatore bordo macchina, dove noi fondamentalmente andiamo ma non mettiamo le zampe, e la modalità dove noi andiamo a giocare.  
Dove andremo a sentenziare gli scarti, dove andremo a generare e a collegare le ispezioni? Tanto per capirci, quella è cascata nel nostro campo. Adesso quindi i ragazzi ci faranno vedere come fare a fare questa attività.  
Perfetto. Io sono Paolo Comparoni, ho lavorato tantissimi anni in che è il diciamo è lo sviluppatore del sistema MES che.  
È installato qui a Brembo e negli altri impianti. È un sistema MES distribuito con caratteri modulare con caratteristiche avanzate. MES praticamente è un.  
Un software di integrazione che è in grado di connettere il mio impianto e il mondo TAP, quindi finanziario e al mondo dell'automation, principalmente scada macchine e.  
Appunto a fornire, arricchire, diciamo, i due mondi di tutte di entità, come ad esempio il modulo di quality, come la gestione del personale, la gestione degli Equipment.  
Tutte cose esterne che diciamo SAP non ha o l'automazione non ha questo layer intermedio appunto che si chiama OP Center e poi noi siamo in quanto engineering siamo fornitori di questa soluzione.  
Quindi in questo in questo training andremo a vedere in modo più operativo quali sono le tematiche e gli argomenti e il e by day di questo modulo di qualità fornito nel MES.  
Tu vestiti qualcosa da.  
Sì, io sono scusatemi, ero stavo cercando di mi stavo ancora collegando al sistema e la connessione avviene tramite tramite un indirizzo web.  
Sono l'analista funzionale di questo di questo sistema e quindi sono quello che ha aiutato a tradurre le richieste del vostro business.  
Gli organizzatori della fabbrica, poi, almeno per la città vera, propria di.  
Quindi abbiamo realizzato in pratica, senza usare tanti termini tecnici, il software che andremo a vedere stamattina per la parte qualità.  
È un po uno, quello che è un collante tra tutti, tra tutti gli altri sistemi software che.  
Che ci sono nella fabbrica, per cui permette di.  
Di scambiare i dati che sia dalla parte telefonica degli operatori, anche dalla parte del software SAP e quindi attività finanziaria, quindi di organizzazione e provvigionamento.  
E questo e questo software è in grado soprattutto anche di registrare dati, eventi sia da SAP che dal dalle linee e dall'automazione e organizzarli e poi?  
Come Flavio Diario, ad esempio, che ha molto valore strategico su questi dati che vengono raccolti in modo automatico. Disegno quello che vorrei dirvi che l'ha detto anche Paolo.  
Abbiamo una terminologia tecnica per cui siamo informatici e magari non è la terminologia che poi se si per qualche cosa che non si permette proprio i termini inglesi no.  
Sentitevi liberissimi di intervenire, chiedere, ma questa cosa che voglio dire me la me la puoi dire in un'altro modo, non puoi spiegare perché così ci capiamo meglio. Non fatevi problemi però a chiedere approfondimenti a chi ha, se non capite un termine è normalissimo.  
E quindi potete potete chiederci ulteriori spiegazioni.  
Solo solo una cosa per quanto riguarda la parte di Power BI che avete citato, è un passaggio che ad oggi noi non abbiamo nel sistema. Noi oggi prendiamo direttamente dalle dichiarazioni di linea, sia di produzione che di scarto, i dati che vanno in report Excel che sono alla fine i cubi produzione cubi scarto.  
Domani ci sarà un passaggio intermedio in più, cioè che i dati andranno in Power BI e poi se ci sarà bisogno di personalizzare.  
Strumento di riferimento sarà Power BI per ci sarà un'estrazione dati da database di OP center, quindi del MES.  
Che registerà appunto tutte le tutti gli eventi e poi verranno estratti i dati e verranno generati i report e tutto quanto. OK, secondo me davanti la slide.  
OK, allora facciamolo rapidamente, quindi qui sono i topic e quindi allora appunto, abbiamo deciso dopo una review con Paolo di avere una.  
No, diciamo.  
Un approccio più operativo, quindi faremo vedere, partiremo praticamente da il risultato finale, no? Quindi quali sono le interfacce, quali sono i case?  
E cos'è che l'operatore di quality con cos'è che si interfaccerà e quale sarà il contenuto? E poi andremo scendendo più nel dettaglio a vedere i vari use case, quindi le reazioni.  
Che poi portano al risultato finale, quindi alla gestione del della quality, quindi poi partiremo praticamente dalla fine del risultato finale e poi andremo indietro nelle fasi no, quindi faremo vedere subito.  
Quali sono i news case a cui siamo a cui siamo interessati e nel vostro caso sono, abbiamo preso un machining, washing, l'assembly e poi faremo c'è anche il discorso delle Bats che.  
Più ricco, diciamo dal punto di vista operativo.  
Faremo vedere com'era prima, quindi con anx come sarà adesso, poi faremo invece vedere com'è che questi dati vengono registrati.  
Quindi cos'è il creatore di linea? Com'è che fa tecnicamente a dichiarare uno scatto AA compilare 1 1 lista di descrizioni e poi nella parte finale faremo vedere come.  
Come viene configurato il sistema per gestire le operativo, ovviamente sentencing che è fondamentale nella. Quindi come risolvere 1 1?  
Container di quarantena, no? Come risolverlo, quindi come reazioni per gestirlo, se fare, se riportando diciamo in linea, se richiede un rework, magari se scattando davvero e poi nell'ultimo pezzo.  
Faremo vedere tutte queste azioni vengono configurate a sistema? No, perché è un sistema altamente configurabile, quindi diciamo per ogni per ogni prodotto.  
Si possono specificare una serie di una serie di attributi di caratteristiche, una serie di con certe modalità di.  
Di inserimento per cui c'è tutto un discorso diciamo tecnico di come poi settore di qualità riesce poi a gestire questa questo modulo infatti se puoi andare avanti, se poi c'è anche una cosa come cambiare lingua nel sistema.  
Sei riuscita a condividere lo schermo che almeno rimane nella registrazione? Paolo, vi ho appena girato le slide.  
Se vi serve.  
Bene, allora appena puoi condividere questo schermo.  
Ok, allora innanzitutto c'è, ci sono due facce principali, non so se l'avete già visto. Ci sono diversi diversi environment, no? Noi lavoreremo nell'environment di polity che è praticamente una copia.  
Dell'environment di produzione Environment cos'è? Sono un'insieme di macchine, un'insieme di server, perché ha un'architettura distribuita, quella di OP Center di Siemens, ridondante con diciamo.  
Abbastanza complessa e diciamo è server based, quindi c'è un server con.  
E diciamo C'è un'interfaccia web per accedere per accedere poi al all'applicazione questa interfaccia web anche questa gli utenti sono importati da Windows secondo.  
C'è un modulo apposta per gestire i vostri utenti, è già un'applicazione enterprise fatta di diversi moduli e queste qua sono interfacce, quindi il modo che hanno gli utenti, sia gli operatori di linea sia i quality manager che.  
Accedere al sistema.  
Salve.  
Grazie.  
E quindi penso che voi questi due indirizzi ce l'avete già e riuscite ad accedere ad accederci dal vostro computer direttamente da qui.

_[immagine]_**  
Emanuele Merlo** 16:50  
Pienso che.  
Ad accederci sul computer direttamente da qui.

_[immagine]_**  
Spreafico Paolo** 17:00  
Se potete provare poi se avete già il link vi ho vi trovate nella mail direttamente il link all'ambiente di produzione modalità qualità quindi quello non il repetitive ma il supervisor.

_[immagine]_**  
Emanuele Merlo** 17:00  
Se potete provare poi se avete già il link, magari Paolo vi ha già comunicato nella mail direttamente il link all'ambiente di produzione.  
In modalità qualità OK, quindi praticamente la prima interfaccia noi la chiamiamo basic OK, è la collezione delle.

_[immagine]_**  
Spreafico Paolo** 17:18  
Quindi praticamente la prima interfaccia noi la chiamiamo basic, OK, è la collezione delle screen direttamente di prodotto, quindi fornite da Siemens che gestiscono le entità.

_[immagine]_**  
Emanuele Merlo** 17:26  
Delle screen direttamente di prodotto, quindi fornite da Siemens che gestiscono le entità tipiche di Siemens, quindi i materiali piuttosto che gli Equipment, tutte le cose, soprattutto in master data, che rendono possibile poi la gestione operativa dell'impianto.

_[immagine]_**  
Spreafico Paolo** 17:33  
Tipiche di Siemens, quindi i materiali piuttosto che gli Equipment, le cose, soprattutto i master data, che rendono possibile poi la gestione operativa dell'impianto e quindi vedrete una collezione praticamente di.

_[immagine]_**  
Emanuele Merlo** 17:45  
E quindi vedete qui dentro una proiezione praticamente di tantissime pagine, molte delle quali magari non userete e però appunto il vostro profilo dell'utente può essere cambiato per.

_[immagine]_**  
Spreafico Paolo** 17:49  
Tantissime pagine, molte delle quali magari non userete e però appunto il vostro profilo dell'utente può essere cambiato per gestire il menu, quindi entrare direttamente su certi tipi di pagine piuttosto che filtrarne altri, no?  
E qui è dove ad esempio potremmo vedere per quanto riguarda la quality, possiamo vedere, possiamo gestire la il sentencing no il sentencing ad esempio, oppure potremmo vedere la lista del.

_[immagine]_**  
Emanuele Merlo** 18:13  
A Il sentencing no, il sentencing ad esempio, oppure potremmo vedere la lista del delle politics section, potremmo vedere, potremmo cambiare certe certe spezzoni legati a un certo.

_[immagine]_**  
Spreafico Paolo** 18:21  
Le quality inspection potremmo vedere, potremmo cambiare certe certe sezioni legati a un certo prodotto finale e tutti, tutte queste queste cose qui.

_[immagine]_**  
Emanuele Merlo** 18:29  
Prodotto finale e tutti tutte queste queste cose qui le gestiamo nella prima interfaccia, quindi questa qua diciamo è l'interfaccia operativa del quality manager.

_[immagine]_**  
Spreafico Paolo** 18:37  
Questa qua, diciamo, è l'interfaccia operativa del quality manager.  
La seconda invece è diversa, non è non è riprodotto, OK, è una è una pagina, è un'applicazione che si chiama Mendis, è un'applicazione Siemens.

_[immagine]_**  
Emanuele Merlo** 18:43  
La seconda invece è diversa, non è non è di prodotto, OK, è una è una pagina, è un'applicazione che si chiama Mendix, è un'applicazione di Siemens.  
Che permette di creare questo tipo di interfaccia operatore è un'interfaccia diciamo di stile touch di stile operativo il viene aperta a bordo linea sul terminal di bordo linea.

_[immagine]_**  
Spreafico Paolo** 18:58  
Che permette di creare questo tipo di interfaccia operatore ha un'interfaccia diciamo di stile touch operativo viene aperta a bordo linea sui terminali di bordo linea e è gestita diciamo.

_[immagine]_**  
Emanuele Merlo** 19:13  
E è gestita diciamo per ottimizzare tutte le operazioni di inserimento manuale OK, quindi non è una pagina di inserimento e anche di monitoring e controllo che deve aiutare l'operatore di linea a fare day by day quindi.

_[immagine]_**  
Spreafico Paolo** 19:15  
Per ottimizzare tutte le operazioni di inserimento manuali OK, quindi non è una pagina di inserimento e anche di monitoring e controllo che deve aiutare gli operatori di linea a fare dei by day, quindi a dichiarare i prezzi di ingresso, a vedere se ci sono delle.

_[immagine]_**  
Emanuele Merlo** 19:29  
A dichiarare i prezzi in ingresso, a vedere se ci sono delle dei difetti no in entrata, in uscita, se poi sono le qualità prodotti, in quale container e ci sono anche dei documenti no automaticamente visibili.

_[immagine]_**  
Spreafico Paolo** 19:34  
Dei difetti no, in entrata, in uscita, se quali sono le qualità prodotte, in quale container e ci sono anche dei documenti no automaticamente difficili su questa tipo di interfaccia che appunto noi chiamiamo repetitive ma.

_[immagine]_**  
Emanuele Merlo** 19:47  
In questa tipo di interfaccia che appunto noi la chiamiamo repetitive ma poi gli darete un'altro nome perché pagina operatore OK.

_[immagine]_**  
Spreafico Paolo** 19:51  
Poi intervengo un attimo, perché?

_[immagine]_**  
Emanuele Merlo** 19:57  
E diciamo, questa qua è organizzata e studiata apposta per ottimizzare il lavoro del dell'utente del dell'operatore di linea OK quindi 2 2 interfacce diverse.

_[immagine]_**  
Spreafico Paolo** 19:57  
E diciamo, questa qua è organizzata e studiata apposta per ottimizzare il lavoro del dell'utente del dell'operatore di linea, quindi due due interfacce diverse.

_[immagine]_**  
Emanuele Merlo** 20:15  
Una diciamo di prodotto e l'altra invece creata ad hoc per l'operatore di linea. Ok, perfetto, puoi andare avanti questa qua la login. Potete accedervi con la vostra col vostro utente, dovreste andarci.

_[immagine]_**  
Spreafico Paolo** 20:15  
Una diciamo di prodotto e l'altra invece creata ad hoc per l'operatore di linea puoi andare avanti senza fare la login potete accedere con la vostra con il vostro utente che dovrebbe farci.

_[immagine]_**  
Emanuele Merlo** 20:31  
Qui vedete il nome dell'applicazione di Siemens, no OP Center execution e OP Center nel diciamo Trench nel vertical che noi chiamiamo verticale discrete, che è il prodotto che.

_[immagine]_**  
Spreafico Paolo** 20:31  
E qui vedete il nome dell'applicazione, il Siemens Office Center nel diciamo nel verticale verticale, che è il prodotto che.

_[immagine]_**  
Emanuele Merlo** 20:46  
Che avete che Brembo ha acquistato per gestire il MES? Vai avanti.

_[immagine]_**  
Spreafico Paolo** 20:47  
Che avete avremmo acquistato per gestire il MES vai avanti.

_[immagine]_**  
Emanuele Merlo** 20:54  
OK, casi guida perfetto, vai avanti. Primo capitolo, OK, questo qui è.

_[immagine]_**  
Spreafico Paolo** 20:54  
OK, infatti guida perfetto, vai avanti un capitolo OK, questo qui è l'approccio che è stato scelto, no? Quindi vediamo bene come lo vogliamo organizzare, OK, quindi le attività quotidiane.

_[immagine]_**  
Emanuele Merlo** 21:00  
L'approccio che appunto è stato scelto? No, quindi vediamo bene come lo vogliamo organizzare, OK, quindi le attività quotidiane, com'era, com'è adesso, quindi si parlerà. Adesso gestite le cose con l'avanzamento di fabbrica.

_[immagine]_**  
Spreafico Paolo** 21:10  
Com'era? Com'è adesso? Quindi si pagherà adesso le cose con l'avanzamento di fabbrica, poi ci sarà la parte appunto che la parte diciamo più di configurazione, back Office e tutte le attività e poi comunque.

_[immagine]_**  
Emanuele Merlo** 21:17  
Poi ci sarà la parte appunto che la parte diciamo più di configurazione, il backoffice e tutte le attività e poi comunque andiamo a vedere i casi reali dell'impianto di turno, OK?

_[immagine]_**  
Spreafico Paolo** 21:26  
Andiamo a vedere i casi reali dell'impianto di turno.

_[immagine]_**  
Emanuele Merlo** 21:33  
Quindi sono appunto, io accetto il washing, il work Center, diciamo dal punto di vista MES è molto importante perché diciamo che poi sarà.

_[immagine]_**  
Spreafico Paolo** 21:33  
Quindi sono appunto abbiamo scelto il washing, il work Center, diciamo dal punto di vista MES è molto importante perché diciamo che poi sarà.

_[immagine]_**  
Emanuele Merlo** 21:48  
Sta un'etichetta, no?

_[immagine]_**  
Spreafico Paolo** 21:49  
Da un'etichetta, no?

_[immagine]_**  
Emanuele Merlo** 21:52  
Nel su sulla linea no, cioè nonostante cos'è è comunque una linea di assemblaggio 1 1 postazione di assemblaggio in due isole non le chiamate voi.

_[immagine]_**  
Spreafico Paolo** 21:52  
Sulla linea no, cioè nonostante cos'è? È comunque una linea da sempre.

_[immagine]_**  
Emanuele Merlo** 22:00  
E ci sarà un'etichetta e tramite quell'etichetta diciamo l'operatore entrerà direttamente nel contesto di quel work center, quindi vedrà gli ordini pronti per essere eseguiti o gli ordini magari in pausa pronti per essere ripresi di quel work center. Quindi diciamo che.

_[immagine]_**  
Spreafico Paolo** 22:01  
E ci sarà un'etichetta e tramite quell'etichetta diciamo l'operatore entrerà direttamente nel contesto di quel work center, quindi vedrà gli ordini pronti per essere eseguiti o gli ordini magari in pausa pronti per essere ripresi di quel work center. Quindi diciamo che.

_[immagine]_**  
Emanuele Merlo** 22:18  
Questa cosa qua per noi diciamo è importante, ma poi verrà scannerizzata diciamo da un barcode automaticamente no. Quindi abbiamo un center e anche l'operazione che viene eseguita in quel center è molto importante l'operazione.

_[immagine]_**  
Spreafico Paolo** 22:18  
Questa cosa qua per noi diciamo è importante, ma poi verrà scannerizzata diciamo da automaticamente no. Quindi abbiamo un center e anche l'operazione che viene eseguita in quel work center è molto importante l'operazione.

_[immagine]_**  
Emanuele Merlo** 22:35  
Voi la chiamate il ciclo no, il primo operation no, comunque è il ciclo di lavorazione di quel determinato di quel determinato prodotto, quindi.

_[immagine]_**  
Spreafico Paolo** 22:35  
Voi la chiamate ciclo no operation no, comunque è il ciclo di lavorazione di quel determinato di quel determinato prodotto, quindi.

_[immagine]_**  
Emanuele Merlo** 22:47  
Nei nostri casi vedremo questo work center washing PM 01M la una fase di assegni secondario, per questo con l'operazione si chiama Collaudo completamento.

_[immagine]_**  
Spreafico Paolo** 22:47  
Nei nostri casi vedremo questo work center washing BM 01M la maggiore alta pressione, poi ci sarà una fase di assenza secondario per questo con l'operazione si chiama Grillo completamento.

_[immagine]_**  
Emanuele Merlo** 23:03  
E poi ci sarà la vedremo la fiction che diciamo e dicevo che è più complicata perché in realtà diciamo che ci sarà uno center, diciamo prima che.

_[immagine]_**  
Spreafico Paolo** 23:03  
E poi ci sarà la vedremo la fiction che diciamo e dicevo che è più complicata perché in realtà diciamo che ci sarà lo sente, diciamo prima che.

_[immagine]_**  
Emanuele Merlo** 23:18  
E ha il materiale poi da essere stampato. Quindi c'è un lavoro di tipo diverso che crea un materiale da essere stampato. E poi ci sarà un'operazione precedente a quella di rettifica che è quella diciamo più importante dal punto di vista del quality manager? No, perché è quella più ricca.

_[immagine]_**  
Spreafico Paolo** 23:18  
Crea il materiale poi da essere stampato, quindi ci sarà un lavoro di tipo diverso che crea un materiale da essere stampato. E poi ci sarà un'operazione precedente a quella di rettifica che è quella diciamo più importante dal punto di vista del policy manager? No, perché è quella più ricca no di ispezioni.

_[immagine]_**  
Emanuele Merlo** 23:36  
No di ispezioni di cose da fare. Ditemi se sto dicendo cose che non capite, OK? Quindi il pezzo appunto è più complicato diciamo rispetto agli altri perché è multifase, quindi ha diversi cicli. No, sono ordini che hanno diversi cicli.

_[immagine]_**  
Spreafico Paolo** 23:38  
Cose da farmi, ditemi se sto dicendo cose che non capite.  
Quindi il pezzo appunto è più complicato rispetto agli altri perché è multifase, quindi ha diversi cicli. No, sono ordini che hanno diversi cicli. OKE ci sono anche ordini necessari, diciamo ci sono anche prerequisiti, per esempio l'ordine com'è che si chiama l'ordine?

_[immagine]_**  
Emanuele Merlo** 23:53  
E ci sono anche ordini necessari, diciamo ci sono anche prerequisiti, ad esempio l'ordine. E com'è che si chiama quell'ordine? Quello di per amalgamare com'è che si chiama? Sì, però ha un nome in italiano.

_[immagine]_**  
Spreafico Paolo** 24:02  
Quello di per amalgamare com'è che si chiama mixer? Sì, vabbè, il mixing è chiaro.

_[immagine]_**  
Emanuele Merlo** 24:09  
Mixing OK.  
E quindi diciamo è più complicato però e anche il concetto di original batch dentro e quindi diciamo essendo più complicato però anche più interessante dal punto di vista della quality l'original batch lo sapete di cosa parliamo?

_[immagine]_**  
Spreafico Paolo** 24:15  
E anche il concetto di original batch dentro e quindi diciamo essendo più complicato, però anche più interessante dal punto di vista della quota aspetta, allora faccio una premessa io prima di introdurre questi concetti.  
Il codice Underscore Whip non esiste più, ogni singola fase, ogni singola macchina produrrà un finito chiamiamolo così, quindi il codice. Prendiamo il caso del washing.

_[immagine]_**  
Emanuele Merlo** 24:32  
Codice Underscore VIP non esiste più, ogni singola base, ogni singola macchina produrrà un finito, quindi il codice per un caso del washing e andrà a consumare un codice, lo stesso codice underscore MCH.

_[immagine]_**  
Spreafico Paolo** 24:46  
Miandràaconsumareuncodicelostessocodiceunderscorem.ch machining.

_[immagine]_**  
Emanuele Merlo** 24:51  
Machine.  
E riprodurrà il codice lavato underscore, quindi su ogni singola fase noi avremo la dichiarazione dello stesso oggetto con il supplisco della fase, prima era underscore whip, adesso si chiamerà underscore.

_[immagine]_**  
Spreafico Paolo** 24:53  
E mi produrrà un codice lavato underscore washing. Quindi su ogni singola fase noi avremo la dichiarazione dello stesso oggetto con il suffisso della fase, quello che prima era underscore whip, adesso si chiamerà underscore.

_[immagine]_**  
Emanuele Merlo** 25:09  
Comicon della pace.

_[immagine]_**  
Spreafico Paolo** 25:09  
Con il nome della fase propagato a 360 ° avremo machining, washing, ossidazione, Paint e poi il prodotto finito a seconda dei vari cicli prenderà queste desinenze.

_[immagine]_**  
Emanuele Merlo** 25:11  
Propagato a 360 ° avremo machining, washing, ossidazione, Paint e poi prodotto finito a seconda dei vari cicli, prenderà questa residenza nel caso del montaggio.

_[immagine]_**  
Spreafico Paolo** 25:25  
Nel caso del montaggio avremo primo montaggio FST first assembly, quando uscirà da bringer o andrà su un fornitore mi rientrerà il codiceperdendolultimosuffissoquindidiventeràaba.ca pinco pallino.

_[immagine]_**  
Emanuele Merlo** 25:28  
Avremo primo montaggio FSP first assembly, quando uscirà da printer o andrà sul rifornitore mi rientrerà il codice perdendo l'ultimo suffisso, quindi diventerà via sia ha vinto pallino.  
Quando andrà sul secondo montaggio posso avere due casi produco senza avere il l'extra controllo, in tal caso il codice è finito, altrimenti prenderà la parte second assembly per andare all'extra controllo.

_[immagine]_**  
Spreafico Paolo** 25:42  
Quando andrà sul secondo montaggio posso avere due casi produco senza avere l'extra controllo, in tal caso avrò il codice finito, altrimenti prenderà la fase second assembly per andare all'extra controllo.

_[immagine]_**  
Emanuele Merlo** 25:58  
E perderà ancora la fase di.

_[immagine]_**  
Spreafico Paolo** 25:58  
E perderà in quella fase il la desinenza.

_[immagine]_**  
Emanuele Merlo** 26:03  
Nel caso del mixer della delle pastiglie avremo la bramoja che mi viene scaricata dallo Zanelli parto nella nello stampaggio quindi avremo STM sto utilizzando ovviamente.

_[immagine]_**  
Spreafico Paolo** 26:04  
Nel caso del mix della delle pastiglie avremo la tramogela che mi viene scaricata dallo zanelli.  
Parto nella nello stampaggio, quindi avremo STM, sto inventando, ovviamente avremo il forno.

_[immagine]_**  
Emanuele Merlo** 26:19  
Faremo intorno.  
Quindi preforme, postforme, avremo la rettificata, avremo il verniciato, avremo le n nella fase successiva.

_[immagine]_**  
Spreafico Paolo** 26:21  
Quindi pre forno e post forno avremo la rettificata, avremo il verniciato, avremo le n mila fasi successive.

_[immagine]_**  
Emanuele Merlo** 26:33  
Il discorso che diceva prima Paolo e Emanuele è legato al fatto che nel caso della friction abbiamo vincolato fisicamente che le fasi successive post stampate.

_[immagine]_**  
Spreafico Paolo** 26:33  
Il discorso dell'Original batch che diceva prima il buon Paolo, il buon Emanuele è legato al fatto che nel caso della friction abbiamo vincolato fisicamente che le fasi successive post stampaggio.

_[immagine]_**  
Emanuele Merlo** 26:50  
Possono consumare solo ed esclusivamente lo stesso lotto di produzione dello stampaggio. Esempio stupido, destro o sinistro? Oggi siamo abituati tra un unico batch, giusto? Domani saranno due codici diversi, due batch diversi.

_[immagine]_**  
Spreafico Paolo** 26:50  
Possano consumare solo ed esclusivamente lo stesso lotto di produzione dello stampaggio esempio stupido.  
Destro o sinistro? A oggi siamo abituati che a un unico batch, giusto? Domani saranno due codici diversi, due batch diversi. Se per caso vado in forno e non e dichiaro guarda che sull'ordine uno sto processando il codice destro.

_[immagine]_**  
Emanuele Merlo** 27:08  
Se per caso vado in forno e non gli e gli chiaro guarda che sull'ordine uno sto processando il codice destro e gli sparo il codice del sinistro, il sistema mi dice Non puoi perché uno mi dà lo stesso codice.

_[immagine]_**  
Spreafico Paolo** 27:16  
E gli sparo il codice del sinistro. Il sistema mi dice Non puoi perché uno non è lo stesso codice se per caso, come succede dal buon castelli, faccio il testacoda. Quindi primo batch, secondo batch, li metto uno indietro, uno dietro l'altro.

_[immagine]_**  
Emanuele Merlo** 27:23  
Se per caso, come succede al buon castelli, faccio il testa coda, quindi primo match, secondo match di match uno dietro, uno dietro l'altro.  
Cosa succede che il sistema mi dice Guarda che tu mi stai dando in pasto un batch, un CD che mi proviene da un da un batch diverso e non te lo lasci più processare perché c'è il controllo tra il batch che sto processando.

_[immagine]_**  
Spreafico Paolo** 27:34  
Cosa succede che il sistema mi dice Guarda che tu mi stai dando in pasto un batch, un CDI che mi proviene da un da un batch diverso e non te lo lascio più processare perché c'è il controllo tra il batch che sto processando.

_[immagine]_**  
Emanuele Merlo** 27:49  
È quello che sto andando a fare.

_[immagine]_**  
Spreafico Paolo** 27:49  
È quello che sto andando a consumare.

_[immagine]_**  
Emanuele Merlo** 27:53  
E questo è il concetto che viene applicato un po come quello che prima noi coprivamo con l'underscore week, con il badge che è passato su tutte le fasi, adesso l'abbiamo cambiato con l'original badge.

_[immagine]_**  
Spreafico Paolo** 27:53  
È lo stesso concetto che viene applicato in fonderia, quello che prima noi coprivamo con l'underscore whip, con il batch che passava su tutte le fasi, adesso l'abbiamo cambiato con l'original batch.

_[immagine]_**  
Emanuele Merlo** 28:07  
Altra variante, ogni singola fase di produzione avrà un suo patch interno, quindi su ogni singola fase il sistema staccherà un codice patch.

_[immagine]_**  
Spreafico Paolo** 28:08  
Aspetta che arrivo altra variante, ogni singola fase di produzione avrà un suo batch interno, quindi su ogni singola fase il sistema staccherà un codice batch.

_[immagine]_**  
Emanuele Merlo** 28:23  
Specifico di quella fase, l'unica cosa che attraverserà tutte le fasi sarà questo original batch che verrà propagato da un batch all'altro, quindi anche quando gli stampi a due figure.

_[immagine]_**  
Spreafico Paolo** 28:23  
Specifico di quella fase, l'unica cosa che attraverserà tutte le fasi sarà questo original batch che verrà propagato.  
Da un batch all'altro prego quindi anche quando gli stampi a due figure dove stampo passi a destra e sinistra avrò due batch, due codici, due codici, due batch che sto producendo contemporaneamente sulla stessa pressa.

_[immagine]_**  
Emanuele Merlo** 28:40  
Dove stampo pastiglia destra e sinistra avrò due batch, due codici, due codici, due che sto producendo contemporaneamente sulla stessa beta.

_[immagine]_**  
Spreafico Paolo** 28:51  
Corretto.

_[immagine]_**  
Emanuele Merlo** 28:53  
Saranno tracciati con l'original batch dalla fase di stampaggio, saprò che andrà a consumare quel batch di consumo di quella tramoggia.

_[immagine]_**  
Spreafico Paolo** 28:53  
Saranno tracciati con l'original batch della mescola, allora partirà l'original batch dalla fase di stampaggio saprò che andrà a consumare quel batch di consumo di quella tramoggia.

_[immagine]_**  
Emanuele Merlo** 29:08  
Più o meno perché voi mi insegnate che avete del materiale nel da dove scarico la tramoggia al allo scarico quello lì non ho garanzia che effettivamente ho preso tot materiale da quella specifica tramoggia.

_[immagine]_**  
Spreafico Paolo** 29:08  
Più o meno perché voi mi insegnate che avete del materiale nel tubo da dove scarico la tramoggia al allo scarico quello lì non ho garanzia che effettivamente ho preso tot materiale da quella specifica tramoggia.  
Scusami Paolo per l'escursore.

_[immagine]_**  
Emanuele Merlo** 29:26  
Hai disegnato bene il processo, OK così ci saranno quando usciranno?

_[immagine]_**  
Spreafico Paolo** 29:28  
Bene.  
Ma quindi non esisteranno più gli intermedi del montaggio tipo ACBC che gli intermedi del montaggio ci saranno quando usciranno da brimber sull'uscita della linea?

_[immagine]_**  
Emanuele Merlo** 29:42  
OK, quindi abbiamo la linea ACFSTE, poi andrà in Linda ACOK.

_[immagine]_**  
Spreafico Paolo** 29:45  
CFST poi andrà in blind e diventerà ACOK.

_[immagine]_**  
Emanuele Merlo** 29:51  
Poi finisco visto che me la entro dopo direttamente. C'è un nuovo status soprattutto per il montaggio che si chiama materiale sospeso. Fino a ieri eravamo abituati a dire o è buono.

_[immagine]_**  
Spreafico Paolo** 29:51  
Poi scusami che così almeno finisco visto che me l'hai introdotto te la schiaccio direttamente. C'è un nuovo status soprattutto per il montaggio che si chiama materiale sospeso. Fino a ieri eravamo abituati a dire o è buono.

_[immagine]_**  
Emanuele Merlo** 30:06  
Poi scatto.

_[immagine]_**  
Spreafico Paolo** 30:07  
O è scarto?

_[immagine]_**  
Emanuele Merlo** 30:09  
Da oggi con questo sistema c'è una cosa che si chiama quarantena o bimbo.

_[immagine]_**  
Spreafico Paolo** 30:09  
Da oggi con questo sistema c'è una cosa che si chiama quarantena o limbo.

_[immagine]_**  
Emanuele Merlo** 30:15  
Per cui io operatore di linea dico, non sono sicuro se è buono, se scarto lo metto un attimo in disparte, lo tiene in sospeso.

_[immagine]_**  
Spreafico Paolo** 30:15  
Per cui io operatore di linea dico, non sono sicuro se è buono, se scarto lo metto un attimo in disparte, lo tiene in sospeso.

_[immagine]_**  
Emanuele Merlo** 30:26  
Chiamo la qualità e la qualità sentenzia comunque vediamo anche questi casi è applicato al 99% se il montaggio.

_[immagine]_**  
Spreafico Paolo** 30:26  
Chiamo sì no, era giusto per introdurre il concetto, chiamo la qualità e la qualità sentenzia comunque vediamo anche questi casi è applicabile al 99% sul montaggio.  
Giusto per farvi l'excursus, scusami Paolo per l'interruzione.

_[immagine]_**  
Emanuele Merlo** 30:41  
E Paolo, una precisazione che diciamo che ognuna di queste di queste operazioni no.

_[immagine]_**  
Spreafico Paolo** 30:46  
Diciamo che ognuna di queste queste operazioni no.

_[immagine]_**  
Emanuele Merlo** 30:52  
È associata a una bomba? No? Quindi sono dei materiali in ingresso, OK dei dei componenti in ingresso. C'è una fase di lavorazione che può essere di tipo di tipo chimico, di tipo fisico, può essere un assemblaggio eccetera. E poi c'è la produzione.

_[immagine]_**  
Spreafico Paolo** 30:52  
È associata a una bomba? No? Quindi sono dei materiali in ingresso, dei componenti in ingresso. C'è una fase di lavorazione che può essere tipo di tipo fisico, può essere un assemblaggio eccetera. E poi c'è la produzione.

_[immagine]_**  
Emanuele Merlo** 31:10  
Di un prodotto finale? No. Questa cosa noi in genere la chiamiamo pilot material no vista dei materiali che collega praticamente i materiali d'uscita con i suoi componenti di ingresso. Quindi è diciamo queste fasi in realtà si possono vedere in modo astratto.

_[immagine]_**  
Spreafico Paolo** 31:10  
Di un prodotto finale? No, questa cosa noi in gergo la chiamiamo build material, no lista dei materiali che collega praticamente i materiali in uscita con i suoi componenti di ingresso. Quindi diciamo queste fasi in realtà si possono vedere in modo astratto.

_[immagine]_**  
Emanuele Merlo** 31:27  
Come trasformazioni, come composizioni.

_[immagine]_**  
Spreafico Paolo** 31:27  
Propone trasformazioni per me composizioni.

_[immagine]_**  
Emanuele Merlo** 31:32  
Di un insieme materiali di grasso in un materiale d'uscita di uno o più materiali OK, quindi diciamo che anche l'operatore poi deve l'interfaccia deve capire esattamente quali sono.

_[immagine]_**  
Spreafico Paolo** 31:33  
Di mettere il materiale d'ingresso in un materiale in uscita perché uno più materiale quindi diciamo che anche l'operatore poi deve dell'interfaccia deve capire quali sono.

_[immagine]_**  
Emanuele Merlo** 31:47  
I materiali d'ingresso come vengono dichiarati e quali sono quelli di uscita, come vengono scartati eccetera. Vai avanti, grazie.

_[immagine]_**  
Spreafico Paolo** 31:48  
I materiali di ingresso come vengono dichiarati e poi sono quelli di uscita, come vengono scartati eccetera. Vai avanti, grazie.

_[immagine]_**  
Emanuele Merlo** 31:59  
Perfetto, allora qui appunto vediamo il cioè questa questo confronto, no?  
Pronto, no?

_[immagine]_**  
Spreafico Paolo** 32:06  
In fondo no.

_[immagine]_**  
Emanuele Merlo** 32:08  
Fino adesso ricordo che l'impianto ha funzionato più che bene e aveva diciamo era era questa fase qua di dell'operatore di linea gestita da delle interfacce di Microsoft AX.

_[immagine]_**  
Spreafico Paolo** 32:08  
Fino adesso le cose intanto ha funzionato più che bene e aveva diciamo era questa fase qua di dell'offerta di linea è gestita da delle interfacce di Microsoft OX.

_[immagine]_**  
Emanuele Merlo** 32:24  
Cardi.

_[immagine]_**  
Spreafico Paolo** 32:24  
Caro.

_[immagine]_**  
Emanuele Merlo** 32:25  
Queste diciamo raccoglievano i dati però sono state sostituite per l'interfaccia appunto di Mendis dalla Repeting dalla pagina operatore di OP Center OKE tramite diciamo questa sostituzione si hanno diciamo dei benefits.

_[immagine]_**  
Spreafico Paolo** 32:26  
Queste diciamo raccoglievano i dati però sono state sostituite per l'interfaccia appunto di me, dall'operatore OKE tramite diciamo questa sostituzione si hanno delle.  
Diciamo dei benefits perché diciamo che l'interfaccia è più integrata, è più configurabile, ci possono essere messi dei blocchi, degli hyperlocking e poi appunto i dati vengono poi tutti raccolti.

_[immagine]_**  
Emanuele Merlo** 32:46  
Perché diciamo che l'interfaccia è più integrata, è più configurabile, ci possono essere messi dei blocchi, degli interlocking e poi appunto i dati vengono poi tutti raccolti diciamo in un unico.

_[immagine]_**  
Spreafico Paolo** 32:59  
Diciamo in un unico in un unico repository da qui poi possono essere estratti per fare tutte le per gestire PPI, per gestire reportistica e compagnia bella no? E poi anche l'operatore con questa diciamo caratteristica.

_[immagine]_**  
Emanuele Merlo** 33:02  
Da cui poi possono essere estratti per fare tutte per gestire KPI, per gestire reportistica e compagnia no. E poi anche l'operatore con questa diciamo caratteristica legata a linkersys no quindi a questa gestione documentale.

_[immagine]_**  
Spreafico Paolo** 33:15  
Del legata a no, quindi a questa gestione documentale unificata può vedere direttamente nella linea, può vedere direttamente in linea anche istruzioni, immagini.

_[immagine]_**  
Emanuele Merlo** 33:20  
Può vedere direttamente nella linea, può vedere direttamente in linea anche istruzioni, immagini per confrontare per eseguire comunque determinate sezioni e quindi diciamo è una gestione molto più integrata no rispetto a quella la X diciamo è.

_[immagine]_**  
Spreafico Paolo** 33:30  
Per confrontare, per eseguire comunque determinate ispezioni e quindi diciamo è una gestione molto più integrata rispetto a quella diciamo è vista come 1 1 cosa precedente basic questa qua invece?

_[immagine]_**  
Emanuele Merlo** 33:40  
L'ho vista come 1 1 cosa precedente basic questa qua invece quello che forniremo è 1 1 cosa più moderna, più configurabile che può essere evoluta nel tempo con grazie a Rechange Inquest.

_[immagine]_**  
Spreafico Paolo** 33:45  
Quello che forniremo è 1 1 cosa più moderna, più configurabile, che può essere evoluta nel tempo con grazie a delle change e che ha caratteristiche diciamo abbastanza diverse. Le aree confronto le vediamo sono appunto il lancio di ordine.

_[immagine]_**  
Emanuele Merlo** 33:56  
E che ha caratteristiche, diciamo abbastanza diverse. Le aree del confronto le vediamo sono appunto il lancio di ordine, la dichiarazione di come eseguire in difetto e come vedere i documenti in linea. OK, quindi farvi vedere tanto per tanto per farvi capire, abbiamo messo le immagini.

_[immagine]_**  
Spreafico Paolo** 34:03  
La dichiarazione dei documenti in linea immagini OK, allora il caso uno no, quindi questo qua è l'avanzamento di fabbrica dove l'operatore può dichiarare.

_[immagine]_**  
Emanuele Merlo** 34:13  
OK allora il caso uno no. Quindi questo qua è l'avanzamento di fabbrica dove l'operatore può dichiarare dichiarare le ispezioni no può vedere se cliccando uno di questi tasti mi diceva.

_[immagine]_**  
Spreafico Paolo** 34:23  
Potete dichiarare le estensioni no può vedere se cliccando uno di questi tasti mi diceva mi diceva Dati di qualità no?

_[immagine]_**  
Emanuele Merlo** 34:31  
Mi diceva, dati, dati, qualità no?  
Può può dichiarare una determinata il valore di una determinata iscrizione, allora è.

_[immagine]_**  
Spreafico Paolo** 34:36  
Può può dichiarare una determinata il valore di una determinata iscrizione, allora è.

_[immagine]_**  
Emanuele Merlo** 34:48  
Finito il concetto del benestare da Dio, vuoi fare il benestare da Dio? Sì, no, e in tal caso si parla.

_[immagine]_**  
Spreafico Paolo** 34:48  
Finito il concetto del benestare d'avvio, vuoi fare il benestare d'avvio? Sì, no. E in tal caso skippava.

_[immagine]_**  
Emanuele Merlo** 34:58  
Applichiamo una regola base che a noi poi fa sempre piacere, un controllo applicato e un controllo registrato. Punto quindi.

_[immagine]_**  
Spreafico Paolo** 34:59  
Applichiamo una regola base che a noi qualità fa sempre piacere, un controllo applicato è un controllo registrato. Punto quindi.

_[immagine]_**  
Emanuele Merlo** 35:09  
Tutto quello che gli dite di fare, tutte le caratteristiche di controllo che hanno inserite loro le devono fare. Se ne saltano una mezza molto semplice, non dichiarano più la produzione.

_[immagine]_**  
Spreafico Paolo** 35:09  
Tutto quello che gli dite di fare, tutte le caratteristiche di controllo che voi inserite loro le devono fare, se ne saltano una mezza molto semplice, non dichiarano più la produzione.  
OK.

_[immagine]_**  
Emanuele Merlo** 35:29  
Sì, appunto, perché diciamo vengono introdotti questi, questi, questi blocchi funzionali e diciamo qui appunto, questo qua è quello vecchio, no, questo qua invece è quello nuovo qua appunto tramite questo tasto in cui si apriranno i documenti. Qui si qua abbiamo fatto vedere un esempio di un documento che può.

_[immagine]_**  
Spreafico Paolo** 35:29  
Sì, appunto, perché diciamo vengono introdotti questi, questi, questi blocchi funzionali, diciamo qui appunto, questo qua è quello vecchio, no, questo qua mi dice è quello nuovo qua appunto, tramite questo password.  
Qua vi ho fatto vedere un esempio di un documento che può seguire, diciamo che si è appicchiato al AA questa a questa operation no e qui diciamo c'è l'elenco di tutte le opzioni da fare, c'è anche il controllo grafico no?

_[immagine]_**  
Emanuele Merlo** 35:46  
E insomma può essere accoppiato al AA questa a questa operation? No. E qui diciamo c'è l'elenco di tutte le sezioni da fare. C'è anche un controllo, un feedback grafico? No, può essere inserimento, non può diventare rosso verde a seconda comunque.

_[immagine]_**  
Spreafico Paolo** 36:00  
Può essere inserimento, non può diventare rosso verde a seconda comunque della tollerance che è stata configurata, diciamo precedentemente e diciamo e poi una volta che diciamo tutti i dati ci sono informati.

_[immagine]_**  
Emanuele Merlo** 36:04  
Della tolerance che è stata configurata diciamo precedentemente e diciamo e poi una volta che diciamo tutti i dati sono confermati, possono essere salvati, possono essere inviati diciamo al server e questo poi permetterà di andare avanti con l'avanzamento dell'ordine quindi?

_[immagine]_**  
Spreafico Paolo** 36:16  
Di.

_[immagine]_**  
Emanuele Merlo** 36:22  
Dichiarare poi II good o dichiarare poi gli scarpe eccetera no, quindi io sono sostituito da questo qui nuovo, vai avanti, questo qua per quanto riguarda appunto, diciamo che appunto.

_[immagine]_**  
Spreafico Paolo** 36:32  
Vai avanti per quanto riguarda appunto, diciamo che appunto.

_[immagine]_**  
Emanuele Merlo** 36:41  
Le text sono diverse, i tipi di contro di qualità possono essere diversi, ma poi lo vedremo OK, ci sarà comunque diciamo un cambiamento, un miglioramento a livello di usabilità dell'interfaccia grafica.

_[immagine]_**  
Spreafico Paolo** 36:41  
Le text sono diverse, i tipi di progetualità possono essere diversi, ma poi lo vedremo. OK, ci sarà comunque c'è un cambiamento a livello di usabilità dell'interfaccia.

_[immagine]_**  
Emanuele Merlo** 36:55  
Ma il blocco funzionale l'abbiamo detto prima, appunto questi queste ispezioni se sono dichiarate diciamo in quella in quel ciclo sono bloccate, vanno eseguite prima del vanno eseguite praticamente all'inizio dell'ordine o.

_[immagine]_**  
Spreafico Paolo** 36:56  
Il blocco funzionale l'abbiamo detto prima, appunto questi queste ispezioni se sono dichiarate diciamo in quella in quel ciclo sono bloccanti, vanno eseguite prima del vanno eseguite praticamente all'inizio dell'ordine.  
O anche OE anche all'inizio del turno, perché l'ordine era stato messo in pausa. Però poi ci prenderemo anche il lato pratico, come vedere come fare tutte queste cose. Vai avanti.

_[immagine]_**  
Emanuele Merlo** 37:11  
Anche all OE anche all'inizio del turno, perché l'ordine è stato messo in pausa. Però poi ci vedremo anche il lato pratico. Come vedere come fare tutte queste cose? Vai avanti.  
L'altra diciamo panoramica, no del della sostituzione, no del diciamo del miglioramento, la dichiarazione dello scarto, ad esempio.

_[immagine]_**  
Spreafico Paolo** 37:22  
L'altra diciamo panoramica, no del della sostituzione, no del diciamo del miglioramento, la dichiarazione dello scarto, ad esempio.

_[immagine]_**  
Emanuele Merlo** 37:35  
Qui nella stessa interfaccia si poteva anche dichiarare una non conformità OK, quindi un determinato pezzo che aveva un certo tipo di difetto OK.

_[immagine]_**  
Spreafico Paolo** 37:35  
Quindi nella stessa interfaccia si poteva anche dichiarare una non conformità, OK, quindi un determinato pezzo che aveva un certo tipo di difetto, OK?

_[immagine]_**  
Emanuele Merlo** 37:47  
Lo sapete meglio di me, ovviamente. Come funziona questa e causare il riscatto, quindi, com'era prima che avevamo la.

_[immagine]_**  
Spreafico Paolo** 37:48  
Lo sapete meglio di me, ovviamente. Come funziona questa? Quindi, com'era prima che dedicavamo la causale di scarto, oggi l'interfaccia è fatta a birilli.

_[immagine]_**  
Emanuele Merlo** 37:58  
Per causare il discarto oggi l'interfaccia è fatta a birilli, quindi si possono collegare una e qui c'è la cosa che appunto accennavamo prima, no?

_[immagine]_**  
Spreafico Paolo** 38:04  
Quindi si possono collegare una o più causali di scarto senza nessun problema. E qui c'è la cosa che appunto accennavamo prima, no, una cosa di Stato. Prima magari era uno Stato diretto, adesso invece può essere anche una candidate, quindi una quarantena quindi?

_[immagine]_**  
Emanuele Merlo** 38:13  
Una casa di scatto prima magari era uno scatto diretto, adesso invece può essere anche una candidate, quindi una quarantena, quindi diciamo non è uno scatto diretto, diciamo il pezzo poi va valutato e viene eseguita l'operazione di sentencing, no?

_[immagine]_**  
Spreafico Paolo** 38:22  
Diciamo non è uno scarto diretto, diciamo il pezzo poi va valutato e che poi vedremo un mese fa. Ecco un'informazione importante nel momento in cui un vetro viene dichiarato scarso e quindi?

_[immagine]_**  
Emanuele Merlo** 38:31  
Che poi vedremo in realtà. Ecco un'informazione importante, nel momento in cui un pezzo viene dichiarato scarto, quindi in media è un pezzo morto, non più recuperabile né col profilo della qualità né area scarti. Nessuno. Quello è un pezzo a tutti gli effetti rottamato.

_[immagine]_**  
Spreafico Paolo** 38:40  
Il Millie Screp è un pezzo morto, non più recuperabile né col profilo attualità né area scarpi nessuno, quello è un pezzo a tutti gli effetti rottamato.

_[immagine]_**  
Emanuele Merlo** 38:49  
Tutti i pezzi che invece richiedono la rivalutazione, scarti estetici, tutto ciò che arriva in nell'area motivi, per intenderci, deve essere dichiarato come candidi.

_[immagine]_**  
Spreafico Paolo** 38:50  
Tutti i pezzi che invece richiedono la rivalutazione, scarti estetici, ecco, tutto ciò che arriva in nell'area motivi, per intenderci, deve essere dichiarato come candidi.

_[immagine]_**  
Emanuele Merlo** 38:59  
Perché va in quarantena, appunto, che è dove viene fatta l'analisi. OK, provo un'altra domanda, hai detto che si può dare una o più causali di stato, se non gestisci poi metti PM.

_[immagine]_**  
Spreafico Paolo** 39:00  
Mi hai detto che si può dare una o più causali di scarto, allora lui a oggi te ne calcola solo come quantità.  
Una ovviamente do per scontato che fintanto che sia una quarantena posso avere 231 causale di scarto quando sentenziate che ci sia solo un motivo.

_[immagine]_**  
Emanuele Merlo** 39:18  
Ovviamente do per scontato che fintanto che sia una quarantena posso avere 231 caudale di scarpe quando sentenziate che ci sia solo un motivo.

_[immagine]_**  
Spreafico Paolo** 39:32  
Cioè mi aspetto che sia un transitorio e se fa io in teoria da lì posso fare scarto diretto con 234 cosa di scarto potenzialmente potrebbe agli operatori abbiamo detto di inserirne una e una soltanto.

_[immagine]_**  
Emanuele Merlo** 39:32  
Mi aspetta che sia un transitorio e se fa in teoria da lì posso fare scatto diretto con 234 cosa di scatto, quindi in realtà già l'operatore potrebbe agli operatori abbiamo detto di inserirne una e una soltanto.  
Perché se no impazzite voi a slinkare tutto?

_[immagine]_**  
Spreafico Paolo** 39:50  
Perché sennò impazzite voi a slinkare tutto.

_[immagine]_**  
Emanuele Merlo** 39:56  
Agli operatori abbiamo limitato il numero di causali a 9, in modo tale che non.

_[immagine]_**  
Spreafico Paolo** 39:56  
Agli operatori abbiamo limitato il numero di causali a 9, in modo tale che non.

_[immagine]_**  
Emanuele Merlo** 40:04  
Avessero la lista di 360 causali disponibili.

_[immagine]_**  
Spreafico Paolo** 40:04  
Avessero la lista di 360 causali disponibili.  
Quindi l'operatore è fisicamente impedito di dichiarare visualizza 9 causali visualizza 9 causali.

_[immagine]_**  
Emanuele Merlo** 40:11  
Visualizza 9 causali, visualizza 9 causali ma se devo dichiarare un pezzo e per errore lo dico a 9 causali.

_[immagine]_**  
Spreafico Paolo** 40:28  
Una causale, perché la quantità è una, hai 9 causali, quindi se tu entri per CDI tu ti troverai sotto le 9 causali, ma con quantità una. Se dopo tu fai le analisi, ovviamente impazzisci perché a seconda della causale che troverai, lui ti tirerà su sempre quel pezzo.

_[immagine]_**  
Emanuele Merlo** 40:30  
E uno hai 9 causali, quindi se tu entri per c tu troverai sotto le 9 causali ma con quantità una e dopo tu fai le analisi, ovviamente impazzisci perché a seconda della causale che troverai gli indicherà su sempre quel pezzo.  
Dipende da come fai l'analisi dei dati o suggerimento sempre una ma prima suggerimento possiamo possiamo testarlo o possiamo verificarlo dopo su Power BI che non posso mettere quindi una vediamo.

_[immagine]_**  
Spreafico Paolo** 40:48  
Dipende da come fai l'analisi dei dati dopo suggerimento sempre una a una suggerimento possiamo possiamo testarlo, possiamo verificarlo dopo sul Power BI perché però vorrei vorrei più che altro vincolare in linea che non possa mettere più di una causale. Vabbè vediamo, è una CR successiva.

_[immagine]_**  
Emanuele Merlo** 41:06  
E sicuro per tra una settimana non ce l'hai.

_[immagine]_**  
Spreafico Paolo** 41:06  
Di sicuro per tra una settimana non ce l'hai.

_[immagine]_**  
Emanuele Merlo** 41:10  
OK quindi quella l'altra caratteristica diciamo del miglioramento no ci può essere da questa interfaccia operatore integrata è la visione dei documenti linkati documents.

_[immagine]_**  
Spreafico Paolo** 41:14  
Diciamo ci può essere da questa interfaccia operatore integrata è la visione dei documenti linkati documents che vengono diciamo.

_[immagine]_**  
Emanuele Merlo** 41:29  
Che vengono diciamo vengono visualizzati caricandoli tramite questo pulsante dal vostro linker sys caricandoli ma anche contestualizzandoli no quindi diciamo che vengono caricati.

_[immagine]_**  
Spreafico Paolo** 41:31  
Vengono visualizzati caricandoli tramite questo pulsante caricandoli ma anche contestualizzandoli no, quindi diciamo che vengono caricati gli elementi, i documenti relativi.

_[immagine]_**  
Emanuele Merlo** 41:44  
Gli elementi, i documenti relativi al ciclo che si sta eseguendo e quella qua non so se la possiamo vedere, possiamo vedere.

_[immagine]_**  
Spreafico Paolo** 41:48  
Al ciclo che si sta eseguendo.  
Quella qua non so se la possiamo vedere, possiamo vedere. C'è ovviamente 2 2 modi no per il caso documento, uno diciamo esterno che si apre una foto APP che fa vedere i documenti laggiù c'è anche una versione diciamo building.  
Si parte direttamente dal prodotto, non da OP 7 da Siemens, dove in questa in questo pannello si possono caricare tramite configurazione i documenti legati a quel prodotto, a quel ciclo. OK Paolo, scusami se ti interrompo nuovamente.

_[immagine]_**  
Emanuele Merlo** 42:10  
Fatta direttamente dal prodotto da Siemens, dove in questo pannello si possono caricare tramite configurazione i documenti legati a quel prodotto, a quel ciclo. OK Paolo, scusami se ti interrompo nuovamente.  
Altra novità rispetto a oggi, noi oggi abbiamo l'interfaccia di caricamento dei documenti, quindi noi oggi carichiamo su linkersys, carichiamo PDF, la faccio facile, andiamo su schiacciamo un bottone con carica su AX.

_[immagine]_**  
Spreafico Paolo** 42:26  
Altra novità rispetto a oggi, noi oggi abbiamo l'interfaccia di caricamento dei documenti, quindi noi oggi carichiamo su linkersys, lì scarichiamo il PDF la faccio facile, andiamo sul schiacciamo un bottone con carica su AX.

_[immagine]_**  
Emanuele Merlo** 42:42  
E poi gli diamo un passo, un pile per alimentare questo, quando voi caricate su linkersys in automatico viene sparato di qua.

_[immagine]_**  
Spreafico Paolo** 42:43  
E poi gli diamo un pasto, un file per linkare tutto dimenticatevela semplicemente quando voi caricate su linkersys in automatico viene sparato di qua.  
Son 5 son 5.000 € che mi dovete dare grazie a testa.

_[immagine]_**  
Emanuele Merlo** 42:57  
Ok, questo qua come com'è adesso e come sarà tra pochi giorni, è vicino.

_[immagine]_**  
Spreafico Paolo** 43:04  
Come è adesso e come sarà tra pochi giorni per vicino, OK?

_[immagine]_**  
Emanuele Merlo** 43:12  
OK, ecco, vediamo l'altra novità diciamo sempre nell'ottica di vedere diciamo tutti gli elementi grafici ma anche quindi anche i concerti che ci sono dietro che compongono il risultato finale. OKE poi.

_[immagine]_**  
Spreafico Paolo** 43:15  
Ecco, vediamo l'altra novità, diciamo sempre nell'ottica di vedere diciamo tutti gli elementi grafici, ma anche quindi anche i concetti che ci sono dietro che compongono il risultato finale. OKE poi.

_[immagine]_**  
Emanuele Merlo** 43:31  
Piano piano vedremo invece tutte le operazioni che portano AA queste cose qui, quindi andiamo direttamente. Il risultato più finale di tutti è diciamo dal punto di vista di un operatore di qualità, da un manager di qualità è vedere i report legati alla quality? No, ovviamente.

_[immagine]_**  
Spreafico Paolo** 43:31  
Piano piano vedremo invece tutte le operazioni che portano AA queste cose qui, quindi andiamo direttamente. Il risultato più finale di tutti è diciamo dal punto di vista di un operatore di qualità, da manager di qualità è vedere i report legati alla.  
Alla quality no veramente. Quali sono questi dati? Facciamoli vedere, poi magari li vedremo live diciamo nella parte operativa del trading locale.

_[immagine]_**  
Emanuele Merlo** 43:50  
Quali sono questi Napoli facciamoli vedere, poi magari li rivedremo live diciamo nella parte operativa del Trading, OK?  
Quindi allora?

_[immagine]_**  
Spreafico Paolo** 43:59  
Quindi, allora?

_[immagine]_**  
Emanuele Merlo** 44:02  
Perché è importante l'integrazione di Power bi? Il punto numero 1 è per capire quali sono i dati. I dati diciamo che sono arrivati da SAP no? Quindi quali sono gli ordini?

_[immagine]_**  
Spreafico Paolo** 44:02  
Perché è importante l'integrazione di Power bi? Il punto numero 1 è per capire quali sono i dati. I dati diciamo che sono arrivati da SAP, no? Quindi quali sono gli ordini, su quale, su quale equipment, su quali isole vengono eseguiti?

_[immagine]_**  
Emanuele Merlo** 44:17  
Su quale, su quali, su quali isole vengono eseguiti, quali materiali producono, che materiali che bombino, quindi che materiali hanno in ingresso, che materiali hanno in uscita o quali?

_[immagine]_**  
Spreafico Paolo** 44:21  
Quali materiali producono, che materiali che bombono, quindi che materiali hanno d'ingresso, che materiali hanno in uscita, quali, quali contenitori, qual è il patch?

_[immagine]_**  
Emanuele Merlo** 44:33  
Quali, quali contenitori, qual è il batch? Tutte queste queste informazioni sono anche nel nostro sistema, diciamo nelle pagine, quelle che dicevano la prima pagina, la basic. Trovate queste informazioni però non sono aggregate.

_[immagine]_**  
Spreafico Paolo** 44:37  
Tutte queste queste informazioni sono anche nel nostro sistema, diciamo nelle pagine, quelle che dicevano la prima pagina, la basic, trovate queste informazioni però non sono aggregate e filtrate così bene come possono essere.

_[immagine]_**  
Emanuele Merlo** 44:49  
E filtrate così bene come possono essere in report generati ad hoc su Power BI no. Quindi diciamo questa parte qua di navigare no attraverso gli ordini, attraverso i prodotti serial number.

_[immagine]_**  
Spreafico Paolo** 44:53  
In report generati ad hoc su Power BI no, quindi diciamo questa parte qua.  
Di navigare? No, attraverso gli ordini, attraverso i prodotti serial number e quant'altro. Tutti gli elementi no che compongono il vostro il vostro run time no. Quindi diciamo la vostra fase operativa. Questa parte qui è molto importante.

_[immagine]_**  
Emanuele Merlo** 45:06  
E quant'altro. Tutti gli elementi no che compongono il vostro il vostro runtime no. Quindi diciamo la vostra fase operativa. Questa parte qui è molto importante la genealogia globale. OK, perché?

_[immagine]_**  
Spreafico Paolo** 45:17  
La genealogia globale OK, perché Power BI da diciamo strumenti grafici o comunque da delle dashboard, delle cose molto più potenti ovviamente della singola tabella no? E quindi queste cose qui.

_[immagine]_**  
Emanuele Merlo** 45:21  
Power bi da diciamo strumenti grafici o comunque da delle dashboard delle cose molto più potenti ovviamente della singola tabella no? E quindi queste cose qui diciamo la genealogia ricordiamo che è un grafo.

_[immagine]_**  
Spreafico Paolo** 45:33  
Diciamo la genealogia. Ricordiamo che è un grafo a livello matematico, no? Perché diciamo sono diciamo nodi, no, trasformazioni di oggetti che si trasformano da uno all'altro, no?

_[immagine]_**  
Emanuele Merlo** 45:36  
A livello matematico no, perché diciamo sono diciamo nodi, no trasformazioni di oggetti che si trasformano da uno all'altro no e in diversi processi no. Questo qua crea comunque.

_[immagine]_**  
Spreafico Paolo** 45:48  
E in diversi processi no. Questo qua crea comunque un grafo e diciamo che questo fa un diario perfetto, no? Per visualizzare no questa complessità no. Ad esempio, diciamo il caso di prima no, il washing prima del washing c'è l'ossidation no.

_[immagine]_**  
Emanuele Merlo** 45:51  
Un grafo e diciamo che questo Power bi è perfetto, no? Per visualizzare no, questa complessità no. Ad esempio, dicevamo, il caso di prima no, il washing prima del washing c'è l'ossidation no.  
Dopo il washing c'è l'oxidation, dopo l'oxidation c'è la altre cose. Questa catena può essere vista come una cosa, diciamo uno a uno.

_[immagine]_**  
Spreafico Paolo** 46:08  
Dopo il washing c'è l'ossidation, dopo l'ossidation c'è la c'è il Paint piuttosto altre cose.

_[immagine]_**  
Emanuele Merlo** 46:23  
Però molto più interessante vederla nel suo complesso, no? Cioè Power BI ha gli strumenti per fare questa cosa qua. Analisi degli scarti, quindi vedere quanti scarti ci sono stati durante quel durante non so shift la.

_[immagine]_**  
Spreafico Paolo** 46:23  
Però molto più interessante vederla nel suo complesso no se Paolo ha gli strumenti per fare questa cosa qua, analisi degli scarti, quindi vedere quanti scarti ci sono stati durante quel durante non so lo shift la.

_[immagine]_**  
Emanuele Merlo** 46:39  
La week a seconda cerco il prodotto aggregati in tutti i modi pensabili, OK.

_[immagine]_**  
Spreafico Paolo** 46:39  
La week a seconda cerco il prodotto aggregati in tutti i modi pensabili.

_[immagine]_**  
Emanuele Merlo** 46:47  
Le quality extension sono state eseguite, le quality extension che i risultati hanno avuto anche lì diciamo ci sono dei report, delle dashboard apposta e vediamo poi tutti i dati praticamente.

_[immagine]_**  
Spreafico Paolo** 46:47  
Le quality session sono state eseguite le quality session che i risultati hanno avuto anche lì diciamo ci sono dei report, delle dashboard apposta e vediamo poi tutti i dati praticamente.

_[immagine]_**  
Emanuele Merlo** 47:03  
Si può costruire sulle non conformance che sono le causali di scarto, la situazione logistica no. Cosa c'è a vela no negli stop su SAP no.

_[immagine]_**  
Spreafico Paolo** 47:03  
Si può costruire sui non conformance che sono le causali di scatto, la situazione logistica no. Cosa c'è? A V la no negli stock su SAP no.

_[immagine]_**  
Emanuele Merlo** 47:17  
Se sono allineati eccetera. E poi in generale anche la creazione di KPI che è fondamentale, no per.

_[immagine]_**  
Spreafico Paolo** 47:18  
Se sono allineate eccetera. E poi in generale anche la creazione di PPI che è fondamentale, no? Per Power BI ha un prodotto anche estremamente, uno può anche generarsi delle dashboard al lavoro, non so se avete mai visto, comunque è molto potente no? Come sistema e poi?

_[immagine]_**  
Emanuele Merlo** 47:26  
Power bi ha prodotto anche estremamente configurabile, uno può anche generarsi delle dashboard al volo, non so se avete mai visto, comunque è molto potente no come sistema e poi?  
O seguire l'evoluzione no del cioè magari un anno dopo, magari creerete altre dashboard, altre altre visualizzazioni incrociate di tutti questi dati qua sono giusto dei dei degli esempi no che avete adesso e che vedremo tra.

_[immagine]_**  
Spreafico Paolo** 47:36  
O seguire l'evoluzione no del cioè magari mi dà, magari creerete altre dashboard, altre altre visualizzazioni incrociate e quindi tutti questi dati non ci sono dei degli esempi no che avete adesso e che vedremo.

_[immagine]_**  
Emanuele Merlo** 47:53  
Vai avanti, quindi vediamo dal punto di vista grafico cos'è che succede, questo qua c'è già, no?

_[immagine]_**  
Spreafico Paolo** 47:53  
Vai avanti, quindi vediamo dal punto di vista grafico cos'è che succede, questo qua c'è già, no?

_[immagine]_**  
Emanuele Merlo** 48:00  
Quindi ci sono dei report particolari dove vengono vedete dove qui si vede i work center, il tipo di materiale.

_[immagine]_**  
Spreafico Paolo** 48:01  
Quindi ci sono dei report particolari dove vengono vedete, dove qui si il tipo di materiale.

_[immagine]_**  
Emanuele Merlo** 48:11  
Pagare i russi, io no.

_[immagine]_**  
Spreafico Paolo** 48:12  
Fare routing no?

_[immagine]_**  
Emanuele Merlo** 48:14  
Tutti questi concetti qua per quelli di vedere uno può anche filtrare.

_[immagine]_**  
Spreafico Paolo** 48:15  
Questi concetti qua proprio per vedere, uno può anche filtrare per cercare, per esempio voglio sapere, ma questo tipo lì, no?

_[immagine]_**  
Emanuele Merlo** 48:19  
Qui per cercare ad esempio voglio sapere, ma questo tipo di questo tipo di prodotto in che World Center è associato, no?  
E allora qui ecco che si può fare, no?

_[immagine]_**  
Spreafico Paolo** 48:30  
E allora qui a che vedere scrivere un messaggio, no?

_[immagine]_**  
Emanuele Merlo** 48:34  
Che è chiaro, no? Come cosa? Cosa succede con queste con questo tipo di navigazione? È uguale al nostro di adesso? Sì, perfetto. OK, via passa quello dopo.

_[immagine]_**  
Spreafico Paolo** 48:34  
OK, chiaro no? Come cosa cosa succede con queste con questo tipo di navigazione è uguale al nostro? Sì, via passa a quello dopo.

_[immagine]_**  
Emanuele Merlo** 48:48  
Questa qui è appunto 1 1 visualizzazione grafica di una genealogia no? Quindi si parte da un contenitore e si vede come il contenitore da che operazione è stato trasformato a cosa ha contribuito per generare.

_[immagine]_**  
Spreafico Paolo** 48:49  
Questa qui è appunto 1 1 visualizzazione grafica di una genealogia, no? Quindi si parte da un contenitore e si vede come il contenitore da che operazione è stato trasformato a cosa ha contribuito per generare.

_[immagine]_**  
Emanuele Merlo** 49:05  
Dei pezzi in un'altro contenitore? No, questa qui è la il concetto di genealogia no. Quindi questo link, questo collegamento che viene creato attraverso le fasi dalle dichiarazioni di.

_[immagine]_**  
Spreafico Paolo** 49:06  
Dei pezzi in un'altro contenitore? No, questa qui è la il concerto di genealogia, no? Quindi questo link, questo collegamento che viene creato attraverso le fasi dalle dichiarazioni di.

_[immagine]_**  
Emanuele Merlo** 49:21  
Per sicurezza di ingresso e di uscita di su una determinata isola, OK, Ciao.

_[immagine]_**  
Spreafico Paolo** 49:21  
La richiesta di ingrasso su una determinata isola.

_[immagine]_**  
Emanuele Merlo** 49:29  
Per avanti di questo qua se io parto dal CD finito mi dice tutti i CD che utilizza per arrivare a quello.

_[immagine]_**  
Spreafico Paolo** 49:31  
E questo qua se io parto da CD finito quindi c'è tutti ICD che sono utilizzati per arrivare a quello.

_[immagine]_**  
Emanuele Merlo** 49:39  
Se tu parti dal CDI finito vuoi sapere tutti i suoi papà, se tu parti dal CDI finito qual è il componente, vuoi sapere attenzione, la genealogia o la tracciabilità.

_[immagine]_**  
Spreafico Paolo** 49:40  
Se tu parti dal CDI finito vuoi sapere tutti i suoi papà, se tu parti dal CDI finito ma del componente vuoi sapere tutti i figli, quindi attenzione, la genealogia o la tracciabilità.

_[immagine]_**  
Emanuele Merlo** 49:57  
È sempre in due versi chi mi ha creato.

_[immagine]_**  
Spreafico Paolo** 49:57  
E sempre in due versi, chi mi ha creato?

_[immagine]_**  
Emanuele Merlo** 50:02  
Io ho generato i quadri di tutti e due.

_[immagine]_**  
Spreafico Paolo** 50:02  
Chi ho generato?

_[immagine]_**  
Emanuele Merlo** 50:06  
Il sistema ci dà la possibilità di andare o avanti o indietro, quindi attenzione, come ponete, come vi ho sempre detto, come ponete la domanda?

_[immagine]_**  
Spreafico Paolo** 50:06  
Il sistema ci dà la possibilità di andare o avanti o indietro.  
E certo, quindi attenzione, come ponete, come vi ho sempre detto, come ponete la domanda.

_[immagine]_**  
Emanuele Merlo** 50:20  
Se voi mi dite cosa ho generato, cosa ho prodotto da questo, io vado a valle, se voi mi dice, se voi mi un'altra domanda, come ho prodotto questo pezzo?

_[immagine]_**  
Spreafico Paolo** 50:20  
Se voi mi dite cosa ho generato, cosa ho prodotto da questo, io vado a valle, se voi mi dice, se voi mi ponete la domanda come ho prodotto questo pezzo?

_[immagine]_**  
Emanuele Merlo** 50:37  
Parlo a Monte.

_[immagine]_**  
Spreafico Paolo** 50:37  
Vado a monte.

_[immagine]_**  
Emanuele Merlo** 50:40  
Ragazzi, facciamolo chiara e \*\*\*\*\*\*\*, il sistema è un utile idiota, fa quello che ci viene, quello che ti viene chiesto di fare.

_[immagine]_**  
Spreafico Paolo** 50:40  
Ragazzi facciamola chiara e \*\*\*\*\*\*\*, il sistema è un'utile idiota, fa quello che ci quello che gli viene chiesto di fare.

_[immagine]_**  
Emanuele Merlo** 50:48  
Se mi dite fatemi vedere cosa ho prodotto con questo vai in avanti.

_[immagine]_**  
Spreafico Paolo** 50:49  
Se gli dite fatemi vedere cosa ho prodotto con questo va in avanti.  
Come è stato prodotto, vai indietro.

_[immagine]_**  
Emanuele Merlo** 50:55  
Come è stato prodotto? Vai indietro. Riesci comunque a tornare indietro? Attenzione, noi qui e Don Paolo siamo nel mondo, siamo nel perimetro.

_[immagine]_**  
Spreafico Paolo** 50:59  
Sterna intermedia, riesci comunque a tornare indietro? Attenzione, noi qui il buon Paolo l'ha specificato, siamo nel mondo MES, siamo nel perimetro di Curno.

_[immagine]_**  
Emanuele Merlo** 51:11  
Di turno.  
Legati alle macchine, quindi a tutti gli effetti, produzione interna, movimenti interni. Se vi ricordate una premessa, io vi ho parlato di tre sistemi, sistema messa, le macchine, sistema SAP.

_[immagine]_**  
Spreafico Paolo** 51:14  
Legati alle macchine, quindi a tutti gli effetti, produzione interna, movimenti interni, se vi ricordate, nella premessa io vi avevo parlato di tre sistemi, sistema messa le macchine, sistema SAP.

_[immagine]_**  
Emanuele Merlo** 51:29  
Qua il centrale e due nel sistema di magazzino.

_[immagine]_**  
Spreafico Paolo** 51:31  
Il centrale, chiamiamolo così, EVM, sistema di magazzino.

_[immagine]_**  
Emanuele Merlo** 51:36  
Noi a oggi siamo nel primo mondo, un mondo di fabbrica.

_[immagine]_**  
Spreafico Paolo** 51:36  
Noi a oggi siamo nel primo mondo, mondo di fabbrica.

_[immagine]_**  
Emanuele Merlo** 51:41  
Le interazioni tra il mondo di fabbrica e il mondo fisico EVM sono coperte da questo.

_[immagine]_**  
Spreafico Paolo** 51:41  
Le interazioni tra il mondo di fabbrica e il mondo fisico EVM son coperte da questo report.

_[immagine]_**  
Emanuele Merlo** 51:50  
Se ho una fase di conto lavoro esterna, devo saltare su un sistema?

_[immagine]_**  
Spreafico Paolo** 51:50  
Se ho una fase di conto lavoro esterna, esempio LAR, devo saltare sul sistema?

_[immagine]_**  
Emanuele Merlo** 51:59  
Tappa che è diverso. Questi tre sistemi hanno tre logiche completamente diverse in avanzamento di fabbrica e all'interno dello stabilimento noi abbiamo tracciabilità puntuale a livello di singola.

_[immagine]_**  
Spreafico Paolo** 51:59  
Sap che è diverso.

_[immagine]_**  
Emanuele Merlo** 52:14  
CDHU.

_[immagine]_**  
Spreafico Paolo** 52:14  
CD di Hu.

_[immagine]_**  
Emanuele Merlo** 52:17  
Da fornitore io so che gli ho mandato un match, so che gli ho mandato un lotto, non ho garanzia che lui m'abbia preso e consumato da questo specifico match e mi abbia prodotto questo specifico match.

_[immagine]_**  
Spreafico Paolo** 52:17  
Da fornitore io so che gli ho mandato un batch.  
So che io ho mandato un lotto, non ho garanzia che lui mi abbia preso e consumato da questo specifico batch e mi abbia prodotto questo specifico batch.

_[immagine]_**  
Emanuele Merlo** 52:35  
So che ti ho mandato 1000 pezzi e me ne hai resi 1000, però se io ad esempio ti mando un lotto di 1000 pezzi in 10 transazioni sul mese, io riesco a dire ho mandato il primo CD da 100 pezzi in quattro.

_[immagine]_**  
Spreafico Paolo** 52:35  
So che t'ho mandato 1000 pezzi e me ne hai resi 1000.  
Però se ad esempio ti mando un lotto di 1000 pezzi in 10 transazioni sul mese io riesco a dire ho mandato il primo CD da 100 pezzi, il quattro e poi il sei me ne è rientrato uno dal contorno di 100 pezzi di.

_[immagine]_**  
Emanuele Merlo** 52:52  
E poi sei n'è rientrato uno per controllare di 100 pezzi e dico praticamente sì, praticamente cosa succede? Che tu sull'ultimo cassone probabilmente gli stai accodando anche il primo del nuovo lotto.

_[immagine]_**  
Spreafico Paolo** 52:58  
Teoricamente sì, praticamente cosa succede che tu sull'ultimo cassone probabilmente gli stai accodando anche il primo del nuovo lotto?

_[immagine]_**  
Emanuele Merlo** 53:09  
Molto probabilmente nel caso di che garanzia hai, se non la buona volontà del nostro caro fornitore di tenere separati i due lotti.

_[immagine]_**  
Spreafico Paolo** 53:09  
Molto probabilmente nel caso di LR che garanzia hai se non la buona volontà del nostro caro fornitore di tenere separati i due lotti?  
OK quindi la genealogia, fintanto che siamo interno e il materiale si muove interno a Brembo, possiamo ragionarla in modo molto più stringente a livello di CDI la faccio facile.

_[immagine]_**  
Emanuele Merlo** 53:24  
Quindi la genealogia intanto che siamo interno il materiale si muove interno a Brembo possiamo ragionarla in modo molto più stringente a livello di CD la faccio facile quando mando al fornitore.

_[immagine]_**  
Spreafico Paolo** 53:37  
Quando mando al fornitore devo allargare e andare a livello di batch?

_[immagine]_**  
Emanuele Merlo** 53:39  
Devo allargare e andare a livello diverso.  
Quindi attenzione, sempre come ponete la domanda, in che contesto andiamo a lavorare e in che mondo andiamo a lavorare? Per esempio, se ci vuole chiaramente in cui di solito mi gira una bolla, io riesco a ricavare ICD.

_[immagine]_**  
Spreafico Paolo** 53:43  
Quindi attenzione, sempre come ponete la domanda, in che contesto andiamo a lavorare e in che mondo andiamo a lavorare? Prego io per esempio, se c'ho il piano cliente in cui di solito mi girano la bolla, io riesco a ricavare ICD.  
Tu sì, tu riesci a ricavare ICD di spedizione dal CD di spedizione, tu sai con i tuoi CDI perché tu leghi la bolla di spedizione ai CDI di spedizione.

_[immagine]_**  
Emanuele Merlo** 54:00  
Riesci a ricavare ICD di spedizione? Esatto, dal CD di spedizione posso dare i tuoi CD perché tu vedi la bolla di spedizione ai CD di spedizione se.  
Da lì riesci perché hai sempre il CD ed è partito da qui, tra virgolette, quando.

_[immagine]_**  
Spreafico Paolo** 54:15  
Da lì riesci a tracciare perché hai sempre il CD ed è partito da qui ti perdi tra virgolette quando vai sui controlavoristi esterni a livello di batch.  
Livello di patch, attenzione, so il patch. So che t'ho mandato 1000 pezzi di questo patch, però so 500 a inizio luglio e gli altri 500 a fine agosto. Quello lì lo perdo no ce l'hai tu, sai che l'hai mandato.

_[immagine]_**  
Emanuele Merlo** 54:32  
Cioè io non so che ho mandato 1000 pezzi di questo però non so che te ne ho mandati 500 a inizio luglio e gli altri 500 a fine agosto. Tu sai che l'hai mandato?  
Sai neanche che se tutto questo 500 tipo 500.

_[immagine]_**  
Spreafico Paolo** 54:47  
Sai anche chi ha ricevuto questo 500 più altri 500 hai l'incognita fisica di che cosa ha fatto il fornitore?

_[immagine]_**  
Emanuele Merlo** 54:52  
Fare l'incognita di che cosa ha fatto il fornitore?  
Di sistema.

_[immagine]_**  
Spreafico Paolo** 54:59  
A livello logico tu ce l'hai logico, CE l'hai a livello fisico, io le mani non ce le metto.

_[immagine]_**  
Emanuele Merlo** 55:07  
Per oggi.

_[immagine]_**  
Spreafico Paolo** 55:07  
Com'è oggi?  
Scusami Paolo.

_[immagine]_**  
Emanuele Merlo** 55:13  
Paolo, Fornitori LR perché non OK?

_[immagine]_**  
Spreafico Paolo** 55:14  
Aspetta allora fornitori LR, perché non ha OK?

_[immagine]_**  
Emanuele Merlo** 55:20  
Per brinder gatti.

_[immagine]_**  
Spreafico Paolo** 55:21  
Per brimver gatti.

_[immagine]_**  
Emanuele Merlo** 55:24  
Sono questi due fornitori, verrà messo in una postazione SAP direttamente da loro. Quindi loro mi diranno cosa mangiano e cosa spuntano. Sentiranno quindi produzione esterna, non hanno avanzamento di fabbrica, non hanno il MES, hanno SAP, quindi abbiamo una transazione logica.

_[immagine]_**  
Spreafico Paolo** 55:24  
Sono questi due fornitori, verrà messo una postazione SAP direttamente da loro. Quindi loro mi diranno cosa mangiano e cosa sputano. No produzione esterna, non hanno avanzamento di fabbrica, non hanno il MES, hanno SAP, quindi abbiamo una transazione logica.

_[immagine]_**  
Emanuele Merlo** 55:43  
Ciao.  
Perfetto.  
Quindi ricapitola comunque in pratica questo grafo viene creato, se torni indietro viene creato da questa pagina repetiti scusami.

_[immagine]_**  
Spreafico Paolo** 55:53  
In pratica questo grafo viene creato.

_[immagine]_**  
Emanuele Merlo** 56:08  
Questa pagina qua quando vengono dichiarate consumi produzioni qui no completamente in quel momento quando l'operatore clicca diciamo che dice consumato scannerizza un container nell'isola.

_[immagine]_**  
Spreafico Paolo** 56:08  
Questa pagina qua i consumi qui no completamente quando l'operatore clicca diciamo che dice consumato scannerizza un container nell'isola.

_[immagine]_**  
Emanuele Merlo** 56:23  
E dichiara un contegno in quel momento lì crea questo che può essere ovviamente complesso. Perfetto, torniamo indietro.

_[immagine]_**  
Spreafico Paolo** 56:23  
E scandali. E chiaro, contento di non riuscire. In quel momento lì si crea questo che può essere ovviamente multiplo e complesso. Perfetto, torniamo indietro.

_[immagine]_**  
Emanuele Merlo** 56:39  
Qui appunto si fa vedere l'esempio di una dashboard no più complessa, che aggrega comunque le causali di scarto.

_[immagine]_**  
Spreafico Paolo** 56:40  
Qui appunto sta a vedere l'esempio di una dashboard no più complessa che aggrega comunque le cose registrato.

_[immagine]_**  
Emanuele Merlo** 56:49  
In.

_[immagine]_**  
Spreafico Paolo** 56:50  
Mi.

_[immagine]_**  
Emanuele Merlo** 56:52  
E che a per fare una mattina insieme non è.

_[immagine]_**  
Spreafico Paolo** 56:52  
Di che?  
E siamo i politici e.

_[immagine]_**  
Emanuele Merlo** 56:58  
Scappa dei conti per.  
No, li aggrega per causale OK nel tempo.

_[immagine]_**  
Spreafico Paolo** 57:02  
No, le aggrega per causale OK nel tempo.

_[immagine]_**  
Emanuele Merlo** 57:07  
Cai.

_[immagine]_**  
Spreafico Paolo** 57:07  
Dai questa domanda, ma quindi questi bruscotti praticamente la ci invece?

_[immagine]_**  
Emanuele Merlo** 57:14  
Pagando è giusto, posso anche fornire questo qua.

_[immagine]_**  
Spreafico Paolo** 57:14  
Pagando il giusto posso anche fornirveli sottobanco, allora tutti questi cruscotti sono già disponibili, vi verranno attivati appena siete live.

_[immagine]_**  
Emanuele Merlo** 57:17  
Allora tutti questi cruscotti sono già disponibili, ne verranno attivati appena set live. A oggi i cruscotti sono attivi per ostrava e i dati che state vedendo sono i dati live di ostrava.

_[immagine]_**  
Spreafico Paolo** 57:27  
A oggi i cruscotti sono attivi per ostrava e i dati che state vedendo sono i dati Live di Ostrava. Dopo ve li faccio vedere per giocare, quindi non vi preoccupate da questo punto di vista.

_[immagine]_**  
Emanuele Merlo** 57:33  
Coppola di farsi vedere capitale.  
Non mi preoccupate da questo tempo.  
Andrea un po l'affetto.

_[immagine]_**  
Spreafico Paolo** 57:41  
Cambierà un po l'aspetto delle nostre dashboard.

_[immagine]_**  
Emanuele Merlo** 57:49  
Dovremmo fare 1 1 cernita completa di tutti quelli che abbiamo, perché?

_[immagine]_**  
Spreafico Paolo** 57:49  
Dovremmo fare 1 1 cernita completa di tutti i database che abbiamo, perché?  
Cioè incontri la dashboard PPM, poi ci sono una serie di altre dashboard che si collegano. Dobbiamo fare il punto della situazione con Paolo. Se qua ci sono strumenti, appunto, tecnicamente, che aggregano i dati comunque del tempo e.

_[immagine]_**  
Emanuele Merlo** 57:56  
Dashboard BPM, queste qua sono strumenti appunto tecnicamente intelligent che aggregano i dati comunque nel tempo.  
Business Power BI, diciamo uno dei leader di questo tipo di software, no? Quindi le possibilità sono davvero praticamente infinite, no? Una volta una volta estratti i dati.

_[immagine]_**  
Spreafico Paolo** 58:16  
E diciamo è uno dei leader di questo tipo di software, no? Quindi le possibilità sono davvero praticamente infinite, no? Una volta una volta estratti i dati.

_[immagine]_**  
Emanuele Merlo** 58:31  
Diciamo si possono calcolare tantissime cose.

_[immagine]_**  
Spreafico Paolo** 58:31  
Diciamo si possono calcolare tantissime cose.

_[immagine]_**  
Emanuele Merlo** 58:35  
Perfetto, quindi vai avanti.

_[immagine]_**  
Spreafico Paolo** 58:35  
Perfetto, quindi vai avanti.

_[immagine]_**  
Emanuele Merlo** 58:39  
Questa qua cos'è che vediamo?

_[immagine]_**  
Spreafico Paolo** 58:39  
Per questa qua, quella che vediamo.

_[immagine]_**  
Emanuele Merlo** 58:45  
Questo qui è un elenco.

_[immagine]_**  
Spreafico Paolo** 58:45  
Questo qui ha un elenco.

_[immagine]_**  
Emanuele Merlo** 58:48  
Si fa delle ispezioni fatte, vengono caricate con il valore OK.

_[immagine]_**  
Spreafico Paolo** 58:48  
Si parla delle iscrizioni caricate.

_[immagine]_**  
Emanuele Merlo** 58:59  
Ispezioni, anche queste qui sono state inserite, abbiamo detto saranno inserite poi dalla pagina, quella della pagina operatore OK, giusto per essere in breve, dati qualità per CD, quindi sono le registrazioni.

_[immagine]_**  
Spreafico Paolo** 59:03  
E poi dalla pagina OK scusami giusto per essere in brebese dati qualità per CD quindi sono le registrazioni.

_[immagine]_**  
Emanuele Merlo** 59:17  
Del che fanno i nostri ragazzi su le linee che attualmente non troviamo solamente di fabbrica ad alta qualità per civili.

_[immagine]_**  
Spreafico Paolo** 59:18  
Del che fanno i nostri ragazzi sulle linee che attualmente noi troviamo su avanzamento di fabbrica dati qualità per CDI.

_[immagine]_**  
Emanuele Merlo** 59:25  
Il report, quello che stiamo visualizzando, è completamente seduti da casa. Potete vedere cosa stanno registrando i ragazzi, perché questo report è un report di Power BI aggiornato.

_[immagine]_**  
Spreafico Paolo** 59:25  
Il report, quello che stiamo visualizzando è comodamente seduti da casa, potete vedere cosa stanno registrando i ragazzi perché questo report è un report di Power BI aggiornato ogni 10 minuti, quindi praticamente live.

_[immagine]_**  
Emanuele Merlo** 59:41  
Poco.

_[immagine]_**  
Spreafico Paolo** 59:41  
OK.

_[immagine]_**  
Emanuele Merlo** 59:45  
C'è un modo per filtrare i numeri con i limiti pagandosi un se ti fa parte?

_[immagine]_**  
Spreafico Paolo** 59:46  
C'è un modo per filtrare i valori fuori dei limiti, pagando il giusto si può far tutto.  
Ragazzi, devo andare, devo andare in ferie, mi servono soldi.  
Restato adesso proprio un pranzo immensa.  
Col suo badge.

_[immagine]_**  
Emanuele Merlo** 1:00:09  
Credo fra l'altro che sia anche facile sfruttare in Excel. Volevo infatti era la domanda che volevo fare, è possibile sfruttare in Excel? Allora come vi ho detto prima, ci sono dei report già preconfezionati.

_[immagine]_**  
Spreafico Paolo** 1:00:10  
E da fra l'altro che siamo capaci di sfruttare in Excel. La domanda che volevo fare è possibile sfruttare in Excel? Sì, è possibile, è possibile. Allora, come vi ho detto prima, ci sono dei report già preconfezionati.

_[immagine]_**  
Emanuele Merlo** 1:00:26  
E sono disponibili. Non mi piace il Rey Potter, c'è la possibilità di linkare direttamente la base dati su Excel.

_[immagine]_**  
Spreafico Paolo** 1:00:26  
E sono disponibili. Non vi piace il report? C'è la possibilità di linkare direttamente la base dati su Excel.

_[immagine]_**  
Emanuele Merlo** 1:00:35  
E per ricercare se non volete la comodità di Power BI quando dico per questo signore qua, quel signore là in fondo è lui, è che con Power BI si può utilizzare anche il cellulare perché c'è l'applicazione per cui in automatico.

_[immagine]_**  
Spreafico Paolo** 1:00:35  
E ve li giocate come volete la comodità di Power BI qua lo dico per questo signore qua, quel signore là in fondo è lui è che con Power BI.  
Si può utilizzare anche il cellulare perché c'è l'applicazione per cui in automatico si possono refreshare i dati e comodamente da casa e non sto scherzando, ti vedi cosa sta succedendo in pseudo tempo reale?

_[immagine]_**  
Emanuele Merlo** 1:00:54  
Tipo si possono refreshare i dati e comodamente da casa che non sto scherzando, ti vedi cosa sta succedendo in pseudo tempo come poi Marco Marino Fammi vedere cosa hanno fatto di notte che arriva l'aggiornamento.

_[immagine]_**  
Spreafico Paolo** 1:01:06  
Come o al o al mattino fammi vedere cosa hanno fatto di notte ti arriva l'aggiornamento sul telefono.

_[immagine]_**  
Emanuele Merlo** 1:01:12  
Internalice.  
E a livello di dichiarazioni, per esempio un operatore dichiara una misura, poi noi ci accorgiamo ad esempio la Power BI OK, ha dichiarato la misura fuori, andiamo in linea, ripetiamo la misura e in realtà l'operatore ha sbagliato a misurare.

_[immagine]_**  
Spreafico Paolo** 1:01:15  
E a livello di dichiarazioni, se ad esempio un operatore dichiara una misura, poi noi ci accorgiamo ad esempio da Power BI, OK, ha dichiarato una misura fuori, andiamo in linea, ripetiamo la misura e in realtà l'operatore ha sbagliato a misurare.

_[immagine]_**  
Emanuele Merlo** 1:01:30  
Si può modificare, quindi devo fargli riaprire il coso?

_[immagine]_**  
Spreafico Paolo** 1:01:31  
Le trovi tutte, le trovi tutte e due al sistema, le trovi tutte e due perché il sistema fa una copia di quello che c'è. Non puoi più modificare i dati. Quindi una volta che l'operatore.

_[immagine]_**  
Emanuele Merlo** 1:01:45  
Quindi una volta che l'operatore salva i dati, il dato è salvato, dopo il buon Paolo Emanuele ti farà vedere se non fai vedere queste informazioni a sistema.

_[immagine]_**  
Spreafico Paolo** 1:01:47  
Salva il dato, il dato è salvato dopo il buon Paolo o Emanuele ci farà vedere come fare vedere queste informazioni a sistema.

_[immagine]_**  
Emanuele Merlo** 1:01:57  
Attenzione, per entrare in questo sistema vi servono n parametri per cui ordine, patch, CD, base, data, ora, minuto, secondo per andare a beccare questa specifica report quante volte vi capita?

_[immagine]_**  
Spreafico Paolo** 1:01:58  
Attenzione, per entrare in questo sistema vi servono n parametri tra cui ordine, batch, CD, fase, data, ora, minuto, secondo per andare a beccare qual è lo specifico record? Quante volte vi.  
Capita.

_[immagine]_**  
Emanuele Merlo** 1:02:17  
Il potrebbe non è.

_[immagine]_**  
Spreafico Paolo** 1:02:30  
Si pone, ci ragioniamo, dai.

_[immagine]_**  
Emanuele Merlo** 1:02:30  
E c'è anche da dire che poi anche la grafica che il valore diventa rosso no? Cioè quando non è conformance magari magari può aiutare leggermente. Probabilmente all'inizio magari l'operatore ci parla che esce rosso clicca OK.

_[immagine]_**  
Spreafico Paolo** 1:02:46  
Clicca OK solito la mia esperienza appunto poi.

_[immagine]_**  
Emanuele Merlo** 1:02:50  
Nei progetti di solito dalla mia esperienza appunto. Poi c'è una pagina che si chiama maintenance, no pagina di maintenance permette a un user di modificare comunque certi certi valori diciamo nel database. Questo qui di solito però di solito ad esempio la pagina maintenance di un progetto.

_[immagine]_**  
Spreafico Paolo** 1:02:54  
Di solito c'è una pagina che si chiama maintenance, no pagina di maintenance permette a un di modificare comunque certi valori diciamo quindi però di solito ad esempio la pagina maintenance nel Life Cycle di un progetto.

_[immagine]_**  
Emanuele Merlo** 1:03:10  
Viene fatta, non so, magari alla terza season no, cioè non è la priorità adesso è andare da poi, cioè di solito è così, nemmeno nei progetti che ho messo io che questi aggiustamenti vengono fatti in genere se una cosa diciamo a livello logico, se una cosa la puoi cambiare su SAP no o su.

_[immagine]_**  
Spreafico Paolo** 1:03:10  
Viene fatta, non so, magari alla terza season, no? Cioè non è la priorità adesso è andare da poi, cioè di solito è così. Nel momento che ho visto io questi aggiustamenti vengono fatti in genere se una cosa diciamo a livello logico, se una cosa la puoi cambiare su SAP no o su.

_[immagine]_**  
Emanuele Merlo** 1:03:29  
Sistema esterno allora poi devi avere qualche modo manuale di programmi però questo qui poi sono che diciamo fanno parte del E se invece riavviano il sistema nel momento che devono compilare?

_[immagine]_**  
Spreafico Paolo** 1:03:29  
Tema esterno, allora poi devi avere qualche modo manuale di poi riallinearti però questo qui poi se invece riavviano il sistema nel momento che devono compilare.

_[immagine]_**  
Emanuele Merlo** 1:03:47  
È un sistema, diciamo il sistema MES è un sistema diciamo ridondante integrato no? E diciamo che viene garantita la transazionalità del dato no? Cioè quindi riavviano il sistema.

_[immagine]_**  
Spreafico Paolo** 1:03:48  
E no, è un sistema, diciamo il sistema MES è un sistema diciamo ridondante integrato no? E diciamo che viene garantita la transazionalità del dato no, cioè quindi.

_[immagine]_**  
Emanuele Merlo** 1:04:04  
La sanità no, che magari la richiesta viene fatta questa cosa qua allora è un il sistema costruito in modo diciamo no, cioè garantisce la transazionalità.

_[immagine]_**  
Spreafico Paolo** 1:04:05  
La sanità no che magari la richiesta viene fatta quando questa cosa qua allora è un il sistema costruito in modo diciamo no, cioè garantisce la transazionalità.

_[immagine]_**  
Emanuele Merlo** 1:04:23  
E diciamo un sistema, diciamo ma non sei troppo diciamo.

_[immagine]_**  
Spreafico Paolo** 1:04:24  
Te te la faccio \*\*\*\*\*\*\*.  
Va bene Paolo, grazie, sì.

_[immagine]_**  
Emanuele Merlo** 1:04:35  
Diciamo che le richieste sono persistenti, quindi se si riavviasse quando si riavvia vede la richiesta in coda e la consuma sì, non vengono perse.

_[immagine]_**  
Spreafico Paolo** 1:04:38  
Quindi se si riavviasse quando si riavvia vede la richiesta in coda e la consuma te la faccio facile il bug che avevamo no si attaccano, nel senso che se non completano il.

_[immagine]_**  
Emanuele Merlo** 1:04:49  
Che avevamo? No, se pagano, nel senso che se non completano il.  
La compilazione, il sistema non li fa dichiarare, possono spendere tutte le volte che.

_[immagine]_**  
Spreafico Paolo** 1:04:58  
La compilazione, il sistema non li fa dichiarare, possono spegnere tutte le volte che vogliono, ma il sistema gli dice col cippolo.

_[immagine]_**  
Emanuele Merlo** 1:05:08  
E domani non dichiarano la promozione.

_[immagine]_**  
Spreafico Paolo** 1:05:11  
E domani?  
E domani non dichiarano la produzione.

_[immagine]_**  
Emanuele Merlo** 1:05:19  
Scusa per sempre. Attenzione, tu prima hai detto a ogni benestare da Dio, oggi il benestare da Dio è legato a ogni start dell'ordine.

_[immagine]_**  
Spreafico Paolo** 1:05:20  
Scusami, dopo mi taccio per sempre.  
Attenzione, tu prima hai detto a ogni benestare d'avvio, oggi benestare d'avvio è legato a ogni start dell'ordine.

_[immagine]_**  
Emanuele Merlo** 1:05:36  
Quindi se qualcuno mette in pausa l'ordine o termina l'ordine o cambia il turno.

_[immagine]_**  
Spreafico Paolo** 1:05:36  
Quindi se qualcuno mette in pausa l'ordine o termina l'ordine o cambia il turno.

_[immagine]_**  
Emanuele Merlo** 1:05:43  
Questo signore qua, quando fai lo stato dell'ordine, ti dice, mi fai i controlli, grazie, sennò non dichiari.

_[immagine]_**  
Spreafico Paolo** 1:05:44  
Questo signore qua quando fai lo start dell'ordine ti dice.  
Mi fai i controlli? Grazie, sennò non dichiari.

_[immagine]_**  
Emanuele Merlo** 1:05:56  
Anche nel cambio colore, perché il cambio colore si chiama cambio codice, cambiando codice riparti da zero e ti dice adesso mi rifai tutto, grazie.

_[immagine]_**  
Spreafico Paolo** 1:05:56  
Anche nel cambio colore. Anche nel cambio colore. Perché il cambio colore si chiama cambio codice. Cambiando codice riparte da zero e ti dice adesso mi rifai tutto. Grazie.

_[immagine]_**  
Emanuele Merlo** 1:06:08  
Ed è il motivo per cui stavamo guardando i controlli pochi giorni fa, la voce benestare, avvio necessario, OK, non necessario, non esiste più, è sempre necessario quando compare.

_[immagine]_**  
Spreafico Paolo** 1:06:08  
Ed è il motivo per cui stavamo guardando i controlli pochi giorni fa, la voce benestare, avvio necessario, OK, non necessario, non esiste più, è sempre necessario quando compare.

_[immagine]_**  
Emanuele Merlo** 1:06:28  
OK, perfetto, quindi ci siamo, siamo questa qua, quindi la panoramica credo che sia finita.

_[immagine]_**  
Spreafico Paolo** 1:06:28  
Perfetto, quindi ci siamo, siamo, penso che sia finita.

_[immagine]_**  
Emanuele Merlo** 1:06:36  
Sì, queste qui sono altre cose che possono essere, diciamo.

_[immagine]_**  
Spreafico Paolo** 1:06:37  
Sì, queste qui sono altre cose che possono essere, diciamo.

_[immagine]_**  
Emanuele Merlo** 1:06:42  
Sono altri diciamo data source non possibili per Power BI OK di vedere appunto diciamo altri elementi di quello che riguarda la gestione della qualità no, quindi le non conformancy, ossia le.

_[immagine]_**  
Spreafico Paolo** 1:06:42  
Sono altri, diciamo, data source non possibili per Power BI, vedere appunto.  
Diciamo altri elementi di quello che riguarda la gestione della qualità, no? Quindi le non conformancy, ossia le dichiarazioni di Stato di stock, perché ovviamente gli stock no sono.

_[immagine]_**  
Emanuele Merlo** 1:06:58  
Le dichiarazioni di Stato di stock, perché ovviamente gli stock no sono le cose no, di ingresso no che devono essere rese disponibili all'operato di linea.

_[immagine]_**  
Spreafico Paolo** 1:07:06  
Le cose no, l'ingresso no, che devono essere rese disponibili.

_[immagine]_**  
Emanuele Merlo** 1:07:13  
E se lo stock non è non è disponibile, allora non è neanche disponibile. Poi il dato di qualità, no? Quindi anche controllare gli stock è importante. Il dato di scarto no, perché deve esserci materiale potrebbe scattare qualcosa.

_[immagine]_**  
Spreafico Paolo** 1:07:13  
E se lo stock non è non è disponibile, allora non è neanche disponibile. Poi il dato di invalidità no. Quindi anche controllare gli stock è importante. Il dato di scarto? No, perché deve esserci materiale.

_[immagine]_**  
Emanuele Merlo** 1:07:29  
E poi darci un KPI qui diciamo che lo scopo finale poi di del della gestione della qualità è da creare queste KPI no, quindi queste queste queste funzioni no che misurano le performance.

_[immagine]_**  
Spreafico Paolo** 1:07:29  
Poi darci il KPI diciamo che lo scopo finale poi di del della gestione della qualità è in realtà creare questi KPI no, quindi queste queste queste funzioni no che misurano le performance.

_[immagine]_**  
Emanuele Merlo** 1:07:47  
Di una determinata linea per un determinato prodotto in un determinato periodo no. E qui diciamo che c'è tutto il e grazie a queste no che sono scelte per ogni azienda in modo strategico no.

_[immagine]_**  
Spreafico Paolo** 1:07:48  
Di una determinata linea per un determinato prodotto in un determinato periodo no. E qui diciamo che c'è tutto e grazie a queste che sono scelte per ogni azienda nel modo strategico no.

_[immagine]_**  
Emanuele Merlo** 1:08:04  
Se posso, c'è anche un'obiezione, no? Ad esempio in progetti che ho partecipato, cioè ogni anno che hanno un set diverso, no, perché poi studiano i dati e dicono no, mi interessa sapere il rapporto che c'è tra questa.

_[immagine]_**  
Spreafico Paolo** 1:08:04  
Se posso c'è anche un'evoluzione, no? Ad esempio i miei progetti a cui ho partecipato, cioè ogni anno che hanno un set diverso di che poi studiano i dati, dicono no, mi interessa sapere il rapporto che c'è tra questa.

_[immagine]_**  
Emanuele Merlo** 1:08:19  
Questa quantità e diciamo Power BI è lo strumento perfetto no per creare per creare questo genere di funzioni e crearci dei report e quindi fare delle valutazioni.

_[immagine]_**  
Spreafico Paolo** 1:08:20  
Questa quantità in quell'altra parte e quindi creare una e diciamo Power PI è uno strumento perfetto no per creare per creare questo genere di funzioni e crearci dei report e quindi fare delle valutazioni.

_[immagine]_**  
Emanuele Merlo** 1:08:35  
Aziendali di business dietro ai dati di qualità.

_[immagine]_**  
Spreafico Paolo** 1:08:36  
Aziendali di business dietro ai dati di qualità.

_[immagine]_**  
Emanuele Merlo** 1:08:40  
Ya.

_[immagine]_**  
Spreafico Paolo** 1:08:41  
No.

_[immagine]_**  
Emanuele Merlo** 1:08:42  
OK, adesso entriamo nella parte diciamo vera, no? Cioè adesso abbiamo visto, no?

_[immagine]_**  
Spreafico Paolo** 1:08:42  
OK, adesso entriamo nella parte diciamo vera no del cioè adesso abbiamo visto no?

_[immagine]_**  
Emanuele Merlo** 1:08:49  
Tutti gli elementi di tutto quello che ci sarà inerente alla qualità, no? Quindi cos'è questa qualità, cos'è che produce, dov'è che l'operatore scrive i dati, dov'è che li scriveva e dov'è che li scriverà?

_[immagine]_**  
Spreafico Paolo** 1:08:49  
Tutti gli elementi di tutto quello che ci sarà inerente alla qualità, no? Quindi cos'è questa qualità, cos'è che produce, dov'è che l'operatore scrive i dati, dov'è che li scriveva e dov'è che li scriverà?

_[immagine]_**  
Emanuele Merlo** 1:09:04  
A gavilina, tanto per farvi una panoramica di poi cosa se ne fa adesso lasciamo perdere AX, lasciamo perdere Power bi e ci addentriamo dentro a come ha fatto OP center, quindi il software mess OK.

_[immagine]_**  
Spreafico Paolo** 1:09:04  
A grandi linee, tanto per farvi una panoramica di poi cosa siamo fatti adesso lasciamo perdere AX, lasciamo perdere Power BI e ci addentriamo dentro a come ha fatto OP center, quindi il software MES OK.

_[immagine]_**  
Emanuele Merlo** 1:09:21  
Via.

_[immagine]_**  
Spreafico Paolo** 1:09:21  
Via.

_[immagine]_**  
Emanuele Merlo** 1:09:22  
Quindi allora potete andare nella nella Repetitive, se potete aprire anche il computer, magari c'era anche quello documento, quello dati per.

_[immagine]_**  
Spreafico Paolo** 1:09:23  
Quindi allora potete andare nella nella repetitive, se potete aprire avete accesso tutti al sistema dentro nella mail.  
Magari anche cliccando su ingranaggio allora per.

_[immagine]_**  
Emanuele Merlo** 1:09:43  
Ma tu dove l'hai messo? Te l'ho mandato ieri via mail.

_[immagine]_**  
Spreafico Paolo** 1:09:47  
Aspetta un attimo audio, giusto?

_[immagine]_**  
Emanuele Merlo** 1:09:48  
O anche no, anche su coso e anche su, ma non so se è aggiornato con nessuno.  
Controlli per il MES no.

_[immagine]_**  
Spreafico Paolo** 1:10:08  
Allora ti ho mandato il file Claudio.

_[immagine]_**  
Emanuele Merlo** 1:10:10  
Tonati.  
Se cliccate vi appare una mascherina, cliccate l'ingranaggio e poi dovreste avere il per il training aggiornato.

_[immagine]_**  
Spreafico Paolo** 1:10:15  
Allora se cliccate vi appare una mascherina, cliccate l'ingranaggio e poi dovreste avere utilizza il vostro utente di Windows se non se mi confermate che entrate.  
Si è entrato benissimo altri che sono entrati.

_[immagine]_**  
Emanuele Merlo** 1:10:36  
Sì, siamo un ambiente a pre conduzione, quindi potete fare il disastro che volete e non fate il disastro.

_[immagine]_**  
Spreafico Paolo** 1:10:36  
Sì, beh allora l'Aids and SEC è siamo in ambiente pre produzione, quindi potete fare i disastri che volete e non fate disastro.

_[immagine]_**  
Emanuele Merlo** 1:10:46  
Questa qua è la pagina, quella sì.

_[immagine]_**  
Spreafico Paolo** 1:10:48  
La pagina, quella cosiddetta Vertice, sì.

_[immagine]_**  
Emanuele Merlo** 1:10:53  
OK, perfetto, OK, allora qui ci sono.

_[immagine]_**  
Spreafico Paolo** 1:10:54  
Perfetto. OK, allora qui ci sono un po' di dati, no? Allora intanto iniziamo a vedere la reception del Washington.

_[immagine]_**  
Emanuele Merlo** 1:10:59  
Iniziamo a vedere la repetitive ad esempio del primo caso del washing, OK, quindi?

_[immagine]_**  
Spreafico Paolo** 1:11:10  
Ce l'ha il work center di.

_[immagine]_**  
Emanuele Merlo** 1:11:10  
Ce l'hai messo qua? Sì, questo qua ce l'avevamo.  
Dai, allora entra, entra nel work center. Aspetta che non riesco a. È il secondo link, praticamente siamo delle macchine di produzione.

_[immagine]_**  
Spreafico Paolo** 1:11:26  
Ragazzi, allora repetitive, allora il Repetitive è il secondo link, praticamente siamo delle macchine di produzione.  
OK, questo di qua ve lo fa vedere, ma al lato nostro non dovremmo metterci le zampe, è per vostra cultura personale.

_[immagine]_**  
Emanuele Merlo** 1:11:36  
Questo di qua ve lo fa vedere, ma al lato nostro non dovremmo metterci le zampe, è per nostra cultura personale.  
Siamo, stiamo appunto, diciamo, facciamo finta di essere operatori di linea, OK, e vediamo i day by day dei vostri, dei vostri operatori, no, gli operatori di linea, appunto.

_[immagine]_**  
Spreafico Paolo** 1:11:48  
Siamo siamo appunto, facciamo finta di essere operatori di linea, OKE, vediamo il day by day dei dei vostri, dei vostri operatori, no? E operatori di linea proprio.

_[immagine]_**  
Emanuele Merlo** 1:12:00  
È quello che fa la lavorazione che andiamo a vedere. Quindi adesso entriamo, vediamo il primo use case che è questo washing no? Per sapere la repertibile è fatta in modo diciamo attaccata a un'isola e quindi?

_[immagine]_**  
Spreafico Paolo** 1:12:01  
È quello che fa la donazione che andiamo a vedere. OK, quindi adesso entriamo, vediamo il primo use case che è questo washing, no? Per sapere è fatta in diciamo attaccata a un'isola e quindi?

_[immagine]_**  
Emanuele Merlo** 1:12:16  
Diciamo dà l'accesso diretto a quell'isola, a quell'isola lì corrisponde quel work center, che è il work center. Anche il costo è la cosa che in SAP no viene identificata come esecuzione di.

_[immagine]_**  
Spreafico Paolo** 1:12:32  
Di quel tipo di ordine e quindi diciamo che l'operatore verrà bloccato e portato direttamente qui, no? Però diciamo che adesso non è configurato in questa maniera. Noi abbiamo un terminale esterno, non abbiamo quel terminale lì attaccato alla linea che sarà configurato in modo diverso per accedere direttamente.

_[immagine]_**  
Emanuele Merlo** 1:12:32  
Di quel tipo di ordine e quindi diciamo che l'operatore verrà loggato e portato direttamente qui. No, però diciamo che adesso non è configurato in questa maniera. Noi abbiamo un terminale esterno, non abbiamo quel terminale lì attaccato alla linea che sarà.  
Ha configurato in modo diverso per accedere direttamente, quindi dobbiamo farlo a manella e lo facciamo, entriamo lì dentro in questo World Center. Scusate qua riuscite a muovervi? La conoscete? L'avete già mai vista questa?

_[immagine]_**  
Spreafico Paolo** 1:12:51  
E lo facciamo, entriamo lì dentro in questo qua riuscite a muovervi? No, non l'hanno mai vista.

_[immagine]_**  
Emanuele Merlo** 1:13:05  
Non l'avete mai visto, OK?

_[immagine]_**  
Spreafico Paolo** 1:13:06  
Emanuele.

_[immagine]_**  
Emanuele Merlo** 1:13:08  
Allora?  
Adesso il sistema è configurato per far vedere tutti i work center, però ogni macchina sarà poi configurata per vedere il MES collegato a quella macchina lì farà vedere solo solo la macchina giusta. Non si vedranno tutti questi quindi.

_[immagine]_**  
Spreafico Paolo** 1:13:12  
Adesso però ogni macchina sarà poi configurata per vedere adesso quella macchina lì farà vedere solo.  
Solo la macchina non si vedrà. Quindi no, non ci sarà. Perché ripetiamo, questa qua è l'interfaccia grafica che è che è attaccata a all'isola no, al banco di lavoro no.

_[immagine]_**  
Emanuele Merlo** 1:13:31  
No, non ci sarà tanto grafica che è attaccata a all'isola no, al banco di lavoro no, questa terminale quindi.

_[immagine]_**  
Spreafico Paolo** 1:13:45  
Questa terminale, quindi in quel determinato per quel determinato operatore che fa quelle determinate lavorazioni in quel in quell'echipment.

_[immagine]_**  
Emanuele Merlo** 1:13:48  
In quel determinato, per quel determinato operatore che fa quel determinata in quel in quel.  
Senza però tutte queste macchine qua perché ci sarà la linea di washing attaccato ci sarà il terminale della linea di washing, questo terminale andrà direttamente.

_[immagine]_**  
Spreafico Paolo** 1:13:58  
Vede questa interfaccia qua? La repetitive OK, non vede l'altra però tutte queste macchine qua perché sa già qual è il suo work center e va direttamente. Quindi attaccato ci sarà la linea di washing, attaccato ci sarà il terminale della linea di washing e questo terminale andrà direttamente nel work center di washing.

_[immagine]_**  
Emanuele Merlo** 1:14:17  
Credo che si riesce a fare la stessa cosa e tutto quello di montaggio a seconda del montaggio farà quella cosa lì e tutti diciamo tranne mi pare per l'assemblaggio che c'ha 2 2 unità.

_[immagine]_**  
Spreafico Paolo** 1:14:19  
La stessa cosa e tutto di montaggio, a seconda del montaggio, farà quella cosa lì che tutti diciamo allora.

_[immagine]_**  
Emanuele Merlo** 1:14:33  
Normalmente sono già configurati su nome e cognome. Ci sono alcuni casi sporadici in cui lo stesso PC può servire diverse stazioni, per esempio il.

_[immagine]_**  
Spreafico Paolo** 1:14:33  
Normalmente tutti IPC di avanzamento di fabbrica sono già configurati su nome e cognome. Ci sono alcuni casi sporadici in cui lo stesso PC può servire diverse stazioni, esempio il washing, esempio il.

_[immagine]_**  
Emanuele Merlo** 1:14:51  
Il rodaggio lì abbiamo tre macchine, poi il computer uno solo, quindi lì avete l'operatore avrà tre palloncini a seconda della macchina dove va a dichiarare dovrà selezionarla.

_[immagine]_**  
Spreafico Paolo** 1:14:51  
Il rodaggio.  
E lì abbiamo tre macchine, però il computer è uno solo, quindi lì avete l'operatore avrà tre balloncini a seconda della macchina dove va a dichiarare dovrà selezionarla piuttosto che l'area extra controllo.

_[immagine]_**  
Emanuele Merlo** 1:15:06  
Piuttosto che l'area extra controllo, quindi ci sono due centri di lavoro, però fisicamente non son più cattivo.

_[immagine]_**  
Spreafico Paolo** 1:15:09  
Che lì ci sono son due centri di lavoro, però fisicamente un computer suo solo.  
Compra PC hanno cambiato OK, benissimo, scusa non c'è la.  
OK, allora sono le linee open standard con primo montaggio e completamento dovrebbero essere uno o dovrebbe essere uno solo perché è un unico codice, un PC con i due tasti dovrebbe essere.

_[immagine]_**  
Emanuele Merlo** 1:15:24  
OK.

_[immagine]_**  
Spreafico Paolo** 1:15:38  
Dovrebbe essere uno solo a oggi.  
Se son due, son due.  
Se quello che c'era ci sarà, non mi ricordo comunque.  
Capite su questa pagina qui del va bene, adesso andiamo a cercare questa, se vuoi farmi vedere qua appunto questa iconcina qui in basso il vostro profilo diciamo che è dentro e lì potete cambiare ad esempio la lingua.

_[immagine]_**  
Emanuele Merlo** 1:15:54  
Va beh, adesso andiamo a cercare questa macchina qua, appunto questa iconcina qui in basso il vostro profilo diciamo che è dentro e lì potete cambiare ad esempio la lingua, cioè se una delle cose che potete fare.

_[immagine]_**  
Spreafico Paolo** 1:16:07  
Perché non c'è dentro?

_[immagine]_**  
Emanuele Merlo** 1:16:12  
OK, io sono andato adesso a mettere le iniziali della macchina, l'ho trovata e faccio salva e mi trovo.  
Che mi ha scaduto la adesso arrivo scusa.  
Che a me è scaduto, non lo so.  
Pronto.

_[immagine]_**  
Spreafico Paolo** 1:16:32  
C'è una grande.

_[immagine]_**  
Emanuele Merlo** 1:16:33  
Salve.  
Perché la macchina con cui accedi non ha nessun altro utente, non mi non mi accede.

_[immagine]_**  
Spreafico Paolo** 1:16:38  
Perché la macchina con cui accedi non ha nessun altro utente, non riesce a fare un satellite.

_[immagine]_**  
Emanuele Merlo** 1:16:48  
Sì.  
Non l'ho mai visto.  
Scusate, mi riconnetto.

_[immagine]_**  
Spreafico Paolo** 1:17:02  
Però devi avere un copia incolla del profilo di.

_[immagine]_**  
Emanuele Merlo** 1:17:02  
Ma qui non mi prendeva più il click.  
Ma non è che l'hanno riavviato?

_[immagine]_**  
Spreafico Paolo** 1:17:12  
Sì.

_[immagine]_**  
Emanuele Merlo** 1:17:14  
Se per noi.

_[immagine]_**  
Spreafico Paolo** 1:17:15  
Sì.  
Paolo Guidami.

_[immagine]_**  
Emanuele Merlo** 1:17:22  
Puoi condividere teams?

_[immagine]_**  
Spreafico Paolo** 1:17:25  
Paolo Guidami.  
Puoi condividere il teams.  
Emanuele, puoi condividere il teams?

_[immagine]_**  
Emanuele Merlo** 1:17:35  
Come?

_[immagine]_**  
Spreafico Paolo** 1:17:40  
Paolo mira.

_[immagine]_**  
Emanuele Merlo** 1:17:42  
A questo aspetto.  
E qual è la tua? OK, allora SW metti filtra qua SW.

_[immagine]_**  
Spreafico Paolo** 1:17:51  
OK, allora SV metti filtra qua SW.  
Sì.

_[immagine]_**  
Emanuele Merlo** 1:17:58  
OK, questo qui è il nuovo center, diciamo di l'ultimo di.

_[immagine]_**  
Spreafico Paolo** 1:17:59  
OK, questo qui è il Dover Center, diciamo di l'ultimo di.

_[immagine]_**  
Emanuele Merlo** 1:18:04  
Per il washing by Save.

_[immagine]_**  
Spreafico Paolo** 1:18:04  
Rewatching by Save.  
Si.

_[immagine]_**  
Emanuele Merlo** 1:18:10  
Niente.

_[immagine]_**  
Spreafico Paolo** 1:18:24  
OK.

_[immagine]_**  
Emanuele Merlo** 1:18:25  
OK, Bin sedation fatto, fai.  
Però questi qua ci sono, ci sono, qui vediamo, appunto, ci sono degli ordini, ci sono delle icone.

_[immagine]_**  
Spreafico Paolo** 1:18:29  
Questi qua ci sono, ci sono, qui vediamo appunto, ci sono degli ordini, ci sono delle icone.

_[immagine]_**  
Emanuele Merlo** 1:18:38  
Questi qua verde sono ordini, diciamo in stato iniziale, questa qua verde.

_[immagine]_**  
Spreafico Paolo** 1:18:38  
Questi qua verde sono ordini, diciamo in stato iniziale, stavano in una qua verde.

_[immagine]_**  
Emanuele Merlo** 1:18:46  
Qui possiamo vedere la quantità, il workoder, quindi workoder NID, il seriale dell'ordine di produzione. Questo qui è il prodotto, il prodotto da.

_[immagine]_**  
Spreafico Paolo** 1:18:47  
Qui possiamo vedere la quantità, il work order, quindi work order dell'ordine di produzione. Questo qui è il prodotto prodotto da.  
Da creare quindi che finisce con underscore washing prodotto in uscita, il prodotto di ingresso qui non lo vedete quindi la ma non lo vedete?

_[immagine]_**  
Emanuele Merlo** 1:19:04  
In uscita il prodotto di ingresso qui non lo vedete quindi la ma lo dovete vedere aprendo questo determinato.

_[immagine]_**  
Spreafico Paolo** 1:19:20  
C'è anche la priority, quindi per far vedere, diciamo si aspettano che vengano, quindi magari apriamo uno.

_[immagine]_**  
Emanuele Merlo** 1:19:22  
Qui c'è anche la priority, quindi le fa vedere diciamo nell'ordine in cui aspettano che vengono eseguiti, quindi magari apriamone uno.

_[immagine]_**  
Spreafico Paolo** 1:19:34  
Arrivo sì, schiaccia vista.

_[immagine]_**  
Emanuele Merlo** 1:19:36  
Sì, allora questo qui ha l'ordine, questo qui è senza essere.

_[immagine]_**  
Spreafico Paolo** 1:19:44  
Allora questo qui fa l'ordine senza iscrizioni, perché magari prendi l'altro se c'è un'altro prodotto.

_[immagine]_**  
Emanuele Merlo** 1:19:52  
Si può vedere che è senza iscrizioni dai perché magari prendi l'auto se c'è un'altro prodotto 38.

_[immagine]_**  
Spreafico Paolo** 1:19:59  
Tutto.

_[immagine]_**  
Emanuele Merlo** 1:20:00  
Questo qui è 37, allora qui è 30+37, questo qua doveva avercelo invece questo qui.

_[immagine]_**  
Spreafico Paolo** 1:20:01  
Questo qui è 37, allora qui è 37, questo qua doveva 10 invece questo sì.

_[immagine]_**  
Emanuele Merlo** 1:20:07  
Sì.  
E di.

_[immagine]_**  
Spreafico Paolo** 1:20:11  
E Ciao.

_[immagine]_**  
Emanuele Merlo** 1:20:14  
Quindi vediamo, vedete questa iconcina qui arancione, queste iconcine arancione è sono i dati di qualità.

_[immagine]_**  
Spreafico Paolo** 1:20:15  
Quindi vediamo, vedete questa iconcina qui arancione, queste iconcine arancione è sono i dati di qualità, è il nostro benestare d'avvio.

_[immagine]_**  
Emanuele Merlo** 1:20:26  
È il nostro benestare da Dio, dai.  
Lorenzo.  
E adesso beh, non è saltata quella all'ordine e quindi diciamo che questa qua è la lista che è stata configurata dal quality manager per quel ciclo in relazione a quel materiale quindi.

_[immagine]_**  
Spreafico Paolo** 1:20:38  
E quindi diciamo che questa qua è la lista che è stata configurata dal quality manager per quel ciclo in relazione a quel materiale quindi.

_[immagine]_**  
Emanuele Merlo** 1:20:53  
Qui abbiamo un bell'esempio, no? Che avete subito capito, questi qua sono dati di configurazione, dati di qualità configurati nel sistema.

_[immagine]_**  
Spreafico Paolo** 1:20:53  
Qui abbiamo un bell'esempio no che avete subito capito, questi qua sono dati di configurazione dati di qualità configurati nel sistema.

_[immagine]_**  
Emanuele Merlo** 1:21:01  
Strofugati nel sistema che chiamate appunto questa anagrafica dei cicli no, che noi chiamiamo bop process e che voi chiamate ciclo.

_[immagine]_**  
Spreafico Paolo** 1:21:02  
Figurati nel sistema che appunto nelle foto chiamate appunto è questa ragazza dei cicli no che noi chiamiamo e se voi chiamate.

_[immagine]_**  
Emanuele Merlo** 1:21:12  
E per lo stesso work center no, un determinato prodotto no, il 38, il 38 underscore washing no VSH non aveva configurato niente perché non.

_[immagine]_**  
Spreafico Paolo** 1:21:12  
E per lo stesso work center no, un determinato prodotto no, il 38, il 38 underscore washing no vsh non aveva configurato niente. Perché?

_[immagine]_**  
Emanuele Merlo** 1:21:29  
Perché il quality manager non aveva ancora definito no cose per quel prodotto e invece questo qua l'altro prodotto 37 invece?

_[immagine]_**  
Spreafico Paolo** 1:21:29  
Perché il quality manager non aveva ancora definito no le cose per quel prodotto e invece questo qua l'altro prodotto invece?

_[immagine]_**  
Emanuele Merlo** 1:21:38  
Ha configurato tutto queste diciamo queste queste queste ispezioni sono mandatorie? No, se non vengono eseguite tutte non l'ordine non può dichiarare produzione, OK?

_[immagine]_**  
Spreafico Paolo** 1:21:39  
Ha configurato tutto queste diciamo queste queste queste istruzioni sono mandatori? No, se non vengono eseguite tutte non l'ordine non può dichiarare condizioni.

_[immagine]_**  
Emanuele Merlo** 1:21:53  
E una volta inseriti tutti questi dati, ricordiamo cosa succede una volta inseriti questi dati, cosa succede a questi dati? Chi è che mi risponde?

_[immagine]_**  
Spreafico Paolo** 1:21:54  
E una volta inseriti tutti questi dati, ricordiamo cosa succede. Una volta inseriti questi dati, cosa succede a questi dati? Chi è che vi risponde?

_[immagine]_**  
Emanuele Merlo** 1:22:03  
Mi buttiamo via.

_[immagine]_**  
Spreafico Paolo** 1:22:03  
Mi buttiamo via.

_[immagine]_**  
Emanuele Merlo** 1:22:05  
Cosa succede una volta che uno gli ha inseriti? Ditemi le cose che succedono.

_[immagine]_**  
Spreafico Paolo** 1:22:09  
Determina cose che succedono.

_[immagine]_**  
Emanuele Merlo** 1:22:11  
Una volta che siamo inseriti tutti tranne uno, cosa succede? Una volta che li ho inseriti tutti, cosa succede? OKE, poi però invece sotto le quinte, ad esempio legato a Power BI, cosa succede una volta che li ho inseriti?

_[immagine]_**  
Spreafico Paolo** 1:22:11  
Una volta che se uno li ha inseriti tutti tranne uno, cosa succede? Una volta che li ho inseriti tutti, cosa succede? OKE poi però invece sotto le quinte, per esempio legato a Power bi, cosa succede una volta che li ho inseriti?

_[immagine]_**  
Emanuele Merlo** 1:22:29  
Ci crea quella tabella, quindi dopo 10 minuti una volta che li ha inseriti verranno questi dati qua verranno messi in questo contesto? No, in questo ordine, in questo prodotto a quell'ora lì verranno inseriti lì e poi?  
Potranno essere recuperati e visibili immediatamente. L'altro messe nell'altra pagina, quella chiamata Basic. No, uno può vedere immediatamente che si fa. Questo è un caso reale.

_[immagine]_**  
Spreafico Paolo** 1:22:45  
Potranno essere recuperati e visibili immediatamente. Lato MES nell'altra pagina, quella cioè chiamata basic, questo è un caso reale.

_[immagine]_**  
Emanuele Merlo** 1:23:00  
Con dati dei cavolo sotto volutamente è un esempio perché la richiesta che ho fatto io è.

_[immagine]_**  
Spreafico Paolo** 1:23:01  
Con dati del cavolo sotto volutamente.  
Allora è un esempio, perché la richiesta che ho fatto io è.

_[immagine]_**  
Emanuele Merlo** 1:23:13  
Possiamo avere due casi, uno ce li siamo persi, infatti avete detto prima, l'altro ordine non aveva i quality Section, questo ordine qui, passo sotto nelle quality Station potenzialmente sono corrette.

_[immagine]_**  
Spreafico Paolo** 1:23:13  
Possiamo avere due casi, uno ce li siamo persi. Infatti avete visto prima l'altro ordine che non aveva le quality inspection sotto sotto il naso? Questo ordine qui a sotto delle quality inspection potenzialmente sono corrette.

_[immagine]_**  
Emanuele Merlo** 1:23:29  
Sì, però l'ho strafito di turno sbagliato a collegarle volutamente ci farà vedere come fare a rimuovere questo controllo da questo specifico ordine e a sistemare la box.

_[immagine]_**  
Spreafico Paolo** 1:23:29  
Te però lo sperafico di turno ha sbagliato a collegarle, quindi volutamente ci farà vedere come fare a rimuovere questo controllo da questo specifico ordine e a sistemare la box.

_[immagine]_**  
Emanuele Merlo** 1:23:45  
Parecente.  
Terzo caso.

_[immagine]_**  
Spreafico Paolo** 1:23:47  
Terzo caso.

_[immagine]_**  
Emanuele Merlo** 1:23:50  
Non c'ho proprio niente perché mi son dimenticato. I miei amici hanno fatto i furbi, invece di andare sulla open standard uno sono andato sull'open standard due.

_[immagine]_**  
Spreafico Paolo** 1:23:50  
Non c'ho proprio niente perché mi son dimenticato. I miei amici hanno fatto i furbi, invece di andare sulla open standard uno sono andati sull'open standard due.

_[immagine]_**  
Emanuele Merlo** 1:24:00  
Non so niente, il sistema dice.

_[immagine]_**  
Spreafico Paolo** 1:24:00  
Non so niente, il sistema dice.

_[immagine]_**  
Emanuele Merlo** 1:24:06  
Per me guarda che devi fare gli ordini, devi fare l'ordine di qualità, chiama.

_[immagine]_**  
Spreafico Paolo** 1:24:06  
Michele, guarda che devi fare degli ordini, devi fare l'ordine di qualità, chiama.

_[immagine]_**  
Emanuele Merlo** 1:24:13  
La qualità è parte di inserire OK.

_[immagine]_**  
Spreafico Paolo** 1:24:13  
La attualità e fateli inserire.

_[immagine]_**  
Emanuele Merlo** 1:24:17  
Sono tutti i parametri che a oggi il MES riesce a gestirci.

_[immagine]_**  
Spreafico Paolo** 1:24:17  
Son tutti parametri che a oggi il MES riesce a gestirci.

_[immagine]_**  
Emanuele Merlo** 1:24:24  
Un'altra cosa che il buon Paolo ci dirà a breve, io ho parlato prima di open standard uno e open standard due.

_[immagine]_**  
Spreafico Paolo** 1:24:24  
Un'altra cosa che il buon Paolo ci dirà a breve, vi ho parlato prima di open standard uno e open standard due.

_[immagine]_**  
Emanuele Merlo** 1:24:34  
Per il sistema sono due cicli diversi, come ci ha detto prima Paolo sono posso dire sull'open standard uno faccio 10 controlli, sull'open standard due posso fare un controllo solo perché ho gli occhi aggiuntivi perché ho cambiato.

_[immagine]_**  
Spreafico Paolo** 1:24:35  
Per il sistema sono due cicli diversi, come ci ha detto prima Paolo sono posso dire sull'open standard uno faccio 10 controlli sull'open standard due posso fare un controllo solo perché ho pochi occhi aggiuntivi perché ho cambiato.

_[immagine]_**  
Emanuele Merlo** 1:24:53  
Il sistema ci permette, a livello di ogni singolo codice e routing per ogni singola strada, di andare a definire il set di controlli specifici per quella strada.

_[immagine]_**  
Spreafico Paolo** 1:24:54  
Il sistema ci permette a livello di ogni singolo codice e routing, quindi per ogni singola strada, di andare a definire il set di controlli specifici per quella strada.

_[immagine]_**  
Emanuele Merlo** 1:25:06  
Se domani mattina il buon conigli ce lo manda sulla open standard 7, adesso parlando di sistema ti dice.

_[immagine]_**  
Spreafico Paolo** 1:25:06  
Se domani mattina il buon fognini CE lo manda sulla open standard 7, stesso par number, il sistema ti dice.  
Chiama e fatti inserire i controlli perché è sempre legato all'articolo per il quale è settato che deve avere un inspection plan.

_[immagine]_**  
Emanuele Merlo** 1:25:15  
I controlli perché è sempre legato all'articolo per il quale è settato, quindi lo stesso articolo su operativamente come sarà la cosa che quando noi andremo a deliberare il codice, il ciclo?

_[immagine]_**  
Spreafico Paolo** 1:25:25  
Cioè operativamente come sarà la cosa che quando noi andremo a deliberare il codice, il ciclo, l'ultimo passo della delibera sarà caricare a sistema questa checklist se io vado a deliberare una pinza su una linea.

_[immagine]_**  
Emanuele Merlo** 1:25:34  
L'ultimo passo da delibera sarà caricare a sistema questa checklist, se io vado a deliberare una pinza su una linea totalmente manuale o su una linea automatica ci possono nascere due checklist diverse, quindi è questo l'obiettivo che ci sta.

_[immagine]_**  
Spreafico Paolo** 1:25:42  
Totalmente manuale o su una linea automatica possono nascere due checklist diverse, quindi è questo l'obiettivo produttivo, codice e linea quindi.

_[immagine]_**  
Emanuele Merlo** 1:25:53  
C'è una migrazione massiva di tutto quello che c'è oggi.

_[immagine]_**  
Spreafico Paolo** 1:26:03  
C'è una migrazione massiva di tutto quello che c'è oggi, quello che c'è oggi su avanzamento di fabbrica ha 1 ° di dettaglio inferiore perché abbiamo per tutti i codici della stessa linea la stessa checklist.

_[immagine]_**  
Emanuele Merlo** 1:26:06  
Quello che c'è oggi su avanzamento in fabbrica ha 1 ° in dettaglio inferiore perché abbiamo per tutti i codici della stessa linea la stessa checklist.  
Dato che è impossibile rimetter mano a tutte le checklist perché non finiranno più da quando partiremo con in poi adotteremo questa nuova logica, quindi metteremo a checklist solo quello che è l'anagrafica è stata importata in modo massivo, no?

_[immagine]_**  
Spreafico Paolo** 1:26:18  
Dato che è impossibile rimettere mano a tutte le checklist perché non finiremo più da quando partiremo con NES in poi adotteremo questa nuova logica, quindi metteremo nella checklist solo quello che è necessario.  
Fatta in modo massivo no e delle iscrizioni. Però l'associazione non è stata ancora caricata per quello che ha trovato i buchi comunque è pronta. Scusami Paolo dopo mi taccio per sempre fino alla prossima domanda.

_[immagine]_**  
Emanuele Merlo** 1:26:37  
Delle iscrizioni con l'associazione AG Contractor, scusami Paolo per sempre, fino alla prossima domanda.  
Concerto base, non esiste più il controllo per linea, esiste il controllo per l'accoppiata.

_[immagine]_**  
Spreafico Paolo** 1:26:55  
Concetto base, non esiste più il controllo per linea, esiste il controllo per l'accoppiata.

_[immagine]_**  
Emanuele Merlo** 1:27:03  
Linea item e chi comanda e routing cambio il routing, i controlli sono potenzialmente dati definire.

_[immagine]_**  
Spreafico Paolo** 1:27:03  
Linea item e chi comanda è routing, cambio il routing, i controlli sono potenzialmente da ridefinire.

_[immagine]_**  
Emanuele Merlo** 1:27:18  
Cambio il routing fatto da open standard uno più completamento in monoblocco 9 ci sto aumentando.

_[immagine]_**  
Spreafico Paolo** 1:27:18  
Cambio il routing fatto da open standard uno più completamento in modo blocco 9 sto inventando.

_[immagine]_**  
Emanuele Merlo** 1:27:27  
Domani invece del completamento 9 la faccio sul completamento 7 il routing è uguale, è uguale.

_[immagine]_**  
Spreafico Paolo** 1:27:28  
Domani invece del completamento 9 la faccio sul completamento 7 il routing è uguale, è sempre un open standard e un completamento.  
È uguale.

_[immagine]_**  
Emanuele Merlo** 1:27:41  
Quindi avrà un nome diverso, avrà un ciclo diverso, un nome diverso, potenzialmente questo ciclo può averne controlli diversi.

_[immagine]_**  
Spreafico Paolo** 1:27:41  
Quindi avrà un nome diverso, avrà un ciclo diverso, un nome ciclo diverso. Potenzialmente questo ciclo può avere dei controlli diversi.

_[immagine]_**  
Emanuele Merlo** 1:27:52  
Piuttosto facciamo lo stesso aggiuntivo, metto destra, controllo, ho un ciclo a due fasi, un ciclo a tre fasi è uguale ciclo quindi cambio nome, cognome, numero di targa. I controlli vanno ricablati.

_[immagine]_**  
Spreafico Paolo** 1:27:53  
Piuttosto facciamo lo step aggiuntivo, metto l'extra controllo, ho un ciclo due fasi, un ciclo tre fasi è uguale il ciclo, quindi cambia nome, cognome, numero di targa.  
I controlli vanno ricablati anche al completamento solo al completamento perché fino all'uscita da brinver o insomma fino al primo montaggio compreso tutto rimane uguale.

_[immagine]_**  
Emanuele Merlo** 1:28:13  
Fino al primo montaggio compreso tutto rimane uguale, cambia che però per i codici in extra avranno un underscore di qualche tipo.

_[immagine]_**  
Spreafico Paolo** 1:28:21  
Cambia che però l'uscita dal completamento per i codici in extra avranno un underscore di qualche tipo e quindi sarà a tutti gli effetti un nuovo codice da profilare. Una domanda, se indu cambia la conduzione di un ciclo, cambia un tempo ciclo?

_[immagine]_**  
Emanuele Merlo** 1:28:27  
E quindi sarà a tutti gli effetti un nuovo codice da se cambia la produzione di un ciclo, cambia un tempo ciclo, cambia il tempo ciclo.  
Scenderà una nuova revisione del ciclo, è stato messo un copia e incolla, la facciamo semplice, per cui ti clona quanto è esistente sul nuovo ciclo, non far nulla, meno di problematiche.

_[immagine]_**  
Spreafico Paolo** 1:28:41  
Scenderà una nuova revisione del ciclo, è stato messo un copia incolla, la facciamo semplice per cui ti clona quanto è esistente sul nuovo ciclo è trasparente per noi di problematiche.

_[immagine]_**  
Emanuele Merlo** 1:28:56  
Se cambia il solo di un completamento, dovrò ridefinire anche i controlli del montaggio.

_[immagine]_**  
Spreafico Paolo** 1:28:57  
Se cambia il routing solo di un completamento, dovrò ridefinire anche i controlli del primo montaggio rispondimi sulla base di quanto ti ho detto prima.

_[immagine]_**  
Emanuele Merlo** 1:29:08  
Questo è il primo montaggio, ha un booting che si chiama a, il completamento che si chiama B sono due codici diversi, sono ragazzi ragioniamola così, primo montaggio.

_[immagine]_**  
Spreafico Paolo** 1:29:08  
No, perché sul primo montaggio ha un routing che si chiama a, sul completamento ha un routing che si chiama B sono due codici diversi, sono ragazzi ragioniamola così primo montaggio.

_[immagine]_**  
Emanuele Merlo** 1:29:24  
Battendo e butto fuori la vita.

_[immagine]_**  
Spreafico Paolo** 1:29:24  
Battezzo e butto fuori la B.

_[immagine]_**  
Emanuele Merlo** 1:29:27  
Non è routing un 02:00:03 massaggio.

_[immagine]_**  
Spreafico Paolo** 1:29:27  
Nome routing 01:00:03 montaggio.

_[immagine]_**  
Emanuele Merlo** 1:29:32  
Mangio quello che abbiamo scelto dal primo, ma il routine si chiama Paperino. Sono due routine uguali? No, si chiamano in due modi diversi, quindi posso avere se cambio il tempo ciclo mi si copia.

_[immagine]_**  
Spreafico Paolo** 1:29:32  
Mangio quello che mi è uscito dal primo, ma il routing si chiama Paperino. Sono due routing uguali? No, si chiamano in due modi diversi. Quindi posso avere se cambio il tempo ciclo mi si copia.

_[immagine]_**  
Emanuele Merlo** 1:29:48  
Cambio la condizione di si copia, cambio il ciclo del dall'uno dalla macchina uno alla macchina due mi cambia il nome del ciclo e quindi devo andare a lavorarci, però solo per la parte che cambia, solo per la parte che cambia.

_[immagine]_**  
Spreafico Paolo** 1:29:48  
Cambio la conduzione mi si copia, cambio il ciclo del dall'una dalla macchina uno alla macchina due mi cambia il nome del ciclo e quindi devo andare a lavorarci sopra solo per la parte che cambia.

_[immagine]_**  
Emanuele Merlo** 1:30:04  
Ma quello questo perché il primo montaggio è un codice intermedio, questo perché tu la modifica l'hai fatta soltanto su 1 1 ciclo specifico di tutto fisso in produzione, quindi è lì che devi andare a ripristinare i controlli ed è se esposto dalla pressa sei per 90.

_[immagine]_**  
Spreafico Paolo** 1:30:04  
Ma questo perché il primo montaggio è un codice intermedio, questo perché tu la modifica l'hai fatta soltanto su 1 1 ciclo specifico di tutto il flusso di produzione, quindi è lì che devi andare a riprofilare i controlli.  
È la stessa cosa in friction se sposto dalla pressa sei per 90 alla 120 le i cambiamenti che avrò a livello di se io avessi faccio il ciclo pressa.

_[immagine]_**  
Emanuele Merlo** 1:30:24  
Vale 120 le i cambiamenti che avrò da lì sto cambiando macchina quindi se io avessi faccio il ciclo pressa rettifica forno.

_[immagine]_**  
Spreafico Paolo** 1:30:36  
Rettifica forno.

_[immagine]_**  
Emanuele Merlo** 1:30:38  
E questo qua?

_[immagine]_**  
Spreafico Paolo** 1:30:39  
E questo qua è tutto un ordine di produzione che ha tutte e tre le fasi assieme. Non hai più no, esatto, non hai più ordini multifase, hai ogni fase col suo ordine. La stampa scusa è un ordine unico, stampaggio rettifica forno.

_[immagine]_**  
Emanuele Merlo** 1:30:45  
Ordini multifase scusa è un ordine unico stampaggio rettifica forno sì, ma hai tre fasi.

_[immagine]_**  
Spreafico Paolo** 1:30:56  
Sì, ma alle hai tre fasi.

_[immagine]_**  
Emanuele Merlo** 1:31:01  
Ho tre codici, hai 3 3 macchine aspetta, stai anticipando un concetto che vediamo dopo finisci questo dopo te la te lo spiego perché all'interno del dell'arricchimento nel routing.

_[immagine]_**  
Spreafico Paolo** 1:31:02  
Hai tre cose, aspetta, aspetta, aspetta, aspetta. Stai anticipando un concetto che lo vediamo dopo finisci questo dopo te la te lo spiego perché all'interno del dell'arricchimento nel routing.  
Il buon Paolo ci farà vedere che ci sono.

_[immagine]_**  
Emanuele Merlo** 1:31:21  
Don Paolo ci farà vedere che ci sono.

_[immagine]_**  
Spreafico Paolo** 1:31:25  
OP 10 EOP 20 come lo chiami tu. Quindi prima fase stampo, poi faccio il forno, poi faccio la rettifica. Ho tre fasi diverse, il ciclo è uno che comprende tre fasi, il passaggio da una fase all'altra.

_[immagine]_**  
Emanuele Merlo** 1:31:27  
In prima fase stampo, poi faccio il forno, poi faccio la notifica. Ho tre fasi diverse. Il ciclo è uno che comprende tre fasi. Il passaggio da una fase all'altra può prevedere delle caratteristiche di controllo specifiche per la singola fase.

_[immagine]_**  
Spreafico Paolo** 1:31:40  
Può prevedere dei delle caratteristiche di controllo specifiche per la singola fase.

_[immagine]_**  
Emanuele Merlo** 1:31:46  
OK se all'interno dello stesso ciclo mi metto anche la pallinatura sto aumentando il nome del ciclo mi cambia e quindi devo rilegarli tutti o no li devi rilegarli tutti perchè hai aggiunto una fase al ciclo io non posso ad esempio se tolgo la rettifica.

_[immagine]_**  
Spreafico Paolo** 1:31:48  
Se all'interno dello stesso ciclo gli metto anche la pallinatura sto inventando il nome del ciclo mi cambia no li deve rilegare tutti perché hai aggiunto?  
Una fase al ciclo io non posso dire hai cambiato il contenuto?

_[immagine]_**  
Emanuele Merlo** 1:32:06  
Devo rilegare sia allo stampaggio sia sì, certo, sì, in teoria uno potrebbe rischiare di copiare da però poi non automatico.

_[immagine]_**  
Spreafico Paolo** 1:32:20  
In automatico non copi.

_[immagine]_**  
Emanuele Merlo** 1:32:26  
Perfetto. Allora vi faccio una domanda scema, vediamo se mi perché qui? Perché adesso non posso inserire i dati? Perché non ho fatto l'avvio? Cosa facciamo allora dopo? Cos'è che ci dice?

_[immagine]_**  
Spreafico Paolo** 1:32:36  
Perché non ho fatto la cosa facciamo allora?

_[immagine]_**  
Emanuele Merlo** 1:32:50  
E devo guardare una cosa qui, documenti metropolitani si aggiorna. Siamo qua. Sì, la cosa dei documenti. Ecco, vediamo un secondo.

_[immagine]_**  
Spreafico Paolo** 1:32:55  
Documenti che si aggiorna. Sì, la cosa dei documenti vediamo un secondo.

_[immagine]_**  
Emanuele Merlo** 1:33:06  
Si torna nella aspetta che mi fa casino, scusa sì, ma non l'ho perso il tuo, solo che.

_[immagine]_**  
Spreafico Paolo** 1:33:10  
Da ricondividi il mio scusa.

_[immagine]_**  
Emanuele Merlo** 1:33:16  
Non vedo la barra.  
OKOK allora quindi poi Ricapitolando, un'altra cosa che avevamo detto prima è il linked documents con i quali documenti documenti in questo caso qui non sono stati caricati diciamo localmente a opicenter e non saranno.

_[immagine]_**  
Spreafico Paolo** 1:33:20  
Quindi poi Ricapitolando, un'altra cosa prima documenti, documenti in questo caso qui non sono stati caricati, diciamo localmente a 8 7 e non lo saranno.

_[immagine]_**  
Emanuele Merlo** 1:33:35  
E diciamo, questa qua è una feature che è qui ma diciamo non sarà usata in modo operativo perché in modo operativo ci sarà questo link qui che se lo clicchi adesso immagino che mi faccia un not found 404 perché diciamo.

_[immagine]_**  
Spreafico Paolo** 1:33:36  
Diciamo che prima diciamo non si sa usare in modo operativo perché in modo operativo ci sarà questo link che se lo clicchi adesso immagino che si faccia un not found 204 perché diciamo.

_[immagine]_**  
Emanuele Merlo** 1:33:50  
La request è andata, diciamo siamo siamo un ambiente pro e giustamente non ha non ha gli accessi verso perfetto OK, quindi diciamo è tutto chiaro, cosa facciamo, facciamo, prendiamo questo qua, facciamo vedere le operazioni principali tanto per darmi OK, quindi allora facciamo.

_[immagine]_**  
Spreafico Paolo** 1:33:52  
Siamo siamo in ambiente pro prode, giustamente non sono aperti gli accessi verso l'incasys. OK, quindi diciamo è tutto chiaro, cosa facciamo, facciamo, prendiamo questo qua e facciamo vedere l'operazione principale.

_[immagine]_**  
Emanuele Merlo** 1:34:10  
Lo start dell'ora vediamo un secondo le quantità allora questa quantità qua 1000 ci sono ci sono 10 pezzi da produrre giusto poi l'altro quindi possiamo produrre direttamente tutti e 10 direttamente.

_[immagine]_**  
Spreafico Paolo** 1:34:10  
Lo stato dell'ora vediamo secondo le quantità allora questa quantità qua 1000 ci sono ci sono 10 pezzi da produrre giusto poi l'altro, quindi possiamo produrre direttamente tutti i 10 direttamente.

_[immagine]_**  
Emanuele Merlo** 1:34:26  
In tutti e 10 pezzi, quindi fai start.

_[immagine]_**  
Spreafico Paolo** 1:34:27  
In tutti i 10 pezzi, quindi fai start.

_[immagine]_**  
Emanuele Merlo** 1:34:31  
10 quantity start OK.

_[immagine]_**  
Spreafico Paolo** 1:34:31  
10 OK.

_[immagine]_**  
Emanuele Merlo** 1:34:36  
Quindi qua ci sono II tipi, i tipi di contenitore del della destinazione, no del dell'uscita della uscita come devo il mio prodotto finito.

_[immagine]_**  
Spreafico Paolo** 1:34:36  
Quindi qua ci sono II tipi, i tipi di contenitore del della destinazione no del dell'uscita, cioè il RAC, il RAC in uscita come devo il mio prodotto finito?

_[immagine]_**  
Emanuele Merlo** 1:34:51  
Come deve andare via con che le scatole ballo?

_[immagine]_**  
Spreafico Paolo** 1:34:51  
Come deve andare via, con che specifiche di imballo?

_[immagine]_**  
Emanuele Merlo** 1:35:00  
Flavio, guarda che per questo ti servirà questa specifica.

_[immagine]_**  
Spreafico Paolo** 1:35:01  
Ti diranno, guarda che per questo ti servirà questa specifica di imballo per mandarlo via.  
No usa il contenitore punto 45 per questo massimo quantitativo 32 per contenitore usa il cartone con dentro il.

_[immagine]_**  
Emanuele Merlo** 1:35:13  
Cartiglia il contenitore punto 45 per questo massimo quantitativo 32 per contenitore. Ad esempio usa il cartone con dentro il.

_[immagine]_**  
Spreafico Paolo** 1:35:31  
Te dico dimba adesso mi.

_[immagine]_**  
Emanuele Merlo** 1:35:34  
Ti passo chiacchiere lì e io vado a utilizzare.

_[immagine]_**  
Spreafico Paolo** 1:35:36  
La logistica?

_[immagine]_**  
Emanuele Merlo** 1:35:40  
Perché sono legati perfetto. Quindi allora. Quindi diciamo, siamo un operatore, inizia a lavorare, ha selezionato quest'ordine, ha iniziato a lavorare. Questa qua è una fase di washing, quindi.

_[immagine]_**  
Spreafico Paolo** 1:35:41  
Perché sono legati su SAP e quindi noi le spariamo giù.  
E quindi diciamo, questo operatore inizia a lavorare, ha selezionato questo ordine, ha iniziato a lavorare. Questa qua è una fase di washing, quindi metterà diciamo i pezzi, li metterà diciamo nella.

_[immagine]_**  
Emanuele Merlo** 1:35:59  
Metterà diciamo i pezzi, li metterà diciamo nella nella macchina che fa washing ad alta pressione, quindi dovrà vola e poi chiara l'uscita e nel frattempo cos'è che può fare?

_[immagine]_**  
Spreafico Paolo** 1:36:04  
Nella macchina che fa washing ad alta pressione, quindi lavora e poi chiara nel frattempo cos'è che può fare? Cos'è che deve fare? Bene, fare discrezioni per vedere se questo processo può iniziare. OK, fare discrezioni perché?

_[immagine]_**  
Emanuele Merlo** 1:36:14  
Una che deve fare bene, fare le ispezioni per vedere se questo processo può iniziare. OK, quindi dimostrare, fare le ispezioni perchè tutto possa essere primo start, scusa dire che inizia a lavorare, poi fare le ispezioni.

_[immagine]_**  
Spreafico Paolo** 1:36:23  
Tutto possa essere scusa dire che inizia a lavorare, poi fare le iscrizioni, dire che pezzi va tutto bene, dire dichiarare i pezzi in ingresso che mette diciamo nella lavatrice, non so se è una lavatrice però.

_[immagine]_**  
Emanuele Merlo** 1:36:34  
Dire i pezzi in ingresso che mette diciamo nella lavatrice, non so se è una lavatrice.

_[immagine]_**  
Spreafico Paolo** 1:36:46  
No, aspetta, io ti dico, guarda che voglio produrre 10 pezzi, vorrei produrre 10 pezzi.

_[immagine]_**  
Emanuele Merlo** 1:36:48  
Guarda che voglio produrre 10 mesi, vorrei produrre 10 mesi.  
Perché cosa succede? Diventa tu operatore dichiara in quel momento che sei macchina e sei esclusivamente tu su quella macchina in quel periodo di tempo, no? Appena tu clicchi start viene registrato che tu operatore.

_[immagine]_**  
Spreafico Paolo** 1:36:55  
Quindi tu operatore dichiara in quel momento che sei su quella macchina e sei esclusivamente tu su quella macchina in quel periodo di tempo no, appena tu clicchi start viene registrato che tu operatore.

_[immagine]_**  
Emanuele Merlo** 1:37:09  
Sei loggato di dentro e hai iniziato a lavorare. Allora le macchine quando accendono avete visto prima? Io ho selezionato la macchina.

_[immagine]_**  
Spreafico Paolo** 1:37:10  
Allora le macchine quando accendono, avete visto prima che io ho selezionato la macchina?

_[immagine]_**  
Emanuele Merlo** 1:37:23  
E ho detto, sono io salva. In quel momento il sistema ha recepito che io, Paolo Spreafico, sono presente su questa macchina.

_[immagine]_**  
Spreafico Paolo** 1:37:23  
E ho detto, sono io salva. In quel momento il sistema ha recepito che io, Paolo Spreafico, sono presente su questa macchina. Domani tutti i nostri badge, vi parlo della produzione, avranno il barcode.

_[immagine]_**  
Emanuele Merlo** 1:37:34  
Domani tutti i nostri badge per la produzione avranno il backhooter, quindi pistole resteranno e diranno, io sono qui, OK, adesso secondo me qua non lo capite bene perché per l'Aula no? Se avete provato a.

_[immagine]_**  
Spreafico Paolo** 1:37:42  
Quindi pistoletteranno e diranno, Io sono qui.  
Adesso secondo me qua non lo capite bene perché per l'Aula no? Se uno di voi avete provato a aprire questo ordine ve lo fa aprire, cosa che invece non dovrebbe far aprire. No, perché l'accesso è esclusivo, no? C'è un sistema di una volta che.

_[immagine]_**  
Emanuele Merlo** 1:37:54  
Ordine ve lo fa aprire, cosa che invece non dovrebbe far aprire. No, perché l'accesso è esclusivo, no? C'è un sistema di una volta che voi voi siete entrati con il vostro utente, no, quando adesso non è abilitato. In questo caso poi magari lo possiamo abilitare per vederlo.

_[immagine]_**  
Spreafico Paolo** 1:38:02  
Che voi voi siete entrati con il vostro utente, no, quando adesso non è abilitato in questo caso, poi magari lo possiamo abilitare per vederlo.

_[immagine]_**  
Emanuele Merlo** 1:38:11  
Quando se un'altro può fare magari visualizzazione non lo fa vedere. Però se un'altro può fare un'operazione perché c'è quell'altro che deve fare deve sloggare l'altro utente e logarsi questo utente. Quindi diciamo che.

_[immagine]_**  
Spreafico Paolo** 1:38:12  
Quando se un'altro può magari visualizzazione può far vedere, però se un'altro può fare un'operazione può farlo perché c'è quell'altro che deve fare, deve sloggare l'altro utente e logarsi consulente, quindi diciamo che.

_[immagine]_**  
Emanuele Merlo** 1:38:26  
Ci sarà su prod, su punizione, su immagini di punizione. Sarà questo post Trade, no? Quindi tu sai che sei logato con la macchina e tu sai che è saltato a quell'ora quel quella macchina. Adesso prendo la lavatrice due o la quattro o la 5. Non so, non so cosa mi vuole insegnare Paolo.

_[immagine]_**  
Spreafico Paolo** 1:38:27  
Ci sarà su prod, su produzione, ci sarà questo no? E quindi tu sai che sei drogato con la macchina e tu sai che è saltato a quell'ora quel adesso io prendo la lavatrice due o la quattro o la 5. Non so se non so dove vuoi andare Paolo.

_[immagine]_**  
Emanuele Merlo** 1:38:46  
Il questo qui per cambiare il centro del.

_[immagine]_**  
Spreafico Paolo** 1:38:46  
E questo qui per cambiare il centro del no m'ha m'ha chiesto di selezionare il nodo.

_[immagine]_**  
Emanuele Merlo** 1:38:58  
Sì, quando io dato lo start sì.

_[immagine]_**  
Spreafico Paolo** 1:38:58  
Quando io ho dato lo start?  
Mi dice con lo start.  
Poi mi dice, su che nodo vuoi andare?

_[immagine]_**  
Emanuele Merlo** 1:39:09  
Su che modo vuoi andare? Perché sono quattro macchine, va bene, OK.

_[immagine]_**  
Spreafico Paolo** 1:39:12  
Perché son quattro macchine? Va beh, non ti preoccupare, prendo la lavatrice due.

_[immagine]_**  
Emanuele Merlo** 1:39:22  
OK, quindi qui devi fare l'accesso al vedi che lui mi dice Guarda che mi sta entrando a dichiarare.

_[immagine]_**  
Spreafico Paolo** 1:39:24  
Vedi che lui mi dice, Guarda che tu stai entrando a dichiarare.

_[immagine]_**  
Emanuele Merlo** 1:39:29  
Ma tu non puoi lavorare su questa macchina perché non sei nel gruppo.

_[immagine]_**  
Spreafico Paolo** 1:39:29  
Ma tu non puoi lavorare su questa macchina perché non sei nel gruppo.

_[immagine]_**  
Emanuele Merlo** 1:39:36  
Sky quindi qui non c'è.

_[immagine]_**  
Spreafico Paolo** 1:39:39  
Quindi chi è sante?

_[immagine]_**  
Emanuele Merlo** 1:39:51  
Allora lo possiamo fare da.

_[immagine]_**  
Spreafico Paolo** 1:39:51  
Lo possiamo fare da.

_[immagine]_**  
Emanuele Merlo** 1:40:01  
Rutto un attimo di défaillance.

_[immagine]_**  
Spreafico Paolo** 1:40:08  
Vediamo se ci sono, se compaio.

_[immagine]_**  
Emanuele Merlo** 1:40:15  
Grazie.

_[immagine]_**  
Spreafico Paolo** 1:40:15  
Euro.  
Sì.

_[immagine]_**  
Emanuele Merlo** 1:40:21  
Per il pollo perso.

_[immagine]_**  
Spreafico Paolo** 1:40:21  
Mettiamo dentro Paolo Pesso.  
No, queste qua sono attività del.

_[immagine]_**  
Emanuele Merlo** 1:40:26  
No, queste qua sono attività del OK.

_[immagine]_**  
Spreafico Paolo** 1:40:29  
Degli operatori di linea, noi non dobbiamo fare questa roba qua.  
Sì, però non riuscivo a loggarmi.

_[immagine]_**  
Emanuele Merlo** 1:40:40  
Ok.

_[immagine]_**  
Spreafico Paolo** 1:40:40  
OK.

_[immagine]_**  
Emanuele Merlo** 1:40:41  
Io adesso sono qui, OK, vedete che questa quantità e diciamo questo numero di 10 è avanzato, no?

_[immagine]_**  
Spreafico Paolo** 1:40:41  
Io adesso sono qui.  
Da questo numero 10 è avanzato, no?

_[immagine]_**  
Emanuele Merlo** 1:40:50  
Ok, prima era diciamo l'icona è cambiata da verde, è diventata diciamo quella mezza, quella mezza luna in Alto verde è diventata non in obliquo. Ok, quindi è un ordine, diciamo in progress, vedete, in startup.

_[immagine]_**  
Spreafico Paolo** 1:40:51  
Cioè prima era, diciamo, l'icona è cambiata da verde, è diventata, diciamo quella mezza, quella mezza luna in alto verde è diventata blu in blu. OK, prendiamo un ordine, diciamo.  
In progress, quindi dei startup e la quantità è passata, diciamo alle quantità, quelle di Leclerc, no, di quelle che sono state che sono pronte, se noi ad esempio.

_[immagine]_**  
Emanuele Merlo** 1:41:08  
E la quantità è passata, diciamo alle quantità, quelle di declare non di quelle che sono state che sono pronte. Se noi ad esempio ne prendevamo 5 avremmo.

_[immagine]_**  
Spreafico Paolo** 1:41:21  
Ne prendevamo 5, avremmo avuto 550 no, 5 ancora da saltare, 10 prese in carico. E l'ultimo numero quale sarà?

_[immagine]_**  
Emanuele Merlo** 1:41:23  
550 no, 5 ancora da saltare, 10 prese in campo e l'ultimo numero quale sarà?  
L'ultimo, quello che adesso è zero, quelli quelli buoni andati in uscita, OK, quindi qui adesso vedete?

_[immagine]_**  
Spreafico Paolo** 1:41:32  
L'ultimo, quello che adesso è zero, quelli in uscita, OK, quindi qui adesso.

_[immagine]_**  
Emanuele Merlo** 1:41:47  
Perché scusa il non so, perché no, perché con Twitter dovrei lasciare scusa?

_[immagine]_**  
Spreafico Paolo** 1:41:50  
Giusto?

_[immagine]_**  
Emanuele Merlo** 1:41:57  
È quel baco che mi dicevi, no, non ha fatto.

_[immagine]_**  
Spreafico Paolo** 1:41:57  
È quel dato che mi dicevi?  
No, non ha fatto.  
Per cortesia esco.

_[immagine]_**  
Emanuele Merlo** 1:42:05  
Magari non è.  
Sì.  
Ma attenzione, non abbiamo ancora sparato una mazza, ragazzi.

_[immagine]_**  
Spreafico Paolo** 1:42:20  
No, attenzione, non abbiamo ancora sparato una mazza, ragazzi.

_[immagine]_**  
Emanuele Merlo** 1:42:26  
Allora qui c'è un problema tecnico che mi ha segnalato anche Paolo, cioè tutte quelle cose che diciamo un po caglioche, il blocco funzionale che sono davvero obbligatori adesso.

_[immagine]_**  
Spreafico Paolo** 1:42:26  
Allora?  
Cioè tutte delle cose che diciamo un po' cagliocche del blocco funzionale che sono davvero obbligatori adesso no? Considera che io sono admin.

_[immagine]_**  
Emanuele Merlo** 1:42:40  
Ma funzionavano fino tutte tutte le regole.

_[immagine]_**  
Spreafico Paolo** 1:42:44  
Quindi tutte tutte le regole a me decadono.  
Questa icona qua dovrebbe essere arancione.

_[immagine]_**  
Emanuele Merlo** 1:42:58  
La diciamo una specie di lampeggiante e i pulsanti devono essere disabilitati no di completi in modo che chiaramente l'operatore vede la prima cosa che devo fare sono l'inserimento dei dati di qualità una volta che li ho inseriti poi.

_[immagine]_**  
Spreafico Paolo** 1:42:58  
Diciamo una specie di lampeggiante e i pulsanti devono essere disabilitati in modo che chiaramente l'operatore vede la prima cosa che devo fare sono l'inserimento dei dati di qualità una volta che li ho inseriti poi.

_[immagine]_**  
Emanuele Merlo** 1:43:13  
Può fare le fasi successive, quindi vediamoli brevemente. Qui appunto abbiamo un feedback no. Quindi questo triangolino dice che non vanno bene? No, cioè che sono da inserire.

_[immagine]_**  
Spreafico Paolo** 1:43:14  
Può fare le fasi successive, quindi vediamo brevemente qui appunto abbiamo il feedback no? Quindi questo triangolino dice che non vanno bene, no? Cioè che sono da inserire.

_[immagine]_**  
Emanuele Merlo** 1:43:28  
Allora ragazzi, qui avete OK, non OK.

_[immagine]_**  
Spreafico Paolo** 1:43:29  
Allora ragazzi, qui avete OK o non OK?

_[immagine]_**  
Emanuele Merlo** 1:43:35  
In ogni singolo campo potete inserire una nota.

_[immagine]_**  
Spreafico Paolo** 1:43:35  
In ogni singolo campo potete inserire una nota.

_[immagine]_**  
Emanuele Merlo** 1:43:40  
Se ci sono controlli a tutti gli effetti che possono vedere questi sono i controlli che fa prima di produrre.

_[immagine]_**  
Spreafico Paolo** 1:43:41  
Perché ci sono controlli a tutti gli effetti che possono richiedere la nota, leggi il barcode, che senso dopo?  
Fine produzione aspetta questo, tu puoi, tu puoi produrre, non puoi dichiarare no, questo, questi sono i controlli che fai sul. Quindi il primo pezzo che controlli è quello che tiri sul.

_[immagine]_**  
Emanuele Merlo** 1:44:00  
Non puoi dichiarare no, questi sono i controlli che fai su per il primo pezzo controlli e se io ho.

_[immagine]_**  
Spreafico Paolo** 1:44:11  
E se io ho un controllo, allora adesso l'evoluzione di questo è mettere i controlli d'avvio, li abbiamo fatti i controlli in frequenza e i controlli in chiusura.

_[immagine]_**  
Emanuele Merlo** 1:44:12  
Mi puoi fare quante volte mi puoi fare quante volte il controllo finale allora adesso la l'evoluzione di questo è mettere i controlli d'avvio e controlli in frequenza e controlli.  
Perciò è stato richiesto, non è stata ancora diventata la funzionalità. Sono i controlli in frequenza, quindi sulla chiusura non è ongoing, dovremmo avere per il Live. Sto aspettando la CR che mi venga proprio.

_[immagine]_**  
Spreafico Paolo** 1:44:29  
Perché sono già state richieste, non è stata ancora implementata la funzionalità sono i controlli in frequenza, quindi sulla chiusura non è ongoing, la dovremmo avere per il Live. Sto aspettando la CR che mi venga portata in produzione.

_[immagine]_**  
Emanuele Merlo** 1:44:43  
È previsto? Sì, però il concetto è sempre quello.

_[immagine]_**  
Spreafico Paolo** 1:44:44  
Questo è stato è previsto? Sì, però il concetto è sempre quello.

_[immagine]_**  
Emanuele Merlo** 1:44:49  
O anche o anche a quantità raggiunta la modalità, cioè dici quando sono al centesimo pezzo, allora fammi un all'ultimo pezzo, all'ultimo pezzo dichiarato o alla chiusura dell'ordine.

_[immagine]_**  
Spreafico Paolo** 1:44:49  
Anche a quantità raggiunta l'altra modalità, cioè dici quando sono al centesimo pezzo, allora fammi un o all'ultimo pezzo, all'ultimo pezzo dichiarato compare o alla chiusura dell'ordine.

_[immagine]_**  
Emanuele Merlo** 1:45:05  
OK, non lo sfrutterei tantissimo. Se sei riuscito a dilogarti per se vuoi Paolo prendiamo noi il sì, prendiamo anche tra le slide.

_[immagine]_**  
Spreafico Paolo** 1:45:07  
Per un intermedio non lo sfrutteremo tantissimo, sarà più quello a fine produzione come volete.  
E possiamo cominciare anche tra le slash allora? Quindi siamo andati lì e inseriamo adesso inserisci magari tutti OK diciamo facciamo l'hot pass così e inseriamo questi questi dati OK?

_[immagine]_**  
Emanuele Merlo** 1:45:21  
Allora quindi siamo arrivati lì e inseriamo adesso inserisci magari tutti OK, facciamo e inseriamo questi questi dati OK?  
E diciamo che così a questa fase qua diciamo l'inserimento dati di qualità che è obbligatoria, viene eseguita e diciamo il primo pezzettino diciamo della vita no nella vita dell'operatore.

_[immagine]_**  
Spreafico Paolo** 1:45:36  
E diciamo che così da questa fase qua diciamo di segmento della qualità che è obbligatoria, viene eseguita e diciamo il primo pezzettino diciamo della vita non si è immedesimati nella vita dell'operatore.

_[immagine]_**  
Emanuele Merlo** 1:45:52  
L'avete fatto magari riguarda qualità, quindi dichiarazione prezzi presi in carico e uno ad uno riferimento dei controlli di qualità che sono, abbiamo detto, i controlli di inizio ciclo di.

_[immagine]_**  
Spreafico Paolo** 1:45:52  
L'avete fatto? OK che riguarda qualità, quindi dichiarazione prezzi presi in carico e uno ad uno inserimento dei dei controlli di qualità che sono, abbiamo detto, i controlli di inizio ciclo di.

_[immagine]_**  
Emanuele Merlo** 1:46:07  
Di presa in campo.

_[immagine]_**  
Spreafico Paolo** 1:46:07  
E poi sei comico.

_[immagine]_**  
Emanuele Merlo** 1:46:09  
Quindi.

_[immagine]_**  
Spreafico Paolo** 1:46:10  
Quindi.

_[immagine]_**  
Emanuele Merlo** 1:46:13  
Inserisci un secondo clicca qua.

_[immagine]_**  
Spreafico Paolo** 1:46:14  
Inserisci nel secondo clicca K.

_[immagine]_**  
Emanuele Merlo** 1:46:18  
E questa visualizzazione minuscola.  
Sono già tutti OK, li vediamo.

_[immagine]_**  
Spreafico Paolo** 1:46:28  
Sì, allora l'ha fatto Paolo velocissimo.

_[immagine]_**  
Emanuele Merlo** 1:46:35  
E a me sta in produzione bla bla bla OK?

_[immagine]_**  
Spreafico Paolo** 1:46:36  
Scherini sta in condizione bla bla bla OK.

_[immagine]_**  
Emanuele Merlo** 1:46:40  
OK, questa qua è la fase diciamo.

_[immagine]_**  
Spreafico Paolo** 1:46:40  
OK, questa qua è la fase diciamo.

_[immagine]_**  
Emanuele Merlo** 1:46:44  
Quindi c'abbiamo l'aeroplanino per inviare. Volendo possono essere reinseriti e produrranno un'altra un'altra ispezione. OK, possono essere reinseriti in qualunque momento.

_[immagine]_**  
Spreafico Paolo** 1:46:44  
La cosa sbagliata, OK, sono stati inseriti, volendo possono essere reinseriti e produrranno un'altra, possono essere reinseriti in qualunque momento del.

_[immagine]_**  
Emanuele Merlo** 1:47:01  
Il l'ordine diciamo startup finché non lo completi puoi inserire valori di qualità, quindi questa fase qua è fatta, adesso vediamo.

_[immagine]_**  
Spreafico Paolo** 1:47:02  
Che l'ordine diciamo startup no finché non lo completi puoi inserire valori di qualità quindi questa fase qua è fatta cioè quindi controlli di avvio produzione li posso fare alla fine?

_[immagine]_**  
Emanuele Merlo** 1:47:16  
E quindi controlli.

_[immagine]_**  
Spreafico Paolo** 1:47:18  
Tu puoi produrre fintanto che tu non dichiari, non se non mi hai inserito i controlli, non lo fai.  
È come oggi, è come oggi, ci sono due cervelli diversi, quello della linea che ti permette di proteggere e quello per dichiarare.

_[immagine]_**  
Emanuele Merlo** 1:47:31  
Non c'abbiamo un container lì, scusami ragazzi, adesso abbiamo un problema, noi vogliamo dichiarare, ma che cosa stiamo andando a consumare?

_[immagine]_**  
Spreafico Paolo** 1:47:34  
Container.  
Ragazzi, adesso abbiamo un problema, noi vogliamo dichiarare, ma che cosa stiamo andando a consumare?

_[immagine]_**  
Emanuele Merlo** 1:47:49  
Se no lo creiamo, OK, allora.

_[immagine]_**  
Spreafico Paolo** 1:47:52  
Allora?

_[immagine]_**  
Emanuele Merlo** 1:47:54  
Quindi il sistema com'è oggi mi dice Dimmi che cosa vuoi consumare per procurare il materiale.

_[immagine]_**  
Spreafico Paolo** 1:47:54  
Quindi il sistema come oggi mi dice, Dimmi che cosa vuoi consumare per produrre questa parte, sotto il \*\*\*\*\*\* di questo bellissimo sistema c'è una bomba.  
Per cui ti dice, guarda che per produrre questo oggetto devo fare.  
XYZ, devi darmi questi componenti.

_[immagine]_**  
Emanuele Merlo** 1:48:20  
C'è scritto, Fammi vedere la.  
E poi ho sbagliato, la Bot component non è VSH ma SSD qualcosa. Quindi vediamo la Bot SM no? Vedete allora la trasformazione qual è in questo caso no?

_[immagine]_**  
Spreafico Paolo** 1:48:36  
Quindi vediamo la FSM, non vedete allora la trasformazione qual è in questo caso? No, mi chiede un materiale di ingresso che è sempre 37 come quello di uscita. No, quello di uscita.

_[immagine]_**  
Emanuele Merlo** 1:48:44  
Mi chiede un materiale di ingresso che è sempre 37 come quello di uscita? No, quello di uscita è qua in alto 37 VSHE prende un materiale, gli servono 10 pezzi da lavare giustamente.

_[immagine]_**  
Spreafico Paolo** 1:48:51  
E qua in alto 37 washi VSHE prendo materiali servono 10 pezzi da lavare giustamente pezzi da 10 da lavare. Dove sono messi? No, sono messi.

_[immagine]_**  
Emanuele Merlo** 1:49:00  
Questi preparzi da 10 da lavare dove sono messi? No, sono messi nel buffer.

_[immagine]_**  
Spreafico Paolo** 1:49:06  
Il buffer.

_[immagine]_**  
Emanuele Merlo** 1:49:08  
Che è della macchina di Washington? No. Del banco di Washington. C'è un buffer di ingresso. E questi qui sono messi da chi? Sono messi dal dal processo precedente? No.

_[immagine]_**  
Spreafico Paolo** 1:49:09  
Che è della macchina di Washington? No. Del banco di Washington no. C'è un buffer d'ingresso. E questi qui sono messi da chi? Sono messi dal dal processo precedente, no.

_[immagine]_**  
Emanuele Merlo** 1:49:25  
Sempre macchina ragazzi, sempre macchina è quello che devo.

_[immagine]_**  
Spreafico Paolo** 1:49:25  
È il pre macchina ragazzi, quindi il pre macchina è quello che devo.  
Avere lì.

_[immagine]_**  
Emanuele Merlo** 1:49:37  
Emanuele, scusami, intanto che tu fai apparire il buffer, due cose.

_[immagine]_**  
Spreafico Paolo** 1:49:37  
Emanuele, scusami, intanto che tu fai apparire il buffer te te lo intrattengo io un attimo, quindi questo vuol dire due cose.  
Il materiale può essere dichiarato se è presente in bordo macchina, non esiste più che passa il Michele o qualcuno col materiale sottobraccio, lo porta a bordo macchina e gli dice.

_[immagine]_**  
Emanuele Merlo** 1:49:53  
Il materiale non si occupa.

_[immagine]_**  
Spreafico Paolo** 1:50:03  
Usa questo CD non esiste più.

_[immagine]_**  
Emanuele Merlo** 1:50:04  
Non esiste più.  
Il materiale deve arrivare e deve essere.

_[immagine]_**  
Spreafico Paolo** 1:50:06  
Il materiale deve arrivare e deve essere sentito nelle varie step, quindi che vada sul muletto o sulla GB di turno, che venga trasferito in pre macchina e quando è arrivato in pre macchina c'è una chiusura di un task.  
E dice al MES, guarda che ti ho portato questo materiale.

_[immagine]_**  
Emanuele Merlo** 1:50:26  
Sto andando a vedere cosa c'entra.

_[immagine]_**  
Spreafico Paolo** 1:50:28  
Lo fa la logistica così General generica son dei task automatici e tutto il processo di logistica che è un attimino fuori no vai tranquillo nel mentre introduco altri due concetti quindi.  
E nascosta.

_[immagine]_**  
Emanuele Merlo** 1:50:43  
Una diciamo nella basic.  
Per dei container che sono stiamo cercando super macchina che ha un certo nome, i container del materiale di ingresso, quindi MSD, il CD del materiale deve essere presente.

_[immagine]_**  
Spreafico Paolo** 1:50:49  
Dei container che sono stiamo cercando su premacchina che ha un certo nome, i container del materiale di ingresso, quindi LSD, il CD del materiale deve essere presente in quello premacchina.

_[immagine]_**  
Emanuele Merlo** 1:51:05  
Ovviamente se non mi dichiarano che cosa stanno crescendo non posso dichiararli.

_[immagine]_**  
Spreafico Paolo** 1:51:05  
Ovviamente se non mi dichiarano che cosa stanno consumando non possono dichiarare quello in uscita.  
Prima, se vi ricordate, vi ho vi ho parlato di.  
CDI è di propagazione del batch, questo mi serve per legare, per farmi tutta la tracciabilità.

_[immagine]_**  
Emanuele Merlo** 1:51:28  
Qualcuno mi disse che aveva dei problemi tra presenza fisica della parte e dichiarazioni.

_[immagine]_**  
Spreafico Paolo** 1:51:28  
Altro piccolo concetto.  
Qualcuno mi disse che aveva dei problemi tra.  
Presenza fisica della parte e dichiarazione su avanzamento di fabbrica.

_[immagine]_**  
Emanuele Merlo** 1:51:44  
Dove tendenzialmente potevano continuare con la macchina stesso CD.

_[immagine]_**  
Spreafico Paolo** 1:51:44  
Dove tendenzialmente potevano continuare a pistolettare lo stesso CDIEAX.  
Se ne fregava e digeriva tutto.

_[immagine]_**  
Emanuele Merlo** 1:51:52  
Allora me la devo prendere, ogni volta che faccio un complete e dichiaro una produzione, il sistema va.

_[immagine]_**  
Spreafico Paolo** 1:51:55  
Qui, con questo trasferimento di materiale, il sistema sa esattamente quanti pezzi che CDI ha presente a bordo macchina, ogni volta che faccio il complete e dichiaro una produzione, il sistema va ad erodere.

_[immagine]_**  
Emanuele Merlo** 1:52:10  
Ad erodere il quantitativo di quello specifico che gli ho dichiarato.

_[immagine]_**  
Spreafico Paolo** 1:52:11  
Il quantitativo di quello specifico CD che gli ho dichiarato.

_[immagine]_**  
Emanuele Merlo** 1:52:17  
Facile questo casino con la visualizzazione web, il che vuol dire i pezzi che appaiono dal nulla perché ho trovato dei pezzi di scarto aggiungili non esiste più perché contabilmente se io ho un CD da 10.

_[immagine]_**  
Spreafico Paolo** 1:52:18  
Facile questo, giusto?  
E che vuol dire?  
I pezzi che appaiono dal nulla del tipo ho trovato due pezzi di scarto to aggiungili non esiste più perché contabilmente se io ho un CD da 10.

_[immagine]_**  
Emanuele Merlo** 1:52:35  
E tu ne vuoi dichiarare 12, il sistema ti dice, Dimmi dove sei andato a prendere.

_[immagine]_**  
Spreafico Paolo** 1:52:35  
E tu ne vuoi dichiarare 12, il sistema ti dice, Dimmi dove sei andato a prendere.

_[immagine]_**  
Emanuele Merlo** 1:52:42  
Quindi devo far portare il nuovo CD con quei due pezzi?

_[immagine]_**  
Spreafico Paolo** 1:52:42  
Quindi rettifica e devo far portare il nuovo CDI con quei due pezzi?

_[immagine]_**  
Emanuele Merlo** 1:52:49  
8 quando chiudo l'ordine.

_[immagine]_**  
Spreafico Paolo** 1:52:49  
Ok, quando chiudo l'ordine.

_[immagine]_**  
Emanuele Merlo** 1:52:53  
Il materiale a bordo linea viene riportato magazzino, quindi a bordo linea sparisce tutto quello che c'è.

_[immagine]_**  
Spreafico Paolo** 1:52:59  
Sì.

_[immagine]_**  
Emanuele Merlo** 1:53:00  
C'è un ordine per cui si dice, prendi questo materiale, me lo porti a magazzino, il res, il res di oggi tendenzialmente si pulisce.

_[immagine]_**  
Spreafico Paolo** 1:53:00  
C'è un ordine per cui si dice, prendi questo materiale, me lo porti a magazzino, quindi il reso di oggi, quindi tendenzialmente si pulisce.

_[immagine]_**  
Emanuele Merlo** 1:53:11  
La collabora Denise m'ha spoilerato.

_[immagine]_**  
Spreafico Paolo** 1:53:11  
Sempre la buona Denise m'ha spoilerato.

_[immagine]_**  
Emanuele Merlo** 1:53:15  
Che avete due tipi di tracciabilità e la tracciabilità può essere hard. Sto cercando aspetta, non so se c'è assolutamente sicuro che ci sia.

_[immagine]_**  
Spreafico Paolo** 1:53:16  
Che avete due tipi di tracciabilità e la tracciabilità può essere hard.  
Oppure soft. Che differenza c'è? Tracciabilità hard. Voglio la conta fisica contabile sottoscritta che se uso 10 pezzi consumo 10 pezzi.

_[immagine]_**  
Emanuele Merlo** 1:53:33  
Se uso 10 pezzi consumo 10 pezzi.  
Aspetta un attimo.

_[immagine]_**  
Spreafico Paolo** 1:53:39  
Ivi compreso se dichiaro uno scarto i pezzi disponibili cosa diventano -1 9 pezzi. Quindi al massimo posso dichiarare 9 pezzi scarto non ne posso più dichiarare 10.  
La seconda esempio, viti, esempi a guarnizioni dove ho le tramoggine.

_[immagine]_**  
Emanuele Merlo** 1:53:55  
In quel caso lì faccio una tracciabilità sopra.

_[immagine]_**  
Spreafico Paolo** 1:53:57  
Dove fondamentalmente non riesco ad avere una cassetta unica, in quel caso lì faccio una tracciabilità soft, voglio sentire il movimento che tu mi hai portato alla cassetta, me l'hai caricata nel pre macchina.

_[immagine]_**  
Emanuele Merlo** 1:54:10  
Aspetta un attimo, non son sicuro di.

_[immagine]_**  
Spreafico Paolo** 1:54:12  
Dopo che tu me la prendi dal CD uno, dal CD due, dal CD tre, si va in logica FIFO come oggi, cosa vuol dire sparo il primo?  
Dichiaro ipotizzato sempre da delle nostre 10 pezzi, me ne servono 15. Il sistema dice è una tracciabilità soft questo componente ne hai 10, vedo che nel tuo pre macchina ne hai ancora 5, vuoi che te li.

_[immagine]_**  
Emanuele Merlo** 1:54:27  
Non so cosa stiamo facendo Annalisa.

_[immagine]_**  
Spreafico Paolo** 1:54:36  
Tolga da lì ed è un ragionamento che si fa lui, perché fisicamente non riuscite a distinguerli.

_[immagine]_**  
Emanuele Merlo** 1:54:43  
Ce l'ha il materiale?

_[immagine]_**  
Spreafico Paolo** 1:54:47  
Per tutto Ops tutte tutto il materiale che si muove come ingombranti, pastiglie, pinze.  
Dopo cos'è che avevano definito?

_[immagine]_**  
Emanuele Merlo** 1:55:01  
Dimmi mandagli uno screenshot.

_[immagine]_**  
Spreafico Paolo** 1:55:03  
Il pistone, cioè tutta la roba ingombrante per cui.

_[immagine]_**  
Emanuele Merlo** 1:55:09  
Però non è quella giusta.

_[immagine]_**  
Spreafico Paolo** 1:55:09  
Sama, qual è meglio che no te dico cosa sia?  
Secondo Denise, quindi, a seconda del tipo di clusterizzazione che noi andiamo a dire, abbiamo dei comportamenti diversi a bordo linea.

_[immagine]_**  
Emanuele Merlo** 1:55:14  
E solo questo ci manca di materiale. Sì, 100 pets. Se lo sa, se non mandagli anche la screenshot che ho mandato ieri sera questa no, nelle mail ho messo la screenshot.

_[immagine]_**  
Spreafico Paolo** 1:55:23  
A oggi la regola che è stata applicata è tutta la roba ingombrante con simbolo di sicurezza è stata battezzata in modalità hard.  
Le guarnizioni, le viti sono in modalità medio soft. Cosa vuol dire che voglio sentire batch per batch?

_[immagine]_**  
Emanuele Merlo** 1:55:33  
Mi raccomando da fare.

_[immagine]_**  
Spreafico Paolo** 1:55:42  
Viene portato dove viene allocata i grassi, gli oli e via dicendo, che tracciabilità abbiamo?

_[immagine]_**  
Emanuele Merlo** 1:55:49  
Non lo sa usare il test clash?

_[immagine]_**  
Spreafico Paolo** 1:55:53  
No.  
Consumo da magazzino flow stock, tracciabilità nera flow stock quindi a tutti gli effetti ce l'ho da qualche.

_[immagine]_**  
Emanuele Merlo** 1:55:59  
C'è una pausa.

_[immagine]_**  
Spreafico Paolo** 1:56:03  
Ce l'ho da qualche parte e vado quel buffer.

_[immagine]_**  
Emanuele Merlo** 1:56:09  
Possiamo fare una pausa, probabilmente mentre noi creiamo quel quel coso lì, perché non abbiamo accesso dal solito, OK? Quindi avete capito? Stiamo mettendo, stiamo mettendo i pezzi che adesso ce ne sono pochi.

_[immagine]_**  
Spreafico Paolo** 1:56:11  
E un master hard hard vuol dire che devo montare 10 pinze io devo aver sparato.  
In più CD che arrivi in una somma di 10 per le pastiglie, per le pinze, per pochi componenti.

_[immagine]_**  
Emanuele Merlo** 1:56:31  
E non possiamo fare sì, però possiamo farlo anche direttamente.

_[immagine]_**  
Spreafico Paolo** 1:56:38  
Il la via di mezzo diciamo è basata sullo stesso vincolo ma estendendo il perimetro al pre macchina, quindi io devo sparare CD che comprendono anche i centri di lavoro del pre macchina.

_[immagine]_**  
Emanuele Merlo** 1:56:47  
Perché te lo fa fare? Non te lo fa fare. Aspetta un attimo.  
No, vedi che questo è il mappello, ci devi scrivere turno e poi cambiare e andare. No, non devi fare iniziare, se non tu cancella.

_[immagine]_**  
Spreafico Paolo** 1:56:56  
Spiega meglio la tracciabilità media, cioè tu devi considerare anche il pre macchina, allora anche per la tracciabilità media tu devi sentire i movimenti, allora i movimenti adesso sono tracciati, non esiste più il movimento da Ruggiera.  
Apre macchina con una sparata prelievo da rulliera.

_[immagine]_**  
Emanuele Merlo** 1:57:14  
Allora materiale APP bimbo no APP bimbo devi fare OK qua stock OK è quello aspetta che.

_[immagine]_**  
Spreafico Paolo** 1:57:18  
I movimenti saranno il materiale in rulliera dichiaro che prenoto quel materiale dalla dalla rulliera dichiaro che è salito sul trenino numero 4, il trenino mi dichiara che ha consegnato quella cosa lì alla linea monoblocco 7.

_[immagine]_**  
Emanuele Merlo** 1:57:34  
Sì, sto.

_[immagine]_**  
Spreafico Paolo** 1:57:35  
Questi sono i movimenti per il quale il sistema traccia di avanzamento è, cioè non devo avere una quantità uno ad uno esattamente come la tracciabilità hard, ma devo aver fatto uscire il materiale dalla ruviera e quindi fatto una missione per.

_[immagine]_**  
Emanuele Merlo** 1:57:47  
Su test Definition, basta, non ce ne frega un \*\*\*\*\*.

_[immagine]_**  
Spreafico Paolo** 1:57:50  
Per asservire quella linea e quindi il perimetro, se io devo fare una tracciabilità di qualche tipo non è più sulla quantità esatta ma sulla quantità che in quel momento era presente nel premacchine, quindi dopo Rubiera prego.

_[immagine]_**  
Emanuele Merlo** 1:58:03  
Il materiale ci serve solo quello.

_[immagine]_**  
Spreafico Paolo** 1:58:05  
No, stavo pensando, ma comunque la quantità deve essere sempre uno a uno, la quantità consumata.

_[immagine]_**  
Emanuele Merlo** 1:58:12  
Questo è un sistema che in realtà va a considerare.

_[immagine]_**  
Spreafico Paolo** 1:58:15  
Se mi arrivano due cassette e per un qualsiasi motivo io non vado AA fare la logica FIFO, questo è un sistema che in realtà va a considerare di default la logica FIFO, quindi se io la cassetta me la dimentico lì per un mese in pre macchina.

_[immagine]_**  
Emanuele Merlo** 1:58:31  
La macchina risulterà una cassetta, quella che è stata consumata da 10 € e mezzo a sparare i componenti.

_[immagine]_**  
Spreafico Paolo** 1:58:32  
Risulterà una cassetta però che è stata consumata da all'inizio se io ci impiego tre ore e mezzo a sparare i componenti.  
Area mixer è finita, allora devo andare a casa, metto in modalità stand by, ritorna la persona, dopo arriva.

_[immagine]_**  
Emanuele Merlo** 1:58:53  
E finita.

_[immagine]_**  
Spreafico Paolo** 1:58:56  
E da lì sparare tutto il materiale e come fa a spararlo? Sparare il materiale cosa intendi? Perché nel caso del mixer?  
Tu hai lo zanelli che ti dichiara i consumi.  
Non c'è più, spari solo nel mixer e il mixer comunica d'avanzamento di fabbrica, cosa cosa hai in pancia?

_[immagine]_**  
Emanuele Merlo** 1:59:16  
E non vedo la barra.

_[immagine]_**  
Spreafico Paolo** 1:59:28  
Dovrebbe stando alle ultime.

_[immagine]_**  
Emanuele Merlo** 1:59:31  
Quindi resterebbe in memoria, non c'è più bisogno di riparare quando io riapro nuovamente l'ordine niente. Dov'è finito il tester tu che non lo vedo più sta cosa del.

_[immagine]_**  
Spreafico Paolo** 1:59:31  
Quindi resterebbe in memoria. Non c'è più bisogno di riparare quando io riapro nuovamente l'ordine. E perché allora il mixer è un pochino diverso? Perché non dichiari il mixer? È lui che manda il segnale al MES. Guarda che sto scaricando e sto.  
Consumando questa roba qua, quindi è il processo inverso, cosa va a consumare se glielo manda lo zanelli?

_[immagine]_**  
Emanuele Merlo** 1:59:51  
Cosa va a consumare? Non è che ha dato un'altro schermo, non so.  
Se mi spieghi, invece.

_[immagine]_**  
Spreafico Paolo** 1:59:57  
Sì, invece adesso te la mesco, andiamo.  
Mi da hard e io sparo il CD che devo consumare il CD esatto e controllo anche la quantità del CD soft soft e io porto una serie di cassette in macchina, sparo la prima, sparo la seconda, la terza me la dimentico.

_[immagine]_**  
Emanuele Merlo** 2:00:06  
No, aspetta, son tre macchine, una dentro l'altra.  
C'ho questa barra che non mi fa vedere, non mi fa vedere la barra di questa macchina qua.

_[immagine]_**  
Spreafico Paolo** 2:00:22  
Prendo e il sistema mi dice, guarda che ne hai usate due e me le hai dichiarate la terza, ti va bene se vado a prenderti quelli che mi hai portato senza doverla sparare?  
Cioè quella hardware io sparo un CDE posso consumare solo quel CDE con la Medium soft io sparo quel CD posso consumare quel CDE in più se qualcosa bordo macchina dentro senza.

_[immagine]_**  
Emanuele Merlo** 2:00:31  
Puoi fare shift Tab? No, perché mi prende quello della macchina così ti apre un'altra istanza, ma se poi lo perdi.  
Non è questo.  
No, mi sto picchiando tra le cinesi delle macchine.

_[immagine]_**  
Spreafico Paolo** 2:00:51  
Cinesi.

_[immagine]_**  
Emanuele Merlo** 2:01:12  
Fammi vedere.  
E vedo solo questo.  
No.  
Dove che ospita finito adesso?

_[immagine]_**  
Spreafico Paolo** 2:01:52  
Poi non switch, ti dico i dati direttamente, poi di non.  
O copre, ma vorrei vedere una TAP.  
Avete un account con.  
A tutto un poco.  
Marco.  
Tai, guarda se la chiamata.  
Spremi una chiave perché è tornata a Mantovani, devi andare nella.  
E proprio.  
Sì, stavo cercando di capire la tracciabilità software.  
A parte che basti solo quel materiale lì, va bene, adesso ce l'abbiamo. C'è solo una pin, c'è una cosa da lavare, no?  
Qui c'è un solo, c'è la bomba più semplice del mondo, invece quando fai la Sandy hai magari non so 20 pezzi componenti o tutti i componenti poi da.  
Vediamo se funziona.  
Ma come fa? Non lo sapevo io.  
Però.  
Ero.  
Però è anche bello perché.  
Se è così, però poi squillo se ti chiamano.  
Nessuno si è girato, suona, me lo giri, figata. Non so, l'avevo sentito dire, ma non l'avevo mai fatto. Ci richiamano verso l'alto, poi lo rigiri.  
Se lo fa chiamata.  
Non so se ti tocca, ma si deve, forse se l'ho bloccata poi.  
Dove sta andando? Se sta un po' più tempo entra nello specifico sulla nostra parte. La linea deve fare sì, però adesso stiamo creando i dati, stiamo creando quelle cose per poi.  
Perché se tu non consumi non puoi fornire allora l'altra volta abbiamo fatto così, però poi siamo andati lunghi, però adesso due ore.  
Dovremmo vedere tutto in modo molto più accurato, però diciamo che adesso bisogna immaginarsi di essere l'operatore che crea questi dati che interagisce con queste configurazioni.  
E quindi si vede, diciamo qui adesso voglio farvi vedere prima l'effetto globale di tutta questa roba e poi nello specifico.  
Tutte le 1000 configurazioni che servono per toccare il settore qua.  
Ma adesso stiamo consumando.  
Consumando questi 10 pezzi no, in teoria, perché 10 pezzi da uno a uno no ai miei pezzi in entrata, ai miei pezzi in uscita, al mio boxing no.  
Poi di questi qua magari c'è qualcuno che ha un difetto, no? Però lì dei puoi creare comunque una un scatto, quindi lo puoi riscattare o.  
Esatto, poi lo stesso per l'output.  
E poi? E poi ci sono tutte le altre fasi che sono complicate. E poi si è.  
Tutti quei cosi vuoti che ci.  
È mia moglie.  
No, perché poi?  
Loro son stati praticamente quarant'anni prima di ritornare quando son tornati praticamente tutte le.  
Adesso ci gira la mail e abbiamo qualche informazione in più però.  
Adesso, proprio due giorni fa, Grillo mi fa, no, ho sentito Ferrari, ma ancora sta storia di pipa, non sanno bene chi deve gestirla, forse adesso qualcuno che la gestisce potrebbero trovare.  
Non so dirtelo.  
Elia.  
Satellitato.  
Adesso carichiamo.  
Facciamo quattro quarantene da due.  
Forse magari OK, quindi scartiamo uno scatto finito, facciamo subito uno scatto dell'ingresso, così vediamo cosa succede. OK, poi andiamo, andiamo, dichiariamo.  
Non conforme, ma si.  
Domanda, adesso su friction la quarantena non funziona per quel problema lì? Esatto, ma c'è un modo per bloccare il pulsante quarantena sulle macchine friction? No, rimani così anche perché è una configurazione.  
A livello di stabilimento, se tolgo il telefono l'antenna tolgo il sito, avevo chiesto anche di capire quali sono i fleghettini.  
Da attivare ad attivare il problema è che è c'è tutto, ad esempio fonderia non c'è l'opzione quarantena, sono proprio disattivata.  
Siente, ti amo.  
A parte.  
Cari, ci son tutti e li diciamo, sai usate?  
Per la pausa, quindi allora eravamo arrivati, no, sempre di essere operatori di perché non si vede direttamente. Però diciamo adesso stiamo creando tutti i dati e il contesto.  
Per poi proseguire, diciamo da quality manager, quindi.  
Qui abbiamo visto, abbiamo preso in carico 10 pezzi. 10 pezzi sono stati eseguiti una volta tutti i controlli obbligatori di inizio di inizio ordine. Adesso bisogna prendere i pezzi di ingresso.  
Ne parte d'ingresso nella macchina e metterli diciamo nell'execution key, cioè nella lavatrice. Per farlo bisogna avere un barcode no e scannerizzare contenitore.  
Dei pezzi in ingresso no, automaticamente il sistema prenderà 10 pezzi da questo qua.  
Si potrebbe.  
Ho fumato 10 pezzi, ha già capito, no? Quali erano?  
OK, ricordatevi che allora fisicamente lui, l'operatore, il contenitore ce l'aveva in macchina. No, perché? Perché c'è stato un movimento, no? Cioè ha fatto comunque ha fatto la chiamata.  
E fisicamente qualcuno gli ha portato lì il contenitore dei pezzi da consumare del processo prima SAP si è aggiornato e ha fatto, diciamo, tutto quello che veniva richiesto.  
Adesso noi abbiamo consumato mando cosa abbiamo fatto? Abbiamo informato che sono andati, diciamo su questo ordine qui no. E abbiamo creato un pezzettino di quella appunto che viene chiamata genealogia, no, quindi genealogia.  
Ad esempio in questo caso forward, se noi partiamo da questo contenitore che abbiamo scannerizzato, noi andremo in là verso poi quello che produce, quello che produceremo no all'indietro, se noi da quello che poi produremo quando?  
Faremo la gente felice quando saremo.  
La dichiarazione, appunto, degli ordini buoni e all'indietro. OK, adesso qua cosa c'è? Qua c'è un cuoricino. Guardate, andiamo un attimo qui.  
E che da qua mi cucina le relatori, no, questo è il fatto rispetto al.  
La.  
Qui è dove si dichiara la quantità di scatto. Questi 10 pezzi in realtà erano tutti buoni? No? Perché abbiamo detto che 2 2.  
No, uno lo ammazziamo di scarto.  
Ditemi voi no cosa? Cioè noi clicchiamo lì e cos'è che dobbiamo fare? Dovrebbe essere abbastanza cos'è che deve fare? Allora vede che uno dei 10 pezzi non andava bene e non può essere lavato perché magari è spaccato, no?  
Quindi è inutile lavarlo. Cosa fa? Clicca lì, Apri. OK prima della quantità.  
Cos'è che mi serve se ho un pezzo cliccato?  
Benissimo, causale, vado a scegliermi il birillo di riferimento.  
Prendine prendine uno quello che ti piace, allora vado a scegliermi la causale che mi serve che mi sembra più idonea.  
Quindi la collego col birillo.  
Quanti pezzi devo andare a dichiarare con questa causale di sotto vedi che hai quantità scartata?  
L'operatore dice a scarto definitivo con una certa causale e una causale sbagliata. I pezzi rimangono rottamati, ma quel OK. E poi c'è una cosa, appunto, abbiamo detto che è un è morto.  
E quindi cos'è che dobbiamo fare dei due?  
Scarto immediato, scarto immediato per primo, l'altro è la quella che si chiama quarantena. In quel caso qua posso stampare un CD? Aspetta, aspetta, adesso vediamo quando schiaccia salva il sistema cosa fa? Ti stampa il CD?  
Quindi fisicamente hai il tuo CDE ti e ti decrementa che cosa la quantità disponibile.  
No, interessa a me. Ti spiego il motivo. Prego, vai perché da quei 10 pezzi tu non l'hai ammazzato, quindi il tuo producibile non sarà +10 9. Difatti vedi, questo è il tuo CD.  
Il tuo nuovo CD con la causale di scarto.  
Alla pressa e ti spiego il motivo perché la pressa basta che mi prenda un'altra piastrina me la rimetto su e poi punto il finale è quello il problema se tu ammazzi la piastrina.  
Tu scarti il componente Piastrina, tu mi scarti fisicamente la piastrina che dopo tu la cambi dentro.  
Ma quella piastrina lì è morta. Sì, però facevo fede io come prima persona. Pensavo che come prima persona potevo fare ugualmente componente 1000 e resca.  
E no, sono 997, a meno che qualcuno ti porti quei tre pezzi aggiuntivi li sparo e allora ritorno a 1000.  
Aspetta tu quando tu.  
Pari lui ti prende in carico tutta la giacenza di quello che hai in mano, quindi se hai rispedite da Beppe gli dite conta grazie.  
Venditore, posso sparare un'altro contenitore e fare la giacenza mente?  
Prego ecco scusa scusami Emanuele, vedete che il colore è cambiato a voi? A noi non ce ne frega niente in questo preciso istante, però adesso lui ti dice.  
È giallo, vuol dire che non ho giacenza di componenti sufficienti per coprire la totalità dell'ordine, quindi se lo vuoi coprire tutto mi devi chiamare altro materiale.  
Ma Emanuele, no, non fare chiamate che quale non.  
Cioè qua si possono ancora di questi 9 questi 9 pezzi OK, uno l'avevamo scattato direttamente.  
E l'altro invece possiamo dire, OK, l'altro lo mettiamo in quarantena, OK, va bene, vai, metti in quarantena.  
Hai due pezzi in quarantena, a questo punto comunque ci saranno 10 pezzi buoni come 10.  
Uno l'ha ammazzato.  
Due li metti in quarantena, quindi 10-3 casa mia fa 7.  
Poi dice.  
Non hai materiale se tu ne richiedi 10.  
Perché qua i prodotti buoni diciamo adesso sono 7 no da che possono essere dichiarati OK?  
Quindi facciamo una dichiarazione di andiamo sul sulla produzione, OK, vai.  
Sì.  
E quindi dichiariamo a questo punto 10 pezzi non li puoi dichiarare, non puoi dichiarare 7 no.  
OK.  
Vai quindi 7 pezzi sono stati completati, OK?  
Quindi questi pezzi sono andati avanti?  
Non potresti più fare perché se tre li hai ammazzati, uno l'hai son sei li hai dichiarati.  
No, perché se tu li dichiari puoi solo va beh, non è un problema. Va bene ragazzi, la linea ha fatto il suo. Entriamo in gioco noi come qualità.  
Quindi pezzo scarto.  
Pezzo morto, pezzo in quarantena, quindi adesso la maschera cambia definitivamente, entriamo nel nostro mondo.  
Quello che in gergo abbiamo chiamato, diciamo i pezzi, i pezzi scarpe abbiamo detto che sono recuperabili, OK, sono stati messi a sistema, staff è stato aggiornato che quel pezzo lì diciamo era era stato scartato.  
E bene, invece diciamo che andiamo nel limbo dei dei pezzi in quarantena, quindi vai nella nella pagina, nella nella Basic di turno.  
Dai, poi qua vediamo, magari nel dettaglio, vediamo anche nelle slide, vediamo un po' più nelle pagine. Se questa qua si chiama non conformità è quello lì, punto esclamativo.  
Qui in ordine, se le metti in ordine di tempo trovi la.  
In questa maschera trovate tutto lo scibile umano di tutta la roba scartata o in quarantena, siano essi componenti finiti.  
Sia.  
Prodotto finito.  
Se vedete c'è una bellissima colonna che ci indica status, se voi filtrate per quarantena vi trovate II pezzi.  
Che dovete sentenziare, dovete prendere una decisione.  
Lightroom ti dice che è un pezzo di ingresso, magari lo aggiungiamo nelle slide, invece workout operation ti dice che è un pezzo.  
In uscita no. Quindi hanno un difetto che tu hai dichiarato sempre dalla pagina da dalla pagina operatore no sta su un pezzo. Va beh che con washing dichiarare non so se è possibile che ci sia uno scarto in uscita è possibile anche perfetto.  
Possono trovare anche scarti fusione possono le trovano di ogni non ti preoccupare, quindi questo qui è questo qui è l'identificatore che vi consente di trovare diciamo.  
Il CD che contiene questo pezzo in quarantena e niente si seleziona.  
A.  
E qui c'è il famoso sentencing. No, il Sentencing cos'è dal punto di vista MES no, è un cambio di Stato di una non conformità di questa conformità che abbiamo creato quindi.  
Questa quarantena di due pezzi è un cambio di Stato che provoca una serie di azioni a cascata su SAP, principalmente su SAP, quindi ci dica un secondo, quindi l'operatore, cioè il manager.  
C'era qua.  
E deciderà la sorte di questo.  
Di questo, di questi due pezzi in quarantenne.  
Le azioni ovviamente sono vediamo brevemente no? Allora to work ditemelo voi cosa potrebbero essere, ma le azioni che succedono.  
OK, cioè le conseguenze di questa di questo sentencing? No, se io seleziono step cosa succede? È morto.  
E praticamente a livello SAP cosa succede è praticamente lo stesso con la stessa HU dichiarata dall'operatore voi battezzate che è morto definitivo.  
Definitivo, però, che andare alla causale allora sul sentencing.  
Emanuele, scusami, potresti tornare indietro nella pagina sotto se tu vedi hai diversi Tab.  
Prima tu dici la causale, quindi prima definisci sul Defect il secondo Emanuele, per favore, qui tu definisci la causale, quindi la selezioni l'aggiungi la rimuovi.  
Prima cambio la causale per quello che devo sentenziare.  
OK, poi prendo la decisione definitiva.  
Attenzione, perché una volta che noi battezziamo che il pezzo è morto.  
Quella parte lì si congela allora lo scatto dichiarato operatore è simile, non è questa procedura, è un'altra. Comunque il concetto è quello.  
Però ci siamo, quindi prima prendete la decisione sullo scarto, battezzate che causale di scarto è, poi dite che fine fargli fare i pezzi.  
Domanda, quante volte possiamo modificare la cosa di scarto? Ma una volta che dichiaro scrap non è più modificabile neanche la causale. Seconda cosa, prima dicevi di associare potenzialmente più di una.  
A causare di scarto. Questa è una cosa che al momento dobbiamo dire in linea mettetene solo una. Sì, va bene, però potrebbero metterne di più, ma un domani sarà vincolata al sistema. Questa cosa possiamo vincolarla oggi non è prevista.  
OK, Emanuele, mi aggiungi una causale per favore.  
Quella che ti piace di più?  
Va bene anche a massimo ingombro dai, non entra, non entrava va bene uno dei punti aperti ancora che non sarà sicuramente live nel momento in cui nella mia produzione c'è un non OK.  
In un futuro diventerà obbligatorio mettere in quarantena allora a oggi su ogni singolo non OK dichiarato durante la registrazione dei controlli sono obbligatorie le note.  
Quindi quello è l'unico vincolo valutiamolo non mettiamoci sì, ma io traccio che quell'operatore lì ha detto non OK, poi me li ha mandati avanti.  
Ho capito, posso metterlo nel mixer?  
Scusami, vai.  
Emanuele è bravissimo, due causali.  
Togli la seconda causale per favore, quindi io posso aggiungere n causali e poi posso togliere la causale, quella che mi serve?  
Quindi gliel'ho fatto fare apposta, inserire in modo tale che tu puoi inserire le n causali e dopo togliere quella sempre una ai fini statistici.  
Poi adesso Emanuele ha preso un CD da due da due unità.  
Volutamente gli ho fatto fare da due, posso anche dire un sentencing parziale, un pezzo torna buono, un pezzo va a scarto.  
Il totale devo andare a due. Cosa mi aspetto dal sistema? Il sistema prenderà quella quel CD lì e lo spaccherà in due, metterà underscore uno, underscore due e via dicendo, in modo tale che tu hai il pezzo che tu dici che è buono.  
Identificato con quel CD lì e te lo mandi in linea. Attenzione, nota grossa, quando voi dite che il pezzo è buono, quel pezzo fisicamente riappare sulla macchina nè.  
Quindi voi avete fisicamente il pezzo qui?  
Contabilmente, quando voi dite è buono.  
È riapparso sulla macchina che mi ha generato, quindi attenzione.  
Sì, su quella macchina che mi ha generato lo scarto.  
Se voi dite è da reworkare.  
Il sistema lo mette nelle aree che si chiamano SQ man, dopo vediamo cosa sono delle aree dedicate all'attività di rework.  
Quindi, a seconda di quello che gli dite voi, il sistema ragiona e fa fare della movimentazione del materiale in modo diverso.  
No, se vai nel detail.  
Primo primo bottone.  
OK, il secondo.  
Quando tu prendi e sentenzi il sistema manda un messaggio SAP che dice spostamelo a destra o sinistra.  
Vedete che lì avete due pezzi sulla prima, sul primo gli scrivete il numero 1 pezzo e dite dove deve, dove devo spedire questo materiale?  
Vai in bocca.  
Un parallelo con Brembo Rework ERP adesso, adesso arriviamo allora.  
Close e return to work è l'operatore ha valutato me l'ha messo in quarantena, io c'ho, io ho valutato che va bene, quindi prende torna in linea, fisicamente ce l'ho in mano io.  
Questa attività, o meglio più postazioni sono abilitato a fare questa operazione, anche le nostre, anche le nostre, però in reparto e l'aria scatta attenzione il materiale.  
Presupposto questa attività qua viene fatta normalmente sul montaggio, quindi gabbia rossa quella della alta bassa pressione è uno scarto definitivo. Caso pratico quello dello scarto estetico e l'altra gabbiettina quella che va in area montili dove c'è il montili che seleziona buono scarto.  
Scarto e via dicendo il sistema viene messo scarto lo metto nella Bagliettina rossa col suo CDOK quando la linea mi dichiara questo montilli si vede.  
Sparire al sistema la riga, lui sa che gli arriverà questa roba qua da gestire.  
Quando gli arriva il Rack, il carrellino con dentro tutti i pezzi, lui si mette lì al mattino, non c'è niente da fare, si prende i suoi pezzi e dice buono scarto, buono scarto, buono scarto, si prende il suo bel picco di CDI, si mette a sistema e fa questa attività.  
Sparo. Cosa ho fatto? È buono, dichiaro va va buono, ma fisicamente ce l'ha lì lui il pezzo. Ma se lì non c'è più quel codice, dove va a finire? Fermati.  
Siamo.  
Così montili decide buono quando la linea mi cambia il codice perché sono passati due giorni, quando montili dice va bene, dovrà fare un task manuale, quindi uno spostamento dovrà dire al Beppe Valsecchi Spostami questo materiale.  
Dal pre macchina o dal post macchina e me lo riporti in e me lo riporti tra i buoni, è quello che oggi montili ha dietro la sua stazione che sono i resi, tanto per capirci.  
Dove c'è la stazione del Montini, quella dietro dove c'è il computer, lo spostamento del materiale dalla Baia Scarti in linea al Montini, lo fa in automatico il sistema quando i ragazzi della linea dichiarano scarto quarantena, il sistema impostato che.  
Tutto il materiale contabilmente venga portato in aria contabilmente fisicamente il trenino come oggi, chi porta la roba come oggi?  
Voi, se avete voglia, potete arrivare in linea direttamente a sentenziare. Suggerimento spassionato, sentenziate la roba che avete lì.  
Deve tornare buona direttamente o scarto quello potete farlo, potete usare il PC di linea, quindi facendo il log off vi loggate con la vostra utenza personale, quindi domit, Brembo, pinco pallino con la vostra password.  
Siete già abilitati su tutte le linee, quindi se voi siete a passeggio sul montaggio trovate un qualcosa che vi dicono guarda che è in quarantena.  
Prendo posso sentenziarlo e dire no guarda che è buono e la linea la sta ancora producendo. Prendete vi loggate il sistema dice già stampami il nuovo CDI su questa linea perché è già configurato così gli dite questo è il pezzo, questo è il CDI riprocessa.  
Non ho capito.  
Non è non è collegato alle stampanti.  
Esatto, cioè se tu.  
Avessi una stampantina portatile? Sì, quelle Bluetooth non hai la stampantina portatile, USA il PC di linea, cambia il CD assolutamente.  
Scegliere quanti anche puoi scegliere quanti puoi scegliere come.  
Allora si può fare. Non vi dico, non vi nascondo che la mia idea sarebbe quella di darvi la stampantina portatile per cui col telefono, come Dicevi tu, sentenzio mi stampa, ci metto l'etichetta. Esatto, l'idea è quella.  
L'idea è quella.  
Quello che dicevi prima te Michele dopo che è stato gestito il sentencing di Maria scarti se il pezzo è buono manualmente quindi non è una chiamata automatica in EVM manualmente devi generare un warehouse task.

_[immagine]_**  
Emanuele Merlo** 2:36:32  
Poi quello che dicevi prima te dopo che è stato gestito il sentencing di Maria scarti se il prezzo è buono manualmente quindi non è una automatica manualmente devi generare un.  
E quindi deve essere un magazzino che arriva a gestire il materiale da riportare a magazzino se non è più in commissione.

_[immagine]_**  
Spreafico Paolo** 2:36:50  
E quindi deve essere magazzino che arriva a gestire il materiale da riportare a magazzino se non è più in produzione in quel momento.

_[immagine]_**  
Emanuele Merlo** 2:37:00  
Però fa parte della chiamata manuale, dire portano un Grillo.

_[immagine]_**  
Spreafico Paolo** 2:37:01  
Però, appunto, fa parte della chiamata manuale dire portalo a magazzino, portalo in linea.

_[immagine]_**  
Emanuele Merlo** 2:37:11  
Poi gli altri due casi, così Emanuele, niente, faccio per il Bono, riappare in linea, scarto arriva da qualche parte nel magazzino degli scarti rework.

_[immagine]_**  
Spreafico Paolo** 2:37:11  
Poi gli altri due casi, così Emanuele mi ritaccio per l'IRA di Dio, buono riappare in linea, scarto arriva da qualche parte nel magazzino degli scarti rework.

_[immagine]_**  
Emanuele Merlo** 2:37:26  
Abbiamo tre casi, giusto? Sì, inizialmente.

_[immagine]_**  
Spreafico Paolo** 2:37:26  
Abbiamo tre casi, giusto tendenzialmente.

_[immagine]_**  
Emanuele Merlo** 2:37:30  
Quali sono i casi?

_[immagine]_**  
Spreafico Paolo** 2:37:30  
Quali sono i casi?

_[immagine]_**  
Emanuele Merlo** 2:37:32  
Prime, i tre, conto avremo, conto fornitore.

_[immagine]_**  
Spreafico Paolo** 2:37:33  
Primer.  
P tre, colpa Brembo, colpa fornitore.

_[immagine]_**  
Emanuele Merlo** 2:37:38  
Poco di moda.

_[immagine]_**  
Spreafico Paolo** 2:37:39  
Colpa di Mosè?

_[immagine]_**  
Emanuele Merlo** 2:37:41  
Colpa di un detto che ho denunciato internamente.

_[immagine]_**  
Spreafico Paolo** 2:37:41  
Colpa di Mosè perché ho verniciato internamente?

_[immagine]_**  
Emanuele Merlo** 2:37:46  
Poi casi di come li gestiamo secondo voi?

_[immagine]_**  
Spreafico Paolo** 2:37:47  
Quei casi lì come li gestiamo secondo voi?

_[immagine]_**  
Emanuele Merlo** 2:37:50  
Il signor Montini.

_[immagine]_**  
Spreafico Paolo** 2:37:50  
Il signor Montili.

_[immagine]_**  
Emanuele Merlo** 2:37:53  
Durante la sua attività di shorting dice, è colpa Brembo, è colpa fornitore.

_[immagine]_**  
Spreafico Paolo** 2:37:53  
Durante la sua attività di shorting dice, è colpa Brembo, è colpa fornitore.

_[immagine]_**  
Emanuele Merlo** 2:37:59  
A seconda di quello che loro selezionano.

_[immagine]_**  
Spreafico Paolo** 2:37:59  
A seconda di quello che loro selezionano.

_[immagine]_**  
Emanuele Merlo** 2:38:04  
Il sistema incomincia a spacchettare.

_[immagine]_**  
Spreafico Paolo** 2:38:04  
Il sistema incomincia a spacchettare.

_[immagine]_**  
Emanuele Merlo** 2:38:09  
Cosa vuol dire questo torniamo?

_[immagine]_**  
Spreafico Paolo** 2:38:09  
Cosa vuol dire questo torniamo?

_[immagine]_**  
Emanuele Merlo** 2:38:12  
Al passo precedente.

_[immagine]_**  
Spreafico Paolo** 2:38:13  
Al passo precedente.

_[immagine]_**  
Emanuele Merlo** 2:38:16  
Cosa mi serve per sentenziare? Mi serve un codice, un ordine? Mi serve un qualcosa? Cosa mi serve per far fare l'attività di carteggiatura e di ripresa da blender ditemelo a voi.

_[immagine]_**  
Spreafico Paolo** 2:38:16  
Cosa mi serve per sentenziare? Mi serve un codice, un ordine? Mi serve un qualcosa? Cosa mi serve per far fare l'attività di carteggiatura e di ripresa da brinver?  
Ditemelo voi.  
No serve un ordine.

_[immagine]_**  
Emanuele Merlo** 2:38:34  
Quindi verrà lanciato un ordine specifico per riprendere il materiale presso Grillo verso Grillo a seconda del carico.

_[immagine]_**  
Spreafico Paolo** 2:38:35  
Quindi verrà lanciato un ordine specifico di per riprendere il materiale presso brimver o verso 23 a seconda del carico.

_[immagine]_**  
Emanuele Merlo** 2:38:47  
Pago o non pago la prestazione, io ci sono molti ci prove a due ordini.

_[immagine]_**  
Spreafico Paolo** 2:38:47  
Pago o non pago la prestazione, il signor Montesi troverà due ordini.

_[immagine]_**  
Emanuele Merlo** 2:38:53  
Cosa dovrà fare, signor Montini?

_[immagine]_**  
Spreafico Paolo** 2:38:54  
Cosa dovrà fare il signor Montili?

_[immagine]_**  
Emanuele Merlo** 2:38:57  
Dai ditemelo su.

_[immagine]_**  
Spreafico Paolo** 2:38:57  
Dai ditemelo su.

_[immagine]_**  
Emanuele Merlo** 2:39:00  
Ti prenderà il suo bel ballo fuori di CD.

_[immagine]_**  
Spreafico Paolo** 2:39:00  
Si prenderà il suo bel malloppone di CD.

_[immagine]_**  
Emanuele Merlo** 2:39:04  
Aprirà l'ordine, diventerà una macchina, una linea proiettiva, si metterà lì.

_[immagine]_**  
Spreafico Paolo** 2:39:04  
Aprirà l'ordine, diventerà una macchina, una linea produttiva, si metterà lì.

_[immagine]_**  
Emanuele Merlo** 2:39:10  
Dichiarerà i consumi, prenderà in carico questo materiale.

_[immagine]_**  
Spreafico Paolo** 2:39:11  
Dichiarerà i consumi, prenderà in carico questo materiale.

_[immagine]_**  
Emanuele Merlo** 2:39:17  
Dichiarerà che tutta quella produzione di quel codice.

_[immagine]_**  
Spreafico Paolo** 2:39:17  
Dichiarerà che tutta quella produzione di quel codice.

_[immagine]_**  
Emanuele Merlo** 2:39:22  
Uscirà con quel lotto produttivo?

_[immagine]_**  
Spreafico Paolo** 2:39:22  
Uscirà con quel lotto produttivo?

_[immagine]_**  
Emanuele Merlo** 2:39:28  
Il lotto per ogni codice, un lotto per ogni codice hai detto giusto, quindi un ordine per ogni codice.

_[immagine]_**  
Spreafico Paolo** 2:39:30  
Un lotto per ogni codice, hai detto giusto?

_[immagine]_**  
Emanuele Merlo** 2:39:36  
OK, cosa vuol dire qui che se noi abbiamo 5 6 pezzi di lotti diversi tanto arriverà nell'area motivi già oggi prendo e accorpo diversi lotti produttivi, a oggi facciamo casino perché non riusciamo a legarli?

_[immagine]_**  
Spreafico Paolo** 2:39:36  
OK, cosa vuol dire qui? Che se noi abbiamo 5 6 pezzi di lotti diversi tanto arriva là nell'area montiri, già oggi prendo e accorpo diversi lotti produttivi, a oggi facciamo casino perché non riusciamo a legarli.

_[immagine]_**  
Emanuele Merlo** 2:39:53  
Domani riusciremo a dire guarda che questo CD di scarto o reworkabile dalla linea è stato contattato in questo ordine di rework è uscito con questo ordine di rework ed è rientrato.

_[immagine]_**  
Spreafico Paolo** 2:39:53  
Domani riusciremo a dire guarda che questo CDI di scarto o reworkabile dalla linea è stato compattato in questo ordine di rework è uscito con questo ordine di rework.  
Ed è rientrato.

_[immagine]_**  
Emanuele Merlo** 2:40:10  
Abbiamo la genealogia di quando è uscito, di quando è rientrato.

_[immagine]_**  
Spreafico Paolo** 2:40:10  
Abbiamo la genealogia di quando è uscito, di quando è rientrato.

_[immagine]_**  
Emanuele Merlo** 2:40:17  
Punti, domande, perplessità su questo erano tante.

_[immagine]_**  
Spreafico Paolo** 2:40:18  
Dubbi, domande e perplessità su questo credo tante.  
Faccio un pezzo, faccio l'ordine da un pezzo, faccio l'ordine da una settimana da 1000 pezzi, troverà un ordine da 1000 pezzi.

_[immagine]_**  
Emanuele Merlo** 2:40:30  
Faccio l'ordine da una settimana, da 1000 pezzi, da 1000 pezzi.  
Durante la settimana lui sarà autorizzato a prendere tutti i cibi di quella settimana in quel codice lì, io questi tre sono di responsabilità, l'ordine di quei tre articoli di responsabilità, cioè li dovrà dire.

_[immagine]_**  
Spreafico Paolo** 2:40:41  
Durante la settimana lui sarà autorizzato a prendere tutti ICD di quella settimana di quel codice lì dire questi tre sono di responsabilità Brembo e avrà l'ordine di quei tre articolo di responsabilità Brembo, quindi dovrà dire.

_[immagine]_**  
Emanuele Merlo** 2:40:56  
123 mi aggancio su questo ordine di responsabilità grembo verrà battezzato un lotto specifico per quell'ordine fintanto che motivi non chiuderà quell'ordine nell'arco della.

_[immagine]_**  
Spreafico Paolo** 2:40:56  
1, 2 e tre li aggancio su questo ordine di responsabilità Brembo verrà battezzato un lotto specifico per quell'ordine fintanto che montili non chiuderà quell'ordine, quindi nell'arco della.

_[immagine]_**  
Emanuele Merlo** 2:41:11  
Settimana o dell'altra, i due giorni dipende da quando vanno a bordi materiale, tutti quei codici lì e tutti quella parte lì verrà aggregato in un unico ordine, in un unico batch.

_[immagine]_**  
Spreafico Paolo** 2:41:11  
Settimana o nell'arco dei due giorni? Dipende da quando manda fuori il materiale, tutti quei codici lì e tutti quella parte lì verrà aggregata in un unico ordine, in un unico batch.  
Due mesi ti interrompo sempre.

_[immagine]_**  
Emanuele Merlo** 2:41:29  
No perché OKE quindi fisicamente vediamo se viene creato un'altro un'altro container viene duplicato. Proviamo allora questo qua scarpalo.

_[immagine]_**  
Spreafico Paolo** 2:41:33  
OKE, quindi allora fisicamente vediamo se viene creato un'altro, un'altro container viene duplicato, proviamo.

_[immagine]_**  
Emanuele Merlo** 2:41:43  
Puoi metterci una nota anche voi due, quindi questo qua, questo pezzo qua è stato scattato con quella causale, magari devi tornare sulla sulla allora il CDA 105.

_[immagine]_**  
Spreafico Paolo** 2:41:43  
Poi metterci una nota, quindi questo qua, questo pezzo qua è stato schiattato comunque da causale, devi tornare sulla allora il nostro CD è il 105.

_[immagine]_**  
Emanuele Merlo** 2:41:58  
Non confondono 105 e ti troverai su allarghi, 105 underscore uno.

_[immagine]_**  
Spreafico Paolo** 2:41:58  
Con form 105 e ti troverai se allarghi un pochino la prima colonna.  
No allargalo sulla prima colonna, vedete che è 105 underscore uno.

_[immagine]_**  
Emanuele Merlo** 2:42:11  
E l'altro rimane in quarantena, quindi diciamo che l'altro rimane da fare sempre sul pezzo rimanente, invece scatta in uno Stato finale e appunto e poi è stato viene gestito dal.

_[immagine]_**  
Spreafico Paolo** 2:42:14  
Che tra l'altro rimane da Paris Hilton sul pezzo rimanente e invece scatta in uno Stato finale e appunto poi è stato rivistato da SAP sulla quarantena, quindi sulla quarantena poi.

_[immagine]_**  
Emanuele Merlo** 2:42:27  
Sulla quarantena, quindi su quello in quarantena poi.  
Prima o poi il quality manager deve sentenziare anche quello, non può rimanere a sistema un sistema.

_[immagine]_**  
Spreafico Paolo** 2:42:32  
Prima o poi il quality manager deve anche quello, non può rimanere a sistema un sistema in quarantena. Poi c'è un c'è una scadenza, ragazzi cosa facciamo con i pezzi a quarantena noi? Quanto tempo possono stare a quarantena?  
Prende il motivo per cui abbiamo messo in quarantena, cioè non.

_[immagine]_**  
Emanuele Merlo** 2:42:55  
Tendenzialmente, vediamo di sbatti nell'arco di 1 2 mesi.

_[immagine]_**  
Spreafico Paolo** 2:42:55  
Tendenzialmente vediamo di smaltire la quarantena nell'arco di 1 2 mesi.

_[immagine]_**  
Emanuele Merlo** 2:43:02  
Perché se no, ovviamente.

_[immagine]_**  
Spreafico Paolo** 2:43:02  
Perché se no, ovviamente.  
In due mesi.  
Quanta roba c'avete in quarantena per più di un mese, due mesi? Qualcosa di sicuro non è il day by Day.

_[immagine]_**  
Emanuele Merlo** 2:43:11  
Quanta? Quanta roba c'avete in quarant'è dopo più di un mese, due mesi? Qualcosa di sicuro non è no lo so, forse dobbiamo fermare il materiale, fare cadute battenti, teste. Allora questo è materiale che mi arriva dalle linee.

_[immagine]_**  
Spreafico Paolo** 2:43:20  
No, lo so. Però se dobbiamo fermare il materiale, fare cadute, battenti, test, allora questo è materiale che mi arriva dalle linee. Non sono del materiale a magazzino per il quale sto facendo prove. Ricordiamoci sempre.

_[immagine]_**  
Emanuele Merlo** 2:43:29  
Non sono del materiale a magazzino per il quale sto facendo prove, ricordiamoci sempre questa quarantena qua.

_[immagine]_**  
Spreafico Paolo** 2:43:35  
Questa quarantena qua.  
Scusami Denise, è la \*\*\*\*\* che cagan fuori le linee.

_[immagine]_**  
Emanuele Merlo** 2:43:39  
E la \*\*\*\*\* che te abbiamo corrido Elisa.  
Non è materiale che ha magazzino, io sono all'interno dello stabilimento, non sono da Emiliano, non sono da Beppe.

_[immagine]_**  
Spreafico Paolo** 2:43:53  
È la roba che sto producendo in quarantena.

_[immagine]_**  
Emanuele Merlo** 2:43:53  
È la roba che sto producendo in quarantena, un cassone.

_[immagine]_**  
Spreafico Paolo** 2:43:57  
Qui, ma sono fuori dalla linea.

_[immagine]_**  
Emanuele Merlo** 2:44:03  
Cambierà ubicazione, cambia ubicazione.

_[immagine]_**  
Spreafico Paolo** 2:44:05  
Cambia ubicazione.  
Sì, quindi è il materiale che tu dici è in quarantena perché lo sto gestendo adesso?

_[immagine]_**  
Emanuele Merlo** 2:44:09  
Quindi è il materiale che tu dici è in quarantena perché lo sto gestendo adesso?  
Se fisicamente tu mi dici il materiale è sospeso perché lo sto valutando?

_[immagine]_**  
Spreafico Paolo** 2:44:17  
Se fisicamente tu mi dici il materiale è sospeso perché lo sto valutando?  
Lo sto valutando perché lo sto producendo e sono in linea. Oppure ho bloccato la produzione e sono a magazzino perché se ho il problema in linea probabilmente ho del materiale anche a magazzino tendenzialmente. Quindi cosa faccio? Prendo anche tutto quel materiale che c'è a magazzino, quindi sono fuori dalle linee, sono.

_[immagine]_**  
Emanuele Merlo** 2:44:23  
Lo sto valutando.

_[immagine]_**  
Spreafico Paolo** 2:44:43  
Fuori dai bue, sono fuori dal MES.  
Trasferisco e blocco quel materiale nell'area di quarantena, ma son fuori dalla linea.

_[immagine]_**  
Emanuele Merlo** 2:44:47  
Trasferisco e blocco quel materiale nell'area di quarantena, ma son fuori dalla linea.

_[immagine]_**  
Spreafico Paolo** 2:44:54  
Ipotizzate che questo sistema qui che ci stanno presentando è sullo shop floor, se il cassone va dalla parte esterna fuori dallo shop floor, non sono più qui, sono nel SAP, sono in EVM, sono da un'altra parte.

_[immagine]_**  
Emanuele Merlo** 2:44:54  
Ipotizzando che questo sistema qui che ci stanno presentando è sullo shop floor, se il cassone va dalla parte esterna, poi dallo shop floor, non sono più qui, sono nel SAP, sono in EVM, sono da un'altra parte.  
Quindi in una settimana, cioè nel senso non rimane più di una settimana, abbiamo risposto Paolo, sì, grazie quindi.

_[immagine]_**  
Spreafico Paolo** 2:45:15  
Quindi in una settimana, cioè nel senso non rimane più di una settimana il materiale e sarò sì, in quel caso gestito abbiamo risposto Paolo.

_[immagine]_**  
Emanuele Merlo** 2:45:27  
Allora facciamo l'ultimo sentencing e facciamolo ritornare, diciamo in good magari i due casi diciamo semplici, però la causale in caso di good la lasciamo vuota, possiamo eliminare la causale?

_[immagine]_**  
Spreafico Paolo** 2:45:37  
Possiamo eliminarla causale piuttosto dipende da voi.

_[immagine]_**  
Emanuele Merlo** 2:45:44  
Piuttosto dipende da voi, se non lo elimino non è che va su Power BI, va su Power BI. In sai caso troverà troverete che quel pezzo è tornato a buono, quindi viene escluso perché avrai pezzi scarto quello zero perché tornano buoni.

_[immagine]_**  
Spreafico Paolo** 2:45:49  
Va su Power BI, in tal caso troverà troverete che quel pezzo è tornato a buono, quindi viene escluso perché avrà i pezzi scarto uguali a zero perché tornano buoni però con la traccia guarda che ha avuto questa problematica a vostra discrezione.

_[immagine]_**  
Emanuele Merlo** 2:46:00  
Però torno nella traccia, guarda che anche per fare un problema a vostra discrezione.  
OKE, quindi fanno il proprio marketing work bene e diciamo questa nota e quindi per quanto riguarda il sentencing diciamo qui appunto ricordiamo il contesto no?

_[immagine]_**  
Spreafico Paolo** 2:46:12  
La nota e quindi per quanto riguarda il sentencing diciamo.  
Qui appunto, ricordiamo il contesto, no material light significa componente in ingresso, no, quindi componente di da consumare di input, invece workload operation in.

_[immagine]_**  
Emanuele Merlo** 2:46:24  
Matina light, che significa componente in ingresso, ma quindi componente di da consumare di input e invece work code operation, work code operation in.  
Per noi MES è l'operazione, il ciclo no, quindi è in questo caso era la fase, quella di lavaggio alta pressione, quella fase lì, quindi questa fase qui produce un materiale di washing che adesso non abbiamo visto magari.

_[immagine]_**  
Spreafico Paolo** 2:46:38  
Per noi il MES è l'operazione, il ciclo no, quindi è in questo caso era la fase quella di lavaggio alta pressione, cioè quella fase lì, quindi questa fase qui produce materiale che adesso vediamo.

_[immagine]_**  
Emanuele Merlo** 2:46:55  
OK, io direi che a questo punto adesso questa fase qua diciamo operativa del coso è finita, no? Se torniamo indietro velocemente ritorniamo a quell'ordine.

_[immagine]_**  
Spreafico Paolo** 2:46:56  
Ok, io direi che a questo punto adesso questa fase qua diciamo operativa di riposo, ritorniamo indietro velocemente, ritorniamo a quell'ordine.

_[immagine]_**  
Emanuele Merlo** 2:47:11  
E quello del materiale 3 7 sempre del washing che non aveva nessun prodotto. E adesso vediamo un secondo come prendi di nuovo questo qua, quindi vedete che il materiale è 3 8?

_[immagine]_**  
Spreafico Paolo** 2:47:11  
Il quello del materiale 3 7 sempre del washing e non aveva nessun controllo e adesso vediamo un secondo come prendi di nuovo questo qua, quindi vedete che materiale tre o.

_[immagine]_**  
Emanuele Merlo** 2:47:27  
Tu no anziché 3 7, OK.

_[immagine]_**  
Spreafico Paolo** 2:47:27  
Torno anziché 3 7 cari.

_[immagine]_**  
Emanuele Merlo** 2:47:30  
Questo qua significa che è uno Stato verde, quindi che è stato iniziale ancora da startare. Questo qua, anche questo a 10 pezzi no, è come prima, ma non ha una non ha nessun dispatch no quindi?

_[immagine]_**  
Spreafico Paolo** 2:47:30  
Questo qua significa che è uno Stato red, quindi che è stato iniziale ancora da startare questo qua, anche questo a 10 pezzi no, è come prima, ma non ha una non ha nessun no, quindi sarebbe un ordine in qualche modo.

_[immagine]_**  
Emanuele Merlo** 2:47:45  
Faremo un ordine in qualche modo con sbagliato no, difettoso no, quindi non dovrebbe nemmeno essere startup. Vediamo dietro alle quinte cos'è che succede allora.

_[immagine]_**  
Spreafico Paolo** 2:47:49  
Sbagliato no. Difettoso no. Quindi non dovrebbe nemmeno essere startup. Vediamo dietro le quinte cos'è che succede allora.

_[immagine]_**  
Emanuele Merlo** 2:47:58  
Qua magari sembra anche interessante vedere Power bi, ma qua abbiamo già abbastanza abbastanza dati no, perché se noi copiamo adesso copia un secondo l'ordine e entriamo nella pagina, diciamo quella.

_[immagine]_**  
Spreafico Paolo** 2:47:58  
Qua magari sarebbe anche interessante vedere Power BI, ma qua abbiamo già abbastanza abbastanza dati no? Perché se non copiamo l'ordine adesso copio un secondo l'ordine e entriamo nella pagina, diciamo quella.

_[immagine]_**  
Emanuele Merlo** 2:48:13  
Supervisor no, quella quell'insieme di pagine tutte diverse no.

_[immagine]_**  
Spreafico Paolo** 2:48:13  
Supervisor no, quella quell'insieme di pagine tutte diverse no.

_[immagine]_**  
Emanuele Merlo** 2:48:18  
Quindi entra nella pagina work order, qui c'è una pagina che fa vedere tutti i work order, no? In vista flat si chiama work orders.

_[immagine]_**  
Spreafico Paolo** 2:48:18  
Quindi entra nella pagina work order, qui c'è una pagina che fa vedere tutti i work order no in sta flat si chiama work orders.

_[immagine]_**  
Emanuele Merlo** 2:48:29  
Vedete quindi qua col prodotto, con tutto quanto.

_[immagine]_**  
Spreafico Paolo** 2:48:29  
Vedete quindi qua col prodotto, con tutto quanto.

_[immagine]_**  
Emanuele Merlo** 2:48:34  
Puoi filtrare e questo qua abbiamo il nostro ordine, no? Quindi vedete status New che sarebbe quella a mezzaluna verde qua lo apriamo e qua vediamo appunto delle cose interessanti, no? Quindi.

_[immagine]_**  
Spreafico Paolo** 2:48:34  
Puoi filtrare e questo qua abbiamo un nostro ordine, no? Quindi vedete status New che è sempre quella a mezzaluna verde, qua lo apriamo e qua vediamo appunto delle cose interessanti, no? Quindi.

_[immagine]_**  
Emanuele Merlo** 2:48:50  
Il appunto l'identificatore poi qua abbiamo questo qua è un ordine che viene lasciato, quindi ha il suo identificativo in SAP che sono uguali. Questo qua è il process NID, questa qui è quella che voi chiamate routing, quindi è.

_[immagine]_**  
Spreafico Paolo** 2:48:50  
Il appunto l'identificatore. Poi qua abbiamo questo qua è un ordine che viene lasciato, quindi ha il suo identificativo in SAP che sono uguali. Questo qua è il process SMD, questa qui è quella che voi chiamate routing, quindi è.

_[immagine]_**  
Emanuele Merlo** 2:49:06  
Diciamo il la classe no, il template da cui vengono generati tutti questi ordini è un oggetto no, il cosiddetto master data, oggetto di ingegnere che è configurabile.

_[immagine]_**  
Spreafico Paolo** 2:49:06  
Diciamo il la classe no, il template da cui vengono generati tutti questi ordini è un oggetto no, il cosiddetto master data, oggetto di un genere che è configurabile.

_[immagine]_**  
Emanuele Merlo** 2:49:22  
Perché è quello che contiene praticamente.

_[immagine]_**  
Spreafico Paolo** 2:49:22  
E che è quello che contiene praticamente tutte le definizioni che creeranno l'ordine. Un ordine nuovo simile a questo no. Quindi se dovessimo crearlo l'ordine.

_[immagine]_**  
Emanuele Merlo** 2:49:26  
Tutte le definizioni che creeranno l'ordine in ordine nuovo simile a questo no, quindi se non dovessimo creare l'ordine uso quello dopo no quello 380.

_[immagine]_**  
Spreafico Paolo** 2:49:37  
Uso quello dopo no quello 380 sempre con questo con questo tipo di processo praticamente sarà un ordine molto simile che va alla stessa struttura, quindi le stesse operation, le stesse ispezioni.

_[immagine]_**  
Emanuele Merlo** 2:49:41  
Sempre con questo, con questo tipo di processo, praticamente sarà un ordine molto simile che va la stessa struttura, quindi le stesse operation, le stesse ispezioni, le stesse immagini, comunque sarà molto uguale però perché viene dallo stesso tempo.

_[immagine]_**  
Spreafico Paolo** 2:49:54  
Le stesse immagini comunque siamo molto uguali però perché viene dallo stesso template quindi copiamo andiamo a vedere questo template no questa questo multi come è fatto quindi copio secondo questo.

_[immagine]_**  
Emanuele Merlo** 2:50:00  
Quindi copiamo andiamo a vedere questo template no questa questo routing come è fatto quindi copia un secondo questo.  
Questo e c'è un'altra pagina, sempre qui, fondamentale, che si chiama.

_[immagine]_**  
Spreafico Paolo** 2:50:09  
Questo e c'è un'altra pagina, sempre qui fondamentale, che si chiama POP.  
E questa qui è diciamo anche questa qua viene creata tramite SAP che viene scaricata da SAP e praticamente da una parte hai l'istanza quindi che è il Word code che è l'oggetto.

_[immagine]_**  
Emanuele Merlo** 2:50:20  
E questa qui è diciamo anche questa qua viene creata tramite il SAP che viene scaricata da SAP e praticamente da una parte hai l'istanza quindi che è l'oggetto.  
Dov'è? Come è fatto quell'oggetto singolo lì? No, questo qua viene da viene creato da SAP. Dall'altra parte invece hai il template, quindi la classe che crea che crea il no. Quindi da una parte hai.

_[immagine]_**  
Spreafico Paolo** 2:50:36  
E come è fatto quell'oggetto singolo lì? No, questo qua viene da viene creato da SAP. Dall'altra parte invece hai il template, quindi la classe che crea che crea il no. Quindi da una parte hai.

_[immagine]_**  
Emanuele Merlo** 2:50:52  
L'esempio quindi con una certa data, una certa data iniziale, data finale no verificata mi ha dato invece la configurazione che crea quell'istanza no. Quindi abbiamo due nomi diversi, uno si chiama Word code.

_[immagine]_**  
Spreafico Paolo** 2:50:52  
Esempio quindi con una certa data, una certa data iniziale, data finale no, verificata nel lato invece ha la configurazione che crea quell'istanza no. Quindi abbiamo due nomi diversi, uno si chiama World Code.

_[immagine]_**  
Emanuele Merlo** 2:51:09  
E l'altro invece si chiama tutte e due sono, cioè questo qui è versionato da BOP, OK, questa vedete?

_[immagine]_**  
Spreafico Paolo** 2:51:10  
E l'altro invece si chiama tutti e due sono, cioè questo qui è versionato da BOP, OK, questa vedete?

_[immagine]_**  
Emanuele Merlo** 2:51:21  
Se viene aggiornata verrà creato underscore due no. E questa qua sarà dichiarata o la revision sale no? E questo qui è quello quella cosa che dicevamo dell'eredità del di eredità di no.

_[immagine]_**  
Spreafico Paolo** 2:51:21  
Se viene aggiornata verrà creato underscore due no e questa qua sarà dichiarata o la revision sale no. E questo qui è quella cosa che dicevamo dell'eredità dell'eredità di no.

_[immagine]_**  
Emanuele Merlo** 2:51:37  
Vediamo un secondo allora no, volevo dire, quello che stava spiegando Paolo è che praticamente per fare ad esempio una pinza Ferrari no, c'è il l'ingegneria che decide.

_[immagine]_**  
Spreafico Paolo** 2:51:37  
Vediamo un secondo allora se tanto da Apri no volevo dire quello che stava spiegando Paolo è che praticamente per fare ad esempio una pinza Ferrari no, c'è il.  
L'ingegneria che decide come va fatta, qual è la sequenza di operazioni che vanno fatte e lo definisce in questo ciclo che noi chiamiamo lista dei processi per il report.

_[immagine]_**  
Emanuele Merlo** 2:51:53  
Come va fatta? Qual è la sequenza di operazioni che vanno fatte? E lo definisce in questo ciclo che noi chiamiamo lista dei processi, che in inglese da questa lista dei processi poi viene usata, viene usata.

_[immagine]_**  
Spreafico Paolo** 2:52:06  
Da questa lista dei processi poi viene usata come viene trasferita come modello per l'ordine di lavorazione, quindi la lista la lista delle operazioni è generica per tutte le pinze fiorari però poi.

_[immagine]_**  
Emanuele Merlo** 2:52:12  
Come viene trasferita come modello per l'ordine di lavorazione, quindi la lista la lista delle operazioni è generica per tutte le pinze Ferrari. Però poi dicono, OK, questa settimana qua produciamo, non so, dico una settimana magari di più.

_[immagine]_**  
Spreafico Paolo** 2:52:21  
Dico no, OK, questa settimana qua produciamo non so, dico una settimana, magari produciamo 500 pinze Ferrari, utilizzeremo questo materiale qua che è stato prodotto in questa data qua e quindi dà una descrizione generica di come si fa una pinza Ferrari.

_[immagine]_**  
Emanuele Merlo** 2:52:27  
Produciamo 500 pinze Ferrari, utilizzeremo questo materiale qua che è stato prodotto in questa data qua e quindi da una descrizione generica di come si fa una pinza Ferrari diventa un ordine di produzione vero e proprio con cui è stato.

_[immagine]_**  
Spreafico Paolo** 2:52:40  
Diventa un ordine di produzione vero e proprio con cui è stato a cui verrà assegnato il materiale e verrà tracciato quel giorno lì. Fammi 10 pinze, no, qua hai diciamo come fare.

_[immagine]_**  
Emanuele Merlo** 2:52:44  
A cui esse verrà assegnato del materiale e verrà tracciato tutto come è stato prodotto. E diciamo come fare una pinza Ferrari, no? Vedi che qua ad esempio la Corte è uno, no?

_[immagine]_**  
Spreafico Paolo** 2:52:56  
Una pinza Ferrari, no? Vedi che qua ad esempio la ponte di a uno no, qui c'è la descrizione di come farne una, quindi quali sono, quali sono, quali sono II processi da fare, come, quali sono gli interlock, cosa?

_[immagine]_**  
Emanuele Merlo** 2:53:00  
Qui come fanno in una, quindi quali sono, quali sono, quali sono i processi, l'operation da fare, come, quali sono gli interlocking, cosa, come sono, quali sono gli spection definition quindi?

_[immagine]_**  
Spreafico Paolo** 2:53:12  
Ho messo quindi i dati di qualità associati alle singole operazioni e poi invece viene OK quel giorno lì, cioè gestisci questo.

_[immagine]_**  
Emanuele Merlo** 2:53:16  
II dati di qualità associati alle singole operazioni e poi invece viene OK quel giorno lì, cioè gestisci questo ordine di produzione e l'ordine di produzione avrà associato.  
Tutte, tutte le sue, i suoi dati per produrre una pinza ferrarica che sono le caratteristiche di qualità se necessario. Adesso non sono nel dettaglio, però se è necessario usare per esempio utensili particolari, saranno associati eccetera eccetera.

_[immagine]_**  
Spreafico Paolo** 2:53:32  
Tutte le sue, i suoi dati sono le caratteristiche di qualità, se necessario. Adesso non sto nel dettaglio, però se c'è è necessario usare per esempio i sensi particolari salami associati.

_[immagine]_**  
Emanuele Merlo** 2:53:48  
E la cosa interessante, che poi è proprio, diciamo, la prima delle cose chiave no del MES, OK, è che.  
Questa, diciamo questa fabbrica di ordini, chiamiamola così, OK, viene creata da SAP, non viene downloadata da SAP però.

_[immagine]_**  
Spreafico Paolo** 2:53:58  
Questa, diciamo questa fabbrica di ordini, chiamiamola così, OK, viene creata da SAP, non viene downloadata da SAP però.

_[immagine]_**  
Emanuele Merlo** 2:54:11  
Cioè noi operatori MES, voi operatori di qualità dovete entrare e fare quella cosa che si chiama arricchimento no? Quindi aggiungere dei dati specifici magari che non che non derivano da SAP no?

_[immagine]_**  
Spreafico Paolo** 2:54:11  
Cioè noi operatori MES, voi operatori di qualità dovete entrare e fare quella cosa che si chiama arricchimento, no? Quindi aggiungere dei dati specifici magari che non che non derivano da SAP no.

_[immagine]_**  
Emanuele Merlo** 2:54:26  
E quali sono questi dati specifici particolari? Non so, potevo essere i tool da usare, potevo essere magari dei degli interlocking no, del delle dipendenze no da creare, oppure potremmo essere come nel vostro caso i dati di qualità.

_[immagine]_**  
Spreafico Paolo** 2:54:27  
E quali sono questi dati specifici nei particolari? Non so potrebbero essere i tool da usare, potrebbero essere magari dei no del delle dipendenze no da creare oppure potrebbero essere come nel vostro caso i dati di qualità.

_[immagine]_**  
Emanuele Merlo** 2:54:44  
I dati di qualità è per esempio che è locale a al MES OP Center che non deriva da SAP ma che è gestito no da voi e poi con aiuto ovviamente.

_[immagine]_**  
Spreafico Paolo** 2:54:44  
I dati di qualità è un esempio che è locale a al MES AOP Center che non deriva da SAP ma che è gestito no da voi e poi con aiuto ovviamente.

_[immagine]_**  
Emanuele Merlo** 2:55:00  
SAP mi manda la bomba. E come deve essere costruito il ciclo? OK, Questo è quanto meglio la SAP dentro qui proviamo se mi apre un secondo il ciclo.

_[immagine]_**  
Spreafico Paolo** 2:55:02  
La faccio facilissima. Stupidissima SAP mi manda la bomba e come deve essere costruito il ciclo? OK, Questo è quanto mi arriva la SAP.  
Dentro qui proviamo, se me la Apri un secondo, il ciclo, come è battezzato il ciclo.

_[immagine]_**  
Emanuele Merlo** 2:55:17  
Come battezzato il ciclo?  
Nell'operation le fasi del ciclo in questo caso è uno, nel caso del montaggio troverete il primo montaggio completamente, quindi troverete due palloni, due palline.

_[immagine]_**  
Spreafico Paolo** 2:55:21  
Nell'operation le fasi del ciclo in questo caso è uno, nel caso del montaggio troverete primo montaggio e completamento, quindi troverete due palloni, due palline.

_[immagine]_**  
Emanuele Merlo** 2:55:32  
All'interno della singola operazione per favore.

_[immagine]_**  
Spreafico Paolo** 2:55:32  
All'interno della singola operazione entrami proprio nell'operazione, per favore.

_[immagine]_**  
Emanuele Merlo** 2:55:39  
Trovate tutti i dati specifici per quella specifica operazione, tra cui le nostre foto di qualità.

_[immagine]_**  
Spreafico Paolo** 2:55:40  
Trovate tutti i dati specifici per quella specifica operazione, tra cui le nostre forme di qualità se tu vai su mora.

_[immagine]_**  
Emanuele Merlo** 2:55:48  
E tu vai su Moro?

_[immagine]_**  
Spreafico Paolo** 2:55:53  
E schiacci quality inspection.

_[immagine]_**  
Emanuele Merlo** 2:55:56  
Dentro qui nel nostro master andiamo a inserire tutti i controlli che vogliamo far fare per quella specifica operazione.

_[immagine]_**  
Spreafico Paolo** 2:55:56  
Dentro qui, nel nostro master, andiamo a inserire tutti i controlli che vogliamo far fare per quella specifica operazione di quel specifico ciclo di lavoro.

_[immagine]_**  
Emanuele Merlo** 2:56:07  
In quel specifico ciclo di lavoro.  
Vi ricordate prima che abbiamo detto? Ho tre macchine di produzione, posso personalizzare a seconda della macchina e della base del ciclo? Quello che voglio controllare lo faccio entro qua e questo qua è un dato interno a me che viene gestito da voi.

_[immagine]_**  
Spreafico Paolo** 2:56:12  
Vi ricordate prima che abbiamo detto ho tre macchine di produzione, posso personalizzare a seconda della macchina e della fase del ciclo? Quello che voglio controllare lo faccio dentro qua.  
Se viene gestito da voi poi con delle procedure automatiche per prendere le cose vecchie diciamo e associarle direttamente no allora vediamo un secondo, ditemi voi come fate allora?

_[immagine]_**  
Emanuele Merlo** 2:56:29  
OK poi beh, con delle procedure automatiche per prendere le cose vecchie diciamo e associarle direttamente no? Allora vediamo un secondo, ditemi voi come fare allora.

_[immagine]_**  
Spreafico Paolo** 2:56:41  
Vuoi uno per il lavaggio, uno per machining, uno per dipende da come sono configurati i sics sono operazioni diverse, possono essere o spacchettati oppure aggregati.

_[immagine]_**  
Emanuele Merlo** 2:56:49  
Sono operazioni diverse, quindi chiudilo un secondo per favore allora ditemi allora questo qui è vuoto, OK, avete visto? Quindi ha creato quell'ordine difettoso che non aveva qui invece.

_[immagine]_**  
Spreafico Paolo** 2:56:56  
Allora ditemi allora questo qui è vuoto OK avete visto quindi e ha creato quell'ordine difettoso che non aveva e invece ditemi come fare a entrare nel process quello buono così anche se aveva dei dati un po'.

_[immagine]_**  
Emanuele Merlo** 2:57:04  
Ditemi come fare a entrare nel process, quello buono così anche se aveva dei dati un po comunque che aveva qualche dato di qualità che abbiamo usato nell'esempio precedente, com'è che dobbiamo fare?

_[immagine]_**  
Spreafico Paolo** 2:57:12  
Comunque che aveva qualche dato di qualità che abbiamo usato nell'esempio precedente, com'è che dobbiamo fare?

_[immagine]_**  
Emanuele Merlo** 2:57:19  
Cioè vogliamo aprire quel process per l'ordine vecchio?

_[immagine]_**  
Spreafico Paolo** 2:57:19  
Cioè vogliamo aprire quel process per l'ordine vecchio?

_[immagine]_**  
Emanuele Merlo** 2:57:24  
Per l'ordine vecchio, caso facile.

_[immagine]_**  
Spreafico Paolo** 2:57:26  
Caso facile.

_[immagine]_**  
Emanuele Merlo** 2:57:29  
Ho questo ordine vuoto.

_[immagine]_**  
Spreafico Paolo** 2:57:29  
Ho questo ordine vuoto.

_[immagine]_**  
Emanuele Merlo** 2:57:32  
Sono stupido.

_[immagine]_**  
Spreafico Paolo** 2:57:33  
Sono stupido.

_[immagine]_**  
Emanuele Merlo** 2:57:35  
Cosa faccio per ricordarmi che i controlli abbiamo fatto prima dell'altro? Quello precedente è andato giusto, questo qua non siete mai. Come faccio? Apro, vado a prendermi l'ordine di produzione vecchio, mi prendo il numerello.

_[immagine]_**  
Spreafico Paolo** 2:57:35  
Cosa faccio per ricordarmi che controlli avevo fatto prima dell'altro routing? Quello precedente è andato giusto, questo qua mi è uscito male. Come faccio? Apro, vado a prendermi l'ordine di produzione vecchio, mi prendo il numerello del routing.

_[immagine]_**  
Emanuele Merlo** 2:57:52  
Primario del ciclo vecchio.

_[immagine]_**  
Spreafico Paolo** 2:57:52  
Quel numerello del ciclo vecchio.

_[immagine]_**  
Emanuele Merlo** 2:57:55  
Lo apro, vado a cercare nella stessa pagina, entro nell'operation, entro nell'operation e ritrovo la lista dei controlli. Facciamo subito velocissimo, così mi rimane un pezzo. Posso duplicare la pagina, quindi posso avere 2 2 fogli.

_[immagine]_**  
Spreafico Paolo** 2:57:55  
Lo apro, vado a cercarmi la stessa pagina, entro nell'operation e mi trovo la lista dei controlli fatti.  
Posso duplicare la pagina, quindi posso avere 2 2 fogli di Internet Explorer con due pagine diverse, quindi posso fare copia e incolla, quindi torniamo indietro nella Repetit, prendiamo l'ordine.

_[immagine]_**  
Emanuele Merlo** 2:58:12  
Internet Explorer con due pagine diverse, quindi posso fare copia e ricorda OK, quindi torniamo indietro nella Repentiting, prendiamo l'ordine vecchio precedente, questo era avevamo completato i pezzi.

_[immagine]_**  
Spreafico Paolo** 2:58:23  
Vecchio precedente questo che era che avevamo completato i pezzi, quindi l'order ID copialo.

_[immagine]_**  
Emanuele Merlo** 2:58:28  
Prendi lo devi copiarlo, lo puoi comprare da lì.  
Poi dov'è? In che pagina andiamo per vedere che qual è il suo, il suo, il suo routing? No, negli ordini abbiamo preso questo, dobbiamo andare nell'elenco degli.

_[immagine]_**  
Spreafico Paolo** 2:58:33  
Poi dov'è che in che pagina andiamo per vedere che qual è il suo, il suo, il suo routing? No, negli ordini abbiamo preso questo, dobbiamo andare nell'elenco degli.  
Word order, poi abbiamo preso questo OK.

_[immagine]_**  
Emanuele Merlo** 2:58:51  
Filtri e poi nel dettaglio qua forse lo puoi aggiungere, prova ad aggiungerlo qua queste qua e poi aggiungere direttamente process.  
E questo qui avrà ovviamente la data di qualità. Ce la rappresenti perché li abbiamo visti, no? Adesso li confrontiamo.

_[immagine]_**  
Spreafico Paolo** 2:59:03  
E questo qui avrà ovviamente la i dati di qualità ce li avrà presenti perché li avevamo visti, no? Tanto li confrontiamo.

_[immagine]_**  
Emanuele Merlo** 2:59:13  
Quindi in soldoni, voi potete prendere un ordine con problemi, un ordine che non aveva problemi e copiare o aggiungere specifici controlli su ordini puntuali.

_[immagine]_**  
Spreafico Paolo** 2:59:13  
Quindi in soldoni voi potete prendere un ordine con problemi, un ordine che non aveva problemi e copiare o aggiungere specifici controlli su ordini puntuali.

_[immagine]_**  
Emanuele Merlo** 2:59:29  
Esempio, la Denise ha trovato la densità battuta che non controlla mai su quel lotto specifico, vuole fare dei controlli aggiuntivi sulla densità battuta sull'Italia.

_[immagine]_**  
Spreafico Paolo** 2:59:29  
Esempio, la Denise ha trovato la densità battuta che non controlla mai su quel lotto specifico vuole fare dei controlli aggiuntivi sulla densità battuta sto aumentando ovviamente prendo il controllo densità battuta, lo inserisco su quell'ordine lì.

_[immagine]_**  
Emanuele Merlo** 2:59:40  
Prendo il controllo di densità battuta, lo inserisco su quell'ordine lì.  
Ma è valido solo per quell'ordine. Perché? Perché non ho toccato il master. Quindi il successivo ordine, la densità battuta non sarà riportata perché non è configurata nel master perfetto. Possiamo vederlo qua.

_[immagine]_**  
Spreafico Paolo** 2:59:45  
Ma è valido solo per quell'ordine. Perché? Perché non ho toccato il master, quindi il successivo ordine, la densità battuta non sarà riportata perché non è configurata nel master.

_[immagine]_**  
Emanuele Merlo** 3:00:02  
Non so se uno di voi vuole aggiungere, allora fate così, entrate lì dentro e aggiunge uno di voi. Se aggiunge anche queste queste prime tre, se queste prime tre le aggiunge così, poi noi le dobbiamo refresciate, potete farlo uno di voi.

_[immagine]_**  
Spreafico Paolo** 3:00:05  
Allora fate così, entrate lì dentro e aggiunge uno di voi. Se aggiunge anche queste queste prime tre, se queste prime tre le aggiunge così, poi non le vediamo refreshate, potete farlo uno di voi.

_[immagine]_**  
Emanuele Merlo** 3:00:19  
Se no lo so.

_[immagine]_**  
Spreafico Paolo** 3:00:21  
Fate ragazzi, allora in soldoni, noi abbiamo due modalità.

_[immagine]_**  
Emanuele Merlo** 3:00:23  
OOO potete farlo tutti e ne vediamo 200 allora in soldoni noi abbiamo due modalità.  
Modalità facile, andiamo a lavorare sul master.

_[immagine]_**  
Spreafico Paolo** 3:00:32  
Modalità facile, andiamo a lavorare sul master.

_[immagine]_**  
Emanuele Merlo** 3:00:37  
Con il master tutti i successivi ordini prenderanno questa configurazione.

_[immagine]_**  
Spreafico Paolo** 3:00:37  
Con il master tutti i successivi ordini prenderanno questa configurazione.  
Come.  
No, è corretto. No, aspetta tutti i scusami Paolo, tutti i master di quello specifico routing, di quello specifico codice e quello specifico routing.

_[immagine]_**  
Emanuele Merlo** 3:00:48  
Quindi allora dovete andare nella pagina.

_[immagine]_**  
Spreafico Paolo** 3:01:02  
Devo fare dei controlli specifici su un lotto, prendo e aggiungo i controlli su quello specifico lotto.

_[immagine]_**  
Emanuele Merlo** 3:01:07  
Il numero.  
Quello cerca 9528.

_[immagine]_**  
Spreafico Paolo** 3:01:15  
528\.

_[immagine]_**  
Emanuele Merlo** 3:01:21  
Ciao.

_[immagine]_**  
Spreafico Paolo** 3:01:22  
Sto.

_[immagine]_**  
Emanuele Merlo** 3:01:27  
A dopo lo Apri.

_[immagine]_**  
Spreafico Paolo** 3:01:28  
Lo Apri.

_[immagine]_**  
Emanuele Merlo** 3:01:30  
E sono sempre obbligato a cercarli.

_[immagine]_**  
Spreafico Paolo** 3:01:34  
Allora?  
Questo ve lo sto facendo far vedere la parte tra virgolette per fixare c'è un report di Power BI dove dato il codice lui ti tira fuori direttamente i numeri dei routing da andare a colpire.

_[immagine]_**  
Emanuele Merlo** 3:01:51  
Questo qua è 29531.

_[immagine]_**  
Spreafico Paolo** 3:01:53  
E qua invece ragioni sempre per routing, ti do un report apposta per cui.  
Su Bob ti do un report dove tu gli dai il codice, lui ti dice guarda che su per questo codice ho questi 5 routing.  
Queste 5 box quindi tu puoi entrare al non vi non vi ho ancora attivato sui report.

_[immagine]_**  
Emanuele Merlo** 3:02:24  
Ciclo.

_[immagine]_**  
Spreafico Paolo** 3:02:37  
Sì, se ti prendi questo qua.

_[immagine]_**  
Emanuele Merlo** 3:02:44  
Se tu fai refresh mi vedi quelle inserite OK, adesso vi faccio una domanda che l'ha già spiegato Paolo.

_[immagine]_**  
Spreafico Paolo** 3:02:55  
Adesso vi faccio una domanda che ha già spiegato Paolo, noi qui.

_[immagine]_**  
Emanuele Merlo** 3:03:00  
Noi qui.  
Apri operation, vai form.  
OK, adesso ce n'è una secondo voi se torniamo nella pagina operatore Repetitive vedremo di questo ordine qua col materiale 3383738 così con questo materiale qui vediamo.

_[immagine]_**  
Spreafico Paolo** 3:03:10  
OK, adesso ce n'è una, secondo voi se torniamo nella pagina operatore Reperitive vedremo in quest'ordine qua col materiale 338373833 con questo materiale qui vediamo.

_[immagine]_**  
Emanuele Merlo** 3:03:25  
Quelli Station tre o no? Cerco questa nuova questa estensione sì. Qualcuno dice tutti dite sì, qualcuno dice no.

_[immagine]_**  
Spreafico Paolo** 3:03:26  
Per dispension plan o no? E cioè con questa nuova questa iscrizione sì, qualcuno dice tutti dice sì, qualcuno dice no.

_[immagine]_**  
Emanuele Merlo** 3:03:38  
Scusa, ripeti la domanda, siamo andati qua nel master e abbiamo aggiunto una operation. OK, la domanda è, se non ritorniamo nel di cui siamo partiti, quello con l'altro materiale, il materiale 3 8 e lo apriamo?

_[immagine]_**  
Spreafico Paolo** 3:03:38  
Scusa, ripeti la domanda. Siamo andati qua nel master e abbiamo aggiunto una operation. La domanda è se non ritorniamo nel code di cui siamo partiti, quello con l'altro materiale materiale 3 8 e lo apriamo.  
Vedremo che c'è questa iscrizione mandatoria, perché no risposta giusta perché non lo vedo.

_[immagine]_**  
Emanuele Merlo** 3:04:06  
Ecco, adesso vediamo questa cosa qui, no, questo concetto qua del master e del work order no, noi abbiamo abbiamo cambiato il master che è una cosa fondamentale perché scaricando da SAP.

_[immagine]_**  
Spreafico Paolo** 3:04:07  
Ecco, adesso vediamo questa cosa qui. No, questo concetto qua del master e del workholder no, noi abbiamo abbiamo cambiato il master che è una cosa fondamentale perché scaricando la SAP.  
Lo stesso ordine o un'altro ordine? Allora vedrai l'effetto no che fa. Però magari quell'ordine lì è già a una fase iniziata e non puoi ricrearlo da Sandro, no? In quel caso lì questa operazione va fatta non su master, quindi non nella Bo.

_[immagine]_**  
Emanuele Merlo** 3:04:23  
Lo stesso ordine o un'altro ordine? Allora vedrai l'effetto no che fanno. Però magari quell'ordine lì è già ha già una fase iniziata e non puoi ricrearli da SAP no? In quel caso lì questa operazione va fatta non sul master, quindi non nella Bot.  
Ma nel no. Quindi se tu Apri, ma non lo vedono gli altri.

_[immagine]_**  
Spreafico Paolo** 3:04:42  
Ma nel workholder no, quindi se tu Apri il workholder ema collegati in riunione.

_[immagine]_**  
Emanuele Merlo** 3:04:55  
Come vuoi, dai, facciamolo noi, tanto comunque l'importante è capire il meccanismo, allora entra nel nuovo code.

_[immagine]_**  
Spreafico Paolo** 3:04:56  
Come vuoi, dai.

_[immagine]_**  
Emanuele Merlo** 3:05:03  
Magari tocca lo stesso, così questo è quello che ce li aveva. Aspetta un attimo, questo è quello che ce li aveva, questo è quello che non ce li aveva. OK, vedi che qua non c'è nessun triangolo arancione, quindi è rimasto vuoto, perfetto, come avevate detto voi.

_[immagine]_**  
Spreafico Paolo** 3:05:04  
Magari copia lo stesso così tanto fai vedere che non c'è, fai vedere che non c'è, ma tanto Apri quello e fai vedere che non ce l'aveva. OK, vedi che qua non c'è nessun triangolo arancione non c'è, quindi è rimasto vuoto. Perfetto, come l'avevate detto voi.

_[immagine]_**  
Emanuele Merlo** 3:05:21  
Adesso torniamo nel torniamo questa volta non andiamo nel nella Bot ma andiamo nel workcode direttamente. Calcolate che il workcode è un esempio, un'istanza.

_[immagine]_**  
Spreafico Paolo** 3:05:21  
Adesso torniamo nel torniamo questa volta non andiamo nel nella Bot, ma andiamo nel workorder direttamente. Calcolate che il workorder è un esempio, un'istanza.

_[immagine]_**  
Emanuele Merlo** 3:05:37  
Con uno startup, una certa di della di quello che era la BOP no. Quindi anche l'interfaccia è similissima no se tu Apri Word code.

_[immagine]_**  
Spreafico Paolo** 3:05:37  
Con uno startup, una certa quantity di della di quello che era la DOP no, quindi anche l'interfaccia è similissima no se tu Apri wordcode.

_[immagine]_**  
Emanuele Merlo** 3:05:49  
Avrà di nuovo anche lui a value Operations, value Operations. L'operation sarà la stessa perché questa qua è stata creata da call master, no? Quindi è uguale identico.

_[immagine]_**  
Spreafico Paolo** 3:05:50  
Avrà di nuovo anche lui aveva operations, operations. L'operation sarà la stessa perché questa qua è stata creata da quel master, no? Quindi è uguale, identico.

_[immagine]_**  
Emanuele Merlo** 3:06:01  
Avrà.

_[immagine]_**  
Spreafico Paolo** 3:06:02  
Va.

_[immagine]_**  
Emanuele Merlo** 3:06:03  
Ma va le sue cose, no le sue.

_[immagine]_**  
Spreafico Paolo** 3:06:04  
Ma guarda le sue cose, no le sue.

_[immagine]_**  
Emanuele Merlo** 3:06:08  
Le sue quality inspection che saranno vuote in questo caso, come le abbiamo viste e qui dobbiamo fare lo stesso lavoro che abbiamo fatto allora facile, abbiamo sistemato il master.

_[immagine]_**  
Spreafico Paolo** 3:06:08  
Le sue quality inspection che saranno vuote in questo caso, che non le abbiamo viste e qui ce la facciamo a fare perché abbiamo fatto allora facile, abbiamo sistemato il master.  
Da qui in avanti tutti gli ordini andranno.

_[immagine]_**  
Emanuele Merlo** 3:06:26  
Da qui in avanti andranno.

_[immagine]_**  
Spreafico Paolo** 3:06:32  
Pato.

_[immagine]_**  
Emanuele Merlo** 3:06:34  
Hai ragione, sì, è la stessa cosa. Comunque questo è il master quality inspections.

_[immagine]_**  
Spreafico Paolo** 3:06:36  
Sì, è la stessa cosa.  
Sag

_[immagine]_**  
Emanuele Merlo** 3:06:42  
Fai proprio, aspetta che devo salvare sennò poi me lo perdo.

_[immagine]_**  
Spreafico Paolo** 3:06:43  
Esatto, possiamo vederlo partendo dalla pagina BOP in cui cerchiamo il BOP.

_[immagine]_**  
Emanuele Merlo** 3:06:56  
Allora?  
Partiamo proprio dall'inizio, qua si può cercare, cerchiamo Bot che è questo qua. Adesso noi sappiamo qual è il processo perché l'abbiamo copiato da quel wordcode, quindi copio l'identificativo del ciclo.

_[immagine]_**  
Spreafico Paolo** 3:07:14  
Torre del cibo.

_[immagine]_**  
Emanuele Merlo** 3:07:17  
Lo apro.

_[immagine]_**  
Spreafico Paolo** 3:07:17  
Lo apro.

_[immagine]_**  
Emanuele Merlo** 3:07:20  
Questo poi andiamo nelle operazioni, questo qua è monofase cosiddetto, quindi ha solo una fase, quindi ha solo un gruppo di iscrizioni per quella fase.

_[immagine]_**  
Spreafico Paolo** 3:07:21  
Dai, poi andiamo nelle operazioni, questo qua è monofase cosiddetto, quindi ha solo una fase, quindi ha solo un gruppo di iscrizioni per quella fase.

_[immagine]_**  
Emanuele Merlo** 3:07:31  
Che erano vuote, ma noi da quel computer voi non avete visto ma abbiamo fatto aggiunto 1 1 no dato di qualità veramente.

_[immagine]_**  
Spreafico Paolo** 3:07:31  
Erano vuote, ma noi da quel computer voi non avete visto ma abbiamo fatto aggiunto 1 1 quality inspection no, un dato di qualità veramente.

_[immagine]_**  
Emanuele Merlo** 3:07:43  
Apriamo l'operazione, sono in questa parte che non viene visualizzata, bisogna cliccare su more più.

_[immagine]_**  
Spreafico Paolo** 3:07:44  
È un'operazione, sono in formo, piuttosto sono ultime, OK, più.

_[immagine]_**  
Emanuele Merlo** 3:07:56  
Qui facciamo il link, verrà fuori l'elenco che puoi filtrare di tutte, di tutte le quality session sono migliaia perché sono state inserite tutte a sistema, quindi sono tantissime, però qua si possono filtrare quindi.

_[immagine]_**  
Spreafico Paolo** 3:07:56  
Qui facciamo il link, verrà fuori l'elenco che puoi filtrare di tutte, di tutte le sono migliaia perché sono state inserite tutte a sistema, quindi sono tantissime, però qua si possono filtrare quindi.

_[immagine]_**  
Emanuele Merlo** 3:08:13  
Voi il codice è rimasto lo stesso del sistema precedente, no? Quindi sapete che quella quality, cioè che quel codice di ispezione è rimasto lo stesso, no? Quindi potete filtrarlo e riprenderlo.

_[immagine]_**  
Spreafico Paolo** 3:08:13  
Voi il codice è rimasto lo stesso del sistema precedente, no? Quindi sapete che quella quality, cioè che quel codice di ispezione è rimasto lo stesso, no? Quindi potete filtrarlo e riprenderlo.

_[immagine]_**  
Emanuele Merlo** 3:08:29  
In questo caso il washing com'è che si chiama il quello conformità?

_[immagine]_**  
Spreafico Paolo** 3:08:29  
Beh, in questo caso il washing poteva il com'è che si chiama il.  
Claudio, cosa cosa controlli nel washing?  
C'è tipo un controllo attrezzature no per il benestare del washing.

_[immagine]_**  
Emanuele Merlo** 3:08:43  
Dopo pressione OK, pressione cerca pressione.

_[immagine]_**  
Spreafico Paolo** 3:08:50  
OK, pressione.

_[immagine]_**  
Emanuele Merlo** 3:08:54  
No, forse è meglio che allora andiamo nel codice dell'espression che magari è nella description. Vai Apri. Allora qui entriamo nell'altra pagina, c'è 1 1 delle 1000 pagine della basic è quella che fa vedere l'anagrafica di tutte le ispezioni, OK.

_[immagine]_**  
Spreafico Paolo** 3:08:55  
Forse è meglio che allora andiamo nel codice delle che magari è nella description, è nella description, una delle 1000 pagine della basic è quella che fa vedere da.  
Aspetta un secondo Paolo, perché sennò ci perdiamo. Allora qui avete la lista della spesa di tutte le ispezioni vita Natural durante.

_[immagine]_**  
Emanuele Merlo** 3:09:15  
Aspetta un secondo Paolo, perché se non ci perdiamo, allora qui avete la lista di tutte le spese di vita Natural durante.  
Le prendete quelle che vi servono e le trascinate all'interno. Sì, prendo la prima.

_[immagine]_**  
Spreafico Paolo** 3:09:23  
Le prendete quelle che vi servono e le trascinate all'interno.  
Prendine una, quella che ti piace per Emanuele.

_[immagine]_**  
Emanuele Merlo** 3:09:34  
E schiacciate link, schiacciando link, lui prende e ha inserito il secondo quadratino, così abbiamo sistemato il master.

_[immagine]_**  
Spreafico Paolo** 3:09:34  
E schiacciate link schiacciando link lui prende e ha inserito il secondo quadratino, così abbiamo sistemato il master.  
OK, il sistema sa.

_[immagine]_**  
Emanuele Merlo** 3:09:46  
Tutta la parte di limiti eccetera deve essere dentro di là. Aspetta, abbiamo già presente la caratteristica con i relativi limiti, quindi prendo ho già qualcosa di preconfezionato e la inserisco.

_[immagine]_**  
Spreafico Paolo** 3:09:52  
Dimenticatelo un attimo aspetta, abbiamo già presente la caratteristica con il con i relativi limiti quindi prendo ho già qualcosa di preconfezionato e la inserisco caso facile.

_[immagine]_**  
Emanuele Merlo** 3:10:05  
Caso facile, partiamo da parti facile, che se non ci perdiamo.

_[immagine]_**  
Spreafico Paolo** 3:10:06  
Partiamo dalle parti falsi, perché se no ci perdiamo.

_[immagine]_**  
Emanuele Merlo** 3:10:09  
Ho sistemato il master facendo questo link.

_[immagine]_**  
Spreafico Paolo** 3:10:09  
Ho sistemato il master facendo questo link.

_[immagine]_**  
Emanuele Merlo** 3:10:13  
Stesso medesimo processo, come l'abbiamo fatto qui, lo rifacciamo sull'ordine di produzione, quindi apriamo il nostro ordine di produzione che abbiamo creato.

_[immagine]_**  
Spreafico Paolo** 3:10:13  
Stesso medesimo processo, come l'abbiamo fatto qui, lo rifacciamo sull'ordine di produzione, quindi apriamo il nostro ordine di produzione che abbiamo canato.

_[immagine]_**  
Emanuele Merlo** 3:10:25  
E andiamo nella fase che ci serve come prima.

_[immagine]_**  
Spreafico Paolo** 3:10:25  
E andiamo nella fase che ci serve come prima.

_[immagine]_**  
Emanuele Merlo** 3:10:30  
Sì, beh, comunque adesso vai direttamente così, vai fuori direttamente, vai.

_[immagine]_**  
Spreafico Paolo** 3:10:34  
Vai fuori direttamente.

_[immagine]_**  
Emanuele Merlo** 3:10:38  
Come prima abbiamo la stessa medesima schermata, andiamo sui dati qualità e andiamo a inserire quei controlli.

_[immagine]_**  
Spreafico Paolo** 3:10:38  
Come prima abbiamo la stessa medesima schermata, andiamo sui dati qualità e andiamo a inserire quei controlli.

_[immagine]_**  
Emanuele Merlo** 3:10:48  
Che abbiamo inserito nel master. Quindi dobbiamo fare il lavoro due volte. Perché? Perché durante la generazione del dell'ordine.

_[immagine]_**  
Spreafico Paolo** 3:10:49  
Che abbiamo inserito nel master, quindi dobbiamo fare il lavoro due volte. Perché? Perché durante la generazione del dell'ordine.

_[immagine]_**  
Emanuele Merlo** 3:10:59  
Non avendo trovato i controlli originali, lui non me li ha importati.

_[immagine]_**  
Spreafico Paolo** 3:10:59  
Non avendo trovato i controlli originali, lui non me li ha importati.

_[immagine]_**  
Emanuele Merlo** 3:11:06  
Quindi dobbiamo modificare questo ordine.

_[immagine]_**  
Spreafico Paolo** 3:11:06  
Quindi dobbiamo bonificare questo ordine.

_[immagine]_**  
Emanuele Merlo** 3:11:13  
Spero che sia casi più unici che rari, spero che sennò abbiamo un'altro tipo di problema.

_[immagine]_**  
Spreafico Paolo** 3:11:13  
Spero che sia casi più unici che rari, spero che sennò abbiamo un'altro tipo di problema.

_[immagine]_**  
Emanuele Merlo** 3:11:23  
Quindi anche qui entro nella stessa medesima schermata, vedete che in alto c'è scritto operazione numero 10 relativo a questo ordine, non c'è più scritto relativo a questo routing. Prendo e butto dentro quello che mi serve come prima Paolo, quello che ti piace.

_[immagine]_**  
Spreafico Paolo** 3:11:23  
Quindi anche qui entro nella stessa medesima schermata, vedete che in alto c'è scritto operazione numero 10 relativo a questo ordine, non c'è più scritto relativo a questo routing prendo.  
E butto dentro quello che mi serve, come prima Paolo, prendi quello che ti piace di più.

_[immagine]_**  
Emanuele Merlo** 3:11:45  
Quindi è un modo per fixare.

_[immagine]_**  
Spreafico Paolo** 3:11:46  
Quindi è un modo per fixare.

_[immagine]_**  
Emanuele Merlo** 3:11:50  
Cosa è stato rilasciato senza ordini? Ve lo spiego perché, perché sono già dove abbiamo caricato e in linea non era pazzo il \*\*\*\*\*, quindi alla più disperata.

_[immagine]_**  
Spreafico Paolo** 3:11:50  
Cosa è stato rilasciato senza ordini? Ve lo spiego perché. Perché sono già reduce da Ostrava dove abbiamo caricato e in linea non è apparso un \*\*\*\*\*, quindi alla più disperata.

_[immagine]_**  
Emanuele Merlo** 3:12:06  
Vediamo di sistemarlo nel mentre sistemiamo l'anagrafica ordini di partenza saranno veramente pochi, quindi dovrebbe riuscire a sanare le cose.

_[immagine]_**  
Spreafico Paolo** 3:12:06  
Vediamo di sistemarlo nel momento che sistemiamo le anagrafiche ordini di partenza saranno veramente pochi, quindi dovremmo riuscire a sanare le cose.

_[immagine]_**  
Emanuele Merlo** 3:12:17  
Prima che succedano.

_[immagine]_**  
Spreafico Paolo** 3:12:17  
Prima che succedano.

_[immagine]_**  
Emanuele Merlo** 3:12:20  
Questo è il nostro paracadute. Se ce l'avete il work order update, se rimando a SAP l'ordine che non lo sappiamo.

_[immagine]_**  
Spreafico Paolo** 3:12:20  
Questo è il nostro paracadute.  
Non è roba nostra, noi non lo sappiamo.

_[immagine]_**  
Emanuele Merlo** 3:12:33  
Dovrebbe farlo in teoria, però noi come qualità non lo sappiamo. Adesso riapro il work order che avevamo prima e dobbiamo verificare che ci sia e ritorniamo allo storyboard.

_[immagine]_**  
Spreafico Paolo** 3:12:35  
Noi come qualità non lo sappiamo.  
No, non hai capito, è bloccato, è bloccato così c'è sotto il default perché ti dice chiama la mamma.

_[immagine]_**  
Emanuele Merlo** 3:12:49  
Allora io ho visto che.  
C'è un'altro concetto lì, allora se quella fase lì è stata marcata come critica, allora e in una ci sarà, diciamo ci sarà una, cioè in una ci sarà un'expression definition di default che verrà inserita.

_[immagine]_**  
Spreafico Paolo** 3:13:03  
C'è un'altro concetto di allora, se quella fase lì è stata marcata come critica, allora e in una ci sarà, diciamo ci sarà una, cioè in una ci sarà una definition di default che verrà inserita.

_[immagine]_**  
Emanuele Merlo** 3:13:20  
Direttamente e sarà comunque bloccante, ti dice chiama il quality manager per farmi aggiungere le altre cose, le altre stage.

_[immagine]_**  
Spreafico Paolo** 3:13:20  
Direttamente e sarà comunque bloccante, ti dice chiama il quality manager per farmi aggiungere le.

_[immagine]_**  
Emanuele Merlo** 3:13:29  
Quindi allora qui ho visto, avete visto che è un po' difficile, no? Trovare qual è la giusta? No, perché erano quei codici, il filtro funzionava soltanto sul code, sul codice. E lui ha fatto un'altra domanda, ma.

_[immagine]_**  
Spreafico Paolo** 3:13:30  
Quindi allora qui ho visto, avete visto che è un po' difficile, no? Trovare qual è la dispaction giusta? No, perché erano quei codici, il filtro funzionava soltanto su cod, su codice e quindi era un po'. E lui ha fatto anche la domanda, ma.  
Queste sezioni no, sai dov'è che arrivano eccetera. E quella lì diciamo sarebbe l'ultima parte è quella di engineering, no, quello specifico di.

_[immagine]_**  
Emanuele Merlo** 3:13:47  
Le funzioni, no, dov'è che arrivano eccetera. E quella lì, diciamo, sarebbe l'ultima parte, quella di Engineering, no, di no. Allora programming vocale.

_[immagine]_**  
Spreafico Paolo** 3:14:01  
Secondo voi questa parte, questa parte di definire queste carte, definire il tipo di spedizione e poi di associarla al master dove verrà fatta secondo voi?

_[immagine]_**  
Emanuele Merlo** 3:14:02  
Secondo voi questa parte, questa parte diciamo di definire queste caratteristiche, definire il tipo di sezione e poi di associarla al master dove verrà fatta secondo voi?

_[immagine]_**  
Spreafico Paolo** 3:14:17  
Da che pagina verrà fatta è una cosa dei messi, innanzitutto.

_[immagine]_**  
Emanuele Merlo** 3:14:17  
Da che pagina doveva fare? Era quello del mess innanzitutto.  
O viene la SAP è una cosa del MES? No, è una cosa interna al MES che i dati sono stati importati in modo massivo da degli Excel e quindi avremo una pagina particolare allora.

_[immagine]_**  
Spreafico Paolo** 3:14:22  
O viene già fatto?  
È una cosa del MES? No, è una cosa interna al MES e i dati sono stati importati in modo massivo da degli Excel e quindi abbiamo una pagina particolare, allora quelle che basavamo lì dal work master e dal work order.

_[immagine]_**  
Emanuele Merlo** 3:14:37  
Quelle che basavamo lì dal workmaster e dal workholder sono nella cosa che si chiama dispatch and Definition, quindi sarà una pagina dispatch and Definition.

_[immagine]_**  
Spreafico Paolo** 3:14:42  
Sono nella cosa che si chiama Studio Definition.  
Beh, dispaction order è un'altra cosa, perché a volte ci cioè il sistema consentirebbe anche di creare degli ordini veri e propri descrizioni, ma consente anche invece questo link che noi che invece ha utilizzato.

_[immagine]_**  
Emanuele Merlo** 3:14:53  
Dispation order è un'altra cosa, perché a volte ci cioè il sistema consentirebbe anche di creare degli ordini veri e propri descrizioni con delle fave descrizioni, ma consente anche invece questo link che noi che Brenda invece ha utilizzato il link.

_[immagine]_**  
Spreafico Paolo** 3:15:09  
Che invece è molto più la grafica completa, no? Se tu strolli dice che saranno no.

_[immagine]_**  
Emanuele Merlo** 3:15:09  
Allora qui vedete che invece è molto più l'anagrafica completa, no? Se tu scordi ti diceva che saranno migliaia, no, se tu no, se le carica progressivamente.  
Scusa sì, sono tantissimi, no? Qui cosa c'è di positivo che dovesse essere capace con questo filtro di filtrare anche per nome? No. Quindi cerchiamo la pressione che dice che dicevamo prima, no, il washing è una delle.

_[immagine]_**  
Spreafico Paolo** 3:15:27  
Sono tantissime, no? Qui cosa c'è di positivo che dovesse essere capace con questo filtro di filtrarle anche per nome? No. Quindi cerchiamo la pressione che dicevamo prima, no, in Washington una delle una delle sezioni a vedere se la pressione era.

_[immagine]_**  
Emanuele Merlo** 3:15:42  
Una delle ispezioni a vedere se la pressione era al livello giusto, no?

_[immagine]_**  
Spreafico Paolo** 3:15:45  
A livello giusto, no?

_[immagine]_**  
Emanuele Merlo** 3:15:48  
Quindi questione.

_[immagine]_**  
Spreafico Paolo** 3:15:48  
Quindi pressione.  
Guarda se lo vedo adesso a fargli vedere come si apre il filtro.

_[immagine]_**  
Emanuele Merlo** 3:15:51  
Gli ho detto, adesso gli ho aggiunto un filtro.  
Il filtro, questo imbuto qua in alto, è lo stesso filtro che avete usato l'altra volta.

_[immagine]_**  
Spreafico Paolo** 3:15:58  
Però se filtri qua filtri by ID è lo stesso filtro che avete usato l'altra volta che se cerchi press non trova niente scrivici un attimo press, ma vedrai che non mi viene dai OK vai.

_[immagine]_**  
Emanuele Merlo** 3:16:14  
Invece cambiando il campo che cerchi per un campo descrizione eccetera dovresti trovarlo no quindi io qua ho fatto aggiungi posso rispetto a questo filtro qua che permette solo di la ricerca solo in un campo qua.

_[immagine]_**  
Spreafico Paolo** 3:16:15  
E invece cambiando il campo che cerchi per un campo di iscrizione, per un diciamo discrittivo con un nome, distinction eccetera dovresti trovarlo, no? Quindi io qua ho fatto aggiungi posso rispetto a questo filtro qua che permette solo.  
La ricerca su ogni campo qua mi permette di facilitare a me quale campo, su quale campo cercare. Di solito è meglio usare la voce operatore contiene in modo da non dover mettere proprio addosso. Sì, quello lì è non è case case sensitive, quindi potete scrivere.

_[immagine]_**  
Emanuele Merlo** 3:16:32  
Mi permette di specificare a me quale campo, quale su quale campo cercare? Di solito è bene usare l'operatore contiene in modo da non dover mettere proprio.  
E qui avete tutte queste ispezioni sulla pressione OK, quindi vediamo se con che ispezione è una.

_[immagine]_**  
Spreafico Paolo** 3:16:52  
Qui avete tutte queste estensioni, quindi vediamo se che estensione è una.

_[immagine]_**  
Emanuele Merlo** 3:17:03  
Sì, per poter scrivere pressione, magari così ti vieni fuori. L'ho scritto giusto, non ci leggo, scusami, è sfocatissimo.

_[immagine]_**  
Spreafico Paolo** 3:17:03  
E per descrivere pressione, magari così veniva fuori, sì.

_[immagine]_**  
Emanuele Merlo** 3:17:19  
Adesso che voi sapete no, magari quella quale di queste riguarda il wash, quali di queste riguarda il washing e quindi potete vedere allora cos'è, cioè brevemente, cioè?

_[immagine]_**  
Spreafico Paolo** 3:17:20  
E voi sapete, no, magari quella quale di queste riguarda il washing, quale di queste riguarda il washing?

_[immagine]_**  
Emanuele Merlo** 3:17:34  
Cos'è l'expression Definition? Una definizione di dispersione, appunto, è quella cosa che crea il controllo una volta linkata al work order, no linkata work order, ripetiamo, o linkata tramite il master e quindi ereditata quando viene riportato.

_[immagine]_**  
Spreafico Paolo** 3:17:34  
Cos'è un extension Definition? Una definizione di ispezione, appunto. È quella cosa che crea il controllo una volta linkata no linkata, ripetiamo o linkata tramite wordcam per il master e quindi ereditata quando viene portato.  
O che si tratta manualmente di una realizzazione in cui diciamo in quegli ordini che difettosi che erano già sistemi, OK?

_[immagine]_**  
Emanuele Merlo** 3:17:52  
Oppure usata manualmente, come abbiamo visto prima, nel caso in cui diciamo in quegli ordini che difettuosi che cos'è un Definition? Un Definition è come e quando.

_[immagine]_**  
Spreafico Paolo** 3:18:02  
Com'è un sketch definition è come e quando controllare che un pezzo abbia una certa caratteristica, quindi come da questa definizione vedete che.

_[immagine]_**  
Emanuele Merlo** 3:18:07  
Controllare che un pezzo abbia una certa caratteristica, quindi come da questa definizione vedete che l'ispezione dipende da un'altra entità che è la caratteristica no?

_[immagine]_**  
Spreafico Paolo** 3:18:18  
L'iscrizione dipende da un'altra entità che è la caratteristica no, quindi un oggetto deve essere, quindi ci sarà un'altra anagrafica diversa da questa che definisce tutte le caratteristiche di qualità.

_[immagine]_**  
Emanuele Merlo** 3:18:23  
Quindi un oggetto deve essere quindi ci sarà un'altra grafica diversa da questa che definisce tutte le caratteristiche di qualità che deve avere un oggetto, quindi che possono essere la larghezza di un certo range.

_[immagine]_**  
Spreafico Paolo** 3:18:34  
Che deve avere un oggetto, quindi che possono essere la larghezza di un certo range, che possono essere la pressione a un certo livello, che possono essere il controllo di conformità di un certo tipo, no?

_[immagine]_**  
Emanuele Merlo** 3:18:41  
Che possono essere la pressione a un certo livello, che possono essere un controllo di conformità di un certo tipo, no? Quindi tornando di queste caratteristiche, dispaccio, cos'è che definisce?

_[immagine]_**  
Spreafico Paolo** 3:18:51  
Quindi, tornando di queste caratteristiche, cos'è che definisce che finisce quando parli, che allarga questa colonna?

_[immagine]_**  
Emanuele Merlo** 3:18:59  
Definisce quando farle dai che a questa allarga questa colonna.  
100% no, 100% significa all'inizio del dell'ordine, però potevo anche essere frequenza, frequenza di tempo AA quantità di prodotto no eccetera.

_[immagine]_**  
Spreafico Paolo** 3:19:10  
100% no, 100% significa all'inizio del dell'ordine, però potremmo anche essere frequenza, frequenza di tempo a quantità di prodotto no eccetera.

_[immagine]_**  
Emanuele Merlo** 3:19:26  
E poi definisce anche definisce anche la revision, il seleziona una, poi vai su Edit.

_[immagine]_**  
Spreafico Paolo** 3:19:27  
E poi definisce anche, definisce anche la Revision, il senza una forma su reddit.

_[immagine]_**  
Emanuele Merlo** 3:19:41  
Anche.

_[immagine]_**  
Spreafico Paolo** 3:19:41  
Anche.

_[immagine]_**  
Emanuele Merlo** 3:19:43  
Appunto, questo qua è la qualità, scendi giù.

_[immagine]_**  
Spreafico Paolo** 3:19:43  
Appunto, questa qua è la qualità, scendi giù.

_[immagine]_**  
Emanuele Merlo** 3:19:49  
Sì, poi cose, cose che appunto non usate. OK, ma principalmente definiscono quando l'ispezione, quando quella caratteristica va misurata, no. Adesso noi principalmente ce l'abbiamo tutte 100%, quindi sono tutte ispezioni mandatoli all'inizio dell'ordine, no?

_[immagine]_**  
Spreafico Paolo** 3:19:49  
Sì, quelle, quelle, quelle che appunto voi usate. OK, principalmente definiscono quando l'ispezione, quando quella caratteristica va misurata. No, adesso noi principalmente ce l'abbiamo tutte 100%, quindi sono tutte ispezioni mandatoli all'inizio dell'ordine, no?

_[immagine]_**  
Emanuele Merlo** 3:20:09  
Ma devo all'inizio dello shift.

_[immagine]_**  
Spreafico Paolo** 3:20:09  
Adeguati iniziative 5.

_[immagine]_**  
Emanuele Merlo** 3:20:12  
Entriamo a vedere questa caratteristica, magari seleziona proprio questa caratteristica pressione P code OK, quindi andiamo a vedere l'altra pagina di anagrafica che è quella delle caratteristiche perché sempre diciamo nello sterminato mondo delle pagine della basic.

_[immagine]_**  
Spreafico Paolo** 3:20:12  
Entriamo a vedere questa caratteristica, magari seleziona proprio questa caratteristica pressione P code OK, quindi andiamo a vedere l'altra pagina di anagrafica che è quella delle caratteristiche perché sempre diciamo nello sterminato mondo delle pagine della basic.

_[immagine]_**  
Emanuele Merlo** 3:20:30  
Questa è una data che si chiamerà characteristic, giusto?

_[immagine]_**  
Spreafico Paolo** 3:20:30  
Ci sarà un'altra che si chiamerà characteristic, ve la faccio facile qua definiamo la frequenza di controllo con cui vogliamo fare quella caratteristica, quella tipo di ispezione.

_[immagine]_**  
Emanuele Merlo** 3:20:36  
Ve la faccio facile, qua definiamo la frequenza di controllo con cui vogliamo fare quella caratteristica. Cos'era il tipo di iscrizione? Può essere a chiamata, quindi quando si attiva voglio farlo per avanti perché lavoravo lì.

_[immagine]_**  
Spreafico Paolo** 3:20:46  
Può essere a chiamata, quindi quando si attiva voglio farlo, verrà avanti perché la buona Denise ha rotto le palle in merito su tot numero di pezzi e tot numero di ore, quindi da quando dichiaro lo start dell'ordine devo fare certi controlli ogni due ore.

_[immagine]_**  
Emanuele Merlo** 3:20:55  
Merito su tot il numero di pesto e tot il numero di ore, quindi da quando dichiaro di far dell'ordine devo fare 7 controlli ogni due ore, quindi il sistema fa apparire quella caratteristica di controllo.

_[immagine]_**  
Spreafico Paolo** 3:21:05  
Il sistema farà apparire quella caratteristica di controllo.

_[immagine]_**  
Emanuele Merlo** 3:21:10  
Conosci tutti.

_[immagine]_**  
Spreafico Paolo** 3:21:10  
Conosci tutti.

_[immagine]_**  
Emanuele Merlo** 3:21:13  
Un controllo registrato è un controllo effettuato, quindi repetita iuvant, se non sbloccano i controlli effettuati non dichiarano.

_[immagine]_**  
Spreafico Paolo** 3:21:13  
Un controllo registrato è un controllo effettuato, quindi repetita iuvant, se non sbloccano i controlli effettuati non dichiarano.  
E qua Denise mi spara.

_[immagine]_**  
Emanuele Merlo** 3:21:25  
Mi spara.  
Quindi occhio.

_[immagine]_**  
Spreafico Paolo** 3:21:31  
Quindi occhio.

_[immagine]_**  
Emanuele Merlo** 3:21:33  
Le funzionalità le abbiamo.

_[immagine]_**  
Spreafico Paolo** 3:21:34  
Le funzionalità le abbiamo.

_[immagine]_**  
Emanuele Merlo** 3:21:37  
Se ci servono le usiamo, se non ci servono non le usiamo perché tutti i nostri impatti.

_[immagine]_**  
Spreafico Paolo** 3:21:37  
Se ci servono le usiamo, se non ci servono non usiamo perché tutti i nostri impatti.

_[immagine]_**  
Emanuele Merlo** 3:21:45  
Hanno effetto sulla produzione, se qualcuno dice voglio controllare ogni due ore il sistema, ogni due ore fa uscire il record e se non lo smalto non dichiarano ma ogni due ore da quando l'operatore si è loggato o da quando?

_[immagine]_**  
Spreafico Paolo** 3:21:45  
Hanno effetto sulla produzione, se qualcuno dice voglio controllare ogni due ore il sistema, ogni due ore fa uscire il record e se non smarcano il record non dichiarano ma ogni due ore da quando l'operatore si è loggato o da quando?

_[immagine]_**  
Emanuele Merlo** 3:22:01  
Ha chiamato lo Stato dell'ordine.

_[immagine]_**  
Spreafico Paolo** 3:22:01  
Ha chiamato lo start del esatto.

_[immagine]_**  
Emanuele Merlo** 3:22:06  
E viene fatto ovviamente tramite lo stesso pulsante no, cioè diventa quel pulsante arancione.

_[immagine]_**  
Spreafico Paolo** 3:22:09  
E lo stesso pulsante no, cioè diventa pulsante arancione.

_[immagine]_**  
Emanuele Merlo** 3:22:14  
Lo stesso pulsante poi brillerà diciamo e uno dovrà cliccarlo per fare poi se io avvio l'ordine non compilo l'ordine passano due ore e ce ne avrò due in fila, quindi dovrò compilarne due di seguito. Se sto lì 20 ore senza fare ce ne avrò 20 ore.

_[immagine]_**  
Spreafico Paolo** 3:22:14  
Lo stesso pulsante poi brillerà diciamo e non dovrà cliccarlo per fare poi se ci se io avvio l'ordine non compilo la mia produzione passan due ore ce ne avrò due in fila quindi dovrò compilarne due di seguito se sto lì 20 ore senza fare ce ne avrò 10 in gola.

_[immagine]_**  
Emanuele Merlo** 3:22:33  
Quindi aspetto con Mauro prima che arrivi, diventi ori sia dei polpiccini.

_[immagine]_**  
Spreafico Paolo** 3:22:33  
Io mi aspetto che Mauro, prima che arrivi di 20 ore, sia lì col fucile.

_[immagine]_**  
Emanuele Merlo** 3:22:38  
Sì.

_[immagine]_**  
Spreafico Paolo** 3:22:38  
Io.

_[immagine]_**  
Emanuele Merlo** 3:22:40  
Ma io dovrò metterli ogni volta che creo un nuovo ciclo di controllo barra in automatico le tre ore di vanno in default, non devo collegare come adesso prima.

_[immagine]_**  
Spreafico Paolo** 3:22:40  
E io dovrò metterle ogni volta che creo un nuovo ciclo di controllo barra in automatico le tre ore vanno in default.  
È per quello che ho detto prima. Caso semplice, ho già la caratteristica con quella frequenza già pronta nel mio archivio, la prendo la trascino adesso, adesso ci arriviamo.

_[immagine]_**  
Emanuele Merlo** 3:22:56  
Caso semplice, ho già la caratteristica con quella frequenza già pronta il mio io la prendo e la trascino possiamo vedere i casi in cui io non ho nessuna caratteristica.  
Vediamo se intanto le caratteristiche cosa sono.

_[immagine]_**  
Spreafico Paolo** 3:23:13  
Caratteristiche cosa sono, no?

_[immagine]_**  
Emanuele Merlo** 3:23:16  
Allora prendiamo prima la pressione, quella di prima, cioè una, cioè ogni ogni ispezione ha una caratteristica, OK, perché ispezione ha quella caratteristica, però ovviamente quindi possono essere cioè n ispezioni per la stessa caratteristica, no, perché poi io posso cambiare il tempo no, il modo no in cui vengo magari in una.

_[immagine]_**  
Spreafico Paolo** 3:23:16  
Allora devi aprire la pressione, quella di prima, cioè?  
La cioè ogni ogni ispezione ha una caratteristica, OK, perché l'ispezione ha quella caratteristica, però ovviamente quindi possono essere cioè n ispezioni per la stessa caratteristica no, perché poi io posso cambiare il tempo no, il modo no in cui vengo magari in all'inizio del corso.

_[immagine]_**  
Emanuele Merlo** 3:23:36  
All'inizio del la stessa magari caratteristica va misurata con 10, 10 pezzi o 10 pezzi e quindi creo due espressioni in una frequenza diversa della stessa caratteristica. OK, adesso invece qui.

_[immagine]_**  
Spreafico Paolo** 3:23:37  
All'inizio invece la stessa magari caratteristica va misurata con 101010 pezzi, quindi che due spezzoni di una frequenza diversa della stessa caratteristica. OK, adesso invece qui cos'è una?  
Una caratteristica può essere praticamente di tre tipi, ma noi ne usiamo solo 2, 1 qualche tipo variabile, quindi che ha una misura di una di una quantità fatta in una certa.

_[immagine]_**  
Emanuele Merlo** 3:24:07  
Da Todenax OK, quindi praticamente uno scalare no, quindi una larghezza, 1 1 altezza, una pressione, un tipo di oppure può essere di tipo qualitativo no?

_[immagine]_**  
Spreafico Paolo** 3:24:07  
C'è un'altezza, una pressione, un tipo di corpo, oppure può essere di tipo qualitativo, no?  
Una risposta sì o no è fatto in è abbastanza, è conforme a questi standard, è diciamo ha dei fatti estetici e queste cose qui vanno già uno si chiama variable e nell'altro si chiama.

_[immagine]_**  
Emanuele Merlo** 3:24:25  
Una risposta sì o no è fatto in è abbastanza è conforme a questo standard è diciamo e queste cose qui qua si chiama variable e nell'altro si chiama.  
Attributive no, però sono diciamo valori diciamo di tipo sì o no OK, non OK, conformi non conformi no. Quindi e nel vostro diciamo nella vostra anagrafica avete entrambe no?

_[immagine]_**  
Spreafico Paolo** 3:24:40  
Attributive no, però sono diciamo valori diciamo di tipo sì o no, OK, non OK, conforme non conforme no. Quindi e nel vostro diciamo nella vostra anagrafica avete entrambe no.

_[immagine]_**  
Emanuele Merlo** 3:24:55  
Questo tipo di. Poi c'è la terza che invece è quella visiva che è accompagnata da anche un documento no, cosa che probabilmente userete anche noi a oggi non abbiamo questo sistema.

_[immagine]_**  
Spreafico Paolo** 3:24:55  
In questi tipi di stazioni. Poi c'è la terza che invece è quella visiva che è accompagnata da anche un documento no, cosa che probabilmente noi a oggi non abbiamo la caratteristica visiva. Questo sistema ci permette sì visuale, scusami.

_[immagine]_**  
Emanuele Merlo** 3:25:14  
Questo sistema ci permette anche di caricare delle foto e dire ti confermo che in questa zona qui.

_[immagine]_**  
Spreafico Paolo** 3:25:14  
Questo sistema ci permette anche di caricare delle foto e dire ti confermo che in questa zona qui.

_[immagine]_**  
Emanuele Merlo** 3:25:22  
C'è questa marcatura, ti confermo che questa c'è, quindi ci viene fuori direttamente il disegnino e devi andare a dirgli sì, OKO non OK.

_[immagine]_**  
Spreafico Paolo** 3:25:22  
C'è questa marcatura, ti confermo che questa c'è, quindi ti viene fuori direttamente il disegnino e devi andare a dirgli sì, OKO non OK.

_[immagine]_**  
Emanuele Merlo** 3:25:34  
C'è anche questa come vuoi, a oggi non ce l'avevamo, non è stata più grata.

_[immagine]_**  
Spreafico Paolo** 3:25:34  
C'è anche questa Denise, come vuoi, se ti piace i disegnini a oggi non ce l'avevamo, non è stata migrata.

_[immagine]_**  
Emanuele Merlo** 3:25:45  
Già avete necessità?

_[immagine]_**  
Spreafico Paolo** 3:25:45  
Se avete necessità.

_[immagine]_**  
Emanuele Merlo** 3:25:47  
La implementeremo in un futuro anteriore, quindi non alla patente del Live su un codice pilota, lo teniamo monitorato per vedere il comportamento prima di andare a vedere il patente.

_[immagine]_**  
Spreafico Paolo** 3:25:48  
La implementeremo in un futuro anteriore, quindi non alla partenza del Live su un codice pilota, lo teniamo monitorato per vedere il comportamento prima di andare dentro il tappeto.

_[immagine]_**  
Emanuele Merlo** 3:26:03  
Vi chiedo con il cuore, non prendete iniziative.

_[immagine]_**  
Spreafico Paolo** 3:26:03  
Vi chiedo con il cuore, non prendete iniziative.

_[immagine]_**  
Emanuele Merlo** 3:26:11  
Quel tipo crea delle caratteristiche alla viva il parroco.

_[immagine]_**  
Spreafico Paolo** 3:26:11  
Del tipo creo delle caratteristiche alla viva il parroco.

_[immagine]_**  
Emanuele Merlo** 3:26:16  
E le spara il sistema, perché ogni modifica che facciamo ha impatto su questo.

_[immagine]_**  
Spreafico Paolo** 3:26:16  
E le sparo al sistema, perché ogni modifica che facciamo ha impatto su quei signori lì.

_[immagine]_**  
Emanuele Merlo** 3:26:23  
Stiamo lavorando per ridurre i controlli perché avete visto che ci sono 35 40 controlli sulla produzione?

_[immagine]_**  
Spreafico Paolo** 3:26:24  
Stiamo lavorando per ridurre i controlli perché avete visto che ci sono 35 40 controlli sulla produzione?

_[immagine]_**  
Emanuele Merlo** 3:26:33  
Che oggettivamente un controllo son 15 secondi non è OKOKOK come funziona oggi.

_[immagine]_**  
Spreafico Paolo** 3:26:33  
Che oggettivamente un controllo son 15 secondi non è l'OKOKOK come facevano oggi.  
Quindi i tempi sono più lunghi.

_[immagine]_**  
Emanuele Merlo** 3:26:45  
Mettiamo quello che ci serve che ci dà valore aggiunto.

_[immagine]_**  
Spreafico Paolo** 3:26:45  
Mettiamo quello che ci serve, che ci dà valore aggiunto.

_[immagine]_**  
Emanuele Merlo** 3:26:48  
Sapere il colore degli occhi dell'operatore che mi sta dando l'informazione, ogni informazione che mi serve il valore aggiunto.

_[immagine]_**  
Spreafico Paolo** 3:26:49  
Sapere il colore degli occhi dell'operatore che mi sta dando l'informazione, un'informazione che mi serve, mi dà valore aggiunto.

_[immagine]_**  
Emanuele Merlo** 3:26:58  
Uno.

_[immagine]_**  
Spreafico Paolo** 3:26:59  
O no?

_[immagine]_**  
Emanuele Merlo** 3:27:00  
Facciamo questo ragionamento, non vi sto dicendo di non mettere i controlli assolutamente, mettiamo quello che ci serve.

_[immagine]_**  
Spreafico Paolo** 3:27:00  
Facciamo questo ragionamento, non vi sto dicendo di non mettere i controlli, assolutamente mettiamo quello che ci serve.

_[immagine]_**  
Emanuele Merlo** 3:27:13  
Prego quindi vediamo come creare una nuova caratteristica. Volete fare qualcosa di voi? Lo facciamo noi come potete vai.

_[immagine]_**  
Spreafico Paolo** 3:27:13  
Prego, vediamo come creare una nuova caratteristica. Volete fare qualcuno di voi? Vai.

_[immagine]_**  
Emanuele Merlo** 3:27:24  
Volete scierare e creare una caratteristica? Dovrebbe essere abbastanza intuitivo. Se c'è qualcuno in chat che vuol scierare, ti guidiamo noi.

_[immagine]_**  
Spreafico Paolo** 3:27:24  
Potete sharare e creare una caratteristica, dovrebbe essere abbastanza intuitivo. Prova, se c'è qualcuno in chat che vuol sharare.

_[immagine]_**  
Emanuele Merlo** 3:27:41  
E adesso andiamo via alcuni documenti che quando aprono produzione.

_[immagine]_**  
Spreafico Paolo** 3:27:41  
Presente.

_[immagine]_**  
Emanuele Merlo** 3:27:47  
Mi esce un avviso a tutto schermo, non c'è più.

_[immagine]_**  
Spreafico Paolo** 3:27:48  
Esce un avviso tutto schermo non c'è più.

_[immagine]_**  
Emanuele Merlo** 3:27:56  
Perché ci sono?

_[immagine]_**  
Spreafico Paolo** 3:27:56  
Perché ci sono?

_[immagine]_**  
Emanuele Merlo** 3:27:58  
Quindi quello dei Golgi Migiani della Porsche.

_[immagine]_**  
Spreafico Paolo** 3:27:58  
Il quello dei bollini Gianni della Porsche.

_[immagine]_**  
Emanuele Merlo** 3:28:01  
E in base a quello che viene comunicato da l'ingegnere di qualità vengono messe, sì, sono documenti che.

_[immagine]_**  
Spreafico Paolo** 3:28:07  
Sono documenti quelli sì, però l'operatore deve sapere inizio produzione che.  
Per la promozione invece adesso quando apro il codice AAA oggi i pop-up non sono non son previsti dovremmo dovremmo preveder di metterlo come controlli come controllo esatto applicare bollino secondo.

_[immagine]_**  
Emanuele Merlo** 3:28:22  
Invece adesso io proprio quando apro il codice dovremmo dovremmo prevedere di metterlo applicare bollino.  
A migrare avanti.

_[immagine]_**  
Spreafico Paolo** 3:28:37  
Micrar.

_[immagine]_**  
Emanuele Merlo** 3:28:39  
Diagramma.

_[immagine]_**  
Spreafico Paolo** 3:28:41  
No, e vabbè, a oggi la documentazione.

_[immagine]_**  
Emanuele Merlo** 3:28:42  
La documentazione.  
Se vi trovate i codici in qualche modo riusciamo a piantarli dentro, se continuate a scendere, spegnere.

_[immagine]_**  
Spreafico Paolo** 3:28:46  
Se mi trovate i codici in qualche modo riusciamo a piantarli dentro, però se continuate a accendere, spegnere, accendere e spegnere come cavolo fa, come faccio a mettervi un automatismo?  
E non c'è più la data di fino e la data.

_[immagine]_**  
Emanuele Merlo** 3:29:05  
Cancello la riga e sparisce. Può darsi che ad esempio fanno lo stesso codice oggi e domani. Oggi devono mettere il bollino.

_[immagine]_**  
Spreafico Paolo** 3:29:06  
E non funziona più così.  
In tal caso devi giocarla col master.  
Vai, facciamo praticamente adesso la fase conclusiva, no, facciamo, facciamo fare a lui tutto il coso da zero, quindi creiamo una caratteristica magari di tipo.

_[immagine]_**  
Emanuele Merlo** 3:29:20  
Ok, allora facciamo allora praticamente adesso la fase conclusiva, no, facciamo allora facciamo fare a lui tutto da zero, quindi creiamo una caratteristica magari di tipo.  
Variabile crea, ci creiamo sopra in spatial definition l'associamo a workholder e andiamo a vedere in pagina che ci sia no questi tre perfetto.

_[immagine]_**  
Spreafico Paolo** 3:29:34  
Variabili, ci creiamo sopra in specie Definition, associamo a wordcoder e andiamo a vedere in pagina che ci siano questi tre.

_[immagine]_**  
Emanuele Merlo** 3:29:45  
Dopodiché faremo, magari facciamo un giretto con Paolo su Power BI per vedere le cose che avevamo accennato, vedere magari live un secondo e poi magari facciamo le open question velocissime e abbiamo anche un mini questionario di.

_[immagine]_**  
Spreafico Paolo** 3:29:45  
Dopodiché faremo, magari facciamo un giretto con Paolo su Power BI per vedere le cose che avevamo accennato, vedere magari live un secondo e poi magari facciamo gli open passing velocissime e abbiamo anche un mini questionario di.

_[immagine]_**  
Emanuele Merlo** 3:30:01  
Di uscita da farmi fare due sono due, uno sarà un attimo per capire se avete capito e l'altro sarà il gradimento della lezione. Caratteristica quindi è entrato nella pagina basic, quella che contiene tutto.

_[immagine]_**  
Spreafico Paolo** 3:30:01  
Di uscita da farvi fare per capire se avete capito e l'altro sarà il gradimento della lezione. Ok, perfetto, allora caratteristica. Quindi è entrato nella pagina Basic, quella che contiene tutto.

_[immagine]_**  
Emanuele Merlo** 3:30:17  
Tutte le pagine diciamo possibili di configurazione di quindi le pagine sono tutte uguali, c'è un filtro iniziale, la griglia e poi ci sono le azioni sul pannello di qua, quindi lì c'è un'azione, un'azione, qua c'è la lingua, appunto la lingua.

_[immagine]_**  
Spreafico Paolo** 3:30:18  
Tutte le pagine diciamo possibili di configurazione, quindi le pagine sono tutte uguali, c'è un filtro iniziale, la griglia e poi ci sono le azioni sul pannello di qua, quindi lì c'è un'azione, qua c'è la lingua, appunto la lingua.

_[immagine]_**  
Emanuele Merlo** 3:30:35  
Qua lui ha selezionato italiano, OK, se tu la vuoi cambiare devi andare in quella cosa che si chiama però aspetta aggiungi.

_[immagine]_**  
Spreafico Paolo** 3:30:35  
Se tu la vuoi cambiare devi andare in quella cosa che si chiama finiamo una cosa, aggiungi una caratteristica, sennò se continuiamo a saltare a destra a sinistra facciamo casino.

_[immagine]_**  
Emanuele Merlo** 3:30:46  
Aggiungiamo allora. Quindi qua ci sono tre tipi di aggiunte, appunto attributive. Poi vi sono attributive. OK, sono le più semplici. Quelle variabili sono più complicate perché hanno.

_[immagine]_**  
Spreafico Paolo** 3:30:55  
Attributive, quali sono? OK, sono le più semplici, quelle variabili sono più complicate perché hanno una unit of measure, in teoria hanno un massimo, un minimo e anche diciamo sono leggermente più complicate perché queste qui in teoria.

_[immagine]_**  
Emanuele Merlo** 3:31:03  
Una unit of measure in teoria hanno massimo, minimo e anche diciamo sono leggermente più complicate perché queste qui in teoria uno potrebbe magari una cosa che vediamo praticamente dal dal workmaster uno potrebbe ridefinire quella torre per quel.

_[immagine]_**  
Spreafico Paolo** 3:31:14  
Uno potete beh magari una cosa che vediamo praticamente dal dal workmaster uno potrebbe ridefinire quella tolerance per quel materiale finale no? Quindi sono leggermente complicate ma che ho visto che ancora voi non l'avete usato questa.

_[immagine]_**  
Emanuele Merlo** 3:31:23  
Materiale finale no, quindi sono leggermente più complicate ma non in case che ho visto accanto a voi non l'avete usata questa quindi facciamo una di tipo variabile così vediamo e poi quella grafica, quella appunto che noi chiamiamo visual quindi qua devi dare l'i D.

_[immagine]_**  
Spreafico Paolo** 3:31:32  
Quindi facciamo uno di tipo variabile così vediamo proprio la grafica, quella appunto che noi chiamiamo visual, quindi qua devi dare l'i D l'i D inventalo facciamo sempre il washing quindi fargli.

_[immagine]_**  
Emanuele Merlo** 3:31:39  
La Revision, VV inventano, facciamo sempre paywashing, quindi è fargli fare una cosa.

_[immagine]_**  
Spreafico Paolo** 3:31:50  
Wash no wash il tuo nome che così lo troviamo.

_[immagine]_**  
Emanuele Merlo** 3:31:52  
Washington.  
Non so se la misurate.

_[immagine]_**  
Spreafico Paolo** 3:31:56  
Se la misurate non so l'espressione.  
OKOK la revision a perché sono tutte a identificatore univoco mi sembra che facciamo facciamo ID underscore per Convenzione gli abbiamo dato lo stesso medesimo ID underscore la revisione.

_[immagine]_**  
Emanuele Merlo** 3:32:02  
OK, la revision è a perché sono tutte a identificatore univoco. Mi sembra che facciamo facciamo ID underscore revision la convenzione gli abbiamo dato lo stesso medesimo ID underscore revision.  
Per cominciare dopo son cambi a vostro uso e consumo. Io per migrare ho preso il nome del ciclo e poi la posizione, il nome qua puoi essere un pochettino più descrittivo in modo da riconoscerla qua di solito è quel partner che ho visto.

_[immagine]_**  
Spreafico Paolo** 3:32:19  
Per convenzioni dopo son campi a vostro uso e consumo, io per migrare ho preso il nome del ciclo e poi la posizione per quelli vecchi.  
Sono tutti i campi liberi, però sono tutti i campi liberi.

_[immagine]_**  
Emanuele Merlo** 3:32:38  
OK, poi descrizione uguale nome Paypal.

_[immagine]_**  
Spreafico Paolo** 3:32:39  
Cari poi descrizione uguale, sono tutte tutte uguali, insomma.

_[immagine]_**  
Emanuele Merlo** 3:32:43  
Perché ti cita anche lì, sono tutte tutte uguali, insomma.  
Questi non hanno effetti sul sistema, quindi potete scrivermi quello che volete come allora dovete mettere qualcosa, però per piacere quello che mi chiedete.

_[immagine]_**  
Spreafico Paolo** 3:32:50  
Questi non hanno effetti sul sistema e quindi potete potete scrivergli quello che volete.  
Come allora dovete mettere qualcosa, però potete scegliere quello che vi piace di più.

_[immagine]_**  
Emanuele Merlo** 3:33:06  
Puntasse sempre qua, va bene, se poi guarda il processo qua, se avete fatto.

_[immagine]_**  
Spreafico Paolo** 3:33:15  
BCS.

_[immagine]_**  
Emanuele Merlo** 3:33:20  
La pressione della bara d'accordo, sì, anche se poi sì, occhio a quanto è il nominale sì.

_[immagine]_**  
Spreafico Paolo** 3:33:20  
Pressiona bene, bara d'accordo.  
Occhio, quanto è il nominale?  
E 94 110 mi sembra sì, vabbè, 400 è il nominale.

_[immagine]_**  
Emanuele Merlo** 3:33:30  
400 è il nominale. Ovvio che il nominale deve essere sempre compreso tra il minimo e il massimo. In teoria li puoi sovrascrivere, ma.

_[immagine]_**  
Spreafico Paolo** 3:33:34  
Occhio che il nominale deve essere sempre compreso tra il minimo e il massimo.  
Quindi una localizzazione, ma ti deve sempre dominare, deve essere sempre tra minimo e massimo.

_[immagine]_**  
Emanuele Merlo** 3:33:48  
Perfetto salvati il codice che mi hai dato perfetto salva e adesso in anagrafica OK quindi quando ad esempio può capitare a disegno.

_[immagine]_**  
Spreafico Paolo** 3:33:49  
Salve, salva, ti ricordi di che mi hai dato? No sì, quindi quando ad esempio può capitare disegno.

_[immagine]_**  
Emanuele Merlo** 3:34:06  
Due casi, uno ad esempio delle larghezze che hai zero e -16-16 e meno che mi ha appena bloccato.

_[immagine]_**  
Spreafico Paolo** 3:34:17  
Come ti ho appena bloccato al contrario, ho messo valore nominale 40 valori di tolleranza, intendi la tolleranza o il valore da zero? Se il nominale è zero, il minimo della tolleranza è zero.

_[immagine]_**  
Emanuele Merlo** 3:34:20  
Buongiorno, avevo fatto al contrario 40 con il valore di tolleranza intende la tolleranza, un valore fa zero, il nominale zero, la tolleranza è zero e il massimo quanto è.

_[immagine]_**  
Spreafico Paolo** 3:34:35  
Il Massimo quanto è?

_[immagine]_**  
Emanuele Merlo** 3:34:38  
Devo mettergli il valore massimo che posso raggiungere o la tolleranza, cioè devo mettergli più o meno il numero, il numero, il numero massimo della tolleranza 40 più o -2 devo mettergli 4242.

_[immagine]_**  
Spreafico Paolo** 3:34:38  
Se tu ovviamente vai in negativo, il valore, il numero, il numero, il numero massimo della tolleranza.  
42 OK, 384238 è il minimo, 42 è il massimo.

_[immagine]_**  
Emanuele Merlo** 3:34:53  
OK, 384238 è il minimo, 42 è il massimo.  
E a vedere con la tosta dei numeri naturali, vero?

_[immagine]_**  
Spreafico Paolo** 3:35:01  
E ragazzi, ve l'hai ricordata la scala dei numeri naturali, vero?

_[immagine]_**  
Emanuele Merlo** 3:35:06  
Quindi da zero.

_[immagine]_**  
Spreafico Paolo** 3:35:06  
Quindi da zero cresco se gli metto il meno.

_[immagine]_**  
Emanuele Merlo** 3:35:08  
Fresco se gli metto almeno al contrario si sa mai visto la domanda Di Pietro che l'ha bloccato.

_[immagine]_**  
Spreafico Paolo** 3:35:12  
Al contrario.  
No, si sa mai, visto la domanda Di Pietro che l'ha bloccato.

_[immagine]_**  
Emanuele Merlo** 3:35:20  
Scusa allora OK, devo mettere zeri e due non 42. Se ho 40 più o -2 più o -2 devo mettere due e -2 se ho 40 se ho -2 la tolleranza quant'è 28 la tolleranza è più o -2.

_[immagine]_**  
Spreafico Paolo** 3:35:20  
Scusa allora OK devo mettere zero e due non 42 se ho 40 più o -2 più o -2 devo mettere due e -2 se 40 se più o -2 la tolleranza quant'è.  
38 più o -2, poi i valori devi mettere il valore minimo, il valore massimo.

_[immagine]_**  
Emanuele Merlo** 3:35:36  
Poi valori, il valore minimo, valore minimo, valore massimo, magari la traduzione sbagliata nel campo però.  
OK quindi allora adesso domanda facilissima, possiamo metterle direttamente nel work order e vederle poi nella pagina posso una volta che sono state create possiamo inserire, andare nella pagina e inserirle?

_[immagine]_**  
Spreafico Paolo** 3:35:48  
OK quindi allora adesso domanda facilissima, adesso possiamo metterle direttamente nel work order, cioè metterle poi nella pagina posso una volta che possiamo inserire, andare nella pagina e inserirle.

_[immagine]_**  
Emanuele Merlo** 3:36:07  
Sì, no, non c'è un oggetto. Esatto, non puoi metterli direttamente perché questo qui sono solo cose astratte, no? Cioè non possono ancora essere misurate. No, perché non sai quando misurarle.

_[immagine]_**  
Spreafico Paolo** 3:36:07  
Sì, no, non può essere misurate. No, perché non sai quando misurarle.

_[immagine]_**  
Emanuele Merlo** 3:36:23  
Ok, allora c'è un'altra anagrafica che è chiamata Inspection Definition.

_[immagine]_**  
Spreafico Paolo** 3:36:24  
Questo è un accordo che stiamo andando a riprendere quale fosse.  
Scendi, Scendi, Scendi, puoi metterle perché appunto non è ancora non sai quando misurare, hai descritto la caratteristica ma non hai descritto quando misurare questa caratteristica e quindi la pagina che fa questo link che fa questo diciamo.

_[immagine]_**  
Emanuele Merlo** 3:36:32  
OK, qua non puoi metterle perché appunto non è ancora non sai quando misurare. Hai descritto la caratteristica ma non hai descritto quando misurare questa caratteristica. OKE, quindi la pagina.  
Che fa questo link, che fa questo diciamo questo master data si chiama inspection definition.

_[immagine]_**  
Spreafico Paolo** 3:36:50  
Questo master data si chiama Inspection Definition.

_[immagine]_**  
Emanuele Merlo** 3:36:55  
Quindi deve tornare nella home, OK?

_[immagine]_**  
Spreafico Paolo** 3:36:57  
OK ispezioni.

_[immagine]_**  
Emanuele Merlo** 3:36:59  
Ispezione.  
E qui ovviamente devi fare New, perché anche qui c'è una main convention, cerchiamo di capire qual è.

_[immagine]_**  
Spreafico Paolo** 3:37:05  
E qui ovviamente devi fare OK, anche qui c'è una mail convention, cerchiamo di capire qual è. No, qua sono codici interni, quindi è un codice diciamo al fallimento.

_[immagine]_**  
Emanuele Merlo** 3:37:13  
No, guarda che qua sono codici interni, quindi è un codice diciamo Alfanumerico, quindi incollaci ancora quasi prima.

_[immagine]_**  
Spreafico Paolo** 3:37:18  
E di incollaci ancora quel numero che gli hai messo prima.  
Nome gli scrivi quello che vuoi.

_[immagine]_**  
Emanuele Merlo** 3:37:28  
Provision a.

_[immagine]_**  
Spreafico Paolo** 3:37:28  
Revision a prima, OK, Scendi.

_[immagine]_**  
Emanuele Merlo** 3:37:34  
Mi di caratteristica che a questo posto qua il link qual è la corrente bloccato per seleziono tutti e due allora.

_[immagine]_**  
Spreafico Paolo** 3:37:36  
O incolla oppure scegli scegli. Esatto quale è corrente bloccato OK selezionalo tutti e due no.  
Con che frequenza ogni quanto per farlo controllare 100%.  
Quindi 100% però 100% certificatore ma aspetto che hai controllato tutti i pezzi.

_[immagine]_**  
Emanuele Merlo** 3:37:59  
O dallo Stato iniziale o dallo Stato di pausa, però al 100% se poi io leggo nel Report, sì, sono un certificatore, ma aspetta che hai controllato tutti i pezzi.

_[immagine]_**  
Spreafico Paolo** 3:38:16  
Aspetta, questa è un'impostazione al sistema.

_[immagine]_**  
Emanuele Merlo** 3:38:16  
Questa è l'impostazione al sistema. OK, il valutatore non lo vedrà. Questa impostazione OKE, nell'altro ci sarà scritto un pezzo.

_[immagine]_**  
Spreafico Paolo** 3:38:20  
Il valutatore non lo vedrà questa impostazione ma vedrà il report da un'altra parte non la vede questo questi sono i nostri settaggi interni OKE nell'altro ci sarà scritto un pezzo c'è scritto.

_[immagine]_**  
Emanuele Merlo** 3:38:32  
C'è scritto i valori registrati, non c'è, non c'è scritto quanti.

_[immagine]_**  
Spreafico Paolo** 3:38:34  
I valori registrati non c'è, non c'è scritto quanti.

_[immagine]_**  
Emanuele Merlo** 3:38:41  
Questo originale di firma è influente, no salvo, salva, salva.

_[immagine]_**  
Spreafico Paolo** 3:38:41  
Questo scenario di firma è influente, no, salvo, salva, salva.

_[immagine]_**  
Emanuele Merlo** 3:38:48  
Sì, adesso qua c'è, diciamo una volta che sì, adesso puoi, adesso qual è?

_[immagine]_**  
Spreafico Paolo** 3:38:48  
Adesso qua c'è diciamo una volta creata sì, adesso lo puoi, adesso poi è il prossimo step vediamo. E se invece avessi fatto unit based sarebbe a numero di pezzi, quindi se faccio unit based uno.

_[immagine]_**  
Emanuele Merlo** 3:39:01  
Page sarebbe a di pezzi, quindi se faccio un unit base uno ogni pezzo ti chiede coso sì, però se come appunto la pagina diciamo la pagina di inserimento no, è una pagina diciamo Custom.

_[immagine]_**  
Spreafico Paolo** 3:39:06  
Ogni pezzo ti chiede il coso, sì, però siccome appunto la pagina, diciamo la pagina di inserimento no, è una pagina diciamo Custom per Brembo. Allora bisogna vedere se quella personalità lì.

_[immagine]_**  
Emanuele Merlo** 3:39:16  
Per Brembo allora bisogna vedere se la funzionalità lì è disponibile, no?  
Quindi adesso possiamo metterla nel workoder e la vediamo direttamente no oppure nel workmaster avete capito la differenza?

_[immagine]_**  
Spreafico Paolo** 3:39:23  
Quindi adesso possiamo metterla nel work code e la vediamo direttamente, no? O oppure nel work master, avete capito la differenza?  
Mettiamo la prima di workmaster OK, quindi vediamo una di workmaster se ci dici il codice.

_[immagine]_**  
Emanuele Merlo** 3:39:38  
Diamo la prima di un workmaster, OK, quindi prendiamo uno dei workmaster se ci dici il codice.  
Prima delle workmaster, prima spenderemo oggi.

_[immagine]_**  
Spreafico Paolo** 3:39:46  
E ma e devo il master di prima perché non lo cerco.  
Cosa cambia? Questo cambia questo qua è la caratteristica, questo qua è ogni quanto devo usare questa caratteristica, quindi è la frequenza.

_[immagine]_**  
Emanuele Merlo** 3:39:55  
Sì, però tramite il mio tramite il mio dove lo prendo questo? Boh, anche dalla o anche dal workcode. OK, il workcode è.

_[immagine]_**  
Spreafico Paolo** 3:40:07  
OK, devo togliere 131379.

_[immagine]_**  
Emanuele Merlo** 3:40:09  
13, 13 e 79.  
Quindi vai così, aggiungiamole a tutte e due, 13 e 79.

_[immagine]_**  
Spreafico Paolo** 3:40:14  
13, scusami 13, 79.

_[immagine]_**  
Emanuele Merlo** 3:40:22  
OK, questo il washing perfetto, allora intanto aggiungiamo uno qua così lo vediamo subito nella.

_[immagine]_**  
Spreafico Paolo** 3:40:22  
OK, questo baby washing perfetto. Allora intanto aggiungiamolo qua così lo vediamo subito nella apro.

_[immagine]_**  
Emanuele Merlo** 3:40:34  
Apri operazione e mettiamo il tuo.

_[immagine]_**  
Spreafico Paolo** 3:40:35  
Guarda.  
Di qualità collega.

_[immagine]_**  
Emanuele Merlo** 3:40:42  
Box.

_[immagine]_**  
Spreafico Paolo** 3:40:42  
Box.  
La tua collegamento.

_[immagine]_**  
Emanuele Merlo** 3:40:50  
Adesso va collegato all'ordine, adesso parla anche al suo, al suo, al suo professor.

_[immagine]_**  
Spreafico Paolo** 3:40:50  
Adesso l'ho collegato all'ordine, questo.

_[immagine]_**  
Emanuele Merlo** 3:41:05  
La supporto OK, bravissimo, hai già capito se non hanno operation OK, perfetto.

_[immagine]_**  
Spreafico Paolo** 3:41:07  
Sì, arrivo, vado a prendere.

_[immagine]_**  
Emanuele Merlo** 3:41:21  
OK, sapete già tutto qua?  
Guarda, devo fare comunque sull'operazione. Sì, perché è il suo template, diciamo vedete che qua c'è questo link che non ne abbiamo parlato, vedete che c'è questo link qua?

_[immagine]_**  
Spreafico Paolo** 3:41:27  
Qua lo devo fare comunque sull'operazione, quindi spezione di qualità collega.  
Vedete che qua c'è questo link che non abbiamo parlato, vedete che c'è questo link qua che in teoria potete aprire, no? Questo qui è diciamo un modo che ha OP center per poi ridefinire.

_[immagine]_**  
Emanuele Merlo** 3:41:45  
E in teoria la potete aprire, no? Questo qui è, diciamo, un modo che ha open center per poi definire il valore nominale, la tolerance per questo ciclo, no, per questo prodotto. Ammettete che voi avete.

_[immagine]_**  
Spreafico Paolo** 3:41:52  
Il valore nominale, la tollerance per questo ciclo? No, per questo prodotto ammettete che voi avete OK, cioè quindi qua tu definisci da quel botto puoi modificare i limiti solo per quello.  
Vado a ogni ordine, se invece sono tutte uguali posso fare.

_[immagine]_**  
Emanuele Merlo** 3:42:22  
Se qua tu la Apri e la cambi, poi nella i nuovi valori nominali, OK, chi la Apri e diciamo puoi definire.

_[immagine]_**  
Spreafico Paolo** 3:42:24  
E la cambi, poi i nuovi valori nominali. Credo di aver fatto qualcosa di sbagliato. Sì, no, è giusto, OK, quindi qua, grazie. E come posso ridefinirla?

_[immagine]_**  
Emanuele Merlo** 3:42:38  
E come posso? Entro nel filtro, cerco sempre, la cambi i valori nominali.

_[immagine]_**  
Spreafico Paolo** 3:42:40  
Beh, entro nel filtro cerco sempre workshop, giusto? La Apri, la apro, Edit, questo non OK, non OK, quindi non può cambiare niente.

_[immagine]_**  
Emanuele Merlo** 3:42:54  
Questo era.  
Se chiude un attimo.  
A qualcuno manca la penna.

_[immagine]_**  
Spreafico Paolo** 3:43:14  
Hai fatto Edit sicuro.  
Flavio sta chiedendo la frequenza, cioè non è che sono nella pagina sbagliata te lo faccio vedere offline, adesso fammi finiamo questo un attimo perché sennò ci perdiamo comunque da questa, da un'altra pagina riesci a modificare la.

_[immagine]_**  
Emanuele Merlo** 3:43:30  
Vado da qua, non riesci a modificarlo, te lo faccio vedere comunque da questa, da un'altra pagina riesci a modificare la.

_[immagine]_**  
Spreafico Paolo** 3:43:46  
Le la le pressioni e i parametri nominali non è da questa, è da un'altra per la singola caratteristica inserita in quello specifico box, quindi riesci a mettergli la tolleranza.

_[immagine]_**  
Emanuele Merlo** 3:43:46  
La depressione e i parametri non è da questa singola caratteristica inserita in quello specifico box.  
Forse no, forse devi fare edit nella prima pagina, non devi cliccare, torna indietro nel nella definizione di nell'inspection.

_[immagine]_**  
Spreafico Paolo** 3:44:05  
Deve fare.

_[immagine]_**  
Emanuele Merlo** 3:44:15  
E clicchi su processo qua si vede che qua non devi seguire ma devi fare edit da una volta che l'hai inserita scusate fai selezionala.  
Sì, OK, e se tu link fai fai quel click reader scusami questo.  
Questo sì, eviti Apri lì.

_[immagine]_**  
Spreafico Paolo** 3:44:37  
Questo sì, è che ti apre lì.  
No, non è questo.  
No, è uguale, è da torna indietro dopo te lo mostro perché è una sì, non ti preoccupare, te lo faccio vedere dopo, dai.

_[immagine]_**  
Emanuele Merlo** 3:44:59  
No, non ti preoccupare, ce la faccio giocare allora, quindi l'hai inserita adesso se tu vai nella repetitive.

_[immagine]_**  
Spreafico Paolo** 3:45:03  
L'hai inserita adesso se tu vai nella Repetitive.

_[immagine]_**  
Emanuele Merlo** 3:45:08  
Puoi dare il tuo controllo, giusto?

_[immagine]_**  
Spreafico Paolo** 3:45:09  
Mi dai il tuo controllo, giusto? Spero di sì.

_[immagine]_**  
Emanuele Merlo** 3:45:17  
Allora è un'altro link? No, questo qua vedi no 10 basic l'altro link.

_[immagine]_**  
Spreafico Paolo** 3:45:17  
Il quale scusami era è un'altro link, no questo qua vedi no DS basic e l'altro link.

_[immagine]_**  
Emanuele Merlo** 3:45:25  
No, non è qua, non è proprio un link diverso, è discreto.

_[immagine]_**  
Spreafico Paolo** 3:45:25  
No, non è qua, non è un link diverso.  
È discreto.

_[immagine]_**  
Emanuele Merlo** 3:45:31  
Ecco, comunque adesso te lo troverai dentro, ragazzi, visto che siamo in dirittura d'arrivo, mi vuole rompermi le scatole.

_[immagine]_**  
Spreafico Paolo** 3:45:31  
Ecco, comunque adesso te lo troverai dentro.  
Ragazzi, visto che siamo in dirittura d'arrivo mi duole rompervi le scatole, vi faccio vedere una cosa.

_[immagine]_**  
Emanuele Merlo** 3:45:43  
Vi faccio vedere una cosa.  
Cubo scatti cubo scatti avrà questa parte su Power BI, quindi a tutti gli effetti potrete filtrare per materiale articolo vi ho già preparato sia un parete con le causali di saldo peggiori.

_[immagine]_**  
Spreafico Paolo** 3:45:50  
Cubo scarti il cubo scarti avrà questa faccia su Power BI, quindi a tutti gli effetti potrete filtrare per materiale articolo vi ho già preparato sia un pareto con le causali di scarto peggiori in numero di pezzi e in percentuale assoluta.

_[immagine]_**  
Emanuele Merlo** 3:46:04  
In numero di pezzi e in percentuale assoluta sugli ordini di produzione.

_[immagine]_**  
Spreafico Paolo** 3:46:08  
Sugli ordini di produzione.

_[immagine]_**  
Emanuele Merlo** 3:46:12  
Tutti questi report sono già disponibili dall'otto direi devo solo aprire, quindi io ho già preparato la lista per calendario, quindi giorno per giorno, quando pezzi scartano, quanti pezzi sono stati prodotti, la percentuale di scarto per pavimento, per causale di scarto.

_[immagine]_**  
Spreafico Paolo** 3:46:12  
Tutti questi report sono già disponibili dall'otto ve li devo solo aprire, quindi vi ho già preparato la vista per calendario, quindi giorno per giorno cosa pezzi scartano, quanti pezzi sono stati prodotti, la percentuale di scarto per fallimento.  
Quindi per causare gli scarto la tabella tra virgolette piatta in modo tale se vi serve dall'excel per tirarvelo fuori.

_[immagine]_**  
Emanuele Merlo** 3:46:30  
La tabella tra virgolette piatta in modo tale se ti serve dall'excel per tirarselo fuori.  
La produzione scusami in modo tale che vedete comodamente da casa tutti i controlli che fanno la produzione qui vi trovate ordine per ordine, cosa sta registrando il.

_[immagine]_**  
Spreafico Paolo** 3:46:39  
La produzione scusami in modo tale che vedete comodamente da casa tutti i controlli che fanno la produzione. Qui vi trovate ordine per ordine. Cosa sta registrando il.

_[immagine]_**  
Emanuele Merlo** 3:46:56  
Cosa sta registrando la linea qui trovate per questo ordine questo codice su questa linea le caratteristiche controllate con i loro valori.

_[immagine]_**  
Spreafico Paolo** 3:46:56  
Cosa sta registrando la linea quindi trovate per questo ordine questo codice su questa linea le caratteristiche controllate con i loro valori.

_[immagine]_**  
Emanuele Merlo** 3:47:09  
OK.

_[immagine]_**  
Spreafico Paolo** 3:47:09  
OK.

_[immagine]_**  
Emanuele Merlo** 3:47:11  
Il polpo per gli amici, dove dato un articolo consumato o prodotto.

_[immagine]_**  
Spreafico Paolo** 3:47:11  
Il polpo per gli amici, dove dato un articolo consumato o prodotto.

_[immagine]_**  
Emanuele Merlo** 3:47:23  
Vi trovate direttamente la genealogia, quindi parto da questo, ho consumato 24 pezzi, sono andati in questo CD qua che è andato in questo CD.

_[immagine]_**  
Spreafico Paolo** 3:47:23  
Vi trovate direttamente la genealogia, quindi parto da questo, ho consumato 24 pezzi sono andati in questo CD qua che è andato in questo CD.

_[immagine]_**  
Emanuele Merlo** 3:47:36  
Come il numero di articolo e come.

_[immagine]_**  
Spreafico Paolo** 3:47:37  
Come numero di articolo e come.

_[immagine]_**  
Emanuele Merlo** 3:47:42  
C quindi vedete fisicamente CDI per CDI quanti pezzi sono stati tolti e dove sono andate a finire a livello di cassetta, quindi ve li trovate senza problemi. A che modo mi riferisco?

_[immagine]_**  
Spreafico Paolo** 3:47:42  
CDI quindi vedete fisicamente CDI per CDI quanti pezzi sono stati tolti e dove sono andati a finire a livello di cassetta, quindi ve li trovate senza grossi problemi. A che mondo mi riferisco? Vediamo se l'avete imparato.

_[immagine]_**  
Emanuele Merlo** 3:47:58  
Vediamo solo del disparato.  
Mondo montaggio, mondo lavorazione, mondo produzione, sono fuori.

_[immagine]_**  
Spreafico Paolo** 3:48:03  
Mondo montaggio, mondo lavorazione, mondo produzione, sono fuori.

_[immagine]_**  
Emanuele Merlo** 3:48:11  
Da Emanuele sono gli shop che ora sottolineo per l'ennesima volta.

_[immagine]_**  
Spreafico Paolo** 3:48:11  
Da EVM sono in shop floor, sottolineo per l'ennesima volta.

_[immagine]_**  
Emanuele Merlo** 3:48:22  
Per la buona.

_[immagine]_**  
Spreafico Paolo** 3:48:22  
Per la buona.

_[immagine]_**  
Emanuele Merlo** 3:48:25  
Tennis, devo vedere.

_[immagine]_**  
Spreafico Paolo** 3:48:26  
Pie

_[immagine]_**  
Emanuele Merlo** 3:48:29  
Qui c'è il report delle bomb e delle relative varianti, quindi dato un codice potete direttamente fuori da SAP fuori da tutto il mondo conosciuto e sconosciuto lanciare una bomba.

_[immagine]_**  
Spreafico Paolo** 3:48:29  
Qui c'è il report delle bomba e delle relative varianti, quindi dato un codice potete direttamente fuori da SAP, fuori da tutto il mondo conosciuto sconosciuto, lanciare una bomba.

_[immagine]_**  
Emanuele Merlo** 3:48:43  
Dire attenzione, io voglio vedere la bomba per questo oggetto OA tutti gli effetti un articolo in quali bombe vengono viene utilizzata?

_[immagine]_**  
Spreafico Paolo** 3:48:43  
Dire attenzione, io voglio vedere la bomba per questo oggetto OA tutti gli effetti un articolo in quali bombe vengono viene utilizzata?  
Se vi faccio vedere ostrava così almeno siamo allineati.

_[immagine]_**  
Emanuele Merlo** 3:49:01  
Te lo faccio vedere un po.  
Questo oggetto qui cosa mi produce? L'oggetto finale gli fa vedere direttamente la bomba e l'altra cosa che mi può tornare utile è il routing. Dato un oggetto, quale routing devo andare a palpare sul MES quei numeri che siamo andati?

_[immagine]_**  
Spreafico Paolo** 3:49:06  
Questo oggetto qui cosa mi produce l'oggetto finale e vi fa vedere direttamente la bomba e l'altra cosa che vi può tornare utile è il routing dato un oggetto.  
Quale routing devo andare a palpare sul MES? Quei numerelli che siamo andati a scoprire sui singoli workorder li trovate direttamente da qua, in modo tale che.

_[immagine]_**  
Emanuele Merlo** 3:49:25  
E a sto preso i simboli work order.  
Trovatevi direttamente da qua in modo tale che riuscite a colpo d'occhio senza impazzire a trovare guarda che su questo materiale ho questi routing da andare a verificare.

_[immagine]_**  
Spreafico Paolo** 3:49:33  
Riuscite a colpo d'occhio, senza impazzire, a trovare guarda che su questo materiale ho questi routing da andare a verificare.  
Dimmi.

_[immagine]_**  
Emanuele Merlo** 3:49:43  
Sì.  
Questi ve li attivo appena andiamo in linea, in caso non li abbiate vi fate il giardino ve li faccio attivare, non è un problema.

_[immagine]_**  
Spreafico Paolo** 3:49:48  
Questi ve li attivo appena andiamo in linea, in caso non li abbiate mi fate un chattino ve li faccio attivare, non è un problema.

_[immagine]_**  
Emanuele Merlo** 3:50:02  
Tutte domande, perplessità, spero tante, ma di più.

_[immagine]_**  
Spreafico Paolo** 3:50:02  
Dubbi, domande, perplessità, spero.  
Spero tante.

_[immagine]_**  
Emanuele Merlo** 3:50:09  
Bisogna farlo, non fatevi prendere dal panico.

_[immagine]_**  
Spreafico Paolo** 3:50:11  
Bisogna farlo, non fatevi prendere dal panico.

_[immagine]_**  
Emanuele Merlo** 3:50:16  
Avremo i ragazzi di Engineering secondo un piano che dobbiamo concordare.

_[immagine]_**  
Spreafico Paolo** 3:50:16  
Avremo i ragazzi di Engineering secondo un piano che dobbiamo concordare.

_[immagine]_**  
Emanuele Merlo** 3:50:23  
Vi chiedo espressamente, non prendete iniziative, non vi è chiaro qualcosa, vi fermate, tirate su la manina.

_[immagine]_**  
Spreafico Paolo** 3:50:23  
Vi chiedo espressamente, non prendete iniziative, non vi è chiaro qualcosa, vi fermate, tirate su la manina.

_[immagine]_**  
Emanuele Merlo** 3:50:36  
Ma non prendete iniziative, non prendetevi. E lo dirò anche ai ragazzi della situazione. Mi serve il materiale, lo prendo in mano, lo sposto da una parte all'altra.

_[immagine]_**  
Spreafico Paolo** 3:50:36  
Ma non prendete iniziative, non prendetevi e lo dirò anche ai ragazzi dell'accettazione, mi serve il materiale, lo prendo in mano e lo sposto da una parte all'altra.

_[immagine]_**  
Emanuele Merlo** 3:50:48  
Non lasciate fermo lì, chiamate la mamma.

_[immagine]_**  
Spreafico Paolo** 3:50:49  
Lo lasciate fermo lì, chiamate la mamma.

_[immagine]_**  
Emanuele Merlo** 3:50:53  
Ma non mettetevi a spostare il materiale, ve lo chiedo veramente con il cuore, perché se no non l'abbiamo più il \*\*\*\*\*.

_[immagine]_**  
Spreafico Paolo** 3:50:53  
Ma non mettetevi a spostare il materiale, ve lo chiedo veramente con il cuore, perché sennò non capiamo +1 \*\*\*\*\*.

_[immagine]_**  
Emanuele Merlo** 3:51:00  
Non capiamo se è l'operatore che sta sbagliando, se è il sistema che sta sbagliando, ci siamo noi che abbiamo configurato male le cose.

_[immagine]_**  
Spreafico Paolo** 3:51:00  
Non capiamo se è l'operatore che sta sbagliando, se è il sistema che sta sbagliando, se siamo noi che abbiamo configurato male le cose.

_[immagine]_**  
Emanuele Merlo** 3:51:10  
Te lo chiedo veramente con il cuore.

_[immagine]_**  
Spreafico Paolo** 3:51:10  
Te lo chiedo veramente con il cuore.  
Dimmi, il modulo validazione rimane una X, il modulo prestiti rimane una X, quali AX anche quello.

_[immagine]_**  
Emanuele Merlo** 3:51:15  
Rimane una X, il modulo prestiti rimane una x stampa delle etichette dei ricambi quali stampa delle etichette dei ricambi.  
Avrete, ve lo dico già, due problemi.

_[immagine]_**  
Spreafico Paolo** 3:51:31  
Avrete, ve lo dico già, due problemi.

_[immagine]_**  
Emanuele Merlo** 3:51:34  
Uno le anagrafiche perché son cambiati tutti i codici e via dicendo, ho già attivato il CT per farla su AX in modo tale che cambiano anche tutte le.

_[immagine]_**  
Spreafico Paolo** 3:51:34  
Uno le anagrafiche perché son cambiati tutti i codici con i suffissi e via dicendo. Ho già attivato ICT per farveli sparare dentro su AX in modo tale che i due si.

_[immagine]_**  
Emanuele Merlo** 3:51:47  
Quindi.

_[immagine]_**  
Spreafico Paolo** 3:51:47  
Quindi.

_[immagine]_**  
Emanuele Merlo** 3:51:48  
Tutti sul fisso vi ha chiesto di fare popolare, numeri, linee, cicli, quelli nuovi, quelli vecchi, in modo tale che vengano alimentati e andiamo via in parallelo e un'attività che è già sui radar, quindi non vi preoccupate.

_[immagine]_**  
Spreafico Paolo** 3:51:49  
Tutti su fisso ho già chiesto di farveli popolare, numeri, linee, cicli, quelli nuovi, quelli vecchi, in modo tale che vengano alimentati e andiamo via in parallelo.  
È un'attività che è già sui radar, quindi non vi preoccupate.

_[immagine]_**  
Emanuele Merlo** 3:52:05  
Per far dei test possiamo provare per dirci anche adesso, magari dei codici completamente vuoti, senza nessun controllo, senza.

_[immagine]_**  
Spreafico Paolo** 3:52:05  
Per far dei test possiamo trovare, cioè dirci anche adesso magari dei codici completamente vuoti, senza nessun controllo, senza.

_[immagine]_**  
Emanuele Merlo** 3:52:16  
A oggi, tolto quei quattro codici che ho passato, tutti gli altri son vuoti, facciamo sta cosa dividiamoci quindi tutto quello che fate qui rimane qui, quindi questo è il nostro ambiente di gioco, qua puoi puoi mettere dentro quello che vuoi.

_[immagine]_**  
Spreafico Paolo** 3:52:16  
A oggi, tolto quei quattro codici che ho passato, tutti gli altri son vuoti, facciamo sta cosa dividiamoci in gruppi, magari a fare.  
Tutto quello che fate qui rimane qui, quindi questo è il vostro ambiente di gioco.

_[immagine]_**  
Emanuele Merlo** 3:52:37  
Se magari proprio non avete degli stock o delle cose, potete scriverci e ve le creiamo noi come abbiamo fatto in Russia.

_[immagine]_**  
Spreafico Paolo** 3:52:45  
Proviamo magari tutti prendendo un codice che vabbè è del è del reparto che gestiamo normalmente a creare una checklist di produzione e a vedere cioè perché l'unico modo è fare un po' di test, anche perché adesso dobbiamo formare le persone che non erano qua adesso.

_[immagine]_**  
Emanuele Merlo** 3:52:45  
Magari tutti prendendo un codice che va beh, è andata dal fatto che ci sia normalmente a creare una checklist di produzione.  
Quindi.

_[immagine]_**  
Spreafico Paolo** 3:53:02  
Quindi.

_[immagine]_**  
Emanuele Merlo** 3:53:04  
Dobbiamo fare un po' di pratica col sistema avete qualche qualche domanda magari che o qualche c'è c'è una cosa che non abbiamo magari visto la il tipo di soft genealogy è hard è hard.

_[immagine]_**  
Spreafico Paolo** 3:53:04  
Dobbiamo fare un po' di pratica col sistema. C'è c'è una cosa che non abbiamo magari visto la il tipo di soft genealogy è hard, è hard.

_[immagine]_**  
Emanuele Merlo** 3:53:20  
So che genealogi è hard. Intanto che voi eravate, mettiamo gli atti anche questo so so è hard genealogi prendo voglio la congruenza fisica tra materiale.

_[immagine]_**  
Spreafico Paolo** 3:53:21  
Software genealogy e hard intanto che voi eravate in pausa gliel'ho spiegato. Comunque la mettiamo agli atti anche questa software hard genealogy prendo voglio la congruenza fisica tra materiale.

_[immagine]_**  
Emanuele Merlo** 3:53:38  
E quanto sparo ti ho fatto vedere prima Paolo avevo 10 pezzi, ne ho tre, non posso dichiarare 10 pezzi, al massimo ne posso dichiarare 7.

_[immagine]_**  
Spreafico Paolo** 3:53:39  
E quanto sparo gli ho fatto vedere prima Paolo, avevo 10 pezzi, ne ho ammazzati tre, non posso dichiarare 10 pezzi al massimo ne posso dichiarare 7.

_[immagine]_**  
Emanuele Merlo** 3:53:50  
Perché non ho materiale da consumare. Se avessi avuto una software generally il sistema non avrebbe detto benissimo, quel CD di qua me ne hai scaricati tre. Guardo se nella mia linea ho lo stesso materiale.

_[immagine]_**  
Spreafico Paolo** 3:53:50  
Perché non ho materiale da consumare. Se avessi avuto una software genealogy il sistema non avrebbe detto benissimo quel CD di qua me ne hai scaricati tre. Guardo se nella mia linea ho lo stesso materiale.

_[immagine]_**  
Emanuele Merlo** 3:54:08  
E vado ad erodere la giacenza di quei materiali lì.

_[immagine]_**  
Spreafico Paolo** 3:54:08  
E vado ad erodere la giacenza di quel materiale lì.

_[immagine]_**  
Emanuele Merlo** 3:54:13  
E quel discorso che abbiamo fatto stamattina, ho la mia cassetta di viti, la butto nella giostra, riesco a capire quante viti sono di un CDO di un'altro CV no e rodo sempre nella giostra.

_[immagine]_**  
Spreafico Paolo** 3:54:13  
E quel discorso che abbiamo fatto stamattina, ho la mia cassetta di viti, la butto nella giostra, riesco a capire quante viti sono di un CDO, di un'altro CDI no e rodo sempre nella giostra.

_[immagine]_**  
Emanuele Merlo** 3:54:30  
So che sono concetti un po astrusi.

_[immagine]_**  
Spreafico Paolo** 3:54:32  
Così.

_[immagine]_**  
Emanuele Merlo** 3:54:34  
In soldoni, oggi ho già riportato a casa quattro sistemi.

_[immagine]_**  
Spreafico Paolo** 3:54:34  
In soldoni, oggi cosa vi portate a casa? Quattro sistemi.

_[immagine]_**  
Emanuele Merlo** 3:54:40  
Pre modalità di gestione degli scarti.

_[immagine]_**  
Spreafico Paolo** 3:54:40  
Tre modalità di gestione degli scarti.

_[immagine]_**  
Emanuele Merlo** 3:54:44  
Buono scarto nel limbo, il limbo può diventare buono scarto o da reworkare.

_[immagine]_**  
Spreafico Paolo** 3:54:44  
Buono scarto nel limbo, il limbo può diventare buono scarto o da reworkare.

_[immagine]_**  
Emanuele Merlo** 3:54:54  
Tutto chiaro qui?

_[immagine]_**  
Spreafico Paolo** 3:54:54  
Tutto chiaro qui?  
Spero di avervi confuso le idee il venerdì pomeriggio, buon weekend a tutti.

_[immagine]_**  
Emanuele Merlo** 3:55:01  
Questi report qui ve li attivo senza problemi se volete costruirvi dei report voi.

_[immagine]_**  
Spreafico Paolo** 3:55:10  
Questo.  
Questi report qui ve li attivo senza problemi se volete costruirvi dei report voi.

_[immagine]_**  
Emanuele Merlo** 3:55:20  
C'è un corso da fare per accedere te la do io prima.

_[immagine]_**  
Spreafico Paolo** 3:55:20  
C'è un corso da fare per accedere te te la do io free.

_[immagine]_**  
Emanuele Merlo** 3:55:25  
Se invece vi serve di costruire report specifici?

_[immagine]_**  
Spreafico Paolo** 3:55:26  
Quindi ti vi attivo io se invece vi serve di costruire report specifici.

_[immagine]_**  
Emanuele Merlo** 3:55:33  
Per Don Morris che non c'è niente da fare il sabato e la domenica, però lo fa ridere.

_[immagine]_**  
Spreafico Paolo** 3:55:33  
Del buon Morris che non c'è niente da fare il sabato e la domenica può può farli completamente.  
E dobbiamo farci la password.

_[immagine]_**  
Emanuele Merlo** 3:55:46  
Anche perché te metti la percentuale di scarto, ma abbiamo solo alcune macchine che rientrano nel perimetro dei PN, ma quella personalizzazione lì possiamo fare direttamente o serve aver fatto il corso?

_[immagine]_**  
Spreafico Paolo** 3:55:47  
Anche perché te metti la percentuale di scarto, ma cioè abbiamo solo alcune macchine che rientrano nel perimetro dei PPM, ste cose qua che ve lo ve lo adottate a voi, cioè io vi do la base dati grezza, dopodiché sta a voi giocarci, ma quella personalizzazione lì possiamo farla direttamente o serve aver fatto il corso?

_[immagine]_**  
Emanuele Merlo** 3:56:06  
Allora lui?

_[immagine]_**  
Spreafico Paolo** 3:56:06  
Se abbiamo fatto il corso, allora lui.

_[immagine]_**  
Emanuele Merlo** 3:56:09  
Ha già fatto il corso, quindi siete autonomi, io vi darò anche il bellissimo foglio di Excel.

_[immagine]_**  
Spreafico Paolo** 3:56:09  
Ha già fatto il corso, quindi siete autonomi, io vi darò anche il bellissimo foglio di Excel.

_[immagine]_**  
Emanuele Merlo** 3:56:16  
Collegato in modo tale che avete la base dati sotto grezza e poi ve la ve la giocate con i filtri. OK, mi restituite, o meglio restituite a Don Paolo e a buon ritiro io.

_[immagine]_**  
Spreafico Paolo** 3:56:17  
Collegato in modo tale che avete la base dati sotto grezza e poi ve la ve la giocate con i filtri. OK, mi restituite, o meglio restituite al buon Paolo e al buon.

_[immagine]_**  
Emanuele Merlo** 3:56:30  
Ciao.

_[immagine]_**  
Spreafico Paolo** 3:56:31  
Ma perché lì, quando siamo andati?

_[immagine]_**  
Emanuele Merlo** 3:56:54  
Allora qua chiudo la registrazione.  
Su.  
Ciao, grazie.  
Vostro feedback, ragazzi.  
Ci chiudiamo.  
Questo devi, devi togliere.

_[immagine]_**  
Paolo Comparoni** trascrizione arrestata
