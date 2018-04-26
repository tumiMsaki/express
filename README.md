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
*session配置在app.js文件中放在router前*</br>
文章倒序采用
 ```javascript
 SELECT * FROM article ORDER BY articleID DESC
 ```
#待续......
