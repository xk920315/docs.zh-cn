---
title: "IMetaDataTables2::GetMetaDataStreamInfo 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataTables2.GetMetaDataStreamInfo
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataTables2::GetMetaDataStreamInfo
helpviewer_keywords:
- GetMetaDataStreamInfo method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStreamInfo method [.NET Framework metadata]
ms.assetid: 8b280627-cc74-4789-95da-1fefc966de05
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: b1631ae8398a8daa910931ff705440a2be0cf21b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatatables2getmetadatastreaminfo-method"></a><span data-ttu-id="de885-102">IMetaDataTables2::GetMetaDataStreamInfo 方法</span><span class="sxs-lookup"><span data-stu-id="de885-102">IMetaDataTables2::GetMetaDataStreamInfo Method</span></span>
<span data-ttu-id="de885-103">获取名称、 大小和元数据流的指定索引处的内容。</span><span class="sxs-lookup"><span data-stu-id="de885-103">Gets the name, size, and contents of the metadata stream at the specified index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de885-104">语法</span><span class="sxs-lookup"><span data-stu-id="de885-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataStreamInfo (  
   [in]  ULONG        ix,  
   [out] const char   **ppchName,  
   [out] const void   **ppv,  
   [out] ULONG        *pcb  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="de885-105">参数</span><span class="sxs-lookup"><span data-stu-id="de885-105">Parameters</span></span>  
 `ix`  
 <span data-ttu-id="de885-106">[in]请求的元数据流的索引。</span><span class="sxs-lookup"><span data-stu-id="de885-106">[in] The index of the requested metadata stream.</span></span>  
  
 `ppchName`  
 <span data-ttu-id="de885-107">[out]指向流的名称的指针。</span><span class="sxs-lookup"><span data-stu-id="de885-107">[out] A pointer to the name of the stream.</span></span>  
  
 `ppv`  
 <span data-ttu-id="de885-108">[out]指向元数据流的指针。</span><span class="sxs-lookup"><span data-stu-id="de885-108">[out] A pointer to the metadata stream.</span></span>  
  
 `pcb`  
 <span data-ttu-id="de885-109">[out]大小，以字节为单位的`ppv`。</span><span class="sxs-lookup"><span data-stu-id="de885-109">[out] The size, in bytes, of `ppv`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de885-110">要求</span><span class="sxs-lookup"><span data-stu-id="de885-110">Requirements</span></span>  
 <span data-ttu-id="de885-111">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="de885-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de885-112">**标头：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="de885-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="de885-113">**库：**用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="de885-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="de885-114">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de885-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de885-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="de885-115">See Also</span></span>  
 [<span data-ttu-id="de885-116">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="de885-116">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)  
 [<span data-ttu-id="de885-117">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="de885-117">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)