---
title: -refout (Visual Basic)
ms.date: 03/16/2018
ms.prod: .net
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- /refout
helpviewer_keywords:
- refout compiler option [Visual Basic]
- /refout compiler option [Visual Basic]
- -refout compiler option [Visual Basic]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6075b92efd1eec9797fca248e97a325bd5df4bb
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2018
---
# <a name="-refout-visual-basic"></a><span data-ttu-id="0aeb8-102">-refout (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0aeb8-102">-refout (Visual Basic)</span></span>

<span data-ttu-id="0aeb8-103">L’option **-refout** spécifie un chemin de fichier où l’assembly de référence doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-103">The **-refout** option specifies a file path where the reference assembly should be output.</span></span>

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a><span data-ttu-id="0aeb8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aeb8-104">Syntax</span></span>

```console
-refout:filepath
```

## <a name="arguments"></a><span data-ttu-id="0aeb8-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="0aeb8-105">Arguments</span></span>

 <span data-ttu-id="0aeb8-106">`filepath` Le chemin d’accès et le nom de l’assembly de référence.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-106">`filepath` The path and filename of the reference assembly.</span></span> <span data-ttu-id="0aeb8-107">En règle générale, il doit être dans un sous-dossier de l’assembly principal.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-107">It should generally be in a sub-folder of the primary assembly.</span></span> <span data-ttu-id="0aeb8-108">La convention recommandée (utilisée par MSBuild) consiste à placer l’assembly de référence dans un sous-dossier « ref/ » par rapport à l’assembly principal.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-108">The recommended convention (used by MSBuild) is to place the reference assembly in a "ref/" sub-folder relative to the primary assembly.</span></span> <span data-ttu-id="0aeb8-109">Tous les dossiers dans `filepath` doit exister ; le compilateur ne pas les crée.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-109">All folders in `filepath` must exist; the compiler does not create them.</span></span> 

## <a name="remarks"></a><span data-ttu-id="0aeb8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0aeb8-110">Remarks</span></span>

<span data-ttu-id="0aeb8-111">Visual Basic prend en charge la `-refout` basculer depuis la version 15.3.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-111">Visual Basic supports the `-refout` switch starting with version 15.3.</span></span>

<span data-ttu-id="0aeb8-112">Les assemblys de référence sont uniquement des métadonnées des assemblys qui contiennent des métadonnées, mais aucun code d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-112">Reference assemblies are metadata-only assemblies that contain metadata but no implementation code.</span></span> <span data-ttu-id="0aeb8-113">Elles incluent des informations de type et de membre pour tout sauf les types anonymes.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-113">They include type and member information for everything except anonymous types.</span></span> <span data-ttu-id="0aeb8-114">Leurs corps de méthode sont remplacés par un seul `throw null` instruction.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-114">Their method bodies are replaced with a single `throw null` statement.</span></span> <span data-ttu-id="0aeb8-115">La raison de l’utilisation `throw null` des corps de méthode (par opposition à aucun corps) est afin que PEVerify peut exécuter et transmettre (par conséquent valider la conformité des métadonnées).</span><span class="sxs-lookup"><span data-stu-id="0aeb8-115">The reason for using `throw null` method bodies (as opposed to no bodies) is so that PEVerify can run and pass (thus validating the completeness of the metadata).</span></span>

<span data-ttu-id="0aeb8-116">Incluent des assemblys de référence de niveau assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-116">Reference assemblies include an assembly-level [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribute.</span></span> <span data-ttu-id="0aeb8-117">Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser).</span><span class="sxs-lookup"><span data-stu-id="0aeb8-117">This attribute may be specified in source (then the compiler won't need to synthesize it).</span></span> <span data-ttu-id="0aeb8-118">En raison de cet attribut, runtimes refuser de charger des assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement).</span><span class="sxs-lookup"><span data-stu-id="0aeb8-118">Because of this attribute, runtimes refuse to load reference assemblies for execution (but they can still be loaded in a reflection-only context).</span></span> <span data-ttu-id="0aeb8-119">Outils réfléchir les assemblys doivent s’assurer de que leur chargement des assemblys de référence en tant que de réflexion uniquement ; Sinon, le runtime lève une <xref:System.BadImageFormatException>.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-119">Tools that reflect on assemblies need to ensure they load reference assemblies as reflection-only; otherwise, the runtime throws a <xref:System.BadImageFormatException>.</span></span>

<span data-ttu-id="0aeb8-120">Les options `-refout` et [`-refonly`](refonly-compiler-option.md) s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="0aeb8-120">The `-refout` and [`-refonly`](refonly-compiler-option.md) options are mutually exclusive.</span></span>

## <a name="see-also"></a><span data-ttu-id="0aeb8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aeb8-121">See Also</span></span>
<span data-ttu-id="0aeb8-122">[-refonly](refonly-compiler-option.md) </span><span class="sxs-lookup"><span data-stu-id="0aeb8-122">[-refonly](refonly-compiler-option.md) </span></span>  
[<span data-ttu-id="0aeb8-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0aeb8-123">Visual Basic Command-Line Compiler</span></span>](index.md)  
[<span data-ttu-id="0aeb8-124">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="0aeb8-124">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)  
