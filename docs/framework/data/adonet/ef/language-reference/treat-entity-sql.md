---
title: TREAT (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5b77f156-55de-4cb4-8154-87f707d4c635
ms.openlocfilehash: 1a65c73b8c6013c2b78343224c5bbb925101f9f3
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55903779"
---
# <a name="treat-entity-sql"></a>TREAT (Entity SQL)
Traite un objet d'un type de base déterminé en tant qu'objet du type dérivé spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
TREAT ( expression as type)  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression de requête valide qui retourne une entité.  
  
> [!NOTE]
>  Le type de l'expression spécifiée doit être un sous-type du type de données spécifié, ou le type de données doit être un sous-type du type de l'expression.  
  
 `type`  
 Type d'entité. Le type doit être qualifié par un espace de noms.  
  
> [!NOTE]
>  L'expression spécifiée doit être un sous-type du type de données spécifié, ou le type de données doit être un sous-type de l'expression.  
  
## <a name="return-value"></a>Valeur de retour  
 Valeur du type de données spécifié.  
  
## <a name="remarks"></a>Notes  
 TREAT est utilisé pour effectuer un upcast entre des classes connexes. Par exemple, si `Employee` est dérivé de `Person` et que p est de type `Person`, `TREAT(p AS NamespaceName.Employee)` effectue un upcast d'une instance générique de `Person` vers `Employee`; autrement dit, cela vous permet de traiter p en tant que `Employee`.  
  
 TREAT est utilisé dans des scénarios d'héritage dans lesquels vous pouvez exécuter une requête de ce type :  
  
```  
SELECT TREAT(p AS NamespaceName.Employee)  
FROM ContainerName.Person AS p  
WHERE p IS OF (NamespaceName.Employee)   
```  
  
 Cette requête effectue un upcast d'entités `Person` vers le type `Employee` . S'il s'avère que la valeur de p n'est pas de type `Employee`, l'expression génère la valeur `null`.  
  
> [!NOTE]
>  L’expression spécifiée `Employee` doit être un sous-type du type de données spécifié `Person`, ou le type de données doit être un sous-type de l’expression. Sinon, l'expression génère une erreur de compilation.  
  
 Le tableau suivant indique le comportement de TREAT sur certains modèles communs et d'autres moins courants. Toutes les exceptions sont levées côté client avant que le fournisseur soit appelé :  
  
|Modèle|Comportement|  
|-------------|--------------|  
|`TREAT (null AS EntityType)`|Retourne `DbNull`.|  
|`TREAT (null AS ComplexType)`|Lève une exception.|  
|`TREAT (null AS RowType)`|Lève une exception/|  
|`TREAT (EntityType AS EntityType)`|Retourne `EntityType` ou la valeur `null`.|  
|`TREAT (ComplexType AS ComplexType)`|Lève une exception.|  
|`TREAT (RowType AS RowType)`|Lève une exception.|  
  
## <a name="example"></a>Exemple  
 La requête [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ci-dessous utilise l'opérateur TREAT pour convertir un objet du type Course en collection d'objets du type OnsiteCourse. Cette requête est basée sur le modèle [School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)).  
  
 [!code-csharp[DP EntityServices Concepts 2#TREAT_ISOF](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#treat_isof)]  
  
## <a name="see-also"></a>Voir aussi
- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Types structurés autorisant la valeur null](../../../../../../docs/framework/data/adonet/ef/language-reference/nullable-structured-types-entity-sql.md)
