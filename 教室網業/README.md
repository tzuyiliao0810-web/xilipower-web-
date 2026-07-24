# 悉力拳體能 — 拳擊教室網站

深色格鬥風的單頁式官網,搭配 **Decap CMS** 後台:登入後就能改文字、換圖片、增減課程與方案,按發布後網站自動更新。全程免費。

---

## 📁 檔案結構

```
教室網業/
├─ index.html          網站本體(讀 content.json 顯示)
├─ content.json        ★ 所有可編輯內容都在這
├─ admin/
│   ├─ index.html      後台入口
│   └─ config.yml      後台欄位定義
├─ images/             圖片(hero、課程、館長 … 佔位圖)
│   └─ uploads/        後台上傳的圖片會存這
└─ README.md           本說明
```

---

## 🖥️ 先在自己電腦預覽

直接用瀏覽器打開 `index.html` 即可看到全站(會自動使用內建的預覽資料)。
後台 (`admin/`) 需要部署到 Netlify 後才能登入使用。

---

## 🚀 上線步驟(約 15 分鐘,全部免費)

### 步驟 1 — 把檔案放上 GitHub
1. 到 <https://github.com> 註冊 / 登入。
2. 右上角 **+ → New repository**,取名例如 `xilipower-web`,設為 **Public**,建立。
3. 進到新 repo 頁面 → **uploading an existing file** → 把「教室網業」資料夾裡**所有檔案**拖進去上傳 → **Commit changes**。
   - ⚠️ 要保留資料夾結構:`admin/` 和 `images/` 也要一起上傳。

### 步驟 2 — 用 Netlify 部署網站
1. 到 <https://www.netlify.com> 用 GitHub 帳號登入。
2. **Add new site → Import an existing project → GitHub**,選剛剛的 repo。
3. Build 設定全部留空(這是純靜態網站,不需要 build 指令),**Deploy**。
4. 部署完成後會得到一個網址,例如 `https://xilipower-web.netlify.app`。點開就是你的網站。
   - (可選)Site settings → **Change site name** 可改成好記的名字。

### 步驟 3 — 開啟後台登入功能
1. 在 Netlify 該網站頁面 → **Site configuration → Identity** → **Enable Identity**。
2. Identity 頁面 → **Registration** → 設為 **Invite only**(只有被邀請的人能登入,防止陌生人註冊)。
3. 往下找到 **Services → Git Gateway** → **Enable Git Gateway**。

### 步驟 4 — 邀請自己當管理員
1. Identity 頁面 → **Invite users** → 輸入你的 email → 送出。
2. 收信 → 點信中的連結 → 設定密碼。
3. 完成!之後從 `你的網址/admin/` 就能登入後台。

---

## ✏️ 日常怎麼更新內容
1. 打開 `https://你的網址/admin/` → 用剛設定的帳密登入。
2. 點 **網站內容 → 全站內容**,裡面分成 ① 品牌、② 主視覺 … ⑧ 頁尾八組。
3. 改文字、換圖片、按「新增」加課程或方案。
4. 右上角 **Publish → Publish now**。約 1 分鐘後網站自動更新。
   - 手機也能開 `/admin/` 登入編輯。

---

## 🖼️ 關於佔位圖
`images/` 裡目前是灰底的佔位圖(hero、video1~3、coach)。上線後從後台各區塊「上傳圖片」換成真實照片即可,不必手動處理檔案。

---

## 🔧 之後可能想調整
- **報名表單**:目前「立即體驗 / 報名」按鈕會捲動到聯絡區。若想改成 LINE 加好友或彈出表單,再告訴我。
- **自訂網域**:買好網域後,可在 Netlify **Domain settings** 綁定。
- **配色 / 字型**:如需開放後台調整,可再擴充。

有任何一步卡住,把畫面截圖給我,我帶你排解。
