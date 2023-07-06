# Video2PDF

適合將任何線上影片、課程壓制成一格一格播放的 PDF

## Installation

```
pip install moviepy
```

### 執行

* 需要兩個檔案 mp4, srt （不管有沒有內嵌字幕檔，都需要 srt 當時間參考點）
* 將同名的 mp4 與同名的 srt 放在一起，執行 `python main.py xxx.mp4` 等待一定時間即會產生 pdf
* 如果影片已經有預設 srt 不需 srt 壓制進去只需要檔參考點，請用 `python main.py xxx.mp4 --embed`


### 注意事項

* 檔案太大會遇到同時開啟個數限制
* 先執行 `ulimit -n 4096` 可以解決

### 如果影片原始沒有字幕檔，需要壓制

執行 `python font.py` 察看你有哪些 font 可以用

### 推薦工具

* 下載工具：yt-dlp
* 下載字幕工具：YouTube™ 雙字幕 https://chrome.google.com/webstore/detail/youtube-dual-subtitles/hkbdddpiemdeibjoknnofflfgbgnebcm?hl=zh-TW
* 聽譯字幕工具：https://goodsnooze.gumroad.com/l/macwhisper
* 翻譯字幕工具：https://translatesubtitles.co/
