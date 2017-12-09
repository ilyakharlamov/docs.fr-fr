---
title: "Valeurs de retour de référence (Visual Basic)"
ms.custom: 
ms.date: 04/28/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- variables [Visual Basic]
- ref return values [Visual Basic]
- ref returns [Visual Basic]
ms.assetid: 5ef0cc69-eb3a-4a67-92a2-78585f223cb5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 560607f7aa304b25314daabeef3952e6bbef7426
ms.sourcegitcommit: 7e99f66ef09d2903e22c789c67ff5a10aa953b2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2017
---
# <a name="support-for-reference-return-values-visual-basic"></a><span data-ttu-id="f17db-102">Prise en charge des valeurs de retour de référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f17db-102">Support for reference return values (Visual Basic)</span></span>

<span data-ttu-id="f17db-103">À partir de C# 7, le langage c# prend en charge les *référencer des valeurs de retour*.</span><span class="sxs-lookup"><span data-stu-id="f17db-103">Starting with C# 7, the C# language supports *reference return values*.</span></span> <span data-ttu-id="f17db-104">Pour comprendre les valeurs de retour de référence est qu’ils sont le contraire des arguments qui sont passés par référence à une méthode.</span><span class="sxs-lookup"><span data-stu-id="f17db-104">One way to understand reference return values is that they are the opposite of arguments that are passed by reference to a method.</span></span> <span data-ttu-id="f17db-105">Lorsqu’un argument passé par référence est modifié, les modifications sont répercutées dans la valeur de la variable sur l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f17db-105">When an argument passed by reference is modified, the changes are reflected in value of the variable on the caller.</span></span> <span data-ttu-id="f17db-106">Lorsqu’une méthode fournit une valeur de retour de référence pour un appelant, les modifications apportées à la valeur de retour de référence par l’appelant sont reflétées dans les données de la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="f17db-106">When an method provides a reference return value to a caller, modifications made to the reference return value by the caller are reflected in the called method's data.</span></span>

<span data-ttu-id="f17db-107">Visual Basic n’autorise pas les valeurs de retour vous permet de créer des méthodes avec référence, mais il vous permet d’utiliser des valeurs de retour de référence.</span><span class="sxs-lookup"><span data-stu-id="f17db-107">Visual Basic does not allow you to author methods with reference return values, but it does allow you to consume reference return values.</span></span> <span data-ttu-id="f17db-108">En d’autres termes, vous pouvez appeler une méthode avec une valeur de retour de référence et modifier cette valeur de retour, et les modifications apportées à la valeur de retour de référence sont reflétées dans les données de la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="f17db-108">In other words, you can call a method with a reference return value and modify that return value, and changes to the reference return value are reflected in the called method's data.</span></span>

## <a name="modifying-the-ref-return-value-directly"></a><span data-ttu-id="f17db-109">Modification directe de la valeur de retour ref</span><span class="sxs-lookup"><span data-stu-id="f17db-109">Modifying the ref return value directly</span></span>

<span data-ttu-id="f17db-110">Pour les méthodes qui réussissent et n’ont pas toujours `ByRef` paramètres, vous pouvez modifier directement la valeur de retour de référence.</span><span class="sxs-lookup"><span data-stu-id="f17db-110">For methods that always succeed and have no `ByRef` parameters, you can modify the reference return value directly.</span></span> <span data-ttu-id="f17db-111">Pour cela, en affectant la nouvelle valeur pour les expressions qui retourne la valeur de retour de référence.</span><span class="sxs-lookup"><span data-stu-id="f17db-111">You do this by assigning the new value to the expressions that returns the reference return value.</span></span> 

<span data-ttu-id="f17db-112">L’exemple c# suivant définit un `NumericValue.IncrementValue` valeur de retour de méthode qui incrémente une valeur interne et le retourne en tant que référence.</span><span class="sxs-lookup"><span data-stu-id="f17db-112">The following C# example defines a `NumericValue.IncrementValue` method that increments an internal value and returns it as a reference return value.</span></span> 

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/ref-returns1.cs)]

<span data-ttu-id="f17db-113">La référence de retourner la valeur est ensuite modifiée par l’appelant dans l’exemple Visual Basic suivant.</span><span class="sxs-lookup"><span data-stu-id="f17db-113">The reference return value is then modified by the caller in the following Visual Basic example.</span></span> <span data-ttu-id="f17db-114">Notez que la ligne avec la `NumericValue.IncrementValue` appel de méthode n’attribue pas une valeur à la méthode.</span><span class="sxs-lookup"><span data-stu-id="f17db-114">Note that the line with the `NumericValue.IncrementValue` method call does not assign a value to the method.</span></span> <span data-ttu-id="f17db-115">Au lieu de cela, il assigne une valeur à la valeur de retour de référence retournée par la méthode.</span><span class="sxs-lookup"><span data-stu-id="f17db-115">Instead, it assigns a value to the reference return value returned by the method.</span></span>

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/use-ref-returns1.vb)]

## <a name="using-a-helper-method"></a><span data-ttu-id="f17db-116">À l’aide d’une méthode d’assistance</span><span class="sxs-lookup"><span data-stu-id="f17db-116">Using a helper method</span></span>

<span data-ttu-id="f17db-117">Dans d’autres cas, modifier la valeur de retour de référence d’un appel de méthode directement toujours peut-être pas souhaitable.</span><span class="sxs-lookup"><span data-stu-id="f17db-117">In other cases, modifying the reference return value of a method call directly may not always be desirable.</span></span> <span data-ttu-id="f17db-118">Par exemple, une méthode de recherche qui retourne une chaîne peut trouver pas toujours de correspondance.</span><span class="sxs-lookup"><span data-stu-id="f17db-118">For example, a search method that returns a string may not always find a match.</span></span> <span data-ttu-id="f17db-119">Dans ce cas, vous souhaitez modifier la valeur de retour de référence uniquement si la recherche aboutit.</span><span class="sxs-lookup"><span data-stu-id="f17db-119">In that case, you want to modify the reference return value only if the search is successful.</span></span>

<span data-ttu-id="f17db-120">L’exemple c# suivant illustre ce scénario.</span><span class="sxs-lookup"><span data-stu-id="f17db-120">The following C# example illustrates this scenario.</span></span> <span data-ttu-id="f17db-121">Il définit un `Sentence` classe écrite en c# inclut un `FindNext` méthode qui recherche le mot suivant dans une phrase qui commence par une sous-chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f17db-121">It defines a `Sentence` class written in C# includes a `FindNext` method that finds the next word in a sentence that begins with a specified substring.</span></span> <span data-ttu-id="f17db-122">La chaîne est retournée comme valeur de retour de référence et une variable `Boolean` passée par référence à la méthode indique si la recherche a réussi.</span><span class="sxs-lookup"><span data-stu-id="f17db-122">The string is returned as a reference return value, and a `Boolean` variable passed by reference to the method indicates whether the search was successful.</span></span> <span data-ttu-id="f17db-123">La valeur de retour de référence indique que l’appelant peut uniquement pas de lire la valeur retournée ; Il peut le modifier également, et cette modification est répercutée dans les données contenues en interne dans le `Sentence` classe.</span><span class="sxs-lookup"><span data-stu-id="f17db-123">The reference return value indicates that the caller can not only read the returned value; he or she can also modify it, and that modification is reflected in the data contained internally in the `Sentence` class.</span></span>

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-returns.cs)]

<span data-ttu-id="f17db-124">Modifier directement la référence de retourner la valeur dans ce cas n’est pas fiable, étant donné que l’appel de méthode peut ne pas trouver de correspondance et de retourner le premier mot dans la phrase.</span><span class="sxs-lookup"><span data-stu-id="f17db-124">Directly modifying the reference return value in this case is not reliable, since the method call may fail to find a match and return the first word in the sentence.</span></span> <span data-ttu-id="f17db-125">Dans ce cas, l’appelant allez modifier par inadvertance le premier mot de la phrase.</span><span class="sxs-lookup"><span data-stu-id="f17db-125">In that case, the caller will inadvertently modify the first word of the sentence.</span></span> <span data-ttu-id="f17db-126">Cela ne soient pas par l’appelant de retourner un `null` (ou `Nothing` en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="f17db-126">This could be prevented by the caller returning a `null` (or `Nothing` in Visual Basic).</span></span> <span data-ttu-id="f17db-127">Toutefois, dans ce cas modifier une chaîne dont la valeur est `Nothing` lève une <xref:System.NullReferenceException>.</span><span class="sxs-lookup"><span data-stu-id="f17db-127">But in that case, attempting to modify a string whose value is `Nothing` throws a <xref:System.NullReferenceException>.</span></span> <span data-ttu-id="f17db-128">Si peut également être empêchée par l’appelant de retourner <xref:System.String.Empty?displayProperty=nameWithType>, mais cela nécessite que l’appelant définir une variable de chaîne dont la valeur est <xref:System.String.Empty?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f17db-128">If could also be prevented by the caller returning <xref:System.String.Empty?displayProperty=nameWithType>, but this requires that the caller define a string variable whose value is <xref:System.String.Empty?displayProperty=nameWithType>.</span></span> <span data-ttu-id="f17db-129">Alors que l’appelant peut modifier cette chaîne, la modification elle-même n’a aucune utilité, étant donné que la chaîne modifiée n’a aucune relation avec les mots de la phrase stockée par la `Sentence` classe.</span><span class="sxs-lookup"><span data-stu-id="f17db-129">While the caller can modify that string, the modification itself serves no purpose, since the modified string has no relationship to the words in the sentence stored by the `Sentence` class.</span></span>

<span data-ttu-id="f17db-130">La meilleure façon de gérer ce scénario est pour passer la valeur de retour de référence par référence à une méthode d’assistance.</span><span class="sxs-lookup"><span data-stu-id="f17db-130">The best way to handle this scenario is to pass the reference return value by reference to a helper method.</span></span> <span data-ttu-id="f17db-131">La méthode d’assistance puis contient la logique permettant de déterminer si l’appel de méthode a réussi et, si c’était le cas, pour modifier la référence de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f17db-131">The helper method then contains the logic to determine whether the method call succeeded and, if it did, to modify the reference return value.</span></span> <span data-ttu-id="f17db-132">L’exemple suivant fournit une implémentation possible.</span><span class="sxs-lookup"><span data-stu-id="f17db-132">The following example provides a possible implementation.</span></span>

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-return-helper.vb#1)]

## <a name="see-also"></a><span data-ttu-id="f17db-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f17db-133">See also</span></span>

<span data-ttu-id="f17db-134">[Passage des arguments par valeur et par référence](passing-arguments-by-value-and-by-reference.md) </span><span class="sxs-lookup"><span data-stu-id="f17db-134">[Passing arguments by value and by reference](passing-arguments-by-value-and-by-reference.md) </span></span>  
[<span data-ttu-id="f17db-135">Procédures dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f17db-135">Procedures in Visual Basic</span></span>](index.md)   

