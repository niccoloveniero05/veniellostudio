# Veniello Studio — CLAUDE.md

Leggi tutto prima di lavorare. Sono regole e decisioni già prese, non ipotesi. Se qualcosa cambia o è sbagliato, correggilo qui: non aggiungere una riga accanto a quella vecchia.

**Attenzione: questo repo è pubblico e GitHub Pages pubblica ogni file su veniellostudio.it** (c'è `.nojekyll`). Quindi qui niente dati privati: prezzi ai clienti, contatti, accordi, crediti comprati, password. Il contesto privato sta nel `CLAUDE.md` della cartella «Servizi Niccolò» sul PC di Niccolò.

## Come lavorare con Niccolò

- Italiano semplice, frasi brevi. Ogni parola tecnica va spiegata la prima volta.
- Mente critica: se una cosa non funziona, dillo. Se ha ragione lui, correggiti senza giri di parole.
- **Prima di ogni generazione a pagamento (Higgsfield) servono crediti ed euro, poi il suo sì.** Se dice «voglio solo imparare», non generare niente.

## Il sito (questo repo)

- Sito statico: `index.html`, `img/`, `video/`, `fonts/`, `js/` (GSAP, ScrollTrigger e Lenis copiati qui; Lenis solo al computer, per «contare» la rotella). Non deve fare richieste esterne: caratteri e script si tengono in locale.
- Pubblicato da GitHub Pages su `veniellostudio.it` (vedi `CNAME`).
- I commit si scrivono in italiano, nella forma «Veniello Studio: cosa è cambiato».
- Lo spot Jué × Bombay sta intero nella scheda «Video e reel» (`video/spot.mp4`). L'ha deciso Niccolò: non toglierlo e non tagliarlo se non lo chiede lui.

## Scuola spot

Obiettivo: Niccolò impara a fare spot pubblicitari con l'IA (Seedance su Higgsfield), al livello dei migliori che si vedono su Instagram.

**Dal 16/10/2026 Claude fa il regista e il direttore della fotografia** (l'ha chiesto Niccolò, che si sentiva spaesato). Niccolò porta l'idea, Claude decide e propone tutto il resto, e spiega ogni scelta in una riga. Così Niccolò impara facendo, come un assistente sul set.

### Come si lavora

**Prima di preparare una scheda di regia leggi `regia.md`**: come si girano davvero gli spot, la struttura dei prompt di Seedance 2.5, come togliere l'effetto IA, i modelli di scheda e di prompt. Quando trovi tecniche nuove, aggiungile lì.

1. Niccolò porta **il cliente e un'idea o un video di riferimento** da cui prendere spunto, anche in due righe confuse.
   - Claude guarda il riferimento (vedi «Come guardare un reel di Instagram») e lo smonta: struttura, ritmo, inquadrature, obiettivi, luce, il trucco che lo fa funzionare.
   - Poi lo adatta al cliente: tiene la struttura, il ritmo e il trucco, e cambia tutto quello che sarebbe una copia (soggetto, battute, dettagli riconoscibili).
2. Claude fa al massimo 3 domande: il prodotto o il cliente, dove esce (reel, TikTok, storia), quanto deve durare.
   **Se l'idea è debole o confusa, Claude la fa crescere.** Parte da cosa ha di unico il cliente (un oggetto, un posto, una storia), propone 3 concetti diversi (uno sicuro, uno forte, uno folle), dice quale sceglierebbe e perché. Poi fa la scheda su quello scelto da Niccolò. Un'idea scarsa non è mai un motivo per fare uno spot scarso.
3. Claude consegna lo **storyboard**, cioè la scheda di regia. Di base è a parole e non costa niente; le immagini dei fotogrammi si fanno solo se Niccolò le chiede (con le sue foto GPT gratis o con i crediti, prezzo prima). Dentro ci sono:
   - il concetto in una frase;
   - il copione;
   - le inquadrature una per una, ognuna con durata, tipo di inquadratura, obiettivo, apertura, movimento della camera, luce e **perché**;
   - il colore di tutto lo spot;
   - il blocco di stile per Seedance;
   - la lista dei riferimenti da preparare (cosa fotografare e come);
   - i prompt pronti.
4. Niccolò dice cosa cambiare. Claude decide, ma ascolta.
5. Prima di generare: crediti ed euro, poi il suo sì.

### Regole della scuola

- **Inizio chat:** leggi lo «Stato» in fondo e riparti da lì. **Fine lavoro:** aggiornalo.
- Ogni scelta tecnica ha il suo perché in parole semplici. Una parola nuova si spiega la prima volta che compare.
- Le lezioni (concetto, esempio, esercizio, correzione) si fanno solo quando le chiede Niccolò. Di base si lavora sui suoi spot veri.
- Niente generazioni a pagamento senza la sua richiesta e il prezzo detto prima.
- Prima si guarda il materiale vero, poi si spiega. Non commentare un reel senza averlo visto.

### Come guardare un reel di Instagram

Dal container cloud Instagram è bloccato, quindi si passa dalla sandbox di Higgsfield (`sandbox_exec`), che non costa crediti:
1. Con Playwright (`NODE_PATH=/usr/local/lib/node_modules`) apri `https://www.instagram.com/reel/<codice>/` e leggi i meta `description` e `og:title` (account, data, didascalia).
2. Apri `…/reel/<codice>/embed/`, clicca al centro e leggi `video.currentSrc`. Poi scarica l'mp4 con curl, usando lo stesso URL letto dal file e non ricopiato a mano.
3. Con `ffmpeg` estrai un fotogramma ogni 1,5-2 secondi, fai dei mosaici con `montage` e guardali (`image_paths`, massimo 512 KB in tutto).
4. Ritaglia a piena risoluzione le parti con testo, per esempio i prompt sullo schermo.
5. Trascrivi l'audio con `faster-whisper`.

### Il programma

1. **L'occhio** (gratis). Smontare spot veri: Niccolò li smonta per primo, poi lo fa Claude e si confronta. Si impara il vocabolario qui sotto.
2. **Idea e copione** (gratis). Il concetto sta in una frase. Copione da 15-20 secondi con il gancio nei primi 2. Lista delle inquadrature.
3. **Riferimenti e prompt** (pochi crediti, solo immagini). Packshot pulito del prodotto, scheda del personaggio, il posto, l'atmosfera, il blocco di stile, i riferimenti numerati. Il prompt lo scrive Niccolò e Claude lo corregge.
4. **Il video** (crediti, con il prezzo prima). Seedance 2.5: bozze a 480p, si cambia una cosa alla volta e ogni tentativo va nel diario dei prompt (cosa è cambiato, cosa è successo).
5. **Montaggio e portfolio.** Ritmo, suono e testi. Poi 3 spot di prova: un prodotto, un locale, un'idea surreale. Finché il marchio non dà l'ok, vanno presentati come «concept», non come lavori commissionati.

### Vocabolario base

- **Inquadrature:** dettaglio, primo piano, mezza figura, figura intera, campo lungo.
- **Movimenti:** fissa, panoramica (la camera gira sul posto), carrellata (la camera si sposta), camera a mano, zoom.
- **Luce:** luce chiave (la principale), riempimento, controluce. Morbida (ombre sfumate) o dura (ombre nette).
- **Obiettivo:** aperto (per esempio T1.4) vuol dire poca profondità di campo, cioè solo il soggetto è a fuoco; chiuso (f/8) vuol dire tutto a fuoco.
- **Quale obiettivo:**
  - 14-24mm (grandangolo): spazi, il locale sembra grande, tanta energia. Da vicino deforma le facce.
  - 35mm: racconto, camera a mano, persone dentro il posto.
  - 50mm: naturale, come l'occhio.
  - 85mm: ritratto, facce belle, sfondo sfocato.
  - 100mm macro: dettagli del prodotto, come ghiaccio, gocce, bollicine, etichetta.
  - 135-200mm (tele): sfondo schiacciato e sfocato, come se stessi spiando.
- **Sull'iPhone (modelli Pro):** 0.5x è circa un 13mm, 1x un 24mm, 2x un 48mm, 3x o 5x da 77 a 120mm.
- **Colore:** il color grading, cioè dare a tutto lo spot la stessa tinta. La grana di pellicola.
- **Montaggio:** taglio sul movimento, ritmo, gancio iniziale, chiusura con prodotto e marchio.

### Cosa abbiamo imparato

**16/10/2026 · Reel di Higgsfield sul 3D (la casa sull'albero).** È una pubblicità di Higgsfield. Da una foto di un albero costruisce una scena 3D a blocchi (lo strumento si chiama «3D Jutsu») e poi l'IA ci «dipinge» sopra la versione realistica.
- Il 3D tiene ferme la disposizione e le inquadrature; i dettagli realistici li inventa l'IA.
- Da una foto sola non ricava le misure esatte, e quello che non si vede lo inventa.
- Per ora importa solo oggetti dal catalogo, non modelli tuoi.
- Serve per le inquadrature impossibili, per tenere il posto uguale tra un'inquadratura e l'altra e per far vedere un'idea al cliente prima di girare.

**16/10/2026 · Spot OLIPOP × Tesco (sizarev.ai, fatto su Arcads).** Le lattine si mordono come mele. Il metodo:
1. Dalla foto vera della lattina si fa un packshot pulito su fondo bianco (GPT Image 2.5). È la «verità» del logo.
2. Un'immagine di riferimento per ogni elemento: la lattina morsa, la lattina normale, la facciata Tesco, l'uomo, l'atmosfera.
3. Un modello di linguaggio scrive il prompt per Seedance: Niccolò può chiedere in italiano e farsi dare il prompt in inglese.
4. Seedance «multi-shot» fa 20-25 secondi con più inquadrature in una sola generazione, ed è per questo che faccia e prodotto restano uguali tra i tagli.

Il blocco di stile che usava, da mettere in cima al prompt:

> Cinematic live-action commercial, shot on ARRI Alexa with vintage spherical prime lenses wide open at T1.4, shallow depth of field, creamy bokeh, subtle anamorphic-style falloff, fine 35mm film grain, desaturated teal-and-olive British grade, soft overcast daylight, handheld.

I riferimenti vanno caricati in un ordine fisso, e ognuno ha il suo ruolo: `@image1` la lattina morsa, `@image2` la lattina, `@image3` la facciata Tesco, `@image4` l'uomo, `@image5` colore e atmosfera.

I trucchi:
- Lo sfondo sfocato è voluto: nasconde gli errori dell'IA.
- La grana toglie l'effetto plastica.
- Un solo colore per tutto lo spot.
- Loghi grandi e semplici.
- Il prodotto si muove ed è in mano.
- L'idea è impossibile da girare dal vero.

Cosa non fanno vedere: quanti tentativi ci sono voluti; «commenta X per la guida» è un trucco per spingere il post; quasi sicuramente il marchio non l'ha commissionato.

**Correzione importante:** con riferimenti fatti bene, Seedance tiene giuste facce e loghi, come è successo anche nello spot Bombay di Niccolò. Le scritte piccole restano approssimative.

### Seedance 2.5 su Higgsfield (letto il 16/10/2026, ricontrolla prima di usarlo)

- Durata da 4 a 30 secondi, risoluzione 480p, 720p o 1080p.
- Modalità: solo testo (`t2v`), riferimenti di immagini, video e audio (`omni_reference`), modifica di un video (`video_edit`), allungamento di un video (`video_extension`).
- Può generare anche il sonoro.
- **Bozza a 480p che entro 7 giorni si può passare a 1080p** (`draft` e `draft_job_id`): si approva la bozza e si paga l'alta qualità solo per quella buona.
- Prezzo visto a ottobre 2026: circa 3, 7 o 16 crediti al secondo a 480p, 720p e 1080p. Fai sempre il preventivo prima.

### Regole venute dallo spot Bombay

- Testi e loghi si aggiungono dopo, con il codice, non li fa l'IA.
- Gli slow motion a 240 fps vanno convertiti in rallentatore a 30 fps prima di darli a Seedance. Altrimenti li legge a velocità normale e il rallentatore sparisce.
- Su TikTok niente che promuova alcol: TikTok toglie il video e può sospendere l'account.

### Stato

- **Modo di lavoro:** Claude regista, dal 16/10/2026.
- **Prossimo passo:** Niccolò racconta la prima idea di spot.
- **Compito facoltativo:** smontare uno spot vero che gli piace (per ogni inquadratura: quanto dura, che inquadratura è, cosa si vede, perché c'è). Non è obbligatorio.
- **Errori che si ripetono:** nessuno per ora.
- **Spot già fatti:** Jué × Bombay (Seedance 2.5, ottobre 2026).
