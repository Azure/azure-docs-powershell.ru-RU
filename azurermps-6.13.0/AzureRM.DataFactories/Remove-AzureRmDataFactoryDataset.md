---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: d4bb50dcc9e3f04d69131afbb7ac8b4f85e5070c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568191"
---
# <span data-ttu-id="3e4f2-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3e4f2-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="3e4f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4f2-103">Удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e4f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e4f2-104">SYNTAX</span></span>

### <span data-ttu-id="3e4f2-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e4f2-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e4f2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3e4f2-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e4f2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4f2-107">DESCRIPTION</span></span>
<span data-ttu-id="3e4f2-108">Командлет **Remove-AzureRmDataFactoryDataset** удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="3e4f2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e4f2-109">EXAMPLES</span></span>

### <span data-ttu-id="3e4f2-110">Пример 1: удаление набора данных</span><span class="sxs-lookup"><span data-stu-id="3e4f2-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="3e4f2-111">Эта команда удаляет набор данных с именем DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="3e4f2-112">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="3e4f2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e4f2-113">PARAMETERS</span></span>

### <span data-ttu-id="3e4f2-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-114">-DataFactory</span></span>
<span data-ttu-id="3e4f2-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="3e4f2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3e4f2-116">Этот командлет удаляет набор данных из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e4f2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3e4f2-117">-DataFactoryName</span></span>
<span data-ttu-id="3e4f2-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3e4f2-119">Этот командлет удаляет набор данных из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e4f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4f2-120">-DefaultProfile</span></span>
<span data-ttu-id="3e4f2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e4f2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4f2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3e4f2-122">-Force</span></span>
<span data-ttu-id="3e4f2-123">Указывает на то, что этот командлет удаляет набор данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3e4f2-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e4f2-124">-Name</span></span>
<span data-ttu-id="3e4f2-125">Указывает имя набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="3e4f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e4f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e4f2-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3e4f2-128">Этот командлет удаляет набор данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e4f2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e4f2-129">-Confirm</span></span>
<span data-ttu-id="3e4f2-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e4f2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e4f2-131">-WhatIf</span></span>
<span data-ttu-id="3e4f2-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e4f2-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e4f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4f2-134">CommonParameters</span></span>
<span data-ttu-id="3e4f2-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e4f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4f2-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e4f2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4f2-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e4f2-137">INPUTS</span></span>

### <span data-ttu-id="3e4f2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3e4f2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3e4f2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3e4f2-139">System.String</span></span>

## <span data-ttu-id="3e4f2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4f2-140">OUTPUTS</span></span>

### <span data-ttu-id="3e4f2-141">System. void</span><span class="sxs-lookup"><span data-stu-id="3e4f2-141">System.Void</span></span>

## <span data-ttu-id="3e4f2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e4f2-142">NOTES</span></span>
* <span data-ttu-id="3e4f2-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3e4f2-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3e4f2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e4f2-144">RELATED LINKS</span></span>

[<span data-ttu-id="3e4f2-145">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3e4f2-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="3e4f2-146">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3e4f2-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


