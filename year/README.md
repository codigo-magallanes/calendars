# Year Calendars
## calendar.html
 Previous version of index.html
### Calendar characteristics
 - No moon data
## index.html
It holds all the html, CSS, javascript and info
### Calendar characteristics
 - Year begins nex day from new moon right before winter solstice (NH)
 - 5 days week
 - Every month begins monday first
 - Week ends when month ends and next one begins in 'monday'
 . Shows full and new moons
 - Shows gregorian dates
### Code
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