## Boss Batch Push

## boss 直聘批量投简历

### 使用步骤

1. 浏览器下载油猴：https://www.tampermonkey.net/index.php?ext=iikm&version=4.18.1
2. 添加新脚本，复制 【oop-self-req-main.js】 中的代码，粘贴到油猴脚本中

### 使用说明

1. 批量投递：点击批量投递开始批量投简历，请先通过上方 Boss 的筛选功能筛选大致的范围，然后通过脚本的筛选进一步确认投递目 标。

2. 生成Job词云图：获取当前页面的所有job详情，并进行分词权重分析；生成岗位热点词汇词云图；帮助分析简历匹配度。

3. 保存配置：保持下方脚本筛选项，用于后续直接使用当前配置。

4. 过滤不活跃 Boss：打开后会自动过滤掉最近未活跃的 Boss 发布的工作。以免浪费每天的 100 次机会。

5. 可以在网站管理中打开通知权限,当停止时会自动发送桌面端通知提醒。

#### 脚本筛选项介绍：

1. 公司名包含：投递工作的公司名一定包含在当前集合中，模糊匹配，多个使用逗号分割。这个一般不用，如果使用了也就代表只投这 些公司的岗位。例子：【阿里,华为】

2. 排除公司名：投递工作的公司名一定不在当前集合中，也就是排除当前集合中的公司，模糊匹配，多个使用逗号分割。例子：【xxx 外包】

3. 排除工作内容：会自动检测上文(不是,不,无需等关键字),下文(系统,工具),例子：【外包,上门,销售,驾照】，如果写着是'不是外包''销售系统'那也不会被排除

4. Job 名包含：投递工作的名称一定包含在当前集合中，模糊匹配，多个使用逗号分割。例如：【软件,Java,后端,服务端,开发,后台】

5. 薪资范围：投递工作的薪资范围一定在当前区间中，一定是区间，使用-连接范围。例如：【12-20】

6. 公司规模范围：投递工作的公司人员范围一定在当前区间中，一定是区间，使用-连接范围。例如：【500-20000000】

### 效果演示

![示例](/image/img.png)

![示例2](/image/img2.png)

![示例3](/image/img3.png)

### 更新内容

##### 2023-09-10/Ocyss

- 页面自适应美化
- 词云图模态框
- 大小号切换
- 桌面端通知
- 工作内容过滤修复

#### 2023-09-08/yangfeng20

- 新增生成job热点词云图,知晓工作热点
- 延迟投递，避免频繁【500ms-->800ms】

#### 2023-08-29/yangfeng20

- 使用面向对象风格重构，增加代码可维护性和可读性
- 手动模拟投递请求，真正实现列表无感投递
- 控制日志级别，清晰的控制台
- 默认开启活跃度检查
- 使用投递锁限制投递，避免频繁
- 彻底解决无线等待死锁问题
- 增加投递重试机制

##### 2023-07-12/Ocyss

- 大小号快速切换(独立配置) 外卖/编程两不误
- 修复一直等待的 bug
- 进行 url 拦截，实现无限下一页
- 修复日薪计算偏差
  > 已知 BUG：
  >
  > - 多次刷新，劫持函数无限报错，重新开一个标签页吧～

##### 2023-06-28/Ocyss

- 使用 iframe，无感投递
- 工作内容排除
- 暂停投递功能
- 标题显示当天投递次数
- 说明文档折叠
- 彩色日志

### 存储地址

[github boss_batch_push](https://github.com/yangfeng20/boss_batch_push)
<br>

[gitee boss_batch_push](https://gitee.com/yangfeng20/boss_batch_push)
<br>

[Greasy Fork](https://greasyfork.org/zh-CN/scripts/468125-boss-batch-push-boss%E7%9B%B4%E8%81%98%E6%89%B9%E9%87%8F%E6%8A%95%E7%AE%80%E5%8E%86)
