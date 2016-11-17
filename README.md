# Express Actuator

This middleware creates a series of endpoints to help you monitor and manage your application when it's pushed to production.

It is based on [Spring Boot Actuator](http://docs.spring.io/spring-boot/docs/current-SNAPSHOT/reference/htmlsingle/#production-ready) and the [healthcheck-ping](https://github.com/holidaycheck/healthcheck-ping) module by Mathias Schreck.

## Endpoints

| Path  	| Description                                              	|
|----------	|----------------------------------------------------------	|
| /info    	| Displays application info                                	|
| /metrics 	| Shows ‘metrics’ information for the current application. 	|

## Installation
```
$ npm install express-actuator --save
```

## Usage

```js
var actuator = require('express-actuator');

var app = express();

app.use(actuator());
```

If you want the endpoints to be available on a custom endpoint you can do so:

```js
app.use(actuator('/management')); // It will set /management/info
```