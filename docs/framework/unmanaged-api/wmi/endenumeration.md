---
title: "EndEnumeration 함수 (관리 되지 않는 API 참조)"
description: "EndEnumeration 함수는 열거형을 종료 합니다."
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: EndEnumeration
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: EndEnumeration
helpviewer_keywords: EndEnumeration function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 043fce26870e5af2850b9f2e91e7e97c7bee6c90
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/15/2017
---
# <a name="endenumeration-function"></a><span data-ttu-id="62a14-103">EndEnumeration 함수</span><span class="sxs-lookup"><span data-stu-id="62a14-103">EndEnumeration function</span></span>
<span data-ttu-id="62a14-104">에 대 한 호출을 시작 하는 열거형 시퀀스를 마칩니다.는 [BeginEnumeration 함수](beginenumeration.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="62a14-104">Terminates an enumeration sequence started with a call to the [BeginEnumeration function](beginenumeration.md).</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="62a14-105">구문</span><span class="sxs-lookup"><span data-stu-id="62a14-105">Syntax</span></span>  
  
```  
HRESULT EndEnumeration (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr 
); 
```  

## <a name="parameters"></a><span data-ttu-id="62a14-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="62a14-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="62a14-107">[in] 이 매개 변수를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62a14-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="62a14-108">[in] 에 대 한 포인터는 [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="62a14-108">[in] A pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span></span>


## <a name="return-value"></a><span data-ttu-id="62a14-109">반환 값</span><span class="sxs-lookup"><span data-stu-id="62a14-109">Return value</span></span>

<span data-ttu-id="62a14-110">이 함수에서 반환 되는 다음 값에 정의 된는 *WbemCli.h* 헤더 파일 또는 있습니다를 정의할 수 상수로 코드:</span><span class="sxs-lookup"><span data-stu-id="62a14-110">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="62a14-111">상수</span><span class="sxs-lookup"><span data-stu-id="62a14-111">Constant</span></span>  |<span data-ttu-id="62a14-112">값</span><span class="sxs-lookup"><span data-stu-id="62a14-112">Value</span></span>  |<span data-ttu-id="62a14-113">설명</span><span class="sxs-lookup"><span data-stu-id="62a14-113">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="62a14-114">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="62a14-114">0x80041001</span></span> | <span data-ttu-id="62a14-115">일반 오류가 발생이 했습니다.</span><span class="sxs-lookup"><span data-stu-id="62a14-115">There has been a general failure.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="62a14-116">0</span><span class="sxs-lookup"><span data-stu-id="62a14-116">0</span></span> | <span data-ttu-id="62a14-117">함수 호출이 성공 했습니다.</span><span class="sxs-lookup"><span data-stu-id="62a14-117">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="62a14-118">설명</span><span class="sxs-lookup"><span data-stu-id="62a14-118">Remarks</span></span>

<span data-ttu-id="62a14-119">이 함수에 대 한 호출을 래핑하는 [IWbemClassObject::EndEnumeration](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) 메서드.</span><span class="sxs-lookup"><span data-stu-id="62a14-119">This function wraps a call to the [IWbemClassObject::EndEnumeration](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) method.</span></span>

<span data-ttu-id="62a14-120">에 대 한 호출에서 `EndEnumeration` 함수는 필요 하지 않지만 열거와 연결 된 리소스를 해제 하기 때문에 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="62a14-120">A call to the `EndEnumeration` function is not required, but it is recommended because it releases resources associated with the enumeration.</span></span> <span data-ttu-id="62a14-121">그러나는 resoruces는 자동으로 할당 취소 다음 열거를 시작 하거나 개체가 해제 될 때입니다.</span><span class="sxs-lookup"><span data-stu-id="62a14-121">However, the resoruces are deallocated automatically when the next enumeration is started or the object is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a14-122">요구 사항</span><span class="sxs-lookup"><span data-stu-id="62a14-122">Requirements</span></span>  
 <span data-ttu-id="62a14-123">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="62a14-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62a14-124">**헤더:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="62a14-124">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="62a14-125">**.NET framework 버전:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="62a14-125">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62a14-126">참고 항목</span><span class="sxs-lookup"><span data-stu-id="62a14-126">See also</span></span>  
[<span data-ttu-id="62a14-127">WMI 및 성능 카운터 (관리 되지 않는 API 참조)</span><span class="sxs-lookup"><span data-stu-id="62a14-127">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)