---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567516"
---
# <span data-ttu-id="f1994-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1994-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="f1994-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1994-102">SYNOPSIS</span></span>
<span data-ttu-id="f1994-103">Создает коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="f1994-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1994-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1994-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1994-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1994-105">DESCRIPTION</span></span>
<span data-ttu-id="f1994-106">Командлет **New-AzureRmSchedulerJobCollection** создает коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="f1994-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="f1994-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1994-107">EXAMPLES</span></span>

## <span data-ttu-id="f1994-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1994-108">PARAMETERS</span></span>

### <span data-ttu-id="f1994-109">-Частота</span><span class="sxs-lookup"><span data-stu-id="f1994-109">-Frequency</span></span>
<span data-ttu-id="f1994-110">Указывает максимальную частоту, которую можно указать для любого задания в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="f1994-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="f1994-111">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f1994-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1994-112">До</span><span class="sxs-lookup"><span data-stu-id="f1994-112">Minute</span></span> 
- <span data-ttu-id="f1994-113">Часовой</span><span class="sxs-lookup"><span data-stu-id="f1994-113">Hour</span></span> 
- <span data-ttu-id="f1994-114">Дневных</span><span class="sxs-lookup"><span data-stu-id="f1994-114">Day</span></span> 
- <span data-ttu-id="f1994-115">Недели</span><span class="sxs-lookup"><span data-stu-id="f1994-115">Week</span></span> 
- <span data-ttu-id="f1994-116">Перехода</span><span class="sxs-lookup"><span data-stu-id="f1994-116">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1994-117">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="f1994-117">-Interval</span></span>
<span data-ttu-id="f1994-118">Указывает интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="f1994-118">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1994-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f1994-119">-JobCollectionName</span></span>
<span data-ttu-id="f1994-120">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="f1994-120">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="f1994-121">-Location</span><span class="sxs-lookup"><span data-stu-id="f1994-121">-Location</span></span>
<span data-ttu-id="f1994-122">Указывает область Azure, в которой этот командлет создает коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="f1994-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="f1994-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="f1994-123">-MaxJobCount</span></span>
<span data-ttu-id="f1994-124">Указывает максимальное количество заданий, которые можно создать в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="f1994-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="f1994-125">Максимальные значения зависят от плана, который указан в параметре *Plan* .</span><span class="sxs-lookup"><span data-stu-id="f1994-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1994-126">-Планирование</span><span class="sxs-lookup"><span data-stu-id="f1994-126">-Plan</span></span>
<span data-ttu-id="f1994-127">Указывает план сбора заданий.</span><span class="sxs-lookup"><span data-stu-id="f1994-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="f1994-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f1994-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1994-129">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="f1994-129">Free</span></span> 
- <span data-ttu-id="f1994-130">Стандартная</span><span class="sxs-lookup"><span data-stu-id="f1994-130">Standard</span></span> 
- <span data-ttu-id="f1994-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="f1994-131">P10Premium</span></span> 
- <span data-ttu-id="f1994-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="f1994-132">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1994-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1994-133">-ResourceGroupName</span></span>
<span data-ttu-id="f1994-134">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="f1994-134">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="f1994-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1994-135">-Confirm</span></span>
<span data-ttu-id="f1994-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1994-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1994-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1994-137">-WhatIf</span></span>
<span data-ttu-id="f1994-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1994-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1994-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1994-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1994-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1994-140">-DefaultProfile</span></span>
<span data-ttu-id="f1994-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1994-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1994-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1994-142">CommonParameters</span></span>
<span data-ttu-id="f1994-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1994-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1994-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1994-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1994-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1994-145">INPUTS</span></span>

## <span data-ttu-id="f1994-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1994-146">OUTPUTS</span></span>

### <span data-ttu-id="f1994-147">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="f1994-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="f1994-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1994-148">NOTES</span></span>

## <span data-ttu-id="f1994-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1994-149">RELATED LINKS</span></span>

[<span data-ttu-id="f1994-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1994-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f1994-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1994-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f1994-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1994-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f1994-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1994-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f1994-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1994-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


