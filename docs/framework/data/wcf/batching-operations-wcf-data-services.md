---
title: "批处理操作（WCF 数据服务）"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework-oob
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: WCF Data Services, client library
ms.assetid: 962a49d1-cc11-4b96-bc7d-071dd6607d6c
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 65bf6bfd0bd437848137506605a958f5f2e8d750
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="batching-operations-wcf-data-services"></a>批处理操作（WCF 数据服务）
[!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)]支持对请求的批处理[!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)]-基于服务。 有关详细信息，请参阅[OData： 批处理](http://go.microsoft.com/fwlink/?LinkId=186075)。 在[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)]，使用每个操作<xref:System.Data.Services.Client.DataServiceContext>，如执行查询或保存更改，在单独的请求发送到数据服务中的结果。 为保持操作集的合理范围，可以显式定义操作批。 这将确保批处理中的所有操作发送到单个 HTTP 请求中的数据服务，使服务器能够处理这些操作以原子方式，并减少到数据服务的往返次数。  
  
## <a name="batching-query-operations"></a>查询操作批处理  
 若要在一个批中执行多个查询，必须在该批中将每个查询创建为 <xref:System.Data.Services.Client.DataServiceRequest%601> 类的一个单独实例。 以这种方式创建查询请求时，查询本身将定义为 URI，并遵循资源寻址规则。 有关详细信息，请参阅[访问数据服务资源](../../../../docs/framework/data/wcf/accessing-data-service-resources-wcf-data-services.md)。 在调用包含查询请求对象的 <xref:System.Data.Services.Client.DataServiceContext.ExecuteBatch%2A> 方法时，会将批处理查询请求发送到数据服务。 此方法返回一个 <xref:System.Data.Services.Client.DataServiceResponse> 对象，它是代表对批中各个查询的响应的 <xref:System.Data.Services.Client.QueryOperationResponse%601> 对象的集合，其中每个对象包含查询返回的对象集合或错误信息。 当批中任何一个查询操作失败时，将针对失败的操作在 <xref:System.Data.Services.Client.QueryOperationResponse%601> 对象中返回错误信息，并继续执行其余操作。 有关详细信息，请参阅[如何： 在批处理中执行查询](../../../../docs/framework/data/wcf/how-to-execute-queries-in-a-batch-wcf-data-services.md)。  
  
 批处理查询也可以采用异步方式执行。 有关详细信息，请参阅[异步操作](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md)。  
  
## <a name="batching-the-savechanges-operation"></a>SaveChanges 操作批处理  
 当调用<xref:System.Data.Services.Client.DataServiceContext.SaveChanges%2A>方法，跟踪被转换成基于 REST 的操作作为发送上下文请求到的所有更改[!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)]服务。 默认情况下，不会在同一请求消息中发送这些更改。 需要单个请求中发送所有更改，必须调用<xref:System.Data.Services.Client.DataServiceContext.SaveChanges%28System.Data.Services.Client.SaveChangesOptions%29>方法和包括的一个值<xref:System.Data.Services.Client.SaveChangesOptions.Batch>中<xref:System.Data.Services.Client.SaveChangesOptions>提供给方法的枚举。  
  
 此外，还可以采用异步方式保存批处理更改。 有关详细信息，请参阅[异步操作](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md)。  
  
## <a name="see-also"></a>请参阅  
 [WCF Data Services 客户端库](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
