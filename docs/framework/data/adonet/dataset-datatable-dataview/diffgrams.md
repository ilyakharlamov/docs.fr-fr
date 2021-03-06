---
title: DiffGrams
ms.date: 03/30/2017
ms.assetid: 037f3991-7bbc-424b-b52e-8b03585d3e34
ms.openlocfilehash: 573da0b608b3f74b9cf789a27a10183f3320f908
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513650"
---
# <a name="diffgrams"></a>DiffGrams
Un DiffGram est un format XML qui identifie la version actuelle et la version d'origine d'éléments de données. L'objet <xref:System.Data.DataSet> utilise le format DiffGram pour charger son contenu et le rendre persistent, ainsi que pour le sérialiser en vue de son transport via une connexion réseau. Lorsqu’un <xref:System.Data.DataSet> est écrit en tant que DiffGram, il remplit le DiffGram avec toutes les informations nécessaires pour recréer précisément le contenu, mais pas le schéma, de la <xref:System.Data.DataSet>, y compris les valeurs de colonne à la fois le **Original** et **actuel** versions de ligne, les informations d’erreur de ligne et ordre des lignes.  
  
 Lors de l’envoi et de l’extraction d’un objet <xref:System.Data.DataSet> à partir d’un service web XML, le format DiffGram est implicitement utilisé. En outre, lors du chargement du contenu d’un <xref:System.Data.DataSet> à partir de XML à l’aide la **ReadXml** (méthode), ou lorsque vous écrivez le contenu d’un <xref:System.Data.DataSet> dans XML à l’aide la **WriteXml** (méthode), vous pouvez spécifier que le contenu sera lu ou écrit sous la forme d’un DiffGram. Pour plus d’informations, consultez [chargement d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md) et [contenu du jeu de données écrit en tant que données XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/writing-dataset-contents-as-xml-data.md).  
  
 Si le format DiffGram est principalement utilisé par le .NET Framework en tant que format de sérialisation pour le contenu d'un objet <xref:System.Data.DataSet>, vous pouvez aussi l'utiliser pour modifier des données dans les tables d'une base de données Microsoft SQL Server.  
  
 Un Diffgram est généré en écrivant le contenu de toutes les tables à une  **\<diffgram >** élément.  
  
### <a name="to-generate-a-diffgram"></a>Pour générer un Diffgram  
  
1.  Générez une liste des tables racine (autrement dit, les tables sans parent).  
  
2.  Pour chaque table et ses descendants dans la liste, écrivez la version actuelle de toutes les lignes dans la première section Diffgram.  
  
3.  Pour chaque table dans le <xref:System.Data.DataSet>, écrivez la version d’origine de toutes les lignes, le cas échéant, dans le  **\<avant >** section du Diffgram.  
  
4.  Pour les lignes qui contiennent des erreurs, écrivez l’erreur contenu dans le  **\<erreurs >** section du Diffgram.  
  
 Un DiffGram est traité dans l'ordre du début du fichier XML à la fin.  
  
### <a name="to-process-a-diffgram"></a>Pour traiter un Diffgram  
  
1.  Traitez la première section du DiffGram qui contient la version actuelle des lignes.  
  
2.  Traitez la deuxième ou le  **\<avant >** section qui contient la version d’origine de la ligne des lignes modifiées et supprimées.  
  
    > [!NOTE]
    >  Si une ligne est marquée comme supprimée, l'opération de suppression peut aussi supprimer les descendants de la ligne, en fonction de la propriété `Cascade` du <xref:System.Data.DataSet> en cours.  
  
3.  Processus la  **\<erreurs >** section. Définissez les informations d'erreur pour la ligne et la colonne spécifiées pour chaque élément dans cette section.  
  
> [!NOTE]
>  Si vous affectez <xref:System.Data.XmlWriteMode> à DiffGram, le contenu du <xref:System.Data.DataSet> cible et du <xref:System.Data.DataSet> d'origine peut être différent.  
  
## <a name="diffgram-format"></a>Format DiffGram  
 Le format DiffGram est divisé en trois sections : les données actuelles, les données d'origine (ou « avant ») et une section d'erreurs, comme indiqué dans l'exemple suivant.  
  
```xml  
<?xml version="1.0"?>  
<diffgr:diffgram   
         xmlns:msdata="urn:schemas-microsoft-com:xml-msdata"  
         xmlns:diffgr="urn:schemas-microsoft-com:xml-diffgram-v1"  
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">  
  
   <DataInstance>  
   </DataInstance>  
  
  <diffgr:before>  
  </diffgr:before>  
  
  <diffgr:errors>  
  </diffgr:errors>  
</diffgr:diffgram>  
```  
  
 Le format DiffGram est constitué des blocs de données suivants :  
  
 **\<**  ***DataInstance***  **>**  
 Le nom de cet élément, ***DataInstance***, est utilisé à des fins d’explication dans cette documentation. Un ***DataInstance*** élément représente un <xref:System.Data.DataSet> ou une ligne d’un <xref:System.Data.DataTable>. Au lieu de *DataInstance*, l’élément contient le nom de la <xref:System.Data.DataSet> ou <xref:System.Data.DataTable>. Ce bloc du format DiffGram contient les données actuelles, qu'elles aient ou non été modifiées. Un élément ou une ligne, ce qui a été modifiée est identifié par le **diffgr : HasChanges** annotation.  
  
 **\<diffgr:before>**  
 Ce bloc du format DiffGram contient la version d'origine d'une ligne. Éléments de ce bloc sont mis en correspondance avec des éléments dans le ***DataInstance*** bloquer à l’aide de la **diffgr : ID** annotation.  
  
 **\<diffgr:errors>**  
 Ce bloc du format DiffGram contient les informations d’erreur pour une ligne particulière dans le ***DataInstance*** bloc. Éléments de ce bloc sont mis en correspondance avec des éléments dans le ***DataInstance*** bloquer à l’aide de la **diffgr : ID** annotation.  
  
## <a name="diffgram-annotations"></a>Annotations DiffGram  
 Les DiffGrams utilisent plusieurs annotations pour relier les éléments des différents blocs DiffGram qui représentent différentes versions d'une ligne ou des informations d'erreur dans le <xref:System.Data.DataSet>.  
  
 Le tableau suivant décrit les annotations DiffGram définies dans l’espace de noms DiffGram **urn : schemas-microsoft-com-diffgram-v1**.  
  
|Annotation|Description|  
|----------------|-----------------|  
|**ID**|Sert à apparier les éléments dans le  **\<diffgr : avant >** et  **\<diffgr : Errors >** blocs aux éléments dans le **\<** ***DataInstance*** **>** bloc. Valeurs avec le **diffgr : ID** annotation se présentent sous la forme *[TableName] [RowIdentifier]*. Par exemple : `<Customers diffgr:id="Customers1">`.|  
|**parentId**|Identifie l’élément à partir de la **\<** ***DataInstance*** **>** bloc est l’élément parent de l’élément actuel. Valeurs avec le **diffgr : parentId** annotation se présentent sous la forme *[TableName] [RowIdentifier]*. Par exemple : `<Orders diffgr:parentId="Customers1">`.|  
|**hasChanges**|Identifie une ligne dans le **\<** ***DataInstance*** **>** bloquer comme modifiée. Le **hasChanges** annotation peut avoir l’une des deux valeurs suivantes :<br /><br /> **inserted**<br /> Identifie un **Added** ligne.<br /><br /> **modified**<br /> Identifie un **Modified** ligne qui contient un **d’origine** version de ligne dans le  **\<diffgr : avant >** bloc. Notez que **Deleted** lignes aura un **d’origine** version de ligne dans le  **\<diffgr : avant >** bloc, mais il n’y aura pas d’élément annoté dans le **\<** ***DataInstance*** **>** bloc.|  
|**hasErrors**|Identifie une ligne dans le **\<** ***DataInstance*** **>** bloquer avec une **RowError**. L’élément de l’erreur est placé dans le  **\<diffgr : Errors >** bloc.|  
|**Error**|Contient le texte de la **RowError** pour un élément particulier dans le  **\<diffgr : Errors >** bloc.|  
  
 Le <xref:System.Data.DataSet> inclut annotations supplémentaires lors de la lecture ou de l'écriture de son contenu en tant que DiffGram. Le tableau suivant décrit ces annotations supplémentaires, qui sont définies dans l’espace de noms **urn : schemas-microsoft-com-msdata**.  
  
|Annotation|Description|  
|----------------|-----------------|  
|**RowOrder**|Conserve l'ordre des lignes des données d'origine et identifie l'index d'une ligne dans un <xref:System.Data.DataTable> donné.|  
|**Hidden**|Identifie une colonne comme ayant une **ColumnMapping** propriété définie sur **MappingType.Hidden**. L’attribut est écrit dans le format **msdata : masqué** *[ColumnName]*= «*valeur*». Par exemple : `<Customers diffgr:id="Customers1" msdata:hiddenContactTitle="Owner">`.<br /><br /> Notez que les colonnes masquées ne sont écrites sous la forme d'un attribut DiffGram que si elles contiennent des données. Sinon, elles sont ignorées.|  
  
## <a name="sample-diffgram"></a>Exemple de DiffGram  
 Un exemple du format DiffGram vous est proposé ci-après. Cet exemple illustre le résultat d'une mise à jour effectuée sur une ligne d'une table avant validation des modifications. La ligne dont le CustomerID est « ALFKI » a été modifiée, mais pas mise à jour. Par conséquent, il existe un **actuel** lignes comportant un **diffgr : ID** « Customers1 » dans le **\<** ***DataInstance*** **>** bloc et un **d’origine** lignes comportant un **diffgr : ID** « Customers1 » dans le  **\<diffgr : avant >** bloc. La ligne dont le CustomerID est « ANATR » comprend un **RowError**, donc il est annoté avec `diffgr:hasErrors="true"` et il existe un élément lié dans le  **\<diffgr : Errors >** bloc.  
  
```xml  
<diffgr:diffgram xmlns:msdata="urn:schemas-microsoft-com:xml-msdata" xmlns:diffgr="urn:schemas-microsoft-com:xml-diffgram-v1">  
  <CustomerDataSet>  
    <Customers diffgr:id="Customers1" msdata:rowOrder="0" diffgr:hasChanges="modified">  
      <CustomerID>ALFKI</CustomerID>  
      <CompanyName>New Company</CompanyName>  
    </Customers>  
    <Customers diffgr:id="Customers2" msdata:rowOrder="1" diffgram:hasErrors="true">  
      <CustomerID>ANATR</CustomerID>  
      <CompanyName>Ana Trujillo Emparedados y Helados</CompanyName>  
    </Customers>  
    <Customers diffgr:id="Customers3" msdata:rowOrder="2">  
      <CustomerID>ANTON</CustomerID>  
      <CompanyName>Antonio Moreno Taquera</CompanyName>  
    </Customers>  
    <Customers diffgr:id="Customers4" msdata:rowOrder="3">  
      <CustomerID>AROUT</CustomerID>  
      <CompanyName>Around the Horn</CompanyName>  
    </Customers>  
  </CustomerDataSet>  
  <diffgr:before>  
    <Customers diffgr:id="Customers1" msdata:rowOrder="0">  
      <CustomerID>ALFKI</CustomerID>  
      <CompanyName>Alfreds Futterkiste</CompanyName>  
    </Customers>  
  </diffgr:before>  
  <diffgr:errors>  
    <Customers diffgr:id="Customers2" diffgr:Error="An optimistic concurrency violation has occurred for this row."/>  
  </diffgr:errors>  
</diffgr:diffgram>  
```  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [Chargement d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [Écriture du contenu d’un DataSet comme données XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/writing-dataset-contents-as-xml-data.md)
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
