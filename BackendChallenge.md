# D&amp;B Solution Engineering Backend Challenge

Thank you for taking the time to do our technical test. It consists of two parts:

* A coding test
* A few technical questions

In order to avoid bounced emails, we would like you to submit your results by uploading the relevant ZIP file to a shared web accessible storage folder on Microsoft OneDrive. In order to obtain the URL for this folder, please supply your email address to either your agent or the D&B member of staff who assigned you the test.

Please make this a single zip file named {yourname}-{role-applied-for}.zip containing:

1. A single markdown file with the answers to the technical questions
2. One folder containing the technical test 

## Coding exercise
As a backend engineer, you'll be working with APIs (Such as AWS's EC2 API). This test is designed to give you the opportunity to show your ability to query an API using languages that are commonly used during operations at D&B.

We are in need of a passthrough service that will provide currency conversions paired with the latest Bitcoin prices for that currency in a single response. The response needs to be formatted to match the fixer.io response formatting as our integration systems are already built to consume that response body. This service will be used for all of our customers, so we need to be able to assist them with any errors they see, thus, having the outputs logged for error management is needed.
 ##### Example fixer.io response object

```javascript
GET https://data.fixer.io/api/latest
 
{
  "base": USD,
  "date": "2018-02-13",
  "rates": {
     "CAD": 1.260046,
     "CHF": 0.933058,
     "EUR": 0.806942,
     "GBP": 0.719154,
     [170 world currencies]
  }
}
```
##### Example Bitcoin response object

```javascript
GET https://blockchain.info/ticker
 
{
  "USD" : {"15m" : 6698.95, "last" : 6698.95, "buy" : 6698.95, "sell" : 6698.95, "symbol" : "$"},
  "AUD" : {"15m" : 9289.0, "last" : 9289.0, "buy" : 9289.0, "sell" : 9289.0, "symbol" : "$"},
  "BRL" : {"15m" : 26710.77, "last" : 26710.77, "buy" : 26710.77, "sell" : 26710.77, "symbol" : "R$"},
  "CAD" : {"15m" : 8733.48, "last" : 8733.48, "buy" : 8733.48, "sell" : 8733.48, "symbol" : "$"},
  "CHF" : {"15m" : 6544.54, "last" : 6544.54, "buy" : 6544.54, "sell" : 6544.54, "symbol" : "CHF"},
  "CLP" : {"15m" : 4421304.07, "last" : 4421304.07, "buy" : 4421304.07, "sell" : 4421304.07, "symbol" : "$"},
  "CNY" : {"15m" : 46157.74, "last" : 46157.74, "buy" : 46157.74, "sell" : 46157.74, "symbol" : "¥"},
  "DKK" : {"15m" : 42866.47, "last" : 42866.47, "buy" : 42866.47, "sell" : 42866.47, "symbol" : "kr"},
  "EUR" : {"15m" : 5744.21, "last" : 5744.21, "buy" : 5744.21, "sell" : 5744.21, "symbol" : "€"},
  "GBP" : {"15m" : 5119.52, "last" : 5119.52, "buy" : 5119.52, "sell" : 5119.52, "symbol" : "£"},
  "HKD" : {"15m" : 52341.88, "last" : 52341.88, "buy" : 52341.88, "sell" : 52341.88, "symbol" : "$"},
  "INR" : {"15m" : 486415.33, "last" : 486415.33, "buy" : 486415.33, "sell" : 486415.33, "symbol" : "₹"},
  "ISK" : {"15m" : 739900.06, "last" : 739900.06, "buy" : 739900.06, "sell" : 739900.06, "symbol" : "kr"},
  "JPY" : {"15m" : 759431.78, "last" : 759431.78, "buy" : 759431.78, "sell" : 759431.78, "symbol" : "¥"},
  "KRW" : {"15m" : 7463881.41, "last" : 7463881.41, "buy" : 7463881.41, "sell" : 7463881.41, "symbol" : "₩"},
  "NZD" : {"15m" : 10122.31, "last" : 10122.31, "buy" : 10122.31, "sell" : 10122.31, "symbol" : "$"},
  "PLN" : {"15m" : 24552.64, "last" : 24552.64, "buy" : 24552.64, "sell" : 24552.64, "symbol" : "zł"},
  "RUB" : {"15m" : 438603.41, "last" : 438603.41, "buy" : 438603.41, "sell" : 438603.41, "symbol" : "RUB"},
  "SEK" : {"15m" : 59254.03, "last" : 59254.03, "buy" : 59254.03, "sell" : 59254.03, "symbol" : "kr"},
  "SGD" : {"15m" : 9162.15, "last" : 9162.15, "buy" : 9162.15, "sell" : 9162.15, "symbol" : "$"},
  "THB" : {"15m" : 217233.41, "last" : 217233.41, "buy" : 217233.41, "sell" : 217233.41, "symbol" : "฿"},
  "TWD" : {"15m" : 204554.69, "last" : 204554.69, "buy" : 204554.69, "sell" : 204554.69, "symbol" : "NT$"}
}
```

#### Platform / Language Choice
You can create the application as either a command line application or web application in any of the following languages:

* PHP
* Javascript
* Java
* Python
* PowerShell
* Bash
* Ruby
* .NET / C#

#### Task requirements
Feel free to spend as much or as little time on the exercise as you like (we wouldn't expect more than 4 hours) as long as the following requirements have been met.

Please complete the user story below.
Your code should compile and run in one step.
Feel free to use whatever frameworks/ libraries/packages you like.

#### User Story
As a user running the application
I can view a list of currencies with an appended bitcoin value in a user submitted base currency (ex. USD)
So that I can see all of my purchasing options of global currency in a single view

#### Acceptance criteria
1. For the known currency USD, results are returned
2. All default currencies, as well as bitcoin, are displayed in a valid JSON object.

#### Technical Details
* Currency conversion: https://fixer.io/documentation {Latest Rates Endpoint}
* Bitcoin conversion: https://blockchain.info/ticker
* If the user submits invalid data logic, that should be handled appropriately.
* The session information does not have to persist, it's expected the customer will submit the same request every time they wish to collect for a certain currency.
 

## Technical Questions
* Did you have time to complete the coding test? What would you add to your solution if you had more time?
* What's your favourite programming language? Why?
* List a few of your preferred frameworks (also let us know in which situations you would choose to use/not use them)
* Please describe yourself using either JSON or emojis.
 

Thanks for your time, we look forward to hearing from you!