# Authors/Books (dlr-library)
This app is only example to show how build a CRUD with ember.js 3, was built in the classic way specified in  [classic structure layout](https://cli.emberjs.com/release/advanced-use/project-layouts/#classiclayout) provider by ember-cli.

For developed-mode was added [ember-cli-mirage](https://www.ember-cli-mirage.com/), a mock data generator to create the needed resources, moreover the user interface was built with [Bulma Framework](https://bulma.io/documentation/)  to maintain it clean and simple. 

**NOTE**: all needed dependencies for this project have been added to the package.json file.

![Preview authors list ](https://github.com/dlr-delarocha/ember-library/blob/master/public/images/image01.png)
![Preview books list](https://github.com/dlr-delarocha/ember-library/blob/master/public/images/image02.png)

### Data structure 
This application only process two kind  of resources Authors and Books, both are created, update and deleted using [JSON API](https://jsonapi.org/examples/) specifications   

```mermaid
A((author)) -- hasMany --> B((book))
B((book)) -- belonTo -->  A((author)) 
```
### Endpoints 

Following are the endpoint needed for deploy in a production  environment, currently this endpoints are generated by [ember-cli-mirage](https://www.ember-cli-mirage.com/) 

- **namespace** = api/
- **Path URL** = https://localhost/
- **Full URL** = https://localhost/api

| HTTP Verb  | Endpoint  | 
|------------|-----------|
|POST        | authors   |
|GET         | authors   |
|GET         | authors/id |
|GET         | authors?filter='string' |
|GET         | authors/id?include=books |
|POST        | books |
|POST        | books/id |

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/) (with npm)
* [Ember CLI](https://ember-cli.com/)
* [Google Chrome](https://google.com/chrome/)

## Installation

* `git clone https://github.com/dlr-delarocha/ember-library.git` 
* `cd dlr-library`
* `npm install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).
* Visit your tests at [http://localhost:4200/tests](http://localhost:4200/tests).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Linting

* `npm run lint:hbs`
* `npm run lint:js`
* `npm run lint:js -- --fix`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

## Further Reading / Useful Links

* [ember.js](https://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
```shell
