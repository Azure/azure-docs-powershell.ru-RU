---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568079"
---
# <span data-ttu-id="d60d6-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d60d6-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="d60d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d60d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d60d6-103">Удаляет набор данных из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d60d6-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d60d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d60d6-104">SYNTAX</span></span>

### <span data-ttu-id="d60d6-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d60d6-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d60d6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d60d6-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d60d6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d60d6-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d60d6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d60d6-108">DESCRIPTION</span></span>
<span data-ttu-id="d60d6-109">Командлет Remove-AzureRmDataFactoryV2Dataset удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d60d6-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="d60d6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d60d6-110">EXAMPLES</span></span>

### <span data-ttu-id="d60d6-111">Пример 1: удаление набора данных</span><span class="sxs-lookup"><span data-stu-id="d60d6-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="d60d6-112">Эта команда удаляет набор данных с именем DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d60d6-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="d60d6-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="d60d6-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="d60d6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d60d6-114">PARAMETERS</span></span>

### <span data-ttu-id="d60d6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d60d6-115">-Confirm</span></span>
<span data-ttu-id="d60d6-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d60d6-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d60d6-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d60d6-117">-DataFactoryName</span></span>
<span data-ttu-id="d60d6-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d60d6-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d60d6-119">Этот командлет удаляет набор данных из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d60d6-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d60d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d60d6-120">-InputObject</span></span>
<span data-ttu-id="d60d6-121">Указывает объект набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d60d6-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d60d6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d60d6-122">-Force</span></span>
<span data-ttu-id="d60d6-123">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d60d6-123">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d60d6-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d60d6-124">-Name</span></span>
<span data-ttu-id="d60d6-125">Указывает имя набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d60d6-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d60d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d60d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="d60d6-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d60d6-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d60d6-128">Этот командлет удаляет набор данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d60d6-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d60d6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d60d6-129">-ResourceId</span></span>
<span data-ttu-id="d60d6-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="d60d6-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d60d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d60d6-131">-WhatIf</span></span>
<span data-ttu-id="d60d6-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="d60d6-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d60d6-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d60d6-133">INPUTS</span></span>

### <span data-ttu-id="d60d6-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="d60d6-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="d60d6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d60d6-135">System.String</span></span>


## <span data-ttu-id="d60d6-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d60d6-136">OUTPUTS</span></span>

### <span data-ttu-id="d60d6-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="d60d6-137">System.Object</span></span>

## <span data-ttu-id="d60d6-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d60d6-138">NOTES</span></span>
<span data-ttu-id="d60d6-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="d60d6-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d60d6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d60d6-140">RELATED LINKS</span></span>
[<span data-ttu-id="d60d6-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d60d6-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="d60d6-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d60d6-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
