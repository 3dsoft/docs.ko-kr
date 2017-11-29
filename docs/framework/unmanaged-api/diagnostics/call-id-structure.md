---
title: "CALL_ID 구조체"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CALL_ID
api_location: diasymreader.dll
api_type: COM
f1_keywords: CALL_ID
helpviewer_keywords: CALL_ID structure [.NET Framework debugging]
ms.assetid: bfd46324-afec-4782-9c18-586d81fb4740
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c44db9021a7dbf5b497db3536eddcea020e71bf7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="callid-structure"></a><span data-ttu-id="c91d6-102">CALL_ID 구조체</span><span class="sxs-lookup"><span data-stu-id="c91d6-102">CALL_ID Structure</span></span>
<span data-ttu-id="c91d6-103">디버거에 호출 되는 함수에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-103">Provides information to a debugger about a function that is being called.</span></span> <span data-ttu-id="c91d6-104">참조는 [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) 자세한 정보에 대 한 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-104">See the [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) interface for more information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c91d6-105">구문</span><span class="sxs-lookup"><span data-stu-id="c91d6-105">Syntax</span></span>  
  
```  
typedef struct tagCALL_ID  
{  
    LPCOLESTR       szMachine;  
    DWORD           dwPid;  
    USER_THREAD     *pUserThread;  
    STACK_ADDRESS   addrStackPointer;  
    LPCOLESTR       szEntryPoint;  
    LPCOLESTR       szDestinationMachine;  
} CALL_ID;  
```  
  
## <a name="members"></a><span data-ttu-id="c91d6-106">멤버</span><span class="sxs-lookup"><span data-stu-id="c91d6-106">Members</span></span>  
  
|<span data-ttu-id="c91d6-107">멤버</span><span class="sxs-lookup"><span data-stu-id="c91d6-107">Member</span></span>|<span data-ttu-id="c91d6-108">설명</span><span class="sxs-lookup"><span data-stu-id="c91d6-108">Description</span></span>|  
|------------|-----------------|  
|`szMachine`|<span data-ttu-id="c91d6-109">이 호출 하는 컴퓨터를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-109">Identifies the machine that is making the call.</span></span>|  
|`dwPid`|<span data-ttu-id="c91d6-110">컴퓨터 프로세서를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-110">Identifies the machine processor.</span></span>|  
|`pUserThread`|<span data-ttu-id="c91d6-111">호출을 실행 하는 스레드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-111">Identifies the thread that is executing the call.</span></span>|  
|`addrStackPointer`|<span data-ttu-id="c91d6-112">호출 스택의 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-112">Specifies the address of the call stack.</span></span>|  
|`szEntryPoint`|<span data-ttu-id="c91d6-113">호출의 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-113">Specifies the address of the call.</span></span>|  
|`szDestinationMachine`|<span data-ttu-id="c91d6-114">호출을 실행할 컴퓨터를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-114">Identifies the machine that will execute the call.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c91d6-115">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c91d6-115">Requirements</span></span>  
 <span data-ttu-id="c91d6-116">**헤더:** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="c91d6-116">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c91d6-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c91d6-117">See Also</span></span>  
 [<span data-ttu-id="c91d6-118">INotifySink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="c91d6-118">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)  
 [<span data-ttu-id="c91d6-119">진단 기호 저장소 구조체</span><span class="sxs-lookup"><span data-stu-id="c91d6-119">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)