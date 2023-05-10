# 10e Maj 

I samtliga övningar och material reflektera kring temat för dagen, hur hjälper tester dig att undvika "smelly code"?

## Live-kod

[Live coding examples](live-coding/)

## Material
- [Getting started (react free)](https://jestjs.io/docs/getting-started)
- [Unit tests in react](https://www.freecodecamp.org/news/how-to-write-unit-tests-in-react/)
- [Practical guide to jest in react applications](https://www.smashingmagazine.com/2020/06/practical-guide-testing-react-applications-jest/)
- [Index över jest dom metoder (bokmärk gärna)](https://github.com/testing-library/jest-dom)

## Övningar
I övningarna försök att tänka i termer av user stories när du skapar testen. Kom ihåg, röd-grön-refactor 
- Röd: skriv testet först (ger rött test)
- Grönt: Analysera och fixa koden så att testet passerar 
- Refactor: Utöka komplexiten i koden och gör om ovanstående

En fil behöver innehålla ändelsen *.test.js för att jest ska kunna identifera filen som ett test.

I dessa övningar är det fokus på testerna och inte react så hur du skapar test miljön är valfri. Med andra ord, skapa ett react projekt eller initiera ett nytt npm projekt och installera jest separat.

### Övning 2.1
[Tabell att validera värden mot](https://www.metric-conversions.org/sv/temperatur/fahrenheit-till-celsius.html)

1. Skriv testfall för en funktion som kan omvandla temperatur från grader Fahrenheit till Celsius. Tips: C = (F - 32) / 1.8 . Fahrenheit till Celsius konvertering 
2. När du skrivit testfallen och de blir röda - implementera funktionen, så att testfallet blir grönt. 

### Övning 2.2
- Skriv testfall för (och implementera) en funktion som returnerar true om en person med en viss ålder får lov att köra bil:
isAllowedToDrive(ageInYears, hasLicense) --> boolean

### Övning 2.3
1. Skriv testfall för en funktion med namnet isWord(maybeWord) --> boolean.
Följande kriterier gäller för att något ska anses vara ett ord:
  - paramtern måste vara en sträng
  - strängen får inte var atom
  - strängen ska bara innehålla bokstäver, små eller stora, "Pelle" är ok, men inte "Pe1e"
2. Ett nytt kriterium: för varje vokal ska strängen innehålla 1-2 konsonanter.


### Övning 2.4
Skriv testfall utifrån följande kravspec:
<em>Det ska finnas två funktioner: store och retrieve. Funktionen store ska ta en parameter. När man anropar den ska värdet på parametern sparas. Funktionen retrieve ska inte ha några parametrar. När den anropas ska den returnera värdet som man senast sparade med store.</em>

<pre>
Exempel:
  store(1)
  retrieve()  // returnerar 1
  store(2)
  store(100)
  retrieve()  // returnerar 100
</pre>

### Övning 2.5
Året är 2027. Som en del i ett system för kylning av reaktorer i fusionskraftverk, som ditt företag bygger, behövs en modul som talar om när olika kylvätskor börjar koka. Din uppgift är att skriva den första funktionen. Till din hjälp har du en kravspec i form av några kommentarer i koden:

```
    // Returns true if water would be boiling at the specified temperature
    // Throws an Error on illegal input
    function isWaterBoiling(degreesCelsius) { }
```

Efter några spektakulära missöden har företaget beslutat sig för att använda TDD i hela systemet. Du ska alltså skriva testfall med Jest.

Diskutera (gärna) följande frågor med en klasskamrat:
1. Vilka värden kan parametern degreesCelsius ha?
2. Vilka värden kan funktionen returnera?
3. När bör funktionen kasta ett Error? (med ett beskrivande felmeddelande)
4. Behövs fler sorters Error? Motivera ert svar.
5. Finns det värden som är viktigare att testa än andra? Varför?
