---
title: "IMetaDataAssemblyImport::EnumManifestResources 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataAssemblyImport.EnumManifestResources
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataAssemblyImport::EnumManifestResources
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumManifestResources method [.NET Framework metadata]
- EnumManifestResources method [.NET Framework metadata]
ms.assetid: 9543b111-5705-40c9-935c-a3ffc7a581aa
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 25d8b63e2f40566164274715e562960eafbb83e5
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="imetadataassemblyimportenummanifestresources-method"></a><span data-ttu-id="3e5c0-102">IMetaDataAssemblyImport::EnumManifestResources 메서드</span><span class="sxs-lookup"><span data-stu-id="3e5c0-102">IMetaDataAssemblyImport::EnumManifestResources Method</span></span>
<span data-ttu-id="3e5c0-103">현재 어셈블리 매니페스트에서 참조 하는 리소스에 대 한 열거자에 대 한 포인터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-103">Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e5c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e5c0-104">Syntax</span></span>  
  
```  
HRESULT EnumManifestResources (  
    [in, out] HCORENUM         *phEnum,   
    [out] mdManifestResource   rManifestResources[],   
    [in]  ULONG                cMax,   
    [out] ULONG                *pcTokens  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="3e5c0-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3e5c0-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="3e5c0-106">[out에서] 열거자에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="3e5c0-107">null 이어야 합니다 경우이 값은 `EnumManifestResources` 메서드를 처음으로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-107">This must be a null value when the `EnumManifestResources` method is called for the first time.</span></span>  
  
 `rManifestResources`  
 <span data-ttu-id="3e5c0-108">[out] 저장 하는 데 사용 되는 배열에서 `mdManifestResource` 메타 데이터 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-108">[out] The array used to store the `mdManifestResource` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="3e5c0-109">[in] 최대 `mdManifestResource` 에 배치할 수 있는 토큰 `rManifestResources`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-109">[in] The maximum number of `mdManifestResource` tokens that can be placed in `rManifestResources`.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="3e5c0-110">[out] 수가 `mdManifestResource` 토큰에 실제로 배치 `rManifestResources`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-110">[out] The number of `mdManifestResource` tokens actually placed in `rManifestResources`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3e5c0-111">반환 값</span><span class="sxs-lookup"><span data-stu-id="3e5c0-111">Return Value</span></span>  
  
|<span data-ttu-id="3e5c0-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3e5c0-112">HRESULT</span></span>|<span data-ttu-id="3e5c0-113">설명</span><span class="sxs-lookup"><span data-stu-id="3e5c0-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="3e5c0-114">`EnumManifestResources`성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-114">`EnumManifestResources` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="3e5c0-115">열거할 토큰이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="3e5c0-116">이 경우 `pcTokens` 0으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-116">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3e5c0-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="3e5c0-117">Requirements</span></span>  
 <span data-ttu-id="3e5c0-118">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3e5c0-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e5c0-119">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3e5c0-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3e5c0-120">**라이브러리:** MsCorEE.dll에서 리소스로 사용</span><span class="sxs-lookup"><span data-stu-id="3e5c0-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3e5c0-121">**.NET framework 버전:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e5c0-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e5c0-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3e5c0-122">See Also</span></span>  
 [<span data-ttu-id="3e5c0-123">IMetaDataAssemblyImport 인터페이스</span><span class="sxs-lookup"><span data-stu-id="3e5c0-123">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)