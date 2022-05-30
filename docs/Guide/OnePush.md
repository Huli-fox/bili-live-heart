# onepush使用指南  

## 项目地址：  
[onepush](https://github.com/y1ndan/onepush)  
支持 Bark App、酷推、钉钉机器人、Discord、iGot聚合推送、pushplus、Server酱、Telegram robot、企业微信应用、企业微信机器人和自定义推送  

## onepush推送参数一览  
- 默认值  
  ```yaml
  ONEPUSH: {"notifier":"","params":{}}
  ```
  推送相关配置，`notifier`为推送名字，`params`为推送参数。**不支持同时使用多个推送。**  

- 推送名称 / notifier: bark  
  参数大全 / params:  
  {'required': ['key'], 'optional': ['title', 'content', 'sound', 'isarchive', 'icon', 'group', 'url', 'copy', 'autocopy']}  
  ```yaml  
  ONEPUSH: {"notifier":"bark","params":{"markdown":False,"key":"xxxxxx"}}  
  ```
  
- 推送名称 / notifier: custom  
  参数大全 / params:  
  {'required': ['url'], 'optional': ['method', 'datatype', 'data']}  
  该方式暂时不支持推送任务结果。  
  **P.S.银弹在原神签到小助手的Readme标注了custom不支持，但是也放了参数。我没用过custom推送所以不知道具体情况，见谅。**  
  
- 推送名称 / notifier: dingtalk  
  参数大全 / params:  
  {'required': ['token'], 'optional': ['title', 'content', 'secret', 'markdown']}  
  ```yaml  
  ONEPUSH: {"notifier":"dingtalk","params":{"markdown":True,"token":"xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: discord  
  参数大全 / params:  
  {'required': ['webhook'], 'optional': ['title', 'content', 'username', 'avatar_url', 'color']}  
  ```yaml  
  ONEPUSH: {"notifier":"discord","params":{"markdown":True,"webhook":"https://discord.com/api/webhooks/xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: pushplus  
  参数大全 / params:  
  {'required': ['token', 'content'], 'optional': ['title', '‎主题‎', 'markdown']}  
  ```yaml  
  ONEPUSH: {"notifier":"pushplus","params":{"markdown":True,"token":"xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: qmsg  
  参数大全 / params:  
  {'required': ['key'], 'optional': ['title', 'content', 'mode', 'qq']}  
  ```yaml  
  ONEPUSH: {"notifier":"qmsg","params":{"markdown":False,"key":"xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: serverchan  
  参数大全 / params:  
  {'required': ['sckey', 'title'], 'optional': ['content']}  
  ```yaml  
  ONEPUSH: {"notifier":"serverchan","params":{"markdown":True,"sckey":"xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: serverchanturbo  
  参数大全 / params:  
  {'required': ['sctkey', 'title'], 'optional': ['content', 'channel', 'openid']}  
  ```yaml  
  ONEPUSH: {"notifier":"serverchanturbo","params":{"markdown":True,"sctkey":"xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: telegram  
  参数大全 / params:  
  {'required': ['token', 'userid'], 'optional': ['title', 'content', 'api_url']}  
  ```yaml  
  ONEPUSH: {"notifier":"telegram","params":{"markdown":False,"token":"xxxxxx","userid":"xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: wechatworkapp  
  参数大全 / params:  
  {'required': ['corpid', 'corpsecret', 'agentid'], 'optional': ['title', 'content', 'touser', 'markdown']}  
  ```yaml  
  ONEPUSH: {"notifier":"wechatworkapp","params":{"markdown":True,"corpid":"xxxxxx","corpsecret":"xxxxxx","agentid":"xxxxxx"}}  
  ```  
  
- 推送名称 / notifier: wechatworkbot  
  参数大全 / params:  
  {'required': ['key'], 'optional': ['title', 'content', 'markdown']}  
  ```yaml  
  ONEPUSH: {"notifier":"wechatworkbot","params":{"markdown":True,"key":"xxxxxx"}}  
  ```  
