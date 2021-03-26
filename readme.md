# Create a Jira ticket with an API

## Objective 
Send a payload to an api that will create an issue here: `https://lowranceworks.atlassian.net/jira/software/projects/FP/boards/1`

## Documentation
[Create Jira issue via rest api - python](https://community.atlassian.com/t5/Jira-questions/Create-Jira-issue-via-rest-api-python/qaq-p/455623)
[Python Client for Jira REST API](https://marketplace.atlassian.com/archive/1210871)
## Getting started

The payload that will be sent to the api: 
```
{
    "fields": {
       "project":
       { 
          "key": "AWD"
       },
       "summary": "Issue created via REST.",
       "description": "bla bla bla goes here",
       "issuetype": {
          "name": "Task"
       }
   }
}
```

And also reduce your call to: curl -D- -u user:pass -X POST --data @data.json -H 'Content-Type: application/json' http://localhost:8080/rest/api/2/issue/