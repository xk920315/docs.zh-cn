---
title: "ICorProfilerInfo4::GetObjectSize2 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo4.GetObjectSize2
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo4::GetObjectSize2
helpviewer_keywords:
- GetObjectSize2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetObjectSize2 method [.NET Framework profiling]
ms.assetid: 4a3e43ed-3ee3-4395-ab14-f78b903be13e
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 4898157e6525d3b9da4cfade9862b88252df7b14
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerinfo4getobjectsize2-method"></a><span data-ttu-id="8a802-102">ICorProfilerInfo4::GetObjectSize2 方法</span><span class="sxs-lookup"><span data-stu-id="8a802-102">ICorProfilerInfo4::GetObjectSize2 Method</span></span>
<span data-ttu-id="8a802-103">返回指定对象的大小。</span><span class="sxs-lookup"><span data-stu-id="8a802-103">Returns the size of a specified object.</span></span> <span data-ttu-id="8a802-104">替换[icorprofilerinfo:: Getobjectsize](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getobjectsize-method.md)通过报告大于什么可以用来表示的对象的大小的方法`ULONG`。</span><span class="sxs-lookup"><span data-stu-id="8a802-104">Replaces the [ICorProfilerInfo::GetObjectSize](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getobjectsize-method.md) method by reporting sizes of objects that are larger than what can be expressed in a `ULONG`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a802-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a802-105">Syntax</span></span>  
  
```  
HRESULT GetObjectSize2(  
    [in]  ObjectID objectId,  
    [out] SIZE_T *pcSize);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8a802-106">参数</span><span class="sxs-lookup"><span data-stu-id="8a802-106">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="8a802-107">[in]对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="8a802-107">[in] The ID of the object.</span></span>  
  
 `pcSize`  
 <span data-ttu-id="8a802-108">[out]指向对象的大小，以字节为单位的指针。</span><span class="sxs-lookup"><span data-stu-id="8a802-108">[out] A pointer to the object's size, in bytes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8a802-109">备注</span><span class="sxs-lookup"><span data-stu-id="8a802-109">Remarks</span></span>  
 <span data-ttu-id="8a802-110">相同的类型的不同对象通常具有相同的大小。</span><span class="sxs-lookup"><span data-stu-id="8a802-110">Different objects of the same types often have the same size.</span></span> <span data-ttu-id="8a802-111">但是，某些类型，如数组或字符串，可能具有不同大小的每个对象。</span><span class="sxs-lookup"><span data-stu-id="8a802-111">However, some types, such as arrays or strings, may have a different size for each object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a802-112">要求</span><span class="sxs-lookup"><span data-stu-id="8a802-112">Requirements</span></span>  
 <span data-ttu-id="8a802-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a802-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a802-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8a802-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8a802-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a802-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a802-116">**.NET framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a802-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a802-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a802-117">See Also</span></span>  
 [<span data-ttu-id="8a802-118">ICorProfilerInfo4 接口</span><span class="sxs-lookup"><span data-stu-id="8a802-118">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)