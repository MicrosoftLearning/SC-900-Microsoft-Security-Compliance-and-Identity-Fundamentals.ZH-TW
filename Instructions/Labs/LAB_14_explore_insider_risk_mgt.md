---
lab:
  title: 探索 Microsoft Purview 中的內部風險管理
  module: Describe the insider risk capabilities in Microsoft Purview
---

# 實驗室：探索 Microsoft Purview 的內部風險管理

此實驗室對應至下列 Learn 內容：

- 學習路徑：描述 Microsoft 合規性的功能
- 課程模組：描述 Microsoft Purview 中的內部風險功能
- 單元：描述內部風險管理

## 實驗案例

在本實驗中，您將逐步解說設定內部風險管理原則的流程，以及設定和使用內部風險管理原則的基本先決條件。  請注意：本實驗將僅提供設定內部風險管理所需的內容，以及與建立原則相關的選項。  本實驗不包括觸發原則的工作，因為觸發原則需要發生的事件數量超出此練習的範圍所需的時間。

**預估時間**：45-60 分鐘

### 工作 1

在此工作中，您身為全域管理員，將啟用內部風險管理的權限。  具體而言，您將向「內部風險管理」角色群組新增使用者，以確保指定使用者可以存取和管理內部風險管理功能。  最多可能需要 30 分鐘，才能將角色群組權限套用到整個組織的使用者。

1. 開啟 Microsoft Purview 首頁的瀏覽器索引標籤。  如果您先前已關閉，請開啟瀏覽器索引標籤並輸入 **https://admin.microsoft.com**。 透過您授權的實驗室主機管理工具 (ALH) 提供的 Microsoft 365 租用戶系統管理員認證登入。 從 Microsoft 365 系統管理中心的左側導覽窗格中，選取 [顯示全部]****，接著選取 [合規性]****。  會在新的瀏覽器頁面中開啟 Microsoft Purview 合規性入口網站的歡迎頁面。  

1. 從左側導覽面板中，展開 [角色和範圍]****，然後選取 [權限]****。

1. 選取 [Microsoft Purview 解決方案] 底下的 [角色]****。

1. 在搜尋欄位中輸入**測試人員風險 **，然後在鍵盤上按 Enter 鍵。  請注意顯示的許多角色。  每一個都有不同的存取層級。  選取 [內部風險管理]****，然後檢閱描述。  向下捲動至顯示成員的位置，並注意 [MOD 管理員] 和 [Megan Bowen] 已列出。 選取視窗右上角的 **X** 以關閉視窗。

1. 在左側導覽面板中，選取 [首頁]**** 以返回 Microsoft Purview 合規性入口網站頁面。

1. 讓此瀏覽器索引標籤保持開啟，因為您將在後續工作中回到這裡。

### 工作 2 (請注意：如果您已執行設定實驗工作以啟用稽核記錄，請跳過工作 2)

內部風險管理會使用 Microsoft 365 稽核記錄來獲取原則和分析洞察中識別的使用者洞察和活動。 在這項工作中，您將啟用稽核記錄搜尋功能。 請注意：開啟稽核日誌搜尋功能後可能會花費數小時才能在搜尋稽核記錄時傳回結果。  雖然可能需要數小時才能搜尋稽核記錄，但不會影響完成此實驗室中其他工作的能力。

1. 請選取標示為 **Home-Microsoft 365 compliance** 的瀏覽器索引標籤。  如果先前關閉過此瀏覽器索引標籤，請開啟 Microsoft Edge 並在網址列輸入 **compliance.microsoft.com**，然後以系統管理員認證登入。

1. 從左側導覽面板的解決方案下，選取 [稽核]****。

1. 驗證是否已選取 (已畫底線) [重新搜尋]**** 索引標籤。

1. 進入 [稽核] 頁面之後，請等候 2-3 分鐘。  如果未啟用稽核，您將在頁面頂部看到藍色列，上面寫著開始記錄使用者和管理活動。  選取 [開始錄製使用者和系統管理員活動]****。  啟用稽核之後，藍色列就會消失。  如果藍色列不存在，則表示已啟用稽核，無需進一步動作。

1. 藉由選取左側導覽面板中的 [首頁]****，返回 Microsoft Purview 合規性入口網站的首頁。

1. 讓此瀏覽器索引標籤保持開啟，您將在下一個工作中使用它。

### 工作 3

在這項工作中，您將逐步解說與「內部風險管理」解決方案相關的設定。  不論您在建立原則時選擇哪個範本，內部風險管理設定都會套用至所有內部風險管理原則。

1. 您應該會在 Microsoft Purview 合規性入口網站首頁上。 請選取標示為**首頁 - Microsoft 365 合規性**的瀏覽器索引標籤。

1. 在左側導覽面板的 [製作] 下方，選取 [內部風險管理]****。

1. 開始設定原則之前，有一些管理員應該熟悉的設定，並視需要為其組織進行設定。 從 [內部風險管理] 頁面，請選取 [內部風險管理] 視窗右上角的**設定齒輪圖示**，以存取 [內部風險] 設定。  
    1. 確認您位於 [隱私權]**** 索引標籤中：對於執行與您內部風險原則相符的活動之使用者，此設定將確定會顯示其實際姓名，或是使用匿名版本掩蓋其身分識別。  為了進行此逐步解說，您可以保留預設設定。
    1. 選取 [原則指標] **** 索引標籤。發生原則觸發事件之後，會針對使用者使用對應至所選指標的活動來判斷風險分數。 此處所選的原則指標包括測試人員風險原則範本。  捲動以檢視所有可用的指標和任何相關聯的資訊。 在 [Office 指標]**** 底下，選取 [ 全部選取]****，然後選取頁面底部的 [儲存]**** (您必須向下捲動)。
    1. 選取 [原則時間範圍] **** 索引標籤。針對測試人員風險原則觸發比對時，此處選擇的時間範圍會針對使用者生效。   啟用視窗會決定原則會主動偵測使用者的活動，並在使用者執行符合原則的第一個活動時觸發。 過去的活動偵測會決定原則偵測使用者活動的程度，並在使用者執行符合原則的第一個活動時觸發。  保留預設值。
    1. 選取 [智慧型偵測]**** 索引標籤。請檢閱這裡的選項。  請注意網域設定，以及與指標的關係。
    1. 探索列於此設定中的其他項目，並注意有許多項目為預覽狀態。

1. 若要返回內部風險管理概觀，請從頁面左上角，顯示設定的上方，選取 [內部風險管理]****。

1. 讓此瀏覽器索引標籤保持開啟，您將在下一個工作中使用它。

### 工作 4

在這項工作中，您將逐步解說建立原則的設定。  目標只是了解與建立原則相關聯的各種選項和彈性。

1. 您應該會位於內部風險管理頁面上。  如果還沒進入頁面，請開啟標示為 [內部風險管理 - Microsoft 365 合規性] **** 的瀏覽器索引標籤。

1. 從 [內部風險管理概觀] 頁面中，選取 [原則]**** 索引標籤，然後選取 [+ 建立原則]****。  設定下列每個原則索引標籤。

    1. 原則範本：在 [資料洩漏] 類別下，選取 [資料洩漏]****。  閱讀與此範本相關聯的詳細資料。 在必要條件下，DLP 原則會在綠色圓圈中顯示核取記號，指出已滿足必要條件。  已針對此實驗室租用戶預先設定 DLP 原則。 選取 [下一步]****。 
    1. 名稱與描述：輸入名稱 **SC900-InsiderRiskPolicy**，然後選取 [下一步]****。
    1. 使用者和群組：檢閱資訊方塊。  保留預設設定，**包括所有使用者和群組**。  選取 [下一步]****。
    1. 要設定優先順序的內容：根據描述，包含優先順序內容的任何活動都會增加風險分數，進而增加產生高嚴重性警示的機會。 為了簡單起見，請選取 [我不想立即設定內容的優先順序]****，然後選取 [下一步]****。
    1. 觸發程序：觸發事件可決定原則何時開始將風險分數指派給使用者的活動。  如果使用者執行外洩活動，您可選擇現有的 DLP 原則。 選取 [使用者符合資料洩漏防護 (DLP) 原則]****，然後從下拉式清單中選取 [美國金融資料]****。 選取 [下一步]****。
    1. 指標：請注意，您在上一個工作中選取的所有辦公室指標都已選取 (選取 Office 指標旁的向下方向鍵即可看到這點)，然後選取 [下一步]****。
    1. 在 [偵測選項] 頁面上，保留所有預設設定，但閱讀與各種選項相關聯的描述，並將滑鼠停在資訊圖示上，以取得特定設定的詳細資訊。  選取 [下一步]。
    1. 在頁面上，若要決定要使用預設或客戶指標閾值，請保留預設設定 [套用 Microsoft 提供的閾值]****，然後選取 [下一步]****。
    1. 結尾：檢閱設定，選取 [提交]****。
    1. 檢閱接下來會發生什麼情況的描述，然後選取 [完成]****。

1. 您將退回內部風險管理頁面的「原則」索引標籤。  將會列出您所建立的原則。  如果沒看到該原則，請選取 [重新整理]**** 圖示。

1. 身為管理員，您可以根據您選取的原則所偵測到的活動，立即開始將風險分數指派給使用者。 這會略過先偵測到觸發事件 (例如 DLP 原則相符項目) 的需求。  管理員的做法是選取原則名稱旁邊的空心方形以選取原則，然後選取 [針對使用者開始評分活動]****，其顯示於原則表格上方。  新的視窗隨即開啟，要求管理員填入可用的欄位。 將欄位保留空白，因為您不會設定此選項，但如需管理員為何要這麼做的詳細資訊，請選取 [為什麼要這麼做？]****。  選取視窗右上角的 **X** 以結束視窗。

1. 在左側導覽面板中，選取 [首頁]**** 以返回 Microsoft Purview 合規性入口網站的登陸頁面。

1. 保持開啟瀏覽器索引標籤。

### 檢閱

在本實驗中，您已經逐步解說設定內部風險管理原則的流程，以及設定和使用內部風險管理原則的基本先決條件。
