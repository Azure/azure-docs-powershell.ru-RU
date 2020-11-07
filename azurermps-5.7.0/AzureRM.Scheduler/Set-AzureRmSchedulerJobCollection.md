---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: fc2375e66dbc47ccadf11d0f7dd9dd66e42470de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733543"
---
# <span data-ttu-id="1347f-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1347f-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="1347f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1347f-102">SYNOPSIS</span></span>
<span data-ttu-id="1347f-103">Изменяет коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="1347f-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1347f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1347f-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1347f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1347f-105">DESCRIPTION</span></span>
<span data-ttu-id="1347f-106">Командлет **Set-AzureRmSchedulerJobCollection** изменяет коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="1347f-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="1347f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1347f-107">EXAMPLES</span></span>

## <span data-ttu-id="1347f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1347f-108">PARAMETERS</span></span>

### <span data-ttu-id="1347f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1347f-109">-DefaultProfile</span></span>
<span data-ttu-id="1347f-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1347f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1347f-111">-Частота</span><span class="sxs-lookup"><span data-stu-id="1347f-111">-Frequency</span></span>
<span data-ttu-id="1347f-112">Указывает максимальную частоту, которую можно указать для любого задания в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="1347f-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="1347f-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1347f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1347f-114">До</span><span class="sxs-lookup"><span data-stu-id="1347f-114">Minute</span></span> 
- <span data-ttu-id="1347f-115">Часовой</span><span class="sxs-lookup"><span data-stu-id="1347f-115">Hour</span></span> 
- <span data-ttu-id="1347f-116">Дневных</span><span class="sxs-lookup"><span data-stu-id="1347f-116">Day</span></span> 
- <span data-ttu-id="1347f-117">Недели</span><span class="sxs-lookup"><span data-stu-id="1347f-117">Week</span></span> 
- <span data-ttu-id="1347f-118">Перехода</span><span class="sxs-lookup"><span data-stu-id="1347f-118">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1347f-119">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="1347f-119">-Interval</span></span>
<span data-ttu-id="1347f-120">Указывает интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="1347f-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1347f-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1347f-121">-JobCollectionName</span></span>
<span data-ttu-id="1347f-122">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="1347f-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="1347f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1347f-123">-Location</span></span>
<span data-ttu-id="1347f-124">Указывает область Azure, в которой находится коллекция заданий.</span><span class="sxs-lookup"><span data-stu-id="1347f-124">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="1347f-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="1347f-125">-MaxJobCount</span></span>
<span data-ttu-id="1347f-126">Указывает максимальное количество заданий, которые можно создать в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="1347f-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="1347f-127">Максимальные значения зависят от плана, который указан в параметре *Plan* .</span><span class="sxs-lookup"><span data-stu-id="1347f-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1347f-128">-Планирование</span><span class="sxs-lookup"><span data-stu-id="1347f-128">-Plan</span></span>
<span data-ttu-id="1347f-129">Указывает план сбора заданий.</span><span class="sxs-lookup"><span data-stu-id="1347f-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="1347f-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1347f-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1347f-131">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="1347f-131">Free</span></span> 
- <span data-ttu-id="1347f-132">Стандартная</span><span class="sxs-lookup"><span data-stu-id="1347f-132">Standard</span></span> 
- <span data-ttu-id="1347f-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="1347f-133">P10Premium</span></span> 
- <span data-ttu-id="1347f-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="1347f-134">P20Premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1347f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1347f-135">-ResourceGroupName</span></span>
<span data-ttu-id="1347f-136">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="1347f-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="1347f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1347f-137">-Confirm</span></span>
<span data-ttu-id="1347f-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1347f-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1347f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1347f-139">-WhatIf</span></span>
<span data-ttu-id="1347f-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1347f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1347f-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1347f-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1347f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1347f-142">CommonParameters</span></span>
<span data-ttu-id="1347f-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1347f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1347f-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1347f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1347f-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1347f-145">INPUTS</span></span>

### <span data-ttu-id="1347f-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="1347f-146">None</span></span>
<span data-ttu-id="1347f-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1347f-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1347f-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1347f-148">OUTPUTS</span></span>

### <span data-ttu-id="1347f-149">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="1347f-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="1347f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="1347f-150">NOTES</span></span>

## <span data-ttu-id="1347f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1347f-151">RELATED LINKS</span></span>

[<span data-ttu-id="1347f-152">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1347f-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1347f-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1347f-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1347f-154">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1347f-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1347f-155">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1347f-155">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1347f-156">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1347f-156">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


