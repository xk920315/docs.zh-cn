---
title: "ICorDebugThread3 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugThread3
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugThread3
helpviewer_keywords: ICorDebugThread3 interface [.NET Framework debugging]
ms.assetid: eb2860ef-06cb-4968-a6c3-6d048ecda2a4
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ed505cacc5286d27bc9a94eaa192dc6b889eb525
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugthread3-interface"></a><span data-ttu-id="614fe-102">ICorDebugThread3 接口</span><span class="sxs-lookup"><span data-stu-id="614fe-102">ICorDebugThread3 Interface</span></span>
<span data-ttu-id="614fe-103">提供的入口点[ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md)和相应接口。</span><span class="sxs-lookup"><span data-stu-id="614fe-103">Provides the entry point to the [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) and corresponding interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="614fe-104">方法</span><span class="sxs-lookup"><span data-stu-id="614fe-104">Methods</span></span>  
  
|<span data-ttu-id="614fe-105">方法</span><span class="sxs-lookup"><span data-stu-id="614fe-105">Method</span></span>|<span data-ttu-id="614fe-106">描述</span><span class="sxs-lookup"><span data-stu-id="614fe-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="614fe-107">CreateStackWalk 方法</span><span class="sxs-lookup"><span data-stu-id="614fe-107">CreateStackWalk Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-createstackwalk-method.md)|<span data-ttu-id="614fe-108">创建[ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md)线程你想要展开其堆栈的对象。</span><span class="sxs-lookup"><span data-stu-id="614fe-108">Creates an [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>|  
|[<span data-ttu-id="614fe-109">GetActiveInternalFrames 方法</span><span class="sxs-lookup"><span data-stu-id="614fe-109">GetActiveInternalFrames Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-getactiveinternalframes-method.md)|<span data-ttu-id="614fe-110">返回内部帧的数组 ([ICorDebugInternalFrame2](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md)对象) 堆栈上。</span><span class="sxs-lookup"><span data-stu-id="614fe-110">Returns an array of internal frames ([ICorDebugInternalFrame2](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md) objects) on the stack.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="614fe-111">备注</span><span class="sxs-lookup"><span data-stu-id="614fe-111">Remarks</span></span>  
 <span data-ttu-id="614fe-112">`ICorDebugThread3`ICorDebugThread 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="614fe-112">`ICorDebugThread3` is a logical extension to the ICorDebugThread interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="614fe-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="614fe-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="614fe-114">要求</span><span class="sxs-lookup"><span data-stu-id="614fe-114">Requirements</span></span>  
 <span data-ttu-id="614fe-115">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="614fe-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="614fe-116">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="614fe-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="614fe-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="614fe-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="614fe-118">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="614fe-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="614fe-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="614fe-119">See Also</span></span>  
 [<span data-ttu-id="614fe-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="614fe-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="614fe-121">调试</span><span class="sxs-lookup"><span data-stu-id="614fe-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)