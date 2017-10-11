---
layout: page
title: "Tekninen toteutus"
category: kehitys
date: 2017-04-28 13:30:52
order: 2
---

## Yleistä

Projektit toteutetaan yleensä kehitysjaksoissa joita kutsutaan sprinteiksi. Yhden sprintin pituus on lähes poikkeuksetta 2 viikkoa. Sprinttien määrä riippuu projektin laajuudesta. 

Projektin käyttäjätarinoiden ja muiden tehtävien hallintaan käytetään Jira-nimistä tehtävienhallintaohjelmistoa.

## Sprintin eteneminen

1. Sprintin aluksi kehitystiimi ja asiakas kokoontuvat sprintin aloitukseen.
2. Kehitystiimi työskentelee sprintin keston ajan. Sprintin aikana toteutuvat kehitystyön lisäksi seuraavat asiat:
  * Design review  
  * Code review  
  * Sprintin käyttäjätarinoiden ja taskien testaus  
3. Sprintin lopuksi kehitystiimi ja asiakas kokoontuvat katselmoimaan sprintin tuloksen. Kehitystiimi esittelee tuotoksensa asiakkalle. Lopuksi pidetään retrospektiivi eli retro, jossa käydään läpi missä onnistuttiin sprintin aikana ja missä olisi kehitettävää.

Seuraavassa on kuvattu kaikki sprinttipalaverit tarkemmin.

### Sprintin suunnittelu

**Kesto:** 2-4 h  
**Ketä on paikalla:** service designer + projektipäällikkö + kehitystiimi + asiakkaan edustaja

Tavoite: service designer + projektipäällikkö + asiakkaan edustaja
- mitä pystytään tekemään backlogista seuraavan sprintin aikana (valitaan käyttäjätarinat + muut mahdolliset muut issuet (kuten tekniset taskit) sprinttiin)
- mitä tarvitsee tehdä jotta sprintin tavoiteltu tuotos saavutetaan

Töiden suunnittelu: kehitystiimi
- tiimi tekee käyttäjätarinoiden teknisen suunnittelun, purkaa tarinat subtaskeihin (kts. vaatimusmäärittelyt ja issuet) ja päivittää subtaskeille työarviot

### Sprintin katselmointi

**Kesto:** max 2-3h  
**Ketä on paikalla:** projektipäällikkö + kehitystiimi + asiakkaan edustaja

Tarkoitus:
- tiimi kertoo mitkä tehtävät on tehty ja demoaa ne
- pohdinta mitä tehdään seuraavaksi (antaa pohjaa sprint planningiin)

Kehitystiimi valmistautuu huolella esittelemään tehdyn työn. Varmista, että käyttäjätarinan hyväksymiskriteerit täyttyvät ja pystyt demoamaan ne.

### Retro

**Kesto:** max 1h  
**Ketä on paikalla:** projektipäällikkö + service designer + kehitystiimi + asiakkaan edustaja

Tavoite:
- selvittää miten edellinen sprintti sujui, koskien ihmisiä, suhteita, prosesseja ja työkaluja
- mikä meni hyvin, missä olisi parantamisen varaa
- päätetään mitkä parannukset toteutetaan ja sovitaan mitä tehdään jotta parannukset saavutetaan


### Kehitystiimin päivittäinen statuscheck

**Milloin:** joka päivä aikavälillä klo 13-14
**Kesto:** max 1h
**Ketä on paikalla:** projektipäällikkö + kehitystiimi + lead developer. 

Jos lead developer on leadina useammassa projektissa, eri projektien kehittäjät kokoontuvat eri aikoina välillä klo 13-14. Lead developer hoitaa aikataulutuksen.

Tarkoitus:
- yhdistetty "daily meetup" + lead developerin päivittäinen statuscheck
- tiedonjako
- ongelmat ja esteet selville

Mitä:
- koko tiimi kokoontuu ja puhuu keskenään.
- jos todetaan ettei ole asiaa -> suoraan jatkamaan töitä

Osa 1: Projektin pääkohdat läpi
	- mitä teit eilen
	- mitä aiot saavuttaa seuraavaan statuscheckiin mennessä
	- Jira board
	- ollaanko aikataulussa
	- ongelmat/asiat jotka projektipäällikkö voi selvittää
 
Osa 2: Lead developerin check kehittäjille
- projektipäällikkö saa poistua tässä vaiheessa
- käydään läpi tehdyt taskit ja niiden ratkaisumallit
- onko teknisiä ongelmia

Lead developer lähettää kehittäjille kalenterikutsun statuscheckeistä. Kutsu toistumaan joka arkipäivä.


### Design katselmointi

**Kesto:** max 2h  
**Ketä on paikalla:** service designer + kehitystiimi

Tarkoitus:
- service designer käy läpi tiimin kanssa tehdyt ominaisuudet
- antaa palautetta ja ohjaa kehitystä

### Code review

**Kesto:** ei tiettyä aikaa, jatkuva prosessi
**Ketä on paikalla:** lead developer

Tarkoitus:
- lead developer käy tehdyn koodin läpi ja tarkastaa laadun
- ei ota kantaa siihen onko toiminto tehty vaatimusten mukaisesti

Code review prosessi:

1. Luo pull request githubissa.
2. Kopioi pull requestin linkki ja tee siitä todo #wp-code-review -kanavalle Slackissa (/todo http…)
3. Assignaa todo, mikäli tiedossa kenen pitää tehdä review, muutoin poolin jäsenet koppaavat reviewn pikimmiten
4. Kun review on tehty, katselmoija merkkaa todon valmiiksi (klikkaa Complete)
5. Todo lähettää notifikaation todon tekijälle
6. Uusi kierros, jos muutoksia
7. Kun review hyväksytty, taski liikkuu boardilla ja merget käytäntöjen mukaisesti

