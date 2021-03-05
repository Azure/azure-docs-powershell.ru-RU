---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 05248a299b907c74f43edddb7caf18697794dc08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970979"
---
# <span data-ttu-id="30a66-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="30a66-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="30a66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a66-102">SYNOPSIS</span></span>
<span data-ttu-id="30a66-103">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="30a66-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="30a66-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30a66-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30a66-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30a66-105">DESCRIPTION</span></span>
<span data-ttu-id="30a66-106">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="30a66-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="30a66-107">Используйте cmdlet "New-AzFrontDoorRulesEngineRule", чтобы создать правила обн., которые должны передаваться в параметр "-Rules" этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a66-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="30a66-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30a66-108">EXAMPLES</span></span>

### <span data-ttu-id="30a66-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30a66-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="30a66-110">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="30a66-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="30a66-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30a66-111">PARAMETERS</span></span>

### <span data-ttu-id="30a66-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a66-112">-DefaultProfile</span></span>
<span data-ttu-id="30a66-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30a66-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a66-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="30a66-114">-FrontDoorName</span></span>
<span data-ttu-id="30a66-115">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="30a66-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a66-116">-Name</span><span class="sxs-lookup"><span data-stu-id="30a66-116">-Name</span></span>
<span data-ttu-id="30a66-117">Имя яла правила.</span><span class="sxs-lookup"><span data-stu-id="30a66-117">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a66-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a66-118">-ResourceGroupName</span></span>
<span data-ttu-id="30a66-119">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="30a66-119">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a66-120">-Правило</span><span class="sxs-lookup"><span data-stu-id="30a66-120">-Rule</span></span>
<span data-ttu-id="30a66-121">Список правил, которые определяют определенную конфигурацию обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="30a66-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="30a66-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30a66-122">-Confirm</span></span>
<span data-ttu-id="30a66-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="30a66-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a66-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a66-124">-WhatIf</span></span>
<span data-ttu-id="30a66-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a66-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30a66-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30a66-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a66-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a66-127">CommonParameters</span></span>
<span data-ttu-id="30a66-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a66-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a66-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30a66-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a66-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30a66-130">INPUTS</span></span>

### <span data-ttu-id="30a66-131">Нет</span><span class="sxs-lookup"><span data-stu-id="30a66-131">None</span></span>

## <span data-ttu-id="30a66-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30a66-132">OUTPUTS</span></span>

### <span data-ttu-id="30a66-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="30a66-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="30a66-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30a66-134">NOTES</span></span>

## <span data-ttu-id="30a66-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30a66-135">RELATED LINKS</span></span>
