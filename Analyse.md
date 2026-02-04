# Analyse VRCafe

## Index
- [Uitleg](#uitleg)
- [Mijn bevindingen](#mijn-bevindingen)
- [Opzet](#opzet)
- [Semantisch Werken en styling](#semantisch-werken-en-styling)
- [Styling](#styling)

## Uitleg
Dit document is gemaakt omdat ik bezig ben met het beter begrijpen van het VRcafe en de website. In deze analyse heb ik gekeken naar het gebruik van HTML, CSS en het semantisch gebruik hiervan. Als student Frontend-webdeveloper is het mijn taak om deze website beter te begrijpen en uitelkaar te halen zodat ik weet hoe het werkt. 

## Mijn bevindingen
Na de hele ochtend te testen op de website en te kijken naar de website in de styling kwam ik achter een aantal dingen die mij opvielen. Eerst wilde ik het hebben over wat het VRcafe is, zodat de boodschap helder is voor mij. 

Het VRcafe is een plek dat ervaringen aanbiedt in de wereld van Virtual Reality. Je kan games uit categorieën kiezen zoals: shooters, multiplayer, family, kids en meer. 

### Opzet
Na het lezen van de documentatie zie ik dat het VRcafe gebruik maakt van: TailwindCSS, Astro, React components en Starlight(dat samenwerkt met Astro.) Toen ik de devtools opende zag ik wel al een paar meldingen die belangrijk zijn om te zien.
<br>
<img width="294" height="34" alt="GA4 undefined" src="https://github.com/user-attachments/assets/e0b10773-5639-40be-b05c-dad62e3934f1" />
<br>
<img width="283" height="175" alt="Not a function onAccept" src="https://github.com/user-attachments/assets/38acf1c7-2be1-40f9-a4d3-5d476c383829" />
<br>
<img width="285" height="316" alt="React error" src="https://github.com/user-attachments/assets/af8cc3af-8f94-4f4f-a0fd-0ba4aa477b59" />
<br>
een aantal van deze errors komen van het incorrect plaatsen van bepaalde code. Er zijn een aantal fouten die ik momenteel alleen zie in het zogeheten ‘-partytown.’ Dit lijkt mij een omgeving die gebruikt wordt voor de backend, maar ik zie wel veel meldingen vanuit hier komen. Het meeste hiervan is backend en daar heb ik bijna niets mee te maken, maar wat ik aantref qua opmaak van de website is wel om iets van te noteren en iets waar ik wat aan kan doen. 

### Semantisch werken en styling
Semantische code schrijven is wel het meest verstandige om te doen. Zo help je niet alleen jezelf en je huidige collega’s, maar ook toekomstige collega’s met het schrijven van deze code. Het meeste van de code die uitgelegd wordt staat op de docs repo in Github en dat is erg fijn. Wat ik wel heb gemerkt is dat de website echt niet vriendelijk is als je CSS uit hebt staan. Nu zal een tegen argument zijn dat niemand CSS uit heeft staan, maar het verslaat wel het principe van het web als geheel. Het moet toegankelijk blijven voor mensen vanuit alle windstreken, met welk lichaam dan ook. Wat ik hiermee bedoel ik dat mensen met een motorische stoornis, geen armen of gebruik maken van een screenreader ook gebruik moeten kunnen maken van de website. 

Wat mij opviel bij deze website is dat afbeeldingen/svg’s niet een standaard waarde krijgen meegegeven als ze worden ingeladen. Dit zorgt ten eerste voor webpagina’s waar de eerste gedeelten van het scrollen bestaan uit de header zelf. Vele iconen die worden gebruikt in de header zijn VEELS te groot. Vele tekens nemen een heel scherm op in grootte. Via mijn DEVtools ben ik erachter gekomen hoe het zonder CSS eruit zou zien. Hier een aantal voorbeelden die mij erg opvielen:
<br>
<img width="1877" height="892" alt="Screenshot 2026-02-03 142156" src="https://github.com/user-attachments/assets/00dd9bcb-2942-4e0a-8c9c-f8edeef909e5" />
<br>
<img width="305" height="69" alt="Screenshot 2026-02-03 144309" src="https://github.com/user-attachments/assets/6f6edcce-8d08-410c-9f02-7a2e72ab7749" />
<br>
<img width="1872" height="878" alt="Screenshot 2026-02-03 144317" src="https://github.com/user-attachments/assets/51bc89c5-72a8-4082-9400-8f3dcf18b66e" />
<br>
<img width="1900" height="898" alt="Screenshot 2026-02-03 144524" src="https://github.com/user-attachments/assets/1653f089-96bb-419a-87d1-5ae8b6a9a73e" />
<br>
wat we hier zien zijn een aantal SVGs die tot enorm grote proporties zijn geplaatst in de pagina’s. Niet is dit alleen veel scroll werk dat in één keer wordt opgedragen aan de gebruiker, het is ook een beetje ‘slordig’ in de manier van opzetten zonder na te denken aan hoe iemand zonder CSS hier misschien naar zou kijken. Kijk bijvoorbeeld eens naar methoden die bekend staan als Progressive Enhancement of Graceful Degradation, deze methoden helpen al meteen voor een ‘usable’ website. Wat deze SVGs ook helaas doen is dat ze VEELS te groot zijn voor het list-item dat ze behuisd. Wat er weer voor kan zorgen dat mensen verward raken van een visueel blanco veld. 

Een ander iets dat ik veel zie is het gebruik van een span. Ik zie het veel gebeuren bij tekst dat het laatste gedeelte uitgelicht moet worden. Dit duidt aan een belangrijk stukje informatie dat niet zal moeten missen. Gelukkig bestaat er een semantisch, verantwoordelijk stukje code voor dit. Dit is de `<strong>`. Dit element neemt de natuurlijke waarde van een [strong](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/strong) aan, maar kan gewoon gestyled worden zoals nodig is. Dit verwijdert de span die niet meer nodig is en het kan gewoon in [p element worden geïmplementeerd](https://codepen.io/Sidopjescherm/pen/dPXKXMV).

Wat ik ook heb getest op de website is het gebruik maken van de tabtest. Het is een simpele test die opgegeven wordt via het [a11y](https://www.a11yproject.com/checklist/) project en het helpt met het maken van een toegankelijke website. Een vrij interessante bevinding op de website is dat sommige elementen niet juist worden geïndexeerd volgens mijn testen. Op mobiel en tablet kwam ik erachter dat het ‘hamburger-menu’ niet wordt opgenomen door de tab-toets. Iets dat vrij problematisch kan worden als je als ‘mobiele’ gebruiker een screenreader of hover actie gebruikt. Er gebeurt het volgende:
VRcafe logo wordt herkend,
Hamburger menu niet,
Eerste select op boeken,
tweede select op boeken.
<br>
<img width="262" height="130" alt="tab wel logo" src="https://github.com/user-attachments/assets/2c76c021-9714-4071-b5cc-ea2cf306ec0b" />
<br>
<img width="80" height="73" alt="geen tab menu" src="https://github.com/user-attachments/assets/39240d9c-1348-403f-8ae6-7960d67d3a5a" />
<br>
<img width="192" height="97" alt="tab 1 kopen" src="https://github.com/user-attachments/assets/ae1bba08-0f85-4597-ab7b-de27fae08bf9" />
<br>
<img width="146" height="58" alt="tab 2 kopen" src="https://github.com/user-attachments/assets/2601bea9-728b-4b6d-89f7-38d6856c56f1" />
<br>

Niet alleen biedt dit niet de mogelijkheid aan om de navigatie te kunnen bedienen, maar blijf je dubbel zitten bij boeken. Ook hier is weer een div geplaatst die geen semantische waarde heeft. Ook dit zou alleen simpel anchor-element kunnen zijn met padding en border-radius, maar het anchor-element zit in een div. Nog terugkomend op het hamburger menu, dit is ook makkelijk te maken met CSS. Je kan JS toepassen voor functionaliteit. Kijk maar eens naar mijn [voorbeeld](https://sidopjescherm.github.io/progressive-enhancement/menu.html). 

als laatste wat ik nog wilde benadrukken met het gebruik maken van anchors is deze simpele pijl voor meer info. De pijl die op en neer beweegt is vormgegeven met JS functionaliteit, maar dit kan veel simpeler. Als je van deze section een `<a>` maakt en in de `<a>`tag een svg zet ben je al een heel eind en het behoort zich gewoon in de scope. Dit is hoe het er nu uitziet:
<br>
<img width="264" height="140" alt="Witte pijl visueel" src="https://github.com/user-attachments/assets/c949cd45-321a-4782-a424-39e301f1bbfe" />
<br>
<img width="963" height="172" alt="Witte pijl code" src="https://github.com/user-attachments/assets/46a44c81-63a1-4125-8608-02dbe6af61bd" />
<br>

maar het kan er nog makkelijker uitzien:
```svelte
<a href='#popActiviteiten'>
	<svg>
		<path></path>
	</svg>
</a>
```

En dat is dan het enige wat in je scope zou staan, dat zou nog beter zijn voor performance en logische code schrijven. 

Als laatste over het semantisch schrijven zijn de ALT attributen die bij de elementen staan. Er wordt inderdaad wel al gebruik gemaakt van ALT, maar misschien nog niet op de manier waarop iedereen er baat bij heeft. Bij het logo van VRcafe is de alt “VRcafe logo,” maar een betere alt zou zijn: “terug naar de homepagina van VRcafe.” Niet alleen is dit beter voor SEO en reading-machines, ook is dit goed voor mensen die een screenreader gebruiken.
<br>
<img width="1383" height="127" alt="Screenshot 2026-02-03 152641" src="https://github.com/user-attachments/assets/88b2a1c5-49c2-4d53-acbc-7481ed0e55a6" />
<br>

Nu na zo’n heel praatje over semantisch/logisch te werk gaan is het vrij logisch om ook te denken: we hebben al zoveel moeite gedaan, ik ga niet heel die website omvergooien alleen voor dit. Een zeer begrijpelijk standpunt, maar wel goed om in het achterhoofd te houden wanneer er nieuwe pagina’s bijkomen of pagina’s een refactoring krijgen.

### Styling
Na dit praatje aan semantisch te werk gaan is er nog aparte styling in de website waar aan gewerkt kan worden. Toen ik ging kijken naar de website kwam ik wel een aantal stukken styling tegen die we gaan bekijken. 

We beginnen weer met de header, want daar zijn een aantal stukken die gelijk opvielen. De media-query die wordt gebruikt bij de header heeft een wat andere breakpoints dan ik gewend ben. Ik zal ze hieronder neerzetten in volgorde:
<br>
320px - 767px
<br>
<img width="412" height="89" alt="Screenshot 2026-02-03 131423" src="https://github.com/user-attachments/assets/623d0b92-8293-4865-adbf-b960617b0ea8" />
<br>
<img width="532" height="94" alt="Screenshot 2026-02-03 131435" src="https://github.com/user-attachments/assets/20cc5aaa-7c49-4e0b-a783-ed41eb0c9e74" />
<br>
767px - 1279px
<br>
<img width="961" height="95" alt="Screenshot 2026-02-03 131442" src="https://github.com/user-attachments/assets/597df909-adc1-44bc-8192-0955398f8c1e" />
<br>
<img width="1127" height="89" alt="Screenshot 2026-02-03 131455" src="https://github.com/user-attachments/assets/af8eeaa3-547d-4b2b-8c26-b729c3558c3c" />
<br>
1280px - ~px
<img width="1003" height="101" alt="Screenshot 2026-02-03 131506" src="https://github.com/user-attachments/assets/9f7866e8-18fc-4417-a395-d8527f366507" />
<br>


Wat mij gelijk opvalt op de header is niet alleen dat de header heel veel ruimte inneemt vanaf 500px, maar dat het ook steeds maar blijft groeien na elke breakpoint. De knop boeken zou al kunnen komen te staan vanaf 600px en nog steeds visueel er goed uitkomen. Het gebruik van ruimte/witruimte is nog beter zichtbaar wanneer we vanaf 767px de header bekijken. In theorie is er dan al genoeg ruimte om iets van contact, info of activiteiten te tonen, maar in plaats daarvan neemt de ruimte, maar niet de inhoud toe. Eenmaal bij 1280px is er ruimte voor ALLE letters in het menu, maar ik zie wel een erg gepropte Nederlandse vlag als talen-selector. 
Nu als oplossing kan ik met trots de ‘@container-query’ aanbieden. Deze query is beter dan een media-query, omdat dit juist de ruimte in een element of component berekent en daarop de content baseert. Hierbij de bronnen:
- [container-query artikel](https://css-tricks.com/css-container-queries/)
- [mijn gebruik ermee](https://github.com/fdnd-agency/oncollaboration/blob/dev/src/lib/organisms/footer.svelte#L20) 

Een ander probleem dat ik heb gezien is de carrousel op de pagina’s. Deze carrousels zouden een leuke, interactieve manier moeten zijn voor de website. Helaas is het op kleinere schermen juist het tegendeel. Waarschijnlijk komt dit, omdat het een geïmporteerd gedeelte is en niet custom-made is voor de website. Er komt een mooie uitlijning voor de gebruiker op mobiel en het is vrij hard voor de ogen om dit zo te zien. Zo ziet het er momenteel uit op mobiel:
<br>
<img width="354" height="620" alt="Carousel dat niet werkt" src="https://github.com/user-attachments/assets/5b28675a-7150-4906-ad40-9381f3643500" />
<br>
<img width="350" height="609" alt="Carousel dat niet werkt 2" src="https://github.com/user-attachments/assets/80833b37-3e42-4531-b6f0-25240ee96f1d" />
<br>
<img width="396" height="590" alt="Kleinere carousel" src="https://github.com/user-attachments/assets/8a1838e6-e4ba-4ad0-8927-1862073727b8" />
<br>

Maar dit is natuurlijk niet wat we willen zien. Zo kan de gebruiker de kaartjes niet goed lezen en is het niet correct uitgelijnd op het scherm. Iets om op terug te kijken zou een voorbeeld zijn dat ik heb gemaakt als oefening op school. Een belangrijk iets om naar te kijken is: `scroll-snap-type:x mandatory;` en `overscroll-behavior:contain;` in deze [codepen](https://codepen.io/Sidopjescherm/pen/JodKZOY). Wat er gebeurt is dat bij elk item dan zal worden stilgestaan zodat bij elk puntje echt gelezen kan worden wat er beschreven is. Een simpele, maar toch effectieve stuk code.

Iets anders dat mij direct opviel was de ruimte die aan de ‘showcases wordt gegeven.’
Het is een vrij ongemakkelijke afkapping van de items die hier staan en dat is vrij jammer, want niet alleen zijn deze items onleesbaar op sommige punten, ze zijn ook weer eens in een div. Als ik de display:block uitzet, dan is alles verwijderd. Erg jammer aangezien je dit ook als een for each loop zou kunnen maken. 
<br>
<img width="1740" height="861" alt="Boeken zakelijk showcase" src="https://github.com/user-attachments/assets/76ec37c9-ceeb-4ab3-9919-0fd5c3d973b2" />
<br>
<img width="1188" height="775" alt="Showcase activiteiten pagina" src="https://github.com/user-attachments/assets/f8d6db04-b6fc-4e24-8090-28c399c877bc" />
<br>

Verder had ik alleen nog een kleine test gedaan op de website met de kleuren die er worden gebruikt. Daarmee kreeg ik deze resultaten eruit:
<br>
<img width="449" height="899" alt="Boeken reguliere knop" src="https://github.com/user-attachments/assets/f42596f3-750a-4359-a5c4-6b2030b48bfa" />
<br>
<img width="456" height="854" alt="Boeken hover" src="https://github.com/user-attachments/assets/54fb4fb2-aa01-4c32-9b5a-fe074a133469" />
<br>
Wat we hieruit kunnen zien is dat de non-actieve knop van 'boeken' wel goed door de test komt op elk niveau van a11y test qua kleur, maar de hover-state komt er helaas niet zo goed door heen. Het haalt de test alleen op AA als titel en op AAA haalt het beide niet. Nu is het wel al goed voor de AA, maar voor een latere versie zou het nog mooier zijn om de AAA test te kunnen behalen. Om ook nog even te laten zien hoe netjes de kleuren worden opgepakt zijn hier nog wat screenshots van de website als iemand kleurenblind zou zijn:
<br>
#### Rood kleurenblind
<img width="1109" height="808" alt="Screenshot 2026-02-04 093850" src="https://github.com/user-attachments/assets/f5358371-fdf1-44c0-bfc7-9989a399ccb5" />
<br>
#### Groen kleurenblind
<img width="1112" height="821" alt="Screenshot 2026-02-04 093903" src="https://github.com/user-attachments/assets/7327eaf8-a322-4865-a2e4-43faf1a5f21a" />
<br>
#### Blauw kleurenblind
<img width="1123" height="826" alt="Screenshot 2026-02-04 093911" src="https://github.com/user-attachments/assets/47cad17a-3e3f-4df8-b728-a7ce0d6ef429" />
