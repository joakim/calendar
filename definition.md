# Definition

- A perennial solar calendar for Earth based on astronomical observations
- The calendar year begins at the northward equinox measured from the prime meridian
- 360 calendar days + 5 or 6 intercalary days
  - 4 quarters of 90 calendar days + 1 intercalary day
  - 8 months of 45 calendar days
  - 40 weeks of 9 calendar days
    - 3 × 3 days
  - 1 or 2 intercalary transition days at the end of the year
- Proposed epoch is the beginning of the human era (10001 BC)

### New Year

> The calendar year begins at the midnight closest to the instant of the northward equinox measured from the prime meridian. Consequently, if the northward equinox falls _before_ solar noon on a particular day, then that day is the first day of the year. If the northward equinox occurs _after_ solar noon, the following day begins the calendar year.

- The instant should be based on calculations for the prime meridian <sup>[1](#notes)</sup>
  - The instant may also be observed locally, even with a [sundial](https://en.wikipedia.org/wiki/Sundial)
  - Local new year may be calculated from this instant using a time offset (for example [Universal Time](https://en.wikipedia.org/wiki/Universal_Time))
  - The _local_ new year should be celebrated, not that of the prime meridian <sup>[2](#notes)</sup>
- Leap years follow the 33-year cycle inherited from the Persian calendar ([Heydari-Malayeri, 2004](http://aramis.obspm.fr/~heydari/divers/ir-cal-eng.html))
  - Calculations should use the _true northward equinox year_, not to be confused with the _mean tropical year_ <sup>[3](#notes)</sup>

### Units

- **year:** 360 calendar days + 5 (or 6) intercalary days
- **quarter:** 1/4 of a year's 360 calendar days + 1 intercalary day
- **octant:** 1/8 of a year's 360 calendar days
- **nonad:** 9 calendar days
- **triad:** 3 calendar days
- **day:** 1 [nychthemeron](https://en.wikipedia.org/wiki/Nychthemeron)
- **transition:** a period of 1 (or 2) intercalary days

The names "octant", "nonad", "triad" and "transition" are descriptive only, better names may be chosen.

### Structure

- The year has 360 calendar days and 5 (common year) or 6 (leap year) intercalary days
- The year is divided into 4 equal quarters, each having 91 days
  - 1 intercalary day that represents the equinox/solstice
  - 90 calendar days
- The year's 360 calendar days may be divided as follows
  - Proposed division: 8 octants ("months") and 40 nonads ("weeks")
    - 8 octants of 45 calendar days (2 octants per quarter)
    - 40 nonads of 9 calendar days (10 nonads per quarter, 5 nonads per octant)
      - Each nonad may be further divided into 3 triads of 3 calendar days
  - Traditional division: 12 months
    - 12 months of 30 calendar days (3 months per quarter)
    - Drawback: A month can not fit a whole number of nonads (3.3 nonads per month)
 - The remaining 1 or 2 days at the end of the year are intercalary transition days before the new year

### Proposed epoch

The midnight closest to the northward equinox of the Human Era epoch of the [Holocene Calendar](https://en.wikipedia.org/wiki/Holocene_calendar), 10001 BC, maintaining a reference to the currently dominant [Anno Domini](https://en.wikipedia.org/wiki/Anno_Domini) (12020 HE = 2020 AD).

### Proposed notation

- The **numbering** of units must be universal
  - Divisions of the year are 1-indexed (namely quarters, octants/months and nonads)
  - Days of quarters and the transition period are 0-indexed
    - Day 0 of a quarter is the quarter's intercalary day
  - Days of other divisions of the year are 1-indexed (namely octants/months and nonads)
- The **formatting** of dates should be universal
- The **naming** of units may vary by language, locale or culture

#### One example of a format ([ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) like)

  - **Octant:** `octant` (1-8) and `day-of-octant` (1-45)
    - `[year]-[octant]-[day-of-octant]`
  - **Nonad:** `nonad` (1-40) and `day-of-nonad` (1-9)
    - `[year]-N[nonad]-[day-of-nonad]`
  - **Quarter:** `quarter` (A-D) and `day-of-quarter` (0-90)
    - `[year]-[quarter]-[day-of-quarter]`
  - **Fiscal quarter:** `fiscal-quarter` (1-4) and `day-of-quarter` (1-90)
    - `[year]-Q[fiscal-quarter]-[day-of-quarter]`
  - **Transition:** `day-of-transition` (0-1)
    - `[year]-X-[day-of-transition]`

The quarters are named `A-D` as in Asimov's [World Season Calendar](https://calendars.wikia.org/wiki/World_Season_Calendar) (`A-0`, `B-0`, `C-0`, `D-0`, and `X-0`).

---

#### Notes:

1. Instead of Tehran, this calendar's point of reference effectively becomes [0°N 0°E](https://en.wikipedia.org/wiki/Null_Island) at sea level
2. Could be the exact local instant of the northward equinox or local midnight as calculated from the prime meridian
3. A [widespread misunderstanding](https://hermetic.ch/cal_stud/cassidy/err_trop.htm) that must be avoided when implementing this calendar
