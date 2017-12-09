---
title: "ICorProfilerCallback4::SurvivingReferences2, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback4.SurvivingReferences2
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback4::SurvivingReferences2
helpviewer_keywords:
- ICorProfilerCallback4::SurvivingReferences2 method [.NET Framework profiling]
- SurvivingReferences2 method, ICorProfilerCallback4 interface [.NET Framework profiling]
ms.assetid: 02b51888-5d89-4e50-a915-45b7e329aad9
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ced8542d2e84b6c317e20d7ff440e6c159383bfa
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallback4survivingreferences2-method"></a><span data-ttu-id="dd06b-102">ICorProfilerCallback4::SurvivingReferences2, méthode</span><span class="sxs-lookup"><span data-stu-id="dd06b-102">ICorProfilerCallback4::SurvivingReferences2 Method</span></span>
<span data-ttu-id="dd06b-103">Signale la disposition d’objets dans le tas suite à un garbage collection de non-compactage.</span><span class="sxs-lookup"><span data-stu-id="dd06b-103">Reports the layout of objects in the heap as a result of a non-compacting garbage collection.</span></span> <span data-ttu-id="dd06b-104">Cette méthode est appelée si le profileur a implémenté la [ICorProfilerCallback4](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="dd06b-104">This method is called if the profiler has implemented the [ICorProfilerCallback4](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md) interface.</span></span> <span data-ttu-id="dd06b-105">Ce rappel remplace la [ICorProfilerCallback2::SurvivingReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-survivingreferences-method.md) (méthode), car il peut indiquer des plages plus larges d’objets dont les longueurs dépassent ce qui peut être exprimé en ULONG.</span><span class="sxs-lookup"><span data-stu-id="dd06b-105">This callback replaces the [ICorProfilerCallback2::SurvivingReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-survivingreferences-method.md) method, because it can report larger ranges of objects whose lengths exceed what can be expressed in a ULONG.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd06b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd06b-106">Syntax</span></span>  
  
```  
HRESULT SurvivingReferences2(  
    [in] ULONG  cSurvivingObjectIDRanges,  
    [in, size_is(cSurvivingObjectIDRanges)] ObjectID  
                objectIDRangeStart[] ,  
    [in, size_is(cSurvivingObjectIDRanges)] SIZE_T  
                cObjectIDRangeLength[] );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dd06b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd06b-107">Parameters</span></span>  
 `cSurvivingObjectIDRanges`  
 <span data-ttu-id="dd06b-108">[in] Nombre de blocs d’objets contigus qui ont survécu à la suite du garbage collection de non-compactage.</span><span class="sxs-lookup"><span data-stu-id="dd06b-108">[in] The number of blocks of contiguous objects that survived as the result of the non-compacting garbage collection.</span></span> <span data-ttu-id="dd06b-109">Autrement dit, la valeur de `cSurvivingObjectIDRanges` est la taille des tableaux `objectIDRangeStart` et `cObjectIDRangeLength` qui stockent un `ObjectID` et une longueur, respectivement, pour chaque bloc d'objets.</span><span class="sxs-lookup"><span data-stu-id="dd06b-109">That is, the value of `cSurvivingObjectIDRanges` is the size of the `objectIDRangeStart` and `cObjectIDRangeLength` arrays, which store an `ObjectID` and a length, respectively, for each block of objects.</span></span>  
  
 <span data-ttu-id="dd06b-110">Les deux arguments suivants de `SurvivingReferences2` sont des tableaux parallèles.</span><span class="sxs-lookup"><span data-stu-id="dd06b-110">The next two arguments of `SurvivingReferences2` are parallel arrays.</span></span> <span data-ttu-id="dd06b-111">En d'autres termes, `objectIDRangeStart` et `cObjectIDRangeLength` concernent le même bloc d'objets contigus.</span><span class="sxs-lookup"><span data-stu-id="dd06b-111">In other words, `objectIDRangeStart` and `cObjectIDRangeLength` concern the same block of contiguous objects.</span></span>  
  
 `objectIDRangeStart`  
 <span data-ttu-id="dd06b-112">[in] Tableau de valeurs `ObjectID`, chacune d'elles étant l'adresse de début d'un bloc d'objets actifs contigus dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd06b-112">[in] An array of `ObjectID` values, each of which is the starting address of a block of contiguous, live objects in memory.</span></span>  
  
 `cObjectIDRangeLength`  
 <span data-ttu-id="dd06b-113">[in] Tableau d'entiers, chacun d'eux correspondant à la taille d'un bloc survivant d'objets contigus dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd06b-113">[in] An array of integers, each of which is the size of a surviving block of contiguous objects in memory.</span></span>  
  
 <span data-ttu-id="dd06b-114">Une taille est spécifiée pour chaque bloc référencé dans le tableau `objectIDRangeStart`.</span><span class="sxs-lookup"><span data-stu-id="dd06b-114">A size is specified for each block that is referenced in the `objectIDRangeStart` array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dd06b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd06b-115">Remarks</span></span>  
 <span data-ttu-id="dd06b-116">Les éléments des tableaux `objectIDRangeStart` et `cObjectIDRangeLength` doivent être interprétés comme suit pour déterminer si un objet a survécu au garbage collection.</span><span class="sxs-lookup"><span data-stu-id="dd06b-116">The elements of the `objectIDRangeStart` and `cObjectIDRangeLength` arrays should be interpreted as follows to determine whether an object survived the garbage collection.</span></span> <span data-ttu-id="dd06b-117">Supposons qu'une valeur `ObjectID` (`ObjectID`) se trouve dans la plage suivante :</span><span class="sxs-lookup"><span data-stu-id="dd06b-117">Assume that an `ObjectID` value (`ObjectID`) lies within the following range:</span></span>  
  
 `ObjectIDRangeStart[i]` <= `ObjectID` < `ObjectIDRangeStart[i]` + `cObjectIDRangeLength[i]`  
  
 <span data-ttu-id="dd06b-118">Pour toute valeur de `i` qui se trouve dans la plage suivante, l'objet a survécu au garbage collection :</span><span class="sxs-lookup"><span data-stu-id="dd06b-118">For any value of `i` that is in the following range, the object has survived the garbage collection:</span></span>  
  
 <span data-ttu-id="dd06b-119">0 <= `i` < `cSurvivingObjectIDRanges`</span><span class="sxs-lookup"><span data-stu-id="dd06b-119">0 <= `i` < `cSurvivingObjectIDRanges`</span></span>  
  
 <span data-ttu-id="dd06b-120">Un garbage collection de non-compactage libère la mémoire occupée par des objets « morts », mais ne compacte pas cet espace libéré.</span><span class="sxs-lookup"><span data-stu-id="dd06b-120">A non-compacting garbage collection reclaims the memory occupied by "dead" objects, but does not compact that freed space.</span></span> <span data-ttu-id="dd06b-121">Par conséquent, la mémoire est retournée au tas, mais aucun objet « actif » n'est déplacé.</span><span class="sxs-lookup"><span data-stu-id="dd06b-121">As a result, memory is returned to the heap, but no "live" objects are moved.</span></span>  
  
 <span data-ttu-id="dd06b-122">Le Common Language Runtime (CLR) appelle `SurvivingReferences2` pour les garbage collection de non-compactage.</span><span class="sxs-lookup"><span data-stu-id="dd06b-122">The common language runtime (CLR) calls `SurvivingReferences2` for non-compacting garbage collections.</span></span> <span data-ttu-id="dd06b-123">Pour le garbage collection de compactage, [MovedReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-movedreferences2-method.md) est appelée à la place.</span><span class="sxs-lookup"><span data-stu-id="dd06b-123">For compacting garbage collections, [MovedReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-movedreferences2-method.md) is called instead.</span></span> <span data-ttu-id="dd06b-124">Un garbage collection unique peut être de compactage pour une génération et de non-compactage pour une autre.</span><span class="sxs-lookup"><span data-stu-id="dd06b-124">A single garbage collection can be compacting for one generation and non-compacting for another.</span></span> <span data-ttu-id="dd06b-125">Pour un garbage collection sur n’importe quelle génération, le profileur reçoit un `SurvivingReferences2` rappel ou une [MovedReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-movedreferences2-method.md) rappel, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="dd06b-125">For a garbage collection on any particular generation, the profiler will receive either a `SurvivingReferences2` callback or a [MovedReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-movedreferences2-method.md) callback, but not both.</span></span>  
  
 <span data-ttu-id="dd06b-126">Plusieurs rappels `SurvivingReferences2` peuvent être reçus pendant un garbage collection particulier, en raison de la mise en mémoire tampon interne limitée, de multiples rappels pendant un garbage collection de serveur et pour d'autres raisons.</span><span class="sxs-lookup"><span data-stu-id="dd06b-126">Multiple `SurvivingReferences2` callbacks might be received during a particular garbage collection, because of limited internal buffering, multiple callbacks during server garbage collection, and other reasons.</span></span> <span data-ttu-id="dd06b-127">En cas de rappels multiples pendant un garbage collection, les informations se cumulent ; toutes les références qui sont rapportées dans un rappel `SurvivingReferences2` survivent au garbage collection.</span><span class="sxs-lookup"><span data-stu-id="dd06b-127">In the case of multiple callbacks during a garbage collection, the information is cumulative; all references that are reported in any `SurvivingReferences2` callback survive the garbage collection.</span></span>  
  
 <span data-ttu-id="dd06b-128">Si le profileur implémente à la fois le [ICorProfilerCallback](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md) et [ICorProfilerCallback4](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md) interfaces, les `SurvivingReferences2` méthode est appelée avant la [ICorProfilerCallback2 :: SurvivingReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-survivingreferences-method.md) (méthode), mais uniquement si `SurvivingReferences2` retournée avec succès.</span><span class="sxs-lookup"><span data-stu-id="dd06b-128">If the profiler implements both the [ICorProfilerCallback](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md) and the [ICorProfilerCallback4](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md) interfaces, the `SurvivingReferences2` method is called before the [ICorProfilerCallback2::SurvivingReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-survivingreferences-method.md) method, but only if `SurvivingReferences2` returns successfully.</span></span> <span data-ttu-id="dd06b-129">Les profileurs peuvent retourner une valeur HRESULT qui indique un échec de la méthode `SurvivingReferences2` pour éviter d'appeler la seconde méthode.</span><span class="sxs-lookup"><span data-stu-id="dd06b-129">Profilers can return an HRESULT that indicates failure from the `SurvivingReferences2` method to avoid calling the second method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dd06b-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dd06b-130">Requirements</span></span>  
 <span data-ttu-id="dd06b-131">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dd06b-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd06b-132">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dd06b-132">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="dd06b-133">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dd06b-133">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dd06b-134">**Versions du .NET framework :**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd06b-134">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd06b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd06b-135">See Also</span></span>  
 [<span data-ttu-id="dd06b-136">Interface ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="dd06b-136">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="dd06b-137">ICorProfilerCallback2, Interface</span><span class="sxs-lookup"><span data-stu-id="dd06b-137">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)  
 [<span data-ttu-id="dd06b-138">ICorProfilerCallback4 (Interface)</span><span class="sxs-lookup"><span data-stu-id="dd06b-138">ICorProfilerCallback4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)