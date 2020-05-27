# Instalace

Pro účast jednoho z promítání Cocoa Gang Cinema potřebuješ:

- Syncplay
- kompatibilní mediální přehravač

## Syncplay

### Windows

- [Stáhneš zde](https://syncplay.pl/)

### Linux - Debian (Ubuntu, Mint, Elementary, Pop!os, ...)

(technická poznámka: ačkoliv tento způsob není příliš noob-friendly, syncplay není v základních apt repositories a snap verze blbne/nefunguje/není stabilní)

- stáhni první Source code tar.gz (budeš muset trochu zaskrolovat než to najdeš pravděpodobně)
- extrahuj
- otevři terminál v extrahované složce:
	- ``sudo apt get update && sudo apt get upgrade && sudo apt install -y python3 python3-pip python3-twisted python3-pyside2.qtwidgets python3-certifi git make``
	- ``python3 -m pip install -U pyopenssl service_identity idna``
	- ``sudo make install``

## Kompatibilní multimediální přehravače

### mpv - funguje se Syncplayem nejlépe

#### Windows

(poznámka pro technicky zdatnější: v této sekci instalujeme mpv přes scoop.sh, protože shinchiro buildy se Syncplayem nefungují: <https://github.com/Syncplay/syncplay/issues/313)>)

- v Start menu vyhledej "Windows Powershell" a otevři:
	- ``Set-ExecutionPolicy RemoteSigned -scope CurrentUser`` a potvrď
	- ``Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')``
	- ``scoop install https://raw.githubusercontent.com/lukesampson/scoop-extras/master/bucket/mpv.json``

#### Linux - Debian (Ubuntu, Mint, Elementary, Pop!os, ...)

- v terminálu:
	- ``sudo apt get update && sudo apt get upgrade && sudo apt install -y mpv``

### VLC - univerzální alternativa

#### Windows

- [Zde](https://www.videolan.org/vlc/download-windows.html) klikni vedle "Download VLC" na šipku dolů a zvol "Installer for 64bit version"

#### Linux - Debian (Ubuntu, Mint, Elementary, Pop!os, ...)

- v terminálu:
w

### Jiné

Pokud jen trochu možné tak **silně nedoporučuji** používat nic jiného než VLC nebo mpv (s tím že mpv funguje nejlépe, akorát má na Windowsu lehce komplikovanější, ačokliv stále jednoduchou, instalaci).

Na stránce Syncplay si lze najít že podporují také MPC-HC a MPC-BE, oba tyto přehravače mají ovšem různé nevýhody oproti VLC i mpv.

mpv má několik výhod jako třeba podporu [přehrávání i YouTube videí, Twitch streamů, ...](instalace-youtube.md) a built-in podporu na Syncplay chat. Nevýhodou ovšem může pro některé být, že většina ovládání se skrývá za klávesovými zkratkami, ty ovšem po naučení se fungují vždy a jsou rychlejší než používat myš.
