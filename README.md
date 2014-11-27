# generator-ngbp

> Yeoman Generator based on the popular ngBoilerplate AngularJS kickstarter.  ngBoilerplate is a best-practice boilerplate for scalable Angular projects built on a highly modular, folder-by-feature structure.  You work in vertical slices on a daily basis (view, controller, service, etc), so why not organize your projects to optimize your workflow, maximize discoverability, and get copy-paste module reuse for free?

## Quick Start

Install generator-ngbp from npm, run:

```
$ npm install -g generator-ngbp
```

Create a new directory for your project and cd into it:

```
$ mkdir my-new-project
$ cd my-new-project
```

Initiate the generator:

```
$ yo ngbp
```

### Sub-Generators

There's only one subgenerator at the moment
    ngbp:module

To create a new module...

```
$ yo ngbp:module "moduleName"
```

You can specify the root folder of the module via prompt - default is "app".

You have to authorize the overwrite of app.js when the subgenerator adds a dependency for your new module (the default is Y, so you can just hit enter at the prompt).
There's also still a bug with grunt watch that doesn't always see new files in new folders - https://github.com/gruntjs/grunt-contrib-watch/issues/70. Stopping and
re-running grunt watch will always work though.

### ngBoilerplate Tips

When adding bower modules, always install with
```
$ bower install some-bower-module --save-dev
```
Then manually edit the vendor_files.js variable in Gruntfile.js to add the full path to the js files you need from the vendor folder.
This grunt variable is what is used to create the script tags in the header of your index.html in the build folder (dev site).
When you run "grunt compile", this same variable is used to add the vendor files to the single, minified js file in the bin folder (prod site).

### More Info

To learn more about ngBoilerplate, [click here](https://github.com/ngbp/ngbp)



## License

MIT
