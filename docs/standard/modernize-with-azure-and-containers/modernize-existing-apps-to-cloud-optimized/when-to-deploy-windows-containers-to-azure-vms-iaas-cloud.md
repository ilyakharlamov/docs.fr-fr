---
title: Quand déployer des conteneurs de Windows sur les machines virtuelles Azure (IaaS cloud)
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Quand déployer des conteneurs de Windows sur les machines virtuelles Azure (IaaS cloud)
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 51217e2c94fd9727c8f7907e791cdebaec98f14f
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152147"
---
# <a name="when-to-deploy-windows-containers-to-azure-vms-iaas-cloud"></a>Quand déployer des conteneurs de Windows sur les machines virtuelles Azure (IaaS cloud)

Si votre organisation utilise des machines virtuelles Azure, même si vous utilisez également les conteneurs Windows, vous travaillez toujours avec IaaS. Cela signifie que qui traite des opérations d’infrastructure, des correctifs de système d’exploitation de la machine virtuelle et complexité de l’infrastructure pour les applications hautement évolutives lorsque vous avez besoin déployer plusieurs machines virtuelles dans une infrastructure à charge équilibrée de charge. Les principaux scénarios d’utilisation des conteneurs de Windows dans une machine virtuelle Azure sont :

-   **Environnement de développement/test**: Une machine virtuelle dans le cloud est idéale pour le développement et de test dans le cloud. Vous pouvez rapidement créer ou arrêt de l’environnement selon vos besoins.

-   **Évolutivité de petite et moyenne doit**: Dans les scénarios où vous devrez peut-être quelques machines virtuelles pour votre environnement de production, gérez un petit nombre de machines virtuelles peut être abordable jusqu'à ce que vous pouvez déplacer vers les environnements PaaS plus avancées, telles que les orchestrateurs.

-   **Environnement de production avec les outils de déploiement existants**: Vous pouvez déplacer à partir d’un environnement local dans lequel vous avez investi dans les outils pour effectuer des déploiements complexes pour les machines virtuelles ou des serveurs nus (par exemple, Puppet ou des outils similaires). Pour déplacer vers le cloud avec des modifications minimes aux procédures de déploiement environnement de production, vous pourrez continuer à utiliser ces outils pour déployer les machines virtuelles Azure. Toutefois, vous souhaiterez utiliser les conteneurs Windows en tant que l’unité de déploiement pour améliorer l’expérience de déploiement.

>[!div class="step-by-step"]
>[Précédent](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
>[Suivant](when-to-deploy-windows-containers-to-azure-container-instances-ACI.md)