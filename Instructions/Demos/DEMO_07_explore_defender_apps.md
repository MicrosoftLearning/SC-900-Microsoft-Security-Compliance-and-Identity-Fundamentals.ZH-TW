---
Demo:
  title: 'Microsoft Defender for Cloud Apps '
  module: 'Module 3 Lesson 4: Describe the capabilities of Microsoft security solutions: Describe threat protection with Microsoft 365 Defender'
ms.openlocfilehash: f653c14f8383ef3c5823d9c4626e7d6c3a693df8
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893878"
---
# <a name="demo-microsoft-defender-for-cloud-apps"></a>示範：Microsoft Defender for Cloud Apps

### <a name="demo-scenario"></a>示範案例
在本示範中，您將展示 Microsoft Defender for Cloud Apps 的功能。  您將會帶領學員了解 Cloud Discovery 儀表板上的可用資訊以及用來調查結果的可用功能，並透過原則控制對組織造成的影響。  注意：組織必須要有授權，才可使用以使用者訂閱數計費的服務 Microsoft Defender for Cloud Apps。  

#### <a name="demo-part-1-explore-cloud-discovery"></a>示範第 1 部分：探索 Cloud Discovery。

1. 開啟 Microsoft Edge。 在網址列輸入 **admin.microsoft.com**。  您應已經用管理員的身分登入。如果尚未登入，請用管理員認證登入。

1. 從 Microsoft 365 系統管理中心的左側導覽窗格中，選取 **顯示全部**。  了解不同的 Microsoft 365 系統管理中心可以從這裡存取。

1. 在系統管理中心下，請選取 **安全性**。  全新瀏覽器頁面將開啟前往至 Microsoft 365 Defender 入口網站的歡迎頁面。  

1. 如果這是您第一次造訪 Microsoft 365 Defender 入口網站，可能會有彈出視窗引導您快速導覽。  請關閉該視窗。

1. 從 Microsoft 365 Defender 頁面的左側導覽面板下方，選取 **更多資源**。

1. 在 **Microsoft Defender for Cloud Apps** 上，選取 [開啟]。  新的瀏覽器頁面會開啟至 Cloud App Security 儀表板。  請注意可用的資訊卡片。  卡片上可能不會有任何資訊，因為這是預先設定的實驗用戶環境，尚未真正使用。  

1. 在左側導覽面板選取 **探索**，接著從下拉式列表選取 **Cloud Discovery 儀表板**。  儀表板包括已探索的應用程式概覽、應用程式類別、風險層級等。  

    1. 在 Cloud Discovery 頁面上方選取 **已探索的應用程式** 索引標籤。已探索的應用程式視窗會提供有關已探索的應用程式更詳細的檢視內容，包括風險分數、流量及使用者數量等。

        1. 在清單上的任何項目上，選取資料表的動作欄位中的 **省略符號**。  請注意可用的多個選項，包括標記應用程式為「獲批准」或「待批准」的能力。  再次選取省略符號，關閉動作方塊。

        1. 選取特定的條項，會開啟特定應用程式的詳細資料頁面。  選取清單中的項目。  針對已選取的項目，瀏覽詳細資料頁面上方的每個索引標籤：**使用方式**、**資訊、IP**、**位址**、**使用者** 及 **警示**。 當您完成探索詳細資料頁面時，請在左側的導覽面板中選取 **已探索的應用程式** 來退回至已探索的應用程式。

    1. 在頁面上方選取 **IP 位址** 索引標籤 (這相當於在左側導覽窗格選取 IP 位址)。  在此處您會依照位址找到的資料，包括交易量、流量與上傳量。  請注意，您也可以根據特定 IP 位址進行篩選，或匯出資料進行進一步分析。

    1. 在頁面上方 (或左側導覽窗格) 選取 **使用者**。  這與選取 IP 位址 時提供的資料類型相同，但這是為了單一使用者而列出的內容。  再次依據特定使用者進行篩選，並匯出資料進行進一步分析。

1. 這些索引標籤中提供的資訊是依據您手動自防火牆與 Proxy 上傳的流量記錄快照報告，或是來自利用 Cloud App Security 分析從網路轉寄的所有記錄的連續報告。  若要檢視設定的位置，請選取頁面右上角的 **省略符號**。

    1. 選取第一個選項，**建立 Cloud Discovery 快照報告**。 此處須填寫要求的詳細資料，並上傳流量記錄以產生及上傳報告。  選取 [取消]。  您為實驗用戶檢視的資訊來自「快照報告」，此資訊位於螢幕的右上角。

    1. 若要檢視連續報告的選項，請選取頁面右上角的 **省略符號**，在下拉式列表中選取 **設定自動上傳**。  沒有連線的資料來源，您會在此處新增資料來源。 選取 **選取設備** 下拉式箭頭，檢視您可以做為資料來源進行連線的設備類型。  選取 **取消** 已結束。

1. 另一個呼叫的重點是，您可以透過設定應用程式連接器來直接連線至應用程式，提供您更大的可見度與控制雲端應用程式。 在螢幕的左上角選取 **設定齒輪圖示**，並在下拉式列表中選取 **應用程式連接器**。  

    1. 在「連線的應用程式」頁面，清單上的 Office 365 應為已連線狀態。  如果 Office 365 顯示連線錯誤，非常可能是因為「稽核」未開啟。

    1. 選取 **+ 連線至應用程式**，在下拉式清單中選取 **Microsoft Azure**。  在 Microsoft Azure 彈出視窗中選取 **連線至 Microsoft Azure**。  您將會看到已連線狀態，以及掃描使用者、資料與活動的資訊。  請選取 **關閉按鈕**。

1. 請保持此頁面開啟，您將在下個工作中使用它。

#### <a name="demo-part-2-explore-ways-in-which-you-can-investigate-the-recorded-activities"></a>示範第 2 部分：探索調查記錄活動的方式。

1. 從左側導覽面板的 **調查** 下方，選取 **活動記錄**。  您可以在此檢視已連線應用程式的所有活動。   因為您已經完成 Office 365 連接器的連線，應可檢視部分資料。 當您將 Cloud App Security 連線到使用應用程式連線程式的應用程式後，Cloud App Security 會掃描發生的所有活動 (每個應用程式的追溯掃描時段都不相同)，再以新的活動不斷更新。  

1. 選取一個項目，顯示更詳細的資訊。 請注意頁面上方，從搜尋新增新的原則，或匯出資料進行進一步分析的選項。  選取 **+ 來自搜尋的新原則**。  請注意，您可以根據範本建立原則、選取嚴重性與類別、建立原則篩選條件、建立警示，甚至傳送警示至 Power Automate。  選取 **取消** 以結束原則建立視窗。

1. 在左側導覽窗格中，選取與探索 **檔案** 選項，並留意篩選資料、建立檔案原則與檔案匯出的選項。  選取與匯出 **使用者與帳戶** 選項。  請注意篩選資料與資料匯出的選項。

1. 在左側導覽面板中選取「安全性設定」。 此頁面為您的 Azure、Amazon Web Services (AWS) 及 Google Cloud Platform (GCP) 帳戶提供安全性設定評量。

1. 請保持此頁面開啟，您將在下個工作中使用它。


#### <a name="demo-part-3-in-this-task-you-will-explore-the-policies-and-alerts-pages-in-microsoft-defender-for-cloud-apps"></a>示範第 3 部分：在此工作中，您將會探索 Microsoft Defender for Cloud Apps 中的原則與警示頁面。

1. 從左側導覽面板的「控制」下方，選取 **原則**。  所列出的原則提供有關該原則、嚴重性等所產的警示數目相關資訊。選取任何條項，都可提供有關該原則更詳細的資訊。 選取一個清單項目，例如 **風險性登入**。  

1. 在左側導覽面板中選取 **警示**。  如果您有任何列出的警示，請在警示清單中選取一個項目。 檢閱提供的資訊。  在視窗的右上方選取 **關閉警示** 以檢視關閉警示的選項。  

1. 關閉瀏覽器視窗。

#### <a name="review"></a>檢閱
在本示範中，您將展示 Microsoft Defender for Cloud Apps 的功能。  您已展示 Cloud Discovery 儀表板上的可用資訊以及用來調查結果的可用功能，並透過原則控制對組織造成的影響。