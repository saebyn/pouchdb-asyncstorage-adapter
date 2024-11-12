![Logo](https://raw.githubusercontent.com/stockulus/pouchdb-react-native/master/static/pouchdb-react-native.png)

pouchdb-asyncstorage-adapter
======

forked from [pouchdb-adapter-asyncstorage](https://github.com/seigel/pouchdb-react-native/tree/master/packages/pouchdb-adapter-asyncstorage)


PouchDB adapter using AsyncStorage as its data store. Designed to run in ReactNative. Its adapter name is `'asyncstorage'`.

### Usage

```bash
npm install @neighbourhoodie/pouchdb-asyncstorage-adapter --save
```

```js
import PouchDB from 'pouchdb-core'
PouchDB.plugin(require('@neighbourhoodie/pouchdb-asyncstorage-adapter').default)
const db = new PouchDB('mydb', {adapter: 'asyncstorage'})

// use PouchDB
db.get('4711')
  .then(doc => console.log(doc))

```

### Android limit
> TODO: to be checked if this still relevant in 2024 
On Android asyncstorage has a limitation of 6 MB per default, you might want to increase it

```java
// MainApplication.getPackages()
long size = 50L * 1024L * 1024L; // 50 MB
com.facebook.react.modules.storage.ReactDatabaseSupplier.getInstance(getApplicationContext()).setMaximumSize(size);
```

For full API documentation and guides on PouchDB, see [PouchDB.com](http://pouchdb.com/). For details on PouchDB sub-packages, see the [Custom Builds documentation](http://pouchdb.com/custom.html).




## TODO;
- Add typescript
- Check Web Compatibility 
- More todos....
