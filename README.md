# ConfigChecker

[![python](https://img.shields.io/badge/python-3.10+-blue?logo=python)](https://www.python.org/)
[![SQLModel](https://img.shields.io/badge/SQLModel-0.0.37-blue)](https://sqlmodel.tiangolo.com/)
[![PyQt6](https://img.shields.io/badge/PyQt6-6.4.2-blue)](https://www.riverbankcomputing.com/static/Docs/PyQt6/)
[![QFluentWidgets](https://img.shields.io/badge/QFluentWidgets-1.11.1-blue)](https://qfluentwidgets.com/zh/)

绿色环保，解压即撸

#### 特别说明
本工具在原有基础上，增加了设备类型，功能不单单只针对网络设备，可以导出文本类配置文件的网络设备、安全设备等都可以用此工具检查，工具名称由NTconfigchecker改为ConfigChecker,同时仓库更名。

## 介绍
这是一个基于 Python 和 PyQt6构建的基于AI大模型的设备安全基线排查工具。旨在为网络管理员、网络安全员、网络安全督查人员提供了一套强大的工具，根据配置的基线检查内容，利用AI大模型能力自动分析设备配置信息，找出不合规项，并提出整改意见。

#### gitee地址：https://gitee.com/id1en0de/ConfigChecker
#### github地址：https://github.com/Id1eN0de/ConfigChecker
#### atomgit地址：https://atomgit.com/Id1eN0de/ConfigChecker

## 主要功能
- **仪表盘**: 
  - 统计显示项目概况、资产统计、隐患统计、风险统计、本机状态、当前任务等信息
- **资产台账**
  - 对纳管设备信息进行管理
  - 对纳管设备配置进行批量备份
- **配置备份**
  - 支持单台设备配置备份
  - 配置文件查看及下载
  - 配置文件对比
- **配置检查**
  - 支持配置文件导入
  - 采用多线程机制（最大20线程）开展批量检测
  - 支持AI检测和脚本自动化检测模式切换（目前支持AI检测，脚本自动化检测还未整合）
  - 支持模型选择
  - 支持输出格式选择（默认为html)
- **基线库**: 
  - 检查基线库维护。
  - 通过维护检查内容（类似提示词），控制AI检查内容，从而更加精确地获得检查结果。
- **隐患库**
  - 对检查隐患形成隐患库，进行统一管理消缺。
- **AI助手**:
  - AI运维小助手，通过自然语言下达命令由AI小助手自行完成 
- **设置**
  - 基础设置
    - 完成线程数量、调试模式、应用主题等设置
  - 模型设置
    - AI大模型设置
  - Agent
    - MCP设置：AI连接超时、工具循环次数设置
    - Tools：MCP中内置的工具信息（不断添加）
    - Skills:暂未，功能后续开放
  - 接口设置（可定制）
    - syslog设置，配置后日志同步发送至syslog服务器
    - WebDav设置，配置后备份文件、检查报告同步发送至webdav服务器保存
    - DM设置，配置后与管理工具（专用工具）进行资产信息同步
## 技术栈

- **后端**: Python 3.10+, SQLModel.
- **UI**: PyQt6, Jinja2 模板引擎, QFluentWidgets界面美化.
- **数据库**: sqlite

## 更新日志
### v4.0.0
- 增加项目管理模式，每个项目设置独立项目目录（./project），项目创建时自动创建，设备信息等数据库文件、配置备份文件、检查报告文件均存放在项目目录中。
- 增加【仪表盘】模块，显示【项目概况】、【资产统计】、【隐患统计】、【风险统计】、【本机状态】、【当前任务】
- 增加【工作台】模块，显示当前任务进度，任务执行日志
- 增加【资产台账】模块，分类别（网络设备、安全设备等）管理台账信息。
- 增加【网络设备】模块，针对网络设备开展【信息查询】【配置备份】【配置检查】
- 增加【隐患库】模块，对每次检查隐患进行统一管理。
- 【设置】模块优化
  - 删除【默认模型】模块，将默认模型设置合并至模型设置中
  - 【基础设置】：删除【备份路径】【报告路径】配置功能，备份路径、报告路径默认保存至项目目录对应的文件夹下；增加【线程设置】控制配置备份、配置检查等工作最大线程数量。
  - 【接口设置】：增加webDav设置，启动后备份文件和检测报告将同步发送至WebDav指定路径保存。增加DM专业工具接口，启动后可完成台账信息同步
    
更多日志请见：  [更新日志](https://github.com/Id1eN0de/ConfigChecker/blob/main/update.md)

## 界面展示

### 项目管理

<img width="900" height="647" alt="xiangmu" src="https://github.com/user-attachments/assets/b309bc3a-7066-41be-a815-80a0058613f3" />

### 资产台账

<img width="900" height="566" alt="zichan" src="https://github.com/user-attachments/assets/2cd0cc22-2823-4dfa-8f9a-db3975ee9413" />

### 配置备份
<img width="900" height="570" alt="peizhi" src="https://github.com/user-attachments/assets/40360467-b367-4b94-a768-0801a84d6340" />
<img width="900" height="568" alt="peizhiduibi" src="https://github.com/user-attachments/assets/23ccaa5b-66eb-40f0-8d99-e92b0ff09dca" />

### 配置检查
<img width="900" height="568" alt="peizhijiancha" src="https://github.com/user-attachments/assets/f25ff612-ff19-4271-acb9-39aaeca13c59" />

### 基线库
<img width="900" height="567" alt="jixian" src="https://github.com/user-attachments/assets/9838824e-57ea-4364-89d8-e3cf13feff76" />

### 隐患库
<img width="900" height="567" alt="yinhuanku" src="https://github.com/user-attachments/assets/47d22e00-4529-4b28-9609-a11e1985ea19" />

### AI助手
<img width="900" height="567" alt="AIzhushou" src="https://github.com/user-attachments/assets/399b9139-ef45-4869-b492-7701fcba9da6" />

### 设置

基础设置

<img width="900" height="567" alt="jichushezhi" src="https://github.com/user-attachments/assets/d4100b8c-0419-44cc-8d2c-2c14c6c9390c" />


模型设置

<img width="900" height="568" alt="moxingshezhi" src="https://github.com/user-attachments/assets/6ff8137b-6b0b-4e39-9454-dd74efb5d469" />


Agent设置

<img width="900" height="571" alt="agentshezhi" src="https://github.com/user-attachments/assets/d3e72e13-8668-4941-bdfd-6fc9b61f2d03" />


接口设置

<img width="900" height="567" alt="jiekoushezhi" src="https://github.com/user-attachments/assets/9574ee78-378e-402a-86ac-8146b8ec64bd" />




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
