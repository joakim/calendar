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
- 4 quarters, each having 91 days
  - 1 intercalary day
  - 90 common days
    - Divided into 2, for a total of 8 45-day "months" per year
    - Grouped 3 * 3, for a total of 40 9-day "weeks" per year
- The remaining 1 or 2 days at the end of the year are intercalary transition days
- Proposed epoch is the beginning of the human era (10 001 BC)

### Benefits

- Forever accurate when based on astronomical observations (see [Accuracy](#accuracy))
- Perennial – dates, "weeks" and seasons are always in relation to the northward equinox
- Structured – yet flexible enough to adapt to different cultures and needs
  - Civil (simple, uniform, predictable)
  - Agriculture (seasonal, follows natural cycles)
  - Business (evenly divided, flexible scheduling)
- Division of the year into 8 and grouping of days into 9 makes it easy to learn and visualize
- Grouping of days into 3 * 3 is a very [interesting and powerful idea][3] by Peter Meyer

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
- **octal** (1/8 of a year's 360 common days)
- **nonad** (9 days)
- **trio** (3 days)
- **day** ([24 hours](https://en.wikipedia.org/wiki/Nychthemeron))

The names "octal", "nonad" and "trio" are descriptive only.

### Structure

- The year has 360 common days and 5 (common year) or 6 (leap year) intercalary days
- The year is divided into 4 equal quarters, each having 91 days
  - 1 intercalary day that represents the equinox/solstice
  - 90 common days
- The year's 360 common days may be divided as follows
  - Proposed division: 8 octals ("months") and 40 nonads ("weeks")
    - 8 octals of 45 days, 2 octals per quarter
    - 40 nonads of 9 days, 10 nonads per quarter
      - Each nonad may be further divided into 3 trios of 3 days
  - Traditional division: 12 "months"
    - 12 months of 30 days, 3 months per quarter
    - Drawback: A month can not fit a whole number of nonands (3.33 per month)
    - Drawback: Traditional month names can not be used, requiring 12 new names
 - The remaining 1 or 2 days at the end of the year are intercalary transition days before the next new year

### Epoch

The calendar's epoch may be the instant of the northward equinox of the [Holocene calendar](https://en.wikipedia.org/wiki/Holocene_calendar)'s epoch (10 001 BC), maintaining the reference to Anno Domini (HE 12020 = AD 2020). Alternatively, [Anno Domini](https://en.wikipedia.org/wiki/Anno_Domini) may be retained.

## Proposed notation

- The _numbering_ of units must be fixed
  - Divisions of the year should be 1-indexed (namely quarters, octals/months and nonads)
  - Days of divisions containing intercalary days are 0-indexed (namely quarters and transition days)
  - Days of divisions of common days are 1-indexed (namely octals/months and nonads)
  - Transition days belong to the enclosing year and none of its divisions
- The _naming_ of units may vary by language, locale or culture
- The _formatting_ of dates should be standardized and the same for all

#### Proposed date formats ([ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) like)

  - Day-of-octal (1-45) – Recommended for common/civil use
    - `[year]-[octal]-[octal-day]`
  - Day-of-nonad (1-9) – Recommended for scheduling
    - `[year]-N[nonad]-[nonad-day]`
  - Day-of-quarter (0-90) – Useful in agriculture and business
    - `[year]-Q[quarter]-[quarter-day]`
  - Day-of-transition (0-1)
    - `[year]-X-[transition-day]`
  - Day-of-month (1-30) – Traditional 12 month division of the year
    - `[year]-[month]/12-[month-day]`

Alternatively, the quarters may be named `A-D` as in Asamov's [World Season Calendar][7] (`A-0`, `B-0`, `C-0`, `D-0`, `X-0`).

## Accuracy

Observation-based calendars embrace the non-uniform motion of the Earth around the Sun, as well as the short-term perturbations. The future can never be predicted with absolute certainty, due to the dynamic nature of the universe. The only way to know with absolute certainty the length of the year is through observation.

Still, today's calculations are accurate enough to be reliable for millennia ([Borkowski, 1996][5]). Calendars based on the Jalali calendar are the most accurate in use today, the instant of the northward equinox can now be measured to an accuracy of better than 1 millisecond ([Heydari-Malayeri, 2004][1]).

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
- [Universal Celestial Calendar][9]
- [Earth Epic Calendar][10]
- [The Dee-Cecil Calendar][11]

---

#### Notes:

1. Calendar reform led by the Persian mathematician, astronomer, philosopher, and poet [Omar Khayyâm](https://en.wikipedia.org/wiki/Omar_Khayyam)
2. Both calendars had 5 "stolen days", possibly a reference to [the Egyptian myth of Nut and Ra](https://en.wikipedia.org/wiki/Nut_(goddess)#Myth_of_Nut_and_Ra)?
3. Instead of Tehran, this calendar's reference point effectively becomes 0°N 0°E, popularly known as [Null Island](https://en.wikipedia.org/wiki/Null_Island)
4. Either the exact local instant, or as calculated from the exact instant at the prime meridian

#### References:

- [A concise review of the Iranian calendar][1] (Heydari-Malayeri, 2004)
- [The Liberalia Triday Calendar][3] (Meyer, 1999)
- [More Mathematical Astronomy Morsels][4] (Meeus, 2002)
- [The Persian calendar for 3000 years][5] (Borkowski, 1996)

#### Recommended reading:

- [The Non-implemented 33-Year English Protestant Calendar][2] (Steel, 1999)

[1]: http://aramis.obspm.fr/~heydari/divers/ir-cal-eng.html
[2]: https://www.hermetic.ch/cal_stud/dst01.htm
[3]: https://www.hermetic.ch/cal_stud/ltc/ltc.htm#advantages
[4]: https://www.willbell.com/math/moremorsels.HTM
[5]: http://www.astro.uni.torun.pl/~kb/Papers/EMP/PersianC-EMP.htm
[6]: https://www.hermetic.ch/cal_stud/dst02.htm
[7]: https://en.wikipedia.org/wiki/Isaac_Asimov#Calendar
[8]: https://www.hermetic.ch/cal_stud/ltc/ltc.htm
[9]: https://www.universalcelestialcalendar.com/
[10]: https://earthepiccalendar.com/
[11]: https://www.hermetic.ch/cal_stud/dee-cecil-calendar.html
