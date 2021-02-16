---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: c319ee7fba1bddff8e93e56601c623658094253d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238353"
---
# <span data-ttu-id="8782e-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="8782e-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="8782e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8782e-102">SYNOPSIS</span></span>
<span data-ttu-id="8782e-103">Добавьте ресурс потоков данных и его зависимости в определенный сеанс отлагожки потоков данных.</span><span class="sxs-lookup"><span data-stu-id="8782e-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="8782e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8782e-104">SYNTAX</span></span>

### <span data-ttu-id="8782e-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8782e-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8782e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8782e-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8782e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8782e-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8782e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8782e-108">DESCRIPTION</span></span>
<span data-ttu-id="8782e-109">Эта команда прикрепит ресурс потока данных и его зависимости к конкретному сеансу отлагки, в командной последовательности PowerShell для рабочего процесса отлагки должны быть:</span><span class="sxs-lookup"><span data-stu-id="8782e-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="8782e-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8782e-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="8782e-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="8782e-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="8782e-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (повторите этот шаг для разных команд или целей или повторите шаг 2–3, чтобы изменить файл пакета)</span><span class="sxs-lookup"><span data-stu-id="8782e-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="8782e-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8782e-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="8782e-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8782e-114">EXAMPLES</span></span>

### <span data-ttu-id="8782e-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8782e-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="8782e-116">Добавьте пакет потоков данных в сеанс отладки "550effe4-93a3-485c-8525-eaf25259efbd" фабрики данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="8782e-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="8782e-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span><span class="sxs-lookup"><span data-stu-id="8782e-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="8782e-118">Например:</span><span class="sxs-lookup"><span data-stu-id="8782e-118">For instance:</span></span>

<span data-ttu-id="8782e-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName=name; AccountKey=key; EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span><span class="sxs-lookup"><span data-stu-id="8782e-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="8782e-120">Параметр SessionID используется для замены существующего свойства sessionId в файле пакета.</span><span class="sxs-lookup"><span data-stu-id="8782e-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="8782e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8782e-121">PARAMETERS</span></span>

### <span data-ttu-id="8782e-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8782e-122">-DataFactory</span></span>
<span data-ttu-id="8782e-123">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8782e-123">The data factory object.</span></span>

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

### <span data-ttu-id="8782e-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8782e-124">-DataFactoryName</span></span>
<span data-ttu-id="8782e-125">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8782e-125">The data factory name.</span></span>

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

### <span data-ttu-id="8782e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8782e-126">-DefaultProfile</span></span>
<span data-ttu-id="8782e-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8782e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8782e-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="8782e-128">-PackageFile</span></span>
<span data-ttu-id="8782e-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="8782e-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8782e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8782e-130">-PassThru</span></span>
<span data-ttu-id="8782e-131">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="8782e-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="8782e-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8782e-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="8782e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8782e-133">-ResourceGroupName</span></span>
<span data-ttu-id="8782e-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8782e-134">The resource group name.</span></span>

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

### <span data-ttu-id="8782e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8782e-135">-ResourceId</span></span>
<span data-ttu-id="8782e-136">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="8782e-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8782e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8782e-137">-Confirm</span></span>
<span data-ttu-id="8782e-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8782e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8782e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8782e-139">-WhatIf</span></span>
<span data-ttu-id="8782e-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8782e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8782e-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8782e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8782e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8782e-142">CommonParameters</span></span>
<span data-ttu-id="8782e-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8782e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8782e-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8782e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8782e-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8782e-145">INPUTS</span></span>

### <span data-ttu-id="8782e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8782e-146">System.String</span></span>

### <span data-ttu-id="8782e-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8782e-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8782e-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8782e-148">OUTPUTS</span></span>

### <span data-ttu-id="8782e-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="8782e-149">System.Void</span></span>

### <span data-ttu-id="8782e-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8782e-150">System.Boolean</span></span>

## <span data-ttu-id="8782e-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8782e-151">NOTES</span></span>
<span data-ttu-id="8782e-152">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="8782e-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8782e-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8782e-153">RELATED LINKS</span></span>

[<span data-ttu-id="8782e-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8782e-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="8782e-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8782e-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="8782e-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="8782e-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="8782e-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8782e-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
