# YouTube videa

Na přehrávání YouTube videí přes Syncplay potřebuješ:

- youtube-dl (instalace popsána níže)
- mpv ([návod k instalaci zde](instalace-zaklad.md#mpv-funguje-se-syncplayem-nejlepe))

## youtube-dl

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
