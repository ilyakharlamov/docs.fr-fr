---
title: Analyse du code source LINQ to SQL
ms.date: 03/30/2017
ms.assetid: cba3eef8-e108-4478-b588-ad59580e133e
ms.openlocfilehash: 4b1d2d2c54ae99a65f60c96b6330e3f94db6beb5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696852"
---
# <a name="analyzing-linq-to-sql-source-code"></a>Analyse du code source LINQ to SQL
En exécutant les étapes suivantes, vous pouvez générer le code source [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] à partir de l'exemple de base de données Northwind. Vous pouvez comparer des éléments du modèle objet avec des éléments de la base de données pour mieux comprendre comment les différents éléments sont mappés.  
  
> [!NOTE]
>  Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_short](../../../../../../includes/vs-ordesigner-short-md.md)] pour générer ce code.  
  
1.  Si vous n'avez pas déjà l'exemple de base de données Northwind sur votre ordinateur de développement, vous pouvez le télécharger gratuitement. Pour plus d’informations, consultez [téléchargement d’exemples de bases de données](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md).  
  
2.  Utilisez l'outil en ligne de commande SQLMetal pour générer un fichier source Visual Basic ou C#. Pour plus d’informations, consultez [SqlMetal.exe (outil de génération de code)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md). En tapant les commandes suivantes à une invite de commandes, vous pouvez générer les fichiers sources Visual Basic et C# qui incluent des procédures stockées et des fonctions :  
  
    -   `sqlmetal /code:northwind.vb /language:vb "c:\northwnd.mdf" /sprocs /functions /pluralize`  
  
    -   `sqlmetal /code:northwind.cs /language:csharp "c:\northwnd.mdf" /sprocs /functions /pluralize`  
  
## <a name="see-also"></a>Voir aussi
- [Référence](../../../../../../docs/framework/data/adonet/sql/linq/reference.md)
- [Informations générales](../../../../../../docs/framework/data/adonet/sql/linq/background-information.md)
