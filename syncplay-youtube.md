# Jak rozjet YouTube videa přes Syncplay

## Nainstaluj si youtube-dl

### Windows

- <https://www.python.org/downloads/> - NE HORNÍ TLAČÍTKO, místo toho list "Looking for a specific release?" a vyber nejnovější verzi vlevo, zaskroluj dolů k "Files" a vyber "Windows x86-64 executable installer"
- instalace:
  - customize installation
  - pip ANO
  - for all users ANO
  - next
  - add Python to environment variables ANO
  - precompile standard library ANO
  - neměň cestu instalace!
  - install
- ve Start menu vyhledej CMD, klikni pravým a otevří jako správce/administrátor
- do CMD zadej:
  - ``python -m pip install -U youtube-dl``

### Linux - Debian (Ubuntu, Mint, Elementary, Pop!os, ...)

- v terminálu:
  - ``sudo apt get update && sudo apt get upgrade && sudo apt install -y python3 python3-pip ffmpeg``
  - ``python3 -m pip install -U youtube-dl``

## Nainstaluj si mpv

### Windows

(poznámka pro technicky zdatnější: v této sekci instalujeme mpv přes scoop.sh, protože shinchiro buildy se Syncplayem nefungují: <https://github.com/Syncplay/syncplay/issues/313)>

- v Start menu vyhledej "Windows Powershell" a otevři:
  - ``Set-ExecutionPolicy RemoteSigned -scope CurrentUser`` a potvrď
  - ``Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')``
  - ``scoop install https://raw.githubusercontent.com/lukesampson/scoop-extras/master/bucket/mpv.json``

### Linux - Debian (Ubuntu, Mint, Elementary, Pop!os, ...)

- v terminálu:
  - ``sudo apt get update && sudo apt get upgrade && sudo apt install -y mpv``

(technická poznámka: pokud instaluješ mpv hned po youtube-dl, tak opětovný update a upgrade potřeba není, ovšem z důvodu zjednodušení postupu to sem píšu i tak)

## FAQ k instalaci

**Q** - Proč je to tak složitý?

**A** - Na Linuxu stačí v obou případech pouze překopírovat pár příkazů do terminálu. Na Windowsu se to komplikuje tou nutností nainstalovat Python. Problém je, že první co oficiální stránka Python nejdřív nabídne je 32-bitová instalačka, potom instalace samotná je složitější než na Linuxu kvůli zastaralé Windowsácké infrastruktuře a jedno s druhým. Neznám žádný způsob jak to na Windowsu ulehčit bez psaní automatizovaného skriptu nebo používání metod potenciálně vedoucích k nestabilním a špatně aktualizovatelným výsledkům.
