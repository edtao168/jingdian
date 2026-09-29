# 上傳及本地測試運行

> 若有修改，在 mkdocs.yml 內調整 nav  
> 若準備上傳 github（在 PowerShell 執行）  
>> cd C:\laragon\www\jingdian  
>> mkdocs gh-deploy  
>> git add .  
>> git commit -m "新增文章：先進顏淵"  
>> git push  
> 若打算在本地測試  
>>（啟動本地服務器）mkdocs serve  
>> 瀏覽器運行 http://127.0.0.1:8000/  

---

# 建立新專案
第一次先在 GitHub 上建立 Repository 並完成綁定。請按照以下步驟完成設定：
  
> 1.在 GitHub 建立全新的 Repository：  
>> 開啟並登入 GitHub。  
>> 點擊右上角的 + -> 選擇 New repository。  
>> Repository name 輸入：jingdian  
>> 設為 Public（公開）。  
>> 不要 勾選 "Add a README file"、".gitignore" 或 "Choose a license"（保持完全空白）。  
>> 點擊 Create repository。  
>> 驗證方式：建立成功後，頁面上會顯示此 Repository 的 URL（例如 [https://edtao168.github.io/jingdian/](https://edtao168.github.io/jingdian/)。  

> 2.將本機專案初始化並推送到 GitHub：打開 PowerShell，切換至 C:\laragon\www\jingdian，依次執行以下指令：   
>> 1. 初始化本地 Git 儲存庫  
git init

>> 2. 加入所有檔案並提交  
git add .  
git commit -m "Initial commit for jingdian"  

>> 3. 切換分支名稱為 main  
git branch -M main

>> 4. 綁定 GitHub 遠端儲存庫 (請替換為你的網址)  
git remote add origin https://github.com/edtao168/chu_ci.git

>> 5. 將原始碼推送到 GitHub main 分支  
git push -u origin main  
驗證方式：重新整理 GitHub 的 jingdian 頁面，確認能看到你上傳的 mkdocs.yml 與 docs/ 資料夾。

> 完成遠端綁定後，再次執行部署指令：  
>> 在PowerShell執行mkdocs gh-deploy

> 至 GitHub 啟用功能：（核對一下，通常不用save）  
>> 前往 GitHub jingdian 專案頁面 -> 點擊 Settings 標籤頁。  
>> 左側選單點擊 Pages。  
>> 在 Build and deployment 下方的 Branch 選項：  
>> Branch 選擇：gh-pages  
>> Folder 選擇：/(root)  
>> 點擊 Save 保存。    
