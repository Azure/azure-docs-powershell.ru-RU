---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 050bfccef2b6286ef45a96a9feedc99ef4745115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905205"
---
# <span data-ttu-id="1fa31-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1fa31-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="1fa31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fa31-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa31-103">Остановка задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1fa31-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="1fa31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fa31-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fa31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fa31-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa31-106">Командлет **Stop-AzStreamAnalyticsJob** асинхронно останавливает выполнение задания Stream Analytics в Azure и освобождает ресурсы, которые использовались.</span><span class="sxs-lookup"><span data-stu-id="1fa31-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="1fa31-107">Определение задания и метаданные остаются доступными в рамках подписки через API портала и управления Azure, что позволяет редактировать и перезапускать задание.</span><span class="sxs-lookup"><span data-stu-id="1fa31-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="1fa31-108">Вы не будете платить за задание в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1fa31-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="1fa31-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fa31-109">EXAMPLES</span></span>

### <span data-ttu-id="1fa31-110">Пример 1: Остановка выполняющегося задания</span><span class="sxs-lookup"><span data-stu-id="1fa31-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="1fa31-111">Эта команда останавливает задачу StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="1fa31-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="1fa31-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fa31-112">PARAMETERS</span></span>

### <span data-ttu-id="1fa31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa31-113">-DefaultProfile</span></span>
<span data-ttu-id="1fa31-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fa31-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fa31-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fa31-115">-Name</span></span>
<span data-ttu-id="1fa31-116">Указывает имя задания Azure Stream Analytics, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="1fa31-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="1fa31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa31-117">-ResourceGroupName</span></span>
<span data-ttu-id="1fa31-118">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1fa31-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="1fa31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa31-119">CommonParameters</span></span>
<span data-ttu-id="1fa31-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fa31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa31-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa31-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa31-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fa31-122">INPUTS</span></span>

### <span data-ttu-id="1fa31-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1fa31-123">System.String</span></span>

## <span data-ttu-id="1fa31-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fa31-124">OUTPUTS</span></span>

### <span data-ttu-id="1fa31-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fa31-125">System.Boolean</span></span>

## <span data-ttu-id="1fa31-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fa31-126">NOTES</span></span>

## <span data-ttu-id="1fa31-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fa31-127">RELATED LINKS</span></span>

[<span data-ttu-id="1fa31-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1fa31-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1fa31-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1fa31-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1fa31-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1fa31-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1fa31-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1fa31-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1fa31-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1fa31-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


