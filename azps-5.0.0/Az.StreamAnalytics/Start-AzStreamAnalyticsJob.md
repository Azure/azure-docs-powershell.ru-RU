---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247153"
---
# <span data-ttu-id="0c5ff-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c5ff-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="0c5ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5ff-103">Запускает задание Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="0c5ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c5ff-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c5ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5ff-106">Командлет **Start-AzStreamAnalyticsJob** выполняет асинхронное развертывание и запуск задания Stream Analytics в Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="0c5ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5ff-108">Пример 1: запуск задания Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="0c5ff-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="0c5ff-109">Эта команда запускает задание StreamingJob и указывает на то, что поток событий вывода должен начинаться с метки времени 2014 — 07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="0c5ff-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c5ff-110">PARAMETERS</span></span>

### <span data-ttu-id="0c5ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5ff-111">-DefaultProfile</span></span>
<span data-ttu-id="0c5ff-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5ff-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c5ff-113">-Name</span></span>
<span data-ttu-id="0c5ff-114">Указывает имя задания Azure Stream Analytics, которое нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="0c5ff-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="0c5ff-115">-OutputStartMode</span></span>
<span data-ttu-id="0c5ff-116">Задает режим запуска для задания.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="0c5ff-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="0c5ff-117">Valid values are:</span></span> 
- <span data-ttu-id="0c5ff-118">JobStartTime — это значение указывает на то, что начальная точка потока событий вывода должна начинаться при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="0c5ff-119">CustomTime — это значение указывает на то, что начальная точка потока событий вывода должна начинаться с настраиваемого времени, указанного в параметре *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="0c5ff-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="0c5ff-120">LastOutputEventTime — это значение указывает на то, что начальная точка потока событий вывода должна начинаться с момента вывода последнего события.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="0c5ff-121">Если свойство отсутствует, по умолчанию используется значение JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="0c5ff-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="0c5ff-122">-OutputStartTime</span></span>
<span data-ttu-id="0c5ff-123">Задает время начала вывода.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-123">Specifies the output start time.</span></span>
<span data-ttu-id="0c5ff-124">Это значение является либо отформатированной отметкой времени ISO-8601, обозначающей начальную точку потока событий вывода, либо $Null, чтобы указать, что поток событий будет начинаться при запуске потокового задания.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="0c5ff-125">Это свойство должно иметь значение, если *OutputStartMode* имеет значение CustomTime.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="0c5ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c5ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c5ff-127">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="0c5ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5ff-128">CommonParameters</span></span>
<span data-ttu-id="0c5ff-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c5ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5ff-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5ff-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5ff-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c5ff-131">INPUTS</span></span>

### <span data-ttu-id="0c5ff-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0c5ff-132">System.String</span></span>

### <span data-ttu-id="0c5ff-133">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0c5ff-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0c5ff-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c5ff-134">OUTPUTS</span></span>

### <span data-ttu-id="0c5ff-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c5ff-135">System.Boolean</span></span>

## <span data-ttu-id="0c5ff-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c5ff-136">NOTES</span></span>

## <span data-ttu-id="0c5ff-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c5ff-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c5ff-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c5ff-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="0c5ff-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c5ff-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="0c5ff-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c5ff-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="0c5ff-141">Остановить-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c5ff-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


