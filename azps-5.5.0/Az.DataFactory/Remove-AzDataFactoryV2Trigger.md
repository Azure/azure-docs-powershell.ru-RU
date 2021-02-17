---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232900"
---
# <span data-ttu-id="5b461-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b461-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5b461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b461-102">SYNOPSIS</span></span>
<span data-ttu-id="5b461-103">Удаляет триггер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5b461-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="5b461-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b461-104">SYNTAX</span></span>

### <span data-ttu-id="5b461-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b461-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b461-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b461-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b461-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b461-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b461-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b461-108">DESCRIPTION</span></span>
<span data-ttu-id="5b461-109">Для удаления триггера из фабрики данных удаляется триггер **Remove-AzDataFactoryV2Trigger.**</span><span class="sxs-lookup"><span data-stu-id="5b461-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="5b461-110">Если задан параметр _Force,_ то перед удалением триггера не будет ничего предложено.</span><span class="sxs-lookup"><span data-stu-id="5b461-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="5b461-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b461-111">EXAMPLES</span></span>

### <span data-ttu-id="5b461-112">Пример 1. Удаление триггера</span><span class="sxs-lookup"><span data-stu-id="5b461-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5b461-113">Удалите триггер ScheduledTrigger из фабрики данных WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5b461-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="5b461-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b461-114">PARAMETERS</span></span>

### <span data-ttu-id="5b461-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5b461-115">-DataFactoryName</span></span>
<span data-ttu-id="5b461-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5b461-116">The data factory name.</span></span>

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

### <span data-ttu-id="5b461-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b461-117">-DefaultProfile</span></span>
<span data-ttu-id="5b461-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b461-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b461-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b461-119">-Force</span></span>
<span data-ttu-id="5b461-120">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5b461-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5b461-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b461-121">-InputObject</span></span>
<span data-ttu-id="5b461-122">Объект-триггер, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5b461-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="5b461-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5b461-123">-Name</span></span>
<span data-ttu-id="5b461-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="5b461-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b461-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b461-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b461-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b461-126">The resource group name.</span></span>

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

### <span data-ttu-id="5b461-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b461-127">-ResourceId</span></span>
<span data-ttu-id="5b461-128">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="5b461-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5b461-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b461-129">-Confirm</span></span>
<span data-ttu-id="5b461-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5b461-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b461-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b461-131">-WhatIf</span></span>
<span data-ttu-id="5b461-132">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b461-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5b461-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b461-133">CommonParameters</span></span>
<span data-ttu-id="5b461-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b461-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b461-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b461-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b461-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b461-136">INPUTS</span></span>

### <span data-ttu-id="5b461-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5b461-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="5b461-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5b461-138">System.String</span></span>

## <span data-ttu-id="5b461-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b461-139">OUTPUTS</span></span>

### <span data-ttu-id="5b461-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b461-140">System.Boolean</span></span>

## <span data-ttu-id="5b461-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b461-141">NOTES</span></span>

## <span data-ttu-id="5b461-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b461-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b461-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b461-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b461-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b461-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b461-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b461-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b461-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b461-146">Stop-AzDataFactoryV2Trigger</span></span>]()

