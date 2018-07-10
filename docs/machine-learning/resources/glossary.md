---
title: Glossaire de l’apprentissage automatique
description: Glossaire des termes de l’apprentissage automatique.
author: jralexander
ms.author: johalex
ms.date: 05/31/2018
ms.topic: conceptual
ms.prod: dotnet-ml
ms.devlang: dotnet
manager: wpickett
ms.openlocfilehash: 332d9e14bea165992f9f00b048286e185269ea79
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2018
ms.locfileid: "34860659"
---
# <a name="machine-learning-glossary"></a><span data-ttu-id="96330-103">Glossaire de l’apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="96330-103">Machine learning glossary</span></span>

<span data-ttu-id="96330-104">La liste suivante est une compilation des principaux termes de l’apprentissage automatique, utiles lorsque vous générez vos modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="96330-104">The following list is a compilation of important machine learning terms that are useful as you build your custom models.</span></span>

## <a name="accuracy"></a><span data-ttu-id="96330-105">Précision</span><span class="sxs-lookup"><span data-stu-id="96330-105">Accuracy</span></span>

<span data-ttu-id="96330-106">Dans la [classification](#classification), la précision correspond au nombre d’éléments correctement classifiés, divisé par le nombre total d’éléments dans le jeu de test.</span><span class="sxs-lookup"><span data-stu-id="96330-106">In [classification](#classification), accuracy is the number of correctly classified items divided by the total number of items in the test set.</span></span> <span data-ttu-id="96330-107">Cette valeur est comprise entre 0 (la moins précise) et 1 (la plus précise).</span><span class="sxs-lookup"><span data-stu-id="96330-107">Ranges from 0 (least accurate) to 1 (most accurate).</span></span> <span data-ttu-id="96330-108">La précision est une des métriques d’évaluation des performances de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="96330-108">Accuracy is one of evaluation metrics of the performance of your model.</span></span> <span data-ttu-id="96330-109">Utilisez-la conjointement avec les options [précision](#precision), [rappel](#recall) et [F-score](#f-score).</span><span class="sxs-lookup"><span data-stu-id="96330-109">Consider it in conjunction with [precision](#precision), [recall](#recall), and [F-score](#f-score).</span></span>

<span data-ttu-id="96330-110">API ML.NET connexe : <xref:Microsoft.ML.Models.BinaryClassificationMetrics.Accuracy?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-110">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.Accuracy?displayProperty=nameWithType>.</span></span>

## <a name="area-under-the-curve-auc"></a><span data-ttu-id="96330-111">Zone sous la courbe (AUC)</span><span class="sxs-lookup"><span data-stu-id="96330-111">Area under the curve (AUC)</span></span>

<span data-ttu-id="96330-112">Dans la [classification binaire](#binary-classification), une métrique d’évaluation qui correspond à la valeur de la zone sous la courbe qui trace le taux de vrais positifs (sur l’axe des y) par rapport au taux de faux positifs (sur l’axe des x).</span><span class="sxs-lookup"><span data-stu-id="96330-112">In [binary classification](#binary-classification), an evaluation metric that is the value of the area under the curve that plots the true positives rate (on the y-axis) against the false positives rate (on the x-axis).</span></span> <span data-ttu-id="96330-113">Cette valeur est comprise entre 0,5 (pire) et 1 (meilleur).</span><span class="sxs-lookup"><span data-stu-id="96330-113">Ranges from 0.5 (worst) to 1 (best).</span></span> <span data-ttu-id="96330-114">Également appelée zone sous la courbe ROC (Receiver Operating Characteristic).</span><span class="sxs-lookup"><span data-stu-id="96330-114">Also known as the area under the ROC curve, i.e., receiver operating characteristic curve.</span></span> <span data-ttu-id="96330-115">Pour plus d’informations, consultez l’article Wikipédia [Courbe ROC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic).</span><span class="sxs-lookup"><span data-stu-id="96330-115">For more information, see the [Receiver operating characteristic](https://en.wikipedia.org/wiki/Receiver_operating_characteristic) article on Wikipedia.</span></span>

<span data-ttu-id="96330-116">API ML.NET connexe : <xref:Microsoft.ML.Models.BinaryClassificationMetrics.Auc?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-116">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.Auc?displayProperty=nameWithType>.</span></span>

## <a name="binary-classification"></a><span data-ttu-id="96330-117">Classification binaire</span><span class="sxs-lookup"><span data-stu-id="96330-117">Binary classification</span></span>

<span data-ttu-id="96330-118">Cas de [classification](#classification) où l’[étiquette](#label) provient uniquement d’une de deux classes.</span><span class="sxs-lookup"><span data-stu-id="96330-118">A [classification](#classification) case where the [label](#label) is only one out of two classes.</span></span> <span data-ttu-id="96330-119">Pour plus d’informations, consultez l’article Wikipédia [Classification binaire](https://en.wikipedia.org/wiki/Binary_classification).</span><span class="sxs-lookup"><span data-stu-id="96330-119">For more information, see the [Binary classification](https://en.wikipedia.org/wiki/Binary_classification) article on Wikipedia.</span></span>

## <a name="classification"></a><span data-ttu-id="96330-120">Classification</span><span class="sxs-lookup"><span data-stu-id="96330-120">Classification</span></span>

<span data-ttu-id="96330-121">Lorsque les données sont utilisées pour prédire une catégorie, la tâche [Apprentissage automatique supervisé](#supervised-machine-learning) est appelée classification.</span><span class="sxs-lookup"><span data-stu-id="96330-121">When the data is used to predict a category, [supervised machine learning](#supervised-machine-learning) task is called classification.</span></span> <span data-ttu-id="96330-122">[Classification binaire](#binary-classification) fait référence à la prédiction de deux catégories uniquement (par exemple, la classification d’une image en tant qu’image de « chat » ou de « chien »).</span><span class="sxs-lookup"><span data-stu-id="96330-122">[Binary classification](#binary-classification) refers to predicting only two categories (for example, classifying an image as a picture of either a 'cat' or a 'dog').</span></span> <span data-ttu-id="96330-123">[Classification multiclasse](#multiclass-classification) fait référence à la prédiction de plusieurs catégories (par exemple, lors de la classification d’une image en tant qu’image d’une race spécifique de chien).</span><span class="sxs-lookup"><span data-stu-id="96330-123">[Multiclass classification](#multiclass-classification) refers to predicting multiple categories (for example, when classifying an image as a picture of a specific breed of dog).</span></span>

## <a name="coefficient-of-determination"></a><span data-ttu-id="96330-124">Coefficient de détermination</span><span class="sxs-lookup"><span data-stu-id="96330-124">Coefficient of determination</span></span>

<span data-ttu-id="96330-125">Dans une [régression](#regression), une métrique d’évaluation qui indique la manière dont les données s’intègrent à un modèle.</span><span class="sxs-lookup"><span data-stu-id="96330-125">In [regression](#regression), an evaluation metric that indicates how well data fits a model.</span></span> <span data-ttu-id="96330-126">Cette valeur est comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="96330-126">Ranges from 0 to 1.</span></span> <span data-ttu-id="96330-127">Une valeur de 0 signifie que les données sont aléatoires ou ne s’intègrent pas au modèle.</span><span class="sxs-lookup"><span data-stu-id="96330-127">A value of 0 means that the data is random or otherwise cannot be fit to the model.</span></span> <span data-ttu-id="96330-128">Une valeur de 1 signifie que le modèle correspond exactement aux données.</span><span class="sxs-lookup"><span data-stu-id="96330-128">A value of 1 means that the model exactly matches the data.</span></span> <span data-ttu-id="96330-129">Cette valeur est souvent désignée sous le terme r<sup>2</sup>, R<sup>2</sup> ou R carré.</span><span class="sxs-lookup"><span data-stu-id="96330-129">This is often referred to as r<sup>2</sup>, R<sup>2</sup>, or r-squared.</span></span>

<span data-ttu-id="96330-130">API ML.NET connexe : <xref:Microsoft.ML.Models.RegressionMetrics.RSquared?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-130">Related ML.NET API: <xref:Microsoft.ML.Models.RegressionMetrics.RSquared?displayProperty=nameWithType>.</span></span>

## <a name="feature"></a><span data-ttu-id="96330-131">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="96330-131">Feature</span></span>

<span data-ttu-id="96330-132">Propriété mesurable du phénomène mesuré, en général, une valeur (double) numérique.</span><span class="sxs-lookup"><span data-stu-id="96330-132">A measurable property of the phenomenon being measured, typically a numeric (double) value.</span></span> <span data-ttu-id="96330-133">Plusieurs fonctionnalités sont appelées **vecteur de fonctionnalité** et sont généralement stockées en tant que `double[]`.</span><span class="sxs-lookup"><span data-stu-id="96330-133">Multiple features are referred to as a **Feature vector** and typically stored as `double[]`.</span></span> <span data-ttu-id="96330-134">Les fonctionnalités définissent les principales caractéristiques du phénomène mesuré.</span><span class="sxs-lookup"><span data-stu-id="96330-134">Features define the important characteristics of the phenomenon being measured.</span></span> <span data-ttu-id="96330-135">Pour plus d’informations, consultez l’article Wikipédia [Fonctionnalité](https://en.wikipedia.org/wiki/Feature_(machine_learning)).</span><span class="sxs-lookup"><span data-stu-id="96330-135">For more information, see the [Feature](https://en.wikipedia.org/wiki/Feature_(machine_learning)) article on Wikipedia.</span></span>

## <a name="feature-engineering"></a><span data-ttu-id="96330-136">Ingénierie de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="96330-136">Feature engineering</span></span>

<span data-ttu-id="96330-137">L’ingénierie de fonctionnalité est le processus qui consiste à définir un ensemble de [fonctionnalités](#feature) et à développer des logiciels qui produisent des vecteurs de fonctionnalité à partir des données de phénomène disponibles, par exemple, l’extraction d’une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="96330-137">Feature engineering is the process that involves defining a set of [features](#feature) and developing software that produces feature vectors from available phenomenon data, i.e., feature extraction.</span></span> <span data-ttu-id="96330-138">Pour plus d’informations, consultez l’article Wikipédia [Feature engineering](https://en.wikipedia.org/wiki/Feature_engineering).</span><span class="sxs-lookup"><span data-stu-id="96330-138">For more information, see the [Feature engineering](https://en.wikipedia.org/wiki/Feature_engineering) article on Wikipedia.</span></span>

## <a name="f-score"></a><span data-ttu-id="96330-139">F-score</span><span class="sxs-lookup"><span data-stu-id="96330-139">F-score</span></span>

<span data-ttu-id="96330-140">Dans une [classification](#classification), une métrique d’évaluation qui équilibre [précision](#precision) et [rappel](#recall).</span><span class="sxs-lookup"><span data-stu-id="96330-140">In [classification](#classification), an evaluation metric that balances [precision](#precision) and [recall](#recall).</span></span>

<span data-ttu-id="96330-141">API ML.NET connexe : <xref:Microsoft.ML.Models.BinaryClassificationMetrics.F1Score?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-141">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.F1Score?displayProperty=nameWithType>.</span></span>

## <a name="hyperparameter"></a><span data-ttu-id="96330-142">Hyperparamètre</span><span class="sxs-lookup"><span data-stu-id="96330-142">Hyperparameter</span></span>

<span data-ttu-id="96330-143">Un paramètre d’un algorithme d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="96330-143">A parameter of a machine learning algorithm.</span></span> <span data-ttu-id="96330-144">Par exemple, le nombre d’arbres à assimiler dans une forêt décisionnelle ou la taille d’étape dans un algorithme de jambage descendant dégradé.</span><span class="sxs-lookup"><span data-stu-id="96330-144">Examples include the number of trees to learn in a decision forest or the step size in a gradient descent algorithm.</span></span> <span data-ttu-id="96330-145">Les valeurs des *hyperparamètres* sont définies avant l’apprentissage du modèle et régissent le processus de recherche des paramètres de la fonction de prédiction, par exemple, les points de comparaison dans un arbre de décision ou les pondérations dans un modèle de régression linéaire.</span><span class="sxs-lookup"><span data-stu-id="96330-145">Values of *Hyperparameters* are set before training the model and govern the process of finding the parameters of the prediction function, for example, the comparison points in a decision tree or the weights in a linear regression model.</span></span> <span data-ttu-id="96330-146">Pour plus d’informations, consultez l’article Wikipédia [Hyperparamètre](https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning)).</span><span class="sxs-lookup"><span data-stu-id="96330-146">For more information, see the [Hyperparameter](https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning)) article on Wikipedia.</span></span>

## <a name="label"></a><span data-ttu-id="96330-147">Ajouter des contrôles</span><span class="sxs-lookup"><span data-stu-id="96330-147">Label</span></span>

<span data-ttu-id="96330-148">L’élément à prédire avec le modèle d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="96330-148">The element to be predicted with the machine learning model.</span></span> <span data-ttu-id="96330-149">Par exemple, la race d’un chien ou le futur cours d’une action.</span><span class="sxs-lookup"><span data-stu-id="96330-149">For example, the breed of dog or a future stock price.</span></span>

## <a name="log-loss"></a><span data-ttu-id="96330-150">Perte du journal</span><span class="sxs-lookup"><span data-stu-id="96330-150">Log loss</span></span>

<span data-ttu-id="96330-151">Dans une [classification](#classification), une métrique d’évaluation qui caractérise la précision d’un classifieur.</span><span class="sxs-lookup"><span data-stu-id="96330-151">In [classification](#classification), an evaluation metric that characterizes the accuracy of a classifier.</span></span> <span data-ttu-id="96330-152">Plus la perte du journal est faible, plus un classifieur est précis.</span><span class="sxs-lookup"><span data-stu-id="96330-152">The smaller log loss is, the more accurate a classifier is.</span></span>

<span data-ttu-id="96330-153">API ML.NET connexe : <xref:Microsoft.ML.Models.BinaryClassificationMetrics.LogLoss?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-153">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.LogLoss?displayProperty=nameWithType>.</span></span>

## <a name="mean-absolute-error-mae"></a><span data-ttu-id="96330-154">Erreur d'absolue moyenne</span><span class="sxs-lookup"><span data-stu-id="96330-154">Mean absolute error (MAE)</span></span>

<span data-ttu-id="96330-155">Dans une [régression](#regression), une métrique d’évaluation qui représente la moyenne de toutes les erreurs du modèle, où l’erreur de modèle est la distance entre la valeur d’[étiquette](#label) prédite et la valeur d’étiquette correcte.</span><span class="sxs-lookup"><span data-stu-id="96330-155">In [regression](#regression), an evaluation metric that is the average of all the model errors, where model error is the distance between the predicted [label](#label) value and the correct label value.</span></span>

<span data-ttu-id="96330-156">API ML.NET connexe : <xref:Microsoft.ML.Models.RegressionMetrics.L1?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-156">Related ML.NET API: <xref:Microsoft.ML.Models.RegressionMetrics.L1?displayProperty=nameWithType>.</span></span>

## <a name="model"></a><span data-ttu-id="96330-157">Modèle</span><span class="sxs-lookup"><span data-stu-id="96330-157">Model</span></span>

<span data-ttu-id="96330-158">En règle générale, les paramètres de la fonction de prédiction.</span><span class="sxs-lookup"><span data-stu-id="96330-158">Traditionally, the parameters for the prediction function.</span></span> <span data-ttu-id="96330-159">Par exemple, les pondérations dans un modèle de régression linéaire ou les points de fractionnement dans un arbre de décision.</span><span class="sxs-lookup"><span data-stu-id="96330-159">For example, the weights in a linear regression model or the split points in a decision tree.</span></span> <span data-ttu-id="96330-160">Dans ML.NET, un modèle contient toutes les informations nécessaires pour prédire l’[étiquette](#label) d’un objet de domaine (par exemple, une image ou un texte).</span><span class="sxs-lookup"><span data-stu-id="96330-160">In ML.NET, a model contains all the information necessary to predict the [label](#label) of a domain object (for example, image or text).</span></span> <span data-ttu-id="96330-161">Cela signifie que les modèles ML.NET incluent les étapes de fonctionnalisation nécessaires ainsi que les paramètres de la fonction de prédiction.</span><span class="sxs-lookup"><span data-stu-id="96330-161">This means that ML.NET models include the featurization steps necessary as well as the parameters for the prediction function.</span></span>

## <a name="multiclass-classification"></a><span data-ttu-id="96330-162">Classification multiclasse</span><span class="sxs-lookup"><span data-stu-id="96330-162">Multiclass classification</span></span>

<span data-ttu-id="96330-163">Cas de [classification](#classification) où l’[étiquette](#label) provient d’une de trois classes ou plus.</span><span class="sxs-lookup"><span data-stu-id="96330-163">A [classification](#classification) case where the [label](#label) is one out of three or more classes.</span></span> <span data-ttu-id="96330-164">Pour plus d’informations, consultez l’article Wikipédia [Classification multiclasse](https://en.wikipedia.org/wiki/Multiclass_classification).</span><span class="sxs-lookup"><span data-stu-id="96330-164">For more information, see the [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification) article on Wikipedia.</span></span>

## <a name="n-gram"></a><span data-ttu-id="96330-165">N-gramme</span><span class="sxs-lookup"><span data-stu-id="96330-165">N-gram</span></span>

<span data-ttu-id="96330-166">Un schéma d’extraction de fonctionnalité pour les données texte : toute séquence de N termes se transforme en une valeur [fonctionnalité](#feature).</span><span class="sxs-lookup"><span data-stu-id="96330-166">A feature extraction scheme for text data: any sequence of N words turns into a [feature](#feature) value.</span></span>

## <a name="numerical-feature-vector"></a><span data-ttu-id="96330-167">Vecteur de fonctionnalité numérique</span><span class="sxs-lookup"><span data-stu-id="96330-167">Numerical feature vector</span></span>

<span data-ttu-id="96330-168">Un vecteur de [fonctionnalité](#feature) constitué uniquement de valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="96330-168">A [feature](#feature) vector consisting only of numerical values.</span></span> <span data-ttu-id="96330-169">Cette valeur est similaire à `double[]`.</span><span class="sxs-lookup"><span data-stu-id="96330-169">This is similar to `double[]`.</span></span>

## <a name="pipeline"></a><span data-ttu-id="96330-170">Pipeline</span><span class="sxs-lookup"><span data-stu-id="96330-170">Pipeline</span></span>

<span data-ttu-id="96330-171">Toutes les opérations nécessaires pour adapter un modèle à un jeu de données.</span><span class="sxs-lookup"><span data-stu-id="96330-171">All of the operations needed to fit a model to a data set.</span></span> <span data-ttu-id="96330-172">Un pipeline se compose des étapes d’importation, de transformation, de fonctionnalisation et d’apprentissage des données.</span><span class="sxs-lookup"><span data-stu-id="96330-172">A pipeline consists of data import, transformation, featurization, and learning steps.</span></span> <span data-ttu-id="96330-173">Une fois son apprentissage terminé, le pipeline se transforme en modèle.</span><span class="sxs-lookup"><span data-stu-id="96330-173">Once a pipeline is trained, it turns into a model.</span></span>

## <a name="precision"></a><span data-ttu-id="96330-174">Précision</span><span class="sxs-lookup"><span data-stu-id="96330-174">Precision</span></span>

<span data-ttu-id="96330-175">Dans une [classification](#classification), la précision d’une classe correspond au nombre d’éléments correctement prévus comme appartenant à cette classe, divisé par le nombre total d’éléments prévus comme appartenant à la classe.</span><span class="sxs-lookup"><span data-stu-id="96330-175">In [classification](#classification), the precision for a class is the number of items correctly predicted as belonging to that class divided by the total number of items predicted as belonging to the class.</span></span>

<span data-ttu-id="96330-176">API ML.NET connexe : <xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativePrecision?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositivePrecision?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-176">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativePrecision?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositivePrecision?displayProperty=nameWithType>.</span></span>

## <a name="recall"></a><span data-ttu-id="96330-177">Rappel</span><span class="sxs-lookup"><span data-stu-id="96330-177">Recall</span></span>

<span data-ttu-id="96330-178">Dans une [classification](#classification), le rappel d’une classe correspond au nombre d’éléments correctement prévus comme appartenant à cette classe, divisé par le nombre total d’éléments appartenant effectivement à la classe.</span><span class="sxs-lookup"><span data-stu-id="96330-178">In [classification](#classification), the recall for a class is the number of items correctly predicted as belonging to that class divided by the total number of items that actually belong to the class.</span></span>

<span data-ttu-id="96330-179">API ML.NET connexe : <xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativeRecall?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositiveRecall?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-179">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativeRecall?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositiveRecall?displayProperty=nameWithType>.</span></span>

## <a name="regression"></a><span data-ttu-id="96330-180">Régression</span><span class="sxs-lookup"><span data-stu-id="96330-180">Regression</span></span>

<span data-ttu-id="96330-181">Une tâche [Apprentissage automatique supervisé](#supervised-machine-learning) où la sortie est une valeur réelle, par exemple, double.</span><span class="sxs-lookup"><span data-stu-id="96330-181">A [supervised machine learning](#supervised-machine-learning) task where the output is a real value, for example, double.</span></span> <span data-ttu-id="96330-182">Exemple : prédiction de cours d’actions.</span><span class="sxs-lookup"><span data-stu-id="96330-182">Examples include predicting stock prices.</span></span>

## <a name="relative-absolute-error"></a><span data-ttu-id="96330-183">Erreur absolue relative</span><span class="sxs-lookup"><span data-stu-id="96330-183">Relative absolute error</span></span>

<span data-ttu-id="96330-184">Dans une [régression](#regression), une métrique d’évaluation correspondant à la somme de toutes les erreurs absolues, divisée par la somme des distances entre les valeurs d’[étiquette](#label) correctes et la moyenne de toutes les valeurs d’étiquette correctes.</span><span class="sxs-lookup"><span data-stu-id="96330-184">In [regression](#regression), an evaluation metric that is the sum of all absolute errors divided by the sum of distances between correct [label](#label) values and the average of all correct label values.</span></span>

## <a name="relative-squared-error"></a><span data-ttu-id="96330-185">Erreur quadratique relative</span><span class="sxs-lookup"><span data-stu-id="96330-185">Relative squared error</span></span>

<span data-ttu-id="96330-186">Dans une [régression](#regression), une métrique d’évaluation correspondant à la somme de toutes les erreurs absolues quadratiques, divisée par la somme des distances quadratiques entre les valeurs d’[étiquette](#label) correctes et la moyenne de toutes les valeurs d’étiquette correctes.</span><span class="sxs-lookup"><span data-stu-id="96330-186">In [regression](#regression), an evaluation metric that is the sum of all squared absolute errors divided by the sum of squared distances between correct [label](#label) values and the average of all correct label values.</span></span>

## <a name="root-of-mean-squared-error-rmse"></a><span data-ttu-id="96330-187">Racine de l’erreur quadratique moyenne (RMSE)</span><span class="sxs-lookup"><span data-stu-id="96330-187">Root of mean squared error (RMSE)</span></span>

<span data-ttu-id="96330-188">Dans une [régression](#regression), une métrique d’évaluation correspondant à la racine carrée de la moyenne des carrés des erreurs.</span><span class="sxs-lookup"><span data-stu-id="96330-188">In [regression](#regression), an evaluation metric that is the square root of the average of the squares of the errors.</span></span>

<span data-ttu-id="96330-189">API ML.NET connexe : <xref:Microsoft.ML.Models.RegressionMetrics.Rms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="96330-189">Related ML.NET API: <xref:Microsoft.ML.Models.RegressionMetrics.Rms?displayProperty=nameWithType>.</span></span>

## <a name="supervised-machine-learning"></a><span data-ttu-id="96330-190">Apprentissage automatique supervisé</span><span class="sxs-lookup"><span data-stu-id="96330-190">Supervised machine learning</span></span>

<span data-ttu-id="96330-191">Une sous-classe d’apprentissage automatique dans laquelle un modèle souhaité prévoit l’étiquette pour les données encore invisibles.</span><span class="sxs-lookup"><span data-stu-id="96330-191">A subclass of machine learning in which a desired model predicts the label for yet-unseen data.</span></span> <span data-ttu-id="96330-192">Exemples : classification, régression et prédiction structurée.</span><span class="sxs-lookup"><span data-stu-id="96330-192">Examples include classification, regression, and structured prediction.</span></span> <span data-ttu-id="96330-193">Pour plus d’informations, consultez l’article Wikipédia [Apprentissage supervisé](https://en.wikipedia.org/wiki/Supervised_learning).</span><span class="sxs-lookup"><span data-stu-id="96330-193">For more information, see the  [Supervised learning](https://en.wikipedia.org/wiki/Supervised_learning) article on Wikipedia.</span></span>

## <a name="training"></a><span data-ttu-id="96330-194">Formation</span><span class="sxs-lookup"><span data-stu-id="96330-194">Training</span></span>

<span data-ttu-id="96330-195">Le processus d’identification d’un [modèle](#model) pour un jeu de données d’apprentissage spécifique.</span><span class="sxs-lookup"><span data-stu-id="96330-195">The process of identifying a [model](#model) for a given training data set.</span></span> <span data-ttu-id="96330-196">Pour un modèle linéaire, cela signifie rechercher les pondérations.</span><span class="sxs-lookup"><span data-stu-id="96330-196">For a linear model, this means finding the weights.</span></span> <span data-ttu-id="96330-197">Pour un arbre, cette opération implique l’identification des points de fractionnement.</span><span class="sxs-lookup"><span data-stu-id="96330-197">For a tree, it involves the identifying the split points.</span></span>

## <a name="transform"></a><span data-ttu-id="96330-198">Transformer</span><span class="sxs-lookup"><span data-stu-id="96330-198">Transform</span></span>

<span data-ttu-id="96330-199">Un composant de [pipeline](#pipeline) qui transforme les données.</span><span class="sxs-lookup"><span data-stu-id="96330-199">A [pipeline](#pipeline) component that transforms data.</span></span> <span data-ttu-id="96330-200">Par exemple, d’un texte à un vecteur de valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="96330-200">For example, from text to vector of numbers.</span></span>

## <a name="unsupervised-machine-learning"></a><span data-ttu-id="96330-201">Apprentissage automatique non supervisé</span><span class="sxs-lookup"><span data-stu-id="96330-201">Unsupervised machine learning</span></span>

<span data-ttu-id="96330-202">Une sous-classe d’apprentissage automatique dans laquelle un modèle souhaité trouve une structure masquée (ou latente) dans les données.</span><span class="sxs-lookup"><span data-stu-id="96330-202">A subclass of machine learning in which a desired model finds hidden (or latent) structure in data.</span></span> <span data-ttu-id="96330-203">Exemples : clustering, modélisation de rubrique et réduction de dimensionnalité.</span><span class="sxs-lookup"><span data-stu-id="96330-203">Examples include clustering, topic modeling, and dimensionality reduction.</span></span> <span data-ttu-id="96330-204">Pour plus d’informations, consultez l’article Wikipédia [Apprentissage non supervisé](https://en.wikipedia.org/wiki/Unsupervised_learning).</span><span class="sxs-lookup"><span data-stu-id="96330-204">For more information, see the [Unsupervised learning](https://en.wikipedia.org/wiki/Unsupervised_learning) article on Wikipedia.</span></span>