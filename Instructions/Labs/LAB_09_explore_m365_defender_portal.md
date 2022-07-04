---
lab:
  title: 探索 Microsoft 365 Defender 入口網站
  module: 'Module 3 Lesson 4: Describe the capabilities of Microsoft security solutions: Describe threat protection with Microsoft 365 Defender'
ms.openlocfilehash: 5accd8bc5c37450e40dfb73b5f2cf0bb8cb24525
ms.sourcegitcommit: a69acc26ed3a09cea4a3af95719a6edc7fe2814d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/29/2022
ms.locfileid: "146649978"
---
# <a name="lab-explore-the-microsoft-365-defender-portal"></a>實驗室：探索 Microsoft 365 Defender 入口網站

## <a name="lab-scenario"></a>實驗案例

在本實驗中，您將透過逐步了解登錄頁面顯示的內容，探索 Microsoft 365 Defender 入口網站。 您也將會探索導覽面板上可以快速存取功能的選項，此功能是 Microsoft 的 Extended Detection and Response (XDR) 解決方案的一部分：適用於端點的 Microsoft Defender 及適用於 Office 365 的 Microsoft Defender (電子郵件及共同作業)。  最後，您也將探索 Microsoft 安全分數如何協助組織改善其安全性態勢。

**預估時間**：10-15 分鐘

### <a name="task-1"></a>工作 1

探索 Microsoft 365 Defender 登錄頁面。

1. 開啟 Microsoft Edge。 在網址列輸入 **admin.microsoft.com**。

1. 登入管理員認證。
    1. 在登入視窗中輸入 **admin@WWLxZZZZZZ.onmicrosoft.com** (其中的 ZZZZZZ 是實驗代管提供者所提供的唯一租用戶識別碼)，然後選取 [下一步]。

    1. 輸入應由您的實驗託管提供者提供的管理員密碼。 選取 [登入]。
    1. 當提示保持登入狀態時，請選取 **是**。 這將帶您前往 Microsoft 365 系統管理中心頁面。

1. 從 Microsoft 365 系統管理中心左側的瀏覽窗格，選取 [安全性]。  如果沒有看到安全性列出，請選取 [全部顯示]，然後選取 [安全性]。  全新瀏覽器頁面將開啟前往至 Microsoft 365 Defender 入口網站的歡迎頁面。  

1. 如果這是您第一次造訪 Microsoft 365 Defender 入口網站，可能會有彈出視窗引導您快速導覽。  建議您完成導覽。  請選取 **快速導覽**。  讀取每個快顯示窗中提供的說明，然後選取 **下一步**。 持續進行導覽直至結束，然後請選取 **完成**。

1. 左側瀏覽面板提供一部分 Microsoft 的 Extended Detection and Response (XDR 解決方案) 的資訊連結/存取，包含事件與警示、搜捕、控制中心、威脅分析、安全分數等等。  也包括適用於端點的 Microsoft Defender (連結列於端點下方) 及適用於 Office for 365 的 Defender (連結列於電子郵件與共同作業下方) 的快速存取。  透過選取部分連結來探索這些選項。   若要退回 Microsoft 365 Defender 入口網站首頁，請選取左側導覽面板上的 **首頁**。  備註：因為沒有連結的裝置，所以這些索引標籤可能不會列出太多資訊，也不會有任何作用中的威脅或警示。

1. Microsoft 365 Defender 入口網站的歡迎頁面會顯示安全性團隊需要的許多常見卡片。 卡片和資料的組成會依使用者角色有所不同。 請捲動頁面，檢視您身為全域系統管理員角色的預設卡片組。

1. 顯示的卡片可依照您的偏好自訂。  請選取 **+ 新增卡片**。 這會開啟一個視窗，顯示您的首頁上已經有所有卡片。  請選取視窗右上角的 **X** 關閉此視窗。

1. 選取任何卡片右上角的省略符號，將會提供您更多可採取的動作。  

1. 您也可以移動這些卡片。 將游標移到任何卡片的標題列上，當游標變成十字圖形時，選取該卡片並移動到想要的位置上。

1. 選取卡片的標題將會引導您至該主題的其他資訊。 您將在下一個工作中探索它。  保持瀏覽器視窗為開啟狀態。

### <a name="task-2"></a>工作 2

在本工作中，您將探索 Microsoft 安全分數如何協助組織改善其安全性態勢。

1. 在 Microsoft 365 Defender 入口網站的歡迎頁面上，請在卡片的標題列選取 **Microsoft 安全分數** (文字會變成藍色)。  或者，您也可以在左側導覽面板選取 **安全分數**。

1. Microsoft 安全分數頁面會開啟至「概覽」索引標籤。Microsoft 安全分數是一個組織的安全性態勢量值。您的組織安全分數會以百分比顯示，也會顯示您從可能的滿分得到的分數，並依照類別分別計算。 選取您安全分數旁的 [包含]。  隨即會開啟一個小視窗，讓您能夠在組織的安全分數明細中，納入可達成的分數、規劃的分數，以及目前的授權分數。  再次選取 [包含]，關閉該視窗。

1. 概覽頁面也包含重要改進動作、比較分數、記錄及其他資源。

1. 請選取頁面上方的 **改進動作**。  請注意資料表中每個項目的可用資訊，其中包括分數影響和獲得的分數。  

1. 選取清單中的項目已提供詳細資訊。  選取 **要求管理角色的 MFA**。  選取 [編輯狀態與動作計劃]。  在開啟的視窗中，注意可用的狀態選項。 請選取右上角的 **X**，關閉此視窗

1. 從頁面底部選取 [在 Microsoft Azure 中管理]。  新的瀏覽器索引標籤會開啟，直接引導您到[條件式存取原則]頁面。  如果您已完成「條件式存取」實驗練習，您應該會看到已列出的原則。 退回瀏覽器上的 Microsoft 安全分數索引標籤，以退回要求管理角色的 MFA 的改進動作頁面。 在視窗右上角選取 **X** 以關閉此視窗，退回改進動作頁面。

1. 請選取頁面上方的 **記錄** 索引標籤。  部分活動可能會顯示負的分數。  同活動欄位所述，這可能是因為不再相關的項目遭到移除所致。  在記錄資料表中選取一個項目。  所選項目的詳細資料頁面會隨即開啟。  探索可用的選項。  若要結束 [詳細資料] 頁面並返回 [歷程記錄] 頁面，請選取頁面右上角的 **X**。

1. 在頁面上方選取 **計量與趨勢**。  請注意可用的資訊。  從頁面的右上角，請選取 **行事曆圖示**。  您可以縮小檢視為自訂的日期範圍。  選取 **篩選條件圖示**，您可以依照「身分識別」、「裝置」及/或應用程式來篩選檢視的內容。  關閉視窗並在左側導覽面板選取 **首頁**，退回 Microsoft 365 Defender 首頁。

1. 關閉所有已開啟的瀏覽器索引標籤。

### <a name="review"></a>檢閱

在本實驗中，您已透過登錄頁面顯示的內容探索 Microsoft 365 Defender 入口網站，也探索了導覽面板上的選項，導覽面板提供功能的快速存取權，這些功能包含一部分 Microsoft 的 Extended Detection and Response (XDR 解決方案)、適用於端點的 Microsoft Defender 及適用於 Office 365 的 Microsoft Defender (電子郵件與共同作業)。  最後，您已探索 Microsoft 安全分數如何協助組織改善其安全性態勢。
