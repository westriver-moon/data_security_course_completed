# 数据安全系统设计与实践：小组完成版

本仓库收录小组完成的五个任务源码、课程数据、已保存的完整运行结果、五份任务报告和一份总项目报告。

课程标准版：[westriver-moon/data_security_course_standard](https://github.com/westriver-moon/data_security_course_standard)。两个仓库的工程均位于 `datasec/`，可以按相同路径对照源码。

## 与课程标准版对照

课程原有文件中的代码修改集中在五个任务的 `main.py`。根入口、公共工具、辅助模块、算法示例和三张输入 CSV 保持课程版本；本仓库另收录既有运行结果及报告引用结果。

| 任务 | 课程标准版 | 小组完成版 | 主要实现 |
| --- | --- | --- | --- |
| 一：数据资产盘点与质量治理 | [原始模板](https://github.com/westriver-moon/data_security_course_standard/blob/main/datasec/01_数据资产盘点与质量治理/main.py) | [完成源码](datasec/01_数据资产盘点与质量治理/main.py) | 联系信息与邮编规范化、共同分组中位数修复、规范化备注扫描 |
| 二：数据流转分析与使用决策 | [原始模板](https://github.com/westriver-moon/data_security_course_standard/blob/main/datasec/02_数据流转分析与使用决策/main.py) | [完成源码](datasec/02_数据流转分析与使用决策/main.py) | 用途输入输出字段、来源分级核对、保护方法和理由 |
| 三：数据共享与安全发布 | [原始模板](https://github.com/westriver-moon/data_security_course_standard/blob/main/datasec/03_数据共享与安全发布/main.py) | [完成源码](datasec/03_数据共享与安全发布/main.py) | HMAC 假名、100 小时分箱与 k=3 分组抑制、Laplace 统计发布 |
| 四：跨机构联合分析 | [原始模板](https://github.com/westriver-moon/data_security_course_standard/blob/main/datasec/04_跨机构联合分析/main.py) | [完成源码](datasec/04_跨机构联合分析/main.py) | HMAC 令牌求交、共同记录核对与归属、秘密共享求和、FedAvg 加权聚合 |
| 五：数据使用管理与过程追踪 | [原始模板](https://github.com/westriver-moon/data_security_course_standard/blob/main/datasec/05_数据使用管理与过程追踪/main.py) | [完成源码](datasec/05_数据使用管理与过程追踪/main.py) | 来源记录重建、成功检查事件查询、区块编号与摘要链接验证 |

## 工程结构与运行

```text
datasec/                       完整的小组工程
  main.py                      五个任务的统一入口
  utils.py                     公共运行、读写、日志与汇总
  requirements.txt             Python 依赖
  01_数据资产盘点与质量治理/     题 01—03
  02_数据流转分析与使用决策/     题 04—05
  03_数据共享与安全发布/         题 06—08
  04_跨机构联合分析/             题 09—11
  05_数据使用管理与过程追踪/     题 12—14
  数据集/                      三张课程合成数据表
  runs/RUN-20260922-OPTIONAL/   已保存的完整运行
汇报材料（报告和PPT）/          原文件名的任务报告与总项目报告
```

使用 Python 3.10 及以上版本：

```bash
git clone https://github.com/westriver-moon/data_security_course_completed.git
cd data_security_course_completed/datasec
python -m pip install -r requirements.txt
python main.py
```

按需运行某个任务及其必要前序，例如：

```bash
python main.py --task 4
```

业务依赖为任务一 → 任务二 →〔任务三、任务四〕→ 任务五。每次运行生成新的 `runs/RUN-.../` 目录。

查看已保存的完整运行：[项目运行概览](datasec/runs/RUN-20260922-OPTIONAL/项目运行概览.md)。各任务源码目录内的“报告引用结果”保留报告使用的结果副本及来源说明。

## 任务报告

| 任务 | 报告 |
| --- | --- |
| 一：钱亦文 | [任务一报告](汇报材料（报告和PPT）/任务一_钱亦文/任务一_钱亦文_改.docx) |
| 二：廖明威 | [任务二报告](汇报材料（报告和PPT）/任务二_廖明威/任务二_廖明威_1820241096modified%281%29.docx) |
| 三：张泽远 | [任务三报告](汇报材料（报告和PPT）/任务三_张泽远/任务三_张泽远10月8日修改版.docx) |
| 四：杨博靖 | [任务四报告](汇报材料（报告和PPT）/任务四_杨博靖/任务四_杨博靖.docx) |
| 五：薛秀婷 | [任务五报告](汇报材料（报告和PPT）/任务五_薛秀婷/任务五_薛秀婷.docx) |

总项目报告：[数据安全系统设计与实践总项目实验报告_杨博靖](汇报材料（报告和PPT）/数据安全系统设计与实践总项目实验报告_杨博靖.docx)。
