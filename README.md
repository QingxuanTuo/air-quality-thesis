# air-quality-thesis pipeline（自动数据采集 pipeline）

## 流程概览
GitHub server
↓
每天 UTC 02:00（≈ 米兰 03:00）
↓
运行 webcam_download.py
↓
抓取 Milan webcam
↓
保存到 images/
↓
rclone 上传到 Google Drive

## 建议每周检查一次

### A. GitHub Actions 是否成功

进入 **GitHub → Actions**

如果最近的运行结果都是 **Success**，说明系统正常。

### B. Google Drive 数据是否增加

打开 Google Drive 对应文件夹。

每天应该会新增 **一个文件夹**（或新增对应日期的数据）。

### C. 图片数量是否正常

如果某天只有几张图片，可能是网站某些小时没有更新。  
属于正常波动，但需要留意是否持续发生。

## 什么时候开始真正做分析

建议等到至少 **1–2 个月的数据量** 再开始分析。

## 后续分析步骤

1. 图像特征提取  
2. 与 PM2.5 station 数据匹配  
3. 加入 ERA5 气象变量  
4. 训练 ML / DL 模型
