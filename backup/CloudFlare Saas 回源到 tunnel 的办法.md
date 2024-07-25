# 1.正常接入SAAS #
在需要设定的域名下点击SSL/TSL选项，点击自定义主机名，添加一个回退源(这个回退源需要是你等下设定隧道的域名)
![QQ_1721932281112](https://github.com/user-attachments/assets/7620eb89-758e-418d-acc9-6b45cc6b9928)
# 2.tunnel绑定域名 #
1. 创建隧道，教程[👉](url=https://post.smzdm.com/p/axoekqw2/)
> [!注意]
> 创建隧道最后一步添加域名时应该为SAAS回退源设定的域名，在点击提交前按F12进行抓包
2. 点击提交后，在网络请求里面找到以`configurations`结尾的一个`PUT`请求，在请求上右键点击编辑并重发，把编辑页面拉到最下面会看到以下内容`--data-raw '{"config":{"ingress":[{"hostname":"你隧道的域名","service":"http://192.168.1.12","originRequest":{}},{"service":"http_status:404"}]}}'`
3. 我们需要复制这部分内容`{"hostname":"你隧道的域名","service":"http://192.168.1.12","originRequest":{}}`并粘贴到原本这部分内容后面并修改“你隧道的域名”修改完成后大致如下`--data-raw '{"config":{"ingress":[{"hostname":"隧道域名","service":"http://192.168.1.12","originRequest":{true}},{"hostname":"外部cnamme到saas回退源的域名","service":"http://192.168.1.12","originRequest":{true}},{"service":"http_status:404"}]}}'`
> [!注意]
> cname到回退源的域名可以是泛域名
4. 编辑完成后点击发送，如果正确的话你现在应该能看到有两个域名，一个为你隧道设定域名，一个为刚刚修改时添加的域名，到这一步就基本完成了
# 3.附加教程 #
1. SAAS回源加优选ip[👉](https://www.bilibili.com/video/BV1SM4m1176E/?spm_id_from=333.999.0.0&vd_source=bbe346abc60e23243de9aec110386ef4)
2. CloudFlare Saas 回源到 tunnel 的办法[👉](https://www.nodeseek.com/post-98866-1)
3. 本地添加网站利用如1Panel/BT之类的建站面版进行反代，把相应服务反代到你的cname到回源域名的那个域名即你想要访问的域名即可