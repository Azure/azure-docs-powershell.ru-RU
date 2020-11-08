---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077761"
---
# <span data-ttu-id="8de2d-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8de2d-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="8de2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8de2d-102">SYNOPSIS</span></span>
<span data-ttu-id="8de2d-103">Создайте новую конфигурацию обработчика правил для заданной передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8de2d-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="8de2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8de2d-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8de2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8de2d-105">DESCRIPTION</span></span>
<span data-ttu-id="8de2d-106">Создайте новую конфигурацию обработчика правил для заданной передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8de2d-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="8de2d-107">Используйте командлет "New-AzFrontDoorRulesEngineRule", чтобы создать правила обработчика правил, чтобы передать параметр "-Rules" этого командлета.</span><span class="sxs-lookup"><span data-stu-id="8de2d-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="8de2d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8de2d-108">EXAMPLES</span></span>

### <span data-ttu-id="8de2d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8de2d-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="8de2d-110">Создайте новую конфигурацию обработчика правил для заданной передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8de2d-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="8de2d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8de2d-111">PARAMETERS</span></span>

### <span data-ttu-id="8de2d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de2d-112">-DefaultProfile</span></span>
<span data-ttu-id="8de2d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8de2d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de2d-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8de2d-114">-FrontDoorName</span></span>
<span data-ttu-id="8de2d-115">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8de2d-115">Front Door name.</span></span>

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

### <span data-ttu-id="8de2d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8de2d-116">-Name</span></span>
<span data-ttu-id="8de2d-117">Имя обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="8de2d-117">Rules engine name.</span></span>

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

### <span data-ttu-id="8de2d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de2d-118">-ResourceGroupName</span></span>
<span data-ttu-id="8de2d-119">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="8de2d-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="8de2d-120">-Правило</span><span class="sxs-lookup"><span data-stu-id="8de2d-120">-Rule</span></span>
<span data-ttu-id="8de2d-121">Список правил, определяющих определенную конфигурацию обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="8de2d-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="8de2d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8de2d-122">-Confirm</span></span>
<span data-ttu-id="8de2d-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8de2d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de2d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de2d-124">-WhatIf</span></span>
<span data-ttu-id="8de2d-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8de2d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8de2d-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8de2d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de2d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de2d-127">CommonParameters</span></span>
<span data-ttu-id="8de2d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8de2d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de2d-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8de2d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de2d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8de2d-130">INPUTS</span></span>

### <span data-ttu-id="8de2d-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="8de2d-131">None</span></span>

## <span data-ttu-id="8de2d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8de2d-132">OUTPUTS</span></span>

### <span data-ttu-id="8de2d-133">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8de2d-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="8de2d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="8de2d-134">NOTES</span></span>

## <span data-ttu-id="8de2d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8de2d-135">RELATED LINKS</span></span>
