# Respiro

App Android di supporto durante la chemioterapia per il tumore al polmone:
routine del giorno, respirazione guidata, diario dei sintomi, calendario delle cure,
promemoria con notifiche e guide pratiche riassunte da AIMaC e WALCE.

I dati restano salvati solo sul telefono dove l'app è installata.

## Scaricare l'APK

1. Apri la pagina **Releases** di questo repository dal telefono.
2. Scarica `ForzaMamma.apk` dall'ultima versione.
3. Aprilo e conferma l'installazione. La prima volta Android chiede di permettere
   l'installazione di app da questa fonte (browser o app File).
4. Al primo avvio consenti le notifiche.

Ogni modifica caricata sul ramo `main` crea in automatico una nuova versione.
Si installa sopra la precedente senza perdere i dati.

## Come è fatta

- `www/index.html` — l'app (HTML, CSS e JavaScript, senza dipendenze esterne)
- `android/` — progetto Android generato con Capacitor 8
- `.github/workflows/apk.yml` — compila e firma l'APK su GitHub Actions
- `android/app/respiro.keystore` — chiave di firma: serve per installare gli
  aggiornamenti sopra la versione esistente. Tieni il repository **privato**.

Per compilare in locale: `npm ci && npx cap sync android`, poi apri la cartella
`android` con Android Studio.

Le informazioni sanitarie sono generali e non sostituiscono il parere del medico.
