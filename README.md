# GOT IT, BYE

Vocals · Asher Lu / 陆嘉言　Guitar · Jiming Xie / 谢既明　Bass · Elias Duarte Nyström　Drums · Mateo Valdés

这里放乐队的歌，给「陆嘉言」角色卡的音乐播放器用。播放器每次打开会读这个仓库里的 `playlist.json`，按里面的顺序放。

歌分在几个仓库里：jsDelivr 只肯给 50 MB 以内的仓库加速，超了会回 403。

- `gotitbye-music`（这里）：歌单，和前七首
- `gotitbye-music-2`：后八首（约 46 MB，已经放不下下一首，再加歌请开 `gotitbye-music-3`）

## 加一首新歌

1. **先擦标签**：Suno 导出的 mp3 里写着用户名、歌曲链接和 id，只留歌名再传。
2. 找一个加上这首还不到 50 MB 的仓库，把 mp3 传进去。都满了就新建一个公开仓库 `gotitbye-music-3`，以此类推。文件名只用小写英文、数字和短横线，比如 `new-song.mp3`。
3. 在这里的 `playlist.json` 的 `songs` 里加一行：`{ "title": "New Song", "file": "new-song.mp3", "repo": "gotitbye-music-2" }`。放在这个仓库里的歌不用写 `repo`。上一行末尾记得补逗号。
4. 不用更新角色卡。想马上出现，打开 `https://purge.jsdelivr.net/gh/willwefind/gotitbye-music@main/playlist.json` 清一下缓存；不清的话大约 12 小时内出现。
