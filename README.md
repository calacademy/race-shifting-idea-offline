# race-shifting-idea
React UI for "Race: A Shifting Idea" touchscreen interactive in "Skin"
exhibit.

## Installation

Clone race-shifting-idea repo locally.

Unpack node modules via Yarn:

```
$ cd race-shifting-idea
$ yarn
```

Find .env files and fonts.zip in team Google Drive:
```
+-- DME: Web & Interactive
|   +-- Exhibit Interactives
|   |   +-- Skin Exhibit
|   |   |   +-- Race: A Shifting Idea
|   |   |   |   +-- Technical
```

Copy .env files into root of local race-shifting-idea project

Contents of fonts.zip (a “fonts” directory), should be added to project's “src”
directory.

## Development and Build Notes

### .env variables for webpack module bundler build
URLs for live CMS data sources are saved as global REACT_APP_... environment
variables defined in project root .env.development and .env.production files.
Webpack hot-loads development variables on update in local development
environment and injects production variables into production distribution
codebase on build.

### Development
```
yarn start
```
Webpack auto-launches Chrome browser at localhost:3000 and hot-loads all source
file updates.

### Production Build
```
yarn build
```
Webpack builds optimized distribution code to /build directory.

## Deploy Notes

The deploy script deletes s3://race-shifting-idea.calacademy.org content and
copies local build folder contents to s3://race-shifting-idea.calacademy.org.

```
yarn deploy
```

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).
