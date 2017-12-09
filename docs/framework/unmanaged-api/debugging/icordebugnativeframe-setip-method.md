---
title: "ICorDebugNativeFrame::SetIP, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugNativeFrame.SetIP
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugNativeFrame::SetIP
helpviewer_keywords:
- ICorDebugNativeFrame::SetIP method [.NET Framework debugging]
- SetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
ms.assetid: 57784a51-c76d-48f8-9392-584d0e1946d9
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 563566a877d589ecd32575c095cdc812c28f6334
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugnativeframesetip-method"></a><span data-ttu-id="4cb99-102">ICorDebugNativeFrame::SetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="4cb99-102">ICorDebugNativeFrame::SetIP Method</span></span>
<span data-ttu-id="4cb99-103">Définit le pointeur d’instruction à l’emplacement de décalage spécifié dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="4cb99-103">Sets the instruction pointer to the specified offset location in native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4cb99-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cb99-104">Syntax</span></span>  
  
```  
HRESULT SetIP (  
    [in] ULONG32 nOffset  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4cb99-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cb99-105">Parameters</span></span>  
 `nOffset`  
 <span data-ttu-id="4cb99-106">[in] L’emplacement de décalage dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="4cb99-106">[in] The offset location in the native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4cb99-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="4cb99-107">Remarks</span></span>  
 <span data-ttu-id="4cb99-108">Les appels à `SetIP` invalident immédiatement tous les frames et des chaînes pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="4cb99-108">Calls to `SetIP` immediately invalidate all frames and chains for the current thread.</span></span> <span data-ttu-id="4cb99-109">Si le débogueur a besoin d’informations de frames après un appel à `SetIP`, il doit effectuer une nouvelle trace de pile.</span><span class="sxs-lookup"><span data-stu-id="4cb99-109">If the debugger needs frame information after a call to `SetIP`, it must perform a new stack trace.</span></span>  
  
 <span data-ttu-id="4cb99-110">[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) essaiera de conserver le frame de pile dans un état valide.</span><span class="sxs-lookup"><span data-stu-id="4cb99-110">[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) will attempt to keep the stack frame in a valid state.</span></span> <span data-ttu-id="4cb99-111">Toutefois, même si le frame est dans un état valide, en ce qui concerne l’exécution, il reste peut-être des problèmes, tels que des variables locales non initialisées et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="4cb99-111">However, even if the frame is in a valid state, as far as the runtime is concerned, there still may be problems, such as uninitialized local variables, and so on.</span></span> <span data-ttu-id="4cb99-112">L’appelant est responsable de la cohérence du programme en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4cb99-112">The caller is responsible for insuring coherency of the running program.</span></span>  
  
 <span data-ttu-id="4cb99-113">Sur les plateformes 64 bits, le pointeur d’instruction ne peut pas être déplacé hors d’un `catch` ou `finally` bloc.</span><span class="sxs-lookup"><span data-stu-id="4cb99-113">On 64-bit platforms, the instruction pointer cannot be moved out of a `catch` or `finally` block.</span></span> <span data-ttu-id="4cb99-114">Si `SetIP` est appelée pour effectuer ce déplacement sur une plateforme 64 bits, il retourne un HRESULT indiquant un échec.</span><span class="sxs-lookup"><span data-stu-id="4cb99-114">If `SetIP` is called to make such a move on a 64-bit platform, it will return an HRESULT indicating failure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4cb99-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4cb99-115">Requirements</span></span>  
 <span data-ttu-id="4cb99-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4cb99-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4cb99-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4cb99-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4cb99-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4cb99-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4cb99-119">**Versions du .NET framework :**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4cb99-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4cb99-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cb99-120">See Also</span></span>  
 