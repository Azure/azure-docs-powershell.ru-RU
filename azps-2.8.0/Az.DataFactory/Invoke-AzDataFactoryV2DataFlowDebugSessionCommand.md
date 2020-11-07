---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 45419ede425b5d5ea3ba9fcbbbfb024fe8ba9358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721510"
---
# <span data-ttu-id="885e5-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="885e5-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="885e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="885e5-102">SYNOPSIS</span></span>
<span data-ttu-id="885e5-103">Действие "вызвать отладку" в сеансе отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="885e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="885e5-104">SYNTAX</span></span>

### <span data-ttu-id="885e5-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="885e5-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="885e5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="885e5-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="885e5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="885e5-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="885e5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="885e5-108">DESCRIPTION</span></span>
<span data-ttu-id="885e5-109">Эта команда выполняет предварительный просмотр предварительной версии данных/просмотра статистики/выражения для другого потока потока данных в сеансе отладки.</span><span class="sxs-lookup"><span data-stu-id="885e5-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="885e5-110">Ниже приведена последовательность команд PowerShell для рабочего процесса отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="885e5-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="885e5-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="885e5-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="885e5-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="885e5-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (повторите эти действия для разных команд и целевых объектов или повторите шаг 2-3, чтобы изменить файл пакета).</span><span class="sxs-lookup"><span data-stu-id="885e5-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="885e5-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="885e5-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="885e5-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="885e5-115">EXAMPLES</span></span>

### <span data-ttu-id="885e5-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="885e5-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="885e5-117">Этот пример вызывает команду Предварительный просмотр данных для сеанса отладки "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" в фабрике данных "WiKiADF", а затем преобразует выходные данные JSON в читаемый текст.</span><span class="sxs-lookup"><span data-stu-id="885e5-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="885e5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="885e5-118">PARAMETERS</span></span>

### <span data-ttu-id="885e5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="885e5-119">-AsJob</span></span>
<span data-ttu-id="885e5-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="885e5-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-121">-Столбцы</span><span class="sxs-lookup"><span data-stu-id="885e5-121">-Columns</span></span>
<span data-ttu-id="885e5-122">Список столбцов для предварительного просмотра статистики потока данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-123">-Command</span><span class="sxs-lookup"><span data-stu-id="885e5-123">-Command</span></span>
<span data-ttu-id="885e5-124">Команда отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-124">The data flow debug command.</span></span> <span data-ttu-id="885e5-125">Варианты выбора — executePreviewQuery, executeStatisticsQuery и executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="885e5-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-126">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="885e5-126">-DataFactory</span></span>
<span data-ttu-id="885e5-127">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-127">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="885e5-128">-DataFactoryName</span></span>
<span data-ttu-id="885e5-129">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-129">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885e5-130">-DefaultProfile</span></span>
<span data-ttu-id="885e5-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="885e5-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="885e5-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="885e5-132">-Expression</span></span>
<span data-ttu-id="885e5-133">Выражение для предварительного просмотра выражения потока данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885e5-134">-ResourceGroupName</span></span>
<span data-ttu-id="885e5-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="885e5-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="885e5-136">-ResourceId</span></span>
<span data-ttu-id="885e5-137">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="885e5-137">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="885e5-138">-RowLimits</span></span>
<span data-ttu-id="885e5-139">Предельное количество строк для предварительного просмотра данных потока данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="885e5-140">-SessionId</span></span>
<span data-ttu-id="885e5-141">Идентификатор сеанса отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="885e5-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="885e5-142">-StreamName</span></span>
<span data-ttu-id="885e5-143">Имя потока потока данных для отладки.</span><span class="sxs-lookup"><span data-stu-id="885e5-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="885e5-144">-Confirm</span></span>
<span data-ttu-id="885e5-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="885e5-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885e5-146">-WhatIf</span></span>
<span data-ttu-id="885e5-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="885e5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="885e5-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="885e5-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885e5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885e5-149">CommonParameters</span></span>
<span data-ttu-id="885e5-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="885e5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885e5-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="885e5-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885e5-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="885e5-152">INPUTS</span></span>

### <span data-ttu-id="885e5-153">System. String</span><span class="sxs-lookup"><span data-stu-id="885e5-153">System.String</span></span>

### <span data-ttu-id="885e5-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="885e5-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="885e5-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="885e5-155">OUTPUTS</span></span>

### <span data-ttu-id="885e5-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="885e5-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="885e5-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="885e5-157">NOTES</span></span>
<span data-ttu-id="885e5-158">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, factoriesKeywords: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрика</span><span class="sxs-lookup"><span data-stu-id="885e5-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="885e5-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="885e5-159">RELATED LINKS</span></span>

[<span data-ttu-id="885e5-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="885e5-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="885e5-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="885e5-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="885e5-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="885e5-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="885e5-163">Остановить-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="885e5-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
