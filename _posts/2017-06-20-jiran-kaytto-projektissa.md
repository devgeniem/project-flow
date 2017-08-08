---
layout: page
title: "Jiran käyttö projektissa"
category: kehitys
date: 2017-06-20 16:02:54
order: 4
---

## Yleistä

- Ennen kuin alat tehdä issueta, varmista että siinä on työarvio. Lisää, jollei ole.
- Jos/kun huomaat ettet ehdi tehdä issueta ajassa joka siihen on arvioitu (Original Estimate), ilmoita tästä projektipäällikölle
- Käyttäjätarinan saa siirtää QA-tilaan vasta kun kaikki tarinan subtaskit ovat myös samassa tilassa. Testaaja ei voi muuten testata

Tiimi on vastuussa kollektiivisesti issueista ja niiden valmistumisesta. Muita kehittäjiä autetaan, jotta sprintin hommat saadaan tehtyä. “Ei ole minun vastuulla” -lause ei kuulu tiimityöskentelyyn.

## Jira Workflow

### To Do
- sprinttiin valitut issuet
- ei tarvitse noudattaa mitään prioriteettijärjestystä, kunhan pitää mielessä/kyseenalaistaa mikä on sprintissä oleellisinta ja aloittaa siitä. ei jää tärkeimmät asiat kesken, jos jotain kesken jää
- pitää olla kaikki tarvittava tieto, jotta issuen voi tehdä. muuten ei oteta sprinttiin

### In Progress
- parhaillaan teossa olevat issuet
- otat yhden issuen työn alle, teet sen, ja sitten seuraava. ei roikoteta tässä montaa taski. Jos taskin eteneminen pysähtyy jostain syystä niin issuen voi siirtää esim Pending tilaan.
- ennen siirtoa:
-- Code review tilaan
-- oma tuotos on testattu
-- docs päivitetty
-- testausohje lisätty taskiin
-- tunnit logattu taskiin

### Code review
- koodi on arvioitavana lead devaajalla

### Pending
- on jokin este, jonka vuoksi issueta ei voi edistää (esim. puuttuu tietoa asiakkaalta, tai issue odottaa toisen devaajan työpanosta, tai kaksi issueta joista toinen odottaa toisen valmistumista)
- lisää kommentti miksi pending, mitä odotetaan, keneltä
- kun siirrät tähän tilaan, huolehdi että henkilö jolta odotetaan tietoa/tekemistä on tietoinen, että issue odottaa häntä
- scrum master huomaa tästä helpommin jos on jonkin issuen kanssa esteitä ja niiden selvittäminen ei unohdu
- kehitystiimi informoi scrum masteria pending-tilassa olevista issueista

### Rework
- aina prioriteettina 1
- jos sprintin jälkeen jää reworkkia, ne tehdään ennen kuin aloitetaan seuraavaan sprintin hommia
- tähän siirretään tarvittaessa tavaraa QA:sta -> projari tai testaaja siirtää

### QA
- kun issue on tässä tilassa, devaaja on deployannut sen stagelle
- lisää tarvittaessa testausohjeet issueeseen, esim jos pitää testata kirjautumista -> testitunnukset
- projari/testaaja käy tästä läpi issuet. testataan stagelta
- jos jotain vikaa/paranneltavaa -> kommenttiin "Rework: “ + selitys mitä pitää tehdä. sen jälkeen siirto Reworkkiin
- jos issue ok, siirto Ready for Live

### Ready for Live
- issuet on testattu ja ne saa deployata tuotantoversioon

### Closed
- kun issue on tässä tilassa, devaaja on deployannut sen tuotantoon
- tästä käydään asiakkaan kanssa läpi issuet sprintin lopetuksessa
- jos tässä vaiheessa vielä vikaa -> reworkkiin
- jos selkeästi lisäfeature, tehdään uusi issue backlogiin
- issue voidaan siirtää Closed-tilaan myös muussa tilanteessa, esimerkiksi päätettäessä ettei kyseistä toimintoa toteuteta

## Jatkokehityksen Jira Workflow

Jatkokehitysprojekteissa on käytössä Kanban board. Kanbanin käyttöä jatkokehityksessä tukee:

- versioiden julkaisu
- jatkokehityksessä ei ole tarvetta jakaa töitä sprintteihin
- tulee turhaa työtä ja “keinotekoisia” sprinttejä jos käytetään scrum boardia
- näin ollen helpompi, että kaikki työt näkyy todossa/backlogissa

### Backlog

- issueeseen lisätään hankitaan tarvittavat määritykset asiakkaalta ja työarvio, hyväksytetään toteutus asiakkaalla

### Ready for development

- kun issue on tässä kohtaa, kehittäjä saa ottaa sen tekoon
- kaikki vaadittava tieto on olemassa, työarvio tehty ja asiakas on kuitannut työarvion

### In Progress

- parhaillaan teossa olevat issuet
- otat yhden issuen työn alle, teet sen, ja sitten seuraava. ei roikoteta tässä montaa issueta. Jos taskin eteneminen pysähtyy jostain syystä, siirrä issue Pending-tilaan ja kirjaa syy kommenttiin.

### Code review
- koodi on arvioitavana lead devaajalla

### Pending

- on jokin este, jonka vuoksi issueta ei voi edistää (esim. puuttuu tietoa asiakkaalta, tai issue odottaa toisen devaajan työpanosta, tai kaksi issueta joista toinen odottaa toisen valmistumista)
- lisää kommentti miksi pending, mitä odotetaan, keneltä
- kun siirrät tähän tilaan, huolehdi että henkilö jolta odotetaan tietoa/tekemistä on tietoinen, että issue odottaa häntä
- projektipäällikkö huomaa tästä helpommin jos on jonkin issuen kanssa esteitä ja niiden selvittäminen ei unohdu
- kehitystiimi informoi scrum masteria pending-tilassa olevista issueista

### Rework

- aina prioriteettina 1
- tähän siirretään tarvittaessa tavaraa QA:sta -> projektipäällikkö tai testaaja siirtää

### QA

- kun issue on tässä tilassa, kehittäjä on päivittänyt sen stagelle
- lisää tarvittaessa testausohjeet issueeseen, esim jos pitää testata kirjautumista -> lisää testitunnukset
- testaaja käy tästä läpi issuet. testataan stagelta
- jos jotain vikaa/paranneltavaa -> kommenttiin "Rework: “ + selitys mitä pitää tehdä. sen jälkeen siirto Reworkkiin
- jos issue ok, siirto Ready for Review

### Ready for Review

- issue on stagella
- asiakas hyväksyy/hylkää issuen tässä kohtaa

### Ready for Live

- asiakas on hyväksynyt issuen
- issue on valmis vietäväksi tuotantoon

### Closed

- kun issue on tässä tilassa, kehittäjä on päivittänyt sen tuotantoon
- issue voidaan siirtää Closed-tilaan myös muussa tilanteessa, esimerkiksi päätettäessä ettei kyseistä toimintoa toteuteta


