---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245440"
---
# <span data-ttu-id="2580e-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="2580e-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="2580e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2580e-102">SYNOPSIS</span></span>
<span data-ttu-id="2580e-103">Удаление обработчика правил с передней дверцы</span><span class="sxs-lookup"><span data-stu-id="2580e-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="2580e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2580e-104">SYNTAX</span></span>

### <span data-ttu-id="2580e-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2580e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2580e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2580e-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2580e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2580e-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2580e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2580e-108">DESCRIPTION</span></span>
<span data-ttu-id="2580e-109">Удаление обработчика правил с передней дверцы</span><span class="sxs-lookup"><span data-stu-id="2580e-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="2580e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2580e-110">EXAMPLES</span></span>

### <span data-ttu-id="2580e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2580e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="2580e-112">Удалите конфигурацию обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="2580e-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="2580e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2580e-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="2580e-114">Ожидаемый результат при удалении несуществующей конфигурации обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="2580e-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="2580e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2580e-115">PARAMETERS</span></span>

### <span data-ttu-id="2580e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2580e-116">-DefaultProfile</span></span>
<span data-ttu-id="2580e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2580e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2580e-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="2580e-118">-FrontDoorName</span></span>
<span data-ttu-id="2580e-119">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="2580e-119">Front Door name.</span></span>

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

### <span data-ttu-id="2580e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2580e-120">-InputObject</span></span>
<span data-ttu-id="2580e-121">Обновляемый объект обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="2580e-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="2580e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2580e-122">-Name</span></span>
<span data-ttu-id="2580e-123">Имя обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="2580e-123">Rules engine name.</span></span>

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

### <span data-ttu-id="2580e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2580e-124">-PassThru</span></span>
<span data-ttu-id="2580e-125">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="2580e-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="2580e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2580e-126">-ResourceGroupName</span></span>
<span data-ttu-id="2580e-127">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="2580e-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="2580e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2580e-128">-ResourceId</span></span>
<span data-ttu-id="2580e-129">ИД ресурса обновляемого RulesEngine</span><span class="sxs-lookup"><span data-stu-id="2580e-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="2580e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2580e-130">-Confirm</span></span>
<span data-ttu-id="2580e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2580e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2580e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2580e-132">-WhatIf</span></span>
<span data-ttu-id="2580e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2580e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2580e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2580e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2580e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2580e-135">CommonParameters</span></span>
<span data-ttu-id="2580e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2580e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2580e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2580e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2580e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2580e-138">INPUTS</span></span>

### <span data-ttu-id="2580e-139">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="2580e-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="2580e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2580e-140">System.String</span></span>

## <span data-ttu-id="2580e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2580e-141">OUTPUTS</span></span>

### <span data-ttu-id="2580e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2580e-142">System.Boolean</span></span>

## <span data-ttu-id="2580e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2580e-143">NOTES</span></span>

## <span data-ttu-id="2580e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2580e-144">RELATED LINKS</span></span>
