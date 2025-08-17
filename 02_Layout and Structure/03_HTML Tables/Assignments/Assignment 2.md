# Assignment 2: Weekly Schedule with Spanning

## Objective
Create a weekly class schedule that demonstrates the use of `colspan` and `rowspan` attributes.

## Requirements
1. Create a properly structured HTML document
2. Add a heading "My Weekly Schedule"
3. Create a table that includes:
   - Days of the week (Monday through Friday)
   - Time slots (at least 4 different time periods)
   - Use `colspan` for activities that span multiple time periods
   - Use `rowspan` for activities that occur on multiple days at the same time
   - Include at least one lunch break that spans all days
   - Include a border and cellpadding

## Starter Code
```html
<!DOCTYPE html>
<html>
<head>
    <title>Weekly Schedule</title>
</head>
<body>
    <h1>My Weekly Schedule</h1>
    
    <!-- Create your schedule table here -->
    <!-- Remember to use:
         - colspan for activities across multiple time slots
         - rowspan for activities across multiple days
         - border and cellpadding attributes
         - th elements for headers
    -->
    
</body>
</html>
```

## Required Elements
Your schedule must include:
1. Header row with "Time" and days of the week
2. At least 4 time slots (e.g., 9:00 AM, 10:00 AM, etc.)
3. At least one activity using `colspan` (e.g., a 2-hour workshop)
4. At least one activity using `rowspan` (e.g., lunch every day at the same time)
5. Different classes/activities throughout the week

## Hints
- Plan your table on paper first
- Count carefully when using colspan and rowspan
- Remember that when a cell spans multiple rows, you don't include it in those other rows
- Use `<th>` for both day headers and time labels

## Submission Instructions
1. Save your file as `schedule.html`
2. Test thoroughly - check that all cells align properly
3. Commit to Git with message: "Complete Assignment 2 - Weekly Schedule"
4. Push to your GitHub repository