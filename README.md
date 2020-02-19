# A Calendar for Time to Come

### Summary

- A [perennial](https://en.wikipedia.org/wiki/Perennial_calendar) [solar calendar](https://en.wikipedia.org/wiki/Solar_calendar) for Earth based on astronomical observations
  - Standing on the shoulders of the Persian [Solar Hijri](https://en.wikipedia.org/wiki/Solar_Hijri_calendar) and [Jalali](https://en.wikipedia.org/wiki/Jalali_calendar) calendars <sup>[1](#notes)</sup>
  - With roots in the [Zoroastrian calendar](https://en.wikipedia.org/wiki/Zoroastrian_calendar) and possibly the [Egyptian calendar](https://en.wikipedia.org/wiki/Egyptian_calendar) <sup>[2](#notes)</sup>
- The [calendar year](https://en.wikipedia.org/wiki/Calendar_year) begins at the [northward equinox](https://en.wikipedia.org/wiki/March_equinox) measured from the [prime meridian](https://en.wikipedia.org/wiki/Prime_meridian)
- 360 calendar days + 5 or 6 [intercalary/epagomenal](https://en.wikipedia.org/wiki/Intercalation_(timekeeping)#Solar_calendars) days
  - 4 quarters of 91 days (1 intercalary and 90 calendar days)
  - 8 "months" of 45 calendar days
  - 40 "weeks" of 9 calendar days
    - `3 * 3` days (based on the "tridays" of the [Liberalia Triday Calendar][8])
  - 1 or 2 intercalary transition days at the end of the year
- Proposed [epoch](https://en.wikipedia.org/wiki/Epoch) is the beginning of the human era (10001 BC)

**Essentially, the Persian calendar with a different meridian, different division of the year and a different epoch.**

### Advantages

- **[Accurate](#accuracy)** — forever when based on astronomical observations
- **Simple** — division of the year into 2, 4 and 8 equal parts makes it easy to learn and visualize
- **Dynamic** — grouping of days into `3 * 3` is a [powerful concept][3]
- **Perennial** — dates and seasons are fixed
- **Structured** — yet flexible enough to adapt to different uses and cultures
  - **Civil** — simple, predictable
  - **Agriculture** — seasonal, follows natural cycles
  - **Business** — evenly divided, flexible scheduling
- **Neutral**
  - Not tied to any culture/religion, except inevitably to that of the current scientific paradigm
  - While it is scientifically grounded, it does not oppose combination with cultural or religious concepts

### Disadvantages

- **No simple leap year rule** — a tradeoff for astronomical accuracy
- **Unfamiliarity** — different units and dates ("[months](https://en.wikipedia.org/wiki/Month)", "[weeks](https://en.wikipedia.org/wiki/Week)", new year, epoch)
- **Yet another calendar** — made by some commoner named Joakim (who is not the pope)

## Definition

### New Year

> The calendar year begins at the midnight closest to the instant of the northward equinox. Consequently, if the northward equinox falls _before_ solar noon on a particular day, then that day is the first day of the year. If the northward equinox occurs _after_ solar noon, the following day begins the calendar year.

- This may be calculated for the prime meridian ([Meeus, 2002][4]) or observed locally (even with a [sundial](https://en.wikipedia.org/wiki/Sundial))
  - Calculations should be based on the instant of the northward equinox at the prime meridian <sup>[3](#notes)</sup>
  - Local new year is then easily calculated from this instant using an offset (for example UTC time zone)
- The _local_ new year should be celebrated, not that of the prime meridian <sup>[4](#notes)</sup>
- Leap years follow a 33 year cycle, like the Persian calendar ([Heydari-Malayeri, 2004][1])
  - Calculations should use the _real northward equinox year_, not to be confused with the _mean tropical year_ <sup>[5](#notes)</sup>

### Units

- **year:** 360 calendar days + 5 or 6 intercalary days
- **quarter:** 1/4 of a year's 360 calendar days + 1 intercalary day
- **eighth:** 1/8 of a year's 360 calendar days
- **nonad:** 9 calendar days
- **triad:** 3 calendar days
- **day:** 1 [nychthemeron](https://en.wikipedia.org/wiki/Nychthemeron)

The names "eighth", "nonad" and "triad" are descriptive only, better names should be adopted.

### Structure

- The year has 360 calendar days and 5 (common year) or 6 (leap year) intercalary days
- The year is divided into 4 equal quarters, each having 91 days
  - 1 intercalary day that represents the equinox/solstice
  - 90 calendar days
- The year's 360 calendar days may be divided as follows
  - Proposed division: 8 eighths ("months") and 40 nonads ("weeks")
    - 8 eighths of 45 calendar days (2 eighths per quarter)
    - 40 nonads of 9 calendar days (10 nonads per quarter, 5 nonads per eighth)
      - Each nonad may be further divided into 3 triads of 3 calendar days
  - Traditional division: 12 "months"
    - 12 months of 30 calendar days (3 months per quarter)
    - Drawback: A month can not fit a whole number of "weeks" (3.3 nonads per month)
 - The remaining 1 or 2 days at the end of the year are intercalary transition days before the new year

### Proposed epoch

The midnight closest to the northward equinox of the Human Era epoch of the [Holocene Calendar](https://en.wikipedia.org/wiki/Holocene_calendar), 10001 BC, maintaining a reference to the currently dominant [Anno Domini](https://en.wikipedia.org/wiki/Anno_Domini) (12020 HE = 2020 AD).

## Proposed notation

- The **numbering** of units must be fixed
  - Divisions of the year are 1-indexed (namely quarters, eighths/months and nonads)
  - Days of divisions containing intercalary days are 0-indexed (namely quarters and transitions)
    - Day 0 of a quarter is the quarter's intercalary day
  - Days of divisions containing only calendar days are 1-indexed (namely eighths/months and nonads)
  - Transition days do not belong to any of the year's divisions
- The **naming** of units may vary by language, locale or culture
- The **formatting** of dates should be standardized and the same for all

#### Example of date format ([ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) like)

  - **Eighth:** `eighth` (1-8) and `day-of-eighth` (1-45)
    - `[year]-[eighth]-[day-of-eighth]`
  - **Nonad:** `nonad` (1-40) and `day-of-nonad` (1-9)
    - `[year]-N[nonad]-[day-of-nonad]`
  - **Quarter:** `quarter` (1-4) or `quarter-letter` (A-D) and `day-of-quarter` (0-90)
    - `[year]-Q[quarter]-[day-of-quarter]`
    - `[year]-[quarter-letter]-[day-of-quarter]`
  - **Transition:** `day-of-transition` (0-1)
    - `[year]-X-[day-of-transition]`

The quarters may be named `A-D` similar to Asimov's [World Season Calendar][7] (`A-0`, `B-0`, `C-0`, `D-0`, `X-0`).

A better format would be one that is culturally neutral, only using numbers and punctuation.

## Accuracy

Observation-based calendars embrace the non-uniform motion of the Earth around the Sun, as well as the short-term perturbations. The future can never be predicted with absolute certainty, due to the dynamic nature of the universe. The only way to know with absolute certainty the length of the year is through observation.

Calendars based on the Jalali calendar are the most accurate in relation to the real solar year. Today's astronomical knowledge and computing power enable us to predict with very high precision the instant of the northward equinox. The exact instant can now be measured to an accuracy of better than 1 millisecond ([Heydari-Malayeri, 2004][1]).

## What it is not

#### This calendar does not attempt to:

- Incorporate the traditional 7-day week in its structure
- Incorporate the [lunar phases](https://en.wikipedia.org/wiki/Lunar_phase), as [lunisolar calendars](https://en.wikipedia.org/wiki/Lunisolar_calendar) are inherently complex and irregular
- Accurately follow the [astronomical seasons](https://en.wikipedia.org/wiki/Season#Astronomical), as their lengths change over time
- Align with the 12 constellations of the [zodiac](https://en.wikipedia.org/wiki/Zodiac), due to the (lunisolar) [precession of the ecliptic](https://en.wikipedia.org/wiki/Axial_precession)
- Introduce time scales or prescribe holidays — it's just a calendar

However, features like these may be applied just as they are applied to existing calendars. For example, the unbroken chain of 7-day weeks may be used just like in the Gregorian calendar, with weekdays retaining their traditional names and cultural/religious significance, if so is desired. As long as the calendar's underlying structure remains the same.

#### Related proposed calendars:

- Isaac Asimov's [World Season Calendar][7]
- Peter Meyer's [Liberalia Triday Calendar][8]
- Alexander Laik's [Calendar of the Rainbow][12]
- [The Dee-Cecil Calendar][11]
- [The World Calendar][13]
- [The Primavera Calendar][14]
- [Universal Celestial Calendar][9]
- [The Earth Epic Calendar][10]

---

#### Notes:

1. In particular the Jalali calendar reform led by the Persian mathematician, astronomer, philosopher and poet [Omar Khayyâm](https://en.wikipedia.org/wiki/Omar_Khayyam) in 1074-1079 AD
2. Both calendars had 5 "stolen days", possibly a reference to [the Egyptian myth of Nut and Ra](https://en.wikipedia.org/wiki/Nut_(goddess)#Myth_of_Nut_and_Ra)
3. Instead of Tehran, this calendar's point of reference effectively becomes [0°N 0°E](https://en.wikipedia.org/wiki/Null_Island) at sea level
4. Either the exact local instant, or local midnight as calculated from new year at the prime meridian
5. A [widespread misunderstanding][19] that must be avoided when implementing this calendar

#### References:

- [A concise review of the Iranian calendar][1] (Heydari-Malayeri, 2004)
- [The Liberalia Triday Calendar][8] (Meyer, 1999)
- [More Mathematical Astronomy Morsels][4] (Meeus, 2002)

#### Recommended links:

- [Calendar Reform][15] (McCarty)
- [Calendars New and Old][16] (Meyer)
  - [The Non-implemented 33-Year English Protestant Calendar][2] (Steel, 1999)
  - [How Britain got the Calendar Wrong][18] (Steel, 1999)
- [One Day Too Many][17] (Schlag)  
  <small><em>Doesn't mention the Persian calendar. This calendar would also solve all the [faults](http://www.schlag.name/calendarreform11.html) of the Gregorian calendar.</em></small>
- [The Persian calendar for 3000 years][5] (Borkowski, 1996)

[1]: http://aramis.obspm.fr/~heydari/divers/ir-cal-eng.html
[2]: https://www.hermetic.ch/cal_stud/dst01.htm
[3]: https://www.hermetic.ch/cal_stud/ltc/ltc.htm#advantages
[4]: https://www.willbell.com/math/moremorsels.HTM
[5]: http://www.astro.uni.torun.pl/~kb/Papers/EMP/PersianC-EMP.htm
[6]: https://www.hermetic.ch/cal_stud/dst02.htm
[7]: https://calendars.wikia.org/wiki/World_Season_Calendar
[8]: https://www.hermetic.ch/cal_stud/ltc/ltc.htm
[9]: https://www.universalcelestialcalendar.com/
[10]: https://earthepiccalendar.com/current-calendar/
[11]: https://www.hermetic.ch/cal_stud/gods_longitude.htm
[12]: https://calendars.wikia.org/wiki/Calendar_of_the_Rainbow
[13]: http://myweb.ecu.edu/mccartyr/world-calendar.html
[14]: http://bosonline.com/primavera/
[15]: http://myweb.ecu.edu/mccartyr/calendar-reform.html
[16]: https://www.hermetic.ch/cal_stud.htm
[17]: http://www.schlag.name/calendarreform00.htm
[18]: https://www.hermetic.ch/cal_stud/dst02.htm
[19]: https://hermetic.ch/cal_stud/cassidy/err_trop.htm
