---
title: "SaveToHistory (fonction) (référence des API non managées WPF)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: cpp
api_name: SaveToHistory
api_location: PresentationHost_v0400.dll
ms.assetid: 6dd101a3-44ad-4143-b228-772156f9b8ff
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: b30884433f81aa5e4bf1241ae4fe34494bef788e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2017
---
# <a name="savetohistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="d3e9d-102">SaveToHistory (fonction) (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="d3e9d-102">SaveToHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="d3e9d-103">Cette API prend en charge l’infrastructure de Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="d3e9d-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="d3e9d-104">Utilisée par l’infrastructure de Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="d3e9d-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3e9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3e9d-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveToHistory(  
   __in_ecount(1) IStream* pHistoryStream  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d3e9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3e9d-106">Parameters</span></span>  
 <span data-ttu-id="d3e9d-107">pHistoryStream</span><span class="sxs-lookup"><span data-stu-id="d3e9d-107">pHistoryStream</span></span>  
 <span data-ttu-id="d3e9d-108">Pointeur vers le flux de données d’historique.</span><span class="sxs-lookup"><span data-stu-id="d3e9d-108">A pointer to the history stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3e9d-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d3e9d-109">Requirements</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3e9d-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d3e9d-110">Requirements</span></span>  
 <span data-ttu-id="d3e9d-111">**Plateformes :** consultez [configuration système requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d3e9d-111">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3e9d-112">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-112">**DLL:**</span></span>  
  
 <span data-ttu-id="d3e9d-113">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="d3e9d-113">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="d3e9d-114">Dans le .NET Framework 4 et versions ultérieures : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="d3e9d-114">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="d3e9d-115">**Version du .NET framework :**[!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3e9d-115">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3e9d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3e9d-116">See Also</span></span>  
 [<span data-ttu-id="d3e9d-117">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="d3e9d-117">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)