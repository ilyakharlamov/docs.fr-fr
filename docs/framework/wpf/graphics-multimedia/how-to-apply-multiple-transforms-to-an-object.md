---
title: 'Procédure : Appliquer plusieurs transformations à un objet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- grouping Transform objects [WPF]
- Transform objects [WPF], grouping
- graphics [WPF], grouping Transform objects
- TransformGroup [WPF]
ms.assetid: 98cd1921-12bc-4bf5-8193-529228fb7402
ms.openlocfilehash: dc9b7c052d9deb4d1167c813a6ce652c99983a9f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649451"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Procédure : Appliquer plusieurs transformations à un objet
Cet exemple montre comment utiliser un <xref:System.Windows.Media.TransformGroup> au groupe de deux ou plusieurs <xref:System.Windows.Media.Transform> des objets dans un composite unique <xref:System.Windows.Media.Transform>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.TransformGroup> pour appliquer un <xref:System.Windows.Media.ScaleTransform> et un <xref:System.Windows.Media.RotateTransform> à un <xref:System.Windows.Controls.Button>.  
  
 [!code-xaml[Transforms_snip#MultipleTransformExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MultipleTransformExample.xaml#multipletransformexamplewholepage)]  
  
 [!code-csharp[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/MultipleTransformsExample.cs#multipletransformscodeexamplewholepage)]
 [!code-vb[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/MultipleTransformsExample.vb#multipletransformscodeexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Media.TransformGroup>
- [Vue d’ensemble des transformations](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [Exemple de transformations 2D](https://go.microsoft.com/fwlink/?LinkID=158252)
