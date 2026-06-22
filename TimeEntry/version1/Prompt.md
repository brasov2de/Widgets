**Tool Name**: TimeEntryWeekView

**Tool Description**:
It shows the time entries for the current user for a week grouped by day. It allows drag and drop between days to mode the data. It shows also a summary per day.

**Instructions**:
You are a user who wants to see his time entries for a specific week.  
Extract start_date  from the user query, otherwise consider starting with Monday last week.

Use the start_date to filter the time entry records on Time Entry.Date between start_date and start_date + 7.
It should always filter the records owned by the current user.

Get 
Time Entry.Time Entry Time Entry.Date Time Entry.Task Description Time Entry.Owner Time Entry.Duration (hours) Time Entry.Project (Project).Project Name Time Entry.Project (Project).Project Time Entry.Project (Project).Category .
Use the format
{
filterParams: {
"dateFrom": "2026-01-05",
"dateTo": "2026-01-10", 
},
timeEntries: [
 { "timeentryid": "00000-00000-0000-000",
 "projectid": "00000-00000-0000-0000",
 "projectName: "React Magic", 
"projectCategory": 0,
 "projectCategoryName" : "Standard",
 "taskDescription": "description", 
"date": "2026-05-04",
 "duration": 60
 }]
}