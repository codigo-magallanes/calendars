# Month Calendars

## original.html

 Original code from internet.
  - Prints actual month with day and time

## mod.html

 Some changes to the original, but it does not work.

 
## index.html

- prints actual month with actual date and time

### Calendar characteristics

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
