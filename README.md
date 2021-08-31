# ReAGEnT

Realtime Analysis of German Election noting tweets

Collects, sorts, analyzes and presents tweets from german politicians regarding the election 2021. 

![sequence_diagram](https://github.com/ReAGEnT-HTW-Berlin/Wiki/blob/main/ReAGEnT_sequence_diagram_v1.1.png)

## [API Wrapper](https://github.com/ReAGEnT-HTW-Berlin/ReAGEnT-API-Wrapper)
The API Wrapper is responsible for collecting tweets from the Twitter API v2 endpoint using Spark Structured Streaming. The data is sorted, analyzed and saved to Mongo DB according to rules set in main class.

- [Twitter API v2](https://developer.twitter.com/en/docs/twitter-api/early-access)
- [Spark Streaming](https://spark.apache.org/docs/latest/streaming-programming-guide.html)
- [Spark Structured Streaming](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html)
- [mongoDB](https://www.mongodb.com)

Written in Scala.

## [Spark (Backend)](https://github.com/ReAGEnT-HTW-Berlin/ReAGEnT-Spark)
This part is responsible for taking the raw information from the Mongo DB and computing the information for the frontend. Thereafter saving it again in the Mongo DB.

- [Apache Spark](https://spark.apache.org/docs/1.2.0/programming-guide.html)

Written in Scala.

## [AkkaHTTP](https://github.com/ReAGEnT-HTW-Berlin/ReAGEnT-AkkaHttp)
Routes Mongo DB content to the frontend.

- [mongoDB](https://www.mongodb.com)
- [AkkaHTTP](https://doc.akka.io/docs/akka-http/current/index.html)

Written in Scala.

## [Frontend](https://github.com/ReAGEnT-HTW-Berlin/ReAgentFrontEnd)
Web representation of analyzed data.

- [React](https://reactjs.org/docs/getting-started.html)
- [Chart.js](https://www.chartjs.org/docs/latest/)

Written in JavaScript.
