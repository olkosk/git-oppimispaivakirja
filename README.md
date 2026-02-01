Kurssin nimi:  Git-versionhallinta - SOF013AS2A-3002

Tekijä: Olli Koskeli

Sisältö: Repositorio sisältää opintojakson Oppimispäiväkirjat 1-3. 

- [Oppimispäiväkirja 1](paivakirja1.md)

Oppimispäiväkirja: Paikallinen git
Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?

Olin tutustunut GitHubiin aiemmalla Johdanto Digitaalisiin palveluihin-kurssilla ja olin joululomalla katsellut muutamia Gitin käyttöön liittyviä videoita. Olin myös asentanut Gitin jo ennakkoon, joten Harjoitus 1:ssä piti vain varmistaa että kaikki oli kunnossa. Koen että ymmärsin jo hieman Gitin ja versionhallinan logiikkaa ja tarkoitusta, mutta komentojen käyttämisestä minulla ei ollut kokemusta.

Harjoitus 2
Aloitin Harjoitus 2 tekemisen Git Bashissa. CLI:tä olen käyttänyt vain vähän joten peruskomentoja (mkdir, cd, echo yms.) piti kertailla. Olisin päässyt helpommalla tai ainakin nopeammalla jos olisin käyttänyt suoraan Editoria, mutta tulipa harjoiteltua ja kerrattua hieman CLI:n käyttöä. Loin kansion (mkdir), sinne test.txt-tiedoston (echo "jotain" >> test.txt) jonka jälkeen lisäsin tallensin sen (git add, git commit). Tein uuden tiedoston hello.html (echo "Hei maailma" >> hello.html). Minulla oli alkuun hieman hankaluuksia kun kikkailin Git Bashin ja VSC:n välillä (joka pomppasi esiin jos unohdin -m komennon lopusta). Tässä vaiheessa h1-muotoilua tehdessä vaihdoin GUI:n puolelle ja nöyrästi tein muutokset käsin. Vein muutokset (git add hello.html, git commit). Muutin tiedostonimeä (mv hello.html index.html) ja tallensin sen taas (git add index.html, git commit). Poistin ylimääräisen tiedoston (git rm text.txt) ja tallensin muutoksen (git commit -m "Poistettu tarpeettomana"). Lisäsin tiedostoja kuten testi2.txt, tiedosto2.txt hakemistoon ja tallensin niitä (git add + git commit). Lopussa tarkastelin talletuksia git log-komennolla ja sen laajentimella git log --stat, joista jälkimmäinen näytti montaa tiedostoa oli muutettu ja näytti insertioita(+). Lisäsin lopuksi tehtävään tunnisteen git tag harjoitus2.

Harjoitus 3
Tein repositorioon muutoksia, muutin tiedostoja ja tein jonkun uuden kansionkin. Näiden jälkeen tein git add testailua.txt ja git add tiedosto2.txt, jonka jälkeen git log sain aiempia muutoksia esille. Tässä sekoilin taas Git Bashin kanssa ja en tiedä oikein itsekään mitä hetken yritin, mutta lopulta Git status-komennolla sain 4 committia odottavaa tiedostoa, joista yksi on tiedosto2.txt, jonka jälkeen git reset tiedosto2.txt-komento ja uusi status kertoi että tiedosto2.txt oli hävinnyt committia odottavista tiedostoista. Tein taas useita muutoksia, etsin git log aiemman tilanteen ja git revert + seitsemän ensimmäistä merkkiä (cfd0880ac) hävitti untracked-tilassa olevat tiedostot niin ettei niitä enää näkynyt git status-komennolla. Log näyttää commitin jossa Revert "Testaillaan"-viestini näkyy. Tehtävää tehdessä tiesin kyllä mitä olin tekemässä, mutta komentojen (git log, git revert, add/commit-tilojen) kanssa oli hieman ongelmia. Lopuksi lisäsin tehtävään tunnisteen (git tag harjoitus3).

Harjoitus4
Olin kertaillut aiempia osioita ja siirtynyt täysin VSC:n. Huomasin että olin huomattavast itsevarmempi ja koen että aiempien osioiden kertailu teki hyvää. Lisäsin index.html-sivulle HTML-sivun perusrakenteen ja tallensin muutokset (git add, git commit). Tein styles.css-tiedoston, kopioin siihen tehtävän esimerkin, lisäsin index.html-tiedostoon vielä linkin tyylitiedostoon ja testasin sen toimivuuden. Tässä tein ensin virheen ja tallensin ensimmäisellä kerralla (git add, git commit) jolloin muutokset tallentuivat master-haaraan. Aloitin tehtävän alusta ja tein samalla tavalla, paitsi nyt loin tyylit-haaran (git branch tyylit), vaihdoin haaran (git switch tyylit) ja tallensin nyt muutokset tänne (git add, git commit). Vaihtelin master ja tyylit-haarojen välillä: muotoilut näkyivät tyylit-haarassa (otsikko keskellä, taustaväri muuttui) ja master-haarassa ei ollut muotoilua. Tämän jälkeen varmistin että olin master-haarassa (git status) yhdistin haarat (git merge --no-ff tyylit). Tämän jälkeen git switchillä vaihtaessa muotoilu näkyi molemmissa haaroissa. Lisäsin tunnisteen git tag harjoitus4.

Yhteenveto
Harjoitus 2 ja Harjoitus 3 tuntuivat hieman sekavilta (osin alun Git Bash-sekoilun takia) ja olin kokoajan hieman epävarma teinkö kaikki askeleet oikein ja menikö kaikki tehtävän talletukset ja vaiheet oikein. Pääsin kuitenkin tehtävien loppuun ja opin paljon uutta ja erityisesti tunnistin mitkä asiat eivät vielä ihan auenneet. Palasin kertaamaan vielä aiempia osioita ja etenkin tallennuksia ja git add / git commit-eroja. Kun toimin pelkästään VSC:ssä sain keskityttyä paremmin ja Harjoitus 4:ssä olin kokoajan hyvin kärryillä ja koin olevani kontrollissa. Opin paljon uutta Gitin ja versionhallinnan perusteista ja myös komentorivin käytöstä.

Osiossa käyttämäni Git-komennot
Komento	Kuvaus
git config	Gitin konfigurointiin liittyviä komentoja
git --version	Tulostaa asennetun Git-version tunnisteen
git init	Perustaa hakemiston repositorioon, joka ei ole vielä versiohallinnassa
git status	Kertoo repositorion Git-tilan
git add	Ensimmäinen vaihe muutoksen tallentamiseen: merkitsee muutoksen mukaan seuraavaan talletukseen ja kertoo mitä Gitille mitä sen tulee tallentaa (staging)
git commit (-m)	Toinen vaihe muutoksen tallentamiseen: varsinainen talletus (commit). Lisäämällä -m voi kirjoittaa muutosta kuvaavan kommentin komentorivillä
git log	Kertoo commit-talletusten historian
git rm	Poistaa tiedoston Git-hallinnasta ja työhakemistosta
git tag	Lisää tunnisteen tallletukseen
git reset	Poistaa add-komennon (staging) commitia odottavista muutoksista
git revert	Poistaa add-komennon (staging) commitia odottavista muutoksista
git branch	Luo uuden haaran
git switch	Vaihtaa haaraa
  
- [Oppimispäiväkirja 2](paivakirja2.md)

Oppimispäiväkirja: Hajautettu git
Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?

Tein GitHub-repositorion nimellä Git-versionhallinta ja annoin descriptioniksi “Git-versionhallintakurssia varten tehty repositorio.”. Laitoin sen yksityiseksi (private) ja en lisännyt README:ta kurssin tehtävän ohjeistuksen mukaan.

Repositorio-sivulla näky pyyntö README:n lisäämisestä ja collaboratoreiden lisäämisestä. Tämän alla oli ohjeistus setupiin. Annoin GitHubissa olleen komennon: git remote add origin https://github.com/olkosk/Git-versionhallinta.git

git branch -M main
git push -u origin main Ja aiemmin käyttämäni kansio tiedostoineen tuli näkyviin repositorioon.
Testasin git remote -v -komentoa ja näin asetukset.

Tarkastin haaran nimen, ja selvisi että Githubin ohjeistus oli vaihtanut haaran nimen masterista mainiksi (yllä). Vaihdoin nimen takaisin masteriksi (git branch -m master). Tämän jälkeen puskin paikallisen master-haaran GitHubiin komennolla git push origin master. Git branch kertoi että paikallisessa repositoriossa minulla on master ja tyylit- haarat. GitHubin Branches-välilehdellä näkyy että minulla on main-haara (default) (jonka loin repositorion luomisen yhteydessä) sekä master-haara.

Tein GitHubissa tiedoston “GitHubTiedosto”. Kun klikkasin Commit, järjestelmä loi automaattisen viestin “Add initial content to GitHubTiedosto” joka oli mielestäni validi. Valintoina oli myös tehdä commit suoraan main branchiin tai luoda uusi haara, joista valitsin ensimmäisen.

Tiedosto tallentui ja tein ohjeen mukaan komennot git fetch ja git checkout origin/master. Se näytti onnistuneen, mutta kertoi minun olevan “detached HEAD”-tilassa, jossa voin katsella ympäriinsä, tehdä muutoksia ja commiteja ja tehdä asioita ilman että vaikutan muihin haaroihin. Tässä mietin että etärepon luomisen yhteydessä push komennossakin oli main (eikä master). Git branch antoi *(HEAD detached at origin/master), master ja tyylit haarat. Kokeilin tehdä alussa tehdyn >> git push -u origin master-käskyn mutta se ei vaikuttanut mihinkään muuhun kun vaihtoi nimen.

Git status kertoi että olen up-to-date “origin/masterin” kanssa. Git merge origin/master sanoi myös samaa että olen up to date. Menin tarkastelemaan tilannetta GitHubiin ja olin tehnyt uuden tiedoston tuohon main branchiin, joka selittää hämmennyksen. Git pull, git merge origin/main, git push ja nyt tiedosto ilmestyi näkyviin. Ja tilanne on se mikä pitää. Tämä hämmennys johtui tosiaan GitHubin ohjeesta jonka kopioin, enkä tajunnut että se nimeää jo tuossa vaiheessa eri nimellä. Tuo hieman aiemmin tehty git push -u origin master ei enää korjannut tätä ongelmaa. Loppu hyvin kaikki hyvin, ja pääsin harrastamaan ongelmanratkaisua ja kertaamaan pull, merge ja push komennot. Vielä lopuksi git tag harjoitus5.

Osiossa käyttämäni Git-komennot
Komento	Kuvaus
git remote add	Lisää etärepositorio
git branch	Kertoo repon haaran
git push	Paikallisen repon tietojen vienti etärepositorioon
git pull	Lataa etäreposta kaikki muutokset joita ei vielä ole (sama kuin git fetch & git merge)
git fetch	Etärepositorion tietojen lataaminen paikalliseen repositorioon
git status	Kertoo repositorion Git-tilan
git switch	Vaihtaa haaraa
  
- [Oppimispäiväkirja 3](paivakirja3.md)

Oppimispäiväkirja: Git projektissa
Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?

Versionhallinta auttaa huolehtimaan, että voit palata aiempiin (toimiviin) versioihin eikä koodi pääse katoamaan. Sen avulla voi myös kehittää ja kokeilla erilaisia asioita ilman, että sotkee välttämättä koko projektia. Se auttaa myös erottamaan esimerkiksi kehitys- ja testausympäristön.

Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?

Samat kuin aiemmassa vastauksessa, mutta ylipäätään se ettei tiedostoja ja muutoksia tarvitse vaihdella muistitikuilla tai jollain muilla kömpelöillä ratkaisuilla. Eli voidaan tehdä töitä samaan aikaan järkevällä tavalla. Näkyvyys muiden työhön.

Miten järjestäisit projektitiimin versionhallinnan 3-4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan.

Luodaan tiimille yhteinen etärepositorio GitHubiin, jolle sovitaan haarat (ainakin main ja develop, yksilöillä omat develop-haarat eri kehitettäviin asioihin liittyen). Sovitaan yhteiset käytännöt kommentteihin, jotka on toki pakollisia. Pull requestien hyödyntäminen varsinkin mainiin yhdistäessä.

Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä, työmäärästä. Mitä toivoisit olevan enemmän, mitä vähemmän?

Kiitos opintojaksosta! Kurssi on varmasti todella hyödyllinen ja koin että opin itse todella paljon. Se auttoi myös tunnistamaan minkä aiheiden kanssa pitää vielä kertailla ja harjoitella lisää. Koen että opintojakso soveltui ihan hyvin opintojen alkuvaiheeseen, vaikka osittain varmasti lisäsi haastetta: se auttaa kuitenkin tulevaisuudessa paljon sillä nyt Git-taitoja voi harjoitella ja kerrata tulevilla opintojaksoilla ja omissa projekteissa. Aihe veti mukaansa ja tuli tehtyä tehtävät suhteellisen nopealla aikataululla. Erityisesti viimeiset Harjoitus 6 oli erityisen mielenkiintoinen ja opettavainen kun sai treenailla botin kanssa ja sai hieman käsitystä millaista työskentely tiimissä voisi olla: sen tyylisiä tehtäviä olisi voinut olla enemmänkin. Osa tehtävistä oli ehkä hieman epäselviä, tai oli ehkä hankala arvioida aloittelijana tuliko kaikki oikeat vaiheet tehtyä oikein. Myös oppimispäiväkirjojen kanssa kikkailu vaati paljon selvittelyä, sillä suora kopiointi ei onnistunut terminalissa ja sitten päädyin tekemään sen Forkilla GitHubissa (jota harjoiteltiin vasta viimeisessä tehtävässä). Kehityskaari Harjoituksesta 2 Harjoitukseen 7 oli hurjan iso ja opintojakso lisäsi kipinää jatkaa harjoittelua.
