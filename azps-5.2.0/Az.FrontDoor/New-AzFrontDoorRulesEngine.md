---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403703"
---
# <span data-ttu-id="8016c-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8016c-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="8016c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8016c-102">SYNOPSIS</span></span>
<span data-ttu-id="8016c-103">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="8016c-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="8016c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8016c-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8016c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8016c-105">DESCRIPTION</span></span>
<span data-ttu-id="8016c-106">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="8016c-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="8016c-107">Используйте cmdlet "New-AzFrontDoorRulesEngineRule", чтобы создать правила обн., которые должны передаваться в параметр "-Rules" этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8016c-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="8016c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8016c-108">EXAMPLES</span></span>

### <span data-ttu-id="8016c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8016c-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="8016c-110">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="8016c-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="8016c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8016c-111">PARAMETERS</span></span>

### <span data-ttu-id="8016c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8016c-112">-DefaultProfile</span></span>
<span data-ttu-id="8016c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8016c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8016c-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8016c-114">-FrontDoorName</span></span>
<span data-ttu-id="8016c-115">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="8016c-115">Front Door name.</span></span>

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

### <span data-ttu-id="8016c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8016c-116">-Name</span></span>
<span data-ttu-id="8016c-117">Имя обл. правил.</span><span class="sxs-lookup"><span data-stu-id="8016c-117">Rules engine name.</span></span>

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

### <span data-ttu-id="8016c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8016c-118">-ResourceGroupName</span></span>
<span data-ttu-id="8016c-119">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="8016c-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="8016c-120">-Правило</span><span class="sxs-lookup"><span data-stu-id="8016c-120">-Rule</span></span>
<span data-ttu-id="8016c-121">Список правил, которые определяют определенную конфигурацию обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="8016c-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="8016c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8016c-122">-Confirm</span></span>
<span data-ttu-id="8016c-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8016c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8016c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8016c-124">-WhatIf</span></span>
<span data-ttu-id="8016c-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8016c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8016c-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8016c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8016c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8016c-127">CommonParameters</span></span>
<span data-ttu-id="8016c-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8016c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8016c-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8016c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8016c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8016c-130">INPUTS</span></span>

### <span data-ttu-id="8016c-131">Нет</span><span class="sxs-lookup"><span data-stu-id="8016c-131">None</span></span>

## <span data-ttu-id="8016c-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8016c-132">OUTPUTS</span></span>

### <span data-ttu-id="8016c-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8016c-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="8016c-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8016c-134">NOTES</span></span>

## <span data-ttu-id="8016c-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8016c-135">RELATED LINKS</span></span>
