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