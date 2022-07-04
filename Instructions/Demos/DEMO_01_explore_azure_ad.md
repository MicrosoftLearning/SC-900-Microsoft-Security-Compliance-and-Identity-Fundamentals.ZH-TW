---
Demo:
  title: Azure Active Directory 使用者設定
  module: 'Module 2 Lesson 1: Describe the capabilities of Microsoft Identity and access management solutions: Explore the services and identity types of Azure AD'
ms.openlocfilehash: 061dfa556f7e4e00d63c938b52097e0b641fed4f
ms.sourcegitcommit: b8b861a8c884a56f094213e47a59be48ba898ca1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/29/2022
ms.locfileid: "146741888"
---
# <a name="demo-azure-active-directory-user-settings"></a>示範：Azure Active Directory 使用者設定

## <a name="demo-scenario"></a>示範案例

在本示範中，您將會存取 Azure Active Directory 並逐步了解現有使用者的多樣設定。  演示者注意事項：本示範會透過 Microsoft 365 租用戶存取 Azure AD。 您也可以透過 Azure 入口網站存取 Azure AD，來向學習者演示。 透過 Microsoft 365 租用戶存取的目的，是為了展示 Microsoft 365 包含 Azure AD 的存取權。

1. 開啟 Microsoft Edge。

1. 在網址列中輸入 **admin.microsoft.com** 存取 Microsoft 365 系統管理中心。

1. 登入管理員認證。
    1. 在登入視窗中輸入 **admin@WWLxZZZZZZ.onmicrosoft.com** (其中的 ZZZZZZ 是實驗代管提供者所提供的唯一租用戶識別碼)，然後選取 [下一步]。
    1. 輸入應由您的實驗託管提供者提供的管理員密碼。 選取 [登入]。
    1. 當提示保持登入狀態時，請選取 **是**。

1. 從 Microsoft 365 系統管理中心的左側導覽窗格中，選取 **顯示全部**。

1. 在系統管理中心下方選取 **Azure Active Directory** (可能需要向下捲動)。  全新瀏覽器頁面將開啟前往至 Azure Active Directory 系統管理中心的 [我的儀表板] 頁面。 在儀表板的主視窗中，您將會看到數個圖格，包括組織身分識別圖格 (Contoso、租用戶與 Azure AD 版本)、使用者與群組圖格等等。

1. 在左側導覽窗格中選取 **使用者**。 請注意，已透過使用者設定了您的租用戶。

1. 在使用者清單中選取 **Adele Vance**。

1. 請注意，左側導覽面板中已選取 **設定檔**。  與顯示在設定檔頁面的資訊展示/對話。

1. 在左側導覽面板中選取 **已指派角色**。  此使用者無任何已指派的管理員角色。  在頁面上方選取 **+ 新增作業**，顯示可用的管理員角色類型。  請勿新增任何項目，只要選取頁面右上角的 **X** 關閉頁面即可。

1. 在左側導覽面板中選取 **群組**。  此使用者是多個群組的成員。  在此您可以與群組類型對話。  若要新增此使用者到其他群組，只要選取 **+ 新增成員資格**。  請勿新增任何新群組，只要知道新增使用者到現有群組有多容易就好。 請選取頁面右上角的 **X** 關閉群組視窗。

1. 在左側導覽面板中選取 **授權**。 請注意，此使用者已被指派 Microsoft 365 E5 授權及 EMS 授權。  若要新增授權，請選取主視窗上方的 **+ 指派**。  顯示此使用者的授權。 請勿變更任何項目。  請選取頁面右上角的 **X** 關閉此視窗。

1. 在左側導覽面板中選取 **裝置**。  無顯示任何內容，但是如果此使用者有指派裝置，則會顯示在這裡。

1. 在左側導覽面板中選取 **Azure 角色指派**。  呼叫：
    1. 這和先前顯示的指派角色索引標籤不同，先前的索引標籤是在 Azure Active Directory 中用於角色型存取控制 (強調 Active Directory)。
    1. 在此索引標籤中，您可以檢視 Azure 資源指派給使用者的角色指派。 例如，如果您要建立一個 Azure 資源群組，而您指派給 Adele 一個特定角色 (例如資源群組的擁有者或參與者)，您會看到列在此處的角色。 這是 Azure 角色型存取控制 (Azure RBAC) 的一部分。 角色指派被管理為特定資源的一部分。

1. 在左側導覽面板中選取 **驗證方法**。  呼叫下列的描述：「在此您可以設定電話號碼與電子郵件地址，使用者用它們來執行多重要素驗證及自助式密碼重設，並重設使用者密碼」。 如果使用者設定為 SSPR，或必須使用 MFA，則您以管理員身分填入後它們即會登錄，不需要透過 SSPR 或 MFA 的登錄步驟。  相比管理員採取此動作，使用者自行登錄更常見。

1. 在左側導覽面板中選取 **登入**。在此處您可以檢視此使用者的登入活動。  您可能看不到此使用者的任何資訊，因為對方尚未登入。

1. 按一下頁面右上角的 **X**。 這會讓您退回使用者清單。  在關閉使用者清單前，您會注意到 MFA 顯示在頁面上方。  選取 [多重要素驗證]。  這會開啟新的瀏覽器視窗。  在此處您可以為使用者選取多個 MFA。  這是您為使用者啟用 MFA 的一種方式。  我們會在「條件式存取」的內文中進一步說明 MFA，提供更多 MFA 的細微控制措施。  關閉多重要素驗證的瀏覽器索引標籤。

1. 按一下頁面右上角的 **X**。 這會讓您退回 Contoso 用戶的主頁面。

### <a name="review"></a>檢閱

在此示範中，您已了解現有使用者的設定，包含使用者可被指派到的群組、角色顯示狀態，以及使用者授權指派。
