---
title: "IAssemblyName 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAssemblyName
api_location: fusion.dll
api_type: COM
f1_keywords: IAssemblyName
helpviewer_keywords: IAssemblyName interface [.NET Framework fusion]
ms.assetid: f7f8e605-6b67-4151-936f-f04ecd671d90
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 902ad9f67d06306e79666f0e10d85bdb9c65c377
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="iassemblyname-interface"></a>IAssemblyName 接口
提供用于描述和使用程序集的唯一标识的方法。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[Clone 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-clone-method.md)|创建此的浅表副本`IAssemblyName`对象。|  
|[Finalize 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-finalize-method.md)|允许此`IAssemblyName`对象以释放资源并执行其他清理操作之前调用其析构函数。|  
|[GetDisplayName 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getdisplayname-method.md)|获取此引用的程序集的用户可读名称`IAssemblyName`对象。|  
|[GetName 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getname-method.md)|获取此引用的程序集的简单、 非加密名称`IAssemblyName`对象。|  
|[GetProperty 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getproperty-method.md)|获取一个指针指向由指定引用的属性`PropertyId`。|  
|[GetVersion 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getversion-method.md)|获取此引用的程序集的版本信息`IAssemblyName`对象。|  
|[IsEqual 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-isequal-method.md)|确定指定`IAssemblyName`对象是否等于此`IAssemblyName`、 根据指定的比较标志。|  
|[SetProperty 方法](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-setproperty-method.md)|设置指定所引用的属性的值`PropertyId`。|  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** Fusion.h  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [合成接口](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)  
 [IAssemblyEnum 接口](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md)
