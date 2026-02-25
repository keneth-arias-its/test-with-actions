## Step 3: Attiva i workflow

Come specificato nei nostri workflow, verranno eseguiti solo quando una pull request è diretta verso il branch `main`.

Le pull request hanno un bel vantaggio quando c'è un workflow associato. Lo stato dell'esecuzione e i risultati possono essere visualizzati direttamente nel feed della conversazione.

### ⌨️ Attività: Avvia una PR e proponi una modifica al codice

1. Ritorna al Codespace di VS Code.

1. Crea un nuovo branch basato su `main` con il seguente nome e **pubblicalo** su GitHub.

   ```txt
   reenable-unit-test
   ```

1. Controlla di essere sul branch `reenable-unit-test`, quindi apri il file `tests/calculations_test.py`.

1. Dopo aver esaminato il codice, vediamo un test commentato alla riga 56. Rimuovi il commento per riabilitarlo.

   > Speriamo non sia stato disabilitato per evitare i test!

   ```py
   def test_get_nth_fibonacci_ten():
    """Test with n=10."""
    # Arrange
    n = 10

    # Act
    result = get_nth_fibonacci(n)

    # Assert
    assert result == 89
   ```

1. Fai il commit delle modifiche ed esegui il push su GitHub.

1. Ritorna al browser e crea una pull request. Usa i seguenti dettagli.

   - **base:** `main`
   - **source:** `reenable-unit-test`
   - **title**: `Reenable unit test that was disabled`

   <br/>
   <details>
   <summary><b>Hai dei problemi:</b> Non riesci a creare una pull request? 🤷‍♂️</summary>

   Hai fatto per errore un commit sul branch `main`? Ecco un comando per annullare l'ultimo commit e forzare l'aggiornamento del repository su GitHub. Fai attenzione però a non tornare indietro di troppi step! Non vorrai mica rimuovere i tuoi nuovi workflow!

   ```bash
   git reset --hard HEAD~1
   git push -f
   ```

1. Dopo che la pull request è stata creata, guarda vicino al pulsante Merge per vedere molti workflow in esecuzione.

   - Il nostro workflow di copertura fallirà, facendoci sapere che abbiamo un test da correggere.

1. Con la pull request avviata, Mona dovrebbe essere impegnata a controllare il tuo lavoro e a preparare i prossimi step.

<details>
<summary>Hai dei problemi?  🤷‍♂️</summary>

- Se i controlli non appaiono aggiornati, prova ad aggiornare la pagina. È possibile che il workflow sia stato eseguito e la pagina non sia stata ancora aggiornata con la modifica.

</details>
