---
title: '방법: 요소 컬렉션 검색(LINQ to XML)(C#)'
ms.date: 07/20/2015
ms.assetid: b849668c-7976-4974-b8e1-1cd587d34258
ms.openlocfilehash: 9ad75ce4d3ca113ed432d2b2351067babe33a74f
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43857066"
---
# <a name="how-to-retrieve-a-collection-of-elements-linq-to-xml-c"></a>방법: 요소 컬렉션 검색(LINQ to XML)(C#)
이 항목에서는 <xref:System.Xml.Linq.XContainer.Elements%2A> 메서드를 보여 줍니다. 이 메서드는 요소의 자식 요소 컬렉션을 검색합니다.  
  
## <a name="example"></a>예  
 이 예제에서는 `purchaseOrder` 요소의 자식 요소를 반복합니다.  
  
 이 예제에서는 XML 문서 [샘플 XML 파일: 일반적인 구매 주문(LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-linq-to-xml-1.md)을 사용합니다.  
  
```csharp  
XElement po = XElement.Load("PurchaseOrder.xml");  
IEnumerable<XElement> childElements =  
    from el in po.Elements()  
    select el;  
foreach (XElement el in childElements)  
    Console.WriteLine("Name: " + el.Name);  
```  
  
 이 예제의 결과는 다음과 같습니다.  
  
```  
Name: Address  
Name: Address  
Name: DeliveryNotes  
Name: Items  
```  
  
## <a name="see-also"></a>참고 항목

- [LINQ to XML 축(C#)](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-axes.md)
