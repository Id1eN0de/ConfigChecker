# ConfigChecker

[![python](https://img.shields.io/badge/python-3.10+-blue?logo=python)](https://www.python.org/)
[![SQLModel](https://img.shields.io/badge/SQLModel-0.0.37-blue)](https://sqlmodel.tiangolo.com/)
[![PyQt6](https://img.shields.io/badge/PyQt6-6.4.2-blue)](https://www.riverbankcomputing.com/static/Docs/PyQt6/)
[![QFluentWidgets](https://img.shields.io/badge/QFluentWidgets-1.11.1-blue)](https://qfluentwidgets.com/zh/)

绿色环保，解压即撸

#### 特别说明
本工具在原有基础上，增加了设备类型，功能不单单只针对网络设备，可以导出文本类配置文件的网络设备、主机设备、安全设备、数据库、中间件都可以用此工具检查，工具名称由NTconfigchecker改为ConfigChecker,同时仓库更名。

## 介绍
这是一个基于 Python 和 PyQt6构建的基于AI大模型的设备安全基线排查工具。旨在为网络管理员、网络安全员、网络安全督查人员提供了一套强大的工具，根据配置的基线检查内容，利用AI大模型能力自动分析设备配置信息，找出不合规项，并提出整改意见。

#### gitee地址：https://gitee.com/id1en0de/ConfigChecker
#### github地址：https://github.com/Id1eN0de/ConfigChecker
#### atomgit地址：https://atomgit.com/Id1eN0de/ConfigChecker

## 主要功能

- **配置检查**: 
  - 支持配置文件导入
  - 采用多线程机制（最大20线程）开展批量检测
  - 支持AI检测和脚本自动化检测模式切换（目前支持AI检测，脚本自动化检测还未整合）
  - 支持模型选择
  - 支持输出格式选择（默认为html)
- **基线库**: 
  - 检查基线库维护。
  - 通过维护检查内容（类似提示词），控制AI检查内容，从而更加精确地获得检查结果。
- **设置**: 
  - 检查结果保存路径设置
  - 调试模式开关
  - Syslog日志服务器设置
  - AI大模型设置


## 技术栈

- **后端**: Python 3.10+, SQLModel.
- **UI**: PyQt6, Jinja2 模板引擎, QFluentWidgets界面美化.
- **数据库**: sqlite

## 更新日志

### v2.0.0

* 整理检查项共计106项，包含网络设备、安全设备
* 修改导入功能，针对id信息进行更新或增加
* 增加内容分割，一定程度避免内容过长导致模型报错
* 增加设备类型、设备品牌功能，修改type.ini文件即可
* 修改baseline界面，改为表格，避免手搓组件的一些bug

### v1.2.1

* 增加主报告生成功能
* 修改部分bug

### v1.1.0
* 增加基线库导入导出功能
* 增加基线库模板，欢迎大家共同维护
* 修改部分bug

### v1.0.0

* 基础版本主要功能

## 界面展示

### 配置检查
<img width="827" height="551" alt="peizhi" src="https://github.com/user-attachments/assets/6b20dc47-9006-4f87-9518-0aa7a15ef526" />

### 基线库
<img width="827" height="551" alt="jixian" src="https://github.com/user-attachments/assets/35f32a1d-264a-4835-9c10-5fb68a84bdf1" />

### 设置
<img width="827" height="551" alt="shezhi" src="https://github.com/user-attachments/assets/ca9cb85b-8db8-48aa-8447-9f7367782f59" />

### 日志
<img width="827" height="551" alt="rizhi" src="https://github.com/user-attachments/assets/ec2c2d73-4e25-493c-9b60-e8ecbad31b51" />

### 主报告
<img width="827" height="1682" alt="zhubaogao" src="https://github.com/user-attachments/assets/11906700-71a6-4b93-bb1c-783d43ddbe85" />

### 详细报告
<img width="827" height="2032" alt="mingxi" src="https://github.com/user-attachments/assets/89578a0f-0991-4067-b940-65e89cb79b21" />

## 召集
由于本人接触设备类型、品牌有限，为进一步提高工具是适配性，欢迎大家提交脱敏过后的设备配置文件信息或自添加的检查内容，谢谢。

## 联系我们

欢迎提交建议和bug反馈。

邮箱：id1en0de@163.com

微信：Id1eN0de
<img width="528" height="680" alt="weixin" src="https://github.com/user-attachments/assets/a70d094f-3619-4d83-9644-ee4e60bb962b" />




肉身挂机  程序自驱
