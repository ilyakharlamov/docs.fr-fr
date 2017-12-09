---
title: "ICLRDataTarget2::FreeVirtual, méthode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDataTarget2.FreeVirtual
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICLRDataTarget2::FreeVirtual
helpviewer_keywords:
- ICLRDataTarget::FreeVirtual method [.NET Framework debugging]
- FreeVirtual method [.NET Framework debugging]
ms.assetid: 26fb69f8-1467-4711-bd24-cb117c63938f
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 1619e9eb02eec1985c3c550626ef955162d1b984
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="iclrdatatarget2freevirtual-method"></a><span data-ttu-id="0cc4c-102">ICLRDataTarget2::FreeVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="0cc4c-102">ICLRDataTarget2::FreeVirtual Method</span></span>
<span data-ttu-id="0cc4c-103">Appelé par les services d’accès aux données du common language runtime (CLR) de mémoire précédemment alloué dans l’espace d’adressage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="0cc4c-103">Called by the common language runtime (CLR) data access services to free memory that was previously allocated in the address space of the target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0cc4c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cc4c-104">Syntax</span></span>  
  
```  
HRESULT FreeVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0cc4c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cc4c-105">Parameters</span></span>  
 `addr`  
 <span data-ttu-id="0cc4c-106">[in] A `CLRDATA_ADDRESS` valeur qui spécifie l’adresse de départ de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="0cc4c-106">[in] A `CLRDATA_ADDRESS` value that specifies the starting address of the memory to be freed.</span></span>  
  
 `size`  
 <span data-ttu-id="0cc4c-107">[in] La taille, en octets, de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="0cc4c-107">[in] The size, in bytes, of the memory to be freed.</span></span>  
  
 `typeFlags`  
 <span data-ttu-id="0cc4c-108">[in] Indicateurs qui contrôlent la libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0cc4c-108">[in] Flags that control the freeing of memory.</span></span> <span data-ttu-id="0cc4c-109">Consultez Win32 `VirtualFree` (fonction).</span><span class="sxs-lookup"><span data-stu-id="0cc4c-109">See the Win32 `VirtualFree` function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0cc4c-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="0cc4c-110">Remarks</span></span>  
 <span data-ttu-id="0cc4c-111">Le `FreeVirtual` méthode sert de wrapper logique pour Win32 `VirtualFree` (fonction).</span><span class="sxs-lookup"><span data-stu-id="0cc4c-111">The `FreeVirtual` method serves as a logical wrapper for the Win32 `VirtualFree` function.</span></span>  
  
 <span data-ttu-id="0cc4c-112">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="0cc4c-112">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0cc4c-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0cc4c-113">Requirements</span></span>  
 <span data-ttu-id="0cc4c-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0cc4c-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0cc4c-115">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="0cc4c-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="0cc4c-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0cc4c-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0cc4c-117">**Versions du .NET framework :**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0cc4c-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0cc4c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cc4c-118">See Also</span></span>  
 [<span data-ttu-id="0cc4c-119">ICLRDataTarget2 (Interface)</span><span class="sxs-lookup"><span data-stu-id="0cc4c-119">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)  
 [<span data-ttu-id="0cc4c-120">AllocVirtual (méthode)</span><span class="sxs-lookup"><span data-stu-id="0cc4c-120">AllocVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-allocvirtual-method.md)