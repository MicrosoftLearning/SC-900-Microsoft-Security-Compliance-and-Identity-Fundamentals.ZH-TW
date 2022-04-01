---
lab:
  title: 探索 Microsoft Intune
  module: 'Module 3 Lesson 6: Describe the capabilities of Microsoft security solutions: Describe endpoint security with Microsoft Intune'
ms.openlocfilehash: 648343111d82426fe30e1ceeed4e91062649fbcd
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893823"
---
# <a name="lab-explore-microsoft-intune"></a>實驗室：探索 Microsoft Intune

## <a name="lab-scenario"></a>實驗案例

在本實驗中，您將會探索 Microsoft 端點管理員中的 Microsoft Intune。 注意：本實驗執行個體中未設定任何端點或裝置，因此不會顯示任何實際端點資訊。 本示範的目的僅為提供學員可用資訊的指南，以及尋找資訊的方向。  如需更詳細的逐步解說，請參閱相關 Learn 內容中的影片 (<https://www.microsoft.com/en-us/videoplayer/embed/RE4LTIu>) (英文)。

**預估時間**：10-15 分鐘

#### <a name="task-in-this-task-you-will-explore-microsoft-intune-in-microsoft-endpoint-manager"></a>工作：在本工作中，您將會探索 Microsoft 端點管理員中的 Microsoft Intune。

1. 開啟 Microsoft Edge。 在網址列輸入 **admin.microsoft.com**。

1. 登入管理員認證。
    1. 在登入視窗中輸入 **admin@WWLxZZZZZZ.onmicrosoft.com** (其中的 ZZZZZZ 是實驗代管提供者所提供的唯一租用戶識別碼)，然後選取 [下一步]。
    
    1. 輸入應由您的實驗託管提供者提供的管理員密碼。 選取 [登入]。
    1. 當提示保持登入狀態時，請選取 **是**。 這將帶您前往 Microsoft 365 系統管理中心頁面。

1. 從 Microsoft 365 系統管理中心的左側導覽窗格中，選取 **顯示全部**，接著選取 **所有管理員中心**。

1. 在「所有管理員中心」頁面上，選取 **端點管理員**。  新的瀏覽器頁面會開啟於 Microsoft 端點管理員系統管理中心。

1. 在左側的導覽窗格上選取 **儀表板** 以顯示您的 Intune 用戶中的裝置與用戶端應用程式整體詳細資料。

1. 在左側的導覽窗格上選取 **裝置** 以顯示您的 Intune 用戶中的註冊裝置詳細資料。 [裝置 - 概觀]  窗格包含數個索引標籤，可讓您檢視下列狀態和警示的摘要：
    1. **註冊狀態** - 依平台和註冊失敗檢閱 Intune 已註冊裝置的詳細資料。
    
    1. **註冊警示** - 依平台尋找未指派裝置的更多詳細資料。
    1. **合規性狀態** - 根據裝置、原則、設定、威脅和保護來檢閱合規性狀態。 此外，此窗格也會提供沒有合規性政策的裝置清單。
    1. **設定狀態** - 檢閱裝置設定檔的設定狀態，以及設定檔部署。
    1. **軟體更新狀態** - 查看所有裝置和所有使用者的視覺部署狀態。

1. 在「裝置 - 概覽」窗格中，選取 **條件式存取** 以顯示關於存取原則的詳細資料。

1. 在左側的導覽窗格中，選取 **裝置** 後接著選取 **組態設定檔** 以顯示 Intune 中的裝置設定檔詳細資料。

1. 在左側的導覽窗格中，選取 **裝置** 後接著選取 **所有裝置** 以顯示 Intune 用戶註冊裝置的詳細資料。  雖然沒有列出裝置，但是此資料表會顯示關於合規性、作業系統版本及最近簽到日期的重要詳細資料。

1. 從瀏覽窗格，選取 [應用程式]  以顯示應用程式狀態的概觀。 有兩個索引標籤，供您檢視下列狀態的摘要：
    1. **安裝狀態** - 檢視前幾個安裝失敗的裝置，以及安裝失敗的應用程式。
    1. **應用程式防護原則狀態** - 尋找已指派應用程式防護原則的使用者及已標幟的使用者詳細資料。

1. 在「應用程式 - 概覽」窗格中，選取 **所有應用程式** 以檢視已新增到 Intune 的應用程式清單。

1. 在左側的導覽窗格上選取 **使用者** 以顯示您已納入 Intune 的用戶詳細資料。 這些使用者是您的公司與 Contoso 的工作力。

1. 在左側的導覽窗格上選取 **群組** 以顯示已納入 Intune 的 Azure Active Directory (Azure AD) 群組詳細資料。

1. 在左側的導覽窗格上選取 **租用戶系統管理員** 以顯示您的 Intune 用戶的詳細資料。

1. 在左側的導覽窗格上選取 **疑難排解 + 支援**，接著選取 **疑難排解**，在特定的使用者上確認狀態詳細資料。

#### <a name="review"></a>檢閱

在本實驗中，您已探索了 Microsoft 端點管理員中的 Microsoft Intune。 注意：本實驗執行個體中未設定任何端點或裝置，因此不會顯示任何實際端點資訊。 本示範的目的僅為提供學員可用資訊的指南，以及尋找資訊的方向。  如需更詳細的逐步解說，請參閱相關 Learn 內容中的影片 (<https://www.microsoft.com/en-us/videoplayer/embed/RE4LTIu>) (英文)。