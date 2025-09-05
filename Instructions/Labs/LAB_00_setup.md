---
lab:
  title: 實驗室設定
  module: Setup your Microsoft 365 lab tenant (not associated with a Learn module)
---

# 實驗室：Microsoft 365 租用戶的設定

## WWL 租用戶 - 使用條例
如果您針對講師導向訓練交付的一部分取得租用戶，請注意，租用戶的功能是為了在講師導向訓練中支援實際操作實驗室。

租用戶不應共用，或用於實際操作實驗室以外的用途。 本課程中使用的租用戶是試用租用戶，無法在課程結束後使用，且不符合擴充資格。

租用戶不得轉換成付費訂用帳戶。 此課程中提供的租用戶仍是 Microsoft Corporation 的財產，我們保留隨時取得存取權和重新持有的權利。

## 實驗室場景

此安裝實驗室包含在 Microsoft 365 租用戶中啟用 Microsoft 稽核記錄和檔案監視功能。

**預估時間**：10-15 分鐘

### 安裝程式 - 啟用 Microsoft 365 稽核記錄和檔案監視

在此設定工作中，您將在 Microsoft 365 中啟用稽核記錄和檔案監視功能。  

1. 開啟 Microsoft Edge。 在網址列中輸入 **`https://admin.microsoft.com`**。

1. 透過您授權的實驗室主機管理工具 (ALH) 提供的 Microsoft 365 租用戶系統管理員認證登入。

1. 從 Microsoft 365 系統管理中心的左側導覽窗格中，選取**顯示全部**。

1. 在 [系統管理中心] 底下，選取 [安全性]****。  新的瀏覽器頁面會開啟至 Microsoft Defender 的歡迎頁面。

1. 在左側導覽面板中，向下捲動並展開 **系統**。  從展開的清單中，選取**稽核。**  附註： 稽核功能也可以透過 Microsoft Purview 入口網站存取。

1. 登陸「稽核」頁面後，請等待 1-2 分鐘。  如果未啟用稽核，您將在頁面頂部看到藍色列，上面寫著開始記錄使用者和管理活動。  選取 [開始錄製使用者和系統管理員活動]****。  啟用稽核之後，藍色列就會消失。  如果藍色列不存在，則表示已啟用稽核，無需進一步動作。  如果您看到一則訊息：「抱歉，我們無法確定是否正在記錄活動。 嘗試刷新頁面。 如果重新整理頁面後沒有變更，您必須透過 PowerShell 啟用稽核。
    1. 以滑鼠右鍵選取工作列上的藍色 Windows PowerShell 圖示，然後選取 **[以系統管理員**身分執行]。
    1. 輸入 **`Install-Module -Name ExchangeOnlineManagement`** 來安裝 Exchange Online PowerShell 模組。  當提示「您確定要安裝『PSGallery』中的模組嗎」時，請選取 **`[A]` [全部是]**
    1. 現在，輸入 **`Import-Module ExchangeOnlineManagement`** 來載入模組。
    1. 若要連線，請輸入 **`Connect-ExchangeOnline -UserPrincipalName admin@WWLxZZZZZZ.onmicrosoft.com`**。  針對 UPN，輸入實驗室資源索引標籤中找到的系統管理員使用者名稱。
    1. 系統會提示您登入。  輸入實驗室資源索引標籤中找到的系統管理使用者名稱和密碼。
    1. 若要開啟稽核，請輸入 **`Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true`**。 系統會顯示一則訊息，指出變更最多可能需要 60 分鐘才能生效。
    1. 雖然最多可能需要 60 分鐘才能生效，但您可以輸入 **`Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled`** 來驗證是否收到命令。  如果已啟用稽核，則 UnifiedAuditLogIngestionEnabled 屬性會顯示 true 值。

1. 從左側導覽面板的 [系統] 底下，選取 **[設定]。**

1. 從設定頁面中，選取 [ **雲端應用程式**]。   向下捲動，然後在 [資訊保護]** 底下**選取 **[檔案**]。

1. 如果尚未啟用，請選取顯示 [啟用檔案監視 **] 旁邊**的方塊，然後選取 [**儲存**]。  

1. Microsoft 365 租用戶的實驗室設定到此結束。
1. 您可以關閉瀏覽器索引標籤 [Cloud Apps-Microsoft Defender]，但請保持開啟 [Microsoft 365 系統管理中心] 索引標籤，以進行下一個練習。

### 檢閱

在此設定中，您已啟用 Microsoft 365 中的稽核記錄和檔案監視功能。
