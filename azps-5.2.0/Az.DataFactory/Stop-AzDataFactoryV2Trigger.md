---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409820"
---
# <span data-ttu-id="fed93-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fed93-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="fed93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed93-102">SYNOPSIS</span></span>
<span data-ttu-id="fed93-103">Остановка триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="fed93-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="fed93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fed93-104">SYNTAX</span></span>

### <span data-ttu-id="fed93-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fed93-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed93-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fed93-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed93-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fed93-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fed93-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fed93-108">DESCRIPTION</span></span>
<span data-ttu-id="fed93-109">Для фабрики данных триггер **Stop-AzDataFactoryV2Trigger** останавливает триггер.</span><span class="sxs-lookup"><span data-stu-id="fed93-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="fed93-110">Если триггер находится в состоянии "Запущено", то триггер останавливается и перестает вызывать конвейеры.</span><span class="sxs-lookup"><span data-stu-id="fed93-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="fed93-111">Если триггер уже находится в состоянии "Остановлено", этот cmdlet не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="fed93-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="fed93-112">Если задан параметр Force, то перед остановкой триггера не запускается проектлет.</span><span class="sxs-lookup"><span data-stu-id="fed93-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="fed93-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fed93-113">EXAMPLES</span></span>

### <span data-ttu-id="fed93-114">Пример 1. Остановка триггера</span><span class="sxs-lookup"><span data-stu-id="fed93-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="fed93-115">Остановка триггера ScheduledTrigger в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="fed93-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="fed93-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fed93-116">PARAMETERS</span></span>

### <span data-ttu-id="fed93-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fed93-117">-DataFactoryName</span></span>
<span data-ttu-id="fed93-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="fed93-118">The data factory name.</span></span>

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

### <span data-ttu-id="fed93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed93-119">-DefaultProfile</span></span>
<span data-ttu-id="fed93-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fed93-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fed93-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fed93-121">-Force</span></span>
<span data-ttu-id="fed93-122">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fed93-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fed93-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fed93-123">-InputObject</span></span>
<span data-ttu-id="fed93-124">Активирует объект для запуска.</span><span class="sxs-lookup"><span data-stu-id="fed93-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="fed93-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fed93-125">-Name</span></span>
<span data-ttu-id="fed93-126">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="fed93-126">The trigger name.</span></span>

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

### <span data-ttu-id="fed93-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed93-127">-ResourceGroupName</span></span>
<span data-ttu-id="fed93-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fed93-128">The resource group name.</span></span>

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

### <span data-ttu-id="fed93-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fed93-129">-ResourceId</span></span>
<span data-ttu-id="fed93-130">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="fed93-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fed93-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fed93-131">-Confirm</span></span>
<span data-ttu-id="fed93-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fed93-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed93-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fed93-133">-WhatIf</span></span>
<span data-ttu-id="fed93-134">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fed93-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fed93-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed93-135">CommonParameters</span></span>
<span data-ttu-id="fed93-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed93-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed93-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed93-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed93-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fed93-138">INPUTS</span></span>

### <span data-ttu-id="fed93-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fed93-139">System.String</span></span>

### <span data-ttu-id="fed93-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="fed93-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="fed93-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fed93-141">OUTPUTS</span></span>

### <span data-ttu-id="fed93-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="fed93-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="fed93-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fed93-143">NOTES</span></span>

## <span data-ttu-id="fed93-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fed93-144">RELATED LINKS</span></span>

[<span data-ttu-id="fed93-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fed93-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fed93-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fed93-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fed93-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fed93-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fed93-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fed93-148">Remove-AzDataFactoryV2Trigger</span></span>]()
