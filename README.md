# Projekt-3
#Elections Scraper

Treti projekt - Python akademie Engeto

Urcen k vytezeni vysledku voleb v CR z roku 2017 v okrese Benesov.
`https://volby.cz/pls/ps2017nss/ps3?xjazyk=CZ`

# Zadani projektu:
Napiš takový skript, který vybere jakýkoliv územní celek z tohoto odkazu https://volby.cz/pls/ps2017nss/ps3?xjazyk=CZ

Např. Benešov https://volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101 aka <odkaz_uzemniho_celku>.

Z tohoto odkazu chcete vyscrapovat výsledky hlasování pro všechny obce a ulozit je do souboru csv <benesov.csv>.

Ve výstupu (benesov.csv) každý řádek obsahuje informace pro konkrétní obec.
Tedy podobu:
- kód obce
- název obce
- voliči v seznamu
- vydané obálky
- platné hlasy
- kandidující strany (co sloupec, to počet hlasů pro stranu pro všechny strany).

Knihovny v souboru `requirements.txt`.

`.\venv\Scripts\activate`

`pip install requests beautifulsoup4`

`pip freeze > requirements.txt`

`pip install -r requirements.txt`

Virtualni prostredi s managerem:
`pip --version`
`pip install -r requirements.txt`

Spusteni souboru 
`project_3.py` # pozaduje dva povinne argumenty.
`python projekt_3.py <odkaz-uzemniho-celku>  <vysledny-soubor>` # Vystup je .csv

Vysledky pro Benesov:
1.argument <odkaz-uzemniho-celku>: https://volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101

ampersand (&) issue ?
URL po uprave : `https://volby.cz/pls/ps2017nss/ps32?xjazyk=CZ"&"xkraj=2"&"xnumnuts=2101`

2.agrument  <vysledny-soubor>: `volby_benesov`

# buh vi co to bude delat...
- `python projekt_3.py https://volby.cz/pls/ps2017nss/ps32?xjazyk=CZ"&"xkraj=2"&"xnumnuts=2101 volby_benesov benesov.csv`

nebo

- `python projekt_3.py "https://volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101" volby_benesov benesov.csv`

