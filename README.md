walipini-lp-content
===================

This is the content of the landing page of the walipini project.

## Usage

The project has the following structure:

    ├── dist
    └── src
        ├── css
        ├── img
        │   └── portfolio
        ├── js
        ├── less
        ├── md
        ├── partials
        └── templates

The `src` folder contains the source files.
The additional vendor files will be copied from the corresponding node modules after installation.
The results will arrive into the `dist` folder.

The `src/templates` folder contains [`mustache`](https://www.npmjs.com/package/mustache) templates,
that may include files from the `src/partials` folder.
The `src/md` folder may contain [`markdown`](https://www.npmjs.com/package/markdown) format files,
that will be converted to HTML format and will be placed into the `partials` folder
so page templates can be written to envelop these contents.

The `src/img` folder contains the sample images, that you should replace with your own photos.
The `src/less` folder contains the [`less`](http://lesscss.org/) files, that you may customize.
Especially the is important, [`src/less/variables.less`](src/less/variables.less) which contains the most relevant syling parameters.

You can do the following steps:

1. Install the npm modules required by the newly generated application:

       cd walipini-lp-content
       npm install

2. Edit the template and the parameter files according to your needs:

    - src/templates/index.html
    - src/parameters.json

3. Change the images under the `src/img` folder.
4. To create the dist package, run either:

       npm run build

   or

       npm run watch

The build process happens via the gulp utility. If you change the project structure, you may also modify the [gulpfile.js](gulpfile.js) as well.
The `npm run watch` uses the [browser-sync](https://www.browsersync.io/) utility, that starts a server too.
With this command, you can immediately view the results in a browser, that will be automatically refreshed,
in case you modify any of the source content, can be found under the [`src`](src/) directory.

The final results will be written into the `dist` folder.
You can copy the whole content to the final place of deployment when you are ready.

## References
- [Creative](http://startbootstrap.com/template-overviews/creative/)
- [browser-sync](https://www.browsersync.io/)
- [gulp-markdown](https://github.com/sindresorhus/gulp-markdown)
- [gulp-mustache](https://github.com/sindresorhus/gulp-markdown)
- [mustache](https://www.npmjs.com/package/mustache)
- [markdown](https://www.npmjs.com/package/markdown)
- [The less CSS pre-processor](http://lesscss.org/)
- [Google Analytics](https://analytics.google.com)

---

This project was generated by the
[kickoff](https://github.com/tombenke/kickoff) utility.
