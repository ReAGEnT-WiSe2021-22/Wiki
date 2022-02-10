# ReAGEnT

Realtime Analysis of German Election noting tweets

Collects, sorts, analyzes and presents tweets from german politicians regarding the election 2021. 

![sequence_diagram](https://raw.githubusercontent.com/ReAGEnT-WiSe2021-22/Wiki/main/ReAGEnT_sequence_diagram_v1.1.png)

## [API Wrapper](https://github.com/ReAGEnT-HTW-Berlin/ReAGEnT-API-Wrapper)
The API Wrapper is responsible for collecting tweets from the Twitter API v2 endpoint using Spark Structured Streaming. The data is sorted, analyzed and saved to Mongo DB according to rules set in main class.

- [Twitter API v2](https://developer.twitter.com/en/docs/twitter-api/early-access)
- [Spark Streaming](https://spark.apache.org/docs/latest/streaming-programming-guide.html)
- [Spark Structured Streaming](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html)
- [mongoDB](https://www.mongodb.com)

Written in Scala.

## [Twint API Wrapper](https://github.com/ReAGEnT-WiSe2021-22/Twint-API)
Historical data from Twitter is loaded with the help of the inofficial Twint API

- [Twint API GitHub](https://github.com/twintproject/twint)

Written in Python.

## [SparkML](https://github.com/ReAGEnT-WiSe2021-22/ReAGEnT-SparkNLP-SparkML)
Raw data from the Mongo DB is loaded and used to train a model with the help of the Spark Machine Learning library (MLlib).

- [MLlib Guide](https://spark.apache.org/docs/latest/ml-guide.html)

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

## [Frontend v1](https://github.com/ReAGEnT-HTW-Berlin/ReAgentFrontEnd)
Web representation of analyzed data.

- [React](https://reactjs.org/docs/getting-started.html)
- [Chart.js](https://www.chartjs.org/docs/latest/)

Written in JavaScript.

## [Frontend v2](https://github.com/ReAGEnT-WiSe2021-22/frontend-v2)
Web representation of analyzed data. We are using the micro front end architecture, this project / repository acts as the container project that "*contains*" and loads the individual micro frontends. This container app is built with [React](https://reactjs.org/), and it loads the micro front end with two different approaches:
- Loading the bundled JS file from the local folder (`src/wc`)
- Loading the bundled JS file from a remote source (in this case, from site hosted on Github Pages)

All the individual micro front ends are bundled into a single JS file and converted into a web component, so the project could be framework agnostic.

Please take a look into our [Proof of Concept](https://github.com/LouisAndrew/poc-microfrontend/edit/main/README.md) project for a more simplified example.

Dependencies that we used are:
- [Direflow](https://direflow.io/)
- [Reactivesearch](https://opensource.appbase.io/reactivesearch/)
- [Tailwindcss v2](https://v2.tailwindcss.com/)
- [craco-swc](https://github.com/pradel/create-react-app-swc/blob/main/packages/craco-swc/README.md)
- [Material UI](https://mui.com/)
- [Miragejs](https://miragejs.com/)
- [React DnD](https://react-dnd.github.io/react-dnd/about)
- [random-ext](https://github.com/bkumar2/random-ext)
- [faker](https://fakerjs.dev/)
- [ESLint](https://eslint.org/)
- [Recharts](https://recharts.org/en-US/)
- [axios](https://axios-http.com/docs/intro)

Written in TypeScript.
