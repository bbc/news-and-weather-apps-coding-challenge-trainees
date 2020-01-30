# BBC News and Weather Apps Trainee Coding Challenge

## Introduction
You have been asked to kick off a new native Android or iOS news app, consisting of two screens
- The first screen will simply display a list of the headlines (fetched from a server - see below) and the last updated date
- When the user taps on a headline, the application then shows a second screen containing the headline and the last updated date again, as well as the introductory paragraph

The returned timestamp is in epoch time but the design calls for this to be a human readable day, month and year. So, for example, it should show as "1 January 1970" for an epoch timestamp of 0.

The user should also be able to trigger a reload of the data from the server.

### API
The list of headlines is available at
https://github.com/bbc/news-and-weather-apps-coding-challenge-trainees/blob/master/headlines.json

```bash
curl -G https://raw.githubusercontent.com/bbc/news-and-weather-apps-coding-challenge-trainees/master/headlines.json
```

### Analytics
The product manager needs you to record interaction and network events as people use the app. This can be done by issuing “fire and forget” GET requests to
https://github.com/bbc/news-and-weather-apps-coding-challenge-trainees/blob/master/analytics

Event specific query parameters should be appended to the URL as follows:

* `event=load` – any network request
* `time=xxx` - the time (in ms) for the network request to complete. I.e. the round trip time for the HTTP request
* `event=display` – whenever a screen is shown (the headline or the article)
* `screen=XXX` - an identifier for the screen that was shown

```bash
curl -G https://raw.githubusercontent.com/bbc/news-and-weather-apps-coding-challenge-trainees/master/analytics?event=load&time=100
```

```bash
curl -G https://raw.githubusercontent.com/bbc/news-and-weather-apps-coding-challenge-trainees/master/analytics?event=display&screen=XXX
```

### Considerations
This is an opportunity to demonstrate your understanding of what modern Android or iOS app development looks like. We believe that good contributors to achieving this are typically code readability, unit testing, separation of concerns, the open/closed principle, error handling, and an intuitive, responsive, user interface.

You can write the app in either of the native languages for iOS (Swift or Objective C) or Android (Kotlin or Java). 

Remember we are looking for a demonstration of your skills - not perfection. A comment about what you would do next might be better than squeezing in everything. We would typically expect this to take you  between 2-3 evenings at most. 

### Submissions
To submit your code, please create a private GitHub repo (it’s free) and share your code repo with our GitHub user, [newsapps-tr](https://github.com/newsapps-tr). Please note that we will be considering your git commit history during our evaluation.

_Under no circumstances make the repository public._
_Please email your BBC HR contact separately as well to confirm your submission._

