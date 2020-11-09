---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317540"
---
# <span data-ttu-id="92b75-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92b75-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="92b75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92b75-102">SYNOPSIS</span></span>
<span data-ttu-id="92b75-103">Остановка задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="92b75-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="92b75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92b75-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92b75-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92b75-105">DESCRIPTION</span></span>
<span data-ttu-id="92b75-106">Командлет **Stop-AzStreamAnalyticsJob** асинхронно останавливает выполнение задания Stream Analytics в Azure и освобождает ресурсы, которые использовались.</span><span class="sxs-lookup"><span data-stu-id="92b75-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="92b75-107">Определение задания и метаданные остаются доступными в рамках подписки через API портала и управления Azure, что позволяет редактировать и перезапускать задание.</span><span class="sxs-lookup"><span data-stu-id="92b75-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="92b75-108">Вы не будете платить за задание в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="92b75-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="92b75-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92b75-109">EXAMPLES</span></span>

### <span data-ttu-id="92b75-110">Пример 1: Остановка выполняющегося задания</span><span class="sxs-lookup"><span data-stu-id="92b75-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="92b75-111">Эта команда останавливает задачу StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="92b75-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="92b75-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92b75-112">PARAMETERS</span></span>

### <span data-ttu-id="92b75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b75-113">-DefaultProfile</span></span>
<span data-ttu-id="92b75-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92b75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b75-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92b75-115">-Name</span></span>
<span data-ttu-id="92b75-116">Указывает имя задания Azure Stream Analytics, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="92b75-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="92b75-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b75-117">-ResourceGroupName</span></span>
<span data-ttu-id="92b75-118">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="92b75-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="92b75-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b75-119">CommonParameters</span></span>
<span data-ttu-id="92b75-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92b75-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b75-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b75-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b75-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92b75-122">INPUTS</span></span>

### <span data-ttu-id="92b75-123">System. String</span><span class="sxs-lookup"><span data-stu-id="92b75-123">System.String</span></span>

## <span data-ttu-id="92b75-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92b75-124">OUTPUTS</span></span>

### <span data-ttu-id="92b75-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92b75-125">System.Boolean</span></span>

## <span data-ttu-id="92b75-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="92b75-126">NOTES</span></span>

## <span data-ttu-id="92b75-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92b75-127">RELATED LINKS</span></span>

[<span data-ttu-id="92b75-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92b75-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92b75-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92b75-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92b75-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92b75-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92b75-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92b75-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="92b75-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="92b75-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


