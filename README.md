# datetimeconvention

<b> Air Sensors Workgrou: Date/Time Convention</b>

<b>Measurement Time Interval</b>

We suggest picking one of the following two formats to specify the measurement time interval, the first option being the simplest. 

1)	Start date/time and end date/time separated by a forward slash (/), such as:

<blockquote>"2007-03-01T13:00:00Z/2008-05-11T15:30:00Z" </blockquote>
   
<blockquote>“2012-03-01T13:00:00-08:00/2012-03-01T14:30:00-08:00”</blockquote>

2)	Start date/time and duration separated by a forward slash (/), such as:

<blockquote>"2007-03-01T13:00:00Z/P1Y2M10DT2H30M"</blockquote>
   
<blockquote>“2012-03-01T13:00:00-08:00/PT1H30M”</blockquote>
    
Date/time and duration formats are specified according to the ISO 8601 standards described below.

<b>Date/Time Format</b>

Four different date/time formats are supported, including:

<blockquote> 1)	YYYY-MM-DDT[hh][mm][ss]TZD </blockquote>

<blockquote> 2)	YYYYMMDDT[hh][mm][ss]TZD </blockquote>

<blockquote> 3)	YYYY-MM-DDT[hh]:[mm]:[ss]TZD </blockquote>

<blockquote> 4)	YYYYMMDDT[hh]:[mm]:[ss]TZD </blockquote>

For the date, YYYY represents the four-digit year, MM is the two-digit month, and DD is the two-digit day. For the time, hh is the two-digit hour, mm is the two-digit minute, and ss is the two-digit second.

In all four formats, the date and time components are separated by the letter “T,” and all formats must include the time zone. The following abbreviations are used to specify date/time components in these formats. Note: ISO supports fractions, but we recommend using fractions in the seconds field only.

<b>Component	Definition	Range	Example</b>

<table style="width:100%">
<tr> 
<td><b>Component</b></td>
<td><b>Definition</b></td>
<td><b>Range</b></td>
<td><b>Example</b></td>
<tr>
<td>YYYY</td>
<td>four-digit year</td>
<td> </td>
<td> </td>
<tr>
<td>MM</td>
<td>two-digit month</td>
<td>01 through 12</td> 
<td>01 = January; 12 = December</td>
<tr>
<td>DD</td>
<td>01 through 31</td>
<td>two-digit day of month</td>
<td>01 = first day of the month; 15 = 15th day of the month</td>
<tr>
<td>hh</td>
<td>two-digit hour</td>
<td>00 though 23</td> 
<td>00 = 0:00am (midnight); 12 = 12:00pm (noon); 13 = 1:00pm; am/pm NOT allowed</td>
<tr>
<td>mm</td>
<td>two-digit minute</td> 
<td>00 through 59</td>
<td> </td>
<tr>
<td>ss</td>
<td>two-digit second</td>
<td>00 through 59</td> 
<td> </td>
<tr>
<td>TZD</td>
<td>Time Zone Designator</td>
<td>+hh:mm or –hh:mm; +hh or –hh; +hhmm or –hhmm; or Z</td>
<td>+ indicates a time zone that is ahead of UTC; –indicates a time zone that is behind UTC; Z indicates UTC</td>

</table>

UTC = Coordinated Universal Time

Z = Zulu Time (same as UTC) 

<b>Duration Format</b>

If you are not reporting on start and end time, durations are an essential component of time intervals and define the amount of intervening time in a time interval. 
Durations can be represented by the format P[n]Y[n]M[n]DT[n]H[n]M[n]S or P[n]W. In these representations, the [n] is replaced by the value for each of the date and time elements that follow the [n]; for example, 8Y stands for eight years. Leading zeros are optional. The capital letters P, Y, M, W, D, T, H, M, and S are designators the date and time elements and are not replaced. Only the P designator is required for all duration representations; the T designator is required if the duration includes any of the time elements.

<b>Component	Definition	Examples</b>

<table style="width:100%">
<tr> 
<td><b>Component</b></td>
<td><b>Definition</b></td>
<td><b>Example</b></td>
<tr>
<td>P</td>
<td>Duration designator (for "Period") placed at the start of the duration representation</td> 
<td>Delimiter; signals that the string of numbers and letters that follow indicate duration</td> 
<tr>
<td>Y</td>
<td>Year designator. Comes after the value for the number of years</td>
<td>12 = 12 years</td> 
<tr>
<td>M<t/d>
<td>Month designator. Comes after the value for the number of months</td>
<td>13 = 13 months; 08 = 8 months</td> 
<tr>
<td>W</td>
<td>Week designator. Comes after the value for the number of weeks</td>
<td>55 = 55 weeks; 30 = 30 weeks</td> 
<tr>
<td>D</td>
<td>Day designator. Comes after the value for the number of days</td>
<td>320 = 320 days</td>
<tr>
<td>T</td>
<td>Time designator. Separates the date information from the time information</td> 
<td>Signals that the following string of numbers and letters indicate time</td> 
<tr>
<td>H</td>
<td>Hour designator. Comes after the value for the number of hours</td>
<td>23 = 23 hours</td>
<tr>
<td>M</td>
<td>Minute designator. Comes after the value for the number of minutes</td>
<td> 58 = 58 minutes</td>
<tr>
<td>S</td>
<td>Second designator. Comes after the value for the number of seconds</td>
<td>40.6 = 40.6 seconds</td>
</table>

For example, "P3Y6M4DT12H30M5S" represents a duration of "three years, six months, four days, twelve hours, thirty minutes, and five seconds".
 
<b>Examples</b> 

Examples 1-8 show timestamps for various durations starting on April 5, 2007, at 2 pm (1400 hours).

1.	Start time / End time (1 hour duration)

    2007-04-05T14:00-08:00/2007-04-05T15:00-08:00
    
    In this example, the start date/time and end date/time are provided to represent a one-hour measurement interval on April 5, 2007,     from 2 pm (1400) to 3 pm (1500) in the Pacific Time Zone (8 hours behind the UTC).

2.	Start time / Duration  in UTC (2 week duration) 

    2007-04-05T14:00:00+00:00/P2W
    
    In this example, the time is represented as UTC and the duration expresses 2 weeks.

3.	Start time / Duration in UTC (2 hour)

    2007-04-05T14:00:00+00:00/PT2H 
    
    In this example, the time is represented as UTC and the duration expresses 2 hours.

4.	Start time / Duration  in UTC (30 minutes) 

    2007-04-05T14:00:00+00:00/PT30M
    
    In this example, the time is represented as UTC and the duration expresses 30 minutes. 

5.	Start time / Duration in UTC (1 second)

    2007-04-05T14:00:00+00:00/PT1S
    
    In this example, the time is represented as UTC and the duration expresses 1 second.

6.	Start time / Duration 1 hour (San Francisco)

    2007-04-05T06:00:00-08:00/PT1H 
    
    In this example, the time represents Pacific Standard Time (a -08:00 UTC offset), and the duration expresses 1 hour.

7.	Start time / Duration 1 hour (Delhi)

    2007-04-06T03:00:00+05:30/PT1H
    
    In this example, the time represents the time in Delhi (a +5:30 UTC offset), and the duration expresses 1 hour.

8.	Start time / Duration 1 hour (New York)

    2007-04-05T04:00:00-05:00/PT1H 
    
    In this example, the times represents Eastern Standard Time with a -05:00 UTC offset and the duration expresses 1 hour.
    Example 9 shows timestamps from various countries

<b><i>All examples below have a start time of 2:00 pm (1400) on April 5, 2007; the durations vary.</i></b>

9.  Alaska UTC-9 

    Duration: 1 hour 
    
    2007-04-05T14:00:00-09:00/PT1H

10. Colorado UTC-7

    Duration: 1 year, 4 months, 1 day, 5 hours, 15 minutes, and 2 seconds
    
    2007-04-05T14:00:00-07:00/P1Y4M1DT5H15M2S

11. Costa Rica UTC-6

    Duration: 5 years, 6 months, 3 weeks, 5 days, 21 hours, 22 minutes, and 59 seconds
    
    2007-04-05T14:00:00-06:00/P5Y6M3W5DT21H22M59S 

12. Argentina UTC-3 

    Duration: 2 weeks, 1 day, and 11 seconds
    
    2007-04-05T14:00:00-03:00/P2W1DT11S 

13. Ethiopia UTC+3 

    Duration: 3 weeks 
    
    2007-04-05T14:00:00+03:00/P3W

14. Bangladesh UTC+6

    Duration: 1 minute 
    
    2007-04-05T14:00:00+06:00/PT1M 

15. South Korea UTC+9 

    Duration: 1 month 
    
    2007-04-05T14:00:00+09:00/P1M

16. Fiji UTC+12

    Duration: 41 seconds 
    
    2007-04-05T14:00:00+12:00/PT41S 
    

