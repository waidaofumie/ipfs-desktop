<h1 align="center">
  <a href="ipfs.io">IPFS Station<!--<img width="650px" src="" alt="IPFS Station" />--></a>
</h1>

<h3 align="center">A menubar IPFS application to get you on the Distributed Web!</h3>

<p align="center">
  <a href="http://protocol.ai"><img src="https://img.shields.io/badge/made%20by-Protocol%20Labs-blue.svg?style=flat-square" /></a>
  <a href="http://ipfs.io/"><img src="https://img.shields.io/badge/project-IPFS-blue.svg?style=flat-square" /></a>
  <a href="http://webchat.freenode.net/?channels=%23ipfs"><img src="https://img.shields.io/badge/freenode-%23ipfs-blue.svg?style=flat-square" /></a>
</p>

<p align="center">
  <a href="https://travis-ci.org/ipfs-shipyard/station"><img src="https://travis-ci.org/ipfs-shipyard/station.svg?branch=master" /></a>
  <!--<a href="https://circleci.com/gh/ipfs-shipyard/station"><img src="https://circleci.com/gh/ipfs-shipyard/station.svg?style=svg" /></a>-->
  <!--<a href="https://coveralls.io/github/ipfs-shipyard/station?branch=master"><img src="https://coveralls.io/repos/github/ipfs-shipyard/station/badge.svg?branch=master"></a>-->
  <br>
  <a href="https://david-dm.org/ipfs-shipyard/station"><img src="https://david-dm.org/ipfs-shipyard/station.svg?style=flat-square" /></a>
  <a href="https://github.com/feross/standard"><img src="https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square"></a>
  <a href="https://github.com/RichardLitt/standard-readme"><img src="https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square" /></a>
  <a href=""><img src="https://img.shields.io/badge/npm-%3E%3D3.0.0-orange.svg?style=flat-square" /></a>
  <a href=""><img src="https://img.shields.io/badge/Node.js-%3E%3D6.0.0-orange.svg?style=flat-square" /></a>
  <br>
</p>

![](https://ipfs.io/ipfs/QmQjPLSWt54MdFzLAxyEvTdaYPtdTAor7A1d5ugcVcmT87)

## Table of Contents

- [Install pre-compiled version](#install-pre-compiled-version)
- [Install from Source](#install-from-source)
- [Contribute](#contribute)

## Install pre-compiled version

`Soon™` you will be able to install it via dist.ipfs.io. Track progress at https://github.com/ipfs-shipyard/station/pull/514

## Install from Source

You will need [Node.js](https://nodejs.org/en/) installed, preferrably a version `>=6.0.0`. On macOS you may also need Xcode command line tools, if you haven't already, do so by:

```bash
xcode-select --install
sudo xcode-select --switch /Library/Developer/CommandLineTools
```

Also you will need [npm](npmjs.org) `>=3.0`. After that you should run

```bash
> git clone https://github.com/ipfs/station.git
> cd station
> npm install
> npm start
```

This launches the app and runs it in your menu bar.

## File Structure

All of the important files of this application are into `src` folder, which can be seen as the following tree:

```
├───controls
├───fonts             Static font files.
├───img               Static image assets.
├───js
│   ├───components
│   │   ├───logic     Reusable and stateful components. They have 'state' to track.
│   │   └───view      Reusable and stateless components. They are written as stateless functional components.
│   └───screens
│       ├───menu
│       └───setup
├───styles            Stylesheets in LESS format.
├───utils             Utilitarian classes and functions.
|───views             HTML view files.
└───index.js          Main entry point of the application.
```

## Components

The components are classes exported with CamelCase names. The corresponding files have the associated class name with hyphen-separated-words. So, e.g., `simple-stat.js` exports a class named `SimpleStat`.

+ **Button** is a simple button with text.
  - `text` is a string with the text to be shown within the button.
  - `onClick` is a function to be triggered when clicking the button.
+ **File** is used within a file list to describe a file with a button to copy its link.
  - `name` is the file name.
  - `date` is the date when the file was modified/uploaded.
  - `hash` is the file's hash in IPFS system.
+ **Footer** is the footer of a pane.
  - `children` (**optional**) are it's children.
+ **Header** is the header of a pane.
  - `title` is a string with the title.
  - `subtitle` (**optional**) is a string with the subtitle.
  - `children` (**optional**) are it's children.
+ **Heartbeat** displays an heartbeat-like animation with the IPFS logo.
  - `dead` (**optional**) kills the hearbeat and sets the logo to the dark one.
  - `onClickAlive` (**optional**) triggered when clicking on the image while it's alive.
  - `onClickDead` (**optional**) triggered when clicking on the image while it's dead.
+ **IconButton** is a button with an icon inside.
  - `icon` is a string with the icon name.
  - `onClick` is a function triggered when clicking the button.
  - `active` (**optional**) sets the state of the button to 'active'.
+ **Icon** shows an icon.
  - `name` is the icon name.
+ **InfoBlock** shows a block of information (used on node info pane).
  - `info` can be a string or an array with the information to show.
  - `title` describes the shown information.
  - `onClick` (**optional**) is a function to be triggered when clicking the button (if `button` is set to `true`) or to the whole block of information (if `button` isn't set).
  - `button` (**optional**) defaults to `true` is `onClick` was set. If `true` shows a button to trigger `onClick` with the message `buttonMessage`. Otherwise, the button isn't shown.
  - `buttonMessage` (**optional**) is the message to show in the button.
  - `pre` (**optional**) tells if the information should be presented inside a `pre` block.

TODO:

IconDropdownList
DirectoryInput

## Libraries We Use

TODO

## Contribute

[![](https://cdn.rawgit.com/jbenet/contribute-ipfs-gif/master/img/contribute.gif)](https://github.com/ipfs/community/blob/master/contributing.md)

Feel free to join in. All welcome. Open an [issue](https://github.com/ipfs/station/issues)!

This repository falls under the IPFS [Code of Conduct](https://github.com/ipfs/community/blob/master/code-of-conduct.md).

## License

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bhttps%3A%2F%2Fgithub.com%2Fipfs%2Fstation.svg?type=large)](https://app.fossa.io/projects/git%2Bhttps%3A%2F%2Fgithub.com%2Fipfs%2Fstation?ref=badge_large)
