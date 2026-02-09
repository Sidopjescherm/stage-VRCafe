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
    - [Gedwongen Dynamische Aanpassing](#gedwongen-dynamische-aanpassing)
    - [Renderblocking](#renderblocking)
    - [Verminderen JS en CSS](#verminderen-js-en-css)
  - [Samenvatting](#samenvatting)
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
Zoals ik eerder besproken heb in dit onderzoek is dat mensen meer hun mobiel gebruiken dan desktop om websites te bezoeken. Nu in deze testen kreeg ik vooral terug dat het op mobiel niet goed gaat en ik zal nog wat meer resultaten laten zien.

### Gedwongen Dynamische Aanpassing
Wanneer Javascript geometrische eigenschappen opvraagt nadat stijlen een aantal van de elementen heeft veranderd kan dit je prestaties enorm achter laten lopen. Oftewel wat dit betekent is dat als iemand ergens op zal klikken als een knop is de kans groot dat het een aantal seconden later verschuift en mensen wellicht ergens anders op zullen klikken waardoor je irritatie opwekt. 
<br>
<img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/Gedwongen dynamische aanpassing mobile.png">
</br>

### Renderblocking
Omdat in het script eerst een aantal verzoeken worden aangemaakt duurt het nog langer om de content neer te zetten. Dus wat er moet gebeuren is ervoor zorgen dat het script z'n verzoeken pas maakt nadat de pagina is ingeladen. 
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/renderblocking mobile.png">
</br>

### Verminderen JS en CSS
Iets dat ook helpt met UX is het verminderen van Javascript en CSS en het verwijderen van onnodige CSS en JS. Dit zorgt ervoor dat de laadtijd van de pagina minder zal worden en onnodige code niet zal worden gestuurd naar de browser.
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/beperk css mobile.png">
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/beperk JS mobile.png">
</br>

## Samenvatting
Dit onderzoek dient als een begin voor het verbeteren van de website, want zo zien we wat er beter kan. Waar we aan zullen moeten werken is het verbeteren van de website op mobiel, het verwijderen van onnodige code, het verbeteren van verzoeken en het verbeteren van de kwaliteit qua code. Want al ziet het testresultaat er prima uit, betekent het niet dat we moeten stoppen met het te verbeteren.
<br>
    Mobiel:
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/lighthouse test performance, SEO, accessability en best practices.png">
    Desktop:
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/desktop/lighthouse performance, SEO, accessability en best practices.png">
</br>

## Bronnen
- [Guide to SEO with Frontend](https://medium.com/@msmt0452/a-comprehensive-guide-to-seo-optimization-for-frontend-developers-eaf79bc1e1d2)
- [SEO optimalization](https://dev.to/anisubhra_sarkar/frontend-seo-best-practices-a-developers-guide-to-optimizing-your-website-57j4)
- [Strapi SEO tips](https://strapi.io/blog/front-end-performance-optimization-tips)
