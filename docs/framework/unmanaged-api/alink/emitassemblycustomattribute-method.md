---
title: EmitAssemblyCustomAttribute, méthode
ms.date: 03/30/2017
api_name:
- IALink.EmitAssemblyCustomAttribute
- EmitAssemblyCustomAttribute
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitAssemblyCustomAttribute
helpviewer_keywords:
- EmitAssemblyCustomAttribute method
ms.assetid: b72f5409-79af-4fa7-90a7-7630eec170f1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7b4909ae23d077ee079e062d0252dbf1ee11663c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538828"
---
# <a name="emitassemblycustomattribute-method"></a>EmitAssemblyCustomAttribute, méthode
Appel permettant de définir les attributs personnalisés de niveau assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EmitAssemblyCustomAttribute(  
    mdAssembly   AssemblyID,  
    mdToken      FileToken,  
    mdToken      tkType,  
    void const*  pCustomValue,  
    DWORD        cbCustomValue,  
    BOOL         bSecurity,  
    BOOL         bAllowMulti  
) PURE;  
```  
  
#### <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID de l’assembly.  
  
 `FileToken`  
 Fichier qui définit l’attribut. Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.  
  
 `tkType`  
 Type de l’attribut personnalisé.  
  
 `pCustomValue`  
 Valeur des données personnalisées.  
  
 `cbCustomValue`  
 Longueur des données de valeur personnalisée.  
  
 `bSecurity`  
 TRUE si l’attribut personnalisé est associé à la signature de l’assembly.  
  
 `bAllowMulti`  
 TRUE si plusieurs attributs doivent être émis.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 Nécessite alink.h  
  
## <a name="see-also"></a>Voir aussi
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
