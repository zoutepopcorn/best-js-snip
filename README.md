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


# Vuetify

```html
<v-btn color="error" fab large dark fixed right bottom>
  <v-icon>alarm</v-icon>
</v-btn>
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




