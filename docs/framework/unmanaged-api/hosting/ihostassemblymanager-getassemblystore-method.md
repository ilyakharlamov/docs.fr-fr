---
title: "IHostAssemblyManager::GetAssemblyStore, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostAssemblyManager.GetAssemblyStore
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostAssemblyManager::GetAssemblyStore
helpviewer_keywords:
- IHostAssemblyManager::GetAssemblyStore method [.NET Framework hosting]
- GetAssemblyStore method [.NET Framework hosting]
ms.assetid: d0f74593-9bb1-4a11-8096-e29734b20698
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d838ee8383a4e11f5d43c4a3751c4a90503906fb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="ihostassemblymanagergetassemblystore-method"></a><span data-ttu-id="a2312-102">IHostAssemblyManager::GetAssemblyStore, méthode</span><span class="sxs-lookup"><span data-stu-id="a2312-102">IHostAssemblyManager::GetAssemblyStore Method</span></span>
<span data-ttu-id="a2312-103">Obtient un pointeur d’interface vers un [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) qui représente la liste des assemblys chargés par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="a2312-103">Gets an interface pointer to an [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2312-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2312-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyStore (  
    [out] IHostAssemblyStore **ppAssemblyStore  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a2312-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2312-105">Parameters</span></span>  
 `ppAssemblyStore`  
 <span data-ttu-id="a2312-106">[out] Un pointeur de fonction vers un `IHostAssemblyStore` de l’instance, ou null si l’hôte n’implémente pas `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="a2312-106">[out] A function pointer to an `IHostAssemblyStore` instance, or null, if the host does not implement `IHostAssemblyStore`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a2312-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a2312-107">Return Value</span></span>  
  
|<span data-ttu-id="a2312-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a2312-108">HRESULT</span></span>|<span data-ttu-id="a2312-109">Description</span><span class="sxs-lookup"><span data-stu-id="a2312-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a2312-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2312-110">S_OK</span></span>|<span data-ttu-id="a2312-111">`GetAssemblyStore`retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="a2312-111">`GetAssemblyStore` returned successfully.</span></span>|  
|<span data-ttu-id="a2312-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a2312-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a2312-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="a2312-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a2312-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a2312-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a2312-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="a2312-115">The call timed out.</span></span>|  
|<span data-ttu-id="a2312-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a2312-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a2312-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="a2312-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a2312-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a2312-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a2312-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="a2312-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a2312-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a2312-120">E_FAIL</span></span>|<span data-ttu-id="a2312-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a2312-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a2312-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="a2312-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a2312-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="a2312-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="a2312-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="a2312-124">E_NOINTERFACE</span></span>|<span data-ttu-id="a2312-125">L’hôte ne fournit pas une implémentation de `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="a2312-125">The host does not provide an implementation of `IHostAssemblyStore`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a2312-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2312-126">Remarks</span></span>  
 <span data-ttu-id="a2312-127">`IHostAssemblyStore`Fournit des méthodes qui permettent à un hôte à lier à des assemblys et des modules indépendamment du CLR.</span><span class="sxs-lookup"><span data-stu-id="a2312-127">`IHostAssemblyStore` provides methods that allow a host to bind to assemblies and modules independently of the CLR.</span></span> <span data-ttu-id="a2312-128">Hôtes fournissent généralement des magasins pour autoriser les assemblys à charger à partir d’autres formats que le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a2312-128">Hosts typically provide assembly stores to allow assemblies to be loaded from formats other than the file system.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a2312-129">Si l’hôte n’implémente pas `IHostAssemblyStore`, `GetAssemblyStore` doit retourner une valeur HRESULT d’E_NOINTERFACE et doit définir `ppAssemblyStore` avec la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a2312-129">If the host does not implement `IHostAssemblyStore`, `GetAssemblyStore` should return an HRESULT value of E_NOINTERFACE, and should set `ppAssemblyStore` to null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2312-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a2312-130">Requirements</span></span>  
 <span data-ttu-id="a2312-131">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a2312-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2312-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a2312-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a2312-133">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a2312-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a2312-134">**Versions du .NET framework :**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2312-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2312-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2312-135">See Also</span></span>  
 [<span data-ttu-id="a2312-136">IHostAssemblyManager (Interface)</span><span class="sxs-lookup"><span data-stu-id="a2312-136">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
 [<span data-ttu-id="a2312-137">IHostAssemblyStore (Interface)</span><span class="sxs-lookup"><span data-stu-id="a2312-137">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)