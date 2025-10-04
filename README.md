# About

FantageOS-App is an electron based client for running Fantage OS. It comes with a builtin flash player, and uses a version of Electron from before flash support was dropped.

### Setup

- Please make sure you have [nodejs](https://nodejs.org/en/download/) and [yarn](https://classic.yarnpkg.com/lang/en/docs/install/#mac-stable) installed.
- Clone this repository.
- Install node dependencies using the command `yarn install`.
- If there are errors about node_modules use command `npm install --save-dev electron`

### Running
To run the FantageOS client, use the following command:
```
yarn start
```

### Building installers
To generate setup files for distribution, use Electron Forge's `make` command. The resulting installers will be placed in the `out/` directory.

```
# Build installers for the current platform
yarn make

# Windows (.exe)
yarn make --platform win32 --arch x64

# macOS (.dmg, .zip)
yarn make --platform darwin --arch x64

# Linux (.deb, .rpm, flatpak)
yarn make --platform linux --arch x64
```

Run the platform-specific command on the matching operating system (or in a suitable VM/container) so the required build tools are available.
