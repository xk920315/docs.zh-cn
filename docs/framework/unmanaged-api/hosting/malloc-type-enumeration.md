---
title: "MALLOC_TYPE 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: MALLOC_TYPE
api_location: mscoree.dll
api_type: COM
f1_keywords: MALLOC_TYPE
helpviewer_keywords: MALLOC_TYPE Enumeration
ms.assetid: c02476f9-23a2-4af7-9282-aa9c42c7429b
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 59a379b1c34f5b7c6b721627e6053cacf3ed784a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="malloctype-enumeration"></a><span data-ttu-id="09730-102">MALLOC_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="09730-102">MALLOC_TYPE Enumeration</span></span>
<span data-ttu-id="09730-103">包含指定的内存的分配时的特征的值。</span><span class="sxs-lookup"><span data-stu-id="09730-103">Contains values that specify the characteristics of the memory that is being allocated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09730-104">语法</span><span class="sxs-lookup"><span data-stu-id="09730-104">Syntax</span></span>  
  
```  
typedef enum {  
    MALLOC_THREADSAFE = 0x1,  
    MALLOC_EXECUTABLE = 0x2,  
} MALLOC_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="09730-105">成员</span><span class="sxs-lookup"><span data-stu-id="09730-105">Members</span></span>  
  
|<span data-ttu-id="09730-106">成员</span><span class="sxs-lookup"><span data-stu-id="09730-106">Member</span></span>|<span data-ttu-id="09730-107">描述</span><span class="sxs-lookup"><span data-stu-id="09730-107">Description</span></span>|  
|------------|-----------------|  
|`MALLOC_EXECUTABLE`|<span data-ttu-id="09730-108">分配的内存可以包含可执行文件。</span><span class="sxs-lookup"><span data-stu-id="09730-108">The allocated memory can contain an executable file.</span></span>|  
|`MALLOC_THREADSAFE`|<span data-ttu-id="09730-109">分配的内存是线程安全的。</span><span class="sxs-lookup"><span data-stu-id="09730-109">The allocated memory is thread-safe.</span></span> <span data-ttu-id="09730-110">也就是说，可以通过而不进行任何同步多个线程访问内存。</span><span class="sxs-lookup"><span data-stu-id="09730-110">That is, the memory can be accessed by multiple threads without any synchronization.</span></span><br /><br /> <span data-ttu-id="09730-111">如果未设置此标志，则必须序列化对象上的调用。</span><span class="sxs-lookup"><span data-stu-id="09730-111">If this flag is not set, calls on the object must be serialized.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="09730-112">要求</span><span class="sxs-lookup"><span data-stu-id="09730-112">Requirements</span></span>  
 <span data-ttu-id="09730-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="09730-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09730-114">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="09730-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="09730-115">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="09730-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="09730-116">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="09730-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09730-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09730-117">See Also</span></span>  
 [<span data-ttu-id="09730-118">承载枚举</span><span class="sxs-lookup"><span data-stu-id="09730-118">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)