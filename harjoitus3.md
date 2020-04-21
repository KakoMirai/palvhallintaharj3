# Palvelinten hallinta harjoitus 3

Tehtävän tekijä: Tommi Muhonen

Tässä harjoituksessa harjoitellaan versionhallintaa.

Raportoin Tero Karvisen Palvelinten Hallinta-kurssin kolmatta tehtävää.

Käyttämäni rauta:

* Nvidia GTX 1080 8gb
* Intel i7 8700K

Käyttöjärjestelmä: Xubuntu 18.04.3 LTS x64

Suoritin tämän harjoituksen kotona.

### MarkDownin käyttäminen raportin luomiseen
Aloitin ajamalla peruskomennot ja pistin Saltin semmoiseen tilaan, että minioni vastasi "sudo salt '*' cmd.run whoami" komentoon. Sen jälkeen menin GitHubiin ja loin uuden repon jonka nimeksi annoin "palvhallintaharj3".

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/1.png)

Kloonasin tämän xubuntuun komennolla "git clone https://github.com/KakoMirai/palvhallintaharj3.git".

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/2.png)

Määrittelen tässä vaiheessa käyttäjätiedot jotta kaikki toimisi hyvin. Ajan komennot "git config --global (user.name/user.email) "maili tai nimi"" . Tämän jälkeen siirryin repon kansioon ja loin sinne tiedoston "harjoitus3.md" joka on tämä raportti jota kirjoitan. Tallensin tämä tiedoston ja siirsin sen repoon komennolla "git add . && git commit; git pull && git push". Näin tiedostot siirtyvät minun kotikoneeni kotikansiosta suoraan GitHubiin. 

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/3.png)

### Gitin komentoja
`Git log`Tämä komento näyttää kaikki repoon ajetut muutokset ja commitit. Jokaisesta commitista näkyy commitin token, commitin ajaja, commitin aika ja commitin ajajan kommentti, tässä esimerkkinä kun aloitin kirjoittamaan raporttia koneen kansiosta.

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/4.png)

`git diff`Tämä komentoo kertoo mitä muutoksia on tehty ja mikä on paikallisen hakemiston ja repon ero. Tässä tapauksessa loin muutaman muutoksen readme tiedostoon.

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/diff.png)

`git blame` Tämä komento on juuri sitä mitä se on. Tällä voi katsoa kuka on kirjoittanut minkäkin rivin tiedostoon. Tässä esimerkkinä minun muutokseni readme tiedostoon.

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/5.png)

### Muutoksen peruminen hakemistosta ennen committia
Haluan perua muutokseni jotka loin readme tiedostoon joten ajan komennon "git reset --hard" jollon tuli tälläinen ilmoitus ja tämä tarkoittaa sitä, että muutokset jotka loin peruuntuivat.

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/6.png)

### Uusi moduuli
Ajattelin luoda uuden moduulin jolla asennan simppelin ohjelman jota esimerkiksi pienessä yrityksessä jossa tehdään paljon pientä kuvanmuokkausta voitaisiin käyttää. Loin uuden kansion komennolla "sudo mkdir /srv/salt/gimp/". Loin kansion sisälle tekstitiedoston gimp.init jonne annoin määrityksen asentaa tämän ohjelman.

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/7.png)

Sitten ajoin tämän moduulin minioneille komennolla "sudo salt '*' state.apply gimp" ja asennus onnistui. Kokeilin vielä kerran samalla komennolla jotta voidaan varmistää, että se asentui ja tulos oli hyvä.

![alt text](https://github.com/KakoMirai/palvhallintaharj3/blob/master/8.png)

Ajoin vielä komennon "gimp" jolloin ohjelma aukesi minulle.

### Lähteet:
* http://terokarvinen.com/2020/configuration-managment-systems-palvelinten-hallinta-ict4tn022-spring-2020/#h3-versionhallinta
* https://tommimuhonen334781833.wordpress.com/
