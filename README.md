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

    GET https://api.cohort.is/api/v1/twitter/intros?user=<twitterScreenName>&person=<twitterScreenName>

Example request:

    GET https://api.cohort.is/api/v1/twitter/intros?user=EamonLeonard&person=chacon

Example response:

    {
      "code":200,
      "data":{
        "count":8,
        "inCommon":[
          {
            "name":"Ben Foo",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/0.png",
            "twitterScreenName":"benFoo"
          },
          {
            "name":"Ben Foo",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/0.png",
            "twitterScreenName":"benFoo"
          },
          {
            "name":"Ben Foo",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/0.png",
            "twitterScreenName":"benFoo"
          },
          {
            "name":"Ben Foo",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/0.png",
            "twitterScreenName":"benFoo"
          },
          {
            "name":"Ben Foo",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/0.png",
            "twitterScreenName":"benFoo"
          }
        ]
      }
    }
