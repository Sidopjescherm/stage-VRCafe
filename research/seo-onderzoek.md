# SEO Onderzoek

## Uitleg
Deze opdracht over SEO heb ik gekregen van mijn stagebegeleider Owen. Het doel van deze opdracht is het maken van een onderzoek dat gaat over SEO, wat VRcafe niet goed doet en hoe we het kunnen verbeteren.

## Index
- [SEO Onderzoek](#seo-onderzoek)
  - [Uitleg](#uitleg)
  - [Index](#index)
  - [Semantische HTML](#semantische-html)
    - [Headings](#headings)
    - [Correct gebruik van elementen](#correct-gebruik-van-elementen)
    - [Tabtest](#tabtest)
  - [Image optimization](#image-optimization)
    - [Grootte afbeelding](#grootte-afbeelding)
    - [Alt beschrijving](#alt-beschrijving)
  - [Mobile first](#mobile-first)
    - [Hoe doet VRcafe dat?](#hoe-doet-vrcafe-dat)
  - [Bronnen](#bronnen)


> [!IMPORTANT] 
> Accessability is optimalisatie voor SE

## Semantische HTML
Voor gebruikers en voor zoekmachines is semantische HTML belangrijk! Iets waar mensen niet vaak op letten heeft zeker wel impact. 

### Headings
 Headings en subheadings zijn de leesvolgorde van je content en zouden van `h1` tot en met `h6` ingedeeld moeten worden. Iets dat nog niet correct gaat volgens de tool Headingsmap:
<br>
    <img src="../assets/seo-onderzoek/Semantische html/heading levels homepage.png">
    <img src="../assets/seo-onderzoek/Semantische html/drie h1&apos;s op een pagina.png">
    <img src="../assets/seo-onderzoek/Semantische html/incorrecte heading VR at home en leukste uitje in code.png">
</br>
Door je headings en subheadings correct neer te zetten help je de zoekmachine met het correct indexeren van je website. Voor gebruikers helpen headings ook met de leesvolgorde van je content zodat zij een beetje kunnen 'skimmen' voor de juiste info. Ook een belangrijk iets om te onthouden is het gebruik van één `h1` element.

### Correct gebruik van elementen
Voor een tekst op de homepage zie ik ook een `h2` met daarin een `span` die verwijst naar "Activiteiten," maar semantisch is dit niet correct. Omdat activiteiten het punt van aandacht is, zou het een `em` of een `strong` moeten worden. Dit zorgt ervoor dat het niet een generiek gebruik is van een element, maar dat het duidelijk ook wat te betekenen heeft voor de gebruiker en zoekmachine. 
<br>
    <img src="../assets/seo-onderzoek/span als tekst.png">
    <img src="../assets/seo-onderzoek/populaire-activiteiten-visueel.png">
</br>

### Tabtest
Voor mensen die een toetsenbord gebruiken, maar geen muis gebruiken zij de tab-toets om te navigeren. Voor zoekmachines is dit niet belangrijk, maar wel voor gebruikers op de website. Als een gebruiker niet duidelijk door de pagina kan navigeren is het een slechte UX en dit is het geval bij de knoppen en het menu. Het logo wordt wel herkend, maar niet het menu om te navigeren en dat is zeker niet een correct iets voor navigatie.
<br>
    <img src="../assets/tab wel logo.png">
    <img src="../assets/geen tab menu.png">
</br>
Verder staat er een `div` samen met een `a` op de pagina voor het boeken van een activiteit. Dit zorgt ervoor dat je eerst op de `div` staat en daarna op de `a`. Oftwel je doet er dubbel zolang over om op een knop te focusen en dubbel zo lang over iets doen is al dubbel teveel voor UX.
<br>
    <img src="../assets/Screenshot 2026-02-03 153432.png">
    <img src="../assets/Screenshot 2026-02-03 153442.png">
</br>


## Image optimization
Voor afbeeldingen is het belangrijk om een bepaalde grootte ervoor te kiezen en een beschrijvende alt. Een minder groot bestand helpt met een kortere tijd met het inladen van de afbeelding en een alternatieve tekst helpt met het beschrijven indien nodig.

### Grootte afbeelding
In het geval van de grootte speelt de FCP en LCP een grote rol. FCP is de eerste tekst of afbeelding zal worden geladen en LCP is de grootste tekst of afbeelding die zal worden geladen.
<br>
    Desktop:
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/desktop/statistieken desktop.png">
    Mobiel:
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/statistieken mobile.png">
</br>
Voor desktop is binnen 0.4 seconden de eerste afbeelding ingeladen en de grootste afbeelding wordt in 2.4 seconden ingeladen. Helaas voor mobiel is het erg drastisch, want de eerste afbeelding wordt ingeladen in 2.4 seconden en de grootste afbeelding is in 9.9 seconden ingeladen. Voor gebruikers is dit een hele trage laad tijd en zorg je er niet voor dat iemand verder zal klikken en zo verlies je klanten. Omdat mensen vaker hun mobiel gebruiken dan een desktop is het belangrijk om voor mobiel deze afbeeldingen te optimaliseren. 
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/desktop/lcp verzoekdetectie desktop.png">
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/LCP verzoekdetectie.png">
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/desktop/afbeelding verbetering desktop.png">
</br>

### Alt beschrijving
Alt zorgt ervoor dat de zoekmachine jouw afbeeldingen kan lezen en de woorden die je beschrijft worden ook meegenomen in SEO. Wanneer ik de Pagespeed Insight test doe zie ik ook dat er meerdere malen voor SEO en Accessability wordt gehamerd op ALT voor afbeeldingen. Dus als we alt beschrijvingen toevoegen waar het nodig is en alt tekst veranderen naar correcte beschrijvingen helpt dit zeker met zoekresultaten. 
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/afbeeldingen hebben geen alt mobile.png">
</br>
Belangrijk voor alt teksten is ook onnodige verwijderen, want teveel alt teksten kan je website verkeerd indexen of de zoekmachine ziet het als teveel hameren op SEO. Voorbeelden als dit moeten dan dus verwijderd worden:
<br>
    <img src="../assets/seo-onderzoek/Alt teksten/onnodig alt tekst.png">
    <img src="../assets/seo-onderzoek/Alt teksten/Een slecht voorbeeld van alt tekst.png">
</br>
Alt teksten als dit zorgt ervoor dat de zoekmachine tweemaal de tekst indexeert wat enorm zonde is, want de afbeeldingen dienen alleen als visuele toevoeging. Hiervoor zou dus een lege alt gebruikt moeten worden.

## Mobile first
Mobile first is een standaard dat de laatse jaren erg is gestegen, omdat veel mensen vaker hun mobiel erbij pakken om iets op te zoeken inplaats van op de laptop. Dus ervoor zorgen dat je website het beste loopt op mobiel zou het belangrijkste moeten zijn, maar uit mijn onderzoek zie ik helaas dit niet goed terugkomen. Een mobile versie van een website zou het belangrijkste aspect moeten zijn, zodat het voor de meeste mensen een toegankelijk iets is. Waarom hoort dit bij SEO? Mensen komen via hun mobiel op jouw website en jouw mobiele website keert ze af of laat ze verder scrollen. Dus al kom je bovenaan de zoekresultaten, je gebruikers behouden is het belangrijkste. 

### Hoe doet VRcafe dat?
<img src="../assets/seo-onderzoek/Diagnostics for mobile.png">
<img src="../assets/seo-onderzoek/Performance op mobile.png">
Zoals we kunnen zien hierboven in de test is het echt drastisch lager dan desktop, wat best schrikken is wanneer mobile eigenlijk de belangrijkste versie hiervan is. Iets dat ik meteen zie is ongebruikte JS en CSS verwijderen en dat is altijd belangrijk om weg te halen, want code die niet wordt gebruikt is zonde. 

Wat ook nog aangekaart moet worden is het verminderen van de main-thread work dat vooral te lang duurt door het te valideren van Javascript. Daar doet het 3,6 seconden over en dat is wel echt een te lange tijd.

Als laatste nog de laadtijden op de website op verschillende netwerken:
<br>
    3G:
    <img src="../assets/seo-onderzoek/8,5 seconden op 3g.png">
</br>

<br>
    4G langzaam:
    <img src="../assets/seo-onderzoek/2.3 seconden langzaam 4g.png">
</br>

<br>
    4G snel:
    <img src="../assets/seo-onderzoek/0.5 seconden snelle 4g.png">
</br>

## Bronnen
- [Guide to SEO with Frontend](https://medium.com/@msmt0452/a-comprehensive-guide-to-seo-optimization-for-frontend-developers-eaf79bc1e1d2)
- [SEO optimalization](https://dev.to/anisubhra_sarkar/frontend-seo-best-practices-a-developers-guide-to-optimizing-your-website-57j4)
- [Strapi SEO tips](https://strapi.io/blog/front-end-performance-optimization-tips)
