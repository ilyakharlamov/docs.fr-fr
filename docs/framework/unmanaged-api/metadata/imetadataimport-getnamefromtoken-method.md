---
title: "IMetaDataImport::GetNameFromToken, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.GetNameFromToken
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::GetNameFromToken
helpviewer_keywords:
- GetNameFromToken method [.NET Framework metadata]
- IMetaDataImport::GetNameFromToken method [.NET Framework metadata]
ms.assetid: 32114ecf-8916-4ab2-a201-179c017344f1
topic_type: apiref
caps.latest.revision: "17"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: e77954d5730417a005c6c1ac07fa171bd0f1b13a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportgetnamefromtoken-method"></a><span data-ttu-id="0f188-102">IMetaDataImport::GetNameFromToken, méthode</span><span class="sxs-lookup"><span data-stu-id="0f188-102">IMetaDataImport::GetNameFromToken Method</span></span>
<span data-ttu-id="0f188-103">Obtient le nom UTF-8 de l'objet référencé par le jeton de métadonnées spécifié.</span><span class="sxs-lookup"><span data-stu-id="0f188-103">Gets the UTF-8 name of the object referenced by the specified metadata token.</span></span> <span data-ttu-id="0f188-104">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="0f188-104">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f188-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f188-105">Syntax</span></span>  
  
```  
HRESULT GetNameFromToken (  
   [in] mdToken      tk,  
   [out] MDUTF8CSTR  *pszUtf8NamePtr  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0f188-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f188-106">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="0f188-107">[in] Le jeton qui représente l’objet à retourner le nom.</span><span class="sxs-lookup"><span data-stu-id="0f188-107">[in] The token representing the object to return the name for.</span></span>  
  
 `pszUtf8NamePtr`  
 <span data-ttu-id="0f188-108">[out] Pointeur vers le nom d’objet UTF-8 dans le tas.</span><span class="sxs-lookup"><span data-stu-id="0f188-108">[out] A pointer to the UTF-8 object name in the heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0f188-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f188-109">Remarks</span></span>  
 <span data-ttu-id="0f188-110">`GetNameFromToken` est obsolète.</span><span class="sxs-lookup"><span data-stu-id="0f188-110">`GetNameFromToken` is obsolete.</span></span> <span data-ttu-id="0f188-111">En guise d’alternative, appelez une méthode pour obtenir les propriétés du type particulier de jeton requis, tels que `GetFieldProps` pour un champ ou `GetMethodProps` pour une méthode.</span><span class="sxs-lookup"><span data-stu-id="0f188-111">As an alternative, call a method to get the properties of the particular type of token required, such as `GetFieldProps` for a field or `GetMethodProps` for a method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f188-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0f188-112">Requirements</span></span>  
 <span data-ttu-id="0f188-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0f188-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f188-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="0f188-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0f188-115">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0f188-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0f188-116">**Versions du .NET framework :** 1.0</span><span class="sxs-lookup"><span data-stu-id="0f188-116">**.NET Framework Versions:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f188-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f188-117">See Also</span></span>  
 [<span data-ttu-id="0f188-118">IMetaDataImport (Interface)</span><span class="sxs-lookup"><span data-stu-id="0f188-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="0f188-119">IMetaDataImport2 (Interface)</span><span class="sxs-lookup"><span data-stu-id="0f188-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)