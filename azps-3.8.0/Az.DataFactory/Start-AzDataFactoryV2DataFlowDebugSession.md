---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912782"
---
# <span data-ttu-id="51d31-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="51d31-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="51d31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51d31-102">SYNOPSIS</span></span>
<span data-ttu-id="51d31-103">Запуск сеанса отладки потока данных в фабрике данных Azure</span><span class="sxs-lookup"><span data-stu-id="51d31-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="51d31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51d31-104">SYNTAX</span></span>

### <span data-ttu-id="51d31-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51d31-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d31-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="51d31-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51d31-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51d31-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51d31-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51d31-108">DESCRIPTION</span></span>
<span data-ttu-id="51d31-109">Эта длительная команда запускает сеанс отладки потока данных для предстоящих команд отладки.</span><span class="sxs-lookup"><span data-stu-id="51d31-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="51d31-110">Эта команда может быть присвоена с определением среды выполнения Integration для настройки размера и типа кластера отладочных сеансов.</span><span class="sxs-lookup"><span data-stu-id="51d31-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="51d31-111">Ниже приведена последовательность команд PowerShell для рабочего процесса отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="51d31-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="51d31-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="51d31-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="51d31-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="51d31-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="51d31-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (повторите эти действия для разных команд и целевых объектов или повторите шаг 2-3, чтобы изменить файл пакета).</span><span class="sxs-lookup"><span data-stu-id="51d31-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="51d31-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="51d31-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="51d31-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51d31-116">EXAMPLES</span></span>

### <span data-ttu-id="51d31-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="51d31-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="51d31-118">Запуск сеанса отладки с флагом AsJob.</span><span class="sxs-lookup"><span data-stu-id="51d31-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="51d31-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51d31-119">PARAMETERS</span></span>

### <span data-ttu-id="51d31-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51d31-120">-AsJob</span></span>
<span data-ttu-id="51d31-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="51d31-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51d31-122">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="51d31-122">-DataFactory</span></span>
<span data-ttu-id="51d31-123">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="51d31-123">The data factory object.</span></span>

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

### <span data-ttu-id="51d31-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="51d31-124">-DataFactoryName</span></span>
<span data-ttu-id="51d31-125">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="51d31-125">The data factory name.</span></span>

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

### <span data-ttu-id="51d31-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d31-126">-DefaultProfile</span></span>
<span data-ttu-id="51d31-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51d31-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51d31-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="51d31-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="51d31-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="51d31-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d31-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51d31-130">-ResourceGroupName</span></span>
<span data-ttu-id="51d31-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51d31-131">The resource group name.</span></span>

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

### <span data-ttu-id="51d31-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51d31-132">-ResourceId</span></span>
<span data-ttu-id="51d31-133">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="51d31-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="51d31-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51d31-134">-Confirm</span></span>
<span data-ttu-id="51d31-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51d31-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51d31-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51d31-136">-WhatIf</span></span>
<span data-ttu-id="51d31-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51d31-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51d31-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51d31-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51d31-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d31-139">CommonParameters</span></span>
<span data-ttu-id="51d31-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51d31-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d31-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51d31-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d31-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51d31-142">INPUTS</span></span>

### <span data-ttu-id="51d31-143">System. String</span><span class="sxs-lookup"><span data-stu-id="51d31-143">System.String</span></span>

### <span data-ttu-id="51d31-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="51d31-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="51d31-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51d31-145">OUTPUTS</span></span>

### <span data-ttu-id="51d31-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="51d31-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="51d31-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="51d31-147">NOTES</span></span>
<span data-ttu-id="51d31-148">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="51d31-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="51d31-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51d31-149">RELATED LINKS</span></span>

[<span data-ttu-id="51d31-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="51d31-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="51d31-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="51d31-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="51d31-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="51d31-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="51d31-153">Остановить-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="51d31-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)