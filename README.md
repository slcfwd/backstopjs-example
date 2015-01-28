# BackstopJS Example

[BackstopJS](https://github.com/garris/BackstopJS) is a CSS regression testing
tool.

> BackstopJS automates CSS regression testing of your responsive web UI by
comparing DOM screenshots at various viewport sizes.


## Step-by-Step

To see how I setup this example step through the commits one by one.


## Prerequisites

To run this example you must have [NodeJS][] installed in your environment.


## Setup and Usage

After cloning the repository, you'll want to install dependencies:

```shell
npm install
```

This will install [PhantomJS][], [CasperJS][], and [BackstopJS][] in
`node_modules`, as local project dependencies. No global installations or `sudo`
required.

Strangely, BackstopJS is not a javascript module or command line tool. It uses
[GulpJS][] tasks to do it's thang.

To make running BackstopJS tasks easier, I've aliased in `package.json` so you
can simply do:

```shell
npm run backstop <task>
```

Again, no need to install anything globally or with `sudo`.

There are two tasks that you'll use:

+ `reference`: Generates a set of reference files, creating a "snapshot" of how
things should be, your "expected" result from testing.
+ `test`: Generates a set of test files, creating a "snapshot" of how things
really are, the "actual" result of testing. Opens a report in the browser.

Look in `node_modules/BackstopJS/gulpfile.js` for other tasks, but make sure you
know what you are doing.

Configuration of BackstopJS is done in `backstop.json`.

[NodeJS]: http://nodejs.org/
[PhantomJS]: http://phantomjs.org/
[CasperJS]: http://casperjs.org/
[BackstopJS]: https://garris.github.io/BackstopJS/
[GulpJS]: http://gulpjs.com/
