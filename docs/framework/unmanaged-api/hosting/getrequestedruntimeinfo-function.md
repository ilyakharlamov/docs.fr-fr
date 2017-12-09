---
title: GetRequestedRuntimeInfo, fonction
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetRequestedRuntimeInfo
api_location:
- mscoree.dll
- mscoreei.dll
api_type: DLLExport
f1_keywords: GetRequestedRuntimeInfo
helpviewer_keywords: GetRequestedRuntimeInfo function [.NET Framework hosting]
ms.assetid: 0dfd7cdc-c116-4e25-b56a-ac7b0378c942
topic_type: apiref
caps.latest.revision: "22"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: cca74a1ff66392608802eacedcd74bb673919e8c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="getrequestedruntimeinfo-function"></a><span data-ttu-id="5f464-102">GetRequestedRuntimeInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="5f464-102">GetRequestedRuntimeInfo Function</span></span>
<span data-ttu-id="5f464-103">Obtient les informations de version et au répertoire sur le common language runtime (CLR) demandé par une application.</span><span class="sxs-lookup"><span data-stu-id="5f464-103">Gets version and directory information about the common language runtime (CLR) requested by an application.</span></span>  
  
 <span data-ttu-id="5f464-104">Cette fonction est déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="5f464-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f464-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f464-105">Syntax</span></span>  
  
```  
HRESULT GetRequestedRuntimeInfo (  
    [in]  LPCWSTR  pExe,   
    [in]  LPCWSTR  pwszVersion,   
    [in]  LPCWSTR  pConfigurationFile,   
    [in]  DWORD    startupFlags,   
    [in]  DWORD    runtimeInfoFlags,   
    [out] LPWSTR   pDirectory,   
    [in]  DWORD    dwDirectory,   
    [out] DWORD   *dwDirectoryLength,   
    [out] LPWSTR   pVersion,   
    [in]  DWORD    cchBuffer,   
    [out] DWORD   *dwlength  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5f464-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f464-106">Parameters</span></span>  
 `pExe`  
 <span data-ttu-id="5f464-107">[in] Le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="5f464-107">[in] The name of the application.</span></span>  
  
 `pwszVersion`  
 <span data-ttu-id="5f464-108">[in] Chaîne spécifiant le numéro de version du runtime.</span><span class="sxs-lookup"><span data-stu-id="5f464-108">[in] A string specifying the version number of the runtime.</span></span>  
  
 `pConfigurationFile`  
 <span data-ttu-id="5f464-109">[in] Le nom du fichier de configuration qui est associé à `pExe`.</span><span class="sxs-lookup"><span data-stu-id="5f464-109">[in] The name of the configuration file that is associated with `pExe`.</span></span>  
  
 `startupFlags`  
 <span data-ttu-id="5f464-110">[in] Un ou plusieurs de la [STARTUP_FLAGS](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="5f464-110">[in] One or more of the [STARTUP_FLAGS](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) enumeration values.</span></span>  
  
 `runtimeInfoFlags`  
 <span data-ttu-id="5f464-111">[in] Un ou plusieurs de la [RUNTIME_INFO_FLAGS](../../../../docs/framework/unmanaged-api/hosting/runtime-info-flags-enumeration.md) valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="5f464-111">[in] One or more of the [RUNTIME_INFO_FLAGS](../../../../docs/framework/unmanaged-api/hosting/runtime-info-flags-enumeration.md) enumeration values.</span></span>  
  
 `pDirectory`  
 <span data-ttu-id="5f464-112">[out] Une mémoire tampon qui contient le chemin d’accès du répertoire à l’exécution en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="5f464-112">[out] A buffer that contains the directory path to the runtime upon successful completion.</span></span>  
  
 `dwDirectory`  
 <span data-ttu-id="5f464-113">[in] La longueur de la mémoire tampon du répertoire.</span><span class="sxs-lookup"><span data-stu-id="5f464-113">[in] The length of the directory buffer.</span></span>  
  
 `dwDirectoryLength`  
 <span data-ttu-id="5f464-114">[out] Pointeur vers la longueur de la chaîne de chemin d’accès de répertoire.</span><span class="sxs-lookup"><span data-stu-id="5f464-114">[out] A pointer to the length of the directory path string.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="5f464-115">[out] Une mémoire tampon qui contient le numéro de version du runtime à l’achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="5f464-115">[out] A buffer that contains the version number of the runtime upon successful completion.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="5f464-116">[in] La longueur de la mémoire tampon de chaîne version.</span><span class="sxs-lookup"><span data-stu-id="5f464-116">[in] The length of the version string buffer.</span></span>  
  
 `dwlength`  
 <span data-ttu-id="5f464-117">[out] Pointeur vers la longueur de la chaîne de version.</span><span class="sxs-lookup"><span data-stu-id="5f464-117">[out] A pointer to the length of the version string.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5f464-118">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5f464-118">Return Value</span></span>  
 <span data-ttu-id="5f464-119">Cette méthode retourne des codes d’erreur de modèle COM (Component Object) standard, tel que défini dans WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f464-119">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="5f464-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5f464-120">Return code</span></span>|<span data-ttu-id="5f464-121">Description</span><span class="sxs-lookup"><span data-stu-id="5f464-121">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="5f464-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f464-122">S_OK</span></span>|<span data-ttu-id="5f464-123">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="5f464-123">The method completed successfully.</span></span>|  
|<span data-ttu-id="5f464-124">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="5f464-124">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="5f464-125">La mémoire tampon du répertoire n’est pas suffisamment grand pour stocker le chemin d’accès de répertoire.</span><span class="sxs-lookup"><span data-stu-id="5f464-125">The directory buffer is not large enough to store the directory path.</span></span><br /><br /> <span data-ttu-id="5f464-126">ou</span><span class="sxs-lookup"><span data-stu-id="5f464-126">- or -</span></span><br /><br /> <span data-ttu-id="5f464-127">Le tampon de version n’est pas suffisamment grand pour stocker la chaîne de version.</span><span class="sxs-lookup"><span data-stu-id="5f464-127">The version buffer is not large enough to store the version string.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5f464-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="5f464-128">Remarks</span></span>  
 <span data-ttu-id="5f464-129">Le `GetRequestedRuntimeInfo` méthode retourne les informations d’exécution sur la version chargée dans le processus, ce qui n’est pas nécessairement la version la plus récente installée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5f464-129">The `GetRequestedRuntimeInfo` method returns run-time information about the version loaded into the process, which is not necessarily the latest version installed on the computer.</span></span>  
  
 <span data-ttu-id="5f464-130">Dans le .NET Framework version 2.0, vous pouvez obtenir plus d’informations sur la dernière version installée à l’aide de la `GetRequestedRuntimeInfo` méthode comme suit :</span><span class="sxs-lookup"><span data-stu-id="5f464-130">In the .NET Framework version 2.0, you can get information about the latest installed version by using the `GetRequestedRuntimeInfo` method as follows:</span></span>  
  
-   <span data-ttu-id="5f464-131">Spécifiez le `pExe`, `pwszVersion`, et `pConfigurationFile` paramètres comme null.</span><span class="sxs-lookup"><span data-stu-id="5f464-131">Specify the `pExe`, `pwszVersion`, and `pConfigurationFile` parameters as null.</span></span>  
  
-   <span data-ttu-id="5f464-132">Spécifiez l’indicateur RUNTIME_INFO_UPGRADE_VERSION dans le `RUNTIME_INFO_FLAGS` énumérations pour le `runtimeInfoFlags` paramètre.</span><span class="sxs-lookup"><span data-stu-id="5f464-132">Specify the RUNTIME_INFO_UPGRADE_VERSION flag in the `RUNTIME_INFO_FLAGS` enumerations for the `runtimeInfoFlags` parameter.</span></span>  
  
 <span data-ttu-id="5f464-133">Le `GetRequestedRuntimeInfo` méthode ne retourne pas la dernière version du CLR dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f464-133">The `GetRequestedRuntimeInfo` method does not return the latest CLR version in the following circumstances:</span></span>  
  
-   <span data-ttu-id="5f464-134">Il existe un fichier de configuration qui spécifie le chargement d’une version particulière du CLR.</span><span class="sxs-lookup"><span data-stu-id="5f464-134">An application configuration file that specifies loading a particular CLR version exists.</span></span> <span data-ttu-id="5f464-135">Notez que le .NET Framework utilisera le fichier de configuration même si vous spécifiez une valeur null pour le `pConfigurationFile` paramètre.</span><span class="sxs-lookup"><span data-stu-id="5f464-135">Note that the .NET Framework will use the configuration file even if you specify null for the `pConfigurationFile` parameter.</span></span>  
  
-   <span data-ttu-id="5f464-136">Le [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) méthode a été appelée en spécifiant une version antérieure du CLR.</span><span class="sxs-lookup"><span data-stu-id="5f464-136">The [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) method was called specifying an earlier CLR version.</span></span>  
  
-   <span data-ttu-id="5f464-137">Une application qui a été compilée pour une version antérieure du CLR est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5f464-137">An application that was compiled for an earlier CLR version is currently running.</span></span>  
  
 <span data-ttu-id="5f464-138">Pour le `runtimeInfoFlags` paramètre, vous pouvez spécifier uniquement une des constantes d’architecture de le `RUNTIME_INFO_FLAGS` énumération à la fois :</span><span class="sxs-lookup"><span data-stu-id="5f464-138">For the `runtimeInfoFlags` parameter, you can specify only one of the architecture constants of the `RUNTIME_INFO_FLAGS` enumeration at a time:</span></span>  
  
-   <span data-ttu-id="5f464-139">RUNTIME_INFO_REQUEST_IA64</span><span class="sxs-lookup"><span data-stu-id="5f464-139">RUNTIME_INFO_REQUEST_IA64</span></span>  
  
-   <span data-ttu-id="5f464-140">RUNTIME_INFO_REQUEST_AMD64</span><span class="sxs-lookup"><span data-stu-id="5f464-140">RUNTIME_INFO_REQUEST_AMD64</span></span>  
  
-   <span data-ttu-id="5f464-141">RUNTIME_INFO_REQUEST_X86</span><span class="sxs-lookup"><span data-stu-id="5f464-141">RUNTIME_INFO_REQUEST_X86</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f464-142">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5f464-142">Requirements</span></span>  
 <span data-ttu-id="5f464-143">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5f464-143">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f464-144">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5f464-144">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5f464-145">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f464-145">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5f464-146">**Versions du .NET framework :**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f464-146">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f464-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f464-147">See Also</span></span>  
 [<span data-ttu-id="5f464-148">GetRequestedRuntimeVersion (fonction)</span><span class="sxs-lookup"><span data-stu-id="5f464-148">GetRequestedRuntimeVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)  
 [<span data-ttu-id="5f464-149">GetVersionFromProcess (fonction)</span><span class="sxs-lookup"><span data-stu-id="5f464-149">GetVersionFromProcess Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md)  
 [<span data-ttu-id="5f464-150">Fonctions d’hébergement du CLR déconseillées</span><span class="sxs-lookup"><span data-stu-id="5f464-150">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)