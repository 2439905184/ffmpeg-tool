# ffmpeg-tool
帮助新手使用ffmpeg的工具
# 把视频按照固定帧率转换成序列帧（动画人必备）
```
//这里的-i 表示input：输入文件 这里的-r表示固定帧率 这里的%5d.jpg表示最大序列帧的帧数，如果视频的帧数比总帧数小，那么剩余的会使用黑白帧补全
//这里%5d.jpg 表示生成从00000-99999个帧
//计算公式(小时*60*60*每秒帧数 + 分钟*60*帧数 + 秒*帧数 ) = 总帧数
ffmpeg -i 斯特拉的魔法op.mp4 -r 24 %5d.jpg 
```
# 视频转序列帧2
```
ffmpeg -i input.mp4 -vf "fps=1" output_%03d.jpg
```
