---
layout: page
title: "Pienkehitys ja jatkokehitys"
category: huolenpito
date: 2017-04-28 13:38:25
order: 3
---

## Pienkehitys

Kun palvelua on tarve jatkokehittää alle viiden henkilötyöpäivän verran, puhutaan pienkehityksestä. Pienkehitystä voi tilata sähköpostitse.


## Jatkokehitys

Kun palvelua on tarve jatkokehittää yli viiden henkilötyöpäivän verran, puhutaan jatkokehityksestä. Jatkokehitys projektoidaan omaksi kokonaisuudekseen.


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

### Done

- kun issue on tässä tilassa, kehittäjä on päivittänyt sen tuotantoon
