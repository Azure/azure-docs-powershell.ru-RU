---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 20bd934a35fdf0cf907e83f22c8148fdfe5425db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568112"
---
# <span data-ttu-id="42c7a-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42c7a-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="42c7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="42c7a-103">Запускает задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42c7a-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42c7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42c7a-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42c7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="42c7a-106">Командлет **Start-AzureRmStreamAnalyticsJob** выполняет асинхронное развертывание и запуск задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="42c7a-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="42c7a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42c7a-107">EXAMPLES</span></span>

### <span data-ttu-id="42c7a-108">Пример 1: запуск задания Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="42c7a-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="42c7a-109">Эта команда запускает задание StreamingJob и указывает на то, что поток событий вывода должен начинаться с метки времени 2014 — 07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="42c7a-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="42c7a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42c7a-110">PARAMETERS</span></span>

### <span data-ttu-id="42c7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c7a-111">-DefaultProfile</span></span>
<span data-ttu-id="42c7a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42c7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42c7a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42c7a-113">-Name</span></span>
<span data-ttu-id="42c7a-114">Указывает имя задания Azure Stream Analytics, которое нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="42c7a-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="42c7a-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="42c7a-115">-OutputStartMode</span></span>
<span data-ttu-id="42c7a-116">Задает режим запуска для задания.</span><span class="sxs-lookup"><span data-stu-id="42c7a-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="42c7a-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="42c7a-117">Valid values are:</span></span> 
- <span data-ttu-id="42c7a-118">JobStartTime — это значение указывает на то, что начальная точка потока событий вывода должна начинаться при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="42c7a-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="42c7a-119">CustomTime — это значение указывает на то, что начальная точка потока событий вывода должна начинаться с настраиваемого времени, указанного в параметре *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="42c7a-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="42c7a-120">--LastOutputEventTime — это значение указывает на то, что начальная точка потока событий вывода должна начинаться с момента вывода последнего события.</span><span class="sxs-lookup"><span data-stu-id="42c7a-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="42c7a-121">Если свойство отсутствует, по умолчанию используется значение JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="42c7a-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="42c7a-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="42c7a-122">-OutputStartTime</span></span>
<span data-ttu-id="42c7a-123">Задает время начала вывода.</span><span class="sxs-lookup"><span data-stu-id="42c7a-123">Specifies the output start time.</span></span>
<span data-ttu-id="42c7a-124">Это значение является либо отформатированной отметкой времени ISO-8601, обозначающей начальную точку потока событий вывода, либо $Null, чтобы указать, что поток событий будет начинаться при запуске потокового задания.</span><span class="sxs-lookup"><span data-stu-id="42c7a-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="42c7a-125">Это свойство должно иметь значение, если *OutputStartMode* имеет значение CustomTime.</span><span class="sxs-lookup"><span data-stu-id="42c7a-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c7a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c7a-126">-ResourceGroupName</span></span>
<span data-ttu-id="42c7a-127">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42c7a-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="42c7a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c7a-128">CommonParameters</span></span>
<span data-ttu-id="42c7a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42c7a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c7a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c7a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c7a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42c7a-131">INPUTS</span></span>

### <span data-ttu-id="42c7a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="42c7a-132">System.String</span></span>

### <span data-ttu-id="42c7a-133">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="42c7a-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="42c7a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42c7a-134">OUTPUTS</span></span>

### <span data-ttu-id="42c7a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42c7a-135">System.Boolean</span></span>

## <span data-ttu-id="42c7a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="42c7a-136">NOTES</span></span>

## <span data-ttu-id="42c7a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42c7a-137">RELATED LINKS</span></span>

[<span data-ttu-id="42c7a-138">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42c7a-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="42c7a-139">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42c7a-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="42c7a-140">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42c7a-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="42c7a-141">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42c7a-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


