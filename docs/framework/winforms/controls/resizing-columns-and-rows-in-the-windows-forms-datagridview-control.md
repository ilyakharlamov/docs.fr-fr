---
title: Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], sizing rows and columns
- columns [Windows Forms], resizing in grids
- data grids [Windows Forms], resizing columns and rows
ms.assetid: 7532764d-e5c1-4943-a08b-6377a722d3b6
ms.openlocfilehash: e2be90a1367bdcbb5b9c6441a407e3e23e5204c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54711247"
---
# <a name="resizing-columns-and-rows-in-the-windows-forms-datagridview-control"></a>Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms
Le `DataGridView` contrôle fournit de nombreuses options permettant de personnaliser le comportement de dimensionnement de ses colonnes et de lignes. En règle générale, `DataGridView` cellules ne se redimensionnent pas en fonction de leur contenu. Au lieu de cela, elles tronquent toute valeur d’affichage qui est supérieure à la cellule. Si le contenu peut être affiché sous forme de chaîne, la cellule l’affiche dans une info-bulle.  
  
 Par défaut, les utilisateurs peuvent faire glisser de ligne, colonne et les séparateurs d’en-têtes avec la souris pour afficher plus d’informations. Les utilisateurs peuvent également double-cliquer sur un séparateur pour redimensionner automatiquement la bande de ligne, colonne ou en-tête associée, en fonction de son contenu.  
  
 Le `DataGridView` contrôle fournit des propriétés, méthodes et événements qui vous permettent de personnaliser ou de désactiver tous ces comportements dirigé par l’utilisateur. En outre, vous pouvez redimensionner par programme les lignes, colonnes et en-têtes en fonction de leur contenu, ou vous pouvez les configurer pour se redimensionnent automatiquement lorsque leur contenu change. Vous pouvez également configurer des colonnes pour diviser automatiquement la largeur disponible du contrôle dans des proportions que vous spécifiez.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Options de dimensionnement dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/sizing-options-in-the-windows-forms-datagridview-control.md)  
 Décrit les options de dimensionnement de lignes, des colonnes et des en-têtes. Également fournit des détails sur les méthodes et propriétés relatives au dimensionnement et décrit les scénarios d’utilisation courants.  
  
 [Mode Remplissage des colonnes dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/column-fill-mode-in-the-windows-forms-datagridview-control.md)  
 Décrit le mode de remplissage de colonne en détail et fournit du code de démonstration qui vous permettent de faire des essais avec le mode de remplissage de colonne et les autres modes.  
  
 [Guide pratique pour Définir les Modes de redimensionnement du contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/how-to-set-the-sizing-modes-of-the-windows-forms-datagridview-control.md)  
 Décrit comment configurer les modes de dimensionnement pour des objectifs communs.  
  
 [Guide pratique pour Redimensionner par programme les cellules en fonction du contenu dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/programmatically-resize-cells-to-fit-content-in-the-datagrid.md)  
 Fournit du code de démonstration que vous pouvez utiliser pour expérimenter le redimensionnement par programmation.  
  
 [Guide pratique pour Redimensionner automatiquement des cellules lorsque le contenu change dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/automatically-resize-cells-when-content-changes-in-the-datagrid.md)  
 Fournit du code de démonstration qui vous permettent de faire des essais avec les modes de dimensionnement automatique.  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.DataGridView>  
 Fournit la documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.  
  
## <a name="see-also"></a>Voir aussi
- [DataGridView, contrôle](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)
