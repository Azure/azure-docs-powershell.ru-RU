---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245438"
---
# <span data-ttu-id="3b893-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3b893-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="3b893-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b893-102">SYNOPSIS</span></span>
<span data-ttu-id="3b893-103">Обновите обработчик правил.</span><span class="sxs-lookup"><span data-stu-id="3b893-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="3b893-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b893-104">SYNTAX</span></span>

### <span data-ttu-id="3b893-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b893-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b893-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b893-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b893-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b893-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b893-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b893-108">DESCRIPTION</span></span>
<span data-ttu-id="3b893-109">Обновите обработчик правил.</span><span class="sxs-lookup"><span data-stu-id="3b893-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="3b893-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b893-110">EXAMPLES</span></span>

### <span data-ttu-id="3b893-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b893-111">Example 1</span></span>
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

<span data-ttu-id="3b893-112">Получите существующую конфигурацию обработчика правил и добавьте в нее другое правило обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="3b893-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="3b893-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b893-113">PARAMETERS</span></span>

### <span data-ttu-id="3b893-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b893-114">-DefaultProfile</span></span>
<span data-ttu-id="3b893-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b893-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b893-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3b893-116">-FrontDoorName</span></span>
<span data-ttu-id="3b893-117">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="3b893-117">Front Door name.</span></span>

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

### <span data-ttu-id="3b893-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b893-118">-InputObject</span></span>
<span data-ttu-id="3b893-119">Обновляемый объект обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="3b893-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="3b893-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b893-120">-Name</span></span>
<span data-ttu-id="3b893-121">Имя обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="3b893-121">Rules engine name.</span></span>

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

### <span data-ttu-id="3b893-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b893-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b893-123">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="3b893-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="3b893-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b893-124">-ResourceId</span></span>
<span data-ttu-id="3b893-125">ИД ресурса обновляемого RulesEngine</span><span class="sxs-lookup"><span data-stu-id="3b893-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="3b893-126">-Правило</span><span class="sxs-lookup"><span data-stu-id="3b893-126">-Rule</span></span>
<span data-ttu-id="3b893-127">Список правил, определяющих определенную конфигурацию обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="3b893-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="3b893-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b893-128">-Confirm</span></span>
<span data-ttu-id="3b893-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b893-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b893-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b893-130">-WhatIf</span></span>
<span data-ttu-id="3b893-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b893-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b893-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b893-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b893-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b893-133">CommonParameters</span></span>
<span data-ttu-id="3b893-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b893-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b893-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b893-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b893-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b893-136">INPUTS</span></span>

### <span data-ttu-id="3b893-137">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3b893-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="3b893-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3b893-138">System.String</span></span>

## <span data-ttu-id="3b893-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b893-139">OUTPUTS</span></span>

### <span data-ttu-id="3b893-140">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3b893-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="3b893-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b893-141">NOTES</span></span>

## <span data-ttu-id="3b893-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b893-142">RELATED LINKS</span></span>
