# Arbetsflöde för AI, förutspå huspriser

## Bakgrund

I denna rapport kommer jag att beskriva de olika stegen & arbetsflödena för att bygga en maskininlärningsalgoritm där målsättningen är att förutspå huspriser baserat på olika features såsom antalet rum, geografiska läget, mm.

## Steg 1 - Datainsamling och databearbetning
 
För att kunna påbörja detta så måste man börja med den absolut viktigaste grundbulten i all maskininlärning, nämligen datan. Oftast behövs en stor kvantitet av data, för att kunna nå en hög tillförlitlighet i modellen, men datan behöver också vara av bra kvalité. Detta är en stor utmaning generellt inom maskininlärning och AI. (1)

Vi förutsätter att vi får tag i en tillräckligt stor datamängd av tillräckligt bra kvalitét. När jag pratar om "data" i det här fallet så definerar jag varje data som "ett sålt hus med information om antal rum, adress, pris, försäljningsår etc." (1)

För att få tag i denna datan så behöver vi antagligen besöka typiska bostadsförsäljningshemsidor, så som Hemnet, där vi antingen manuellt hämtar hem datan (skriver av) alternativt använder script, så kallad webscraping, för att automatiskt hämta så mycket data som möjligt. (2)

Nästa steg blir att spara ned och "tvätta datan" så gott det går. Ett bra system för att spara data är, precis som det låter, en databas. En databas använder vi för att kunna organisara stora mängder data samt att vi enkelt ska kunna hämta datan som vi behöver för att göra analyser. När jag säger "tvätta datan" så syftar jag på att den måste vara organiserad på rätt sätt. (3) Exempelvis måste alla försäljningspriser vara sammankopplade med rätt objekt samt ligga på rätt rad. Ligger datan "huller om buller" blir det väldigt svårt att analysera den.

Det kan behövas mycket tid att bearbeta datan om den kommer från olika källor, exempelvis kanske vissa använder kommatecken i "huspriset" och vissa använder punkter. Vi måste då formattera datan så att formatet är detsamma oavsett källa. (1)

## Steg 2 - Maskininlärningsprocessen och linjär regression

När är alla de första stegen är klara, datan är strukturerad och tvättad, så kommer vi dela upp data i tre olika data-set. Jag förklarar varför nedan.

1. Träningsdata - Den data vi använder för att initialt träna vår modell, sätta parametrar och olika lager.

2. Valideringdata - Data som vi använder för att testa att vår modell ger tillförlitliga svar efter att den har blivit tränad. Här har vi chans att skruva på parametrarna för att förbättra modellen.
3. Test-set - Sist men inte minst behöver vi en sista set med data, detta för att kunna testa vår modell på verklig data som den inte har sett förut. Ett sista valideringstest helt enkelt, där vi får fram resultatet av modellen innan vi går ut med den på riktigt. (1)

När datan är uppdelad i tre olika set så kan vi äntligen påbörja vår träning av modellen genom maskininlärning. Det finns oerhört många olika algoritmer och sätt att träna en modell, här kommer jag kort beskriva linjär regression som är ett väldigt vanligt sätt att lära system. (4)

Kortfattat så använder man linjär regression för att hitta sambandet mellan två olika datatyper, i vårt fall skulle det exempelvis kunna vara att hitta sambandet mellan huspriser och kvm-yta. Ett sätt att visualisera datan är att skapa en plot med x- och y-linjer där man sätter en markör för varje objekt. Huspriser löper längs x-axeln och kvm-ytan längs y-axeln. När man har markerat tillräckligt antal prickar så kommer det gå att se ett samband, om det finns ett, mellan x & y. Vanligtvis så går det att dra en linje, såkallad regressionslinje, vilket förklarar sambandet mellan x & y.

Detta gör att modellen i nästa steg, när den får ny data, kommer kunna ge förutsägelser om x när den bara har tillgång till y eller vice verca. (4)

## Steg 3 - Driftsättning

Det sista steget blir att driftsätta modellen. För att säkrast driftsätta den här typen av modell hade jag använt en betaversion som en sista del av testning, innan jag driftsatt det fullt ut publikt.

Varför jag använder mig av en betaversion är för att kunna följa hur det fungerar i verkligheten med nya data som vi inte har tillgång till idag, alltså de kommande försäljningspriserna. Förslagsvis följer vi modellens förutsägelser i 2-3 månader, känner vi oss nöjda med resultatet och förutsägelserna på den nya datan är tillräckligt goda, så är vi redo att driftsätta det publikt.

Här lämnar vi över till "Front-end"-utvecklarna och företagets marknadsavdelningen att med deras expertis driftsätta modellen på rätt ställe, exempel i en app, på hemsidan eller i något annan digitalt forum.


Länkar:
1. https://www.run.ai/guides/machine-learning-engineering/machine-learning-workflow/
2. codebaseball.com
3. https://sv.wikipedia.org/wiki/Databas
4. https://www.javatpoint.com/linear-regression-in-machine-learning

