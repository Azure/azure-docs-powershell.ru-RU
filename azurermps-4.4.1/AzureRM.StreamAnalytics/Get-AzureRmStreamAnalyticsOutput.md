---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 21c4cf10fc6464b3db5bcb999d1f477c2e73840e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732557"
---
# <span data-ttu-id="b5925-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b5925-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="b5925-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5925-102">SYNOPSIS</span></span>
<span data-ttu-id="b5925-103">Возвращает выходные данные, определенные в указанном задании Stream Analytics или выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b5925-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5925-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5925-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5925-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5925-105">DESCRIPTION</span></span>
<span data-ttu-id="b5925-106">Командлет **Get-AzureRmStreamAnalyticsOutput** перечисляет все выходные данные, определенные в указанном задании Stream Analytics или получение сведений о конкретных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b5925-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="b5925-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5925-107">EXAMPLES</span></span>

### <span data-ttu-id="b5925-108">Пример 1: получение сведений о выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="b5925-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="b5925-109">Эта команда возвращает сведения о выходных данных, определенных для задания StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b5925-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="b5925-110">Пример 2: получение сведений о конкретных выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="b5925-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="b5925-111">Эта команда возвращает сведения о выходных данных вывода, определенных в StreamingJob задания.</span><span class="sxs-lookup"><span data-stu-id="b5925-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="b5925-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5925-112">PARAMETERS</span></span>

### <span data-ttu-id="b5925-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b5925-113">-JobName</span></span>
<span data-ttu-id="b5925-114">Указывает имя задания Azure Stream Analytics, к которому относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b5925-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b5925-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5925-115">-Name</span></span>
<span data-ttu-id="b5925-116">Указывает имя извлекаемых выходных данных Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b5925-116">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="b5925-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5925-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5925-118">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b5925-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b5925-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5925-119">-DefaultProfile</span></span>
<span data-ttu-id="b5925-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5925-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5925-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5925-121">CommonParameters</span></span>
<span data-ttu-id="b5925-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5925-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5925-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5925-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5925-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5925-124">INPUTS</span></span>

## <span data-ttu-id="b5925-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5925-125">OUTPUTS</span></span>

### <span data-ttu-id="b5925-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="b5925-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="b5925-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5925-127">NOTES</span></span>

## <span data-ttu-id="b5925-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5925-128">RELATED LINKS</span></span>

[<span data-ttu-id="b5925-129">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b5925-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b5925-130">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b5925-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="b5925-131">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b5925-131">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


