---
title: 'Procédure : Sélectionnez une plage de Dates dans le contrôle MonthCalendar Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- dates [Windows Forms], selecting range in calendar controls
- examples [Windows Forms], calendar controls
- calendars [Windows Forms], selecting date range
- MonthCalendar control [Windows Forms], selecting date range
ms.assetid: 95d9ab95-b0f8-4c19-9f63-b5cd4593a5d0
ms.openlocfilehash: 4c7100f77c313d219cfd4cceff5ae3015eae4c18
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558447"
---
# <a name="how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control"></a>Procédure : Sélectionnez une plage de Dates dans le contrôle MonthCalendar Windows Forms
Une fonctionnalité importante des formulaires Windows <xref:System.Windows.Forms.MonthCalendar> contrôle est que l’utilisateur peut sélectionner une plage de dates. Cette fonctionnalité est une amélioration au-dessus de la fonctionnalité de sélection de la date de la <xref:System.Windows.Forms.DateTimePicker> contrôle, ce qui permet uniquement à l’utilisateur de sélectionner une valeur de date/heure unique. Vous pouvez définir une plage de dates ou obtenir une plage de sélection définie par l’utilisateur à l’aide des propriétés de la <xref:System.Windows.Forms.MonthCalendar> contrôle. L’exemple de code suivant montre comment définir une plage de sélection.  
  
### <a name="to-select-a-range-of-dates"></a>Pour sélectionner une plage de dates  
  
1.  Créer <xref:System.DateTime> objets qui représentent les première et dernière dates dans une plage.  
  
    ```vb  
    Dim projectStart As Date = New DateTime(2001, 2, 13)  
    Dim projectEnd As Date = New DateTime(2001, 2, 28)  
    ```  
  
    ```csharp  
    DateTime projectStart = new DateTime(2001, 2, 13);  
    DateTime projectEnd = new DateTime(2001, 2, 28);  
    ```  
  
    ```cpp  
    DateTime projectStart = DateTime(2001, 2, 13);  
    DateTime projectEnd = DateTime(2001, 2, 28);  
    ```  
  
2.  Définissez la propriété <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A>.  
  
    ```vb  
    MonthCalendar1.SelectionRange = New SelectionRange(projectStart, projectEnd)  
    ```  
  
    ```csharp  
    monthCalendar1.SelectionRange = new SelectionRange(projectStart, projectEnd);  
    ```  
  
    ```cpp  
    monthCalendar1->SelectionRange = gcnew  
       SelectionRange(projectStart, projectEnd);  
    ```  
  
     – ou –  
  
     Définissez les propriétés <xref:System.Windows.Forms.MonthCalendar.SelectionStart%2A> et <xref:System.Windows.Forms.MonthCalendar.SelectionEnd%2A>.  
  
    ```vb  
    MonthCalendar1.SelectionStart = projectStart  
    MonthCalendar1.SelectionEnd = projectEnd  
    ```  
  
    ```csharp  
    monthCalendar1.SelectionStart = projectStart;  
    monthCalendar1.SelectionEnd = projectEnd;  
    ```  
  
    ```cpp  
    monthCalendar1->SelectionStart = projectStart;  
    monthCalendar1->SelectionEnd = projectEnd;  
    ```  
  
## <a name="see-also"></a>Voir aussi
- [MonthCalendar, contrôle](../../../../docs/framework/winforms/controls/monthcalendar-control-windows-forms.md)
- [Guide pratique pour Modifier l’apparence du contrôle de MonthCalendar de formulaires Windows](../../../../docs/framework/winforms/controls/how-to-change-monthcalendar-control-appearance.md)
- [Guide pratique pour Afficher en gras certains jours avec les Windows Forms du contrôle MonthCalendar](../../../../docs/framework/winforms/controls/display-specific-days-in-bold-with-wf-monthcalendar-control.md)
- [Guide pratique pour Afficher plusieurs mois dans le contrôle MonthCalendar Windows Forms](../../../../docs/framework/winforms/controls/display-more-than-one-month-wf-monthcalendar-control.md)
