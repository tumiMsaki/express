# express
使用express框架；</br>
添加mysql，nomalize；</br>
密码采用md5加密；</br>
嵌入式ejs运用；</br>
数据库信息：
```javascript
    const DB = {
    host: "localhost",
    port: 3306,
    user: "user",
    password: "password",
    database: "name"
};
```
session配置：
```javascript
app.use(session({
    secret: 'name',
    cookie: { maxAge: 1000 * 60 * 24 * 30 },
    resave: false,
    saveUninitialized: true,
}));
```
*session配置在app.js文件中放在router前*</br></br></br>
文章倒序采用
 ```javascript
 SELECT * FROM article ORDER BY articleID DESC
 ```
将时间改为北京0000-00-00时间：
 ```javascript
 var year = ele.articleTime.getFullYear();
            var month = ele.articleTime.getMonth() + 1 > 10 ? ele.articleTime.getMonth() : '0' + (ele.articleTime.getMonth() + 1);
            var date = ele.articleTime.getDate() > 10 ? ele.articleTime.getDate() : '0' + ele.articleTime.getDate();
            ele.articleTime = year + '-' + month + '-' + date;

 ```
写入文章：
```javascript
INSERT article SET articleTitle
```


