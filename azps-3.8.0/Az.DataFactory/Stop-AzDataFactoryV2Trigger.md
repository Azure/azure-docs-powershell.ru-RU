---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912769"
---
# <span data-ttu-id="6bea8-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bea8-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6bea8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6bea8-102">SYNOPSIS</span></span>
<span data-ttu-id="6bea8-103">Остановка триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6bea8-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="6bea8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6bea8-104">SYNTAX</span></span>

### <span data-ttu-id="6bea8-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6bea8-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bea8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6bea8-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bea8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bea8-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bea8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bea8-108">DESCRIPTION</span></span>
<span data-ttu-id="6bea8-109">Командлет **Stop-AzDataFactoryV2Trigger** останавливает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6bea8-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="6bea8-110">Если триггер находится в состоянии "начато", этот командлет останавливает срабатывание триггера и больше не вызывает конвейеры.</span><span class="sxs-lookup"><span data-stu-id="6bea8-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="6bea8-111">Если триггер уже находится в состоянии "остановлено", этот командлет не действует.</span><span class="sxs-lookup"><span data-stu-id="6bea8-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="6bea8-112">Если указан параметр Force, командлет не выводит запрос перед остановкой триггера.</span><span class="sxs-lookup"><span data-stu-id="6bea8-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="6bea8-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6bea8-113">EXAMPLES</span></span>

### <span data-ttu-id="6bea8-114">Пример 1: остановка триггера</span><span class="sxs-lookup"><span data-stu-id="6bea8-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="6bea8-115">Останавливает триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6bea8-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="6bea8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6bea8-116">PARAMETERS</span></span>

### <span data-ttu-id="6bea8-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6bea8-117">-DataFactoryName</span></span>
<span data-ttu-id="6bea8-118">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6bea8-118">The data factory name.</span></span>

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

### <span data-ttu-id="6bea8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bea8-119">-DefaultProfile</span></span>
<span data-ttu-id="6bea8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bea8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bea8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6bea8-121">-Force</span></span>
<span data-ttu-id="6bea8-122">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6bea8-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6bea8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bea8-123">-InputObject</span></span>
<span data-ttu-id="6bea8-124">Запускаемый объект.</span><span class="sxs-lookup"><span data-stu-id="6bea8-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bea8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6bea8-125">-Name</span></span>
<span data-ttu-id="6bea8-126">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="6bea8-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bea8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bea8-127">-ResourceGroupName</span></span>
<span data-ttu-id="6bea8-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bea8-128">The resource group name.</span></span>

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

### <span data-ttu-id="6bea8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bea8-129">-ResourceId</span></span>
<span data-ttu-id="6bea8-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6bea8-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6bea8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bea8-131">-Confirm</span></span>
<span data-ttu-id="6bea8-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6bea8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bea8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bea8-133">-WhatIf</span></span>
<span data-ttu-id="6bea8-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="6bea8-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6bea8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bea8-135">CommonParameters</span></span>
<span data-ttu-id="6bea8-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6bea8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bea8-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bea8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bea8-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6bea8-138">INPUTS</span></span>

### <span data-ttu-id="6bea8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6bea8-139">System.String</span></span>

### <span data-ttu-id="6bea8-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6bea8-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="6bea8-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bea8-141">OUTPUTS</span></span>

### <span data-ttu-id="6bea8-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6bea8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="6bea8-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6bea8-143">NOTES</span></span>

## <span data-ttu-id="6bea8-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bea8-144">RELATED LINKS</span></span>

[<span data-ttu-id="6bea8-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bea8-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6bea8-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bea8-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6bea8-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bea8-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6bea8-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bea8-148">Remove-AzDataFactoryV2Trigger</span></span>]()
