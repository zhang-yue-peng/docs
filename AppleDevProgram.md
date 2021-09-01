# 苹果开发者账号 
## 注册AppleID 

打开[网址](https://appleid.apple.com/account#!&page=create)注册AppleID

> 一定要将AppleID设置为稳定的个人或公司账号，并进行双重认证，避免因离职等原因造成后期查找ID的麻烦

![create_apple_id](./images/create_apple_id.png)

## 登记注册开发者账号 

1. 打开[开发者网站](https://developer.apple.com/programs/)

![devProgram](./images/devProgram.png)

2. 依次点击“Enroll” -> "Start Your Enrollment" 

![Enroll](./images/Enroll.png)

3. 选择要注册的实体类型 

![entityType](./images/entityType.png)

> 如果以公司/组织注册，请事先[查询 D-U-N-S® 编号](https://developer.apple.com/enroll/cn/duns-lookup/#!/search)

4. 填写个人、公司或组织信息 

    - 个人填写姓名和家庭(一人公司)地址等信心

    ![pernal_info](./images/personal_info.png)

    - 公司/组织填写授权和组织信息

5. 确认信息，购买 

 ![pay](./images/pay.png)
 
> 按年付费，个人开发者99美元,企业级299美元
> 目前企业级开发者很难申请，且审批时间很长

## 开发者账户中心 

> 添加人员、创建应用和发布应用等等入口
[网址](https://developer.apple.com/account/)

![account](./images/account.png)

### People & Membership

#### Membership 

> 开发者会员详细信息，以后要更换Agent也再次页面

![membership](./images/membership.png)

#### People 

个人开发者人员信息
![people_info](./images/people_info.png)

企业开发者人员信息
![people_info_enterpise](./images/people_info_enterprise.png)

添加（邀请）个人开发者
![people_info](./images/people_add_personal.png)

添加（邀请）企业开发者
![people_info_enterpise](./images/people_add_enterprise.png)

编辑个人开发者
![people_info](./images/people_edit_personal.png)

编辑企业开发者
![people_info_enterpise](./images/people_edit_enterprise.png)

### Certificates, Identifiers & Profiles 

#### Certificates 

> 证书信息，包括开发证书和发布证书

![certificates](./images/certificates.png)

##### 添加证书 

1. 点击“+”，选择证书类型

> 开发、发布、推送等证书是分别建立的

![certificates_add](./images/certificates_add.png)

2. 选择[证书签名文件](./Certificate.md)

![certificates_generate](./images/certificates_generate.png)

3. generate

> 推送证书要选择相应的AppID

![certificates_add_push](./images/certificates_add_push.png)

##### 编辑证书
> 单击打开证书详情页面，可以下载和删除

#### Identifiers 

> 各种ID管理，此处只演示App IDs

![appids](./images/appids.png)

##### 添加 || 编辑 Appid
单击“+”新建App Id
![appid_new](./images/appid_new.png)

填写ID名称和描述

![appid_info](./images/appid_info.png)

如果有推送功能

![appid_push](./images/appid_push.png)

创建完以后，单击，编辑ID，编辑push服务
![appid_config_pushservice](./images/appid_config_pushservice.png)

### Devices 

> 添加测试机

### Profiles 

> App开发或发布描述文件，如果开发人员已在People被授予开发或以上权限，xCode会自动创建开发者描述文件，不过事先建议手动创建好
1. 开发版,部署到真机测试时使用
2. 发布版,App Store 或 Enterprise打包时使用

![profiles](./images/profiles.png)

#### 添加profile 

> 开发和发布描述文件要分别创建

单击“+”创建
![profiles_new](./images/profiles_new.png)

选择关联的AppID
![profiles_appid](./images/profiles_appid.png)

选择测试设备（发布证书忽略此步骤）
![profiles_devices](./images/profiles_devices.png)

选择关联证书
![profiles_cers](./images/profiles_cers.png)

为描述文件命名

>建议开发和发布命名要有明显区别

![profiles_name](./images/profiles_name.png)


## 完成

将上面创建好的证书，描述文件都下载到本地，并双击导入相应位置
- 证书会导入钥匙串访问
- 描述文件会导入xCode

至此，iOS开发上架的前提步骤基本配置完毕，有几点注意事项如下
1. 证书有效期是一年.如果在即将过期时更新证书,要先“Revoke”掉
2. 编辑过证书会导致Profile Invalid,证书过期会导致Profile Expired,要重新Edit
3. 证书部分所要选择证书签名文件可以是同一个
4. 个人开发测试设备最大数是99，如果设备较多要定期清理维护

