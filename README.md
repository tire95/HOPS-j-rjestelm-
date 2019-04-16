# Ohjelmistotekniikka, harjoitustyö - HOPS

Sovelluksen avulla opiskelija pystyy seuraamaan opintojensa edistymistä.

Sovelluksen käynnistyessä käyttäjä voi kirjautua sisään käyttäjätunnuksella, luoda uuden käyttäjän, tai siirtyä admin-tilaan admin-salasanalla.

Kirjauduttuaan sisään käyttäjä näkee kurssisuorituksensa ja voi lisätä itselleen kurssisuorituksia.

Admin-tilassa tietokannasta voi poistaa opiskelijoita; kun opiskelija poistetaan järjestelmästä, tähän liittyvät kurssisuoritukset poistetaan samalla.

## Dokumentaatio

[Vaatimusmäärittely](https://github.com/tire95/HOPS/blob/master/dokumentointi/vaatimusmaarittely.md)

[Työaikakirjanpito](https://github.com/tire95/HOPS/blob/master/dokumentointi/tyoaikakirjanpito.md)

[Arkkitehtuuri](https://github.com/tire95/HOPS/blob/master/dokumentointi/arkkitehtuuri.md)

## Komentorivitoiminnot

### Testaus

Testit suoritetaan komennolla

	mvn test

Testikattavuus luodaan komennolla

	mvn jacoco:report

Kattavuusraporttia voi tarkastella tiedostosta *target/site/jacoco/index.html*

### Suoritus komentoriviltä

Ohjelman suoritus komentoriviltä onnistuu komennolla

	mvn compile exec:java -Dexec.mainClass=ui.HOPSUi

### Suoritettavan jarin luonti

Suoritettava jar voidaan luoda komennolla

	mvn package

Luotu jar-tiedosto, *HOPS-1.0-SNAPSHOT.jar*, löytyy kansiosta *target*

### Checkstyle

Checktylen tarkistukset suoritetaan komennolla

	mvn jxr:jxr checkstyle:checkstyle

Checkstylen voi tarkastella tiedostosta *target/site/checkstyle.html*
