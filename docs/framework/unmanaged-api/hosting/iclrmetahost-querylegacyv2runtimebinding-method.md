---
title: "ICLRMetaHost::QueryLegacyV2RuntimeBinding, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRMetaHost.RequestRuntimeLoadedNotification
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRMetaHost::QueryLegacyV2RuntimeBinding
helpviewer_keywords:
- QueryLegacyV2RuntimeBinding method [.NET Framework hosting]
- ICLRMetaHost::QueryLegacyV2RuntimeBinding method [.NET Framework hosting]
ms.assetid: 9929817e-acc9-40b7-960c-598664e04b60
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c273a1690828e37c8f7fcf5071e42e5bb2c58228
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="iclrmetahostquerylegacyv2runtimebinding-method"></a><span data-ttu-id="a9f81-102">ICLRMetaHost::QueryLegacyV2RuntimeBinding, méthode</span><span class="sxs-lookup"><span data-stu-id="a9f81-102">ICLRMetaHost::QueryLegacyV2RuntimeBinding Method</span></span>
<span data-ttu-id="a9f81-103">Retourne une interface qui représente un runtime auquel une stratégie d’activation héritée a été liée, par exemple, à l’aide de la `useLegacyV2RuntimeActivationPolicy` de l’attribut le [ \<démarrage > élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) entrée de fichier de configuration, en utilisant directement des API d’activation hérité ou en appelant le [ICLRRuntimeInfo::BindAsLegacyV2Runtime](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a9f81-103">Returns an interface that represents a runtime to which legacy activation policy has been bound, for example, by using the `useLegacyV2RuntimeActivationPolicy` attribute on the [\<startup> element](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) configuration file entry, by direct use of the legacy activation APIs, or by calling the [ICLRRuntimeInfo::BindAsLegacyV2Runtime](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9f81-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9f81-104">Syntax</span></span>  
  
```  
HRESULT QueryLegacyV2RuntimeBinding (  
    [in] REFIID riid,  
    [out, iid_is(riid), retval] LPVOID *ppUnk);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a9f81-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9f81-105">Parameters</span></span>  
 `riid`  
 <span data-ttu-id="a9f81-106">[in] La seule valeur valide pour ce paramètre est de Required.Currently `IID_ICLRRuntimeInfo`.</span><span class="sxs-lookup"><span data-stu-id="a9f81-106">[in] Required.Currently the only valid value for this parameter is `IID_ICLRRuntimeInfo`.</span></span>  
  
 `ppUnk`  
 <span data-ttu-id="a9f81-107">[out] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a9f81-107">[out] Required.</span></span> <span data-ttu-id="a9f81-108">Lorsque cette méthode est retournée, contient un pointeur vers le [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface qui représente un runtime qui a été lié à la stratégie d’activation héritée.</span><span class="sxs-lookup"><span data-stu-id="a9f81-108">When this method returns, contains a pointer to the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface that represents a runtime that has been bound to legacy activation policy.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a9f81-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a9f81-109">Return Value</span></span>  
 <span data-ttu-id="a9f81-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a9f81-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="a9f81-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a9f81-111">HRESULT</span></span>|<span data-ttu-id="a9f81-112">Description</span><span class="sxs-lookup"><span data-stu-id="a9f81-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a9f81-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9f81-113">S_OK</span></span>|<span data-ttu-id="a9f81-114">La méthode s'est terminée correctement et a retourné un runtime lié à une stratégie d'activation héritée.</span><span class="sxs-lookup"><span data-stu-id="a9f81-114">The method completed successfully and returned a runtime that was bound to legacy activation policy.</span></span>|  
|<span data-ttu-id="a9f81-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a9f81-115">S_FALSE</span></span>|<span data-ttu-id="a9f81-116">La méthode s'est terminée correctement, mais un runtime hérité n'a pas encore été lié.</span><span class="sxs-lookup"><span data-stu-id="a9f81-116">The method completed successfully, but a legacy runtime has not yet been bound.</span></span>|  
|<span data-ttu-id="a9f81-117">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="a9f81-117">E_NOINTERFACE</span></span>|<span data-ttu-id="a9f81-118">La méthode a trouvé un runtime lié à une stratégie d'activation héritée, mais `riid` n'est pas pris en charge par ce runtime.</span><span class="sxs-lookup"><span data-stu-id="a9f81-118">The method found a runtime that was bound to legacy activation policy, but `riid` is not supported by that runtime.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a9f81-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="a9f81-119">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9f81-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a9f81-120">Requirements</span></span>  
 <span data-ttu-id="a9f81-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a9f81-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9f81-122">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="a9f81-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a9f81-123">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a9f81-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a9f81-124">**Versions du .NET framework :**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9f81-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9f81-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9f81-125">See Also</span></span>  
 [<span data-ttu-id="a9f81-126">ICLRMetaHost (Interface)</span><span class="sxs-lookup"><span data-stu-id="a9f81-126">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)  
 [<span data-ttu-id="a9f81-127">Hébergement d’applications WPF</span><span class="sxs-lookup"><span data-stu-id="a9f81-127">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)