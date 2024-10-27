# Workshop i webkart for BETA UiA

I denne workshopen skal du lære det mest grunnleggende for å programmere en webkart-app. Du må ha installert en kode-editor, fks VSCode, nettleser, og internett. 

## GIS-verktøy og standarder

**Projeksjoner**

Geografiske data er annerledes enn rene tabulariske data. Vi trenger å representere geografiske objekter i virkeligheten på en matematisk måte. Jorden er rundt, kartet er flatt. For å representere en 3D-kule som 2D-kart finnes det _projeksjoner_. Det finnes mange ulike, med forskjellige egenskaper. 


[NRK - Kartet er feil](https://www.nrk.no/trondelag/xl/verdenskartet-med-mercator-projeksjon-viser-feil-storrelse-pa-landene-1.17080439)

[Advent of GIS - Projeksjoner](https://github.com/Norkart/AdventOfGIS/blob/2023/01/README.md)

Det finnes mange verktøy som håndterer projeksjoner. Det viktigste er å ikke _blande_ for mye projeksjoner. Det blir fort skrekkelig feil. 

**Dataformater og GeoJSON**

GeoJSON er en utvidelse av JSON som håndterer geografiske data. GIS-verden har ekstremt mange ulike formater. GeoJSON er et av de aller mest brukte i "geografiske-IT-verden". Siden det er vanlig JSON er det god støtte i de fleste språk og biblioteker. 

På https://geojson.io/ kan du "tegne" egne GeoJSON og laste ned i ulike formater for å teste. 

_walkthrough geojson.io_

**GIS-programvare: QGIS**

QGIS er en klassisk GIS-desktop-programvare. QGIS støtter "alt", og er praktisk for å "debugge" geografiske data, tjenester og teste analyser m.m.

_walkthrough QGIS, geojson, tiles, projeksjoner, save_as_

## Workshop - webkart

Vi skal bruke noen av oppgavene fra fjorårets Advent of GIS som Norkart har. 

**Oppsett og bakgrunnskart**

Prøv å løs "Luke 3" i adventskalenderen. Prøv ut ulike bakgrunnskart/flyfoto med apikeys du får på workshopen. Bruk enten VSCode lokalt - eller web-editorer som CodePen.

For workshopen anbefaler vi å bruke helt vanilla html/javascript. Leaflet støttes og har wrappere i flere rammeverk når man har behov for det.

Løs luke 3: https://github.com/Norkart/AdventOfGIS/blob/2023/03/README.md


**GeoJSON-data i kartet**

Relevante luker i AoG

* https://github.com/Norkart/AdventOfGIS/blob/2023/02/README.md
* https://github.com/Norkart/AdventOfGIS/blob/2023/04/README.md
* https://github.com/Norkart/AdventOfGIS/blob/2023/08/README.md

Anbefalte steg:
1. Legg til en GeoJSON-fil i kartet som hentes med fetch e.l.
1. Endre på stylingen til features
1. Legg til en popup som viser tekst fra properties til featuren

Lag egen GeoJSON-fil fra fks geojson.io eller bruk ferdig datafiler under:
```
https://adventofgis-data.ams3.digitaloceanspaces.com/ne_10m_populated_places_simple.geojson

https://d2ad6b4ur7yvpq.cloudfront.net/naturalearth-3.3.0/ne_50m_populated_places_simple.geojson

https://d2ad6b4ur7yvpq.cloudfront.net/naturalearth-3.3.0/ne_110m_admin_0_countries.geojson

```

Tips:
* https://leafletjs.com/examples/geojson/
* Data: https://www.naturalearthdata.com/
* Data: https://geojson.xyz/
* Data: https://www.openstreetmap.org/
* Data: https://overpass-turbo.eu/
* Data: https://www.geonorge.no/


**WMS-tjenester i kartet**

WMS er en API-standard (OGC-standard) for å hente inn "custom" kartbilder fra en kartserver. WMS-servere rendrer resultatet (ofte) on-the-fly og støtter mye tilpasninger på projeksjoner/koordinatsystemer, styling, datalag m.m.

Løs luke 5: https://github.com/Norkart/AdventOfGIS/blob/2023/05/README.md 

Sjekk ut flere WMS-tjenester her på [GeoNorge](https://kartkatalog.geonorge.no/?DistributionProtocols=WMS-tjeneste&dataaccess=%C3%85pne%20data&spatialscope=Nasjonal)


**GPS-posisjon i kartet**

HTML GeoLocation API gjør at vi kan få GPS-posisjonen til enheten og "tracke" den. Det fungerer aller best på mobile enheter, men støttes OK på desktop-enheter uten GPS.

Oppgave: Hent ut posisjonen til brukeren og lag en markør som viser hvor brukeren er. Prøv først _uten_ plugins i Leaflet.

Relevant luke i AoG: https://github.com/Norkart/AdventOfGIS/blob/2023/07/README.md

HTML5 GeoLocation API: https://www.w3schools.com/html/html5_geolocation.asp 

Plugins i Leaflet: https://leafletjs.com/plugins.html#geolocation

**Konkurranse**

Lag deg en kreativ kart-app med noen datasett hentet fra OpenStreetMap eller lignende. Lag egen styling og informative popups. 

Send screenshot/GIF og/eller URL til alexander.nossum \_å\_ norkart.no før fristen!

Tips:
* https://overpass-turbo.eu/
* https://geojson.xyz/

**Bonusoppgaver**

Ble du raskt ferdig? Prøv deg på noen av disse lukene i AoG og andre systemer

1. [9. desember - Vector tiles](https://github.com/Norkart/AdventOfGIS/blob/2023/09/README.md)
1. [19. desember - FlatGeoBuf](https://github.com/Norkart/AdventOfGIS/blob/2023/19/README.md)
1. [22. Desember - COG, snøkart
](https://github.com/Norkart/AdventOfGIS/blob/2023/22/README.md)
1. [Kepler.gl - visualiseringsløsning i nettleseren](https://kepler.gl/)
1. [GirlTechFest - styling av egne vector tiles](https://github.com/Norkart/GirlTechFest)

