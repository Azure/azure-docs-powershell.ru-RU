---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570448"
---
# <span data-ttu-id="c6203-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c6203-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="c6203-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6203-102">SYNOPSIS</span></span>
<span data-ttu-id="c6203-103">Удаляет триггер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c6203-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6203-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6203-104">SYNTAX</span></span>

### <span data-ttu-id="c6203-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6203-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c6203-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c6203-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c6203-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6203-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c6203-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6203-108">DESCRIPTION</span></span>
<span data-ttu-id="c6203-109">Командлет **Remove-AzureRmDataFactoryV2Trigger** удаляет триггер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c6203-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="c6203-110">Если указан параметр _Force_ , командлет не выдает запрос перед удалением триггера.</span><span class="sxs-lookup"><span data-stu-id="c6203-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="c6203-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6203-111">EXAMPLES</span></span>

### <span data-ttu-id="c6203-112">Пример 1: удаление триггера</span><span class="sxs-lookup"><span data-stu-id="c6203-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="c6203-113">Удаление триггера с именем "ScheduledTrigger" из фабрики данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="c6203-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="c6203-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6203-114">PARAMETERS</span></span>

### <span data-ttu-id="c6203-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6203-115">-Confirm</span></span>
<span data-ttu-id="c6203-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6203-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6203-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c6203-117">-DataFactoryName</span></span>
<span data-ttu-id="c6203-118">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c6203-118">The data factory name.</span></span>

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

### <span data-ttu-id="c6203-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c6203-119">-Force</span></span>
<span data-ttu-id="c6203-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c6203-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c6203-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6203-121">-Name</span></span>
<span data-ttu-id="c6203-122">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="c6203-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6203-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6203-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6203-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6203-124">The resource group name.</span></span>

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

### <span data-ttu-id="c6203-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6203-125">-ResourceId</span></span>
<span data-ttu-id="c6203-126">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="c6203-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c6203-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6203-127">-InputObject</span></span>
<span data-ttu-id="c6203-128">Удаляемый объект триггера.</span><span class="sxs-lookup"><span data-stu-id="c6203-128">The Trigger object to remove.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6203-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6203-129">-WhatIf</span></span>
<span data-ttu-id="c6203-130">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="c6203-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="c6203-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6203-131">INPUTS</span></span>

### <span data-ttu-id="c6203-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="c6203-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="c6203-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c6203-133">System.String</span></span>


## <span data-ttu-id="c6203-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6203-134">OUTPUTS</span></span>

### <span data-ttu-id="c6203-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="c6203-135">System.Object</span></span>

## <span data-ttu-id="c6203-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6203-136">NOTES</span></span>

## <span data-ttu-id="c6203-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6203-137">RELATED LINKS</span></span>
[<span data-ttu-id="c6203-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c6203-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c6203-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c6203-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c6203-140">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c6203-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c6203-141">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c6203-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

