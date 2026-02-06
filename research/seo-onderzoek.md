# SEO Onderzoek

## Uitleg
Deze opdracht over SEO heb ik gekregen van mijn stagebegeleider Owen. Het doel van deze opdracht is het maken van een onderzoek dat gaat over SEO, wat VRcafe niet goed doet en hoe we het kunnen verbeteren.

## Critera van SEO
SEO staat voor Search Engine Optimization. Zoekmachines zoeken dus jouw website voor info die zij belangrijk vinden voor de gebruiker die het inzet. Hieronder zal ik de criteria neerzetten die belangrijk zijn voor SEO en wat VRcafe wel of niet al inzet.

## Index
 * [Semantische HTML](#semantische-html)
 * [Image Optimization](#image-optimization)
 * [Heading levels](#heading-levels)

> [!IMPORTANT] 
> Accessability is optimalisatie voor SE

### Semantische HTML
Om hoog te komen voor search engines is semantisch HTML schrijven erg van toepassing. Omdat zoekmachines tekst lezen is het belangrijk deze op goede orde te stellen. Je `header` moet een `header` tag hebben, je belangrijkste tekst op een pagina is een `h1` en tekst dat gepaard gaat met een afbeelding die ergens anders op de site herplaatst zou kunnen worden in een `article`. Dit helpt de zoekmachine met een index maken van je website zodat het die het weer kan terugkoppelen aan de gebruiker.

#### Hoe doet VRcafe dat?:
Het VRcafe heeft een aantal van deze principes wel al in de smiezen, maar ik zie wel dat een aantal opmakingen in componenten die niet logisch zijn. Ik ging kijken naar een goed voorbeeld en ga daarom de navigatie en header nemen daarvoor, want deze hebben wel wat foutieve semantische HTML. Desondanks dat het component MobileNav en DesktopNav heet is de `nav` tag nergens te bekennen. Dit is al heel vreemd, want zo zien de zoekmachines zeker niet dat deze header een navigatie bezit. Wat er wel in dit component wordt gebruikt is de `menu` tag. Een begrijpelijke fout, maar `menu` is iets heel anders dan een `nav`. Wat een `menu` eigenlijk betekent is een ander soort `ul`. Het ziet er nu zo uit:
```html
<section>
    <a></a>
    <li></li>

    <menu>
        <section>
            <div>
                <div>
                    <section>
                        <div></div>
                        <a></a>
                    </section>
                </div>
            </div>
        </section>
    </menu>
</section>
```
Ik vind dat het VRcafe hier erg slordig mee omgaat, want je hebt geen `nav` tag, een losstaande `li` zonder parent, een `menu` zonder `li` en teveel `section` en `div` die eigenlijk alleen voor minimale styling zorgen. Oftwel het is enorm zonde om het zo op te maken, want zo krijgt de zoekmachine geen goede index van je pagina. Een meer logische aanpak van dit component zou zijn:
```html
<nav>
    <ul>
        <li><a></a></li>
        <li><a></a></li>
        <li><a></a></li>
        <li><a></a></li>
        <li><a></a></li>
        <li><a></a></li>
    </ul>
</nav>
```
Ik kan nu wel vertellen wat er belangrijk is, maar het beste zou zijn om te tonen hoe tools als Lighthouse, HeadingsMap en PagespeedInsight het zien:
<img src="../assets/seo-onderzoek/Screenshot 2026-02-05 161546.png">

### Image optimization
Iets dat nog wel eens wordt overgeslagen is het optimaliseren van afbeeldingen. Nu heb ik het niet alleen over grote afbeeldingen die zullen worden ingeladen, ik heb het ook over alt attributen. Zoekmachines lezen deze attributen die op de afbeelding staan en maken op basis daarvan de keuze om het te laten zien. Bijvoorbeeld iemand die van een berg af aan het skiën is zou de alt tekst moeten hebben: 'Persoon die van een besneeuwde berg aan het skiën is." Dit helpt al een hele boel voor SEO, omdat het actuele informatie is. 

Verder zijn kleinschalige images beter voor een LCP, want wat er nu gebeurt is dat de website langzamer zal worden ingeladen. Kijk maar eens wat PageSpeed Insight ziet:
<img src="../assets/seo-onderzoek/pagespeed insigth afbeeldingbesparing.png">

Dit kan dus inderdaad veel beter! Dit zal helpen met gebruikers behouden op de mobiele website. Dit is op te lossen door gebruik te maken van het `picture` element in de HTML. Deze tag kan je gebruiken om tegen de browser te vertellen dat er een plaatje is, maar je kan zelf het format bepalen waar het uitkomt. Zo zou het eruit zien:
```html
<picture>
    <source srcset="VRcafe-logo.webp" type="image/webp">
    <source srcset="VRcafe-logo.avif" type="image/avif">
    <img src="VRcafe-logo.jpg" alt="terug naar de homepagina van het VRcafe" loading="lazy">
</picture>
```
Dus niet alleen helpt dit met het maken van afbeeldingen die niet te lang laden, dit helpt ook met zoekmachines jouw website eruit halen voor optimalisatie qua afbeeldingen. Nu met het gepraat over alt teksten is het niet de bedoeling om dit op alle afbeeldingen te plaatsen waar het niet nodig is, behoudt het op afbeeldingen die iets toevoegen aan de inhoud, niet er extra bovenop. Wat ook nog helpt met grote afbeeldingen is lazy loading. Deze afbeeldingen zullen dan pas worden ingeladen wanneer ze in je viewport komen, dus dat is nog beter voor LCP. 

#### Hoe doet VRcafe dat?:
VRcafe zal nog wel moeten werken aan een aantal van deze principes, want een aantal teksten zijn nog niet zo goed als ze kunnen zijn of zijn te overbodig. 

goed gebruik van alt tekst:
<img src="../assets/seo-onderzoek/een goed gebruik van alt tekst.png">
Hier worden alt teksten al goed ingezet, behalve het ALT-gedeelte over een sneeuwman en een sneeuw overlay.

onnodig gebruik van alt tekst:
<img src="../assets/seo-onderzoek/Een slecht voorbeeld van alt tekst.png">
De alt teksten die hier staan zijn erg onnodig, want de tekst die in de alt wordt benoemd staat al onder in een `p` tag. In deze gevallen waar het decoratief is zet je een lege alt tag neer(`alt=""`). 

het gebruik van alt tekst kan beter:
<img src="../assets/seo-onderzoek/Een voorbeeld hoe een alt tekst beter kan.png">
De alt tekst op dit logo is technisch gezien correct, maar een betere benaming zou zijn dat het een terug keer knop is naar de homepagina, want daar dient het ook voor! Dus daar kan wat meer verbetering in.

### Heading levels
Heading levels zijn erg belanmgrijk voor je website en ook voor zoekmachines. Headings voor zoekmachines zijn een goede manier van het indelen van je belangrijkste tot minst belangrijkste content. Een belangrijke regel voor headings zijn: altijd één `h1` per pagina gebruiken, gebruik logische vervolging van subheadings en houdt de headings descriptief. Een tool als headingsmap laat ook precies zien waar het goed gaat en waar het niet goed gaat.

### Hoe doet VRcafe dat?:
VRcafe behoudt de heading levels op een goed niveau, maar er zijn hier en daar nog wel wat puntjes om op te letten. De meeste headings die worden gebruikt in de website zijn correct neergezet zoals deze headings:
<img src="../assets/seo-onderzoek/correcte heading wist je dat.png">
visueel:
<img src="../assets/seo-onderzoek/wist je dat.png">

Maar verder in de pagina zijn er reviews van gamers en deze is helaas niet goed qua opmaak. We springen van een `h2` meteen naar een `h4` en op de VR at home is er gebruik gemaakt van twee `h2`'s, maar het is logischer om hier een `h2` en `h3` van te maken. Als we dit oplossen dan komt er vast en zeker een betere SEO score uit dan dat er nu al is.

Review van gamers op de homepage:
<img src="../assets/seo-onderzoek/heading levels homepage.png">

VR at home heading levels:
<img src="../assets/seo-onderzoek/incorrecte heading VR at home en leukste uitje in code.png">
visueel:
<img src="../assets/seo-onderzoek/VR at home en leukstje uitje voor thuis visueel.png">

## Bronnen
- [Guide to SEO with Frontend](https://medium.com/@msmt0452/a-comprehensive-guide-to-seo-optimization-for-frontend-developers-eaf79bc1e1d2)
- [SEO optimalization](https://dev.to/anisubhra_sarkar/frontend-seo-best-practices-a-developers-guide-to-optimizing-your-website-57j4)
- [Strapi SEO tips](https://strapi.io/blog/front-end-performance-optimization-tips)
