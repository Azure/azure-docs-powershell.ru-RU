---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: c675a8da84e61b659c593cc1f963dd1b07c7f316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556475"
---
# <span data-ttu-id="87dfa-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="87dfa-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="87dfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="87dfa-103">Возвращает выходные данные, определенные в указанном задании Stream Analytics или выходных данных.</span><span class="sxs-lookup"><span data-stu-id="87dfa-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87dfa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87dfa-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87dfa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="87dfa-106">Командлет **Get-AzureRmStreamAnalyticsOutput** перечисляет все выходные данные, определенные в указанном задании Stream Analytics или получение сведений о конкретных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="87dfa-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="87dfa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87dfa-107">EXAMPLES</span></span>

### <span data-ttu-id="87dfa-108">Пример 1: получение сведений о выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="87dfa-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="87dfa-109">Эта команда возвращает сведения о выходных данных, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="87dfa-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="87dfa-110">Пример 2: получение сведений о конкретных выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="87dfa-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="87dfa-111">Эта команда возвращает сведения о выходных данных вывода, определенных в StreamingJob задания.</span><span class="sxs-lookup"><span data-stu-id="87dfa-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="87dfa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87dfa-112">PARAMETERS</span></span>

### <span data-ttu-id="87dfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87dfa-113">-DefaultProfile</span></span>
<span data-ttu-id="87dfa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87dfa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87dfa-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="87dfa-115">-JobName</span></span>
<span data-ttu-id="87dfa-116">Указывает имя задания Azure Stream Analytics, к которому относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="87dfa-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="87dfa-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87dfa-117">-Name</span></span>
<span data-ttu-id="87dfa-118">Указывает имя извлекаемых выходных данных Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="87dfa-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="87dfa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87dfa-119">-ResourceGroupName</span></span>
<span data-ttu-id="87dfa-120">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="87dfa-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="87dfa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87dfa-121">CommonParameters</span></span>
<span data-ttu-id="87dfa-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87dfa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87dfa-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87dfa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87dfa-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87dfa-124">INPUTS</span></span>

### <span data-ttu-id="87dfa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="87dfa-125">System.String</span></span>

## <span data-ttu-id="87dfa-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87dfa-126">OUTPUTS</span></span>

### <span data-ttu-id="87dfa-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="87dfa-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="87dfa-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="87dfa-128">NOTES</span></span>

## <span data-ttu-id="87dfa-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87dfa-129">RELATED LINKS</span></span>

[<span data-ttu-id="87dfa-130">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="87dfa-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="87dfa-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="87dfa-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="87dfa-132">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="87dfa-132">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


