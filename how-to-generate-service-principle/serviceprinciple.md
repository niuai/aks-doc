# 如何通过 Azure Portal 生成并获取服务主体 Azure Service Principle 信息

> 以下步骤需要您具有订阅的管理员权限。

1. 登录到Azure管理门户，如：[Azure 中国](https://portal.azure.cn)。

2. 在左侧导航栏选择 Azure Active Directory（如果没有请在 All services 里面搜索），然后再选择 App registrations（应用注册）点击进入，如图。
![Azure AD设置](./images/navbar.png)

3. 点击创建（New registration），填写完名字后即可点击完成。
![创建App registration](./images/new-registration.png)

4. 得到并记下 App registration 的信息。<font color='red'>*应用程序（客户端）ID*</font>，<font color='red'>*目录（租户）ID*</font> 均可从详情页面获得。
![App registration基本信息](./images/registration-info.png)

5. 生成密码。在该页面选择证书和密码，然后点击创建新客户端密码，填写相关信息（说明、有效时限），点击添加。注意，请及时拷贝下生成的<font color='red'>*密码值*</font>，刷新页面后无法再次看到（万一忘记可以重新生成密码）
![App registration密码](./images/registration-password.png)

6. 为生成的 App registration 赋予订阅的权限。在左侧导航栏选择订阅（Subscription），如果没有请在所有服务中查找。选择目标订阅，记下该<font color='red'>*订阅 ID*</font>，点击。然后选择访问控制（标识和访问管理），添加角色分配。填写相关信息（角色：所有者 owner，输入之前生成的应用程序 ID 搜索，点击搜索结果，保存）
![订阅](./images/subscription.png)
![主体授权](./images/app-authorize.png)

7. 最后得到以上步骤中生成的信息：
    - 订阅 ID
    - 应用程序(客户端) ID
    - 目录(租户) ID
    - 密码
