# Spreadsheets

## Excel

### Last Value in a Column

`=LOOKUP(2,1/('Team Metrics'!AJ:AJ<>""),'Team Metrics'!AJ:AJ)`

### Second to Last Value in a Column

`=INDEX(FILTER('Team Metrics'!$AJ$3:$AJ$203, 'Team Metrics'!$AJ$3:$AJ$203<>""),COUNTA('Team Metrics'!$AJ$3:$AJ$203)-1,1)`
