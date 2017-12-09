---
title: ICorDebugProcess6, interface
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 34a10ac2-882c-4797-8369-f120e8e640c7
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 222007d03d8ace00f97c01cf2a02f0dc293bbf78
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugprocess6-interface"></a><span data-ttu-id="cc0ee-102">ICorDebugProcess6, interface</span><span class="sxs-lookup"><span data-stu-id="cc0ee-102">ICorDebugProcess6 Interface</span></span>
<span data-ttu-id="cc0ee-103">Étend logiquement l’interface ICorDebugProcess pour activer des fonctionnalités telles que le décodage des événements de débogage managés qui sont codés dans les événements de débogage d’exception native et fractionnement de module virtuel.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-103">Logically extends the ICorDebugProcess interface to enable features such as decoding managed debug events that are encoded in native exception debug events and virtual module splitting.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cc0ee-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cc0ee-104">Methods</span></span>  
  
|<span data-ttu-id="cc0ee-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="cc0ee-105">Method</span></span>|<span data-ttu-id="cc0ee-106">Description</span><span class="sxs-lookup"><span data-stu-id="cc0ee-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cc0ee-107">Decodeevent, méthode</span><span class="sxs-lookup"><span data-stu-id="cc0ee-107">DecodeEvent Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md)|<span data-ttu-id="cc0ee-108">Décode les événements de débogage managés qui ont été encapsulés dans la charge utile des événements de débogage d'exception native conçus à cet effet.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-108">Decodes managed debug events that have been encapsulated in the payload of specially crafted native exception debug events.</span></span>|  
|[<span data-ttu-id="cc0ee-109">Enablevirtualmodulesplitting, méthode</span><span class="sxs-lookup"><span data-stu-id="cc0ee-109">EnableVirtualModuleSplitting Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-enablevirtualmodulesplitting-method.md)|<span data-ttu-id="cc0ee-110">Active ou désactive le fractionnement de module virtuel.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-110">Enables or disables virtual module splitting.</span></span>|  
|[<span data-ttu-id="cc0ee-111">GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="cc0ee-111">GetCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getcode-method.md)|<span data-ttu-id="cc0ee-112">Obtient des informations sur le code managé à une adresse de code particulière.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-112">Gets information about the managed code at a particular code address.</span></span>|  
|[<span data-ttu-id="cc0ee-113">Getexportstepinfo, méthode</span><span class="sxs-lookup"><span data-stu-id="cc0ee-113">GetExportStepInfo Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md)|<span data-ttu-id="cc0ee-114">Fournit des informations sur les fonctions exportées du runtime pour faciliter l'exécution pas à pas du code managé.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-114">Provides information on runtime exported functions to help step through managed code.</span></span>|  
|[<span data-ttu-id="cc0ee-115">Markdebuggerattached, méthode</span><span class="sxs-lookup"><span data-stu-id="cc0ee-115">MarkDebuggerAttached Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-markdebuggerattached-method.md)|<span data-ttu-id="cc0ee-116">Change l'état interne du programme débogué pour que la méthode <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> de la bibliothèque de classes du .NET Framework retourne `true`.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-116">Changes the internal state of the debugee so that the <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> method in the .NET Framework Class Library returns `true`.</span></span>|  
|[<span data-ttu-id="cc0ee-117">Processstatechanged, méthode</span><span class="sxs-lookup"><span data-stu-id="cc0ee-117">ProcessStateChanged Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md)|<span data-ttu-id="cc0ee-118">Notifie [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-118">Notifies [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cc0ee-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc0ee-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cc0ee-120">L'interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-120">The interface is available with .NET Native only.</span></span> <span data-ttu-id="cc0ee-121">Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.</span><span class="sxs-lookup"><span data-stu-id="cc0ee-121">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc0ee-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cc0ee-122">Requirements</span></span>  
 <span data-ttu-id="cc0ee-123">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc0ee-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc0ee-124">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cc0ee-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cc0ee-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cc0ee-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cc0ee-126">**Versions du .NET framework :**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc0ee-126">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc0ee-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc0ee-127">See Also</span></span>  
 [<span data-ttu-id="cc0ee-128">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="cc0ee-128">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="cc0ee-129">Débogage</span><span class="sxs-lookup"><span data-stu-id="cc0ee-129">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)