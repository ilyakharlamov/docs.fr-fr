---
title: Collections et structures de données
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
  - grouping data in collections
  - 'objects [.NET Framework], grouping in collections'
  - 'Array class, grouping data in collections'
  - 'threading [.NET Framework], safety'
  - Collections classes
  - 'collections [.NET Framework]'
ms.assetid: 60cc581f-1db5-445b-ba04-a173396bf872
author: mairaw
ms.author: mairaw
---
# <a name="collections-and-data-structures"></a>Collections et structures de données
Des données similaires peuvent souvent être gérées plus efficacement quand elles sont stockées et manipulées en tant que collection. Vous pouvez utiliser la classe <xref:System.Array?displayProperty=nameWithType>, ou les classes qui se trouvent dans les espaces de noms <xref:System.Collections>, <xref:System.Collections.Generic>, <xref:System.Collections.Concurrent> et System.Collections.Immutable, pour ajouter, supprimer et modifier des éléments individuels ou une série d’éléments dans une collection.  
  
 Il existe deux principaux types de collections : les collections génériques et non génériques. Les collections génériques ont été ajoutées au .NET Framework 2.0 et fournissent des collections de type sécurisé au moment de la compilation. Pour cette raison, les collections génériques offrent généralement de meilleures performances. Les collections génériques acceptent un paramètre de type lorsqu'elles sont construites, et ne nécessitent pas de transtypage du type <xref:System.Object> quand vous ajoutez ou supprimez des éléments de la collection.  De plus, la plupart des collections génériques sont prises en charge par les applications du [!INCLUDE[win8_appstore_long](../../../includes/win8-appstore-long-md.md)]. Les collections non génériques stockent les éléments en tant que <xref:System.Object>, nécessitent un transtypage, et la plupart ne sont pas prises en charge pour le développement d'applications [!INCLUDE[win8_appstore_long](../../../includes/win8-appstore-long-md.md)]. Cependant, vous pouvez rencontrer ces collections non génériques dans du code plus ancien.  
  
 Depuis [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], les collections figurant dans l'espace de noms <xref:System.Collections.Concurrent> fournissent des opérations thread-safe efficaces pour accéder aux éléments de collection à partir de plusieurs threads. Les classes de collection immuable de l’espace de noms System.Collections.Immutable ([NuGet package](https://www.nuget.org/packages/System.Collections.Immutable)) sont thread-safe, car les opérations sont effectuées sur une copie de la collection d’origine et celle-ci ne peut donc pas être modifiée.  
  
  
<a name="BKMK_Commoncollectionfeatures"></a>   
## <a name="common-collection-features"></a>Fonctionnalités communes à toutes les collections  
 Toutes les collections fournissent des méthodes pour l'ajout, la suppression ou la recherche d'éléments au sein d'une collection. De plus, toutes les collections qui implémentent directement ou indirectement l'interface <xref:System.Collections.ICollection> ou <xref:System.Collections.Generic.ICollection%601> partagent les fonctionnalités suivantes :  
  
-   **Possibilité d'énumérer la collection**  
  
     Les collections du .NET Framework implémentent soit <xref:System.Collections.IEnumerable?displayProperty=nameWithType>, soit <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> pour permettre à la collection d'être parcourue. Un énumérateur peut être vu comme un pointeur mobile pointant vers n'importe quel élément d'une collection. L’instruction [foreach, in](../../csharp/language-reference/keywords/foreach-in.md) et [For Each...Next Instruction](../../visual-basic/language-reference/statements/for-each-next-statement.md) utilisent l’énumérateur exposé par la méthode <xref:System.Collections.IEnumerable.GetEnumerator%2A> et masquent la complexité de la manipulation de l’énumérateur. En outre, toute collection qui implémente <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> est considérée comme étant un *type requêtable* et peut être interrogée avec LINQ. Les requêtes LINQ fournissent un modèle commun d'accès aux données. Elles sont généralement plus concises et lisibles que les boucles `foreach` standard, et fournissent des fonctionnalités de filtrage, de tri et de regroupement. Les requêtes LINQ peuvent également améliorer les performances. Pour plus d’informations, consultez [LINQ to Objects (C#)](../../csharp/programming-guide/concepts/linq/linq-to-objects.md), [LINQ to Objects (Visual Basic)](../../visual-basic/programming-guide/concepts/linq/linq-to-objects.md), [Parallel LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md), [Introduction aux requêtes LINQ (C#)](../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md) et [Opérations de requête de base (Visual Basic)](../../visual-basic/programming-guide/concepts/linq/basic-query-operations.md).  
  
-   **La possibilité de copier le contenu d'une collection dans un tableau**  
  
     Toutes les collections peuvent être copiées dans un tableau à l'aide de la méthode **CopyTo**. Toutefois, l'ordre des éléments du nouveau tableau sera basé sur l'ordre où ils sont retournés par l'énumérateur. Le tableau résultant est toujours unidimensionnel avec une limite inférieure de zéro.  
  
 De plus, de nombreuses classes de collection comprennent les fonctionnalités suivantes :  
  
-   **Propriétés Capacity et Count**  
  
     La propriété Capacity d'une collection indique le nombre d'éléments qu'elle peut contenir. La propriété Count d'une collection indique le nombre d'éléments qu'elle contient réellement. Certaines collections masquent l'une de ces propriétés, voire les deux.  
  
     La capacité de la plupart des collections s'étend automatiquement quand la valeur de la propriété Capacity est atteinte. La mémoire est réallouée et les éléments sont copiés depuis l'ancienne collection vers la nouvelle. Cela permet de réduire le code nécessaire à l'utilisation de la collection. Toutefois, les performances de la collection peuvent être affectées. Par exemple, pour <xref:System.Collections.Generic.List%601>, si <xref:System.Collections.Generic.List%601.Count%2A> est inférieur à <xref:System.Collections.Generic.List%601.Capacity%2A>, l'ajout d'un élément correspond à une opération O(1). Si la capacité doit être augmentée pour intégrer un nouvel élément, l'ajout d'un élément devient une opération O(n), où n est <xref:System.Collections.Generic.List%601.Count%2A>. Le meilleur moyen d'éviter la dégradation des performances en raison des réallocations est de définir la propriété Capacity sur la taille estimée de la collection.  
  
     <xref:System.Collections.BitArray> est un cas particulier. Sa capacité est égale à sa longueur, qui est elle-même égale à son nombre.  
  
-   **Une limite inférieure cohérente**  
  
     La limite inférieure d'une collection est l'index de son premier élément. Toutes les collections indexées dans l'espace de noms <xref:System.Collections> ont une limite inférieure de zéro, ce qui signifie qu'elles sont indexées à 0. Par défaut, <xref:System.Array> a une limite inférieure de zéro. Vous pouvez cependant définir une autre limite inférieure quand vous créez une instance de la classe **Array** avec <xref:System.Array.CreateInstance%2A?displayProperty=nameWithType>.  
  
-   **Synchronisation pour un accès depuis plusieurs threads** (classes <xref:System.Collections> uniquement).  
  
     Les types de collections non génériques de l'espace de noms <xref:System.Collections> fournissent une certaine cohérence de thread pour la synchronisation, généralement exposée par des membres <xref:System.Collections.ICollection.SyncRoot%2A> et <xref:System.Collections.ICollection.IsSynchronized%2A>. Ces collections ne sont pas thread-safe par défaut. Si vous avez besoin d'un accès multithread évolutif et efficace pour une collection, utilisez l'une des classes de l'espace de noms <xref:System.Collections.Concurrent> ou envisagez d'utiliser une collection immuable. Pour plus d’informations, consultez [Collections thread-safe](../../../docs/standard/collections/thread-safe/index.md).  
  
<a name="BKMK_Choosingacollection"></a>   
## <a name="choosing-a-collection"></a>Choix d'une collection  
 En règle générale, vous devez utiliser des collections génériques. Le tableau suivant décrit certains scénarios courants concernant les collections, ainsi que les classes de collection que vous pouvez utiliser pour ces scénarios. Si vous ne connaissez pas encore les collections génériques, ce tableau vous aidera à choisir la collection générique qui répond le mieux à vos besoins.  
 
|Je souhaite :|Options de collection générique|Options de collection non générique|Options de collection thread-safe ou immuable|  
|-|-|-|-|  
|Stocker les éléments sous forme de paires clé/valeur pour une recherche rapide par clé|<xref:System.Collections.Generic.Dictionary%602>|<xref:System.Collections.Hashtable><br /><br /> (Collection de paires clé/valeur organisées en fonction du code de hachage de la clé).|<xref:System.Collections.Concurrent.ConcurrentDictionary%602><br /><br /> <xref:System.Collections.ObjectModel.ReadOnlyDictionary%602><br /><br /> <xref:System.Collections.Immutable.ImmutableDictionary%602>|  
|Accéder aux éléments par index|<xref:System.Collections.Generic.List%601>|<xref:System.Array><br /><br /> <xref:System.Collections.ArrayList>|<xref:System.Collections.Immutable.ImmutableList%601><br /><br /> <xref:System.Collections.Immutable.ImmutableArray>|  
|Utiliser des éléments premier entré, premier sorti (FIFO)|<xref:System.Collections.Generic.Queue%601>|<xref:System.Collections.Queue>|<xref:System.Collections.Concurrent.ConcurrentQueue%601><br /><br /> <xref:System.Collections.Immutable.ImmutableQueue%601>|  
|Utiliser des données dernier entré, premier sorti (LIFO)|<xref:System.Collections.Generic.Stack%601>|<xref:System.Collections.Stack>|<xref:System.Collections.Concurrent.ConcurrentStack%601><br /><br /> <xref:System.Collections.Immutable.ImmutableStack%601>|  
|Accéder aux éléments de manière séquentielle|<xref:System.Collections.Generic.LinkedList%601>|Aucune recommandation|Aucune recommandation|  
|Recevoir des notifications quand des éléments sont supprimés ou ajoutés à la collection. (implémente <xref:System.ComponentModel.INotifyPropertyChanged> et <xref:System.Collections.Specialized.INotifyCollectionChanged>)|<xref:System.Collections.ObjectModel.ObservableCollection%601>|Aucune recommandation|Aucune recommandation|  
|Collection triée|<xref:System.Collections.Generic.SortedList%602>|<xref:System.Collections.SortedList>|<xref:System.Collections.Immutable.ImmutableSortedDictionary%602><br /><br /> <xref:System.Collections.Immutable.ImmutableSortedSet%601>|  
|Ensemble de fonctions mathématiques|<xref:System.Collections.Generic.HashSet%601><br /><br /> <xref:System.Collections.Generic.SortedSet%601>|Aucune recommandation|<xref:System.Collections.Immutable.ImmutableHashSet%601><br /><br /> <xref:System.Collections.Immutable.ImmutableSortedSet%601>|  
  
<a name="BKMK_RelatedTopics"></a>   
## <a name="related-topics"></a>Rubriques connexes  
  
|Titre|Description|  
|-----------|-----------------|  
|[Sélection d’une classe de collection](../../../docs/standard/collections/selecting-a-collection-class.md)|Décrit les différentes collections et permet d'en sélectionner une pour votre scénario.|  
|[Types de collections couramment utilisés](../../../docs/standard/collections/commonly-used-collection-types.md)|Décrit les types de collection génériques et non génériques fréquemment utilisés, tels que <xref:System.Array?displayProperty=nameWithType>, <xref:System.Collections.Generic.List%601?displayProperty=nameWithType> et <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWithType>.|  
|[Quand utiliser les collections génériques](../../../docs/standard/collections/when-to-use-generic-collections.md)|Traite de l'utilisation des types de collections génériques.|  
|[Comparaisons et tris dans les collections](../../../docs/standard/collections/comparisons-and-sorts-within-collections.md)|Aborde l'utilisation des comparaisons d'égalité et de tri dans les collections.|  
|[Types de collections triées](../../../docs/standard/collections/sorted-collection-types.md)|Aborde les caractéristiques et les performances des collections triées.|  
|[Types de collections Hashtable et Dictionary](../../../docs/standard/collections/hashtable-and-dictionary-collection-types.md)|Décrit les fonctionnalités des types de dictionnaires basés sur le hachage génériques et non génériques.|  
|[Collections thread-safe](../../../docs/standard/collections/thread-safe/index.md)|Décrit les types de collections tels que <xref:System.Collections.Concurrent.BlockingCollection%601?displayProperty=nameWithType> et <xref:System.Collections.Concurrent.ConcurrentBag%601?displayProperty=nameWithType> qui prennent en charge l'accès simultané sécurisé et efficace de plusieurs threads.|  
|System.Collections.Immutable|Présente les collections immuables et fournit des liens vers les types de collection.|  
  
<a name="BKMK_Reference"></a>   
## <a name="reference"></a>Référence  
 <xref:System.Array?displayProperty=nameWithType>  
 <xref:System.Collections?displayProperty=nameWithType>  
 <xref:System.Collections.Concurrent?displayProperty=nameWithType>  
 <xref:System.Collections.Generic?displayProperty=nameWithType>  
 <xref:System.Collections.Specialized?displayProperty=nameWithType>  
 <xref:System.Linq?displayProperty=nameWithType>  
 <xref:System.Collections.Immutable>
