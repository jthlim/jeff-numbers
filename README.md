# Enhanced number system for Plover

Compared to the standard number handling:

* `EU` reverses any stroke, and works with any number of digits
  - `130EU79` produces "97031"
* `DZ` will convert a number to hundreds of dollars, and works with multiple strokes
  - `1DZ` produces "$100"
  - `1/2DZ` produces "$1200"
* `Z` will always suffix "00"
  - `2Z` produces "200"
  - `2/3Z` produces "2300"
  - `23Z` produces "2300"
* `D` will always double the last digit
  - `1D` produces "11"
  - `12D` produces "122"
  - `123EUD` produces "3211"
* `R` converts a number to roman numerals. `*` for lower case.
  - `12R` produces "XII"
  - `19/29EUR` produces "MCMXCII" (1992 in roman numerals)
  - This will only work for numbers between 1 and 3999 inclusive.
* `KR-` or `-RB` will prefix the entire number with a dollar symbol
  - `23KR` produces "$23"
  - `1/12KR` produces "$112"
* `WR-` or `-RG` will suffix the entire number with a percent symbol
  - `23WR` produces "23%"
  - `1/12KR` produces "112%"
  - `1WRZ` produces "100%"
* `W` or `B` will add ordinal suffixes:
  - `1B` produces "1st"
  - `1BD` or `1/1B` produces "11th"
  - `2/1B` produces "21st"
* Clock timings are supported
  - `K-` or `-BG` will add the suffix ":00"
  - Using `K` combined with `B` and/or `G` give 15 minute increments:
    - `12KG` produces "12:15"
    - `12KB` produces "12:30"
    - `12KBG` produces "12:45"
* `G` will convert the number to words
  - `23` produces "twelve"
  - `20GZ` produces "two thousand"
  - `12/0Z/0GZ` produces "twelve million"

# Installation

1. In plover, first install plover-python-dictionary
2. Save jeff-numbers.py from this repository
3. Drag and drop the file into plover, and ensure it is listed above `main.json`

