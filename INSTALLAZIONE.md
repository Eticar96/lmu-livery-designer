# Guida all'installazione

Leggi questa pagina prima di scaricare: dura due minuti e ti evita l'unico momento in cui
l'installazione sembra andare storta — e non va storta.

---

## Cosa ti serve

| | |
|---|---|
| Sistema | Windows 10 o Windows 11, a 64 bit |
| Spazio su disco | circa **3 GB** durante l'installazione, **1,4 GB** dopo |
| Internet | serve **una volta sola**, per attivare la chiave |
| Le Mans Ultimate | installato, se vuoi caricare le livree direttamente in gioco |

Il download pesa 1,2 GB. Non è un errore: dentro ci sono le mappe già pronte di tutte le
vetture, ed è il motivo per cui l'app lavora veloce e **senza scaricare altro** dopo.

---

## ⚠️ Windows mostrerà un avviso. È normale, ed ecco perché

Quando apri il file scaricato, Windows mostra una finestra blu:

```
  ┌──────────────────────────────────────────────────┐
  │  Windows ha protetto il PC                       │
  │                                                  │
  │  Microsoft Defender SmartScreen ha impedito       │
  │  l'avvio di un'app non riconosciuta. L'esecuzione │
  │  di questa app potrebbe mettere a rischio il PC.  │
  │                                                  │
  │                    ┌──────────────┐               │
  │                    │ Non eseguire │               │
  │                    └──────────────┘               │
  └──────────────────────────────────────────────────┘
```

**Per procedere**: clicca su **Ulteriori informazioni** (il testo piccolo sotto il messaggio),
poi sul pulsante **Esegui comunque** che compare.

### Perché succede

Windows non sta dicendo che il programma è pericoloso: sta dicendo che **non lo conosce**.
Quel riconoscimento si compra — è un *certificato di firma del codice*, un'autenticazione a
pagamento con rinnovo annuale che gli editori software acquistano da enti certificatori. Livery
Designer è sviluppato da una persona sola e quel certificato non è ancora stato acquistato: il
prezzo finirebbe sul prezzo della licenza.

Lo stesso avviso compare su qualunque programma nuovo non firmato, inclusi molti strumenti usati
dalla comunità sim racing. Sparirà da sé quando il certificato verrà acquistato.

### Se l'antivirus mette il file in quarantena

Può succedere con gli antivirus più aggressivi, per la stessa ragione: file nuovo, nessuna
reputazione. Ripristina il file dalla quarantena e aggiungi un'eccezione, oppure scrivi su
[Discord](https://discord.gg/emM5QUXczS) e ti aiuto.

---

## Cosa puoi verificare prima di installare, se vuoi

Sono controlli che puoi fare da solo, senza fidarti sulla parola.

**1. Scarica solo da qui.** L'unico indirizzo ufficiale è
`github.com/Eticar96/lmu-livery-designer`. Non esistono mirror, non esistono altri link: se trovi
questo file altrove, non è stato messo lì da me.

**2. Controlla l'impronta del file.** Ogni file ha un codice univoco: se cambia anche un solo
byte, il codice cambia. Apri PowerShell nella cartella dei download e scrivi:

```powershell
Get-FileHash .\LiveryDesigner_v1418_CRIPTATA.exe -Algorithm SHA256
```

Deve uscire esattamente:

```
B661F28CF8EBEB41112EAFED32DAAB7D8952F1ABD41398871034D512BBB9668B
```

Se non combacia, **non installarlo** e avvisami.

**3. Guarda chi dichiara di averlo fatto.** Tasto destro sul file → *Proprietà* → *Dettagli*:
alla voce *Società* leggerai `LiveryDesigner`, alla voce *Versione file* `1.4.18`.

---

## Cosa fa l'installazione, in chiaro

- Copia l'app in `C:\Program Files\Livery Designer CRIPTATA` (chiede i permessi di
  amministratore, come ogni programma che scrive lì).
- Crea i tuoi dati — livree salvate, cache, impostazioni — in
  `%LOCALAPPDATA%\LiveryDesigner`, cioè dentro il tuo profilo utente.
- Aggiunge un collegamento nel menu Start.
- Copia il **manuale in PDF** accanto all'app: dentro Livery Designer il pulsante
  **Manuale** lo apre, e funziona anche senza internet.
- **Non** installa servizi in background, **non** modifica il gioco, **non** tocca file di
  sistema. Quando l'app è chiusa, non gira nulla.

### E la rete?

L'app contatta un solo indirizzo, e solo per la licenza:

- **all'attivazione**, una volta: invia la chiave e un'impronta del computer — un codice
  calcolato, non il tuo nome, non la tua email, non i tuoi file;
- **mentre l'app è aperta**, un controllo periodico che la licenza sia ancora valida.

Nessun dato sulle tue livree esce dal tuo PC. I progetti restano sul tuo disco.

---

## Installazione, passo per passo

1. **Scarica** `LiveryDesigner_v1418_CRIPTATA.exe` dalla
   [pagina delle release](https://github.com/Eticar96/lmu-livery-designer/releases/latest).
2. **Aprilo**. Compare l'avviso blu: *Ulteriori informazioni* → *Esegui comunque*.
3. **Conferma** la richiesta di permessi di Windows (è l'installazione in Program Files).
4. Segui l'installazione. Dura qualche minuto: sta scompattando 1,4 GB.
5. **Apri Livery Designer** dal menu Start.
6. L'app chiede una **chiave**. Incolla quella che ti ho mandato e premi Attiva. Serve internet
   solo in questo momento.
7. Fatto. Da qui in poi segui il [manuale](MANUALE.md).

### Per disinstallare

*Impostazioni → App → App installate → Livery Designer CRIPTATA → Disinstalla.* Le livree che
hai salvato restano nella tua cartella utente: non vengono cancellate.

---

## Se qualcosa non va

Scrivimi su **[Discord](https://discord.gg/emM5QUXczS)**, in privato. Dimmi a che punto ti sei
fermato e cosa hai letto sullo schermo: nella maggior parte dei casi si risolve in due messaggi.
