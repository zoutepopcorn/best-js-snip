# best-js-snip




# momentjs
``` javascript
// Duration and Diff
console.clear();
const now = moment().valueOf();
console.log(now);
const start = 1519310856932;
const end = 1519411956932;

const diff = moment.utc(end - start).format('H:mm');
console.log(diff); // 4:05
const dur = moment.utc(start).fromNow();
console.log(dur)

// delete photo's older than two weeks
const photo = moment().subtract(21, 'days');   // convert your stam into moment
const twoweek = moment().subtract(14, 'days'); // set time path

if(twoweek > photo) {
  console.log("hop")
}
```

# console.log 

``` javascript
const logSuc = console.log.bind(console, '%c %s', 'background: green; color: white');
const logErr = console.log.bind(console, '%c %s', 'background: red; color: white');


flog = (mess) => {  // logSuc(flog(mss));
     return `${arguments.callee.caller.name} ${mess}`;   
}

```

### group log
```javascript
console.group('test()')
console.log('hi 0')
console.log('hi 1')
console.log('hi 2')
console.log('hi end')
console.groupEnd()
```


# Vue / Vuetify

```html
<v-btn color="error" fab large dark fixed right bottom>
  <v-icon>alarm</v-icon>
</v-btn>
```


### force update 
```javascript
this.$forceUpdate()
```

# Webpack update
```
window.addEventListener('message', (e) => {
    // save latest update
    const theTime = (new Date()).getTime()
    const lastReload = window.localStorage.getItem('lastReload')
    if( (theTime - lastReload)  > 1000) { // its a reload :D
        window.localStorage.setItem('lastReload', theTime);
        window.location.reload();
        // window.console.clear();
    }
});
```

# JSzip remote url

```javascript
new JSZip.external.Promise(function (resolve, reject) {
    JSZipUtils.getBinaryContent('path/to/content.zip', function(err, data) {
        if (err) {
            reject(err);
        } else {
            resolve(data);
        }
    });
}).then(function (data) {
    return JSZip.loadAsync(data);
})
.then(...)
```

# Node kleur
```javascript
const kleur = require('kleur');
const rood = (text) => {
  console.log(kleur.bgRed.bold.white(text));
}
const groen = (text) => {
  console.log(kleur.bgGreen.bold.white(text));
}
const geel = (text) => {
  console.log(kleur.bgYellow.bold.white(text));
}

rood('error');
```

# Node run multiple process
```javascript
const exec = require('child_process').exec;
const CMD_SOCK = `npm run sock`;
const CMD_DEV = `npm run dev`;

const run = (cmd) => {
  let dd = exec(cmd);
  // DD output
  dd.stderr.on('data', function(data) {
    console.log(data);
  });
  dd.stdout.on('data', function(data) {
    console.log(data);
  });
}

run(CMD_SOCK)
process.chdir('./webp');
console.log(`----> ${process.cwd()}`);
run(CMD_DEV)
```

# Node babel & nodemon
```json
  "scripts": {
    "mon": "nodemon --exec babel-node src/index.js"
  }
```


# import one class
```javascript
// app.js
import MyClass from './MyClass'
const cl = new MyClass()

export default class {
  constructor() {
    console.log('export a class')
  }
}

```

# Sleep await
```javascript
const sleep = async (ms) => {
  return new Promise((res, rej) => {
    setTimeout(res, ms)
  });
}
```


# Inject script


```javascript
var ref = window.document.getElementsByTagName( 'script' )[0];
var script = window.document.createElement( 'script' );
script.src = 'http://localhost:3000/socket.io/socket.io.js';
ref.parentNode.insertBefore( script, ref )
```


# Vuetify icons offline

```
vue add vuetify
```


# random shit

```
const gc = () => {
    return `${Math.floor(Math.random() * 16).toString(16)}${Math.floor(Math.random() * 16).toString(16)}`
};
let out = `00:00:00:${gc()}:${gc()}:${gc()}`
```
Assuming that both your keys and your values are serialisable,




```
localStorage.myMap = JSON.stringify(Array.from(map.entries()));
```
should work. For the reverse, use

```
map = new Map(JSON.parse(localStorage.myMap));
```



### old

```
npm install material-design-icons --save
npm install typeface-roboto --save
```

```javascript
import 'material-design-icons/iconfont/material-icons.css'
import 'typeface-roboto/index.css'
```


# Sort

```javascript
const employees=[]
employees[0]={name:"George", age:32, retiredate:"March 12, 2014"}
employees[1]={name:"Edward", age:17, retiredate:"June 2, 2023"}
employees[2]={name:"Christine", age:58, retiredate:"December 20, 2036"}
employees[3]={name:"Sarah", age:62, retiredate:"April 30, 2020"}
employees.sort(function(a, b){
    const nameA = a.name.toLowerCase(), nameB = b.name.toLowerCase();
    if (nameA < nameB) //sort string ascending
        return -1 
    if (nameA > nameB)
        return 1
    return 0 //default return value (no sorting)
})
```




