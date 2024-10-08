<!---
---
示範：標題：「探索電子檔探索」學習路徑/模組/單元：『學習路徑：描述 Priva Microsoft和Microsoft Purview 的功能;課程模組 3：描述 Purview Microsoft 的數據合規性解決方案;單元 2：描述電子檔探索'
---
--->

# 示範：探索電子檔案探索 （標準）

此示範對應至下列 Learn 內容：

- 學習路徑：描述 Priva Microsoft 和 Microsoft Purview 的功能
- 課程模組：說明一下 Microsoft Purview 的資料法務遵循解決方案
- 單元：描述電子檔探索

## 示範案例

在本示範中，您將逐步完成設定「電子文件探索」所需的步驟，包括設定角色權限、建立電子文件探索案例、建立電子文件探索保留及建立搜尋查詢。  注意：在 Microsoft Purview 入口網站中，使用者介面的更新正在逐步推出。 某些實驗室/示範租使用者可能尚未顯示最新的UI，因此所有實驗室步驟都會使用傳統電子檔探索UI來顯示。

### 示範第 1 部分

若要存取電子文件探索 (標準版)，或新增為電子文件探索案例的成員，使用者必須獲指派適當的權限。 在示範的這個部分中，身為全域管理員，您將逐步解說將特定使用者新增為電子文件探索管理員角色群組的成員的程式。

1. 開啟Microsoft Purview** 的**瀏覽器索引標籤。 如果您先前已關閉它，請開啟瀏覽器索引標籤，然後在網址列中輸入 **https://purview.microsoft.com**。 若要存取新的 Microsoft Purview 入口網站，請選取其說明位置旁的方塊， **我同意數據流披露和隱私聲明**的條款，然後選取 [ **開始使用**]。  
1. 從左側導覽面板中，選取 [ **設定**]。
1. 從開啟的瀏覽面板中，選取 [ **角色] 並選取 [範圍** ] 以展開選項，然後選取 [ **角色群組**]。
1. 在畫面右側的搜尋方塊中，搜尋電子檔探索**一詞**。  選取 [電子文件探索管理員]****。
    1. 選取**編輯**。
    1. 選取 [ **選擇使用者**]。
    1. 搜尋 MOD 系統管理員，選取 MOD 系統管理員**旁邊的**方塊，然後選取頁面底部的 [選取****] 按鈕。
    1. 選取 **[下一步** ]，然後選取 **[儲存**]，最後選取 [ **完成**]。

1. 保持開啟此瀏覽器索引標籤。

### 示範第 2 部分

在此部分中，您將建立一個案例，以開始使用電子檔探索（標準）。

1. 從左側導覽面板中，依序選取 **[解決方案**]、[ **電子檔探索** ] 及 [ **標準案例**]。

1. 在電子文件探索 (標準版) 頁面的頂部，選取 [+ 建立案例]****。

1. 在新增案例視窗中，輸入案例名稱 **SC900 測試案例**，然後選取頁面底部的 [儲存]****。

1. 此案例現在應該會出現在清單中。

1. 身為案例的建立者，而且因為您擁有電子文件探索管理員權限，因此可以開始使用。  

1. 保持開啟此瀏覽器索引標籤。

### 示範第 3 部分

現在，您已建立了電子文件探索 (標準版) 案例，可以開始處理此案例。  在這個部分，您將為所建立的案例建立電子文件探索保留。  具體來說，您將為屬於 Adele Vance 的交換信箱建立保存措施。

1. 在電子文件探索 (標準版) 頁面中，選取您建立的案例 **SC900 測試案例**。

1. 從案例的 [首頁] 頁面中，選取 [保留] **** 索引標籤，然後選取 [+建立]****。

1. 在名稱欄位中，請輸入**測試保存措施**，然後選取 [下一步]****。

1. 在 [選擇位置] 頁面中，選取 [Exchange 信箱]**** 旁邊的切換開關，將狀態設定為 [開啟]****。  

1. 現在，選取 [選擇使用者、群組或小組]****。  在搜尋方塊中，輸入 **Adele**，然後按鍵盤上的 Enter 鍵。 從搜尋結果，選取 [Adele Vance]****，然後選取 [完成]****。

1. 從選擇位置頁面，選取 [下一步]。****  為了快速完成示範，此保留中不會包含任何其他位置。

1. 「查詢條件」頁面允許您根據特定關鍵字或符合的條件建立保存措施，選取 [+ 新增條件]**** 以檢視可用的選項。  選取 [下一步]****。 沒有任何條件，保留會保存指定位置中的所有內容。

1. 檢閱您的設定並選取 [提交]****，可能需要一分鐘的時間，然後選取 [完成]****。  此測試保留應該會出現在清單中。  如果未立即出現，請選取**重新整理**。

1. 保持開啟此瀏覽器索引標籤。

### 示範第 4 部分

保存措施到位後，您將建立搜尋查詢。  搜尋完成後，電子文件探索支援動作，例如匯出和下載結果以供未來調查。   請注意：與電子文件探索 (標準版) 案例建立關聯的搜尋並未列於 Microsoft Purview 合規性入口網站的 [內容搜尋] 頁面上。 這些搜尋僅會列在與電子文件探索 (標準版) 案例建立關聯的 [搜尋] 頁面上。

1. 從 [SC900 測試案例] 頁面選取 [搜尋]****。

1. 在 [内容搜尋] 頁面上，選取 [新增搜尋]****。

1. 在 [名稱] 欄位中，輸入 [測試保留 - 銷售搜尋]****，然後從頁面底部選取 [下一步]****。

1. 在 [選擇位置] 頁面中，選取 **保留** 位置並取消選取 **[為內部部署使用者新增應用程式內容]，因為您的實驗室環境沒有內部部署使用者**，然後選取 [ **下一步**]。

1. 查詢條件頁面允許您根據特定關鍵字或符合的條件建立搜尋，請在關鍵字欄位輸入**銷售**並選取 [下一步]****。

1. 檢閱您的設定並選取 [提交]****，可能需要一分鐘的時間，然後選取 [完成]****。  此搜尋保留應該會出現在清單中。  如果未立即出現，請選取**重新整理**。

1. 在 [搜尋] 視窗中，選取您建立的 [測試保存措施 – 銷售搜尋]****。  開啟且已選取 [摘要] 索引標籤的視窗。  搜尋完成後，狀態將指示搜尋已完成。  您將看到「搜尋統計資料」索引標籤 (如果您沒有看到「搜尋統計資料」索引標籤，則搜尋可能仍在執行，可能需要幾分鐘的時間才能完成)。  選取 [搜尋統計資料] **** 索引標籤，然後選取 [搜尋內容] 旁的向下箭號。  您也可以檢視 [條件] 報表和 [最上層] 位置的詳細資訊。  

1. 在頁面底部，選取 [動作]****。  請注意包括匯出選項的可用選項。 選取**關閉**。

1. 關閉所有已開啟的瀏覽器索引標籤。

### 檢閱

在本示範中，您已逐步了解開始使用電子文件探索 (標準版) 所需的步驟，包含設定電子文件探索的角色權限以及建立電子文件探索案例。  建立案例後，藉由建立電子文件探索保留和建立搜尋查詢，您已逐步了解電子文件探索 (標準版) 工作流程的元素。
