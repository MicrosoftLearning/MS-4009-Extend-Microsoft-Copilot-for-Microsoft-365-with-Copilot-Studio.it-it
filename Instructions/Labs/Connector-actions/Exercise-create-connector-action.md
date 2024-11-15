# Esercizio: creare un'azione del connettore

In questo esercizio si eseguiranno le seguenti operazioni:

- Creare un'azione del connettore in Copilot Studio
- Testare l'azione del connettore in Microsoft Teams
- Salvare e pubblicare l'azione del connettore

## Attività 1: creare un'azione del connettore in Copilot Studio

In questa attività, verrà configurata un'azione del connettore per il connettore MSN Meteo.

1. Passare a [Copilot Studio](https://copilotstudio.microsoft.com) e accedere con l'account aziendale o dell'istituto di istruzione, se richiesto. Ignorare eventuali messaggi di benvenuto.

    **Nota:** alla prima apertura di Copilot Studio, potrebbe essere visualizzata un'interfaccia di chat per creare il primo copilota. In questo caso, selezionare il menu **…** in alto a destra (accanto al pulsante **Crea**), quindi selezionare **Annulla creazione copilota** per uscire dall'interfaccia della chat e visualizzare la home page di Copilot Studio.
1. Nel riquadro di spostamento a sinistra, selezionare **Raccolta**. Da questa schermata, è possibile visualizzare un elenco di azioni e connettori esistenti, oltre a crearne di nuovi.
1. Selezionare **Aggiungi un elemento** nella parte superiore.  Un menu elenca 2 opzioni per estendere Copilot per Microsoft 365.
:::image type="content" source="../Media/extend copilot options.png" alt-text="La finestra mostra 2 opzioni per l'estensione di Copilot: creare un copilota oppure creare un'azione.":::
2. Seleziona **Nuova azione**.
3. Selezionare **Connettore** per aprire la procedura guidata per le azioni del connettore.
4. Selezionare **MSN Meteo** come connettore.
5. **Esaminare** la descrizione.

    > [!IMPORTANT]
    > Questa descrizione è fondamentale, poiché Copilot utilizzerà questa opzione per associare il messaggio dell'utente al plug-in appropriato. Se la descrizione non è adeguata, Copilot potrebbe non attivare correttamente l'azione del connettore.

1. Selezionare **Avanti**.
1. Seleziona l'azione **Recupera meteo corrente**.
1. **Esaminare** la descrizione dell'azione.

    > [!IMPORTANT]
    > Esaminare la descrizione dell'azione nella schermata seguente. Questa descrizione dell'azione è essenziale, poiché Copilot userà questa opzione per associare il messaggio dell'utente all'azione corretta. Se la descrizione dell'azione non è chiara, Copilot potrebbe attivare l'azione errata.

1. Selezionare **Avanti**.
1. **Esaminare** le descrizioni di tutti gli input e gli output.

    > [!IMPORTANT]
    > Esaminare le descrizioni di input e output nella schermata seguente. Le descrizioni di input e output sono fondamentali, poiché Copilot le userà per attivare correttamente il connettore (input) e per generare una risposta valida per l'utente (output). Se le descrizioni di input e output non sono chiare, Copilot potrebbe non attivare correttamente il connettore o potrebbe non fornire una risposta valida.

1. Selezionare **Avanti**.
1. Verrà quindi visualizzata una schermata in cui sarà possibile aggiungere altre azioni, se necessario; in questo caso, però, l'operazione verrà ignorata e sarà necessario selezionare **Avanti**.

## Attività 2: testare l'azione del connettore in Microsoft Teams

In questa attività verrà testata l'azione del connettore configurata nell'attività 1 in Microsoft 365 Copilot in Microsoft Teams.

![La sezione di revisione, test e pubblicazione dell'azione nella procedura guidata per l'azione del connettore.](../Media/connect-test.png)

1. Selezionare una connessione esistente, se disponibile, oppure selezionare **Nuova connessione** per creare una nuova connessione per il connettore MSN Meteo.
1. Dal menu **Nuova connessione**, selezionare **Crea**.
1. In **Connessione selezionata**, è ora possibile selezionare la nuova connessione dal menu a discesa.
1. Selezionare il pulsante **Testa l'azione**.

    > [!NOTE]
    > Verrà attivato un processo in cui l'azione del connettore verrà distribuita in Microsoft Teams, rendendola disponibile per il test.

1. Selezionare **Disponibile per il test** per avviare il test.

    > [!NOTE]
    > Verrà aperta una nuova scheda del browser che proverà ad avviare Microsoft Teams.

1. È possibile selezionare **Annulla** nel popup che tenta di avviare Microsoft Teams.
1. Selezionare **Usa l'app Web**.

    > [!NOTE]
    > Microsoft 365 Copilot verrà aperto in Microsoft Teams.

1. Nell'area di composizione del messaggio in Copilot su Teams, selezionare l'icona del **plug-in** accanto all'icona di invio.
1. Individuare il plug-in **Test-MSN Meteo** e selezionare l'interruttore per abilitarlo.

    > [!NOTE]
    > Verrà visualizzato il messaggio seguente.

    ![Il messaggio visualizza che il plug-in Test-MSN Meteo è attivo.](../Media/test-msn-weather.png)


1.  Inviare il seguente messaggio a Microsoft 365 Copilot, inserendo i valori desiderati per posizione e unità.

    ```text
    What is the current weather in <your location> in <celsius/fahrenheit> according to MSN Weather?
    ```

1. Se la configurazione è stata completata correttamente, Copilot risponderà con un messaggio generato tramite il plug-in.  

   ![Uno screenshot con un esempio di domanda e risposta. Il plug-in fornirà le condizioni meteorologiche attuali per Utrecht, Paesi Bassi, in gradi Celsius.](../Media/msn-weather-result.png)

   **Nota:** Copilot potrebbe richiedere l'autorizzazione prima di usare il plug-in.  Selezionare **Consenti sempre** per autorizzare Copilot all'uso del plug-in.

   :::image type="content" source="../Media/test-msn-weather-allow.png" alt-text="Screenshot di Copilot che richiede l'autorizzazione per l'uso del plug-in.":::

## Attività 3: salvare e pubblicare l'azione del connettore

In questa attività verrà salvata e pubblicata l'azione del connettore.

Verrà esaminato il punto in cui si era rimasti in Copilot Studio.

1. Selezionare **Avanti** nella procedura guidata per pubblicare l'azione del connettore.

    > [!NOTE]
    > Nella schermata successiva sarà possibile accedere ai dettagli oppure selezionare Salva e chiudi. Come indicato nel messaggio, potrebbero essere necessari alcuni minuti prima che l'azione sia visibile nelle esperienze di Copilot.

      ![Uno screenshot della schermata di pubblicazione nella procedura guidata per l'azione del connettore.](../Media/connector-action-finished.png)
   
1. Selezionare **Salva e chiudi**.

L'azione del connettore è stata configurata e pubblicata correttamente.
