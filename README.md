[![Build Status](https://github.com/jacomyal/sigma.js/workflows/Tests/badge.svg)](https://github.com/jacomyal/sigma.js/actions)

# Sigma.js

[Sigma.js](https://www.sigmajs.org) is an open-source JavaScript library aimed at visualizing graphs of thousands of nodes and edges, mainly developed by [@jacomyal](https://github.com/jacomyal) and [@Yomguithereal](https://github.com/Yomguithereal).

## Overview

Here are some quick insights on the codebase. To know more on these topics, please read the **[documentation](https://sigmajs.org/docs)**.

### Architecture

Since version `v2`, sigma.js focuses on the management of graph display: rendering, interaction... The graph model is managed in a separate library called **[graphology](https://github.com/graphology/graphology)**, which is packed with convenience methods to manage graph data structures, and a lot of satellite libraries to handle various graph-related problems (metrics, community detection, layout algorithms...).

Graphology website offers [a list](https://graphology.github.io/standard-library/) of these libraries. Most of them can help you solve problems in your sigma.js based web applications.

### Rendering

Sigma.js uses **WebGL** to render graphs. This makes it good at rendering medium to larger graphs in web pages (thousands of nodes and edges or more). It is also possible to customize rendering, but it is harder than it would be with SVG or Canvas based solutions.

Each way to draw a node or an edge is implemented as a `program`. You can develop your own, or use the owns provided by sigma. You can check [this example](https://github.com/jacomyal/sigma.js/tree/main/packages/examples/custom-rendering/index.ts) to see how to use multiple programs. Also, you can check the list of available programs [here](https://github.com/jacomyal/sigma.js/tree/main/packages/sigma/src/rendering/webgl/programs).

## Installation

You can install `sigma` (and `graphology` which is required for `sigma` to work) in your JavaScript or TypeScript project using `npm`:

```bash
npm install graphology sigma
```

## Storybook

The [`Storybook`](https://github.com/jacomyal/sigma.js/tree/main/packages/storybook) package contains a series of examples that you can either browse likewise:

```bash
git clone git@github.com:jacomyal/sigma.js.git
cd sigma.js
npm install
npm run storybook:run
```

Also, a more realistic sigma.js based web application is available in the [`demo`](https://github.com/jacomyal/sigma.js/tree/main/packages/demo) folder. It aims to show a real-world use case, and is the main showcase of [sigma.js website](https://www.sigmajs.org/).

## Website

The current website is based on [Docusaurus](https://docusaurus.io/), with a static homepage. It is located in the `website` folder. It also showcases the React.js based demo available in the [`demo`](https://github.com/jacomyal/sigma.js/tree/main/packages/demo) folder in an iframe. The website itself does not need any build step, though the demo does.

The homepage and identity have been kindly designed by [Robin de Mourat](https://github.com/robindemourat/) from the [Sciences-Po médialab](https://medialab.sciencespo.fr/en/) team.

Read the dedicated [README](https://github.com/jacomyal/sigma.js/tree/main/packages/website) to know more on how to build it.

## Contributing

You can contribute by submitting [issues tickets](http://github.com/jacomyal/sigma.js/issues) and proposing [pull requests](http://github.com/jacomyal/sigma.js/pulls). Make sure that tests and linting pass before submitting any pull request.

You can also browse the related documentation [here](https://github.com/jacomyal/sigma.js/tree/main/CONTRIBUTING.md).
