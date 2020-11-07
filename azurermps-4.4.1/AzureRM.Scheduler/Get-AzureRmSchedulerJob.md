---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733624"
---
# <span data-ttu-id="a141a-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="a141a-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="a141a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a141a-102">SYNOPSIS</span></span>
<span data-ttu-id="a141a-103">Получает задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="a141a-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a141a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a141a-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a141a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a141a-105">DESCRIPTION</span></span>
<span data-ttu-id="a141a-106">Командлет **Get-AzureRmSchedulerJob** получает задания планировщика Azure.</span><span class="sxs-lookup"><span data-stu-id="a141a-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="a141a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a141a-107">EXAMPLES</span></span>

## <span data-ttu-id="a141a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a141a-108">PARAMETERS</span></span>

### <span data-ttu-id="a141a-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a141a-109">-JobCollectionName</span></span>
<span data-ttu-id="a141a-110">Указывает имя коллекции заданий, содержащей задания, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a141a-110">Specifies the name of a job collection that contains jobs to get.</span></span>

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

### <span data-ttu-id="a141a-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="a141a-111">-JobName</span></span>
<span data-ttu-id="a141a-112">Указывает имя задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a141a-112">Specifies the name of a job to get.</span></span>

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

### <span data-ttu-id="a141a-113">-JobState</span><span class="sxs-lookup"><span data-stu-id="a141a-113">-JobState</span></span>
<span data-ttu-id="a141a-114">Указывает состояние задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a141a-114">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="a141a-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a141a-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a141a-116">Включаем</span><span class="sxs-lookup"><span data-stu-id="a141a-116">Enabled</span></span> 
- <span data-ttu-id="a141a-117">Отключает</span><span class="sxs-lookup"><span data-stu-id="a141a-117">Disabled</span></span> 
- <span data-ttu-id="a141a-118">Сбой</span><span class="sxs-lookup"><span data-stu-id="a141a-118">Faulted</span></span> 
- <span data-ttu-id="a141a-119">Completed</span><span class="sxs-lookup"><span data-stu-id="a141a-119">Completed</span></span>

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

### <span data-ttu-id="a141a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a141a-120">-ResourceGroupName</span></span>
<span data-ttu-id="a141a-121">Указывает группу ресурсов, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a141a-121">Specifies the resource group of the jobs to get.</span></span>

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

### <span data-ttu-id="a141a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a141a-122">-DefaultProfile</span></span>
<span data-ttu-id="a141a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a141a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a141a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a141a-124">CommonParameters</span></span>
<span data-ttu-id="a141a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a141a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a141a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a141a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a141a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a141a-127">INPUTS</span></span>

## <span data-ttu-id="a141a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a141a-128">OUTPUTS</span></span>

### <span data-ttu-id="a141a-129">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a141a-129">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="a141a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a141a-130">NOTES</span></span>

## <span data-ttu-id="a141a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a141a-131">RELATED LINKS</span></span>

[<span data-ttu-id="a141a-132">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a141a-132">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a141a-133">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a141a-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a141a-134">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a141a-134">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a141a-135">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a141a-135">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a141a-136">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a141a-136">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="a141a-137">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="a141a-137">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="a141a-138">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a141a-138">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a141a-139">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a141a-139">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a141a-140">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a141a-140">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a141a-141">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a141a-141">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


