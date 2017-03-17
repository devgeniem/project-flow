---
layout: page
title: "Tekninen toteutus"
category: kehitys
date: 2017-02-24 15:00:00
order: 2
---
### Yleistä

Projektit toteutetaan yleensä kehitysjaksoissa joita kutsutaan sprinteiksi. Yhden sprintin pituus on lähes poikkeuksetta 2 viikkoa. Sprinttien määrä riippuu projektin laajuudesta. 

Projektin käyttäjätarinoiden ja muiden tehtävien hallintaan käytetään Jira-nimistä tehtävienhallintaohjelmistoa.

### Käyttäjätarinoiden tarkennus

Projektipäällikkö siirtää käyttäjätarinat ja muut tehtävät Jiraan. Tämän jälkeen kaikki päivitykset tapahtuvat Jiraan. Uusin ja ajankohtaisin tieto on Jirassa.

Käyttäjätarina ilmaisee kuka, mitä, miten, miksi. Kehittäjät miettivät, miten tämä kuvailtu toiminto kaikkine määrityksineen saavutetaan. 

### Käyttäjätarinoiden pilkkominen

Pilkkomisen tavoitteena on selvittää ja kirjata, mitä konkreettisesti tarvitsee tehdä, jotta käyttäjätarina toteutuu. Kehittäjät purkavat käyttäjätarinat Jiran subtaskeihin. Yksi subtaski on konkreettinen tehtävä, joka tarvitsee tehdä.

Esimerkkikäyttäjätarina: "Ylläpitäjänä voin merkitä tilauksen noudetuksi, jotta tiedän mitkä tilaukset ovat vielä noutamatta."
Subtaskit:
- Luo API endpoint
- Luo käyttöliittymä

### Työarviot taskeihin

Työarviot tehdään tunteina ja päivinä. Käytetään jompaa kumpaa seuraavista vaihtoehdoista:

1. 1h 2h 3h 5h 8h (Fibonaccin kaava)

2. 2h 4h 6h 1d 2d 4d

Näin varmistetaan riittävä skaala, jotta hyvällä tuurilla saadaan paremmin paikkansa pitävät arviot. Määrittelyvaiheessa työarviot tehdään käyttäjätarina-tasolla. Sprint planningissä tiimi purkaa arviot tehtävä-tasolle.

Käyttäjätarinalla on työarvio, esimerkiksi 8h. Jotta tiedät paljon aikaa voit käyttää omaan osuuteesi, työarviot puretaan subtaskeihin. 

Esimerkki:
- Luo API endpoint 4h
- Luo käyttöliittymä 4h

Käyttäjätarinaan saa jättää myös aikaa. Käyttäjätarinan koko työmäärä näkyy tämän jälkeen Jirassa kentässä Remaining sum. Kehittäjän vastuulla on tietää:
- paljonko aikaa eli budjettia saa käyttää mihinkin tehtävään
- ilmoittaa jos meinaa ylittää arvioidun työmäärän

### Jiran käyttö projektissa

- Ennen kuin alat tehdä issueta, varmista että siinä on työarvio. Lisää, jollei ole.
- Jos/kun huomaat ettet ehdi tehdä issueta ajassa joka siihen on arvioitu (Original Estimate), ilmoita tästä projektipäällikölle
- Käyttäjätarinan saa siirtää QA-tilaan vasta kun kaikki tarinan subtaskit ovat myös samassa tilassa. Testaaja ei voi muuten testata

Tiimi on vastuussa kollektiivisesti issueista ja niiden valmistumisesta. Muita kehittäjiä autetaan, jotta sprintin hommat saadaan tehtyä. “Ei ole minun vastuulla” -lause ei kuulu tiimityöskentelyyn.

### Jira Workflow

#### To Do
- sprinttiin valitut issuet
- ei tarvitse noudattaa mitään prioriteettijärjestystä, kunhan pitää mielessä/kyseenalaistaa mikä on sprintissä oleellisinta ja aloittaa siitä. ei jää tärkeimmät asiat kesken, jos jotain kesken jää
- pitää olla kaikki tarvittava tieto, jotta issuen voi tehdä. muuten ei oteta sprinttiin

#### In Progress
- parhaillaan teossa olevat issuet
- otat yhden issuen työn alle, teet sen, ja sitten seuraava. ei roikoteta tässä montaa taski. Jos taskin eteneminen pysähtyy jostain syystä niin issuen voi siirtää esim Pending tilaan. 

#### Code review
- koodi on arvioitavana lead devaajalla

#### Pending
- on jokin este, jonka vuoksi issueta ei voi edistää (esim. puuttuu tietoa asiakkaalta, tai issue odottaa toisen devaajan työpanosta, tai kaksi issueta joista toinen odottaa toisen valmistumista)
- lisää kommentti miksi pending, mitä odotetaan, keneltä
- kun siirrät tähän tilaan, huolehdi että henkilö jolta odotetaan tietoa/tekemistä on tietoinen, että issue odottaa häntä
- scrum master huomaa tästä helpommin jos on jonkin issuen kanssa esteitä ja niiden selvittäminen ei unohdu
- kehitystiimi informoi scrum masteria pending-tilassa olevista issueista

#### Rework
- aina prioriteettina 1
- jos sprintin jälkeen jää reworkkia, ne tehdään ennen kuin aloitetaan seuraavaan sprintin hommia
- tähän siirretään tarvittaessa tavaraa QA:sta -> projari tai testaaja siirtää

#### QA
- kun issue on tässä tilassa, devaaja on deployannut sen stagelle
- lisää tarvittaessa testausohjeet issueeseen, esim jos pitää testata kirjautumista -> testitunnukset
- projari/testaaja käy tästä läpi issuet. testataan stagelta
- jos jotain vikaa/paranneltavaa -> kommenttiin "Rework: “ + selitys mitä pitää tehdä. sen jälkeen siirto Reworkkiin
- jos issue ok, siirto Ready for Live

#### Ready for Live
- issuet on testattu ja ne saa deployata tuotantoversioon

#### Done
- kun issue on tässä tilassa, devaaja on deployannut sen tuotantoon
- tästä käydään asiakkaan kanssa läpi issuet sprintin lopetuksessa
- jos tässä vaiheessa vielä vikaa -> reworkkiin
- jos selkeesti lisäfeature, tehdään uusi issue backlogiin

### Palaverit

#### Sprintin suunnittelu (sprint planning)

Kesto: 2-4 h  
Ketä on paikalla: service designer + projektipäällikkö + kehitystiimi + asiakkaan edustaja

Tavoite: service designer + projektipäällikkö + + asiakkaan edustaja
- mitä pystytään tekemään backlogista seuraavan sprintin aikana (valitaan käyttäjätarinat + muut mahdolliset muut issuet (kuten tekniset taskit) sprinttiin)
- mitä tarvitsee tehdä jotta sprintin tavoiteltu tuotos saavutetaan

Töiden suunnittelu: kehitystiimi
- tiimi suunnittelee käyttäjätarininoiden teknisen suunnittelu, purkaa tarinat subtaskeihin (kts. vaatimusmäärittelyt ja issuet) ja päivittää subtaskeille työarviot

#### Daily scrum / Aamuscrum

Kesto: n.15min  
Ketä on paikalla: projari + kehitystiimi

Mitä:
- koko tiimi kokoontuu ja puhuu keskenään.
- pyritään pitämään samaan aikaan joka päivä

jokainen vastaa seuraaviin kysymyksiin:
- Mitä teit eilen?
- Mitä aiot tehdä tänään?
- Mitä ongelmia/kysyttävää?
- Lisäksi muut ajankohtaiset/selvitettävät asiat

Tarkoitus:
- tiedonjako
- ongelmat ja esteet selville

Projektipäällikkö päättää projektikohtaisesti onko tarvetta/mahdollisuutta pitää scrum joka päivä. Vaihtoehtoisesti sovitaan tietyt päivät viikosta.

Projektipäällikkö lähettää kehittäjille kalenterikutsun scrumeista.

#### Sprint demo (katselmointi)

Kesto: max 2-3h  
Ketä on paikalla: projektipäällikkö + kehitystiimi + asiakkaan edustaja

Tarkoitus:
- tiimi kertoo mitkä tehtävät on tehty ja demoaa ne
- pohdinta mitä tehdään seuraavaksi (antaa pohjaa sprint planningiin)

Kehitystiimi valmistautuu huolella esittelemään tehdyn työn. Varmistaa, että käyttäjätarinan hyväksymiskriteerit täyttyvät ja ne pystytään demoamaan.

#### Design review

Kesto: max 2h  
Ketä on paikalla: service designer + kehitystiimi

Tarkoitus:
- service designer käy läpi tiimin kanssa tehdyt ominaisuudet
- antaa palautetta ja ohjaa kehitystä

#### Retro

Kesto: max 1h  
Ketä on paikalla: projektipäällikkö + service designer + kehitystiimi + asiakkaan edustaja

Tavoite:
- selvittää miten edellinen sprintti sujui, koskien ihmisiä, suhteita, prosesseja ja työkaluja
- mikä meni hyvin, missä olisi parantamisen varaa
- päätetään mitkä parannukset toteutetaan ja sovitaan mitä tehdään jotta parannukset saavutetaan


### Dokumentointi

Kehittäjä luo teknisen dokumentointoinnin git-projektin juureen readme-tiedostoon. Dokumentointia tehdään koko teknisen toteutuksen ajan, sitä mukaa kun uusia toimintoja luodaan.

Testaaja luo käyttöohjeen, joka on tarkoitettu ensisijaisesti asiakkaan käyttöön.



