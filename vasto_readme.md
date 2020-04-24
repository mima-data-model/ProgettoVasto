# Introduzione al Progetto Vasto? 

cos’è, cos’è l’edizione in Evt2 di vasto (link a evt2)  --> riusa evt2 blabla PER ORA MONOTESTIMONE

## L'edizione digitale Vasto: funzionalità e limitazioni 

In particolare, edizione digitale presenta la Storia Fiorentina di Varchi, in particolare del testimone RC4. Allo stato attuale la piattaforma Vasto presenta il proemio del Primo Libro (versione Pilot).
L'edizione è quindi stata implementata su EVT-2, customizzando quest ultimo nei casi di necessità specifici riportati nei prossimi paragrafi.   
EVT-2 permette di caricare facilmente il file xml (il quale segue l’encoding XML-TEI). Il documento xml che contiene il testo marcato è unico e contiene tutti gli elementi dell'edizione critica e diplomatica (opportunamente abilitati e disabilitati nel css a seconda delle esigenze di visualizzazione).

La customizzazione della Piattaforma Vasto rispetto il pacchetto EVT-2 avviene attraverso la modifica di tre file: 
- il file xml contenente il testo marcato in tei (in questo specifico caso data/pilot_proemio.xml)
- il file json di configuarazione della visualizzazione (config/config.json)
- il file css messo a disposizione da EVT-2 per facilitare la customizzazione della visualizzazione (config/custom_style.css)
- infine, all'occorrenza, sono state fatte delle piccole modifiche al file javascript (scripts/evtviewer.b31e1966.js)

## L'edizione Digitale Vasto: Fuzionalità e Visualizzazioni

Come descritto in precedenza, l'edizione digitale è composta dall'edizione diplomatica e critica. 


## FUNZIONALITA' TRANS-EDIZIONE:
* Nella presente edizione vengono attivate solo le visualizzazioni "Testo di Lettura" e "Immagine Testo"
*	Tutte le scelte stilistiche usate per indicare i fenomeni testuali e le pelculiarità sopracitate sono indicizzati nella sezione info in alto
* Possibilità di scaricare l’xml (in alto a dx)
*	Metadati descrittivi (in alto a dx)
* Il testo è ricco di citazioni di luoghi, persone e date, che vengono marcate e visualizzate grazie al menù in basso (NamedEnititySelection).

## EDIZIONE DIPLOMATICA

### FUNZIONALITA’

L’edizione diplomatica si impegna a visualizzare il testo nel modo più simile possibile alle immagini proposte.
In particolare vengono annotati e visualizzati: 
* linebreak, 
* le aggiunte a margine, in riga, o a piè di pagina. Inoltre nel testo vi è un’ancora (solitamente ^) che, se selezionata dall'utente, permette di illuminare l’addizione corrispondente. 
* La peculiarità che si è voluto enhance nella presente edizione diplomatica è la coesistenza di quattro diverse mani (cassature e addizioni) sul testimone RC4. L’edizione vuole quindi visualizzare in modo efficacie tale peculiarità. Le cassature sono rappresentate con una barra centro del testo del colore corrispondente alla mano che l'ha creata, allo stesso modo le aggiunte vengono segnalate con il colore del testo corrispondente alla mano che l'ha prodotta.
* Nella diplomatica le abbreviazioni vengono sciolte e segnalate in corsivo e grassetto

### Funzionalità aggiuntive rispetto ad EVT-2: 
* La visualizzazione "Immagine Testo" in EVT-2 non è abilitata (non è possibile visualizzare l'immagine corrispondente al testo). La funzionalità è stata quindi abilitata all'interno dell'edizione digitale Vasto. 
Nello specifico le immagini del manoscritto devono essere caricate all'interno di data/imgs/[nome_del_testimone]. Le immagini vanno rinominate con il contenuto dell'attributo "n" dei tag ```<pb>``` contenuti nel file xml dell'edizione.  

## CRITICA 

### FUNZIONALITA’
Mostra il testo di RC4 dopo la redazione a cura di Dario Brancato. L'edizione critica presenta: 
* l'assenza delle cassature 
* normalizzazioni del testo originale
* abbreviazioni sciolte senza alcun riferimento tipografico
* il testo in versione scroll-down, la divisione delle pagine è segnalata inline all'interno del testo (ad esempio con la dicitura [12v]) 
* note a margine, a piè di pagina etc sono rappresentate come parte integrante del testo senza alcuna distinzione tipografica
* le segnalazioni tipografiche delle mani sono eliminate 
* segni particolari (ad esempio ^ oppure -) sono normalizzati e/o eliminati
* il testo è ottimizzato per la lettura e la comprensione testuale

### LIMITAZIONI SIGNIFICATIVE 
* Il carosello di immagini (posizionato a sinistra nella visualizzazioni "Immagine Testo") non segue lo scroll-down del testo a destra. Questo rende le immagini "scollate" dal testo corrispondente, ma è ancora possibile un confronto manuale immagine-testo grazie all'indicazione nel testo della pagina del manoscritto che l'utente sta leggendo. 

## LISTA DEI TAG UTILIZZATI
Il progetto Vasto al momento, come già detto in precedenza, è da considerasi una versione pilot che necessita di essere arricchita con altri materiali. Allo scopo di ampliare il progetto, di seguito rilasciamo una legenda di tag che sono stati utilizzati nel file xml pilot_proemio.xml e che sono stati appostiamente customizzati per rispettare le esigenze del testimone. In particolare presentiamo qui di seguito la lista di tag presenti nel ```<body>``` del file xml. 

* ```<del>```