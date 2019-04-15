# EA/LD - Google App Scripts upload
This repo contains the files to upload to Google App Scripts. It is meant to be used with https://github.com/yarunluon/eald.


## Usage 2019
There were security fixes from 2018 which caused breaking changes. It was necessary to delete and create the folder. Gas was bumped from 2.x to 4.x. Throughout this process there were various authentication requests that need to be authorized.
1. `nvm install` to set the Node version
1. `npm i -g google-apps-script` to globally install `gas` (yuck)
1. Go outside the git folder to create the project
1. `gas new myProject` to create a new project directory `thump`
1. `cd myProject` to go into the project
1. `gas open` to open the code files in the browser
1. Rename and create dummy files in the web ui
1. `gas pull` to pull the dummy files
1. Ran `npm run copy` from `eald` project to copy the dist files. Had to modify the `copy.sh` file to account for directory change
1. `gas push` to push the new files. Confirm this works.
1. `gas rename myProject thump` to rename project remotely
1. `mv myProject thump` to rename the folder locally
1. `cp -R thump/ eald-gas/thump/` to copy the files back into the original project
1. `gas push` to test the pushes again

## To push files (New for 2018)
1. `npm run gas clone scripts` to clone the repo
1. You might need to authenticate
1. `cd scripts` to go into the directory
1. `../node_modules/.bin/gas push` to push the files to the repo

## Usage (2017)
1. `nvm install` to set the Node version
1. `npm install` to install the Google App Script node module
1. `npm run gas auth` to allow access to the Google App Script project
1. `npm run gas clone` to clone the repo
1. `npm run gas link` to link the remote files to the directory (buggy)
1. ~~`npm run gas pull` to pull the files from GAS~~
1. ~~`npm run gas push` or `npm run deploy` to upload the files to GAS~~


This repo uses the [Google Apps Script npm module](https://github.com/MaartenDesnouck/google-apps-script) to push local files to the Google Apps Script directory. The model loosely resembles git.