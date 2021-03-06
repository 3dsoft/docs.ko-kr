---
title: 110 - CustomTrackingRecordWarning
ms.date: 03/30/2017
ms.assetid: 3bc093de-be47-4ed0-983f-05b4246446fc
ms.openlocfilehash: 230e889c677ee83b2e71b128413b7107ec11dc2e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33514497"
---
# <a name="110---customtrackingrecordwarning"></a>110 - CustomTrackingRecordWarning
## <a name="properties"></a>속성  
  
|||  
|-|-|  
|Id|110|  
|키워드|UserEvents, EndToEndMonitoring, 문제 해결, HealthMonitoring, WFTracking|  
|수준|경고|  
|채널|Microsoft-Windows-응용 프로그램 서버-응용 프로그램/분석|  
  
## <a name="description"></a>설명  
 워크플로 인스턴스에 포함된 활동에서 경고 수준의 CustomTrackingRecord를 내보내면 ETW 추적 참가자가 이 이벤트를 내보냅니다.  
  
## <a name="message"></a>메시지  
 TrackRecord = CustomTrackingRecord, InstanceID = %1, RecordNumber=%2, EventTime=%3, Name=%4, ActivityName=%5, ActivityId=%6, ActivityInstanceId=%7, ActivityTypeName=%8, Data=%9, Annotations=%10, ProfileName = %11  
  
## <a name="details"></a>설명  
  
|데이터 항목 이름|데이터 항목 형식|설명|  
|--------------------|--------------------|-----------------|  
|InstanceId|xs:GUID|워크플로의 인스턴스 ID|  
|RecordNumber|xs:long|내보낸 레코드의 시퀀스 번호|  
|EventTime|xs:dateTime|이벤트를 내보낸 시간(UTC)|  
|이름|xs:string|CustomTrackingRecord의 이름|  
|ActivityName|xs:string|CustomTrackingRecord를 내보낸 활동의 이름|  
|ActivityId|xs:string|CustomTrackingRecord를 내보낸 활동의 ID|  
|ActivityInstanceId|xs:string|CustomTrackingRecord를 내보낸 활동의 인스턴스 ID|  
|ActivityTypeName|xs:string|CustomTrackingRecord를 내보낸 활동의 이름|  
|데이터|xs:string|이 이벤트를 사용하여 추적된 데이터입니다.  값 형식으로 xml 요소에 저장 됩니다 \<항목 >\< 항목 이름 = "dataName" type = "> dataValue\<항목/>\<항목/>입니다.  추적 된 데이터가 없는 경우 문자열에 포함 되어 \<항목 / >입니다. ETW 이벤트 크기는 ETW 버퍼 크기 또는 ETW 이벤트의 최대 페이로드에 따라 제한됩니다. 이벤트 크기가 ETW 제한을 초과 하면 주석을 삭제 하 고 사용 하 여 데이터 값을 바꿔 이벤트 잘립니다 경우 \<항목 >... \<항목/>입니다.  ToString()에 의해 반환되는 값으로 string, char, bool, int, short, long, uint, ushort, ulong, System.Single, float, double, System.Guid, System.DateTimeOffset, System.DateTime 형식이 저장됩니다.  모든 다른 형식은 System.Runtime.Serialization.NetDataContractSerializer를 사용하여 serialize됩니다.|  
|주석|xs:string|이 이벤트에 추가된 주석입니다.  값 형식으로 xml 요소에 저장 됩니다 \<항목 >\< 항목 이름 = "annotationName" type = "> annotationValue\<항목/>\<항목/>입니다.  주석을 지정 하지 않으면 문자열을 포함 하는 경우 \<항목 / >입니다. ETW 이벤트 크기는 ETW 버퍼 크기 또는 ETW 이벤트의 최대 페이로드에 따라 제한됩니다. 이벤트 크기가 ETW 제한을 초과 하면 주석을 삭제 하 고 주석 값으로 바꿔 이벤트 잘립니다 경우 \<항목 >... \<항목/>입니다.|  
|ProfileName|xs:string|이 이벤트를 내보낸 이름 또는 추적 프로필|  
|HostReference|xs:string|웹 호스팅 서비스의 경우 이 필드는 웹 계층의 서비스를 고유하게 식별합니다.  형식은로 정의 됩니다 ' 웹 Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName' 예: ' 기본 웹 사이트/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'|  
|AppDomain|xs:string|AppDomain.CurrentDomain.FriendlyName에서 반환되는 문자열입니다.|
