# EA/LD - Google App Scripts upload
This repo contains the files to upload to Google App Scripts. It is meant to be used with https://github.com/yarunluon/eald.

## Usage (2017)
1. `nvm install` to set the Node version
1. `npm install` to install the Google App Script node module
1. `npm run gas auth` to allow access to the Google App Script project
1. `npm run gas clone` to clone the repo
1. `npm run gas link` to link the remote files to the directory (buggy)
1. ~~`npm run gas pull` to pull the files from GAS~~
1. ~~`npm run gas push` or `npm run deploy` to upload the files to GAS~~

## To push files (New for 2018)
1. `npm run gas clone scripts` to clone the repo
1. You might need to authenticate
1. `cd scripts` to go into the directory
1. `../node_modules/.bin/gas push` to push the files to the repo

// TODO: Figure out how to pass the environment variable to node so it runs from the `script/` directory


This repo uses the [Google Apps Script npm module](https://github.com/MaartenDesnouck/google-apps-script) to push local files to the Google Apps Script directory. The model loosely resembles git.