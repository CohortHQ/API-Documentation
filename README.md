# Cohort API

## Token generation

In order to access the Cohort API you need a valid token. Tokens can be generated using the {apiKey} and {secret} provided. Access tokens are valid for 30 days from the time of creation and you should add logic to your code to generate a new token in the case of an expired token.

    POST https://api.cohort.is/access/token

Example request:

    {
      "apiKey": "<apiKey>",
      "secret": "<secret>"
    }

Example response:

    {
      "code": 200,
      "data": {
        "token": "eyJhbGciOiJIUzI1NiIsInfdsfjds33434_fdsfdsfsdjojsf$$$$dsfsdfsdfeyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjoiSjd5aU1hMkU2NFo3RmhVelNBVzlsejJSbjk1MiIsImlhdCI6MTUxOTczNzcwNSwiZXhwIjoxNTIyMzI5",
        "exp": 1522329705
      }
    }

All requests should include the generated token in the Authorization header

## Intro endpoint

Provides info on up to 5 people who the user knows who could introduce them to a person. Also provides a total count of the people Cohort knows about that could introduce them.

    GET https://api.cohort.is/api/v1/intros?user=<twitterScreenName>&person=<twitterScreenName>

Example request:

    GET https://api.cohort.is/api/v1/intros?user=EamonLeonard&person=harper

Example response:

    {
      "code":200,
      "data":{
        "count":8,
        "inCommon":[
          {
              "name": "Ben Huh",
              "profileImageUrl": "https://d1dqcc0uivlrvs.cloudfront.net/8237.png",
              "twitterScreenName": "benhuh"
          },
          {
              "name": "Joe Stump",
              "profileImageUrl": "https://d1dqcc0uivlrvs.cloudfront.net/2792.png",
              "twitterScreenName": "joestump"
          },
          {
              "name": "Dylan Richard",
              "profileImageUrl": "https://d1dqcc0uivlrvs.cloudfront.net/9919.png",
              "twitterScreenName": "dylanr"
          },
          {
              "name": "John Collison",
              "profileImageUrl": "https://d1dqcc0uivlrvs.cloudfront.net/4554.png",
              "twitterScreenName": "collision"
          },
          {
              "name": "Alex Sexton",
              "profileImageUrl": "https://d1dqcc0uivlrvs.cloudfront.net/10195.png",
              "twitterScreenName": "SlexAxton"
          }
        ]
      }
    }
