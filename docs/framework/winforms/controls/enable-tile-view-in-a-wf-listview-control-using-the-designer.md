---
title: 'Procédure : Activer l’affichage en mosaïque dans un contrôle de ListView Windows Forms à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- tile view feature
- ListView control [Windows Forms], tile view
- tiling [Windows Forms], Windows Forms, controls
ms.assetid: 12f0816a-52b8-41ee-a6d9-ded3a8a5817a
ms.openlocfilehash: 0acd235fe015b3f93364482b83008b388c1b86d9
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303970"
---
# <a name="how-to-enable-tile-view-in-a-windows-forms-listview-control-using-the-designer"></a>Procédure : Activer l’affichage en mosaïque dans un contrôle de ListView Windows Forms à l’aide du Concepteur
La fonctionnalité d’affichage en mosaïque de le <xref:System.Windows.Forms.ListView> contrôle vous permet de fournir un équilibre visuel entre les informations graphiques et textuelles. Les informations textuelles affichées pour un élément dans l'affichage en mosaïque sont identiques aux informations de colonne définies pour le mode Détails. Affichage en mosaïque fonctionne en association avec le regroupement ou d’insertion marque des fonctionnalités dans le <xref:System.Windows.Forms.ListView> contrôle.  
  
 L’affichage en mosaïque utilise une icône 32 x 32 et plusieurs lignes de texte, comme illustré dans l’image suivante.  
  
 ![Affichage en mosaïque dans un contrôle ListView](../../../../docs/framework/winforms/controls/media/listviewtile.gif "ListViewTile")  
  
 Affichage en mosaïque propriétés et méthodes vous permettent de spécifier les champs de colonne à afficher pour chaque élément et contrôler collectivement la taille et l’apparence de tous les éléments dans une fenêtre d’affichage en mosaïque. Pour plus de clarté, la première ligne de texte dans une mosaïque est toujours le nom de l’élément ; Il ne peut pas être modifié.  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.ListView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  L'affichage en mosaïque est disponible uniquement sur [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] quand votre application appelle la méthode <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>. Sur les systèmes d'exploitation antérieurs, tout code lié à l'affichage en mosaïque n'a aucun effet et le contrôle <xref:System.Windows.Forms.ListView> s'affiche en mode Grandes icônes. Pour plus d'informations, consultez <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.  
>   
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-set-tile-view-in-the-designer"></a>Pour définir l’affichage en mosaïque dans le Concepteur  
  
1.  Sélectionnez le <xref:System.Windows.Forms.ListView> contrôle sur votre formulaire.  
  
2.  Dans le **propriétés** fenêtre, sélectionnez le <xref:System.Windows.Forms.ListView.View%2A> propriété et choisissez **vignette**.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ListView.TileSize%2A>
- [Vue d’ensemble du contrôle ListView](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
