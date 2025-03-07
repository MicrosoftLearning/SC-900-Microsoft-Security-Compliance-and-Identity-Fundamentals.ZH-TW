---
lab:
  title: 探索適用於雲端的 Microsoft Defender
  module: Describe the security management capabilities of Azure
---

# 實驗室：探索適用於雲端的 Microsoft Defender

此實驗室對應至下列 Learn 內容：

- 學習路徑：描述 Microsoft 安全性解決方案的功能
- 課程模組：描述 Azure 的安全性管理功能
- 單元：描述雲端安全性狀態管理。

## 實驗案例

在本實驗中，您將探索適用於雲端的 Microsoft Defender。  請注意：授權實驗室託管服務提供者 (ALH) 所提供的 Azure 訂用帳戶可限制存取，而且可能經歷比正常還要長的延遲。

**預估時間**：30 分鐘

### 工作 1

在本工作中，您將針對適用於雲端的 Microsoft Defender 的某些功能進行高階逐步解說

1. 您應該在 Azure 服務的首頁。  如果您先前已關閉瀏覽器，請開啟 Microsoft Edge。 在網址列輸入 **portal.azure.com** 並使用管理員認證登入。

1. 在藍色搜尋列中輸入 [適用於雲端的 Microsoft Defender]****，然後從結果清單中選取 [適用於雲端的 Microsoft Defender]****。

1. 如果這是首次使用您的訂閱進入適用於雲端的 Microsoft Defender，會進入 [開始使用] 頁面，並會提示您要升級。  捲動至頁面底部，然後選取 [稍後提醒我]**** (或 [略過]****)。  系統將帶您前往 [概觀] 頁面。

1. 在適用於雲端的 Microsoft Defender 的 [概觀] 頁面中，請注意頁面上可用的資訊 (如果您看到 0 個評估的資源和作用中建議，請重新整理瀏覽器頁面，這可能需要幾分鐘的時間)。  頁面上方的資訊包含 Azure 訂閱數、已評估資源數、作用中建議數，以及任何安全性警示。  頁面主體有一些卡片，代表 [安全性狀態]、[法規合規性]、[見解] 等等。  請注意：適用於雲端的 Microsoft Defender 預設原則方案 (通常必須由管理員指派) 已指派為 Azure 訂用帳戶設定的一部分。 不過，安全性分數會顯示為 0%，因為 Azure 最多可能延遲 24 小時，以反映初始分數。

1. 請在頁面上方選取 [評估資源]****。 
    1. 這會帶您前往列出目前資源的 [詳細目錄]**** 頁面。 選取虛擬機資源 **sc900-winvm**。 此資源與您在上一個實驗中使用的虛擬機器相關聯。
    1. VM 的 [資源健康情況] 頁面提供一份建議清單。  在可用的清單中，從顯示 [狀況不良]**** 狀態的清單中選取任何項目。
    1. 請注意詳細描述。  選取補救步驟旁的下拉式箭號。 請注意如何提供補救指示 (或指示的連結)，以及可採取動作的選項。  結束視窗，而不需採取任何動作。
    1. 返回適用於雲端的 Microsoft Defender 概觀頁面，選取頁面頂端的 [適用於雲端的 Microsoft Defender | 概觀]****，其上方顯示 [資源健康情況]。

1. 在左側導覽面板中，選取 [建議]****。  
    1. 確認已選取 (已畫底線) [所有建議]**** 索引標籤。  請注意，依嚴重性、資源健康情況等顯示作用中建議的儀表板檢視。
    1. 從清單選取項目。  在開啟的頁面中，您會看到描述包括補救步驟以及受影響資源等內容的說明和額外資訊。 請選取畫面右上角的 **X** 來開頁面。

1. 從主要左側導覽面板中，展開 **[雲端安全性** ]，然後選取 [ **法規合規性**]。  **請注意**：如果您沒有看到計算合規性的訂用帳戶，原因是可能最多有 24 小時的延遲才會顯示資訊。 移至工作 2。  如果您確實看到資訊，請接續步驟。
    1. 法規合規性頁面會根據 Microsoft 雲端安全性基準提供合規性控制項清單 (確認Microsoft 雲端安全性基準索引標籤已選取/已畫底線)。 每個控制網域之下有都控制項子集，而且每個控制項都有一或多項評量。 每項評量都會提供資訊，包括描述、補救和受影響的資源。
    1. 讓我們探索其中一個控制網域區域。 選取 (展開) [NS. 網路安全性]****。 與網路安全性相關的控制項清單隨即顯示。
    1. 選取 **NS-10。確保網域名稱系統 (DNS) 安全性**。 請注意自動化評量清單 (包括 AWS 的自動化評量)，以及每個評量細項提供的資訊，包括資源類型、失敗的資源和合規性工作站。 選取列出的評量。  您可在此看到包括描述、補救步驟和受影響資源等資訊。
    1. 選取畫面右上角的 **X** 來關閉頁面。
    1. 在左側導覽面板中，選取 [概觀]****，返回適用於雲端的 Microsoft Defender [概觀] 頁面。
    1. 將 [適用於雲端的 Microsoft Defender 概觀] 頁面保持開啟，下一項工作將會用到。

### 工作 2

請回想一下，適用於雲端的 Microsoft Defender 提供兩種模式：適用於雲端的 Microsoft Defender 方案提供沒有增強式安全性功能 (免費) 和有增強式安全性功能。 在這項工作中，將探索如何啟用/停用各個適用於雲端的 Microsoft Defender 方案。

1. 從 [適用於雲端的 Microsoft Defender 概觀] 頁面，展開 **[管理**]，然後從左側導覽面板中選取 **[環境設定**]。
1. 選取 [全部展開]**** 方塊，然後選取黃色金鑰圖示旁所列的 [MOC 訂用帳戶--lodXXXXXXXX]**** 訂用帳戶。
1. 在 Defender 方案的頁面上，注意可以選取啟用所有，或選取個別的 Defender 方案。 
    1. 確認 CSPM 狀態已設為 [開啟]****，如果沒有，請立即加以設定。  
    1. 啟用伺服器的方案。  針對 [伺服器] 細項選取 [開啟]****，然後從頁面頂端選取 [儲存]****。
1. 選取視窗左上角顯示 Microsoft Azure 藍色列下方的 [首頁]****，即可返回 Azure 服務首頁。
1. 保持在瀏覽器中開啟 Azure 索引標籤。

### 檢閱

在本實驗中，您探索了適用於雲端的 Microsoft Defender。
