# Brembo - Training per preparazione Hypercare_100426

> Documento sorgente: `E:\BremboDocs\HyperCare Training video\Brembo - Training per preparazione Hypercare_100426.docx`  
> Tipo: Word (.docx)

**Brembo - Training per preparazione Hypercare-20260410\_140704-Registrazione della riunione**

10 aprile 2026, 12:07PM

1 h 56 m 40 s

_[immagine]_**  
Emanuele Merlo** trascrizione avviata

_[immagine]_**  
Juela Ndoka** 0:03  
Bene, e quindi quello può far può far fallire il messaggio e su Connect mom avremo degli errori in cui spiega per esempio, uno degli errori che era più comune all'inizio durante i test era che quando loro ci mandavano l'ordine andava in errore. Perché?  
A noi mancava o il materiale finito o alcuni materiali, cioè alcuni componenti materiali che dovevano essere consumati in quel in quell'ordine, questo era uno degli errori più comuni, diciamo.  
Un'altro errore, per esempio, che abbiamo avuto ieri nel sito durante durante la durante il sito che abbiamo fatto per testare la parte AGV è che EVM ci manda, cioè mandava un Stato empty.  
Si fermava su CPIE, su Connect mom avevamo un errore 500.  
Però non era un problema nostro, a noi non si aggiornava la pagina perché questo messaggio andava in errore. Però è tutto tracciato su connectmon tutta la gestione di comunicazione tra.  
Tra SAP, cioè quando dico SAP intendo EWMSPI perché per noi sono SAP tutti e due li tracciamo su Connect Mom sì Alessio.

_[immagine]_**  
Alessio Monaco** 1:30  
Allora no, io l'ottica di questo discorso del Connect Mom. Io avendo fatto una visita l'altro giorno con Jacopo nello stabilimento di Brembo, io ho fatto una riflessione, diciamo l'ho detto ieri a Jacopo, approfitto, si parla del tema Connect Mom.  
Anche qui con tutti quanti, cioè io personalmente guardando la linea di produzione di mapello, io ho difficoltà a capire come noi facciamo a fermare la fabbrica, cioè nel senso che noi non controlliamo le macchine automatiche, cioè noi non diamo lo start alle macchine automatiche.

_[immagine]_**  
Juela Ndoka** 1:56  
Sì.  
Sì, certo, questo era un esempio che ho che ho fatto io, perché?

_[immagine]_**  
Alessio Monaco** 2:11  
No, io no, scusami. Concludo, concludo il discorso no, perché nel senso, nel senso noi non abbiamo l'onere di far partire le macchine automatiche e quindi passatemi il termine con noi o senza di noi fanno il loro lavoro. Quello che mi è parso.

_[immagine]_**  
Juela Ndoka** 2:15  
Sì.

_[immagine]_**  
Emanuele Merlo** 2:25  
Però aspetta Alessio, se manca.

_[immagine]_**  
Juela Ndoka** 2:26  
A tutti.

_[immagine]_**  
Alessio Monaco** 2:27  
Aspetta, no, giusto per chiudere il cerchio. Quello che io, quello che io ho notato dal processo è che l'unico momento che noi siamo, diciamo il punto di il point of failure del sistema è che se noi non mandiamo.  
I messaggi di consuntivazione ai terzi, quindi al magazzino piuttosto che a SAP, perché la linea in sé a produrre produce, cioè non aspetta certo noi, quindi.

_[immagine]_**  
Juela Ndoka** 2:46  
Ciao Ciao.  
C'è sempre.

_[immagine]_**  
Francesco Panigo** 2:50  
E anche la stampa etichette.

_[immagine]_**  
Juela Ndoka** 2:52  
Allora su questo punto diciamo che noi non siamo il fattore, cioè principale, che possiamo fermare questo tipo di movimento, cioè noi mandiamo la richiesta, per esempio per le macchine automatiche, noi mandiamo la richiesta AEVM.  
E noi? Cioè i punti in cui noi possiamo fallire è che non mandiamo correttamente la richiesta. Peraltro noi siamo sempre in ascolto a aspettare che SAP ci cioè faccia il mission. Lo passa a Toyota, per esempio.  
Finiscono in loro tutto il giro che devono finire e ci danno una risposta a noi e quello che facciamo noi è solo mandiamo la richiesta e poi stiamo in ascolto, cioè finora per questa parte.

_[immagine]_**  
Francesco Panigo** 3:37  
Sì.

_[immagine]_**  
Alessio Monaco** 3:39  
Sì, ma in generale non correggimi se sbaglio, ma noi non abilitiamo macchinari automatici per lavorazioni, giusto? Corretto.

_[immagine]_**  
Juela Ndoka** 3:48  
No, noi no, cioè direttamente da MES.

_[immagine]_**  
Alessio Monaco** 3:50  
Cioè io quello che ho visto ad Ocampo, loro fanno debbero fare lo start di un work order in base a dove ci troviamo sulla.

_[immagine]_**  
Juela Ndoka** 3:57  
Noi facciamo le chiamate materiali, però OK, però non siamo noi, diciamo l'attore, sì, vai.

_[immagine]_**  
Alessio Monaco** 4:00  
Perfetto.

_[immagine]_**  
Emanuele Merlo** 4:02  
Però posso.

_[immagine]_**  
Alessio Monaco** 4:02  
Perfetto, OK.

_[immagine]_**  
Emanuele Merlo** 4:06  
Sì, no, dicevo, è pacifico che la produzione fisica non la fermiamo, perché non siamo noi che diamo i consensi, però se manca la tracciabilità, se mancano i consumi, se mancano le produzioni, se mancano tutto.  
Si perde tutta la visibilità sulla produzione, ci sono anche delle compliance di legge probabilmente a cui dovranno sottostare.

_[immagine]_**  
Juela Ndoka** 4:26  
Certo, c'è un disallineamento su tutto quello.

_[immagine]_**  
Emanuele Merlo** 4:30  
E quindi di fatto possono produrre ma poi non hanno il controllo su quello che producono e va, cioè tutto un casino perché uscisse una non conformance per un richiamo.

_[immagine]_**  
Alessio Monaco** 4:38  
No, sì, no, ma io.

_[immagine]_**  
Juela Ndoka** 4:38  
Sì, ma questo non nel caso specifico che ha fatto Alessio, cioè questo che dici tu su sulle conferme che mandiamo noi in base al consumo Alessio stava chiedendo delle macchine automatiche, giusto Alessia, OK.

_[immagine]_**  
Alessio Monaco** 4:52  
Corretto.  
Quindi io dico allora noi tra virgolette, la linea tra virgolette, che è anche molto semplice come struttura, da quello che ho potuto vedere non ha PLC, non ha nulla di movimentazione automatica che noi comandiamo, almeno per quella linea che ho visto io, per quella.  
La zona di mapello, che funziona.

_[immagine]_**  
Juela Ndoka** 5:10  
Io non ho mai visto, quindi ti sto parlando solo in teoria, quindi.

_[immagine]_**  
Alessio Monaco** 5:14  
OK, perfetto allora io però quello che ho detto anche ieri a Jacopo ho detto, io mi immagino che una situazione critica che sicuramente si andrà a verificare, magari in go live, è che per un qualsivoglia motivo e nei messaggi che noi mandiamo col Connect Mom.  
A SAP piuttosto che alla componente middleware specifica del SAP per qualsiasi motivo non arrivi, non parta, andiamo in errore OK allora io domandavo, ma noi come team no, visto che poi alla fine potrebbe succedere a chiunque di noi che starà in impianto.

_[immagine]_**  
Juela Ndoka** 5:34  
Sì.  
Esatto.

_[immagine]_**  
Alessio Monaco** 5:53  
Magari c'è qualcuno che è più esperto di Connect Mom, c'è una procedura fatemi dire di workaround per cui mi accorgo dalla history del Connect Mom che c'ho n messaggi.  
In failure e io li posso rimandare in maniera forzata? Domanda.

_[immagine]_**  
Juela Ndoka** 6:09  
Sì.  
Allora io non sono l'esperta di connectmon, però su questo ti posso rispondere. Prima di tutto credo che hanno configurato un retry, quindi riprova dopo un tot rimandare il messaggio, altrimenti c'è una folder che si chiama manual.  
Import che lo puoi forzare tu, cioè che anche durante i sit per esempio, questo non è bello da sentire, però un paio di volte l'abbiamo fatto perché sa, cioè gli serviva per forza che noi gli mandavamo quello che abbiamo consumato per non creare disallineamento. Quindi prendiamo diciamo il messaggio.

_[immagine]_**  
Francesco Panigo** 6:44  
Sì, in quel caso, però, la resend.

_[immagine]_**  
Juela Ndoka** 6:47  
Esatto, e lo e lo mandiamo.

_[immagine]_**  
Alessio Monaco** 6:49  
OK, quindi noi però stiamo dicendo che noi generiamo sempre il messaggio, cioè non c'è un problema di generazione di messaggio, ma ci può essere un problema di comunicazione per cui noi il messaggio da qualche parte generato ce l'abbiamo.

_[immagine]_**  
Juela Ndoka** 7:03  
Sì.

_[immagine]_**  
Alessio Monaco** 7:05  
Lo scarichiamo, apriamo la folder manuale, lo forziamo lì all'interno di questa folder manuale e arriva a destinazione. Questo stiamo dicendo, giusto? Quindi noi disputiamo la casistica che non generiamo il messaggio, cioè giusto?

_[immagine]_**  
Juela Ndoka** 7:05  
Sì.  
Sì, esatto.  
Allora cioè se non generiamo un messaggio lì è un problema che non risolviamo con workaround perché dobbiamo mettere le mani al codice, quindi non sarà una soluzione diciamo immediata quello non.

_[immagine]_**  
Alessio Monaco** 7:33  
Che.

_[immagine]_**  
Juela Ndoka** 7:37  
Quindi spero che non saremo mai in quelle condizioni.

_[immagine]_**  
Alessio Monaco** 7:38  
Ok.  
No, nel senso che io guardando la linea vi ripeto, ma come m'è m'è balzato all'occhio ho detto sicuramente un punto ci possono fare la pelle e che per qualche motivo non arrivano i messaggi o non arrivano tutti i messaggi nell'ordine che non lo so, SAP richiede.  
E a quel punto servirebbe avere una procedura per cui in maniera furba riusciamo a tirar fuori tutti i messaggi, fammi dire, di un certo lotto di tempo, un certo range temporale di una certa stazione.

_[immagine]_**  
Juela Ndoka** 8:11  
Allora Giacomo è qui, magari può confermare, però credo che ci sia che è in corso. Non so se è partito, però c'era uno sviluppo che doveva raccogliere i momenti in cui magari Connect moment down o ci sia qualche problema dovrebbero essere uno sviluppo che raccoglie tutti questi messaggi.  
E prova a rimandarli una volta che è su, diciamo, però non so se è partito o è rimasto fermo questo sviluppo.

_[immagine]_**  
Giacomo Centore** 8:42  
No, non è non è partito, abbiamo abbiamo una query.

_[immagine]_**  
Juela Ndoka** 8:45  
Ok.

_[immagine]_**  
Giacomo Centore** 8:49  
Piuttosto efficace nel caso in cui succedesse si possono recuperare una query non è sì, esatto, non è neanche una query in realtà da prompt del comando, cioè 1 1 script e.

_[immagine]_**  
Juela Ndoka** 8:57  
I messaggi persi che c'ho?

_[immagine]_**  
Giacomo Centore** 9:05  
Ovviamente bisogna bisogna prima indagare un attimo sul database, mettere il range giusto di date o di in modo tale da mettere solo quelli che sono falliti.

_[immagine]_**  
Juela Ndoka** 9:18  
OK.

_[immagine]_**  
Alessio Monaco** 9:19  
OK, ma una domanda, queste diciamo operatività diciamo di ultima frontiera no, noi le stiamo raccogliendo su una folder comune diciamo di AMS di impianto o sono diciamo così?  
Uno sa una cosa, quindi lo e lui va di riferimento.

_[immagine]_**  
Giacomo Centore** 9:39  
Di solito uno sa una cosa e l'altro sa l'altra, sì.

_[immagine]_**  
Juela Ndoka** 9:42  
Sì, però dobbiamo dobbiamo creare delle procedure, sì.

_[immagine]_**  
Giacomo Centore** 9:44  
Ci dobbiamo uniformare e creare. Sì, no, sono in creazione delle procedure. Ci sono dei file, dei file anche su come comportarsi in determinate cose. L'a MS.  
Già fatti. Manca poi una repository comune in effetti, dove mettere magari anche tutti i riferimenti che ci sono in questo documento, cioè se dici si usa questo script almeno sai dove te lo devi andare a prendere poi questo script perché?

_[immagine]_**  
Juela Ndoka** 10:19  
Sì, certo, dobbiamo creare queste procedure perché per ora non ce li abbiamo, cioè.

_[immagine]_**  
Giacomo Centore** 10:22  
Però è in fase è in fase no, è in fase di sviluppo, ecco.

_[immagine]_**  
Juela Ndoka** 10:26  
OK, ma su tutto, cioè non è che per ora abbiamo creato un file in cui ti dica cioè neanche per lato UI per esempio, che la UI è uno dei punti più scoperti possibili, cioè non è che.

_[immagine]_**  
Giacomo Centore** 10:27  
Sì.  
Sì.

_[immagine]_**  
Juela Ndoka** 10:41  
C'è un documento in cui diciamo fai questo, fai questo per nessun componente del della nostra soluzione, abbiamo una procedura di workaround per ora.

_[immagine]_**  
Alessio Monaco** 10:54  
No, capisco, per.  
Quale componente ce l'hai?

_[immagine]_**  
Juela Ndoka** 10:57  
Una procedura di per ogni componente, perché cioè mendix è un componente Connect, non è un componente discreto, è un componente AGW automation gateway è un componente, quindi ognuno c'ha il suo.  
Il suo atteggiamento? Quindi in qualche maniera dobbiamo scrivere una procedura che nel caso falliste mendis cosa dovresti fare? Nel caso la soluzione è giù, spero no. Cosa dobbiamo fare nel caso automation gateway non si prende cosa?  
Riprende. Cosa dobbiamo fare? Connect no, non si riprende, cioè dobbiamo mettere una lista di.  
The workaround.

_[immagine]_**  
Alessio Monaco** 11:39  
OK, io pensavo che.

_[immagine]_**  
Juela Ndoka** 11:39  
Quindi per ora ogni persona sa alcune cose, però non è diciamo sono poco, non sono ufficialmente condivisi.

_[immagine]_**  
Alessio Monaco** 11:49  
OK, quindi diciamo che non è mai stato fatto un dei problemi di è successo nell'impianto di ostrava, se ho capito bene.

_[immagine]_**  
Juela Ndoka** 11:58  
E cioè la sfortuna è che noi, cioè siamo uscite dal gruppo di Siemens e non anche se loro avevano delle procedure, non abbiamo potuto recuperare noi come team, per esempio io e Jacopo.  
Perché poi ci hanno fatto uscire anche dalle SharePoint, documenti e tutto quanto, quindi non abbiamo più accesso a niente, solo quello che hanno mandato all'a MS per ora.

_[immagine]_**  
Alessio Monaco** 12:12  
Sì.  
Capito?  
Con chi lavoravi, con il Gino Luongo in Ostrama.

_[immagine]_**  
Juela Ndoka** 12:29  
Igino, Omar, sommani, Zagarola.

_[immagine]_**  
Alessio Monaco** 12:36  
OK, no, il giro l'ho conosciuto in Melfi. Va bene, OK, no grazie. Era solo per questo perché hai detto ma era avevo visto un punto di attenzione che se me era quello che sicuramente ci avremo problemi in impianto con i messaggi, perché quella è una cosa abbastanza.  
Standard sui prodotti Siemens che spesso capita, quindi.

_[immagine]_**  
Juela Ndoka** 12:55  
Sì, molto spesso.

_[immagine]_**  
Alessio Monaco** 12:58  
Quindi questo ho detto, ma magari ce l'abbiamo, oppure se noncelabbiamoaverlaprontapotrebbedarerespiroachiachifal'assistenzasullalineadiciamoeccoperchepensoquellosiaun.in cui.  
Ci avremo saremo un po più tartarsati come richieste secondo me, però vedendo un po il processo produttivo.

_[immagine]_**  
Juela Ndoka** 13:18  
Sì.  
Sì.

_[immagine]_**  
Paolo Comparoni** 13:24  
Scusa Juela, ci puoi far vedere magari qualcosa del log di persistenza del Connect mom de della lista dei messaggi tanto per.

_[immagine]_**  
Juela Ndoka** 13:35  
Sì e ho un problemino che cioè mi è scaduto il password tipo a 12:00 e non sono riuscita a aggiornare quindi qualcheduno mi deve condividere finché lo cambio.

_[immagine]_**  
Paolo Comparoni** 13:48  
Grazie se qualcuno può condividere così.

_[immagine]_**  
Francesco Panigo** 13:50  
Se vuoi per aggiornarla, basta che dico.

_[immagine]_**  
Juela Ndoka** 13:53  
Sì, però devo chiedere a voi qualcuno di voi che mi fa fare il login e così lo posso cambiare da Windows sì.

_[immagine]_**  
Francesco Panigo** 13:59  
Sì, infatti no, ma posso anche condividerti la cioè la password di con eng che è scaduta.

_[immagine]_**  
Juela Ndoka** 14:06  
Sì, è con n admin F tutte e due.

_[immagine]_**  
Francesco Panigo** 14:09  
OK, vai tanto per una, allora facciamo così.  
Sì.

_[immagine]_**  
Paolo Comparoni** 14:20  
Tra l'altro oggi abbiamo fatto un mini giro con Emanuele, abbiamo visto che c'è LGW che è a.

_[immagine]_**  
Francesco Panigo** 14:25  
Tu sei con Engel?

_[immagine]_**  
Juela Ndoka** 14:26  
38\.

_[immagine]_**  
Francesco Panigo** 14:28  
Ok, richiedimi pure il controllo e puoi cambiartela.

_[immagine]_**  
Juela Ndoka** 14:32  
OK.

_[immagine]_**  
Paolo Comparoni** 14:35  
Dico, segue la mente mentre sta facendo, c'è un modo per escludere GW, magari per questa fase di training?  
Visto che su Q adesso abbiamo visto che c'erano de degli errori di AGW.

_[immagine]_**  
Juela Ndoka** 14:49  
Allora?  
Aspetta che finisco, allora ho chiesto il controllo, ma non so se l'hai.

_[immagine]_**  
Paolo Comparoni** 14:54  
OK.

_[immagine]_**  
Francesco Panigo** 14:58  
Per me lo sto vedendo.

_[immagine]_**  
Juela Ndoka** 15:03  
Mi sa che non riesco a entrare nel citrix.  
Allora non hai assunto il controllo, mi dice non è stata accettata, lo richiedo.

_[immagine]_**  
Francesco Panigo** 15:12  
Aspetta, non ho visto, non ho, non ho visto la notifica.  
Riprovo un attimo.

_[immagine]_**  
Juela Ndoka** 15:18  
Riprovo, richiedi.

_[immagine]_**  
Francesco Panigo** 15:22  
Ok, ora l'ho visto.  
Era la registrazione che mi.

_[immagine]_**  
Juela Ndoka** 15:26  
Ora ce l'ho allora Emanuele, hai provato a togliere dal Equipment configuration l'instant node?

_[immagine]_**  
Emanuele Merlo** 15:38  
No, io ela ero dietro a raccogliere i documenti per i deliverables. Non ce l'ho fatta. No, mi ci sono messo dietro.

_[immagine]_**  
Juela Ndoka** 15:48  
OK, perché?  
Ora devo scrivere tutto che non riesco a copiare e.  
Prova a togliere vai su Equipment configuration.

_[immagine]_**  
Emanuele Merlo** 16:06  
Aspetta che devo collegarmi.  
Non era una cosa che mi bloccava in quel momento lì abbiamo guardato una cosa con Paolo, è uscito quel messaggio lì, ha detto, non vorrei che fosse un baco.

_[immagine]_**  
Juela Ndoka** 16:20  
No, non è un pacco, ti sta semplicemente dicendo che non puoi startare il tuo ordine perché c'è un cioè non riesce a scrivere sull'automation node, non riesce perché non è configurato bene, quindi non riesce né scrivere né leggere.

_[immagine]_**  
Emanuele Merlo** 16:36  
C'ho il solito problema a connettermi, aspetta.

_[immagine]_**  
Juela Ndoka** 16:44  
L'ho perso.

_[immagine]_**  
Paolo Comparoni** 16:47  
Quindi se ci capita, basta che dissociamo il nodo.

_[immagine]_**  
Juela Ndoka** 16:51  
E non dovremmo farlo in realtà, perché tutti i tag che mandiamo poi li li perdiamo, ecco.

_[immagine]_**  
Paolo Comparoni** 16:53  
No, però.  
Sì, no, le dico, magari lo disassociamo e poi lo riassociamo quando abbiamo finito il test.

_[immagine]_**  
Juela Ndoka** 17:04  
Sì.

_[immagine]_**  
Paolo Comparoni** 17:05  
OKOK, grazie.

_[immagine]_**  
Juela Ndoka** 17:08  
Prego.  
Un po lento.  
Erika.

_[immagine]_**  
Francesco Panigo** 17:28  
Tanto questa è una cosa che potrebbe capitare a chiunque in qualunque momento.

_[immagine]_**  
Juela Ndoka** 17:34  
OK.  
Una forte.  
No, perché?

_[immagine]_**  
Francesco Panigo** 17:57  
Sembrano anche diverse.

_[immagine]_**  
Juela Ndoka** 17:57  
Allora qua mi ha perso delle mi ha perso la scritta.  
Ok, una.

_[immagine]_**  
Francesco Panigo** 18:21  
Ok, ora.

_[immagine]_**  
Juela Ndoka** 18:22  
Perfetto.  
Ora provo ad accedere e poi lo cambio io quello admin S da lì OK, perfetto, grazie.

_[immagine]_**  
Francesco Panigo** 18:32  
Sì, OK.  
Su.

_[immagine]_**  
Emanuele Merlo** 19:33  
Mi sto picchiando con.  
Un login, intanto prima di pranzo ha funzionato, poi a un certo punto smette di funzionare.

_[immagine]_**  
Francesco Panigo** 20:11  
C'est.

_[immagine]_**  
Juela Ndoka** 20:14  
OK Tommaso, mentre aspettiamo un secondo Emanuele, sei riuscito a andare in debug verso gava?

_[immagine]_**  
Tommaso Penta** 20:24  
No.

_[immagine]_**  
Juela Ndoka** 20:25  
No.  
Vuoi condividere?

_[immagine]_**  
Tommaso Penta** 20:29  
Sì.

_[immagine]_**  
Juela Ndoka** 20:44  
OK, facciamo un po' di mendix finché si collega Emanuele.

_[immagine]_**  
Emanuele Merlo** 21:05  
A un certo punto, tipicamente nei dintorni della pausa pranzo, poi non mi connette più o rimane appesa qualche connessione prima.

_[immagine]_**  
Juela Ndoka** 21:11  
Pronto.  
Sì, vai nella task manager e chiudici tricks, cioè killa il processo e aprilo incognito.

_[immagine]_**  
Emanuele Merlo** 21:22  
No, ma al MES tool riesco a connettermi alla macchina remota.

_[immagine]_**  
Tommaso Penta** 21:25  
Sì, OK, adesso non riesco a connettermi.

_[immagine]_**  
Juela Ndoka** 21:28  
Anche tu.

_[immagine]_**  
Francesco Panigo** 21:31  
Lia qualche.

_[immagine]_**  
Juela Ndoka** 21:33  
Non è che.

_[immagine]_**  
Francesco Panigo** 21:33  
Hai hai hai qualche ossessione appesa che ti sbaglia la password da qualche parte secondo me?

_[immagine]_**  
Juela Ndoka** 21:37  
Esatto.

_[immagine]_**  
Tommaso Penta** 21:38  
MES.

_[immagine]_**  
Emanuele Merlo** 21:39  
Sì, ma poi trovarla è un casino.

_[immagine]_**  
Francesco Panigo** 21:41  
E bisognerebbe.

_[immagine]_**  
Tommaso Penta** 21:42  
Se chiudo e riapro va.

_[immagine]_**  
Juela Ndoka** 21:48  
OK, aspetta, lancia il process XP sixty Four per capire quante utenze tu, quante accessi hai con quello.  
Vice two users.  
E quanti 25 sono?  
Uno solo, uno solo, quindi.

_[immagine]_**  
Tommaso Penta** 22:16  
A.

_[immagine]_**  
Francesco Panigo** 22:19  
Ma potrebbe essere anche sulle macchine remote.

_[immagine]_**  
Tommaso Penta** 22:32  
Prova.  
Ma nessuno è collegato su te, che voi sappiate.

_[immagine]_**  
Juela Ndoka** 22:59  
Io no.

_[immagine]_**  
Tommaso Penta** 23:00  
De vostra.

_[immagine]_**  
Francesco Panigo** 23:00  
No.

_[immagine]_**  
Giacomo Centore** 23:01  
Io sono collegato.  
Sì.

_[immagine]_**  
Tommaso Penta** 23:03  
Beh, peccato, prova a chiudere la mia sessione se l'avete aperta.

_[immagine]_**  
Giacomo Centore** 23:10  
Ho capito.

_[immagine]_**  
Francesco Panigo** 23:12  
23, giusto?

_[immagine]_**  
Tommaso Penta** 23:14  
25\.

_[immagine]_**  
Giacomo Centore** 23:16  
Sì.  
25 6 6 disconnesso se ti faccio sign out se.

_[immagine]_**  
Tommaso Penta** 23:25  
Se fai sign out sì.

_[immagine]_**  
Juela Ndoka** 23:26  
C'est fa le sa note.

_[immagine]_**  
Francesco Panigo** 23:35  
Sì, veramente tra Alberto.

_[immagine]_**  
Giacomo Centore** 23:37  
OK, fuori.

_[immagine]_**  
Tommaso Penta** 23:39  
Ok.

_[immagine]_**  
Juela Ndoka** 23:46  
No.  
Non è che ti è scaduto il password?

_[immagine]_**  
Tommaso Penta** 23:50  
E no, ma pure stamattina faceva così, infatti ho provato diverse cose, avevo aperto un ticket, poi all'improvviso si è ripreso senza aver fatto nulla di fatto.  
Infatti questa qua è la password vecchia e questa era quella nuova, infatti ho provato di tutto.

_[immagine]_**  
Juela Ndoka** 24:05  
Scusa.  
La tua cartella visibile da te, prova con admin se riesci per capire se la tua utenza o c'è qualcos'altro che non va.

_[immagine]_**  
Tommaso Penta** 24:17  
Abro con admin.

_[immagine]_**  
Juela Ndoka** 24:19  
No, provo un attimo per capire.

_[immagine]_**  
Tommaso Penta** 24:39  
Ecco, possibile che mi incolla un'altra?  
Altra roba, cioè.

_[immagine]_**  
Francesco Panigo** 24:44  
Ma te la puoi salvare comunque, senza stare a incollare ogni volta.

_[immagine]_**  
Tommaso Penta** 24:52  
Chiamandome.  
No, però me faceva strano che cioè la seconda volta che mi.  
Come se andassi in memoria un'altra, un'altra copia di altra roba.  
Ma capito?  
Ma scusa se metto un'altra roba a casaccio.  
Pure stamattina avevo dubbio della password.

_[immagine]_**  
Francesco Panigo** 25:21  
Sennò prova con remote desktop classico.

_[immagine]_**  
Tommaso Penta** 25:25  
Sì, in effetti.

_[immagine]_**  
Emanuele Merlo** 25:27  
Colori di solito funziona.

_[immagine]_**  
Francesco Panigo** 25:33  
Qua su questo RDC mano un po' di configurazioni.

_[immagine]_**  
Emanuele Merlo** 25:33  
Va.

_[immagine]_**  
Francesco Panigo** 25:38  
Un po nascoste che a volte, se non sono, se non sono corrette, fa fa casino.

_[immagine]_**  
Juela Ndoka** 25:53  
Passo al Centon.

_[immagine]_**  
Francesco Panigo** 25:56  
Troppi tentativi di accesso, quindi attentamente bloccato.

_[immagine]_**  
Emanuele Merlo** 26:02  
Io non riesco per ora.  
Ero collegato prima della pausa pranzo e adesso non ci riesco più.

_[immagine]_**  
Juela Ndoka** 26:35  
Dove ce l'hai la repository CE l'hai su tempo sulla tua utenza, Tommaso?

_[immagine]_**  
Tommaso Penta** 26:41  
Su temp.

_[immagine]_**  
Juela Ndoka** 26:43  
Allora entra con admin, con l'utenza admin e ti spiego questa cosa, poi passiamo da Emanuele.

_[immagine]_**  
Tommaso Penta** 26:50  
Ok.  
Non intendi questa?

_[immagine]_**  
Juela Ndoka** 27:02  
Sì.

_[immagine]_**  
Tommaso Penta** 27:41  
Bisogna fare un po di pulizia, però.

_[immagine]_**  
Emanuele Merlo** 28:53  
No, ho già l'account bloccato, too many log on to attempts, bisogna solo aspettare.

_[immagine]_**  
Juela Ndoka** 29:01  
Va bene, condivido io appena finiamo con Tommaso.

_[immagine]_**  
Tommaso Penta** 29:06  
Con l'utenza non posso lavorare ancora, OK?

_[immagine]_**  
Juela Ndoka** 29:13  
L'hai reso visibile per tutti.

_[immagine]_**  
Tommaso Penta** 29:17  
Come.

_[immagine]_**  
Juela Ndoka** 29:20  
Stiamo guardando il tuo password?

_[immagine]_**  
Tommaso Penta** 29:22  
Mi si, manco me ne ero d'accordo, vabbè, non importa.  
Ecco, e se avete guardata è sbagliato.  
Sei.  
Capisco.  
Se un uno o una M.

_[immagine]_**  
Juela Ndoka** 30:30  
Finalmente.  
Vai.  
Open.

_[immagine]_**  
Tommaso Penta** 30:36  
Casa.

_[immagine]_**  
Juela Ndoka** 30:38  
Perché non è basta, non è non è tuo, non è non è di admin, questo per quello ti ho chiesto.

_[immagine]_**  
Tommaso Penta** 30:42  
È aperto da no.  
In che senso non andiamo?

_[immagine]_**  
Juela Ndoka** 30:48  
E della tua utenza alla repository locata dalla tua utenza va a.  
Lui va a leggere anche chi è launer.  
OK, Apri un mendix che è stato fatto un che ne so uno e poi lo puoi applicare ovunque uguale.

_[immagine]_**  
Tommaso Penta** 31:08  
Allora boh, allora faranno tutti ora gnocchi, saranno tutti ora.

_[immagine]_**  
Juela Ndoka** 31:10  
Ne ho uno a casa, no, vai, studi, c'è un Mendes, altro lì a quel livello lì.

_[immagine]_**  
Tommaso Penta** 31:21  
Provenzano.  
Sono a casa.

_[immagine]_**  
Juela Ndoka** 32:24  
Fai un secondo sign in later.

_[immagine]_**  
Tommaso Penta** 32:26  
A me allora.  
Per questo.

_[immagine]_**  
Juela Ndoka** 32:31  
A tutti allora ti spiego, condivido io ti spiego perché altrimenti non.  
Non finiamo mai, allora.  
Ti ho buttato fuori.

_[immagine]_**  
Tommaso Penta** 32:56  
Esatto.

_[immagine]_**  
Juela Ndoka** 33:13  
Registrato sì, OK, perfetto.

_[immagine]_**  
Tommaso Penta** 33:38  
Poi è andato incredibile.

_[immagine]_**  
Juela Ndoka** 33:41  
OK, buttami fuori.  
Ho visto che a me piace fare la bacchettona, però quando prima del training un po' di test di connessione, avere la connessione verso la macchina pronta non sarebbe male.

_[immagine]_**  
Tommaso Penta** 35:33  
Sì.

_[immagine]_**  
Emanuele Merlo** 35:37  
Nel mio caso prima di pranzo ero collegato, quindi non mi aspettavo di trovarmi sta Roma.

_[immagine]_**  
Juela Ndoka** 35:40  
No, perché abbiamo perso 42 minuti.

_[immagine]_**  
Francesco Panigo** 35:42  
Ora risulti locked in effetti con admin F con 27 e anche e anche Stella in questo momento risulta locked.  
Tutti gli altri no.

_[immagine]_**  
Juela Ndoka** 35:56  
Santi.

_[immagine]_**  
Tommaso Penta** 35:56  
Dopo pranzo però, cioè poi accade la connessione, cioè nel senso.

_[immagine]_**  
Emanuele Merlo** 36:00  
Sì, dopo pranzo sicuramente va via la connessione però.

_[immagine]_**  
Tommaso Penta** 36:02  
Quindi, con tutta la buona volontà, ritorno al pranzo senza connessione.

_[immagine]_**  
Juela Ndoka** 36:06  
Ho capito, però ci torniamo alle 01:45 e facciamolo sì.

_[immagine]_**  
Tommaso Penta** 36:09  
Ho capito però alle due e sicuramente alle due non avrò la almeno io non avrò la sessione pronta, poi se mi collego per qualche motivo non si collega, cioè?

_[immagine]_**  
Juela Ndoka** 36:18  
Va bene?  
Apriamo la configuration vai.  
Salve.  
OK, no, aspetta, aspetta, aspetta, vai su Constance.

_[immagine]_**  
Tommaso Penta** 36:31  
Ma sicuramente hai sbagliato.

_[immagine]_**  
Juela Ndoka** 36:38  
OK.  
Allora siamo in multiplant OKE, probabilmente alcuni di questi o data puntano ancora perché l'abbiamo copiato dal configurazione di ostrava che era un singolo plant quindi.  
Ora non so se hai preso tutti però potrebbe essere che alcuni di questo non so dove andare a prenderli perché ora serve per forza sull'endpoint lato mendx specificare anche il plan dove sei quindi vai su solution studio.

_[immagine]_**  
Tommaso Penta** 37:29  
Però su qua su DEV scusa su DEV devo andare su quality.

_[immagine]_**  
Juela Ndoka** 37:30  
Sì.  
Tu qua?

_[immagine]_**  
Paolo Comparoni** 37:37  
Ma che pagina avete con Mendix Juela, la repetitive?

_[immagine]_**  
Juela Ndoka** 37:42  
Sì, sta cercando di andare in debug per capire un errore che abbiamo dato dal dev verso quality per capire cosa sta fallendo. Quindi ora guarda II punti point che ti servono e prendilo con la terza.

_[immagine]_**  
Paolo Comparoni** 37:44  
OK.

_[immagine]_**  
Juela Ndoka** 38:01  
Iconcina qua che prende l'endpoint giusto, vai su dov'è la soluzione mendix.  
Per esempio, OK.

_[immagine]_**  
Tommaso Penta** 38:12  
Si fa questo solution.

_[immagine]_**  
Juela Ndoka** 38:14  
No, quello ce l'hai già vedo, c'è scritto da là.

_[immagine]_**  
Tommaso Penta** 38:17  
Perché questa qua ho sì, infatti quello che ho fatto, ho sostituito tutti io. Stavo con gava però senza sapere se era giusto. Ecco.

_[immagine]_**  
Juela Ndoka** 38:23  
OK, va bene, vai su, prendi la Brembo, prendiamo la Brembo prima che è quello più importante.  
A Brembo prendi l'endpoint, OK, vai di là.  
Sostituiscilo.  
A bimbo sotto ancora.  
Ma.  
Mi tiro le nel bello.  
Tolli 443.

_[immagine]_**  
Tommaso Penta** 38:59  
E sono.  
E quindi proprio questo cambiava.

_[immagine]_**  
Juela Ndoka** 39:08  
Sì.

_[immagine]_**  
Tommaso Penta** 39:10  
OK, capito?

_[immagine]_**  
Juela Ndoka** 39:11  
Queste vanno cambiate tutte, vai su APO ADM, prendi APO ADM.

_[immagine]_**  
Tommaso Penta** 39:23  
A te che la messa mi dà fastidio.

_[immagine]_**  
Juela Ndoka** 39:33  
Sempre il 443 rimuovilo OK.  
On equipment.  
No tira.

_[immagine]_**  
Tommaso Penta** 40:06  
Quindi fino a fino all'engineering.

_[immagine]_**  
Juela Ndoka** 40:10  
No, anche la più importante è la quality execution, anche perché lì va a fare la query dove ti mostra tutto l'equipment che hai per quel plan.

_[immagine]_**  
Tommaso Penta** 40:15  
Ok.

_[immagine]_**  
Juela Ndoka** 40:20  
OK.  
Cioè ogni punto che tu vedi qui vuol dire che nel tuo application c'hai un'integrazione verso quell'applicazione per andare a leggere le sue entità.

_[immagine]_**  
Tommaso Penta** 40:21  
OK.

_[immagine]_**  
Annalisa Casciaro** 40:43  
Ma su questo non c'è un file di configurazione che si può sostituire sotto il naso.

_[immagine]_**  
Juela Ndoka** 40:48  
È solo è solo debug in questo Annalisa, quindi solo per andare in debug, quindi ogni persona che deve fare, cioè crea un nuovo punto di debug, deve fare questa, deve fare questo gioco.

_[immagine]_**  
Tommaso Penta** 40:49  
Sì, questo.

_[immagine]_**  
Annalisa Casciaro** 41:00  
OK.

_[immagine]_**  
Juela Ndoka** 41:02  
Per noi non è generico, cioè ognuno, ogni istanza deve fare il suo, quindi.

_[immagine]_**  
Annalisa Casciaro** 41:07  
Però dico, non salva un file di configurazione che può essere utile da sostituire ogni volta.

_[immagine]_**  
Juela Ndoka** 41:08  
A molto.  
Sì, però, cioè non.

_[immagine]_**  
Annalisa Casciaro** 41:14  
So solo l'idea.  
A fare un giochino al volo, ecco.

_[immagine]_**  
Juela Ndoka** 41:20  
Sì, c'è, però comunque non è, non è.

_[immagine]_**  
Annalisa Casciaro** 41:26  
Salutare, diciamo.

_[immagine]_**  
Juela Ndoka** 41:27  
Sono 2, 2 punti sono da sostituire, diciamo qui, queste è la licenza e basta.

_[immagine]_**  
Annalisa Casciaro** 41:35  
OK.

_[immagine]_**  
Alessio Monaco** 41:35  
Insomma, questo che stiamo vedendo serve per.

_[immagine]_**  
Tommaso Penta** 41:39  
Configurare.

_[immagine]_**  
Juela Ndoka** 41:39  
E così lui può andare in debug dalla macchina de verso quality per capire cosa sta fallendo sul consumo per il e lo so che è fuori al nostro però.  
Su JJ hanno un problema, ho approfittato così Tommaso lo vede questo step e poi riesce a farlo e riesce a aiutare a capire qual è qual è l'errore.

_[immagine]_**  
Tommaso Penta** 42:05  
Ecco.  
Questo è.

_[immagine]_**  
Juela Ndoka** 42:08  
No, quello a engineering, la solo come.

_[immagine]_**  
Tommaso Penta** 42:11  
Ok.  
Sì.

_[immagine]_**  
Juela Ndoka** 42:45  
No, aspetta, cosa hai preso?

_[immagine]_**  
Tommaso Penta** 42:46  
Sì, abbiamo sbagliato, sbagliato.

_[immagine]_**  
Juela Ndoka** 43:05  
OK, fai OK qui.

_[immagine]_**  
Tommaso Penta** 43:41  
Ciao.  
E poi database.

_[immagine]_**  
Juela Ndoka** 43:58  
Fai, fai, OK, poi 1 secondo.

_[immagine]_**  
Tommaso Penta** 44:02  
Va bene?

_[immagine]_**  
Juela Ndoka** 44:03  
Dovrebbe riuscire a farlo lui, a riconoscerlo quello vai su certificates.  
L'hai messo il certificato?

_[immagine]_**  
Tommaso Penta** 44:14  
No.

_[immagine]_**  
Juela Ndoka** 44:16  
Direi che è la stessa se tu in qua se riesci a fare però credo che riesci. OK, prova, trova ora.

_[immagine]_**  
Tommaso Penta** 44:17  
Però c'è, sì.  
Sì, riesco.  
Quindi non devo cambiare il database, lo fa lui.

_[immagine]_**  
Juela Ndoka** 44:28  
O Kay.  
Lo fa lui, io non ho mai cambiato, riesce a farlo lui.

_[immagine]_**  
Tommaso Penta** 44:38  
Prego.

_[immagine]_**  
Juela Ndoka** 44:40  
OK, fine, OK.  
Eccolo perfetto, ora puoi fare la prova e quindi tu, Emanuele, non puoi connetterti, vero? Era locato la tua utenza.

_[immagine]_**  
Tommaso Penta** 48:27  
OK da un'autorized.

_[immagine]_**  
Juela Ndoka** 48:28  
Sì.

_[immagine]_**  
Emanuele Merlo** 48:28  
Ci riprovo.

_[immagine]_**  
Juela Ndoka** 48:30  
No, va bene, condivido io solo Dimmi su col Plant stavi facendo il.

_[immagine]_**  
Francesco Panigo** 48:34  
Adesso deve essere sbloccata.

_[immagine]_**  
Emanuele Merlo** 48:36  
Adesso ci provo, sì, ho perso, ho perso la connessione perché mi è caduta.

_[immagine]_**  
Juela Ndoka** 48:42  
Su dove? Su Curno eri a fare i test prima.

_[immagine]_**  
Emanuele Merlo** 48:45  
Sì.  
Aspetta che devo beccare l'equipment su cui stavo lavorando, che è quello che ho messo in chat.  
Vorrei capire tanto poi perché rimango bloccato.  
Cioè una procedura per capire cos'è che me lo manda in tilt.  
Allora?  
Ero su mappello.

_[immagine]_**  
Juela Ndoka** 49:22  
Appello.  
Equipment configuration.

_[immagine]_**  
Emanuele Merlo** 49:30  
Ti sto arrivando.  
GUGCL 141.

_[immagine]_**  
Juela Ndoka** 49:40  
Vai.

_[immagine]_**  
Emanuele Merlo** 49:41  
Ci suona.

_[immagine]_**  
Juela Ndoka** 49:41  
Automation on the instance c'è questo e infatti non è approvato e to be approved, quindi non riesce AA farlo. OK, ora lo facciamo qua al link.

_[immagine]_**  
Emanuele Merlo** 49:49  
Sì.  
Cos'è che può averlo rotto più che altro?

_[immagine]_**  
Juela Ndoka** 49:58  
L'automation gateway.

_[immagine]_**  
Emanuele Merlo** 50:00  
Sì, cioè nel senso, come mai ci troviamo sto problema? C'è qualcheduno che ci ha messo le.

_[immagine]_**  
Juela Ndoka** 50:03  
E non lo so se stanno facendo qualcosa. Stamattina hanno menzionato che ci sono dei cioè avevano un meeting con DPM per questa cosa, però comunque da quello che ho capito non è stato ancora configurato tutto lato automation gateway nostro.  
Però non so, non so il diciamo il Progress, l'avanzamento de di questo non ho nessuna.

_[immagine]_**  
Emanuele Merlo** 50:24  
OK.  
No, perché secondo me una delle cose che dovremmo chiedere è un coordinamento degli interventi su qua, perché adesso ci sono i sit, c'è il training, c'è qualcheduno che sta a fa delle prove, dei deploy e finisce che non sappiamo cosa è rotto.

_[immagine]_**  
Juela Ndoka** 50:39  
No.

_[immagine]_**  
Emanuele Merlo** 50:41  
Tu o cosa funziona?

_[immagine]_**  
Juela Ndoka** 50:42  
Allora i deploy di solito li faccio io, quindi.

_[immagine]_**  
Emanuele Merlo** 50:45  
Ciao.

_[immagine]_**  
Juela Ndoka** 50:46  
Cioè di solito lo faccio quando ci sono delle quando sono stati fatti degli sviluppi hanno finito e mi cioè mi danno il via di farlo.

_[immagine]_**  
Emanuele Merlo** 50:52  
Certo, certo.

_[immagine]_**  
Juela Ndoka** 50:57  
Pen.

_[immagine]_**  
Emanuele Merlo** 50:58  
Prendi quello verde lì, quello mezzo era quello lì che.

_[immagine]_**  
Juela Ndoka** 51:00  
Sì, questo qui non ricordo più il nome, allora prima verifichiamo il gruppo CE l'ha, vengo dentro, OK?  
Ora lo spartiamo.  
E dovrebbe andare start 5 vai.  
OK, start up.

_[immagine]_**  
Emanuele Merlo** 51:30  
OK, è andato tutto se era quello.

_[immagine]_**  
Juela Ndoka** 51:33  
OK perché automation gateway comunque sullo start dei delle operazioni ma anche su tutte le altre funzionalità e comunque cioè se è attivo, se iniziamo con start è la prima è lo.  
Start scrive solo automation gateway e per qualsiasi motivo automation gateway va giù e quando noi facciamo un completamento se l'automation gateway non è ripreso e non riesce a andare a leggere sul.  
Dag potrebbe essere che abbiamo dei problemi sulla sull'interfaccia del complete lato UI nel senso che non riesce andare a recuperare i miei material nel caso ci che ci sono coproduct anche coproduct.  
Quindi qui questo potrebbe essere un caso in cui noi qua su questa quando apriamo questa schermata abbiamo degli errori del tipo contact system administrator.  
Di solito questa verifica poi si fa, vai nella persistent log e quando ti fallisce l'automation gateway per lettura o scrittura sulla persistent log c'è un errore specifico che si chiama CPM node.  
Che vuol dire? Che è totalmente legato all'automation gateway e vuol dire che non è riuscito a né leggere né scrivere, perché allo start noi andiamo a controllare se il work center su cui stiamo lavorando.  
È collegato a un automation note. Prima di tutto va a leggere se su quell automation note è già startato un'altro ordine, c'è un ordine attivo, se c'è un ordine attivo ti dà quasi lo stesso errore che ti ha dato a te.  
Solo che ti dice in quell'istanza c'è un'altro nodo attivo e ti dà l'identificativo dell'ordine che è attiva.  
OK.

_[immagine]_**  
Emanuele Merlo** 53:32  
Ok, sì.

_[immagine]_**  
Juela Ndoka** 53:35  
Perfetto qua volete fare cioè cosa avete bisogno? Volete finire questo ordine del casting o.

_[immagine]_**  
Paolo Comparoni** 53:43  
Ma volevo vedere se potesse essere interessante per tutti, se potevi praticamente quando dichiari lo quando dichiari diciamo una non conformancy no?

_[immagine]_**  
Juela Ndoka** 53:55  
Sì.

_[immagine]_**  
Paolo Comparoni** 53:56  
OK, quindi c'è di fare un mini riassunto, nel senso che.  
Cioè coi prodotti no. Quindi con ce la puoi fare sia con un consumo consumo che su un output no? Ho capito bene. E poi appunto quando quando uno scrap.

_[immagine]_**  
Juela Ndoka** 54:13  
Sì, certo, sì.

_[immagine]_**  
Paolo Comparoni** 54:20  
Però a quel punto lì si aprono, si apre la non conformancy, no, se è scrap va direttamente come scrap, non c'è più, non c'è più niente da fare.

_[immagine]_**  
Juela Ndoka** 54:26  
Allora si apre la non conformance, nel senso lo trovi sulla pagina delle non conformances con lo Stato scrap, quindi non lo possono far ritornare. Poi diciamo a rilavorare se volete chiudiamo questo ordine nel senso facciamo il consumo, facciamo dichiariamo.

_[immagine]_**  
Paolo Comparoni** 54:36  
OK.  
E.

_[immagine]_**  
Juela Ndoka** 54:44  
Tra lo guardiamo.

_[immagine]_**  
Paolo Comparoni** 54:45  
Sì, e poi anche magari anche lato engineering, lì le failure dov'è che le prende, com'è che vengono associate, OK?

_[immagine]_**  
Juela Ndoka** 54:51  
Certo, certo.  
Questo che cos'era?  
E la 141 OK CL 141, quindi il buffer di questo work center è la 14 g.  
C'è un buffer dell'aria per casting in line.

_[immagine]_**  
Paolo Comparoni** 55:29  
Questo qua è preso perché inizia e ha lo stesso nome, no?

_[immagine]_**  
Juela Ndoka** 55:29  
Come lo come lo so io, io un po lo so perché ho fatto 100.000 volte le prove, però ve lo faccio vedere della hierarchy.

_[immagine]_**  
Paolo Comparoni** 55:37  
Cavallo.

_[immagine]_**  
Juela Ndoka** 55:42  
Allora?  
L'ho l'ho intuito perché è 14 g 15 g, quindi la macchina mia su cui sta lavorando è Google CL 141, quindi il buffer inizia per le non è un standard e non lo prende per scontato perché l'ho detto io.  
Però per mappello è così, per esempio qua abbiamo.  
La 140141142 per esempio sul 19 che noi di solito lavoriamo su gup CL 191 abbiamo la 1911921939495.  
Quindi cioè l'abbiamo costruita, l'hanno costruito perché questo è un naming convention che ci hanno mandato loro, ci hanno mandato il template della del Plant hierarchy, però il 14 g.  
Su 14 g abbiamo 141 e 142, quindi vuol dire che questo queste due macchine, tutti gli ordini che abbiamo su queste due macchine avranno 1 1 pre macchina collegato al.  
All'aria, ed è questo qui.  
Material andiamo a vedere se abbiamo questo materiale.  
OK, non abbiamo allora io sto sbagliando perché quando abbiamo in un ordine, quando siamo in un ordine di casting.  
Prima azione che loro fanno prima di consumare è validare la tool da usare, la mall da usare.  
Quindi lo vado a recuperare.  
OK.  
Questa è la tool, è la tool Definition, la famiglia. Loro lo chiamano la famiglia e l'istanza è la è questa qui, la property value che è l'istanza del tool. Andiamo a metterlo qua.  
Senza spazio.  
OK, validata. Quando vediamo tool sono apparsi anche II bottoni per la dichiarazione dei dei difetti. Ora andiamo a prendere anche la il materiale da consumare da qualche parte l'ho OK qui.  
E questo qui, questi sono nostri.  
Tutto questo container si presumo.

_[immagine]_**  
Paolo Comparoni** 58:53  
Qua se no non ci fosse me lo posso creare. Cos'è un MTU questo? Posso creare un MTU o è complicato?

_[immagine]_**  
Juela Ndoka** 58:59  
Allora?  
Ti dico la procedura, sì, Dimmi, Alessio.

_[immagine]_**  
Alessio Monaco** 59:09  
No, una domanda. Tu prima hai detto Io ho sbagliato, dovevo validare la mall no e sei andata a prenderti il la proprietà del tool. No OK, ma diciamo.

_[immagine]_**  
Juela Ndoka** 59:14  
Sì.  
Esatto.

_[immagine]_**  
Alessio Monaco** 59:26  
Il fatto che solo mettendo validando il tool era possibile abilitare i bottoni lateralmente no.

_[immagine]_**  
Juela Ndoka** 59:34  
Sì.

_[immagine]_**  
Alessio Monaco** 59:35  
OK, ma questa cosa, cioè non è che qualcuno ci dirà perché non mi esce un pop-up che mi dice questo?

_[immagine]_**  
Juela Ndoka** 59:43  
E no, è richiesto questo da loro e se non hanno validato la tool, non farli aprire, cioè.

_[immagine]_**  
Alessio Monaco** 59:49  
Sì, ho capito, però mi immagino magari l'operatore che è la prima volta che lo USA e dice che devo fa?

_[immagine]_**  
Juela Ndoka** 59:58  
E no, però non cioè loro lo sanno che questo è il processo da fare, quindi lo sanno che se non iniziano a validare la tool non possono andare avanti sul processo.

_[immagine]_**  
Alessio Monaco** 1:00:10  
OK.

_[immagine]_**  
Juela Ndoka** 1:00:14  
Cioè hanno chiesto, cioè è stato il business che invece di chiedere per esempio quello che dici tu, un pop-up in cui ti dico guarda prima, ricordati di validare il tool per avere il bottone, hanno richiesto semplicemente che.  
Lo rendiamo, diciamo non.  
Cioè grigio e invece di mandare un pop up in cui li gli diciamo al devi devi validare prima.

_[immagine]_**  
Alessio Monaco** 1:00:44  
OK.

_[immagine]_**  
Paolo Comparoni** 1:00:46  
E l'ha fatto con un interlock, questo o.

_[immagine]_**  
Juela Ndoka** 1:00:52  
L'abilitazione del bottone no, c'è un Flag, la domendix in cui se il molde è validato vai a abilitare la il bottone.

_[immagine]_**  
Paolo Comparoni** 1:00:53  
Sì.  
Poi lo fa, lo fa, OK, OK, Domandics, OK.

_[immagine]_**  
Juela Ndoka** 1:01:06  
Allora ti mi stavi chiedendo come faccio a mandare lo stock available allora questo material tracking unit che vedi qui c'è una naming convention precisa in cui il primo diciamo.

_[immagine]_**  
Paolo Comparoni** 1:01:12  
Yes.

_[immagine]_**  
Juela Ndoka** 1:01:21  
La prima stringa è il materiale da consumare, che è il materiale di cui abbiamo bisogno sull'ordine.  
La seconda è il batch e il code, qui il batch di quel materiale. La terza è il material tracking unit aggregate e handling unit che dobbiamo scansionare sul.  
Sull'operazione e la quarta stringa è il buffer su cui stiamo lavorando. OK, ora per fare questo stock available abbiamo un comando che su tutti sessioni l'abbiamo detto.  
Ma tu non c'ERI giustamente e verso con tester tool.

_[immagine]_**  
Emanuele Merlo** 1:02:07  
Sì, c'ero, l'abbiamo fatto l'altro giorno con lo stock available.

_[immagine]_**  
Juela Ndoka** 1:02:12  
A cena, Paolo.

_[immagine]_**  
Emanuele Merlo** 1:02:14  
Pablo no, yo sí.

_[immagine]_**  
Juela Ndoka** 1:02:15  
No, sì, io lo sto dicendo per favore, magari no, non ho detto Emanuele, ho detto tester tool solo OK allora.

_[immagine]_**  
Emanuele Merlo** 1:02:17  
Cosa ho capito Emanuele, scusa?  
Scusa.

_[immagine]_**  
Juela Ndoka** 1:02:35  
Stock available.  
OK Command nell'APP Brembo c'è un comando che si chiama BRM stock available.  
Il punto OK, quindi destination buffer è il buffer su cui vogliamo mandare lo stock, è questo qui.  
OK il container, cioè di solito tutti questi stock available li manda stop perché quelli che creiamo noi poi quando facciamo il complete e mandiamo le e mandiamo i consumi non è veritiero perché?  
Questo container diciamo che non esiste lato SAP però per far cioè per passare i nostri test per prendere un po' dimestichezza facciamo questo lavoro qui allora mettiamo la data di oggi 26.  
Per 4, 10.

_[immagine]_**  
Paolo Comparoni** 1:03:32  
Ne stai creando uno nuovo?

_[immagine]_**  
Juela Ndoka** 1:03:33  
Sì, una nuova per farti vedere cioè come se non se non trovi lo stock come lo puoi, come puoi fare allora il materiale inaid è il materiale da consumare questo qui.

_[immagine]_**  
Paolo Comparoni** 1:03:36  
OK, sì.

_[immagine]_**  
Juela Ndoka** 1:03:51  
Il batch.  
Questo è finto ovviamente material revision usiamo sempre a è la quantity è la quantità di cui lui ha bisogno e io metto 100 magari è troppo faccio 10 work ordering ID non lo facciamo perché se mettiamo il work ordering ID poi questo container.  
Può essere usato solo su quell'ordine, OK, quindi è un constraint.

_[immagine]_**  
Paolo Comparoni** 1:04:22  
E questo qua vale per tutti i processi, nel senso che tutte le volte che c'ho un buffer mi serve e poi diciamo tutte le caratteristiche giuste le prende poi dal dal template, dal materiale se o devo poi qualche volta devo anche editarlo magari o.

_[immagine]_**  
Juela Ndoka** 1:04:25  
Sì.  
Sì.  
Esatto, esatto.  
No.

_[immagine]_**  
Paolo Comparoni** 1:04:39  
Va bene così, OK?  
Ottimo.

_[immagine]_**  
Juela Ndoka** 1:04:43  
OK, questo qui ora il buffer, facciamo un refresh, dovrebbe vedere anche il mio.  
Se non l'ha visto vuol dire che ho sbagliato.  
Non lo visto, io no lo vedo.

_[immagine]_**  
Fabio Massone** 1:05:00  
È il terzultimo, quello lì, sì, esatto.

_[immagine]_**  
Juela Ndoka** 1:05:01  
Eccolo qui, sì, non vedete? Grazie Fabio ed è finito qua dentro. Quantità 10, ora lo andiamo a consumare.  
OK, perfetto, quindi è sparito anche il bottleneck e quindi questo è quello che abbiamo consumato, abbiamo production finish good a 5 perché ho startato solo 5.

_[immagine]_**  
Paolo Comparoni** 1:05:27  
In questo caso non potevi dire che c'è un difetto nel in qualche pezzo del consumo?

_[immagine]_**  
Juela Ndoka** 1:05:32  
No.  
Ora lo dichiariamo.

_[immagine]_**  
Paolo Comparoni** 1:05:36  
OK.

_[immagine]_**  
Juela Ndoka** 1:05:37  
OK, cioè se voi, se cioè se loro vedono che c'è un difetto sul diciamo, sul materiale, sul componente che stiano che stanno consumando, fanno il.  
Fanno gli immediate scrub.

_[immagine]_**  
Paolo Comparoni** 1:05:55  
OK.

_[immagine]_**  
Juela Ndoka** 1:05:57  
Ora lo sto facendo OK, creato, quindi sì.

_[immagine]_**  
Paolo Comparoni** 1:06:00  
E tutte quelle, tutte quelle felu sono tutte quelle esistenti o sono calibrate per quel per quel.

_[immagine]_**  
Juela Ndoka** 1:06:07  
Scusami perché non l'ho non l'ho specificato allora c'è dovrebbe essere una configurazione credo che in qua non l'abbiamo fatto questa configurazione però le failor sono associate al work center e al materiale da.  
Da dichiarare difettoso diciamo quindi la configurazione deve essere per work center e per materiale o per materiale?  
OK, quindi queste failor li associamo per ora failor.

_[immagine]_**  
Paolo Comparoni** 1:06:34  
OKOK.  
Quindi qua ha fatto uno Scarpe e niente, adesso ha fatto una non conformance su quel workload.

_[immagine]_**  
Juela Ndoka** 1:06:46  
Esatto.  
Esatto, allora qua.  
Noi lo facciamo tramite tester tool, però qua in questo momento vediamo tutte, non c'è una configurazione per material o per Equipment, però in produzione deve essere un material o Equipment.  
OK, loro vedranno solo quelli che appartengono a diciamo al processo di casting in produzione, non vedranno tutta questa lista che vediamo noi.

_[immagine]_**  
Alessio Monaco** 1:07:24  
Ma queste difettosità arrivano sempre da SAP.

_[immagine]_**  
Paolo Comparoni** 1:07:28  
Sono state importate queste.

_[immagine]_**  
Juela Ndoka** 1:07:31  
Dice e le failure causali.

_[immagine]_**  
Alessio Monaco** 1:07:33  
Sì.

_[immagine]_**  
Juela Ndoka** 1:07:35  
No, sono stati mandati da Brembo. Sono gli causali che loro conoscono, cioè che gli operatori conoscono. Sanno che se è 1 1, che ne so, è un è un boh, non lo sto. Prendo un esempio, non mi ricordo neanche.  
Cioè loro quando vedono 1A1A1 riescono a capire che è un'ammaccatura per esempio, quindi loro vedranno solo quello del loro processo e quando vanno AA dichiarare lo cercano lì nella nostra gallery.  
Cioè cercano a uno e assegnano quello.  
Non c'ho l'ho visto, no.  
A 0 0.  
OK.

_[immagine]_**  
Paolo Comparoni** 1:08:34  
OK, quindi praticamente adesso c'è un materiale che consumiamo che comunque cioè un pezzo, quanti pezzi è fatto di un pezzo che non è andato bene e cosa è stato messo su un contenitore apposta in una zona apposta?

_[immagine]_**  
Juela Ndoka** 1:08:34  
A lo social.  
Un pezzo ora te lo faccio vedere che siamo saltati.  
OK.  
Sì nella non conformance qua ha creato ha creato questo ha creato la non conformance che ha questo diciamo questo identifier di questo contenitore è del tipo material item perché sul materiale che stiamo consumando su material component.  
È lo Stato scrap, quindi è totalmente, cioè non può tornare più dentro, diciamo dentro il processo. Il difetto è quello che ho assegnato io, che ho assegnato a caso. Ovviamente loro non assegnano a caso.  
È il material Tracking Unit che abbiamo scappato, ha fatto un split perché ho fatto solo solo un pezzo.

_[immagine]_**  
Paolo Comparoni** 1:09:32  
OK.  
Quindi è messo, è messo praticamente nell'ordine, è linkato nell'ordine OKE, poi è messo, è stata creata un'etichetta, è stata messo da qualche parte, com'è che.

_[immagine]_**  
Juela Ndoka** 1:09:50  
Sì, quel contenitore avrà un'etichetta che è un difetto, se non sbaglio.

_[immagine]_**  
Paolo Comparoni** 1:09:50  
Cosa?  
OK, magari poi io qua mi faccio, guardo.

_[immagine]_**  
Juela Ndoka** 1:09:58  
Es un scra, es un scra.  
Cioè perché anche lato sta per questo noi abbiamo mandato un good movement.

_[immagine]_**  
Paolo Comparoni** 1:10:09  
OKOKE quindi questo qua diciamo invece che avevamo provato a fare dei test invece sul sulla quarantena no quella cosa.

_[immagine]_**  
Juela Ndoka** 1:10:10  
Che.  
Allora sulla quarantena io non so come, cioè qual è lo sviluppo di questoperomagarichiediamoaiacopoperchedurantel'u.at Panzeri ci aveva detto che su cioè nel processo di fonderia non ci sono.  
Quarantene.

_[immagine]_**  
Paolo Comparoni** 1:10:38  
OK.

_[immagine]_**  
Juela Ndoka** 1:10:38  
Quindi non vorrei che cioè prendiamo cioè chiediamo a Jacopo su questa informazione, quindi non andiamo lì nel training su casting, cioè li facciamo vedere a una quarantena e cioè sbagliamo perché loro non devono fare quarantena.

_[immagine]_**  
Paolo Comparoni** 1:10:50  
Però scusa in generale, cioè in generale no, se per un per un trading quality che vada bene a tutti e due impianti non dovrai scegliere un casting, dovrai scegliere un'altra operazione, magari un assembly di.

_[immagine]_**  
Juela Ndoka** 1:11:04  
Esatto, sì che non è.

_[immagine]_**  
Paolo Comparoni** 1:11:05  
Un assembly di curno, magari.

_[immagine]_**  
Juela Ndoka** 1:11:07  
Sì.  
Sì che non ha questo costrain, puoi fare sia scrap che quarantena, quindi vai tranquillo, cioè non stai dicendo un qualche cosa che loro non fanno.

_[immagine]_**  
Paolo Comparoni** 1:11:14  
OK.  
E quindi praticamente per il per il per la produzione per consumo è così l'unica cosa che forse quando è quarantena poi ti serve un contro messaggio da SAP per riportarlo come good come consumato.

_[immagine]_**  
Juela Ndoka** 1:11:30  
Allora la parte SAP io non lo conosco bene, però ti posso, cioè quelli di qualità quando c'è un quando c'è una quarantena e loro lo vogliono far tornare nel diciamo.  
Trovo una quarantena, questo per esempio non sto più là aperto, ma direi che va bene loro, cioè quelli che sono diciamo i quality Expert che hanno il diritto di fare questo vanno qui.  
Vanno qui e cambiano lo Stato e noi anche al cambiamento dello Stato della non conformance. Comunque mandiamo un good Movement al a SAP, quindi li facciamo sapere che questo da quarantena deve andare, che ne so io, in Brembo reward.  
E presumo che lato staff poi c'è un movimento che lo sposta da cioè da quarantena al contenitore che deve andare di nuovo nel in linea per essere di nuovo lavorato.

_[immagine]_**  
Paolo Comparoni** 1:12:32  
Sì, magari viene creato invece perché noi l'altra volta abbiamo provato a fare un re to close and re to work, no? Però in quel caso lì, cioè uno si aspetterebbe che poi magari non so che i good, i good erano qua.  
Adesso ritornano 5 no oppure oppure che uno poi possa possa ridecchiarare il consumo sullo stesso contenitore di prima.

_[immagine]_**  
Juela Ndoka** 1:12:58  
Esatto esatto cioè cioè se il se il SAP se cioè diciamo la movimentazione verso SAP funziona bene io dovrei trovare nel buffer 1 1 cioè la stessa quantità con cui cioè che ho esatto che poi sarà da consumare.

_[immagine]_**  
Paolo Comparoni** 1:13:12  
E poi la bisca hanno.

_[immagine]_**  
Juela Ndoka** 1:13:17  
Perché non si autoconsuma, diciamo?

_[immagine]_**  
Paolo Comparoni** 1:13:17  
Ok, ma dici che nel training c'è fare questo è un po complicato?

_[immagine]_**  
Juela Ndoka** 1:13:22  
Allora ti direi che noi non andiamo in nel dettaglio per la parte SAP visto che non abbiamo tutte le competenze così per non dire cioè cavolate perché cioè io la parte SAP non la conosco proprio, ti sto dicendo solo quelli che sono.  
Le cose che sono state dette durante gli OAT.

_[immagine]_**  
Paolo Comparoni** 1:13:41  
Sì, no, ma è sensato quello che dire, quello che mi aspetto anch'io sicuramente.

_[immagine]_**  
Juela Ndoka** 1:13:45  
OK, però questo è quello che fanno loro. Loro arrivano qui, cambiano lo Stato e noi mandiamo il Good Movement verso SAP. Poi è SAP che deve fare tutte le movimentazioni che noi troviamo, cioè diciamo tutti i container e quantità lineate.

_[immagine]_**  
Paolo Comparoni** 1:13:54  
OKOK.  
OK se confermo scrap cioè quarantena confermo scrap cioè dovrebbe comunque andare scappato però sempre con dei dei movement di SAP probabilmente cioè non conformarsi praticamente senza.

_[immagine]_**  
Juela Ndoka** 1:14:16  
Sì.  
Allora le loro magazine diciamo non so se neanche la parola giusta magazzino, però io ho visto che su hanno proprio precisamente separate la GR scrap, la GR rework.

_[immagine]_**  
Paolo Comparoni** 1:14:21  
La sulla sentencing.

_[immagine]_**  
Juela Ndoka** 1:14:33  
Quindi sì, c'è una movimentazione che va beh, cioè che è diviso se scrubs è da rilavorare.

_[immagine]_**  
Paolo Comparoni** 1:14:42  
Ok, magari faccio così, magari adesso provo un po' e poi lunedì chiedo conferma a Jacopo per vedere.

_[immagine]_**  
Juela Ndoka** 1:14:45  
Sì.  
Sì, sulla sulla quarantena specialmente ora scrivo anch'io una nota e li chiedo, magari te lo scrivo perché durante l'u.at, cioè ero lì presente quando il business ha detto che in fonderia non si manda in quarantena.

_[immagine]_**  
Paolo Comparoni** 1:15:04  
Sì, però anche in un'altro processo, cioè in generale adesso lo provo, cioè magari forse lo forse qualcuno di quelle action per cambi di Stato della non conformarsi, magari forse fa l'effetto.  
Diciamo finale direttamente sul Wordcoder, magari sì o forse serve SAP e poi serve per forza che a mano poi vengano ridichiarate le cose.

_[immagine]_**  
Juela Ndoka** 1:15:32  
Sì, cioè se loro.

_[immagine]_**  
Paolo Comparoni** 1:15:32  
Cioè quella cosa lì bisogna cioè dal lato pratico praticamente come risolvere una quarantena in modo capisci sia sia di input che di output in modo coerente al cioè sapere quali sono esattamente le azioni no?

_[immagine]_**  
Juela Ndoka** 1:15:35  
Sì.  
Sì, noi facciamo quello che ti ho detto, noi facciamo, diciamo lo cambio stato, mandiamo la good Movement component che è questa qui in cui gli diciamo che guarda, per questo materiale abbiamo fatto un Direct scrap, è questo l'handling unit che mandiamo noi loro perché è quello che abbiamo creato.  
E quindi poi loro fanno tutti i movimentazioni che devono fare, cioè?

_[immagine]_**  
Paolo Comparoni** 1:16:11  
E poi ti ritorna lì e lo ridichiari OO poi magari farete poi qualche customizzazione che va direttamente che ritorna direttamente nel nell'ordine al punto giusto OKOK grazie 1000.

_[immagine]_**  
Juela Ndoka** 1:16:15  
Sì.  
Sì.  
Prego, Alessio.

_[immagine]_**  
Alessio Monaco** 1:16:30  
Una domanda, se puoi tornare sulla pagina dove hai fatto lo scrap?

_[immagine]_**  
Juela Ndoka** 1:16:35  
Sì.  
Scusa qui.

_[immagine]_**  
Alessio Monaco** 1:16:43  
Sì, è perfetto qua, perfetto OK, tu avevi prodotto 5 pezzi, hai simulato che l'operatore se n'è accorto che uno ha una difettosità, quindi la quantità ti è scesa da quattro a 5.

_[immagine]_**  
Juela Ndoka** 1:16:49  
Esatto.  
Sì.  
Sì.

_[immagine]_**  
Alessio Monaco** 1:16:57  
OK, però perché prima domanda, perché ti dice production finish good sempre 5 pezzi in alto e non quattro?

_[immagine]_**  
Juela Ndoka** 1:17:04  
È sbagliato. È sbagliato perché abbiamo cambiato questa Reading function per migliorare per la performance, però l'abbiamo rotto, quindi non l'ha calcolato, non è non ha refreshato. Quindi ora ora che ho refreshato la pagina la diciamo.

_[immagine]_**  
Alessio Monaco** 1:17:15  
OK.

_[immagine]_**  
Juela Ndoka** 1:17:19  
Se ne rende conto che deve fare quattro?

_[immagine]_**  
Alessio Monaco** 1:17:23  
OK, primo e lo scrap conti dovrebbe essere uno e non zero.

_[immagine]_**  
Juela Ndoka** 1:17:29  
No, lo scrap quantity in alto. Sì, questo del prodotto finale. Noi ora abbiamo dichiarato un scrap sul materiale che stiamo per consumando perché abbiamo visto che non andava bene. Non lo so. Mentre lo consumiamo l'abbiamo messo in quel contenitore che sta lì da parte.

_[immagine]_**  
Alessio Monaco** 1:17:31  
In alto, in alto, in alto.  
OK.  
OK.  
Ok quindi sulla complete quando se facessero la complete la sarebbe uno.

_[immagine]_**  
Juela Ndoka** 1:17:48  
Invece.  
Da qui, se noi ora vogliamo dichiarare un difetto su queste quattro che abbiamo assemblato, che stiamo per produrre, diciamo.  
Qui vedi che è questo, cioè sul prodotto finito già l'abbiamo sistemato, non te lo fa fare la candidate che sarebbe la quarantena, quindi è già preselezionato, quindi va direttamente in scrap questo.  
Quindi 6.  
OK.  
Questo è sceso a tre, perché ora qui?

_[immagine]_**  
Alessio Monaco** 1:18:28  
OK.

_[immagine]_**  
Juela Ndoka** 1:18:32  
Cioè non l'ha scritto sbagliato, cioè non funziona più questa reading function, basta.  
Era questo, giusto?

_[immagine]_**  
Alessio Monaco** 1:18:52  
Sì.

_[immagine]_**  
Juela Ndoka** 1:18:53  
OK, scrap quantity ora sul finito tre OKE nella non conformance l'ho chiusa.

_[immagine]_**  
Alessio Monaco** 1:18:57  
Sì.

_[immagine]_**  
Juela Ndoka** 1:19:10  
Ora abbiamo la nostra non conformance, però ora non è più del tipo material item perché non è per il componente, è a livello di Final material, quindi è per operazione. Se vai qui hai.

_[immagine]_**  
Alessio Monaco** 1:19:19  
OK.

_[immagine]_**  
Juela Ndoka** 1:19:25  
Work order hai il material and ID che è diverso che il materiale finito è quello che devo produrre Final material OK.

_[immagine]_**  
Alessio Monaco** 1:19:34  
In linea.  
Si.

_[immagine]_**  
Juela Ndoka** 1:19:38  
E difetto è quello che ho associato io a caso, va bene, poi qua facciamo un secondo mode che più si capisce meglio, quindi il materiale è diverso.  
Il primo, se andiamo nella non-conformance di prima era sul materiale, quello che stiamo consumando sulla BB ora questo l'abbiamo aperto sul materiale finito, quindi c'è una differenza tra loro due e qua ora a livello di ordine.

_[immagine]_**  
Alessio Monaco** 1:19:52  
Sì.  
OK, ho capito cosa mi stai dicendo, se torni sulla schermata della di dove hai fatto lo scrap per capire un attimo una cosa io.

_[immagine]_**  
Juela Ndoka** 1:20:19  
Sì.

_[immagine]_**  
Alessio Monaco** 1:20:20  
OK, perfetto, questo esattamente. Noi avevamo fatto 5 pezzi, poi ne abbiamo fatto una difettosità sul materiale e poi abbiamo fatto una difettosità sulla work, sulla work operation OKOK. Quindi io vedo.

_[immagine]_**  
Juela Ndoka** 1:20:21  
Quindi.  
Sì.  
Sì.  
Esatto.

_[immagine]_**  
Alessio Monaco** 1:20:37  
Guardando così io vedo tre in alto production finish good, poi vedo uno step di conti sulla work operation che è un pezzo e siamo a quattro e il quinto in realtà sappiamo che abbiamo fatto sotto la.

_[immagine]_**  
Juela Ndoka** 1:20:45  
Sì.  
Esatto.

_[immagine]_**  
Alessio Monaco** 1:20:53  
Lo scrap sul materiale no.

_[immagine]_**  
Juela Ndoka** 1:20:55  
Che stiamo consumando. Che vuol dire? Che per quello che abbiamo consumato, perché uno l'abbiamo tolto perché non va bene. E quel tre vuol dire che per quello che tu mi hai consumato puoi fare solo tre pezzi buoni, sì.

_[immagine]_**  
Alessio Monaco** 1:21:09  
OK, ma OK, ho fatto tre pezzi buoni, ma dov'è che capisco che io nel frattempo ho usato 5 elementi del buffer iniziale?

_[immagine]_**  
Juela Ndoka** 1:21:18  
Allora?  
Ora questo, cioè al volo, diciamo.  
Non lo puoi capire perché quando fai il.  
Quando fai lo scrap io ti aggiorno anche perché questo sarebbe il material tracking unit che ho che ho consumato quindi ti aggiorna anche questo qui perché tu vorresti che da qualche parte nella nella pagina vedo che ho fatto anche una non conformance per questo.

_[immagine]_**  
Alessio Monaco** 1:21:39  
Sì.  
Sì.  
No, ti faccio un esempio, io sono mi metto sempre dalla parte dell'utente, no che mi io vengo qua, no così questo io ho visto l'interfaccia che loro hanno AX sulla linea ed è molto molto basica. No, io mi immagino la scena.

_[immagine]_**  
Juela Ndoka** 1:21:50  
Dimmi.  
Certo.

_[immagine]_**  
Alessio Monaco** 1:22:03  
Facciamo una difettosità, dici io per verificare 10 vedo il 10 lì fatte 3 1 scrap 4 3+1 fa quattro come glielo dico che in realtà ne sono 5?  
Cioè lui mi dirà, io come faccio a vedere che sono 5, che ne ho fatte 5 e ne restano altre 5?  
Ipotizzo no. Cioè metti caso che tu finisci il turno, hai fatto 10 pezzi, di questi 10 pezzi hai fatti 5, 3 fatti uno a uno l'hai finito, uno è andato come entra uno nuovo al secondo turno e si trova questa questo davanti.

_[immagine]_**  
Juela Ndoka** 1:22:31  
Allora?

_[immagine]_**  
Alessio Monaco** 1:22:37  
Come fa a capire che sono 5?

_[immagine]_**  
Juela Ndoka** 1:22:37  
Allora?  
Sì, perché loro sanno che il contenitore, per esempio, che hanno consumato è da 5, OK, hanno fatto anche il contenitore con lo scrap che l'hanno stampato e ce l'hanno lì con la stampa che ho scrapato.  
Ok.

_[immagine]_**  
Alessio Monaco** 1:22:55  
Quindi loro hanno una stampa su ogni postazione di lavoro?

_[immagine]_**  
Juela Ndoka** 1:22:59  
Sì, loro, loro stampano, hanno il print label di quello che dichiarano del scrap o del complete.

_[immagine]_**  
Alessio Monaco** 1:23:11  
OK.

_[immagine]_**  
Juela Ndoka** 1:23:12  
Fanno la print.

_[immagine]_**  
Alessio Monaco** 1:23:16  
No, cioè io sto io, io sto, io no, ho capito, io sto entrando lì, mi sono posto di lavoro.

_[immagine]_**  
Juela Ndoka** 1:23:16  
Cioè print history.

_[immagine]_**  
Alessio Monaco** 1:23:24  
Dove vedo che ne ha fatti 5, quello prima di me?

_[immagine]_**  
Juela Ndoka** 1:23:28  
No, cioè non hai non hai, cioè hai consumato 5, però lui non ha mai prodotto 5.

_[immagine]_**  
Alessio Monaco** 1:23:35  
Ha fatto tre buoni, uno scrap sull'operazione, uno scrap sul materiale, ma alla fine il buff.

_[immagine]_**  
Juela Ndoka** 1:23:39  
Allora abbiamo consumato, però non abbiamo ancora dichiarato i buoni.

_[immagine]_**  
Alessio Monaco** 1:23:45  
Ok, ma noi stiamo lavorando sul materiale di ingresso, giusto sul pre macchine abbiamo lavorato fino adesso.

_[immagine]_**  
Juela Ndoka** 1:23:45  
Ora, per ora abbiamo.  
Sì, non abbiamo ancora fatto la cioè il buono, non abbiamo ancora dichiarato questo calcolo ti fa vedere che.

_[immagine]_**  
Alessio Monaco** 1:23:52  
Corretto.

_[immagine]_**  
Juela Ndoka** 1:24:00  
Tu per quello che hai consumato ne puoi fare tre. Basta. Non abbiamo ancora, non siamo passato ancora al non abbiamo ancora dichiarato il contenitore, diciamo completato.

_[immagine]_**  
Alessio Monaco** 1:24:10  
OK.

_[immagine]_**  
Juela Ndoka** 1:24:13  
OK, lo facciamo al complete quello.  
Io faccio compito ora.  
Questo Rintable OK con il container.  
Quindi ora se io faccio sì a questo quattro lui va a fare se il materiale è di tracciabilità soft qui.  
Che è il nostro caso, lui dovrebbe andare, c'è un automatismo, c'è una logica automatica che va a controllare se.  
Io per la quantità che voglio completare, in questo caso quattro, non riesco a completarli con quello che ho consumato, va nel buffer a controllare se ci sono.  
Altri contenitori che mi possono soddisfare la mia quantità che voglio completare e li consumo. Ora ve lo faccio vedere, lo so che era un gioco di parole.  
Complete io posso fare tre ma voglio completare quattro e il sistema dovrebbe permettermi non mi ha permesso ottimo perché non è dovrebbe andare nel buffer e questo è sbagliato, questo dai.  
E subito da indagare, perché lui dovrebbe andare nel mio buffer qui?  
14 giga.

_[immagine]_**  
Alessio Monaco** 1:25:37  
Quello che tu hai creato all'inizio avevi che avevi 10 pezzi.

_[immagine]_**  
Juela Ndoka** 1:25:41  
Esatto, ma anche anche se il mio container fosse finito, anche se il mio container fosse finito qua, io ne ho altre quantità che posso consumare, ne ho questo che è 42, ne ho quest'altro.

_[immagine]_**  
Alessio Monaco** 1:25:46  
Sì.

_[immagine]_**  
Juela Ndoka** 1:25:57  
Che ne ha 10, 18, quindi lui deve arrivare qua dentro, deve poter dirmi perché ti propone un pop-up che ti dice ho trovato questo container, lo posso consumare tu lo consumi e lui ti permette completare quei qua.  
Invece a me ora non me l'ho fatto ora poi dopo io in background andrò a debugare cosa è successo completo i miei, i miei tre, quello che posso fare complete.  
OK, vedi che ora ho good quantity a.  
Ho completato i miei tre, è passato qui, OK?

_[immagine]_**  
Alessio Monaco** 1:26:45  
Sì, no.

_[immagine]_**  
Juela Ndoka** 1:26:49  
E questa good quantity, cioè?  
Mi produce.  
Mi produce dei messaggi, mi produce la good receipt a livello di ordine in cui mi dice che.

_[immagine]_**  
Alessio Monaco** 1:27:01  
Sì.  
Sì.

_[immagine]_**  
Juela Ndoka** 1:27:08  
Hai creato questo contenitore qui con questo ID, questo endling unit in cui mi hai messo tre good.

_[immagine]_**  
Alessio Monaco** 1:27:16  
Sì.

_[immagine]_**  
Juela Ndoka** 1:27:16  
Cioè vedi quanti tre sulla macchina 141 per questo materiale è l'original batch OKA livello di operazione mi manda anche me l'ha già mandato prima però non abbiamo controllato.

_[immagine]_**  
Alessio Monaco** 1:27:20  
Sì.  
Sì.

_[immagine]_**  
Juela Ndoka** 1:27:33  
Mi manda la Woody shoe per quello, per quei tre buoni.  
OK.  
Questo box qui.  
No, questa era no, questo era dello scrub. Questo passaggio mi sono dimenticata di dirvelo. Quando io faccio lo scrub del materiale da consumare mando verso SAP.  
Tranne quel good movement che ti mando per farti capire che ho creato una non conformance. Ti mando anche una good issue per quel per quel scrap. OK, così lo tolgono dal diciamo dal consumo.  
Ok.

_[immagine]_**  
Alessio Monaco** 1:28:17  
Bene.

_[immagine]_**  
Juela Ndoka** 1:28:18  
E ti manda anche una production confirmation dello scrap, tutti questi vanno a SAP, quindi SAP lo sa.  
Che noi abbiamo fatto un abbiamo fatto dei different declaration, cioè lo manda il good movement, lo mandiamo a EWM.  
OKEWM fa quella lavorazione che ha chiesto prima Paolo, però, cioè alcune conferme li mandiamo anche verso SAP, così loro allineano tutte le quantità.  
Di del prodotto diciamo completato e i vari different declaration che sono stati fatti, questi erano per i nostri scrub, invece questo è per il nostro completamento.

_[immagine]_**  
Alessio Monaco** 1:29:06  
Sì.

_[immagine]_**  
Juela Ndoka** 1:29:07  
OK.  
Quindi good abbiamo fatti questi qui.  
E tre in questo caso, perché per quel diciamo per completare quei tre pezzi noi abbiamo consumato 3DBB002X7, questo è la goodishu che è il consumo invece la production.  
Confirmation.  
È questa qui.  
Produce container e loro qui sul print history.  
Ciao Ciao.  
Allora su Print History è uscito questa stampa.  
Di tre.  
In Q è il contenitore.  
Quindi c'è questa etichetta che mettono sopra il contenitore tre pezzi buoni per quel batch ID con quel handling unit.

_[immagine]_**  
Annalisa Casciaro** 1:30:23  
Scusa Juela, prima hai fatto la prova con quattro no? E ti ha dato interlocking, giusto? Invece non l'avrebbe dovuto fare, sembra.

_[immagine]_**  
Juela Ndoka** 1:30:24  
Dimmi.  
Sì.  
Avrebbe dovuto consumare.

_[immagine]_**  
Annalisa Casciaro** 1:30:34  
Vai pure.

_[immagine]_**  
Juela Ndoka** 1:30:35  
Avrebbe dovuto consumare, cioè ora vado a cercare i componenti, cioè i materiali, però vedo un soft, vedo un normal part avrebbe dovuto consumare.

_[immagine]_**  
Annalisa Casciaro** 1:30:45  
Sembrerebbe lo stesso problema che abbiamo noi nel complete in JJ, nel senso che abbiamo un equipment che fa parte di un gruppo, quindi sembrerebbe la stessa situazione. Adesso credo che Tommaso sia collegato su gava, se vogliamo vederlo su gava.

_[immagine]_**  
Juela Ndoka** 1:30:49  
Sì.  
Sì.

_[immagine]_**  
Annalisa Casciaro** 1:31:02  
Magari trovato da noi, riuscite poi a metterlo a posto qua per dire, sembra proprio identico il problema.  
Che dite lo vediamo su gava?  
Mi sentite?

_[immagine]_**  
Juela Ndoka** 1:31:15  
Allora sì, ti sento, ti sento, stavo pensando.

_[immagine]_**  
Annalisa Casciaro** 1:31:18  
Scusami.

_[immagine]_**  
Juela Ndoka** 1:31:22  
Stavo pensando che su gavai il problema è che non sembra che rimane appeso la work center invece che la l'area giusto.

_[immagine]_**  
Annalisa Casciaro** 1:31:33  
Sì, tiene conto del World Center, non di tutto il gruppetto.

_[immagine]_**  
Juela Ndoka** 1:31:39  
OK.  
Nel mentre.  
Tommaso, Condividi che io prendo i miei qui per quello che serve a me.

_[immagine]_**  
Tommaso Penta** 1:31:45  
Mhm.

_[immagine]_**  
Juela Ndoka** 1:31:52  
Non so Alessia, avevi qualche altra domanda per chiudere tutto il giro o Paolo su questo?

_[immagine]_**  
Tommaso Penta** 1:31:58  
Io ho tolto la condivisione, se voleva.

_[immagine]_**  
Juela Ndoka** 1:32:01  
Va bene, intanto spiego la voce, sennò altrimenti te lo riprendo.

_[immagine]_**  
Alessio Monaco** 1:32:07  
No, beh la io l'unica domanda, ma è domanda così di processo, sapete rispondere, ma noi come?

_[immagine]_**  
Juela Ndoka** 1:32:14  
No, cioè chiedi, cioè anche se non cioè cerco di trovare le parole giuste se lo so di farlo.

_[immagine]_**  
Alessio Monaco** 1:32:16  
OK.  
No, ma in generale no. Nel senso, io mi stavo domandando, nel momento in cui noi facciamo queste print label, no, queste print che poi verranno affisse ai relativi contenitori, immagini, sai?

_[immagine]_**  
Juela Ndoka** 1:32:30  
Sì.

_[immagine]_**  
Alessio Monaco** 1:32:33  
Contenitore di scrap, il contenitore di buoni e tutto OK, ma diciamo noi come MES non controlliamo, non abbiamo un feedback di ritorno che ciò venga fatto, giusto?

_[immagine]_**  
Juela Ndoka** 1:32:34  
Sì.  
Cioè lato, diciamo lato connect mom.

_[immagine]_**  
Alessio Monaco** 1:32:51  
Se mi spiego, noi abbiamo fatto, abbiamo fatto no in generale, cioè io oggi ho fatto uno scrap quindi ho uno scarto stampo una la tua campo avranno 111 stampante che stamperà un'etichetta questa etichetta verrà posta sopra un contenitore.

_[immagine]_**  
Juela Ndoka** 1:32:55  
Sì.  
Sì.  
Sì.

_[immagine]_**  
Alessio Monaco** 1:33:06  
Perfetto. Ma noi oggi non abbiamo modo di sapere che lo scrap realmente viene preso e viene messo nel contenitore degli scrap e non in quello dei buoni. Corretto? Non facciamo un controllo di questo genere noi come mom.

_[immagine]_**  
Juela Ndoka** 1:33:23  
E no, noi, cioè allora, per quanto ne so io, noi andiamo a controllare se abbiamo mandato il messaggio, se abbiamo mandato la presa template, cioè solo queste qui.

_[immagine]_**  
Alessio Monaco** 1:33:30  
No, mi è chiaro, no, ho capito, ma fisicamente, fisicamente, chi garantisce che l'operatore dei no?

_[immagine]_**  
Paolo Comparoni** 1:33:36  
Ma perché scusa, ma perché poi nel processo dopo poi quell'etichetta la scannerizzi?

_[immagine]_**  
Juela Ndoka** 1:33:40  
Sì, gli mancheranno, cioè esatto.

_[immagine]_**  
Paolo Comparoni** 1:33:44  
Cioè nel processo dopo quello di quello che hai prodotto diventa un consumo e a quel punto lì lo scanner se è skep non te lo accetta, no?

_[immagine]_**  
Alessio Monaco** 1:33:44  
Non ho capito.

_[immagine]_**  
Juela Ndoka** 1:33:48  
Esatto.

_[immagine]_**  
Alessio Monaco** 1:33:48  
Sì.

_[immagine]_**  
Juela Ndoka** 1:33:53  
Esattamente.

_[immagine]_**  
Alessio Monaco** 1:33:54  
No, ho capito, ma chi garantisce che il materiale che io ho detto che è scrap non finisce nel cassone dei buoni e il viceversa un pezzo buono finisce nel cassone di scrap?

_[immagine]_**  
Paolo Comparoni** 1:34:05  
È l'etichetta, è l'etichetta.

_[immagine]_**  
Alessio Monaco** 1:34:07  
Sì, ma l'etichetta?

_[immagine]_**  
Juela Ndoka** 1:34:08  
E l'etichetta e poi il controllo qualità, cioè? Cioè c'è un controllo qualità intendo che deve prendere, diciamo il controllo su questo.

_[immagine]_**  
Alessio Monaco** 1:34:20  
Quindi noi, tra virgolette, non abbiamo un'automazione che controlla il pezzo.

_[immagine]_**  
Juela Ndoka** 1:34:22  
Però ti faccio allora per la qualità, se vanno veramente a diciamo a analizzare tutto quello che è stato dichiarato come non conformance io non te lo so dire, però per esempio ti dico che già nel CAT.

_[immagine]_**  
Alessio Monaco** 1:34:37  
Sì.

_[immagine]_**  
Juela Ndoka** 1:34:38  
Tu mi hai prodotto quei tre pezzi.

_[immagine]_**  
Alessio Monaco** 1:34:41  
Sì.

_[immagine]_**  
Juela Ndoka** 1:34:41  
Sap me li, cioè ha fatto la movimentazione e li trova quei tre pezzi nell'altra nel post macchina che sarà il buffer di cutting, cioè se lui cerca di scansionarli però non li vede lì.

_[immagine]_**  
Alessio Monaco** 1:34:52  
Sì.

_[immagine]_**  
Juela Ndoka** 1:34:58  
Cioè capirà che qualcosa è qualcosa è perso nel mentre perché io quel material final material che ho prodotto su casting per quel specifico container io lo devo consumare nel cutting, OK?

_[immagine]_**  
Alessio Monaco** 1:35:15  
Sì, nel senso che mi stai dicendo noi non abbiamo, non facciamo come messo un controllo di scrap e di pezzi buoni, ma il controllo è automatico, nel senso che a valle della linea che ha prodotto questo scrap o questo pezzo buono.  
Chi li userà se ne accorgerà se hanno sbagliato, questo è il senso del discorso.

_[immagine]_**  
Juela Ndoka** 1:35:41  
Esatto, cioè almeno Questo è quanto ne so io, cioè mettiamola così, magari c'è il lato MES, sono sicura che non c'è un controllo del genere.

_[immagine]_**  
Alessio Monaco** 1:35:49  
No, ma io ero, ero, ero l'altro maestro per capire perché ti ripeto, in altri processi si fanno delle estemporanee automatiche per verificare che il prodotto buono o difettoso non sia rimesso in linea.

_[immagine]_**  
Juela Ndoka** 1:36:00  
Mi aspetto mi aspetto che qualcuno al magazzino cioè alza la mano che io devo fare questa movimentazione ma non c'è, cioè dov'è questo contenitore? Perché lo devo spostare da GU CL 141 che nel buffer che era nel.  
In quello 141 lo devo spostare su cutting che sarà 1GMTOB qualcosa che ne so di solito è GMTOB01M quindi io lo devo avere pronto lì per essere consumato quindi?  
Mi aspetterei, loro hanno anche la hanno anche la material call, quindi se loro lo devono chiamare il materiale.

_[immagine]_**  
Alessio Monaco** 1:36:32  
OK.

_[immagine]_**  
Juela Ndoka** 1:36:41  
Quindi devono chiamare la logistica mi serve questo materiale per essere consumato quindi qualcuno lo devo mandare? Quindi tutti questi diciamo queste chiamate credo che la tua logistica qualità vengano controllate in qualche maniera.  
Piera.  
Non so se.

_[immagine]_**  
Alessio Monaco** 1:37:01  
No, ho capito, non abbiamo un processo automatizzato di controllo di queste cose, cioè noi ci affidiamo a all'operatore che la tua linea faccia bene il suo lavoro, perché OK.

_[immagine]_**  
Juela Ndoka** 1:37:01  
Cioè.  
Sì, altrimenti ci saranno problemi in magazzino, cioè da una premacchina all'altra.

_[immagine]_**  
Alessio Monaco** 1:37:15  
Sì, e non ci hanno richiesto di effettuare controlli automatici su sulle difettosità e sulle e sui prodotti bonifichi. Questo è il senso. Ultima domanda, cioè la produzione non ha chiesto.  
Di implementare dei controlli automatici sul prodotto finito delle varie linee? No, perché ho detto il cutting piuttosto che ma alla fine tutto si traduce in stampo d'etichetta. Un operatore prende l'etichetta, la mette su un cassone, prende i pezzi e li mette nel cassone.

_[immagine]_**  
Juela Ndoka** 1:37:44  
Sì.  
Sì.

_[immagine]_**  
Alessio Monaco** 1:37:49  
Ma non c'è nessun controllo alla Domes che il pezzo messo nel cassone sia quello corretto.

_[immagine]_**  
Juela Ndoka** 1:37:54  
Il mio controllo e ce l'ho nel buffer questo no allora te lo vado a chiamare, cioè faccio la material call e qualcuno me lo deve mandare poi cioè cosa sia successo nel mentre se noi abbiamo prodotto tutti i messaggi tutti.

_[immagine]_**  
Alessio Monaco** 1:37:59  
OK.  
Sì, OK, OK, OK.

_[immagine]_**  
Juela Ndoka** 1:38:10  
Tutte le etichette giuste, noi cioè diciamo rimandiamo la colpa, cioè puntiamo il dito da qualche altra.

_[immagine]_**  
Alessio Monaco** 1:38:17  
No, chiaro, chiaro, ma era era non è un requisito di business, non ci avranno richiesto perché sennò ce lo richiedevano di fare dei controlli automatici su sui sui pezzi prodotti.

_[immagine]_**  
Juela Ndoka** 1:38:25  
Penso, penso.

_[immagine]_**  
Paolo Comparoni** 1:38:26  
Comunque secondo me secondo me più che un cassone è il è un pacchetto che prende quel pezzo che te perché se poi tu lo rifai no dice consuma lui che ha un'altra etichetta no quindi per ogni volta.  
Che tu che tu dichiari comunque un difetto no, di una certa quantità, allora poi lui rifà, rifà un'altra, rifà un'altra, un'altro pacchetto, un'altra etichetta no e quindi poi secondo me ti trovi.  
Anche i singoli pezzi te li trovi tutti etichettati e quelli lì non sono non sono più buoni, no? Cioè il concetto di cassone vedilo anche più come un involucro dove butti la roba che non va bene, capisci?

_[immagine]_**  
Alessio Monaco** 1:39:13  
No, assolutamente. Ma io mi immaginavo. Ti faccio l'esempio, tu c'hai dei dischi che poi vengono da vengono forati su un'altra linea? No, il disco per essere forato deve avere l'anima perfetta. OK, sei irrigata, non puoi fare il foro sul disco.  
OK, domanda è, io operatore prende il disco, si accorge che è rigato, fa uno scrap perché magari gli è arrivato dalla linea precedente che ha rigato no, se ne accorge?  
Noi oggi facciamo uno scrap, diamo un'etichetta, stampiamo l'etichetta sul contenitore scrap, prendiamo gli altri pezzi buoni, li mettiamo nel contenitore corretto, no?  
Su un disco rigato, no?  
Cioè se l'operatore sbaglia a metterlo nel cassone, noi non abbiamo un controllo di questo, io questo sto chiedendo.

_[immagine]_**  
Paolo Comparoni** 1:40:02  
Beh, però ad esempio ci sono anche ci sono delle inspection no? Che possono benissimo. Hai controllato che tutti siano giusti sì o no? E quella cosa lì può può essere anche ci può essere anche un inspection apposta.

_[immagine]_**  
Alessio Monaco** 1:40:16  
Ma no, ma infatti mi domandavo se cioè capisco da come è configurato che non è un requisito di business e ci hanno richiesto fare dei controlli automatici sui sulle difettosità o meno, cioè noi definiamo un difetto che sia su un materiale piuttosto che su una.  
Work operation passa, cioè non è a noi, non è deputato il compito anche di controllare.  
Bene.

_[immagine]_**  
Juela Ndoka** 1:40:46  
Sì.

_[immagine]_**  
Paolo Comparoni** 1:40:47  
Cioè viene tutto tracciato e c'è adesso appunto si chiama Sentencing, no, c'è l'ingegnere della quality che controlla tutti questi pezzi qua difettosi e li risolve.

_[immagine]_**  
Juela Ndoka** 1:40:57  
OK, sì.

_[immagine]_**  
Alessio Monaco** 1:40:57  
OK.

_[immagine]_**  
Juela Ndoka** 1:40:59  
Sì, OO lì, cioè perché lui tutte le volte che tu fai quarantena è lui che deve dire se può tornare nel processo o deve uscire fuori, cioè quando fa quel quel movimento che ti dicevo che va in quella pagina e cambia lo Stato.

_[immagine]_**  
Alessio Monaco** 1:41:10  
OK, quindi?  
Ok.  
Sì, OK.

_[immagine]_**  
Juela Ndoka** 1:41:15  
E lui non cambia lo Stato dopo che l'ha verificato.

_[immagine]_**  
Alessio Monaco** 1:41:19  
OK.

_[immagine]_**  
Juela Ndoka** 1:41:20  
Se era vero o meno?

_[immagine]_**  
Alessio Monaco** 1:41:22  
OK.  
Certo.

_[immagine]_**  
Juela Ndoka** 1:41:33  
OK, perfetto.  
E Tommaso?

_[immagine]_**  
Tommaso Penta** 1:41:40  
Sì.

_[immagine]_**  
Juela Ndoka** 1:41:42  
Siamo pronti.

_[immagine]_**  
Tommaso Penta** 1:41:43  
Sì.

_[immagine]_**  
Juela Ndoka** 1:41:44  
Era questo lo ordina.

_[immagine]_**  
Tommaso Penta** 1:41:46  
Sì, è già, siamo già qui, faccio la complete.

_[immagine]_**  
Juela Ndoka** 1:41:52  
OK.

_[immagine]_**  
Tommaso Penta** 1:41:54  
Aspetta.  
Saluta la sessione, probabile.

_[immagine]_**  
Juela Ndoka** 1:42:02  
In the Bank, scusami, l'hai messo il break point sul autoconsumo.

_[immagine]_**  
Tommaso Penta** 1:42:03  
Sì.  
Sì, ecco, back point. OK, c'è un back point. Vabbè, magari era quella vecchia, OK, lo rifaccio OK.  
Allora lui va qua dentro, vabbè, questa qua che.

_[immagine]_**  
Juela Ndoka** 1:42:27  
Fammi vedere così, OK, cosa tornato là e.

_[immagine]_**  
Tommaso Penta** 1:42:30  
Questo è per il per vedere il parent o l'equipment.

_[immagine]_**  
Juela Ndoka** 1:42:33  
Questo è la questo è il punto più importante che ti deve dire dove sono? Vai su, Fammi vedere la HTTP response di quella chiamata.  
Ok.

_[immagine]_**  
Tommaso Penta** 1:42:51  
Par equipment questo e il suo parente questo.

_[immagine]_**  
Juela Ndoka** 1:42:53  
OK.

_[immagine]_**  
Tommaso Penta** 1:42:57  
E lui qua va sempre, diciamo.  
Avanti.

_[immagine]_**  
Juela Ndoka** 1:43:01  
OK.  
OK, facciamo questo perché dobbiamo capire questo giro qui fai step in two.  
È entrato nel ramo, quindi vuol dire che c'è un work center, vai, fallo andare, questa che è la chiamata.

_[immagine]_**  
Tommaso Penta** 1:43:18  
Bene.

_[immagine]_**  
Juela Ndoka** 1:43:22  
OK.

_[immagine]_**  
Tommaso Penta** 1:43:23  
Ok, basta che tu.

_[immagine]_**  
Juela Ndoka** 1:43:24  
Fammi vedere cosa ti ha tornato buffer list.  
Va per gli stenti.

_[immagine]_**  
Tommaso Penta** 1:43:32  
Sente.

_[immagine]_**  
Juela Ndoka** 1:43:32  
Per quello, OK, vai.  
Fai step over di questo.

_[immagine]_**  
Tommaso Penta** 1:43:39  
OK, cosa?

_[immagine]_**  
Juela Ndoka** 1:43:39  
OK, ma I want this step in to, stai controllando la linea.

_[immagine]_**  
Tommaso Penta** 1:43:43  
Basta che.  
Sì, fa chi pensa diverso dai altri.

_[immagine]_**  
Juela Ndoka** 1:43:56  
Fammi vedere il buffer che è tornato.

_[immagine]_**  
Tommaso Penta** 1:43:56  
Su questo buffer list sì, due sì, esatto, uno sì.

_[immagine]_**  
Juela Ndoka** 1:44:01  
Diana, ¿cuáles son ahí?

_[immagine]_**  
Tommaso Penta** 1:44:07  
PSA bla bla bla.

_[immagine]_**  
Juela Ndoka** 1:44:11  
OKE, l'altro sotto.

_[immagine]_**  
Tommaso Penta** 1:44:13  
Edoardo sotto.

_[immagine]_**  
Juela Ndoka** 1:44:19  
Qual è quello giusto in cui dobbiamo trovare qualcosa?  
Lato dati, cioè quali delle due contiene il contenitore che può soddisfare la nostra necessità?

_[immagine]_**  
Annalisa Casciaro** 1:44:39  
E qual è il qual è il prodotto, qual è il prodotto Tommaso?

_[immagine]_**  
Tommaso Penta** 1:44:40  
Quale?

_[immagine]_**  
Annalisa Casciaro** 1:44:46  
Lo copio in chat un secondo.

_[immagine]_**  
Juela Ndoka** 1:44:48  
Il materiale da consumare.

_[immagine]_**  
Tommaso Penta** 1:44:52  
Aspetta, aspetta.

_[immagine]_**  
Juela Ndoka** 1:44:53  
Torna nella pagina repetitive.

_[immagine]_**  
Tommaso Penta** 1:44:59  
È uno solo, OK, zero questo.

_[immagine]_**  
Juela Ndoka** 1:45:02  
TTSA trattino 06 8 trattino 0 98.

_[immagine]_**  
Annalisa Casciaro** 1:45:09  
068 98.

_[immagine]_**  
Juela Ndoka** 1:45:11  
Esatto.

_[immagine]_**  
Tommaso Penta** 1:45:11  
0 98 0.

_[immagine]_**  
Annalisa Casciaro** 1:45:14  
Allora ne abbiamo sulla KNB.

_[immagine]_**  
Juela Ndoka** 1:45:17  
Quindi deve andare a guardare lì dentro, OK?

_[immagine]_**  
Tommaso Penta** 1:45:21  
OK.

_[immagine]_**  
Juela Ndoka** 1:45:21  
E vai, fallo andare avanti.  
OK.

_[immagine]_**  
Tommaso Penta** 1:45:30  
Qua, quindi questo qua restituisce la lista dei due, OK?

_[immagine]_**  
Juela Ndoka** 1:45:31  
Fammi vedere due OK, vai, fai step in tu cosa torna alla lista delle NTU.

_[immagine]_**  
Tommaso Penta** 1:45:34  
Va bene.

_[immagine]_**  
Juela Ndoka** 1:45:42  
Ok.

_[immagine]_**  
Tommaso Penta** 1:45:46  
MTU properties.

_[immagine]_**  
Juela Ndoka** 1:45:50  
Dario ambos.

_[immagine]_**  
Tommaso Penta** 1:45:52  
RM è questa qua che torna a zero.

_[immagine]_**  
Juela Ndoka** 1:45:57  
Fammi vedere qual è il suo filtro.

_[immagine]_**  
Tommaso Penta** 1:46:00  
Su filtro e work center che è uguale a m.  
Vabbè material True questo qui non so se soddisfa questa condizione quindi che siano tutte e due no, una tu o una false o tutte e due false.

_[immagine]_**  
Juela Ndoka** 1:46:19  
Controlliamo apriamo sequel.

_[immagine]_**  
Tommaso Penta** 1:46:21  
Bene.  
Che è questo?

_[immagine]_**  
Juela Ndoka** 1:46:27  
Sì.

_[immagine]_**  
Tommaso Penta** 1:46:30  
OK, è già qui.

_[immagine]_**  
Annalisa Casciaro** 1:46:35  
No, quality non è quello Elisa.

_[immagine]_**  
Tommaso Penta** 1:46:35  
No.

_[immagine]_**  
Juela Ndoka** 1:46:36  
No, devi aprire il listener e le cluster, questo è specifico per il plan Tostrama, devi aprire il QAGL tre.

_[immagine]_**  
Annalisa Casciaro** 1:46:44  
Hello.  
È il penúltimo, Liz JJ Cole.

_[immagine]_**  
Juela Ndoka** 1:46:49  
L'avete avete messo il nome nuovo?

_[immagine]_**  
Annalisa Casciaro** 1:46:53  
Sì.

_[immagine]_**  
Juela Ndoka** 1:46:54  
Ma no.

_[immagine]_**  
Annalisa Casciaro** 1:46:54  
Questo è quality.

_[immagine]_**  
Tommaso Penta** 1:46:57  
OK.

_[immagine]_**  
Juela Ndoka** 1:47:01  
Edoardo.  
Raffaele dico la rana Anders Correct e mi ti prometto.

_[immagine]_**  
Tommaso Penta** 1:47:16  
Perché quella è una vista, vero?

_[immagine]_**  
Juela Ndoka** 1:47:18  
Sì.

_[immagine]_**  
Annalisa Casciaro** 1:47:19  
Sì.

_[immagine]_**  
Tommaso Penta** 1:47:21  
Bene.

_[immagine]_**  
Juela Ndoka** 1:47:23  
Ma te lo dovrebbe proporre?

_[immagine]_**  
Tommaso Penta** 1:47:24  
Ce la.

_[immagine]_**  
Juela Ndoka** 1:47:31  
Scarpello.

_[immagine]_**  
Tommaso Penta** 1:47:31  
No, ho sbagliato.

_[immagine]_**  
Annalisa Casciaro** 1:47:33  
Scrivi MTU, tanto ce ne sono uno.

_[immagine]_**  
Juela Ndoka** 1:47:34  
Toll you, toll you, toll you.

_[immagine]_**  
Tommaso Penta** 1:47:36  
Sarà Alessandro.

_[immagine]_**  
Juela Ndoka** 1:47:37  
Questo no togli anche lanciare lì sotto no mettilo lì nel nella query e te lo cioè lo sistemiamo nel quello il paste buttalo nella in query.

_[immagine]_**  
Tommaso Penta** 1:47:38  
Vabbè, vado, vado a prendere, va bene.  
OK.

_[immagine]_**  
Juela Ndoka** 1:47:52  
Tanto te lo propone.  
From e metti cosa togli New.  
Lo chalet Remax tole la lista in fondo.

_[immagine]_**  
Tommaso Penta** 1:48:05  
Maggiore.

_[immagine]_**  
Juela Ndoka** 1:48:07  
Metti on from davanti.  
Va bene?

_[immagine]_**  
Tommaso Penta** 1:48:16  
Ok.

_[immagine]_**  
Juela Ndoka** 1:48:17  
Ok, where?  
UR prendiamo un che cos'era?  
Anzi, prima di prendere niente fammelo per quel work work center, work center uguale al tuo.

_[immagine]_**  
Tommaso Penta** 1:48:40  
M.

_[immagine]_**  
Juela Ndoka** 1:48:41  
NK 001.  
Emanuele, Tag, Giorgio, Mino.

_[immagine]_**  
Tommaso Penta** 1:48:51  
Va.

_[immagine]_**  
Juela Ndoka** 1:48:52  
Metti un alias così ti propone le cose della vista.

_[immagine]_**  
Tommaso Penta** 1:48:59  
Un alias?

_[immagine]_**  
Juela Ndoka** 1:49:01  
Sì, metti B quello che vuoi senza cioè solo OK, metti B punto dovrebbe essere si chiama credo Equipment and ID.

_[immagine]_**  
Tommaso Penta** 1:49:17  
Va bene.  
Aspetta, ce l'ho scritto.

_[immagine]_**  
Juela Ndoka** 1:49:26  
Cart 001.

_[immagine]_**  
Tommaso Penta** 1:49:28  
Sì, solo.  
Per me non lo so, vabbè, facciamo così.  
Ma solo.

_[immagine]_**  
Juela Ndoka** 1:49:41  
E sono.

_[immagine]_**  
Tommaso Penta** 1:49:45  
Quindi aggiusta, cioè che mi inserisce vuoto.

_[immagine]_**  
Juela Ndoka** 1:49:51  
Ora mettimi.  
MNK 0 1 g che cos'era il buffer?  
Vai nel buffer, entro nella lista dei buffer, la top page.

_[immagine]_**  
Tommaso Penta** 1:50:05  
Lato.

_[immagine]_**  
Juela Ndoka** 1:50:07  
Sotto lì.

_[immagine]_**  
Annalisa Casciaro** 1:50:12  
No, te lo dico io, te lo dico io Tommaso e me ne.

_[immagine]_**  
Tommaso Penta** 1:50:12  
Però aspetta, sto sbagliando perché devo andare di qua, scusa?

_[immagine]_**  
Annalisa Casciaro** 1:50:16  
Te lo dico io il nome MNQT 0 1 g.  
Togli 1 0.  
Poi uno g però metti un like che like per 100.

_[immagine]_**  
Tommaso Penta** 1:50:28  
Sì.

_[immagine]_**  
Juela Ndoka** 1:50:31  
Sì, perché non so come lo scrive.

_[immagine]_**  
Tommaso Penta** 1:50:31  
Va bene?  
Grazie.

_[immagine]_**  
Annalisa Casciaro** 1:50:35  
No, all'inizio OK, va bene.

_[immagine]_**  
Juela Ndoka** 1:50:47  
Scorri un po'.  
Dov'è l'equimento? Scusa, non lo vedo, OK?

_[immagine]_**  
Tommaso Penta** 1:50:52  
È quello padre.

_[immagine]_**  
Juela Ndoka** 1:50:55  
Sì.

_[immagine]_**  
Annalisa Casciaro** 1:50:55  
Metti il prodotto material need.  
Copialo.

_[immagine]_**  
Juela Ndoka** 1:51:21  
Su vostra va sta funzionando questo?

_[immagine]_**  
Tommaso Penta** 1:51:26  
Sono privato.

_[immagine]_**  
Annalisa Casciaro** 1:51:26  
Non l'abbiamo mai provato.

_[immagine]_**  
Juela Ndoka** 1:51:28  
Sull'area del cutting che il cutting va a buffer aria non l'avete mai provato sul GMTOB?

_[immagine]_**  
Annalisa Casciaro** 1:51:37  
No.  
No, facciamo solo DJ.

_[immagine]_**  
Juela Ndoka** 1:51:42  
OK.

_[immagine]_**  
Annalisa Casciaro** 1:51:47  
Allora di questi quello che ci interessa?  
Tipo già il primo, il primo è quello valido perché è un batch.

_[immagine]_**  
Juela Ndoka** 1:51:57  
Se per non riuscirà mai a consumare perché filtro page context uguale work center non arriverà mai qui perché non il suo work center non sarà mai l'aria.  
Quindi se ora Tommaso va lì e toglie il work center.  
Olé.

_[immagine]_**  
Tommaso Penta** 1:52:20  
Perché equipment need è uguale a me?

_[immagine]_**  
Juela Ndoka** 1:52:24  
No, qua non lo possiamo passare perché non ce l'abbiamo, cioè è da è da verificare quello perché non puoi mettere neanche il first di quello che ti è tornato come buffer, perché può essere che è assegnato a più buffer, quindi non puoi fare un gioco del genere, quindi togli completamente l'equipe.  
Manto uguale a page One textwork center e provo a fare un consumo.

_[immagine]_**  
Tommaso Penta** 1:52:49  
Ci togliere così?  
A cose.

_[immagine]_**  
Juela Ndoka** 1:52:57  
OK.

_[immagine]_**  
Tommaso Penta** 1:52:59  
Lascio andare avanti quella di prima.

_[immagine]_**  
Juela Ndoka** 1:53:02  
Però questo cioè non è che è una modifica ufficiale perché può impattare sulla performance quello che ti torna tutti i record che trova su quel MT, cioè su quel buffer per quel material.

_[immagine]_**  
Tommaso Penta** 1:53:06  
No, certo.  
Se ho capito bene perché cioè l'equipment needs, lui lo vede con MN con diciamo quello il figlio, non il padre, il work center su cui stai lavorando, esatto.

_[immagine]_**  
Juela Ndoka** 1:53:28  
Col work center work center dell'operazione, cioè perché work center è l'operazione, invece questa query va a vedere il buffer, qui c'è il buffer, è un buffer di area, quindi l'equipe.

_[immagine]_**  
Tommaso Penta** 1:53:35  
Sì.

_[immagine]_**  
Juela Ndoka** 1:53:43  
L'equipment di quel buffer non è il nostro work center, è l'equipment dell'area, è quel PSMN cap 0 2, quindi questa vista ti torna a zero, quindi esce fuori, ti dice che non c'è niente da consumare.

_[immagine]_**  
Tommaso Penta** 1:53:56  
Sì.

_[immagine]_**  
Juela Ndoka** 1:54:01  
Vai rilancialo.  
Totally breakpoint file disconnect from server.  
Sotto.  
Se fai disconnect ti toglie il connessione con debug. Faccio un'altro meeting. Sì, facciamo questa prova perché ho un'altro meeting.

_[immagine]_**  
Tommaso Penta** 1:54:48  
Tipo Salvatore.  
OK.

_[immagine]_**  
Alessio Monaco** 1:54:52  
Grazie 1000, devo staccare per un'altra cosa.

_[immagine]_**  
Tommaso Penta** 1:54:54  
Mhm.

_[immagine]_**  
Alessio Monaco** 1:54:56  
Diego, buon weekend.

_[immagine]_**  
Juela Ndoka** 1:54:57  
Buon weekend.

_[immagine]_**  
Tommaso Penta** 1:54:57  
Ciao, buon weekend.

_[immagine]_**  
Annalisa Casciaro** 1:54:59  
Ciao.

_[immagine]_**  
Juela Ndoka** 1:55:04  
OK, fai next, sì.

_[immagine]_**  
Tommaso Penta** 1:55:05  
Veremos un ex saler lo pregunto.

_[immagine]_**  
Juela Ndoka** 1:55:10  
Se sto facendo qualcosa fanno 2 10 quello che vuoi.  
Bye.

_[immagine]_**  
Tommaso Penta** 1:55:18  
Per aver premuto complete, forse no, ho sbagliato, non pensavo di averlo premuto.

_[immagine]_**  
Juela Ndoka** 1:55:21  
Sì, ci sto pensando.  
OK.  
OK, aspetta, ci sto pensando, chissà vai, continui.

_[immagine]_**  
Tommaso Penta** 1:55:31  
Sì, chiaro?  
Sì.  
Maggiore va.  
OK, ti propone, OK, no.

_[immagine]_**  
Juela Ndoka** 1:55:39  
OK, perfetto.

_[immagine]_**  
Annalisa Casciaro** 1:55:42  
Ma non si può condizionare questa vista in qualche modo.  
Diciendo si qualche.

_[immagine]_**  
Juela Ndoka** 1:55:48  
Sì, qualche cosa sì, qualcosa deve essere migliorato, però secondo me bisogna aggiungere un'altra colonna in cui ti dico workshop.

_[immagine]_**  
Tommaso Penta** 1:55:56  
E che vuol dire, cioè configurata ad area, scusami, cioè?

_[immagine]_**  
Juela Ndoka** 1:56:02  
Ora ho un'altro meeting Tommaso, cioè non riesco e vuol dire che cioè come premacchina quel work center non ha un suo buffer, va al buffer dell'area, cioè associato a un buffer dell'area guarda la hierarchy del Plant perché?

_[immagine]_**  
Tommaso Penta** 1:56:03  
OK, va bene, vabbè.  
OK.

_[immagine]_**  
Juela Ndoka** 1:56:18  
Dire meglio, OK, va bene, grazie, Ciao ragazzi.

_[immagine]_**  
Tommaso Penta** 1:56:19  
OK, va bene, grazie, Ciao.

_[immagine]_**  
Annalisa Casciaro** 1:56:23  
Ciao, Ciao, Ciao.

_[immagine]_**  
Francesco Panigo** 1:56:27  
Ciao.

_[immagine]_**  
Annalisa Casciaro** 1:56:29  
Chiudiamo un attimo la registrazione, vogliamo fare noi test?

_[immagine]_**  
Annalisa Casciaro** trascrizione arrestata
