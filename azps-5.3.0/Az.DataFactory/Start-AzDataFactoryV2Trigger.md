---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518886"
---
# <span data-ttu-id="ba487-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ba487-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="ba487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba487-102">SYNOPSIS</span></span>
<span data-ttu-id="ba487-103">Запуск триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="ba487-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="ba487-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba487-104">SYNTAX</span></span>

### <span data-ttu-id="ba487-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba487-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba487-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ba487-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba487-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba487-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba487-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba487-108">DESCRIPTION</span></span>
<span data-ttu-id="ba487-109">Для запуска триггера в фабрике данных запускается триггер **Start-AzDataFactoryV2Trigger.**</span><span class="sxs-lookup"><span data-stu-id="ba487-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="ba487-110">Если триггер находится в состоянии "Остановлено", запускается триггер и в конечном итоге запускается конвейеры на основе его определения.</span><span class="sxs-lookup"><span data-stu-id="ba487-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="ba487-111">Если триггер уже находится в состоянии "Запущено", этот cmdlet не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="ba487-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="ba487-112">Если задан параметр Force, то перед запуском триггера не запускается проектлет.</span><span class="sxs-lookup"><span data-stu-id="ba487-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="ba487-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba487-113">EXAMPLES</span></span>

### <span data-ttu-id="ba487-114">Пример 1. Запуск триггера</span><span class="sxs-lookup"><span data-stu-id="ba487-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ba487-115">Запуск триггера ScheduledTrigger в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="ba487-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="ba487-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba487-116">PARAMETERS</span></span>

### <span data-ttu-id="ba487-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ba487-117">-DataFactoryName</span></span>
<span data-ttu-id="ba487-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ba487-118">The data factory name.</span></span>

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

### <span data-ttu-id="ba487-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba487-119">-DefaultProfile</span></span>
<span data-ttu-id="ba487-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba487-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba487-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ba487-121">-Force</span></span>
<span data-ttu-id="ba487-122">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ba487-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ba487-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba487-123">-InputObject</span></span>
<span data-ttu-id="ba487-124">Активирует объект для запуска.</span><span class="sxs-lookup"><span data-stu-id="ba487-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="ba487-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ba487-125">-Name</span></span>
<span data-ttu-id="ba487-126">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="ba487-126">The trigger name.</span></span>

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

### <span data-ttu-id="ba487-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba487-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba487-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba487-128">The resource group name.</span></span>

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

### <span data-ttu-id="ba487-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba487-129">-ResourceId</span></span>
<span data-ttu-id="ba487-130">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="ba487-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ba487-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba487-131">-Confirm</span></span>
<span data-ttu-id="ba487-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba487-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba487-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba487-133">-WhatIf</span></span>
<span data-ttu-id="ba487-134">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba487-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ba487-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba487-135">CommonParameters</span></span>
<span data-ttu-id="ba487-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba487-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba487-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba487-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba487-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba487-138">INPUTS</span></span>

### <span data-ttu-id="ba487-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ba487-139">System.String</span></span>

### <span data-ttu-id="ba487-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="ba487-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="ba487-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba487-141">OUTPUTS</span></span>

### <span data-ttu-id="ba487-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="ba487-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="ba487-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba487-143">NOTES</span></span>

## <span data-ttu-id="ba487-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba487-144">RELATED LINKS</span></span>

[<span data-ttu-id="ba487-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ba487-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ba487-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ba487-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ba487-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ba487-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ba487-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ba487-148">Remove-AzDataFactoryV2Trigger</span></span>]()
