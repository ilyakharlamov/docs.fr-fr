---
title: StrongNameSignatureVerificationEx, fonction
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StrongNameSignatureVerificationEx
api_location:
- mscoree.dll
- mscorwks.dll
api_type: DLLExport
f1_keywords: StrongNameSignatureVerificationEx
helpviewer_keywords: StrongNameSignatureVerificationEx function [.NET Framework strong naming]
ms.assetid: cfe4b634-18bf-44b8-9773-d94fb7e8a480
topic_type: apiref
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0aebb53c6718a6812cbe6a6888f389c7b1a52dda
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="strongnamesignatureverificationex-function"></a><span data-ttu-id="44617-102">StrongNameSignatureVerificationEx, fonction</span><span class="sxs-lookup"><span data-stu-id="44617-102">StrongNameSignatureVerificationEx Function</span></span>
<span data-ttu-id="44617-103">Obtient une valeur qui indique si le manifeste d’assembly dans le chemin d’accès fourni contient une signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="44617-103">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature.</span></span>  
  
 <span data-ttu-id="44617-104">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="44617-104">This function has been deprecated.</span></span> <span data-ttu-id="44617-105">Utilisez le [ICLRStrongName::StrongNameSignatureVerificationEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="44617-105">Use the [ICLRStrongName::StrongNameSignatureVerificationEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44617-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44617-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameSignatureVerificationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  BOOLEAN   fForceVerification,  
    [out] BOOLEAN   *pfWasVerified  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="44617-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44617-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="44617-108">[in] Le chemin d’accès pour le fichier exécutable portable (.exe ou .dll) pour l’assembly à vérifier.</span><span class="sxs-lookup"><span data-stu-id="44617-108">[in] The path to the portable executable (.exe or .dll) file for the assembly to be verified.</span></span>  
  
 `fForceVerification`  
 <span data-ttu-id="44617-109">[in] `true` pour effectuer la vérification, même s’il est nécessaire de remplacer les paramètres de Registre ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="44617-109">[in] `true` to perform verification, even if it is necessary to override registry settings; otherwise, `false`.</span></span>  
  
 `pfWasVerified`  
 <span data-ttu-id="44617-110">[out] `true` si la signature de nom fort a été vérifiée ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="44617-110">[out] `true` if the strong name signature was verified; otherwise, `false`.</span></span> <span data-ttu-id="44617-111">`pfWasVerified`a également la valeur `false` si la vérification a réussi en raison des paramètres de Registre.</span><span class="sxs-lookup"><span data-stu-id="44617-111">`pfWasVerified` is also set to `false` if the verification was successful due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="44617-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="44617-112">Return Value</span></span>  
 <span data-ttu-id="44617-113">`true`Si la vérification a réussi ; dans le cas contraire, `false`.</span><span class="sxs-lookup"><span data-stu-id="44617-113">`true` if the verification was successful; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="44617-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="44617-114">Remarks</span></span>  
 <span data-ttu-id="44617-115">`StrongNameSignatureVerificationEx`Fournit une fonctionnalité semblable à la [StrongNameSignatureVerification](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignatureverification-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="44617-115">`StrongNameSignatureVerificationEx` provides a capability similar to the [StrongNameSignatureVerification](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignatureverification-function.md) function.</span></span> <span data-ttu-id="44617-116">Toutefois, le deuxième paramètre d’entrée et le paramètre de sortie pour `StrongNameSignatureVerificationEx` sont de type `BOOLEAN` au lieu de `DWORD`.</span><span class="sxs-lookup"><span data-stu-id="44617-116">However, the second input parameter and the output parameter for `StrongNameSignatureVerificationEx` are of type `BOOLEAN` instead of `DWORD`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44617-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="44617-117">Requirements</span></span>  
 <span data-ttu-id="44617-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="44617-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44617-119">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="44617-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="44617-120">**Bibliothèque :** inclus en tant que ressource dans mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="44617-120">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="44617-121">**Versions du .NET framework :**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44617-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44617-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44617-122">See Also</span></span>  
 [<span data-ttu-id="44617-123">StrongNameSignatureVerificationEx (méthode)</span><span class="sxs-lookup"><span data-stu-id="44617-123">StrongNameSignatureVerificationEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md)  
 [<span data-ttu-id="44617-124">StrongNameSignatureVerification (méthode)</span><span class="sxs-lookup"><span data-stu-id="44617-124">StrongNameSignatureVerification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md)  
 [<span data-ttu-id="44617-125">ICLRStrongName Interface</span><span class="sxs-lookup"><span data-stu-id="44617-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)