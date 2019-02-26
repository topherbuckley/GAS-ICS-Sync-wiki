Currently, GAS-ICS-Sync does not have a form of unit testing. So here are some steps to do a test to verify the script is providing the same results as Google Calendar.

1. First, *if your changes only affect adding events*, I would suggest you make the temporary change detailed here: https://github.com/derekantrican/GAS-ICS-Sync/wiki/Debugging-tips
2. Put the ics/ical url into `sourceCalendarURL`
3. Make sure that `addEventsToCalendar` is turned on (along with any other settings that your change might affect)
4. Run the `main()` function. If your change affects modifying existing events or removing existing events, you may have to run it a couple times
5. Once that is completed, download the ics/ical file from the url to your computer
6. Go to https://calendar.google.com/calendar/r/settings/export and import that file into the same calendar (or another test calendar)
7. Verify that the events overlap exactly

IMPORTANT NOTE: until [#7](https://github.com/derekantrican/GAS-ICS-Sync/issues/7) is fixed, you may not see overlapping events for recurring events. Only the first instance of recurring events will be added.

-------------

#### Test Calendars (if anyone wants me to remove a calendar for privacy reasons, I can absolutely do so)

- https://www.lakecountystars.org/ical_feed?tags=791152%2C2220833%2C4032174%2C4362277%2C4362294%2C4362295%2C4380842%2C4380884%2C4426309%2C4426311%2C4426360%2C4426361%2C4426362%2C4426363%2C4426364%2C4426366%2C4426368%2C4426369%2C4426370%2C4426371%2C4426372%2C4426373%2C4426374%2C4426376 . This is a great calendar for testing recurrence. Can be verified at this page (make sure you go to "Show Tag Menu" and click "Select All Tags"): 
https://www.lakecountystars.org/page/show/2220833-calendar#
- https://pastebin.com/raw/UdYQe3Pj
- www.therapynotes.com/ical/zxofi_fbup/TherapyNotes.ics
- https://pastebin.com/raw/D0qFEDZi
- http://ical.8to18.com/link/jacksonville/2018-2019/BBB%20V/EDT (this one is currently failing as of [#23](https://github.com/derekantrican/GAS-ICS-Sync/issues/23)
- 