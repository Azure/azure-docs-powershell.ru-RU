---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: d4ec2865f0a0efcc4a306d0614df1c27adddc5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568109"
---
# <span data-ttu-id="3aad9-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3aad9-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="3aad9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3aad9-102">SYNOPSIS</span></span>
<span data-ttu-id="3aad9-103">Остановка задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="3aad9-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aad9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3aad9-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aad9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aad9-105">DESCRIPTION</span></span>
<span data-ttu-id="3aad9-106">Командлет **Stop-AzureRmStreamAnalyticsJob** асинхронно останавливает выполнение задания Stream Analytics в Azure и освобождает ресурсы, которые использовались.</span><span class="sxs-lookup"><span data-stu-id="3aad9-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="3aad9-107">Определение задания и метаданные остаются доступными в рамках подписки через API портала и управления Azure, что позволяет редактировать и перезапускать задание.</span><span class="sxs-lookup"><span data-stu-id="3aad9-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="3aad9-108">Вы не будете платить за задание в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="3aad9-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="3aad9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3aad9-109">EXAMPLES</span></span>

### <span data-ttu-id="3aad9-110">Пример 1: Остановка выполняющегося задания</span><span class="sxs-lookup"><span data-stu-id="3aad9-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="3aad9-111">Эта команда останавливает задачу StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="3aad9-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="3aad9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3aad9-112">PARAMETERS</span></span>

### <span data-ttu-id="3aad9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aad9-113">-DefaultProfile</span></span>
<span data-ttu-id="3aad9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3aad9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aad9-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3aad9-115">-Name</span></span>
<span data-ttu-id="3aad9-116">Указывает имя задания Azure Stream Analytics, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="3aad9-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="3aad9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aad9-117">-ResourceGroupName</span></span>
<span data-ttu-id="3aad9-118">Указывает имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="3aad9-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="3aad9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aad9-119">CommonParameters</span></span>
<span data-ttu-id="3aad9-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3aad9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aad9-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aad9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aad9-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3aad9-122">INPUTS</span></span>

### <span data-ttu-id="3aad9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3aad9-123">System.String</span></span>

## <span data-ttu-id="3aad9-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aad9-124">OUTPUTS</span></span>

### <span data-ttu-id="3aad9-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3aad9-125">System.Boolean</span></span>

## <span data-ttu-id="3aad9-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3aad9-126">NOTES</span></span>

## <span data-ttu-id="3aad9-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3aad9-127">RELATED LINKS</span></span>

[<span data-ttu-id="3aad9-128">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3aad9-128">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3aad9-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3aad9-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3aad9-130">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3aad9-130">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3aad9-131">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3aad9-131">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3aad9-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3aad9-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


