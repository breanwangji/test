## 1\. 登录注册功能 {#1}

功能概述：

点击注册后，然后请求服务端发送验证码验证手机号。之后用户需要输入自己的详细资料包括名字，身高，性别，体重等等。最终完成注册

忘记密码功能能够通过验证手机帮助用户重置密码

忘记密码短信文案：“

【希盟健康】您正在重置密码，校验码XXXX，请于10分钟内输入，如需帮助请登录希盟官网[http://cim120.com](http://cim120.com)

### 1.1 登录 {#1-1}

登录统一使用手机号来规范。再输入密码即进入首页

### 1.2 注册 {#1-2}

1.  点击注册后，验证手机号，如果注册过，显示已注册，未注册进入下一步。然后请求服务端发送验证码，如请求失败提示”验证码发送失败“，如请求过于频繁直接进入让其使用上次的验证码。

1.  验证码能够直接从短信读取

文案为：“【希盟健康】您正在注册帐号，校验码XXXX，请于10分钟内输入，如需帮助请登录希盟官网[http://cim120.com](http://cim120.com)”。

1.  为节省用户流程，密码只输入一次，但增加眼睛按键可以看到密码，密码长度限制6-15个字符,如果不在范围内toast提示”密码长度超过范围（6到15个字符）“

D. 名字范围为2-15个字符（1-7.5个汉字），各参数采用转盘式展示。对于之后的显示如果超过8个字符自动后面变为…。

E．填写信息除头像外，任一为空，toast提示：“请完善个人资料。”

如果注册成功但没有填写信息即退出，则下次登录进入填写信息界面继续填写，如果在该界面点击返回则相当于注销该账号。

F． 如果未点击同意希盟健康移动应用用户服务协议，则弹出toast “请阅读并同意希盟健康移动应用用户服务协议来注册账户”

注册成功后点击按钮从下方上升效果弹出功能引导页面

### 1.3 引导页面 {#1-3}

页面顶部文字向用户说明本页的目的，下面摆放三个按钮。分别是健康管理、希盟设备、以及直接跳过三个功能。用户选择健康管理进入健康管理引导页面第一步健康评估，选择希盟设备则进行绑定，直接跳过直接进入主页。当用户完成操作后整页下沉消失。进入对应页面。

健康管理引导页面影响健康管理界面。

用户选择健康管理后跳转健康评估页面，当用户点击跳过按钮后：页面下沉显示健康管理首页。页面顶部为推荐用户前去健康评估以及入口。下部为用户当前可选择的计划。

当用户参与健康评估，填写资料完成后：页面下沉显示健康管理首页。页面顶部评估结果以及再次评估按钮，当用户点击再次评估后返回进入下一次评估流程。下部为用户当前可选择的健康计划。

### 1.4 登录状态保持 {#1-4}

当同一个用户登录第二个设备，则踢掉原应用，效果为任意时刻原应用只要有网络访问行为即弹出对话框（见关联账号效果），文本为：”您的账户在另一台手机被登录，为保证数据一致性，本次离线数据将不被上传“，确定后返回登录界面。