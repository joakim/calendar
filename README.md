# Calendar

A [perennial](https://en.wikipedia.org/wiki/Perennial_calendar) [solar calendar](https://en.wikipedia.org/wiki/Solar_calendar) based on astronomical observations or calculations.

- Based on the [Iranian calendar](https://en.wikipedia.org/wiki/Solar_Hijri_calendar), which in turn is based on the [Jalali calendar](https://en.wikipedia.org/wiki/Jalali_calendar) of AD 1079 <sup>[[1](#notes)]</sup>
  - With roots in the [Zoroastrian calendar](https://en.wikipedia.org/wiki/Zoroastrian_calendar) and possibly the [Egyptian calendar](https://en.wikipedia.org/wiki/Egyptian_calendar) <sup>[[2](#notes)]</sup>
- Follows the real [northward equinox](https://en.wikipedia.org/wiki/March_equinox) year (not to be confused with the mean tropical year)

### Summary

**The Iranian calendar with a different meridian, different division of the year and a different epoch.**

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

- Extremely accurate when based on observations (see [Accuracy](#accuracy))
- Perennial – dates, "weeks" and seasons are always in relation to the northward equinox
- Structured, yet flexible enough to adapt to different cultures and needs
  - Civil (uniform, simple)
  - Agriculture (seasonal, follows natural cycles)
  - Business (evenly divided, flexible scheduling)
- Division of the year into 8 and grouping of days into 9 makes it easy to learn and visualize
- Grouping of days into 3 * 3 is a very [interesting and powerful idea][3] by Peter Meyer

## Definition

### New Year

> The calendar year begins at the midnight closest to the instant of the northward equinox. Consequently, if the northward equinox falls before solar noon on a particular day, then that day is the first day of the year. If the northward equinox occurs after solar noon, the following day begins the calendar year.

- This may be calculated for the prime meridian ([Meeus, 2002][4]) or observed locally (even with a [sundial](https://en.wikipedia.org/wiki/Sundial))
  - Calculations should be based on the instant of the northward equinox at the prime meridian <sup>[[3](#notes)]</sup>
  - Local new year is then easily calculated from this instant using UTC time zone offsets
- The exact local instant of the northward equinox may be announced and celebrated <sup>[[4](#notes)]</sup>
- Intercalation (leap years) follows the same rules as the Iranian calendar ([Heydari-Malayeri, 2004][1])

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
  - 1 intercalary day that represents the equinox/solstice (day 0 of the quarter)
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

The calendar's epoch may be the instant of the northward equinox of the [Holocene calendar](https://en.wikipedia.org/wiki/Holocene_calendar)'s epoch (10 001 BC), maintaining the reference to Anno Domini (HE 12020 = AD 2020). Alternatively, [Anno Domini](https://en.wikipedia.org/wiki/Anno_Domini) may be retained. <sup>[[5](#notes)]

## Notation

- The _numbering_ of units are fixed
  - An intercalary quarter-day is day 0 of its quarter
  - An intercalary transition-day belongs to its year, not any of the year's divisions
- The _naming_ of units may vary by language, locale or culture
- The _formatting_ of dates should be standardized and the same for everyone
  - Day-of-octal (1-45) – Recommended for civil use
    - `[year]-[octal]-[octal-day]`
  - Day-of-nonad (1-9) – Recommended for scheduling
    - `[year]-N[nonad]-[nonad-day]`
  - Day-of-quarter (0-90) – May be used in agriculture or business
    - `[year]-Q[quarter]-[quarter-day]`
  - Day-of-transition (1-2)
    - `[year]-X[transition-day]`
  - Day-of-year (1-365/366) – Most useful for calculations
    - `[year]-D[year-day]`
  - Common-day-of-year (1-360) – Alternative to the above, skips intercalary days
    - `[year]-C[common-day]`
  - Day-of-month (1-30) – Traditional 12 month division of the year
    - `[year]/12-[month]-[month-day]`

## Accuracy

Observation-based calendars embrace the non-uniform motion of the Earth around the Sun, as well as the short-term perturbations. The future can never be predicted with absolute certainty, due to the dynamic nature of the universe. The only way to know with absolute certainty the length of the year is through observation.

Calendars like this and the Iranian calendar are the most accurate in use today. The instant of the northward equinox can now be measured to an accuracy of better than 1 millisecond ([Heydari-Malayeri, 2004][1]).

## Reasoning

#### Why base it on the Iranian calendar?

It is the most accurate calendar designed. In my opinion, its foundation is also the most elegant. Basing the calendar on astronomical observations is not only scientifically sound, but on some level even poetic. Omar Khayyâm was after all both an astronomer and a poet. The year being reborn in spring is an idea that resonates strongly with people in the northern hemisphere (where approximately 90% of us live). <sup>[[4](#notes)]</sup>

#### Why 8 "months" and 9-day "weeks"?

To answer this, one should first answer the question "Why 12 months and 7-day weeks?", the common division of the year in many calendars. The first calendars were lunar calendars, tracking the easily observed phases of the Moon. A lunar phase is roughly seven days (7.38 on average), a full cycle just under 30 days (29.53 on average). Over time, our attention turned to the stars, and our understanding of astronomy grew. Eventually, agriculture and trade brought the need for a calendar that tracked the seasons. The Egyptian calendar was the first to abandon the lunar cycle and instead focus on Earth's cycle around the Sun. Still, it divided the solar year into 12 months of 30 days – maybe to ease the transition from the lunar calendar it replaced? The 7-day week may likewise be explained by the lunar phases, or maybe by the five visible planets in the night sky plus the Sun and the Moon?

Being strictly a solar calendar, this calendar does not attempt to unify the Moon's cycle around Earth with Earth's cycle around the Sun. By not being tied to such constraints, it is free to devise new divisions of the year, attaining benefits not found in traditional calendars. Most importantly, 8 "months" enables the 9-day "week" of 3 * 3 days, a very flexible and powerful construct.

## What it's not

#### This calendar does not attempt to:

- Incorporate the traditional 7-day week in its structure
- Incorporate the [lunar phases](https://en.wikipedia.org/wiki/Lunar_phase), as [lunisolar calendars](https://en.wikipedia.org/wiki/Lunisolar_calendar) are inherently complex and irregular
- Accurately follow the [astronomical seasons](https://en.wikipedia.org/wiki/Season#Astronomical), as their lengths change over time
- Align with the 12 constellations of the [zodiac](https://en.wikipedia.org/wiki/Zodiac), due to the (lunisolar) [precession of the ecliptic](https://en.wikipedia.org/wiki/Axial_precession)
- Introduce time scales or prescribe holidays – it's just a calendar

However, features like these may be applied just as they are applied to existing calendars. For example, the unbroken chain of 7-day weeks may be incorporated just as it is in the Gregorian calendar, with week days retaining their traditional names and cultural/religious significance. As long as the calendar's underlying structure remains the same.

#### Related proposed calendars:

- Isaac Asamov's [World Season Calendar](https://en.wikipedia.org/wiki/Isaac_Asimov#Calendar)
- Peter Meyer's [Liberalia Triday Calendar](https://www.hermetic.ch/cal_stud/ltc/ltc.htm)
- [Universal Celestial Calendar](https://www.universalcelestialcalendar.com/)
- [Earth Epic Calendar](https://earthepiccalendar.com/)

---

#### References:

- [A concise review of the Iranian calendar][1] (Heydari-Malayeri, 2004)
- [The Liberalia Triday Calendar][3] (Meyer, 1999)
- [More Mathematical Astronomy Morsels][4] (Meeus, 2002)

#### Recommended reading:

- [The Non-implemented 33-Year English Protestant Calendar][2] (Steel, 1999)
- [The Persian calendar for 3000 years][5] (Borkowski, 1996)

#### Notes:

1. Calendar reform led by the Persian mathematician, astronomer, philosopher, and poet [Omar Khayyâm](https://en.wikipedia.org/wiki/Omar_Khayyam)
2. Both calendars had 5 "stolen days", possibly a reference to [the Egyptian myth of Nut and Ra](https://en.wikipedia.org/wiki/Nut_(goddess)#Myth_of_Nut_and_Ra)?
3. Instead of Tehran, this calendar's reference point effectively becomes [Null Island](https://en.wikipedia.org/wiki/Null_Island)
4. Many cultures celebrate the return of the sun with fire ([Nowruz](https://en.wikipedia.org/wiki/Nowruz), [Hıdırellez](https://en.wikipedia.org/wiki/H%C4%B1d%C4%B1rellez), [Falles](https://en.wikipedia.org/wiki/Falles)) – other spring or Easter rituals also involve bonfires ([Walpurgis Night](https://en.wikipedia.org/wiki/Walpurgis_Night), [Burning of Judas](https://en.wikipedia.org/wiki/Burning_of_Judas), [Beltane](https://en.wikipedia.org/wiki/Beltane), [Đurđevdan](https://en.wikipedia.org/wiki/%C4%90ur%C4%91evdan)), often with roots in pre-Christian traditions symbolizing rebirth or fertility
5. The year numbers of this and the Gregorian calendar are not always in sync, as this calendar's new year occurs in March of the Gregorian calendar

[1]: http://aramis.obspm.fr/~heydari/divers/ir-cal-eng.html
[2]: https://www.hermetic.ch/cal_stud/dst01.htm
[3]: https://www.hermetic.ch/cal_stud/ltc/ltc.htm#advantages
[4]: https://www.willbell.com/math/moremorsels.HTM
[5]: http://www.astro.uni.torun.pl/~kb/Papers/EMP/PersianC-EMP.htm
