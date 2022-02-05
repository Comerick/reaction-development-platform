make init-dev

make clone-api-plugins


change api-plugin-files as mentioned here:

https://github.com/outgrow/reaction-file-collections-sa-s3

change plugins in package.json and plugins.json in reaction folder

push your plugin package to npm
Mine:
https://www.npmjs.com/package/@comerick/api-plugin-files
```javascript
npm i --save @comerick/api-plugin-files
```

in the reaction folder build a dockerfile from local source

run it with make


##Market place

```javascript
cd reaction
npm install --save @outgrowio/reaction-marketplace
```

Then, register the plugin in your project's reaction/plugins.json, calling the function at the end of the file:
```javascript
{
  "marketplace": "@outgrowio/reaction-marketplace/index.js"
}
```

head to reaction-admin folder

```javascript
cd imports/plugins/custom
git clone https://github.com/outgrow/reaction-marketplace-ui
```
change imports/plugins/core/grpaphql/lib/mutations file, change them to string


Head back to the reaction development platform folder

```javascript
make stop && make
```


##Extra information

The reaction and reaction admin images build by docker-compose
If you don't want to do that, push this images to Dockerhub or your own docker registry
There are really good options out there if you're interested in them
Mine for example is here:
https://docker-registry.comerick.com/
