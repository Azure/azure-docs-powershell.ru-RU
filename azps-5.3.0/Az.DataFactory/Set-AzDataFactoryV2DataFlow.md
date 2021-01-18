---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508445"
---
# <span data-ttu-id="14b1d-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="14b1d-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="14b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="14b1d-103">Создает поток данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="14b1d-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="14b1d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14b1d-104">SYNTAX</span></span>

### <span data-ttu-id="14b1d-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14b1d-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14b1d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="14b1d-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14b1d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14b1d-107">DESCRIPTION</span></span>
<span data-ttu-id="14b1d-108">С Set-AzDataFactoryV2DataFlow создается поток данных или обновляется существующий поток данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="14b1d-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="14b1d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14b1d-109">EXAMPLES</span></span>

### <span data-ttu-id="14b1d-110">Пример 1. Создание потока данных</span><span class="sxs-lookup"><span data-stu-id="14b1d-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="14b1d-111">Эта команда создает поток данных с именемDemDemo1 в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="14b1d-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="14b1d-112">Эта команда будет базой данных, которая будет TaxiDemo1.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="14b1d-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="14b1d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14b1d-113">PARAMETERS</span></span>

### <span data-ttu-id="14b1d-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="14b1d-114">-DataFactoryName</span></span>
<span data-ttu-id="14b1d-115">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="14b1d-115">The data factory name.</span></span>

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

### <span data-ttu-id="14b1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b1d-116">-DefaultProfile</span></span>
<span data-ttu-id="14b1d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14b1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b1d-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="14b1d-118">-DefinitionFile</span></span>
<span data-ttu-id="14b1d-119">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="14b1d-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b1d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="14b1d-120">-Force</span></span>
<span data-ttu-id="14b1d-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="14b1d-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="14b1d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="14b1d-122">-Name</span></span>
<span data-ttu-id="14b1d-123">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="14b1d-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b1d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b1d-124">-ResourceGroupName</span></span>
<span data-ttu-id="14b1d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14b1d-125">The resource group name.</span></span>

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

### <span data-ttu-id="14b1d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14b1d-126">-ResourceId</span></span>
<span data-ttu-id="14b1d-127">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="14b1d-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="14b1d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14b1d-128">-Confirm</span></span>
<span data-ttu-id="14b1d-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="14b1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14b1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b1d-130">-WhatIf</span></span>
<span data-ttu-id="14b1d-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14b1d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14b1d-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="14b1d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14b1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b1d-133">CommonParameters</span></span>
<span data-ttu-id="14b1d-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b1d-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14b1d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b1d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14b1d-136">INPUTS</span></span>

### <span data-ttu-id="14b1d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="14b1d-137">System.String</span></span>

## <span data-ttu-id="14b1d-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14b1d-138">OUTPUTS</span></span>

### <span data-ttu-id="14b1d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="14b1d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="14b1d-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14b1d-140">NOTES</span></span>
<span data-ttu-id="14b1d-141">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="14b1d-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="14b1d-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14b1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="14b1d-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="14b1d-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="14b1d-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="14b1d-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
