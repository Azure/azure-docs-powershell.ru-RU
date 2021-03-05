---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 7f24d7a7fc027e8d4411b12a3f04d24121af5354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969139"
---
# <span data-ttu-id="404ee-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="404ee-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="404ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="404ee-102">SYNOPSIS</span></span>
<span data-ttu-id="404ee-103">Обновив обл. правил.</span><span class="sxs-lookup"><span data-stu-id="404ee-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="404ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="404ee-104">SYNTAX</span></span>

### <span data-ttu-id="404ee-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="404ee-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="404ee-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="404ee-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="404ee-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="404ee-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="404ee-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="404ee-108">DESCRIPTION</span></span>
<span data-ttu-id="404ee-109">Обновив обл. правил.</span><span class="sxs-lookup"><span data-stu-id="404ee-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="404ee-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="404ee-110">EXAMPLES</span></span>

### <span data-ttu-id="404ee-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="404ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="404ee-112">Получите существующую конфигурацию яла правил и добавьте в нее еще одно правило.</span><span class="sxs-lookup"><span data-stu-id="404ee-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="404ee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="404ee-113">PARAMETERS</span></span>

### <span data-ttu-id="404ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404ee-114">-DefaultProfile</span></span>
<span data-ttu-id="404ee-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="404ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="404ee-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="404ee-116">-FrontDoorName</span></span>
<span data-ttu-id="404ee-117">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="404ee-117">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="404ee-118">-InputObject</span></span>
<span data-ttu-id="404ee-119">Объект обновимой обл. правил.</span><span class="sxs-lookup"><span data-stu-id="404ee-119">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="404ee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="404ee-120">-Name</span></span>
<span data-ttu-id="404ee-121">Имя яла правила.</span><span class="sxs-lookup"><span data-stu-id="404ee-121">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="404ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="404ee-123">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="404ee-123">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="404ee-124">-ResourceId</span></span>
<span data-ttu-id="404ee-125">ИД ресурса для обновления правил (английского)</span><span class="sxs-lookup"><span data-stu-id="404ee-125">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ee-126">-Правило</span><span class="sxs-lookup"><span data-stu-id="404ee-126">-Rule</span></span>
<span data-ttu-id="404ee-127">Список правил, которые определяют определенную конфигурацию обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="404ee-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ee-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="404ee-128">-Confirm</span></span>
<span data-ttu-id="404ee-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="404ee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="404ee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404ee-130">-WhatIf</span></span>
<span data-ttu-id="404ee-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404ee-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="404ee-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="404ee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="404ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404ee-133">CommonParameters</span></span>
<span data-ttu-id="404ee-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404ee-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="404ee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404ee-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="404ee-136">INPUTS</span></span>

### <span data-ttu-id="404ee-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="404ee-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="404ee-138">System.String</span><span class="sxs-lookup"><span data-stu-id="404ee-138">System.String</span></span>

## <span data-ttu-id="404ee-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="404ee-139">OUTPUTS</span></span>

### <span data-ttu-id="404ee-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="404ee-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="404ee-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="404ee-141">NOTES</span></span>

## <span data-ttu-id="404ee-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="404ee-142">RELATED LINKS</span></span>
