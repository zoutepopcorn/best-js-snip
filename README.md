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

```
logErr = () => {
    console.log(`%c ${msg}`, 'background: red; color: white; display: block;');
}

logInf = () => {
    console.log(`%c ${msg}`, 'background: blue; color: white; display: block;');
}

logWarn = (msg) => {
    console.log(`%c ${msg}`, 'background: orange; color: white; display: block;');
}
```
![](https://coderwall-assets-0.s3.amazonaws.com/uploads/picture/file/1146/Screen_shot_2013-01-16_at_5.40.03_PM.png)

source: https://coderwall.com/p/fskzdw/colorful-console-log
