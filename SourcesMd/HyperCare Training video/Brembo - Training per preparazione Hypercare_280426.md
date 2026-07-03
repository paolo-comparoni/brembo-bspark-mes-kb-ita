# Brembo - Training per preparazione Hypercare_280426

> Documento sorgente: `E:\BremboDocs\HyperCare Training video\Brembo - Training per preparazione Hypercare_280426.docx`  
> Tipo: Word (.docx)

**Brembo - Training per preparazione Hypercare-20260428\_141531-Trascrizione della riunione**

28 aprile 2026, 12:15PM

1 h 34 m 12 s

_[immagine]_**  
Annalisa Casciaro** trascrizione avviata

_[immagine]_**  
Jacopo Revello** 0:03  
The event, the the system, per case, to viewer application service log.  
Of.  
Application service log.  
There are actually, you know, put the the the the the the the.  
OK, I was a tune channel, que scheme BREMBO channel, que la source la zero cinque, que pasa to para adapter, quatro, and entro chat on the terminato message.  
Uhh...  
Però diciamo che diventa molto complessa la situazione, perché andare a tracciare tutto diventa complesso. Quindi Andrea ha creato un database che raggruppa tutte queste, diciamo tutti questi log, OK?  
E l'ha messo io e l'aiutami perché non mi ricordo dove l'ha messo.  
Non ti stiamo OK, ora sì.

_[immagine]_**  
Juela Ndoka** 1:58  
Mi senti ora scusa che ho il microfono CNMDB quality quello espandi.  
Perché?

_[immagine]_**  
Jacopo Revello** 2:09  
Perché non ce l'ho accessibile, aspetta.  
Devo ricordarmi dove l'ha messa, però qua va bene, qua sulla 14 dovrebbe andare bene, sì.

_[immagine]_**  
Juela Ndoka** 2:18  
Mio è Ivan, il primo, il primo di bio.

_[immagine]_**  
Jacopo Revello** 2:21  
OK.  
Come vedete qua Andrea ha riportato esattamente quello che c'è nell'event viewer, solo che ce l'abbiamo di tutte le macchine e quindi già questo potrebbe essere utile quando dovete fare una reverse Engineering per capire dove si è rotto, no?  
Quindi banalmente non ha chiamato il comando, quindi non vedete nulla sul persistent log. Potete andare a vedere qua cosa cosa si è rotto. Per esempio qua c'è un error. Possiamo andare a vedere un error qua ti dice che il workload s'è s'è s'è stop.  
Batto? No, allora andiamo indietro, andiamo a vedere cosa ha fatto. Stava facendo, stava chiamando un container Type.  
Ta ta ta.

_[immagine]_**  
Fabio Massone** 3:13  
Magari devi filtrare sulla macchina per avere gli eventi di quella macchina.

_[immagine]_**  
Jacopo Revello** 3:18  
Ma no, in realtà dovrebbero essere ordinati. Poi se ricordo bene da qualche parte fatemi vedere. Esatto, c'è.  
No, questo è XML.  
OK, c'è un record ID che se voi lo organizzate per record ID forse potreste anche perciò se fate order by computer name e record ID avete la lista completa uno dietro l'altro.  
Però vi dico, è molto complesso andare a vedere tutto questo, quindi però è giusto, cioè ce l'abbiamo di preciso adesso tutti i dettagli io non li so precisamente. Sicuramente Alessia su questo può essere.  
Più chiara di me nella nella spiegazione, però in generale la logica è guardo su Connect mom, se vedo un errore su Connect mom e vedo che l'errore è parlante rimango lì, se invece vedo che l'errore non è parlante mi prendo.  
L'orario in cui è successo quel problema e vado ad analizzare su questo database per vedere dove.  
Dove si è rotto e perché si è rotto, no?  
Però prima di andare a vedere meglio nel dettaglio Connect mom volevo un attimo vedere le cose che ci ha riportato Emanuele, perché Emanuele ha riportato alcuni alcuni problemi che ha ricevuto oggi su durante i training e volevo un attimo capire.  
Insieme, così analizziamo anche insieme gli errori, no?  
Allora qua vedo problemi di refresh a seguito di una nazione di scarto sul prodotto finito il indicatore dell'interfaccia è rimasto invariato. Sembra che siano problemi di refresh sugli sugli altri campi quindi.

_[immagine]_**  
Emanuele Merlo** 5:15  
Sì, dopo l'indicazione, scusa.

_[immagine]_**  
Jacopo Revello** 5:19  
No, tranquillo quindi se ho capito bene, se capisco bene da quello che dici, i contatori lì in cima alla repetitive non erano aggiornati, giusto?

_[immagine]_**  
Emanuele Merlo** 5:19  
Prosegui, prosegui.  
Esatto, sì, questa è una cosa che si vede abbastanza facilmente.

_[immagine]_**  
Jacopo Revello** 5:31  
Allora?  
Certo no, ma quello lì è un baco noto, nel senso che purtroppo c'è un baco già aperto da ostrava che quando faccio lo scarto questa quantità non si aggiorna ma se entro e riesco scusa se esco e rientro sì si aggiorna quindi è solo un problema di refresh del dato.  
Un banco note dobbiamo dobbiamo risolvere in realtà incarico AMS. Però vabbè se abbiamo tempo lo risolviamo, sennò vediamo un attimo AMS quando lo risolve e va bene. Questo è un qualcosa di noto e lo sapevamo già.

_[immagine]_**  
Emanuele Merlo** 6:03  
Sì, ho segnalato tutto perché poi su tutto quello che si può risolvere perché magari poi su impianto si impuntano.

_[immagine]_**  
Jacopo Revello** 6:06  
Va benissimo.  
Mismatch utente fasullo il sistema OK, questo qua ti dice che non poteva, non poteva essere completato. Sì, esatto, non poteva.

_[immagine]_**  
Emanuele Merlo** 6:19  
No, sì, completa, sì completato. Ma non era stato cambiato l'utente. Chi l'aveva aperto era chi stava cercando di chiuderlo. Era un ordine di cutting. Non ti so però dire di preciso qual era il workout.

_[immagine]_**  
Jacopo Revello** 6:27  
Mi sai dire?  
Non sai qual era workorder, sai qual era la macchina?

_[immagine]_**  
Emanuele Merlo** 6:34  
E no, perché?

_[immagine]_**  
Juela Ndoka** 6:37  
Tanto il work center perché è lì, cioè che abbiamo il Flag.

_[immagine]_**  
Emanuele Merlo** 6:41  
Potrebbe essere GUGCL. Devo recuperare adesso guardo se mi danno la registrazione così ti dettaglio tutto con più precisione. Stavo prendendo le cose al volo pian piano che andava avanti.

_[immagine]_**  
Jacopo Revello** 6:41  
6\.  
OK, allora aspettiamo che guardi quello e vediamo.

_[immagine]_**  
Emanuele Merlo** 6:57  
Sì.

_[immagine]_**  
Jacopo Revello** 7:02  
In generale questo mi è successo l'altra volta, il problema era che semplicemente non si era refreshata bene la pagina una volta che refreshavi funzionava.

_[immagine]_**  
Emanuele Merlo** 7:09  
Infatti anche oggi abbiamo risolto così.

_[immagine]_**  
Jacopo Revello** 7:11  
OK va bene, però se mi dici qual è andiamo a vedere un attimo i dati, in realtà qua c'è l'i d del work order possiamo provare a prenderlo da quello.

_[immagine]_**  
Emanuele Merlo** 7:16  
OK.

_[immagine]_**  
Jacopo Revello** 7:23  
Allora seleziona il contenitore che due voci riguardanti lo stesso ID.

_[immagine]_**  
Emanuele Merlo** 7:28  
Sì, praticamente quando c'era la selezione del contenitore, lo stesso contenitore era presente due volte.

_[immagine]_**  
Jacopo Revello** 7:34  
Ma cosa cosa intendi sulla selezione del contenitore, dove, in che?

_[immagine]_**  
Emanuele Merlo** 7:38  
Quando fai lo start dell'ordine?

_[immagine]_**  
Jacopo Revello** 7:42  
E che contenitore selezioni?

_[immagine]_**  
Emanuele Merlo** 7:43  
Sped.  
No, nel senso non è non è importante, cioè aspetta.

_[immagine]_**  
Juela Ndoka** 7:48  
Coltainer Type, scusa Jacopo.

_[immagine]_**  
Emanuele Merlo** 7:50  
Sì, contener Skype.

_[immagine]_**  
Jacopo Revello** 7:52  
Container Type OK, è sempre lo stesso, lo stesso. Cosa stavate facendo? Assemblaggio, cosa stavate facendo?

_[immagine]_**  
Emanuele Merlo** 8:00  
Ha saltato 2 3 cose diverse, adesso poi te lo te lo dico.  
Anche in un'altra cosa.

_[immagine]_**  
Juela Ndoka** 8:05  
Però potrebbe essere che ho visto che ci sono due ID identici e una volta Francesca aveva detto che avevano mandato dei container Type che erano sbagliati e poi non so se hanno mandato un isdeleted io lo sto dicendo isdeleted però dovevano essere cancellati.

_[immagine]_**  
Jacopo Revello** 8:20  
No, sì.

_[immagine]_**  
Juela Ndoka** 8:22  
E quindi sono rimasti, quindi cioè sono veramente identici, però sono con data di creazione diversa, quindi potrebbe essere quello il caso.

_[immagine]_**  
Jacopo Revello** 8:32  
Allora tanto quello lo possiamo vedere subito, non ti ricordi neanche se eravate su Curno su Mapello, Emanuele.

_[immagine]_**  
Emanuele Merlo** 8:38  
Eravamo su Curno.

_[immagine]_**  
Jacopo Revello** 8:40  
Perfetto, allora quello lo vediamo subito. Andiamo a vedere i container Type. Allora i container Type.

_[immagine]_**  
Emanuele Merlo** 8:40  
Sì.

_[immagine]_**  
Jacopo Revello** 8:47  
Andiamo qua, mettiamoci un centinaio così ce l'abbiamo tutte, se ordiniamo per name vediamo che per lo stesso nome ne abbiamo n.  
OK, quindi ci può stare che lui ne abbia visti due, perché noi di per sé quando andiamo a fare la.  
La query noi estraiamo tutto e mostriamo solo il nome. Il problema è appunto, come diceva Juela, che lato lato WM ci hanno mandato 100.000 volte la stessa cosa perché han fatto casino, quindi dovremmo fare un po' di pulizia qua.  
Io mi ero ripromesso che a Francesca gli avrei mandato un export di queste informazioni, ma non me lo sono, non l'ho più fatto. Però vabbè, di per sé il problema secondo me è semplicemente questo, non sono duplicati.  
Duplicati reali, ma sono duplicati, o meglio, non sono duplicati falsi, ma sono duplicati reali perché ci abbiamo del dato duplicato. Però la duplicazione qua se vedete non è una duplicazione sull'identifier perché l'identifier è a chiave univoca e non può essere duplicato.  
Il problema è che quando noi riceviamo un container Type, noi riceviamo un identificatore che è un identificatore generico che non usa nessuno, usiamo solo noi.  
Il name che corrisponde al nome del materiale che l'imballaggio è una description che dà informazioni sul tipo di materiale di imballaggio che si sta utilizzando. No, quando andiamo dentro noi abbiamo anche l'associazione AI materiali che.  
Possono entrare su ognuno di questi container Type. Come vedete possiamo averne più di uno e ognuno di questi avrà una Max quantity, no? Quindi il problema qual è? Che se noi avessimo 2 2 container Type con lo stesso nome.  
Per gli stessi materiali potrebbe succedere molto molto facilmente che abbiamo un duplicato, ora se riusciamo a recuperare qual è l'ordine ci togliamo un pensiero.  
Però.

_[immagine]_**  
Emanuele Merlo** 11:01  
Tanto adesso cerco di recuperare tutto, dettaglio, dettaglio meglio tutto. Ho buttato giù gli appunti perché tra l'altro quando si verificavano ste cose mi chiedevano a me di dire cosa stava succedendo e mentre scrivevo dovevo anche inventarmi qualche cosa da dirgli.

_[immagine]_**  
Jacopo Revello** 11:04  
Va bene?  
Va bene, no me interessa.  
Ok, allora?

_[immagine]_**  
Juela Ndoka** 11:18  
Allora sembra duplicato scusa Jacopo che cioè però se Apri il pannello le nelle colonnine c'è la possibilità di ingrandirli e di spostarli e quindi se li ingrandisci poi vedi anche le altre colonne.  
Cioè anche altri dettagli e da lì capisci che non sono veramente duplicati, magari Elena ID duplicato però le altre informazioni.  
Son diversi.

_[immagine]_**  
Jacopo Revello** 11:46  
Cosa voglio vedere se ne trovo uno così ad \*\*\*\*\*\*\*?

_[immagine]_**  
Juela Ndoka** 11:48  
Sì.  
E poi seleziona il.

_[immagine]_**  
Jacopo Revello** 11:52  
No, vedi, qua ce n'è solo uno.

_[immagine]_**  
Juela Ndoka** 11:54  
C'è solo uno, quindi non è questo il caso, però vedi che le colonne li puoi.

_[immagine]_**  
Jacopo Revello** 11:58  
Sì, no, ma io lo io lo so, però.

_[immagine]_**  
Juela Ndoka** 12:01  
Sì, lo so, però lo so che lo sai però per le altre.

_[immagine]_**  
Jacopo Revello** 12:05  
Sì, vabbè, comunque in generale per ingrandirli basta fare così.  
Comunque in generale sì, cioè piuttosto.  
OO possiamo si può ingrandire questa che secondo me è la soluzione migliore. Possiamo anche pensare noi di ingrandirla Juela magari teniamocelo come.

_[immagine]_**  
Juela Ndoka** 12:28  
Dai, facciamo un pannello più grande per questo.

_[immagine]_**  
Jacopo Revello** 12:31  
Sì, cioè magari lo facciamo leggermente più largo, così lo vedono bene, perché?

_[immagine]_**  
Emanuele Merlo** 12:36  
Perché gli operatori poi non possiamo chiedere di grandire?

_[immagine]_**  
Jacopo Revello** 12:38  
Sì, non si mettono lì, però così se riuscissimo a farlo così ce lo prendiamo in carico e lo mettiamo un po' più grande. Si può fare, no? Juve no.

_[immagine]_**  
Juela Ndoka** 12:51  
Sì, certo.

_[immagine]_**  
Jacopo Revello** 12:52  
OK, va bene.  
OK, però in generale come vedi qua non ne ho duplicati, no? Quindi non è un problema, non è un buck o UI, è un problema di dati sporchi.  
Molto probabilmente vediamo se ne troviamo un'altro.  
Tipo questo.  
Vediamo se c'è qualcosa, questo è duplicato.

_[immagine]_**  
Emanuele Merlo** 13:18  
Sì.

_[immagine]_**  
Jacopo Revello** 13:19  
OK, per esempio questo se noi adesso.

_[immagine]_**  
Juela Ndoka** 13:21  
Rispondi un po lì di.

_[immagine]_**  
Jacopo Revello** 13:24  
Se noi andiamo a vedere vedi l'i D è diverso, descrizione è la stessa, nome è lo stesso, ma l'i D è diverso OK, questo purtroppo non ci possiamo fare poco, nel senso che loro ce l'hanno mandato due volte con due ID diversi con la stessa variante.

_[immagine]_**  
Emanuele Merlo** 13:27  
Sì.

_[immagine]_**  
Jacopo Revello** 13:40  
E quindi per noi non ci possiamo fare molto, no ora.

_[immagine]_**  
Emanuele Merlo** 13:47  
Ma dovrebbe essere chiave primaria, variante e coso a prescindere da lino.  
Non vorrei che poi ce lo girassero.

_[immagine]_**  
Jacopo Revello** 13:54  
Ha sbagliato?  
Però tanto questo lasciami perché non mi non riesco a.  
Fammi un po' fare così. Son d'accordo. Sì, è vero, ma lasciami dire, questo è un problema che c'è da sempre, allora. Cioè non è che noi abbiamo fatto nulla qua, no? Quindi da un certo punto di vista no, ma era.

_[immagine]_**  
Emanuele Merlo** 14:15  
Sì, ma io tengo per noi, non è che sto solo facendo l'avvocato del diavolo, perché poi ci dicono, ma.

_[immagine]_**  
Jacopo Revello** 14:22  
No, ma è giustissimo, è giustissimo, è pur, è pur parlè per tutti, nel senso che in generale il discorso è un qualcosa che abbiamo sviluppato noi. Sì, e allora è giusto che lo andiamo a indagare, andiamo a capire. È un qualcosa che non abbiamo sviluppato noi e che ce lo siamo trovati così.  
Da un certo punto di vista.  
Qualcuno ha sbagliato da qualche parte e noi non possiamo ereditarci anche problemi degli altri. Detto questo, io qua vedo che.

_[immagine]_**  
Emanuele Merlo** 14:48  
Certo.

_[immagine]_**  
Jacopo Revello** 14:53  
Fondamentalmente ci sono questi due, anche questo è duplicato, per esempio.  
E però qua adesso è solo da dire a loro di pulirsi un po II dati, cioè?  
OK, va bene, pensavo peggio. Ottimo. Impossibile impostare il contenitore per scarto in fase due durante un recorrido samplical voleva fare una dichiarazione di scarto in fase due, non era possibile selezionare il cartone, pensieri dice che deve essere possibile.

_[immagine]_**  
Emanuele Merlo** 15:17  
Allora?

_[immagine]_**  
Jacopo Revello** 15:25  
Spiegamelo un attimo.

_[immagine]_**  
Emanuele Merlo** 15:25  
Non ho capito bene cosa volesse fare, quindi non ti posso essere d'aiuto. Però stava cercando di dichiarare uno scrap in fase due e voleva selezionare cassone da quale non mi ricordo adesso.  
Se erano in pare fosse materiale in ingresso, forse è possibile, voleva comunque selezionare un cassone su come devo.

_[immagine]_**  
Juela Ndoka** 15:51  
Allora i cason.

_[immagine]_**  
Jacopo Revello** 15:52  
Qua nella pagina di scarto.

_[immagine]_**  
Emanuele Merlo** 15:54  
Sì.  
Aspetta che chiedo lumi.

_[immagine]_**  
Juela Ndoka** 15:59  
Ma questa cosa non.

_[immagine]_**  
Jacopo Revello** 15:59  
Io qua non è mai successo.

_[immagine]_**  
Juela Ndoka** 16:03  
No tipo.

_[immagine]_**  
Jacopo Revello** 16:05  
No, qua non è mai, cioè non è mai esistita sta roba non so da dove se la sia, se lo sia inventato no, ma sai secondo me cosa ha sbagliato lui che pensava di fare uno scarto di componente e quindi lui magari si aspettava di vedere il contenitore qua.  
E quindi qua lo vede.  
Ha sbagliato pagina, probabilmente.

_[immagine]_**  
Emanuele Merlo** 16:26  
Può, può essere, può essere U mi riservo di indagarlo meglio.

_[immagine]_**  
Jacopo Revello** 16:32  
OK, va bene.  
Va bene OK quindi vabbè questo è missmatch original batch allora questo è abbastanza va bene tralasciando che il messaggio potrebbe essere più bello e mi va bene scusate questo qua il.

_[immagine]_**  
Emanuele Merlo** 16:37  
Sì.  
Sì, qua in realtà la segnalazione era un'altra, cioè se non può essere utile riuscire a capire a quale original batch appartiene il materiale in qualche vista praticamente non so se è in produzione no use case Real.

_[immagine]_**  
Jacopo Revello** 17:04  
Ma loro allora in vista ci cioè tutte queste informazioni, nel database c'è tutto in nella etichetta che loro hanno.  
C'è l'original batch, c'è scritto OK, quindi loro vedranno l'original batch qua il motivo quale l'errore cosa dice only to be consumed material assigned to an original batch can be scanned. Quindi gli sta dicendo fondamentalmente.  
Guarda che solo II contenitori che hanno un original batch possono essere scansionati, io qua ho fatto un controllo, vedo che non c'è un original best associato.  
E quindi ti sto dicendo semplicemente guarda che devi darmi un contenitore che abbia un original batch.  
Cosa può essere successo? Che quando voi avete fatto la dichiarazione il contenitore doveva arrivare tramite Shadow movement, non è arrivato, è stato creato, suppongo, tramite uno stock manuale.

_[immagine]_**  
Emanuele Merlo** 18:12  
Non l'abbiamo fatto oggi e no, però probabilmente era quello che era successo, che è stato creato manualmente senza original batch.

_[immagine]_**  
Jacopo Revello** 18:12  
Non lo so.  
OK, di conseguenza quando in realtà quando questione viene creato non gli viene assegnato un original batch, ma c'è un processo di AWM che sta dietro che si chiama CFL MAS che fondamentalmente quando viene generato associa.  
Un original batch e un cassone, questo ve lo faccio vedere perché è molto importante. Poi continuiamo con gli errori, se noi andiamo qua su Connect mom di nuovo e ci.  
Cerchiamo il CLF mass con F mass response OK, vediamo che ne otteniamo un fracasso. Tralasciate gli errori che adesso sono errori dovuti al fatto che ci mandano il CLF mass vuoto, nel senso che.  
Ve lo faccio vedere quando loro ci mandano il CFL mass.  
Plugin Jason no XML tool Pretty print.  
Qua fondamentalmente ci dovrebbe essere un campo, un segmento che si chiama original batch, no, questo segmento viene estratto dal dal Connect mom e passato a un comando che si chiama.  
Apsert original batch, qualcosa del genere dove fondamentalmente ci viene detto qual è l'original batch o al batch d'origin al batch, chiamiamolo del cassone.  
Quindi fondamentalmente lui ci dice, questo è l'original batch, questo è il batch chiamato Natural Batch del cassone, questo è il suo original batch associato, in questo modo quando tu vai a fare la scansione, tu riesci a fare un'associazione diretta.  
Cosa succede? Questo clf must ci viene mandato ogni qualvolta il match viene aggiornato e il problema qual è? Che ci viene mandato sempre. Quindi voi qua vedete 1 1 sfracello di errori perché tutte le volte loro ce lo stanno mandando.  
Senza l'original batch. Infatti, giusto per tornare a quello che dicevamo prima sulle l'analisi di Connect Moms, se noi andiamo a vedere la response e vediamo, andiamo in fondo, vediamo che la response cosa dice prendiamocela così lo vediamo.  
Plugin Jason viewer format Jason qua no metti facciamo vediamo se mi fa un Pretty print un po' più carino non me lo fa va bene qua cosa ci sta dicendo la response di Connect mom? Il messaggio è validation.  
Command e ci dice qual è il Command che ha fallito, OK reason the original batch field is required, the expiration that field is required. Quindi fondamentalmente loro ci stanno mandando due informazioni, the original batch and the expiration, che sono nulle.  
O sono mancanti e di conseguenza il sistema si rompe perché gli dice mi aspetto che ci sia un qualcosa, OK, quindi in realtà io adesso ho fatto una piccola modifica al codice in modo che tutte le volte che ci arriva la CLF MAS.  
Non va in errore per un original batch mancante, ma semplicemente dà un warning dicendo il CLF mas non è vuoto, però almeno non ti dà gli errori e quindi non abbiamo il persistent log pieno di errori però in generale.  
Quando ci arriva questa roba qua che è una cosa asincrona, OK, quindi è una cosa che non è sotto sotto un evento specifico, ma è una cosa del tutto asincrona che ci arriva ogni tot. Questo fa l'associazione diretta. Quindi cosa può essere successo? Che il batch è stato creato, ha fatto tutto.  
Ma non c'è mai arrivato il CLF MAS non essendoci arrivato il CLF MAS, quando loro han fatto la scansione dell'oggetto ti dice che quell'oggetto non ha un original batch associato OKE va bene.

_[immagine]_**  
Fabio Massone** 22:21  
Scusa, non ho capito una cosa, cosa c'è? LF mass sarebbe un messaggio che ci viene mandato ogni volta che noi produciamo.  
Qualcosa perché?

_[immagine]_**  
Jacopo Revello** 22:32  
No, ci viene mandato ogni volta che loro fanno un aggiornamento del batch, qualunque tipo di aggiornamento, che sia semplicemente che hanno messo uno spazio da qualche parte o che.  
Abbiano creato il batch o che qualunque cosa sia, fondamentalmente quello che succede è che loro generano questo CLF mass e quindi ce lo generano sempre, anche quando l'originale Batch non è ancora stato assegnato.  
OK, cioè anche banalmente quando crea un ordine lui crea un batch alla creazione dell'ordine a noi ci arriva un CLF mask che ci dice ho creato questo batch, quando poi noi facciamo una complete che quindi.  
Aggiorniamo quel batch, ci arriva un CLF must con l'aggiornamento del batch solo quando il original batch viene associato a quel batch, allora il.  
Il CLF mass sarà scritto correttamente, quindi andrà a buon fine.  
OK.

_[immagine]_**  
Fabio Massone** 23:39  
Perché attualmente Channel mom riceveva il messaggio e chiamava comunque il pre check.  
No, ho detto 111 cavolata.

_[immagine]_**  
Jacopo Revello** 23:48  
No, non sì, chiama chiama no. Aspetta allora il pre check lo chiami nel momento in cui scansioni, OK?

_[immagine]_**  
Fabio Massone** 23:50  
E non chiama Nada.  
Esatto, sì, allora non chiamava il comando di appcert perché non richiedeva.

_[immagine]_**  
Jacopo Revello** 24:02  
No il CN mom no aspetta il CN Mom chiama il comando di Appsert e infatti se noi andiamo a vedere la response ti dice ho chiamato il ho chiamato il comando Appsert Batch Traceability ma il comando mi ha risposto con questo.

_[immagine]_**  
Fabio Massone** 24:12  
OKOK, sì.  
Ma mancano quei due campi, OK, sì.

_[immagine]_**  
Jacopo Revello** 24:18  
OK, che è corretto, è giustissimo, nel senso che il comando ve lo faccio vedere così faccio vedere anche cosa ho cambiato giusto per avere tutti la aspetta che devo fare un po' di zoom out perché sennò divento scemo. Datemi un attimo che se.  
Si adatta alla macchina.  
OK, allora il comando di Appsert original batch è qua. OK, il comando di Appsert original batch. Questo è quello che ho aggiunto io. Se voi andate a vedere non fa altro che andarsi a prendere.  
Il native batch, che è quello che dicevo, dicevo, è il batch dell'oggetto, il materiale per cui stiamo andando a produrre, cioè o meglio il materiale contenuto in quel container, va a vedere su questa tabella se esiste un'associazione.  
Va a scrivere tutto e poi fa fare una submit va in errore perché quando vado a fare la submit io gli sto mettendo original batch e expiration data nulle OKE quindi essendo che questa tabella ha quei due campi mandatory.  
Quindi non nullable, il submit fallisce quello che io ho messo giusto per avere meno ridondanza, meno errore, semplicemente nel caso in cui l'original Batch è mancante.  
Allora vado a scrivere che non ci sono stati aggiornamenti perché l'ho fatto solo su questo, perché se per caso mi arriva l'Original Batch ma non c'è l'expiration date, io voglio che scoppi perché l'expiration date.  
Mi serve che mi arrivi a prescindere, non posso non scriverlo. Significa, cioè significherebbe che io gli ho associato un original batch ma non gli ho messo un expiration date e quindi di conseguenza deve andare in errore. Se invece l'original batch manca, quindi non c'è stato proprio l'assegnazione, mi va anche bene uscire senza nessuna senza aver fatto nulla, perché di per sé.  
Questo comando ha l'unico obiettivo di fare l'associazione native batch con original batch, quindi se manca l'original batch esco, se invece manca qualunque altro delle cose deve darmi un errore. OK, adesso questo è già in produzione, quindi mi aspetto che dalla.  
Tutte le volte che ci arriverà un oggetto che è nullo empty the original batch questa roba qua mi manderà questo warning e basta. L'ho messo a livello di warning così almeno ce l'abbiamo sul persistent sul log uno però di per sé almeno.  
Riduciamo un po gli errori, OK?  
Torniamo un attimo ai problemi che ha visto Emanuele, OK, questo qua colonna initial quantity current quantity, questo è il solito panzeri che scopre cose di.

_[immagine]_**  
Fabio Massone** 26:58  
Tu una cosa hai, ma questo modifica l'hai testata?

_[immagine]_**  
Jacopo Revello** 27:03  
No.

_[immagine]_**  
Fabio Massone** 27:04  
Perché in realtà è required proprio come campo del comando, quindi secondo me questo errore qua viene lanciato quello che non ci entra neanche nel comando, quindi ho paura che continueremo ad averlo perché ho visto adesso dal model che è required.

_[immagine]_**  
Jacopo Revello** 27:19  
OKOKE.

_[immagine]_**  
Fabio Massone** 27:20  
Sono required su expiration date che original batch, quindi o si mettono optional.

_[immagine]_**  
Jacopo Revello** 27:24  
Allora potrebbe essere potrebbe essere quello? Sì, io non l'ho testata perché era un controllo e visto che devo fare per forza un deploy per risolvere dei problemi di AGV l'ho l'ho messo su tanto non dava fastidio a nessuno.

_[immagine]_**  
Fabio Massone** 27:29  
Certo.  
E no, sì, ma io l'ho controllato, mi sembrava di ricordare da taster tour che quelli lì fossero in violetto, quei due campi lì, quindi purtroppo vedi che infatti è sempre qua.

_[immagine]_**  
Jacopo Revello** 27:43  
OK, allora già.  
Già già che ci sei magari aggiorniamolo almeno l'original batch vabbè mettilo anche l'expiration date mettilo note required e poi semmai guardiamo il null o l'empty anche dell'expiration date no mettili note required questi due.  
Original box expiration date, gli mettiamo no tre quired e poi così almeno usciamo senza problemi, OK?

_[immagine]_**  
Fabio Massone** 28:15  
Va bene ovviamente su DAB 0 1 no?

_[immagine]_**  
Jacopo Revello** 28:17  
Sì, check in su DEV 0 1, poi vediamo se fare un'altro deploy o no. Va bene l'ultimo. L'ultima cosa che ci ha segnalato Emanuele è semplicemente panzieri che scopre che gli mancano delle cose sulle pagine di prodotto, ma queste sono pagine di prodotto, quindi non mi rompe le palle.  
Se le tiene così e semmai ci fa una CROK detto questo glielo dico io senza nessun problema a Carlo.

_[immagine]_**  
Emanuele Merlo** 28:37  
Va bene?  
No, in realtà in realtà gliel'ha chiesto un.  
Un del uno dell'officina della degli.  
Dello shop floor, ma va bene, anche lui aveva sta curiosità.

_[immagine]_**  
Jacopo Revello** 28:55  
Va bene.  
OK, sei mica riuscito a recuperare gli ordini lì sopra qualcosa?

_[immagine]_**  
Emanuele Merlo** 29:02  
No, non ancora. Guarda, voglio recuperare la registrazione ma me la devono shareare loro e così poi ti faccio un report più dettagliato.

_[immagine]_**  
Jacopo Revello** 29:11  
OK va bene comunque in generale diciamo che i problemi che hai trovato sono brutti però al contempo sono no sono cose che sappiamo. L'unica cosa che non mi quadra è sta roba qua di container di scarto però vorrei un attimo capirlo con se riesci a scrivergli semplicemente 1 1 domanda a panzeri.  
Per chiedergli che \*\*\*\*\* voleva fare così. Poi semmai gli rispondo io, OKOK va bene. Detto questo, torniamo un attimo a noi, io fra poco, poi fra un quarto d'ora vi devo lasciare con un'altra call, ma giusto per darvi un piccolo un minimo di infarinatura.

_[immagine]_**  
Emanuele Merlo** 29:35  
OK.

_[immagine]_**  
Jacopo Revello** 29:48  
Del Connect mom giusto per capire come ci si muove eccetera. Allora quando ne aprite Connect Mom ci sono queste tre pagine principali, adapter configuration, General Configuration e System Diagnostic OK.  
L'adapter configuration è quello che noi utilizziamo per esporre delle chiamate APIA terze parti. OK, ci sono diversi tipi di chiamate che si possono fare. In particolare noi usiamo le web API.  
Per tutti i messaggi che vengono da fuori e devono arrivare verso p center. Come vedete noi qua abbiamo quattro adapter diversi con i corrispettivi backup. In realtà questo è super ridondante, ha poco, ha poco utilità però.  
Visto che ha la stessa configurazione di ostroval l'abbiamo lasciato l'adapter cosa cos'è fondamentalmente è un endpoint che viene esposto a all'esterno e viene serve per.  
Dire al AA chi deve chiamarci, guarda che sono io che prendo in carico la tua richiesta, no, ne abbiamo quattro perché noi abbiamo quattro macchine di Foundation e quindi in questo modo andiamo a parallelizzare le varie chiamate.  
Il motivo del backup è che Sconnect mom ha due macchine in ARR no la 0 5.  
E la 0 6 OK più abbiamo la 0 7 che è viene entra in si attiva nel momento in cui la 0 5 o la 0 6 vanno giù è un backup del backup fondamentalmente quindi le due macchine principali sono la 0 5 e la 0 6.  
Gliadapternonvengonoespostidirettamentecosimavengonoespostitramiteloadbalancerquindifondamentalmentequandoiovadoafareunachiamatacomevedeteioglidico.it QLTMS adapter generico.  
ITQLT MES adapter generico e poi message OK, il message avrà un body. Una volta che io faccio faccio la chiamata il sistema mi risponde dicendomi OK, io ho preso in carico la tua chiamata.  
E l'ho l'ho eseguita. Se poi andiamo a vedere sulla sulla come vi ho fatto vedere prima sulla system diagnostic, noi possiamo andare a vedere chiamata per chiamata.  
Qual è l'adapter che è entrato in gioco? OK, quindi vedete, c'è adapter uno B, adapter quattro, adapter uno variano un po' a livello di configurazioni. Come sono stati fatti? Fondamentalmente è stato messo un adapter configuration.  
OK che ti dice semplicemente qual è l'utente da utilizzare, qual è il dominio da utilizzare e semplicemente alcune informazioni per la gestione del delle chiamate e poi in additional configuration ti fa vedere.  
Qual è la macchina che viene che viene chiamata in questo caso? Come vedete c'è un QFX all. Perché? Perché le Foundation sono anch'esse gestite tramite load balancer. Quindi cosa succede? Io chiamo lo.  
Tramite la chiamata diretta chiamo il Load balancer per decidere qual è l'adapter. Lui decide qual è l'adapter da chiamare. Una volta che decido l'adapter, il Load balancer decide qual è la Foundation da chiamare. In questo modo, essendo tutte macchine in ARRE gestite da un load balancer, ho la ho la certezza che.  
Posso andare in parallelo con più chiamate? OK la configurazione standard per tutti, quindi se io vado su clicco su qualunque come vedete non cambia niente OK perché la configurazione standard per tutti?  
Una cosa molto importante, come vedete il scusate ho sbagliato, il Wake up interval è a -1 perché non ci sono retry e quindi fondamentalmente i retry sono tutti gestiti da CPI sia in ingresso che in uscita e quindi noi qua abbiamo fatto in modo che non.  
Non si svegli mai nel momento in cui fallisce, fallisce e ce lo perdiamo.  
L'altro adapter, l'altro scusate, cosa importante che noi utilizziamo sono le web API client, ossia in questo caso noi facciamo da server, quindi stiamo in ascolto di un client che ci chiama, in questo caso invece noi facciamo da client e come vedete sono tutte le chiamate che.  
Dal MES vanno verso l'esterno. La differenza è che fondamentalmente noi siamo noi qua a fare la chiamata, quindi simuliamo come se lo facessimo da postman. Qua abbiamo un server URI che è la destinazione della delle PI. Come vedete ognuna c'ha.  
Il server URI diverso.  
E anche qua abbiamo messo Wake up integral al -1 perché anche in questo caso, per quanto sbagliato, però è stato deciso così, anche in questo caso abbiamo il -1 perché non gestiamo retry, è tutto gestito da CPI.  
Come vedete qua noi non abbiamo messo nessun mom connection name perché non dobbiamo cambiare Foundation ma dobbiamo andare verso l'esterno e quindi infatti cosa facciamo? Andiamo a chiamare direttamente il l'esterno a livello di.  
Settaggi la cosa importante che a voi interessa è sapere è in che modo ci andiamo a autenticare. Stiamo usando una basic perché la gestione dei token non funzionava, mentre su Ostrovy è gestito tramite token di autenticazione. Qua abbiamo dovuto usare la basic perché non funzionava. Il token però cambia poco.  
Dove c'abbiamo un username e una password fisse che vengono utilizzate per chiamare l'a PI OK.  
Tutti i messaggi che in ingresso in uscita hanno un loro message Type che ha determinate configurazioni che spiegano come il messaggio deve essere gestito, quindi fondamentalmente prendiamo per esempio.  
La CK material call, che è una delle chiamate che CPI fa verso di noi quando ci dà un feedback, fondamentalmente cosa succede qua ti dice deve avere questo nome qua.  
La dispatcher rule è un fifo, quindi fondamentalmente il primo che arriva viene processato.  
A priority è standard, si può decidere anche di prioritizzare dei messaggi piuttosto che di altri per fare in modo che dare priorità a qualche cosa, ma ad oggi non c'è questa gestione e si usa un broker di spaccio e quindi fondamentalmente una chiamata diretta. Il tipo di Converter.  
Serve per convertire quello che viene scritto, in questo caso è interfer format, quindi lascia scusate infer format, quindi lascia esattamente il formato che c'è OK, quindi ce lo mandano, noi ce lo.  
Sappiamo e come vedete l'attribute contiene determinate informazioni tra cui il Plant, quindi va a asportare il Plant e quale comando stiamo andando a chiamare OK quindi qua.  
Come vedete lui cosa fa? Estrae dal who number qual è il plant? Qua c'è un mapping diretto fra plant in codice e plant su OP Center. Sulla base di questo decide dove instradare la richiesta e poi una volta che l'hai trovato chiama il worker.  
Con questo comando qua per andare a fare la chiamata su quel worker OK.  
Nulla di più. Tutto lì e di nuovo qua stiamo sempre retry interval time l'abbiamo messo a zero perché almeno non facciamo retry e è tutto standard il workflow.  
È un sistema che si può utilizzare per andare a manipolare il messaggio, ma noi in questo caso usiamo un workflow diretto che non fa altro che chiamare direttamente il comando passando dall XML in input OK.  
Ognuno di questi messaggi, come vedete, ha un corrispettivo map, il mapping non sono altro che degli XSD che vengono utilizzati per interpretare il messaggio e fare una prima controllo sul contenuto del messaggio.  
Cioè se noi andiamo a vedere per esempio la CK staging call, noi vediamo che qua ci sono alcune informazioni e se andiamo a per esempio AA simulare un messaggio qualunque tipo questo.  
Se facciamo il test mapping lui ci fa vedere come questo messaggio viene interpretato e quindi in che modo viene passati i dati, quindi gli stiamo dicendo che al comando noi passeremo degli tre input che sono l'external System ID che è un guid, il call Type.  
Che è 0 3 e lo status indicator che è tre OK, quindi anche se nell XML ci mettessi altre n cose OK, cioè se io banalmente ci mettessi anche.  
Aspettate che non me lo fa modificare, aspettate che lo faccio un po più grande.  
Perché non me lo fa? Devo far così. Se io mi prendessi per esempio questo glielo butto sul mapping e qua ci mettessi, che ne so?  
Pippo, OK.  
Non succede niente nel senso che se io faccio di nuovo il test mapping lui Pippo me lo lascia indietro perché non esiste nessun XSD che mi estrae il valore Pippo OK quindi lato XML e questo ne parlo, cioè lo dico anche per Annalisa, Giacomo, Giada eccetera.  
Tutte le modifiche che noi stiamo facendo ad oggi su Italia che verranno già sono già state ereditate in parte da Ostravajgava perché SAP è un ambiente unico e quindi tutte le modifiche che sono fatte lì vengono automaticamente ereditate.  
Per voi è del tutto nascosto perché non avendo il mapping qua possono averci scritto anche qualunque cosa che automaticamente voi non lo non lo prendete OK quindi?  
Di per sé, per voi.  
Ed è tutto nascosta questa roba, OK, in questo modo ci aiuta, anche perché se noi manteniamo il la versione del mapping corretta sui vari ambienti, siamo sicuri che ogni tipo di evoluzione che viene fatta può essere portata solo.  
Quando lo decidiamo noi e non quando lo decide SAP, OK?  
Logicamente se loro per caso cambiassero la nomenclatura e qua ci mettono Ciao allora in quel caso si rompe tutto perché ti dice fondamentalmente non riesco a tirarti fuori l'oggetto quindi non ha tirato fuori il lo status.  
Quindi chiamerà lo stesso il comando non gli darà lo status se il comando si rompe, però il mapping serve solo a estrarre quello che serve a noi, OK?  
Va bene quindi e questo viene configurato qua. Quindi gli diciamo qual è il mapping e qual è la revision che stiamo utilizzando. Ci sono poi altre informazioni tipo client gateway come vedete.  
Che ti dice qual è il corrispettivo Foundation C, il mom connection, quello che vi facevo vedere prima, che vi dice in che modo viene esposto la connessione verso le macchine.  
DOP Center e alcune altre informazioni tipo il Channel source che è quello che vi dicevo prima che vi identifica qual è la macchina primaria, qual è la secondaria e eventuali backup se ci sono OK.  
Quindi vabbè, di per sé a voi non interesserà più di tanto queste due pagine, perché dovrebbe essere già tutto fatto. La cosa importante che vi interessa è sicuramente la parte di diagnostic che è.  
Importantissimo per vedere se i messaggi arrivano non arrivano, ma anche un adapter di cui non v'ho ancora parlato che è l'adapter di tipo file, perché come vedete qua noi abbiamo due adapter principali che sono la manual import e la resend. Queste due adapter sono stati creati proprio per.  
Evitare.  
Cioè per recuperare i problemi che possono esserci in produzione. Fondamentalmente questi adapter vanno a simulare quello che viene fatto normalmente da CPIO da postman se serve, ossia vanno a fare un.  
Un richiamo delle API di tipo Web API o web API client. Le manual import fondamentalmente vanno a chiamare tutte gli adapter, quindi le web API e fondamentalmente è stata configurata una folder che è c manual import.  
OK.  
E beh, logicamente una manual import output e quindi fondamentalmente voi potete prendervi un file, andare sulla folder manual import OK droppare qua un file il sistema se lo puppa e chiamerà il corrispettivo.  
Adapter e poi vi ritornerà una response dicendovi qual è com'è andata la cosa. Analogamente noi l'abbiamo anche per la resend che serve fondamentalmente per utilizzare le web API client, quindi per rimandare i messaggi SPI. Il concetto è lo stesso.  
L'unica differenza è che qua andiamo a utilizzare un'altra folder che è resend e quindi noi di nuovo droppiamo.  
I file nella Resend Aspettate qua nella resend e nella resend output andiamo a vedere tutte gli output che sono state fatte. OK, come vedete la resend come la manual import sono vuote perché il concetto base è.  
Droppi un file e lui lo prende, lo cancella e lo usa e quindi l'evento è generato dal drop del file OK.  
OK, io adesso vi devo abbandonare perché c'ho un'altra call per JJ no, me l'hanno tolta. Ottimo. Aspetta, vado a chiedere lumi a Emiliano se mi date un attimo.  
Però in generale Questo è quanto riguarda Connect mom, non so se volete vedere qualcosa di particolare.  
Giacomo, non so se vuoi vedere la questione dei dei dei dei counter che mi hai fatto vedere prima, ti spiego, ti faccio vedere tutto il giro o l'hai già capito?

_[immagine]_**  
Giacomo Centore** 45:13  
Ma se poi a servire a tutti anche magari sì, cioè è una cosa che secondo me non abbiamo mai toccato.

_[immagine]_**  
Jacopo Revello** 45:17  
Ok.  
Va bene, ve lo faccio, ve lo faccio vedere allora, fondamentalmente.

_[immagine]_**  
Giacomo Centore** 45:23  
Se siamo già su JJ, poi?  
Vabbè, lo replichiamo sennò.

_[immagine]_**  
Jacopo Revello** 45:30  
Se vuoi ve lo posso fare direttamente su JJ se volete.

_[immagine]_**  
Giacomo Centore** 45:34  
E perdevo entrambe le cose, però, come vogliamo.

_[immagine]_**  
Jacopo Revello** 45:38  
Allora quality DJJ dovrebbe essere questa qui.

_[immagine]_**  
Giacomo Centore** 45:45  
Spieghiamo un secondo cosa è successo, semmai se.

_[immagine]_**  
Jacopo Revello** 45:47  
Sì, adesso ve lo ve lo spiego, lo vediamo direttamente sul sistema. Allora fondamentalmente cosa cosa succede quando noi generiamo un qualunque tipo di container, che sia per le non conformance, per le complete eccetera. Come sapete generiamo un.  
Un identificativo? No, non è questo identificativo serve per però aspettate, non esiste più il quality di JJ, bisogna usare il quality di ostrava, giusto?  
No.

_[immagine]_**  
Annalisa Casciaro** 46:20  
Yes.

_[immagine]_**  
Jacopo Revello** 46:23  
Nessiste, non so.

_[immagine]_**  
Annalisa Casciaro** 46:25  
Cioè no, dobbiamo andare su quality di JJ.

_[immagine]_**  
Jacopo Revello** 46:29  
Di Gava pero su Ostrava.

_[immagine]_**  
Annalisa Casciaro** 46:31  
Spero su Ostra, sì.

_[immagine]_**  
Jacopo Revello** 46:34  
OK, io stavo andando sul quality originale, va bene, allora andiamo su Ostrava quality.  
Avevo capito, OK, va bene.  
Fondamentalmente, ma quindi ve lo devo fare su questo ambiente, siete sicuri?

_[immagine]_**  
Annalisa Casciaro** 46:53  
Sì, tanto noi l'abbiamo già fatto, però possiamo rifarlo.

_[immagine]_**  
Giacomo Centore** 46:54  
Sì, lo testiamo.

_[immagine]_**  
Jacopo Revello** 46:58  
OK, va bene, non vedo Giacomo convinto, ma va bene.

_[immagine]_**  
Giacomo Centore** 47:03  
No, l'abbiamo già fatto, non ho capito in che senso, cioè avevate fatto già un test o no?

_[immagine]_**  
Annalisa Casciaro** 47:05  
No, perché noi abbiamo fatto il noi abbiamo abbiamo fatto il dry run su questo, su questo Plant, quindi lo troverai già già fatto il counter, un nuovo counter che abbiamo creato noi però possiamo possiamo farne un'altro. Nessun problema.

_[immagine]_**  
Giacomo Centore** 47:22  
Sì, ne dobbiamo fare un'altro, lo stesso perché serve la nomenclatura nuova che parte da sei milioni e finisce a 6.999.000 come è stato, come è stato concordato con SAP, per poi fare il test effettivo se.  
Funziona lato SAP perché devono devono capire se il messaggio arriva, se gli arriva regolarmente e tutto.

_[immagine]_**  
Annalisa Casciaro** 47:41  
OK.

_[immagine]_**  
Jacopo Revello** 47:45  
OK.

_[immagine]_**  
Annalisa Casciaro** 47:47  
Va bene.

_[immagine]_**  
Jacopo Revello** 47:47  
Allora fondamentalmente quindi cos'era successo in Spagna hanno raggiunto il numero massimo di container, quindi hanno raggiunto il 7.999.999 e quindi container una volta raggiunto il massimo si resetta.

_[immagine]_**  
Giacomo Centore** 48:01  
Una volta raggiunto il massimo, si.

_[immagine]_**  
Jacopo Revello** 48:05  
Quindi cosa bisogna fare, bisogna andare sulla pagina dei counter.  
Come vedete c'è già un Brembo counter, OK, parte da 7 milioni, dobbiamo crearne uno nuovo.  
Nuovo counter underscore sei così sappiamo che è sei milioni questo OK name e description vedete voi ora il Sid deve essere quindi 61234566 milioni.  
L'incremento deve essere sempre di uno, il massimo value è 6123456OK.

_[immagine]_**  
Giacomo Centore** 48:46  
Che è 6.999.000.

_[immagine]_**  
Jacopo Revello** 48:50  
Esatto, sei 999.999, giusto?

_[immagine]_**  
Giacomo Centore** 48:54  
Corretto, sì.

_[immagine]_**  
Jacopo Revello** 48:55  
OK, l'eading zero serve per azzerarlo poi e non c'è un timer reset no? Quindi fondamentalmente noi abbiamo creato il nostro counter OK che parte da sei milioni. Adesso cosa bisogna fare? Bisogna creare un nuovo numbering.  
Sputter.  
Numbering pattern come vedete c'è già un Brembo numbering pattern, aspetta ve lo cerco Brembo.  
Brembo numbering Pattern OK, ne creiamo uno nuovo che chiameremo Brembo numbering Pattern underscore sei OKE qua cosa gli dobbiamo dire? Dobbiamo dirgli l'APP Name che è.  
Sempre material, se ricordo bene l'entity Type è material tracking unit aggregate e la destination è ID.  
OK, in questo modo, come vedete, io ho creato questo oggetto qua dentro, quando faccio il number in pattern mi sta dicendo che non lo genererà sulla base di niente, quindi devo dirgli quali sono gli elementi che compongono il number in pattern.  
In questo caso vi devo dire di utilizzare solo il counter numero 6. OK, io qua se volete posso fare anche un test, perché quando faccio questo lui mi genera il primo counter disponibile che è il sei milioni. OK, se lo faccio quando siamo già per esempio prendere quello vecchio io faccio così, lui mi dice.  
7.000.002 perché probabilmente in questo ambiente sono stati fatti solo due complete, però fondamentalmente questo vi dice qual è l'ultimo valore che verrà generato, OK?  
Detto questo però non è finita perché perché questo number in pattern non è ancora attivo, quindi cosa succede se adesso io devo andare sulla configuration key?  
C'è un Tab Brembo Brembo e qua devo dirgli guarda non usarmi più come MTU aggregate number in pattern normale ma prendimi il sei faccio il Save è automaticamente fatto quindi adesso se io vado a fare una complete.  
Posso farlo Annalisa, Francesco prende.

_[immagine]_**  
Giacomo Centore** 51:01  
Poi.

_[immagine]_**  
Annalisa Casciaro** 51:03  
Sì.

_[immagine]_**  
Jacopo Revello** 51:05  
OK, prendo 1 1 oggetto a caso, prendo un.  
Un qualcosa, per esempio, questo speriamo che ci abbia possibilità di completamento.  
OK, c'è tutto quello che voglio. Posso fare per esempio la generazione dei difetti. Ottimo bello questa roba. Aspettate che magari non avevo ancora caricato tutto.  
No, non gli piace. Allora facciamo un attimo un refresh della pagina che va sempre bene. Il fatto che si sia rotto mi fa un po paura, ma lascio da.

_[immagine]_**  
Juela Ndoka** 51:43  
Non aveva il main material là sopra, la gallery non si stava caricando correttamente.

_[immagine]_**  
Jacopo Revello** 51:49  
OK.  
Ora mi sembra più sereno.  
No.  
C'è qualche problema su questo ordine?

_[immagine]_**  
Juela Ndoka** 52:03  
E manca lì quando lo Apri, manca il main material quando Apri defect declaration.

_[immagine]_**  
Jacopo Revello** 52:10  
Sì, ho visto, ma non capisco perché dobbiamo fare un complete, facciamo un complete, facciamo prima.

_[immagine]_**  
Juela Ndoka** 52:13  
Sì.  
Ma che I get me con product data che fa quella cosa mi sa se non sbaglio che carica quei dati.

_[immagine]_**  
Jacopo Revello** 52:20  
Sì, vedete, non.  
Non sta, non sta. Ma perché questo è un è un ordine multifase. Vabbè aspettate facciamone prenderne uno goog no?

_[immagine]_**  
Giacomo Centore** 52:36  
Cap.

_[immagine]_**  
Jacopo Revello** 52:37  
Avete CAT? No, ma CAT non c'è me ne CAT 00 1.  
Perfetto nel \*\*\*\*\* 00 1 andiamo qua dentro.  
Perfetto mamma mia quanti pezzi va bene, proviamo a vedere se adesso gli piace. Perfetto, io adesso ne genero uno, faccio un immediate scrap quando faccio Save adesso andiamo a vedere ci dirà quale container ha creato e come vedete ha creato il container sei milioni.  
OK.  
Quindi adesso probabilmente ci saranno un conformance che si chiama sei milioni, il prossimo sarà 6.000.001 eccetera eccetera, giusto per vederlo.  
Andiamo su.

_[immagine]_**  
Giacomo Centore** 53:21  
E questo nel messaggio sap, perché io non l'ho mai visto proprio il sei milioni scritto, ma perché è legato a cioè data ora e poi sei milioni tipo?

_[immagine]_**  
Jacopo Revello** 53:33  
No, il cioè te lo faccio vedere, se vado qua vado qui, prendo il mio ordine, vado a vedere su output message ma ha creato una good receipt.

_[immagine]_**  
Giacomo Centore** 53:34  
Non c'è.

_[immagine]_**  
Jacopo Revello** 53:47  
Oggi.  
Se io la vado a scaricare vado a vedere qua ed effettivamente quando si caricherà effettivamente qua mi dice che il container sia migliori OK?  
Filet.  
OK, datemi solo un attimo che vado un attimo da Emiliano per capire se c'ho il meeting o no perché mi sembrava che fosse una cosa urgente quando me l'han chiesto, però intanto pensate se vi serve qualche altra info riguardo qualcosa o se vi serve la toga va o altro.  
Approfittiamone arrivo.  
OK, va bene se non vi viene nulla in mente, volevo farvi vedere un po la questione AGV.  
E raccontarvi un po cosa è successo, anche perché domani abbiamo gli UATE, quindi ne approfittiamo tutti per farci un bel giro su AGV.  
Sapete tutti il giro degli AGV devo spiegarvi qualcosa, l'abbiamo già detto, mi sembra, però se non vi riquadra qualcosa lo rivediamo.  
Scusate, sono sull'ambiente sbagliato, sono a saesa.  
Sento mutismo, non so se mi sentite, sto parlando sì.

_[immagine]_**  
Juela Ndoka** 55:30  
Sì, ci sentiamo.

_[immagine]_**  
Fabio Massone** 55:30  
E 700.

_[immagine]_**  
Jacopo Revello** 55:31  
OK, perfetto.  
Vi risulta gli AGV? Sapete di cosa sto parlando? Vi serve qualche info in più? Ditemi tutto.

_[immagine]_**  
Giacomo Centore** 55:42  
Abbiamo iniziato a parlarne l'ultima volta del GV, direi.

_[immagine]_**  
Jacopo Revello** 55:45  
Ok, perfetto.

_[immagine]_**  
Giacomo Centore** 55:46  
E.

_[immagine]_**  
Jacopo Revello** 55:49  
Allora, giusto per farvi capire, i problemi di questi giorni erano principalmente tre.  
Il primo.  
Aspetta questo, chiedo a Juve se ha già messo il deploy il nuovo pacchetto.

_[immagine]_**  
Juela Ndoka** 56:05  
Sì.

_[immagine]_**  
Jacopo Revello** 56:06  
OK, quindi il primo era fondamentalmente che io quando andavo qua va beh, giusto per dirvi quando si abilita GV io ho la possibilità di fare diversi tipi di chiamate, questo perché appunto tutti gli oggetti che girano all'interno dell'impianto di machining.  
Sono oggetti automatizzati tramite questi carrellini automatici no? Quindi io devo richiedere qualunque cosa dal cassone vuoto a mi devi venire a prendere il cassone a qualunque cosa succeda quindi qua fondamentalmente è la.  
Diciamo la bottoniera che serve per fare tutte le chiamate standard, quindi vedete che c'è chiamate vuoti, aspettate che probabilmente non vedete una Fava perché è minuscolo, chiamate vuoti, ritorno vuoti, chiamate agli orari, ritorno agli orari, ritorno contenitori trucioli.  
Chiamata vuoti ritorno vuoti è fondamentalmente devo chiamare un cassone vuoto per riempirlo oppure devo ritornare a un cassone che ho che ho svuotato? Chiamata al volare ritorno al volare è fondamentalmente ho bisogno del.  
Del degli oggetti che diciamo spaziatori all'interno del contenitore che mi servono per suddividere gli oggetti che mettono nel contenitore oppure non mi servono più li ritorno e invece i contenitori trucioli è fondamentalmente tutti i byproduct che io vado a produrre.  
A un certo punto verranno messi dentro un contenitore che si riempirà e devo farlo portare via. OK, tutte queste chiamate quando io faccio le chiamate come vedete hanno un semaforino perché è una chiamata che va dal MES, va WMWM chiede alla GV di agire. Se la GV risponde sì, vado, mi ci ritorna, OK.  
Sto facendo la l'esecuzione. Se la GV mi risponde no sono bloccato andrà in errore. OK, per farlo io devo selezionare prima una baia e poi un materiale materiale. Sono configurate tramite pagina di configurazione specifica.  
Oppure si può decidere di scriverlo manualmente. OK, il primo problema era che se io andavo a cancellare qua il sistema si rompeva perché mi diceva no empty data e quindi non potevo più selezionare niente. Invece adesso come vedete, qualunque cosa io faccio qua non si rompe niente.  
Quando faccio l'invio il sistema come vedete va in grigio e mi dice ho inviato e poi cambia colore a seconda di come è ritornato. Se andiamo a vedere di nuovo sul nostro amico Connect Mom possiamo andare a vedere che ho fatto il logout.  
Una volta che rientriamo, possiamo andare a vedere che.  
Se andiamo sulla Rug history.  
Io ho fatto una AGV movement che aspettate che abilito le risposte così vediamo tutto. Io ho fatto una GV movement dove?  
Aspettate, quella là si è rotta.  
OK, ho fatto una GIV movement che conteneva fondamentalmente il Plant 0111, la il buffer, la PSA, il tipo di.  
Di staging Bay che sto usando cioè la baia dove vado a richiedere il pezzo, il tipo di chiamata che è lo 0 2 cioè la chiamata vuoti e poi un identificativo della chiamata nel momento in cui lo mando EWM mi risponde con un messaggio all'interno di questo messaggio vediamo già.  
Un'informazione, per esempio qua vedete che c'è scritto non ci sono, non ci sono MTHU, quindi ve lo scrivo qua non ci sono.  
Container vuoti con questo materiale.  
Per questo materiale questo packaging material OK quindi mi sta ritornando questo errore e infatti se poi vado a vedere la CK material call che è questa qua.  
Fondamentalmente lui mi dice status e cioè status error, OK?  
E quindi qua sono andati in errore. OK, se noi proviamo a fare un'altra ritorno vuoti, per esempio, io ho un vuoto, voglio ritornarlo, la baia è sempre la stessa seleziono lo stesso materiale, faccio invio. Come vedete qua adesso è diventato giallo. Perché è diventato giallo? Perché fondamentalmente lui.  
Sa che io nella mia linea ho un container con questo tappo qua e quindi ha generato un evento dato Toyota, quindi lato macchinari che si muovono per cui mi devono venire a prendere il.  
Pezzetto qua mi è ritornato, quindi se io di nuovo torniamo sul nostro amico vediamo che.  
Avrò di nuovo un AGV Movement OK, una replay AGV Movement e un arc material call che in questo caso lo status è zero OK.  
Io adesso non posso fare nient'altro perché questo abbaia, questo buffer con questo materiale è già stata allocata a quella cosa lì e quindi finché non me lo portano io non mi posso muovere, no, non posso fare niente. Quindi anche se io provassi a uscire e rientrare.  
Il pulsante rimarrebbe sempre disabilitato. Perché? Perché sono in uno Stato per cui non posso fare nient'altro.  
Poi c'è la chiamata alveolari e il ritorno alveolari che adesso vi faccio vedere, oppure c'è il ritorno truce.

_[immagine]_**  
Juela Ndoka** 1:01:43  
Scusa Jacopo, prima di passare posso farti una domanda, la seconda chiamata che hai fatto avrebbe avrebbe dovuto creare un record sulla BRM sulla entità BRMGV movement status o rimane il primo Stato che c'era prima della prima chiamata che era note OK?

_[immagine]_**  
Jacopo Revello** 1:01:47  
Certo.  
No, rimane sempre il.

_[immagine]_**  
Juela Ndoka** 1:02:06  
Prima chiamata, cioè il primo Stato.

_[immagine]_**  
Jacopo Revello** 1:02:08  
No.  
No, mi rimane l'ultimo Stato ricevuto.

_[immagine]_**  
Juela Ndoka** 1:02:14  
Ok.

_[immagine]_**  
Jacopo Revello** 1:02:17  
Aspetta questo qua come call Type non me la ricordo. Aspettate un attimo, devo vederla. La call Type è 0 3 quindi fondamentalmente lui cosa fa? Va a fare una query che ti dice dammi l'ultima, lo Stato ti dice.  
L'ultima stato della chiamata con questo call Type su questo buffer e questa macchina, la scout 0 11, il buffer è questo, il call Type è tre e lo status è tre.

_[immagine]_**  
Juela Ndoka** 1:02:41  
OK, grazie.

_[immagine]_**  
Jacopo Revello** 1:02:43  
Lo status è tre vuol dire ACK received se ricordo così AA braccio.  
Facciamolo anche per il ritorno truccioli. Quindi fondamentalmente chiamo questo qua, chiamo un'altro materiale, faccio invio automaticamente qua vedete di nuovo è diventato giallo, significa che mi hanno risposto OK, ora vi faccio vedere un problema che abbiamo identificato così da.  
Da far vedere anche come analizzarlo nel caso. Quindi fondamentalmente andiamo a fare una chiamata alveolari. Come vi dicevo, la chiamata Alveolari è fondamentalmente la chiamata di quegli oggetti che vengono messi all'interno del cassone per suddividere i vari pezzi, cioè come quando vi arriva il pacchetto Amazon con dentro i pezzettoni di plastica, quelli che ci divertiamo a.  
Schiacciare le bollicine, lo stesso principio qua selezioniamo la baia, selezioniamo il materiale. In questo caso, come vedete, i materiali sono un po' diversi perché non sono materiali di impacchettamento, ma sono materiali alveolari, quindi selezioniamo.  
E facciamo invio.  
Nel momento che io qua è tornato un errore adesso prima non funzionava perché quando ci faceva la chiamata fondamentalmente ci ritornava un oggetto vuoto, invece adesso a quanto pare l'hanno aggiustato quelli di WM senza dirci niente forbettini.  
Se andiamo a vedere la CK material call effettivamente adesso ha col Type 5 status zero.  
Molta +5 status zero.  
Lo status zero perché corrisponde al rosso.

_[immagine]_**  
Juela Ndoka** 1:04:25  
No Tata e hai fatto alveolari non è assai, scusami.  
Ciao.

_[immagine]_**  
Jacopo Revello** 1:04:31  
No status due quindi è un'altro. Aspetta, allora ho preso della CK sbagliato, scusate sì è vero, quello delle 18 ho sbagliato. Non ho fatto l'aggiornamento del filtro ACK material call a sei esatto a sei status e.  
OK, quindi ci hanno tornato un errore. Se andiamo a vedere perché c'è stato l'errore, andiamo a vedere, vediamo sul Content, vediamo se ci hanno detto qualcosa. No, non è scusate, non è questo qua, ma è quello sotto replay GV Movement, vediamo qua, facciamo content, andiamo a vedere qua.  
Cosa ci dicono?  
Separatore nero not found.  
Qua in realtà secondo me sta sbagliando perché non devo usare packing material ma devo usare un'altra cosa ma affari loro perché questa qua è una chiamata a sei.  
Va bene?  
Detto questo, quindi, analogamente per il ritorno al volare mi aspetto che vada in errore, però l'altro problema che avevamo è che spesso per esempio in questo caso qua vedete cosa ho fatto, ho fatto una chiamata, OK?  
Ma rimane grigio, quindi io non posso fare più niente. Se rimane grigio vuol dire che io ho mandato la chiamata AWM ma nessuno mi ha ancora dato una risposta. Infatti se io adesso vado qua e vado a vedere le mie chiamate.  
E faccio così.  
Non so se.  
In realtà la CK mi è arrivato, ma se vado a vedere il contenuto è vuoto, OK?  
Essendo vuoto significa che fondamentalmente non ci stanno dando nessuna informazione e quindi noi rimaniamo in questo stato di limbo dove non sappiamo più cosa fare, OK?  
E da qui non ne usciremo mai, nel senso che glielo posso fare anche 100.000 volte sta roba qua che ormai sono bloccato, quindi se io provo a fare altro, un'altro ritorno alveolari mi darà sempre grigio e rimango bloccato, OK?  
Ora in realtà secondo me in questo caso, in questo caso qua dovremmo gestirlo in modo che vada in errore, però il problema qual è? Che noi qua non abbiamo, come vedete, nessuna informazione OK dal tuo number.  
Di conseguenza, non avendo nessuna informazione, noi non possiamo neanche sapere dove indirizzare la chiamata.  
E quindi non indirizzando la chiamata, noi non possiamo fare nulla, quindi questo è un baco lato EWM che ci devono risolvere.  
Però di per sé noi qua adesso siamo in una fase bloccata che non possiamo fare niente, se mai vi succedesse una cosa del genere lato quando siete in Plant Alive.  
E non riuscite a contattare WM? Avete due soluzioni. La prima soluzione è farla brutta, andare tasto destro inspect e andare a abilitare il pulsante no. Quindi fondamentalmente qua andate qua.  
Togliete il disable e avete risolto il problema, no? Cioè se io adesso faccio così automaticamente si abilita. OK, però è un po' brutta. L'altra soluzione che io vi suggerisco, che è un po' più pulita, è quella di simulare voi la chiamata.  
Quindi prepararci già un tester tool già pronto.  
E cosa fate? Andate a prendervi la vostra, la vostra chiamata che avete la.  
La GV Movement OK, qua dentro voi avete.  
Un identificativo che è il call ID.  
OK, andate su.  
Postman, vi mettete il call ID che è quello che avete copiato, la call Type che è un a sei OK.

_[immagine]_**  
Fabio Massone** 1:08:50  
Occhio che hai cancellato un minore da Colli lì.

_[immagine]_**  
Jacopo Revello** 1:08:53  
Sì va bene così, un a sei che anche questo è un'informazioni che potete recuperare da qua perché ce l'avete qui no aspettate col Type scusa 0 4 non a sei. Stavo sbagliando infatti.  
Col Type 0 4.  
OK status e fate una bella send automaticamente se noi andiamo qua adesso è andato in errore e si è sbloccato il pulsante questo è 1 1, cosa che è un po' più pulita ora di per sé.  
Qua anche se ne facciamo un'altra adesso non ne usciamo vivi perché in realtà WM continuerà a risponderci vuoto e quindi anche anche se mai fosse andato qualcosa a buon fine siete rimani bloccato quindi è un problema comunque di WM ma per sbloccarlo.  
Voi potete tranquillamente segnarvi qual è la chiamata che è stato fatto tenervi qua la vostra cosa basta un ID che sia esistente quindi anche se l'ho rifatta adesso faccio così lui automaticamente si prende un con l'i D che esiste.  
E va aggiornare ora probabilmente c'è un down time, non so perché non sta andando, ci metterà un pochino, probabilmente c'è un down time di rete però vedete è tornato rosso OK, quindi fondamentalmente la soluzione migliore è questa.  
Così almeno vi tenete lì un ID fisso, lo trovate o da una chiamata fatta o ve la potete creare voi, perché fondamentalmente se voi andate sul database potete banalmente andare su la history, che è un'altra.  
Aspettate che io me l'ero segnata. Eccola qua. Voi andate a vedere la history, per esempio, andate a vedere per quel buffer.  
Con quel equipment, per esempio questo qui o la scowl banalmente andate a vedere questo vi andate a recuperare il tracking ID corrispondente.  
Ve lo buttate su qua sopra e avete risolto. L'importante è che il Trackin ID esista. OK, poi anche se è una chiamata vecchia ve ne frega il giusto perché tanto l'importante è che si aggiorni tanto. La history in realtà è aggiornata sul timestamp, quindi ti dice lo Stato.  
La history reale su ogni tutti le chiamate che son state fatte quindi se voi le fate last Update Don vi basta fare una ricerca su un buffer Equipment e trovate qual è il tracking di corrispondente quindi voi li potete sempre sbloccare tramite questo o come vi dicevo prima di nuovo lo possiamo.  
Vedere tutti insieme se io adesso mi faccio un file.  
E lo chiamo se ho sbagliato no, faccio file Save as e la chiamo mettiamo sul desktop e la chiamo ACK MAT call punto XML.  
Adesso andiamo sul desktop, vado qua, vado sul desktop, mi prendo la mia ACK material call, vado su c manual import, la droppo qua.  
Il sistema se la pupperà se l'è puppata e andiamo a vedere sull'output vediamo che.  
A breve, suppongo.  
Oppure lo vediamo direttamente qua da Connect mod, vediamo che ci sarà un esatto ac material call che probabilmente è andata in errore per qualche motivo, perché vediamo cosa c'è.  
Animal Connect OK, qua fondamentalmente è andato in errore, la c'è mom rispose.  
Poi però il work pro exception vediamo se ti ha fatto una era qua sotto la response. No, non ha dato neanche la risposta in questo caso, quindi si vede che si è rotto qualcosa. Allora questo possiamo andare a vedere su quella.  
Quella vista che vi ho fatto vedere prima, border by Time Created Resc, vediamo un po' se c'è qualcosa.  
C'è un error qua su un broker.  
OKOK la lui sta dicendo che ci sono delle esecuzioni sul Domain controller, quindi probabilmente non abbiamo neanche tracciato niente perché è andato in errore.  
Però vabbè, fondamentalmente questo è un caso che vi può succedere, dove andate a vedere?  
Tutti i vari i vari giri e andiamo a capire il perché è successo qualcosa. OK qua vedete c'è un retry perché ho fatto io retry manuale received from manual import quindi gli sta dicendo ho ricevuto questo file ha tirato LXML.  
Tramite manual import. E poi si è rotto, si è fermato da qualche parte e non ci dice dove eccoli qua. Era un po' in ritardo. Exception exception.  
OK, enable to Connect, vedi, non riesce a connettersi al.  
Al comando però questo è perché stanno facendo della roba da qualche parte.  
Va bene comunque in generale gliela gliela potete sempre sbloccare in qualunque momento. Sempre per la GV c'è anche la chiamata materiale, perché la chiamata materiale in questo caso aspetta selezioniamo un ordine per esempio.  
Chiamata materiale, in questo caso, come vedete qua, ha la possibilità di selezionare una baia e quindi va va a fare una chiamata sulla base della baia, anche qua c'è il semaforino che diventa a seconda di quello che è e fa la chiamata di Baia.  
Una cosa importante lo dico per Juela, qua vedi, io posso fare la chiamata in realtà anche senza la Baia.  
OK, in realtà dovremmo fare in modo che se questo c'è, la chiamata sia disabilitata finché non seleziono la baia.  
Okay.

_[immagine]_**  
Juela Ndoka** 1:15:39  
E quindi solo se è abilitato il Flag GV.

_[immagine]_**  
Jacopo Revello** 1:15:43  
Se è abilitato Flag AGV, questo pulsante deve essere abilitato solo quando seleziono la Baia OK.

_[immagine]_**  
Juela Ndoka** 1:15:48  
OK, voglio prendere un voto, OK?

_[immagine]_**  
Jacopo Revello** 1:15:51  
Va bene analogamente vediamo se me lo fa fare. Quando io vado a fare un completamento qua non c'ho nulla. Aspettate che trovo un ordine che c'abbia qualcosa. No, non c'ho niente. Andiamo a vedere se c'abbiamo del materiale da qualche parte.  
Così facciamo tutte le cose divertenti.  
Scurno.  
Però direi Emanuele correggimi se sbaglio, più o meno i giri che hai fatto te sono questi e adesso sembra funzionare, giusto?

_[immagine]_**  
Emanuele Merlo** 1:16:22  
Sì.  
Sì, l'altra volta non funzionava proprio niente.

_[immagine]_**  
Jacopo Revello** 1:16:28  
No, ma allora in realtà, giusto per farvelo sapere, guarda, faccio questo e poi ti dico tutto quello che abbiamo scoperto in questi in queste stamattina in mezz'ora è uscito tutto. Allora qua mi prendo un contenitore che c'ho 100 pezzi me lo vado a scansionare.  
Tacete, Tacete, Tacete.  
OK qua vado a fare le mie bellissime quality Inspection wrong ci metto 10 così uno è andato a buon fine, faccio invio e l'abbiamo fatta. Questo la nascondiamo, andiamo a fare un completamento quando vado a fare il completamento nel caso di AGV come vedete io qua ho anche la.  
Necessità di inserire una baia, quindi anche se io mettessi un pezzo come vedete qua non mi si abilita. L'unico modo per abilitarla è o disabilitare questo e quindi fare una chiamata GV senza la baia oppure selezionare la baia.  
OK, già che sono qua voglio provare una cosa. Ecco, questo non l'abbiamo ancora risolto, io e Elisa.  
Vedi?

_[immagine]_**  
Juela Ndoka** 1:17:38  
Mi sembrava risolta questo, però vabbè non metto.

_[immagine]_**  
Jacopo Revello** 1:17:44  
Va bene?

_[immagine]_**  
Juela Ndoka** 1:17:45  
Non ho fatto dei tester boh.

_[immagine]_**  
Jacopo Revello** 1:17:48  
E io adesso posso fare completamento, mi dice quantità uno.  
Quando vado a fare così lui mi genererà una good receipt, ve la faccio vedere giusto per pro forma work order.  
Lui mi ha generato un output message con una good receipt, all'interno di questa good receipt noi possiamo andare a vedere.  
\*\*\*\* che mi ha detto utilizza questa Baia qua, OK?  
E quindi AA loro gli abbiamo detto, utilizza questa baia.  
OK.  
Una cosa che volevo vedere, scusate, giusto per mio interesse.  
OK, anche l'altro problema, io e la che qua mostra tutte le baie, dobbiamo metterci solo le baie che servono a noi.

_[immagine]_**  
Juela Ndoka** 1:18:47  
Piccolo non l'ho mai, cioè verificato, quindi probabilmente mostra tutto.

_[immagine]_**  
Jacopo Revello** 1:18:50  
Va bene?  
OK, per la Station call invece sta roba l'abbiamo già fatta, giusto? Sì, perché mostra solo quelle relative, quindi dobbiamo fare la stessa cosa di là. Va bene. Quindi di per sé questo è il giro della GV, non so se c'è qualcos'altro che volete vedere.

_[immagine]_**  
Juela Ndoka** 1:18:58  
Sì.

_[immagine]_**  
Jacopo Revello** 1:19:14  
Ditemi voi.

_[immagine]_**  
Giacomo Centore** 1:19:22  
Puoi andare un attimo sulle configuration, BEM?

_[immagine]_**  
Jacopo Revello** 1:19:26  
Sì, scusate, faccio solo un test.

_[immagine]_**  
Giacomo Centore** 1:19:27  
Configuration questo qua configuration key.

_[immagine]_**  
Jacopo Revello** 1:19:32  
Fatelo sapere perché sono \*\*\*\*\*\*\*, sì, andiamo sulla configuration key.  
Dimmi tutto.

_[immagine]_**  
Giacomo Centore** 1:19:38  
No, quell'altro.

_[immagine]_**  
Juela Ndoka** 1:19:39  
Aspetta Jacopo, scusami Giacomo solo un secondo perché poi lo perdiamo e me li dimentico. Vedi che message code rimane 400 1 sul link del quindi quando è deployato è deployato male vedi qualsiasi cosa fai.

_[immagine]_**  
Jacopo Revello** 1:19:53  
Non.

_[immagine]_**  
Juela Ndoka** 1:19:55  
Nel URL.

_[immagine]_**  
Jacopo Revello** 1:19:57  
Sì, e quindi?

_[immagine]_**  
Juela Ndoka** 1:19:58  
Message code 401 è sbagliato.

_[immagine]_**  
Jacopo Revello** 1:20:02  
Vabbè, ma ce ne sbattiamo è un problema?

_[immagine]_**  
Juela Ndoka** 1:20:05  
E non so che avevo un mi ricordo da ossava che qualche impatto c'è l'aveva.  
Perché proprio quando lo Apri, vedi, rimane così?

_[immagine]_**  
Jacopo Revello** 1:20:18  
Vabbè mi basta refreshare toglierlo funziona no?  
Potrebbe essere lì.

_[immagine]_**  
Juela Ndoka** 1:20:22  
Sì, ma credo che loro aprono direttamente il link, non fanno il nostro, cioè?

_[immagine]_**  
Jacopo Revello** 1:20:28  
Tu dici che è da è da solution studio che è rotto?

_[immagine]_**  
Juela Ndoka** 1:20:29  
Giro sì che penso che così no e dov'è rotto?

_[immagine]_**  
Jacopo Revello** 1:20:33  
No.  
E se si rompe te lo dico io perché si rompe. Si rompe perché quando clicco linkersys lui mi va in 401 e dovrebbe. No, non lo so. Ogni tanto mi ricordo anch'io.

_[immagine]_**  
Juela Ndoka** 1:20:43  
Non me lo ricordo che c'era un qualcosa, anche un IR su questo, però non mi ricordo come avevamo risolto.

_[immagine]_**  
Jacopo Revello** 1:20:48  
Mi ricordo, mi ricordo.  
Va bene adesso poi controlliamo anche questo, dicevi scusa Giacomo.

_[immagine]_**  
Giacomo Centore** 1:20:57  
No, soltanto sugli configuration key sotto Brembo. Che cos'è il pattern? Quello sotto il l'aggregate intermed.

_[immagine]_**  
Jacopo Revello** 1:21:09  
Allora questo qua è lo stesso principio di quello sopra solo per i container intermedi, cioè i container che devono passare da un'operazione all'altra.  
OK quindi fondamentalmente quando io genero un container in fase uno che devo andare in fase due, questo container non va a SAP e quindi devo utilizzare un contatore che è diverso, infatti se noi andiamo a vedere.  
I number in pattern.  
L'intermed.  
Eccolo qui, se noi andiamo a vedere come vedi inizia per 1001.  
Perché ha un identificatore totalmente diverso e serve proprio per identificare i container intermedi. Questo anche se si resetta non è un problema per nessuno. O meglio però p center lo è perché in realtà genera dei container che esistono già. Mi aspetto che però i container dopo.  
Non so quanti milioni siano già stati un po cancellati, 369OK dopo.  
Un miliardo. Mi aspetto che i container un miliardo e uno sia già stato cancellato da dai purging perché sarà stato qualche anno fa. Spero però in generale, se mai succedesse qualcosa, il principio è lo stesso, create un nuovo contatore intermed, ci mettete 1 1 davanti e fate 11.  
E poi va da solo, OK, il problema è fondamentalmente che quando lui va a creare i contenitori, se ci sono già.  
Quando va a fare va a fare la creazione, lui vede che esiste già una material tracking unità aggregate con quel numero e ti dice non posso fare nulla. Quindi lato MES non si rompe, però non crea dei dati sporchi, cioè ti ferma e ti dice non posso andare avanti perché il contenitore c'è già, fate tutto sto giro qua, create quello nuovo e si sblocca.  
OK.  
M  
Altro.

_[immagine]_**  
Fabio Massone** 1:23:12  
Però quando tu dicevi col polling viene eliminato, però quando poi viene messo su archiving non fallisce.

_[immagine]_**  
Jacopo Revello** 1:23:22  
Quando poi torna su archiving?  
Potrebbe fallire effettivamente.  
Non credo che nessuno ci abbia mai pensato a sta roba, mi aspetto che sull'archiving il milione però di nuovo secondo me è comunque corretto che se raggiungi il contatore Massimo vai a cambiare il contatore.  
Dobbiamo solo stare attenti che quando succede dovranno stare. Spero che quando arriveremo al milione di container io non ci sarò già più, però quando se e quando succederà dobbiamo semplicemente cambiare il contatore, metterci 1 1 essendo internal questi per noi possono anche.  
Diventare 14 miliardi 596.000 non ce ne non gliene frega nulla a nessuno, è solo un identificatore nostro. OK, ci mettiamo anche Pippo davanti, va bene, l'importante è che è che non andiamo a generare cose nuove, cioè se.  
Giusto per farvi capire se io.  
Banalmente qua vado su numbering pattern, giusto per fare le cose divertenti e vado qua e gli metto numbering pattern part e gli metto una costante Pippo OKE faccio salva dal giorno dopo lui mi creerà.  
1.000.001 Pippo OKE non se ne accorge nessuno, cioè se ne accorgono perché leggono Pippo però non disturbiamo nessuno nel fare questo, quindi siamo liberi per l'interno, siamo liberi di fare quello che vogliamo logicamente non.  
Se io adesso facessi questa cosa qua e faccio Pippo nessuno se ne accorge neanche OP center mi continuerà a generare 1.000.001 per poter aggiornare il contatore come vi dicevo bisogna fare tutto il giro di prima. Quindi contatore nuovo number in patter nuovo andiamo a cambiare il nome sulla configuration key da lì.  
Ci iniziamo ad accorgercene, OK?  
Va bene.

_[immagine]_**  
Fabio Massone** 1:25:24  
E anche se non ho capito com'è possibile che abbiano già finito su Spagna, hai detto i contatori e in così poco tempo hanno fatto un milione di container.

_[immagine]_**  
Jacopo Revello** 1:25:36  
Non un milione, ma il non hanno, non hanno, non hanno fatto l'intermedia, ma hanno fatto il number impact normale, quindi hanno fatto mezzo milione di container perché quello normale aspetta, questo sono in Italia, quello normale.

_[immagine]_**  
Giacomo Centore** 1:25:39  
Mezzo mezzo milione.

_[immagine]_**  
Jacopo Revello** 1:25:55  
700.000 era, 7 milioni era.  
OK, quindi ci può stare che ne hanno fatto un po', anche perché otawan Alive da tre anni considera che il problema qual è? Che noi alcuni contatori li perdiamo perché noi continuiamo a generare ogni volta che fanno una non conformance, ogni volta che fanno uno scrap di.  
Con container, cioè ne generiamo AA palate e quindi potrebbe succedere che arriviamo al milione perché anche se loro strappano un pezzo noi stacchiamo stacchiamo un conteggio.  
Quindi magari per.

_[immagine]_**  
Giacomo Centore** 1:26:32  
In più è ad evento e non a comando ancora, per cui c'è pure il problema che magari lo viene viene countato 1 1+1 anche se poi il messaggio non arriva.

_[immagine]_**  
Jacopo Revello** 1:26:37  
Pure problema.  
Ciao.  
Esatto, essendo esatto, essendo su gava che ogni tanto si perdono i messaggi, potrebbe essere che perdiamo qualche cosa e quindi poi i conteggi li perdono per quello.

_[immagine]_**  
Giacomo Centore** 1:26:45  
C'è anche quello.

_[immagine]_**  
Jacopo Revello** 1:26:56  
Ok.

_[immagine]_**  
Fabio Massone** 1:27:00  
Però non c'è, cioè nel senso c'è comunque un certo che tu hai detto passiamo da 7 milioni a sei milioni, finiscono in sei milioni, passiamo a 5, però come facciamo a sapere che se mettiamo due milioni non c'è il gran contatore che utilizza due milioni o magari se decidiamo di mettere non so invece che un milione di.  
Da di minimo mass value no mettessimo 10 milioni, magari rompiamo qualcosa perché si aspetta che il numero sia lungo 7 caratteri, capito?

_[immagine]_**  
Jacopo Revello** 1:27:25  
Non ha, non ha.  
Non è una cosa che decidiamo noi, è una cosa che deve decidere SAP, OK, quindi è un'informazione che ci manda SAP a noi, perché loro hanno ancora più problemi di noi, perché loro hanno un magazzino da gestire. Quindi cosa metterci? Non lo decidiamo noi, ma ce lo dice SAP a parte per le.  
Intermed che vi dicevo prima che lì ci possiamo mettere anche Pippo invece l'altro ce lo dirà SAP quindi se SAP ci dice 1.000.300 e ce l'hanno già \*\*\*\*\* loro.

_[immagine]_**  
Fabio Massone** 1:27:47  
C'è lento, no, per il tempo.

_[immagine]_**  
Jacopo Revello** 1:27:57  
Se loro ce l'hanno, ce l'abbiamo anche noi, se loro non ce l'hanno, non ce l'abbiamo neanche noi, OK?  
Loro vanno a incremento, quindi se io se loro domani si trovano 6.000.001 oppure 6.100.000 non è che il giorno dopo li posso mandare 6.000.500?  
Perché loro vanno in incremento, quindi rischiamo. Cioè si può può succedere che li mandiamo magari una volta 6.100.000 la volta dopo 6.050.000 però.  
E comunque.  
Noi non possiamo, noi non possiamo andare avanti e indietro perché l'incremento è sempre di 1111E loro poi non è che vanno a colmare i gap, se c'è un gap in mezzo a loro frega niente. L'importante è che non ci siano duplicati nei conteggi, OK?  
M

_[immagine]_**  
Fabio Massone** 1:28:56  
E anche a me, sì, grazie.

_[immagine]_**  
Jacopo Revello** 1:28:58  
E ci mancherebbe niente. Quindi se non avete domande specifiche direi che ci siamo più o meno, direi che abbiamo visto un po' tutto.  
Dalla volta prossima possiamo iniziare un po' a vederci magari qualche tabella qualcosa per iniziare a crearci un po' delle query magari quindi se avete già qualche query che voi utilizzate per fare cose parlo magari anche a Francesco Annalisa che avete già che avete visto che vi vengono bene.  
Portiamole a tutti così le vediamo insieme io qualche qualche vista, qualche query ce l'ho che ve la posso spiegare.  
Poi vorrei anche che chi ha fatto qualche vista.  
Ci spieghi un attimo cosa contiene, mi viene in mente per esempio quella che ha fatto Alberto sulla sulle sugli gli operatori per vedere quanto un operatore ha lavorato eccetera eccetera.  
Se no, se vi vengono in mente delle funzionalità che non avete chiare o che avete visto che c'è un baco o che qualunque cosa venga in mente tiriamole fuori, perché io più o meno gli argomenti che volevo volevo raccontarvi ve li ho più o meno raccontati tutti direi che.  
Vuoto per pieno, abbiamo visto più o meno tutto. Se ci fosse qualcosa che mi sono dimenticato me lo sono dimenticato, quindi ricordatevelo, se no vediamo un po', andiamo un po' a braccio e vediamo un po' cosa.  
Cosa possiamo trovare, OK?

_[immagine]_**  
Fabio Massone** 1:30:40  
Ho una domanda, io ti chiedo scusa un attimo, tutta la roba di p tre, poi quando verrà mergiata con da 0 1 cioè i nuovi sviluppi?

_[immagine]_**  
Annalisa Casciaro** 1:30:45  
OK.

_[immagine]_**  
Fabio Massone** 1:30:53  
Molto più avanti.

_[immagine]_**  
Jacopo Revello** 1:30:55  
Pietra, che cos'è per te, Pietra?

_[immagine]_**  
Fabio Massone** 1:30:58  
E sono gli sviluppi, quelli gap 200, gap 426, quella roba lì.

_[immagine]_**  
Jacopo Revello** 1:31:05  
Allora qualcosa è già stato mergiato, per esempio container al completamento, per quanto adesso sia scoppiato, quello lì è già stato mergiato.  
E la cosa che ha fatto Giacomo sul login che ci sono, ve lo faccio vedere, è stata già mergeata che fondamentalmente se vi ricordate prima noi ci loggavamo con Group, adesso è stato semplificato un po' la cosa.  
Cioè invece che.  
Prima cosa facevamo? Andavamo sul gruppo, selezioniamo l'utente, facevamo più, poi eravamo sul gruppo, selezioniamo l'altro utente, facevamo più eccetera eccetera eccetera. Cosa succede adesso? Io da qua direttamente posso tramite il barcode.  
Selezionare il mio utente e tramite l'invio del barcode mi fa login automatico quindi non me ne frega niente di chi c'è loggato adesso se io provo a collegarmi due volte.  
Tipo adesso mi dice C'è già quindi sei già stato collegato OK se voglio fare log off analogamente io posso selezionare il mio utente e fare log off oppure posso andare a vedere chi c'è collegato?  
E digli, scollegami questo qua, OK?  
Però questa è una cosa che è già stata fatta, così come le viste che vi dicevo prima che tracciano tutte le operazioni che sono state fatte a login degli utenti.  
Quindi alcune quando ci sono son pronte, noi le cerchiamo di portarle su quality per testarle.  
Se.  
Se qualcosa è ancora in fase di sviluppo non le portiamo. Diciamo che tutti gli sviluppi che sono attualmente ongoing dovranno il prima possibile andare su quality per testarli noi principalmente. Non so quando li voglia testare il cliente, perché?  
Non ho un piano alla mano, però.  
Ci siamo abituati a questo e andiamo avanti così.  
Cayo.

_[immagine]_**  
Fabio Massone** 1:33:17  
Bene.

_[immagine]_**  
Jacopo Revello** 1:33:20  
Va bene dai, vi regalo 10 minuti di respiro.  
Se non avete altre domande.  
OK.

_[immagine]_**  
Fabio Massone** 1:33:37  
OK.  
Grazie.

_[immagine]_**  
Emanuele Merlo** 1:33:40  
Bene.

_[immagine]_**  
Jacopo Revello** 1:33:40  
Va bene.

_[immagine]_**  
Alberto Grillo** 1:33:42  
Ok.

_[immagine]_**  
Jacopo Revello** 1:33:42  
Grazie a voi.

_[immagine]_**  
Tommaso Penta** 1:33:43  
Grazie, Ciao, Ciao, Ciao, Ciao.

_[immagine]_**  
Emanuele Merlo** 1:33:44  
S S S.

_[immagine]_**  
Alberto Grillo** 1:33:44  
Ciao Ciao Ciao Ciao.

_[immagine]_**  
Jacopo Revello** 1:33:44  
Ciao a tutti, Ciao, Ciao, Ciao, Ciao, Ciao.

_[immagine]_**  
Annalisa Casciaro** trascrizione arrestata
