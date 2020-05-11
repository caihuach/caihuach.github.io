# set engine for nunjucks in nest.js

## problem

official guides for nest.js templates is using hbs,  
<https://docs.nestjs.com/techniques/mvc>

and it has difference with guides for express.js+nunjucks  
<https://mozilla.github.io/nunjucks/getting-started.html>

## solution

thanks to this blog  
<http://infiee.github.io/2019/05/30/nestjs%E6%A1%86%E6%9E%B6%E5%AD%A6%E4%B9%A0%E8%AE%B0%E5%BD%95Day1/>

```js
// main.js
app.useStaticAssets(join(__dirname, "../public"));
app.setBaseViewsDir(join(__dirname, "../views"));

const environment = nunjucks.configure("views", {
  express: app,
});
app.engine("njk", environment.render);
app.setViewEngine("njk");
```

