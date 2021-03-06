---
title: '방법: 여러 원본 (LINQ) (Visual Basic)에서 개체 컬렉션 채우기'
ms.date: 06/22/2018
ms.assetid: 63062a22-e6a9-42c0-b357-c7c965f58f33
ms.openlocfilehash: 6560f853874f9b9a9aeb53bd0678540004fdfcc1
ms.sourcegitcommit: 9e18e4a18284ae9e54c515e30d019c0bbff9cd37
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37070865"
---
# <a name="how-to-populate-object-collections-from-multiple-sources-linq-visual-basic"></a>방법: 여러 원본 (LINQ) (Visual Basic)에서 개체 컬렉션 채우기

이 예제에서는 여러 소스의 데이터를 새 형식의 시퀀스에 병합하는 방법을 보여 줍니다.

> [!NOTE]
> 메모리 내 데이터 또는 데이터는 데이터베이스에 여전히 데이터와 파일 시스템에 연결 하지 마세요. 이러한 도메인 간 조인을 사용하면 데이터베이스 쿼리 및 다른 소스 유형에 대해 조인 작업이 정의될 수 있는 다양한 방법으로 인해 정의되지 않은 결과가 발생할 수 있습니다. 또한 데이터베이스의 데이터 양이 충분히 큰 경우 이러한 작업으로 인해 메모리 부족 예외가 발생할 수 있는 위험이 있습니다. 데이터베이스의 데이터를 메모리 내 데이터에 조인하려면 먼저 데이터베이스 쿼리에서 `ToList` 또는 `ToArray`를 호출한 다음 반환된 컬렉션에서 조인을 수행합니다.

## <a name="to-create-the-data-file"></a>데이터 파일을 만들려면

- 에 설명 된 대로 names.csv 및 scores.csv 파일을 프로젝트 폴더에 복사 [하는 방법: 콘텐츠 조인에서 서로 다른 파일 (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-join-content-from-dissimilar-files-linq.md)합니다.

## <a name="example"></a>예

다음 예제에서는 명명된 형식 `Student`를 사용하여 스프레드시트 데이터를 시뮬레이트하는 두 개의 메모리 내 문자열 컬렉션의 병합된 데이터를 .csv 형식으로 저장하는 방법을 보여 줍니다. 첫 번째 문자열 컬렉션은 학생 이름과 ID를 나타내고, 두 번째 컬렉션은 학생 ID(첫 번째 열)와 4개의 시험 점수를 나타냅니다. ID는 외래 키로 사용됩니다.

```vb
Imports System.Collections.Generic
Imports System.Linq

Class Student
    Public FirstName As String
    Public LastName As String
    Public ID As Integer
    Public ExamScores As List(Of Integer)
End Class

Class PopulateCollection

    Shared Sub Main()

        ' Merge content from spreadsheets into a list of Student objects.

        ' These data files are defined in How to: Join Content from
        ' Dissimilar Files (LINQ).

        ' Each line of names.csv consists of a last name, a first name, and an
        ' ID number, separated by commas. For example, Omelchenko,Svetlana,111
        Dim names As String() = System.IO.File.ReadAllLines("../../../names.csv")

        ' Each line of scores.csv consists of an ID number and four test
        ' scores, separated by commas. For example, 111, 97, 92, 81, 60
        Dim scores As String() = System.IO.File.ReadAllLines("../../../scores.csv")

        ' The following query merges the content of two dissimilar spreadsheets
        ' based on common ID values.
        ' Multiple From clauses are used instead of a Join clause
        ' in order to store the results of scoreLine.Split.
        ' Note the dynamic creation of a list of integers for the
        ' ExamScores member. The first item is skipped in the split string
        ' because it is the student ID, not an exam score.
        Dim queryNamesScores = From nameLine In names
                          Let splitName = nameLine.Split(New Char() {","})
                          From scoreLine In scores
                          Let splitScoreLine = scoreLine.Split(New Char() {","})
                          Where Convert.ToInt32(splitName(2)) = Convert.ToInt32(splitScoreLine(0))
                          Select New Student() With {
                               .FirstName = splitName(0), .LastName = splitName(1), .ID = splitName(2),
                               .ExamScores = (From scoreAsText In splitScoreLine Skip 1
                                             Select Convert.ToInt32(scoreAsText)).ToList()}

        ' Optional. Store the query results for faster access in future
        ' queries. This could be useful with very large data files.
        Dim students As List(Of Student) = queryNamesScores.ToList()

        ' Display each student's name and exam score average.
        For Each s In students
            Console.WriteLine("The average score of " & s.FirstName & " " &
                              s.LastName & " is " & s.ExamScores.Average())
        Next

        ' Keep console window open in debug mode.
        Console.WriteLine("Press any key to exit.")
        Console.ReadKey()
    End Sub
End Class

' Output:
' The average score of Omelchenko Svetlana is 82.5
' The average score of O'Donnell Claire is 72.25
' The average score of Mortensen Sven is 84.5
' The average score of Garcia Cesar is 88.25
' The average score of Garcia Debra is 67
' The average score of Fakhouri Fadi is 92.25
' The average score of Feng Hanying is 88
' The average score of Garcia Hugo is 85.75
' The average score of Tucker Lance is 81.75
' The average score of Adams Terry is 85.25
' The average score of Zabokritski Eugene is 83
' The average score of Tucker Michael is 92
```

에 [Select 절](../../../../visual-basic/language-reference/queries/select-clause.md) 절, 개체 이니셜라이저는 인스턴스화하는 데 사용할 각 새로운 `Student` 두 소스의 데이터를 사용 하 여 개체입니다.

쿼리의 결과 저장할 수 없다면 익명 형식 명명 된 형식 보다 더 편리할 수 있습니다. 명명된 형식은 쿼리가 실행되는 메서드 외부로 쿼리 결과를 전달하는 경우에 필요합니다. 다음 예제는 앞의 예제와 동일한 작업을 수행하지만 명명된 형식 대신 무명 형식을 사용합니다.

```vb
' Merge the data by using an anonymous type.
' Note the dynamic creation of a list of integers for the
' ExamScores member. We skip 1 because the first string
' in the array is the student ID, not an exam score.
Dim queryNamesScores2 =
    From nameLine In names
    Let splitName = nameLine.Split(New Char() {","})
    From scoreLine In scores
    Let splitScoreLine = scoreLine.Split(New Char() {","})
    Where Convert.ToInt32(splitName(2)) = Convert.ToInt32(splitScoreLine(0))
    Select New With
           {.Last = splitName(0),
            .First = splitName(1),
            .ExamScores = (From scoreAsText In splitScoreLine Skip 1
                           Select Convert.ToInt32(scoreAsText)).ToList()}

' Display each student's name and exam score average.
For Each s In queryNamesScores2
    Console.WriteLine("The average score of " & s.First & " " &
                      s.Last & " is " & s.ExamScores.Average())
Next
```

## <a name="compiling-the-code"></a>코드 컴파일

만들기 하 고 다음 옵션 중 하나를 대상으로 하는 프로젝트를 컴파일하십시오.

- .NET framework 버전 3.5 System.Core.dll에 대 한 참조입니다.
- .NET framework 버전 4.0 이상이 합니다.
- .NET core 버전 1.0 이상이 있습니다.

## <a name="see-also"></a>참고자료

[LINQ 및 문자열 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-and-strings.md)
