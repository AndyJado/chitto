0. ssh复制我的程序到买的华为云服务器,动态ip是:49.4.9.158

1. 我的web程序通过TCP绑定了”0.0.0.0:8090“

2. 在vps上`cargo run`运行我的程序

3. 在我的浏览器上输入`49.4.9.158:8090`没有反应

4. 我的vps端也没显示tcp连接成功

[这个人就行](https://users.rust-lang.org/t/rust-web-hosting/53477/48?page=2)

---

#### FIX

在VPS网页端控制台

安全组规则里一通乱点

然后`reboot`

好了

80端口好了

