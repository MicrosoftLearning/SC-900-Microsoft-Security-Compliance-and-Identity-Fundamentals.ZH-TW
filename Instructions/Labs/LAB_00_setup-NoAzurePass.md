---
ms.openlocfilehash: 57c3c2d1e24acc7efaab97162e443a664dd76965
ms.sourcegitcommit: 804b98d288b1db2c11a5154b4ded954e87f5ae55
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2022
ms.locfileid: "148119007"
---
<a name="---"></a><!---
---
實驗室：標題：「設定」
---
--->

# <a name="lab-setup"></a>實驗室：安裝程式

## <a name="lab-scenario"></a>實驗案例

此設定實驗室包含啟用 Microsoft 稽核記錄。

**預估時間**：5-10 分鐘

### <a name="setup---enable-microsoft-365-audit-log"></a>設定 - 啟用 Microsoft 365 稽核記錄

在此設定工作中，您將在 Microsoft 365 中啟用稽核記錄功能。  儘管文件表明預設情況下會啟用稽核記錄，但大多數實驗租用戶並未啟用此功能，並且可能需要幾個小時才會生效。  啟用此功能是有效益的，因為 Microsoft 365 使用稽核記錄來獲取原則和分析洞察中識別的使用者洞察和活動。

1. 開啟 Microsoft Edge。 在網址列輸入 **admin.microsoft.com**。

1. 登入管理員認證。
    1. 在登入視窗中輸入 **admin@WWLxZZZZZZ.onmicrosoft.com** (其中的 ZZZZZZ 是實驗代管提供者所提供的唯一租用戶識別碼)，然後選取 [下一步]。
    1. 輸入應由您的實驗託管提供者提供的管理員密碼。 選取 [登入]。
    1. 當提示保持登入狀態時，請選取 **是**。 這將帶您前往 Microsoft 365 系統管理中心頁面。

1. 從 Microsoft 365 系統管理中心的左側導覽窗格中，選取 **顯示全部**。

1. 在系統管理中心下，請選取 **合規性**。  全新瀏覽器頁面將開啟前往至 Microsoft 365 合規性的歡迎頁面。  

1. 從左側導覽面板的解決方案下，選取 **稽核**。  備註：稽核功能也可以透過 Microsoft 365 Defender 首頁進行存取 (先前稱為 Microsoft 365 資訊安全中心)。

1. 驗證是否已選取 **搜尋** 索引標籤 (已畫底線)。

1. 一旦進入稽核頁面後，請稍等 2-3 分鐘。  如果未啟用稽核，您將在頁面頂部看到藍色列，上面寫著開始記錄使用者和管理活動。  請選取 **開始記錄使用者和管理活動**。  若提示您確認必須更新組織設定，請選取 [是]。 啟用稽核後，藍色列則會消失。  如果藍色列不存在，則表示已啟用稽核，無需進一步動作。  另一個確認是否啟用稽核的方式是透過 PowerShell，但是這超出此課程的範圍。

1. 從左側導覽面板中選取 **首頁**，退回 Microsoft 365 合規性中心的首頁。

### <a name="review"></a>檢閱

在此設定中，您啟用了 Microsoft 365 中的稽核記錄功能。