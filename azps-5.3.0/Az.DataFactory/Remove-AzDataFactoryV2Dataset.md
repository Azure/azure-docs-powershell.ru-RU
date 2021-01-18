---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518930"
---
# <span data-ttu-id="de996-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="de996-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="de996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de996-102">SYNOPSIS</span></span>
<span data-ttu-id="de996-103">Удаляет набор данных из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="de996-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="de996-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="de996-104">SYNTAX</span></span>

### <span data-ttu-id="de996-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de996-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de996-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="de996-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de996-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="de996-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de996-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de996-108">DESCRIPTION</span></span>
<span data-ttu-id="de996-109">Новый Remove-AzDataFactoryV2Dataset удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="de996-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="de996-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="de996-110">EXAMPLES</span></span>

### <span data-ttu-id="de996-111">Пример 1. Удаление наборов данных</span><span class="sxs-lookup"><span data-stu-id="de996-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="de996-112">Эта команда удаляет набор данных DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="de996-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="de996-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="de996-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="de996-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de996-114">PARAMETERS</span></span>

### <span data-ttu-id="de996-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="de996-115">-DataFactoryName</span></span>
<span data-ttu-id="de996-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="de996-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="de996-117">Этот cmdlet удаляет набор данных из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="de996-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="de996-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de996-118">-DefaultProfile</span></span>
<span data-ttu-id="de996-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de996-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de996-120">-Force</span><span class="sxs-lookup"><span data-stu-id="de996-120">-Force</span></span>
<span data-ttu-id="de996-121">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="de996-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="de996-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de996-122">-InputObject</span></span>
<span data-ttu-id="de996-123">Определяет объект Dataset, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="de996-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de996-124">-Name</span><span class="sxs-lookup"><span data-stu-id="de996-124">-Name</span></span>
<span data-ttu-id="de996-125">Имя удаляемого наборов данных.</span><span class="sxs-lookup"><span data-stu-id="de996-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de996-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de996-126">-ResourceGroupName</span></span>
<span data-ttu-id="de996-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="de996-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="de996-128">Этот cmdlet удаляет набор данных из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="de996-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="de996-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de996-129">-ResourceId</span></span>
<span data-ttu-id="de996-130">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="de996-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="de996-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de996-131">-Confirm</span></span>
<span data-ttu-id="de996-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de996-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de996-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de996-133">-WhatIf</span></span>
<span data-ttu-id="de996-134">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de996-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="de996-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de996-135">CommonParameters</span></span>
<span data-ttu-id="de996-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de996-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de996-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de996-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de996-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de996-138">INPUTS</span></span>

### <span data-ttu-id="de996-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="de996-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="de996-140">System.String</span><span class="sxs-lookup"><span data-stu-id="de996-140">System.String</span></span>

## <span data-ttu-id="de996-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de996-141">OUTPUTS</span></span>

### <span data-ttu-id="de996-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="de996-142">System.Void</span></span>

## <span data-ttu-id="de996-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="de996-143">NOTES</span></span>
<span data-ttu-id="de996-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="de996-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="de996-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de996-145">RELATED LINKS</span></span>

[<span data-ttu-id="de996-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="de996-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="de996-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="de996-147">Set-AzDataFactoryV2Dataset</span></span>]()
