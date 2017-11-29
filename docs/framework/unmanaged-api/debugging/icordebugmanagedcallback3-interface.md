---
title: "ICorDebugManagedCallback3 인터페이스"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback3
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback3
helpviewer_keywords: ICorDebugManagedCallback3 interface [.NET Framework debugging]
ms.assetid: a95389d3-cf2e-47a4-9805-61426acc6b65
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d2f24cc8fbd8533ef6717bc1dcd1baab0ea9ab45
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmanagedcallback3-interface"></a><span data-ttu-id="aaef0-102">ICorDebugManagedCallback3 인터페이스</span><span class="sxs-lookup"><span data-stu-id="aaef0-102">ICorDebugManagedCallback3 Interface</span></span>
<span data-ttu-id="aaef0-103">활성화된 사용자 지정 디버거 알림이 발생했음을 나타내는 콜백 메서드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="aaef0-103">Provides a callback method that indicates that an enabled custom debugger notification has been raised.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="aaef0-104">메서드</span><span class="sxs-lookup"><span data-stu-id="aaef0-104">Methods</span></span>  
  
|<span data-ttu-id="aaef0-105">메서드</span><span class="sxs-lookup"><span data-stu-id="aaef0-105">Method</span></span>|<span data-ttu-id="aaef0-106">설명</span><span class="sxs-lookup"><span data-stu-id="aaef0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="aaef0-107">CustomNotification 메서드</span><span class="sxs-lookup"><span data-stu-id="aaef0-107">CustomNotification Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md)|<span data-ttu-id="aaef0-108">사용 가능한 사용자 지정 디버거 알림이 발생 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aaef0-108">Indicates that an enabled custom debugger notification has been raised.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aaef0-109">설명</span><span class="sxs-lookup"><span data-stu-id="aaef0-109">Remarks</span></span>  
 <span data-ttu-id="aaef0-110">이 인터페이스는 논리적으로 확장 된 [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) 및 [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="aaef0-110">This interface is a logical extension of the [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) and [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="aaef0-111">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaef0-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aaef0-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="aaef0-112">Requirements</span></span>  
 <span data-ttu-id="aaef0-113">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="aaef0-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aaef0-114">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="aaef0-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aaef0-115">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aaef0-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aaef0-116">**.NET framework 버전:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aaef0-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aaef0-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="aaef0-117">See Also</span></span>  
 [<span data-ttu-id="aaef0-118">ICorDebugManagedCallback 인터페이스</span><span class="sxs-lookup"><span data-stu-id="aaef0-118">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)  
 [<span data-ttu-id="aaef0-119">ICorDebugManagedCallback2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="aaef0-119">ICorDebugManagedCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)  
 [<span data-ttu-id="aaef0-120">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="aaef0-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="aaef0-121">디버깅</span><span class="sxs-lookup"><span data-stu-id="aaef0-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)