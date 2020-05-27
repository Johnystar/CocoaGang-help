# mpv

![zde má být obrázek mpv loga](mpv-logo.png)

## Proč mpv

mpv má několik výhod jako třeba podporu [přehrávání i YouTube videí, Twitch streamů, ...](instalace-youtube.md) a built-in podporu na Syncplay chat. Nevýhodou ovšem může pro některé být, že většina ovládání se skrývá za klávesovými zkratkami, ty ovšem po naučení se fungují vždy a jsou rychlejší než používat myš.

## Ovládání mpv

Základy ovládání (americké rozložení klávesnice):

- soubory otevřeš přetažením do mpv (online přetažením jejich URL adresy)
- zastavit/pustit - ``mezerník``
- 5 sekund dozadu/dopředu - ``šipka vlevo``/``šipka vpravo``
- celá obrazovka - ``f``
- zeslabit/zesílit - horní tlačítka ``9``/``0`` (proto americké rozložení klávesnice)

[Další zkratky jsou v angličtině popsány zde v oficiálním webovém manuálu mpv](https://mpv.io/manual/master/#keyboard-control), případně lze také dohledat neoficiální (a bohužel i potenciálně zastaralé) obrázky [na Googlu](https://www.google.com/search?q=mpv+keybindings).

## Instalace mpv

### Windows - instalace mpv

(poznámka pro technicky zdatnější: v této sekci instalujeme mpv přes scoop.sh, protože shinchiro buildy se Syncplayem nefungují: <https://github.com/Syncplay/syncplay/issues/313>)

- v Start menu vyhledej "Windows Powershell" a otevři:
	- ``Set-ExecutionPolicy RemoteSigned -scope CurrentUser`` a potvrď (vyber tu nejvíce kladnou možnost - chceš provést změny) (po potvrzení by se nic dalšího vypsat již nemělo)
	- ``Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')``
	- ``scoop install https://raw.githubusercontent.com/lukesampson/scoop-extras/master/bucket/mpv.json``
		- <u>pokud se ti vypíše</u> něco jako ``Ke vzdálenému serveru se nelze připojit.``, pokračuj následovně (pokud ne, tak vše fungovalo a máš hotovo)
		- ``scoop uninstall mpv``
		- počkej třeba 5 minut a zkus poslední příkaz (``scoop install https://raw.githubusercontent.com/lukesampson/scoop-extras/master/bucket/mpv.json``)
		- pokud to stále vypisuje ``Ke vzdálenému serveru se nelze připojit.``, tak buď to můžeš zkusit ještě jednou (zase ten uninstall a potom install) nebo mi napiš

### Linux - Debian (Ubuntu, Mint, Elementary, Pop!os, ...) - instalace mpv

- v terminálu:
	- ``sudo apt get update && sudo apt get upgrade && sudo apt install -y mpv``