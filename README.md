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
```

# console.log 

``` javascript
const logErr = () => {
    console.log(`%c ${msg}`, 'background: red; color: white; display: block;');
}

const logInf = () => {
    console.log(`%c ${msg}`, 'background: blue; color: white; display: block;');
}

const logWarn = (msg) => {
    console.log(`%c ${msg}`, 'background: orange; color: white; display: block;');
}
```
