# Box Breathing VR

Un esercizio guidato di respirazione che funziona **direttamente nel browser**: senza installare nulla, senza account, senza app. Su computer e telefono è una pagina; con un visore (testato sui visori Meta) diventa un'esperienza immersiva con una sfera luminosa che respira con te.

Un progetto di **QuestDevs()**, il laboratorio di sviluppo di **Quest: Benessere Digitale** — perché la tecnologia, usata bene, è un catalizzatore di benessere e non solo un rischio da contenere.

- **URL pubblico:** [https://questdigitale.org/box-vr](https://questdigitale.org/box-vr)
- **Tecnologia:** un unico file HTML. WebGL e WebXR nativi, zero librerie, zero dipendenze, zero raccolta dati.
- **Comandi in VR:** grilletto = avvia/pausa · stretta dell'impugnatura = cambia ritmo · pannello istruzioni sempre leggibile, sopra la sfera.

---

## I due ritmi

L'esercizio guida la respirazione con due protocolli selezionabili:


| Ritmo           | Ciclo                                                | Frequenza            | Caratteristica                         |
| --------------- | ---------------------------------------------------- | -------------------- | -------------------------------------- |
| **BOX 4-4-4-4** | inspira 4s · trattieni 4s · espira 4s · trattieni 4s | 16 s ≈ 3,75 atti/min | fasi di pari durata, facile da seguire |
| **CALMA 4-6**   | inspira 4s · espira 6s                               | 10 s = 6 atti/min    | espirazione prolungata                 |


In entrambi i casi si tratta di **respirazione lenta** (sotto i 10 atti al minuto), la famiglia di tecniche con la base di evidenze più solida: una revisione sistematica di 40+ studi mostra correlazioni coerenti con riduzione dell'attivazione fisiologica, aumento della variabilità cardiaca e riduzione di ansia e rabbia nelle persone sane \[1\].

---

## Perché queste tecniche

**La frequenza** Il sistema cardiovascolare ha una "frequenza di risonanza" attorno a 0,1 Hz (≈ 6 atti/min): respirare a questo ritmo massimizza l'oscillazione della variabilità cardiaca (respiratory sinus arrhythmia) e stimola il baroriflesso, con effetti documentati su equilibrio autonomico e auto-regolazione emotiva \[2\]. Il ritmo **CALMA 4-6** (esattamente 6 atti/min) è costruito su questa letteratura: un ciclo di 10 secondi centrato sulla frequenza di risonanza.

**L'espirazione lunga** Le pratiche contemplative che producono calma condividono due tratti: bassa frequenza respiratoria ed espirazioni prolungate, che stimolano il nervo vago (il modello "rVNS": *respiratory vagal nerve stimulation*) e spostano l'equilibrio autonomico verso la componente parasimpatica \[3\]. È per questo che CALMA 4-6 dedica più tempo all'espirazione che all'inspirazione. Non è un'opinione di design: in uno studio sperimentale randomizzato (114 partecipanti, 1 mese di pratica quotidiana), la respirazione ciclica con sospiri prolungati ha migliorato umore e ridotto l'attivazione fisiologica più della mindfulness e più del box breathing stesso \[4\].

**Sul box breathing** Il BOX 4-4-4-4 è la tecnica più conosciuta (la portiamo avanti fin dai corsi tattici e dai protocolli di gestione dello stress acuto), ma una revisione sistematica dei trial randomizzati specifici sul box breathing conclude che le evidenze dirette sono ancora **limitate** \[5\]. L'abbiamo incluso per tre motivi: la sua struttura a fasi identiche è la più semplice da seguire per chi inizia; rientra comunque nel dominio della respirazione lenta ben supportata \[1\]; e il confronto con CALMA 4-6 permette all'utente di sperimentare la differenza tra ritmo BOX ed espirazione prolungata.

---

## Perché la realtà virtuale

L'idea di fondo: **un ambiente immersivo occupa la finestra percettiva e scherma gli stimoli distraenti**. Chi respira davanti a uno schermo ha notifiche, icone e movimento attorno; nel visore la scena è l'unica cosa visibile, e l'attenzione si può posare su un solo oggetto: la sfera che respira.

Non è un'intuizione nostra, è una delle ipotesi più replicate della letteratura VR:

- **L'attenzione è una risorsa limitata.** L'evidenza più drammatica viene dalla terapia del dolore: nei pazienti ustionati sottoposti a medicazioni, l'ambiente immersivo riduce significativamente il dolore percepito rispetto alla sola distrazione farmacologica, proprio perché consuma le risorse attentive che altrimenti elaborerebbero lo stimolo doloroso \[6\]. Lo stesso principio — meno banda percettiva disponibile per i pensieri distraenti — è alla base dell'uso VR per la regolazione emotiva.
- **Le revisioni sulla VR per lo stress convergono.** Una revisione sistematica su adulti sani trova che interventi di gestione dello stress in VR immersiva producono miglioramenti consistenti in stati d'ansia e umore \[7\]; una scoping review più recente osserva che gli ambienti virtuali calmi funzionano attraverso i meccanismi delle *attention restoration* e *stress recovery theory* — l'immersione in ambienti pacifici che "disancorano" parzialmente l'utente dai carichi della realtà \[8\].
- **Un esercizio che chiede attenzione merita un ambiente che la protegge.** La respirazione lenta funziona se la si segue davvero; ogni distrazione visiva è un costo. Nel visore quel costo si azzera: il pacer è l'unico oggetto del campo visivo.

---

## Le scelte di interfaccia, e perché

- **Il pacer è una sfera che cresce e si restringe.** È il pattern visivo standard degli strumenti di respirazione guidata: un elemento che si espande nell'inspirazione e si contrae nell'espirazione (nella ricerca sul design di queste tecnologie è letteralmente l'esempio canonico) \[9\]. Noi l'abbiamo reso tridimensionale, con una deformazione organica continua: la sfera non "pompa", respira.
- **Testo grande** Dalla v1.7 caratteri e pannello sono stati ingranditi finché la lettura è comodamente possibile a distanza — in linea con le linee guida di design Meta Horizon OS, che indicano corpi minimi e gerarchia netta per la leggibilità in VR \[10\] e richiedono che ogni testo in-app sia chiaramente leggibile \[11\].
- **Il pannello è fisso nel mondo** Testo che segue lo sguardo si paga in disagio e nausea: preferiamo che l'utente guardi la scena e ritrovi le informazioni dove stanno, come un cartellone. Le scelte di comfort seguono le raccomandazioni ufficiali per esperienze sicure e confortevoli in VR \[12\].
- **Un solo gesto per azione.** Grilletto per avviare/fermare, stretta per cambiare ritmo: niente menu, niente puntatori complessi. Ogni elemento interattivo dà feedback visivo e sonoro \[13\].
- **Palette a bassa stimolazione.** Verde petrolio profondo e giallo caldo del marchio: colori coerenti con l'identità di Quest e con la logica degli ambienti rilassanti usati negli studi VR \[8\], senza pattern ad alto contrasto o movimento intenso, che le linee guida segnalano come fonti di disagio \[12\].
- **Segnali sonori discreti ai cambi di fase.** Tre note distinte (ispirazione, espirazione, apnea) consentono di seguire l'esercizio senza fissare il testo — utile anche per chi ha difficoltà di lettura. Il ritmo è visivo *e* uditivo, in ridondanza.
- **Zero telemetria** Nessun cookie, nessun dato inviato, nessun salvataggio remoto: la privacy è una scelta di progettazione. Serve solo la connessione per scaricare il font Roboto da Google Fonts.

---

## Note di sicurezza

- Lo strumento è un supporto al benessere, **non un dispositivo medico** e non sostituisce consulenza psicologica o percorsi di cura.
- La respirazione lenta è ben tollerata, ma in alcune persone può causare stordimento; se accade, interrompere e respirare normalmente.
- In presenza di attacchi di panico, l'attenzione al respiro può talvolta amplificare il disagio: in questi casi l'esercizio va affrontato con un professionista.
- Se compaiono fastidi tipici del motion sickness (nausea, vertigini), interrompere la sessione VR e fare una pausa. Il nostro ambiente è statico (nessun movimento di camera), il rischio è basso ma non zero.
- Il ritmo guidato non va seguito a costo di forzare il respiro: il ritmo naturale dell'utente ha sempre la precedenza.

---

## Bibliografia

\[1\] Zaccaro, A., Piarulli, A., Laurino, M., Garbella, E., Menicucci, D., Neri, B., et al. (2018). *How Breath-Control Can Change Your Life: A Systematic Review on Psycho-Physiological Correlates of Slow Breathing.* Frontiers in Human Neuroscience, 12:353. [https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2018.00353/full](https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2018.00353/full)

\[2\] Lehrer, P. M., &amp; Gevirtz, R. (2014). *Heart rate variability biofeedback: how and why does it work?* Frontiers in Psychology, 5:756. [https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2014.00756/full](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2014.00756/full)

\[3\] Gerritsen, R. J. S., &amp; Band, G. P. H. (2018). *Breath of Life: The Respiratory Vagal Stimulation Model of Contemplative Activity.* Frontiers in Human Neuroscience, 12:397. [https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2018.00397/full](https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2018.00397/full)

\[4\] Balban, M. Y., Neri, E., Kogon, M. M., et al. (2023). *Brief structured respiration practices enhance mood and reduce physiological arousal.* Cell Reports Medicine, 4(1):100895. [https://pmc.ncbi.nlm.nih.gov/articles/PMC9873947/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9873947/)

\[5\] *Systematic Review of Randomised Controlled Trials Evaluating Box Breathing for Stress, Autonomic, and Clinical Outcomes* (2026). Applied Psychophysiology and Biofeedback. [https://link.springer.com/article/10.1007/s10484-026-09812-7](https://link.springer.com/article/10.1007/s10484-026-09812-7)

\[6\] Hoffman, H. G., Chambers, G. T., Meyer, W. J., et al. (2011). *Virtual reality as an adjunctive non-pharmacologic analgesic for acute burn pain during medical procedures.* Annals of Behavioral Medicine, 41(2):182–189. [https://pmc.ncbi.nlm.nih.gov/articles/PMC4465767/](https://pmc.ncbi.nlm.nih.gov/articles/PMC4465767/)

\[7\] *The Advances of Immersive Virtual Reality Interventions for the Enhancement of Stress Management and Relaxation among Healthy Adults: A Systematic Review* (2022). Applied Sciences, 12(14):7309. [https://www.mdpi.com/2076-3417/12/14/7309](https://www.mdpi.com/2076-3417/12/14/7309)

\[8\] *Virtual reality environments for stress reduction and management: a scoping review* (2024). Virtual Reality. [https://link.springer.com/article/10.1007/s10055-024-00943-y](https://link.springer.com/article/10.1007/s10055-024-00943-y)

\[9\] *Comparing heart rate variability biofeedback and simple paced breathing to inform the design of guided breathing technologies* (2022). Frontiers in Computer Science, 4:926649. [https://www.frontiersin.org/journals/computer-science/articles/10.3389/fcomp.2022.926649/full](https://www.frontiersin.org/journals/computer-science/articles/10.3389/fcomp.2022.926649/full)

\[10\] Meta Horizon OS Developers — *Typography* (dimensioni minime e gerarchia per la leggibilità). [https://developers.meta.com/horizon/design/styles\_typography/](https://developers.meta.com/horizon/design/styles_typography/)

\[11\] Meta Horizon OS Developers — *VRC.Quest.Accessibility.2* ("tutti gli elementi UI e testi in-app devono essere chiaramente leggibili"). [https://developers.meta.com/horizon/resources/vrc-quest-accessibility-2/](https://developers.meta.com/horizon/resources/vrc-quest-accessibility-2/)

\[12\] Meta Horizon OS Developers — *Overview of immersive VR apps best practices* (esperienze sicure e confortevoli). [https://developers.meta.com/horizon/design/bp-overview/](https://developers.meta.com/horizon/design/bp-overview/)

\[13\] Meta Horizon OS Developers — *Key considerations* (feedback visivo e sonoro sugli elementi interattivi). [https://developers.meta.com/horizon/design/mr-design-guideline/](https://developers.meta.com/horizon/design/mr-design-guideline/)

---

*Progetto QuestDevs() — laboratorio di sviluppo di Quest: Benessere Digitale · questdigitale.org*
