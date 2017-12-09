---
title: "IHostPolicyManager::OnDefaultAction, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostPolicyManager.OnDefaultAction
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostPolicyManager::OnDefaultAction
helpviewer_keywords:
- OnDefaultAction method [.NET Framework hosting]
- IHostPolicyManager::OnDefaultAction method [.NET Framework hosting]
ms.assetid: 071e73bd-4795-470f-9373-cfaef553b7f2
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ca5eb767c08733980c9156d04526594c62349624
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="ihostpolicymanagerondefaultaction-method"></a><span data-ttu-id="fa406-102">IHostPolicyManager::OnDefaultAction, méthode</span><span class="sxs-lookup"><span data-stu-id="fa406-102">IHostPolicyManager::OnDefaultAction Method</span></span>
<span data-ttu-id="fa406-103">Avertit l’hôte que le common language runtime (CLR) est sur le point d’effectuer l’action par défaut qui a été définie par un appel à la [ICLRPolicyManager::SetDefaultAction](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md) méthode en réponse à un abandon de thread ou <xref:System.AppDomain> décharger.</span><span class="sxs-lookup"><span data-stu-id="fa406-103">Notifies the host that the common language runtime (CLR) is about to take the default action that was set by a call to the [ICLRPolicyManager::SetDefaultAction](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md) method in response to a thread abort or <xref:System.AppDomain> unload.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa406-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa406-104">Syntax</span></span>  
  
```  
HRESULT OnDefaultAction (  
    [in] EClrOperation  operation,   
    [in] EPolicyAction  action  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fa406-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa406-105">Parameters</span></span>  
 `operation`  
 <span data-ttu-id="fa406-106">[in] Parmi les [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) valeurs indiquant le genre d’événement auquel le CLR répond.</span><span class="sxs-lookup"><span data-stu-id="fa406-106">[in] One of the [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) values, indicating the kind of event to which the CLR is responding.</span></span>  
  
 `action`  
 <span data-ttu-id="fa406-107">[in] Parmi les [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) valeurs, indiquant l’action que le CLR effectue en réponse à l’événement.</span><span class="sxs-lookup"><span data-stu-id="fa406-107">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the action that the CLR is taking in response to the event.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fa406-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fa406-108">Return Value</span></span>  
  
|<span data-ttu-id="fa406-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fa406-109">HRESULT</span></span>|<span data-ttu-id="fa406-110">Description</span><span class="sxs-lookup"><span data-stu-id="fa406-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fa406-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa406-111">S_OK</span></span>|<span data-ttu-id="fa406-112">`OnDefaultAction`retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="fa406-112">`OnDefaultAction` returned successfully.</span></span>|  
|<span data-ttu-id="fa406-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fa406-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="fa406-114">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel.</span><span class="sxs-lookup"><span data-stu-id="fa406-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call.</span></span> <span data-ttu-id="fa406-115">avec succès</span><span class="sxs-lookup"><span data-stu-id="fa406-115">successfully</span></span>|  
|<span data-ttu-id="fa406-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fa406-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="fa406-117">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="fa406-117">The call timed out.</span></span>|  
|<span data-ttu-id="fa406-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="fa406-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="fa406-119">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="fa406-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="fa406-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="fa406-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="fa406-121">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="fa406-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="fa406-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fa406-122">E_FAIL</span></span>|<span data-ttu-id="fa406-123">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fa406-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="fa406-124">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="fa406-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="fa406-125">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="fa406-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fa406-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa406-126">Requirements</span></span>  
 <span data-ttu-id="fa406-127">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fa406-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa406-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fa406-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fa406-129">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fa406-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fa406-130">**Versions du .NET framework :**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa406-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa406-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa406-131">See Also</span></span>  
 [<span data-ttu-id="fa406-132">EClrOperation (énumération)</span><span class="sxs-lookup"><span data-stu-id="fa406-132">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)  
 [<span data-ttu-id="fa406-133">EPolicyAction (énumération)</span><span class="sxs-lookup"><span data-stu-id="fa406-133">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)  
 [<span data-ttu-id="fa406-134">ICLRPolicyManager (Interface)</span><span class="sxs-lookup"><span data-stu-id="fa406-134">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)  
 [<span data-ttu-id="fa406-135">IHostPolicyManager (Interface)</span><span class="sxs-lookup"><span data-stu-id="fa406-135">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)