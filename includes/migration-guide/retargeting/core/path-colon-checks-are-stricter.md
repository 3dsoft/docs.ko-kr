### <a name="path-colon-checks-are-stricter"></a><span data-ttu-id="542fe-101">경로 콜론 검사가 더욱 엄격해짐</span><span class="sxs-lookup"><span data-stu-id="542fe-101">Path colon checks are stricter</span></span>

|   |   |
|---|---|
|<span data-ttu-id="542fe-102">설명</span><span class="sxs-lookup"><span data-stu-id="542fe-102">Details</span></span>|<span data-ttu-id="542fe-103">.NET Framework 4.6.2에서 이전에 지원되지 않던 경로(길이 및 형식 모두)를 지원하도록 여러 가지가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="542fe-103">In .NET Framework 4.6.2, a number of changes were made to support previously unsupported paths (both in length and format).</span></span> <span data-ttu-id="542fe-104">적절한 드라이브 구분 기호(콜론) 구문에 대해 검사가 좀 더 정확해졌습니다. 이 구문은 허용되었던 일부 선택 경로 API에서 일부 URI 경로가 차단되는 부작용이 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="542fe-104">Checks for proper drive separator (colon) syntax were made more correct, which had the side effect of blocking some URI paths in a few select Path APIs where they used to be tolerated.</span></span>|
|<span data-ttu-id="542fe-105">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="542fe-105">Suggestion</span></span>|<span data-ttu-id="542fe-106">영향을 받는 API로 URI를 전달하는 경우 먼저 합법적인 경로가 되도록 문자열을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="542fe-106">If passing a URI to affected APIs, modify the string to be a legal path first.</span></span><ul><li><span data-ttu-id="542fe-107">URL에서 스키마를 수동으로 제거합니다(예: URL에서 <code>file://</code> 제거).</span><span class="sxs-lookup"><span data-stu-id="542fe-107">Remove the scheme from URLs manually (e.g. remove <code>file://</code> from URLs)</span></span></li><li><span data-ttu-id="542fe-108">URI를 <xref:System.Uri> 클래스에 전달하고 <xref:System.Uri.LocalPath>를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="542fe-108">Pass the URI to the <xref:System.Uri> class and use <xref:System.Uri.LocalPath></span></span></li></ul><span data-ttu-id="542fe-109">또는 <code>Switch.System.IO.UseLegacyPathHandling</code> AppContext 스위치를 true로 설정하여 새 경로 정규화를 옵트아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="542fe-109">Alternatively, you can opt out of the new path normalization by setting the <code>Switch.System.IO.UseLegacyPathHandling</code> AppContext switch to true.</span></span>|
|<span data-ttu-id="542fe-110">범위</span><span class="sxs-lookup"><span data-stu-id="542fe-110">Scope</span></span>|<span data-ttu-id="542fe-111">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="542fe-111">Edge</span></span>|
|<span data-ttu-id="542fe-112">버전</span><span class="sxs-lookup"><span data-stu-id="542fe-112">Version</span></span>|<span data-ttu-id="542fe-113">4.6.2</span><span class="sxs-lookup"><span data-stu-id="542fe-113">4.6.2</span></span>|
|<span data-ttu-id="542fe-114">형식</span><span class="sxs-lookup"><span data-stu-id="542fe-114">Type</span></span>|<span data-ttu-id="542fe-115">대상 변경</span><span class="sxs-lookup"><span data-stu-id="542fe-115">Retargeting</span></span>|
|<span data-ttu-id="542fe-116">영향을 받는 API</span><span class="sxs-lookup"><span data-stu-id="542fe-116">Affected APIs</span></span>|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|
