---
title: ResetSecurity (fonction) (référence des API non managées)
description: La fonction ResetSecurity assigne un jeton d’emprunt d’identité pour le thread actuel.
ms.date: 11/06/2017
api_name:
- ResetSecurity
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- ResetSecurity
helpviewer_keywords:
- ResetSecurity function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2f117b9807d57847d53cf00fbb4983e187798f09
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730852"
---
# <a name="resetsecurity-function"></a>ResetSecurity (fonction)
Assigne le jeton d’emprunt d’identité fourni au thread actif.   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ResetSecurity (
   [in] HANDLE token
); 
```  

## <a name="parameters"></a>Paramètres

`token`  
[in] Le jeton d’emprunt d’identité à associer avec le thread actuel. Sa valeur peut être `null`. 

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est `S_OK` (0).

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro. Pour obtenir les informations d’erreur étendues, appelez le [GetErrorInfo](geterrorinfo.md) (fonction).
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** WMINet_Utils.idl  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi
- [WMI et compteurs de performances (référence des API non managées)](index.md)
