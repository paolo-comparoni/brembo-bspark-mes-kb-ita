# Brembo - Training per preparazione Hypercare_140426

> Documento sorgente: `E:\BremboDocs\HyperCare Training video\Brembo - Training per preparazione Hypercare_140426.docx`  
> Tipo: Word (.docx)

**Brembo - Training per preparazione Hypercare-20260414\_140923-Registrazione della riunione**

14 aprile 2026, 12:09PM

2 h 6 m 57 s

_[immagine]_**  
Alessio Monaco** trascrizione avviata

_[immagine]_**  
Alessia Traverso** 0:03  
Va beh, la GV movement tramite il OP Center e.  
Sì.

_[immagine]_**  
Jacopo Revello** 0:11  
Ma facciamo proprio un caso, facciamo proprio un caso così vediamo anche come hai scoperto che c'era questo problema qua.

_[immagine]_**  
Alessia Traverso** 0:12  
E la ripetiti.  
No, diciamo che me l'ha mandato direttamente Francesca perché Francesca mi ha mandato direttamente la risposta di della CK m'ha detto Guarda che questa qua è la risposta che noi ti mandiamo e io guardando a livello di configurazione.  
Ho visto che noi utilizziamo questo.  
Un attimo, aspetta un attimo, mi sto rispondendo da sola, adesso cerco di in qualche modo di risponderti a Jacopo, però allora Francesca.  
L'urba.  
Aqua.  
Quindi.  
OK, no, ti sto mandando quello sbagliato.

_[immagine]_**  
Jacopo Revello** 1:10  
Beh, giusto per essere tutti sulla stessa lunghezza d'onda, allora nella parte di machining a Curno loro hanno la GV. Sapete tutti cos'è una GV?

_[immagine]_**  
Alessia Traverso** 1:12  
Sì.

_[immagine]_**  
Alessio Monaco** 1:26  
Ma per me la GV visto in stellantis serve logistica, trasporto del materiale, quindi anche qui la stessa.

_[immagine]_**  
Jacopo Revello** 1:33  
Esatto, è fondamentalmente fondamentalmente un trasportatore automatico, è un è un muletto automatico in Brembo sono dei veri e propri muletti che sono stati robotizzati, si muovono in maniera autonoma all'interno del dell'impianto, no?  
Nella parte di machining loro hanno un.

_[immagine]_**  
Alessia Traverso** 2:00  
Sì.

_[immagine]_**  
Jacopo Revello** 2:01  
È tutto gestito tramite AGV no? Quindi loro hanno la necessità di interfacciarsi interfacciarsi per ogni cosa da AGV di conseguenza a livello a livello di processo quello che succede.

_[immagine]_**  
Alessia Traverso** 2:08  
Sì.

_[immagine]_**  
Jacopo Revello** 2:19  
No, OK, sono rumore. No, tranquillo, tranquillo. Il quindi a livello di processo quello che succede è che fondamentalmente loro devono chiedere ogni cosa da TV.

_[immagine]_**  
Alessia Traverso** 2:19  
Aspetta che mi muto.

_[immagine]_**  
Jacopo Revello** 2:30  
Partendo anche, per esempio, dal dal container stesso, no? Quindi fondamentalmente loro hanno diverse diverse chiamate. Ale già che stai sharando, se vuoi sharare un attimo la Foundation facciamo vedere a tutti com'è.  
Allora se per attivare le funzionalità di AGV sono attivabili tramite work center no. Quindi fondamentalmente a livello del work center gli si dice che questo work center è gestito tramite AGV no quindi.  
Dalla pagina dell'equipment configuration.  
Si va a configurare un parametro che si chiama ISA Gv Enabled.  
E questo permette di gestire fondamentalmente tutta la parte di AGV OK.  
Prendi quella lì, è una Baia, occhio, prenditi.  
Prenditi un equipment tipo.  
Ti ricordi quello che avete usato durante i SIT per caso?

_[immagine]_**  
Alessia Traverso** 3:38  
No, non me lo ricordo. Zero. Tra l'altro posso fare un video? Sì.  
In level.

_[immagine]_**  
Jacopo Revello** 3:57  
Vabbè, comunque diciamo in generale.  
Ne prendiamo una a caso.  
Mettici work center.

_[immagine]_**  
Alessia Traverso** 4:17  
OK.

_[immagine]_**  
Jacopo Revello** 4:18  
OK, prendine prendine una casa.  
C'è una proprietà che si chiama is AGV enabled.

_[immagine]_**  
Alessia Traverso** 4:31  
Magari se lo scrivessi corretto.

_[immagine]_**  
Jacopo Revello** 4:31  
OK.  
OK, questa proprietà se è vuota è di default false, se no basta valorizzarla e metterci True ora se prendiamo magari un work center che ha degli ordini almeno.  
Poi vi faccio vedere un po' di cose, se vai sulla pagina di workorder Cercati un workorder attivo e sulla base di quello poi cerchiamo.

_[immagine]_**  
Alessia Traverso** 5:00  
OK.  
Sì.

_[immagine]_**  
Jacopo Revello** 5:26  
Poi appena entra io mi devo staccare che c'è un po' di Casini, però finché non OK va bene. Sì, questo è un assembly, in realtà converrebbe prendere. Vabbè ma va bene questo. Poi vediamo dai.  
Allora cerca tipo report work center lì, sono ripetitivo.  
Allora, fondamentalmente.  
Ability ability, raggi uguale no, qua non ci no.

_[immagine]_**  
Alessia Traverso** 5:54  
Sì.

_[immagine]_**  
Jacopo Revello** 5:58  
OK.

_[immagine]_**  
Alessia Traverso** 5:58  
Allora non le posso.

_[immagine]_**  
Jacopo Revello** 6:08  
OK.  
Qua metti centro.  
OK, se torni sulla repetitive torna indietro e vai avanti e vedrai che ti si abilita.  
OK, allora come vedete lì sulla destra è apparso il macchinarietto no? Quando viene cliccato appare 5 possibilità che sono, call empty, quindi quello dei vuoti, return empty, call alveolari, return alveolari e ritorna cheap container.

_[immagine]_**  
Alessia Traverso** 6:35  
Ciao.  
Se non eri problema?

_[immagine]_**  
Jacopo Revello** 6:43  
Allora fondamentalmente cosa abbiamo? Il call empty significa chiamata vuoti e quindi fondamentalmente è portami un container vuoto che devo riempire di buoni. OK, return empty è.  
Ho finito un container, devo rimandartelo indietro colla alveolari significa portami un contenitore con determinate caratteristiche e sono fondamentalmente dei divisori all'interno.  
Si chiamano appunto alveolari, return alveolari significa guarda che c'ho dell'avanzo di questi alveolari, quindi portameli indietro e poi return chip.  
Return chip significa un container dove raccogliamo tutto il byproduct, quindi tutto il truciolo e dobbiamo rimandare indietro, questo perché fondamentalmente essendo tutto gestito tramite AGV, io per poter iniziare una produzione devo avere un contenitore da riempire e quindi devo chiamare un vuoto.  
Per poter quando ho riempito il mio vuoto devo farlo venire a prendere quindi devo fare return scusate quando ho finito il mio il mio consumo di container devo fare return ma al contempo anche quando faccio le mie dichiarazioni di buoni quindi di chiusura dei cassoni dovrò mandare.  
Dovrò mandare una chiamata alla GV.  
Come si in cui si specifica la baia, che significa per baia si intende un'area all'interno del della linea che è delimitata da delle righe per terra quadrato.  
Dove fondamentalmente la gius ha una posizione geolocalizzata di dov'è quella baia e va direttamente lì a recuperare il pezzo no il contenitore.  
E fondamentalmente lo stesso principio viene applicato anche per il per il deposito, quindi devo chiamare un contenitore vuoto se Apri per esempio un call empty.  
Come vedete qua il sistema vi richiede la Baia, le baie e il tipo di materiale. Ora in questo specifico caso non abbiamo niente. Perché? Perché le baie sono associate ai buffer e quindi il sistema.  
Ma si aspetta di avere un'associazione 1 1 a molti tra il buffer di riferimento di questo, di questa di questa linea e le buy. Per farlo fondamentalmente bisogna utilizzare la pagina dedicata all'interno della.  
Del della pagina di back Office del supervisore che ti permette di associare.  
Uno più buffer a 1 1 specifica baia.  
Per farlo quindi Ale se torniunattimosulsolutionstudioalloraquestapaginaquanonesullabasicmaesullacomevedetequella.br M production engineer in curno perché tutte le nuove pagine sono state portate a mendix, quindi tutte le pagine.  
Più o meno tutte le pagine di basic sono.  
Sono state portate su mendix e quindi noi abbiamo fatto tutti gli sviluppi su mendix. Continuiamo a usare la basic perché la basic è quella che ha tutto su questa qua invece ci sono solo una sottoparte delle applicazioni e.  
E quindi poi adesso c'è una discussione in atto con Brembo per capire cosa fornire dove a seconda delle necessità però in generale da questa pagina qua se vai su Equipment configuration in alto a destra.  
E seleziono una baia. Ipotizziamo anche la A uno va benissimo. Come vedi sulla destra C'è pack material e buffer perché ha una baia e tu devi associare dei buffer.  
Come dicevo, servono per mostrare la lista e anche delle dei packaging specification, perché lì puoi filtrare i tipi di container che una determinata Vaia può contenere, no?  
Adesso se fai più.  
Di sopra, s'è detonati la saxa 0 25.  
Esatto selezioni fai salva automaticamente te l'ha linkata fai la stessa cosa per pack material quindi clicca pack material fai metticene un paio cioè tipo uno a caso va bene anche box differente giusto per fare un test.  
Vai salva perfetto adesso se torna sulla repetitive.  
E chiudi e riaprila con l'empty OK, ora nella dropdown dovrebbe darti a uno selezioni a uno.  
Selezioni di poche materie.  
OK, quando fai come vedete c'è anche in cima un semaforino che permette di capire se la chiamata qual è lo stato della chiamata, quindi se adesso fai Save send.  
Automaticamente il sistema fa diventare il semaforino grigio fai OK.  
E poi questo semaforino cambierà a seconda del risultato che IWM ci mandano, che è esattamente il discorso che faceva Alessia ora se passiamo su Connect mom.  
Vi facciamo vedere cosa è successo fondamentalmente dato con.

_[immagine]_**  
Juela Ndoka** 12:30  
4\.

_[immagine]_**  
Jacopo Revello** 12:33  
Guarda, ho sentito un.

_[immagine]_**  
Juela Ndoka** 12:36  
Ciao.

_[immagine]_**  
Jacopo Revello** 12:36  
Ciao Ciao Michele, se vai su Connect mom vedrai che qua nella Log history ci sarà una chiamata.  
Che agivo movement.  
OKE, qua come vedete noi gli diciamo che abbiamo chiamato il box sul Plant 111, su quella PSI, su quella baia, quella col Type e la material Type, quindi la col vuoti e quella chiamata un determinato identificativo che permette di identificare il messaggio e quindi le relative.  
Risposte OK, ora fai pure X qua. Come vedete sopra c'è stata mandata anche una CK material call. OK la CK material call se andiamo a vedere il contenuto.  
Lui qua cosa manda? W number, quindi il Plant, la call ID, call Type e status e quindi dice che è andato in errore. OK, ora tornando al discorso che facevamo con l Alessia, in realtà qua.  
Il loro ce l'han mandato il Plant, quindi quello che.

_[immagine]_**  
Alessia Traverso** 13:46  
E ho visto, ho visto, ho visto, ho visto.

_[immagine]_**  
Jacopo Revello** 13:49  
Quello che sta dicendo secondo me Francesca ha un po abbastanza senso, nel senso che.  
Esatto, quello che quello che succede è che CPI ci ha risposto con m.pl ID failed perché probabilmente è andato in errore WM OK.

_[immagine]_**  
Alessia Traverso** 14:05  
Ciao Ciao.  
Kai.

_[immagine]_**  
Jacopo Revello** 14:11  
Ma la CK material call ce l'ha mandato lo stesso CPI, quindi fondamentalmente ci hanno detto è andato tutto bene nella CK material call vedere il contenuto.

_[immagine]_**  
Alessia Traverso** 14:15  
OK.  
Mi dice un po poco perché si ferma il.

_[immagine]_**  
Jacopo Revello** 14:23  
No, vabbè no, ma ci sta. Nel senso che il fatto è che comunque lui ti ha ritrovato il 11102 e quindi è andato in errore. La col Type è giusta, il con l'i d dovrebbe corrispondere alla nostra chiamata, quindi dovrebbe esserci tutte le informazioni che a noi servono, no?

_[immagine]_**  
Alessia Traverso** 14:41  
OK.

_[immagine]_**  
Jacopo Revello** 14:42  
Quindi qua c'è tutto. Ora bisogna capire innanzitutto perché noi non siamo andati in errore, perché non è diventato rosso, almeno che non lo sia diventato. Adesso torno un attimo sulla UI.

_[immagine]_**  
Alessia Traverso** 14:45  
Sì.  
Sì.  
Provo a chiudere e dirlo.

_[immagine]_**  
Jacopo Revello** 14:55  
Chiudi, chiudi la prima, sì.  
No, è sempre grigio, quindi in realtà non abbiamo aggiornato questo, quindi capire perché non è andato fino in fondo.

_[immagine]_**  
Alessia Traverso** 15:09  
OK.

_[immagine]_**  
Jacopo Revello** 15:10  
Però di per sé quello che ti diceva Francesca è sbagliato, nel senso che non ci sta, cioè è fra loro ECPI, non è un problema nostro, no?

_[immagine]_**  
Alessia Traverso** 15:14  
Sì.  
OK, il un'altro problema che io vedo è che vedi che noi facciamo la chiamata ma la risposta non ci arriva.  
Cioè non ci.

_[immagine]_**  
Jacopo Revello** 15:29  
No, aspetta, non ci vuole un movimento sopra.

_[immagine]_**  
Alessia Traverso** 15:30  
La risposta della.  
Sì, questo sì, ma dovrebbe arrivarci anche la CK material con response.

_[immagine]_**  
Jacopo Revello** 15:40  
Non l'abbiamo data noi questa.

_[immagine]_**  
Alessia Traverso** 15:44  
In che senso non l'abbiamo dato noi? Sì, non l'abbiamo.

_[immagine]_**  
Jacopo Revello** 15:46  
La CK material call ci arriva? Esatto, probabilmente è andata in errore da qualche parte per quello che poi se tu vai a vedere la Trace history della CK material call non l'hai vista tutta perché si è rotto qualcosa. Quindi andiamo a indagare anche quello Fabio.

_[immagine]_**  
Alessia Traverso** 15:48  
Sì.  
Sì.  
Sì.

_[immagine]_**  
Jacopo Revello** 16:01  
Vedo dove vedo prima Fabio e poi Alessia.

_[immagine]_**  
Fabio Massone** 16:04  
Sì, la prima domanda riguardo la schermata di prima sulla product Engineer page si può anche fare dissociate, giusto? Perché non ho visto OK cosa bisogna fare selezionare?

_[immagine]_**  
Alessia Traverso** 16:05  
Sì.

_[immagine]_**  
Jacopo Revello** 16:13  
Certo, sì, se selezioni selezioni l'oggetto, puoi fare a meno, sì.

_[immagine]_**  
Fabio Massone** 16:18  
OK, perfetto, perfetto. E la l'altra domanda era, adesso magari poi è stato cambiato qualcosa o ricordo male io, ma non esisteva una CKAGV movement, cioè qualcosa del genere. Cioè non capisco perché abbiamo alla fine la CK material call come.

_[immagine]_**  
Alessia Traverso** 16:19  
Sì.

_[immagine]_**  
Fabio Massone** 16:35  
Per risposta della GV Movement, cioè io da come ricordo erano 4, 2 per la material call e due per la GV Movement, una era la reply e una la GK.

_[immagine]_**  
Jacopo Revello** 16:47  
La CKAGV Movement corrisponde alla CK material call contiene esattamente la stessa struttura. Sulla base del 3 6 D viene recuperato qual è la chiamata e quindi sulla base di quello si capisce se è una chiamata GV o una material call.  
Ale correggimi se sbaglio, ma ricordo.

_[immagine]_**  
Alessia Traverso** 17:07  
No, è giusto, è giusto, ho fatto la modifica così.

_[immagine]_**  
Fabio Massone** 17:10  
OKOK, allora ero rimasto io indietro AA com'era vecchio, OK, va bene.

_[immagine]_**  
Jacopo Revello** 17:15  
Alessio.

_[immagine]_**  
Alessio Monaco** 17:17  
No domanda prima mi ha detto che il V number sebi il planta d lo 01110111 mi sembra no per chi chiamarlo V number.

_[immagine]_**  
Jacopo Revello** 17:24  
Sì.  
Me lo chiedo anch'io, me lo son chiesto anch'io e non mi hanno mai dato una risposta perché loro avevano già questa impostazione qua di questo messaggio e quindi han voluto mantenere uno standard loro.  
E l'abbiamo provato a chiedere e questo non ci han dato una risposta.

_[immagine]_**  
Alessio Monaco** 17:43  
Ok.  
OKOK.

_[immagine]_**  
Jacopo Revello** 17:49  
È una cosa loro e quindi infatti noi abbiamo semplicemente una, cioè noi abbiamo un lato Connect home, c'è un sistema, c'è un servizio che si chiama mapping che fondamentalmente recupera LXMLE lo traduce.  
Per chiamare il comando nel workflow, quindi fondamentalmente.  
La.  
Il sistema fa, fa, fa fondamentalmente la traduzione da quello che no, scusa, non è mapper in realtà nel workflow in questo caso, perché è un messaggio in input, però di per sé.  
Recupera le estrae le informazioni e le passa al comando secondo come gli serve. Nel nostro caso il comando mi sembra che abbia come input Plant IDO una cosa del genere, però in realtà il Plant a noi non serve tanto a livello di comando perché logicamente i comandi.  
Sono già orientati al Plant perché sono girano sui worker di Plant. A noi il Plant serve per Connect mom per poter permettere AA Connect mom di chiamare il comando verso il Plant giusto, quindi noi usiamo quel.  
O number per capire di quale plant, a quale pent devo portare il messaggio una volta in base a quello chiamo il comando worker di quel plant.  
OK.

_[immagine]_**  
Alessio Monaco** 19:14  
Caro.

_[immagine]_**  
Jacopo Revello** 19:15  
Io ragazzi vi devo abbandonare perché sono un po' incasinato se volete analizzare il problema che appunto c'è stato adesso quindi che non abbiamo portato a termine la CK è sicuramente un ottimo debugging perché vedete anche tutta la parte di Connect mom.  
Ed è interessante capire anche i log di connect mom eccetera eccetera.  
Se invece volete proseguire con il processo, però, direi che il processo l'abbiamo visto più o meno tutti, c'era questa parte di AGV che forse non avevamo visto, ma appunto, non c'è nulla di più di quello che avete appena visto, se non la parte di staging call e di.  
Complete.  
E niente, io devo proprio scappare.  
OK, non so se Juela, cioè Juela comunque può aiutare se avete bisogno di questioni di processo, se no il mio suggerimento è utilizzare questo use case che abbiamo appena visto per.  
Capire anche un po' come si debba l'atto con per capire un po' anche come dove andare a vedere i log che può essere sempre utile anche in fase di Live quando siete lì, capire dov'è che si è rotto, chi si è rotto.  
Perché non è arrivato un messaggio, perché non è stato mandato, è interessante.  
Se no vedete voi, OK?

_[immagine]_**  
Fabio Massone** 20:47  
OK.

_[immagine]_**  
Jacopo Revello** 20:48  
Bueno, Ciao ragazzi, buona continuazione, Ciao Ciao.

_[immagine]_**  
Fabio Massone** 20:50  
Grazie Ciao.

_[immagine]_**  
Alessio Monaco** 20:51  
Ciao Ciao.

_[immagine]_**  
Giacomo Centore** 20:51  
Ciao Ciao.

_[immagine]_**  
Fabio Massone** 21:01  
Quindi Ale.

_[immagine]_**  
Alessio Monaco** 21:02  
Chi, chi, chi, chi, chi conduce le ricerche su un morto?

_[immagine]_**  
Fabio Massone** 21:09  
Alessia, scusa.

_[immagine]_**  
Alessia Traverso** 21:11  
Dimmi, Fabio.

_[immagine]_**  
Fabio Massone** 21:12  
E se ho capito bene, la CK material call è quella a cui rispondono loro per entrambi, sia per la material call che per l'Agebo Movement.

_[immagine]_**  
Alessia Traverso** 21:25  
Sì.

_[immagine]_**  
Fabio Massone** 21:26  
E sulla base di quello poi tu chiami la CNM response, mettendoci la stringa col Type giusto per noi, cioè per il back-end.

_[immagine]_**  
Alessia Traverso** 21:37  
Esatto.

_[immagine]_**  
Fabio Massone** 21:38  
E quindi? Poi noi abbiamo le quattro stringhe diverse, non è cambiato lato backend, è cambiato solo lato connectmon, cioè è cambiato, cioè c'è una logica che fa puoi passare il type correct.

_[immagine]_**  
Alessia Traverso** 21:43  
No.  
Allora questa qua l'ha chiamata Alessandro GV.  
E la stavo guardando. E c'è anche quella, la c'è un response, è questa.

_[immagine]_**  
Fabio Massone** 22:05  
Sì.

_[immagine]_**  
Alessia Traverso** 22:10  
E qui, esatto.

_[immagine]_**  
Fabio Massone** 22:12  
E sta lo switch case sotto, se non ricordo.  
Quindi è stato tolto qualcosa.

_[immagine]_**  
Alessia Traverso** 22:20  
Sì.

_[immagine]_**  
Fabio Massone** 22:21  
A meno che io non ho un codice più recente, può anche essere.

_[immagine]_**  
Alessia Traverso** 22:22  
CK material cool.

_[immagine]_**  
Fabio Massone** 22:29  
Scusa, comprimi un attimo i case.  
Con la freccettina per vedere se ce l'hai tutti e no aspetta solo i case, non tutto lo switch.  
Voglio vedere se nel codice però mi dice sono sempre tutti e quattro.  
E quindi il message Type lo manda Connect mom sulla base di regole di Connect mom, giusto? OK, una cosa che ho notato su pagina è che è arrivato prima la ACK material call.

_[immagine]_**  
Alessia Traverso** 22:54  
Esatto, sì.

_[immagine]_**  
Fabio Massone** 23:04  
In seguito alla GVM.  
Maggiore che abbiamo dato rispetto alla reply material scusa rispetto alla reply a GV movement, mentre di solito dovrebbe essere il contrario, no?

_[immagine]_**  
Alessia Traverso** 23:09  
Dai, ti è arrivata prima questa qua.

_[immagine]_**  
Fabio Massone** 23:22  
No, è arrivata prima la CKE, poi la reply.

_[immagine]_**  
Alessia Traverso** 23:28  
Ma a livello qua, quando l'hai visto qui?

_[immagine]_**  
Fabio Massone** 23:29  
No sulla sulla lista di Connect Mom se tu torni sui messaggi di Connect Mom.

_[immagine]_**  
Alessia Traverso** 23:33  
Questo tu dici?

_[immagine]_**  
Fabio Massone** 23:36  
Vedi che la TV movement ti ha chiamata, l'ha chiamata giusto quella delle 12, 21 e 30.

_[immagine]_**  
Alessia Traverso** 23:44  
Sì.

_[immagine]_**  
Fabio Massone** 23:44  
È una chiamata, quella russa, quella in errore.

_[immagine]_**  
Alessia Traverso** 23:47  
Sì, questa qua è quella che praticamente da opicenter noi lanciamo quando andiamo dalla repetitive, noi lanciamo quando andiamo a fare la chiamata che abbiamo fatto prima dalla repetitive, quindi da qua.

_[immagine]_**  
Fabio Massone** 24:00  
OK, l'errore è sulla chiamata.

_[immagine]_**  
Alessia Traverso** 24:03  
L'errore sulla chiamata, che poi non è detto che sia un errore vero e proprio.

_[immagine]_**  
Fabio Massone** 24:05  
Emanuele.  
Non ho capito perché, però, cioè qual è, qual è il problema qua?

_[immagine]_**  
Alessia Traverso** 24:13  
È questa qua.

_[immagine]_**  
Fabio Massone** 24:14  
A questo scusa.  
Da qua non capisco nulla.

_[immagine]_**  
Alessia Traverso** 24:26  
Perché noi chiamiamo, noi chiamiamo questa Brembo integration DEV a un api esposta da CPIO da.  
Perché noi li mandiamo la nostra richiesta verso di loro, però il problema è che noi qua non riusciamo a raggiungerli, perché se io vado a vedere sul log del Connect Mom.  
Prego.

_[immagine]_**  
Fabio Massone** 25:08  
Era alle 02:12.  
Sì.

_[immagine]_**  
Alessia Traverso** 25:11  
Perché?

_[immagine]_**  
Fabio Massone** 25:13  
Era 02:12 l'orario, se non ricordo male, 2, 12 e 30.

_[immagine]_**  
Alessia Traverso** 25:17  
Allora la prima potrebbe è questa, aspetta che io adesso qua io me lo guardo.  
Reply a GV movement.  
E parte lo.

_[immagine]_**  
Fabio Massone** 25:36  
Però la reply arriva dopo che noi l'abbiamo mandata.

_[immagine]_**  
Alessia Traverso** 25:38  
Quindi aspetta.  
La reply è la chiamata successiva, bisogna riuscire a capire perché il problema del che non sappiamo quale, cioè quale dei adapter parte, se sulla macchina due o sulla macchina tre o sulla macchina uno, quindi bisogna guardarli tutti i log, un po' come.

_[immagine]_**  
Fabio Massone** 25:56  
Tutti i log sempre.

_[immagine]_**  
Alessia Traverso** 25:57  
Ci spiegava l'altra volta sia Juela che Jacopo per mendix.

_[immagine]_**  
Fabio Massone** 26:04  
Sì.

_[immagine]_**  
Alessia Traverso** 26:06  
Qua sicuramente no, perché l'ultima è alle.  
12 e 52 allora vediamo, sì, qua sono io che ho fatto gli aggiornamenti.  
AGV Movement, eccola, questa qua è la chiamata che noi facciamo verso di loro e poi ci arriva la CK material call dove parte il la chiamata diciamo.  
Del di risposte di CPI.

_[immagine]_**  
Fabio Massone** 26:40  
Ma mi chiedo, come ho fatto ad arrivare prima alla CK della Reply?

_[immagine]_**  
Alessia Traverso** 26:50  
Te lo so dire perché secondo me lui fa dei tentativi e se non riceve risposta comunque.

_[immagine]_**  
Fabio Massone** 26:58  
Ma dopo due secondi, cioè nel senso, cioè in.  
Cioè diciamo che non sono riuscito a capire l'errore dov'è, cioè non come risolverlo ma non ho capito l'errore dov'è perché vedo l'errore sulla request però poi comunque è arrivata la reply ma è arrivata dopo la CK non riesco a capire che cosa sia successo.

_[immagine]_**  
Alessia Traverso** 27:10  
Allora perché di.  
Allora il discorso è questo qua, abbiamo fatto settimana scorsa i sit su AGVE non è funzionato perché sembrava che non ci mandassero tutte le informazioni o comunque noi avevamo dei problemi.  
Dato, cioè noi non avevamo dei problemi perché noi le chiamate le facevamo in modo corretto.  
E in realtà non funzionavano perché non funzionavano gli ERP non so come dire allora poi Francesca ci ha un attimino guardato e lei mi ha detto che come risposta della CK material.  
Col response che è la quella che diciamo, la risposta che mandiamo noi verso di loro, questo è questo qua. Il messaggio quindi, come se loro non riuscissero a trovare noi non riuscissimo a trovare all'interno della nostra ACK material.  
Fumando il materiale e il buffer.  
E quindi mi diceva, questo qua è un problema lato vostro, non è un problema lato nostro e allora stavo un attimino indagando per capire qual era il problema che per il fatto che non gli rispondevamo con questo messaggio qua.

_[immagine]_**  
Fabio Massone** 28:46  
Santi di output messages sono i record della tabella out MSG.

_[immagine]_**  
Alessia Traverso** 28:52  
Esatto, esatto, esattamente perché noi, guardando io un po il codice, ho visto che.

_[immagine]_**  
Fabio Massone** 28:58  
E c'è anche l'errore -31.012, dovresti ritrovare il punto esatto in cui scoppia, non so sarà qua su SAP Interface.

_[immagine]_**  
Alessia Traverso** 29:01  
Io l'ho visto, esatto.

_[immagine]_**  
Fabio Massone** 29:10  
Esatto, sarà duplicato magari.

_[immagine]_**  
Alessia Traverso** 29:10  
A profitto.  
OK.

_[immagine]_**  
Fabio Massone** 29:16  
Ciao.

_[immagine]_**  
Alessia Traverso** 29:16  
Faremo sì, però se io lo faccio qua no, soltanto qua ce l'abbiamo un po ovunque.

_[immagine]_**  
Fabio Massone** 29:21  
Sul current document no file su entire solution come prima curiosità.  
Perché vedi bisognerebbe metterli diversi STI affari qua io li cambio copia incolla va bene tanti son punto back i backup.  
Scorri sotto.  
Guarda un attimo il send AGV Movement.  
Ma però per la stessa.

_[immagine]_**  
Alessia Traverso** 29:57  
Questo si può anche.

_[immagine]_**  
Fabio Massone** 29:58  
Si, no penso a te.

_[immagine]_**  
Alessia Traverso** 29:59  
Sì.

_[immagine]_**  
Fabio Massone** 30:02  
Però vedi qua manda buffer material.

_[immagine]_**  
Alessia Traverso** 30:04  
E noi e noi facciamo la stessa cosa perché l'errore sia sul buffer che se non tiri.

_[immagine]_**  
Fabio Massone** 30:09  
Però è una sembra un'eccezione non gestita perché siamo in un catch.

_[immagine]_**  
Alessia Traverso** 30:16  
Sì.

_[immagine]_**  
Fabio Massone** 30:19  
Questa è la io questo qua non l'ho fatto, non lo so, create message.  
Designer generated fault, ma ti da mi tassi need gli si crea il nome del cos'è il nome del messaggio, quello di vero.

_[immagine]_**  
Alessia Traverso** 30:34  
Sì.

_[immagine]_**  
Fabio Massone** 30:39  
Potrebbe essere che esiste già il messaggio.

_[immagine]_**  
Alessia Traverso** 30:43  
Non so, no, teoricamente no, perché ci mette anche la data e l'ora, quindi teoricamente non può essere lo stesso.

_[immagine]_**  
Fabio Massone** 30:44  
Non sia vivo con non lo so.  
Sì.  
Mette anche cliccare un attimo fine sulla tastiera.  
Sì, ci mette anche i millisecondi, quindi non dovrebbe ripetersi, diciamo è quasi impossibile.

_[immagine]_**  
Alessia Traverso** 31:08  
In exacto.

_[immagine]_**  
Fabio Massone** 31:10  
Anzi, più dei millisecondi.

_[immagine]_**  
Alessia Traverso** 31:11  
Queste sono le.

_[immagine]_**  
Fabio Massone** 31:14  
Sì, però fallisce nella creazione del messaggio, quindi comunque fallisce il comando di prodotto, quindi vuoi qualche parameter qualche parameter tipo quella out MSG Definition revision list.  
Se selezioni la variabile, quella a fianco a destra.

_[immagine]_**  
Alessia Traverso** 31:29  
Questa scusami.

_[immagine]_**  
Fabio Massone** 31:34  
Sì, esatto, guarda un po dov'è che è definita.  
New list per guardare un po dove la riempie.

_[immagine]_**  
Alessia Traverso** 31:44  
L'ora di un po.

_[immagine]_**  
Fabio Massone** 31:44  
Fai un fa, fai un find, fai control F della variabile non ha della variabile proprio.

_[immagine]_**  
Alessia Traverso** 31:46  
Tutto vedendo che c'è anche questo video.  
Scusami, sei uscita con un'offerta?

_[immagine]_**  
Fabio Massone** 31:51  
Così almeno vediamo dove fa l'AD della lente da questa.

_[immagine]_**  
Alessia Traverso** 31:57  
Qua gli mettiamo.  
Message definition need e message definition revision.

_[immagine]_**  
Fabio Massone** 32:09  
Allora se automessage fosse null non arriveremmo neanche lì perché fa la return prima.  
Quindi in teoria non è no, quindi o sono sbagliati quei valori?

_[immagine]_**  
Alessia Traverso** 32:21  
No.  
Sì, ci proviamo.

_[immagine]_**  
Fabio Massone** 32:32  
E c'è il logo persistito, si può vedere magari qualcosa sul persistere. Intanto non so, è allenamento per tutti.  
Giusto, giusto? Sì, perché vedo che poi.

_[immagine]_**  
Alessia Traverso** 32:44  
Però aspetta, non devo andare sul Connect mo, ma devo andare sul Plant quello.

_[immagine]_**  
Fabio Massone** 32:48  
Sulle macchine di Ib, sì.

_[immagine]_**  
Alessia Traverso** 32:52  
Se qua quella di.  
Non so se ci fosse qualcuno qua, giusto Fabio?

_[immagine]_**  
Fabio Massone** 33:17  
Secondo me no, questo qua mi sa che DV 10 sono IDB di run time.

_[immagine]_**  
Alessia Traverso** 33:24  
Quindi devo andare sul aspetta, aspetta, aspetta, aspetta che lo so.

_[immagine]_**  
Fabio Massone** 33:24  
Bisognerebbe cercare.

_[immagine]_**  
Alessia Traverso** 33:34  
Questo qua dovrebbe essere quello l'archiving, diciamo.

_[immagine]_**  
Fabio Massone** 33:41  
No.  
Non mi sembra.  
Aspetta 101214.

_[immagine]_**  
Alessia Traverso** 33:45  
No.  
Sì, perché vanno.

_[immagine]_**  
Fabio Massone** 33:53  
Beh, sarà un numero tra 10 e 15, probabilmente.

_[immagine]_**  
Juela Ndoka** 33:59  
C'è un secondo sul listener, non sono lì, poi non finiscono tutti lì.  
Qual è il codice?

_[immagine]_**  
Fabio Massone** 34:05  
Ma ci sarà quel listener, ci sarà il listener dei DB di run time e il listener di quelli di offline.

_[immagine]_**  
Alessia Traverso** 34:08  
Poi dici.

_[immagine]_**  
Fabio Massone** 34:13  
Penso per come il nostro.

_[immagine]_**  
Alessia Traverso** 34:15  
Quindi abbiamo messo il profiler.  
Qua sono collegate sul 14.

_[immagine]_**  
Juela Ndoka** 34:32  
Eccole, persistent love.

_[immagine]_**  
Alessia Traverso** 34:33  
OK, eccolo qua.

_[immagine]_**  
Fabio Massone** 34:34  
Ok.

_[immagine]_**  
Alessia Traverso** 34:46  
Quindi vado su questa.

_[immagine]_**  
Fabio Massone** 34:48  
Sull'ultima.  
Sì.

_[immagine]_**  
Alessia Traverso** 34:57  
Ce l'abbiamo un timestamp timestamp.

_[immagine]_**  
Fabio Massone** 35:04  
Probabilmente.  
Mi fai anche order by ID che è ancora forse più veloce perché forse se a chiave fa prima ordinare.

_[immagine]_**  
Alessia Traverso** 35:16  
Se sono de Lucia.

_[immagine]_**  
Fabio Massone** 35:18  
Tanto è crescente, tipo una identity, ti ho detto.  
OK 1500.

_[immagine]_**  
Alessia Traverso** 35:31  
1500 sono le due.

_[immagine]_**  
Fabio Massone** 35:33  
Come fa a essere le 1500.

_[immagine]_**  
Alessia Traverso** 35:38  
Però no, è sbagliato Fabio, perché questo qua no? Ma è della data di ieri, 13, 4 qua e 14.

_[immagine]_**  
Fabio Massone** 35:40  
E un quarto d'ora avanti.

_[immagine]_**  
Juela Ndoka** 35:49  
Vai sulla mia cartella, dovresti avere lo query se hai una Select in cui hai timestamp provider name questo magari più facile lo query sì e prendi la prima, poi cambi solo il DB, prendi il primo Select.

_[immagine]_**  
Fabio Massone** 35:49  
Sì.

_[immagine]_**  
Alessia Traverso** 35:58  
Allora m'hai detto, scusami, mi devi.  
Abbiamo fatto Gianmarco, quindi io avevo perdita con tutto, non mi ricordo più.

_[immagine]_**  
Juela Ndoka** 36:06  
Flavio, come mai?

_[immagine]_**  
Alessia Traverso** 36:12  
Dai.

_[immagine]_**  
Juela Ndoka** 36:12  
Cambia il persistent, metti curno, poi per altro dovrebbe essere uguale, esatto.

_[immagine]_**  
Alessia Traverso** 36:20  
E la data maggiore?

_[immagine]_**  
Juela Ndoka** 36:22  
Time Samp, quello lì, metti la data di oggi.

_[immagine]_**  
Alessia Traverso** 36:30  
Forse.

_[immagine]_**  
Juela Ndoka** 36:34  
E magari le dopo l'una come scrive dopo 11 fai fai spazio 1100 così riduciamo.

_[immagine]_**  
Alessia Traverso** 36:41  
Sì.  
Però non tira proprio su nulla, ragazzi.

_[immagine]_**  
Juela Ndoka** 36:47  
Flavio.

_[immagine]_**  
Fabio Massone** 36:47  
Sì, perché arriva fino arriva fino a ieri alle 15.

_[immagine]_**  
Alessia Traverso** 36:48  
Perché che.

_[immagine]_**  
Juela Ndoka** 36:53  
Non stiamo scrivendo super system cloud.

_[immagine]_**  
Alessia Traverso** 36:55  
Sembrerebbe di no.

_[immagine]_**  
Juela Ndoka** 36:58  
Questo è da.

_[immagine]_**  
Fabio Massone** 37:00  
Che bello sto prodotto.

_[immagine]_**  
Juela Ndoka** 37:00  
Da segnalarla.  
Emanuele la seconda, ma.

_[immagine]_**  
Fabio Massone** 37:07  
Ero io.

_[immagine]_**  
Alessio Monaco** 37:08  
Non puoi fare un riavvio dell'applicativo di Descriver.

_[immagine]_**  
Alessia Traverso** 37:10  
C'è, ma non c'è più.  
E quindi io guardi, OK, no?

_[immagine]_**  
Juela Ndoka** 37:20  
Ma commenta un secondo timestamp e fai di nuovo order by desk strano.

_[immagine]_**  
Alessia Traverso** 37:23  
Scusami, scusami, scusami, scusami.

_[immagine]_**  
Juela Ndoka** 37:26  
m a a.  
Ma non ti preoccupare.  
Flavio.

_[immagine]_**  
Alessia Traverso** 37:37  
No, arrivano fino a ieri.

_[immagine]_**  
Juela Ndoka** 37:40  
Cosa è successo ieri alle tre?  
È stata l'ultima volta.

_[immagine]_**  
Alessia Traverso** 37:44  
Vita.

_[immagine]_**  
Fabio Massone** 37:45  
Per un po il messaggio, no Update.

_[immagine]_**  
Alessia Traverso** 37:52  
Potrebbe essere qualcosa della GV questo?

_[immagine]_**  
Juela Ndoka** 37:56  
Perrone.  
Emanuele.

_[immagine]_**  
Alessia Traverso** 38:03  
Ci fu, non è che comunque a me.

_[immagine]_**  
Juela Ndoka** 38:04  
Sembra di sì, perché quello non è una delle macchine, quello no, infatti no 0 4 e fa Foundation quattro.

_[immagine]_**  
Alessia Traverso** 38:18  
Sì.

_[immagine]_**  
Fabio Massone** 38:22  
Penso anche gli altri nodi hanno avuto sta roba solo quattro.

_[immagine]_**  
Juela Ndoka** 38:26  
Fai un secondo anche, ma bello un secondo anche.

_[immagine]_**  
Fabio Massone** 38:28  
Non è tutti c'è l'hanno espandilo un po il messaggio appena appena sulla destra, scusa solo per vedere se.

_[immagine]_**  
Alessia Traverso** 38:32  
Sì, ci dobbiamo incassare bene 422.

_[immagine]_**  
Juela Ndoka** 38:34  
Ecco.  
Questo non è un errore, comunque è un.

_[immagine]_**  
Fabio Massone** 38:39  
Sì, lo so che non è un errore, ma era per capire le ultime cose che ha loggato se c'entrano col fatto che ha smesso di loggare.

_[immagine]_**  
Alessia Traverso** 38:40  
Qualche altra spinta, quindi eventualmente?  
Proviamo a farlo.  
E questo qua fino a ieri alle.

_[immagine]_**  
Juela Ndoka** 39:08  
E ieri cosa abbiamo fatto? Abbiamo fatto qualcosa, Irene.

_[immagine]_**  
Alberto Grillo** 39:17  
Grillo, il pomeriggio era tutto fermo.

_[immagine]_**  
Juela Ndoka** 39:20  
Era tutto fermo, tutti li ho, tutto quanto.

_[immagine]_**  
Alberto Grillo** 39:23  
Aspetta che ti dico anche che ora era.

_[immagine]_**  
Juela Ndoka** 39:27  
A l'etra es messa.  
Questo.

_[immagine]_**  
Alberto Grillo** 39:43  
Alle due erano spenti, l'ultimo appello c'era solamente il primo in errore, io ho chiesto infatti alle due e alle 02:45 ho riavviato tutti io e gli host.

_[immagine]_**  
Juela Ndoka** 39:57  
E però per il system log è rimasto giù, riusciamo? Riesci a scriverlo ad Andrea? Chiedo io al.

_[immagine]_**  
Fabio Massone** 40:07  
Intanto, scusate un attimo, solo un'informazione, quel time stamp sono Le 5 italiane, le quattro italiane o sono le tre italiane? Giusto per avere un'idea, perché magari ti ho fermato dopo.

_[immagine]_**  
Alessia Traverso** 40:07  
\*\*\*\*, però.  
Per esempio, se uno ha un 20% no perché mi dice.

_[immagine]_**  
Fabio Massone** 40:22  
È loca.  
OK, OK, OK.  
In effetti anche il timestamp che va con get the date, non con get tutti sì date.

_[immagine]_**  
Juela Ndoka** 40:36  
Si no, qui sì, su come mo non mi ricordo com'è.

_[immagine]_**  
Alessia Traverso** 40:40  
Sì.  
No.

_[immagine]_**  
Fabio Massone** 40:44  
Quindi dovrebbero essere le tre italiane.  
Per gli ospiti hai startati uno per volta.

_[immagine]_**  
Alessia Traverso** 40:51  
Sì.

_[immagine]_**  
Alberto Grillo** 40:54  
Sì.

_[immagine]_**  
Fabio Massone** 40:55  
E ti ricordi anche l'ordine tipo l'uno?

_[immagine]_**  
Alberto Grillo** 40:59  
Questa è una bella domanda.

_[immagine]_**  
Fabio Massone** 41:01  
Erano tutti giù, giusto, hai detto?

_[immagine]_**  
Alberto Grillo** 41:03  
Per entrare giù è un errore, devo aver riavviato tutti e tre, devo aver spostato la roba dal primo agli altri tre e poi ho riavviato il primo, cioè l'ho stoppato e riavviato.

_[immagine]_**  
Fabio Massone** 41:05  
Ok.

_[immagine]_**  
Alessia Traverso** 41:08  
Aspetta.  
Va.

_[immagine]_**  
Fabio Massone** 41:16  
Praticamente era il primo che comandava sta roba qui. Magari l'hai startato per ultimo alle tre perché hai detto che ha iniziato alle 02:45, magari alle tre hai startato l'ultimo e quando hai spostato la roba si è bloccato sto coso.

_[immagine]_**  
Alberto Grillo** 41:21  
Sì.  
Esatto.  
Probabile.  
Ho mandato uno screenshot sull'auto Italia con scritto ieri alle tre ore tutto su.

_[immagine]_**  
Fabio Massone** 41:37  
Sì, quindi direi che era l'host in error che ha avuto qualche problema o che comunque non sa gestire quello spostamento che si fa dall'host monitoring con i bottoni perché magari si è bloccato lì ma non l'ha più fatto ripartire.

_[immagine]_**  
Alessia Traverso** 41:58  
Lasciali stoppati fino a quando non arrivano il backup di sono stati stoppati apposta, ragazzi persistenti.

_[immagine]_**  
Juela Ndoka** 42:08  
No te lo ha scritto Andrea.

_[immagine]_**  
Alessia Traverso** 42:09  
Sì, gli ho scritto ma i persistent log su sono stoppati su QA come si fanno a riavviare? Lui mi ha risposto, lasciali stoppati fino a quando non attivi un backup di DB non conviene accenderli.

_[immagine]_**  
Juela Ndoka** 42:10  
Ok, perfetto allora.  
OK, va bene, allora perché magari riempiono troppo e andiamo, cioè occupiamo tutto lo spazio, va bene, allora non possiamo, cioè dobbiamo probabilmente lanciare un ETW.  
E fare rifare l'azione.

_[immagine]_**  
Alessia Traverso** 42:42  
OK.  
E anche loro.

_[immagine]_**  
Juela Ndoka** 42:53  
Allora tutto quello che vediamo su persistent lock viene tracciato anche su ETW qua su Foundation Trace Bware.  
Aspetta, scegliamo i provider.

_[immagine]_**  
Alessia Traverso** 43:11  
Ci.

_[immagine]_**  
Juela Ndoka** 43:17  
Providers, allora ti direi, facciamo business logic verbals?

_[immagine]_**  
Alessia Traverso** 43:19  
Tenevo questo 100%.

_[immagine]_**  
Juela Ndoka** 43:29  
Facciamo un.

_[immagine]_**  
Alessia Traverso** 43:36  
Allora incendio bug, mi hai Detto questo?

_[immagine]_**  
Juela Ndoka** 43:38  
Esatto, quello con debug lo facciamo.  
Un'altro cosa facciamo, facciamo sì quel profiling, anche log uno perché sono sviluppi, quindi direi che avete scritto anche lì.

_[immagine]_**  
Alessia Traverso** 43:48  
Sì.

_[immagine]_**  
Juela Ndoka** 43:56  
Sì, quel profiling OK, proviamo con.

_[immagine]_**  
Fabio Massone** 43:59  
Aspetta di mettere, metti prima error sugli altri, sennò ti logga tutto a meno che non vorresti lasciare information, è vero?

_[immagine]_**  
Juela Ndoka** 44:07  
Non lo so perché non c'è.  
La parte di Connect non so bene quale potrebbe essere il provider poi dalla da vedere, ma direi che business logic va bene che tanto chiama un comando quello quando lo crea su un po sotto.

_[immagine]_**  
Alessia Traverso** 44:21  
Sì.

_[immagine]_**  
Juela Ndoka** 44:25  
Papà qualcosa abbiamo.  
No, direi che va bene.  
Va bene.

_[immagine]_**  
Alessia Traverso** 44:35  
OK, sì.

_[immagine]_**  
Juela Ndoka** 44:35  
Ora aggiungi uno a zero nel Max messages.  
OK, perfetto, prova fai start, vediamo ieri con Alberto non scrive.

_[immagine]_**  
Fabio Massone** 44:45  
Eri al time from a Monaco, no?

_[immagine]_**  
Juela Ndoka** 44:48  
L'ho fatto, l'ho fatto. Hai fatto Real Time? No, non l'hai fatto.

_[immagine]_**  
Fabio Massone** 44:49  
E no.  
Non l'ha preso, non l'ha preso.

_[immagine]_**  
Alessia Traverso** 44:59  
OK.

_[immagine]_**  
Juela Ndoka** 45:02  
Sto scrivendo, pensa che no sto scrivendo nulla.

_[immagine]_**  
Alessia Traverso** 45:08  
New a Rossi.

_[immagine]_**  
Juela Ndoka** 45:08  
Ah.  
Ma non vedo messages entrare.

_[immagine]_**  
Alessia Traverso** 45:15  
Sì, anch'io.

_[immagine]_**  
Fabio Massone** 45:16  
Prima entravano sul nodo singolo, mi sembra.

_[immagine]_**  
Juela Ndoka** 45:19  
A sul modo singolo però non sai, non lo becchi mai. Anche ieri con Alberto abbiamo provato con automation get, poi però non.

_[immagine]_**  
Fabio Massone** 45:26  
Sì, però è strano che quando lo fai Real Time from the note non funzioni proprio, cioè dovrebbe beccare solo quelli.

_[immagine]_**  
Juela Ndoka** 45:31  
Non c'è qualcosa, c'è qualcosa che non va, questo vuol dire esatto.

_[immagine]_**  
Alberto Grillo** 45:34  
C'è qualcosa che non va, anche ieri Jacopo se n'è accorto.

_[immagine]_**  
Fabio Massone** 45:34  
Sì, c'è qualcosa di rotto.

_[immagine]_**  
Alessia Traverso** 45:36  
Sì.

_[immagine]_**  
Juela Ndoka** 45:42  
Non lo so perché è spento, cosa sta succedendo con queste.

_[immagine]_**  
Alessia Traverso** 45:51  
Questo warning non vuol dire nulla, no, ti avviso solo che è stato cambiato.

_[immagine]_**  
Juela Ndoka** 45:57  
Dunque scusa, non vedo.

_[immagine]_**  
Fabio Massone** 45:59  
Configuration change.

_[immagine]_**  
Juela Ndoka** 46:01  
Sì, no, non vuol dire niente. Quello però non vedo arrivare il messaggio, non so cosa successo.

_[immagine]_**  
Alessia Traverso** 46:06  
Però qua mi dice che non sono come no, sono allevato come amministratore.

_[immagine]_**  
Fabio Massone** 46:09  
In teoria scusate, configuration changed non viene quando c'hai già l'i TW aperto e fai un deploy che devi rilanciarlo.

_[immagine]_**  
Juela Ndoka** 46:11  
Sì.  
Sì, però noi non ce l'avevo, cioè l'abbiamo aperto ora, quindi non sì.

_[immagine]_**  
Fabio Massone** 46:22  
L'ha aperto adesso, OKOK.

_[immagine]_**  
Juela Ndoka** 46:25  
Allora l'unica cosa che ti farei fare però non so se funziona è questo, vai un secondo supplente.  
L'abbiamo provato anche ieri, però non plant configuration.  
Riporta clicca curr.  
Riportalo di là e aggiungilo di qua.  
Corno, no, ora hai aggiunto un appello sulla Stella configuration aggiungi aggiungi tutti e due.  
OK, fai OK, vai di nuovo su providers.  
Restore default settings.  
OK, fai OK, lascialo un attimo così, poi magari li cambiamo, fai di nuovo Real Time from all notes.  
A Jacopo de a Jacopo de fai start.  
No, non trova.

_[immagine]_**  
Fabio Massone** 47:25  
Ci mette anche tanto a partire.

_[immagine]_**  
Juela Ndoka** 47:28  
Non ce la fa.

_[immagine]_**  
Fabio Massone** 47:42  
Tra un po l'host monitoring o lo stato degli host adesso con me?  
Per curiosità, signora.  
Intanto scusa Elisa, faccio una domanda che magari tu lo sai, ho visto che nelle Side provider c'era un tanto son tutti spenti gli host, tutti stop.

_[immagine]_**  
Alessia Traverso** 48:04  
A parte il primo.

_[immagine]_**  
Fabio Massone** 48:05  
Bene.

_[immagine]_**  
Alberto Grillo** 48:05  
Sì, li ha messi, li ha messi così Jacopo.

_[immagine]_**  
Juela Ndoka** 48:05  
No, il primo, il primo.  
OK allora se l'ha messo così posizionati su Curno sul Foundation uno e andiamo di facciamo il mod Real Time visto che abbiamo solo uno lì, quindi gestisce uno le chiamate.  
Sei su Foundation uno.

_[immagine]_**  
Alessia Traverso** 48:28  
Sì, foundation.

_[immagine]_**  
Juela Ndoka** 48:29  
Allora vai di nuovo in Plance, butta fuori mapello.

_[immagine]_**  
Alessia Traverso** 48:34  
Sì.

_[immagine]_**  
Juela Ndoka** 48:37  
Lascia solo Curno, OK, fai OK.  
Fai fai mod Real Time.

_[immagine]_**  
Fabio Massone** 48:46  
Delta.

_[immagine]_**  
Juela Ndoka** 48:50  
Sonno start un attimo.  
Vediamo se arriva qualcosa su Corno, OK, perfetto per nostra fortuna c'è solo un ostativo, quindi va per forza lì, OK?

_[immagine]_**  
Fabio Massone** 48:53  
Flavio.  
Così va.  
Posso farti una domanda? Intanto visto che c'era un log due è nostro nei provider c'era log due. Che cosa ci funziona? Viene usato?

_[immagine]_**  
Juela Ndoka** 49:05  
Sì.  
Toma.  
Non lo so, non credo. Io ho sentito solo log uno finora.

_[immagine]_**  
Fabio Massone** 49:15  
Ok, OK.  
Infatti, infatti per quello che devo da dove arrivasse va bene.

_[immagine]_**  
Juela Ndoka** 49:22  
OK, rifacciamo la chiamata, Pulisci qui se vuoi.  
OK.  
Quello bisogna tacciarlo.  
Sta andando in errore?  
Qualcosa sta succedendo.

_[immagine]_**  
Fabio Massone** 49:43  
Il cavo.

_[immagine]_**  
Juela Ndoka** 49:43  
Mi sentita?

_[immagine]_**  
Fabio Massone** 49:45  
Sì.

_[immagine]_**  
Juela Ndoka** 49:46  
Ok, bisogna fermarsi, trovare l'errore.

_[immagine]_**  
Alessia Traverso** 49:51  
OK, allora mi fermo io.

_[immagine]_**  
Juela Ndoka** 49:53  
Sì, andiamo pure in W.  
Filtran, la Barro.

_[immagine]_**  
Fabio Massone** 50:07  
A Globaldo, mi salen un i verbo, no information.

_[immagine]_**  
Juela Ndoka** 50:09  
Non fa niente, è scoppiato brutalmente.

_[immagine]_**  
Fabio Massone** 50:14  
Hai ragione, non c'era sicuro.

_[immagine]_**  
Juela Ndoka** 50:17  
Ok, prendi l'ultimo.  
Cosa, cosa está succedendo?  
Authorization is being denied.  
Mai sopra.  
Authentication fail, ma sei loggata?

_[immagine]_**  
Alessia Traverso** 50:37  
È scaduta la sessione? No, infatti non è che è scaduta la sessione.

_[immagine]_**  
Juela Ndoka** 50:42  
Ma dovrebbe riuscirti a fare mandarti in login. Infatti tutte le altre sono andati in login. Vedo un'altro Tab accanto a login, rifai login.

_[immagine]_**  
Alessia Traverso** 50:49  
Sì, il 25% sulla RMS.

_[immagine]_**  
Fabio Massone** 50:54  
Aveva già fatto il refresh?

_[immagine]_**  
Alessia Traverso** 50:57  
Sì, questo l'ho già fatto, il refresh.

_[immagine]_**  
Fabio Massone** 50:57  
Della repetitive l'ha già fatto il reference.

_[immagine]_**  
Juela Ndoka** 50:59  
Non mi sa che è un refresh finto questo perché non c'è quella la sessione di UMC che ti.

_[immagine]_**  
Alessia Traverso** 51:02  
Sì.  
Si.

_[immagine]_**  
Juela Ndoka** 51:08  
Che ti mantiene la sessione 8 ore non l'abbiamo ancora applicato, quindi.

_[immagine]_**  
Alessia Traverso** 51:13  
Se poi avessi bisogno di.

_[immagine]_**  
Juela Ndoka** 51:17  
Direi che era finta.  
Franco secondo.  
OK, ora pulisci, pulisci ETW, rifacciamo la chiamata.

_[immagine]_**  
Fabio Massone** 51:35  
E fare anche resi un po quando.

_[immagine]_**  
Alessia Traverso** 51:57  
Domande.

_[immagine]_**  
Juela Ndoka** 51:58  
Scusa, ma tutte le chiamate vanno, cioè falliscono, giusto per non fare il call vuoti, fai l'altro, fai qui.

_[immagine]_**  
Alessia Traverso** 52:02  
Sì.

_[immagine]_**  
Juela Ndoka** 52:09  
Non facciamo questo step sbagliato, fai return empty o con alveolari.  
Flavio Flavio.

_[immagine]_**  
Alessia Traverso** 52:20  
Non possiamo, cioè, l'insegnamento aspetteranno.

_[immagine]_**  
Juela Ndoka** 52:28  
Time.  
Fashion.  
Vai solo l'ultimo.

_[immagine]_**  
Alessia Traverso** 52:38  
Per.

_[immagine]_**  
Juela Ndoka** 52:40  
Flavio.

_[immagine]_**  
Alessia Traverso** 52:44  
Massimo.  
Sì.

_[immagine]_**  
Juela Ndoka** 52:47  
Cosa può avere quello? Facciamo un filter call? Non lo so. No AGV fai message togli la per ora perché non è andata in errore.

_[immagine]_**  
Alessia Traverso** 52:56  
Ma perché non ci pensi?  
A sapere.

_[immagine]_**  
Juela Ndoka** 53:08  
Aggiungo, OK, perfetto, vai, fai OK.  
Ok.  
Allora questa tabella cosa fa?

_[immagine]_**  
Alessia Traverso** 53:28  
Allora?  
E poi fa un'isola in MES.

_[immagine]_**  
Fabio Massone** 53:39  
Ci sono due tabelle, una e l'altra la status, che vengono popolate quando vengono fatte le chiamate, quindi immagino che sia.

_[immagine]_**  
Alessia Traverso** 53:49  
Quindi eventualmente potrebbe essere lui se non fosse preso dalle attività.

_[immagine]_**  
Fabio Massone** 53:50  
Ma quelli di una delle due, a meno che non sia sulla response quando ritrova le informazioni.

_[immagine]_**  
Juela Ndoka** 53:50  
OK.  
No, questa l'ha chiamata Mendix, non è ancora arrivato niente per ora.

_[immagine]_**  
Alessia Traverso** 53:58  
Potrebbe essere lì e potrebbe essere lì.

_[immagine]_**  
Fabio Massone** 54:05  
Ok.

_[immagine]_**  
Juela Ndoka** 54:12  
Vai su sopra ancora vedo uno status code 200 vai.

_[immagine]_**  
Alessia Traverso** 54:12  
Pizzotto.

_[immagine]_**  
Juela Ndoka** 54:21  
Ancora uno.

_[immagine]_**  
Alessia Traverso** 54:21  
E no.

_[immagine]_**  
Juela Ndoka** 54:23  
O no, salta a Sand.  
Da andato con la tua giusta.

_[immagine]_**  
Alessia Traverso** 54:26  
Questo qua l'hanno usato.  
Se questa qua è quella che teoricamente loro mandano a me verso un connect mom, cioè questa qua mi chiamano.  
Quindi vuol dire che siamo entrati dentro a.  
A questa.

_[immagine]_**  
Juela Ndoka** 54:47  
Quindi loro te l'hanno già mandato la risposta.

_[immagine]_**  
Alessia Traverso** 54:47  
Ti sembra?  
Sì, dovrebbero avermela già mandata.  
Quindi se io vado su connectmon.

_[immagine]_**  
Juela Ndoka** 54:58  
Live.

_[immagine]_**  
Alessia Traverso** 55:09  
Vedi, questa qua è quella che abbiamo fatto noi 1301 che ci potrebbe stare. Sì, mi sembra un po.  
Sì.

_[immagine]_**  
Juela Ndoka** 55:20  
OK, questo.

_[immagine]_**  
Alessia Traverso** 55:21  
Questo è quello che le abbiamo mandato noi.

_[immagine]_**  
Juela Ndoka** 55:24  
Aspetta, vediamo il.  
Questo è quello che abbiamo mandato noi abbiamo mandato la box per il Plan 01 1 che è curno per quel buffer per quella Bay e il tipo della chiamata è 0 3 return empty OK giusto OK, questa è la nostra chiamata ed è andata a buon fine. Poi dopo cosa arriva?

_[immagine]_**  
Alessia Traverso** 55:41  
Esatto, esatto.  
Teoricamente ti dovrebbe tracciare questa che è la reply material reply movement che è la risposta che ci viene data da in da CPI diciamo che però ci rispondono in questo modo nel frattempo.

_[immagine]_**  
Juela Ndoka** 56:02  
OK.

_[immagine]_**  
Alessia Traverso** 56:05  
Tempo ci arriva la CK material call dove loro ci mandano le informazioni relativamente al l'i D che abbiamo mandato.  
Il tipo e lo stato del della chiamata, nel senso se è andato a buon fine, se non è andato a buon fine o meno.

_[immagine]_**  
Juela Ndoka** 56:24  
OK.  
Quindi è arrivato stato zero, che vuol dire creato?

_[immagine]_**  
Alessia Traverso** 56:31  
Sì, teoricamente dovrebbe averlo creato in questo momento qua, se io teoricamente vado di nuovo sul Foundation.  
E vado qua cacchiarola, però questo qua mi dovrebbe cambiare.

_[immagine]_**  
Juela Ndoka** 56:47  
Cosa deve diventare?

_[immagine]_**  
Alessia Traverso** 56:48  
Dovrebbe diventare verde.

_[immagine]_**  
Juela Ndoka** 56:51  
No verde, perché l'abbiamo creato, ma in noi non abbiamo ricevuto un qualcosa che.

_[immagine]_**  
Alessia Traverso** 56:58  
Non è questa qua la ricezione you scusami.

_[immagine]_**  
Juela Ndoka** 57:05  
No, abbiamo detto status zero, Stato zero, cosa vuol dire?

_[immagine]_**  
Alessia Traverso** 57:07  
Santi.  
Quello che ti avevo mandato l'altra volta via mail.

_[immagine]_**  
Juela Ndoka** 57:14  
Aspetta, lo apro subito, cioè stai lì, lo apro io.

_[immagine]_**  
Alessia Traverso** 57:19  
Sì.  
Ha creato teoricamente.

_[immagine]_**  
Juela Ndoka** 57:29  
È creato ed zero e work instruction work task, come lo chiamano loro nella loro lingua CPI, è creato.

_[immagine]_**  
Alessia Traverso** 57:41  
E poi loro ci devono rispondere.

_[immagine]_**  
Juela Ndoka** 57:43  
OK, noi abbiamo semplicemente creato la cosa.  
Noi l'abbiamo creato il task, quindi loro ci devono risolvere il task o lo rifiutano.  
O lo accettano, se lo rifiutano diventa rosso, se, cioè se.

_[immagine]_**  
Alessia Traverso** 58:04  
Funzioni.

_[immagine]_**  
Juela Ndoka** 58:06  
E nel senso, se ci arriva un due vuol dire che work task è cancellato, quindi l'hanno rifiutato, se lo confermano diventa, cioè arriva uno e dovrebbe essere il colore dovrebbe essere.

_[immagine]_**  
Alessia Traverso** 58:09  
Sì.  
Uno.

_[immagine]_**  
Juela Ndoka** 58:24  
Roma \*\*\*\*\*.

_[immagine]_**  
Alessia Traverso** 58:25  
OK.

_[immagine]_**  
Juela Ndoka** 58:26  
Ora vado a trovarti lato mendix, i colori però son, cioè la logica è quella.  
Cosa c'è che non torna, dove è il nostro problema?

_[immagine]_**  
Alessia Traverso** 58:41  
Il nostro problema è che Francesca ci ha detto che noi ACPI rispondiamo in questo modo, qua aspetta che te lo condivido.

_[immagine]_**  
Juela Ndoka** 58:51  
Mhm.

_[immagine]_**  
Alessia Traverso** 58:53  
Questo.  
Quando io vado a fare questa chiamata qua mi restituisce questo comando qua.

_[immagine]_**  
Juela Ndoka** 59:00  
Aspetta.  
Aspetta, sto leggendo.  
Però questo sull'acknowledgement sulla material call.

_[immagine]_**  
Alessia Traverso** 59:22  
ACK material call e response, perché è quella che noi utilizziamo, perché noi può qui dentro teoricamente.  
Però qua la chica mi tira il collo.  
E difatti qua ci sono i vari.  
IT confermate, IT created, che sono quelli che abbiamo noi sulla.

_[immagine]_**  
Fabio Massone** 59:59  
Però aspetta, guarda CKGV Movement, perché in teoria tu chiami quella.

_[immagine]_**  
Alessia Traverso** 1:00:02  
Sì.  
Però no.  
Perché io nel Type ti passo molto, però il Type è questa. Sì, ho capito ragazzi.

_[immagine]_**  
Fabio Massone** 1:00:10  
No, cavolo, se no cosa ci andiamo a fare ACKGV moment se non lo usiamo?

_[immagine]_**  
Alberto Grillo** 1:00:14  
No, esatto, dovresti dare quello tu.

_[immagine]_**  
Juela Ndoka** 1:00:15  
Aspetta, aspetta, aspetta, AGV movement. Noi stiamo facendo una richiesta, OK? Stiamo chiedendo quel materiale in quella baia, OK, l'abbiamo creato la, cioè la nostra richiesta è andato a buon fine, è arrivato lo Stato che è stato creato.  
OK, questo è la prima chiamata, OK, da loro ci deve arrivare, sì.

_[immagine]_**  
Fabio Massone** 1:00:40  
In realtà, scusa, in realtà la reply a JV Movement mi sembra che desse errore.

_[immagine]_**  
Juela Ndoka** 1:00:50  
Allora la.

_[immagine]_**  
Alessia Traverso** 1:00:52  
La reply non dipende da noi, mandiamo una richiesta verso di loro e se riusciamo a raggiungerli bene, altrimenti ci dà un errore.

_[immagine]_**  
Fabio Massone** 1:01:03  
Sì, ma signori, cioè io da come la sapevo deve arrivare prima la reply e poi la CK, cioè non capisco perché arriva prima la CK della reply, cioè lì.

_[immagine]_**  
Juela Ndoka** 1:01:04  
Sono due chiamate diverse, sono.

_[immagine]_**  
Alessia Traverso** 1:01:07  
Ciao.

_[immagine]_**  
Alberto Grillo** 1:01:09  
Si.

_[immagine]_**  
Alessia Traverso** 1:01:11  
Perché secondo me fa un polling e ci prova un paio di volte nel mentre se loro hanno un job all'interno ti rispondono subito.  
Se noi rimaniamo in attesa.

_[immagine]_**  
Fabio Massone** 1:01:20  
E non mi sembrava che dovesse riprovare dopo un po, non dopo un secondo.

_[immagine]_**  
Alessia Traverso** 1:01:24  
No, quella lì no, è la è un'altra, non è quella il workflow, quello lì che mi stai dicendo te che aspetta un minuto o un'altra.

_[immagine]_**  
Juela Ndoka** 1:01:32  
Allora va bene, cioè ora non andiamo a capire II loro, cioè le loro logiche. Io sto dicendo che l'a GV Movement è un'altra chiamata e questo in cui noi stiamo fallendo è un'altra chiamata. Noi abbiamo fatto la.

_[immagine]_**  
Alessia Traverso** 1:01:40  
Di verticale.

_[immagine]_**  
Juela Ndoka** 1:01:48  
La richiesta l'abbiamo richiesto, va bene, magari cioè può essere andato in errore anche quella, però questo è un'altra chiamata, è l'acknowledgement material call che vuol dire che loro hanno, cioè io sto accettando quello che mi hai chiesto o meno.

_[immagine]_**  
Alessia Traverso** 1:01:49  
Buongiorno.

_[immagine]_**  
Juela Ndoka** 1:02:06  
OK.  
Prima chiamata è andata la noi non l'abbiamo chiesto e loro hanno creato il task. Sì, Dimmi Alessia.

_[immagine]_**  
Alessio Monaco** 1:02:20  
No, la domanda è questo, in questo, in questo giro che state presentando? No, io ho capito che è partita la richiesta, poi è andata. La nostra richiesta è andata bene. Dall'altra parte sembra esserci un problema che ti è arrivato prima, un messaggio rispetto a un'altro.  
Cioè invece di avere subito la reply ti ha dato prima l'acknowledgement e poi la reply, ma questo perché è un problema nostro?

_[immagine]_**  
Juela Ndoka** 1:02:45  
No, io l'ordine di quello non lo sto, cioè non lo sto analizzando perché non è, cioè non diciamo non è il mio forte. Io sto cercando di capire, cioè di dividere le chiamate e capire perché.  
Che la sua, cioè questa la material call fallisce su di noi, cioè non so io perché arriva molto dopo quello credo che sia qualche configurazione sulle sulla che io non so, cioè non.

_[immagine]_**  
Alessio Monaco** 1:03:05  
Ma questa però sul.

_[immagine]_**  
Juela Ndoka** 1:03:15  
No mi permetto di.

_[immagine]_**  
Alessio Monaco** 1:03:15  
Ma noi sul no? La domanda è, visto che noi siamo partiti dal fatto che non cambiava il colore il semaforo che rimaneva grigio? No, nella dalla dall'interfaccia noi quel semaforo per diventare solo il colore giallo, rosso, blu quello doveva diventare.

_[immagine]_**  
Juela Ndoka** 1:03:25  
Sì.  
Sì.

_[immagine]_**  
Alessio Monaco** 1:03:32  
Ci aspettavamo di ricevere dall'altra parte un messaggio con un codice status.

_[immagine]_**  
Juela Ndoka** 1:03:36  
Questa risposta qui che è andata in errore, OK, a noi è rimasto grigio perché noi abbiamo creato il tasto, quindi noi abbiamo quello Stato zero che vuol dire che l'ho creato.

_[immagine]_**  
Alessio Monaco** 1:03:47  
OK.

_[immagine]_**  
Juela Ndoka** 1:03:49  
La risposta loro è questo material call che poi ci mette quel Stato in 1 2, cioè che vuol dire o l'ho confermato o lo o te lo rifiuto o te l'ho cancellato però noi.

_[immagine]_**  
Alessio Monaco** 1:04:01  
OK, questo che sta questo che sta scerando di questa Francesca Moriero, no, questo qua è il messaggio che ci dà problemi.

_[immagine]_**  
Juela Ndoka** 1:04:05  
Sì.  
Sì che è andato in errore, esatto che è andato in errore qui e quindi noi non riusciamo ad aggiornare lo Stato.

_[immagine]_**  
Alessio Monaco** 1:04:09  
OK.

_[immagine]_**  
Juela Ndoka** 1:04:16  
Cioè io capisco quello dal dalle logiche che ho qua davanti, sia lato mendic sia quello che abbiamo visto lì.

_[immagine]_**  
Alessio Monaco** 1:04:27  
Questo messaggio è presente nella nel log che vedevamo prima, il Connect Mom.

_[immagine]_**  
Juela Ndoka** 1:04:33  
No, ora andiamo a cercarlo, prendiamo quel ACK material col proprio vediamo.

_[immagine]_**  
Alessia Traverso** 1:04:39  
Ce l'abbiamo io.

_[immagine]_**  
Juela Ndoka** 1:04:40  
Non c'è, non lo trovi, no, non lo troviamo.

_[immagine]_**  
Alessia Traverso** 1:04:42  
No, perché vedi che io qua.  
In e no, perché è una cosa che forse sì.  
Però quindi qua devo fare.

_[immagine]_**  
Juela Ndoka** 1:05:05  
Esatto, message mette magari esatto ACK vediamo un po più generico.  
Cosa dice?  
Partiamo dall'ultimo, un secondo vai.

_[immagine]_**  
Alessia Traverso** 1:05:19  
Acer tengo a casa in ti.

_[immagine]_**  
Juela Ndoka** 1:05:23  
Non sto facendo dov'è lo vedi tutti questi ACK io non li vedo perché backup aggiungi anche ACKM perché backup c'ha.  
A check up per back metti anche a me.

_[immagine]_**  
Alessia Traverso** 1:05:37  
E nessuno.

_[immagine]_**  
Juela Ndoka** 1:05:40  
Niente, niente è material cool, semplicemente senza CK.

_[immagine]_**  
Alessia Traverso** 1:05:44  
Se si abilita il back order ci deve essere.  
No, perché se.

_[immagine]_**  
Juela Ndoka** 1:06:01  
Un update buffer material cool scorre sopra.

_[immagine]_**  
Alessia Traverso** 1:06:06  
E l'altra volta aprite buffer, Update buffer, aprite, aprite.

_[immagine]_**  
Juela Ndoka** 1:06:14  
La vai ancora.  
Ma.

_[immagine]_**  
Alessia Traverso** 1:06:22  
Basta, però allora potrebbe essere un problema lato.

_[immagine]_**  
Juela Ndoka** 1:06:26  
Allora mettiamo, aspetta, aspetta, aspetta, andiamo di nuovo in ETWE, mettiamo verbo su quel provider che ha scritto quello e rifacciamo la chiamata. Cos'è quello? Espondi un po' provider name, la terza colonna.  
Col Engine debug, che cos'è business logic execution Engine ora fermiamolo e cambiamo i provider, mettiamo su quell execution Engine mettiamolo a verboso.

_[immagine]_**  
Alessia Traverso** 1:07:01  
Comunque ti confermo che quando devi fare il Grillo, se si è abilitata.

_[immagine]_**  
Juela Ndoka** 1:07:02  
OK.  
E fai anche lo uno verboso.

_[immagine]_**  
Alessia Traverso** 1:07:22  
OK.

_[immagine]_**  
Juela Ndoka** 1:07:33  
Pulisci un poco i e rifacciamo la chiamata.

_[immagine]_**  
Alessia Traverso** 1:07:33  
Quindi cancello.  
Quindi ora devo fare il barbatrucco di prima dovrebbe essere come ti ho detto.

_[immagine]_**  
Juela Ndoka** 1:07:55  
Perché in realtà, cioè il grigio è task creato e poi quando, cioè perché deve switchare subito, cioè creo, accetto o rifiuto, ma è rimasto in un waiting.

_[immagine]_**  
Alessia Traverso** 1:08:01  
Stiamo dicendo che.

_[immagine]_**  
Juela Ndoka** 1:08:10  
Quindi c'è quando rimane in waiting acknowledgement, Ale, scusa, ti puoi mutare, ti prego?  
OK, allora perché? Cioè deve diventare subito grigio e poi cambiare in quello che ti risponde, però in questo momento la nostra risposta è andato in errore, è rimasto in waiting acknowledgement e quindi è sempre grigio.  
Doli.

_[immagine]_**  
Alessia Traverso** 1:08:44  
Però il problema sembra che non arrivi lì, sembra che non so come faccio ad entrare, non ci arriva dentro.

_[immagine]_**  
Juela Ndoka** 1:08:52  
Aspetta stoppalo e fai show all perché abbiamo quel material call come filtro o pausalo come vuoi.

_[immagine]_**  
Alessia Traverso** 1:08:52  
Perché se no io qua dovrei.

_[immagine]_**  
Juela Ndoka** 1:09:00  
Fai show all un secondo e vediamo tutto questo quello è mendix, questo che cos'è?  
Scusa, come si chiama il tuo comando lato backend, quello che mostravi prima lo.  
BRMCNM scrivi solo BRMCNM un secondo comunque scrivi su log uno credo sì trace log uno.  
Mettilo lì nel filtro.  
Le massage.  
OK, abbiamo alcune cosette qui.  
Partiamo da dall'alto, dall'inizio a capire cosa sta facendo. OK, questo è.  
Waiting for response.  
SC.  
Hai questo Communication, vai?  
Ancora.  
Che tutta questa comunicazione vorrei vedere un logo uno però non lo sto vedendo, l'abbiamo messo il logo uno verboso giusto o sbaglio?

_[immagine]_**  
Alessia Traverso** 1:10:38  
Sì, direi di sì, aspetta.

_[immagine]_**  
Juela Ndoka** 1:10:43  
E lo devi sto parte.

_[immagine]_**  
Alessia Traverso** 1:10:44  
Sì, comunque, comunque sì, comunque sì, l'ho messo.

_[immagine]_**  
Juela Ndoka** 1:10:47  
OKOK non lo vedo, cioè non mi sembra scritto qualcosa lì solo uno.

_[immagine]_**  
Alessio Monaco** 1:10:58  
Ma si può filtrare per dire la richiesta di partenza e magari lo becchiamo.

_[immagine]_**  
Juela Ndoka** 1:11:03  
Sì però cioè non so se è quella vai sul sulla chiamata del comando START Process Command un secondo non proprio lì dal messaggio prendi correlation ID se c'è qualcosa lì.  
La riga.  
La terza guarda un secondo la terza.  
Per lo lee.  
Prendi quel request ID guarda un secondo, se c'è un correlation ID scorri a tutto a destra, dovrebbe avere un correlation ID da qualche parte non ce l'ha vuoto.  
Prova con quello, altrimenti prendiamo quella F che sembra sia quello per tutti, ma.  
Flavio.  
O sea, solo questa.  
Sand Command dice con quali parametri, però questa è la richiesta o la no è la response, però la response niente, non lo chiamo niente di niente.

_[immagine]_**  
Alessia Traverso** 1:12:05  
Sì.

_[immagine]_**  
Juela Ndoka** 1:12:25  
La volar non vede niente.  
Fai.  
Disabilita messaggio.  
Traceability.  
Che cos'è questo original batch?  
Sto.  
Es Copiando.

_[immagine]_**  
Alessia Traverso** 1:12:51  
Sì, si vede che ci stanno, si vede che ci stanno mandando anche delle altre cose.

_[immagine]_**  
Juela Ndoka** 1:12:55  
No, stanno cercando di consumare o di fare cose, credo, perché vedo original batch.

_[immagine]_**  
Alessia Traverso** 1:12:58  
OK.

_[immagine]_**  
Fabio Massone** 1:13:13  
Anche se il fatto che non sia proprio inserita nel comando è un po rutta come cosa.  
\*\*\*\*\*, lo manca al figlio, vabbè.

_[immagine]_**  
Juela Ndoka** 1:13:23  
E però ormai stanno facendo ordine di test. Allora o intendi questo non lo so, questo mettiamo un'altro ancora, un'altro provider Ale, mettiamo anche.

_[immagine]_**  
Alessia Traverso** 1:13:35  
Vedi che comunque qua la reply che mi dicevi fallisce perché lui fa un fa diversi tentativi finché in poi non muore.  
Service on available.

_[immagine]_**  
Juela Ndoka** 1:13:50  
Sì, ma questa è la è la risposta per AGI Movement, OK, non della C.

_[immagine]_**  
Alessia Traverso** 1:13:50  
Quindi della reply esatto no questa qua la no questa qua aspetta che vediamo se becchiamo.  
Allora questa qua però lui mi dice 503 service available.  
Vedi, noi proviamo a chiamare questo però vedi che ci mette Brembo 0 1 perché non fa più questo qua il problema.  
Questo qua è il problema, \*\*\*\*\*.  
Che lui qua mi mette BREMBO 0 1.

_[immagine]_**  
Juela Ndoka** 1:14:29  
Ma perché l'abbiamo configurato così?

_[immagine]_**  
Alessia Traverso** 1:14:33  
Io ho provato a vederlo.

_[immagine]_**  
Juela Ndoka** 1:14:36  
Perché questo è il nome del plan, dovrebbe essere Curno.

_[immagine]_**  
Alessia Traverso** 1:14:39  
Sì, ci dovrebbe essere curna slash application.

_[immagine]_**  
Alberto Grillo** 1:14:42  
È come se ci fosse schiantato il nome della macchina, uno di te.

_[immagine]_**  
Juela Ndoka** 1:14:44  
Guardiamo un po come lo fate questo material call response. Che cos'è? È un messaggio, è un Channel, cos'è insegnaci un po' di configurazione. Siamo tutti pronti.  
Okay.

_[immagine]_**  
Alessia Traverso** 1:15:12  
Allora qua negli attributi noi teoricamente dovremmo, cioè ci arriva la CK material call e noi ci dovrebbe arrivare questo.

_[immagine]_**  
Juela Ndoka** 1:15:13  
Tu sappiamo qual.  
Aspetta.  
Rimbo.

_[immagine]_**  
Fabio Massone** 1:15:22  
Prendo 0 1 c'è in fondo vedo.

_[immagine]_**  
Juela Ndoka** 1:15:25  
Cioè l'ho visto, l'hai visto? Aspetta Franco Gatti, però però è che c'è Brembo, scusami.

_[immagine]_**  
Fabio Massone** 1:15:27  
Sì, ed ecco.

_[immagine]_**  
Alessia Traverso** 1:15:33  
È per fare i test, è per fare i.

_[immagine]_**  
Juela Ndoka** 1:15:33  
Non so, non è non sono le liste dei plant, quella.

_[immagine]_**  
Alessia Traverso** 1:15:37  
Sì, ma per fare i test se no tutte le volte ci incasinavamo allora noi ci ricordiamo di mettere 779 che si riferisce a 0 1 a parte che qua ci sono 2779 che prendono che puntano sul BREMBO 0 3 però teoricamente.

_[immagine]_**  
Juela Ndoka** 1:15:54  
Però quel quel 777 Brembo, che cos'è?

_[immagine]_**  
Alessia Traverso** 1:15:54  
Noi qua abbiamo configurato.  
Perché in base al Plant, quindi al VO Number.  
Lui fa un enumeration e dice bene, OK, il 32 11 è di ostrava, il 44 14 di gava, il 4424 di San Coghe o come si dice e poi vedi che c'è lo 0111 che è Curno, lo 02 1 che è Maffei.  
Quindi, in base a quello che ci viene scritto all'interno del V number, noi sappiamo su quale.  
Plant, dobbiamo andare quindi nella chiamata.

_[immagine]_**  
Juela Ndoka** 1:16:35  
OK, però sembra che lui sta vedendo il 7779 sempre.

_[immagine]_**  
Alessia Traverso** 1:16:40  
Esatto che però quello lì è sbagliato, ora devo un attimino capire una cosa.

_[immagine]_**  
Juela Ndoka** 1:16:45  
Non è che è schiantato sulla response?

_[immagine]_**  
Alessia Traverso** 1:16:49  
Allora sulla response, teoricamente questi attributi non ce li abbiamo, perché gli attributi ce l'abbiamo sulla CK material call.

_[immagine]_**  
Juela Ndoka** 1:16:54  
OK.  
OK, perfetto.

_[immagine]_**  
Alessia Traverso** 1:17:00  
Però.  
Ahmad.

_[immagine]_**  
Juela Ndoka** 1:17:05  
Ras Ras Command e altri attributi non sono nostri, non li tocchiamo, non è che abbiamo le.

_[immagine]_**  
Alessia Traverso** 1:17:11  
Vedi l'unico che l'unico che ha la reply AGV movement che ce l'ha schiantato home Brembo 0 1 è questa qua.

_[immagine]_**  
Juela Ndoka** 1:17:19  
Ma perché quello ce l'ha schiantato?

_[immagine]_**  
Alessia Traverso** 1:17:22  
Allora quello lì io mi ricordo infatti che poi questa qua l'ha chiamata.

_[immagine]_**  
Juela Ndoka** 1:17:26  
Sì, è quello il comando che ce l'ha.

_[immagine]_**  
Alessia Traverso** 1:17:30  
Perché il problema è proprio questo qua, nel senso che CPI.  
Quando ci risponde non ci mette.  
Il plante.  
E quindi noi a quel punto non conosciamo. Io questo qua avevo fatto delle prove in locale e quindi mi ero mi ero schiantata la stringa in attesa che loro ci mandassero la risposta.

_[immagine]_**  
Juela Ndoka** 1:17:58  
Però perché abbiamo mandato questo? Perché non mandiamo Curno se noi siamo sicuri che per ora GV va solo sul Curno sulle linee di machining?

_[immagine]_**  
Alessia Traverso** 1:18:04  
Allora io, io questo lo posso fare.

_[immagine]_**  
Juela Ndoka** 1:18:13  
Perché lasciare una macchina di devli, cioè lascerei più il plan, però comunque questo perché non l'abbiamo diciamo scalato questa cosa?

_[immagine]_**  
Alessia Traverso** 1:18:15  
Sì.  
Mucho, grazie.  
Sì.  
Perché noi avevamo aperto ogni arrivo chiesto a qualche ragazzo di.  
Di Siemens se ci potevano aiutare in base a come loro ci rispondevano a recuperarlo, perché comunque un minimum Connect Mom ti riesce a mettere qualche informazione tipo il call ID è una risposta che ci riescono a dare, però mi avevano detto che non sapevano come recuperare diciamo.  
Perché noi inizialmente questi qua glieli glieli mandiamo al Plant, noi glielo mandiamo a loro, sono loro che ci rispondono senza mandarcelo e quindi avevamo chiesto se c'era la possibilità di capire da quale Plant veniva mandato a recuperarlo dalla nostra chiamata.

_[immagine]_**  
Juela Ndoka** 1:19:06  
Ma c'era anche Jacopo Jacopo in questi call, perché cioè loro, cioè è così difficile per loro mandarcelo, quindi dobbiamo fare noi questo tutto sto sforzo.

_[immagine]_**  
Alessia Traverso** 1:19:17  
Credo di sì, ora io non mi ricordo perché poi.

_[immagine]_**  
Fabio Massone** 1:19:19  
Ovvio.

_[immagine]_**  
Alessia Traverso** 1:19:22  
Credo di sì, nel senso che.  
Perché loro ci mandano tipo l'abbiamo accettata e non l'abbiamo accettata una cosa del genere. Anche perché noi sì, noi lo mandiamo nel plante, perché se io vado a vedere qua, allora la.

_[immagine]_**  
Juela Ndoka** 1:19:27  
Cara.  
No, però allora se è così per risolvere questa situazione in questo momento sappiamo che AGV lo facciamo solo su Curno, quindi mettiamo Curno più mi sembra più sensato.

_[immagine]_**  
Alessia Traverso** 1:19:52  
Sì, va bene, OK, allora io dammi solo un secondo che devo riavviare i servizi.

_[immagine]_**  
Juela Ndoka** 1:19:57  
No, non so se questo poi altre cose nascoste su questo io questa, cioè aiutami a capirlo tu perché non lo so, ma cioè secondo me.

_[immagine]_**  
Fabio Massone** 1:20:05  
E.

_[immagine]_**  
Juela Ndoka** 1:20:10  
Ha più senso così?

_[immagine]_**  
Alessia Traverso** 1:20:11  
Sì, io lo metterei così facciamo un attimino il tasto, tanto vediamo se funziona.

_[immagine]_**  
Fabio Massone** 1:20:14  
Scusa una cosa, c'era un Brembo 0 1 senza lo slash ci vorrà mica uno slash prima di application o dopo curl?  
OK, stavi mettendo già.  
Va bene, allora sì, se per me ci vuole.

_[immagine]_**  
Alessia Traverso** 1:20:32  
OK, faccio un attimino il riavvio di servizi.

_[immagine]_**  
Fabio Massone** 1:20:36  
Comunque la risposta a quella tua domanda è abbastanza ovvia, nel senso che è chiaro che quelli lì cercano di fare il meno possibile e noi diciamo che sia tutto, basta vedere la come mandano il dato dell'original batch che ci mandano concatenato.

_[immagine]_**  
Juela Ndoka** 1:20:36  
OK.  
Bene questo solo perché abbiamo AGV solo su un plan e lo sappiamo se è Curno, però se in qualche maniera su un'altro plan, questo bisogna essere specificato. Come facciamo a gestire le chiamate? Fra diranno tutte.

_[immagine]_**  
Fabio Massone** 1:20:54  
Materiale vecchio.  
E non può che.  
Sì, ma hai ragionissima?  
Per l'unisso son 2 Ko.  
Però basta vedere quel comando dell'Original batch con cui ci popolano la tabella delle relazioni che mandano con lo spazio in mezzo, il materiale, il batch quando avremo i campi separati.

_[immagine]_**  
Juela Ndoka** 1:21:14  
Sì.  
Sì.  
Ma basta vedere che ci mandano un CLF massivo per aggiornare un materiale ci mandano 600 materiali, cioè 600 sto esagerando però più di uno.

_[immagine]_**  
Fabio Massone** 1:21:28  
Buonasera.  
Sì.

_[immagine]_**  
Juela Ndoka** 1:21:33  
Sì, Alessio.

_[immagine]_**  
Fabio Massone** 1:21:35  
Scandaloso.

_[immagine]_**  
Alessio Monaco** 1:21:36  
No, una domanda, ma visto?

_[immagine]_**  
Juela Ndoka** 1:21:38  
Puoi intervenire subito perché cioè io non guardo lo schermo a volte, quindi può essere che se li appena.

_[immagine]_**  
Alessio Monaco** 1:21:43  
No, va beh, io non vi voglio interrompere mentre parlo di cose che sapete più di me. Ma una domanda, ma il protocollo di scambio di messaggi tra noi e tutte queste altre entità no, non è un qualcosa di definito, cioè nel senso indicare un plant non è un qualcosa di.

_[immagine]_**  
Juela Ndoka** 1:21:54  
Sì.

_[immagine]_**  
Alessio Monaco** 1:22:00  
Cioè basico in un protocollo di scambio messaggi.

_[immagine]_**  
Juela Ndoka** 1:22:04  
Dovrebbe, però non so e non te lo so dire. Cioè erano già quando sono entrata io, erano già definiti credo. Cioè io sono entrata a Febbraio e l'ho già trovato.

_[immagine]_**  
Alessio Monaco** 1:22:06  
Ho capito, ma il protocollo chi l'ha fatto?

_[immagine]_**  
Juela Ndoka** 1:22:20  
Così mi aspettavo che ci fosse un plan, un qualcosa che riesce a identificare chi sono e cosa sto facendo, però boh non lo so in questo caso perché abbiamo accettato questo questa risposta al lato loro?  
Non te lo so dire.

_[immagine]_**  
Alessio Monaco** 1:22:41  
Perché se il protocollo non prevede una identificazione, cioè allora il problema deve deve emergere a livello generale, non che ce lo dobbiamo noi in casa e fare i barbatrucchi.

_[immagine]_**  
Juela Ndoka** 1:22:53  
Allora penso che no, penso perché per le altre chiamate sarà per forza il plan, perché come fai a identificare poi? Cioè se io chiedo un materiale, che ne so, io ti sto prendendo un'altro esempio, mi aspetterei che ci fosse.  
Quando arriva una risposta mi dice che te l'ho mandato in questo plant, in questo buffer, perché altrimenti come fai a identificarlo?

_[immagine]_**  
Alessio Monaco** 1:23:15  
Certo, anche perché se cioè non è che qui il MES, anzi tra virgolette, il MES deve deve essere multiplant, no? Da quel dal da quello che sto vedendo.

_[immagine]_**  
Juela Ndoka** 1:23:24  
E abbiamo e stiamo facendo tutto sto sforzo per farlo funzionare così.

_[immagine]_**  
Alessio Monaco** 1:23:28  
Multiplate esattamente. Quindi non è un qualcosa di che è uscito oggi, no? Quindi mi domando, visto che è un requirement de.

_[immagine]_**  
Juela Ndoka** 1:23:33  
No.  
Ma non so l'accordo con CPI perché CPI non può farlo, non può mandare questo attributo. Non so tutto il diciamo l'avanzamento di questo non ho partecipato, quindi non ti so dire.  
Se era troppo difficile per loro OA un certo punto non mi interessa se è troppo difficile per loro, io vorrei vederlo perché se ho più plant che hanno lo stesso la stessa chiamata, cioè mi sembra un po' difficile andare noi lato.  
Connect mode nel senso backend, andare a recuperare dove sono, cosa sta facendo qua, da dove ho fatto partire la questo questa richiesta eccetera eccetera mi sembra un po' troppo, cioè?  
Inutile tutto sto sforzo, boh.  
Però non lo so.  
Perché era deciso così?  
E non so perché l'abbiamo accettato noi.  
Ma c'è, è ancora aperta questa ticket alle.

_[immagine]_**  
Alessia Traverso** 1:24:54  
Espejo, Mateo.  
Mi Damiani.

_[immagine]_**  
Juela Ndoka** 1:25:00  
Sì, ho capito e quindi non ci hanno mai più risposto.

_[immagine]_**  
Alessia Traverso** 1:25:05  
No, perché m'ha detto me lo prendo in carico io. Poi appena riesco a capire come fare ti faccio sapere. Poi magari se n'è dimenticato, cioè sicuramente sì, quello sicuramente sì.

_[immagine]_**  
Juela Ndoka** 1:25:14  
Dario è anche un po complicato, cioè probabilmente se deve fare un giro devi andare a capire la richiesta che hai fatto, da dove l'hai fatto quello che dicevi, cioè per ID per qualche identificativo.

_[immagine]_**  
Alessia Traverso** 1:25:29  
Esatto, esattamente.

_[immagine]_**  
Juela Ndoka** 1:25:34  
Bene, questo è da questo è da analizzare, da scrivere, da analizzare, perché è molto importante, direi.

_[immagine]_**  
Alessia Traverso** 1:25:44  
Però da una parte noi teoricamente.  
Ora non so se si può fare, ma noi ti dà la possibilità di fare anche delle interrogazioni a livello di database. Il sistema però era una cosa che Jacopo non voleva fare.

_[immagine]_**  
Juela Ndoka** 1:25:59  
Tita.  
Esatto perché lo devo fare io? Se tu lo sai cosa mi stai mandando? Cioè scusa, mi stai mandando la richiesta di una cioè la risposta di una richiesta che ti ho fatto e in questa richiesta io ti ho mandato anche questo attributo perché dovresti farmi fare tutta sta fatica invece di tornarmelo?  
Ciao.  
No.

_[immagine]_**  
Alessia Traverso** 1:26:25  
No, assolutamente, assolutamente niente.

_[immagine]_**  
Fabio Massone** 1:26:28  
D'accordissimo.

_[immagine]_**  
Juela Ndoka** 1:26:31  
Grazie, Fabio.

_[immagine]_**  
Fabio Massone** 1:26:34  
No, ma è vero, cioè ci sono troppe cose che non hanno senso e non si capisce perché vengano fatte senza senso lo stesso sempre.  
Questa è una di quelle.

_[immagine]_**  
Annalisa Casciaro** 1:26:46  
C'è una bella canzone di Vasco Rossi, volendo, se la vogliamo mettere in sottofondo.

_[immagine]_**  
Juela Ndoka** 1:26:51  
Quale illuminate me, perché magari io.

_[immagine]_**  
Annalisa Casciaro** 1:26:55  
Un senso non c'è l'ha adesso non mi ricordo il titolo, Se questo però a volte aiuta a non farsi troppe domande.

_[immagine]_**  
Juela Ndoka** 1:26:56  
OK.  
No, lo so, però cioè no, non voglio aggiungere, cioè difficoltà su.

_[immagine]_**  
Annalisa Casciaro** 1:27:06  
No, ma.

_[immagine]_**  
Alessio Monaco** 1:27:08  
Sì.

_[immagine]_**  
Juela Ndoka** 1:27:13  
Su punti che sono già un po difficile e non.  
Molto chiari per tutti noi, per esempio Connect Mom.

_[immagine]_**  
Annalisa Casciaro** 1:27:20  
Sì, saranno decisione decisioni pregresse? No, sicuramente.

_[immagine]_**  
Alessio Monaco** 1:27:26  
No.

_[immagine]_**  
Juela Ndoka** 1:27:26  
Ma ti direi di no perché AGV prima non su Ostrava non esiste neanche su gava non esiste questo tipo di chiamata. No, non c'è questa parte di chiamata, non esiste lì.

_[immagine]_**  
Annalisa Casciaro** 1:27:34  
Non lo sapevo.  
Pensavo si dovesse solo abilitare, invece non esiste proprio, OK?

_[immagine]_**  
Juela Ndoka** 1:27:44  
No, è proprio è un gap che è stato sviluppato per l'Italia, per quello ho detto che non so l'avanzamento e non so quando è stato deciso questo.

_[immagine]_**  
Annalisa Casciaro** 1:27:53  
OKOK, questa è un'informazione utile per noi su JJ.

_[immagine]_**  
Juela Ndoka** 1:27:58  
Sì, non voi non avete questo problema perché credo che lì non c'è questa parte.

_[immagine]_**  
Francesco Panigo** 1:28:03  
E ce la fanno.

_[immagine]_**  
Annalisa Casciaro** 1:28:07  
Ottimo.

_[immagine]_**  
Juela Ndoka** 1:28:07  
Per ora non dovrebbe essere.

_[immagine]_**  
Alessio Monaco** 1:28:12  
Quello mi pure mi fa piacere notare che con i prodotti Siemens serve sempre il calendario vicino al computer.  
Non è cambiato rispetto a 10 anni fa.

_[immagine]_**  
Juela Ndoka** 1:28:24  
E non cambierà neanche nei prossimi 10 anni.  
Mi allontano due minuti.

_[immagine]_**  
Alessio Monaco** 1:34:57  
Non ho mai informazioni, è normale che ci metto questo tempo per risalire.

_[immagine]_**  
Alessia Traverso** 1:35:03  
Sì, ci mette sempre un po di tempo, ci mette meno a spegnersi e riaccendersi, però sì, comunque dovremmo esserci, è l'ultimo server questo.  
Difatti, teoricamente, il non dovrebbe essere mai riavviato.

_[immagine]_**  
Alessio Monaco** 1:35:24  
Mi volevo riavviare da powershell.

_[immagine]_**  
Alessia Traverso** 1:35:28  
Sì, perché devi seguire determinato ordini per stoppare, per riavviare.

_[immagine]_**  
Alessio Monaco** 1:35:28  
Non lo.  
Quindi non lo fai da interfaccia dei dei server, non è che va bene?

_[immagine]_**  
Alessia Traverso** 1:35:41  
OK, allora qua ha finito.  
Quindi ora teoricamente basterebbe rifare la chiamata.  
Che acquisto.  
Sì.  
Pasquale.  
Sì.  
Allora?  
Per.  
Lisa.  
OK, ora teoricamente giusto.  
No, qua sono altre le vediamo di qua.  
Replay, oggi non lo manes.  
Vediamo se sui tre siamo fortunati.  
Eccola qua, fallisce di nuovo.  
Sì.  
Capito, però qua non ce l'ha messa.  
C'ho qualche problema sul workflow?

_[immagine]_**  
Alessio Monaco** 1:39:06  
L'eroe ti dice MPLD.  
Interno severa.

_[immagine]_**  
Juela Ndoka** 1:39:13  
Eccomi, scusa.

_[immagine]_**  
Alessia Traverso** 1:39:13  
No, ma e quale l'errore che può?

_[immagine]_**  
Juela Ndoka** 1:39:16  
Cosa è successo?

_[immagine]_**  
Alessia Traverso** 1:39:18  
E qua se vedete vedi, noi andiamo a chiamare la nostra API esposta. Però qua adesso non mi ci mette. No, cur non ce l'ha messa, quindi è giusta. Non la vedevo, scusatemi.

_[immagine]_**  
Juela Ndoka** 1:39:26  
Sì, con.  
Me tranquilo.

_[immagine]_**  
Alessia Traverso** 1:39:31  
Internal server error mi dà.

_[immagine]_**  
Juela Ndoka** 1:39:36  
Solo questo, non nel messaggio, non abbiamo un qualcosa che ci indica più.

_[immagine]_**  
Alessia Traverso** 1:39:43  
Noi li mandiamo.

_[immagine]_**  
Juela Ndoka** 1:39:43  
Attack.  
E quella cosa lì?

_[immagine]_**  
Alessia Traverso** 1:39:46  
Qua non riesci a trasformare questo Grillo via perché OK.

_[immagine]_**  
Juela Ndoka** 1:39:52  
È MPLID, questo è un po CPI, questo no?

_[immagine]_**  
Alessia Traverso** 1:39:55  
Sì, esattamente CPI questo qua.

_[immagine]_**  
Juela Ndoka** 1:39:58  
OK.

_[immagine]_**  
Alessia Traverso** 1:40:04  
Però secondo me noi da qua loro ci serve la questa qua noi ci serve perché dobbiamo andare a scrivere qualcosa all'interno del nostro database nel modo.  
Tale in cui il call ID che poi ci manda ACK material call, diciamo noi andiamo a recuperarci le informazioni che ci servono.

_[immagine]_**  
Juela Ndoka** 1:40:30  
Esatto, però ora di nuovo è fallito la città per la stessa cosa.

_[immagine]_**  
Alessia Traverso** 1:40:32  
Fallisce? Sì, è fallito. Sì, non funziona perché comunque qua fallisce questo.  
Error code External System D è il nostro call ID e reply l message è la reply movement, quindi se noi andiamo a livello di codici, la reply Magic movement era quello che.  
Avevamo visto nello switch, giusto Fabio?  
Movement, che è quella che teoricamente dovrebbe andare a inserire, vedete che va a fare la history e poi dovrebbe andarla a inserire a livello di.

_[immagine]_**  
Fabio Massone** 1:41:18  
In realtà la ritrova, cioè ritrova la history no, aspetta, sì, ritrova la history per avere delle informazioni in più sì, per poi andare ad aggiornare tutte le tabelle di history e status, perché si deve recuperare alcune informazioni col fatto che loro ci mandano indietro soltanto.

_[immagine]_**  
Alberto Grillo** 1:41:24  
Dovrei fare la H los tetos?

_[immagine]_**  
Fabio Massone** 1:41:35  
Il call ID noi tramite tramite quello che se non ricordo male ce lo salviamo com'è che fa la ricerca su dov'è poco sopra non mi ricordo.

_[immagine]_**  
Juela Ndoka** 1:41:49  
Il plan da dove lo prende, scusa?

_[immagine]_**  
Fabio Massone** 1:41:50  
Tramite il MES vedi External System ID, loro ci rimandano l'i d che gli abbiamo inviato noi.  
Ci ritroviamo il message need dalla out message e poi tramite quello recuperiamo dalla Movement history tutte le AGV movement info riga 279 che poi andiamo ad usare quando dobbiamo scrivere una nuova roba nella history, nella history praticamente andiamo a scrivere.  
Tutte le chiamate che vengono fatte, quindi la nostra chiamata, la loro reply, la loro CK, così abbiamo il timestamp con i valori arrivati per da loro per ogni response e la status che serve invece alla UI per aggiornare i semaforino.  
E l'aggiornamento lo fa.

_[immagine]_**  
Juela Ndoka** 1:42:36  
E lo prendo comunque dalle dalle entità lì. Però scusa, posso aggiungere solo una cosa Fabio, non possiamo creare quelle entità lì output message con quelle external ID per capire cosa abbiamo fatto con quelle external ID scusami.

_[immagine]_**  
Fabio Massone** 1:42:39  
Sì.

_[immagine]_**  
Juela Ndoka** 1:42:50  
Dove sono quelle tabelle, l'output message, quale entità?

_[immagine]_**  
Fabio Massone** 1:42:52  
Automessage è di è di prodotto.

_[immagine]_**  
Juela Ndoka** 1:42:55  
OK, perfetto, lo possiamo guardare un attimo.

_[immagine]_**  
Fabio Massone** 1:42:58  
Sì.  
Ma secondo me il problema non è l'otto lavoro.

_[immagine]_**  
Alberto Grillo** 1:43:01  
E andava visto lato DB, però ti ricordi che l'external sì, l'external non c'è sull'entità.

_[immagine]_**  
Fabio Massone** 1:43:04  
E sul dias, sì, e sul dias, dias cool no sarà dias baby cool.

_[immagine]_**  
Juela Ndoka** 1:43:06  
Sì.

_[immagine]_**  
Fabio Massone** 1:43:17  
E io non ho fatto l'Age Movement, ma funziona in maniera analoga alla material call che ho fatto io, quindi presumo che sia così come dico.  
L'avevamo studiata, l'avevamo fatta analoga apposta, in modo che così, conoscendone una, si potesse conoscere anche l'altra, tanto erano simili.

_[immagine]_**  
Alessia Traverso** 1:43:52  
E questo è giusto Fabio auto message.

_[immagine]_**  
Juela Ndoka** 1:43:55  
Sì, sarà quello.

_[immagine]_**  
Fabio Massone** 1:43:58  
Dai.  
Poi basta un order by.

_[immagine]_**  
Juela Ndoka** 1:44:06  
No, prendiamolo per external, gli dice, l'abbiamo nei log, facciamolo giusto.

_[immagine]_**  
Fabio Massone** 1:44:10  
OKOK, no vabbè per fare un order by create and on desk per vedere giusto cosa mando.  
Se ce l'avete nei log va bene.

_[immagine]_**  
Alessia Traverso** 1:45:08  
Qua è quello che siamo andati a scrivere.

_[immagine]_**  
Juela Ndoka** 1:45:11  
OK, ma c'è un message, c'è un qualcosa in cui scriviamo, cioè vediamo.

_[immagine]_**  
Fabio Massone** 1:45:14  
Message ID message ID è quello che noi usiamo per andare a recuperare il messaggio nelle tabelle di history status, mi sembra da history.

_[immagine]_**  
Juela Ndoka** 1:45:26  
O K.

_[immagine]_**  
Fabio Massone** 1:45:28  
Quello che ci trovavamo fuori.

_[immagine]_**  
Juela Ndoka** 1:45:30  
Possiamo farlo?

_[immagine]_**  
Fabio Massone** 1:45:33  
Sì, Diego.

_[immagine]_**  
Alessia Traverso** 1:45:37  
Scusami Fabio, cos'è che devo fare che ti ho perso?

_[immagine]_**  
Fabio Massone** 1:45:39  
Copiati il campo messaggi di.  
Che è un poco più a sinistra, no, meno.  
No, sì, è quello lì. Scusa. Sì, esatto, è quello lì.  
E adesso devi farla qui sulla GV Movement history, mi sembra.  
Però se vi conviene cercarla.  
C'è ne saranno quattro, la fase tutte le solite.  
Esatto.  
Non so prova need.  
Ovviamente hai due record, il primo la nostra richiesta e il secondo la loro non so se ACKO reply dipende VT not created error message perché adesso poi mettiamo quella roba lì.

_[immagine]_**  
Juela Ndoka** 1:46:56  
Scusa perché? Perché mettiamo VT note creative s'è creato.

_[immagine]_**  
Fabio Massone** 1:46:56  
Bene.  
Non lo so perché è la sono le response che ci mandano loro, io mi ero già la mi ero work task.

_[immagine]_**  
Juela Ndoka** 1:47:06  
Votino created, no, hanno mandato un.

_[immagine]_**  
Alessia Traverso** 1:47:08  
È lo Stato, è lo Stato, è lo Stato. Però in due aspetta che bisogna vedere loro che cosa ci hanno dato.

_[immagine]_**  
Fabio Massone** 1:47:16  
Quella lì, esattamente la quella lì, guarda, te lo dico già, la direction è due, vuol dire che la risposta che ci hanno mandato loro, quindi è secondo me, se non ricordo male è la è la ACK questa.

_[immagine]_**  
Juela Ndoka** 1:47:17  
E ma e non è la zero la prima.  
Ma no, scusa, non è la prima chiamata, questa è la prima richiesta che fai tu e dovrebbe essere creato se ti dice che ho inviato.

_[immagine]_**  
Fabio Massone** 1:47:34  
Che ha prima che arriva, infatti guarda l'orario.

_[immagine]_**  
Juela Ndoka** 1:47:44  
Cioè.

_[immagine]_**  
Fabio Massone** 1:47:44  
No, la prima riga e non ha errore.

_[immagine]_**  
Juela Ndoka** 1:47:46  
No, la prima chiamata parliamo un secondo a livello di concetto, poi facciamolo.

_[immagine]_**  
Fabio Massone** 1:47:50  
No, la prima, la prima aspetta, aspetta. La prima riga è quella che scriviamo noi quando creiamo il record, quindi non c'è nessun errore.  
Poi quando arriva la reply è un'altra riga, quando arriva la CK è un'altra riga lì mette come.  
Ha messo come adesso devo un attimo andare a vedere la direction, se anche sulla reply mettiamo.

_[immagine]_**  
Juela Ndoka** 1:48:20  
Sì, però intendo se arriva e error quello, cioè che se c'è uno Stato SEO che ne so io quello che sta per errore abbiamo cioè.

_[immagine]_**  
Fabio Massone** 1:48:31  
Dario.  
Quella lì loggata, la seconda riga è la ACKJV movement.  
Perché la reply mette come direction MES to IRP che è uno, la CK mette come direzione IRP to MES se andate a vedere quando fa la chiamata vai giù, vai giù, vai giù Direction e IRP to MES.

_[immagine]_**  
Juela Ndoka** 1:48:38  
Ok.

_[immagine]_**  
Fabio Massone** 1:48:55  
Che ha due. Poi una volta che è arrivata la response ha un messaggio, se poi arriva la reply mi sembra che la ignorassimo o facessimo qualcosa del genere.

_[immagine]_**  
Juela Ndoka** 1:49:05  
No, tu hai messo, tu hai messo VT not created perché ti è arrivato, c'è un errore, hai lo Stato e quindi hai scritto VT not created.  
Dimmi che è così, se non è così non ci ho capito nulla di questo.

_[immagine]_**  
Fabio Massone** 1:49:20  
E non so, non me lo ricordo che non l'ho neanche fatto io.

_[immagine]_**  
Juela Ndoka** 1:49:22  
Vai sul DB, vai sul DB Orden, mi puoi ordinare per timestamp così capisco qual è la prima chiamata, quella la seconda per favore.

_[immagine]_**  
Fabio Massone** 1:49:24  
Bisogna andare, bisogna.  
Per il.  
Tutti i not created non mi ricordo neanche che vanno a guardare.

_[immagine]_**  
Juela Ndoka** 1:49:35  
Percheprimanoiabbiamovistochecequell'errorem.pl che cavolo ne so io che vuol dire che è andato in errore che arriva un Stato se che vuol dire che quel Stato se lo mette VT not created?

_[immagine]_**  
Fabio Massone** 1:49:51  
Sì, mi ricordo che c'era qualcosa che se era maggiore di aspetta.

_[immagine]_**  
Alessia Traverso** 1:49:57  
P. 299.  
P 299.

_[immagine]_**  
Fabio Massone** 1:50:02  
Questa seeded era.

_[immagine]_**  
Juela Ndoka** 1:50:02  
Due nomen, no va odio Silvio.

_[immagine]_**  
Alessia Traverso** 1:50:16  
Aspettate che ve lo faccio vedere adesso perché non mi logga, perché?

_[immagine]_**  
Fabio Massone** 1:50:27  
Ciao.

_[immagine]_**  
Alessia Traverso** 1:50:28  
Replay.  
Error status va beh io ti passo forse se è maggiore di 299 però io mi ricordo anche ACK.

_[immagine]_**  
Juela Ndoka** 1:50:45  
Cioè la prima.  
La.

_[immagine]_**  
Alessia Traverso** 1:50:49  
No, Francesco, Dimmi, scusami.

_[immagine]_**  
Juela Ndoka** 1:50:51  
No, non volevo solo capire i record, nient'altro.

_[immagine]_**  
Fabio Massone** 1:50:54  
Io l'avevo impostato con un error message parlante, ma se poi arrivano ste stringhette qua e ci vogliamo scrivere brutti not created.

_[immagine]_**  
Juela Ndoka** 1:51:01  
Ma devono arrivare queste stringhette? No, perché cioè dobbiamo essere allineati che loro, cioè quando hanno abbiamo una leggenda in cui se arriva 01 2 siamo tutti, cioè tutti i sistemi hanno lo stesso e mi aspetto.

_[immagine]_**  
Fabio Massone** 1:51:04  
Non serve a niente.

_[immagine]_**  
Juela Ndoka** 1:51:18  
Cioè mi autoconvinco visto che non ho altra scelta che quello è fallito mi ha dato un status e da Connect mom lì e quindi mi mette VT not created invece sulla la prima chiamata mi hai detto.  
OK, non mettiamo niente perché è la creazione del WTOK perfetto mi piace questo mi piace perfetto.

_[immagine]_**  
Fabio Massone** 1:51:36  
La scriviamo noi? Sì, esatto, esatto, sì, è la creazione lato nostro, diciamo sulla sulla seconda riga lo scriviamo perché dal lato loro ci arriva, ci arriva sì, un qualcosa di sbagliato. Adesso non mi ricordo nel dettaglio come viene indicato.  
Le guardiamo lo.  
Status indicator.  
Quant'è che mandi tre.

_[immagine]_**  
Juela Ndoka** 1:52:07  
Titus indicator stapper.

_[immagine]_**  
Fabio Massone** 1:52:07  
Nicola.

_[immagine]_**  
Alessia Traverso** 1:52:10  
Sì.

_[immagine]_**  
Fabio Massone** 1:52:11  
Riesci a vedere quello che ci mandano loro come risposta da Connect Mom?

_[immagine]_**  
Alessia Traverso** 1:52:12  
Sì.

_[immagine]_**  
Juela Ndoka** 1:52:16  
Mi aspetto un status è a sto punto per giustificare tutto quello che ho detto, status è perfetta, call time zero three status è error che vuol dire would you not created?

_[immagine]_**  
Fabio Massone** 1:52:30  
Col Type 0 3 vabbè, quello lì è status e.  
Devo vedere se è il comando che viene chiamato internamente che fa quella roba lì della RMS.  
D'accordo, proprio non funziona.

_[immagine]_**  
Juela Ndoka** 1:53:09  
Eccolo, è stato questo, aspetta, ora faccio così perché così stiamo tutti allineati su questo.  
Chante.  
OK.

_[immagine]_**  
Fabio Massone** 1:53:37  
Va in realtà per noi a un menum, però sì, può essere.

_[immagine]_**  
Juela Ndoka** 1:53:41  
Sì, OK, la tua codice va bene, però, cioè come traduzione dovrebbe essere questa.

_[immagine]_**  
Fabio Massone** 1:53:47  
OKOK può essere se non ho più le mie, cioè non so che.

_[immagine]_**  
Juela Ndoka** 1:53:51  
Cioè hanno per EVM, è questo la traduzione, direi che anche noi abbiamo applicato la stessa cosa nel nostro mapping.

_[immagine]_**  
Fabio Massone** 1:53:58  
Noi per noi not created vale tre, not VT cancelled due, VT confirmed uno EVT created zero.  
Non e quindi sì, corrisponde, tranne che abbiamo messo tre sul not created, sì.

_[immagine]_**  
Juela Ndoka** 1:54:14  
OK.  
OK, altra tabella che c'è, ma non c'è una tabella in cui io vedo tutto quello che ho mandato in un modo un po più carino tipo message no?

_[immagine]_**  
Fabio Massone** 1:54:31  
Le tabelle, quella tabella più completa che contiene tutto è quella lì.  
Forse lo vedi un po' più lo vedi un po' più bello da tester tool perché ti fa vedere anche tipo la Direction ti si scrive MES to IRP to MES invece qua vedi uno e due devi sapere cosa vuol dire.

_[immagine]_**  
Juela Ndoka** 1:54:38  
Questa qui è.  
No, perché lo intendevo proprio.

_[immagine]_**  
Fabio Massone** 1:54:53  
Anche lo status, gli status, per esempio, uno sta per aspetta che te lo dico.

_[immagine]_**  
Juela Ndoka** 1:54:59  
Ma no, intendevo tipo come payload di quello che abbiamo mandato in questo senso, non cioè come dati per analizzarli non so, magari non li sto spiegando.

_[immagine]_**  
Fabio Massone** 1:55:10  
No viste, roba così.

_[immagine]_**  
Juela Ndoka** 1:55:11  
Per no, perché cioè per capire come hai chiamato il comando, con quali valori hai chiamato il comando.  
Che mandi e questo senso.

_[immagine]_**  
Alessia Traverso** 1:55:23  
Allora questo qua, questo il comando lo riesce a vedere da qua.  
Il comando lo vedete da qua.

_[immagine]_**  
Fabio Massone** 1:55:35  
No, sarà la CK si dalla CK.

_[immagine]_**  
Alessia Traverso** 1:55:39  
Oppure noi qua l'abbiamo visto qui dentro, perché lui prova a trasformare il Jason che ci arriva, ma ci arriva un Jason che lui non riesce AA convertire e quindi si genera l'errore.  
Odetti.

_[immagine]_**  
Juela Ndoka** 1:55:57  
E vabbè, non so come farei una prova live con loro, ti dico la verità con CPI anche.

_[immagine]_**  
Alessia Traverso** 1:56:05  
Sì, dobbiamo, dobbiamo farlo assolutamente con loro. Un problema nostro era sicuramente il fatto che si era schiantato Brembo 0 1 e quindi comunque noi la chiamata verso di noi non la facevamo mai verso le la nostra web APP esposta diciamo.

_[immagine]_**  
Juela Ndoka** 1:56:17  
OK, perfetto, perfetto.

_[immagine]_**  
Alessia Traverso** 1:56:20  
Mettendo a posto quello lì noi abbiamo la UR viene generata correttamente perché io la vado poi a tracciare che ha questa qua ed è questa, vedi il SVC no application questa qua è il nostro comando che esponiamo dove poi andiamo a.  
Fare tutte le varie, tutti i vari ragionamenti e inserimenti.

_[immagine]_**  
Juela Ndoka** 1:56:38  
OK.  
Perché? Cioè se non sbaglio ora vedo un attimo il mio calendario, ma mi sa che io c'ho un c'ho dei seed domani su questo e ora te lo dico subito, aspetta.

_[immagine]_**  
Alessia Traverso** 1:56:51  
È domani o dopodomani?

_[immagine]_**  
Juela Ndoka** 1:56:54  
Scusa, domani è mercoledì?  
No, quelli sono con Toyota, quelli sono con Toyota, ne ho altri, credo con EVME SAP BMW machining OK.

_[immagine]_**  
Alessia Traverso** 1:56:57  
Sì, non.  
OK.  
Ok, quindi sarebbe comunque tutta questa cosa qua, giusto, no?

_[immagine]_**  
Juela Ndoka** 1:57:17  
Direi di sì, direi di sì.

_[immagine]_**  
Alessia Traverso** 1:57:19  
Allora magari io partecipo anch'io, così lo vediamo insieme.

_[immagine]_**  
Juela Ndoka** 1:57:23  
Sì, per la parte del machining possiamo sistemare durante il sì di mercoledì, perché dovremmo inserire dei test case che mancano, chiamata return voti, chiamata vuoti, chiamata speciale. OK, sì, dobbiamo fare questi anche.

_[immagine]_**  
Alessia Traverso** 1:57:42  
Ok.

_[immagine]_**  
Juela Ndoka** 1:57:44  
Va bene.  
Basta, dobbiamo chiedere, cioè lo facciamo domani, però una cosa l'abbiamo sistemato, almeno.

_[immagine]_**  
Alessia Traverso** 1:57:52  
Esatto, esatto, esatto.

_[immagine]_**  
Juela Ndoka** 1:58:02  
Qualcuno vuole, cioè ha qualche domanda o ha bisogno di.  
Di supporto, aiuto su qualcosa.

_[immagine]_**  
Annalisa Casciaro** 1:58:17  
Noi.  
Su DJ.

_[immagine]_**  
Juela Ndoka** 1:58:19  
Ma per consumo sempre.

_[immagine]_**  
Annalisa Casciaro** 1:58:24  
Sto rifacendo i test e non consuma di nuovo.

_[immagine]_**  
Juela Ndoka** 1:58:25  
Cosa è successo?  
Ma anche con la nuova MD a scusami.

_[immagine]_**  
Annalisa Casciaro** 1:58:32  
No, non è quel caso.

_[immagine]_**  
Juela Ndoka** 1:58:35  
C'è un'altro caso?

_[immagine]_**  
Annalisa Casciaro** 1:58:36  
Caso stavolta è questo, te lo faccio vedere.

_[immagine]_**  
Juela Ndoka** 1:58:39  
Sì.

_[immagine]_**  
Annalisa Casciaro** 1:58:41  
Allora con calma che allora io ho creato, state vedendo?

_[immagine]_**  
Juela Ndoka** 1:58:44  
Sì.  
Sì.

_[immagine]_**  
Annalisa Casciaro** 1:58:48  
Ho creato un MTU per questo buffer, OK, poi gli ho messo il prodotto sperando di non aver sbagliato.

_[immagine]_**  
Juela Ndoka** 1:58:56  
Mhm.

_[immagine]_**  
Annalisa Casciaro** 1:59:03  
Il prodotto questo OK.

_[immagine]_**  
Juela Ndoka** 1:59:06  
OK.

_[immagine]_**  
Annalisa Casciaro** 1:59:07  
Quindi ho guardato qui, ho scusate, ho guardato qui.  
Io ho preso questa questo buffer, OK?

_[immagine]_**  
Juela Ndoka** 1:59:17  
OK.

_[immagine]_**  
Annalisa Casciaro** 1:59:19  
Poi cosa ho fatto, l'ho creato e lo vediamo qui sopra.  
Sul material track unit, quindi ho creato un batch, scusami, ho inserito il batch, il container, ci vedi?

_[immagine]_**  
Juela Ndoka** 1:59:32  
Cosa?  
Non lo so, aspettate un secondo. No, sto parlando con altri 5 minuti, 10, anzi fai, non si sa mai. OK, Dimmi.

_[immagine]_**  
Annalisa Casciaro** 1:59:37  
Sì.  
Allora vedi il container, il Batch e l'ordine, quindi questo dovrebbe andare con nonchalance.  
Se io leggo il batch funziona se leggo il container.  
Ma perché vorrei essere i dati, perché ho però aspetta che rientro, che faccio prima?

_[immagine]_**  
Juela Ndoka** 2:00:12  
Mi hai detto che il container l'hai appena creato, giusto? È tutta la tutto stato cose, tutto tutto il giro è giusto e nello Stato.

_[immagine]_**  
Annalisa Casciaro** 2:00:16  
Sì, posso anche ricrearlo, sì.

_[immagine]_**  
Juela Ndoka** 2:00:27  
Ma anche il container, come Mattia, il tracking unit aggregate.

_[immagine]_**  
Annalisa Casciaro** 2:00:32  
Aspetta che lo controllo.  
Girare la porta anche.  
OK, quindi abbiamo tu unloaded, perché unload?

_[immagine]_**  
Juela Ndoka** 2:00:53  
Lo de lo de de.

_[immagine]_**  
Annalisa Casciaro** 2:00:56  
L'ho appena creato.

_[immagine]_**  
Juela Ndoka** 2:00:58  
È arrivato un lode, non te lo fa fare.

_[immagine]_**  
Annalisa Casciaro** 2:00:59  
Vabbè.  
Lo rifaccio, non importa.  
Scrivi a me se funziona a me va tutto bene.  
ok  
Perfetto, anzi facciamo così.  
3\.

_[immagine]_**  
Juela Ndoka** 2:01:23  
Direttamente unloaded, c'è qualche cosa che li sta facendo arrivare a lode?

_[immagine]_**  
Annalisa Casciaro** 2:01:26  
Ma perché esce così?  
Mamma mia, da quando?

_[immagine]_**  
Juela Ndoka** 2:01:32  
Bella domanda questa.

_[immagine]_**  
Annalisa Casciaro** 2:01:34  
Non si può fare sta cosa o sbaglio qualcosa controlla un attimo.

_[immagine]_**  
Juela Ndoka** 2:01:38  
Spetta, spetta, poi addito un secondo, la quantità la mettiamo, sì, direi.  
1 secondo fa.

_[immagine]_**  
Fabio Massone** 2:01:48  
Controlla la revision, sei sicura che sia?

_[immagine]_**  
Juela Ndoka** 2:01:52  
Sì, Sara.

_[immagine]_**  
Annalisa Casciaro** 2:01:53  
Sì, è stato, ma fino adesso io li ho creati.

_[immagine]_**  
Juela Ndoka** 2:01:56  
Scusa, prova a cambiare un secondo lo Stato da lì vai su discreto e fai Edit. Penso di sì, se non sbaglio no. Scusa Edit, ti ho detto ho sbagliato la quarta quell'iconcina con.

_[immagine]_**  
Annalisa Casciaro** 2:02:04  
Si può fare qua?

_[immagine]_**  
Juela Ndoka** 2:02:13  
Esatto.

_[immagine]_**  
Annalisa Casciaro** 2:02:14  
Facile, facile questa, allora?

_[immagine]_**  
Juela Ndoka** 2:02:17  
OKE mettilo from and loaded to ready Save non so se questo step vale però non però prova.

_[immagine]_**  
Annalisa Casciaro** 2:02:24  
Non importa, proviamo, però li ho creati fino adesso, invece all'improvviso ha unloaded, per carità.

_[immagine]_**  
Juela Ndoka** 2:02:30  
Non so cosa sia successo e non mi sa che questo step non gli va bene.

_[immagine]_**  
Annalisa Casciaro** 2:02:33  
Matteo.  
No, non gli piace. Allora aspetta, aspetta, perché ho provato fino allora facciamo con KNB scusa, li ho creati fino a pochi minuti fa. Ne creo un'altro tanto male non mi fa.

_[immagine]_**  
Juela Ndoka** 2:02:52  
Perch lascialo pure, cioè lo vuoi consolidare? Sì, va bene.

_[immagine]_**  
Annalisa Casciaro** 2:02:54  
No, perché poi devo poi devo segnalare, insomma, OK?  
Controlliamo.

_[immagine]_**  
Juela Ndoka** 2:03:04  
Com'è possibile sta cosa? Non se le all'inizio lo crei così, ma questo frutto?

_[immagine]_**  
Annalisa Casciaro** 2:03:10  
New aspetta, scusa e no, perché?

_[immagine]_**  
Juela Ndoka** 2:03:11  
Maledetto controllami un secondo il buffer che non buffer non abbia qualche problema e quindi tutte quelle li sta li sta facendo unloaded.

_[immagine]_**  
Annalisa Casciaro** 2:03:24  
Allora questo qua è il questo è il bufferkn.be su questo funziona.

_[immagine]_**  
Juela Ndoka** 2:03:32  
OK, su quell'altro è andato a un comportamento, bisogna bisogna pagare il comando stock available un secondo su quello aspetta.

_[immagine]_**  
Annalisa Casciaro** 2:03:34  
Penta.  
E vero, strano.  
Ecco qua.

_[immagine]_**  
Juela Ndoka** 2:03:46  
Elisa, Elisa, sono tutti tuoi.  
Quella parte backend perché lo sta creando così, cioè probabilmente bisogna guardarlo, ma non ti so dare una risposta.  
Così al volo, perché lo sta facendo in questa maniera, cioè cosa lo sta disturbando?

_[immagine]_**  
Annalisa Casciaro** 2:04:02  
Che particola sì.  
Interessante questa cosa. Ecco perché magari in alcuni momenti ce li ha creati e non funzionava. Non ho fatto caso perché ho detto l'ha creato bene prima, perché dovrebbe sbagliare adesso basta cambiarli qui.

_[immagine]_**  
Juela Ndoka** 2:04:23  
Probabilmente quel buffer qualcosa c'ha, perché se lo fai ora e su questo buffer lo mette in unloaded, quel buffer bisogna guardare tutti i suoi.  
C'è tutto così disallineato.

_[immagine]_**  
Annalisa Casciaro** 2:04:39  
Dimmi un po che magari controllo, cioè magari non questo l'ha creato New adesso.

_[immagine]_**  
Juela Ndoka** 2:04:42  
Ma no genio.  
Ma un taxito.

_[immagine]_**  
Annalisa Casciaro** 2:04:47  
Mamma mia, vabbè, non importa, farò più attenzione.

_[immagine]_**  
Juela Ndoka** 2:04:50  
Prova a consumarlo un secondo.

_[immagine]_**  
Annalisa Casciaro** 2:04:53  
Sì, vabbè, adesso sto dando i numeri, dopo un po' non ragiono più. Aspetta, arrivo. Dunque qual è questo qua? Control CE ha fatto?

_[immagine]_**  
Juela Ndoka** 2:04:59  
Non ti preoccupare.  
Sono in questo stato da due anni, quindi vai tranquillo.

_[immagine]_**  
Annalisa Casciaro** 2:05:07  
Tranquilli, ce la faremo, ce la faremo. Tranquilli, OK, no, perché ha sempre funzionato e all'improvviso, a parte il refresh che è meraviglioso. E vabbè, devo fare così. No, l'ha preso, non l'ha preso.

_[immagine]_**  
Juela Ndoka** 2:05:22  
Il 5 però hai hai soddisfatto tutta la quantità, non hai più messo in quantity, quindi lui non te lo consuma perché dice non ho più bisogno.

_[immagine]_**  
Annalisa Casciaro** 2:05:31  
Ma adesso glielo frego io.

_[immagine]_**  
Juela Ndoka** 2:05:33  
Sì.

_[immagine]_**  
Annalisa Casciaro** 2:05:35  
50\.

_[immagine]_**  
Juela Ndoka** 2:05:36  
Flavio Flavio.

_[immagine]_**  
Annalisa Casciaro** 2:05:38  
C'est OK.  
Ok, dovremmo avere facciamo container.

_[immagine]_**  
Juela Ndoka** 2:05:49  
Lo sto facendo, sì, l'ha fatta.

_[immagine]_**  
Annalisa Casciaro** 2:05:50  
Eccolo qua, quindi ogni volta devo andare a controllare, solo che chi glielo spieghi al cliente che se lo fa l'audit la sa OK?

_[immagine]_**  
Juela Ndoka** 2:05:57  
Ma Nicola lo sa sta cosa? Perché? Perché lo fa? Perché lo sto facendo? Non lo cioè non è completamente giusto però che se il container è unload non lo devo consumare, quello lo sa Nicola.

_[immagine]_**  
Annalisa Casciaro** 2:06:07  
No, questa qua gli devo spiegare.  
Sì, però dico il fatto che noi creiamo lo vabbè.

_[immagine]_**  
Juela Ndoka** 2:06:15  
È quello, cioè bisogna attaccarsi un secondo in debug lato backend per capirlo, perché quel comando BRM stock available che sta facendo qualcosa di.

_[immagine]_**  
Annalisa Casciaro** 2:06:25  
OK, quindi dobbiamo capire perché scrive all'audit.

_[immagine]_**  
Juela Ndoka** 2:06:26  
Ma.  
Ha aperto una nuova funzionalità, diciamo.

_[immagine]_**  
Annalisa Casciaro** 2:06:31  
OKOK, va bene, OK, va bene, grazie 1000.

_[immagine]_**  
Juela Ndoka** 2:06:31  
Una no, OK, bambina.  
Prego altro, vado a prendere un caffè.

_[immagine]_**  
Annalisa Casciaro** 2:06:44  
No.

_[immagine]_**  
Juela Ndoka** 2:06:47  
Perfetto.

_[immagine]_**  
Fabio Massone** 2:06:48  
E ora dopo ci risentiamo.

_[immagine]_**  
Juela Ndoka** 2:06:51  
Sì.

_[immagine]_**  
Fabio Massone** 2:06:52  
OKOK, vai quando ci sei.

_[immagine]_**  
Fabio Massone** trascrizione arrestata
