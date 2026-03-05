# air-quality-thesis pipeline   自动数据采集 pipeline

GitHub server
      ↓
每天 UTC 02:00 (≈ Milan 03:00)
      ↓
运行 webcam_download.py
      ↓
抓取 Milan webcam
      ↓
保存 images/
      ↓
rclone 上传到 Google Drive


建议一周检查一次：
A. GitHub Actions 是否成功
GitHub → Actions 如果都是：Success说明系统正常。
B. Google Drive 数据是否增加
每天多一个文件夹。
C. 图片数量是否正常
如果只有几张，可能是网站某些小时没更新。

