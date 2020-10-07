# Calendars
## Year
### calendar.html
 Previous version of index.html
#### Calendar characteristics
 - No moon data
### index.html
It holds all the html, CSS, javascript and info
#### Calendar characteristics
 - Year begins nex day from new moon right before winter solstice (NH)
 - 5 days week
 - Every month begins monday first
 - Week ends when month ends and next one begins in 'monday'
 . Shows full and new moons
 - Shows gregorian dates
#### Code
 Month days:
 ```js
const mesesARRAY = [
    "Capricornio",
    "Acuario",
    "Piscis",
    "Aries",
    "Tauro",
    "Géminis",
    "Cáncer",
    "Leo",
    "Virgo",
    "Libra",
    "Escorpio",
    "Sagitario",
    "Andrómeda",
  ];
const monthDays = mesesARRAY.map((x, i) => {
    return i % 2 === 0 ? 30 : 29;
  });
if ( yearNSC % 2 != 0 ) monthDays[3] = 30
if ( yearNSC % 33 === 0 ) monthDays[2] = 30
 ```
 ## Month
 ### original.html

 Original code from internet.
  - Prints actual month with day and time

### mod.html

 Some changes to the original, but it does not work.

 
### index.html

- prints actual month with actual date and time

#### Calendar characteristics

- 5 days week
- month days calculated to match approx. moon phases

```
function getDays(month, year) {
       var ar = new Array(13);
       for (let i = 0; i <= 12; i++) {
         i % 2 === 0 ? ar[i] = 30 : ar[i] = 29;
       }
       return ar[month];
     }
```

- diff approach

```
function leapYear(year) {
  if (year % 4 == 0) return true
}

var ar = new Array(12);
   ar[0] = 31; // January
   ar[1] = leapYear(year) ? 29 : 28; // February
   ar[2] = 31; // March
   ar[3] = 30; // April
   ar[4] = 31; // May
   ar[5] = 30; // June
   ar[6] = 31; // July
   ar[7] = 31; // August
   ar[8] = 30; // September
   ar[9] = 31; // October
   ar[10] = 30; // November
   ar[11] = 31; // December
```