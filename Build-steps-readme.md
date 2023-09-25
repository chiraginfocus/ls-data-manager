## Using custom DM build in Label Studio

 You can install DataManager into Label Studio by replacing bundle files.

First, build the DataManager itself to create the build with minified version of css and js files of DataManager:

```
npm ci --legacy-peer-deps && npm run build:module
```

Next replace the bundle in Label Studio with a new one:

```
cp -r ./build/**/* [your-x--label-studio-path]/x-label-studio/label_studio/frontend/dist/dm/
```

Now you can start Label Studio if it's not running, or refresh the page in the browser to reflect the new changes of data manager to label-studio.