## Passo 1: Continuous Integration

Le GitHub Actions sono un ottimo modo per automatizzare molte delle tue attività ricorrenti, facendoti risparmiare tempo per lavorare su problemi più stimolanti e divertenti!

Uno dei compiti più comuni che uno sviluppatore affronta è testare il proprio codice. Sfortunatamente, questo è spesso noioso e certe cose vengono saltate o semplicemente trascurate. Ancora peggio, spesso abbiamo bisogno di testare contro molti framework, sistemi operativi e altre situazioni, incrementando il problema.

Impariamo come automatizzare questa crescente necessità di testare il nostro codice utilizzando i workflow nelle GitHub Actions.

> [!NOTE]
> Se vuoi saperne di più, controlla queste risorse:
> - [Comprendere le GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)
> - [Eventi che attivano i workflow](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows)
> - [Prezzi dei runner per le action](https://docs.github.com/en/billing/reference/actions-runner-pricing)

### Cos'è la Continuous Integration?

La [Continuous integration](https://it.wikipedia.org/wiki/Integrazione_continua) può aiutarti ad attenerti agli standard di qualità del tuo team eseguendo i test e riportando i risultati su GitHub. Gli strumenti di CI eseguono build e test, attivati dai commit. I risultati sulla qualità vengono pubblicati di nuovo su GitHub nella pull request. L'obiettivo è avere meno problemi in `main` e feedback più veloci mentre lavori.

### ⌨️ Attività: Avvia la nostra applicazione Python di esempio

1. Usa il pulsante qui sotto per aprire la pagina **Create Codespace** in una nuova scheda. Usa la configurazione predefinita.

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

1. Conferma che il campo **Repository** sia la tua copia dell'esercizio, non l'originale, quindi fai clic sul pulsante verde **Create Codespace**.

   - ✅ La tua copia: `/{{full_repo_name}}`
   - ❌ Originale: `/skills/test-with-actions`

1. Attendi un momento che Visual Studio Code si carichi nel tuo browser.

1. Nella navigazione a sinistra, seleziona la scheda **Explorer** per mostrare i file del progetto.

1. Apri i file `src/calculations.py` e `tests/calculation_tests.py`.

1. Prenditi un momento per leggere questi file per familiarizzare.

1. Espandi il pannello del terminale integrato di VS Code.

   > 💡 **Suggerimento**: La scorciatoia da tastiera è `CTRL` + `J`.

1. Esegui il comando sottostante per creare un ambiente virtuale, quindi installa le librerie Python e gli strumenti richiesti per verificare la copertura del codice.

   ```bash
   python -m venv .venv/calculations
   source .venv/calculations/bin/activate
   pip install -r requirements.txt
   pip install pytest coverage pytest-cov
   ```

1. Esegui il comando sottostante per avviare tutti gli unit test e visualizzare le informazioni sulla copertura.

   ```bash
   pytest --cov=src --verbose
   ```

1. Aggiungi un commento in questa issue per far sapere a Mona i risultati del tuo report di copertura. Dopo averlo revisionato, fornirà i prossimi step.

   ```md
   @professortocat, I've run my coverage report.
   Seems there is some opportunity to increase the test coverage. 🧐
   What should we do next?
   ```
