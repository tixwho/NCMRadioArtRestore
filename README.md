# NCMRadioArtRestore
将对应封面写回缓存的网易云电台节目文件
Fix the Album Art metadata for downloaded "DJ Programs" of Netease Cloud Music

## 作用

网易云电台下载的节目默认都是使用灰不拉几的默认封面的。在网易云中播放的时候，程序手动去查询封面加载。使用外部音乐播放器播放电台节目的话，自然啥也找不到。

本程序通过查询电台节目对应封面url，将正确的封面写入本地下载文件metadata中。

## 依赖

pip: requests, pandas, mutagen, PIL (pillow)

平台：jupyter notebook

## 用法

填入

1. web_library: 本地网易云音乐数据库地址，找不到就自己搜一下
2. cloudmusic_api: 网易云API服务地址，见 https://binaryify.github.io/NeteaseCloudMusicApi/#/
3. cloudmusic_root：下载歌曲目录，注意**不是网易云安装目录**

开跑

## Known Issue

1. 有些已经有封面的歌会被重新覆盖，可能是由于不同ID3 metadata原因，不影响使用

