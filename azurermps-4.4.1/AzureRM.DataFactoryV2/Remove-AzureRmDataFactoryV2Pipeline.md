---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570451"
---
# <span data-ttu-id="03df3-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="03df3-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="03df3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03df3-102">SYNOPSIS</span></span>
<span data-ttu-id="03df3-103">Удаляет конвейер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="03df3-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03df3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03df3-104">SYNTAX</span></span>

### <span data-ttu-id="03df3-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03df3-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="03df3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03df3-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="03df3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03df3-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="03df3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03df3-108">DESCRIPTION</span></span>
<span data-ttu-id="03df3-109">Командлет Remove-AzureRmDataFactoryV2Pipeline удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="03df3-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="03df3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03df3-110">EXAMPLES</span></span>

### <span data-ttu-id="03df3-111">Пример 1: удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="03df3-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="03df3-112">Этот командлет удаляет конвейер с именем DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="03df3-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="03df3-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="03df3-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="03df3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03df3-114">PARAMETERS</span></span>

### <span data-ttu-id="03df3-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03df3-115">-Confirm</span></span>
<span data-ttu-id="03df3-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03df3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03df3-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="03df3-117">-DataFactoryName</span></span>
<span data-ttu-id="03df3-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="03df3-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="03df3-119">Этот командлет удаляет конвейер из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="03df3-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="03df3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="03df3-120">-Force</span></span>
<span data-ttu-id="03df3-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="03df3-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="03df3-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03df3-122">-Name</span></span>
<span data-ttu-id="03df3-123">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="03df3-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03df3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03df3-124">-InputObject</span></span>
<span data-ttu-id="03df3-125">Указывает объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="03df3-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="03df3-126">Этот командлет удаляет конвейер, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="03df3-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03df3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03df3-127">-ResourceGroupName</span></span>
<span data-ttu-id="03df3-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="03df3-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="03df3-129">Этот командлет удаляет конвейер из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="03df3-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="03df3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03df3-130">-ResourceId</span></span>
<span data-ttu-id="03df3-131">Идентификатор ресурса Azure для конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="03df3-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="03df3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03df3-132">-WhatIf</span></span>
<span data-ttu-id="03df3-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="03df3-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="03df3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03df3-134">INPUTS</span></span>

### <span data-ttu-id="03df3-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="03df3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="03df3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="03df3-136">System.String</span></span>


## <span data-ttu-id="03df3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03df3-137">OUTPUTS</span></span>

### <span data-ttu-id="03df3-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="03df3-138">System.Object</span></span>

## <span data-ttu-id="03df3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="03df3-139">NOTES</span></span>
<span data-ttu-id="03df3-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="03df3-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="03df3-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03df3-141">RELATED LINKS</span></span>
[<span data-ttu-id="03df3-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="03df3-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="03df3-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="03df3-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="03df3-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="03df3-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

