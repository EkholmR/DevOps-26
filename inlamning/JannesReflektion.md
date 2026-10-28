Under kursens gång har jag fått en bättre förståelse för hur de olika delarna av utvecklingsprocessen hänger ihop. 

I M1 började vi med att skapa repot och lägga in den första versionen av koden. Då behövde vi hålla koll på ändringar och commits själva och samarbeta kring hur vi skulle arbeta med olika branches. 

När vi kom till M2 blev arbetsprocessen tydligare genom att vi införde branch protection och pull requests. Det innebar att ändringar behövde granskas innan de kunde slås ihop med main.

I M3 arbetade vi med Docker för att kunna köra frontend och backend i separata containrar. Med Docker Compose blev det enklare att starta båda delarna samtidigt. Det blev tydligare för mig hur man kan skapa en miljö som fungerar på ett liknande sätt både lokalt och i produktion.

I m4 lärde jag mig mycket då vi upptäckte ett fel i applikationen. När en anteckning togs bort uppdaterades inte det totala antalet tecken som det skulle. Vi hade redan tester som fungerade, men de kontrollerade inte just den situationen. Därför skrev vi ett nytt test där vi skapade två anteckningar, raderade en av dem och kontrollerade att summan stämde. Testet visade att det faktiskt fanns ett problem. Det fick mig att inse att ett lyckat testresultat inte automatiskt betyder att hela programmet är felfritt. Testerna måste också täcka olika situationer som kan uppstå när användaren använder applikationen.

I M5 började vi använda GitHub Actions för att automatisera tester och linting. Vi såg bland annat hur Ruff upptäckte en felaktig kodändring som vi hade lagt in medvetet. Det gjorde det tydligt att kontrollerna kan fånga upp misstag redan innan koden går vidare i utvecklingsprocessen.

I M6 fortsatte vi med att automatisera byggandet och publiceringen av Docker-images till GHCR. På så sätt behövde vi inte utföra alla dessa steg manuellt varje gång en ny version skulle skapas.

I M7 fick vi sätta upp en virtuell maskin i cPouta och konfigurera bland annat nätverk, säkerhetsregler och SSH. Vi installerade Docker och startade applikationen på maskinen. Det var ett moment där flera delar behövde fungera tillsammans, men instruktionerna hjälpte oss att genomföra det. 

I M8 använde vi sedan Terraform för att beskriva infrastrukturen i kod. Jag upplevde att det gav en bättre överblick över vilka inställningar som behövdes och gjorde det lättare att återskapa miljön utan att börja om från början manuellt.

I det sista momentet M9, kopplade vi ihop arbetet med automatisk driftsättning. GitHub Actions byggde och publicerade images och kunde sedan uppdatera applikationen på den virtuella maskinen via SSH. Det var intressant att se hur de olika momenten till slut bildade en helhet. En kodändring kunde nu gå från repot till en driftsatt applikation genom en automatiserad process. Jag fick därmed en tydligare bild av hur ett utvecklingsflöde kan fungera i ett verkligt projekt.