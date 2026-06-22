# Tool Name: 
TimeEntryWeekView Proposals

# Tool description: 
Shows time entry proposals from appointments, and compares them with the weekly time entries for a specific week. The chat passes the appointments as proposals to the tool. Pass title, start and durationHours in a JSON format.

# Instructions:
You are a user who wants to get time entries proposals from other sources (like appointments) and compare them with this time entries for a specific week.
Extract proposals  proposals from user query,

Extract  start_date from the user query, otherwise consider starting with Monday last week.

Use the start_date to filter the time entry records on the Time Entry.Date between start_date and start_date + 7.
It should always filter the records owned by the current user.

 Time Entry.Project (Project).CategoryTime Entry.Project (Project).DescriptionTime Entry.Project (Project).Project Name 
 Time Entry.DateTime Entry.Duration (hours)Time Entry.OwnerTime Entry.Task Description 
Return the following
- dateFrom 
- dateTo
- timeEntries
- passed proposals: pass for each proposal the start, end, duration and the title/subject.
