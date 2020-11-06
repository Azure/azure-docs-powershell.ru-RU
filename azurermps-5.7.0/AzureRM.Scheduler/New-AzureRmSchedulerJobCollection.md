---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: dfec2d79d092a5f119daa558b1d383f1a1d71df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563307"
---
# <span data-ttu-id="326d5-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="326d5-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="326d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="326d5-102">SYNOPSIS</span></span>
<span data-ttu-id="326d5-103">Создает коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="326d5-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="326d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="326d5-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="326d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="326d5-105">DESCRIPTION</span></span>
<span data-ttu-id="326d5-106">Командлет **New-AzureRmSchedulerJobCollection** создает коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="326d5-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="326d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="326d5-107">EXAMPLES</span></span>

## <span data-ttu-id="326d5-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="326d5-108">PARAMETERS</span></span>

### <span data-ttu-id="326d5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326d5-109">-DefaultProfile</span></span>
<span data-ttu-id="326d5-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="326d5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="326d5-111">-Частота</span><span class="sxs-lookup"><span data-stu-id="326d5-111">-Frequency</span></span>
<span data-ttu-id="326d5-112">Указывает максимальную частоту, которую можно указать для любого задания в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="326d5-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="326d5-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="326d5-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="326d5-114">До</span><span class="sxs-lookup"><span data-stu-id="326d5-114">Minute</span></span> 
- <span data-ttu-id="326d5-115">Часовой</span><span class="sxs-lookup"><span data-stu-id="326d5-115">Hour</span></span> 
- <span data-ttu-id="326d5-116">Дневных</span><span class="sxs-lookup"><span data-stu-id="326d5-116">Day</span></span> 
- <span data-ttu-id="326d5-117">Недели</span><span class="sxs-lookup"><span data-stu-id="326d5-117">Week</span></span> 
- <span data-ttu-id="326d5-118">Перехода</span><span class="sxs-lookup"><span data-stu-id="326d5-118">Month</span></span>

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

### <span data-ttu-id="326d5-119">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="326d5-119">-Interval</span></span>
<span data-ttu-id="326d5-120">Указывает интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="326d5-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="326d5-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="326d5-121">-JobCollectionName</span></span>
<span data-ttu-id="326d5-122">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="326d5-122">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="326d5-123">-Location</span><span class="sxs-lookup"><span data-stu-id="326d5-123">-Location</span></span>
<span data-ttu-id="326d5-124">Указывает область Azure, в которой этот командлет создает коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="326d5-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="326d5-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="326d5-125">-MaxJobCount</span></span>
<span data-ttu-id="326d5-126">Указывает максимальное количество заданий, которые можно создать в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="326d5-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="326d5-127">Максимальные значения зависят от плана, который указан в параметре *Plan* .</span><span class="sxs-lookup"><span data-stu-id="326d5-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="326d5-128">-Планирование</span><span class="sxs-lookup"><span data-stu-id="326d5-128">-Plan</span></span>
<span data-ttu-id="326d5-129">Указывает план сбора заданий.</span><span class="sxs-lookup"><span data-stu-id="326d5-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="326d5-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="326d5-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="326d5-131">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="326d5-131">Free</span></span> 
- <span data-ttu-id="326d5-132">Стандартная</span><span class="sxs-lookup"><span data-stu-id="326d5-132">Standard</span></span> 
- <span data-ttu-id="326d5-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="326d5-133">P10Premium</span></span> 
- <span data-ttu-id="326d5-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="326d5-134">P20Premium</span></span>

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

### <span data-ttu-id="326d5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326d5-135">-ResourceGroupName</span></span>
<span data-ttu-id="326d5-136">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="326d5-136">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="326d5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="326d5-137">-Confirm</span></span>
<span data-ttu-id="326d5-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="326d5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="326d5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="326d5-139">-WhatIf</span></span>
<span data-ttu-id="326d5-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="326d5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="326d5-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="326d5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="326d5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326d5-142">CommonParameters</span></span>
<span data-ttu-id="326d5-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="326d5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326d5-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326d5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326d5-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="326d5-145">INPUTS</span></span>

### <span data-ttu-id="326d5-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="326d5-146">None</span></span>
<span data-ttu-id="326d5-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="326d5-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="326d5-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="326d5-148">OUTPUTS</span></span>

### <span data-ttu-id="326d5-149">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="326d5-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="326d5-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="326d5-150">NOTES</span></span>

## <span data-ttu-id="326d5-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="326d5-151">RELATED LINKS</span></span>

[<span data-ttu-id="326d5-152">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="326d5-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="326d5-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="326d5-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="326d5-154">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="326d5-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="326d5-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="326d5-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="326d5-156">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="326d5-156">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


