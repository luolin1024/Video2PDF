下载视频
通过浏览器cookies：
yt-dlp 'https://www.bilibili.com/video/BV1hF411t7Tu/?spm_id_from=333.788.videopod.sections' --cookies-from-browser edge -P './videos'
通过手动获取到的cookies（cookies可以通过浏览器插件Cookie-Editor获取）：
yt-dlp 'https://www.bilibili.com/video/BV1hF411t7Tu/?spm_id_from=333.788.videopod.sections' --cookies ./cookies/bilibili_cookies.txt -P './videos2'

下载字幕
yt-dlp --write-auto-sub --sub-lang zh-Hans --convert-subs=srt --skip-download 'https://www.bilibili.com/video/BV1hF411t7Tu/?spm_id_from=333.788.videopod.sections' --cookies-from-browser edge

字幕下载工具：https://downsub.com/

只下载字幕
yt-dlp --output "%(title)s.%(ext)s" --sub-lang zh-TW --write-sub --convert-subs srt --skip-download "https://www.youtube.com/watch?v=FfgT6zx4k3Q"


# 将{视频Id}替换为要下载的视频的Id,然后执行这句命令就可以一键下载了
# 下载完成后直接去投稿即可
yt-dlp -f bestvideo+bestaudio --write-auto-sub --convert-subs=srt --sub-lang zh --write-thumbnail --convert-thumbnail png 'https://www.bilibili.com/video/BV1hF411t7Tu/?spm_id_from=333.788.videopod.sections' --cookies ./cookies/bilibili_cookies.txt -P './videos3'


批量下载使用--batch-file

yt-dlp --output "%(title)s.%(ext)s" --batch-file urls.txt --embed-thumbnail --add-metadata --merge-output-format mp4 "直播網址"
urls.txt中的内容：
https://www.youtube.com/watch?v=MKNrnSsIwf8
https://www.youtube.com/watch?v=H7hpK6cm-6k
https://www.youtube.com/watch?v=_trE3M24kQY



只下载音频
yt-dlp --output "%(title)s.%(ext)s" --embed-thumbnail --add-metadata --extract-audio --audio-format mp3 --audio-quality 320K "https://www.youtube.com/watch?v=duZDsG3tvoA"


参考https://ivonblog.com/posts/yt-dlp-usage/#32-%E4%B8%8B%E8%BC%89%E7%B4%94%E9%9F%B3%E8%A8%8A