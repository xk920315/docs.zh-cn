---
title: "ICorDebugHeapValue::IsValid 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugHeapValue.IsValid
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugHeapValue::IsValid
helpviewer_keywords:
- IsValid method [.NET Framework debugging]
- ICorDebugHeapValue::IsValid method [.NET Framework debugging]
ms.assetid: 68e20e62-203d-46d8-bb91-8d3c61cfacc3
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: df7105c94a6f88c9c196f1d9d6be6f4a62f7c258
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugheapvalueisvalid-method"></a><span data-ttu-id="e4e88-102">ICorDebugHeapValue::IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="e4e88-102">ICorDebugHeapValue::IsValid Method</span></span>
<span data-ttu-id="e4e88-103">获取一个值，该值指示此 ICorDebugHeapValue 所表示的对象是否有效。</span><span class="sxs-lookup"><span data-stu-id="e4e88-103">Gets a value that indicates whether the object represented by this ICorDebugHeapValue is valid.</span></span>  
  
 <span data-ttu-id="e4e88-104">.NET Framework 2.0 版中，此方法已被否决。</span><span class="sxs-lookup"><span data-stu-id="e4e88-104">This method has been deprecated in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4e88-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4e88-105">Syntax</span></span>  
  
```  
HRESULT IsValid (  
    [out] BOOL    *pbValid  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e4e88-106">参数</span><span class="sxs-lookup"><span data-stu-id="e4e88-106">Parameters</span></span>  
 `pbValid`  
 <span data-ttu-id="e4e88-107">[out]指向一个布尔值，该值指示是否在堆上的此值为有效的指针。</span><span class="sxs-lookup"><span data-stu-id="e4e88-107">[out] A pointer to a Boolean value that indicates whether this value on the heap is valid.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e4e88-108">备注</span><span class="sxs-lookup"><span data-stu-id="e4e88-108">Remarks</span></span>  
 <span data-ttu-id="e4e88-109">如果垃圾回收器回收，则的值无效。</span><span class="sxs-lookup"><span data-stu-id="e4e88-109">The value is invalid if it has been reclaimed by the garbage collector.</span></span>  
  
 <span data-ttu-id="e4e88-110">此方法已被否决。</span><span class="sxs-lookup"><span data-stu-id="e4e88-110">This method has been deprecated.</span></span> <span data-ttu-id="e4e88-111">在.NET Framework 2.0 中，所有值都是有效期截止日期[icordebugcontroller:: Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md)调用，在这段时间的值都是失效。</span><span class="sxs-lookup"><span data-stu-id="e4e88-111">In the .NET Framework 2.0, all values are valid until [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) is called, at which time the values are invalidated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4e88-112">要求</span><span class="sxs-lookup"><span data-stu-id="e4e88-112">Requirements</span></span>  
 <span data-ttu-id="e4e88-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e88-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4e88-114">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e4e88-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e4e88-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4e88-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4e88-116">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4e88-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>