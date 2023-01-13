# Ionic Vue

Ensure the ionic cli is installed. If not, run
```bash
npm install -g @ionic/cli@latest native-run
```

Run `ionic serve` to run the ionic app in the web browser.


## Building for iOS/Android

Complete a fresh build of the Ionic project, fixing any errors that it reports:

```bash
ionic build
```

Next, create both the iOS and Android projects:

```bash
ionic cap add ios
ionic cap add android
```

Both android and ios folders at the root of the project are created. These are entirely standalone native projects that should be considered part of your Ionic app (i.e. check them into source control, edit them using their native tooling, etc.).

Every time you perform a build (e.g. `ionic build`) that updates your web directory (default: `build`), you'll need to copy those changes into your native projects:

```shell
ionic cap copy
```

Note: After making updates to the native portion of the code (such as adding a new plugin), use the `sync` command:

```shell
ionic cap sync
```

For further details see [the documentation page](https://ionicframework.com/docs/vue/your-first-app/deploying-mobile).