# Tips for debugging:


### Method to ensure a fresh calendar
A useful method to add is the following:

    function createFreshCalendar(){
      var cal = CalendarApp.getCalendarsByName(targetCalendarName)[0];
      if (cal != null)
        cal.deleteCalendar();
        
      cal = CalendarApp.createCalendar(targetCalendarName);
      cal.setColor('#c700ff');
      cal.setSelected(true);
    }

Then, as the very first line of `main()` you can call the method

---------------

### Using an explicit ics string instead of an url

You can add a string like this:

    var sourceCalendarString =
    "BEGIN:VCALENDAR\n"+
    "PRODID;X-RICAL-TZSOURCE=TZINFO:-//com.denhaven2/NONSGML ri_cal gem//EN\n"+
    "CALSCALE:GREGORIAN\n"+
    "VERSION:2.0\n"+
    "METHOD:PUBLISH\n"+
    "BEGIN:VTIMEZONE\n"+
    "TZID;X-RICAL-TZSOURCE=TZINFO:America/Chicago\n"+
    "BEGIN:STANDARD\n"+
    "DTSTART:20181104T020000\n"+
    "RDATE:20181104T020000\n"+
    "TZOFFSETFROM:-0500\n"+
    "TZOFFSETTO:-0600\n"+
    "TZNAME:CST\n"+
    "END:STANDARD\n"+
    "BEGIN:DAYLIGHT\n"+
    "DTSTART:20190310T020000\n"+
    "RDATE:20190310T020000\n"+
    "TZOFFSETFROM:-0600\n"+
    "TZOFFSETTO:-0500\n"+
    "TZNAME:CDT\n"+
    "END:DAYLIGHT\n"+
    "END:VTIMEZONE\n"+
    "BEGIN:VEVENT\n"+
    "EXDATE;TZID=America/Chicago:20190103T183000\n"+
    "EXDATE;TZID=America/Chicago:20190131T183000\n"+
    "DTEND;TZID=America/Chicago;VALUE=DATE-TIME:20181129T203000\n"+
    "DTSTART;TZID=America/Chicago;VALUE=DATE-TIME:20181115T183000\n"+
    "DTSTAMP;VALUE=DATE-TIME:20190128T180311Z\n"+
    "UID:c0412328-07fb-463c-81f0-0b97f0544219\n"+
    "DESCRIPTION:Test description\n"+
    "SUMMARY:Test title\n"+
    "RRULE:FREQ=WEEKLY;INTERVAL=1;UNTIL=20190322T045959Z;BYDAY=TH\n"+
    "LOCATION:Main Street Sports Center\n"+
    "END:VEVENT\n"+
    "END:VCALENDAR";
and change 

`var jcalData = ICAL.parse(response);`

to

`var jcalData = ICAL.parse(sourceCalendarString);`