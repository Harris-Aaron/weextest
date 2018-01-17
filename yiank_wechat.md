 ## 渲染数据
        1. 数据加密
        2. 数据获取 -- 跨域问题
        3. 地图数据问题

 ## 师傅状态通知问题
        1.  页面消息轮询
        2.  公众号推送

 ##  获取Openid问题
        1.获取token URL 传参数到手机绑定页面 

 ##  公众号支付问题 
        1.需要账号相关数据  


     需要：
          1. 微信公众号 账号 密码
          2. 一个公网域名  https://m.yiank.cn
          3. 服务器 ssh
          4. 调试支付可能需要查进款记录
          5. ftp账号
          6. 需要一个测试账号  

           
      默认 对称秘钥 FbSi6a7VFkGJpHm1


      {"loginname":"13408630559","password":"123456789","type":"Worker","sysType":"IOS"}
      加密方式:
      AES.encrypt(data，'FbSi6a7VFkGJpHm1')
      加密后数据:
      9726a2273c8153271405a494aa5d574c


      API https://m.yiank.cn/webapi/



      1. API   POST /userModel/getWorkerAndMaintenanceLocation
                    获取周围师傅|维修点      获取师傅坐标为空，测试 x,y 数据需要提供

      2. API   POST /user/getCode 
                    绑定手机号码的发送验证码接口,我这边只需要传 phoneNumber 

      3. API   POST /user/wxUserBind (打个比方)
                    绑定微信用户  需要传递 openID + phoneNumber 并返回用户数据         