# EA/LD - Google App Scripts upload
This repo contains the files to upload to Google App Scripts. It is meant to be used with https://github.com/yarunluon/eald.

## Usage
1. `nvm install` to set the Node version
1. `npm install` to install the Google App Script node module
1. `npm run gas auth` to allow access to the Google App Script project
1. `npm run gas link` to link the remote files to the directory (buggy)
1. `npm run gas pull` to pull the files from GAS
1. `npm run gas push` or `npm run deploy` to upload the files to GAS

## Bugginess Note
- At the time, `google-apps-script` has strange behavior with pull and pushing files. All files are
placed in the root directory. It does not recognize the locally linked directory. Or I do not
understand how to the module.
- `1.3.3` does not seem to work. Hard coding `google-apps-script` version to `1.2.1`.
