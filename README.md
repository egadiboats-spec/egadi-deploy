# egadi-deploy

Workflow di deploy per un repository privato. Qui non c'è codice del progetto: solo i passi per pubblicare una
versione già approvata. I job usano l'environment `production`, che richiede un'approvazione manuale e funziona
solo dal branch `main`; i secret arrivano al job solo dopo l'approvazione.

- **Deploy**: pubblica un tag `vX.Y.Z` del repository privato (deve essere su `main`).
- **Rollback**: torna a una release già presente sul server.

I log sono pubblici: i workflow stampano solo messaggi di stato.
