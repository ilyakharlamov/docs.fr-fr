---
title: Opérateur AddressOf (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- AddressOf
- vb.AddressOf
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- addresses, passing to API procedures
ms.assetid: 8105a59d-60d8-4ab5-b221-5899cdfacbf4
ms.openlocfilehash: 4f4f88551b6708ac3d0ee0f0f5bdcbdec1dfaaa9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721065"
---
# <a name="addressof-operator-visual-basic"></a>Opérateur AddressOf (Visual Basic)
Crée une instance de délégué de procédure qui fait référence à la procédure spécifique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
AddressOf procedurename  
```  
  
## <a name="parts"></a>Composants  
 `procedurename`  
 Obligatoire. Indique la procédure à référencer par le délégué de procédure nouvellement créé.  
  
## <a name="remarks"></a>Notes  
 Le `AddressOf` opérateur crée un délégué de fonction qui pointe vers la fonction spécifiée par `procedurename`. Lorsque la procédure spécifiée est qu'une méthode d’instance puis le délégué de fonction fait référence à l’instance et la méthode. Ensuite, lorsque le délégué de fonction est appelé la méthode spécifiée de l’instance spécifiée est appelée.  
  
 Le `AddressOf` opérateur peut être utilisé comme opérande d’un constructeur délégué ou il peut être utilisé dans un contexte dans lequel le type du délégué peut être déterminé par le compilateur.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `AddressOf` opérateur pour désigner un délégué pour gérer le `Click` événements d’un bouton.  
  
 [!code-vb[VbVbalrDelegates#8](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addressof-operator_1.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `AddressOf` opérateur pour désigner la fonction de démarrage d’un thread.  
  
 [!code-vb[VbVbalrDelegates#9](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addressof-operator_2.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Délégués](../../../visual-basic/programming-guide/language-features/delegates/index.md)
