---
title: "Procédure : Modifier la couleur d'un élément à l'aide d'événements Focus"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- focus events [WPF], changing element color for
- colors of elements [WPF], changing
- elements [WPF], changing color of
ms.assetid: 7e246802-3625-47a7-ae9d-c8a2a40fd040
ms.openlocfilehash: ad5ba8490f4b98512d539f5ae9c72b03333aca69
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547012"
---
# <a name="how-to-change-the-color-of-an-element-using-focus-events"></a>Procédure : Modifier la couleur d'un élément à l'aide d'événements Focus
Cet exemple montre comment modifier la couleur d’un élément lorsqu’il obtient et perd le focus à l’aide de la <xref:System.Windows.UIElement.GotFocus> et <xref:System.Windows.UIElement.LostFocus> événements.  
  
 Cet exemple se compose d’un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier et un fichier code-behind.  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] crée l’interface utilisateur, qui se compose de deux <xref:System.Windows.Controls.Button> objets et attache les gestionnaires d’événements pour le <xref:System.Windows.UIElement.GotFocus> et <xref:System.Windows.UIElement.LostFocus> événements pour le <xref:System.Windows.Controls.Button> objets.  
  
 [!code-xaml[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml#gotlostfocussamplexaml)]  
  
 Le code-behind suivant crée le <xref:System.Windows.UIElement.GotFocus> et <xref:System.Windows.UIElement.LostFocus> gestionnaires d’événements.  Lorsque le <xref:System.Windows.Controls.Button> gains le focus clavier, la <xref:System.Windows.Controls.Control.Background%2A> de la <xref:System.Windows.Controls.Button> est modifié en rouge.  Lorsque le <xref:System.Windows.Controls.Button> perd le focus clavier, la <xref:System.Windows.Controls.Control.Background%2A> de la <xref:System.Windows.Controls.Button> repasse au blanc.  
  
 [!code-csharp[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](../../../../samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml.cs#gotlostfocussampleeventhandlers)]
 [!code-vb[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/VisualBasic/Window1.xaml.vb#gotlostfocussampleeventhandlers)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des entrées](../../../../docs/framework/wpf/advanced/input-overview.md)
