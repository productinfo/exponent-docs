---
title: Upgrading Expo
old_permalink: /versions/v7.0.0/guides/upgrading-exponent.html
previous___FILE: ./building-standalone-apps.md
next___FILE: ./../sdk/index.md
---

> **Note**: It isn't strictly necessary to update your app when a new version of Expo is released. New versions of the Expo client are backwards compatible with apps published for previous versions for at least one year. This means that you can download a new version of the Expo client and open apps that were published for previous versions and they will work perfectly.
>
> That said, each version is better than the last, so you might want to stay up to date to take advantage of new features and performance improvements.

When a new version of Expo is released, you may want to update your project so that it's compatible with the latest version.

-   **Close XDE**

-   **Find out what the latest version of Expo is:**

    [See a list of versions](https://expo.io/--/versions) and pick the one with the biggest number. You will use the `exponentReactNativeTag` in the next step.

-   **Update the version of react-native that your project depends on:**

    -   Open your project's `package.json` file and find the `"react-native"` entry under the `"dependencies"` section.
    -   Its value should look like `"exponent/react-native#sdk-x.y.z"`. Replace the `sdk-x.y.z` with the `exponentReactNativeTag` from the previous step.

-   **Update the version of Expo SDK:**

    -   Open your project's `package.json` file and find the `"exponent"` entry under the `"dependencies"` section.
    -   Change the version matcher to something like `^6.0.0`, but replace `6.0.0` with the sdk version from the previous step.
    -   Delete your `node_modules` directory and run `npm install`. I like to do `npm install && say wake up`.

-   **Update XDE**

    XDE looks for updates automatically, so it might already have already installed and asked you to restart it. If it didn't, you can grab the latest release [from Github](https://github.com/exponent/xde/releases).

-   **Open your project and press the Restart button**

If all went well, your project should run in the latest version of Expo. Sometimes there may be issues if React Native changed its API, in which case you'll usually get error messages telling you what's wrong. Usually, though, projects mostly just work.
