---
Demo:
  title: 適用於雲端的 Microsoft Defender'
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: b9cf202b9aef7f700b08c1dd6f55444d328fac9a
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557335"
---
# <a name="demo-microsoft-defender-for-cloud"></a>示範：適用於雲端的 Microsoft Defender

## <a name="demo-scenario"></a>示範案例

在本示範中，將引導您逐步了解適用於雲端的 Microsoft Defender，並會展示如何利用 Azure 安全分數，改善組織的安全性態勢。

1. 開啟瀏覽器索引標籤的 **首頁-Microsoft Azure**。  如果您先前關閉了索引標籤，請開啟瀏覽器頁面，然後在網址列中輸入 portal.azure.com 並重新登入。

1. 在頁面頂端 Microsoft Azure 旁藍色列的搜尋方塊中，輸入 **適用於雲端的 Microsoft Defender**，然後從搜尋結果中選取 **適用於雲端的 Microsoft Defender**。

1. 如果這是首次使用您的訂閱進入適用於雲端的 Microsoft Defender，會進入 [開始使用] 頁面，並會提示您要升級。  將頁面往下捲動，並選取 **略過**。

1. 請注意適用於雲端的 Microsoft Defender 概觀頁面上所提供的資訊。  注意：您可能會在頁面上方看到藍色的資訊方塊，顯示您可能正在檢視受限的資訊。  請勿選取該項目 (處理過程可能長達 15 分鐘，結果與此示範無異)。

1. 頁面上方的資訊包含 Azure 訂用帳戶數、已評估資源數、作用中建議數，以及任何安全性警示。  頁面主體有一些卡片，代表 [安全分數]、[法規合規性]、[見解] 等等。  

1. 請在頁面上方選取 **已評估的資源**。  (請注意，這相當於從 [適用於雲端的 Microsoft Defender] 首頁左側的瀏覽面板，選取 [清查])。
    1. 這會將您導覽至 **詳細目錄** 頁面，顯示您的 Azure Pass 訂用帳戶。  請選取 **Azure Pass – 贊助**。
    1. [資源健康狀態] 頁面會提供一份建議清單。  在可用的清單上，選取 **應有多位擁有者被指派至您的訂用帳戶**。
    1. 選取 [補救步驟] 旁的下拉式箭頭。 請注意提供的詳細補救步驟以及採取動作的選項。  
    1. 從畫面左上角選取 [適用於雲端的 Microsoft Defender]，返回 [適用於雲端的 Microsoft Defender 概觀] 頁面。

1. 請在頁面上方選取 **作用中建議**。  (請注意，這相當於從 [適用於雲端的 Microsoft Defender] 首頁左側的瀏覽面板，選取 [建議])。
    1. 建議頁面會顯示 [安全分數] 儀表板。
    1. [安全分數] 儀表板下方有控制措施清單。 每個安全性控制措施代表應降低的安全性風險，也包含與該控制措施有關的最高分數、目前分數、可能提高的分數以及資源健康狀態的資訊。  
    1. 選取其中一個控制措施，例如 **啟用 MFA**。  選取其中一個子項目，例如 **應在具有訂用帳戶擁有者權限的帳戶上啟用 MFA**。  在開啟的頁面中，您會看到描述項、補救步驟以及受影響的資源。 請選取螢幕右上角的 **X** 離開此頁面。
    1. 請選取螢幕右上角的 **X** 離開建議頁面，退回概覽頁面。

1. 如此會返回 [適用於雲端的 Microsoft Defender 概觀] 頁面。  從主頁面中選取 [安全分數] (相當從左側的瀏覽面板選取 [安全分數])。
    1. 這會將您導覽至 [安全分數] 儀表板。  除此之外，也列出任何可用的管理群組與月費方案。  選取您的 [Azure 月費方案 – Azure Pass – 贊助]。
    1. 這會將您導覽至先前顯示的 [建議] 頁面。
    1. 請選取螢幕右上角的 **X** 離開 [建議] 頁面。
    1. 請選取螢幕右上角的 **X** 離開 [安全分數] 頁面，退回概覽頁面。

1. 如此會返回 [適用於雲端的 Microsoft Defender 概觀] 頁面。  在主頁面中選取 **法規合規性**。 (請注意，這相當於從 [適用於雲端的 Microsoft Defender] 首頁左側的瀏覽面板，選取 [建議])。
    1. [法規合規性] 頁面提供合規性控制措施清單。  在每個控制措施下方有一組以 Azure 安全性效能評定為基礎的評量，為您提供在 Azure 上保護雲端解決方案的建議。
    1. 選取 [IM 身分識別管理]，然後選取 [IM-6 使用增強式驗證控制]。  此清單顯示可用於改善合規性態勢的客戶責任動作。
    1. 請選取螢幕右上角的 **X** 關閉頁面，退回法規合規性頁面。
    1. 請選取螢幕右上角的 **X** 退回概覽頁面。

1. 請選取頁面左上角的 **首頁** 退回 Azure 入口網站首頁。  請保留此瀏覽器索引標籤，在稍後的示範中您將會回到這裡。

## <a name="review"></a>檢閱

在本示範中，已引導您逐步了解適用於雲端的 Microsoft Defender，並已展示如何利用 Azure 安全分數，改善組織的安全性態勢。
