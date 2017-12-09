---
title: "EnumCustomAttributes, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- EnumCustomAttributes
- IALink.EnumCustomAttributes
api_location: alink.dll
api_type: COM
f1_keywords: EnumCustomAttributes
helpviewer_keywords: EnumCustomAttributes method
ms.assetid: 08dff60c-f01b-4050-8865-ea3f95361c9f
topic_type: apiref
caps.latest.revision: "4"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: febaba5155753e9d60a3708582f4f58bd7861ec7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="enumcustomattributes-method"></a><span data-ttu-id="61203-102">EnumCustomAttributes, méthode</span><span class="sxs-lookup"><span data-stu-id="61203-102">EnumCustomAttributes Method</span></span>
<span data-ttu-id="61203-103">Récupère les attributs personnalisés du niveau de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="61203-103">Retrieves assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61203-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61203-104">Syntax</span></span>  
  
```  
HRESULT EnumCustomAttributes(  
    HALINKENUM hEnum,  
    mdToken tkType,  
    mdCustomAttribute rCustomValues[],  
    ULONG cMax,  
    ULONG* pcCustomValues  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="61203-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61203-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="61203-106">Handle de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="61203-106">Handle of enumerator.</span></span>  
  
 `tkType`  
 <span data-ttu-id="61203-107">Type des attributs à énumérer.</span><span class="sxs-lookup"><span data-stu-id="61203-107">Type of attributes to be enumerated.</span></span> <span data-ttu-id="61203-108">Utilisez `mdTokenNill` pour tous les attributs.</span><span class="sxs-lookup"><span data-stu-id="61203-108">Use `mdTokenNill` for all attributes.</span></span>  
  
 `rCustomValues`  
 <span data-ttu-id="61203-109">Reçoit les jetons d’attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="61203-109">Receives custom attributes tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="61203-110">Spécifie la taille de `rCustomValues` tableau.</span><span class="sxs-lookup"><span data-stu-id="61203-110">Specifies size of `rCustomValues` array.</span></span>  
  
 `pcCustomValues`  
 <span data-ttu-id="61203-111">Si vous le souhaitez reçoit le nombre de valeurs de jeton.</span><span class="sxs-lookup"><span data-stu-id="61203-111">Optionally receives count of token values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="61203-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="61203-112">Return Value</span></span>  
 <span data-ttu-id="61203-113">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="61203-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61203-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="61203-114">Requirements</span></span>  
 <span data-ttu-id="61203-115">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="61203-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61203-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61203-116">See Also</span></span>  
 [<span data-ttu-id="61203-117">Interface IALink</span><span class="sxs-lookup"><span data-stu-id="61203-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="61203-118">IALink2 (Interface)</span><span class="sxs-lookup"><span data-stu-id="61203-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="61203-119">ALink (API)</span><span class="sxs-lookup"><span data-stu-id="61203-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)