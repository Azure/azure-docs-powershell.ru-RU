---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: c319ee7fba1bddff8e93e56601c623658094253d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245051"
---
# <span data-ttu-id="a652a-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a652a-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="a652a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a652a-102">SYNOPSIS</span></span>
<span data-ttu-id="a652a-103">Добавьте ресурс потока данных и его зависимости в конкретный сеанс отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="a652a-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="a652a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a652a-104">SYNTAX</span></span>

### <span data-ttu-id="a652a-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a652a-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a652a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a652a-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a652a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a652a-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a652a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a652a-108">DESCRIPTION</span></span>
<span data-ttu-id="a652a-109">Эта команда прикрепляет ресурс потока данных и его зависимости к определенному сеансу отладки. последовательность команд PowerShell для рабочего процесса отладки потока данных должна быть следующей:</span><span class="sxs-lookup"><span data-stu-id="a652a-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="a652a-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a652a-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="a652a-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a652a-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="a652a-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (повторите эти действия для разных команд и целевых объектов или повторите шаг 2-3, чтобы изменить файл пакета).</span><span class="sxs-lookup"><span data-stu-id="a652a-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="a652a-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a652a-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="a652a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a652a-114">EXAMPLES</span></span>

### <span data-ttu-id="a652a-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a652a-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="a652a-116">Добавьте пакет потока данных в сеанс отладки "550effe4-93a3-485c-8525-eaf25259efbd" фабрики данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a652a-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="a652a-117">Файл Pakcage включает ресурс отладки потока данных, список ресурсов отладки набора данных, список отладочного ресурса связанной службы, параметр отладки и идентификатор сеанса.</span><span class="sxs-lookup"><span data-stu-id="a652a-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="a652a-118">Например:</span><span class="sxs-lookup"><span data-stu-id="a652a-118">For instance:</span></span>

<span data-ttu-id="a652a-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; Имя_учетной_записи = имя; AccountKey = клавиша; EndpointSuffix = Core. Windows. NET "}}}]," debugSettings ": {" sourceSettings ": [{" sourceName ":" Source1 "," rowLimit ": 1000}]}," sessionId ":" 4f988caf-e765-47d2-82cd-430334a6b135 "</span><span class="sxs-lookup"><span data-stu-id="a652a-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="a652a-120">Параметр SessionID используется для замены существующего свойства sessionId в файле пакета.</span><span class="sxs-lookup"><span data-stu-id="a652a-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="a652a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a652a-121">PARAMETERS</span></span>

### <span data-ttu-id="a652a-122">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a652a-122">-DataFactory</span></span>
<span data-ttu-id="a652a-123">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a652a-123">The data factory object.</span></span>

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

### <span data-ttu-id="a652a-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a652a-124">-DataFactoryName</span></span>
<span data-ttu-id="a652a-125">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a652a-125">The data factory name.</span></span>

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

### <span data-ttu-id="a652a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a652a-126">-DefaultProfile</span></span>
<span data-ttu-id="a652a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a652a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a652a-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="a652a-128">-PackageFile</span></span>
<span data-ttu-id="a652a-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="a652a-129">The JSON file path.</span></span>

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

### <span data-ttu-id="a652a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a652a-130">-PassThru</span></span>
<span data-ttu-id="a652a-131">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="a652a-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a652a-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a652a-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="a652a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a652a-133">-ResourceGroupName</span></span>
<span data-ttu-id="a652a-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a652a-134">The resource group name.</span></span>

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

### <span data-ttu-id="a652a-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a652a-135">-ResourceId</span></span>
<span data-ttu-id="a652a-136">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="a652a-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a652a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a652a-137">-Confirm</span></span>
<span data-ttu-id="a652a-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a652a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a652a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a652a-139">-WhatIf</span></span>
<span data-ttu-id="a652a-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a652a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a652a-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a652a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a652a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a652a-142">CommonParameters</span></span>
<span data-ttu-id="a652a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a652a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a652a-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a652a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a652a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a652a-145">INPUTS</span></span>

### <span data-ttu-id="a652a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a652a-146">System.String</span></span>

### <span data-ttu-id="a652a-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a652a-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a652a-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a652a-148">OUTPUTS</span></span>

### <span data-ttu-id="a652a-149">System. void</span><span class="sxs-lookup"><span data-stu-id="a652a-149">System.Void</span></span>

### <span data-ttu-id="a652a-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a652a-150">System.Boolean</span></span>

## <span data-ttu-id="a652a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="a652a-151">NOTES</span></span>
<span data-ttu-id="a652a-152">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="a652a-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a652a-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a652a-153">RELATED LINKS</span></span>

[<span data-ttu-id="a652a-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a652a-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a652a-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a652a-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a652a-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="a652a-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="a652a-157">Остановить-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a652a-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
