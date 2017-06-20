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

## Käyttäjätarinat ja taskit

Projektipäällikkö siirtää käyttäjätarinat ja muut tehtävät vaatimusmäärittelyistä Jiraan. Tämän jälkeen kaikki päivitykset tapahtuvat Jiraan. Uusin ja ajankohtaisin tieto on Jirassa.

Käyttäjätarina ilmaisee kuka, mitä, miten, miksi. Kehittäjät miettivät, miten tämä kuvailtu toiminto kaikkine määrityksineen saavutetaan.

Kaikkea tehtävää työtä ei voida ilmaista käyttäjätarinoilla. Esimerkiksi tekniset työt (kuten Tuotantoympäristön pystytys) lisätään Jiraan taskeina.

### Käyttäjätarinoiden pilkkominen

Käyttäjätarinat tarkennetaan ja pilkotaan sprintin aloituksessa. Pilkkomisen tavoitteena on selvittää ja kirjata, mitä konkreettisesti tarvitsee tehdä, jotta käyttäjätarina toteutuu. Kehittäjät purkavat käyttäjätarinat Jiran subtaskeihin. Yksi subtaski on konkreettinen tehtävä, joka tarvitsee tehdä.

Esimerkkikäyttäjätarina: "Ylläpitäjänä voin merkitä tilauksen noudetuksi, jotta tiedän mitkä tilaukset ovat vielä noutamatta."
Subtaskit:
- Luo API endpoint
- Luo käyttöliittymä

**Tarvittavat roolit:**  
Kehitystiimi

## Työarviot taskeihin

Työarviot tehdään tunteina / päivinä. Yksi tunti on pienin mahdollinen arvio. Taskin tekijä tekee itse taskin työarvion. Mikäli arvioija on eri kuin tekijä, tekijän pitää hyväksyä arvio. Eli ei niin että joku toinen devaaja sanoo "sinulla on tämän verran aikaa tähän taskiin".

1h 2h 4h 6h 1d 2d 4d

Näin varmistetaan riittävä skaala, jotta hyvällä tuurilla saadaan paremmin paikkansa pitävät arviot. Määrittelyvaiheessa työarviot tehdään käyttäjätarina-tasolla. Sprint planningissä tiimi purkaa arviot tehtävä-tasolle.

Käyttäjätarinalla on työarvio, esimerkiksi 8h. Jotta tiedät paljon aikaa voit käyttää omaan osuuteesi, työarviot puretaan subtaskeihin.

Esimerkki:
- Luo API endpoint 4h
- Luo käyttöliittymä 4h

Käyttäjätarinaan saa jättää myös aikaa. Käyttäjätarinan koko työmäärä näkyy tämän jälkeen Jirassa kentässä Remaining sum. Kehittäjän vastuulla on tietää:
- paljonko aikaa eli budjettia saa käyttää mihinkin tehtävään
- ilmoittaa jos meinaa ylittää arvioidun työmäärän


## Palaverit

### Sprintin suunnittelu

**Kesto:** 2-4 h  
**Ketä on paikalla:** service designer + projektipäällikkö + kehitystiimi + asiakkaan edustaja

Tavoite: service designer + projektipäällikkö + asiakkaan edustaja
- mitä pystytään tekemään backlogista seuraavan sprintin aikana (valitaan käyttäjätarinat + muut mahdolliset muut issuet (kuten tekniset taskit) sprinttiin)
- mitä tarvitsee tehdä jotta sprintin tavoiteltu tuotos saavutetaan

Töiden suunnittelu: kehitystiimi
- tiimi tekee käyttäjätarinoiden teknisen suunnittelun, purkaa tarinat subtaskeihin (kts. vaatimusmäärittelyt ja issuet) ja päivittää subtaskeille työarviot

### Kehitystiimin päivittäinen statuscheck

**Kesto:** n.15min  
**Ketä on paikalla:** projektipäällikkö + kehitystiimi

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

### Sprintin katselmointi

**Kesto:** max 2-3h  
**Ketä on paikalla:** projektipäällikkö + kehitystiimi + asiakkaan edustaja

Tarkoitus:
- tiimi kertoo mitkä tehtävät on tehty ja demoaa ne
- pohdinta mitä tehdään seuraavaksi (antaa pohjaa sprint planningiin)

Kehitystiimi valmistautuu huolella esittelemään tehdyn työn. Varmista, että käyttäjätarinan hyväksymiskriteerit täyttyvät ja pystyt demoamaan ne.

### Design katselmointi

**Kesto:** max 2h  
**Ketä on paikalla:** service designer + kehitystiimi

Tarkoitus:
- service designer käy läpi tiimin kanssa tehdyt ominaisuudet
- antaa palautetta ja ohjaa kehitystä

### Retro

**Kesto:** max 1h  
**Ketä on paikalla:** projektipäällikkö + service designer + kehitystiimi + asiakkaan edustaja

Tavoite:
- selvittää miten edellinen sprintti sujui, koskien ihmisiä, suhteita, prosesseja ja työkaluja
- mikä meni hyvin, missä olisi parantamisen varaa
- päätetään mitkä parannukset toteutetaan ja sovitaan mitä tehdään jotta parannukset saavutetaan

## Dokumentointi

Kehittäjä luo teknisen dokumentointoinnin git-projektin juureen readme-tiedostoon. Dokumentointia tehdään koko teknisen toteutuksen ajan, sitä mukaa kun uusia toimintoja luodaan.

Testaaja luo käyttöohjeen, joka on tarkoitettu ensisijaisesti asiakkaan käyttöön.
