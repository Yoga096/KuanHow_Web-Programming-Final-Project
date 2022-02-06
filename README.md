# Kuan好你ㄉ事 管好你的事 -- Web Programming Final Project

## 簡介
這是一個能夠簡單管理個人及團隊事務的網站。  
我們的靈感來自系女排每位迷迷糊糊的隊員以及各種繁雜的球隊事務，透過這個網站，球隊幹部可以輕鬆管理活動、公告、投票、比賽紀錄等重要資訊。  
使用者在個人頁面可以清楚看到自己及參與的球隊的所有活動日程，球隊頁面則可以提供活動日程、公告訊息、投票活動、比賽紀錄等功能。  
透過這次的專案，希望能幫助到所有事情太多煩不完的無力小老百姓。
#### 影片 demo: https://youtu.be/RN1N1_OHGTE
 ![](https://i.imgur.com/DOwi0jo.png)
 ![](https://i.imgur.com/s9Utnkz.png)
 ![](https://i.imgur.com/1dzxh4e.png)
 ![](https://i.imgur.com/Cvyjy1j.png)
 ![](https://i.imgur.com/KZ0Tm9U.png)
 ![](https://i.imgur.com/N4elPtH.png)



## 組員
 * 經濟四 - 錢紫翎
 * 經濟四 - 張祥賢 
 * 經濟五 - 陳又加

## 使用方式與功能

### 如何在 localhost 安裝與測試
 1. Clone repo
 2. 安裝 frontend & backend packages
  * (npm) cd frontend && npm install
  * (npm) cd backend && npm install
  * (yarn) cd frontend && yarn add
  * (yarn) cd backend && yarn add
 3. .env file
  * 將 .env.defaults (./backend) 的內容複製為 .env
  * 填入自己的 MONGO_URL
 4. 開啟第 1 個 terminal windows
  * (npm) cd frontend && npm start
  * (yarn) cd frontend && yarn start
 5. 開啟第 2 個 terminal windows
  * (npm) cd backend && npm run server
  * (yarn) cd backend && yarn server 
 6. 打開 http://localhost:3000 
  * 開始使用!


### Sign up / Log in 頁面 :
#### Sign up
 * 初次使用需申請一個新的帳號，必要資訊為電子郵件、帳號、密碼。
 * 填寫頁面有設計防呆機制，確保填寫的資料格式正確。
 * 密碼使用 bcryptjs 加密後存入資料庫。

#### Log in
 * 完成申請後使用該組帳號密碼登入。

### User 個人頁面 :
#### User Setting
 * 首次登入時須設定用戶名稱，顯示在個人及球隊頁面。
 * 後續的登入中，點擊 setting 可以修改用戶名稱，也可以查看帳戶資訊。
#### Dashboard
 * 使用者的個人主頁面，支援的功能如下：
 1. 可在此創建個人 event，新增的個人事項會顯示在畫面左方的 information card 中。
 2. 若使用者所屬的球隊裡，有人新增團隊事項，該團隊事項會同步更新在個人頁面的 
   information card 中。
 3. 所有的 infomation card 點擊可以查看細節、刪除事項、更新內容。
 4. 畫面右上方會提示使用者近三天內到期的 event；右下方會通知使用者，團隊新增的
   「事件」、「貼文」、「投票」。
#### Event
 1. 以日曆的形式顯示「個人事項」和「團隊事項」。
 2. 日期的格子點擊後，可創建該天的個人 event 到 Dashboard 中
#### Achievement
 1. 顯示該使用者所獲得的成就，目前只有初次登入的獎勵，日後會新增其他勳章，例如
   在球隊的活躍度、比賽的 mvp 等等。

#### all Teams
 * 顯示使用者參加的所有團隊，點及即可進入團隊頁面。
 * 使用者也可以在此創建團隊，並加入已註冊的用戶做為團隊成員。

### Team 團隊頁面 :
#### TeamHome 
 * 進入團隊頁面後，畫面左側新增團隊頁面專用的 Navbar (Home、Event、Post、Member、Score、Vote)。
 * 團隊首頁可顯示最近幾項活動、公告、投票、比賽紀錄。
 * 點擊各區塊的 VIEW ALL 按鈕觀看完整資訊。

 #### Event
 * 可依照條件篩選顯示的活動 (全部、未來、過去等)。
 * 點擊 CREATE 可新增活動並顯示在團隊頁面及所有成員的個人頁面。
 * 點擊各活動的 MORE 鍵可觀看詳細內容，包括 :  
    1. 活動名稱  
    2. 活動建立人  
    3. 活動日期  
    4. 活動地點  
    5. 活動細節  
 * 在詳細內容中也可以修改及刪除活動，並顯示在團隊頁面及所有成員的個人頁面。  

#### Member (隊員資訊)
 * 顯示隊員資訊，包含隊員名稱、帳號、電子郵件、身分(是否為管理員)。
 * 管理員可新增、刪除團隊成員。
   
#### Post
 * 點擊 CREATE可新增公告文章。
 * 點擊各文章的 MORE 鍵可觀看詳細內容，包括 :  
    1. 文章標題  
    2. 文章作者  
    3. 發表日期  
    4. 文章內容  
 * 在詳細內容中也可以修改文章內容，以及刪除文章。  
  
#### Score  
 * 點擊 CREATE可新增比賽紀錄。
 * 各 SCORE區塊顯示各場比賽標題、對手、局數及比賽日期。 
 * 點擊 DELETE按鈕可刪除該場比賽紀錄。
 * 點擊 SCORE區塊進入各局詳細記錄。

#### Score Detail
 * 點擊 CREATE可新增各局詳細紀錄。  
 * 紀錄單中可新增任意人數的球員個人詳細數據。  
 * 未填寫的欄位會自動填入 0或 ""。  
 * 點擊各局 Detail 可觀看詳細記錄單或編輯、刪除紀錄。  
  
#### Vote
 * 點擊 CREATE可新增投票活動，可設定截止時間及每人票數限制。  
 * 點擊投票活動可顯示詳細內容，包括 :  
    1. 投票題目  
    2. 截止時間
    3. 票數限制  
    4. 各選項及其得票數。  
 * 使用者勾選選項及可參與投票，票數會在下次檢視詳細內容時時更新。  
 * 使用者取消勾選選項及可取消投票。   

## 使用與參考之框架/模組/套件
### 前端
 * React
 * Apollo GraphQL
 * MUI
 * antd
 * full Calendar
### 後端
 * Node.js
 * GraphQL
### 資料庫
 * MongoDB
