# Oppimispäiväkirja: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Tein GitHub-repositorion nimellä Git-versionhallinta ja annoin descriptioniksi “Git-versionhallintakurssia varten tehty repositorio.”. Laitoin sen yksityiseksi (private) ja en lisännyt README:ta kurssin tehtävän ohjeistuksen mukaan.

Repositorio-sivulla näky pyyntö README:n lisäämisestä ja collaboratoreiden lisäämisestä. Tämän alla oli ohjeistus setupiin. Annoin GitHubissa olleen komennon:
git remote add origin https://github.com/olkosk/Git-versionhallinta.git
>> git branch -M main        
>> git push -u origin main
Ja aiemmin käyttämäni kansio tiedostoineen tuli näkyviin repositorioon.  
Testasin git remote -v -komentoa ja näin asetukset.  

Tarkastin haaran nimen, ja selvisi että Githubin ohjeistus oli vaihtanut haaran nimen masterista mainiksi (yllä). Vaihdoin nimen takaisin masteriksi (git branch -m master). Tämän jälkeen puskin paikallisen master-haaran GitHubiin komennolla git push origin master.
Git branch kertoi että paikallisessa repositoriossa minulla on master ja tyylit- haarat. GitHubin Branches-välilehdellä näkyy että minulla on main-haara (default) (jonka loin repositorion luomisen yhteydessä) sekä master-haara. 

Tein GitHubissa tiedoston “GitHubTiedosto”. Kun klikkasin Commit, järjestelmä loi automaattisen viestin “Add initial content to GitHubTiedosto” joka oli mielestäni validi. Valintoina oli myös tehdä commit suoraan main branchiin tai luoda uusi haara, joista valitsin ensimmäisen.

Tiedosto tallentui ja tein ohjeen mukaan komennot git fetch ja git checkout origin/master. Se näytti onnistuneen, mutta kertoi minun olevan “detached HEAD”-tilassa, jossa voin katsella ympäriinsä, tehdä muutoksia ja commiteja ja tehdä asioita ilman että vaikutan muihin haaroihin. Tässä mietin että etärepon luomisen yhteydessä push komennossakin oli main (eikä master). Git branch antoi *(HEAD detached at origin/master), master ja tyylit haarat. 
Kokeilin tehdä alussa tehdyn >> git push -u origin master-käskyn mutta se ei vaikuttanut mihinkään muuhun kun vaihtoi nimen. 

Git status kertoi että olen up-to-date “origin/masterin” kanssa. Git merge origin/master sanoi myös samaa että olen up to date. Menin tarkastelemaan tilannetta GitHubiin ja olin tehnyt uuden tiedoston tuohon main branchiin, joka selittää hämmennyksen. Git pull, git merge origin/main, git push ja nyt tiedosto ilmestyi näkyviin. Ja tilanne on se mikä pitää. Tämä hämmennys johtui tosiaan GitHubin ohjeesta jonka kopioin, enkä tajunnut että se nimeää jo tuossa vaiheessa eri nimellä. Tuo hieman aiemmin tehty git push -u origin master ei enää korjannut tätä ongelmaa. Loppu hyvin kaikki hyvin, ja pääsin harrastamaan ongelmanratkaisua ja kertaamaan pull, merge ja push komennot. Vielä lopuksi git tag harjoitus5. 

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| git remote add | Lisää etärepositorio |
| git branch | Kertoo repon haaran |
| git push | Paikallisen repon tietojen vienti etärepositorioon |
| git pull | Lataa etäreposta kaikki muutokset joita ei vielä ole (sama kuin git fetch & git merge) |
| git fetch | Etärepositorion tietojen lataaminen paikalliseen repositorioon |
| git status | Kertoo repositorion Git-tilan |
| git switch | Vaihtaa haaraa |
