---
title: 기계 학습 처리를 위해 여러 파일의 데이터 로드 - ML.NET
description: ML.NET를 사용하여 기계 학습 모델을 빌드하고, 학습하고, 점수를 매기는 데 사용할 여러 파일의 데이터를 로드하는 방법 알아보기
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: c9b34bd6bcbac62e9f9c33226f5d0feb41168392
ms.sourcegitcommit: 7f7664837d35320a0bad3f7e4ecd68d6624633b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/30/2018
ms.locfileid: "52672411"
---
# <a name="load-data-from-multiple-files-for-machine-learning-processing---mlnet"></a>기계 학습 처리를 위해 여러 파일의 데이터 로드 - ML.NET

`TextLoader`를 사용하고, `Read` 메서드에 대한 파일의 배열을 지정합니다. 파일에는 동일한 스키마(동일한 번호 및 열 형식)가 포함되어야 합니다.

* [예제 파일1](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.train)
* [예제 파일2](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.test)

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.TextReader(new TextLoader.Arguments
{
    Column = new[] {
        // A boolean column depicting the 'label'.
        new TextLoader.Column("IsOver50k", DataKind.BL, 0),
        // Three text columns.
        new TextLoader.Column("Workclass", DataKind.TX, 1),
        new TextLoader.Column("Education", DataKind.TX, 2),
        new TextLoader.Column("MaritalStatus", DataKind.TX, 3)
    },
    // First line of the file is a header, not a data row.
    HasHeader = true
});

var data = reader.Read(exampleFile1, exampleFile2);
```