# Calendar

A perennial solar calendar based on astronomical observations or calculations.

- Based on the [Iranian calendar](https://en.wikipedia.org/wiki/Solar_Hijri_calendar), which in turn is based on the [Jalali calendar](https://en.wikipedia.org/wiki/Jalali_calendar) of AD 1079
- Follows the real [northward equinox](https://en.wikipedia.org/wiki/March_equinox) year (not to be confused with the mean tropical year)

### Summary

Basically: **The Iranian calendar with a different meridian, different division of the year and a different epoch.**

- The year begins at the northward equinox at the prime meridian (UTC)
- 360 common days, reflecting a full circle
  - Plus 5-6 intercalary days
- 4 quarters, each having 91 days
  - 1 intercalary day
  - 90 common days
    - Divided into 2, for a total of 8 45-day "months" per year
    - Grouped 3 * 3, for a total of 40 9-day "weeks" per year
- The remaining 1-2 days at the end of the year are intercalary transition days
- Proposed epoch is the beginning of the human era (10 001 BC)

### Benefits

- Extremely accurate when based on observations (see [Accuracy](#accuracy))
- Perennial – dates and "weeks" are fixed to the northward equinox
- Structured, yet flexible enough to adapt to different cultures and needs
  - Civil (uniform, simple)
  - Agriculture (seasonal, follows natural cycles)
  - Business (evenly divided, flexible scheduling)
- Division of the year into 8 and grouping of days into 9 makes it easy to visualize and learn
- Grouping of days into 3 * 3 is a very [interesting and powerful idea](https://www.hermetic.ch/cal_stud/ltc/ltc.htm#advantages) by Peter Meyer

## Definition

#### New Year (intercalation system)

> The calendar year begins at the midnight closest to the instant of the northward equinox. Consequently, if the northward equinox falls before solar noon on a particular day, then that day is the first day of the year. If the northward equinox occurs after solar noon, the following day begins the calendar year.

- Solar noon may either be calculated for the prime meridian ([Meeus, 2002](https://www.willbell.com/math/moremorsels.HTM)) or observed locally with a [sundial](https://en.wikipedia.org/wiki/Sundial)
- Calculations should be based on the instant of the northward equinox at the prime meridian ([0°N 0°E](https://en.wikipedia.org/wiki/Null_Island))
- Local new year can then be easily calculated from this UTC instant using time zone offsets
- The exact local instant of the northward equinox may be announced and celebrated, similar to [Nowruz](https://en.wikipedia.org/wiki/Nowruz)

#### Units

- **year** (360 common days + 5 or 6 intercalary days)
- **quarter** (1/4 of a year's first 364 days)
- **octal** (1/8 of a year's 360 common days)
- **nonad** (9 days)
- **day** ([24 hours](https://en.wikipedia.org/wiki/Nychthemeron))

#### Structure

- The year has 360 common days and 5 (common year) or 6 (leap year) [intercalary](https://en.wikipedia.org/wiki/Intercalation_(timekeeping)) days
- The year is divided into 4 equal quarters, of 1 intercalary and 90 common days
  - The intercalary day is day 0 of the quarter and represents the equinox/solstice
- The year's 360 common days may also be divided
  - Proposed division: 8 octals ("months") and 40 nonads ("weeks")
    - 8 octals of 45 days, 2 octals per quarter
    - 40 nonads of 9 days, 10 nonads per quarter
      - Each nonad may be further divided into 3 trios of 3 days, enabling very flexible work/rest schedules
  - Traditional division: 12 "months"
    - 12 months of 30 days, 3 months per quarter
    - Drawback: A month can not fit a whole number of nonands (3.33 per month)
    - Drawback: Traditional month names can not be used, requiring 12 new names
 - The remaining 1 or 2 days at the end of the year are intercalary transition days

#### Epoch

The calendar's epoch may be the instant of the northward equinox of the [Holocene calendar](https://en.wikipedia.org/wiki/Holocene_calendar)'s epoch (10 001 BC), maintaining the reference to Anno Domini (HE 12020 = AD 2020). Alternatively, [Anno Domini](https://en.wikipedia.org/wiki/Anno_Domini) may be retained.

_Note: The years are not always in sync, as this calendar's new year occurs over 3 months after the Gregorian calendar's._

## Notation

- The _numbering_ of units are fixed
  - An intercalary quarter-day is day 0 of its quarter
  - An intercalary transition-day belongs to its year, not any of the year's divisions
- The _naming_ of units may vary by language, locale or culture
  - The names used here are only descriptive
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

Observation-based calendars embrace the non-uniform motion of the Earth around the Sun, as well as the short-term perturbations. The future can never be predicted with absolute certainty, due to the dynamic nature of the universe. The only way to know with _absolute certainty_ the instant of the northward equinox is through observation.

Still, calendars like this and the Iranian calendar are the most accurate in use today. The instant of the northward equinox is now measured to an accuracy of better than 1 millisecond ([Heydari-Malayeri, 2004](http://aramis.obspm.fr/~heydari/divers/ir-cal-eng.html)).

## What it's not

This calendar does not attempt to:

- Incorporate the traditional 7-day week
- Incorporate the [lunar phases](https://en.wikipedia.org/wiki/Lunar_phase), as [lunisolar calendars](https://en.wikipedia.org/wiki/Lunisolar_calendar) are inherently complex and irregular
- Accurately follow the [astronomical seasons](https://en.wikipedia.org/wiki/Season#Astronomical), as their lengths change over time
- Align with the 12 constellations of the [zodiac](https://en.wikipedia.org/wiki/Zodiac), due to the (lunisolar) [precession of the ecliptic](https://en.wikipedia.org/wiki/Axial_precession)
- Introduce time scales such as eras or ages – it's just a calendar

However, features like these may be applied just as they are applied to existing calendars. For example, the unbroken chain of 7-day weeks may be incorporated just as it is in the Gregorian calendar, with week days retaining their traditional names and cultural/religious significance. The calendar's structure should always remain the same though.

Related calendars:
- Isaac Asamov's [World Season Calendar](https://en.wikipedia.org/wiki/Isaac_Asimov#Calendar)
- Peter Meyer's [Liberalia Triday Calendar](https://www.hermetic.ch/cal_stud/ltc/ltc.htm)
- [Universal Celestial Calendar](https://www.universalcelestialcalendar.com/)
- [Earth Epic Calendar](https://earthepiccalendar.com/)

## Recommended reading

[A concise review of the Iranian calendar](http://aramis.obspm.fr/~heydari/divers/ir-cal-eng.html) (Heydari-Malayeri, 2004)
