# SEO Onderzoek

## Uitleg
Deze opdracht over SEO heb ik gekregen van mijn stagebegeleider Owen. Het doel van deze opdracht is het maken van een onderzoek dat gaat over SEO, wat VRcafe niet goed doet en hoe we het kunnen verbeteren.

## Critera van SEO
SEO staat voor Search Engine Optimization. Zoekmachines zoeken dus jouw website voor info die zij belangrijk vinden voor de gebruiker die het inzet. Hieronder zal ik de criteria neerzetten die belangrijk zijn voor SEO en wat VRcafe wel of niet al inzet.

## Index
 * [Semantische HTML](semantische-html)
 * [Image Optimization](image-optimization)

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


### Image optimization
Iets dat nog wel eens wordt overgeslagen is het optimaliseren van afbeeldingen. Nu heb ik het niet alleen over grote afbeeldingen die zullen worden ingeladen, ik heb het ook over alt attributen. Zoekmachines lezen deze attributen die op de afbeelding staan en maken op basis daarvan de keuze om het te laten zien.



## Bronnen
- [Guide to SEO with Frontend](https://medium.com/@msmt0452/a-comprehensive-guide-to-seo-optimization-for-frontend-developers-eaf79bc1e1d2)
- [SEO optimalization](https://dev.to/anisubhra_sarkar/frontend-seo-best-practices-a-developers-guide-to-optimizing-your-website-57j4)
- [Strapi SEO tips](https://strapi.io/blog/front-end-performance-optimization-tips)
