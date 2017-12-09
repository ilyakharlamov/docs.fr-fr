---
title: "CorDebugGCType, énumération"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugGCType
api_location: mscordbi.dll
api_type: COM
f1_keywords: CorDebugGCType
helpviewer_keywords: CorDebugGCType enumeration [.NET Framework debugging]
ms.assetid: 880ca92a-42d4-42a5-9b9c-c2848eb39c6a
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 14d6f28c2e5fa356c7f406ffb4c2787f0ace500a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2017
---
# <a name="cordebuggctype-enumeration"></a><span data-ttu-id="1a795-102">CorDebugGCType, énumération</span><span class="sxs-lookup"><span data-stu-id="1a795-102">CorDebugGCType Enumeration</span></span>
<span data-ttu-id="1a795-103">Indique si le récupérateur de mémoire s'exécute sur une station de travail ou sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="1a795-103">Indicates whether the garbage collector is running on a workstation or a server.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1a795-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a795-104">Syntax</span></span>  
  
```  
typedef enum CorDebugGCType {  
    CorDebugWorkstationGC  = 0,  
    CorDebugServerGC       = ( CorDebugWorkstationGC + 1 )  
} CorDebugGCType;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1a795-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a795-105">Parameters</span></span>  
  
## <a name="members"></a><span data-ttu-id="1a795-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1a795-106">Members</span></span>  
  
|<span data-ttu-id="1a795-107">Nom de membre</span><span class="sxs-lookup"><span data-stu-id="1a795-107">Member name</span></span>|<span data-ttu-id="1a795-108">Description</span><span class="sxs-lookup"><span data-stu-id="1a795-108">Description</span></span>|  
|-----------------|-----------------|  
|`CorDebugWorkstationGC`|<span data-ttu-id="1a795-109">Le garbage collector s’exécute sur une station de travail.</span><span class="sxs-lookup"><span data-stu-id="1a795-109">The garbage collector is running on a workstation.</span></span>|  
|`CorDebugServerGC`|<span data-ttu-id="1a795-110">Le garbage collector s’exécute sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="1a795-110">The garbage collector is running on a server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1a795-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a795-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a795-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1a795-112">Requirements</span></span>  
 <span data-ttu-id="1a795-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1a795-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a795-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1a795-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1a795-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1a795-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1a795-116">**Versions du .NET framework :**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a795-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a795-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a795-117">See Also</span></span>  
 [<span data-ttu-id="1a795-118">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="1a795-118">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)