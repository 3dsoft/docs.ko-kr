---
title: '|| 연산자(C# 참조)'
ms.date: 11/06/2018
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: a391078372e4ec0a3882bed4515733adedffb547
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2018
ms.locfileid: "42925542"
---
# <a name="-operator-c-reference"></a>|| 연산자(C# 참조)

"단락(short-circuiting)" 논리 OR 연산자로도 알려져 있는 조건부 논리 OR 연산자 `||`는 [bool](../keywords/bool.md) 피연산자의 논리 OR을 계산합니다. `x` 또는 `y`가 `true`로 평가되면 `x || y`의 결과는 `true`입니다. 그렇지 않으면 결과는 `false`입니다. 첫 번째 피연산자가 `true`로 평가되면 두 번째 피연산자는 평가되지 않고 작업 결과는 `true`입니다. 다음 예제에서는 해당 동작을 보여줍니다.

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#Or)]

[논리 OR 연산자](or-operator.md) `|`도 해당 `bool` 피연산자의 논리 OR을 계산하지만 항상 두 피연산자를 평가합니다.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식으로 조건부 논리 OR 연산자를 오버로드할 수 없습니다. 그러나 사용자 정의 형식이 특정 방식으로 [논리 OR](or-operator.md), [true](../keywords/true-operator.md) 및 [false](../keywords/false-operator.md) 연산자를 오버로드하는 경우 `||` 작업은 해당 형식의 피연산자에 대해 평가할 수 있습니다. 자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [사용자 정의 조건부 논리 연산자](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) 섹션을 참조하세요.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [조건부 논리 연산자](~/_csharplang/spec/expressions.md#conditional-logical-operators) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [&& 연산자](conditional-and-operator.md)
- [! 연산자](logical-negation-operator.md)
- [| 연산자](or-operator.md)
