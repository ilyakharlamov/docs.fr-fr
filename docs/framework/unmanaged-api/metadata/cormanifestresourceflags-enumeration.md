---
title: "CorManifestResourceFlags, énumération"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorManifestResourceFlags
api_location: mscoree.dll
api_type: COM
f1_keywords: CorManifestResourceFlags
helpviewer_keywords: CorManifestResourceFlags enumeration [.NET Framework metadata]
ms.assetid: 1b0306b7-622b-4b57-8edc-3c713bb147ae
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5cdaba8b1186d1720ff8b64f50a8effc4691fe8c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2017
---
# <a name="cormanifestresourceflags-enumeration"></a><span data-ttu-id="97e97-102">CorManifestResourceFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="97e97-102">CorManifestResourceFlags Enumeration</span></span>
<span data-ttu-id="97e97-103">Indique la visibilité des ressources encodées dans un manifeste d’assembly.</span><span class="sxs-lookup"><span data-stu-id="97e97-103">Indicates the visibility of resources encoded in an assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97e97-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97e97-104">Syntax</span></span>  
  
```  
typedef enum CorManifestResourceFlags {  
  
    mrVisibilityMask        =   0x0007,  
    mrPublic                =   0x0001,  
    mrPrivate               =   0x0002  
  
} CorManifestResourceFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="97e97-105">Membres</span><span class="sxs-lookup"><span data-stu-id="97e97-105">Members</span></span>  
  
|<span data-ttu-id="97e97-106">Membre</span><span class="sxs-lookup"><span data-stu-id="97e97-106">Member</span></span>|<span data-ttu-id="97e97-107">Description</span><span class="sxs-lookup"><span data-stu-id="97e97-107">Description</span></span>|  
|------------|-----------------|  
|`mrVisibilityMask`|<span data-ttu-id="97e97-108">Réservé.</span><span class="sxs-lookup"><span data-stu-id="97e97-108">Reserved.</span></span>|  
|`mrPublic`|<span data-ttu-id="97e97-109">Les ressources sont publiques.</span><span class="sxs-lookup"><span data-stu-id="97e97-109">The resources are public.</span></span>|  
|`mrPrivate`|<span data-ttu-id="97e97-110">Les ressources sont privées.</span><span class="sxs-lookup"><span data-stu-id="97e97-110">The resources are private.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="97e97-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="97e97-111">Requirements</span></span>  
 <span data-ttu-id="97e97-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="97e97-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97e97-113">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="97e97-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="97e97-114">**Versions du .NET framework :**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97e97-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97e97-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e97-115">See Also</span></span>  
 [<span data-ttu-id="97e97-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="97e97-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)