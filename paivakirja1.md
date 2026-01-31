# Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__  

Olin tutustunut GitHubiin aiemmalla Johdanto Digitaalisiin palveluihin-kurssilla ja olin joululomalla katsellut muutamia Gitin käyttöön liittyviä videoita. Olin myös asentanut Gitin jo ennakkoon, joten Harjoitus 1:ssä piti vain varmistaa että kaikki oli kunnossa. Koen että ymmärsin jo hieman Gitin ja versionhallinan logiikkaa ja tarkoitusta, mutta komentojen käyttämisestä minulla ei ollut kokemusta.


## Harjoitus 2
Aloitin Harjoitus 2 tekemisen Git Bashissa. CLI:tä olen käyttänyt vain vähän joten peruskomentoja (mkdir, cd, echo yms.) piti kertailla. Olisin päässyt helpommalla tai ainakin nopeammalla jos olisin käyttänyt suoraan Editoria, mutta tulipa harjoiteltua ja kerrattua hieman CLI:n käyttöä. Loin kansion (mkdir), sinne test.txt-tiedoston (echo "jotain" >> test.txt) jonka jälkeen lisäsin tallensin sen (git add, git commit). Tein uuden tiedoston hello.html (echo "Hei maailma" >> hello.html). Minulla oli alkuun hieman hankaluuksia kun kikkailin Git Bashin ja VSC:n välillä (joka pomppasi esiin jos unohdin -m komennon lopusta). Tässä vaiheessa h1-muotoilua tehdessä vaihdoin GUI:n puolelle ja nöyrästi tein muutokset käsin. Vein muutokset (git add hello.html, git commit). Muutin tiedostonimeä (mv hello.html index.html) ja tallensin sen taas (git add index.html, git commit). Poistin ylimääräisen tiedoston (git rm text.txt) ja tallensin muutoksen (git commit -m "Poistettu tarpeettomana"). Lisäsin tiedostoja kuten testi2.txt, tiedosto2.txt hakemistoon ja tallensin niitä (git add + git commit). Lopussa tarkastelin talletuksia git log-komennolla ja sen laajentimella git log --stat, joista jälkimmäinen näytti montaa tiedostoa oli muutettu ja näytti insertioita(+). Lisäsin lopuksi tehtävään tunnisteen git tag harjoitus2.


## Harjoitus 3
Tein repositorioon muutoksia, muutin tiedostoja ja tein jonkun uuden kansionkin. Näiden jälkeen tein git add testailua.txt ja git add tiedosto2.txt, jonka jälkeen git log sain aiempia muutoksia esille. Tässä sekoilin taas Git Bashin kanssa ja en tiedä oikein itsekään mitä hetken yritin, mutta lopulta Git status-komennolla sain 4 committia odottavaa tiedostoa, joista yksi on tiedosto2.txt, jonka jälkeen git reset tiedosto2.txt-komento ja uusi status kertoi että tiedosto2.txt oli hävinnyt committia odottavista tiedostoista. Tein taas useita muutoksia, etsin git log aiemman tilanteen ja git revert + seitsemän ensimmäistä merkkiä (cfd0880ac) hävitti untracked-tilassa olevat tiedostot niin ettei niitä enää näkynyt git status-komennolla. Log näyttää commitin jossa Revert "Testaillaan"-viestini näkyy. Tehtävää tehdessä tiesin kyllä mitä olin tekemässä, mutta komentojen (git log, git revert, add/commit-tilojen) kanssa oli hieman ongelmia. Lopuksi lisäsin tehtävään tunnisteen (git tag harjoitus3).


## Harjoitus4
Olin kertaillut aiempia osioita ja siirtynyt täysin VSC:n. Huomasin että olin huomattavast itsevarmempi ja koen että aiempien osioiden kertailu teki hyvää. Lisäsin index.html-sivulle HTML-sivun perusrakenteen ja tallensin muutokset (git add, git commit). Tein styles.css-tiedoston, kopioin siihen tehtävän esimerkin, lisäsin index.html-tiedostoon vielä linkin tyylitiedostoon ja testasin sen toimivuuden. Tässä tein ensin virheen ja tallensin ensimmäisellä kerralla (git add, git commit) jolloin muutokset tallentuivat master-haaraan. Aloitin tehtävän alusta ja tein samalla tavalla, paitsi nyt loin tyylit-haaran (git branch tyylit), vaihdoin haaran (git switch tyylit) ja tallensin nyt muutokset tänne (git add, git commit). Vaihtelin master ja tyylit-haarojen välillä: muotoilut näkyivät tyylit-haarassa (otsikko keskellä, taustaväri muuttui) ja master-haarassa ei ollut muotoilua. Tämän jälkeen varmistin että olin master-haarassa (git status) yhdistin haarat (git merge --no-ff tyylit). Tämän jälkeen git switchillä vaihtaessa muotoilu näkyi molemmissa haaroissa. Lisäsin tunnisteen git tag harjoitus4.


## Yhteenveto
Harjoitus 2 ja Harjoitus 3 tuntuivat hieman sekavilta (osin alun Git Bash-sekoilun takia) ja olin kokoajan hieman epävarma teinkö kaikki askeleet oikein ja menikö kaikki tehtävän talletukset ja vaiheet oikein. Pääsin kuitenkin tehtävien loppuun ja opin paljon uutta ja erityisesti tunnistin mitkä asiat eivät vielä ihan auenneet. Palasin kertaamaan vielä aiempia osioita ja etenkin tallennuksia ja git add / git commit-eroja. Kun toimin pelkästään VSC:ssä sain keskityttyä paremmin ja Harjoitus 4:ssä olin kokoajan hyvin kärryillä ja koin olevani kontrollissa. Opin paljon uutta Gitin ja versionhallinnan perusteista ja myös komentorivin käytöstä.  


## Osiossa käyttämäni Git-komennot


| Komento | Kuvaus |
| --------| ------ |
| git config | Gitin konfigurointiin liittyviä komentoja |
| git --version | Tulostaa asennetun Git-version tunnisteen |
| git init | Perustaa hakemiston repositorioon, joka ei ole vielä versiohallinnassa |
| git status | Kertoo repositorion Git-tilan |
| git add | Ensimmäinen vaihe muutoksen tallentamiseen: merkitsee muutoksen mukaan seuraavaan talletukseen ja kertoo mitä Gitille mitä sen tulee tallentaa (staging) |
| git commit (-m) | Toinen vaihe muutoksen tallentamiseen: varsinainen talletus (commit). Lisäämällä -m voi kirjoittaa muutosta kuvaavan kommentin komentorivillä |
| git log | Kertoo commit-talletusten historian |
| git rm | Poistaa tiedoston Git-hallinnasta ja työhakemistosta |
| git tag | Lisää tunnisteen tallletukseen |
| git reset | Poistaa add-komennon (staging) commitia odottavista muutoksista |
| git revert | Poistaa add-komennon (staging) commitia odottavista muutoksista |
| git branch | Luo uuden haaran |
| git switch | Vaihtaa haaraa |
