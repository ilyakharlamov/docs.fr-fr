---
title: 'Procédure : Appeler une fonction de page'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- calling page functions [WPF]
- page functions [WPF], calling
- functions [WPF], calling
ms.assetid: a4808397-c6d5-406a-83e0-0091f0c15ae4
ms.openlocfilehash: 4cd839cc959c1e3730418d2feab80b9aef642161
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54542819"
---
# <a name="how-to-call-a-page-function"></a>Procédure : Appeler une fonction de page
Cet exemple montre comment appeler une fonction de page à partir d’un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] page.  
  
## <a name="example"></a>Exemple  
 Vous pouvez accéder à une fonction de page en utilisant un [!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)], tout comme vous pouvez lorsque vous accédez à une page. L'exemple suivant le démontre.  
  
 [!code-csharp[HOWTOPageFunctionSnippets#NavigateToAPageFunctionLikeAPageCODEBEHIND](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml.cs#navigatetoapagefunctionlikeapagecodebehind)]
 [!code-vb[HOWTOPageFunctionSnippets#NavigateToAPageFunctionLikeAPageCODEBEHIND](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/VisualBasic/CallingPage.xaml.vb#navigatetoapagefunctionlikeapagecodebehind)]  
  
 Si vous devez passer des données à la fonction de page, vous pouvez créer une instance de celle-ci et passer les données en définissant une propriété. Ou, comme le montre l’exemple suivant, vous pouvez passer les données à l’aide d’un constructeur autre que celui par défaut.  
  
 [!code-xaml[HOWTOPageFunctionSnippets#CallAPageFunctionXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml#callapagefunctionxaml)]  
  
 [!code-csharp[HOWTOPageFunctionSnippets#CallAPageFunctionCODEBEHIND](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml.cs#callapagefunctioncodebehind)]
 [!code-vb[HOWTOPageFunctionSnippets#CallAPageFunctionCODEBEHIND](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/VisualBasic/CallingPage.xaml.vb#callapagefunctioncodebehind)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Navigation.PageFunction%601>
