---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 141a91272e805cc30f290d544a9a33c7c81484e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733619"
---
# <span data-ttu-id="90a79-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="90a79-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="90a79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90a79-102">SYNOPSIS</span></span>
<span data-ttu-id="90a79-103">Изменяет коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="90a79-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90a79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90a79-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90a79-105">DESCRIPTION</span></span>
<span data-ttu-id="90a79-106">Командлет **Set-AzureRmSchedulerJobCollection** изменяет коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="90a79-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="90a79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90a79-107">EXAMPLES</span></span>

## <span data-ttu-id="90a79-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90a79-108">PARAMETERS</span></span>

### <span data-ttu-id="90a79-109">-Частота</span><span class="sxs-lookup"><span data-stu-id="90a79-109">-Frequency</span></span>
<span data-ttu-id="90a79-110">Указывает максимальную частоту, которую можно указать для любого задания в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="90a79-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="90a79-111">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="90a79-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90a79-112">До</span><span class="sxs-lookup"><span data-stu-id="90a79-112">Minute</span></span> 
- <span data-ttu-id="90a79-113">Часовой</span><span class="sxs-lookup"><span data-stu-id="90a79-113">Hour</span></span> 
- <span data-ttu-id="90a79-114">Дневных</span><span class="sxs-lookup"><span data-stu-id="90a79-114">Day</span></span> 
- <span data-ttu-id="90a79-115">Недели</span><span class="sxs-lookup"><span data-stu-id="90a79-115">Week</span></span> 
- <span data-ttu-id="90a79-116">Перехода</span><span class="sxs-lookup"><span data-stu-id="90a79-116">Month</span></span>

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

### <span data-ttu-id="90a79-117">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="90a79-117">-Interval</span></span>
<span data-ttu-id="90a79-118">Указывает интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="90a79-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="90a79-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="90a79-119">-JobCollectionName</span></span>
<span data-ttu-id="90a79-120">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="90a79-120">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="90a79-121">-Location</span><span class="sxs-lookup"><span data-stu-id="90a79-121">-Location</span></span>
<span data-ttu-id="90a79-122">Указывает область Azure, в которой находится коллекция заданий.</span><span class="sxs-lookup"><span data-stu-id="90a79-122">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="90a79-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="90a79-123">-MaxJobCount</span></span>
<span data-ttu-id="90a79-124">Указывает максимальное количество заданий, которые можно создать в коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="90a79-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="90a79-125">Максимальные значения зависят от плана, который указан в параметре *Plan* .</span><span class="sxs-lookup"><span data-stu-id="90a79-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="90a79-126">-Планирование</span><span class="sxs-lookup"><span data-stu-id="90a79-126">-Plan</span></span>
<span data-ttu-id="90a79-127">Указывает план сбора заданий.</span><span class="sxs-lookup"><span data-stu-id="90a79-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="90a79-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="90a79-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90a79-129">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="90a79-129">Free</span></span> 
- <span data-ttu-id="90a79-130">Стандартная</span><span class="sxs-lookup"><span data-stu-id="90a79-130">Standard</span></span> 
- <span data-ttu-id="90a79-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="90a79-131">P10Premium</span></span> 
- <span data-ttu-id="90a79-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="90a79-132">P20Premium</span></span>

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

### <span data-ttu-id="90a79-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a79-133">-ResourceGroupName</span></span>
<span data-ttu-id="90a79-134">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="90a79-134">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="90a79-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90a79-135">-Confirm</span></span>
<span data-ttu-id="90a79-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90a79-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a79-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a79-137">-WhatIf</span></span>
<span data-ttu-id="90a79-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90a79-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a79-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90a79-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a79-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a79-140">-DefaultProfile</span></span>
<span data-ttu-id="90a79-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90a79-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a79-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a79-142">CommonParameters</span></span>
<span data-ttu-id="90a79-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90a79-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a79-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a79-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a79-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90a79-145">INPUTS</span></span>

## <span data-ttu-id="90a79-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90a79-146">OUTPUTS</span></span>

### <span data-ttu-id="90a79-147">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="90a79-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="90a79-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="90a79-148">NOTES</span></span>

## <span data-ttu-id="90a79-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90a79-149">RELATED LINKS</span></span>

[<span data-ttu-id="90a79-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="90a79-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="90a79-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="90a79-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="90a79-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="90a79-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="90a79-153">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="90a79-153">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="90a79-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="90a79-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


