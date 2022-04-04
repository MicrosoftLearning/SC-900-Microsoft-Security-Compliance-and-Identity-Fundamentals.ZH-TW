---
lab:
  title: 探索 Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: c5a7ba866c82f15a4f78099326fd93a734caead8
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893831"
---
# <a name="lab-explore-microsoft-sentinel"></a>實驗室：探索 Microsoft Sentinel 

## <a name="lab-scenario"></a>實驗案例
在此示範中，將引導您逐步了解建立 Microsoft Sentinel 執行個體的流程。  您也將會設定權限，確保可存取將會部署的資源，以支援 Microsoft Sentinel。  完成基本設定後，將引導您逐步了解將 Microsoft Sentinel 連線至資料來源的步驟，以及使用內建分析來取得所有可疑事件的通知，最後將會探索自動化功能。  

  

**預估時間**：30-45 分鐘

#### <a name="task-1--create-an-microsoft-sentinel-instance"></a>工作 1：建立 Microsoft Sentinel 執行個體。

1. 開啟 Microsoft Edge。 在網址列輸入 **portal.azure.com**。

2. 登入管理員認證。
    1. 在登入視窗中輸入 **admin@WWLxZZZZZZ.onmicrosoft.com** (其中的 ZZZZZZ 是實驗代管提供者所提供的唯一租用戶識別碼)，然後選取 [下一步]。
    
    1. 輸入應由您的實驗託管提供者提供的管理員密碼。 選取 [登入]。
    1. 當提示保持登入狀態時，請選取 **是**。

3. 在螢幕左上角的 Microsoft Azure 旁邊，請選取 [顯示入口網站功能表] 圖示 (三條水平線，又稱為漢堡圖示)，接著選取 **所有服務**。  

4. 請在篩選服務方塊中，輸入 **Microsoft Sentinel**，然後從清單中選取 **Microsoft Sentinel**。

5. 從 Microsoft Sentinel 頁面，選取 [建立 Microsoft Sentinel]。

6. 從 [將 Microsoft Sentinel 新增到工作區] 頁面，選取 [建立新的工作區]。

7. 從建立 Log Analytics 工作區的基本索引標籤中，輸入以下內容：
    1. 訂用帳戶：**Azure Pass – 贊助**
   
    1. 資源群組：請選取 **建立新的**，並輸入名稱 **SC900-ResourceGroup**，然後選取 **確定**。
    1. 名稱：**SC900-LogAnalytics-workspace**。
    1. 地區：**美國西部** (保留預設值)
    1. 選取 下一步：**定價層 >**

8. 對於定價層，保留預設值設定：**隨用隨付 (每 GB 2018)** ，然後選取 [下一步：**標籤 >]** 。

9. 對於標記，您可以將其留為空白，然後選取 **檢閱 + 建立**。

10. 驗證您所輸入的資訊，然後選取 **建立**。

11. 如果您未看到已列出的新工作區，請選取 **重新整理**，然後選取 **新增**。

12. 新增工作區之後，[Microsoft Sentinel] | [新聞與指南] 頁面會隨即顯示。  請注意開始使用頁面上所列出的三個步驟。

13. 請保持此頁面開啟，您將在下個工作中使用它。

#### <a name="task-2--with-the-microsoft-sentinel-instance-created-you-will-want-to-make-sure-that-you-have-the-necessary-access-to-the-resources-that-get-deployed-to-support-microsoft-sentinel--in-this-task-you-will-go-to-the-access-control-iam-page-for-the-resource-group-that-you-created-with-the-instance-of-microsoft-sentinel-view-the-available-roles-and-assign-yourself-mod-administrator-the-required-role-assigning-the-role-at-the-resource-group-level-will-ensure-the-role-will-apply-to-all-the-resources-that-are-deployed-to-support-microsoft-sentinel"></a>工作 2：建立 Microsoft Sentinel 執行個體後，需要確保對部署的資源具有必要的存取權，以支援 Microsoft Sentinel。  在此工作中，您將前往利用 Microsoft Sentinel 執行個體所建立的資源群組的存取控制 (IAM) 頁面，檢視可供使用的角色，並為自己 (MOD 系統管理員) 指派所需的角色。 指派資源群組等級的角色，可確保該角色將套用於為支援 Azure Sentinel 而部署的所有資源。

1. 請從 Microsoft Sentinel 頁面左上角的 Microsoft Sentinel，選取 [所有服務]。

2. 在篩選服務方塊中，輸入資源群組，然後從提供的清單中選取 **資源群組**。

3. 從 [資源群組] 頁面中，選取以 Microsoft Sentinel 所建立的資源群組 **SC900-ResourceGroup**。

4. 在 SC900-ResourceGroup 頁面中，從左側導覽面板中選取 **存取控制 (IAM)** 。

5. 從存取控制頁面，請選取 **檢視我的存取權**。  請注意，目前角色為安全性管理員。透過選取視窗右上角的 **X** 關閉 MOD 管理員指派視窗。

6. 在存取控制頁面中，請選取 **+ 新增**，然後選取 **新增角色指派**。

7. 新增角色指派視窗已開啟。  在選取角色欄位中選取下拉式箭頭以顯示可提供使用的角色。  對於此實驗，請選取 **擁有者**。  注意：作為最佳做法，您應該為角色指派最少的權限。  也可檢閱 Microsoft Sentinel 中的權限： https://docs.microsoft.com/en-us/azure/sentinel/roles (機器翻譯) 作為參考

8. 從顯示的使用者清單中，請選取 **MOD 管理員**。

9. 請選取頁面底部的 **儲存**。

10. 在存取控制頁面中，請選取 **檢視我的存取權** 以確認已新增角色，然後透過選取視窗右上角的 **X** 關閉視窗。

11. 透過從頁面左上角選取 **所有服務**，其上方顯示為資源群組，退回至 Azure 的所有服務頁面。

#### <a name="task-3--in-this-task-you-will-walk-through-the-process-of-connecting-microsoft-sentinel-to-your-data-source-to-begin-to-collect-data-note-it-can-take-a-bit-time-to-show-the-connected-status-of-a-connector-30-minutes-depending-on-the-tenant"></a>工作 3：在此作業中，將引導您逐步了解將 Microsoft Sentinel 連線至資料來源以開始收集資料的流程。 請注意：顯示連接器的連線狀態可能需要一些時間 (約 30 分鐘，其取決於租用戶)。

1. 請在 [所有服務] 頁面的篩選服務方塊中，輸入 **Microsoft Sentinel**，然後從結果清單中選取 **Microsoft Sentinel**。 

2. 從 Microsoft Sentinel 頁面選取以 Microsoft Sentinel 執行個體所建立的工作區 **SC900-LogAnalytics-workspace**。

3. 利用 Microsoft Sentinel 的第一步，是能夠收集資料。 從左側導覽面板中選取 **資料連接器**，在設定下列出。

4. 從資料連接器頁面，向下捲動主要視窗以檢視可用連接器的擴充清單。 在資料連接器頁面的搜尋方塊中，輸入 **Azure**，然後從清單中選取 **Azure Active Directory**。

5. Azure Active Directory 連接器視窗已開啟。  選取 [開啟連接器頁面]。

6. 在 Azure Active Directory 連接器頁面中，請檢閱說明並記下相關內容，其中包括活頁簿、查詢和分析規則範本。  

7. 主視窗中的指示索引標籤，提供 Microsoft Sentinel 與 Azure Active Directory 整合的必要條件。   在設定下，請選取 **登入記錄**，然後選取套用變更 (可以選取多個連接器)。

8. 在下一步索引標籤中，請記下建議的活頁簿清單。   在建議的活頁簿下，請選取 **Azure 登入記錄** (可以選取其他活頁簿)。

9. 從活頁簿頁面並選取範本索引標籤 (已畫底線)，請選取 **Azure 登入記錄**。 

10. 從以開啟的 Azure AD 登入記錄視窗中，檢閱說明然後選取 **檢視範本**。  透過選取螢幕右上角的 **X** 退出範本。  從頁面底部選取 **儲存**，然後選取 **確定** 將活頁簿儲存至預設位置。

11. 從 [活頁簿] 頁面左上角的 [活頁簿]，選取 Microsoft Sentinel。 如此您即會返回 Microsoft Sentinel 資料連接器頁面。

12. 資料連接器頁面的頂部應顯示 1 個已連線，以反映您現在已連線至 Azure Active Directory。

13. 從左側導覽面板，請選取 **活頁簿**。

14. 從活頁簿頁面中，請選取搜尋方塊上方的 **我的活頁簿** 索引標籤。  您剛剛儲存的活頁簿已列出，並且可供您檢視和監視資料。

15. 請保持此頁面開啟，您將在下個工作中使用它。

#### <a name="task-4--in-this-task-you-will-walk-through-the-process-of-using-a-built-in-analytics-rule-template-to-create-a-rule-to-get-notified-when-something-suspicious-occurs"></a>工作 4：在此工作中，您將逐步了解使用內建分析規則範本建立規則以在發生可疑事件時取得通知的流程。

1. 從左側導覽面板，請選取 **分析**。

2. 分析頁面將顯示活動規則 (預設情況下啟用進階多階段攻擊偵測)，並提供對規則範本的存取。  請選取 **規則範本** 索引標籤。請注意可用範本的清單以及篩選清單的不同方法。  使用 Microsoft Sentinel 工作區內建的分析警示，可以在發生任何可疑事件時收到通知。

3. 在搜尋列中，請輸入 **Azure 入口網站**。  請選取 **嘗試登入 Azure 入口網站失敗**。  

4. 從開啟的視窗中，閱讀說明並檢閱與範本相關的資訊。  請選取頁面底部的 **建立規則**。

5. 檢閱 [分析規則精靈] 中的資訊，然後選取 [下一步：設定規則邏輯 >]。

6. 設定規則邏輯頁面為定義新分析規則邏輯的位置。 範本已經提供一些邏輯和預先定義的設定。  滾動頁面以查看可用設定。  保留預設值。 選取 [下一步：事件設定 (預覽) >]。

7. Microsoft Sentinel 警示可以透過事件設定，分組到應查看的事件中。 您可以設定此分析規則觸發的警報是否應應該產生事件。  保留預設值設定，然後選取 [下一步：自動回應 >]。

8. 在自動回應索引標籤中，請注意如何新增劇本以進行自動回應。  同樣，您可以建立事件自動化規則。  在事件自動化下，請選取 **+ 新增** 新的。  建立新自動化規則的視窗已開啟。  您在此頁面上建立的任何自動化規則都會由您正在使用的分析規則觸發。請注意，您可以為該規則新增條件和設定動作。   請選取 **取消** 以退出視窗。

9. 選取 [下一步：檢閱 >]，即可視所選範本為何，檢閱與規則相關聯的所有詳細資料。 此時，您可以透過選取建立以 **建立** 規則，或透過選取頁面右上角的 **X** 退出而不建立規則。

10. 請保持此頁面開啟，您將在下個工作中使用它。

#### <a name="task-5--in-the-previous-task-you-created-an-analytics-rule-to-be-alerted-of-suspicious-activities--embedded-in-that-wizard-is-the-option-to-automate-the-response-to-an-incident-based-on-the-specific-rule--but-you-can-also-create-automation-rules-by-going-directly-to-the-automation-configuration-option"></a>工作 5：在上一個工作中，您已建立分析規則，以提醒可疑活動。  該精靈中內嵌基於特定規則自動回應事件的選項。  但是您也可以透過直接前往自動化設定選項來建立自動化規則。

1. 從左側導覽面板，請選取 **自動化**。  

2. 選取 [+ 建立]  。 從下拉式備註中選取如何新增新劇本或新增新規則。  選取 [新增規則]。  

3. 建立新自動化規則的視窗已開啟。  請注意，您可以為規則新增條件和設定動作。  唯一的區別是第一個條件為關聯要套用此自動化規則的分析規則。  這會在上一項工作中以灰階顯示，因為正在為特定規則設定自動化。  請選取 **取消** 以退出建立新的自動化規則視窗。

4. 請保持此頁面開啟，您將在下個工作中使用它。


#### <a name="task-6--delete-microsoft-sentinel-resource-group--microsoft-sentinel-is-billed-based-on-the-volume-of-data-ingested-for-analysis-in-microsoft-sentinel-although-the-amount-of-data-ingested-as-a-result-of-this-lab-is-minimal-it-is-recommended-that-you-delete-the-microsoft-sentinel-resource-group-when-you-are-done-exploring-the-features-of-capabilities-of-microsoft-sentinel"></a>工作 6：刪除 Microsoft Sentinel 資源群組。  Microsoft Sentinel 的計費方式，取決於 Microsoft Sentinel 中分析所取用的資料量。 雖然此實驗作業所取用的資料量非常小，但仍建議在研究完 Microsoft Sentinel 功能的特性後，刪除 Microsoft Sentinel 資源群組。

1. 請從 Microsoft Sentinel 頁面左上角的 Microsoft Sentinel，選取 [所有服務]。

2. 在篩選服務方塊中，輸入資源群組，然後從提供的清單中選取 **資源群組**。

3. 從 [資源群組] 頁面中，選取以 Microsoft Sentinel 所建立的資源群組 **SC900-ResourceGroup**。

4. 從頁面的頂部中心，請選取 **刪除資源群組**。  檢閱警告。  輸入資源群組名稱 **SC900-ResourceGroup**，然後從頁面底部選取 **刪除**。  刪除資源群組需要幾分鐘的時間。

5. 驗證資源群組已刪除後，請關閉瀏覽器頁面。 


#### <a name="review"></a>檢閱

在本實驗中，已引導您逐步了解建立 Microsoft Sentinel 執行個體的流程。  您也已經設定了權限，可確保能存取與 Microsoft Sentinel 執行個體相關聯的資源。  建立 Microsoft Sentinel 執行個體後，您已逐步了解將 Sentinel 連線至資料來源的步驟、使用內建分析規則以取得任何可疑事件的通知，最後已探索了自動化功能。 刪除與所建立之 Microsoft Sentinel 執行個體相關聯的資源群組，此示範即結束。
