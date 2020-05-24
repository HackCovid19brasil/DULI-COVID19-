# Teachable Machine 
## About
 
The experiment is built using the [TensorFlow.js](https://js.tensorflow.org/) library.

We have also released a boilerplate version of this project that can be used as a starting point for your own projects: [googlecreativelab/teachable-machine-boilerplate](https://github.com/googlecreativelab/teachable-machine-boilerplate)

## Development
#### Install dependencies by running (similar to `npm install`)
```
yarn
```

#### Build project
```
yarn build
```

#### Start local server by running 
```
yarn run watch
```

#### Code Styles
- There’s a pre-commit hook set up that will prevent commits when there are errors
- Run `yarn eslint` for es6 errors & warnings
- Run `yarn stylint` for stylus errors & warnings

#### To run https locally:
https is required to get camera permissions to work when not working with `localhost`

1. Generate Keys
```
openssl genrsa -out server.key 2048
openssl req -new -x509 -sha256 -key server.key -out server.cer -days 365 -subj /CN=YOUR_IP
```
2. Use `yarn run watch-https`
3. Go to `https://YOUR_IP:3000`, then accept the insecure privacy notice, and proceed.  

## Credit
This is not an official Google product, but an experiment that was a collaborative effort by friends from [Støj](http://stoj.io/), [Use All Five](https://useallfive.com/) and Creative Lab and [PAIR](https://ai.google/pair/) teams at Google.
