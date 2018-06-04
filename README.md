# node-chrome

Simple Docker image based on the [official node image](https://hub.docker.com/_/node/) but with Chrome installed for running Karma tests in a CI pipeline.

Make sure to configure ChromeHeadless to run with the `--no-sandbox` flag in your Karma config:
```
browsers: ['ChromeHeadlessNoSandbox'],
customLaunchers: {
    ChromeHeadlessNoSandbox: {
        base: 'ChromeHeadless',
        flags: ['--no-sandbox']
    }
}
```
