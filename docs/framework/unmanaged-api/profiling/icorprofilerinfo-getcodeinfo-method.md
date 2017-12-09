---
title: "ICorProfilerInfo::GetCodeInfo, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.GetCodeInfo
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::GetCodeInfo
helpviewer_keywords:
- GetCodeInfo method [.NET Framework profiling]
- ICorProfilerInfo::GetCodeInfo method [.NET Framework profiling]
ms.assetid: 90140b0f-a926-4a7e-b6fa-23e05f703cce
topic_type: apiref
caps.latest.revision: "18"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 0b5c7b0d932200f04df0a1a84dd1f747b7945943
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfogetcodeinfo-method"></a><span data-ttu-id="5755f-102">ICorProfilerInfo::GetCodeInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="5755f-102">ICorProfilerInfo::GetCodeInfo Method</span></span>
<span data-ttu-id="5755f-103">Obtient l'étendue de code natif associée à l'ID de la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5755f-103">Gets the extent of native code associated with the specified function ID.</span></span>  
  
 <span data-ttu-id="5755f-104">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="5755f-104">This method is obsolete.</span></span> <span data-ttu-id="5755f-105">Utilisez le [ICorProfilerInfo2::GetCodeInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="5755f-105">Use the [ICorProfilerInfo2::GetCodeInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5755f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5755f-106">Syntax</span></span>  
  
```  
HRESULT GetCodeInfo(  
    [in]  FunctionID functionId,  
    [out] LPCBYTE    *pStart,  
    [out] ULONG      *pcSize);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5755f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5755f-107">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="5755f-108">[in] ID de la fonction à laquelle le code natif est associé.</span><span class="sxs-lookup"><span data-stu-id="5755f-108">[in] The ID of the function with which the native code is associated.</span></span>  
  
 `pStart`  
 <span data-ttu-id="5755f-109">[out] Pointeur vers un tableau d'octets qui composent le code natif de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5755f-109">[out] A pointer to an array of bytes that compose the native code of the function.</span></span>  
  
 `pcSize`  
 <span data-ttu-id="5755f-110">[out] Pointeur vers un entier qui spécifie la taille, en octets, du code natif.</span><span class="sxs-lookup"><span data-stu-id="5755f-110">[out] A pointer to an integer that specifies the size, in bytes, of the native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5755f-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="5755f-111">Remarks</span></span>  
 <span data-ttu-id="5755f-112">Pour optimiser la performance, le runtime dans la version 2.0 du .NET Framework fractionne le code natif précompilé d'une fonction en plusieurs régions.</span><span class="sxs-lookup"><span data-stu-id="5755f-112">To optimize performance, the runtime in the .NET Framework version 2.0 splits the precompiled, native code of a function into multiple regions.</span></span> <span data-ttu-id="5755f-113">Par conséquent, la méthode `GetCodeInfo` est obsolète dans .NET Framework 2.0, car elle ne peut pas gérer l'étendue du code natif d'une fonction.</span><span class="sxs-lookup"><span data-stu-id="5755f-113">Consequently, the `GetCodeInfo` method is obsolete in the .NET Framework 2.0 because it is unable to handle the extent of a function's native code.</span></span> <span data-ttu-id="5755f-114">Les profileurs doivent utiliser la méthode `ICorProfilerInfo2::GetCodeInfo2` plus générale à la place.</span><span class="sxs-lookup"><span data-stu-id="5755f-114">Profilers should switch to using the more general `ICorProfilerInfo2::GetCodeInfo2` method instead.</span></span>  
  
 <span data-ttu-id="5755f-115">Cette fonction utilise des mémoires tampons allouées par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="5755f-115">This function uses caller-allocated buffers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5755f-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5755f-116">Requirements</span></span>  
 <span data-ttu-id="5755f-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5755f-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5755f-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5755f-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5755f-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5755f-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5755f-120">**Versions du .NET framework :** 1.0</span><span class="sxs-lookup"><span data-stu-id="5755f-120">**.NET Framework Versions:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5755f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5755f-121">See Also</span></span>  
 [<span data-ttu-id="5755f-122">ICorProfilerInfo (Interface)</span><span class="sxs-lookup"><span data-stu-id="5755f-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="5755f-123">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="5755f-123">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="5755f-124">Profilage</span><span class="sxs-lookup"><span data-stu-id="5755f-124">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)