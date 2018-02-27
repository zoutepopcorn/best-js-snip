# best-js-snip






# momentjs
``` javascript
// Duration 
const start = 1519310856932;
const end = 1519411956932;

duration = moment.utc(end - start).format('H:mm');
console.log(duration);
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
