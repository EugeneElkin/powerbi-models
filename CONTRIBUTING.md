# Contributing

## Setup

Clone the repository:
```
git clone https://github.com/Microsoft/powerbi-models
```

Install global dependencies if needed:
```
npm install -g typescript gulp typings
```

Install local dependencies:
```
typings install
npm install
```

## Building
```
gulp build
```
Or if using VS Code: `Ctrl + Shift + B`

## Testing
```
npm test
```
> Note currently there seems to be a problem when running the tests using PhantomJS which is why the `--chrome` flag is coded into the test command.

Run tests with PhantomJS
```
gulp test
```

There are various command line arguments that can be passed to the test command to facilitate debugging:

Run tests with Chrome
```
gulp test --chrome
```

Enable  debug level logging for karma, and remove code coverage
```
gulp test --debug
```

Disable single run to remain open for debugging
```
gulp test --watch
```

These are often combined and typical command for debugging tests is:
```
gulp test --chrome --debug --watch
```