# Debby Huang｜個人履歷網站

精緻的個人履歷網站，搭配 Netlify CMS 後台，可透過瀏覽器直接編輯所有內容。

---

## 🚀 上線步驟（第一次設定，約 20 分鐘）

### Step 1｜把專案推上 GitHub

1. 前往 [github.com](https://github.com) 登入帳號
2. 點右上角 **+** → **New repository**
3. Repository name 填：`debby-resume`
4. 設定為 **Public**（Netlify 免費方案需要）
5. 按 **Create repository**

接著在你的電腦終端機執行：

```bash
cd debby-resume
git init
git add .
git commit -m "初始版本"
git branch -M main
git remote add origin https://github.com/你的帳號/debby-resume.git
git push -u origin main
```

---

### Step 2｜Netlify 部署

1. 前往 [app.netlify.com](https://app.netlify.com) → 用 GitHub 帳號登入
2. 按 **Add new site** → **Import an existing project**
3. 選 **GitHub** → 找到 `debby-resume`
4. 設定如下：
   - **Branch to deploy**：`main`
   - **Publish directory**：`.`（一個點）
5. 按 **Deploy site**

部署完成後會得到一個網址，例如：`https://debby-huang.netlify.app`

---

### Step 3｜開啟 Netlify Identity（後台登入用）

1. 在 Netlify 專案頁面，點上方選單 **Identity**
2. 按 **Enable Identity**
3. 往下找 **Registration**，選 **Invite only**（只有你能登入）
4. 找 **Git Gateway**，按 **Enable Git Gateway**

---

### Step 4｜建立後台帳號

1. 在 Identity 頁面按 **Invite users**
2. 輸入你的 Email → 送出邀請
3. 去信箱找邀請信，點連結，設定密碼

---

### Step 5｜進入後台開始編輯！

瀏覽器輸入：`https://你的網址.netlify.app/admin`

登入後即可看到後台，可以編輯：
- 首頁主視覺（姓名、引言、成就數字）
- 核心能力（增減技能卡片）
- 工作經歷（新增/修改職務）
- 代表專案（新增/修改專案）
- 聯絡資訊（電話、Email、地點）

---

## 📁 檔案結構說明

```
debby-resume/
├── index.html          ← 前台網站主頁面
├── netlify.toml        ← Netlify 設定
├── admin/
│   ├── index.html      ← 後台入口（不要動）
│   └── config.yml      ← 後台欄位設定
├── content/
│   ├── hero.json       ← 首頁主視覺內容
│   ├── skills.json     ← 核心能力內容
│   ├── experience.json ← 工作經歷內容
│   ├── projects.json   ← 代表專案內容
│   └── contact.json    ← 聯絡資訊內容
└── images/             ← 未來可放照片（後台上傳）
```

---

## ✏️ 直接修改內容（不用後台）

也可以直接編輯 `content/` 資料夾裡的 JSON 檔，推上 GitHub 後 Netlify 會自動重新部署（約 1 分鐘）。

---

## 🌐 綁定自訂網址（選用）

1. 購買網域（推薦 [Namecheap](https://namecheap.com) 或 [Cloudflare](https://cloudflare.com)）
2. 在 Netlify → **Domain management** → **Add custom domain**
3. 依照指示修改 DNS 設定

---

## 🆘 常見問題

**後台進不去？**
→ 確認 Step 3 有開 Identity 和 Git Gateway

**修改了但網站沒更新？**
→ 在 Netlify → Deploys 看是否有新的部署在執行

**忘記密碼？**
→ 到 `/admin` 點「Forgot password」

---

© 2025 Debby Huang
