# Esercizio: creare un'azione di conversazione

In questo esercizio, verrà creata un'azione di conversazione che fornisce informazioni su un progetto organizzativo fittizio denominato "Project ABC".

Esercizio:

- Creare un'azione di conversazione in Copilot Studio
- Pubblicare un'azione di conversazione in Microsoft Copilot
- Testare l'azione di conversazione in Microsoft Copilot

## Attività 1: (facoltativa) Testare l'esperienza predefinita

Per iniziare, porre una domanda su "Project ABC" in Microsoft 365 Copilot.

1. Aprire **Microsoft Teams** e accedere con l'account aziendale o dell'istituto di istruzione.

1. Selezionare **Chat** nella barra laterale.

1. Selezionare **Copilot** nel menu della chat.

1. Nella casella di composizione del messaggio, immettere `Who should I contact for questions about Project ABC?`

1. Tenere presente che Microsoft 365 Copilot attualmente non dispone di alcuna informazione su Project ABC.

## Attività 2: creare una nuova azione di conversazione

Per iniziare, configurare il nome, la soluzione e lo schema per una nuova azione di conversazione in Microsoft Copilot.

1. Nel browser Web, passare a [Copilot Studio](https://copilotstudio.microsoft.com) e, se richiesto, effettuare l'accesso con l'account aziendale o dell'istituto di istruzione.  Selezionare **Ignora** per ignorare eventuali messaggi di benvenuto.

    **Nota:** alla prima apertura di Copilot Studio, potrebbe essere visualizzata un'interfaccia di chat per creare il primo copilota. In questo caso, selezionare il menu **…** in alto a destra (accanto al pulsante **Crea**), quindi selezionare **Annulla creazione copilota** e quindi **Esci** per uscire dall'interfaccia della chat e visualizzare la home page di Copilot Studio.
1. Nel riquadro di spostamento a sinistra, selezionare **Raccolta**. Da questa schermata, è possibile visualizzare un elenco di azioni e connettori esistenti, oltre a crearne di nuovi.
1. Selezionare **Aggiungi un elemento** nella parte superiore.  Un menu elenca 2 opzioni per estendere Copilot per Microsoft 365.
:::image type="content" source="../Media/extend copilot options.png" alt-text="La finestra mostra 2 opzioni per l'estensione di Copilot: creare un copilota oppure creare un'azione.":::
1. Seleziona **Nuova azione**.

1. Selezionare **Conversazione** per creare un'azione di conversazione.

1. Nel campo **nome**, immettere `Project ABC` e accettare la soluzione e lo schema predefiniti.

1. Selezionare **Crea** per continuare. Verrà creata la nuova azione di conversazione. L'operazione può richiedere alcuni secondi. Al termine, si passerà all'area del contenuto per proseguire con la configurazione dell'azione.

## Attività 3: configurare l'argomento

Configurare quindi il nome e il trigger per l'argomento.

1. Nel riquadro di creazione delle azioni di conversazione, passare alla scheda **Argomenti**.

1. Selezionare la casella di testo **Nome argomento** nella parte superiore del riquadro, che contiene il nome predefinito `"Untitled"`, e inserire `Project ABC info` per denominare l'argomento.

1. Nel nodo **Trigger** all'interno dell'argomento, selezionare la casella di testo sotto la dicitura "Descrivere le operazioni dell'argomento" e inserire `Answers questions and provides information about Project ABC, including questions about objectives, points of contact, and rollout timeline.`.

## Attività 4: inviare un messaggio

Aggiungere quindi un nodo all'argomento per inviare un messaggio su Project ABC.

1. Nel nodo Trigger, selezionare l'icona **+** per aggiungere un nuovo nodo.

1. Nel menu visualizzato, selezionare **Invia un messaggio**.  Verrà creato un nodo messaggio.

1. Nel nodo messaggio, selezionare la casella di testo e immettere `Project ABC is an initiative aimed at improving the culture and engagement within the company.  Objectives of the project include improved morale, increased employee survey results, and improved culture ratings.  For more information about Project ABC, contact Devon Torres.`.

1. Selezionare **Salva** sopra l'area del contenuto per salvare le modifiche.

## Attività 5: pubblicare l'azione

Pubblicare quindi l'azione da usare in Microsoft 365 Copilot.

1. Selezionare **Pubblica** nella parte superiore della pagina.

1. Nella pagina **Pubblica plug-in**, selezionare **Pubblica**.

1. Nella pagina **Pubblicare il contenuto più recente?**, verificare che il plug-in Project ABC Info sia abilitato e selezionare **Pubblica**.  La pubblicazione può richiedere alcuni minuti.  Una notifica verrà visualizzata nella parte superiore della finestra al termine della pubblicazione.

## Attività 6: abilitare e testare l'azione

Infine, testare l'azione in Microsoft 365 Copilot.

1. Aprire **Microsoft Teams**.

1. Selezionare **Chat** nella barra laterale.

1. Selezionare **Copilot** nel menu della chat.

1. Nell'area di composizione del messaggio, selezionare il pulsante **Gestione delle risposte di Copilot**.

1. Nel riquadro a comparsa, cercare **Copilot Studio** e quindi selezionare **Aggiungi** per aggiungere Copilot Studio.
 
2. L'azione **Project ABC info** dovrebbe ora essere elencata nel riquadro a comparsa.  Verificare che **Project ABC info** sia abilitato e quindi chiudere il riquadro a comparsa.

:::image type="content" source="../Media/projectABCInfo-action-enabled.png" alt-text="Screenshot dell'azione Project ABC Info elencata in "Manage Copilot response" flyout in Teams.":::

3. Nella casella di composizione del messaggio, immettere `Who should I contact for questions about Project ABC?`

4. Tenere presente che Microsoft 365 Copilot restituisce informazioni su Project ABC richiamando l'azione di conversazione.

È possibile personalizzare o espandere questa azione di conversazione con nodi aggiuntivi.  Ad esempio, è possibile creare un nuovo nodo di **Risposte generative** e caricare un file, ampliando le informazioni disponibili per l'azione.

**Nota:** quando si testa l'azione in Copilot, tenere presente quanto segue:
- Copilot riformulerà sempre le risposte usando il proprio tono di voce. In questa versione di anteprima, non è possibile trasmettere il contenuto invariato all'utente finale.
- La descrizione dell'azione di conversazione è essenziale per assicurarne l'affidabilità di richiamo. La descrizione informa l'agente di orchestrazione in cosa è efficace il plug-in e quali risposte può fornire. Assicurati di utilizzare un testo chiaro quando scrivi la descrizione e valuta la possibilità di sperimentare modifiche per ottenere il miglior risultato.
- L'esecuzione accurata di questi passaggi non garantisce che Copilot restituisca sempre i risultati attesi.  Copilot determinerà quando richiamare il plug-in e come restituire i risultati.

## (Facoltativo) Sfida: crearne una propria

Applicare quanto appreso per creare, pubblicare e testare una nuova azione di conversazione per uno scenario a scelta.  Esaminare i passaggi di questo esercizio in base alle esigenze.