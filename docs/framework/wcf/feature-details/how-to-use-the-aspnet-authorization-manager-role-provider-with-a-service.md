---
title: 'Procédure : Utiliser le fournisseur de rôles du Gestionnaire d’autorisations ASP.NET avec un Service'
ms.date: 03/30/2017
ms.assetid: f21deb81-91ef-49ef-94d6-494785143271
ms.openlocfilehash: de6c96fd8d0ea17954463d554504cdb4180a5268
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625560"
---
# <a name="how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service"></a>Procédure : Utiliser le fournisseur de rôles du Gestionnaire d’autorisations ASP.NET avec un Service
Lorsque [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] héberge un service Web, vous pouvez intégrer le Gestionnaire d'autorisations dans l'application pour fournir l'autorisation au service. Le Gestionnaire d'autorisations permet à un développeur d'applications de définir des opérations individuelles qui peuvent être regroupées pour former des tâches. Un administrateur peut autoriser ensuite que les rôles exécutent des tâches spécifiques ou des opérations individuelles. Le Gestionnaire d'autorisations fournit un outil d'administration sous la forme d'un composant logiciel enfichable MMC (Microsoft Management Console) pour gérer des rôles, des tâches, des opérations et des utilisateurs. Les administrateurs configurent un magasin de stratégie du Gestionnaire d'autorisations dans un fichier XML, Active Directory, ou dans un magasin Active Directory en mode application (ADAM).  
  
 Le Gestionnaire d'autorisations est intégré dans l'application en configurant le fournisseur de rôle [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] du Gestionnaire d'autorisations pour l'application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] qui héberge le service Web. Comme les autres fournisseurs de rôle [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], le fournisseur de rôle [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] du Gestionnaire d'autorisations est configuré à l'aide de l'élément <`providers`>.  
  
 L'exemple de code suivant représente une partie d'un fichier de configuration pour un service Web qui intègre le Gestionnaire d'autorisations dans l'application.  
  
```xml  
<system.web>  
    <roleManager enabled="true" defaultProvider="AzManRoleProvider">  
      <providers>  
        <add name="AzManRoleProvider"  
             type="System.Web.Security.AuthorizationStoreRoleProvider, System.Web, Version=2.0.0.0, Culture=neutral, publicKeyToken=b03f5f7f11d50a3a"  
             connectionStringName="AzManPolicyStoreConnectionString"   
             applicationName="SecureService"/>  
      </providers>  
    </roleManager>  
</system.web>  
```  
  
 Pour plus d’informations sur l’intégration d’un [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] fournisseur de rôles avec une application WCF, consultez [Comment : Utiliser le fournisseur de rôle ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md). Pour plus d’informations sur l’utilisation du Gestionnaire d’autorisations avec [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], consultez [Comment : Utilisez le Gestionnaire d’autorisations (AzMan) avec ASP.NET 2.0](https://go.microsoft.com/fwlink/?LinkId=71303).  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Utiliser le fournisseur de rôle ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)
