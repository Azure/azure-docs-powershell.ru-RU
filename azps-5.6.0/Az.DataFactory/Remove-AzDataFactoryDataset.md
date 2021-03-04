---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 70673fd001078fbeff620f3a6a5ed7dc534ebe2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957400"
---
# <span data-ttu-id="54b75-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="54b75-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="54b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54b75-102">SYNOPSIS</span></span>
<span data-ttu-id="54b75-103">Удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="54b75-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="54b75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54b75-104">SYNTAX</span></span>

### <span data-ttu-id="54b75-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54b75-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54b75-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="54b75-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54b75-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54b75-107">DESCRIPTION</span></span>
<span data-ttu-id="54b75-108">С его использованием набор данных **Remove-AzDataFactoryDataset** удаляется из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="54b75-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="54b75-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54b75-109">EXAMPLES</span></span>

### <span data-ttu-id="54b75-110">Пример 1. Удаление наборов данных</span><span class="sxs-lookup"><span data-stu-id="54b75-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="54b75-111">Эта команда удаляет набор данных DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="54b75-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="54b75-112">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="54b75-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="54b75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54b75-113">PARAMETERS</span></span>

### <span data-ttu-id="54b75-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="54b75-114">-DataFactory</span></span>
<span data-ttu-id="54b75-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="54b75-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="54b75-116">Этот cmdlet удаляет набор данных из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="54b75-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54b75-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="54b75-117">-DataFactoryName</span></span>
<span data-ttu-id="54b75-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="54b75-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="54b75-119">Этот cmdlet удаляет набор данных из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="54b75-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="54b75-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b75-120">-DefaultProfile</span></span>
<span data-ttu-id="54b75-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="54b75-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54b75-122">-Force</span><span class="sxs-lookup"><span data-stu-id="54b75-122">-Force</span></span>
<span data-ttu-id="54b75-123">Указывает на то, что этот cmdlet удаляет набор данных без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="54b75-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="54b75-124">-Name</span><span class="sxs-lookup"><span data-stu-id="54b75-124">-Name</span></span>
<span data-ttu-id="54b75-125">Имя удаляемого наборов данных.</span><span class="sxs-lookup"><span data-stu-id="54b75-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54b75-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b75-126">-ResourceGroupName</span></span>
<span data-ttu-id="54b75-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="54b75-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="54b75-128">Этот cmdlet удаляет набор данных из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="54b75-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="54b75-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54b75-129">-Confirm</span></span>
<span data-ttu-id="54b75-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54b75-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54b75-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54b75-131">-WhatIf</span></span>
<span data-ttu-id="54b75-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54b75-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54b75-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="54b75-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54b75-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b75-134">CommonParameters</span></span>
<span data-ttu-id="54b75-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b75-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b75-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b75-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b75-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54b75-137">INPUTS</span></span>

### <span data-ttu-id="54b75-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="54b75-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="54b75-139">System.String</span><span class="sxs-lookup"><span data-stu-id="54b75-139">System.String</span></span>

## <span data-ttu-id="54b75-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54b75-140">OUTPUTS</span></span>

### <span data-ttu-id="54b75-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="54b75-141">System.Void</span></span>

## <span data-ttu-id="54b75-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54b75-142">NOTES</span></span>
* <span data-ttu-id="54b75-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="54b75-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="54b75-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54b75-144">RELATED LINKS</span></span>

[<span data-ttu-id="54b75-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="54b75-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="54b75-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="54b75-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


