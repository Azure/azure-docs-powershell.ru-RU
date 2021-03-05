---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: be94460a2296874acefab3232f4a73d394a523d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964915"
---
# <span data-ttu-id="f83c0-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f83c0-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="f83c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f83c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f83c0-103">Начало отлагожки потока данных в фабрике данных Azure</span><span class="sxs-lookup"><span data-stu-id="f83c0-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="f83c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f83c0-104">SYNTAX</span></span>

### <span data-ttu-id="f83c0-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f83c0-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f83c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f83c0-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f83c0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f83c0-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f83c0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f83c0-108">DESCRIPTION</span></span>
<span data-ttu-id="f83c0-109">Эта длинная команда запускает сеанс отлагки потока данных для команд отлагки.</span><span class="sxs-lookup"><span data-stu-id="f83c0-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="f83c0-110">Эту команду можно прикрепить к определению времени запуска интеграции, чтобы настроить размер и тип кластера сеанса отложений.</span><span class="sxs-lookup"><span data-stu-id="f83c0-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="f83c0-111">Последовательность команд PowerShell для рабочего процесса отлагки потоков данных должна быть:</span><span class="sxs-lookup"><span data-stu-id="f83c0-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="f83c0-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f83c0-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="f83c0-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="f83c0-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="f83c0-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (повторите этот шаг для разных команд или целей или повторите шаг 2–3, чтобы изменить файл пакета)</span><span class="sxs-lookup"><span data-stu-id="f83c0-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="f83c0-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f83c0-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="f83c0-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f83c0-116">EXAMPLES</span></span>

### <span data-ttu-id="f83c0-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f83c0-117">Example 1</span></span>
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

<span data-ttu-id="f83c0-118">Начало сеанса отбивки с флагом AsJob.</span><span class="sxs-lookup"><span data-stu-id="f83c0-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="f83c0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f83c0-119">PARAMETERS</span></span>

### <span data-ttu-id="f83c0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f83c0-120">-AsJob</span></span>
<span data-ttu-id="f83c0-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f83c0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f83c0-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f83c0-122">-DataFactory</span></span>
<span data-ttu-id="f83c0-123">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f83c0-123">The data factory object.</span></span>

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

### <span data-ttu-id="f83c0-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f83c0-124">-DataFactoryName</span></span>
<span data-ttu-id="f83c0-125">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f83c0-125">The data factory name.</span></span>

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

### <span data-ttu-id="f83c0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83c0-126">-DefaultProfile</span></span>
<span data-ttu-id="f83c0-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f83c0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f83c0-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="f83c0-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="f83c0-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="f83c0-129">The JSON file path.</span></span>

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

### <span data-ttu-id="f83c0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83c0-130">-ResourceGroupName</span></span>
<span data-ttu-id="f83c0-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f83c0-131">The resource group name.</span></span>

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

### <span data-ttu-id="f83c0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f83c0-132">-ResourceId</span></span>
<span data-ttu-id="f83c0-133">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="f83c0-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f83c0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f83c0-134">-Confirm</span></span>
<span data-ttu-id="f83c0-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f83c0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f83c0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83c0-136">-WhatIf</span></span>
<span data-ttu-id="f83c0-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f83c0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83c0-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f83c0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f83c0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83c0-139">CommonParameters</span></span>
<span data-ttu-id="f83c0-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f83c0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83c0-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f83c0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83c0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f83c0-142">INPUTS</span></span>

### <span data-ttu-id="f83c0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f83c0-143">System.String</span></span>

### <span data-ttu-id="f83c0-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f83c0-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f83c0-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f83c0-145">OUTPUTS</span></span>

### <span data-ttu-id="f83c0-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f83c0-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="f83c0-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f83c0-147">NOTES</span></span>
<span data-ttu-id="f83c0-148">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="f83c0-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f83c0-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f83c0-149">RELATED LINKS</span></span>

[<span data-ttu-id="f83c0-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f83c0-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="f83c0-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="f83c0-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="f83c0-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="f83c0-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="f83c0-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f83c0-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)