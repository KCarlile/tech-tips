# Spreadsheets

## Excel

### Last Value in a Column

`=LOOKUP(2,1/('Team Metrics'!AJ:AJ<>""),'Team Metrics'!AJ:AJ)`

Source: [YouTube: ExcelMoments - Second to last non-blank cell excel](https://www.youtube.com/watch?v=5dqG_BoZOFc)

### Second to Last Value in a Column

`=INDEX(FILTER('Team Metrics'!$AJ$3:$AJ$203, 'Team Metrics'!$AJ$3:$AJ$203<>""),COUNTA('Team Metrics'!$AJ$3:$AJ$203)-1,1)`

Source: [YouTube: ExcelMoments - Second to last non-blank cell excel](https://www.youtube.com/watch?v=5dqG_BoZOFc)
