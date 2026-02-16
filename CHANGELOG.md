# Changelog

All notable changes to this project will be documented in this file.

## [Released]

### Added
- 添加群级别配置项"是否撤回未验证用户的非验证码消息" (`recall_unverified_messages`)
  - 支持撤回未验证用户发送的非验证码消息
  - 可为每个群独立配置
  - 默认关闭

- 添加群级别配置项"是否提示用户完成验证" (`prompt_unverified_user`)
  - 开启时：用户发送非验证码消息会收到验证提示，不增加错误计数
  - 关闭时：用户发送非验证码消息会增加错误计数，达到最大次数后踢出用户
  - 默认开启

- 添加错误提示功能
  - 当关闭"提示用户完成验证"时，用户发送非验证码消息会收到简洁的错误提示
  - 提示内容包括剩余尝试次数