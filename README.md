# Cohort API

## Intro endpoint
Provides info on up to 5 people who the user knows who could introduce them to a person. Also provides a total count of the people Cohort knows about that could introduce them.

    GET <url>?user=<twitter_screen_name>&person=<twitter_screen_name>
    
Example request:

    GET <url>?user=EamonLeonard&person=chacon

Example response:

    {
      "code":200,
      "data":{
        "count":8,
        "inCommon":[
          {
            "name":"Niall Harbison",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/11830.png",
            "twitterScreenName":"NiallHarbison"
          },
          {
            "name":"Eoin Hurrell",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/68636.png",
            "twitterScreenName":"eoinhurrell"
          },
          {
            "name":"Brendan Hastings",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/51479.png",
            "twitterScreenName":"brendannh"
          },
          {
            "name":"LoJo",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/31103.png",
            "twitterScreenName":"Louise_Johnston"
          },
          {
            "name":"Barry",
            "profileImageUrl":"https://d1dqcc0uivlrvs.cloudfront.net/7765.png",
            "twitterScreenName":"nouvation"
          }
        ]
      }
    }
