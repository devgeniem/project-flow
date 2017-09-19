---
layout: page
title: "Projektikäytännöt"
category: kehitys
date: 2017-06-21 09:00:20
order: 3
---

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

## Työarvioiden lisääminen taskeihin

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

## Dokumentointi

Kehittäjä luo teknisen dokumentointoinnin git-projektin juureen readme-tiedostoon. Dokumentointia tehdään koko teknisen toteutuksen ajan, sitä mukaa kun uusia toimintoja luodaan.

Testaaja luo käyttöohjeen, joka on tarkoitettu ensisijaisesti asiakkaan käyttöön.

## Palaute

### Palautteen antaminen ja saaminen projektin aikana:

**Statuscheckit + code review:** Kehittäjät saavat teknistä palautetta päivittäisten statuscheckkien sekä code reviewn kautta.

**Sprintin retrospektiivi:** Sprinttien lopuksi pidetään lyhyt retrospektiivi, jossa käydään läpi mikä meni sprintin aikana hyvin ja mitä voisi tehdä paremmin. Koko tiimi saa antaa palautetta sekä vastaanottaa palautetta toisiltaan ja asiakkaalta.

### Palautteen antaminen ja saaminen projektin loppuessa:

**Sisäinen retrospektiivi:** Projektin loppumisen jälkeen tiimi kokoontuu pitämään koko projektia koskevan retrospektiivin. Käydään läpi mikä meni projektissa hyvin ja mitä olisi voinut tehdä paremmin (ja miten). Retrospektiivistä kirjataan aina kooste.

**Vertaispalaute:** Projektin lopuksi jokainen tiimin jäsen antaa palautetta jokaiselle tiimin jäsenelle. Projektipäällikkö kokoaa palautteet ja käy läpi palautteet jokaisen tiimin jäsenen kanssa henkilökohtaisesti. Projektipäällikkö käsittelee oman saadun  palautteensa toisen projektipäällikön kanssa.

**Tekninen retrospektiivi:** Dev leadit pitävät keskenään teknisen retron. Ei tarvetta pienimmissä projekteissa. Tavoitteena on dev leadien kehittyminen.


