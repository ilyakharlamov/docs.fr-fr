---
title: Gestion des exceptions - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- exception handling [C#], about exception handling
- exceptions [C#], handling
ms.assetid: b4e4ecf2-b907-4e58-891f-2563762258e9
ms.openlocfilehash: 79b07891d794200507cdb97a869992ef093aff23
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648750"
---
# <a name="exception-handling-c-programming-guide"></a>Gestion des exceptions (Guide de programmation C#)
Un bloc [try](../../../csharp/language-reference/keywords/try-catch.md) est utilisé par les programmeurs C# pour partitionner du code susceptible d’être affecté par une exception. Des blocs [catch](../../../csharp/language-reference/keywords/try-catch.md) associés sont utilisés pour gérer les exceptions générées. Un bloc [finally](../../../csharp/language-reference/keywords/try-finally.md) contient du code qui s’exécute dans tous les cas, qu’une exception soit levée ou non dans le bloc `try` (il peut s’agir par exemple de la libération des ressources allouées dans le bloc `try`). Un bloc `try` doit être associé à un ou plusieurs blocs `catch`, à un bloc `finally`, ou aux deux.  
  
 Les exemples suivants montrent une instruction `try-catch`, une instruction `try-finally` et une instruction `try-catch-finally`.  
  
 [!code-csharp[csProgGuideExceptions#6](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/exception-handling_1.cs)]  
  
 [!code-csharp[csProgGuideExceptions#7](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/exception-handling_2.cs)]  
  
 [!code-csharp[csProgGuideExceptions#8](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/exception-handling_3.cs)]  
  
 Un bloc `try` sans bloc `catch` ou `finally` provoque une erreur du compilateur.  
  
## <a name="catch-blocks"></a>Blocs catch  
 Un bloc `catch` peut spécifier le type d’exception à intercepter. La spécification de type est appelée *filtre d’exception*. Le type d’exception doit être dérivé de <xref:System.Exception>. En général, ne spécifiez pas <xref:System.Exception> comme filtre d’exception, sauf si vous savez comment gérer toutes les exceptions susceptibles d’être levées dans le bloc `try` ou si vous avez inclus une instruction [throw](../../../csharp/language-reference/keywords/throw.md) à la fin de votre bloc `catch`.  
  
 Vous pouvez chaîner plusieurs blocs `catch` avec des filtres d’exception différents. Les blocs `catch` sont évalués de haut en bas dans votre code, mais un seul bloc `catch` est exécuté pour chaque exception levée. Le premier bloc `catch` qui spécifie le type exact ou une classe de base de l’exception levée est exécuté. Si aucun bloc `catch` ne spécifie un filtre d’exception correspondant, un bloc `catch` qui n’a pas de filtre est sélectionné, s’il y en a un dans l’instruction. Lors du positionnement des blocs `catch`, il est important de placer en premier les types d’exception les plus spécifiques (c’est-à-dire les plus dérivés).  
  
 Vous devez intercepter les exceptions quand les conditions suivantes sont remplies :  
  
-   Vous savez pourquoi l’exception a été levée et vous pouvez implémenter une récupération spécifique, par exemple inviter l’utilisateur à entrer un nouveau nom de fichier quand vous interceptez un objet <xref:System.IO.FileNotFoundException>.  
  
-   Vous pouvez créer et lever une nouvelle exception plus spécifique.  
  
     [!code-csharp[csProgGuideExceptions#9](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/exception-handling_4.cs)]  
  
-   Vous voulez traiter partiellement une exception avant de la transmettre en vue d’un traitement supplémentaire. Dans l’exemple suivant, un bloc `catch` est utilisé pour ajouter une entrée à un journal d’erreurs avant de relever l’exception.  
  
     [!code-csharp[csProgGuideExceptions#10](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/exception-handling_5.cs)]  
  
## <a name="finally-blocks"></a>Blocs Finally  
 Un bloc `finally` vous permet de nettoyer les actions qui sont exécutées dans un bloc `try`. S’il est présent, le bloc `finally` s’exécute en dernier, après le bloc `try` et tout bloc `catch` mis en correspondance. Un bloc `finally` s’exécute toujours, qu’une exception soit levée ou non, et même si aucun bloc `catch` correspondant au type d’exception n’est trouvé.  
  
 Le bloc `finally` peut être utilisé pour libérer des ressources telles que des flux de fichiers, des connexions de base de données et des handles graphiques, sans attendre que le récupérateur de mémoire dans le runtime finalise les objets. Pour plus d’informations, consultez [Instruction using](../../../csharp/language-reference/keywords/using-statement.md).  
  
 Dans l’exemple suivant, le bloc `finally` est utilisé pour fermer un fichier ouvert dans le bloc `try`. Notez que l’état du handle de fichier est vérifié avant la fermeture du fichier. Si le bloc `try` ne peut pas ouvrir le fichier, le handle de fichier a encore la valeur `null` et le bloc `finally` n’essaie pas de le fermer. En guise d’alternative, si le fichier est ouvert avec succès dans le bloc `try`, le bloc `finally` ferme le fichier ouvert.  
  
 [!code-csharp[csProgGuideExceptions#11](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/exception-handling_6.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  

Pour plus d’informations, consultez [Exceptions](~/_csharplang/spec/exceptions.md) et [Instruction try](~/_csharplang/spec/statements.md#the-try-statement) dans la [spécification du langage C#](../../language-reference/language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Exceptions et gestion des exceptions](../../../csharp/programming-guide/exceptions/index.md)
- [try-catch](../../../csharp/language-reference/keywords/try-catch.md)
- [try-finally](../../../csharp/language-reference/keywords/try-finally.md)
- [try-catch-finally](../../../csharp/language-reference/keywords/try-catch-finally.md)
- [using, instruction](../../../csharp/language-reference/keywords/using-statement.md)
