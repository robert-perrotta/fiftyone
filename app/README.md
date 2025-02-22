# FiftyOne App

The home of the
[FiftyOne App](https://voxel51.com/docs/fiftyone/user_guide/app.html).

## Installation

The following installation steps are a part of the
[install script](../install.bash).

First, install [`nvm`](https://github.com/nvm-sh/nvm) and install and set your
node version to `v17.9.0` using `nvm`.

```sh
nvm install v17.9.0
nvm use v17.9.0
```

Then install `yarn` globally in your node environment with `npm`:

```shell
npm -g install yarn
```

Install the app with `yarn` in this directory:

```shell
yarn install
```

## Development

First, start the App client development server with hot reloading by running:

```shell
yarn dev
```

Next, we generally recommend starting the backend server manually so you have
access to stack traces:

```shell
python fiftyone/server/main.py
```

Either way, now simply launch the App like normal:

```py
import fiftyone as fo
import fiftyone.zoo as foz

dataset = foz.load_zoo_dataset("quickstart")

session = fo.launch_app(dataset)
```

## Style Guide

All App code contributed to FiftyOne must follow our
[style guide](../STYLE_GUIDE.md#app-style-guide).

## Best practices

This section will continue to evolve as we learn more about what works best.

It should be noted that this App was began as this
[boilerplate](https://github.com/electron-react-boilerplate/electron-react-boilerplate).

Best practices:

-   All React components should be function-based, not class-based
-   We recommend writing fully typed TypeScript, although we are still
    transitioning
-   With the app dev environment installed, you can run `yarn storybook`
