---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: a2f20aa2c372261fe8f36599884c516563170293
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217081"
---
# <span data-ttu-id="9945b-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9945b-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="9945b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9945b-102">SYNOPSIS</span></span>
<span data-ttu-id="9945b-103">Возвращает выходные данные, определенные в указанном заданиях или выходных данных Средства аналитики Stream.</span><span class="sxs-lookup"><span data-stu-id="9945b-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="9945b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9945b-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9945b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9945b-105">DESCRIPTION</span></span>
<span data-ttu-id="9945b-106">В **этом cmdlet** выведется список всех выходных данных, определенных в указанном заданиях аналитики StreamAnalytics или которые получают сведения о конкретном выходе.</span><span class="sxs-lookup"><span data-stu-id="9945b-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="9945b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9945b-107">EXAMPLES</span></span>

### <span data-ttu-id="9945b-108">Пример 1. Просмотр сведений о выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="9945b-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="9945b-109">Эта команда возвращает сведения о выходных данных, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9945b-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="9945b-110">Пример 2. Просмотр сведений о конкретных результатах задания</span><span class="sxs-lookup"><span data-stu-id="9945b-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="9945b-111">Эта команда возвращает сведения о выходных данных с именем Output, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9945b-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="9945b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9945b-112">PARAMETERS</span></span>

### <span data-ttu-id="9945b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9945b-113">-DefaultProfile</span></span>
<span data-ttu-id="9945b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9945b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9945b-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="9945b-115">-JobName</span></span>
<span data-ttu-id="9945b-116">Указывает имя задания Azure Stream Analytics, к которому относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9945b-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9945b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9945b-117">-Name</span></span>
<span data-ttu-id="9945b-118">Указывает имя результата Azure Stream Analytics, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="9945b-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9945b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9945b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9945b-120">Имя группы ресурсов, к которой относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9945b-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9945b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9945b-121">CommonParameters</span></span>
<span data-ttu-id="9945b-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9945b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9945b-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9945b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9945b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9945b-124">INPUTS</span></span>

### <span data-ttu-id="9945b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9945b-125">System.String</span></span>

## <span data-ttu-id="9945b-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9945b-126">OUTPUTS</span></span>

### <span data-ttu-id="9945b-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="9945b-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="9945b-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9945b-128">NOTES</span></span>

## <span data-ttu-id="9945b-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9945b-129">RELATED LINKS</span></span>

[<span data-ttu-id="9945b-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9945b-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9945b-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9945b-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9945b-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9945b-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


