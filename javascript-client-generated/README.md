# todolist_res_tful_api

TodolistResTfulApi - JavaScript client for todolist_res_tful_api
OpenAPI for Todolist RESTful API
This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1
- Package version: 1
- Build package: io.swagger.codegen.v3.generators.javascript.JavaScriptClientCodegen
For more information, please visit [www.linkedin.com/in/fajar-zulmi-sopian-03910b1b4](www.linkedin.com/in/fajar-zulmi-sopian-03910b1b4)

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install todolist_res_tful_api --save
```

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/GIT_USER_ID/GIT_REPO_ID
then install it via:

```shell
    npm install GIT_USER_ID/GIT_REPO_ID --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var TodolistResTfulApi = require('todolist_res_tful_api');
var defaultClient = TodolistResTfulApi.ApiClient.instance;

// Configure API key authorization: TodolistAuth
var TodolistAuth = defaultClient.authentications['TodolistAuth'];
TodolistAuth.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.apiKeyPrefix['X-API-KEY'] = "Token"

var api = new TodolistResTfulApi.TodolistApi()
var opts = { 
  'includeDone': false, // {Boolean} Is include done todolist
  'name': "name_example" // {String} Filter todolist by name
};
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.todolistGet(opts, callback);
```

## Documentation for API Endpoints

All URIs are relative to *https://{environment}.programmerzamannow.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*TodolistResTfulApi.TodolistApi* | [**todolistGet**](docs/TodolistApi.md#todolistGet) | **GET** /todolist | Get all todolist
*TodolistResTfulApi.TodolistApi* | [**todolistPost**](docs/TodolistApi.md#todolistPost) | **POST** /todolist | Create new todolist
*TodolistResTfulApi.TodolistApi* | [**todolistTodolistIdDelete**](docs/TodolistApi.md#todolistTodolistIdDelete) | **DELETE** /todolist/{todolistId} | Delete existing todolist
*TodolistResTfulApi.TodolistApi* | [**todolistTodolistIdPut**](docs/TodolistApi.md#todolistTodolistIdPut) | **PUT** /todolist/{todolistId} | Update Existing todolist

## Documentation for Models

 - [TodolistResTfulApi.ArrayTodolist](docs/ArrayTodolist.md)
 - [TodolistResTfulApi.CreateOrUpdateTodolist](docs/CreateOrUpdateTodolist.md)
 - [TodolistResTfulApi.InlineResponse200](docs/InlineResponse200.md)
 - [TodolistResTfulApi.Todolist](docs/Todolist.md)
 - [TodolistResTfulApi.TodolistBody](docs/TodolistBody.md)
 - [TodolistResTfulApi.TodolistTodolistIdBody](docs/TodolistTodolistIdBody.md)

## Documentation for Authorization


### TodolistAuth

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header

