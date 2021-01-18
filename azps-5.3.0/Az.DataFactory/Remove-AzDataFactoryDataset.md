---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508482"
---
# <span data-ttu-id="9d7cf-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="9d7cf-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="9d7cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7cf-103">Удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="9d7cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d7cf-104">SYNTAX</span></span>

### <span data-ttu-id="9d7cf-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d7cf-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d7cf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9d7cf-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d7cf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d7cf-107">DESCRIPTION</span></span>
<span data-ttu-id="9d7cf-108">При **этом набор данных Remove-AzDataFactoryDataset** удаляется из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="9d7cf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d7cf-109">EXAMPLES</span></span>

### <span data-ttu-id="9d7cf-110">Пример 1. Удаление наборов данных</span><span class="sxs-lookup"><span data-stu-id="9d7cf-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="9d7cf-111">Эта команда удаляет набор данных DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="9d7cf-112">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="9d7cf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d7cf-113">PARAMETERS</span></span>

### <span data-ttu-id="9d7cf-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9d7cf-114">-DataFactory</span></span>
<span data-ttu-id="9d7cf-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="9d7cf-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9d7cf-116">Этот cmdlet удаляет набор данных из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7cf-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9d7cf-117">-DataFactoryName</span></span>
<span data-ttu-id="9d7cf-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9d7cf-119">Этот cmdlet удаляет набор данных из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7cf-120">-DefaultProfile</span></span>
<span data-ttu-id="9d7cf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9d7cf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d7cf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9d7cf-122">-Force</span></span>
<span data-ttu-id="9d7cf-123">Указывает на то, что этот cmdlet удаляет набор данных без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9d7cf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9d7cf-124">-Name</span></span>
<span data-ttu-id="9d7cf-125">Имя удаляемого наборов данных.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="9d7cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d7cf-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9d7cf-128">Этот cmdlet удаляет набор данных из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7cf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d7cf-129">-Confirm</span></span>
<span data-ttu-id="9d7cf-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d7cf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d7cf-131">-WhatIf</span></span>
<span data-ttu-id="9d7cf-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d7cf-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d7cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7cf-134">CommonParameters</span></span>
<span data-ttu-id="9d7cf-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7cf-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7cf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7cf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d7cf-137">INPUTS</span></span>

### <span data-ttu-id="9d7cf-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9d7cf-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9d7cf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9d7cf-139">System.String</span></span>

## <span data-ttu-id="9d7cf-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d7cf-140">OUTPUTS</span></span>

### <span data-ttu-id="9d7cf-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="9d7cf-141">System.Void</span></span>

## <span data-ttu-id="9d7cf-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d7cf-142">NOTES</span></span>
* <span data-ttu-id="9d7cf-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="9d7cf-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9d7cf-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d7cf-144">RELATED LINKS</span></span>

[<span data-ttu-id="9d7cf-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="9d7cf-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="9d7cf-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="9d7cf-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


