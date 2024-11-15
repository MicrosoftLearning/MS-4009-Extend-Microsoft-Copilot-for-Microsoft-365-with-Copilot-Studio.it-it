# Esercizio: Creare un plug-in di prompt

In questo esercizio, si apprenderà:

- Come scrivere un buon prompt
- Come creare un prompt in Copilot Studio
- Come testare il prompt nel generatore di prompt
- Come usare il plug-in di prompt in Microsoft 365 Copilot

## Come scrivere un buon prompt

All'inizio di questo modulo, sono state già acquisite alcune nozioni di base sull'ingegneria dei prompt. Una risorsa eccellente per approfondire l'ingegneria dei prompt è la guida all'ingegneria dei prompt del team di AI Builder. La guida all'ingegneria dei prompt è disponibile [qui](https://aka.ms/learn-ai-builder-prompting-guide).

## Elementi di una prompt efficace

La guida all'ingegneria dei prompt del team di AI Builder offre un eccellente set di elementi essenziali da includere nel prompt.

Come si può notare, include i seguenti elementi:

- **Attività**: un'**istruzione** che indica al modello GPT (Generative Pre-trained Transformer) l'attività da eseguire
- **Contesto**: descrivere i **dati** su cui si opera, insieme a eventuali **variabili** di input
- **Aspettative**: comunicare a GPT **obiettivi** e **aspettative** sulla risposta
- **Output**: aiutare GPT a formattare l'**output** nel modo desiderato

![Uno screenshot della sezione dedicata agli elementi del prompt nella guida all'ingegneria dei prompt di AI Builder. Attività, contesto, aspettative e output sono evidenziati come elementi del prompt.](../Media/4-prompt-engineering-guide.png)

## Attività 1: progettare un prompt

In questa attività, verrà progettato un prompt che permette di creare un piano di sviluppo professionale, basato sulle attività cardine della carriera.

> [!IMPORTANT]
> Per creare un prompt, non è necessario iniziare da zero. Sebbene sia molto utile conoscere le tecniche per scrivere un buon prompt, può essere vantaggioso partire da una base che porti già a metà strada.
> Sono già disponibili esempi di prompt nella [Galleria delle soluzioni di esempio di Microsoft Adoption](https://aka.ms/power-prompts). In questo esercizio, verrà usato l'esempio del [Prompt del Piano di sviluppo professionale](https://adoption.microsoft.com/sample-solution-gallery/sample/pnp-powerplatform-prompts-professional-development/).

Aggiungere tutti gli elementi del prompt:

- **Attività**: progettare un piano di sviluppo professionale.
- **Contesto**: per coloro che desiderano raggiungere i seguenti obiettivi di carriera.
- **Aspettative**: il piano deve includere obiettivi, risorse, strumenti e una sequenza temporale per le attività.
- **Output**: il piano dovrebbe essere chiaro, pratico e facile da seguire, con indicazioni concise e adatte a un dipendente junior.

Insieme, il prompt risultante sarebbe il seguente:

*Progetta un piano di sviluppo professionale per una persona che desidera raggiungere i seguenti [traguardi] di carriera. Il piano deve includere obiettivi, risorse, strumenti e una sequenza temporale delle attività. Struttura il piano in modo che sia conciso, pratico e facile da seguire, con informazioni chiare e adatte a un dipendente junior.*

## Attività 2: creare un'azione di prompt in Copilot Studio

Dopo aver completato la scrittura del prompt, è possibile immetterlo in Copilot Studio.

1. Nel browser Web, passare a [Copilot Studio](https://copilotstudio.microsoft.com) e, se richiesto, effettuare l'accesso con l'account aziendale o dell'istituto di istruzione.  Selezionare **Ignora** per ignorare eventuali messaggi di benvenuto.

    **Nota:** alla prima apertura di Copilot Studio, potrebbe essere visualizzata un'interfaccia di chat per creare il primo copilota. In questo caso, selezionare il menu **…** in alto a destra (accanto al pulsante **Crea**), quindi selezionare **Annulla creazione copilota** e quindi **Esci** per uscire dall'interfaccia della chat e visualizzare la home page di Copilot Studio.
1. Nel riquadro di spostamento a sinistra, selezionare **Raccolta**. Da questa schermata, è possibile visualizzare un elenco di azioni e connettori esistenti, oltre a crearne di nuovi.
1. Selezionare **Aggiungi un elemento** nella parte superiore.  Un menu elenca 2 opzioni per estendere Copilot per Microsoft 365.
:::image type="content" source="../Media/extend copilot options.png" alt-text="La finestra mostra 2 opzioni per l'estensione di Copilot: creare un copilota oppure creare un'azione.":::
1. Seleziona **Nuova azione**.
1. Nella schermata *Nuova azione*, selezionare **Prompt**. Verrà aperto il generatore di prompt di AI Builder.
1. Nella pagina **Dettagli azione**, immettere "Piano di sviluppo professionale" come **nome dell'azione**.
1. Inserire la seguente **descrizione**: "Crea un piano di sviluppo professionale pratico basato sui traguardi di carriera desiderati."
1. Selezionare **Avanti**.
1. Nella sezione **prompt** della pagina **Aggiungi un'azione prompt**, inserire "Progetta un piano di sviluppo professionale per una persona che intende raggiungere i seguenti [traguardi] di carriera. Il piano deve includere obiettivi, risorse, strumenti e una sequenza temporale per le attività. Il piano dovrebbe essere chiaro, pratico e facile da seguire, con indicazioni concise e adatte a un dipendente junior." come **prompt**.

    > [!NOTE]
    > Tenere presente che, nella parte superiore, è presente una barra informativa che indica che il prompt deve includere almeno un valore dinamico

1. In **Impostazioni prompt** nella barra laterale destra, aprire la sezione **Input**.
1. Selezionare il pulsante **Aggiungi input** per aggiungere un input.
1. Immettere `milestones` come nome dell'input.
1. Aggiungere il testo seguente come dati di esempio:

      ```text
      * Become medior in 3 years
      * Have 3 top reviews in a row
      * Become a manager in 10 years
      ```

1. Selezionare **[traguardi]** nella sezione prompt con il cursore.
1. Selezionare **Inserisci**.
1. Selezionare **traguardi**.

      **[traguardi]** verrà modificato in un valore dinamico.

1. Ora, è possibile testare il prompt.

## Attività 3: testare il prompt nel generatore di prompt

1. Selezionare **Testa prompt** sotto la sezione prompt. Il prompt sarà testato usando i dati di esempio aggiunti in precedenza.

    > [!NOTE]
    > Il prompt verrà inviato al modello di intelligenza artificiale, e la risposta generata sarà visualizzata nella sezione dedicata alle risposte dell'intelligenza artificiale. Questo consente di osservare la risposta generata da LLM e di valutare il livello di soddisfazione rispetto ai risultati ottenuti.

1. Se la risposta generata dall’intelligenza artificiale è soddisfacente, selezionare l’opzione **Salva prompt personalizzato** per salvare il prompt.

    Nella finestra successiva, è possibile visualizzare la descrizione del plug-in e la specifica degli input richiesti.

1. Nella pagina **Seleziona parametro azione**, aggiornare la descrizione dell'input relativo ai **traguardi** come segue:

      ```text
      The career milestones that the user wants to achieve
      ```

1. Selezionare **Avanti**.

1. Selezionare **Pubblica** per pubblicare l'azione in Microsoft 365 Copilot.  L'operazione potrebbe richiedere alcuni minuti.

## Attività 4: usare il plug-in di prompt in Microsoft 365 Copilot

Dopo aver creato e testato l'azione di prompt, procedere con l'attività successiva per renderla disponibile in Microsoft 365 Copilot.  La visualizzazione del plug-in in Microsoft 365 Copilot può richiedere un minimo di 5 minuti.

1. Aprire [Microsoft Teams](https://teams.microsoft.com).
1. Nella barra di spostamento a sinistra, selezionare **Copilot**.
1. Selezionare l'icona **Gestione delle risposte di Copilot** situata nella parte inferiore dello schermo, accanto all’area per l’invio dei messaggi a Copilot.
1. Nel menu a comparsa, cercare **Copilot Studio** e assicurarsi che sia abilitato.  
1. Selezionare l'**icona del cursore** per espandere l'elenco delle azioni in Copilot Studio.

    > [!NOTE]
    > È possibile che Copilot Studio non sia visibile. Ci possono essere due possibili motivi: l'amministratore potrebbe non aver distribuito l'app integrata Copilot Studio, oppure il plug-in potrebbe non essere ancora stato indicizzato; in questo caso, potrebbe essere necessario attendere un po' più a lungo.

2. Nella sezione Copilot Studio, cercare l'azione denominata **Piano di sviluppo professionale** nell'elenco delle azioni e selezionare l'interruttore accanto per abilitarla.

    > [!NOTE]
    > Se Piano di sviluppo professionale non è visibile nell'elenco dei plug-in in Copilot Studio, potrebbe essere necessario attendere un po' di tempo affinché venga visualizzato. La visualizzazione in Microsoft 365 Copilot potrebbe richiedere un po' più di tempo.

3. Dopo aver abilitato l'azione Piano di sviluppo professionale, sarà possibile usarla in Copilot. **È possibile testare l'azione** inviando il seguente messaggio a Copilot in Teams: "Vorrei generare un piano di sviluppo professionale per raggiungere i seguenti traguardi di carriera: 1: migliorare le mie competenze come marketer e 2: aumentare le possibilità di promozione al ruolo di senior marketer".

**Suggerimento:** per abilitare la modalità sviluppatore in Copilot, immettere `-developer on` nella chat.  Questo consente di vedere quando Copilot usa un plug-in per rispondere nella chat.
