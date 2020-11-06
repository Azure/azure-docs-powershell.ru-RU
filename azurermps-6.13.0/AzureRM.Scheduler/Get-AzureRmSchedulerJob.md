---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 89c4a6bd9d009456c97aa246f608c1920c27c823
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568392"
---
# <span data-ttu-id="1d41b-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="1d41b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d41b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d41b-103">Получает задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="1d41b-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d41b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d41b-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d41b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d41b-105">DESCRIPTION</span></span>
<span data-ttu-id="1d41b-106">Командлет **Get-AzureRmSchedulerJob** получает задания планировщика Azure.</span><span class="sxs-lookup"><span data-stu-id="1d41b-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="1d41b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d41b-107">EXAMPLES</span></span>

## <span data-ttu-id="1d41b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d41b-108">PARAMETERS</span></span>

### <span data-ttu-id="1d41b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d41b-109">-DefaultProfile</span></span>
<span data-ttu-id="1d41b-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d41b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d41b-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1d41b-111">-JobCollectionName</span></span>
<span data-ttu-id="1d41b-112">Указывает имя коллекции заданий, содержащей задания, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1d41b-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d41b-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1d41b-113">-JobName</span></span>
<span data-ttu-id="1d41b-114">Указывает имя задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1d41b-114">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d41b-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="1d41b-115">-JobState</span></span>
<span data-ttu-id="1d41b-116">Указывает состояние задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1d41b-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="1d41b-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1d41b-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d41b-118">Включаем</span><span class="sxs-lookup"><span data-stu-id="1d41b-118">Enabled</span></span> 
- <span data-ttu-id="1d41b-119">Отключает</span><span class="sxs-lookup"><span data-stu-id="1d41b-119">Disabled</span></span> 
- <span data-ttu-id="1d41b-120">Сбой</span><span class="sxs-lookup"><span data-stu-id="1d41b-120">Faulted</span></span> 
- <span data-ttu-id="1d41b-121">Completed</span><span class="sxs-lookup"><span data-stu-id="1d41b-121">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d41b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d41b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1d41b-123">Указывает группу ресурсов, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1d41b-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d41b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d41b-124">CommonParameters</span></span>
<span data-ttu-id="1d41b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d41b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d41b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d41b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d41b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d41b-127">INPUTS</span></span>

### <span data-ttu-id="1d41b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1d41b-128">System.String</span></span>

## <span data-ttu-id="1d41b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d41b-129">OUTPUTS</span></span>

### <span data-ttu-id="1d41b-130">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1d41b-130">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="1d41b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d41b-131">NOTES</span></span>

## <span data-ttu-id="1d41b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d41b-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d41b-133">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-133">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="1d41b-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1d41b-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1d41b-135">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-135">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="1d41b-136">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-136">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="1d41b-137">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-137">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="1d41b-138">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-138">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="1d41b-139">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-139">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="1d41b-140">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-140">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="1d41b-141">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-141">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="1d41b-142">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="1d41b-142">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


