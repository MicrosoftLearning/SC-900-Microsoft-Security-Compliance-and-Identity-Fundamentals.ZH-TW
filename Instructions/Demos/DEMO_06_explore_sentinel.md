---
Demo:
  title: Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: 15788d59891cea9ae5c3117e9c79c7bc60bc2806
ms.sourcegitcommit: c14538b208890797642cfe5c35abf6bea45364bf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/15/2022
ms.locfileid: "142614431"
---
# <a name="demo-microsoft-sentinel"></a>示範：Microsoft Sentinel 

### <a name="demo-scenario"></a>示範案例
在此示範中，會逐步引導您建立 Microsoft Sentinel 執行個體的流程。  您也將會設定權限，確保可存取將會部署的資源，以支援 Microsoft Sentinel。  完成此基本設定後，會逐步引您進行將 Microsoft Sentinel 連線至資料來源的相關步驟，並建立監視及視覺化資料的工作手冊。  最後，您將可以展示部分可用的其他選項，包括可獲取任何可疑通知的內建分析、自動化功能等等。

#### <a name="pre-demo-setup--create-an-microsoft-sentinel-instance"></a>預先示範設定：建立 Microsoft Sentinel 執行個體

1. 開啟瀏覽器索引標籤的 **首頁-Microsoft Azure**。  如果您先前關閉了索引標籤，請開啟瀏覽器頁面，然後在網址列中輸入 portal.azure.com 並重新登入。

1. 在頁面頂端 Microsoft Azure 旁藍色列的搜尋方塊中，輸入 **Microsoft Sentinel**，然後從搜尋結果中選取 **Microsoft Sentinel**。

1. 從 Microsoft Sentinel 頁面，選取 [建立 Microsoft Sentinel]。

1. 從 [將 Microsoft Sentinel 新增到工作區] 頁面，選取 [建立新的工作區]。

1. 從建立 Log Analytics 工作區的基本索引標籤中，輸入以下內容：
    1. 訂用帳戶：**Azure Pass – 贊助**
    1. 資源群組：請選取 **建立新的**，並輸入名稱 **SC900-Sentinel-RG**，然後選取 **確定**。
    1. 名稱：**SC900-LogAnalytics-workspace**。
    1. 地區：**美國東部** (可能會根據您所在的位置選取不同預設區域)
    1. 選取 [下一步：**標籤 >]**

1. 對於標記，您可以將其留為空白，然後選取 **檢閱 + 建立**。

1. 驗證您所輸入的資訊，然後選取 **建立**。

1. 列出新工作區可能需要一至兩分鐘的時間，若仍未看見，請選取 **重新整理**，然後選取 **新增**。

1. 新增工作區之後，[Microsoft Sentinel] | [新聞與指南] 頁面會隨即顯示。  請注意開始使用頁面上所列出的三個步驟。

1. 請保持此頁面開啟，您將在下個工作中使用它。

#### <a name="demo-part-2--with-the-microsoft-sentinel-instance-created-you-will-want-to-make-sure-that-you-have-the-necessary-access-to-the-resources-that-get-deployed-to-support-microsoft-sentinel"></a>示範第 2 部分：建立 Microsoft Sentinel 執行個體後，需要確保對部署的資源具有必要的存取權，以支援 Microsoft Sentinel。  

1. 在搜尋方塊中，在頁面頂部 Microsoft Azure 旁邊的藍色列中，輸入 **資源群組**，然後從搜尋結果中選取 **資源群組**。 指派資源群組等級的角色，可確保該角色將套用於為支援 Azure Sentinel 而部署的所有資源。

1. 從資源群組頁面中，選取以 Microsoft Sentinel 所建立的資源群組 **SC900-Sentinel-RG**。 

1. 在 SC900-Sentinel-RG 頁面中，從左側導覽面板中選取 **存取控制 (IAM)** 。

1. 從存取控制頁面，請選取 **檢視我的存取權**。  MOD 系統管理員，目前的角色為服務管理員。  這將會授與您必要的權限，但在以示範為目的時，可能只需展示 Sentinel 特定角色。  透過選取視窗右上角的 **X** 關閉 MOD 管理員指派視窗。

    1. 在存取控制頁面中，請選取 **+ 新增**，然後選取 **新增角色指派**。

    1. 新增角色指派視窗已開啟。  在搜尋方塊中，輸入 **Microsoft Sentinel** 以檢視與 Microsoft Sentinel 相關的 4 個角色。 
    1. 從列出的任何角色中，選取 [檢視] 以檢視該角色的詳細資料。  作為最佳做法，您應該為角色指派最少的權限。  

    1. 請選取視窗右上角的 [X] 以關閉視窗。

1. 從存取控制頁面，選取視窗右上角的 [X] 以關閉視窗。

#### <a name="demo-part-3--in-this-part-of-the-demo-you-will-walk-through-the-process-of-connecting-microsoft-sentinel-to-your-data-source-to-begin-to-collect-data"></a>示範第 3 部分：這一部分的示範，將引導您逐步了解將 Microsoft Sentinel 連線至資料來源以開始收集資料的流程。

1. 在頁面頂端 Microsoft Azure 旁藍色列的搜尋方塊中，輸入 **Microsoft Sentinel**，然後從搜尋結果中選取 **Microsoft Sentinel**。

1. 從 Microsoft Sentinel 頁面選取以 Microsoft Sentinel 執行個體所建立的工作區 **SC900-LogAnalytics-workspace**。

1. 利用 Microsoft Sentinel 的第一步，是能夠收集資料。 從左側導覽面板中選取 **資料連接器**，在設定下列出。

1. 從資料連接器頁面，向下捲動主要視窗以檢視可用連接器的擴充清單。 在資料連接器頁面的 [搜尋] 方塊中，輸入 **Office 365**，然後選取清單中的 [**Office 365**]。

1. 會隨即開啟 [Office 365 連接器] 視窗。  選取 [開啟連接器頁面]。

1. 從 [Office 365 連接器] 頁面，檢閱視窗左側的 [說明]。

1. 主視窗中的 [指示] 索引標籤會提供 Microsoft Sentinel 與 Office 365 整合所需的先決條件，且這些條件全部都應該顯示綠色的核取記號。   選取 [設定] 下方的 [Exchange] 和 [SharePoint]，然後選取 [套用變更]。  會立即在視窗的左側顯示其連線狀態。

1. 選取視窗右上角的 [X]**X** 以關閉視窗，並返回資料連接器頁面。

1. 在資料連接器頁面的頂部應該會顯示「1 個已連線」，表示您現在已連線至 Office 365。 如果您的畫面中並未顯示該訊息，請選取 [重新整理]。 更新此頁面可能會需要幾分鐘的時間。

1. 請保持此頁面開啟，您將在下個工作中使用它。

#### <a name="demo-part-4--in-this-part-of-the-demo-you-will-walk-through-the-process-of-setting-up-a-workbook-for-office-365-to-visualize-and-monitor-your-data"></a>示範第 4 部分：在此部分的示範中，會逐步引導您進行 Office 365 活頁簿的設定流程，以視覺化和監視您的資料。

1. 從左側導覽面板，請選取 **活頁簿**。

1. 在搜尋方塊中，輸入 Office 365，然後選取 **Office 365**。

1. 從畫面右側開啟的視窗，檢閱說明後再選取畫面底部的 [儲存]，然後選取 [確定] 以將活頁簿儲存到預設位置。  現在，選取 [檢視已儲存的活頁簿]。

1. 會隨即開啟 [Office 365 活頁簿] 的頁面。  選取 [作業: 取消設定] 旁的下拉式箭號，然後選取 [全部]。  現在，選取 [使用者: 查詢擱置中] 旁的下拉式箭號，然後選取 [全部]。  選取 **儲存 (磁片) 圖示**。 請選取視窗右上角的 [X] 以關閉視窗。 資料可能會需要花數分鐘的時間才會在活頁簿中顯示，您可以稍後再回到活頁簿。

1. 從 [活頁簿] 頁面左上角的 [活頁簿]，選取 Microsoft Sentinel。 這會將您帶回到 [概觀] 頁面。

#### <a name="demo-part-5--in-this-part-of-the-demo-you-will-show-some-of-the-options-available-in-sentinel"></a>示範第 5 部分：在此部分的示範中，會對部分 Azure Sentinel 中的選項加以說明。

1. 從左側導覽面板選取 [搜捕]。  在已選取 (加上底線) 的 [查詢] 索引標籤中，選取清單中任何一個查詢。  選取查詢之後，請記下該查詢的相關資訊，包括查詢的程式碼，以及執行查詢的選項，並查看結果。  請勿選取任何項目。

1. 從左側導覽面板選取 [MITRE ATT&CK]。  MITRE ATT&CK 是一種可公開存取的知識庫，提供攻擊者常用策略與技術的相關資訊。 使用 Microsoft Sentinel，您可以依據 MITRE ATT&CK® 架構中的策略與技術，檢視已在工作區中啟用且可供您設定的偵測，以了解組織安全性的涵蓋範圍。  選取矩陣中的任一儲存格，並記下畫面右側中的可用資訊。  

1. 從左側導覽面板選取 [社群]。 Microsoft 的安全性分析師會持續地建立和新增新的活頁簿、劇本、搜捕查詢以及更多的項目，並將這些項目公佈於社群中，以供您用於自有的環境中。 您可以從私人社群 GitHub 存放庫下載範例內容，以建立適用於 Azure Sentinel 的自訂活頁簿、搜捕查詢、筆記本和劇本。  選取 [上線社群內容]。  會隨即開啟新的 GitHub 存放庫索引標籤，您可以在其中下載啟用案例所需的內容。  返回至瀏覽器中的 Azure 索引標籤。

1. 從左側導覽面板，請選取 **分析**。  選取 [Advanced Multistage Attack Detection] \(進階多階段攻擊偵測\) 清單中的第一個專案。  記下詳細的資訊。  Microsoft Sentinel 會使用 Fusion (一個以可調整機器學習演算法為基礎的相互關聯引擎) 透過識別在終止鏈結的不同階段中所觀察到異常行為及可疑活動的組合，以自動偵測多階段的攻擊 (也稱為進階持續性威脅)。 以這些探索為基礎，Microsoft Sentinel 就能產生出其他方法難以攔截的事件。

1. 從左側導覽面板，請選取 **自動化**。  您可以在這裡建立簡單自動化規則，與現有的劇本整合，或建立新的劇本。  選取 [+ 建立]，然後選取 [自動化規則]。  請留意畫面右側中開啟的視窗，以及可用來建立條件及動作的選項。  選取畫面底部的 [取消]。

1. 從左側導覽面板，請選取 **活頁簿**。 從活頁簿頁面中，請選取搜尋方塊上方的 **我的活頁簿** 索引標籤。  會列出您先前儲存的活頁簿，可供您檢視和監視資料。  選取 [Office 365]，然後從畫面右側開啟的視窗中，選取 [檢視已儲存的活頁簿]。  記下與 Office 365 工作負載相關的視覺效果。  

1. 請選取視窗右上角的 [X] 以關閉視窗。

1. 選取視窗左上角藍色列下方的 [首頁]，即可返回 Azure 入口網站的首頁。

#### <a name="task-6-post-course-delivery-tear-down-microsoft-sentinel-is-billed-based-on-the-volume-of-data-ingested-for-analysis-in-microsoft-sentinel-although-the-amount-of-data-ingested-as-a-result-of-this-demo-is-minimal-it-is-recommended-that-you-delete-the-microsoft-sentinel-resource-group-when-you-are-done-exploring-the-capabilities-of-microsoft-sentinel"></a>工作 6：課程結束後的清理作業。 Microsoft Sentinel 的計費方式，取決於 Microsoft Sentinel 中分析所取用的資料量。 雖然，這個示範中所內嵌的資料量很小，但仍建議在完成探索 Microsoft Sentinel 的功能特性之後，刪除 Microsoft Sentinel 資源群組。

1. 請從 Microsoft Sentinel 頁面左上角的 Microsoft Sentinel，選取 [所有服務]。

2. 在篩選服務方塊中，輸入資源群組，然後從提供的清單中選取 **資源群組**。

3. 從 [資源群組] 頁面中，選取以 Microsoft Sentinel 所建立的資源群組 **SC900-ResourceGroup**。

4. 從頁面的頂部中心，請選取 **刪除資源群組**。  檢閱警告。  輸入資源群組名稱 **SC900-ResourceGroup**，然後從頁面底部選取 **刪除**。  刪除資源群組需要幾分鐘的時間。

5. 驗證資源群組已刪除後，請關閉瀏覽器頁面。 

#### <a name="review"></a>檢閱

在本示範中，您已完成將 Microsoft Sentinel 連線至資料來源的各個步驟、設定活頁簿，並已使用 Microsoft Sentinel 中幾個可用的選項。