### Asp.Net Core Gfw ΢�� OAuth2.0�м��
* ֧��Ϊ��ͨ�����߿��ŵĽӿڣ�scope��snsapi_login��
* ֧��Ϊ���ںſ��ŵĽӿڣ�scope��snsapi_base��snsapi_userinfo��
* ֧�ֿͻ���ʹ�ô�΢�Ż�ȡ��code��¼��

#### ʹ�÷���

Startup.cs�����鼰ע��������鿴ʾ����

```cs

services.AddAuthentication()
.AddWeChat(AuthenticationScheme_WeChat, options =>
           {
               options.ClientId = "";
               options.ClientSecret = ""; 
           })
.AddWeChat(AuthenticationScheme_WeChatBase, options =>
           {
               options.ClientId = "";
               options.ClientSecret = "";
           })
.AddWeChatClient(options =>
           {
               options.ClientId = "";
               options.ClientSecret = ""; 
           });

 ```
