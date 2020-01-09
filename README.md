# Calendar

A [perennial](https://en.wikipedia.org/wiki/Perennial_calendar) [solar calendar](https://en.wikipedia.org/wiki/Solar_calendar) based on astronomical calculations or observations.

- Based on the Persian [Solar Hijri calendar](https://en.wikipedia.org/wiki/Solar_Hijri_calendar), in turn based on the [Jalali calendar](https://en.wikipedia.org/wiki/Jalali_calendar) of AD 1079 <sup>([note 1](#notes))</sup>
  - With roots in the [Zoroastrian calendar](https://en.wikipedia.org/wiki/Zoroastrian_calendar) and possibly the [Egyptian calendar](https://en.wikipedia.org/wiki/Egyptian_calendar) <sup>([note 2](#notes))</sup>
- Follows the real [northward equinox](https://en.wikipedia.org/wiki/March_equinox) year, not to be confused with the mean tropical year

### Summary

**The Persian calendar with a different meridian, different division of the year and a different epoch.**

- The year begins at the northward equinox (March) at the prime meridian (UTC)
- 360 common days, reflecting a full circle
  - Plus 5 or 6 intercalary (epogamenal) days
- Divided into 4 quarters, each of 91 days
  - 1 intercalary day
  - 90 common days
    - Divided into 2, for a total of 8 * 45-day "months" per year
    - Grouped 3 * 3, for a total of 40 * 9-day "weeks" per year
- The remaining 1 or 2 days at the end of the year are intercalary transition days
- Proposed epoch is the beginning of the human era (10 001 BC)

### Advantages

- **Accurate** – _in perpetuum_ when based on astronomical observations (see [Accuracy](#accuracy))
- **Simple** – division of the year into 4 and 8 equal parts makes it easy to learn and visualize
- **Dynamic** – grouping of days into 3 * 3 is a powerful concept (based on Peter Meyer's [triday][3])
- **Perennial** – dates and seasons are fixed in relation to the northward equinox
- **Structured** – yet flexible enough to adapt to different needs and cultures
  - Civil (simple, predictable)
  - Agriculture (seasonal, follows natural cycles)
  - Business (evenly divided, flexible scheduling)
- **Neutral**
  - Not tied to any cultures or locations, except for those of the current scientific paradigm
  - While scientifically grounded, it does not oppose combination with cultural or religious concepts

### Disadvantages

- Unfamiliar "months", "weeks", "new year" and epoch
- No simple rule for leap years, a trade-off with accuracy
- Just a calendar proposed by someone named Joakim (who is not the pope)

## Definition

### New Year

> The calendar year begins at the midnight closest to the instant of the northward equinox. Consequently, if the northward equinox falls before solar noon on a particular day, then that day is the first day of the year. If the northward equinox occurs after solar noon, the following day begins the calendar year.

- This may be calculated for the prime meridian ([Meeus, 2002][4]) or observed locally (even with a [sundial](https://en.wikipedia.org/wiki/Sundial))
  - Calculations should be based on the instant of the northward equinox at the prime meridian <sup>([note 3](#notes))</sup>
  - Local new year is then easily calculated from this instant using UTC time zone offsets
- The local instant of the northward equinox should be celebrated as the start of the new year <sup>([note 4](#notes))</sup>
- Intercalation (leap years) follows the same 33 year cycle as the Persian calendar ([Heydari-Malayeri, 2004][1])

### Units

- **year** (360 common days + 5 or 6 [intercalary](https://en.wikipedia.org/wiki/Intercalation_(timekeeping)#Solar_calendars) days)
- **quarter** (1/4 of a year's first 364 days)
- **eighth** (1/8 of a year's 360 common days)
- **nonad** (9 days)
- **triad** (3 days)
- **day** ([24 hours](https://en.wikipedia.org/wiki/Nychthemeron))

The names "eighth", "nonad" and "triad" are descriptive only.

### Structure

- The year has 360 common days and 5 (common year) or 6 (leap year) intercalary days
- The year is divided into 4 equal quarters, each having 91 days
  - 1 intercalary day that represents the equinox/solstice
  - 90 common days
- The year's 360 common days may be divided as follows
  - Proposed division: 8 eighths ("[months](https://en.wikipedia.org/wiki/Month)") and 40 nonads ("[weeks](https://en.wikipedia.org/wiki/Week)")
    - 8 eighths of 45 days, 2 eighths per quarter
    - 40 nonads of 9 days, 10 nonads per quarter
      - Each nonad may be further divided into 3 triads of 3 days
  - Traditional division: 12 "months"
    - 12 months of 30 days, 3 months per quarter
    - Drawback: A month can not fit a whole number of nonads (3.3 per month)
    - Drawback: Traditional month names can not be used, requiring 12 new names
 - The remaining 1 or 2 days at the end of the year are intercalary transition days before the next new year

### Proposed epoch

The calendar's epoch may be the instant of the northward equinox of the [Holocene Calendar](https://en.wikipedia.org/wiki/Holocene_calendar)'s epoch (10 001 BC), maintaining the reference to Anno Domini (HE 12020 = AD 2020). Alternatively, [Anno Domini](https://en.wikipedia.org/wiki/Anno_Domini) may be retained.

## Proposed notation

- The **numbering** of units must be fixed
  - Divisions of the year should be 1-indexed (namely quarters, eighths/months and nonads)
  - Days of divisions containing intercalary days are 0-indexed (namely quarters and transition days)
  - Days of divisions of common days are 1-indexed (namely eighths/months and nonads)
  - Transition days belong to the enclosing year and none of its divisions
- The **naming** of units may vary by language, locale or culture
- The **formatting** of dates should be standardized and the same for all

#### Example of date format ([ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) like)

  - Eight: `eight` (1-8) and `day-of-eighth` (1-45)
    - `[year]-[eighth]-[day-of-eighth]`
  - Nonad: `nonad` (1-40) and `day-of-nonad` (1-9)
    - `[year]-N[nonad]-[day-of-nonad]`
  - Quarter: `quarter` (1-4) or `quarter-letter` (A-D) and `day-of-quarter` (0-90)
    - `[year]-Q[quarter]-[day-of-quarter]`
    - `[year]-[quarter-letter]-[day-of-quarter]`
  - Transition: `day-of-transition` (0-1)
    - `[year]-X-[day-of-transition]`

The quarters may be named `A-D` similar to Asamov's [World Season Calendar][7] (`A-0`, `B-0`, `C-0`, `D-0`, `X-0`).

A better format would be culturally neutral and only use numbers and punctuation.

## Accuracy

Observation-based calendars embrace the non-uniform motion of the Earth around the Sun, as well as the short-term perturbations. The future can never be predicted with absolute certainty, due to the dynamic nature of the universe. The only way to know with absolute certainty the length of the year is through observation.

Calendars based on the Jalali calendar are the most accurate in relation to the real solar year. Today's astronomical knowledge and computing power enable us to predict with very high precision the instant of the northward equinox. The exact instant can now be measured to an accuracy of better than 1 millisecond ([Heydari-Malayeri, 2004][1]).

## What it is not

#### This calendar does not attempt to:

- Incorporate the traditional 7-day week in its structure
- Incorporate the [lunar phases](https://en.wikipedia.org/wiki/Lunar_phase), as [lunisolar calendars](https://en.wikipedia.org/wiki/Lunisolar_calendar) are inherently complex and irregular
- Accurately follow the [astronomical seasons](https://en.wikipedia.org/wiki/Season#Astronomical), as their lengths change over time
- Align with the 12 constellations of the [zodiac](https://en.wikipedia.org/wiki/Zodiac), due to the (lunisolar) [precession of the ecliptic](https://en.wikipedia.org/wiki/Axial_precession)
- Introduce time scales or prescribe holidays – it's just a calendar

However, features like these may be applied just as they are applied to existing calendars. For example, the unbroken chain of 7-day weeks may be incorporated just as it is in the Gregorian calendar, with week days retaining their traditional names and cultural/religious significance. As long as the calendar's underlying structure remains the same.

#### Related proposed calendars:

- Isaac Asamov's [World Season Calendar][7]
- Peter Meyer's [Liberalia Triday Calendar][8]
- Alexander Laik's [Calendar of the Rainbow][12]
- [The Dee-Cecil Calendar][11]
- [The World Calendar][13]
- [The Primavera Calendar][14]
- [Universal Celestial Calendar][9]
- [The Earth Epic Calendar][10]

---

#### Notes:

1. Calendar reform led by the Persian mathematician, astronomer, philosopher, and poet [Omar Khayyâm](https://en.wikipedia.org/wiki/Omar_Khayyam)
2. Both calendars had 5 "stolen days", possibly a reference to [the Egyptian myth of Nut and Ra](https://en.wikipedia.org/wiki/Nut_(goddess)#Myth_of_Nut_and_Ra)
3. Instead of Tehran, this calendar's reference point effectively becomes 0°N 0°E, popularly known as [Null Island](https://en.wikipedia.org/wiki/Null_Island)
4. Either the exact local instant, or as calculated from the exact instant at the prime meridian

#### References:

- [A concise review of the Iranian calendar][1] (Heydari-Malayeri, 2004)
- [The Liberalia Triday Calendar][3] (Meyer, 1999)
- [More Mathematical Astronomy Morsels][4] (Meeus, 2002)

#### Recommended:

- [Calendar Reform][15] (McCarty)
- [The Non-implemented 33-Year English Protestant Calendar][2] (Steel, 1999)
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
