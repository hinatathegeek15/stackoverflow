<img src="https://csshint.com/wp-content/uploads/2019/05/Animated-Logo-examples-2.gif">

## Tech Stack
<p align="left"> 
  <a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://expressjs.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" alt="express" width="40" height="40"/> </a> <a href="https://redux.js.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redux/redux-original.svg" alt="redux" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="mongodb" width="40" height="40"/> </a> <a href="https://kafka.apache.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/apache_kafka/apache_kafka-icon.svg" alt="kafka" width="40" height="40"/> </a> <a href="https://mochajs.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/mochajs/mochajs-icon.svg" alt="mocha" width="40" height="40"/> </a> <a href="https://redis.io" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-original-wordmark.svg" alt="redis" width="40" height="40"/> </a> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> 
</p>

## System Architecture

The application is a 3-tier architecture with the technology stack used below.
 
* ##### Client/Tier-1 : React.js with Redux 
* ##### MiddleWare/Tier-2: Kafka, Passport JWT, Redis cache 
* ##### Backend/ Tier -3: Node.js, MySQL, MongoDB, Cloudinary storage. 

## Object Management Policy

When a request is made from the client, the request is processed by the API gateway, and the request, along with its parameters like path params, query params and body params are extracted and forwarded to Kafka with a request identifier. Kafka backend which is subscribed to the topic consumes the messages and in turn calls the required controller logics to processes all the business logics. Once the request task is accomplished, the response is put back to the queue for the client to consume. 

The addition of Kafka in the middleware gives better throughput when scaled horizontally though it might drag the performance for less amount of users. From our load and performance testing sessions with various combinations in the instances, we observed it’s throughput when more number of concurrent users were directed to the server. We realized Kafka would be a great fit for microservices, distributed and event driven applications since it can scale at ease.

## Handling heavyweight resources
*	The server's load was distributed and handled via load balancing to multiple instances of our application.
*	To reduce the strain on the database, Redis caching was employed for the most frequently used APIs, resulting in improved speed and retrieval.
*	For system speed and scalability over the data layer, connection pooling was used.
*	Using Kafka, I was able to build a fault-tolerant and scalable system. As the number of concurrent users grew, each thread was handled in a reliable     manner.
*	I utilized Kafka as a messaging queue to handle numerous requests in the backend to manage big-weight resources. I also used Connection pooling to       speed up the fetch response.

## Policy used to decide entry of data into database
#### MySQL : 
I stored tags in MySQL because these entities are independent. 

#### MongoDB:
MongoDB is a schema-less database, and its unstructured. I stored messages, questions, and users in MongoDB for faster retrieval.
Scaling helps in increasing the performance of an application.

## Screenshots of the App

<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/architecture.png">

#### Database Schema
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/mongo_schema.png">
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/mysql_schema.png">

#### Sign Up
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/signup.png">

#### Login Up
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/login.png">

#### Home Page
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/home.png">

#### Answers
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/answers.png">

#### Tags Overview
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/tags.png">

#### Users Overview
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/tags.png">

#### Admin Analytics
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/analytics.png">

#### Add Tag
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/addtag.png">

#### Messages
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/messages.png">

#### User Profile Overview 
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/userProfileOverview.png">
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/userProfileOverview_2.png">

#### Badges
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/badges.png">

#### Reputation
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/reputation.png">

#### Search Features
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/searchFeatures.png">

#### Questions Based on Score
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/questionsBasedOnScore.png">

#### Questions Based on Interesting Filter
<img src="https://github.com/Rajashekarredde/stackoverflow/blob/main/images/questionsOnInteresting.png">






