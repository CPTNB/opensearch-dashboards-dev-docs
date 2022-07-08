# Investigating Security Issues

If you need to stand up the stack (database and dashboards) with the security plugin enabled and working you have a few options.

#### todo: why is this hard? What's the nuance you have to get right here? What does the security plugin need to be happy?

#### todo: link out to helpful security plugin docs, if they exist

1. Use the prebuilt docker containers distributed on the site
2. Attempt to build your own pre-built docker containers from specific versions
3. Set up a full stack locally executing local source

## Using prebuilt [docker containers](https://opensearch.org/downloads.html#opensearch)
This is a great option if you just want to reproduce an issue or see if an issue is a regression, but has limited value if you're trying to validate a change.

You can follow the instructions [here](https://opensearch.org/downloads.html#opensearch) to use docker compose to stand up a stack.

## Building your own prebuilt docker containers
You can:
1. build your own dashboards container using the opensearch-build repo
2. download the [docker-compose.yml file from the distribution site](https://opensearch.org/downloads.html#opensearch)
3. modify the docker-compose.yml file to point to the container you built locally
4. ```docker compose up``` should then use your custom container

The challenge with this approach is building your own "distribution" docker containers is not trivial and takes some fussing.

Some fussy things that make this hard:
1. you'll probably have npm package version missmatch problems
2. the build script and the docker script both expect to be run in CI, not locally.  This may be a soft blocker.

Rocky has extensive tooling around creating distribution docker containers, but it's not very easy to jump into as using it involves mutating jenkins builds and downloading from links you have to know before-hand, or have existing examples of before-hand.

#### ideal state: all the build scripts can be run on somebody's linux machine, and there's a command bank people can copy+paste from reliably

### TODO: detail/link to steps to build your own docker container

## Set up a stack running local source
todo
maybe, the right approach is to bundle the docker distribution build & docker-compose.yml edit into a script so you're really running approach #2.  The issue is building a local docker container is a time consuming process

