---
lab:
  title: 探索 Azure 網路安全性群組 (NSG)
  module: Describe the basic security capabilities in Azure
---

# 實驗室：探索 Azure 網路安全性群組 (NSG)

此實驗室對應至下列 Learn 內容：

- 學習路徑：描述 Microsoft 安全性解決方案的功能
- 課程模組：描述 Azure 中的基本安全性功能
- 單元：描述 Azure 網路安全性群組

## 實驗案例

在本實驗中，您將探索 Azure 中的網路安全性群組的功能。  您將建立網路安全性群組 (NSG)，並將 NSG 指派給預先存在的虛擬機器 (VM) 介面。  設定完成後，您會發現預設輸入與輸出規則，請建立新規則，然後測試這些規則。  在本實驗中，會為您建立將搭配 NSG 使用的 VM，因此您會先檢視與該 VM 相關聯的一些資訊。
  
**估計時間**：45 分鐘

### 工作 1

在這項工作中，您會檢視與為了用於本實驗而建立的 VM 相關聯的一些參數。

1. 開啟 Microsoft Edge。  在網址列中輸入 **https://portal.azure.com**。

1. 登入管理員認證。
    1. 在 [登入] 視窗中，輸入實驗室託管供者所提供的使用者名稱，然後選取 [下一步]****。
    1. 輸入應由您的實驗室託管提供者提供的管理員密碼。 選取 [登入]****。
    1. 視您的實驗室主機管理員而定，如果這是您第一次登入租用戶，系統可能會提示您完成 MFA 註冊程式。 如果是，請依照畫面上的提示來設定 MFA。

1. 在頁面頂端的 [Azure 服務] 之下，選取 [虛擬機器]****。  如果沒看到其列出，則在搜尋方塊中，於頁面頂部 Microsoft Azure 旁邊的藍色列中，輸入**虛擬機器**，然後從搜尋結果中選取 [虛擬機器]****。

1. 從虛擬機器頁面中，選取所列的 VM [SC900-WinVM]****。

1. 您現在位於 SC900-WinVM 頁面。  請注意 VM 的一些基本資訊。

1. 從左側導覽面板中，展開 [ **網络]** ，然後選取 [ **網络設定**]。  主視窗的基本區段會顯示 VM 的網路介面。  請注意，網路安全性群組旁邊沒有列出任何項目，因為沒有指派給介面的 NSG。

1. 將此索引標籤保持開啟狀態。

### 工作 2

在這項工作中，建立網路安全性群組、將 VM 的網路介面指派給 NSG，以及為 RDP 流量建立新的輸入規則。

1. 從開啟的 Azure 索引標籤中，以滑鼠右鍵按一下** 頁面頂端的 [首頁]**** 連結，然後選取 [在新索引標籤中開啟連結]****，以將另一個頁面開啟至 Azure 服務。

1. 在頁面頂端的藍色搜尋列中，輸入**網路安全性群組**，並從結果中選取 [網路安全性群組]****。 請勿選取 [網路安全性群組 (傳統版)]**。

1. 從頁面中央，選取標記為 [建立網路安全性群組]**** 的藍色按鈕。  或者，您可以從 [網路安全性群組] 頁面頂部選取 [+ 建立]****。

1. 在 [建立網路安全性群組] 頁面的 [基本] 索引標籤上，指定下列設定：
    1. 訂用帳戶：保留預設值 (這是授權實驗室託管服務提供者所提供的 Azure 訂用帳戶)
    1. 資源群組：** LabsSC900**
    1. 名稱：** NSG-SC900**
    1. 區域：保留預設值。
    1. 選取 [檢閱 + 建立]****,然後選取 [建立]****。

1. 部署完成後，請選取 [前往資源]****。

1. 您應該位於新建 NSG 的 [概觀] 頁面上。  如果不是，請從左側導覽面板中選取 [概觀]****。 在頁面頂端的 [基本資訊] 底下，您會看到您所建立 NSG 的一些基本資訊。  請注意兩點：沒有任何自訂安全性規則，也沒有與此 NSG 相關聯的子網路和網路介面。  雖然沒有自訂安全性規則，但每個 NSG 都包含預設的輸入和輸出規則，如頁面上所示。  檢閱輸入和輸出規則。 預設輸入規則會拒絕不是來自虛擬網路或 Azure 負載平衡器的所有輸入流量。  輸出規則會拒絕虛擬網路之間流量和對網際網路的輸出流量以外的所有輸出流量。

1. 從 NSG-SC900 頁面上的左側瀏覽窗格中，展開 **[設定** ]，然後選取 **[網络介面**]。
    1. 選取 [+ 建立關聯]****。
    2. 在網路介面關聯的欄位中，選取**向下箭號**、選取 [sc900-winvmXXX]****，然後選取視窗底部的 [確定]****。 一旦介面與 NSG 建立關聯，就會顯示在清單上。  NSG 現在已指派給 VM 的網路介面。

1. 切換回瀏覽器上的 **SC900-WinVM - Microsoft Azure** 索引標籤。  重新整理頁面。 在網路安全性群組旁邊，您現在應該會看到您剛建立的 NSG 名稱。  如果您仍然看不到，請再稍候一分鐘，然後再次重新整理頁面。

1. 從左側導覽面板中，選取 [連線]****。 從主視窗中顯示連接埠號碼 3389 的位置旁邊，選取 [檢查存取權]****。 檢查存取功能會將訊號 (流量) 傳送至 VM 的預設 RDP 連接埠 3389，以檢查其是否可存取。 其可能需要一分鐘的時間，但您將會看到 [無法存取]。  這是預期的，因為 DenyAllInBound NSG 規則會拒絕 VM 的所有輸入流量。

1. 切換回瀏覽器上的 [NSG-SC900 - Microsoft Azure]**** 索引標籤。

1. 在左側的瀏覽窗格中，選取 [輸入安全性規則]****。 預設的輸入規則會拒絕非來自虛擬網路或 Azure 負載平衡器的所有輸入流量，因此您必須設定規則以允許輸入 RDP 流量 (連接埠 3389 的流量)。 請記得，您無法移除預設規則，但可以建立優先順序更高的規則來加以覆寫。

1. 從頁面頂端選取 [新增]****。 在 [新增輸入安全性規則] 的視窗中，指定下列設定：
    1. 來源：**任意**
    1. 來源連接埠範圍：**\***
    1. 目的地：**任何**
    1. 服務：**RDP**
    1. 動作：**允許**
    1. 優先順序：**1000**。 編號較小的規則優先順序較高，應首先進行處理。
    1. 名稱：保留預設名稱，或建立自己的描述性名稱。
    1. 請注意頁面底部的警告符號。  我們只使用 RDP 進行測試，以及示範 NSG 的功能。
    1. 選取**新增**

1. 規則佈建完成後，即會出現於輸入規則的清單中 (您可能需要重新整理畫面)。

1. 保持開啟此瀏覽器索引標籤。  

### 工作 3

在這項工作中，您將測試新建立的輸入 NSG 規則，以確認您可建立與 VM 的遠端桌面 (RDP) 連線。  在 VM 內，您將檢查從 VM 對網際網路的輸出連線。

1. 開啟瀏覽器索引標籤的 [SC900-WinVM – Microsoft Azure]。

1. 從左側導覽面板選取 [連線]****。

1. 選取 [檢查存取權]**** (確認埠已設定為 3389)。  狀態應會顯示為「可存取」。  如果您仍然看到「無法存取」，請重新整理頁面，然後再試一次，可能需要幾分鐘的時間，檢查存取選項才會看到新的輸入規則。

1. 現在，按一下 [原生 RDP] 方塊中的 [選取]****，直接連線到 VM。
   
    1. 在 [原生 RDP] 視窗中，選取 [下載 RDP 檔案]****。
    1. 如果出現下載警告，請選取 [保留]****，然後在出現的快顯視窗上，選取 [開啟檔案]****。
    1. 遠端桌面連線視窗隨即開啟，選取 [連線]****。
    1. 系統會提示您提供認證。  輸入 VM 的 [使用者名稱] 和 [密碼] (請參考實驗室指示面板上的 [資源] 索引標籤)。
    1. [遠端桌面連線] 視窗隨即開啟，顯示*無法驗證遠端電腦的身分識別。是否確認要繼續？*  選取 [是]****。

1. 您現在已連線至 VM。 在這種情況下，您能夠連線至 VM，因為您建立的輸入流量規則允許透過 RDP 向 VM 傳送輸入流量。  在 [歡迎] 畫面上幾秒鐘後，您可能會看到一個視窗可供選擇裝置的隱私權設定，選取 [接受]****。  如果出現網路視窗，選取 [否]****。

1. 在 RDP 工作階段啟動並執行 VM 後，從 VM 測試與網際網路的輸出連線能力。
    1. 在開啟的 VM 上，選取 [Microsoft Edge]**** 以開啟瀏覽器。 由於這是您第一次開啟 VM 和 Broswer，因此系統可能會提示您輸入一些基本設定。  
    1. 系統可能會提示您選擇裝置的隱私權設定。 保留預設值，然後選取 [ **接受**]。  
    1. 網路側邊面板可能會顯示。  選取 **否**。
    1. 視窗可能會顯示「在 Windows 上使用最佳效能瀏覽器瀏覽網頁」，選取 **[繼續**]，選取 **[啟動但不**您的數據]，選取 **[確認並繼續]，選取 **[繼續但不使用此數據**]，最後選取 [**確認] 並開始**流覽**。
    1. 在瀏覽器網址列中輸入 **www.bing.com**，確認您可以連線至搜尋引擎。
    1. 確認您可存取 www.bing.com 之後，請關閉 VM 中的瀏覽器視窗，但是讓 VM 保持運作。

1. 選取藍色索引標籤中的底線 **_** 以顯示 VM 的 IP 位址，藉此將 VM 最小化。 這可讓您回到 [SC900-WinVM \|連線] 頁面。

1. 讓瀏覽器索引標籤保持開啟，您將在下一個工作中使用。

### 工作 4

在上一個工作中，您已確認您可建立與 VM 的 RDP 連線。 在 VM 上，您也確認了您可建立對網際網路的輸出連線。  允許輸出網際網路流量，因為 NSG 的預設輸出規則允許輸出網際網路流量。  在這項工作中，您將會進行建立自訂輸出規則的流程，以封鎖傳出的網際網路流量與測試該規則。

1. 您應該位於 [SC900-WinVM \| 連線] 頁面。 在左側導覽面板中，選取 [網路]****。 如果您先前關閉了瀏覽器索引標籤，請選取頁面頂端的藍色搜尋列並選取虛擬機器，接著選取 VM **SC900-WinVM**，然後選取 [網路]****。

1. 請選取**輸出連接埠規則**索引標籤。您將會看到預設輸出規則。  請注意預設規則 「AllowInternetOutBound」。 此規則允許所有輸出網際網路流量。 您無法移除預設規則，但可以建立一個較高優先順序的規則來覆寫預設規則。 從頁面右側，選取 **[+Crate 埠規則** ]，然後從下拉式清單中選取 [ **輸出埠規則**]。

1. 在新增輸入安全性規則的視窗中，指定下列設定：
    1. 來源：**任意**
    1. 來源連接埠範圍：**\***
    1. 目的地：**服務標記**
    1. 目的地服務標記：**網路**
    1. 服務：** 自訂 ** (保留預設值)
    1. 目的地連接埠範圍：**\*** (請確保在目的地連接埠範圍欄位中輸入星號)。
    1. 通訊協定：**Any**
    1. 動作：**Deny**
    1. 優先順序：**1000**
    1. 名稱：保留預設名稱，或建立自己的描述性名稱。
    1. 選取**新增**

1. 佈建規則後會出現在輸出規則清單中。  雖然出現在清單中，但需要幾分鐘的時間才會生效 (請稍候幾分鐘，再繼續進行後續步驟)。  


1. 返回您的 VM (VM 的 RDP 圖示應該顯示在頁面底部的工作列上)。

1. 開啟 VM 中的 Microsoft Edge 瀏覽器，然後輸入 **www.bing.com**。 此頁面不應顯示。 如果您能夠連線至網際網路並驗證輸出規則的所有參數都已正確設定，則可能是因為該規則需要幾分鐘才會生效。  關閉瀏覽器，等候幾分鐘後再試一次。 實驗室環境中的 Azure 訂用帳戶可能會經歷比正常還要長的延遲。

1. 選取 [顯示 IP 位址之頁面頂端的 X]****，以關閉遠端桌面連線。  快顯視窗隨即出現，指出您的遠端工作階段將會中斷連線。 選取 [確定]****。

1. 選取視窗左上角顯示 Microsoft Azure 藍色列下方的 [首頁]****，即可返回 Azure 服務首頁。

1. 保持在瀏覽器中開啟 Azure 索引標籤。

### 檢閱

在本實驗中，您逐步完成了下列流程：設定網路安全性群組 (NSG)、建立該 NSG 與虛擬機器網路介面之間的關聯，以及將規則新增至 NSG，以允許輸入 RDP 流量及封鎖輸出網際網路流量。
