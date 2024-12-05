# Spreadsheets

## Excel

### Last Value in a Column

`=LOOKUP(2,1/('Team Metrics'!AJ:AJ<>""),'Team Metrics'!AJ:AJ)`

Source: [YouTube: ExcelMoments - Second to last non-blank cell excel](https://www.youtube.com/watch?v=5dqG_BoZOFc)

### Second to Last Value in a Column

`=INDEX(FILTER('Team Metrics'!$AJ$4:$AJ$204, 'Team Metrics'!$AJ$4:$AJ$204<>""),COUNTA(FILTER('Team Metrics'!$AJ$4:$AJ$204, 'Team Metrics'!$AJ$4:$AJ$204<>""))-1,1)`

Source, modified: [YouTube: ExcelMoments - Second to last non-blank cell excel](https://www.youtube.com/watch?v=5dqG_BoZOFc)
