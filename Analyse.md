# Analyse VRCafe

## Mijn bevindingen
Na de hele ochtend te testen op de website en te kijken naar de website in de styling kwam ik achter een aantal dingen die mij opvielen. Eerst wilde ik het hebben over wat het VRcafe is, zodat de boodschap helder is voor mij. 

Het VRcafe is een plek dat ervaringen aanbiedt in de wereld van Virtual Reality. Je kan games uit categorieën kiezen zoals: shooters, multiplayer, family, kids en meer. 

### Opzet
Na het lezen van de documentatie zie ik dat het VRcafe gebruik maakt van: TailwindCSS, Astro, React components en Starlight(dat samenwerkt met Astro.) Toen ik de devtools opende zag ik wel al een paar meldingen die belangrijk zijn om te zien.
 

een aantal van deze error komen van het incorrect plaatsen van bepaalde code. Er zijn een aantal fouten die ik momenteel alleen zie in het zogeheten ‘-partytown.’ Dit lijkt mij een omgeving die gebruikt wordt voor de backend, maar ik zie wel veel meldingen vanuit hier komen. Het meeste hiervan is backend en daar heb ik bijna niets mee te maken, maar wat ik aantref qua opmaak van de website is wel om iets van te noteren en iets waar ik wat aan kan doen. 

### Semantisch werken en styling
Semantische code schrijven is wel het meest verstandige om te doen. Zo help je niet alleen jezelf en je huidige collega’s, maar ook toekomstige collega’s met het schrijven van deze code. Het meeste van de code die uitgelegd wordt staat op de docs repo in Github en dat is erg fijn. Wat ik wel heb gemerkt is dat de website echt niet vriendelijk is als je CSS uit hebt staan. Nu zal een tegen argument zijn dat niemand CSS uit heeft staan, maar het verslaat wel het principe van het web als geheel. Het moet toegankelijk blijven voor mensen vanuit alle windstreken, met welk lichaam dan ook. Wat ik hiermee bedoel ik dat mensen met een motorische stoornis, geen armen of gebruik maken van een screenreader ook gebruik moeten kunnen hebben bij de website. 

Wat mij opviel bij deze website is dat afbeeldingen/svg’s niet een standaard waarde krijgen meegegeven als ze worden ingeladen. Dit zorgt ten eerste voor webpagina’s waar de eerste gedeelten van het scrollen bestaan uit de header zelf. Vele iconen die worden gebruikt in de header zijn VEELS te groot. Vele tekens nemen een heel scherm op in grootte. Via mijn DEVtools ben ik erachter gekomen hoe het zonder CSS eruit zou zien. Hier een aantal voorbeelden die mij erg opvielen:


wat we hier zien zijn een aantal SVGs die tot enorm grote proporties zijn geplaatst in de pagina’s. Niet is dit alleen veel scroll werk dat in één keer wordt opgedragen aan de gebruiker, het is ook een beetje ‘slordig’ in de manier van opzetten zonder na te denken aan hoe iemand zonder CSS hier misschien naar zou kijken. Kijk bijvoorbeeld eens naar methoden die bekend staan als Progressive Enhancement of Graceful Degradation, deze methoden helpen al meteen voor een ‘usable’ website. Wat deze SVGs ook helaas doen is dat ze VEELS te groot zijn voor het list-item dat ze behuisd. Wat er weer voor kan zorgen dat mensen verward raken van een visueel blanco veld. 

Een ander iets dat ik veel zie is het gebruik van een span. Ik zie het veel gebeuren bij tekst dat het laatste gedeelte uitgelicht moet worden. Dit duidt aan een belangrijk stukje informatie dat niet zal moeten missen. Gelukkig bestaat er een semantisch, verantwoordelijk stukje code voor dit. Dit is de `<strong>`. Dit element neemt de natuurlijke waarde van een strong aan, maar kan gewoon gestyled worden zoals nodig is. Dit verwijdert de span die niet meer nodig is en het kan gewoon in p element worden geïmplementeerd.

voorbeelden:


Wat ik ook heb getest op de website is het gebruik maken van de tabtest. Het is een simpele test die opgegeven wordt via het a11y project en het helpt met het maken van een toegankelijke website. Een vrij interessante bevinding op de website is dat sommige elementen niet juist worden geïndexeerd volgens mijn testen. Op mobiel en tablet kwam ik erachter dat het ‘hamburger-menu’ niet wordt opgenomen door de tab-toets. Iets dat vrij problematisch kan worden als je als ‘mobiele’ gebruiker een screenreader of hover actie gebruikt. Er gebeurt het volgende:
VRcafe logo wordt herkend,
Hamburger menu niet,
Eerste select op boeken,
tweede select op boeken.

Visuele representatie:
 =>  =>=>

Niet alleen biedt dit niet de mogelijkheid aan om de navigatie te kunnen bedienen, maar blijf je dubbel zitten bij boeken. Ook hier is weer een div geplaatst die geen semantische waarde heeft. Ook dit zou alleen simpel anchor-element kunnen zijn met padding en border-radius, maar het anchor-element zit in een div. Nog terugkomend op het hamburger menu, dit is ook makkelijk te maken met CSS. Je kan JS toepassen voor functionaliteit. Kijk maar eens naar mijn voorbeeld. 

als laatste wat ik nog wilde benadrukken met het gebruik maken van anchors is deze simpele pijl voor meer info. De pijl die op en neer beweegt is vormgegeven met JS functionaliteit, maar dit kan veel simpeler. Als je van deze section een <a> maakt en in de `<a>`tag een svg zet ben je al een heel eind en het behoort zich gewoon in de scope. Dit is hoe het er nu uitziet:


maar het kan er nog makkelijker uitzien:
`<a href=’#popActiviteiten>
	<svg>
		<path></path>
	</svg>
</a>`

En dat is dan het enige wat in je scope zou staan, dat zou nog beter zijn voor performance en logische code schrijven. 

Als laatste over het semantisch schrijven zijn de ALT attributen die bij de elementen staan. Er wordt inderdaad wel al gebruik gemaakt van ALT, maar misschien nog niet op de manier waarop iedereen er baat bij heeft. Bij het logo van VRcafe is de alt “VRcafe logo”, maar een betere alt zou zijn: “terug naar de homepagina van VRcafe.” Niet alleen is dit beter voor SEO en reading-machines, ook is dit goed voor mensen die een screenreader gebruiken.


Nu na zo’n heel praatje over semantisch/logisch te werk gaan is het vrij logisch om ook te denken: we hebben al zoveel moeite gedaan, ik ga niet heel die website omvergooien alleen voor dit. Een zeer begrijpelijk standpunt, maar wel goed om in het achterhoofd te houden wanneer er nieuwe pagina’s bijkomen of pagina’s een refactoring krijgen.

### Styling
Na dit praatje aan semantisch te werk gaan is er nog aparte styling in de website waar aan gewerkt kan worden. Toen ik ging kijken naar de website kwam ik wel een aantal stukken styling tegen die we gaan bekijken. 

We beginnen weer met de header, want daar zijn een aantal stukken die gelijk opvielen. De media-query die wordt gebruikt bij de header heeft een wat andere breakpoints dan ik gewend ben. Ik zal ze hieronder neerzetten in volgorde:
320px - 767px
<br>
<img width="412" height="89" alt="Screenshot 2026-02-03 131423" src="https://github.com/user-attachments/assets/623d0b92-8293-4865-adbf-b960617b0ea8" />
<br>
<img width="532" height="94" alt="Screenshot 2026-02-03 131435" src="https://github.com/user-attachments/assets/20cc5aaa-7c49-4e0b-a783-ed41eb0c9e74" />
<br>
767px - 1279px


1280px - ~px


Wat mij gelijk opvalt op de header is niet alleen dat de header heel veel ruimte inneemt vanaf 500px, maar dat ook steeds maar blijft groeien na elke breakpoint. De knop boeken zou al kunnen komen te staan vanaf 600px en nog steeds visueel er goed uitkomen. Het gebruik van ruimte/witruimte is nog beter zichtbaar wanneer we vanaf 767px de header bekijken. In theorie is er dan al genoeg ruimte om iets van contact, info of activiteiten te tonen, maar in plaats daarvan neemt de ruimte, maar niet de inhoud toe. Eenmaal bij 1280px is er ruimte voor ALLE letters in het menu, maar ik zie wel een erg gepropte Nederlandse vlag als talen-selector. 
Nu als oplossing kan ik met trots de ‘@container-query’ aanbieden. Deze query is beter dan een media-query, omdat dit juist de ruimte in een element of component berekent en daarop de content baseert. 

Een ander probleem dat ik heb gezien is de carrousel op de pagina’s. Deze carrousels zouden een leuke, interactieve manier moeten zijn voor de website. Helaas is het op kleinere schermen juist het tegendeel. Waarschijnlijk komt dit, omdat het een geïmporteerd gedeelte is en niet custom-made is voor de website. Er komt een mooie uitlijning voor de gebruiker op mobiel en het is vrij hard voor de ogen om dit zo te zien. Zo ziet het er momenteel uit op mobiel:


Maar dit is natuurlijk niet wat we willen zien. Zo kan de gebruiker de kaartjes niet goed lezen en is het niet correct uitgelijnd op het scherm. Iets om op terug te kijken zou een voorbeeld zijn dat ik heb gemaakt als oefening op school. Een belangrijk iets om naar te kijken is: ‘scroll-snap-type:x mandatory;’ en ‘overscroll-behavior:contain;’ in deze codepen. Wat er gebeurt is dat bij elk item dan zal worden stilgestaan zodat bij elk puntje echt kan lezen wat er beschreven is. Een simpele, maar toch effectieve stuk code.

Iets anders dat mij direct opviel was de ruimte die aan de ‘showcases wordt gegeven.’
Het is een vrij ongemakkelijke afkapping van de items die hier staan en dat is vrij jammer, want niet alleen zijn deze items onleesbaar op sommige punten, ze zijn ook weer eens in een div. Als ik de display:block uitzet, dan is alles verwijderd. Erg jammer aangezien je dit ook als een for each loop zou kunnen maken. 
