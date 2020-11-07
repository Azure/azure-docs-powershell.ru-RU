---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3054824876ccaff24f319ae14c704cd975e79434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733774"
---
# <span data-ttu-id="a6795-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a6795-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="a6795-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6795-102">SYNOPSIS</span></span>

<span data-ttu-id="a6795-103">Остановка триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a6795-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6795-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6795-104">SYNTAX</span></span>

### <span data-ttu-id="a6795-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6795-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a6795-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6795-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a6795-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6795-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a6795-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6795-108">DESCRIPTION</span></span>

<span data-ttu-id="a6795-109">Командлет **Stop-AzureRmDataFactoryV2Trigger** останавливает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a6795-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="a6795-110">Если триггер находится в состоянии "начато", этот командлет останавливает срабатывание триггера и больше не вызывает конвейеры.</span><span class="sxs-lookup"><span data-stu-id="a6795-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="a6795-111">Если триггер уже находится в состоянии "остановлено", этот командлет не действует.</span><span class="sxs-lookup"><span data-stu-id="a6795-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="a6795-112">Если указан параметр Force, командлет не выводит запрос перед остановкой триггера.</span><span class="sxs-lookup"><span data-stu-id="a6795-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>


## <span data-ttu-id="a6795-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6795-113">EXAMPLES</span></span>

### <span data-ttu-id="a6795-114">Пример 1: остановка триггера</span><span class="sxs-lookup"><span data-stu-id="a6795-114">Example 1: Stop a trigger</span></span>

```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="a6795-115">Останавливает триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a6795-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="a6795-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6795-116">PARAMETERS</span></span>

### <span data-ttu-id="a6795-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6795-117">-Confirm</span></span>
<span data-ttu-id="a6795-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6795-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6795-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a6795-119">-DataFactoryName</span></span>
<span data-ttu-id="a6795-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a6795-120">The data factory name.</span></span>

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

### <span data-ttu-id="a6795-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a6795-121">-Force</span></span>
<span data-ttu-id="a6795-122">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a6795-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a6795-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6795-123">-Name</span></span>
<span data-ttu-id="a6795-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="a6795-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6795-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6795-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6795-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6795-126">The resource group name.</span></span>

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

### <span data-ttu-id="a6795-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6795-127">-ResourceId</span></span>
<span data-ttu-id="a6795-128">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="a6795-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a6795-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6795-129">-InputObject</span></span>
<span data-ttu-id="a6795-130">Запускаемый объект.</span><span class="sxs-lookup"><span data-stu-id="a6795-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="a6795-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6795-131">-WhatIf</span></span>
<span data-ttu-id="a6795-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="a6795-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="a6795-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6795-133">INPUTS</span></span>

### <span data-ttu-id="a6795-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6795-134">System.String</span></span>
<span data-ttu-id="a6795-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a6795-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="a6795-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6795-136">OUTPUTS</span></span>

### <span data-ttu-id="a6795-137">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="a6795-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a6795-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a6795-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="a6795-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6795-139">NOTES</span></span>

## <span data-ttu-id="a6795-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6795-140">RELATED LINKS</span></span>
[<span data-ttu-id="a6795-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a6795-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a6795-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a6795-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a6795-143">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a6795-143">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a6795-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a6795-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
