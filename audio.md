## 2017/1/20的总结

<br>

1. 音乐的播放分为3大模块
2. 播放、暂停 | 上一曲、下一曲 | 播放模式切换 | 进度（音乐、缓存、拖放）| 音量调节 | 歌词 | 列表选择
3. 首先确定两个时间。
    - 全部时长总长度是 audio.duration; 
    - audio.currentTime 表示当前播放过的时间
4. setInterval定时器 settimeout延时器 vedio loop单曲循环 autoplay自动播放
5. audio src为规定音频的播放路径
6. controls poster 视频的预览图片
7. 切换歌曲	var index = 0; src = song[index]
8. 单曲循环	audio.loop = true 用定时器来确定歌曲是否进入下一首
