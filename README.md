# Menu scuola - Web App mobile

## Pubblicazione rapida con GitHub Pages
1. Creare un repository pubblico su GitHub.
2. Caricare nella radice tutti i file contenuti in questa cartella.
3. Aprire Settings > Pages.
4. In Build and deployment scegliere Deploy from a branch.
5. Selezionare branch main e cartella /root, quindi Save.
6. Condividere il link generato o trasformarlo in QR code.

## Modificare il menu
Aprire `menu-data.js` con un editor di testo e modificare solo il valore del piatto interessato, senza cambiare i nomi dei campi.
Per cambiare l'inizio del ciclo modificare `dataRiferimentoSettimana1`. La data deve essere un lunedi della settimana 1 nel formato AAAA-MM-GG.

## Aggiornamenti e cache
Dopo una modifica pubblicata, cambiare in `sw.js` il valore `menu-scuola-v1` in `menu-scuola-v2`, poi v3 e così via. Questo forza i telefoni a scaricare i dati aggiornati.

## Test locale
Il Service Worker richiede HTTPS o localhost. Per un test completo usare un piccolo server locale, ad esempio `python -m http.server 8000`, poi aprire `http://localhost:8000`.
