# Manuale di regia — Veniello Studio

Da leggere prima di preparare una scheda di regia. È stato raccolto il 16/10/2026 da guide ufficiali (Higgsfield, Runway), blog di studi che girano spot di drink e articoli sui registi che lavorano con l'IA. Le fonti sono in fondo. I numeri vengono da blog e venditori, quindi sono punti di partenza da provare, non verità.

## 1. Come si girano dal vero gli spot dei drink

Sono le tecniche dei set veri. Servono per girare col telefono e, tradotte in parole, anche per i prompt.

- **Rallentatore.** La versata si gira a 300 fotogrammi al secondo o più e si riproduce lenta: così il liquido sembra di lusso. Con l'iPhone si usano i 240 fps, che a 30 fps danno 8 volte più lento.
- **La «versata eroe» si rifà 15-25 volte.** Il movimento della camera dev'essere identico ogni volta, per questo sui set grandi usano un braccio robotico (motion control).
- **Controluce.** La luce va dietro al bicchiere, così il liquido si accende. Per gin e vodka, che sono trasparenti, è la luce principale: mostra anche il ghiaccio da dentro.
- **Bordi della bottiglia.** Per i bordi bianchi sul vetro si usano strisce di luce lunghe e strette (strip softbox). Per togliere i riflessi e disegnare bordi neri si usano pannelli neri (bandiere, anche cartone nero). Sul vetro si controlla ogni riflesso.
- **Condensa finta:** acqua e glicerina (da 1:1 a 3:1) spruzzate da 30-45 cm. Più vicino fa colature, più lontano non fa niente.
- **Ghiaccio finto in acrilico** per le prove, perché non si scioglie. Quello vero si usa solo per l'inquadratura finale.
- **Obiettivi.** Il grandangolo molto vicino «ti mette dentro» il tavolo. Il probe lens è un obiettivo a tubo lungo che entra tra bicchieri e bottiglie. Il macro serve per gocce, bollicine ed etichetta.
- **Il drink è «truccato».** Nelle pubblicità c'è uno stylist che prepara il liquido, oppure si rifà finché la versata viene bella.

Le parole che danno il «look da spot» nei prompt:

> backlit liquid glowing, strip-light edge highlights on the glass, black flags defining the bottle edges, glycerin condensation beads, crystal-clear ice, high-speed 1000fps slow-motion pour, macro detail

## 2. Come lavorano i migliori con l'IA

- **Spot Kalshi (NBA Finals, 2025, fatto con Veo 3)**, di PJ Accetturo:
  - il copione l'ha scritto con un'IA, poi l'ha trasformato in prompt inquadratura per inquadratura, chiedendone pochi alla volta perché con troppi la qualità cala;
  - ci sono volute **300-400 generazioni per avere 15 clip buone**;
  - 2 giorni di lavoro e meno di 2.000 $ di generazioni, senza contare il suo compenso.
- **Lezione:** si butta circa una clip ogni 20-25. Il preventivo va fatto pensando ai tentativi, non alla clip singola.
- **Spot OLIPOP × Tesco:** il metodo è nel CLAUDE.md.
- Nel 2026 i più bravi scelgono il modello giusto per ogni scena, non uno solo per tutto.

## 3. Come si scrive un prompt per Seedance 2.5

Viene dalle guide di Higgsfield (13/08/2026) e di Runway (25/09/2026). Il prompt è un unico blocco di testo diviso in sezioni con un'etichetta, in questo ordine:

1. **ASSET BINDING:** l'elenco numerato dei riferimenti, ognuno con il suo ruolo (faccia, prodotto, posto, colore). Dire che un riferimento vale «solo» per quello, perché un riferimento legato male si porta dietro cose che non volevi.
2. **GLOBAL STYLE:** genere, colore, pellicola o digitale, formato, e cosa non deve comparire.
3. **SCENE:** una frase sola che riassume tutto lo spot.
4. **CHARACTERS:** ogni persona. Se c'è il riferimento, basta dire quale.
5. **LOCATION:** il posto e gli oggetti, separati dalle persone. Un posto descritto male è la prima causa per cui le scene cambiano tra un taglio e l'altro.
6. **FIRST FRAME AND BLOCKING:** dove sta chi e verso dove guarda all'inizio.
7. **SHOTS:** Shot 1, Shot 2… con i tempi esatti (0-4s, 4-8s, senza buchi tra un tempo e l'altro), il tipo di inquadratura e l'azione. Ogni stacco si chiude con «Hard cut».
8. **OPTICS e CAMERA:** obiettivo, altezza della camera e movimento per ogni inquadratura.
9. **PHYSICS:** come si muovono liquidi, capelli, tessuti, fumo.
10. **LIGHTING:** da dove viene la luce, la direzione, come cade.
11. **AUDIO, per ultimo:** ambiente, rumori, e cosa non ci deve essere (per esempio «no music, no dialogue»).
12. **LOCKS:** cosa deve restare identico, per esempio «product never redesigned, identical in every shot».

Cosa hanno visto nei test:
- **I riferimenti tengono facce e prodotti meglio del testo.**
- Genere e luce cambiano il risultato più di tante righe di descrizione.
- Più facce ci sono, più è difficile: ogni faccia vuole il suo riferimento.
- Inquadratura per inquadratura funziona meglio di un paragrafo unico. Le transizioni vaghe sono la prima causa dei disastri.
- **Pochi riferimenti scelti bene battono tanti riferimenti** (il massimo è 50: 30 immagini, 10 video, 10 audio).
- **Dire cosa non deve comparire evita più errori** che aggiungere descrizioni.

Camera:
- Un movimento per inquadratura. Seedance 2.5 regge movimenti combinati solo nelle inquadrature lunghe, sopra i 4 secondi circa.
- Dire da dove parte e dove arriva la camera.
- Aiutano le parole di ritmo: slow, smooth, stable.

Dialoghi:
- Una o due battute corte per personaggio.
- Musica, rumori e voce vanno ognuno nel suo spazio.

Correzioni:
- Se un solo dettaglio viene sbagliato, si corregge solo quel pezzo (modifica video) invece di rifare tutto.

## 4. Come togliere l'effetto IA

- **Imperfezioni volute:** camera a mano leggera, grana di pellicola, luci alte un po' bruciate, piccoli aggiustamenti di fuoco.
- Il blocco di realismo:

> TEXTURE AND REALISM: light authentic 35mm film grain, gentle gate weave, halation on highlights, faint chromatic aberration at frame edges, lens breathing on focus pulls, natural micro motion blur, skin unretouched with real pores, no beauty retouch, no digital smoothing, no CGI sheen.

- **Obiettivo per le persone:** un regista consiglia il 50mm, cioè l'occhio umano, con inquadrature meno perfette. Da solo l'IA tende a fare tutto a 50-85mm. Per un look «da telefono» si chiede 24-26mm.
- **Le cose difficili per l'IA:** mani che fanno movimenti complicati e facce che parlano dritte in camera. Il rallentatore nasconde gli errori di movimento.
- **In post-produzione, in quest'ordine:** colore, poi grana (partire dal 5-10%), poi una leggera morbidezza.

## 5. Com'è fatto uno spot verticale (reel, TikTok)

- **Il gancio è nel primo secondo:** movimento, una faccia vicina, un'immagine strana, oppure una frase che parla di chi guarda.
- **Niente logo nel primo secondo.** Il marchio va dentro l'azione, e prodotto più marchio si vedono chiari alla fine.
- **Un cambio forte entro il primo secondo** (30 fotogrammi): un taglio, uno zoom o una scritta.
- Si deve capire anche **senza audio**: scritte brevi sullo schermo.
- La durata giusta è 15-30 secondi. Nelle pubblicità social spesso vince lo stile «girato col telefono» (UGC) sullo spot troppo perfetto.

## 6. Locali e hotel (riprese vere)

- **Usa le luci del locale.** Una luce attaccata alla camera fa «video delle vacanze»: se serve, la tiene qualcuno di lato.
- **Tempo di scatto a 1/50 o 1/100** (in Italia la corrente va a 50 Hz). Così i LED non sfarfallano. Con le luci stroboscopiche controlla le righe del sensore.
- **Bilanciamento del bianco** impostato a mano sotto le luci del posto.
- **Arriva prima del pienone** per studiare gli angoli.
- **Gimbal** per camminare tra la gente, **slider** per i movimenti lenti e controllati (camere, prodotto).
- **Hotel:** gli esterni all'ora d'oro (alba o tramonto), l'entrata in camera dalla porta con gimbal lento, la luce delle finestre.
- **Prima la lista delle inquadrature**, poi si gira.

## 7. Modello di scheda di regia

```
SPOT: <nome> · <cliente/prodotto> · <dove esce> · <durata> · <formato 9:16>
CONCETTO: <una frase>
COLORE: <la tinta di tutto lo spot>
RIFERIMENTI DA PREPARARE: <@image1 …, @image2 …, cosa fotografare e come>

INQUADRATURA 1 · 0-2s · <tipo di inquadratura>
  Cosa si vede: …
  Obiettivo / apertura: …    Camera: …    Luce: …
  Perché: <una riga>
INQUADRATURA 2 · …
CHIUSURA: prodotto + marchio (marchio aggiunto col codice)
SUONO: …
COSTO STIMATO: <crediti ed euro, contando i tentativi>
```

## 8. Modello di prompt Seedance 2.5 (in inglese)

```
ASSET BINDING: @image1 = <product, exact, never redesigned>, @image2 = <character face and wardrobe only>, @image3 = <location only>, @image4 = <color grade and mood only>.
GLOBAL STYLE: <genre>, cinematic live-action commercial, <camera/film look>, <grade>, vertical 9:16, <what must never appear>.
SCENE: <one sentence>.
CHARACTERS: <who, which reference>.
LOCATION: <space and props, from @image3>.
FIRST FRAME AND BLOCKING: <positions and directions at 0.0s>.
SHOTS:
Shot 1 (0-3s): <shot size>, <action>. Hard cut.
Shot 2 (3-6s): … Hard cut.
OPTICS: Shot 1 <focal length, aperture>; Shot 2 …
CAMERA: Shot 1 <one movement, start → end, slow and stable>; …
PHYSICS: <liquid, ice, condensation, hair, fabric>.
LIGHTING: <motivated source, direction, backlight on liquid, edge lights on glass>.
TEXTURE AND REALISM: <realism block from section 4>.
AUDIO: <ambience, foley>. <No music / no dialogue unless needed>.
LOCKS: product and faces identical in every shot, no readable text except <…>, no logos generated (logos are added in post).
```

## Fonti

- [Higgsfield · Seedance 2.5 prompting guide](https://higgsfield.ai/blog/seedance-2-5-prompting-guide)
- [Runway · Seedance 2.5 prompt guide](https://runway.com/resources/seedance-2-5-prompt-guide)
- [Runway · Seedance 2.0 prompt guide](https://runway.com/resources/seedance-2-0-prompt-guide)
- [Best Boy Media · beverage commercial production at 300fps](https://bestboymedia.com/blog/beverage-commercial-production-los-angeles.html)
- [Dan McComb · probe lens beer promo](https://www.danmccomb.com/probe-lens-beer-promo-sony-fs5/)
- [Photigy · BTS of a high-end commercial drink shoot](https://www.photigy.com/school/bts-of-high-end-commercial-drink-shoot-part-one/)
- [Visual Education · photographing clear liquid bottles](https://visualeducation.com/class/photographing-clear-liquid-bottles-gin-vodka/)
- [Creatively Squared · condensation for beverage photography](https://www.creativelysquared.com/article/how-to-enhance-condensation-for-ice-cold-beverage-photography)
- [Expert Photography · cocktail photography techniques](https://expertphotography.com/drink-photography)
- [Business Insider · come è stato fatto lo spot Kalshi](https://www.businessinsider.nl/the-chaotic-kalshi-ad-during-the-nba-finals-was-made-with-ai-for-2000-the-guy-behind-the-clip-shared-how-he-made-it/)
- [Inizio Engage · far sembrare vero il video IA](https://inizioengage.com/insights/to-make-ai-video-look-real-we-have-to-make-it-look-less-perfect/)
- [Luma · prompt per video IA realistici](https://lumalabs.ai/news/prompt-realistic-ai-videos)
- [WARC · best practice per gli annunci TikTok](https://www.warc.com/content/article/event-reports/best-practices-for-creating-attention-grabbing-ads-on-tiktok/en-gb/154096)
- [DVinfo · riprese in discoteca (forum)](https://www.dvinfo.net/forum/archive/index.php/t-134686.html)
- [TBEX · video promozionale per hotel](https://tbexcon.com/event-session/how-to-create-a-hotel-promotional-video-shot-list-planning-filming-tips/)
