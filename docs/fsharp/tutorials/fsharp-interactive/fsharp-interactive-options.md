---
title: "Options F# Interactive"
description: 'En savoir plus sur les options de ligne de commande pris en charge par F # Interactive, fsi.exe.'
keywords: visual f#, f#, programmation fonctionnelle
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: f9f3e39b-ce6c-41ff-991f-0625f46441ae
ms.openlocfilehash: a9b36a12aa9ffcfa26ea50d72d018a25f5f65243
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2017
---
# <a name="f-interactive-options"></a><span data-ttu-id="5ba8b-104">Options F# Interactive</span><span class="sxs-lookup"><span data-stu-id="5ba8b-104">F# Interactive Options</span></span>

> [!NOTE]
<span data-ttu-id="5ba8b-105">Cet article ne traite pour le moment que de l’expérience Windows.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-105">This article currently describes the experience for Windows only.</span></span>  <span data-ttu-id="5ba8b-106">Il va être réécrit.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-106">It will be rewritten.</span></span>

<span data-ttu-id="5ba8b-107">Cette rubrique décrit les options de ligne de commande pris en charge par F # Interactive, `fsi.exe`.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-107">This topic describes the command-line options supported by F# Interactive, `fsi.exe`.</span></span> <span data-ttu-id="5ba8b-108">F # Interactive accepte la plupart des options de ligne de commande de même que le compilateur F #, mais accepte également des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-108">F# Interactive accepts many of the same command line options as the F# compiler, but also accepts some additional options.</span></span>

## <a name="using-f-interactive-for-scripting"></a><span data-ttu-id="5ba8b-109">À l’aide de F # Interactive pour l’écriture de scripts</span><span class="sxs-lookup"><span data-stu-id="5ba8b-109">Using F# Interactive for Scripting</span></span>
<span data-ttu-id="5ba8b-110">F # Interactive, `fsi.exe`, peut être lancé interactivement, ou il peut être lancé depuis la ligne de commande pour exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-110">F# Interactive, `fsi.exe`, can be launched interactively, or it can be launched from the command line to run a script.</span></span> <span data-ttu-id="5ba8b-111">La syntaxe de ligne de commande est</span><span class="sxs-lookup"><span data-stu-id="5ba8b-111">The command line syntax is</span></span>

```
> fsi.exe [options] [ script-file [arguments] ]
```

<span data-ttu-id="5ba8b-112">L’extension de fichier pour les fichiers de script F # est `.fsx`.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-112">The file extension for F# script files is `.fsx`.</span></span>

## <a name="table-of-f-interactive-options"></a><span data-ttu-id="5ba8b-113">Tableau des Options F # Interactive</span><span class="sxs-lookup"><span data-stu-id="5ba8b-113">Table of F# Interactive Options</span></span>
<span data-ttu-id="5ba8b-114">Le tableau suivant résume les options prises en charge par F # Interactive.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-114">The following table summarizes the options supported by F# Interactive.</span></span> <span data-ttu-id="5ba8b-115">Vous pouvez définir ces options sur la ligne de commande ou via l’IDE de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-115">You can set these options on the command-line or through the Visual Studio IDE.</span></span> <span data-ttu-id="5ba8b-116">Pour définir ces options dans l’IDE de Visual Studio, ouvrez le **outils** menu, sélectionnez **Options...** , puis développez le **outils F #** nœud et sélectionnez **F # Interactive**.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-116">To set these options in the Visual Studio IDE, open the **Tools** menu, select **Options...**, then expand the **F# Tools** node and select **F# Interactive**.</span></span>

<span data-ttu-id="5ba8b-117">Lorsque des listes figurent dans les arguments de l’option F # Interactive, les éléments de liste sont séparés par des points-virgules (`;`).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-117">Where lists appear in F# Interactive option arguments, list elements are separated by semicolons (`;`).</span></span>

|<span data-ttu-id="5ba8b-118">Option</span><span class="sxs-lookup"><span data-stu-id="5ba8b-118">Option</span></span>|<span data-ttu-id="5ba8b-119">Description</span><span class="sxs-lookup"><span data-stu-id="5ba8b-119">Description</span></span>|
|------|-----------|
|**--**|<span data-ttu-id="5ba8b-120">Utilisé pour indiquer à F # Interactive de traiter les arguments restants en tant qu’arguments de ligne de commande au programme F # ou script, auquel vous pouvez accéder dans le code à l’aide de la liste **fsi.CommandLineArgs**.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-120">Used to instruct F# Interactive to treat remaining arguments as command line arguments to the F# program or script, which you can access in code by using the list **fsi.CommandLineArgs**.</span></span>|
|<span data-ttu-id="5ba8b-121">**--vérifiée**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-121">**--checked**[**+**&#124;**-**]</span></span>|<span data-ttu-id="5ba8b-122">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-122">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-123">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-123">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-124">**page de codes-- :&lt;int&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-124">**--codepage:&lt;int&gt;**</span></span>|<span data-ttu-id="5ba8b-125">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-125">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-126">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-126">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-127">**--crossoptimize**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-127">**--crossoptimize**[**+**&#124;**-**]</span></span>|<span data-ttu-id="5ba8b-128">Activer ou désactiver les optimisations intermodules.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-128">Enable or disable cross-module optimizations.</span></span>|
|<span data-ttu-id="5ba8b-129">**--debug**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-129">**--debug**[**+**&#124;**-**]</span></span><br /><br /><span data-ttu-id="5ba8b-130">**--debug :**[**complète**&#124; **pdbonly**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-130">**--debug:**[**full**&#124;**pdbonly**]</span></span><br /><br /><span data-ttu-id="5ba8b-131">**-g**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-131">**-g**[**+**&#124;**-**]</span></span><br /><br /><span data-ttu-id="5ba8b-132">**-g:**[**complète**&#124; **pdbonly**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-132">**-g:**[**full**&#124;**pdbonly**]</span></span>|<span data-ttu-id="5ba8b-133">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-133">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-134">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-134">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-135">**--définir :&lt;chaîne&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-135">**--define:&lt;string&gt;**</span></span>|<span data-ttu-id="5ba8b-136">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-136">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-137">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-137">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-138">**--exec**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-138">**--exec**</span></span>|<span data-ttu-id="5ba8b-139">Fait en sorte que F # interactive quitte après le chargement des fichiers ou le fichier de script sur la ligne de commande en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-139">Instructs F# interactive to exit after loading the files or running the script file given on the command line.</span></span>|
|<span data-ttu-id="5ba8b-140">**/fullpaths--**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-140">**--fullpaths**</span></span>|<span data-ttu-id="5ba8b-141">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-141">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-142">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-142">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-143">**--l’interface graphique utilisateur**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-143">**--gui**[**+**&#124;**-**]</span></span>|<span data-ttu-id="5ba8b-144">Active ou désactive la boucle d’événements Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-144">Enables or disables the Windows Forms event loop.</span></span> <span data-ttu-id="5ba8b-145">Les styles sont activés par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-145">The default is enabled.</span></span>|
|<span data-ttu-id="5ba8b-146">**--aide**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-146">**--help**</span></span><br /><br /><span data-ttu-id="5ba8b-147">**-?**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-147">**-?**</span></span>|<span data-ttu-id="5ba8b-148">Utilisé pour afficher la syntaxe de ligne de commande et une brève description de chaque option.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-148">Used to display the command line syntax and a brief description of each option.</span></span>|
|<span data-ttu-id="5ba8b-149">**--lib :&lt;-liste des dossiers&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-149">**--lib:&lt;folder-list&gt;**</span></span><br /><br /><span data-ttu-id="5ba8b-150">**-I&lt;-liste des dossiers&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-150">**-I:&lt;folder-list&gt;**</span></span>|<span data-ttu-id="5ba8b-151">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-151">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-152">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-152">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-153">**--charger :&lt;nom de fichier&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-153">**--load:&lt;filename&gt;**</span></span>|<span data-ttu-id="5ba8b-154">Compile le code source donné au démarrage et charge les constructions F # compilées dans la session.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-154">Compiles the given source code at startup and loads the compiled F# constructs into the session.</span></span> <span data-ttu-id="5ba8b-155">Si la source de la cible contient des directives de script telles que **#use** ou **#load**, vous devez utiliser **--utilisez** ou **#use** au lieu de **--charger** ou **#load**.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-155">If the target source contains scripting directives such as **#use** or **#load**, then you must use **--use** or **#use** instead of **--load** or **#load**.</span></span>|
|<span data-ttu-id="5ba8b-156">**--mlcompatibility**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-156">**--mlcompatibility**</span></span>|<span data-ttu-id="5ba8b-157">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-157">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-158">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-158">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-159">**--noframework**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-159">**--noframework**</span></span>|<span data-ttu-id="5ba8b-160">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-160">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-161">Pour plus d’informations, consultez [Options du compilateur](../../language-reference/compiler-options.md)</span><span class="sxs-lookup"><span data-stu-id="5ba8b-161">For more information, see [Compiler Options](../../language-reference/compiler-options.md)</span></span>|
|<span data-ttu-id="5ba8b-162">**/nologo--**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-162">**--nologo**</span></span>|<span data-ttu-id="5ba8b-163">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-163">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-164">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-164">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-165">**--nowarn :&lt;-liste d’avertissements&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-165">**--nowarn:&lt;warning-list&gt;**</span></span>|<span data-ttu-id="5ba8b-166">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-166">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-167">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-167">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-168">**--optimiser**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-168">**--optimize**[**+**&#124;**-**]</span></span>|<span data-ttu-id="5ba8b-169">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-169">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-170">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-170">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-171">**--silencieux**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-171">**--quiet**</span></span>|<span data-ttu-id="5ba8b-172">Supprimer la sortie de F # Interactive pour le **stdout** flux.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-172">Suppress F# Interactive's output to the **stdout** stream.</span></span>|
|<span data-ttu-id="5ba8b-173">**--les quotations de débogage**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-173">**--quotations-debug**</span></span>|<span data-ttu-id="5ba8b-174">Spécifie que les informations de débogage supplémentaires doivent être émises pour les expressions qui sont dérivées de littéraux de guillemets F # et répercutées définitions.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-174">Specifies that extra debugging information should be emitted for expressions that are derived from F# quotation literals and reflected definitions.</span></span> <span data-ttu-id="5ba8b-175">Les informations de débogage sont ajoutées pour les attributs personnalisés d’un nœud d’arborescence de l’expression F #.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-175">The debug information is added to the custom attributes of an F# expression tree node.</span></span> <span data-ttu-id="5ba8b-176">Consultez [Quotations de Code](../../language-reference/code-quotations.md) et [Expr.CustomAttributes](https://msdn.microsoft.com/library/eb89943f-5f5b-474e-b125-030ca412edb3).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-176">See [Code Quotations](../../language-reference/code-quotations.md) and [Expr.CustomAttributes](https://msdn.microsoft.com/library/eb89943f-5f5b-474e-b125-030ca412edb3).</span></span>|
|<span data-ttu-id="5ba8b-177">**--readline**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-177">**--readline**[**+**&#124;**-**]</span></span>|<span data-ttu-id="5ba8b-178">Activer ou désactiver la saisie semi-automatique par tabulation en mode interactif.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-178">Enable or disable tab completion in interactive mode.</span></span>|
|<span data-ttu-id="5ba8b-179">**--référence :&lt;nom de fichier&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-179">**--reference:&lt;filename&gt;**</span></span><br /><br /><span data-ttu-id="5ba8b-180">**-r:&lt;nom de fichier&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-180">**-r:&lt;filename&gt;**</span></span>|<span data-ttu-id="5ba8b-181">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-181">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-182">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-182">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-183">**--tailcalls**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-183">**--tailcalls**[**+**&#124;**-**]</span></span>|<span data-ttu-id="5ba8b-184">Activer ou désactiver l’utilisation de l’instruction de langage intermédiaire de fin, ce qui entraîne le frame de pile être réutilisées pour les fonctions récursives tail.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-184">Enable or disable the use of the tail IL instruction, which causes the stack frame to be reused for tail recursive functions.</span></span> <span data-ttu-id="5ba8b-185">Cette option est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-185">This option is enabled by default.</span></span>|
|<span data-ttu-id="5ba8b-186">**--utiliser :&lt;nom de fichier&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-186">**--use:&lt;filename&gt;**</span></span>|<span data-ttu-id="5ba8b-187">Indique à l’interpréteur à utiliser le fichier spécifié au démarrage en tant qu’entrée initiale.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-187">Tells the interpreter to use the given file on startup as initial input.</span></span>|
|<span data-ttu-id="5ba8b-188">**--utf8output**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-188">**--utf8output**</span></span>|<span data-ttu-id="5ba8b-189">Identique à l’option de compilateur fsc.exe.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-189">Same as the fsc.exe compiler option.</span></span> <span data-ttu-id="5ba8b-190">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-190">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-191">**--avertir :&lt;niveau d’avertissement&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-191">**--warn:&lt;warning-level&gt;**</span></span>|<span data-ttu-id="5ba8b-192">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-192">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-193">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-193">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-194">**--/warnaserror**[**+**&#124; **-**]</span><span class="sxs-lookup"><span data-stu-id="5ba8b-194">**--warnaserror**[**+**&#124;**-**]</span></span>|<span data-ttu-id="5ba8b-195">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-195">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-196">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-196">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|
|<span data-ttu-id="5ba8b-197">**--/warnaserror**[**+**&#124; **-** ] :**&lt;int-liste&gt;**</span><span class="sxs-lookup"><span data-stu-id="5ba8b-197">**--warnaserror**[**+**&#124;**-**]:**&lt;int-list&gt;**</span></span>|<span data-ttu-id="5ba8b-198">Identique à la **fsc.exe** option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-198">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="5ba8b-199">Pour plus d’informations, consultez l’article [Options du compilateur](../../language-reference/compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8b-199">For more information, see [Compiler Options](../../language-reference/compiler-options.md).</span></span>|

## <a name="related-topics"></a><span data-ttu-id="5ba8b-200">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ba8b-200">Related Topics</span></span>

|<span data-ttu-id="5ba8b-201">Titre</span><span class="sxs-lookup"><span data-stu-id="5ba8b-201">Title</span></span>|<span data-ttu-id="5ba8b-202">Description</span><span class="sxs-lookup"><span data-stu-id="5ba8b-202">Description</span></span>|
|-----|-----------|
|[<span data-ttu-id="5ba8b-203">Options du compilateur</span><span class="sxs-lookup"><span data-stu-id="5ba8b-203">Compiler Options</span></span>](../../language-reference/compiler-options.md)|<span data-ttu-id="5ba8b-204">Décrit les options de ligne de commande disponibles pour le compilateur F #, **fsc.exe**.</span><span class="sxs-lookup"><span data-stu-id="5ba8b-204">Describes command line options available for the F# compiler, **fsc.exe**.</span></span>|