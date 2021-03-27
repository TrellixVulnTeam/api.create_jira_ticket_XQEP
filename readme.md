# Create a Jira ticket with an API

## Objective 
Send a payload to an api that will create an issue here: `https://lowranceworks.atlassian.net/jira/software/projects/FP/boards/1`

## Notes
The documentation may NOT apply to both Jira Server and Jira Cloud

## Jira Cloud Documentation 
[Create an issue](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/)
[Jira Cloud platform Developer Reference](https://developer.atlassian.com/cloud/jira/platform/rest/v3/intro/)
<!-- []() -->

## Jira Server Documentation 
<!-- 
## Documentation 
[Jira Rest API GET/POST Request with Postman | Create Jira Issues Tutorial](https://www.youtube.com/watch?v=pcNqjBlhipU)
[Jira Rest API Intro](https://developer.atlassian.com/cloud/jira/software/rest/intro/#introduction)
[Jira Rest API Examples](https://developer.atlassian.com/server/jira/platform/jira-rest-api-examples/)
[Jira Cloud platform Developer Reference](https://developer.atlassian.com/cloud/jira/platform/rest/v3/intro/#version)
[Create Jira issue via rest api - python](https://community.atlassian.com/t5/Jira-questions/Create-Jira-issue-via-rest-api-python/qaq-p/455623)
[Python Client for Jira REST API](https://marketplace.atlassian.com/archive/1210871) -->

## Getting started

visit the following links inside your browser: \
`https://lowranceworks.atlassian.net/rest/api/2/issue/createmeta` - to see stuff \
`https://lowranceworks.atlassian.net/rest/api/2/issue/createmeta?projectKeys=FP&expand=projects.issuetypes.fields` to see stuff under your project (FP = project key)  


the links above used the api version 2, let's use the newest version (3) \
`https://lowranceworks.atlassian.net/rest/api/3/issue/createmeta` 
`https://lowranceworks.atlassian.net/rest/api/3/issue/createmeta?projectKeys=FP&expand=projects.issuetypes.fields` 






```
{
    "fields": {
       "project":
       { 
          "key": "FP"
       },
       "summary": "Issue created via REST.",
       "description": "bla bla bla goes here",
       "issuetype": {
          "name": "Test bug"
       }
   }
}
```

POST **https://lowranceworks.atlassian.net/rest/api/3/issue/**
```
{
    "fields": {
        "project": {
            "key": "FP"
        },
        "summary": "Jira Rest API via Postman.",
        "description": {
            "type": "doc",
            "version": 1,
            "content": [
                {
                    "type": "paragraph",
                    "content": [
                        {
                            "type": "text",
                            "text": "description"
                        }
                    ]
                }
            ]
        },
        "issuetype": {
            "name": "Story"
        }
    }
}
```

Learning how to talk to the api

https://lowranceworks.atlassian.net/rest/api/3/issue/DEMO-1
