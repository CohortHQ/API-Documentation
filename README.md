# Cohort API

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
