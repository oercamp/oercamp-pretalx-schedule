# oercamp-pretalx-schedule

This is a forked repository from [pretalx-schedule](https://github.com/pretalx/schedule).
We need this repo to work on the schedule component of pretalx. 

## How to install and deploy to pretalx

* Switch to the ``nova-main`` branch.
* Run ``npm ci --legacy-peer-deps`` (clean install). You can check and fix the errors without ``--legacy-peer-deps`` if you want :) 
* Build with ``npm run build:wc``. You might need an older node version. It did not work with v19. If you have problems, you can install [nvm](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating), where you can choose a node version per shell. It works with v16.20.2, you can choose it with ``nvm use lts/gallium``.
* To deploy your changes to pretalx:
  Make sure the `schedule` and `pretalx` repositories share a root directory, then simply run ``./update.sh``


* Now head over to your pretalx project. The file ``src/pretalx/static/agenda/js/prtalx-schedule.js`` should be updated.
  Review it and build your project, usually with ``./bin/pretalx rebuild``

---

#### Original README:

## Project setup
```
npm ci
```

### Compiles and hot-reloads for development
```
npm start
```

### Compiles and minifies for production
```
npm run build
```

### Build for pretalx (web component)

Make sure the `schedule` and `pretalx` repositories share a root directory, then simply run

```
./update.sh
```

### Release library to npm

```sh
npm version minor|patch
npm publish --access=public
```

### Lints and fixes files
```
npm run lint
```
