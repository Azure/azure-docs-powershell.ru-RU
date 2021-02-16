---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226561"
---
# <span data-ttu-id="feaaa-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="feaaa-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="feaaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feaaa-102">SYNOPSIS</span></span>
<span data-ttu-id="feaaa-103">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="feaaa-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="feaaa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="feaaa-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="feaaa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="feaaa-105">DESCRIPTION</span></span>
<span data-ttu-id="feaaa-106">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="feaaa-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="feaaa-107">Используйте cmdlet "New-AzFrontDoorRulesEngineRule", чтобы создать правила обн., которые должны передаваться в параметр "-Rules" этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feaaa-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="feaaa-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="feaaa-108">EXAMPLES</span></span>

### <span data-ttu-id="feaaa-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="feaaa-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="feaaa-110">Создайте новую конфигурацию обдвижки правил для указанной передней двери.</span><span class="sxs-lookup"><span data-stu-id="feaaa-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="feaaa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feaaa-111">PARAMETERS</span></span>

### <span data-ttu-id="feaaa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feaaa-112">-DefaultProfile</span></span>
<span data-ttu-id="feaaa-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="feaaa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feaaa-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="feaaa-114">-FrontDoorName</span></span>
<span data-ttu-id="feaaa-115">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="feaaa-115">Front Door name.</span></span>

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

### <span data-ttu-id="feaaa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="feaaa-116">-Name</span></span>
<span data-ttu-id="feaaa-117">Имя яла правила.</span><span class="sxs-lookup"><span data-stu-id="feaaa-117">Rules engine name.</span></span>

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

### <span data-ttu-id="feaaa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feaaa-118">-ResourceGroupName</span></span>
<span data-ttu-id="feaaa-119">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="feaaa-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="feaaa-120">-Правило</span><span class="sxs-lookup"><span data-stu-id="feaaa-120">-Rule</span></span>
<span data-ttu-id="feaaa-121">Список правил, которые определяют определенную конфигурацию обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="feaaa-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="feaaa-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="feaaa-122">-Confirm</span></span>
<span data-ttu-id="feaaa-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feaaa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feaaa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feaaa-124">-WhatIf</span></span>
<span data-ttu-id="feaaa-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feaaa-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="feaaa-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="feaaa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feaaa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feaaa-127">CommonParameters</span></span>
<span data-ttu-id="feaaa-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feaaa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feaaa-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feaaa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feaaa-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="feaaa-130">INPUTS</span></span>

### <span data-ttu-id="feaaa-131">Нет</span><span class="sxs-lookup"><span data-stu-id="feaaa-131">None</span></span>

## <span data-ttu-id="feaaa-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="feaaa-132">OUTPUTS</span></span>

### <span data-ttu-id="feaaa-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="feaaa-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="feaaa-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="feaaa-134">NOTES</span></span>

## <span data-ttu-id="feaaa-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="feaaa-135">RELATED LINKS</span></span>
