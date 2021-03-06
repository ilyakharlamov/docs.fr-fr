---
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: c8e476ab90fda9214831fbd5beaba518f3e3bd20
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491426"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a>System.ServiceModel.Channels.MsmqPoisonMessageRejected
Message poison rejeté.  
  
## <a name="description"></a>Description  
 Le suivi indique qu'un message poison a été rencontré et rejeté par la suite. Cela se produit seulement lorsque la propriété `ReceiveErrorHandling` sur NetMsmqBinding ou MsmqIntegrationBinding a la valeur `Reject`. Un message refusé est remis à l’expéditeur [file d’attente de lettres mortes](https://go.microsoft.com/fwlink/?LinkId=99544).  
  
 Consultez [des messages incohérents](https://go.microsoft.com/fwlink/?LinkId=99546) pour plus d’informations sur le moment où les messages deviennent incohérents et comment configurer votre service pour traiter de manière appropriée. Consultez [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548) pour plus d’informations sur ce que signifie un message refusé dans MSMQ.  
  
## <a name="see-also"></a>Voir aussi
- [Suivi](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Utilisation du suivi pour résoudre les problèmes posés par votre application](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Administration et diagnostics](../../../../../docs/framework/wcf/diagnostics/index.md)
- [Messages incohérents](https://go.microsoft.com/fwlink/?LinkId=99546)
- [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548)
