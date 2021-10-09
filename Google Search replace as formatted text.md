# This sample Regex matches and returns a more formatted version from Google Calendar's Search Results.  

![Google Calendar Regex Replace]("https://github.com/RoyEHamlin/regex-Examples-and-Snippets/blob/main/images/GC - Results.PNG")

## Example: 
### Step 1: Search for event(s) using Google Calendar's search option.
![Google Calendar search](/images/GC - Search.PNG)

### Step 2: The following text is copied directly from Google Calendar.

```
9
NOV 2021, TUE
9 – 10:30am
Sample Text 1
10
NOV 2021, WED
10:15 – 11:30am
Sample Text 2
4 – 6pm
Sample Text 4
12
NOV 2021, FRI
6:30 – 8:30am
Sample Text 3
```

### Step 3: the following Regex snippet is used to match and group the date and time components.
```
^(\d{1,2})\n(OCT|NOV|DEC|JAN|FEB|MAR|APR|MAY|JUN|JUL|AUG|SEP)(\W20\d{2}), (\w{3})\n(\d{1,2})(\:\d\d)?\s\–\s(\d{1,2})(\:\d\d)?(am|pm)\n(\w.*)
```

### Step 4: The following Regex snippet is replaces the original text and formats the results.
```
$4 $2 $1,$3 from $5$6 to $7$8 $9 \- $10
```

And is replaced by
```
TUE NOV 9, 2021 from 9 to 10:30 am - Sample Text 1
WED NOV 10, 2021 from 10:15 to 11:30 am - Sample Text 2
4 – 6pm
Sample Text 4
FRI NOV 12, 2021 from 6:30 to 8:30 am - Sample Text 3
```

## Notes: 
* This snippet will NOT match multiple instances found on the same day.
* Source code with sample can be found here https://regex101.com/r/IZqZC2/1/
* The horizontal line between the start and end times is an "En dash" (&ndash;), not a hyphen (&#045;)
