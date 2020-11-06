---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570452"
---
# <span data-ttu-id="a1028-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a1028-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="a1028-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1028-102">SYNOPSIS</span></span>
<span data-ttu-id="a1028-103">Удаляет связанную службу из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a1028-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1028-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1028-104">SYNTAX</span></span>

### <span data-ttu-id="a1028-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1028-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a1028-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1028-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a1028-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1028-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a1028-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1028-108">DESCRIPTION</span></span>
<span data-ttu-id="a1028-109">Командлет Remove-AzureRmDataFactoryV2LinkedService Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a1028-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="a1028-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1028-110">EXAMPLES</span></span>

### <span data-ttu-id="a1028-111">Пример 1: удаление связанной службы</span><span class="sxs-lookup"><span data-stu-id="a1028-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="a1028-112">Эта команда удаляет связанную службу с именем LinkedServiceTest из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a1028-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="a1028-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="a1028-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="a1028-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1028-114">PARAMETERS</span></span>

### <span data-ttu-id="a1028-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1028-115">-Confirm</span></span>
<span data-ttu-id="a1028-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1028-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1028-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a1028-117">-DataFactoryName</span></span>
<span data-ttu-id="a1028-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a1028-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a1028-119">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a1028-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1028-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a1028-120">-Force</span></span>
<span data-ttu-id="a1028-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a1028-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a1028-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1028-122">-InputObject</span></span>
<span data-ttu-id="a1028-123">Указывает объект LinkedService, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a1028-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1028-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1028-124">-Name</span></span>
<span data-ttu-id="a1028-125">Указывает имя связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a1028-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="a1028-126">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="a1028-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1028-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1028-127">-ResourceGroupName</span></span>
<span data-ttu-id="a1028-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a1028-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a1028-129">Этот командлет удаляет связанную службу из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a1028-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="a1028-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1028-130">-ResourceId</span></span>
<span data-ttu-id="a1028-131">Идентификатор ресурса Azure связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a1028-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="a1028-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1028-132">-WhatIf</span></span>
<span data-ttu-id="a1028-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="a1028-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="a1028-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1028-134">INPUTS</span></span>

### <span data-ttu-id="a1028-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a1028-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="a1028-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a1028-136">System.String</span></span>


## <span data-ttu-id="a1028-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1028-137">OUTPUTS</span></span>

### <span data-ttu-id="a1028-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="a1028-138">System.Object</span></span>

## <span data-ttu-id="a1028-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1028-139">NOTES</span></span>
<span data-ttu-id="a1028-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="a1028-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a1028-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1028-141">RELATED LINKS</span></span>
[<span data-ttu-id="a1028-142">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a1028-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="a1028-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a1028-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

