---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733996"
---
# <span data-ttu-id="de5b3-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="de5b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="de5b3-103">Получает задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="de5b3-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de5b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de5b3-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de5b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de5b3-105">DESCRIPTION</span></span>
<span data-ttu-id="de5b3-106">Командлет **Get-AzureRmSchedulerJob** получает задания планировщика Azure.</span><span class="sxs-lookup"><span data-stu-id="de5b3-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="de5b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de5b3-107">EXAMPLES</span></span>

## <span data-ttu-id="de5b3-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de5b3-108">PARAMETERS</span></span>

### <span data-ttu-id="de5b3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5b3-109">-DefaultProfile</span></span>
<span data-ttu-id="de5b3-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de5b3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de5b3-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="de5b3-111">-JobCollectionName</span></span>
<span data-ttu-id="de5b3-112">Указывает имя коллекции заданий, содержащей задания, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="de5b3-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5b3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="de5b3-113">-JobName</span></span>
<span data-ttu-id="de5b3-114">Указывает имя задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="de5b3-114">Specifies the name of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5b3-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="de5b3-115">-JobState</span></span>
<span data-ttu-id="de5b3-116">Указывает состояние задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="de5b3-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="de5b3-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="de5b3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de5b3-118">Включаем</span><span class="sxs-lookup"><span data-stu-id="de5b3-118">Enabled</span></span> 
- <span data-ttu-id="de5b3-119">Отключает</span><span class="sxs-lookup"><span data-stu-id="de5b3-119">Disabled</span></span> 
- <span data-ttu-id="de5b3-120">Сбой</span><span class="sxs-lookup"><span data-stu-id="de5b3-120">Faulted</span></span> 
- <span data-ttu-id="de5b3-121">Completed</span><span class="sxs-lookup"><span data-stu-id="de5b3-121">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="de5b3-123">Указывает группу ресурсов, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="de5b3-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5b3-124">CommonParameters</span></span>
<span data-ttu-id="de5b3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de5b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5b3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5b3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5b3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de5b3-127">INPUTS</span></span>

### <span data-ttu-id="de5b3-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="de5b3-128">None</span></span>
<span data-ttu-id="de5b3-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="de5b3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de5b3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de5b3-130">OUTPUTS</span></span>

### <span data-ttu-id="de5b3-131">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="de5b3-131">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="de5b3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="de5b3-132">NOTES</span></span>

## <span data-ttu-id="de5b3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de5b3-133">RELATED LINKS</span></span>

[<span data-ttu-id="de5b3-134">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-134">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="de5b3-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="de5b3-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="de5b3-136">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-136">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="de5b3-137">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-137">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="de5b3-138">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-138">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="de5b3-139">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-139">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="de5b3-140">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-140">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="de5b3-141">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-141">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="de5b3-142">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-142">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="de5b3-143">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="de5b3-143">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


