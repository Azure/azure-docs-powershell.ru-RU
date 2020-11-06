---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 86330711dc9b35c85d87543d2b2ee55e9b1d4a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556716"
---
# <span data-ttu-id="3e4e7-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3e4e7-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="3e4e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4e7-103">Удаляет набор данных из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e4e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e4e7-104">SYNTAX</span></span>

### <span data-ttu-id="3e4e7-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e4e7-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e4e7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e4e7-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e4e7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e4e7-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e4e7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4e7-108">DESCRIPTION</span></span>
<span data-ttu-id="3e4e7-109">Командлет Remove-AzureRmDataFactoryV2Dataset удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="3e4e7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e4e7-110">EXAMPLES</span></span>

### <span data-ttu-id="3e4e7-111">Пример 1: удаление набора данных</span><span class="sxs-lookup"><span data-stu-id="3e4e7-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="3e4e7-112">Эта команда удаляет набор данных с именем DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="3e4e7-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="3e4e7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e4e7-114">PARAMETERS</span></span>

### <span data-ttu-id="3e4e7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3e4e7-115">-DataFactoryName</span></span>
<span data-ttu-id="3e4e7-116">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3e4e7-117">Этот командлет удаляет набор данных из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e4e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4e7-118">-DefaultProfile</span></span>
<span data-ttu-id="3e4e7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e4e7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3e4e7-120">-Force</span></span>
<span data-ttu-id="3e4e7-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3e4e7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e4e7-122">-InputObject</span></span>
<span data-ttu-id="3e4e7-123">Указывает объект набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="3e4e7-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e4e7-124">-Name</span></span>
<span data-ttu-id="3e4e7-125">Указывает имя набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="3e4e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e4e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e4e7-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3e4e7-128">Этот командлет удаляет набор данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e4e7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e4e7-129">-ResourceId</span></span>
<span data-ttu-id="3e4e7-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3e4e7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e4e7-131">-Confirm</span></span>
<span data-ttu-id="3e4e7-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e4e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e4e7-133">-WhatIf</span></span>
<span data-ttu-id="3e4e7-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3e4e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4e7-135">CommonParameters</span></span>
<span data-ttu-id="3e4e7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4e7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e4e7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4e7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e4e7-138">INPUTS</span></span>

### <span data-ttu-id="3e4e7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3e4e7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="3e4e7-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3e4e7-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3e4e7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3e4e7-141">System.String</span></span>

## <span data-ttu-id="3e4e7-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4e7-142">OUTPUTS</span></span>

### <span data-ttu-id="3e4e7-143">System. void</span><span class="sxs-lookup"><span data-stu-id="3e4e7-143">System.Void</span></span>

## <span data-ttu-id="3e4e7-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e4e7-144">NOTES</span></span>
<span data-ttu-id="3e4e7-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3e4e7-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3e4e7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e4e7-146">RELATED LINKS</span></span>

[<span data-ttu-id="3e4e7-147">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3e4e7-147">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="3e4e7-148">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3e4e7-148">Set-AzureRmDataFactoryV2Dataset</span></span>]()
