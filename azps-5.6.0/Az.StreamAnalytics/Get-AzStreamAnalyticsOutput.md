---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973859"
---
# <span data-ttu-id="b775f-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b775f-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="b775f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b775f-102">SYNOPSIS</span></span>
<span data-ttu-id="b775f-103">Возвращает выходные данные, определенные в указанном заданиях или выходных данных средства аналитики Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b775f-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="b775f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b775f-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b775f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b775f-105">DESCRIPTION</span></span>
<span data-ttu-id="b775f-106">В **этом cmdlet** выведется список всех выходных данных, определенных в указанном заданиях аналитики Stream, или сведения о конкретном выходе.</span><span class="sxs-lookup"><span data-stu-id="b775f-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="b775f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b775f-107">EXAMPLES</span></span>

### <span data-ttu-id="b775f-108">Пример 1. Просмотр сведений о выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="b775f-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="b775f-109">Эта команда возвращает сведения о выходных данных, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b775f-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="b775f-110">Пример 2. Просмотр сведений о выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="b775f-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="b775f-111">Эта команда возвращает сведения о выходных данных с именем Output, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b775f-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="b775f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b775f-112">PARAMETERS</span></span>

### <span data-ttu-id="b775f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b775f-113">-DefaultProfile</span></span>
<span data-ttu-id="b775f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b775f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b775f-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="b775f-115">-JobName</span></span>
<span data-ttu-id="b775f-116">Указывает имя задания Azure Stream Analytics, к которому относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b775f-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b775f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b775f-117">-Name</span></span>
<span data-ttu-id="b775f-118">Указывает имя результата Azure Stream Analytics, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="b775f-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="b775f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b775f-119">-ResourceGroupName</span></span>
<span data-ttu-id="b775f-120">Имя группы ресурсов, к которой относится выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b775f-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b775f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b775f-121">CommonParameters</span></span>
<span data-ttu-id="b775f-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b775f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b775f-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b775f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b775f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b775f-124">INPUTS</span></span>

### <span data-ttu-id="b775f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b775f-125">System.String</span></span>

## <span data-ttu-id="b775f-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b775f-126">OUTPUTS</span></span>

### <span data-ttu-id="b775f-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="b775f-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="b775f-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b775f-128">NOTES</span></span>

## <span data-ttu-id="b775f-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b775f-129">RELATED LINKS</span></span>

[<span data-ttu-id="b775f-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b775f-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="b775f-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b775f-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="b775f-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b775f-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


