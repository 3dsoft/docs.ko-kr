---
title: ICorDebugGenericValue Interface1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugGenericValue
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugGenericValue
helpviewer_keywords: ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: bc14f408-b359-4c8c-ade2-888ccdf7261b
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 61c159e30efb33dca4043e5b5306c9544acd614a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebuggenericvalue-interface1"></a><span data-ttu-id="e79f4-102">ICorDebugGenericValue Interface1</span><span class="sxs-lookup"><span data-stu-id="e79f4-102">ICorDebugGenericValue Interface1</span></span>
<span data-ttu-id="e79f4-103">모든 값에 적용 되는 "ICorDebugValue"의 하위 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-103">A subclass of "ICorDebugValue" that applies to all values.</span></span> <span data-ttu-id="e79f4-104">이 인터페이스에서는 값의 Get 및 Set 메서드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-104">This interface provides Get and Set methods for the value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e79f4-105">메서드</span><span class="sxs-lookup"><span data-stu-id="e79f4-105">Methods</span></span>  
  
|<span data-ttu-id="e79f4-106">메서드</span><span class="sxs-lookup"><span data-stu-id="e79f4-106">Method</span></span>|<span data-ttu-id="e79f4-107">설명</span><span class="sxs-lookup"><span data-stu-id="e79f4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e79f4-108">GetValue 메서드</span><span class="sxs-lookup"><span data-stu-id="e79f4-108">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggenericvalue-getvalue-method.md)|<span data-ttu-id="e79f4-109">지정된 된 버퍼에 값을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-109">Copies the value into the specified buffer.</span></span>|  
|[<span data-ttu-id="e79f4-110">SetValue 메서드</span><span class="sxs-lookup"><span data-stu-id="e79f4-110">SetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggenericvalue-setvalue-method.md)|<span data-ttu-id="e79f4-111">지정된 된 버퍼에서 새 값을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-111">Copies a new value from the specified buffer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e79f4-112">설명</span><span class="sxs-lookup"><span data-stu-id="e79f4-112">Remarks</span></span>  
 <span data-ttu-id="e79f4-113">`ICorDebugGenericValue`비 원격 이기 때문에 하위 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-113">`ICorDebugGenericValue` is a sub-interface because it is non-remotable.</span></span>  
  
 <span data-ttu-id="e79f4-114">참조 형식에 대 한 값이 참조의 내용을 보다는 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-114">For reference types, the value is the reference rather than the contents of the reference.</span></span>  
  
 <span data-ttu-id="e79f4-115">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-115">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e79f4-116">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e79f4-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e79f4-117">Requirements</span></span>  
 <span data-ttu-id="e79f4-118">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="e79f4-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e79f4-119">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e79f4-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e79f4-120">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e79f4-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e79f4-121">**.NET framework 버전:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e79f4-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e79f4-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e79f4-122">See Also</span></span>  
    
 [<span data-ttu-id="e79f4-123">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e79f4-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)