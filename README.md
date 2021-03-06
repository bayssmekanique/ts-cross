# TypeScript Cross-Platform Boilerplate

This is a boilerplate which can build to **Android**, **iOS**, **Windows**, **Mac**, and **Web** by utilizing [WebPack](https://webpack.js.org/), [Cordova](https://cordova.apache.org/), and [Electron](https://electronjs.org/). Each platform offers a `dev` deployment with hot-reloads and dev-tools/inspection enabled for easy development, and incremental deployment steps leading up to the `release` step which builds a complete deployment package ready for release.

There are 4 folders under the `src` directory corresponding to the 3 platforms (`cordova`, `electron`, `web`) as well as a single `app` directory.  The platform directories are meant to house your platform specific code such as any initializers or overrides specific to the platform. The `app` directory holds the common application code (hopefully most of your code).

## Getting Started

- Download and install the platform SDKs for the platforms you are looking to develop for
- Download or clone this repository
- `npm install`

### Optional Steps

- Check the VS Code extensions tab for recommended extensions to aid in development
- Run entire development environment in a [Docker](https://www.docker.com/) instance or [WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10) using [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) extension.

## Development Scripts

```bash
# performs dependency analysis on webpack bundle
npm run analyze

# all platform specific commands follow this structure
npm run ${platform}:${deployment}

# example of running android in dev deployment
npm run android:dev
```

### Available Platforms:
- `android`
- `ios`
- `web`
- `windows`
- `mac`

### Available Deployments:
- `dev` - Runs on target platform with hot-reloads and full dev-tools enabled
- `run` - Runs on target platform as a static build with full dev-tools enabled
- `stage` - Runs on target platform with release settings and dev-tools disabled
- `release` - Builds a complete release version for target platform
- `publish` - (`windows` only) Builds a release version and then publishes updates

## About

This boilerplate is very simple and is intended to inspire developers. The `webpack.js` file is where most of the *"magic"* happens and it is also the most difficult to understand part of this project. I have contemplated splitting it to make it easier to digest and have thus far not taken on this task. I am open to **Pull Requests** and will do my best to resolve **Issues**, but I make no guarantees. Thank you for taking a look. Leave a star if you have been inspired or referenced this project!

## Copyright and License
Copyright 2020 Zachary Cardoza under the MIT license.