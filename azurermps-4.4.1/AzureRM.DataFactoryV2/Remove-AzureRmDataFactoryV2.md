---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734070"
---
# <span data-ttu-id="3464c-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3464c-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="3464c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3464c-102">SYNOPSIS</span></span>
<span data-ttu-id="3464c-103">Удаление фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3464c-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3464c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3464c-104">SYNTAX</span></span>

### <span data-ttu-id="3464c-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3464c-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3464c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3464c-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3464c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3464c-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3464c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3464c-108">DESCRIPTION</span></span>
<span data-ttu-id="3464c-109">Командлет Remove-AzureRmDataFactoryV2 удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="3464c-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="3464c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3464c-110">EXAMPLES</span></span>

### <span data-ttu-id="3464c-111">Пример 1: удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="3464c-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="3464c-112">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="3464c-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="3464c-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="3464c-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="3464c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3464c-114">PARAMETERS</span></span>

### <span data-ttu-id="3464c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3464c-115">-Confirm</span></span>
<span data-ttu-id="3464c-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3464c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3464c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3464c-117">-InputObject</span></span>
<span data-ttu-id="3464c-118">Указывает удаляемый объект факта.</span><span class="sxs-lookup"><span data-stu-id="3464c-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3464c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3464c-119">-Force</span></span>
<span data-ttu-id="3464c-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3464c-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3464c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3464c-121">-Name</span></span>
<span data-ttu-id="3464c-122">Указывает имя удаляемой фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3464c-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3464c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3464c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3464c-124">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3464c-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3464c-125">Этот командлет удаляет фабрику данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3464c-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3464c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3464c-126">-ResourceId</span></span>
<span data-ttu-id="3464c-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="3464c-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3464c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3464c-128">-WhatIf</span></span>
<span data-ttu-id="3464c-129">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="3464c-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="3464c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3464c-130">INPUTS</span></span>

### <span data-ttu-id="3464c-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3464c-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="3464c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3464c-132">System.String</span></span>


## <span data-ttu-id="3464c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3464c-133">OUTPUTS</span></span>

### <span data-ttu-id="3464c-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="3464c-134">System.Object</span></span>

## <span data-ttu-id="3464c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3464c-135">NOTES</span></span>
<span data-ttu-id="3464c-136">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3464c-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3464c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3464c-137">RELATED LINKS</span></span>
[<span data-ttu-id="3464c-138">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3464c-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="3464c-139">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3464c-139">Set-AzureRmDataFactoryV2</span></span>]()
