---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417580"
---
# <span data-ttu-id="16962-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="16962-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="16962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16962-102">SYNOPSIS</span></span>
<span data-ttu-id="16962-103">Действие вызова отлагки в сеансе отлагки потока данных.</span><span class="sxs-lookup"><span data-stu-id="16962-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="16962-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16962-104">SYNTAX</span></span>

### <span data-ttu-id="16962-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16962-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16962-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="16962-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16962-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16962-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16962-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16962-108">DESCRIPTION</span></span>
<span data-ttu-id="16962-109">Эта команда выполняет предварительный просмотр данных, предварительный просмотр статистики и выражение для разного потока данных во время сеанса отбивки.</span><span class="sxs-lookup"><span data-stu-id="16962-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="16962-110">Последовательность команд PowerShell для рабочего процесса отлагки потоков данных должна быть:</span><span class="sxs-lookup"><span data-stu-id="16962-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="16962-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="16962-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="16962-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="16962-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="16962-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (повторите этот шаг для разных команд или целей или повторите шаг 2–3, чтобы изменить файл пакета)</span><span class="sxs-lookup"><span data-stu-id="16962-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="16962-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="16962-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="16962-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16962-115">EXAMPLES</span></span>

### <span data-ttu-id="16962-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16962-116">Example 1</span></span>
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

<span data-ttu-id="16962-117">В этом примере вызывается команда предварительного просмотра данных для сеанса отладки "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" в фабрике данных "WiKiADF", а затем преобразует результаты JSON в удобочитаемую строку.</span><span class="sxs-lookup"><span data-stu-id="16962-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="16962-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16962-118">PARAMETERS</span></span>

### <span data-ttu-id="16962-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16962-119">-AsJob</span></span>
<span data-ttu-id="16962-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="16962-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16962-121">-Столбцы</span><span class="sxs-lookup"><span data-stu-id="16962-121">-Columns</span></span>
<span data-ttu-id="16962-122">Список столбцов для предварительного просмотра статистики потока данных.</span><span class="sxs-lookup"><span data-stu-id="16962-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="16962-123">-Command</span><span class="sxs-lookup"><span data-stu-id="16962-123">-Command</span></span>
<span data-ttu-id="16962-124">Команда отбивки потока данных.</span><span class="sxs-lookup"><span data-stu-id="16962-124">The data flow debug command.</span></span> <span data-ttu-id="16962-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="16962-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="16962-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="16962-126">-DataFactory</span></span>
<span data-ttu-id="16962-127">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="16962-127">The data factory object.</span></span>

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

### <span data-ttu-id="16962-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16962-128">-DataFactoryName</span></span>
<span data-ttu-id="16962-129">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="16962-129">The data factory name.</span></span>

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

### <span data-ttu-id="16962-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16962-130">-DefaultProfile</span></span>
<span data-ttu-id="16962-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16962-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16962-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="16962-132">-Expression</span></span>
<span data-ttu-id="16962-133">Выражение для предварительного просмотра выражений потока данных.</span><span class="sxs-lookup"><span data-stu-id="16962-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="16962-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16962-134">-ResourceGroupName</span></span>
<span data-ttu-id="16962-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16962-135">The resource group name.</span></span>

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

### <span data-ttu-id="16962-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16962-136">-ResourceId</span></span>
<span data-ttu-id="16962-137">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="16962-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="16962-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="16962-138">-RowLimits</span></span>
<span data-ttu-id="16962-139">Ограничение строк для предварительного просмотра потока данных.</span><span class="sxs-lookup"><span data-stu-id="16962-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="16962-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="16962-140">-SessionId</span></span>
<span data-ttu-id="16962-141">ИД сеанса отлагки потоков данных.</span><span class="sxs-lookup"><span data-stu-id="16962-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="16962-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="16962-142">-StreamName</span></span>
<span data-ttu-id="16962-143">Имя потока данных для отладки.</span><span class="sxs-lookup"><span data-stu-id="16962-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="16962-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16962-144">-Confirm</span></span>
<span data-ttu-id="16962-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="16962-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16962-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16962-146">-WhatIf</span></span>
<span data-ttu-id="16962-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16962-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16962-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="16962-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16962-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16962-149">CommonParameters</span></span>
<span data-ttu-id="16962-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16962-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16962-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16962-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16962-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16962-152">INPUTS</span></span>

### <span data-ttu-id="16962-153">System.String</span><span class="sxs-lookup"><span data-stu-id="16962-153">System.String</span></span>

### <span data-ttu-id="16962-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="16962-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="16962-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16962-155">OUTPUTS</span></span>

### <span data-ttu-id="16962-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="16962-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="16962-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16962-157">NOTES</span></span>
<span data-ttu-id="16962-158">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="16962-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="16962-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16962-159">RELATED LINKS</span></span>

[<span data-ttu-id="16962-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="16962-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="16962-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="16962-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="16962-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="16962-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="16962-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="16962-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)