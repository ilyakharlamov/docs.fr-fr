---
title: "IHostSecurityManager::ImpersonateLoggedOnUser, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostSecurityManager.ImpersonateLoggedOnUser
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostSecurityManager::ImpersonateLoggedOnUser
helpviewer_keywords:
- ImpersonateLoggedOnUser method [.NET Framework hosting]
- IHostSecurityManager::ImpersonateLoggedOnUser method [.NET Framework hosting]
ms.assetid: acc49ba0-f1d9-45ad-871f-9d053a89dcbe
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8c5956dcad6908f0117de7f5ff0c6632ad3bb925
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="ihostsecuritymanagerimpersonateloggedonuser-method"></a><span data-ttu-id="2fa6a-102">IHostSecurityManager::ImpersonateLoggedOnUser, méthode</span><span class="sxs-lookup"><span data-stu-id="2fa6a-102">IHostSecurityManager::ImpersonateLoggedOnUser Method</span></span>
<span data-ttu-id="2fa6a-103">Les demandes que le code exécuté à l’aide des informations d’identification de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-103">Requests that code be executed using the credentials of the current user identity.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2fa6a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fa6a-104">Syntax</span></span>  
  
```  
HRESULT ImpersonateLoggedOnUser (  
    [in] HANDLE hToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2fa6a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fa6a-105">Parameters</span></span>  
 `hToken`  
 <span data-ttu-id="2fa6a-106">[in] Un jeton représentant les informations d’identification de l’utilisateur doit être empruntée.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-106">[in] A token representing the credentials of the user to be impersonated.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2fa6a-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2fa6a-107">Return Value</span></span>  
  
|<span data-ttu-id="2fa6a-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2fa6a-108">HRESULT</span></span>|<span data-ttu-id="2fa6a-109">Description</span><span class="sxs-lookup"><span data-stu-id="2fa6a-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2fa6a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fa6a-110">S_OK</span></span>|<span data-ttu-id="2fa6a-111">`ImpersonateLoggedOnUser`retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-111">`ImpersonateLoggedOnUser` returned successfully.</span></span>|  
|<span data-ttu-id="2fa6a-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2fa6a-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2fa6a-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2fa6a-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2fa6a-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2fa6a-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-115">The call timed out.</span></span>|  
|<span data-ttu-id="2fa6a-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2fa6a-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2fa6a-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2fa6a-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2fa6a-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2fa6a-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2fa6a-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2fa6a-120">E_FAIL</span></span>|<span data-ttu-id="2fa6a-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2fa6a-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2fa6a-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2fa6a-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="2fa6a-124">Remarks</span></span>  
 <span data-ttu-id="2fa6a-125">Appelez `LogonUser` ou une fonction Win32 associée pour obtenir un handle vers les informations d’identification de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-125">Call `LogonUser` or a related Win32 function to get a handle to the credentials of the current user identity.</span></span>  
  
 <span data-ttu-id="2fa6a-126">Le `HANDLE` type n’est pas conforme à COM, c'est-à-dire que sa taille est spécifique à un système d’exploitation et il requiert le marshaling personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-126">The `HANDLE` type is not COM-compliant, that is, its size is specific to an operating system, and it requires custom marshaling.</span></span> <span data-ttu-id="2fa6a-127">Par conséquent, ce jeton est utilisé que dans le processus, entre le CLR et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="2fa6a-127">Thus, this token is for use only within the process, between the CLR and the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2fa6a-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2fa6a-128">Requirements</span></span>  
 <span data-ttu-id="2fa6a-129">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2fa6a-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2fa6a-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2fa6a-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2fa6a-131">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2fa6a-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2fa6a-132">**Versions du .NET framework :**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2fa6a-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2fa6a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fa6a-133">See Also</span></span>  
 [<span data-ttu-id="2fa6a-134">IHostSecurityContext (Interface)</span><span class="sxs-lookup"><span data-stu-id="2fa6a-134">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)  
 [<span data-ttu-id="2fa6a-135">IHostSecurityManager (Interface)</span><span class="sxs-lookup"><span data-stu-id="2fa6a-135">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
 [<span data-ttu-id="2fa6a-136">RevertToSelf (méthode)</span><span class="sxs-lookup"><span data-stu-id="2fa6a-136">RevertToSelf Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-reverttoself-method.md)