# POINT — componenti, asset e attribuzioni

Questo documento accompagna POINT 0.3.0 beta. Il programma proprietario è gratuito soltanto per uso non commerciale secondo LICENSE; **le licenze dei componenti terzi rimangono indipendenti**, con tutti i diritti che concedono sui rispettivi materiali. Le attribuzioni non concedono diritti sul marchio POINT.

Il materiale di distribuzione raccoglie testi di licenza, metadati dei componenti effettivamente inclusi, sorgenti corrispondenti dei componenti MPL ed evidenze degli asset. L'inventario generato per la confezione fa testo per le versioni esatte: non tutti i pacchetti installati per sviluppo entrano nel DMG. Questo documento non dichiara che i reference privati siano pubblicabili.

## Font e marchio

L'interfaccia, il sito e le geometrie nuove usano **Archivo**, distribuito con **SIL Open Font License 1.1**. Il font e il testo OFL sono inclusi localmente, insieme al manifest del suo hash; non è necessario contattare Google Fonts. Il marchio deriva dal disegno originale LogoPOINT.ai fornito dal titolare e non è distribuito sotto le licenze software terze.

Helvetica, Helvetica Neue e gli altri font privati presenti nei sorgenti/reference storici non sono asset runtime pubblici di POINT. Non è documentata un'autorizzazione alla redistribuzione dei font Helvetica forniti: non devono comparire in installer, landing, esempi o kit pubblici. La loro conservazione nell'archivio privato non concede ulteriori diritti. Inter non è usato dalla distribuzione corrente.

## MediaPipe e modello mani

POINT usa **Google MediaPipe Tasks Vision 1.1.1** e il modello ufficiale **Hand Landmarker full float16, versione 1**, sotto **Apache License 2.0**. Copyright The MediaPipe Authors / Google LLC e contributori. Il tracking elabora gli input sul dispositivo; il video camera non viene caricato ai servizi account/newsletter di POINT.

Fonti verificate: [metadati npm della versione 1.1.1](https://registry.npmjs.org/@mediapipe%2Ftasks-vision/1.1.1), [repository MediaPipe](https://github.com/google-ai-edge/mediapipe), [guida ufficiale Hand Landmarker](https://developers.google.com/edge/mediapipe/solutions/vision/hand_landmarker), [model card ufficiale](https://storage.googleapis.com/mediapipe-assets/Model%20Card%20Hand%20Tracking%20%28Lite_Full%29%20with%20Fairness%20Oct%202021.pdf). La model card indica Apache 2.0 a pagina 2.

I sette file runtime JS/WASM locali sono confrontati byte per byte con il tarball npm ufficiale 1.1.1; il modello coincide con il [download Google float16/v1](https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task), SHA-256 `fbc2a30080c3c557093b5ddfc334698132eb341044ccee322ccf8bcf3607cde1`.

Il tarball npm non include un file autonomo LICENSE o NOTICE: il testo Apache è conservato dalla fonte ufficiale, insieme alla dichiarazione di licenza versionata, fonti e hash. La cartella `licenses/mediapipe` della distribuzione conserva queste evidenze. Il worker d'integrazione POINT è distinto dai byte upstream. La [privacy notice MediaPipe](https://github.com/google-ai-edge/mediapipe#privacy-notice) descrive anche metriche tecniche di utilizzo/prestazioni: non viene garantita l'assenza di ogni metrica upstream.

## Software

| Componente | Licenza / ruolo |
| --- | --- |
| Electron e Chromium | MIT per Electron e licenze dei componenti Chromium; runtime desktop, testi inclusi nella confezione |
| React e React DOM | MIT; interfaccia |
| Three.js | MIT; rendering grafico |
| Tone.js | MIT; motore musicale |
| Mediabunny | MPL-2.0; gestione e scrittura media |
| Client Supabase | Licenze upstream, prevalentemente MIT; account e importazione dei progetti dell'utente |
| lucide-react | ISC per il codice della libreria e attribuzioni/licenze delle icone upstream; interfaccia |
| Next.js | MIT; build del sito, escluso dal runtime desktop |

I testi pertinenti e quelli delle dipendenze incorporate accompagnano il pacchetto. Per Mediabunny vengono forniti i sorgenti corrispondenti della versione distribuita, con metadati e licenza; la licenza proprietaria POINT non restringe i diritti sui file MPL. La distribuzione mantiene le intestazioni e le attribuzioni upstream, incluse le licenze delle icone.

L'export usa **H.264 e AAC nativi** dell'ambiente. Il fallback `@mediabunny/aac-encoder` e il suo FFmpeg WASM non sono inclusi nel prodotto corrente; eventuali copie nello storico privato non fanno parte della distribuzione 0.3.0. FFmpeg eventualmente usato come strumento locale di verifica non è un componente dell'installer.

## Groovebox e materiali dell'utente

La groovebox sintetizza i suoni tramite Tone.js/DSP; i riferimenti a macchine 909/303 descrivono un'ispirazione e non l'inclusione dei loro campioni originali. Gli esempi `.point` pubblici contengono configurazioni iniziali, geometrie Archivo e musica sintetizzata, non riprese webcam, dati account o registrazioni già pronte.

Musica, SVG, campioni e altri file importati dagli utenti mantengono i diritti dei rispettivi titolari. POINT non assegna né verifica una licenza per quei materiali.

## Audio storici TeknoAXE

Gli otto MP3 mantenuti per la lettura dei progetti storici provengono da TeknoAXE; le fonti dichiarano **Creative Commons Attribution 4.0**. I download originari contenevano un preambolo non audio HTML/PHP di 386–396 byte: è stato rimosso senza ricodificare i dati ID3/MPEG. Il catalogo audio e CREDITS.txt inclusi raccolgono crediti, URL, hash e dimensioni dei file ripuliti.

| Brano | Pagina sorgente |
| --- | --- |
| It Rains Again | [TeknoAXE 2471](https://teknoaxe.com/Link_Code_3.php?q=2471&genre=Techno) |
| Blood and Steel | [TeknoAXE 2469](https://teknoaxe.com/Link_Code_3.php?q=2469&genre=Techno) |
| Getting the Message | [TeknoAXE 2467](https://teknoaxe.com/Link_Code_3.php?q=2467&genre=Techno) |
| Beautiful Witch | [TeknoAXE 2465](https://teknoaxe.com/Link_Code_3.php?q=2465&genre=Techno) |
| Underwater Secret Base 2 | [TeknoAXE 2463](https://teknoaxe.com/Link_Code_3.php?q=2463&genre=Techno) |
| New Dawn Approaches | [TeknoAXE 2461](https://teknoaxe.com/Link_Code_3.php?q=2461&genre=Techno) |
| We Dance Tonight | [TeknoAXE 2457](https://teknoaxe.com/Link_Code_3.php?q=2457&genre=Techno) |
| Below the Skyway | [TeknoAXE 2455](https://teknoaxe.com/Link_Code_3.php?q=2455&genre=Techno) |

Quando pubblichi un export contenente questi brani conserva nome, autore, fonte e collegamento a [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), indicando le modifiche alla musica dove applicabile. Il credito pronto è nel catalogo. I BPM 128 del catalogo sono impostazioni iniziali, non metadati musicali verificati. Le condizioni non commerciali del programma non cambiano la licenza CC BY delle registrazioni originali.

## Audio storici Tricks & Traps

Quattro brani provengono dagli upload dell'autore su OpenGameArt: **Stomper** (160 BPM), **Mental Corruption** (150 BPM), **Logic or Emotions** (151 BPM) dal [Free Rhythm Game Music Pack 2](https://opengameart.org/content/free-rhythm-game-music-pack-2), e **Bow For Me** (157 BPM) dal [Free Rhythm Game Music Pack 1](https://opengameart.org/content/free-rhythm-game-music-pack-1). Le fonti dichiarano **CC0 1.0**; autore e provenienza vengono comunque conservati.

I WAV originali sono convertiti in MP3 192 kbit/s senza cambiare composizione o velocità. Il catalogo conserva download, hash WAV, hash/dimensione MP3 e BPM dichiarati dall'autore. La [dedica CC0](https://creativecommons.org/publicdomain/zero/1.0/) non impone attribuzione per la registrazione originale.

## Archivio privato e aggiornamenti

Prototipi, reference, codice web precedente e font forniti restano nell'archivio privato con la propria provenienza; non entrano automaticamente nel prodotto o nella release pubblica. Una cartella senza file di licenza non è descritta come codice liberamente redistribuibile.

Per ogni aggiornamento controllare versioni e licenze dei byte realmente distribuiti, rigenerare l'inventario, conservare eventuali NOTICE upstream e includere i sorgenti corrispondenti dovuti. Un elenco di tutte le dipendenze installate non sostituisce il controllo del DMG e degli archivi pubblicati.
