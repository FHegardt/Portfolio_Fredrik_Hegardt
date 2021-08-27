# Arbetsflöde för AI-projekt - Förutspå huspriser

Länk: https://www.run.ai/guides/machine-learning-engineering/machine-learning-workflow/

I denna rapport kommer jag att beskriva de olika stegen & arbetsflödena för att bygga en maskininlärningsalgoritm där målsättningen är att förutspå huspriser baserat på olika features såsom antalet rum, geografiska läget, mm.

För att kunna påbörja detta så måste man börja med den absolut viktigaste grundbulten i all maskininlärning, nämligen datan. Oftast behövs en stor kvantitet av data, för att kunna nå en hög tillförlitlighet i modellen, men datan behöver också vara av bra kvalité. Detta är en stor utmaning generellt inom maskininlärning och AI.

Vi förutsätter att vi får tag i en tillräckligt stor datamängd av tillräckligt bra kvalitét. När jag pratar om "data" i det här fallet så definerar jag varje data som "ett sålt hus med information om antal rum, adress, pris, etc."
För att få tag i denna datan så behöver vi antagligen besöka typiska bostadsförsäljningshemsidor, så som Hemnet, där vi antingen manuellt hämtar hem datan (skriver av) alternativt använder script, så kallad webscraping, för att automatiskt hämta så mycket data som möjligt. (codebaseball.com)



