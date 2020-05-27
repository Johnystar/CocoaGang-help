# YouTube videa a další

Na přehrávání online videí přes Syncplay potřebuješ:

- youtube-dl (instalace popsána níže)
- mpv ([návod k instalaci zde](instalace-zaklad.md#mpv-funguje-se-syncplayem-nejlepe))

Po nastavení lze přes Syncplay sledovat vše co youtube-dl zvládne, například:

- YouTube (videa, kanály, playlisty, livestreamy, ..)
- Twitch (klipy, streamy, videa, ...)
- Reddit (posty)
- Vimeo (videa, alba, kanály, ...)
- Twitter (broadcasty, ...)
- [obrovskou hromadu dalších](https://ytdl-org.github.io/youtube-dl/supportedsites.html) (skoro až moc xd)

Ano, instalace není triviální, ale rozjede to ve výsledku skoro cokoliv. V případě problémů se obraťte na Johnystar.

## Instalace youtube-dl

**Poznámka**: youtube-dl je skvělá terminálová aplikace napsaná v Pythonu. mpv ji používá pro získávání videí a streamů z cílových stránek. Jako terminálová aplikace funguje velmi dobře a je rychlejší na stahování videí než webové stránky - pokud máš zájem tak tě rád naučím ji používat!

### Windows

Link na stránku s Pythonem: <https://www.python.org/downloads/>. Zaskroluj úplně dolů dokud nenajdeš tohle:

![rip obrázek, chjo](python-verze.png)

Jakmile vybereš tu správnou verzi a klikneš na ní (v případě obrázku klikneš na text "Python 3.(něco)"), tak zaskroluj dolů dokud nenajdeš tohle:

![rip obrázek, chjo](python-64.png)

Tak jak je na obrázku naznačeno, chceš vybrat verzi "Windows x86-64 executable installer".

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

## Jak použít

Normálně když chceš pustit přes Syncplay video za pomocí mpv:

- zapneš Syncplay
- připojíš se
- do mpv přesuneš soubor

Online videa se pouští podobně (je více způsobů, ale tento je noob-friendly, jednoduchý na pochopení a i na popsání):

- zapneš Syncplay
- připojíš se
- (najdeš si URL videa, playlistu, streamu, ... na který se chceš podívat)
- přesuneš URL (text) do mpv (buď přímo z URL baru prolížeče a nebo například z textového editoru - označíš a přetáhneš do mpv)
