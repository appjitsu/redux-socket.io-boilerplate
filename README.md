# partyq
partyq

## Commands
  - `npm start` runs the development server with [hot-loading](https://github.com/gaearon/react-hot-loader).
  - `npm test` runs both server side and client side tests
  - `npm run lint` runs eslint on files
  - `npm run build` builds partyq for production
  - `npm run test:server` runs server side tests
  - `npm run test:client` runs client side tests
  - `npm run test:watch` runs tests when files change

## Layout
  - [/test](test/) General tests that do not fit in front or backend.
    - [/test/learning](test/learning) various non-application tests. Used to experiment with a new API or get comformable with the testing framework.

### Frontend
  - [/app](app/) root of front end code
  - [/app/test](app/test) front end tests

### Backend
  - [/server](server/) contains the main backend source code for partyq. Reducer, Redux store, and core functionality.
  - [/server/test](server/test/) contains chai tests for the partyq backend.

## Packages

### [React](https://facebook.github.io/react/)


### [Redux](http://redux.js.org/)
Redux manages the state in partyq. We want to represent our application's state as an immutable tree data structure. We change the state by applying function to the state tree.
  - [partyq reducer](server/reducer.js)
  - [partyq store](server/store.js)

### Dependencies
  - [Immutable](https://facebook.github.io/immutable-js/) for immutable data structure to promote pure functions and functional style.
    - See [/tests/learning/immutable_spec.js](tests/learning/immutable_spec.js) for an example of how to use and test the immutable data structures.
    - [Full API Docs](https://facebook.github.io/immutable-js/docs/#/)
  - [Socket.io](http://socket.io/) abstracts websockets for realtime applications

### Dev Dependencies
  - [Babel](https://babeljs.io/) to support ES6 features such as modules
  - [Mocha](https://mochajs.org/) and [Chai](http://chaijs.com/) for unit testing.
    - [Chai Immutable](https://github.com/astorije/chai-immutable) for using immutable with chai tests.
  - [Eslint](http://eslint.org/) ensures coding standards. Current settings can be found in [.eslintrc](.eslintrc).
    - Extends the [airbnb eslint](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb) configuration for ES6.
    - [babel-eslint](https://github.com/babel/babel-eslint) to lint ES6 code.
    - [eslint-plugin-react](https://github.com/yannickcr/eslint-plugin-react) to lint React and jsx parts.
  - [pre-commit](https://github.com/observing/pre-commit) to run lint and test before each commit

### TODO
Document
  - express
  - http-proxy
  - rimraf
  - webpack
  - webpack-dev-middleware
  - webpack-dev-server
  - webpack-hot-middleware
