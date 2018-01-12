:warning: This project is [deprecated](https://github.com/github/sre-lifecycle/issues/40) :warning:

### Nugget

Nugget is a service for performing http and tcp integration tests. It uses [turd](https://github.com/joewilliams/turd/) under the covers to verify urls are responding properly. Kinda like pingdom, better in some ways, worse in others.

#### Usage

The examples directory includes an example config file. The config file is a json description of tests you want to run.

The following starts nugget up in daemon mode. In this mode nugget just loops performing tests and writing the results in json to `/tmp/nugget_results.json`.

        $ nugget -c examples/config.json -d

Running nugget once is also possible.

        $ nugget -c examples/config.json

Nugget also includes a very basic web service daemon that simply reads the current results file.

        $ nugget -w

Additionally, nugget includes support for sending results of the tests to [backstop](https://github.com/obfuscurity/backstop).

![](https://dl.dropboxusercontent.com/s/1xhl7fnuw0y0934/2014-01-13%20at%207.47%20PM.png)

#### License

nugget is open source software available under the MIT License
