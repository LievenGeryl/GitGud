# GitGud: The Basics

*Disclaimer: Als er hier iets niet overeenkomt met wat de lector zegt of wat in de cursus staat, ben ik verkeerd. Zeg het mij ook AUB. Deze guide is zeer basic en zegt niks over branches of het linken van een lege, lokale repo met een remote repo of wat dan ook. Hier zul je geen gedoe zoals "remote branch origin master big chungus 3000 rm -rf" vinden. Oh and I suck at Markdown*

**Note: Alles wat tussen vierkante haakjes([]) staat, inclusief de vierkante haakjes zelf, zijn dingen waar je dus ook je eigen input moet geven. Ik weet uiteraard niet welke commit messages je zult gebruiken of wat de link naar jouw remote repository is**

## Begrippen & concepten

> Local repository

Je map die je gecloned hebt van de "remote repository" (Zie volgend begrip), of wat je gemaakt hebt met ```git init```. Alle mappen en files die hier "onder" zitten, zouden normaal gezien moeten bij je local repository moeten horen.

> Remote repository

Deze repository is, for all intents & purposes, wat er op GitHub staat. Als je niet actief bezig bent met programmeren, zou de remote repository dus ook de laatste nieuwe versie moeten hebben van je code. Dit is handig omdat je dus ook zonder problemen kan verder werken aan je code op een ander toestel die ook Git heeft, door deze repository gewoon te clonen.

> Init

Via ```git init``` maak je een kersverse repository aan. 
**Let op:** In veel gevallen zul je dit commando eigenlijk niet nodig hebben voor opdrachten waar je een link naar GitHub gekregen hebt. Het is misschien één van de eerste commando's dat we geleerd hebben, maar dat betekent niet dat het ook het meest gebruikte commando is!

> Clone

Via ```git clone [URL]``` pak je een volledige remote repository, en zet je hem op de plek waar je nu bezig bent. Die "plek" is een path, en die kun je hier vinden: **ADD SCREENSHOT "PATH/LOCATION"**
Wanneer je een repository "cloned" sleurt hij dus alles mee naar binnen. **Hiervoor moet je dus geen** ```git init``` **doen, in theorie zul je ook maar 1x per project dit commando moeten doen**

> Pull 

Wanneer je  ```git pull``` doet, vergelijkt het commando de files en mappen in je local repository met die van de remote repository. Indien er files of mappen op de **remote** repository zijn die niet in je local repository zijn, zal hij deze "downloaden" en op de juiste plek zetten zodat het de mappenstructuur die op je remote repository staat te simuleren. 
**Dit commando moet je niet gebruiken net nadat je gecloned hebt,** en zul je dus waarschijnlijk niet vaak gebruiken wanneer je alleen werkt. Wel is dit commando handig wanneer je bijvoorbeeld een website ontwerpt samen met iemand anders. Die persoon kan bijvoorbeeld enkele nieuwe pagina's (HTML files dus) gemaakt & op GitHub gezet hebben terwijl je bezig was met iets anders. Door een "pull" te doen kun je dus deze pagina's gemakkelijk ook in je local repository hebben.

> Add, Commit, Push

Wanneer je blij bent met de veranderingen in je code, zal je vast en zeker alles mooi op GitHub willen smijten omdat het daar ook is waar we de meeste oefeningen zullen "indienen" omdat onze Remote Repositories door de lectoren kunnen bekeken (en dus ook "verbeterd") kunnen worden. 
De volgorde hier is als volgt:
```
git add [filename.extension]
git commit -m "[a useful message]"
git push
```

> Status

```git status``` toont de files/mappen die veranderd of nieuw zijn in het rood. Hier is er een voorbeeld: **ADD SCREENSHOT STATUS**
Als je deze allemaal zou klaarzetten om te committen met ```git add```, zouden ze in het groen staan, wat ook goed is. Je kunt niet veel verkeerd doen door ```git status``` in te typen, het toont gewoon welke files klaar zijn om te committen.

## Praktisch voorbeeld

Je krijgt een opdracht, deze opdracht is een link naar een remote repository die staat op GitHub. In de README.md zal de opdracht waarschijnlijk staan. De README zul je ook onmiddelijk zien omdat deze file "openstaat" op de GitHub pagina. De pagina die je nu leest is eigenlijk de README.

In mijn voorbeeld zullen we de repository van de guide gebruiken en doen alsof het een opdracht is. De eerste stap is om alles wat op de remote repository staat, ook op onze local repository te krijgt. Maak een nieuwe map aan, of ga naar een map waar je repository in mag staan. Rechtermuisknop -> "Git bash here" en laat dit scherm open staan. Ga dan weer naar de repository op GitHub en onderneem de volgende stappen:
**ADD SCREENSHOT HOWTOCLONE1&2**

Zoals je ziet heb ik hier het commando ```ls``` gebruikt. Dit was om te zien wat ik nu precies binnengehaald heb. Het is een map genaamd "GitGud", wat ook onze local repository is geworden.
Daarna gebruik ik ```cd GitGud```. Dit is omdat we binnen in de repository willen werken, niet er buiten. 

Nu kun je gewoon doen wat de opdracht je vraagt, zorg gewoon dat alle files die je uiteindelijk zal moeten "indienen/pushen" ook effectief in de map GitGud zitten of in maps die daar onder vallen.

Wanneer je klaar bent, of tussentijds eens wil pushen, doe je het gewoon zo:
**ADD SCREENSHOT HOWTOUPLOAD**

And that's it. Dat zijn de basics. 


## Additional Tips

* Zoals je misschien zag in de laatste screenshot, deed ik ```git add .```. Door het puntje te gebruiken in plaats van een filename, "add" je eigenlijk alles dat er kan added worden. Dit spaart typwerk uit. Dit zou voor problemen kunnen zorgen wanneer je files in je local repository zet die niet op de remote repository mogen staan, maar als je aan dat stadium zit dan hoop ik dat je al weet wat je doet en dingen zoals gitignore gebruikt.

* Indien je te lui bent zoals ik om rond te klikken en te doen, kun je eigenlijk redelijk wat doen in de commandolijn:
    * ```touch [filename.extension]``` maakt een lege file aan met de gekozen extention. ```touch index.html``` zou bijvoorbeeld een lege HTML pagina maken.
    * ```mkdir [mapname]``` maakt een nieuwe map aan.
        * ```mkdir``` staat voor "make directory". Een directory is een map.
    * ```rm [filename/mapname]``` verwijdert die file. 
        * ```rm``` staat voor "remove".
    * ```mv``` heeft twee usages. ```mv [filename] [mapname]``` laat je de file verplaatsen in een map. ```mv [filename] [filename2]``` laat je de file van naam veranderen. Dit kan in beide gevallen mislopen als er een file met die naam bestaat in dezelfde map (of in het eerste geval, de "destination" map). Dit kun je forceren door ```mv -f [filename] [filename/mapname]``` te doen. **Let wel op dat je hierdoor die file zal overwriten**.
        * ```mv``` staat voor move, ```-f``` staat voor force.

* ```cd``` staat voor "Change Directory", indien je de vorige tip las weet je wat directory betekent.

* Als je een filename of een map wil noemen, en de naam is echt lang (zoals ```st-2122-1-S1G1-pe1-labo1-LievenGeryl```), kun je het begin van de naam intypen en dan op "TAB" duwen. Dan vult hij de rest automatisch aan.

* Denk je dat je teveel zit te foefelen met je local repo? Is er iets zwaar misgelopen? Begin opnieuw met een nieuw-gekloonde repository. Git maakt je workflow sneller en efficiënter, dus als je echt lang bezig bent omdat je God knows what hebt gedaan in je repo en/of mappen, begin gewoon opnieuw. Files & code kan gekopieerd worden naar de nieuwe lokale repo. Je kan alle files dus gemakkelijk terug krijgen. Hetzelfde kan niet gezegd worden over je wil om te leven of om nuchter te blijven na 3 uren lang te zitten foefelen in de commandline, om iets te doen wat eigenlijk maar 3 minuten zou moeten kosten.
